---
title: Cards Block
description: Display content in a card layout with images, headings, text, and links using the Cards block.
---

# Cards Block

Display content in a grid of cards with images and links.

## Syntax

```markdown
<Cards slots="image, heading, text, links" width="33%" />

![Card Image](path/to/image.png)

## Card Heading

Card description text goes here.

[Learn more](link-url.md)
```

## Parameters

- **slots**: Content structure per card
  - `"image, heading, text, links"` - Full card with all elements
  - `"heading, text, links"` - Card without image
  - `"image, heading, links"` - Card without description text

- **width**: Card width for grid layout (optional)
  - Full width (default)
  - `"33%"` - Three cards per row (3-column grid)
  - `"50%"` - Two cards per row (2-column grid)
  - `"25%"` - Four cards per row (4-column grid)

- **Image size**: 80 x 80 px recommended

## Examples

<Cards slots="image, heading, text, links" width="33%" />

![Card Image](../../assets/column.jpg)

## First Card

This is a sample description for the first card in the grid.

[Learn more](https://developer.adobe.com/)

<Cards slots="image, heading, text, links" width="33%" />

![Card Image](../../assets/column.jpg)

### Second Card

This is a sample description for the second card in the grid.

[Learn more](https://developer.adobe.com/)

<Cards slots="image, heading, text, links" width="33%" />

![Card Image](../../assets/column.jpg)

### Third Card

This is a sample description for the third card in the grid.

[Learn more](https://developer.adobe.com/)