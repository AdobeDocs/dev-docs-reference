---
title: Superhero - Default Variant
description: Standard superhero layout for documentation pages with heading and text.
---

# Superhero - Default Variant

The default superhero variant provides a standard hero banner layout ideal for documentation pages and product introductions.

## Overview

This variant is best suited for:
- Documentation home pages
- API landing pages
- Product introductions
- Getting started pages

## Syntax

```markdown
<Superhero slots="heading, text" />

# Your Heading

Your descriptive text here.
```

## Parameters

- **slots**: Content structure
  - `"heading"` (required): Main heading
  - `"text"` (required): Descriptive text
  - `"image"` (optional): Hero image
  - `"buttons"` (optional): Call-to-action buttons

- **background**: Custom background color (default: `rgb(29, 125, 238)`)
  - Example: `background="rgb(22, 49, 42)"`

- **textColor**: Text color (default: white)
  - Options: `white`, `black`, `navy`, `gray`

## Example

<Superhero slots="heading, text" />

# Adobe Photoshop and Lightroom API

Unlock the potential of Photoshop, Lightroom, and cutting edge Sensei services through an easy-to-use RESTful API.

## Best Practices

- Keep heading clear and focused (5-10 words)
- Use descriptive text to expand on the heading (1-2 sentences)
- Choose background colors that align with your brand
- Ensure text color has sufficient contrast with background

## Related

- [Superhero Half Width](/blocks/superhero/superhero-halfwidth.md) - Split layout variant
- [Superhero Centered](/blocks/superhero/superhero-centered.md) - Centered layout