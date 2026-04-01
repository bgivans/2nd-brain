---
name: obsidian-cli
description: Interact with Obsidian vaults using the Obsidian CLI to read, create, search, and manage notes, tasks, properties, and more. Use when the user asks to interact with their Obsidian vault, manage notes, search vault content, or perform vault operations from the command line.
---

# Obsidian CLI

Use the `obsidian` CLI to interact with a running Obsidian instance. Requires Obsidian to be open.

## Syntax

Parameters take a value with `=`. Quote values with spaces:

```bash
obsidian create name="My Note" content="Hello world"
```

File targeting:
- `file=<name>` — resolves like a wikilink
- `path=<path>` — exact path from vault root

## Common Commands

```bash
obsidian read file="My Note"
obsidian create name="New Note" content="# Hello" silent
obsidian append file="My Note" content="New line"
obsidian search query="search term" limit=10
obsidian daily:read
obsidian daily:append content="- [ ] New task"
obsidian property:set name="status" value="done" file="My Note"
obsidian tasks daily todo
obsidian tags sort=count counts
obsidian backlinks file="My Note"
```

Use `--copy` to copy output to clipboard. Use `silent` to prevent files from opening.

Full docs: https://help.obsidian.md/cli
