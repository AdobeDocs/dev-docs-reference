---
title: Side Navigation
description: Learn how to configure sidebar navigation using subPages in config.md.
---

# Side Navigation

Configure sidebar navigation in `config.md` using `subPages`.

## Example

```md
- subPages:
    - [Content Blocks](#content-blocks)
      - [Accordion](/blocks/accordion/index.md)
        - [Accordion Basic](/blocks/accordion/accordion-basic.md)
        - [Accordion with Table & Code](/blocks/accordion/accordion-with-table-and-code.md)
```

## Format

`[Display Text](path/to/file.md)`

**Indentation = Nesting:**
```md
- [Overview](blocks/index.md)           # Top level
  - [Accordion](/blocks/accordion/index.md)  # Nested (2 spaces)
    - [Basic](/blocks/accordion/basic.md)     # Nested deeper (4 spaces)
```

## Result

![sidenav image](../../assets/sidenav.png)

## Paths

All paths start from `src/pages/`. Leading `/` is optional.

| In config.md | Resolves to |
| --- | --- |
| `blocks/index.md` | `src/pages/blocks/index.md` |
| `/blocks/index.md` | `src/pages/blocks/index.md` |

**Note:** This differs from markdown files, where paths are relative to the current file (e.g., `../sidenav/index.md`).

## Related

[TopNav](/blocks/topnav/index.md) - Configure top navigation

