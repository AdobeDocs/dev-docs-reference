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

**External**: Full URL to external sites
```markdown
[External Site](https://example.com)
```

## Link Requirements

**Internal links must end with `.md`**

All links within the content repo must point to a `.md` file:

```markdown
✅ [Accordion](/blocks/accordion/index.md)
❌ [Accordion](/blocks/accordion/)
```

## Anchor Links

To link to a specific section on a page, you **must include the `.md` file** before the anchor:

```markdown
✅ CORRECT - Include .md before #anchor
[Configuration Blocks](/blocks/index.md#configuration-blocks)
[SideNav Section](/blocks/sidenav/index.md#header-format)

❌ INCORRECT - Missing .md file
[Configuration Blocks](/blocks/#configuration-blocks)
[SideNav Section](/blocks/sidenav/#header-format)
```

**Format:** `path/to/file.md#anchor-name`

## Path Resolution

| From | To | Relative | Absolute |
| --- | --- | --- | --- |
| `blocks/links/index.md` | `blocks/columns/index.md` | `../columns/index.md` | `/blocks/columns/index.md` |
| `blocks/index.md` | `blocks/columns/index.md` | `columns/index.md` | `/blocks/columns/index.md` |
| `blocks/columns/index.md` | `index.md` (root) | `../../index.md` | `/index.md` |
