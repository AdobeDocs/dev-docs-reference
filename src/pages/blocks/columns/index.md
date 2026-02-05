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

- **slots**:
  - `image` / `video` (required)
  - `image` — Use Markdown image syntax: `![alt text](url)`. Supports absolute and relative URLs.
  - `video` — Use Markdown link syntax: `[video](url)`. Must be an absolute URL.
  - `heading` (optional)
  - `text` (optional)
  - `buttons` (optional)

- **repeat**: Number of columns (2-4)

- **Image size**: 580 x 350 px recommended

