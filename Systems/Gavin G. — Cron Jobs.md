---
title: Gavin G. — Cron Jobs
tags:
  - system
  - gavin
  - automation
last-updated: 2026-03-24
---

# Gavin G. — Cron Jobs

> Scheduled tasks Gavin runs automatically. Stored here for reference.
> Jobs are configured in Claude Code settings — this note is the human-readable record.

---

## Active Cron Jobs

| Job | Schedule | Trigger ID | Status |
|-----|----------|-----------|--------|
| Morning Brief | Weekdays 8am PDT | `trig_01PTGYddMSdDTAUemhSigqJi` | ✅ Live |
| Close of Day | Weekdays 6pm PDT | `trig_01M5iXfbDyyz9fEXKfm7qAs6` | ✅ Live |
| Weekly Drift Check | Mondays 9am PDT | `trig_01DGv2WWi1Mg8ZBEfyzXJvhT` | ✅ Live |
| Weekly Ideas | Fridays 4pm PDT | — | ❌ Plan limit (3 max) |

> [!note] Plan Limit
> Current Claude plan allows 3 scheduled jobs. Upgrade to add Weekly Ideas, or swap one of the above.

---

## Project-Linked Jobs

*As you build client projects, add a row here linking the job to its project note.*

| Job | Schedule | Command | Project |
|-----|----------|---------|---------|
| | | | |

---

## How to Add a New Cron Job

1. Open terminal in `Desktop/my brain`
2. Tell Gavin: *"Schedule [task] every [time]"*
3. Gavin sets it up in Claude Code
4. Add a row to this note with the details
5. Link to the relevant project note in the Project column

---

## Project Folders

*Add links here as you build them out.*

- [[Projects/_Project Template]] ← template for new projects
-

---

## Notes

- Cron output lands in the Claude Code terminal — open it to read Gavin's output
- Jobs run as remote agents, independent of whether terminal is open
- To cancel a job: tell Gavin *"Cancel the [job name] cron"*

---

*Managed by [[CLAUDE]] · Part of [[Systems Overview]]*
