---
title: Superhero - Half Width with Background Image
description: Split-screen superhero with full-width background image and foreground content image.
---

# Superhero - Half Width with Background Image

The half width variant with background image creates a layered visual effect with a full-width background and split-screen content.

## Overview

This variant is best suited for:
- Premium product pages
- Brand-focused landing pages
- Creative showcases
- Applications with strong visual identity

## Syntax

```markdown
<Superhero slots="fullWidthBackground, image, heading, text, buttons" variant="halfWidth" textColor="white" overGradient />

![Background image](path/to/background.png)

![Foreground image](path/to/image.png)

# Your Heading

Your text here

* [Button 1](url)
* [Button 2](url)
```

## Parameters

- **variant**: Set to `"halfWidth"` for split layout

- **slots**: Content structure
  - `"fullWidthBackground"`: Background image spanning full width
  - `"image"`: Foreground content image
  - `"heading"` (required): Main heading
  - `"text"` (required): Descriptive text
  - `"buttons"` (optional): Call-to-action buttons

- **textColor**: Text color (recommended: `white` for overlay)

- **overGradient**: Improves button visibility over background

## Example

<Superhero slots="fullWidthBackground, image, heading, text, buttons" variant="halfWidth" textColor="white" overGradient />

![Gradient background](../../assets/vertical-gradient.png)

![Platform illustration](../../assets/cc-hero.png)

# Build Extensions for Your Users

Create powerful tools and integrations that extend platform functionality and help users accomplish more with seamless workflows.

* [Get Started](https://example.com/getting-started)
* [View Examples](https://example.com/examples)
