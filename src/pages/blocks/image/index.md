---
title: Image
description: Learn how to display and format images in your documentation.
---

# Image

Display images in your documentation using standard Markdown syntax. Use a plain Markdown image by default. To limit how wide an image displays, for example to keep a small screenshot or diagram from stretching across the page, wrap it in the optional Image block.

## Syntax

**Markdown image:**
```markdown
![Alt text](path/to/image.png)
```

**Image block:**
```markdown
<Image slots="image" maxWidth="medium" />

![Alt text](path/to/image.png)
```

## Parameters

These parameters apply to the Image block. Plain Markdown images don't take parameters; see [Image guidelines](#image-guidelines) for guidance that applies to both.

- **slots**: `image` (required). Put a standard Markdown image after the tag, with a blank line between them.
- **maxWidth** (optional): The widest the image displays. Without it, the image displays like a plain Markdown image.
  - `small`: 300px
  - `medium`: 500px
  - `large`: 600px
  - A custom positive value in `px`, `%`, or `rem`, for example `550px`, `90%`, or `34.375rem`. Decimals are allowed. On this site, `1rem` is `14px`.

`maxWidth` is a limit, not a fixed width. The image keeps its aspect ratio, shrinks to fit smaller screens, and is never enlarged beyond its original size. Unsupported values, such as a number without a unit, are ignored, and the image displays at the default width.

In the Image block, put the alt text and an optional link on the Markdown image, as you would for a plain image.

The Image block must be at the top level of the page. It doesn't work inside lists, tables, or other blocks.

## Image guidelines

These apply to both plain Markdown images and images in an Image block.

- **Alt text**: Descriptive text for accessibility (required)
- **Path**: Relative path to assets folder or absolute URL
- **Formats**: PNG, JPG, GIF, WebP, SVG

## File size limits

- **SVG**: keep under **40 KB**.
- **PNG / JPG / GIF / WebP**: keep under **20 MB**.  

Files larger than the suggested size will fail to deploy and render via EDS' image pipeline.

## Examples

### Plain image

```markdown
![Two pink and white flowers with water drops](../../assets/image2.jpeg)
```

![Two pink and white flowers with water drops](../../assets/image2.jpeg)

### Image block with a preset

```markdown
<Image slots="image" maxWidth="medium" />

![Two pink and white flowers with water drops](../../assets/image2.jpeg)
```

<Image slots="image" maxWidth="medium" />

![Two pink and white flowers with water drops](../../assets/image2.jpeg)

### Image block with a custom value

```markdown
<Image slots="image" maxWidth="550px" />

![Two pink and white flowers with water drops](../../assets/image2.jpeg)
```

<Image slots="image" maxWidth="550px" />

![Two pink and white flowers with water drops](../../assets/image2.jpeg)
