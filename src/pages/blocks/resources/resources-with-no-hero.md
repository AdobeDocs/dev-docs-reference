---
title: Resources Block without Hero
description: Display a resources section with useful links without a hero banner for a simpler layout.
---

# Resources Block without Hero

Display a clean resources section with links to documentation and references.

## Syntax

```markdown
<Resources slots="heading, links"/>

#### Resources

* [Link 1](url)
* [Link 2](url)
```

## Parameters

- **slots**: Define content structure
  - `"heading, links"`: Heading and list of links

<Resources slots="heading, links"/>

#### Resources

* [Quick start guide](getting-started/index.md)
* [Endpoint guides](endpoints/index.md)
* [API reference](https://example.com/api-reference)
* [GitHub repository](https://github.com/example/repo)

## Best Practices

- Use descriptive headings for resource sections
- Keep link text clear and action-oriented
- Order links by importance
