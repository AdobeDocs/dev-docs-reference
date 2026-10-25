---
title: Cards with Buttons
description: Display cards with button calls to action using the Cards block.
---

# Cards with Buttons

Cards that show their call to action as a button. See [Cards parameters](index.md) for `slots`, `width`, and other options.

## Syntax

```markdown
<Cards slots="image, heading, text, buttons" width="33%" />

![Card Image](path/to/image.png)

## Card Heading

Card description text goes here.

[Learn more](link-url.md)

```

## Parameters

- **slots**: Use `buttons` instead of `links` to show the call to action as a button. Don't use `links` and `buttons` in the same block.

## Example

<Cards slots="image, heading, text, buttons" width="33%" />

![Card Image](../../assets/column.jpg)

### First Card

This is a sample description for the first card in the grid.

[Learn more](https://developer.adobe.com/)

<Cards slots="image, heading, text, buttons" width="33%" />

![Card Image](../../assets/column.jpg)

### Second Card

This is a sample description for the second card in the grid.

[Learn more](https://developer.adobe.com/)

<Cards slots="image, heading, text, buttons" width="33%" />

![Card Image](../../assets/column.jpg)

### Third Card

This is a sample description for the third card in the grid.

[Learn more](https://developer.adobe.com/)
