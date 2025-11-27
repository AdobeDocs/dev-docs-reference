---
title: Redocly API Block - No Sidebar No Search
description: Redocly API Block with both sidebar navigation and search functionality disabled.
---

# Redocly API Block - No Sidebar No Search

Display the Redocly API Block with both sidebar navigation and search functionality disabled for a minimalist documentation experience.

## Overview

By default, both sidebar and search are enabled (`disableSidebar: false`, `disableSearch: false`). Combining `disableSidebar` and `disableSearch` attributes creates the most streamlined documentation view. This is ideal for:
- Very simple APIs with minimal endpoints
- Embedded documentation in custom pages
- Print-friendly documentation
- Linear reading experiences

## Syntax

```markdown
<RedoclyAPIBlock src="path/to/openapi.yaml" disableSidebar disableSearch />
```

## Parameters

- **src**: Path to OpenAPI specification file
- **disableSidebar**: Hide the left navigation sidebar
- **disableSearch**: Disable the search functionality

## Example

<RedoclyAPIBlock src="../../assets/openapi.yaml" disableSidebar disableSearch />

## Best Practices

- Use only for very simple APIs
- Ensure content is logically organized for linear reading
- Consider alternative navigation methods if needed
- Good for documentation that will be read sequentially
