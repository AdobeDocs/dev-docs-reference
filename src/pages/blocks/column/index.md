---
title: Column Block
description: Create multi-column layouts for content organization using the Column block.
---

# Column Block

Create multi-column layouts to display content side-by-side with images, headings, text, and links.

## Syntax

```markdown
<Columns slots="image, heading, text, buttons" repeat="3" />
```

## Parameters

- **slots**: Content structure for each column
  - `"heading, text"`: Heading and text
  - `"image, heading, text"`: Image, heading, and text
  - `"image, heading, text, buttons"`: All elements including links

- **repeat**: Number of columns to display (typically 2-4)

## Example

<Columns slots="image, heading, text, buttons" repeat ="3" />

![Feature 1](../../images/column_image.webp)

### Feature Heading

Description of the feature or content. Keep text concise for better readability in column layouts.

[Learn more](https://example.com)

![Feature 2](../../images/column_image2.webp)

### Another Feature

More details about this feature or capability. Column layouts work well for comparing options or showcasing multiple features.

[Learn more](https://example.com)

![Feature 3](../../images/column_image.webp)

### Third Feature

Additional content for the third column. Use consistent structure across all columns for visual balance.

[Learn more](https://example.com)

## Best Practices

- Keep column count to 2-4 for readability
- Use consistent content structure across all columns
- Keep text concise to maintain visual balance
- Use similar image sizes for consistency

## Related

- [DiscoverBlock](/blocks/discoverblock/index.md) - Card-based content display
- [List](/blocks/list/index.md) - Styled lists with icons
