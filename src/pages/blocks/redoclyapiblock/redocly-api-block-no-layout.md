---
title: Redocly API Block - No Layout
description: Redocly API Block displayed without a layout wrapper for full-page API documentation.
layout: none
--- 

# Redocly API Block - No Layout

Display the Redocly API Block without the standard page layout wrapper, creating a full-page, immersive API documentation experience.

## Overview

Setting `layout: none` in the frontmatter removes the typical page layout elements (header, footer, sidebars), allowing the API documentation to occupy the full viewport. This is ideal for:
- Dedicated API reference pages
- Standalone API documentation
- Embedded documentation in external sites

## Syntax

Add `layout: none` to the page frontmatter:

```markdown
---
title: Your Page Title
layout: none
---

<RedoclyAPIBlock src="path/to/openapi.yaml" scrollYOffset={64} />
```

## Parameters

- **src**: Path to OpenAPI specification file
- **scrollYOffset**: Offset in pixels for fixed headers (optional)

## Example

<RedoclyAPIBlock src="../../assets/openapi.yaml" scrollYOffset={64} />

## Best Practices

- Use for dedicated API reference pages
- Set scrollYOffset when you have fixed headers
- Consider removing navigation elements for cleaner focus
- Test on different screen sizes for responsive design

## Related

- [Redocly API Block Default](/blocks/redoclyapiblock/redocly-api-block-default.md) - With standard layout
- [Redocly API Block Configs](/blocks/redoclyapiblock/redocly-api-block-configs.md) - Configuration options
