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

[SideNav](blocks/sidenav/index.md)
Configure the side navigation menu for your documentation site.

### TopNav

[TopNav](blocks/topnav/index.md)
Configure the top navigation bar for your documentation site.

### Breadcrumbs

[Breadcrumbs](blocks/breadcrumb/index.md)
Automatically generated navigation trail based on TopNav and SideNav configuration.

### Footer

[Footer](blocks/footer/index.md)
Centrally managed footer appearing on all pages. Contact the team via Slack (#adobe-developer-website) for changes.

## Content Blocks

All content presentation blocks for creating and organizing your documentation content.

### Accordion

[Accordion](blocks/accordion/index.md)  
Collapsible content sections for organizing information.

### Announcement

[Announcement](blocks/announcement/index.md)  
Display important announcements or notices.

### Code Block

[Code Block](blocks/codeblock/code-block.md)  
Display multiple code snippets with headings.
- [Standard Code Block](blocks/codeblock/code-block.md) - Multiple code blocks with headings
- [With Language Picker](blocks/codeblock/code-block-with-picklist.md) - Dropdown to switch languages
- [Without Picker](blocks/codeblock/code-block-without-picklist.md) - All blocks visible

### Code Block Examples

[Code Examples](blocks/codeblock/code.md)  
Various code block features and formatting options.
- [Basic Code Block](blocks/codeblock/code-0.md) - Simple code blocks
- [Advanced Features](blocks/codeblock/code.md) - Line highlighting, offsets, disable line numbers
- [Highlighted Lines](blocks/codeblock/code-highlighted-line.md) - Highlight specific lines
- [Code in Lists](blocks/codeblock/code-in-list.md) - Code blocks nested in lists
- [Code in Tables](blocks/codeblock/code-in-table.md) - Inline code in table cells
- [Combined Features](blocks/codeblock/code-overload.md) - Multiple features together

### Column

[Column](blocks/column/index.md)  
Multi-column layouts for content organization.

### Discover Block

[Discover Block](blocks/discoverblock/index.md)  
Showcase featured content or resources.

### Edition

[Edition](blocks/edition/index.md)  
Edition-specific content display.

### HeroSimple

[HeroSimple](blocks/herosimple/herosimple-default.md)  
Simpler hero option for clean, focused pages.
- [Default](blocks/herosimple/herosimple-default.md)
- [Full Width](blocks/herosimple/herosimple-fullwidth.md)
- [Half Width](blocks/herosimple/herosimple-halfwidth.md)

### Image

[Image](blocks/image/index.md)  
Image display and formatting examples.

### Inline Alert

[Inline Alert](blocks/inline-alert/index.md)  
Inline alert messages for warnings, tips, and notes.

### Inline Code

[Inline Code](blocks/inline-code/index.md)  
Format inline code snippets, variable names, and technical terms using backticks.

### List

[List](blocks/list/index.md)  
Styled lists with icons and formatting options.

### On This Page

[On This Page](blocks/onthispage/index.md)  
Automatic table of contents sidebar displaying H2 and H3 headings for in-page navigation.

### Redocly API Block

[Redocly API Block](blocks/redoclyapiblock/redocly-api-block-default.md)  
Interactive API documentation from OpenAPI specifications.

**Configuration Options:**
- [Default](blocks/redoclyapiblock/redocly-api-block-default.md) - Standard configuration
- [Custom Configurations](blocks/redoclyapiblock/redocly-api-block-configs.md) - Customize styling and behavior

**Layout Options:**
- [Without Layout](blocks/redoclyapiblock/redocly-api-block-no-layout.md) - Full-page documentation
- [Without Sidebar](blocks/redoclyapiblock/redocly-api-block-no-sidebar.md) - Hide sidebar navigation
- [Without Sidebar & Search](blocks/redoclyapiblock/redocly-api-block-no-sidebar-no-search.md) - Minimalist view
- [With Scroll Offset](blocks/redoclyapiblock/redocly-api-block-no-y-scroll-offset.md) - For fixed headers

**Advanced:**
- [External API Example](blocks/redoclyapiblock/redocly-overflow.md) - Load from external URLs

### Resources

[Resources](blocks/resources/resources.md)  
Display resource links with optional hero banner.
- [With Hero](blocks/resources/resources.md)
- [Without Hero](blocks/resources/resources-with-no-hero.md)

### Superhero

[Superhero](blocks/superhero/index.md)  
Create impactful hero banners with images, headings, and call-to-action buttons. Choose from 8 variants:

**Layout Variants:**
- [Default](blocks/superhero/superhero-default.md) - Standard layout for documentation pages
- [Half Width](blocks/superhero/superhero-halfwidth.md) - Split-screen layout for product pages
- [Centered](blocks/superhero/superhero-centered.md) - Centered layout for home pages
- [Centered XL](blocks/superhero/superhero-centeredxl.md) - Extra-large centered layout

**Enhanced Variants:**
- [Default with Background](blocks/superhero/superhero-default-with-background-image.md) - With custom background color
- [Default with Gradient](blocks/superhero/superhero-default-with-background-image-and-color.md) - With gradient background
- [Half Width with Background](blocks/superhero/superhero-halfwidth-with-background-image.md) - With full-width background
- [Half Width with Video](blocks/superhero/superhero-halfwidth-with-background-image-and-video.md) - With video content

### Tab

[Tab](blocks/tab/index.md)  
Tabbed content for organizing related information.

## Getting Started

1. Choose your hero block variant based on page type
2. Configure navigation in `config.md`
3. Use content blocks to build your page
4. Add code examples with appropriate formatting
5. Include alerts and announcements as needed

