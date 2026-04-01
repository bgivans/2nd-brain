# Lovable → Claude Code Pipeline

> The standard process for taking a Lovable prototype and turning it into production-ready code.

---

## When to Use This

Any time a Lovable prototype is worth developing further — for a client, for a real product, or for your own tools.

---

## The Pipeline

### Step 1 — Capture the idea in Obsidian
Before opening Lovable, write a brief note:
- What are you building and for whom?
- What's the goal / what does success look like?
- Any constraints (stack, timeline, design direction)?

### Step 2 — Build the prototype in Lovable
- Generate the rough layout, UI, or flow
- Iterate quickly — don't overthink it at this stage
- Screenshot or export anything worth preserving

### Step 3 — Review and document in Obsidian
Open the project note and add a **Prototype Review** section:

```
## Prototype Review — [date]

**What works:**
-

**What needs to change:**
-

**What to scrap:**
-

**Claude Code brief:**
-
```

Be honest. If most of it is wrong, say so. The point is to extract what's useful.

### Step 4 — Claude Code session
Open Claude Code and paste:
1. The project goal (from Step 1)
2. The prototype review (from Step 3)
3. Any exported code or screenshots from Lovable

Let Claude Code take it from there — refactoring, rebuilding, or extending as needed.

### Step 5 — Log decisions back to Obsidian
After the session, update the project note:
- What was built
- Key decisions made and why
- What's next
- Any open questions

---

## Common Scenarios

### Scenario A: Keep the structure, improve the code
Lovable got the layout right but the code is messy.
→ Export the Lovable code, paste it in Claude Code, ask for a clean refactor.

### Scenario B: Keep the idea, rebuild from scratch
The prototype showed you what you want but the code isn't worth saving.
→ Use screenshots as reference, build fresh in Claude Code.

### Scenario C: The prototype revealed the idea was wrong
The prototype showed the concept doesn't work as imagined.
→ Log the learning in Obsidian. Rethink the brief. Repeat from Step 1.

---

## Related

- [[Systems Overview]]
- [[Lovable — Prototype Layer]]
- [[Claude Code — Production Layer]]
