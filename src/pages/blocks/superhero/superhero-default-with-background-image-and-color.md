---
title: Superhero - Default with Gradient Background
description: Standard superhero layout with gradient background for modern visual appeal.
---

# Superhero - Default with Gradient Background

The default variant with a gradient background creates a modern, visually appealing hero with smooth color transitions.

## Overview

This variant is best suited for:
- Modern product pages
- Creative applications
- Brand-focused landing pages
- Pages needing visual flair

## Syntax

```markdown
<Superhero slots="image, heading, text, buttons" background="linear-gradient(180deg, #c946eb, #6372f5)"/>

![Hero image](path/to/image.png)

# Your Heading

Your descriptive text here.

* [Button](url)
```

## Parameters

- **slots**: Content structure
  - `"image"`: Hero image
  - `"heading"` (required): Main heading
  - `"text"` (required): Descriptive text
  - `"buttons"` (optional): Call-to-action buttons

- **background**: CSS gradient
  - Format: `linear-gradient(angle, color1, color2)`
  - Example: `background="linear-gradient(180deg, #c946eb, #6372f5)"`
  - Supports multiple color stops

- **textColor**: Text color (default: white)
  - Options: `white`, `black`, `navy`, `gray`

## Example

<Superhero slots="image, heading, text, buttons" background="linear-gradient(180deg, #c946eb, #6372f5)"/>

![Hero image](../../assets/wide-SDK-Banner-570x400.png)

# Adobe Photoshop and Lightroom API

Unlock the potential of Photoshop, Lightroom, and cutting edge Sensei services through an easy-to-use RESTful API.

* [Get the SDKs](https://developer.adobe.com/console/servicesandapis/ae)

## Gradient Tips

- Use 2-3 colors for smooth transitions
- Start with brand colors
- Consider accessibility and text readability
- Test gradients at different angles (90deg, 180deg, 45deg)
- Common format: `linear-gradient(180deg, #color1, #color2)`

## Best Practices

- Choose gradient colors that align with brand
- Ensure text has sufficient contrast throughout gradient
- Test on multiple screen sizes
- Avoid overly busy or distracting gradients
- Use subtle gradients for professional look

## Related

- [Superhero Default with Background](/blocks/superhero/superhero-default-with-background-image.md) - With solid color
- [Superhero Default](/blocks/superhero/superhero-default.md) - Standard version
