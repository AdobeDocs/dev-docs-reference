---
title: Superhero - Centered XL Variant
description: Extra-large centered superhero layout for maximum visual impact on index home pages.
---

# Superhero - Centered XL Variant

The centered XL variant creates an extra-large, visually dominant hero banner with centered content for maximum impact on landing pages.

## Overview

This variant is best suited for:
- Main portal home pages
- High-impact marketing pages
- Brand showcases
- Major product launches

## Syntax

```markdown
<Superhero slots="image, heading, text, buttons" variant="centeredXL" background="rgb(51, 51, 51)" />

![Hero image](path/to/image.png)

# Your Heading

Your text here

* [Button 1](url)
* [Button 2](url)
```

## Parameters

- **variant**: Set to `"centeredXL"` for extra-large centered layout

- **slots**: Content structure
  - `"heading"` (required): Main heading
  - `"text"` (required): Descriptive text
  - `"image"` (optional): Hero image
  - `"buttons"` (optional): Call-to-action buttons

- **background**: Custom background color (default: `rgb(29, 125, 238)`)

- **textColor**: Text color (default: white)
  - Options: `white`, `black`, `navy`, `gray`

## Example

<Superhero slots="image, heading, text, buttons" variant="centeredXL" background="rgb(51, 51, 51)" />

![Hero banner](../../assets/hero.png)

# Build Amazing Digital Experiences

Unleash your developer creativity with our powerful platform and tools

* [Explore our APIs](https://example.com/api)
* [Get Started](https://example.com/getting-started)

## Best Practices

- Reserve for most important pages only
- Use compelling, high-resolution images
- Keep messaging bold and concise
- Ensure typography scales well at large sizes
- Test on various screen sizes for responsiveness

