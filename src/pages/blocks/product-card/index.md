---
title: Product Card Block
description: Display product or technology information in a card format with icons, descriptions, and action buttons.
---

# Product Card Block

Display product or technology information in a styled card format with an icon, description text, and action buttons.

## Syntax

```markdown
<Product-Card slots="icon, text, buttons" repeat="2" />

![Product Icon](path/to/icon.svg)

Description text for the product or technology goes here. This can include multiple sentences describing the features and benefits.

- [Learn more](https://example.com/)
- [View Docs](https://example.com/docs)

![Product Icon](path/to/icon2.svg)

Description text for the second product card.

- [Learn more](https://example.com/)
```

## Parameters

- **slots**: Content structure per card
  - `"icon, text, buttons"` - Icon with description and action buttons

- **repeat**: Number of product cards to display
  - Set to match the number of card content blocks provided

- **Icon size**: SVG icons recommended for best quality

## Content Structure

Each product card requires the following content in order:

1. **Icon**: An image (preferably SVG) representing the product or technology
2. **Text**: A paragraph describing the product, its features, or benefits
3. **Buttons**: A list of links that will render as action buttons

## Example

<Product-Card slots="icon, text, buttons" repeat="2" />

![Product Icon](../../assets/adobe.svg)

This is a sample description for the first product card. Add details about the product features, benefits, and use cases to help users understand what this product offers.

- [Learn more](https://developer.adobe.com/)
- [View Docs](https://developer.adobe.com/)

![Product Icon](../../assets/adobe.svg)

This is a sample description for the second product card. Include relevant information about the product capabilities and how it can help developers.

- [Learn more](https://developer.adobe.com/)