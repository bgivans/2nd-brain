---
date: 2026-03-29
status: active
client: internal
project: MoonPay Agents — Research Log
tags: #moonpay #agents #crypto #research #trading #automation
ai-summary: Running log of MoonPay Agents research, test results, and system iterations. Phase one goal: agent self-funding (pays for Claude Pro, APIs, tools). Productize if the system works at small scale.
related: [[Logs/Log — 2026-03-29 — Agent Wallet Infrastructure]] [[Ideas/Agent Self-Funding Model]] [[Projects/Internal Tools — Overview]]
---

# MoonPay Agents — Research Log

> Test → Log → Analyze → Improve → Repeat.
> The compounding loop is the asset. Not the first $100.

---

## Phase One Parameters

**Capital:** $100–200 (tuition, not investment)
**Timeline:** 30–60 days
**Success metric:** Agent self-funds its operating costs (Claude Pro, APIs, tools)
**Failure condition:** Capital goes to zero with no learnings — still fine, treat as research cost

**What this is NOT:**
- A business plan
- A pitch to clients (yet)
- Serious capital deployment

---

## Setup Checklist

- [ ] Create MoonPay account
- [ ] Set up non-custodial wallet (agent-specific — not linked to personal bank)
- [ ] Decide: which chain, which asset, which strategy for first test
- [ ] Research OpenClaw — understand what it does that Claude doesn't natively
- [ ] Define the minimum Claude-native trading agent architecture (MCP + MoonPay?)
- [ ] Check compliance/legal on setting this up for clients (flag before productizing)

---

## Test Log

<!-- Add entries as tests run — format: date, setup, result, what changed -->

### Template
```
**Date:** YYYY-MM-DD
**Setup:** [what was configured]
**Action:** [what the agent did]
**Result:** [outcome, P&L, observations]
**Change for next run:** [one thing adjusted]
```

---

## Learnings

<!-- Running list of non-obvious things discovered — update as tests run -->

---

## Productization Trigger

If after 30–60 days the system shows real (not survivorship bias) results at small scale:
- Define the client offer
- Likely first clients: Javier, Ellie, Cisco, crypto-adjacent future clients
- Build the setup as a service (agent wallet + trading system install)

---

## Origin
[[Logs/Log — 2026-03-29 — Agent Wallet Infrastructure]]
