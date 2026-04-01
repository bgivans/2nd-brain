---
date: 2026-03-29
status: active
client: internal
project: GG Network
tags: #internal #tool #networking #build #mobile
ai-summary: Mobile-first contact logger for networking events. Black-and-gold GG branded, voice input, Claude API processes each contact and returns pain points, opportunity flags, follow-up timing, and copy-paste outreach draft.
related: [[Projects/Internal Tools — Overview]]
---

# GG Network — Networking Contact Logger

## Concept

Mobile-first, black-and-gold contact logging app for use *at* networking events. Designed to be discreet, fast, and GG-branded so it doesn't read as a data collection tool in the field.

Bryce logs the contact. **Gavin G.** processes it and returns structured intelligence: pain points, opportunity flags, follow-up timing, and a copy-paste outreach draft.

---

## Build #1 — What Was Built

- **Mobile-first HTML artifact** (black + GG gold `#F5C518`, Bebas Neue + DM Sans)
- **Voice input** via Web Speech API — speak naturally, fields auto-fill
- **Manual form** — Name, Company, Role, What They Do, Notes
- **AI processing** via Anthropic API (claude-sonnet-4) — generates:
  - Pain points
  - Opportunity for Givans Global
  - Follow-up action with timing
  - Draft outreach message (copy-paste ready)
- **Persistent contact storage** via `window.storage`
- **Contacts log** with color-coded tags (Pain Point / Opportunity / Follow-up)
- **Detail modal** with full Gavin analysis + one-tap copy of outreach draft
- **Toast notifications**, bottom nav, tab switching

---

## Build #2 Ideas

- [ ] Event tagging — log which event each contact came from
- [ ] Priority flag (🔥 Hot / Warm / Cold)
- [ ] Email export / AirDrop of contact card
- [ ] Filter/search contacts log
- [ ] Dave database scope-of-work outline

---

## Session Log

### 2026-03-29 — Build #1
Concept defined and built. First live use at networking event same day.
Contacts logged: [[People/Ben — Stealth Cybersecurity]] · [[People/Dave — Communication Consultant]]
