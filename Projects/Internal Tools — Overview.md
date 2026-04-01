---
date: 2026-03-29
status: active
tags: #internal #tools #portfolio #build-log
ai-summary: Running index of internal tools and apps built by Bryce — concepts, v1 builds, and shipped products that aren't client work.
---

# Internal Tools — Overview

> Tools built for Givans Global operations, content strategy, or personal use.
> Not client work. Not commissioned. Built because the need existed or the idea had legs.

---

## Active Builds

### [[Human Logic - AI Satire Video Generator]]
**Status:** v1 complete — not published
**What it is:** Browser-based React app. Generates "Human logic" meme-format short videos using Claude API for ideation + Pexels/Pixabay for clips. Canva export pipeline. Vertical 9:16 for Reels/TikTok.
**File:** `ai-satire-generator.jsx`
**Next:** Deploy to Netlify/Vercel, build Canva template, test end-to-end

---

### [[INTEL — Competitor Content Analyzer]]
**Status:** Build #1 complete — not published
**What it is:** Browser-based HTML tool that replicates Blort AI ($97/mo) for ~$0.003/analysis. Claude API + yt-dlp + Whisper. 6 tactic modules — hook stealing, frame-by-frame, comment mining, inspiration rewrite.
**File:** `competitor-analyzer app.html`
**Next:** Build #2 — swipe file, batch mode, niche profile, viral velocity calculator

---

## Concepts (Built but Not Pitched)

### [[Logs/Log — 2026-03-29 — GG ROI Tracker]]
**Status:** v1 concept — not presented to clients
**What it is:** Supabase-backed single-file HTML dashboard. Tracks lead sources, ad spend, labor costs, commissions owed. Scoped to Ellie (C2C Legal) and Javier (Unlock Your Property) as potential clients.
**Files:** `gg-roi-tracker-v2.html` + `gg_schema_v2.sql`
**Next:** Present to Ellie after current deliverables close. Fork for Javier if she moves on it.

---

### [[GG Network]]
**Status:** Build #1 complete — used live at networking event same day
**What it is:** Mobile-first contact logger for networking events. Black-and-gold GG branded, voice input. Claude API processes each contact — returns pain points, opportunity flags, follow-up timing, copy-paste outreach draft.
**Next:** Build #2 — event tagging, priority flags, email export, filter/search

---

### [[GG Command Center]] ← Primary Tool
**Status:** Build #1 complete — on Desktop, ready to use
**What it is:** Local desktop app (HTML → Chrome shortcut). Sidebar navigation, full KPI dashboard, daily note writer with vault save, /drift + /schedule + Research automations, vault browser. Requires Obsidian Local REST API plugin.
**File:** `C:\Users\givan\Desktop\gg-command-center.html`
**Build #2:** CRM Kanban, Send Proposal, Pitch Retainer, Resend email automations

---

## Future / Parked

<!-- Add ideas that haven't been built yet -->

---

## Notes
- All tools are single-file or minimal-dependency by design — fast to ship, easy to fork
- Client-facing tools get moved to `Projects/[Client Name]` once adopted
