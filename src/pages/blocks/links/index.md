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
[Column Block](../column/index.md)    # Go up one level
[Tab Block](column/index.md)          # Same directory
```

**Absolute**: Start from `src/pages/` with `/`
```markdown
[Column Block](/blocks/column/index.md)
```

## Path Resolution

| From | To | Relative | Absolute |
| --- | --- | --- | --- |
| `blocks/links/index.md` | `blocks/column/index.md` | `../column/index.md` | `/blocks/column/index.md` |
| `blocks/index.md` | `blocks/column/index.md` | `column/index.md` | `/blocks/column/index.md` |
| `blocks/column/index.md` | `index.md` (root) | `../../index.md` | `/index.md` |

## External Links

```markdown
[External Site](https://example.com)
```
