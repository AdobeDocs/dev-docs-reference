---
title: Discover Block
description: Showcase featured content and resources using the Discover block component.
---

# Discover Block

Featured content in a card layout.

## Syntax

```markdown
<DiscoverBlock slots="heading, link, text"/>

## Your Heading

[Link Text](url)

Description text here.
```

## Parameters

- **slots**: Content structure
  - `"link, text"` - Link with description
  - `"heading, link, text"` - With heading
  - `"image, heading, link, text"` - With image

- **width**: Card width
  - Full width (default)
  - `"25%"` - Quarter (4-column grid)
  - `"33%"` - Third (3-column grid)
  - `"50%"` - Half (2-column grid)

- **Image size**: 512 x 512 px recommended

## Examples

### Basic:

<DiscoverBlock slots="heading, link, text"/>

## Get Started

[Developer Guide](https://example.com/quickstart)

Start building your first application.

<DiscoverBlock slots="link, text"/>

[API Reference](https://example.com/api)

Explore the complete API documentation.

### Grid Layout:

Use `width="33%"` for a 3-column grid:

<DiscoverBlock slots="image, heading, link, text" width="33%"/>

![Community](../../assets/test-icon.png)

### Community

[Forum](https://example.com/forum)

Ask questions and share knowledge.

<DiscoverBlock slots="link, text" width="33%"/>

[Portal](https://example.com/portal)

Manage your applications.

<DiscoverBlock slots="link, text" width="33%"/>

[Contributing](https://github.com/example/project)

Contribute to the project.
