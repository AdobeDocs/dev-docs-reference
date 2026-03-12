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

- **src**: Path to OpenAPI specification file (YAML or JSON). The file can be placed in either location:
  - **Under `/src/pages`**: Use a relative path (e.g., `../../assets/openapi.yaml`).
  - **In the `static/` folder** (legacy, at repo root, not under `/src/pages`): Use `src="/{pathPrefix}/{pathToFileRelativeToStaticFolder}"` — the path includes pathPrefix but excludes the `static` segment.  

## Default Settings

- Width: 500px
- Sidebar navigation enabled
- Search enabled
- Try-it-out panel enabled
- JSON samples expanded to 2 levels

## Example

<RedoclyAPIBlock src="../../assets/openapi.yaml" />
