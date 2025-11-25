---
title: Superhero - Half Width with Background and Video
description: Split-screen superhero with full-width background image and video content.
---

# Superhero - Half Width with Background and Video

The half width variant with background image and video creates a dynamic, engaging hero with a background image and video content.

## Overview

This variant is best suited for:
- Product demonstrations
- Feature showcases with motion
- Interactive application previews
- Dynamic marketing pages

## Syntax

```markdown
<Superhero slots="fullWidthBackground, video, heading, text, buttons" variant="halfWidth" textColor="white" overGradient />

![Background image](path/to/background.png)

[video_url](https://video-url.mp4)

# Your Heading

Your text here

* [Button 1](url)
* [Button 2](url)
```

## Parameters

- **variant**: Set to `"halfWidth"` for split layout

- **slots**: Content structure
  - `"fullWidthBackground"`: Background image spanning full width
  - `"video"`: Video content (replaces image)
  - `"heading"` (required): Main heading
  - `"text"` (required): Descriptive text
  - `"buttons"` (optional): Call-to-action buttons

- **textColor**: Text color (recommended: `white` for overlay)

- **overGradient**: Improves button visibility over background

## Example

<Superhero slots="fullWidthBackground, video, heading, text, buttons" variant="halfWidth" textColor="white" overGradient />

![Gradient background transitioning from pink at the top to blue at the bottom, with no visible objects or text.](../../assets/vertical-gradient.png)

[video_url](https://main--adp-devsite--adobedocs.aem.page/test/melissa/superhero/media_18687901ae5613eb6494cfe0da186a541403e0feb.mp4)

# Build add-ons for a global creative community.

[Adobe Express](https://adobe.com/express) is an AI-first all-in-one app to easily create and share standout content. Make tools and integrations for users that extend the functionality of Adobe Express.

* [Get started](https://developer.adobe.com/express/add-ons/docs/guides?aio_external)
* [Explore add-ons](https://new.express.adobe.com/add-ons)

## Video Setup

To add a video:
1. Upload video to Google Drive or hosting service
2. Publish the video and get the public URL
3. Add as markdown link in the `video` slot: `[video_url](https://url-to-video.mp4)`

## Best Practices

- Use short, engaging videos (15-30 seconds)
- Ensure video works on mobile devices
- Optimize video file size for fast loading
- Consider autoplay behavior and user experience
- Provide fallback for users who prefer reduced motion

## Related

- [Superhero Half Width with Background Image](/blocks/superhero/superhero-halfwidth-with-background-image.md) - With static image
- [Superhero Half Width](/blocks/superhero/superhero-halfwidth.md) - Basic version