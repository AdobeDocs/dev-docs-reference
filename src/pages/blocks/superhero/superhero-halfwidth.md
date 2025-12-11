---
title: Superhero - Half Width Variant
description: Split-screen superhero layout with image and content side-by-side for product pages.
---

# Superhero - Half Width Variant

Hero with content and image side-by-side used for Product/Platform authored pages.

## Syntax

```markdown
<Superhero slots="image, heading, text, buttons" variant="halfWidth" />

![Hero image](../../assets/cc-hero.png)

# Extend Your Application

Build powerful extensions and integrations with our developer platform. Create custom tools, automate workflows, and seamlessly integrate with existing systems using our comprehensive APIs and SDKs.

* [Get Started](https://example.com/getting-started)
```

## Parameters

- **variant**: `"halfWidth"`
- **slots**: 
  - `heading` (required)
  - `text` (required)
  - `image` or `video` (required): Right-side image
    - `video`: Upload to Google drive, publish, then use the URL
  - `fullWidthBackground` (optional): Background image
  - `buttons` (optional)

- **background**: Background color (default: `rgb(255, 255, 255)`)
- **textColor**: Text color (default: `black`)
- **overGradient**: Improves button visibility over a gradient background


<Superhero slots="image, heading, text, buttons" variant="halfWidth" />

![Hero image](../../assets/cc-hero.png)

# Extend Your Application

Build powerful extensions and integrations with our developer platform. Create custom tools, automate workflows, and seamlessly integrate with existing systems using our comprehensive APIs and SDKs.

* [Get Started](https://example.com/getting-started)
