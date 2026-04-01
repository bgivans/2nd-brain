---
name: json-canvas
description: Create and edit JSON Canvas files (.canvas) with nodes, edges, groups, and connections. Use when working with .canvas files, creating visual canvases, mind maps, flowcharts, or when the user mentions Canvas files in Obsidian.
---

# JSON Canvas Skill

## File Structure

```json
{
  "nodes": [],
  "edges": []
}
```

## Node Types

| Type | Required fields |
|------|----------------|
| `text` | `text` (Markdown string) |
| `file` | `file` (vault path) |
| `link` | `url` |
| `group` | optional `label` |

All nodes require: `id` (16-char hex), `type`, `x`, `y`, `width`, `height`

## Edges

```json
{
  "id": "0123456789abcdef",
  "fromNode": "6f0ad84f44ce9c17",
  "fromSide": "right",
  "toNode": "a1b2c3d4e5f67890",
  "toSide": "left",
  "toEnd": "arrow",
  "label": "leads to"
}
```

`fromSide`/`toSide`: `top`, `right`, `bottom`, `left`
`fromEnd`/`toEnd`: `none`, `arrow`

## Colors

Preset: `"1"` Red, `"2"` Orange, `"3"` Yellow, `"4"` Green, `"5"` Cyan, `"6"` Purple. Or hex `"#FF0000"`.

## Layout

- x increases right, y increases down
- Space nodes 50-100px apart
- Use `\n` for newlines in text nodes (not `\\n`)

## Validation

- All `id` values unique
- Every `fromNode`/`toNode` references existing node
- Required fields present per type

## References

- [JSON Canvas Spec 1.0](https://jsoncanvas.org/spec/1.0/)
