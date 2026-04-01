# Systems Overview

> This is the master map of my three-tool stack. Start here.

---

## The Three Layers

| Layer | Tool | Role |
|-------|------|------|
| 🧠 Brain | [[Obsidian — Brain Layer]] | Thinking, notes, decisions, documentation |
| ⚡ Prototype | [[Lovable — Prototype Layer]] | Fast UI/UX drafts, rough flows, quick wins |
| 🏗️ Production | [[Claude Code — Production Layer]] | Real builds, refactors, complex systems |

---

## How Work Flows

```
Idea / Problem
     ↓
Obsidian — capture the idea, define the goal, outline the scope
     ↓
Lovable — generate a rough prototype (UI, flow, structure)
     ↓
Obsidian — review the prototype, document what's good, what needs changing
     ↓
Claude Code — harden, refactor, or rebuild to production quality
     ↓
Obsidian — document decisions, outcomes, lessons learned
```

See: [[Lovable → Claude Code Pipeline]] for the detailed handoff process.

---

## Core Principles

1. **Obsidian is always the source of truth.** If it's not in Obsidian, it doesn't exist as a decision.
2. **Lovable output is always a draft.** Nothing from Lovable ships without a Claude Code pass.
3. **Claude Code is for serious work.** Complex builds, production refactors, real client sites.
4. **Human-written vault.** I write everything. Claude reads and responds — it doesn't write into the vault unless asked.
5. **Context compounds.** Every session logged means every future session starts warm.

---

## Vault Structure

```
CLAUDE.md                    ← instructions for Claude Code
Systems Overview.md          ← you are here

Context/
  About Me.md                ← who I am (fill this in first)
  Active Work Ledger.md      ← live work state

Systems/                     ← how my tools work
Workflows/                   ← step-by-step processes
Projects/                    ← one note per project (use Project Template)
Daily Notes/                 ← daily log (YYYY-MM-DD)
People/                      ← notes on people I work with
Meetings/                    ← meeting notes
Beliefs/                     ← principles and mental models
Ideas/                       ← raw captures, process weekly
Reference/                   ← lookup notes
Templates/                   ← note templates
Logs/                        ← session and decision logs

.claude/
  skills/                    ← kepano/obsidian-skills installed
  commands/                  ← slash commands for Claude Code
```

---

## Slash Commands

Run these in Claude Code when working in this vault:

| Command | What it does |
|---------|-------------|
| `/context` | Load full life and work overview |
| `/today` | Generate a prioritized daily plan |
| `/close-day` | End-of-day review and next-day setup |
| `/ghost [question]` | Answer a question in my writing style |
| `/challenge [belief]` | Pressure-test a belief using my own writing |
| `/emerge` | Surface hidden patterns across notes |
| `/drift` | Compare stated priorities vs. actual focus |
| `/ideas` | Generate cross-domain ideas from vault context |
| `/trace [topic]` | Track how an idea has evolved over time |
| `/connect [A] [B]` | Bridge two unrelated domains |
| `/graduate [idea]` | Promote a raw idea to an active project |

---

## Active Projects

*Link active project notes here as you start them.*

-

---

## Related Notes

- [[Obsidian — Brain Layer]]
- [[Lovable — Prototype Layer]]
- [[Claude Code — Production Layer]]
- [[Lovable → Claude Code Pipeline]]
- [[Context/About Me]]
- [[Context/Active Work Ledger]]
- [[Gavin G. — Cron Jobs]]
