---
title: Columns Block
description: Create multi-column layouts for content organization using the Columns block.
---

# Columns Block

Multi-column layouts for side-by-side content.

## Syntax

```markdown
<Columns slots="image, heading, text, buttons" repeat="2" />

![Image 1](path/to/image1.jpg)

### Column One

Description text.

[Link text](https://example.com)

![Image 2](path/to/image2.jpg)

### Column Two

Description text.

[Link text](https://example.com)

```

## Parameters

- **slots**: Content per column
  - `"heading, text"` - Text only
  - `"image, heading, text"` - With image
  - `"image, heading, text, buttons"` - With image and links
  - `"video, heading, text"` - With video
  - `"video, heading, text, buttons"` - With video and links

- **repeat**: Number of columns (2-4)

- **Image size**: 580 x 350 px recommended

