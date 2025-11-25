---
title: Redocly API Block - External API Example
description: Example of Redocly API Block with external OpenAPI specification and custom typography.
layout: none
--- 

# Redocly API Block - External API Example

Load OpenAPI specifications from external URLs and customize typography for brand consistency.

## Overview

The Redocly API Block can load OpenAPI specifications from:
- Local files (relative paths like `../../assets/openapi.yaml`)
- External URLs (remote API specifications)
- API registries (like Redocly)
- GitHub raw content URLs

This flexibility allows you to document APIs hosted elsewhere or maintain specifications in a centralized location.

You can also customize the typography to match your brand. The default font stack is:
```
adobe-clean, "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Ubuntu
```

## Syntax

```markdown
<RedoclyAPIBlock 
    src='https://example.com/openapi.yaml' 
    typography='fontFamily: `"Source Sans Pro", sans-serif`' 
/>
```

## Parameters

- **src**: URL to external OpenAPI specification
- **typography**: Custom font family and styles

## Example

This example loads the AEM Assets Author API from Adobe's API registry:

<RedoclyAPIBlock src='https://api.redocly.com/registry/bundle/adobe-developers/AEM-assets-author/stable/openapi.yaml?branch=prod' typography='fontFamily: `"Source Sans Pro", sans-serif`' />

## Best Practices

- Use HTTPS URLs for external specifications
- Ensure external APIs have CORS enabled
- Consider caching external specs for performance
- Verify external URLs are stable and maintained
- Use custom typography to match your brand

## Related

- [Redocly API Block Default](/blocks/redoclyapiblock/redocly-api-block-default.md) - Local specifications
- [Redocly API Block Configs](/blocks/redoclyapiblock/redocly-api-block-configs.md) - All configuration options