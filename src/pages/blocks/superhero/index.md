---
title: Superhero Block
description: Create impactful hero banners with images, headings, text, and call-to-action buttons.
---

# Superhero Block

The Superhero block creates prominent hero banners at the top of pages to capture attention and set the tone with images, headings, text, and call-to-action buttons.

## Overview

A Superhero block should be used on every home page. **Only 1 Hero block per page is allowed**.

Hero blocks are used to:
- Set the tone and purpose of the page
- Highlight key value propositions
- Provide call-to-action buttons
- Create visual impact with images or backgrounds

## Available Variants

There are 4 different variants to choose from:

- **[Default](superhero-default.md)**: Standard variant for documentation pages
- **[Half Width](superhero-halfwidth.md)**: Split layout for product/platform pages
- **[Centered](superhero-centered.md)**: Centered layout for index home pages
- **[Centered XL](superhero-centeredxl.md)**: Large centered layout for impact

## Common Parameters

All Superhero variants support these parameters:

- **slots**: Content structure
  - `"heading, text"`: Basic hero with heading and text
  - `"image, heading, text, buttons"`: Full hero with all elements

- **background**: Custom background color (default: `rgb(29, 125, 238)`)
  - Format: `rgb(r, g, b)` or hex color

- **textColor**: Text color (default: white)
  - Options: `white`, `black`, `navy`, `gray`

- **variant**: Layout variant
  - `"default"`, `"halfWidth"`, `"centered"`, `"centeredXL"`

## Best Practices

- Use only one hero block per page
- Choose the variant that matches your page type
- Keep heading text concise and impactful
- Use high-quality images that support your message
- Limit call-to-action buttons to 1-2 for focus
- Ensure sufficient contrast between text and background

## Related

- [HeroSimple](/blocks/herosimple/herosimple-default.md) - Simpler hero option
- [Resources](/blocks/resources/resources.md) - Pair hero with resource links