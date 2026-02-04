---
title: Superhero - Centered XL Variant
description: Extra-large centered hero used for Index home pages.
---

# Superhero - Centered XL Variant

Extra-large centered hero used for Index home pages.

## Syntax

```markdown
<Superhero slots="image, heading, text, buttons" variant="centeredXL" background="rgb(51, 51, 51)" />

![Hero banner](../../../assets/hero.png)

# Page Heading

This is a sample description text for the superhero block.

* [Explore our APIs](https://example.com/api)
* [Get Started](https://example.com/getting-started)
```

## Parameters

- **variant**: `"centeredXL"`
- **slots**: 
  - `heading` (required)
  - `text` (required)
  - `image` (optional): Background image
  - `icon` (optional): Filename from the [icons directory](https://github.com/AdobeDocs/adp-devsite/tree/stage/hlx_statics/icons). If unavailable, please contact the dev-site team to upload.
  - `buttons` (optional)
- **background**: Background color (default: `rgb(29, 125, 238)`)
- **textColor**: Text color. Options: `black`, `white`, `gray`, `navy` (default: `white`)

<Superhero slots="image, heading, text, buttons" variant="centeredXL" background="rgb(51, 51, 51)" />

![Hero banner](../../../assets/hero.png)

# Page Heading

This is a sample description text for the superhero block.

* [Explore our APIs](https://example.com/api)
* [Get Started](https://example.com/getting-started)
