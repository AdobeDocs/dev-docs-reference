---
title: Side Navigation
description: Learn how to configure sidebar navigation using subPages in config.md.
---

# Side Navigation

Configure sidebar navigation in `config.md` using `subPages`.

## Example

```md
- subPages:
    - [Content Blocks](/blocks/index.md)
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

## Headers

You can use headers to organize navigation items into labeled sections.

### Header Format

Headers are **plain text** (not links) that appear as non-clickable labels in the sidebar:

```md
  - subPages:
    - Content Blocks header
    - [Accordion](/blocks/accordion/index.md)
    - [Cards](/blocks/cards/index.md)
    - [Code](/blocks/code/index.md)
```

**Important:** After a header, the next item **must be at the same indentation level** as the header. You cannot indent the items after a header.

### Nested Header Usage

```md

- subPages:
    - Content Blocks header
    - [Accordion](/blocks/accordion/index.md)
    - [Cards](/blocks/cards/index.md)
       - Configuration Blocks header
       - [SideNav](/blocks/sidenav/index.md)
         - [TopNav](/blocks/topnav/index.md)
```

### Result

![sidenav header](../../assets/side-nav-header.png)

## Link Requirements

Every entry in the side navigation must have a link (except headers, which are plain text).

**Link Format:**
- **Internal links** must end with `.md` (e.g., `/blocks/accordion/index.md`)
- **External links** must be absolute URLs (e.g., `https://example.com`)

### Path Rules

1. **First-level entries** must use relative paths (relative to `/src/pages/`)
2. **First-level entries** must start with a TopNav item
3. **Child entries** can use either:
   - Relative paths ending in `.md` (to pages within your site)
   - Absolute URLs (external links like `https://example.com`)

### Examples

```md
- subPages:
    # First level - must be relative and start with a TopNav item
    - [Content Blocks](/blocks/index.md)
      # Children - can be relative (ending in .md) or absolute URLs
      - [Accordion](/blocks/accordion/index.md)
      - [External Guide](https://example.com/guide)
```

All relative paths in `config.md` are relative to `/src/pages/`.


## Related

[TopNav](/blocks/topnav/index.md) - Configure top navigation

