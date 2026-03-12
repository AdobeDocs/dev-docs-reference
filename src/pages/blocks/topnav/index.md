---
title: Top Navigation
description: Learn how to configure top navigation in config.md for your documentation site.
---

# Top Navigation

Configure top navigation in `config.md` using `pages`.

## How TopNav and SideNav Work Together

**The sidebar (SideNav) only appears when the current page belongs to a section defined in the top navigation.** Think of it this way:

1. **TopNav** (`pages`) defines the main sections in your site's header (e.g., Getting Started, Blocks, Deploy).
2. **SideNav** (`subPages`) defines the sidebar for each of those sections.
3. For a sidebar to show on a page, that page must be **under** one of the TopNav sections, and that section must have corresponding entries in `subPages`.

If your sidebar isn't showing, check: Is the page's section listed in both `pages` and `subPages`? The first-level items in `subPages` must align with your TopNav sections.

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
    - API Reference
      - [Reference v2.0](blocks/version1.md) - 🟢 Current version
      - [Reference v1.4](blocks/version2.md) - 🔴 Deprecated
    - [Support](support/index.md) 
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

## Buttons

You can add an optional **buttons** section to show action buttons in the top navigation (e.g., Code Playground, Console). Each button is a link followed by optional identifiers.

### Syntax

```yaml
- buttons:
  - [Code Playground](https://www.adobe.com/go/addon-playground?session=saved) playgroundId
  - [Console](https://developer.adobe.com/console/) consoleId
```

### Button identifiers

- **playgroundId**: Identifies the button as a playground (for Code Playground).
- **consoleId**: Identifies the button as the Console link.

The **Console** button may always appear in the top nav regardless of the `buttons` section; confirm behavior in your environment. The first button in your list is typically styled as the primary button and the second automatically takes a secondary button style.

## Paths

All paths in `config.md` are relative to `/src/pages/`. External links require full paths (e.g., `https://example.com`).

## Related

[SideNav](/blocks/sidenav/index.md) - Configure sidebar navigation. Sidebar items must be under a TopNav section to appear.
