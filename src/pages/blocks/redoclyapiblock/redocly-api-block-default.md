---
title: Redocly API Block - Default
description: Default configuration of the Redocly API Block for displaying interactive API documentation.
---

# Redocly API Block - Default

The Redocly API Block component renders interactive API documentation from OpenAPI specification files, providing a rich, user-friendly interface for exploring APIs.

## Overview

This component transforms OpenAPI (Swagger) specification files into beautiful, interactive documentation with features like:
- Automatic endpoint navigation with left sidebar
- Interactive API explorer with try-it-out functionality
- Code samples in multiple languages
- Search functionality for quick access
- Customizable styling and behavior

## Default Behavior

The default configuration includes:
- Width: 500px
- Sidebar navigation enabled
- Search enabled
- Try-it-out panel enabled
- JSON samples expanded to 2 levels
- Adobe Clean font stack

## Syntax

```markdown
<RedoclyAPIBlock src="path/to/openapi.yaml" />
```

## Parameters

- **src**: Path to your OpenAPI specification file (YAML or JSON)

## Example

<RedoclyAPIBlock src="../../assets/openapi.yaml" />

## Best Practices

- Use valid OpenAPI 3.0+ specification files
- Keep your OpenAPI spec well-organized with clear descriptions
- Provide examples in your specification for better documentation
- Use relative paths for local OpenAPI files

## Related

- [Redocly API Block Configs](/blocks/redoclyapiblock/redocly-api-block-configs.md) - Custom configuration options
- [Redocly API Block No Sidebar](/blocks/redoclyapiblock/redocly-api-block-no-sidebar.md) - Without sidebar navigation
