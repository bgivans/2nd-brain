---
name: obsidian-bases
description: Create and edit Obsidian Bases (.base files) with views, filters, formulas, and summaries. Use when working with .base files, creating database-like views of notes, or when the user mentions Bases, table views, card views, filters, or formulas in Obsidian.
---

# Obsidian Bases Skill

## Workflow

1. **Create the file**: Create a `.base` file in the vault with valid YAML content
2. **Define scope**: Add `filters` to select which notes appear (by tag, folder, property, or date)
3. **Add formulas** (optional): Define computed properties in the `formulas` section
4. **Configure views**: Add one or more views (`table`, `cards`, `list`, or `map`) with `order` specifying which properties to display
5. **Validate**: Verify the file is valid YAML with no syntax errors

## Schema

```yaml
filters:
  and: []
  or: []
  not: []

formulas:
  formula_name: 'expression'

properties:
  property_name:
    displayName: "Display Name"

summaries:
  custom_summary_name: 'values.mean().round(3)'

views:
  - type: table | cards | list | map
    name: "View Name"
    limit: 10
    groupBy:
      property: property_name
      direction: ASC | DESC
    filters:
      and: []
    order:
      - file.name
      - property_name
      - formula.formula_name
    summaries:
      property_name: Average
```

## Filter Syntax

```yaml
# Single filter
filters: 'status == "done"'

# AND
filters:
  and:
    - 'status == "done"'
    - 'priority > 3'

# OR
filters:
  or:
    - 'file.hasTag("book")'
    - 'file.hasTag("article")'

# NOT
filters:
  not:
    - 'file.hasTag("archived")'
```

## File Properties Reference

| Property | Type | Description |
|----------|------|-------------|
| `file.name` | String | File name |
| `file.path` | String | Full path to file |
| `file.folder` | String | Parent folder path |
| `file.size` | Number | File size in bytes |
| `file.ctime` | Date | Created time |
| `file.mtime` | Date | Modified time |
| `file.tags` | List | All tags in file |
| `file.links` | List | Internal links in file |

## Formula Syntax

```yaml
formulas:
  days_until_due: 'if(due_date, (date(due_date) - today()).days, "")'
  is_overdue: 'if(due, date(due) < today() && status != "done", false)'
  status_icon: 'if(done, "✅", "⏳")'
  days_old: '(now() - file.ctime).days'
```

**Duration pitfall:** Date subtraction returns a Duration. Access `.days`, `.hours`, etc. before calling `.round()`.

```yaml
# CORRECT
"(date(due_date) - today()).days.round(0)"
# WRONG
"((date(due) - today()) / 86400000).round(0)"
```

## References

- [Bases Syntax](https://help.obsidian.md/bases/syntax)
- [Functions Reference](references/FUNCTIONS_REFERENCE.md)
