---
title: Image Block
description: Learn how to display and format images in your documentation.
---

# Image Block

Add images to your documentation using standard markdown syntax or advanced image features.

## Overview

Images help illustrate concepts, showcase features, and improve visual appeal. The platform supports:
- Standard markdown image syntax
- Alt text for accessibility
- Relative and absolute image paths
- Multiple image formats (PNG, JPG, GIF, WebP, SVG)
- Responsive images

## Syntax

### Basic Image

```markdown
![Alt text](path/to/image.png)
```

### Relative Path

```markdown
![My Image](../../assets/my-image.png)
```

### Absolute URL

```markdown
![External Image](https://example.com/image.png)
```

## Image Paths

- **Relative paths**: Use `../../assets/` for images in the assets folder
- **Absolute URLs**: Use full URLs for external images
- **Local assets**: Store images in `src/pages/assets/` directory

## Image Requirements

- **Format**: PNG, JPG, GIF, WebP, or SVG
- **Size**: Optimize images for web (recommended < 500KB)
- **Dimensions**: Consider responsive layout (recommended max width 1200px)
- **Alt text**: Always provide descriptive alt text for accessibility

## Examples

### Single Image

![Documentation example](../../assets/image1.jpeg)

### Multiple Images

![Platform interface](../../assets/image1.jpeg)

![Creative Cloud integration](../../assets/image2.jpeg)

![External Image](https://loremflickr.com/800/400/technology)

## Best Practices

- **Always include alt text**: Describe what the image shows for accessibility
- **Use descriptive file names**: `user-dashboard.png` instead of `image1.png`
- **Optimize file size**: Compress images before uploading
- **Choose appropriate format**: 
  - PNG for screenshots, diagrams with text
  - JPG for photographs
  - SVG for logos, icons, and vector graphics
  - WebP for best compression (with fallbacks)
- **Consider dark mode**: Ensure images work on both light and dark backgrounds
- **Provide context**: Add explanatory text around images when needed

## Accessibility

- **Alt text is required**: Screen readers depend on it
- **Be descriptive**: "Screenshot of login form with email and password fields" not "login"
- **Decorative images**: Use empty alt text `![]()` only for purely decorative images
- **Complex diagrams**: Consider providing a text description or summary

## Common Use Cases

- **Screenshots**: Illustrate UI elements or workflows
- **Diagrams**: Explain architecture or processes
- **Logos**: Display brand or partner logos
- **Charts/Graphs**: Present data visually
- **Examples**: Show code output or results
- **Hero images**: Add visual interest to landing pages

## Related

- [HeroSimple](/blocks/herosimple/herosimple-default.md) - Hero sections with images
- [Superhero](/blocks/superhero/index.md) - Large hero banners with background images
- [DiscoverBlock](/blocks/discoverblock/index.md) - Cards with images
