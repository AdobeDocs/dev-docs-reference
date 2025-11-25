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

![Gradient background transitioning from pink at the top to blue at the bottom, with no visible objects or text.](../../assets/vertical-gradient.png)

![Illustration of a computer monitor displaying the Adobe Creative Cloud logo, surrounded by a smartphone, tablet, cloud icon, color palette, and geometric design tools, set against a blue background.](../../assets/cc-hero.png)

# Build add-ons for a global creative community.

[Adobe Express](https://adobe.com/express) is an AI-first all-in-one app to easily create and share standout content. Make tools and integrations for users that extend the functionality of Adobe Express.

* [Get started](https://developer.adobe.com/express/add-ons/docs/guides?aio_external)
* [Explore add-ons](https://new.express.adobe.com/add-ons)

## Best Practices

- Use high-quality background images
- Ensure text is readable over background (use white text)
- Enable `overGradient` for better button contrast
- Test on various screen sizes
- Keep foreground image focused and clear

## Related

- [Superhero Half Width with Video](/blocks/superhero/superhero-halfwidth-with-background-image-and-video.md) - With video
- [Superhero Half Width](/blocks/superhero/superhero-halfwidth.md) - Without background