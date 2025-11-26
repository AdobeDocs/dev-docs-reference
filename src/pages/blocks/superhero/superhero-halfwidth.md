---
title: Superhero - Half Width Variant
description: Split-screen superhero layout with image and content side-by-side for product pages.
---

# Superhero - Half Width Variant

The half width variant creates a split-screen layout with an image on one side and content on the other, ideal for product and platform pages.

## Overview

This variant is best suited for:
- Product pages
- Platform landing pages
- Feature showcases
- Application overviews

## Syntax

```markdown
<Superhero slots="image, heading, text, buttons" variant="halfWidth" />

![Hero image](path/to/image.png)

# Your Heading

Your descriptive text here.

* [Button](url)
```

## Parameters

- **variant**: Set to `"halfWidth"` for split layout

- **slots**: Content structure
  - `"heading"` (required): Main heading
  - `"text"` (required): Descriptive text
  - `"image"` or `"video"` (required): Visual element
  - `"fullWidthBackground"` (optional): Full-width background option
  - `"buttons"` (optional): Call-to-action buttons

- **background**: Custom background color (default: `rgb(255, 255, 255)`)

- **textColor**: Text color (default: black)
  - Options: `white`, `black`, `navy`, `gray`

- **overGradient**: Improves button visibility against gradient backgrounds

## Example

<Superhero slots="image, heading, text, buttons" variant="halfWidth" />

![Hero banner](../../assets/hero.png)

# Extend Your Application

Build powerful extensions and integrations with our developer platform. Create custom tools, automate workflows, and seamlessly integrate with existing systems using our comprehensive APIs and SDKs.

* [Get Started](https://example.com/getting-started)

## Best Practices

- Use images that complement rather than compete with text
- Keep text concise to fit the half-width layout
- Choose images with clear focal points
- Consider using video for dynamic content
- Test layout on mobile where it stacks vertically
