---
title: ADP Developer Site - Block Overview
description: Explore all available blocks for the Adobe Developer documentation site, including content blocks, code blocks, and API documentation components.
---

# DevDoc Block Examples

## Overview

This reference site showcases all available blocks that can be used to create engaging developer documentation. Each block is a modular component designed to present specific types of content, from hero banners and code examples to interactive API documentation and media resources.

These blocks provide a consistent, standardized way to structure and display content across Adobe developer documentation sites. Whether you're building tutorials, API references, or product guides, these blocks enable you to create professional, accessible documentation efficiently.

## Categories of Blocks

There are two main categories of blocks available:

* **Configuration Blocks**: Essential navigation and layout configuration blocks including SideNav and TopNav. These blocks define the structure and navigation of your documentation site (set in `config.md`).
* **Content Blocks**: All content presentation blocks including heroes, accordions, code blocks, API documentation, tabs, and more. These blocks help you create and organize your documentation content with rich formatting and interactive elements.

## Configuration Blocks

Control your site's structure and navigation through `config.md`.

### [SideNav](sidenav/index.md)

Side navigation menu.

### [TopNav](topnav/index.md)

Top navigation bar.

### [Breadcrumbs](breadcrumb/index.md)

Auto-generated navigation trail from your TopNav and SideNav.

### [Hide Page Actions](hide-page-actions/index.md)

Control visibility of Edit in GitHub, Log an issue, and Copy Markdown per page.

### [Footer](footer/index.md)

Site footer (centrally managed).

### [Site-Wide Banner](site-wide-banner/index.md)

Announcement banner displayed across all pages.

## Content Blocks

Build and organize your page content.

### [Accordion](accordion/index.md)

Collapsible sections.

### [Announcement](announcement/index.md)

Important notices and announcements.

### [Cards](cards/index.md)

Content cards in grid layouts.

### [Code](code/index.md)

Markdown code snippet with syntax.
- [Basic](code/code-basic.md) - Simple examples
- [Highlighted Lines](code/code-highlighted-line.md) - Line highlighting
- [In Lists](code/code-in-list.md) - Nested in lists
- [In Tables](code/code-in-table.md) - Inline in tables
- [Combined Features](code/code-overload.md) - Multiple features

### [CodeBlock](codeblock/index.md)

Multiple code block with headings.
- [With Language Picker](codeblock/code-block-with-picklist.md) - Switch between languages
- [Without Language Picker](codeblock/code-block-without-picklist.md) - Show all at once

### [Columns](columns/index.md)

Multi-column layouts.
- [With Image](columns/columns-with-image.md)
- [With Video](columns/columns-with-video.md) 

### [Discover Block](discoverblock/index.md)

Featured content showcase.

### [Edition](edition/index.md)

Edition-specific content.

### [Embed](embed/index.md)

Integrate videos, social media posts, and other external media.

### [Fragment](fragment/index.md)

Include reusable content from other markdown files.

### [Iframe](iframe/index.md)

Embed external content and web pages.

### [Image](image/index.md)

Add and format images.

### [Inline Alert](inline-alert/index.md)

Warnings, tips, and notes.

### [Inline Code](inline-code/index.md)

Format inline code with backticks.

### [Links](links/index.md)

Link between pages using relative and absolute paths.

### [List](list/index.md)

Styled lists with icons.

### [On This Page](onthispage/index.md)

Auto-generated table of contents from H2 and H3 headings.

### [Redocly API Block](redoclyapiblock/redocly-api-block-default.md)

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

### [Resources](resources/index.md)

Resource links displayed on right sidebar.

### [Superhero](superhero/index.md)

Hero banners with images and CTAs. 8 variants:

**Layouts:**
- [Default](superhero/superhero-default.md) - Standard
- [Half Width](superhero/superhero-halfwidth.md) - Split-screen
- [Centered](superhero/superhero-centered.md) - Center-aligned
- [Centered XL](superhero/superhero-centeredxl.md) - Extra-large

**Enhanced:**
- [Default + Background](superhero/superhero-default-with-background-image.md) - Custom background
- [Half Width + Background](superhero/superhero-halfwidth-with-background-image.md) - Full-width background
- [Half Width + Video](superhero/superhero-halfwidth-with-background-image-and-video.md) - Video background

### [Tab](tab/index.md)

Organize content in tabs.

