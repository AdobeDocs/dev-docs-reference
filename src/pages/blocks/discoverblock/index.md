---
title: Discover Block
description: Showcase featured content and resources using the Discover block component.
---

# Discover Block

Display featured content, resources, or links in a visually appealing card-based layout to help users discover important information.

## Overview

Discover Blocks are useful for:
- Highlighting key resources or guides
- Showcasing multiple related links
- Creating resource hubs or landing pages
- Organizing community links (forums, GitHub)
- Feature showcases with images

## Syntax

```markdown
<DiscoverBlock slots="heading, link, text"/>

## Your Heading

[Link Text](url)

Description text here.
```

## Parameters

- **slots**: Content structure
  - `"link, text"`: Link with description
  - `"heading, link, text"`: Heading, link, and description
  - `"image, heading, link, text"`: Icon/image, heading, link, and description

- **width**: Card width (optional)
  - Default: Full width
  - `"25%"`: Quarter width (for grid layouts)
  - `"33%"`: Third width
  - `"50%"`: Half width

## Image Suggestions

For the `image` slot, use a **512 x 512 px** image for optimal display quality.

## Examples

### Basic Discover Blocks

<DiscoverBlock slots="heading, link, text"/>

## Get Started with Basics

[Developer Quickstart Guide](https://example.com/quickstart)

Start building your first application with our platform.

<DiscoverBlock slots="link, text"/>

[API Reference](https://example.com/api-reference)

Explore the complete API documentation and endpoints.

<DiscoverBlock slots="link, text"/>

[Development Tools](https://example.com/tools)

Access the essential tools to help you create, debug, and deploy your applications efficiently.

<DiscoverBlock slots="link, text"/>

[Code Samples](https://example.com/samples)

Browse code examples to accelerate your development workflow.

<DiscoverBlock slots="link, text"/>

[Migration Guide](https://example.com/migration)

Transitioning from a previous version? Find migration resources here.

<DiscoverBlock slots="link, text"/>

[Design Guidelines](https://example.com/design)

Learn best practices for creating user-friendly applications.

### With Images and Grid Layout

Use `width="25%"` to create a grid layout with multiple cards:

<DiscoverBlock slots="image, heading, link, text" width="25%"/>

![Community](../../assets/test-icon.png)

### Developer Community

[Community forum](https://example.com/forum)

Ask questions, share knowledge, and participate in discussions with other developers.

<DiscoverBlock slots="link, text" width="25%"/>

[Developer portal](https://example.com/portal)

Access your developer account, manage applications, and view analytics.

<DiscoverBlock slots="image, heading, link, text" width="25%"/>

![GitHub](../../assets/test-icon.png)

### GitHub

[Contributing](https://github.com/example/project/blob/main/.github/CONTRIBUTING.md)

Learn how you can contribute to the project documentation.

<DiscoverBlock slots="link, text" width="25%"/>

[Issues](https://github.com/example/project/issues)

Submit an issue to the repository for the team to review.

<DiscoverBlock slots="link, text" width="25%"/>

[Pull requests](https://github.com/example/project/pulls)

View open pull requests for the repository.

<DiscoverBlock slots="image, heading, link, text" width="25%"/>

![Slack](../../assets/test-icon.png)

### Slack

[Request an invite](https://example.com/slack-invite)

Join our developer community Slack workspace to connect with other developers.

<DiscoverBlock slots="link, text" width="25%"/>

[Developer channel](https://example.slack.com/channels/developers)

Connect with developers in our main community channel.

## Best Practices

- **Use descriptive headings**: Make it clear what users will find
- **Keep text concise**: Brief descriptions work best in card layouts
- **Group related content**: Organize similar items together
- **Use images consistently**: Choose a consistent image style and size (512 x 512 px recommended)
- **Grid layouts**: Use `width="25%"` for 4-column grids, `"33%"` for 3-column

## Common Use Cases

- **Resource hubs**: Link to guides, tutorials, and documentation
- **Community sections**: Forums, GitHub, social channels
- **Tool discovery**: Showcase available tools and utilities
- **Getting started**: Quick links for new users
- **Feature highlights**: Showcase product features or capabilities

## Related

- [Resources](/blocks/resources/resources.md) - Simple resource link lists
- [List](/blocks/list/index.md) - Styled lists with images
- [Column](/blocks/column/index.md) - Multi-column layouts
