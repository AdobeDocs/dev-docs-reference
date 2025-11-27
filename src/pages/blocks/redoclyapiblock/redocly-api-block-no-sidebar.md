---
title: Redocly API Block - No Sidebar
description: Redocly API Block with the sidebar navigation disabled for a streamlined view.
---

# Redocly API Block - No Sidebar

Display the Redocly API Block without the left sidebar navigation, providing a streamlined, full-width documentation view.

## Overview

By default, the Redocly API Block shows a left sidebar with navigation (`disableSidebar: false`). Setting `disableSidebar` to `true` or using the `disableSidebar` attribute removes the left navigation panel that typically shows API endpoints and tags. This is useful for:
- Simple APIs with few endpoints
- Cleaner, more focused documentation
- Maximizing content width
- Custom navigation implementations

## Syntax

```markdown
<RedoclyAPIBlock src="path/to/openapi.yaml" disableSidebar />
```

## Parameters

- **src**: Path to OpenAPI specification file
- **disableSidebar**: Boolean flag to hide the sidebar

## Example

<RedoclyAPIBlock src="../../assets/openapi.yaml" disableSidebar />

## Best Practices

- Use for APIs with limited endpoints
- Combine with search disabled for even cleaner layout
- Consider if users need quick navigation between endpoints
- Good for sequential documentation reading
