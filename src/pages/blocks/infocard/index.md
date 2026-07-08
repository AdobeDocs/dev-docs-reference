---
title: InfoCard Block
description: Displays large info cards with an image, heading, and descriptive text.
---

# InfoCard Block

The InfoCard Block displays large cards with an image at the top, followed by a heading and descriptive text.

## Syntax

```markdown
<InfoCard slots="image, heading, text" repeat="2" />

![Alt text](path/to/image.png)

### Heading 1

Content 1

![Alt text](path/to/image.png)

### [Heading 2](https://adobe.com)

Content 2
```

## Parameters

- **slots**: Defines the content structure of each info card.
  - `"image, heading, text"` - Displays an image, heading, and text.

- **repeat**: Specifies the number of info cards to display.
  - Set this value to match the number of content blocks provided.

## Content Structure

Each info card should contain the following content in the specified order:

1. **Image**: An image that represents the info card.
2. **Heading**: A heading that serves as the title of the info card. You can use the heading with or without a link. If a link is provided, the entire info card becomes clickable and navigates to the specified URL. 
3. **Text**: A paragraph that describes the information, features, or benefits of the card.

## Example

<InfoCard slots="image, heading , text "  repeat="2" />

![Alt text](../../assets/column.jpg)

### Heading 1

This is the sample description for the info card content one. Add details about the card features, benefits, and use cases to help users understand what this product offers.

![Alt text](../../assets/column.jpg)

### [Heading 2](https://adobe.com)

This is the sample description for the info card content two. Add details about the card features, benefits, and use cases to help users understand what this product offers.