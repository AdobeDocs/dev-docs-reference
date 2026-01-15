---
title: Superhero - Half Width Variant
description: Hero with content and image side-by-side used for Product/Platform authored pages.
---

# Superhero - Half Width Variant

Hero with content and image side-by-side used for Product/Platform authored pages.

## Syntax

```markdown
<Superhero slots="image, heading, text, buttons" variant="halfWidth" />

![Hero image](../../../assets/cc-hero.png)

# Extend Your Application

Build powerful extensions and integrations with our developer platform. Create custom tools, automate workflows, and seamlessly integrate with existing systems using our comprehensive APIs and SDKs.

* [Get Started](https://example.com/getting-started)
```

## Parameters

- **variant**: `"halfWidth"`
- **slots**: 
  - `heading` (required)
  - `text` (required)
  - `image` or [`video`](../../../faq/index.md#where-can-i-upload-videos) (required): Right-side media
  - `fullWidthBackground` (optional): Background image
  - `icon` (optional): Filename from the [icons directory](https://github.com/AdobeDocs/adp-devsite/tree/stage/hlx_statics/icons). If unavailable, please contact the dev-site team to upload.
  - `buttons` (optional)

- **background**: Background color (default: `rgb(255, 255, 255)`)
- **textColor**: Text color. Options: `black`, `white`, `gray`, `navy` (default: `black`)
- **overGradient**: Improves button visibility over a gradient background


<Superhero slots="image, heading, text, buttons" variant="halfWidth" />

![Hero image](../../../assets/cc-hero.png)

# Extend Your Application

Build powerful extensions and integrations with our developer platform. Create custom tools, automate workflows, and seamlessly integrate with existing systems using our comprehensive APIs and SDKs.

* [Get Started](https://example.com/getting-started)
