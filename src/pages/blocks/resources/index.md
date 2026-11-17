---
title: Resources Block
description: Display a resources section with useful links.
---

# Resources Block

Resource links displayed on the right side of the page, above "On This Page" if present.

## Syntax

```markdown
<Resources slots="heading, links"/>

#### Resources

* [Quick start guide](getting-started/index.md)
* [Endpoint guides](https://developer.adobe.com/dev-docs-reference/blocks/resources/endpoints/)
* [API reference](../redoclyapiblock/redocly-api-block-default.md?aio_external)
* [GitHub repository](https://github.com/example/repo)
```

## Parameters

- **slots**: `"heading, links"` - Heading and links

Absolute URLs to internal Adobe developer pages open in the same tab without an external-link icon. Add `?aio_external` to a relative URL to open it in a new tab with the icon.

<Resources slots="heading, links"/>

#### Resources

* [Quick start guide](getting-started/index.md)
* [Endpoint guides](https://developer.adobe.com/dev-docs-reference/blocks/resources/endpoints/)
* [API reference](../redoclyapiblock/redocly-api-block-default.md?aio_external)
* [GitHub repository](https://github.com/example/repo)

