---
tags:
  - dashboard
  - moc
---

# GG — Operations Dashboard

---

## Right Now
> Three things. That's it.

1. **Javier** — 15 site revisions. Close it.
2. **Ellie** — Instagram audit → funnel → 4 content pieces. Close it.
3. **Dad** — Finish binder. Deliver. Pitch maintenance.

→ [[Context/Active Work Ledger]] for full picture

---

## Open Tasks

```tasks
not done
path does not include Templates
path does not include Reference/Vault Coverage Map
limit 20
```

---

## Active Projects

```dataview
TABLE file.mtime AS "Last Updated"
FROM "Projects"
WHERE !contains(file.name, "Template")
SORT file.mtime DESC
```

---

## Recent Logs

```dataview
LIST
FROM "Logs"
WHERE file.name != "AION - Shelved" AND file.name != "INR Circle - Shelved"
SORT file.mtime DESC
LIMIT 10
```

---

## Ideas Inbox

```dataview
TABLE file.ctime AS "Captured"
FROM "Ideas"
SORT file.ctime DESC
LIMIT 8
```

---

## People — Active Clients

```dataview
TABLE file.mtime AS "Last Touch"
FROM "People"
SORT file.mtime DESC
LIMIT 8
```

---

## The Anchor

> "First say to yourself what you would be; and then do what you have to do."
> — Epictetus

*Swap this line for whatever you need right now.*

---

*→ [[Context/Active Work Ledger]] · [[Goals/Financial Goals]] · [[Beliefs/North Star]]*
