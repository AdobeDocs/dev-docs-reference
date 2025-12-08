---
title: Redocly API Block - Default
description: Default configuration of the Redocly API Block for displaying interactive API documentation.
---

# Redocly API Block - Default

Display interactive API documentation from OpenAPI specification files.

## Syntax

```markdown
<RedoclyAPIBlock src="path/to/openapi.yaml" />
```

## Parameters

- **src**: Path to OpenAPI specification file (YAML or JSON)

## Default Settings

- Width: 500px
- Sidebar navigation enabled
- Search enabled
- Try-it-out panel enabled
- JSON samples expanded to 2 levels

## Example

<RedoclyAPIBlock src="../../assets/openapi.yaml" />
