---
date: 2026-03-29
status: active
tags: #ops #obsidian #workflow #system
ai-summary: Two-layer capture system — Apple Notes for mobile capture, Obsidian for synthesis. Weekly batch transfer with AI export skill for session notes.
related: [[Systems/Obsidian — Brain Layer]] [[GG_Build_System]]
---

# Vault Capture Workflow

> Two layers. Never conflate them.
> **Apple Notes = capture.** Obsidian = synthesis.

---

## Layer 1 — Mobile Capture (Apple Notes)

Use Apple Notes for everything on mobile. No friction, no setup, already open.

**What to capture:**
- Thoughts on active projects
- Client notes mid-conversation
- Ideas while watching / reading / walking
- Quick logs of what happened that day

**Rules:**
- Don't try to structure it — just get it out
- One note per day is fine. Multiple is fine too.
- Label by date or topic loosely so weekly transfer is easy

---

## Layer 2 — Weekly Batch Transfer (Desktop, Sundays)

Every Sunday: open Apple Notes, open Obsidian, transfer.

**Transfer process:**
1. Read through the week's Apple Notes
2. Create the daily note for each day that has content (`Daily Notes/YYYY-MM-DD.md`)
3. For anything that references a client or project — open that project note and append
4. For anything that looks like a belief, idea, or system decision — route to the right folder
5. Delete or archive Apple Notes after transfer

**Routing guide:**

| What it is | Where it goes |
|------------|--------------|
| Project update / client note | `Projects/[Client Name].md` |
| System or workflow decision | `Systems/` or `Workflows/` |
| Raw idea, half-formed | `Ideas/` |
| Belief or principle | `Beliefs/` |
| Meeting or conversation | `Meetings/` |
| General daily log | `Daily Notes/YYYY-MM-DD.md` |

---

## Layer 3 — Session Export (Claude Brainstorms)

At the end of any meaningful Claude session, use the `obsidian-export` skill.

**Trigger phrases:** "export this", "save this session", "end of session", "add this to my vault"

**What it produces:**
- A structured session note (Strategy / Debrief / Idea Dump template)
- Vault Update Suggestions — inferred, not instructions
- Copy-paste ready for Apple Notes or direct vault paste

**Where it lands:**
- Session note → `Daily Notes/YYYY-MM-DD.md`
- New standalone notes → relevant folder per content type

---

## Discipline Dependency

The skill and the structure don't matter if the weekly transfer doesn't happen.
Sunday is the anchor. Miss it once, catch up. Miss it twice, the system breaks.

---

## Related

- [[Systems/Obsidian — Brain Layer]]
- [[Daily Notes/2026-03-29]] ← decision log for this system
