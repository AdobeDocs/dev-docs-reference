---
title: Site-Wide Banner
description: Learn how to add a site-wide banner that appears across all pages using site-wide-banner.json.
---

# Site-Wide Banner

Display an announcement banner across all pages of your site.

## Setup

Create a `site-wide-banner.json` file in your root directory under /src/pages/ with the following structure:

```json
{
  "total": 1,
  "offset": 0,
  "limit": 1,
  "data": [
    {
      "bgColor": "success",
      "icon": "info",
      "text": [
        "Your announcement message here."
      ],
      "button": "Learn More",
      "buttonLink": "https://example.com",
      "isClose": true
    }
  ],
  ":type": "sheet"
}
```

## Properties

| Property | Type | Description |
| --- | --- | --- |
| `bgColor` | string | `notice` (yellow), `info` (blue), `warning` (orange), `success` (green), `neutral` (dark gray), `light` (white) |
| `icon` | string | Icon to display: `info`, `warning`, `success` |
| `text` | array | Message text (supports multiple lines) |
| `button` | string | Button text |
| `buttonLink` | string | Button URL |
| `isClose` | boolean | Allow users to dismiss the banner |

## Example

This is what it looks like visually.

![sitewidebanner](../../ßassets/sitewidebanner.png)
