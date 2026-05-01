---
title: Embed Block
description: Learn how to use the Embed block to integrate videos, social media posts, and other external media directly into your documentation.
---

# Embed Block

The Embed block allows you to display videos and social media posts directly on your page. It supports a variety of platforms and automatically selects the appropriate player based on the provided URL.

## Syntax

Standard video

```markdown
<Embed slots="video" />

https://your-media-link.com
```

Short-form video new

```markdown
<Embed slots="video" short="true"/>

https://your-media-link.com
```

## Parameters

- **slots**:
  - `"video"` - A slot for the URL of the media you wish to embed.

- **short**
  - `"true"` - An attribute displays the video in a short-form (vertical) format, similar to YouTube Shorts or Instagram Reels.

<InlineAlert slots="text" />

When using a `youtube.com/shorts/` URL, the block automatically detects it as a Short. Use `short="true"` explicitly when the URL does not include `/shorts/` in the path.

## Supported Platforms

The block automatically detects and handles links from the following sources:

- Video Services: YouTube (including Shorts and Playlists), Vimeo.
- Social Media: Instagram (Reels and Posts), TikTok, X (formerly Twitter).
- Direct Files: MP4 video files.
- Generic: Other URLs will attempt to use a default iframe embed.

## Examples

#### Standard YouTube video

<Embed slots="video" />

https://www.youtube.com/embed/4haZJxpf9Bo?si=9Pfm0yJD_62ZQnqg

#### Short-form video

<Embed slots="video" short="true"/>

https://www.youtube.com/embed/76hGc6mlSSA

#### YouTube Shorts URL

<Embed slots="video" />

https://youtube.com/shorts/BwjjMllBahU?si=NkufHO7QIoHbFELP
