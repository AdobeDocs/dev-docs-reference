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

You can also customize the typography to match your brand. The default font stack includes system fonts for optimal rendering across platforms.

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

This example loads an API specification from an external registry:

<RedoclyAPIBlock src='https://petstore3.swagger.io/api/v3/openapi.json' typography='fontFamily: `"Source Sans Pro", sans-serif`' />