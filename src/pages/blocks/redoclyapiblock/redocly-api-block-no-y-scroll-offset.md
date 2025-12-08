---
title: Redocly API Block - With Y-Scroll Offset
description: Redocly API Block configured with a vertical scroll offset for fixed headers.
layout: none
--- 

# Redocly API Block - With Y-Scroll Offset

Configure the Redocly API Block with a vertical scroll offset to account for fixed headers or navigation elements.

## Overview

The `scrollYOffset` parameter adjusts scroll behavior when navigating to anchors within the API documentation (default: `0`). Setting a scroll offset is essential when you have:
- Fixed top navigation bars
- Sticky headers
- Floating UI elements at the top of the page

Without this offset, anchor links might scroll content underneath fixed elements, making it partially hidden.

## Syntax

```markdown
<RedoclyAPIBlock src="path/to/openapi.yaml" scrollYOffset={64} />
```

## Parameters

- **src**: Path to OpenAPI specification file
- **scrollYOffset**: Pixel value for scroll offset (typically the height of your fixed header)

## Example

<RedoclyAPIBlock src="../../assets/openapi.yaml" />
