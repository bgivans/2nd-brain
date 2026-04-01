---
title: SD Probate Case Extraction
tags:
  - project
  - completed
  - automation
  - script
status: Complete
started: 2026-03-24
last_updated: 2026-03-24
---

# Project — SD Probate Case Extraction

> Automated scraper for extracting probate case data from the San Diego Superior Court public portal.

**Status:** `Complete`
**Started:** 2026-03-24
**Last updated:** 2026-03-24

---

## Goal

Automate extraction of probate case records (case numbers, parties, filing dates, ROA details) from the San Diego court CIS Public portal into structured CSV output — removing the need for manual lookups.

---

## Context

- **Who is this for?** Bryce / internal automation
- **What problem does it solve?** Manual probate case research is slow. Script automates search, drill-down, and data extraction by date range.
- **Stack:** Python + Playwright (headless Chromium)

---

## Current State

- [x] Script built and delivered
- [x] Adaptive CSS selectors with fallbacks (handles portal changes)
- [x] Rate limiting (randomized 1.5–3.5s delays between actions)
- [x] Crash resilience (CSV written after each date — no lost data)
- [x] Multi-date support (single date or date range)
- [x] PDF download support (skips paywalled docs automatically)
- [x] `--diagnose` / `--no-headless` debug mode

---

## Script Features

| Feature | Detail |
|---------|--------|
| Input | `--date YYYY-MM-DD` or `--start / --end` for range |
| Output | CSV with case number, parties, dates, ROA, notes |
| Selector strategy | 5–6 CSS fallback selectors per form element |
| Rate limiting | 1.5–3.5s between actions, 3–6s between dates |
| PDF handling | Downloads free docs; skips + logs paywalled links |
| Debug mode | `--diagnose --no-headless` dumps all form elements |

---

## Setup (one-time)

```bash
pip install playwright
playwright install chromium
```

## Usage

```bash
# Single date
python sd_probate_scraper.py --date 2026-03-10

# Date range with PDF downloads
python sd_probate_scraper.py --start 2026-03-01 --end 2026-03-15 --download-pdfs

# Table only (skip ROA drill-down)
python sd_probate_scraper.py --date 2026-03-10 --no-roa

# Debug: visible browser + diagnostics
python sd_probate_scraper.py --diagnose --no-headless
```

---

## Session Logs

### 2026-03-24 — Script built and delivered

**Goal for this session:**
Build a robust, crash-resilient scraper for the SD Superior Court probate portal.

**What was built / decided:**
- Full Python/Playwright script with adaptive selectors, rate limiting, and CSV output
- `--diagnose` mode added for first-run selector verification
- Paywalled PDF detection built in

**Key decisions and why:**
- Adaptive `SelectorStrategy` class used so portal UI reshuffles don't break the script
- CSV written per-date (not at end) so partial runs aren't lost

**What's next:**
- Optional: add OCR pipeline for purchased petition PDFs if address/deceased date data is needed

---

## Open Questions

- Is a paid PDF OCR pipeline worth building for `deceased_date` and `address_at_death` fields?

---

## Decisions Made

| Decision | Why | Date |
|----------|-----|------|
| Playwright over requests/BS4 | Portal requires JS rendering | 2026-03-24 |
| Randomized delays | Avoid bot detection / rate limiting | 2026-03-24 |
| Per-date CSV writes | Crash resilience — no lost progress | 2026-03-24 |

---

## Related

- [[Systems Overview]]
