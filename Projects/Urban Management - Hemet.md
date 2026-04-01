---
title: Urban Management - Hemet
tags:
  - project
  - real-estate
  - hemet
  - urban-management
  - investment
status: researching
---

# Hemet Opportunity — Urban Management

> **Brainstorming context:** Market research and a drafted partnership proposal. Not a closed deal or confirmed strategy.

**Parent:** [[Projects/Urban Management]]
**What it is:** Hemet, CA identified as an emerging real estate market for off-market acquisition, ADU development, and distressed property outreach.

---

## Why Hemet

- Inland Empire market — lower entry cost vs. coastal SoCal
- Strong rental demand relative to purchase prices
- Growing school enrollment (positive population signal)
- Job search activity trending up (1-year Google Trends)
- Multi-unit properties bought 2007–2010 are now 80–100% paid off — motivated sellers
- 2010 price: ~$250K → 2025 price: ~$650K (property appreciation creates equity-rich sellers)

**Multi-unit revenue math (brainstormed):**
- 4-unit at $2,800/unit/month = $134,400/year gross
- 4-unit at $1,700/unit = $81,600/year gross
- At 2010 prices: paid off in 4.7 years from rental income
- At 2025 prices: still only 4.8 years to pay off

---

## Target Property Profile (Data Scraping Criteria)

- 80–100% paid off
- Underperforming rental income vs. surrounding area
- 15+ years of ownership (bought 2007–2010)
- Long-term tenants renting
- 2–6 units
- **Exclude:** Properties with an online payment portal / website (likely managed professionally)

---

## West Cal Builders Partnership Proposal

**Partner:** West Cal Builders (owns labor force — construction + renovation in-house)
**Urban Management's role:** Exclusive sourcing, evaluation, and marketing of deals
**Their edge:** Own labor = flexible risk tolerance + better margins on renovation

**Proposal summary:**
> Urban Management provides a pipeline of motivated sellers in the Inland Empire (as-is, bilingual outreach) to West Cal Builders. They evaluate and execute. We source and market.

**Objectives:**
1. Risk-controlled deal sourcing matched to West Cal's tolerance
2. Streamlined backend: Dialer + Guerilla Marketing + CRM + Google Sheets
3. Localized focus on Hemet zip codes
4. Bilingual outreach (English + Spanish)

**Budget:** $3,000 initial
**Past lead pull:** 34,000 leads at $310 (cost of list)

→ Full proposal PDF was in original Milanote

---

## Oside / North Valley RE Legal Campaign

A separate but related distressed property campaign targeting Oceanside / North Valley.

**Target list filters:**
- Owned 10+ years, 35%+ equity
- Non-owner-occupied (landlords)
- Probate / inheritance, divorce, NOD/pre-foreclosure, eviction
- Elderly owners (70+)
- Recently paid-off mortgage

**North Valley:** 1,804 doors identified for outreach

**3-mailer sequence:**
1. "You're Not Alone"
2. "You Don't Have to Sell Low"
3. "Turn Stress Into a Solution"

**Follow-up cadence:**
- SMS → Ringless VM → ISA phone call → 3-touch email
- Triggered 3 days after each mailer drop

**Consult flow:**
- Rapport → uncover motivations → present 2–3 paths (buy as-is, list, JV flip, ADU build) → action plan

**Compliance notes:**
- Bilingual printing (English + Spanish + Samoan for certain zip codes)
- UPL (unauthorized practice of law) compliance for legal service boundaries
- Opt-out / do-not-contact records maintained

---

## Probate Scraper (Bryce Built)

SD Superior Court probate filing scraper — autonomous data collector for probate leads.
- 17-column schema: case number, estate, deceased date, attorney, petitioner, property, confidence score
- Triggers: `run probate` (7-day scrape), `count probate` (dry run), `export csv`
- Outputs to Google Sheet + CSV fallback
- Confidence scoring (100 base, deductions for missing fields)

→ **Status:** Delivered 2026-03-24. See [[Context/Active Work Ledger]] — SD Probate Case Extraction.

---

## Related
- [[Projects/Urban Management]] — parent
- [[Projects/Javier - Unlock Your Property]] — primary deal team
- [[People/Raul Garcia - El Gato Studios]] — lending on deals
- [[Context/Active Work Ledger]] — probate scraper delivered
