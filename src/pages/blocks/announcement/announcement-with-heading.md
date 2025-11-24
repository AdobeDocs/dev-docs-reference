---
title: Announcement Block with Heading
description: Full announcement with title, description, and action button.
---

# Announcement with Heading Examples

This example shows full-featured announcements with heading, descriptive text, and an action button. You can customize the variant and background color.

## Secondary Variant (Subtle)

<Announcement slots="heading, text, button" variant="secondary" backgroundColor = "background-color-gray" />

### Lorem Ipsum Dolor Sit

Consectetur adipiscing elit sed do eiusmod tempor incididunt ut labore.

- [Read more details](https://example.com)

## Primary Variant (Prominent)

<Announcement slots="heading, text, button" variant="primary" backgroundColor = "background-color-gray"/>

### Amet Consectetur Adipiscing

Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

- [View full content](https://example.com)

## White Background

<Announcement slots="heading, text, button" variant="secondary" backgroundColor = "background-color-white" />

### Eiusmod Tempor Incididunt

Ut labore et dolore magna aliqua enim ad minim veniam quis nostrud.

- [Learn more here](https://example.com)

## Usage

Use `slots` to identify the markdown content:

- `heading` (optional) - The title of the announcement
- `text` (optional) - The descriptive content
- `button` (optional) - Call-to-action link

Available attributes:

- `variant` - Set to `primary` or `secondary` (default: `primary`)
- `backgroundColor` - Set to `background-color-gray` or `background-color-white` (default: `background-color-gray`)

