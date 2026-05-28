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

Optional playback attributes (`loop`, `autoplay`, `nocontrols`) apply to the same pattern: add them on the opening tag, then put the media URL on the following line.

```markdown
<Embed slots="video" loop />

https://your-media-link.com
```

```markdown
<Embed slots="video" nocontrols />

https://your-media-link.com
```

```markdown
<Embed slots="video" autoplay />

https://your-media-link.com
```

```markdown
<Embed slots="video" loop autoplay />

https://your-media-link.com
```

A self-closing tag with no space before `/>` (for example `loop/>`) is equivalent to `loop />`.

## Parameters

- **slots**:
  - `"video"` - A slot for the URL of the media you wish to embed.

- **short**
  - `"true"` - An attribute displays the video in a short-form (vertical) format, similar to YouTube Shorts or Instagram Reels.

- **loop** (optional, boolean)
  - When present, the video repeats when it finishes. Example: `<Embed slots="video" loop />` or `<Embed slots="video" loop/>`.

- **autoplay** (optional, boolean)
  - When present, playback starts automatically when the player loads. For YouTube (including Shorts), Vimeo, and MP4, the block mutes the player automatically when autoplay is on. For Instagram, TikTok, and X (Twitter), autoplay is passed through to third-party iframe embeds without muting—the block does not control those players. Browser autoplay restrictions may still apply on some platforms.

- **nocontrols** (optional, boolean)
  - When present, hides the default player controls. Hiding controls forces autoplay.

You can combine attributes on the same opening tag (for example `loop autoplay`).

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

#### Hidden player controls

<Embed slots="video" nocontrols />

https://www.youtube.com/embed/4haZJxpf9Bo?si=9Pfm0yJD_62ZQnqg
