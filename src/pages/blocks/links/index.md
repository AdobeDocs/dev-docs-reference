---
title: Links
description: Learn how to create links between documentation pages using relative and absolute paths.
---

# Links

Link between pages using relative or absolute paths.

## Syntax

```markdown
[Link Text](path/to/page.md)
```

## Path Types

**Relative**: Based on current page location
```markdown
[Columns Block](../columns/index.md)    # Go up one level
[Tab Block](columns/index.md)          # Same directory
```

**Absolute**: Start from `src/pages/` with `/`
```markdown
[Columns Block](/blocks/columns/index.md)
```

## Path Resolution

| From | To | Relative | Absolute |
| --- | --- | --- | --- |
| `blocks/links/index.md` | `blocks/columns/index.md` | `../columns/index.md` | `/blocks/columns/index.md` |
| `blocks/index.md` | `blocks/columns/index.md` | `columns/index.md` | `/blocks/columns/index.md` |
| `blocks/columns/index.md` | `index.md` (root) | `../../index.md` | `/index.md` |

## External Links

```markdown
[External Site](https://example.com)
```
