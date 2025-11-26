---
title: Image Block
description: Learn how to display and format images in your documentation.
---

# Image Block

Display images in your documentation using standard markdown syntax.

## Syntax

```markdown
![Alt text](path/to/image.png)
```

**Relative path:**
```markdown
![My Image](../../assets/my-image.png)
```

**Absolute URL:**
```markdown
![External Image](https://example.com/image.png)
```

## Parameters

- **Alt text**: Descriptive text for accessibility (required)
- **Path**: Relative path to assets folder or absolute URL
- **Formats**: PNG, JPG, GIF, WebP, SVG

## Example

![Documentation example](../../assets/image1.jpeg)

![Platform interface](../../assets/image1.jpeg)

![External Image](https://via.placeholder.com/800x400/6366f1/ffffff?text=Example+Image)

## Best Practices

- Always include descriptive alt text for accessibility
- Optimize images for web (< 500KB recommended)
- Use PNG for screenshots, JPG for photos, SVG for icons
- Store local images in `src/pages/assets/` directory

## Related

- [Superhero](/blocks/superhero/index.md) - Hero banners with background images
- [DiscoverBlock](/blocks/discoverblock/index.md) - Cards with images
- [Column](/blocks/column/index.md) - Multi-column layouts with images
