---
title: Breadcrumbs
description: Automatically generated navigation trail based on TopNav and SideNav configuration.
---

# Breadcrumbs

Breadcrumbs provide users with a hierarchical navigation trail showing their current location within the documentation site structure.

## Overview

Breadcrumbs are **automatically generated** based on your TopNav and SideNav configuration. They require no separate configuration or setup - the breadcrumb trail is built dynamically from your existing navigation structure defined in `config.md`.

## How Breadcrumbs Work

The breadcrumb trail is constructed by combining:

1. **TopNav** - Provides the top-level navigation context
2. **SideNav** - Provides the hierarchical page structure

As users navigate through your documentation, breadcrumbs automatically update to reflect their current position in the site hierarchy.

## Example

The breadcrumb trail is automatically generated from:
- **TopNav**: Products > Overview > Reference Docs (top-level sections)
- **SideNav**: Overview > Configuration Blocks > Breadcrumbs

![breadcrumb](../../assets/breadcrumb.png)

## Configuration

Breadcrumbs are configured through your `config.md` file's navigation structure:

```markdown
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

This navigation structure automatically generates breadcrumbs for each page based on its position in the hierarchy.

## Best Practices

- **Maintain clear hierarchy**: Organize your `config.md` with logical parent-child relationships
- **Use descriptive titles**: Breadcrumb text is taken from the link titles in your navigation
- **Avoid deep nesting**: Keep navigation depth to 3-4 levels for optimal user experience
- **Test navigation paths**: Verify that breadcrumbs accurately reflect the intended page hierarchy

## Related Configuration

- [TopNav](/blocks/topnav/index.md) - Configure the top navigation bar
- [SideNav](/blocks/sidenav/index.md) - Configure the side navigation menu

