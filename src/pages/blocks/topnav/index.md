---
title: Top Navigation
description: Learn how to configure top navigation in config.md for your documentation site.
---

# Top Navigation

Configure top navigation in `config.md` using `pages`.

## Default Links

The top navigation always includes these links first:
- **Adobe Developer** → `developer.adobe.com`
- **Products** → `developer.adobe.com/apis`

Your custom links from `pages` appear after these default links.

## Example

```md
- pathPrefix:
    - /dev-docs-reference/

- pages:
    - [Overview](index.md)
    - [Reference Docs](blocks/index.md)
        - [Version 1.0](blocks/version1.md)
        - [Version 2.0](blocks/version2.md)
```

Indent items to create dropdowns:

![topnav_dropdown](../../assets/topnav.png)

## Components

**pathPrefix**: Base URL path prepended to the domain
```md
- pathPrefix:
    - /dev-docs-reference/
```

**pages**: Navigation items in the top bar
```md
- pages:
    - [Home](index.md)
    - [Documentation](docs/index.md)
```

## Paths

All paths in `config.md` are relative to `/src/pages/`. External links require full paths (e.g., `https://example.com`).


## Related

[SideNav](/blocks/sidenav/index.md) - Configure sidebar navigation
