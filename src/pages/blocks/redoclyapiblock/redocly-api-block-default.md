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

- **src**: Path to OpenAPI specification file (YAML or JSON). Placement depends on file type:
  - **YAML files**: Can be under `/src/pages` (use a relative path from the current page) or in the `static/` folder (see below). Example: from `src/pages/api/reference/index.md`, a spec at `src/pages/assets/openapi.yaml` → `src="../../assets/openapi.yaml"`
  - **JSON files**: Must be in the `static/` folder only — JSON files under `/src/pages` will fail deployment.
  - **`static/` folder** (at repo root, not under `/src/pages`): Use `src="/{pathPrefix}/{pathToFileRelativeToStaticFolder}"` — the path includes pathPrefix but excludes the `static` segment.  

## Default Settings

- Width: 500px
- Sidebar navigation enabled
- Search enabled
- Try-it-out panel enabled
- JSON samples expanded to 2 levels

## Examples

**Relative path** (YAML under `/src/pages`): From a page at `api/reference/index.md`, referencing `assets/openapi.yaml`:

```markdown
<RedoclyAPIBlock src="../../assets/openapi.yaml" />
```

**Static folder** (pathPrefix format): For `static/petstore.json` with pathPrefix `my-product`:

```markdown
<RedoclyAPIBlock src="/my-product/petstore.json" />
```

<RedoclyAPIBlock src="../../assets/openapi.yaml" />
