---
date: 2026-03-29
session-type: strategy
status: idea
client: internal
project: GG Marketing ROI Tracker
tags: #build #system #client-work #marketing #roi #supabase
ai-summary: Concept and v1 build of a Marketing ROI Tracker — Supabase-backed single-file HTML dashboard. Scoped to Ellie and Javier as potential clients but not presented to either. Self-initiated idea, not a commissioned project.
related: [[Projects/Ellie - C2C Legal]] [[Projects/Javier - Unlock Your Property]] [[GG_Build_System]]
---

# GG Marketing ROI Tracker — Build Session

## What This Was

Self-initiated concept — not commissioned, not presented to either client yet. Built v1 independently as a proof of concept to potentially pitch to Ellie and Javier.

The idea: one clean dashboard per client that tracks where leads come from, what they cost, what they convert at, and who gets paid — without double-entry into existing tools (GHL, Trello). Ellie scoped as the first template instance, Javier queued if she moves on it.

---

## Architecture Decisions

| Decision | Choice | Why |
|---|---|---|
| Backend | Supabase | Already on the stack. Separate project per client. |
| Frontend | Single-file HTML artifact | Fastest to ship, easiest to fork per client |
| Visual tone | Instrument Serif + DM Sans | Light, client-facing — not a dev tool |
| Auth | Supabase email login | Simple, secure, no third-party dependency |
| Roles | Admin (Bryce) / Viewer (Ellie/Javier) | Ellie texts Bryce to add campaigns or managers — no self-serve admin |
| Commission | Flat $ per closed deal, per campaign manager | Eliminates multi-touch disputes |
| Revenue tracking | Collected only — never projected | Keeps ROI math honest, especially for real estate |
| Channel attribution | First-touch source on every lead | Separate from the closing campaign — fixes the attribution blind spot |
| Integrations | GHL webhook (Javier) + Trello webhook (Ellie) | Fires on deal close / card move. Manual collection confirmation required |

---

## Screens Built

1. **Login** — Supabase auth, email/password
2. **Dashboard** — 5 KPI cards, spend vs revenue chart, date filter (All Time / This Month / Custom), stale webhook alert
3. **Channel Comparison** — Side-by-side ROI cards, sorted by ROI % descending
4. **Commission Owed** — Per manager: campaign, deals closed, revenue, rate, total owed (collected only, pending flagged)
5. **Log a Lead** — 3-step mobile wizard, first-touch source required on step 1
6. **Log Sign Deployment** — Ellie-specific, employee + city + date + hours + rate → auto-calculates labor cost
7. **Campaigns** — Admin only, create campaigns with channel + manager + ad spend
8. **Campaign Managers** — Admin only, set flat commission rate (locks permanently once a conversion is recorded)

---

## Key Insights From Research

- **First-touch source at intake or it's gone forever** — if John puts up a sign and the lead Googles a week later, Google gets the credit unless you capture source at intake
- **Labor cost is the hidden ROI killer** — almost nobody tracks hours. Ellie's "cheap" sign channel might be her most expensive per conversion once labor is counted
- **60-second logging rule** — if the form takes longer than 60 seconds, field workers stop using it within 3 weeks. Wizard form, pre-filled dropdowns, defaults to today
- **Flat rate per campaign owner** — eliminates commission disputes. No percentages, no multi-touch arguments. John owns signs, Bryce owns Nextdoor, done
- **Webhooks go stale silently** — 6 weeks of bad data before anyone notices. Added last-sync timestamp in sidebar + yellow/red banner at 7/14 days
- **Collected vs projected revenue** — real estate deals collapse after contract. ROI math is fictional until money is in hand

---

## Bugs Found and Fixed (3 Audit Rounds)

### v1 → v2
- `profiles` and `webhook_log` tables missing from schema entirely
- Schema used UUID foreign keys for channels; HTML used plain text — inserts would fail on go-live
- No update flow for leads already in `closed_pending` — couldn't mark as collected after the fact
- Employee and city dropdowns were hardcoded HTML, not DB-driven
- Commission rate lock was display-only, not enforced at the database level

### v2 Red Fixes
- **Apostrophe injection** — `onclick="openModal('${l.name}')"` breaks on O'Brien, D'Angelo, etc. Fixed with `data-action` / `data-id` event delegation + `escHtml()` utility
- **Custom date range invisible** — `.hidden { display:none!important }` fought `display:flex` on the date inputs div. Fixed with direct `style.display` control
- **Campaign total cost wrong** — null `ad_spend` from Supabase was corrupting totals. Fixed with `isNaN` guards on both `ad_spend` and `labor_cost`
- **`collected_date` trigger missed inserts** — trigger only fired on `UPDATE`. If a lead was logged as Collected on first entry, date never set. Fixed to fire on `INSERT OR UPDATE`

---

## Files Delivered

- `gg-roi-tracker-v2.html` — full working dashboard, demo mode pre-loaded with sample data, swap 2 lines to go live
- `gg_schema_v2.sql` — paste into Supabase SQL editor. Includes: profiles, campaigns, leads, sign_deployments, campaign_managers, employees, locations, webhook_log, RLS policies, triggers, views

**Local copies:** `C:\Users\givan\Downloads\files\`

---

## Go-Live Checklist (Ellie)

- [ ] Run `gg_schema_v2.sql` in Supabase SQL editor
- [ ] Create Bryce + Ellie in Supabase Auth → Users
- [ ] Run: `update profiles set role = 'admin' where email = 'bryce@givansglobal.com';`
- [ ] Swap `SUPABASE_URL` and `SUPABASE_ANON_KEY` at top of HTML file
- [ ] Test login as both roles (admin + viewer)
- [ ] Add real employees and locations via Admin screens

---

## Open Loops

- [ ] Javier's instance — fork Ellie template, swap channels (no sign deployment screen), adjust commission structure
- [ ] Supabase Edge Functions for GHL + Trello webhooks (v2)
- [ ] Mobile action button layout polish — stacks awkwardly on small screens
- [ ] Commission rate edit UI guard in admin panel (currently DB-enforced but no UI message)
- [ ] Push notification for stale webhook (v2)

---

## Financial Context

Ellie — $800 paid. Retainer pitch ($200–300/mo) after deliverables are closed.
Javier — Commission deal pending. This tracker becomes the source of truth for what Bryce is owed once live.
Both clients are in the Oceanside office.
