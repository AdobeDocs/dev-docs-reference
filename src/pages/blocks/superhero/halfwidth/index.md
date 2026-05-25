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

# Page Heading

This is a sample description text for the superhero block.

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

- **Video playback** (optional, when `video` is in `slots`): Add any of these as boolean attributes on the opening `<Superhero>` tag (no value)
  - **controls** — Present to show the default browser video controls.
  - **autoplay** — Start playback when the hero loads.
  - **loop** — Repeat the video when it ends.

**Example :**

```markdown
<Superhero slots="video, heading, text, buttons" variant="halfWidth" textColor="black" overGradient controls autoplay loop/>

[video_url](https://example.com/path/to/video.mp4)

# Build Extensions for Your Users

Create powerful tools and integrations.

* [Get Started](https://example.com/getting-started)
* [View Examples](https://example.com/examples)
```

For a hero with a **background image** and video together, see [Half Width with Background Image and Video](with-background-image-and-video.md).
