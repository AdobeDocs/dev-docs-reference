---
title: InfoCard Block with Video
description: Displays large info cards with a video, heading, and descriptive text.
---

# InfoCard Block with Video

The InfoCard Block displays large cards with an video at the top, followed by a heading and descriptive text.

## Syntax

```markdown
<InfoCard slots="video, heading, text" repeat="2" />

[Alt text](path/to/video.mp4)

### Heading 1

Content 1

[Alt text](path/to/video.mp4)

### [Heading 2](https://adobe.com)

Content 2
```

## Parameters

- **slots**: Defines the content structure of each info card.
  - `"video, heading, text"` - Displays an video, heading, and text.

- **repeat**: Specifies the number of info cards to display.
  - Set this value to match the number of content blocks provided.

## Content Structure

Each info card should contain the following content in the specified order:

1. **Video**: An video that represents the info card.
2. **Heading**: A heading that serves as the title of the info card. You can use the heading with or without a link. If a link is provided, the entire info card becomes clickable and navigates to the specified URL.
3. **Text**: A paragraph that describes the information, features, or benefits of the card.

## Example

<InfoCard slots="video, heading , text " repeat="2" />

[Alt video](https://youtu.be/E9atPm5djco)

### [March 18, 2026](https://events.ringcentral.com/events/office-hours-for-adobe-express-developers-march-2026)

Join our monthly Office Hours focused on Adobe Express Add-ons development and bring your questions

[Alt Video](https://youtu.be/E9atPm5djco)

### [How to Get Your Adobe Express Add-on Approved: Avoiding the Most Common Rejections](https://events.ringcentral.com/events/office-hours-for-adobe-express-developers-march-2026)

Join our monthly Office Hours focused on Adobe Express Add-ons development and bring your questions. How to Get Your Adobe Express Add-on Approved: Avoiding the Most Common Rejections
