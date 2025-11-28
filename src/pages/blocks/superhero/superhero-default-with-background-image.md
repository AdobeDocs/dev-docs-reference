---
title: Superhero - Default with Background Image
description: Standard superhero layout with custom background image for visual impact.
---

# Superhero - Default with Background Image

The default variant with a background image combines standard layout with visual interest through a custom background.

## Overview

This variant is best suited for:
- Documentation pages with branding
- Product pages with thematic backgrounds
- Landing pages with visual context
- Pages requiring visual hierarchy

## Syntax

```markdown
<Superhero slots="image, heading, text, buttons" background="rgb(22, 49, 42)"/>

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

- **background**: Custom background color
  - Format: `rgb(r, g, b)` or hex color
  - Example: `background="rgb(22, 49, 42)"`

- **textColor**: Text color (default: white)
  - Options: `white`, `black`, `navy`, `gray`

## Example

<Superhero slots="image, heading, text, buttons" background="rgb(22, 49, 42)"/>

![Hero image](../../assets/hero.png)

# Developer Platform API

Build powerful applications with our comprehensive API platform and services.

* [Get Started](https://example.com/getting-started)
