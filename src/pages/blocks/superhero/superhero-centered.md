---
title: Superhero - Centered Variant
description: Centered superhero layout with image and buttons for index home pages.
---

# Superhero - Centered Variant

The centered variant creates a visually balanced hero banner with centered content, perfect for high-impact landing pages and home pages.

## Overview

This variant is best suited for:
- Index home pages
- Marketing landing pages
- Product showcases
- Main portal pages

## Syntax

```markdown
<Superhero slots="image, heading, text, buttons" variant="centered" textColor="white"/>

![Hero image](path/to/image.png)

## Your Heading

Your text here

* [Button 1](url)
* [Button 2](url)
```

## Parameters

- **variant**: Set to `"centered"` for centered layout

- **slots**: Content structure
  - `"heading"` (required): Main heading
  - `"text"` (required): Descriptive text
  - `"image"` (optional): Hero image
  - `"buttons"` (optional): Call-to-action buttons

- **background**: Custom background color (default: `rgb(29, 125, 238)`)

- **textColor**: Text color (default: white)
  - Options: `white`, `black`, `navy`, `gray`

## Example

<Superhero slots="image, heading, text, buttons" variant="centered" textColor="white"/>

![Hero image](../../assets/hero.png)

## Build Amazing Digital Experiences

Unleash your developer creativity with our powerful platform and tools

* [Explore our APIs](https://example.com/api) 
* [Get Started](https://example.com/getting-started)