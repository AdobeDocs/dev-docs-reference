---
title: Resources Block with Hero
description: Display a resources section with links alongside a hero banner for an engaging landing page.
---

# Resources Block with Hero

Combine a hero banner with a resources section to display key documentation links.

## Syntax

### Hero Component

```markdown
<Superhero slots="image, heading, text, buttons" background="rgb(22, 49, 42)"/>
```

### Resources Component

```markdown
<Resources slots="heading, links"/>
```

## Example

<Superhero slots="image, heading, text, buttons" background="rgb(22, 49, 42)"/>

![Hero image](../../../assets/hero.png)

# Adobe Photoshop and Lightroom API

Unlock the potential of Photoshop, Lightroom, and cutting edge Sensei services through an easy-to-use RESTful API.

* [Get the SDKs](https://developer.adobe.com/console/servicesandapis/ae)

# Resources Example With Hero

<Resources slots="heading, links"/>

#### Resources

* [Quick start guide](getting-started/index.md)
* [Endpoint guides](endpoints/index.md)
* [API reference](https://github.com/AdobeDocs/data-collection-apis)
* [Github repository](https://github.com/AdobeDocs/data-collection-apis)

## Best Practices

- Keep resource links concise and clearly labeled
- Link to the most important resources first
- Use hero to introduce the product or API

## Related

- [Resources without Hero](/blocks/resources/resources-with-no-hero.md) - Simpler layout
- [Superhero](/blocks/superhero/index.md) - Hero banner component
- [DiscoverBlock](/blocks/discoverblock/index.md) - Card-based content display

