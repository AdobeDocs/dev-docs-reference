---
title: Next/Previous Navigation
description: Automatically generated page navigation links based on SideNav configuration.
---

# Next/Previous Navigation

The Next/Previous block provides users with navigation links to move sequentially through documentation pages.

## Overview

Next/Previous navigation is **automatically generated** based on your SideNav configuration. The block reads the page hierarchy from your side navigation menu and creates links to the adjacent pages - allowing users to easily move forward or backward through your documentation.

## How Next/Previous Works

The navigation links are constructed by:

1. **Reading the SideNav** - Extracts all page links from the side navigation menu
2. **Finding the current page** - Identifies where the user is in the page sequence
3. **Displaying adjacent pages** - Shows links to the previous and next pages in the hierarchy

The block automatically displays:
- **Previous link** (left side) - Links to the page before the current page
- **Next link** (right side) - Links to the page after the current page

If there is no previous page (you're on the first page), only the next link appears. If there is no next page (you're on the last page), only the previous link appears.

## Configuration

The Next/Previous block requires no separate configuration. It automatically uses your existing SideNav structure defined in `config.md`:

```markdown
- subPages:
  - [Overview](blocks/index.md)
      - [Configuration Blocks](#configuration-blocks)
          - [SideNav](/blocks/sidenav/index.md)
          - [TopNav](/blocks/topnav/index.md)
          - [Breadcrumbs](/blocks/breadcrumb/index.md)
```

In this example, when viewing the "TopNav" page:
- **Previous** page would be "SideNav"
- **Next** page would be "Breadcrumbs"

![NextprevExample](../../assets/nextprev.png)

The block will render navigation arrows with the page titles pulled from your SideNav configuration.

## Best Practices

- **Maintain logical order**: Ensure your SideNav pages are ordered in the sequence users should follow
- **Use with linear content**: Best suited for documentation with a clear reading order (tutorials, guides, walkthroughs)

## Related Configuration

- [SideNav](/blocks/sidenav/index.md) - Configure the side navigation menu that determines page order
