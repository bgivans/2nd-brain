# Functions Reference

## Global Functions

| Function | Signature | Description |
|----------|-----------|-------------|
| `date()` | `date(string): date` | Parse string to date (`YYYY-MM-DD HH:mm:ss`) |
| `duration()` | `duration(string): duration` | Parse duration string |
| `now()` | `now(): date` | Current date and time |
| `today()` | `today(): date` | Current date (time = 00:00:00) |
| `if()` | `if(condition, trueResult, falseResult?)` | Conditional |
| `min()` | `min(n1, n2, ...): number` | Smallest number |
| `max()` | `max(n1, n2, ...): number` | Largest number |
| `link()` | `link(path, display?): Link` | Create a link |
| `file()` | `file(path): file` | Get file object |
| `image()` | `image(path): image` | Create image for rendering |
| `icon()` | `icon(name): icon` | Lucide icon by name |
| `html()` | `html(string): html` | Render as HTML |

## Duration Type

When subtracting two dates, the result is a **Duration** type (not a number).

**Duration Fields:** `.days`, `.hours`, `.minutes`, `.seconds`, `.milliseconds`

Duration does NOT support `.round()` directly — access a numeric field first.

```yaml
# CORRECT
"(date(due_date) - today()).days.round(0)"
# WRONG
"(now() - file.ctime).round(0)"
```

## Date Functions

**Fields:** `date.year`, `date.month`, `date.day`, `date.hour`, `date.minute`

| Function | Description |
|----------|-------------|
| `date.format(string)` | Format with Moment.js pattern |
| `date.relative()` | Human-readable relative time |

## String Functions

| Function | Description |
|----------|-------------|
| `contains(value)` | Check substring |
| `startsWith(query)` | Starts with query |
| `lower()` | To lowercase |
| `title()` | To Title Case |
| `trim()` | Remove whitespace |
| `replace(pattern, replacement)` | Replace pattern |
| `split(separator)` | Split to list |
| `slice(start, end?)` | Substring |

## Number Functions

| Function | Description |
|----------|-------------|
| `abs()` | Absolute value |
| `ceil()` | Round up |
| `floor()` | Round down |
| `round(digits?)` | Round to digits |
| `toFixed(precision)` | Fixed-point notation string |

## List Functions

| Function | Description |
|----------|-------------|
| `contains(value)` | Element exists |
| `filter(expression)` | Filter by condition |
| `map(expression)` | Transform elements |
| `join(separator)` | Join to string |
| `sort()` | Sort ascending |
| `unique()` | Remove duplicates |
| `flat()` | Flatten nested lists |

## File Functions

| Function | Description |
|----------|-------------|
| `asLink(display?)` | Convert to link |
| `hasTag(...tags)` | Has any of the tags |
| `hasLink(otherFile)` | Has link to file |
| `hasProperty(name)` | Has property |
| `inFolder(folder)` | In folder or subfolder |
