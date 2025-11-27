---
title: Overview - Block Examples
description: Explore all available blocks for the Adobe Developer documentation site, including content blocks, code blocks, and API documentation components.
---

# DevDoc Block Examples

Explore all available blocks for creating rich, interactive documentation. Blocks are organized into two main categories:

- **Configuration Blocks**: Define site structure and navigation (configured in `config.md`)
- **Content Blocks**: Create and format your documentation content

## Configuration Blocks

These blocks define the structure and navigation of your documentation site. They are configured in your `config.md` file and control the overall navigation experience.

### SideNav

[SideNav](sidenav/index.md)
Configure the side navigation menu for your documentation site.

### TopNav

[TopNav](topnav/index.md)
Configure the top navigation bar for your documentation site.

### Breadcrumbs

[Breadcrumbs](breadcrumb/index.md)
Automatically generated navigation trail based on TopNav and SideNav configuration.

### Footer

[Footer](footer/index.md)
Centrally managed footer appearing on all pages. Contact the team via Slack (#adobe-developer-website) for changes.

## Content Blocks

All content presentation blocks for creating and organizing your documentation content.

### Accordion

[Accordion](accordion/index.md)  
Collapsible content sections for organizing information.

### Announcement

[Announcement](announcement/index.md)  
Display important announcements or notices.

### Code Block

[Code Block](codeblock/index.md)  
Display multiple code snippets with headings.
- [Standard Code Block](codeblock/index.md) - Multiple code blocks with headings
- [With Language Picker](codeblock/code-block-with-picklist.md) - Dropdown to switch languages
- [Without Picker](codeblock/code-block-without-picklist.md) - All blocks visible

### Code Block Examples

[Code Examples](codeblock/code.md)  
Various code block features and formatting options.
- [Basic Code Block](codeblock/code-0.md) - Simple code blocks
- [Advanced Features](codeblock/code.md) - Line highlighting, offsets, disable line numbers
- [Highlighted Lines](codeblock/code-highlighted-line.md) - Highlight specific lines
- [Code in Lists](codeblock/code-in-list.md) - Code blocks nested in lists
- [Code in Tables](codeblock/code-in-table.md) - Inline code in table cells
- [Combined Features](codeblock/code-overload.md) - Multiple features together

### Column

[Column](column/index.md)  
Multi-column layouts for content organization.

### Discover Block

[Discover Block](discoverblock/index.md)  
Showcase featured content or resources.

### Edition

[Edition](edition/index.md)  
Edition-specific content display.

### HeroSimple

[HeroSimple](herosimple/herosimple-default.md)  
Simpler hero option for clean, focused pages.
- [Default](herosimple/herosimple-default.md)
- [Full Width](herosimple/herosimple-fullwidth.md)
- [Half Width](herosimple/herosimple-halfwidth.md)

### Image

[Image](image/index.md)  
Image display and formatting examples.

### Inline Alert

[Inline Alert](inline-alert/index.md)  
Inline alert messages for warnings, tips, and notes.

### Inline Code

[Inline Code](inline-code/index.md)  
Format inline code snippets, variable names, and technical terms using backticks.

### Links

[Links](links/index.md)  
Learn how to create links between documentation pages using relative and absolute paths.

### List

[List](list/index.md)  
Styled lists with icons and formatting options.

### On This Page

[On This Page](onthispage/index.md)  
Automatic table of contents sidebar displaying H2 and H3 headings for in-page navigation.

### Redocly API Block

[Redocly API Block](redoclyapiblock/redocly-api-block-default.md)  
Interactive API documentation from OpenAPI specifications.

**Configuration Options:**
- [Default](redoclyapiblock/redocly-api-block-default.md) - Standard configuration
- [Custom Configurations](redoclyapiblock/redocly-api-block-configs.md) - Customize styling and behavior

**Layout Options:**
- [Without Layout](redoclyapiblock/redocly-api-block-no-layout.md) - Full-page documentation
- [Without Sidebar](redoclyapiblock/redocly-api-block-no-sidebar.md) - Hide sidebar navigation
- [Without Sidebar & Search](redoclyapiblock/redocly-api-block-no-sidebar-no-search.md) - Minimalist view
- [With Scroll Offset](redoclyapiblock/redocly-api-block-no-y-scroll-offset.md) - For fixed headers

**Advanced:**
- [External API Example](redoclyapiblock/redocly-overflow.md) - Load from external URLs

### Resources

[Resources](resources/resources.md)  
Display resource links with optional hero banner.
- [With Hero](resources/resources.md)
- [Without Hero](resources/resources-with-no-hero.md)

### Superhero

[Superhero](superhero/index.md)  
Create impactful hero banners with images, headings, and call-to-action buttons. Choose from 8 variants:

**Layout Variants:**
- [Default](superhero/superhero-default.md) - Standard layout for documentation pages
- [Half Width](superhero/superhero-halfwidth.md) - Split-screen layout for product pages
- [Centered](superhero/superhero-centered.md) - Centered layout for home pages
- [Centered XL](superhero/superhero-centeredxl.md) - Extra-large centered layout

**Enhanced Variants:**
- [Default with Background](superhero/superhero-default-with-background-image.md) - With custom background color
- [Default with Gradient](superhero/superhero-default-with-background-image-and-color.md) - With gradient background
- [Half Width with Background](superhero/superhero-halfwidth-with-background-image.md) - With full-width background
- [Half Width with Video](superhero/superhero-halfwidth-with-background-image-and-video.md) - With video content

### Tab

[Tab](tab/index.md)  
Tabbed content for organizing related information.

## Getting Started

1. Choose your hero block variant based on page type
2. Configure navigation in `config.md`
3. Use content blocks to build your page
4. Add code examples with appropriate formatting
5. Include alerts and announcements as needed

