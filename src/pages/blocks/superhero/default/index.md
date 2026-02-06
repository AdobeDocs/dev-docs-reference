---
title: Superhero - Default Variant
description: Basic hero used for Documentation pages.
---

# Superhero - Default Variant

Basic hero used for Documentation pages.

## Syntax

```markdown
<Superhero slots="heading, text" />

# Page Heading

This is a sample description text for the superhero block.

```

## Parameters

- **slots**: 
  - `heading` (required)
  - `text` (required)
  - `image` (optional): Background image
  - `icon` (optional): Filename from the [icons directory](https://github.com/AdobeDocs/adp-devsite/tree/stage/hlx_statics/icons). If unavailable, please contact the dev-site team to upload.
  - `buttons` (optional)
- **background**: Background color (default: `rgb(29, 125, 238)`)
- **textColor**: Text color. Options: `black`, `white`, `gray`, `navy` (default: `white`)

<Superhero slots="heading, text" />

# Page Heading

This is a sample description text for the superhero block.
