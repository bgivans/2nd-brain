---
date: 2026-03-29
session-type: strategy
status: active
client: internal
project: INTEL — Competitor Content Analyzer
tags: #concept #build #tool #ai-tools #content-strategy #competitor-analysis #claude-api #no-code
ai-summary: Browser-based competitor content analysis tool that replicates Blort AI ($97/mo) using Claude API + yt-dlp + Whisper for ~$0.003/analysis. Build #1 complete — single HTML file, no backend, no hosting.
related: [[Projects/Human Logic - AI Satire Video Generator]]
---

# INTEL — Competitor Content Analyzer

## The Concept

A free, browser-based competitor content analysis tool that replicates the core functionality of **Blort AI** ($97/mo) using:
- Claude API (~$0.003/analysis)
- yt-dlp (free, open source)
- OpenAI Whisper (free, local)
- Zero backend, zero hosting

The insight: Blort charges for the wrapper. The intelligence is just Claude + a transcript. Build the wrapper yourself.

---

## Use Case

**Primary:** Analyze competitor social media content on Instagram, TikTok, and YouTube — extract hooks, structures, CTAs — and adapt them for your own product. Without paying for expensive tools.

**Who it's for:** Creators and marketers who move fast and want an unfair advantage on content strategy.

---

## Build #1 — What Was Built

Single HTML file (`competitor-analyzer.html`) that runs entirely in the browser.

**Local file:** `C:\Users\givan\Downloads\competitor-analyzer app.html`

### Architecture
- **Input:** Paste a URL or raw transcript into the left panel
- **Extraction:** For URLs → generates yt-dlp + Whisper terminal commands to pull transcript locally
- **Analysis:** Claude Sonnet API processes the transcript with a content strategist system prompt
- **Chat:** Full conversation interface with the transcript baked into every message as context
- **API Key:** User's own Anthropic key, stored in-browser only — never transmitted anywhere else

### Stack
```
HTML / CSS / Vanilla JS   — zero dependencies, runs offline
Claude API (Sonnet)       — claude-sonnet-4-20250514, max_tokens: 1500
yt-dlp                    — local video download (pip install yt-dlp)
OpenAI Whisper            — local transcription (pip install openai-whisper)
```

---

## Features Shipped in Build #1

### Quick Prompt Bar
- Hook / Structure / CTA / Virality

### Tactics Bar (6 modules)

| Tactic | What It Does |
|---|---|
| ⚡ 3-Sec Hook Steal | Extracts opening hook, explains why it works, generates 5 variations for your niche tagged by emotion |
| 🎞 Frame-by-Frame | Maps every scene beat, purpose, and viewer emotion like a storyboard |
| 💬 Comment Mining | Simulates top comments, finds 3 audience themes, writes 30-sec scripts from each |
| ⬇ yt-dlp Pipeline | Generates copy-paste terminal commands to transcribe any public video for $0 |
| 👁 #2 Creator Clone | Strategy to find the about-to-blow-up #2 in any niche and clone their format before saturation |
| ✍ Inspiration Rewrite | Rewrites loaded transcript for your product keeping identical sentence rhythm, structure, and emotional arc |

---

## Key Tactics From the Session

1. **3-Second Hook Steal** — Screenshot/transcribe only the first 3 seconds. Build a swipe file categorized by emotion (curiosity, fear, desire, controversy).
2. **Frame-by-Frame via Captions** — Turn on auto-captions, screenshot every scene change. Free storyboard of any competitor video.
3. **Comment Mining** — Sort by Top Comments on any viral post. The complaints and questions = your next 10 hooks. Paste into Claude → "turn these into hooks."
4. **yt-dlp + Whisper Pipeline** — Download any public video free, transcribe locally, paste into Claude. Total cost: $0.
5. **#2 Creator Clone** — Skip the biggest creator (too polished, too copied). Target the hungry #2 whose formats are popping but not yet saturated. Clone aggressively now.
6. **Sound + Format Decoupling** — Find trending audio, extract the format from top 5 videos using it, rebuild for your product.
7. **Viral Velocity Tracking** — Check view count at 2hrs, 24hrs, 72hrs. Still climbing at 72hrs = algorithm is pushing it. Clone immediately.
8. **Inspiration Rewrite** — Transcribe competitor video word for word → paste into Claude → "rewrite this script for [my product] keeping identical sentence rhythm, hook structure, and emotional arc."

---

## Cost Model

| Component | Cost |
|---|---|
| Claude API (per analysis) | ~$0.003 |
| yt-dlp | Free |
| Whisper (local) | Free |
| Hosting | $0 (runs in browser) |
| vs. Blort AI | $97/mo |

---

## Build #2 Ideas

- [ ] Swipe file — save and tag analyzed hooks/structures locally
- [ ] Batch URL mode — analyze 5+ videos and compare patterns
- [ ] Niche profile — save "my product" and "my audience" so tactics auto-populate
- [ ] Viral velocity calculator — paste view counts at different timestamps, get a verdict
- [ ] Export analyzed content as a formatted content brief
- [ ] Sound trend finder prompt built in
- [ ] Chrome extension wrapper

---

## Reference
- **Blort AI** (what this replaces): getblort.com
- **Instagram:** @getblortai

---

## Session Log

### 2026-03-29 — Build #1
Concept defined. Full single-file HTML build complete. 6 tactic modules shipped.
