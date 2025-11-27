---
title: Overview - Block Examples
description: Explore all available blocks for the Adobe Developer documentation site, including content blocks, code blocks, and API documentation components.
---

# DevDoc Block Examples

Build rich, interactive documentation using blocks organized into two categories:

- **Configuration Blocks**: Site structure and navigation (set in `config.md`)
- **Content Blocks**: Page content and formatting

## Configuration Blocks

Control your site's structure and navigation through `config.md`.

### [SideNav](sidenav/index.md)

Side navigation menu.

### [TopNav](topnav/index.md)

Top navigation bar.

### Breadcrumbs

[Breadcrumbs](breadcrumb/index.md)
Auto-generated navigation trail from your TopNav and SideNav.

### Footer

[Footer](footer/index.md)
Site footer (centrally managed).

## Content Blocks

Build and organize your page content.

### Accordion

[Accordion](accordion/index.md)  
Collapsible sections.

### Announcement

[Announcement](announcement/index.md)  
Important notices and announcements.

### Code

[Code](code/index.md)  
Markdown code snippet with syntax.
- [Basic](code/code-basic.md) - Simple examples
- [Highlighted Lines](code/code-highlighted-line.md) - Line highlighting
- [In Lists](code/code-in-list.md) - Nested in lists
- [In Tables](code/code-in-table.md) - Inline in tables
- [Combined Features](code/code-overload.md) - Multiple features

### CodeBlock

[CodeBlock](codeblock/index.md)  
Multiple code block with headings.
- [With Language Picker](codeblock/code-block-with-picklist.md) - Switch between languages
- [Without Language Picker](codeblock/code-block-without-picklist.md) - Show all at once

### Column

[Column](column/index.md)  
Multi-column layouts.

### Discover Block

[Discover Block](discoverblock/index.md)  
Featured content showcase.

### Edition

[Edition](edition/index.md)  
Edition-specific content.

### HeroSimple

[HeroSimple](herosimple/herosimple-default.md)  
Simple hero banner.
- [Default](herosimple/herosimple-default.md)
- [Full Width](herosimple/herosimple-fullwidth.md)
- [Half Width](herosimple/herosimple-halfwidth.md)

### Image

[Image](image/index.md)  
Add and format images.

### Inline Alert

[Inline Alert](inline-alert/index.md)  
Warnings, tips, and notes.

### Inline Code

[Inline Code](inline-code/index.md)  
Format inline code with backticks.

### Links

[Links](links/index.md)  
Link between pages using relative and absolute paths.

### List

[List](list/index.md)  
Styled lists with icons.

### On This Page

[On This Page](onthispage/index.md)  
Auto-generated table of contents from H2 and H3 headings.

### Redocly API Block

[Redocly API Block](redoclyapiblock/redocly-api-block-default.md)  
Interactive API docs from OpenAPI specs.

**Configuration:**
- [Default](redoclyapiblock/redocly-api-block-default.md) - Standard setup
- [Custom](redoclyapiblock/redocly-api-block-configs.md) - Styling and behavior

**Layout:**
- [Without Layout](redoclyapiblock/redocly-api-block-no-layout.md) - Full-page
- [Without Sidebar](redoclyapiblock/redocly-api-block-no-sidebar.md) - No sidebar
- [Without Sidebar & Search](redoclyapiblock/redocly-api-block-no-sidebar-no-search.md) - Minimal
- [With Scroll Offset](redoclyapiblock/redocly-api-block-no-y-scroll-offset.md) - Fixed headers

**Advanced:**
- [External API](redoclyapiblock/redocly-overflow.md) - Load from URLs

### Resources

[Resources](resources/resources.md)  
Resource links with optional hero.
- [With Hero](resources/resources.md)
- [Without Hero](resources/resources-with-no-hero.md)

### Superhero

[Superhero](superhero/index.md)  
Hero banners with images and CTAs. 8 variants:

**Layouts:**
- [Default](superhero/superhero-default.md) - Standard
- [Half Width](superhero/superhero-halfwidth.md) - Split-screen
- [Centered](superhero/superhero-centered.md) - Center-aligned
- [Centered XL](superhero/superhero-centeredxl.md) - Extra-large

**Enhanced:**
- [Default + Background](superhero/superhero-default-with-background-image.md) - Custom background
- [Default + Gradient](superhero/superhero-default-with-background-image-and-color.md) - Gradient background
- [Half Width + Background](superhero/superhero-halfwidth-with-background-image.md) - Full-width background
- [Half Width + Video](superhero/superhero-halfwidth-with-background-image-and-video.md) - Video background

### Tab

[Tab](tab/index.md)  
Organize content in tabs.

## Getting Started

1. Pick a hero variant
2. Set up navigation in `config.md`
3. Add content blocks
4. Include code examples
5. Add alerts as needed

