---
title: Breadcrumbs
description: Automatically generated navigation trail based on TopNav and SideNav configuration.
---

# Breadcrumbs

Auto-generated navigation trail from your TopNav and SideNav.

## How It Works

Breadcrumbs are built automatically from your `config.md` navigation structure:
- **TopNav**: Top-level context
- **SideNav**: Page hierarchy

![breadcrumb](../../assets/breadcrumb.png)

## Example

```yaml
- pages:
    - [Overview](index.md)
    - [Reference Docs](blocks/index.md)

- subPages:
    - [Overview](blocks/index.md)
        - [Configuration Blocks](#configuration-blocks)
            - [SideNav](/blocks/sidenav/index.md)
            - [TopNav](/blocks/topnav/index.md)
            - [Breadcrumbs](/blocks/breadcrumb/index.md)
```

## Hide

To hide breadcrumbs, add `hideBreadcrumbs: true` to your page's frontmatter:

```
---
title: Breadcrumbs
description: Automatically generated navigation trail based on TopNav and SideNav configuration.
hideBreadcrumbs: true
---
```

![hide breadcrumb](../../assets/hide_breadcrumb.png)

## Related

- [TopNav](/blocks/topnav/index.md) - Top navigation
- [SideNav](/blocks/sidenav/index.md) - Side navigation
