---
title: Embed Block
description: Learn how to use the Embed block to integrate videos, social media posts, and other external media directly into your documentation.
---

# Embed Block

The Embed block allows you to display videos and social media posts directly on your page. It supports a variety of platforms and media types, automatically selecting the appropriate player based on the provided URL.

## Syntax

```markdown
<Embed slots="video" />

https://your-media-link.com
```

## Parameters

- **slots**:
  - `"video"` - A slot for the URL of the media you wish to embed.

## Supported Platforms

The block automatically detects and handles links from the following sources:

- Video Services: YouTube (including Shorts and Playlists), Vimeo.
- Social Media: Instagram (Reels and Posts), TikTok, X (formerly Twitter).
- Direct Files: MP4 video files.
- Generic: Other URLs will attempt to use a default iframe embed.

## Examples

<Embed slots="video" />

https://www.youtube.com/embed/4haZJxpf9Bo?si=9Pfm0yJD_62ZQnqg
