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

![Creative Cloud banner](../../assets/cc-hero.png)

#  Extend the Power of After Effects

Opportunities abound for building for After Effects. Extend the capabilities of After Effects using plug-ins, scripts, and panels that integrate seamlessly into existing workflows. Create stunning visual effects, manipulate project elements, and automate complex tasks using After Effects APIs.

* [Get the SDKs](https://developer.adobe.com/console/servicesandapis/ae)

## Best Practices

- Use images that complement rather than compete with text
- Keep text concise to fit the half-width layout
- Choose images with clear focal points
- Consider using video for dynamic content
- Test layout on mobile where it stacks vertically

## Related

- [Superhero Half Width with Background Image](/blocks/superhero/superhero-halfwidth-with-background-image.md) - With background
- [Superhero Default](/blocks/superhero/superhero-default.md) - Full-width layout
