---
date: 2026-03-29
session-type: strategy
status: active
client: internal
project: Human Logic - AI Satire Video Generator
tags: #project #contenttools #ai #satire #videogeneration #reels #tiktok #canva #react #buildsession
ai-summary: Built a browser-based React app that generates "Human logic" meme-format short videos using Claude API for ideation and Pexels/Pixabay for clips, with Canva export pipeline.
related: [[Workflows/Vault Capture Workflow]]
---

# Human Logic: AI Satire Video Generator

## What We Built
A browser-based React app that generates viral "Human logic" meme-format short videos with an AI satire angle. Full pipeline from concept to Canva-ready export.

---

## The Idea
Inspired by the "Human logic" meme format — 4-step image sequence with arrows, dry deadpan captions, ironic punchline. Repurposed as a content engine satirizing human inefficiency, generational decline, and AI fear.

**Core marketing insight:** The topic of AI is hot, the format is proven, and there's a clean opportunity for seamless ad integration (a branded step inside the sequence that doesn't read as an ad).

---

## Final Spec

| Layer | Decision |
|---|---|
| Platform | Browser app — no install |
| Format | Vertical 9:16 (Reels / TikTok) |
| Layout | Side-by-side 2-column grid (exact meme format) |
| Ideation | Claude API — batch of 5–10 concepts |
| Steps per video | 4 (expandable to 4–10 in v2) |
| Clip sources | Pexels → Pixabay → Coverr → User upload |
| Editing | Canva template link + ZIP download |
| Memory | Saves batches to localStorage between sessions |
| Language | English |
| Ad integration | Skipped for v1 |

---

## Themes Claude Riffs On
- AI replacing human jobs
- Humans fearing AI they created
- AI used for embarrassingly trivial things
- Everyday people vs AI tools
- Generational decline (great-grandparents built civilizations → grandkid plays Fortnite in basement at 35)
- Humans working 40 years so the next generation can do nothing with it

**Tone:** Dry, deadpan. No exclamation marks. Just cold facts laid out in sequence. Nature documentary narrator who has given up on humanity.

---

## How the App Works

### 4 Screens
1. **Settings** — Enter Anthropic + Pexels + Pixabay keys (stored locally, never sent anywhere else)
2. **Ideate** — Generate batch of 5–10 concepts, expand cards to preview steps, pick favorites
3. **Clips** — Per step: top 3 results from source chain, pick one or upload your own
4. **Export** — Download step-1.mp4 → step-4.mp4 + open pre-built Canva 9:16 template

### Clip Source Chain (auto-fallback)
Pexels → Pixabay → Coverr (no key needed) → User upload

---

## To Get Running

- [ ] Get Anthropic API key — console.anthropic.com
- [ ] Get free Pexels key — pexels.com/api
- [ ] Get free Pixabay key — pixabay.com/api/docs (optional)
- [ ] Build Canva 9:16 template with 2-col grid + white arrows + "Human logic" title
- [ ] Paste Canva share URL into line 29 of `ai-satire-generator.jsx`
- [ ] Deploy to Netlify or Vercel (needed to whitelist domain for Pexels CORS)

---

## V2 Upgrade Path
Canva Connect API is stubbed at the top of the file — clearly commented. When volume increases, swap `window.open(CANVA_TEMPLATE_URL)` for `createCanvaDesign(concept, clips, canvaApiKey)` and the grid auto-populates. No manual drag & drop.

---

## File
`ai-satire-generator.jsx` — single React file, self-contained, no build step needed beyond a JSX renderer.

---

## Session Log

### 2026-03-29 — Initial Build
Full app spec locked. Single-file React implementation. Canva Connect API stubbed for v2. Ad integration deferred.
