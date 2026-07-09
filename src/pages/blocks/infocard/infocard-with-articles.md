---
title: InfoCard Block with Articles
description: Displays large info cards generated from article links using the article's image, title, and description.
---

# InfoCard Block with Articles

The InfoCard Block with Articles automatically generates info cards from the provided article links. Each card displays the article's image, title, and description.

## Syntax

```markdown
<InfoCard slots="articles" wide />

- [Blog 1](https://blog-link)
- [Blog 2](https://blog-link)
```

## Parameters

- **slots**: Defines the content structure for the InfoCard block.
  - `"articles"` - Automatically generates info cards from the metadata of the provided article links.

- **wide**: By default, images are displayed with a 4:3 aspect ratio. Add the `wide` attribute to display images with a 16:9 aspect ratio.

## Content Structure

The `articles` slot accepts a list of article URLs. The InfoCard block automatically retrieves the article metadata, including the image, title, and description, and displays it as an info card.

## Example

<InfoCard slots="articles" wide />

- [Blog 1](https://blog.developer.adobe.com/en/publish/2026/05/how-to-get-your-adobe-express-add-on-approved-avoiding-the-most-common-rejections)
- [Blog 2](https://blog.developer.adobe.com/en/publish/2026/05/help-your-adobe-express-add-on-reach-enterprise-users-with-granular-admin-approvals)
