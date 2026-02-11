---
title: Page Actions
description: Control the visibility of the Edit in GitHub link, Log an issue button, and Copy Markdown button using hideEditInGitHub, hideLogIssue, and hideCopyMarkDown frontmatter options.
hideEditInGitHub: true
hideLogIssue: true
hideCopyMarkDown: true
---

# Page Actions

Control the visibility of page action links and buttons: **Edit in GitHub**, **Log an issue**, and **Copy Markdown**. Use these frontmatter options on a per-page basis when you want to hide one or more of these actions.

## Overview

By default, documentation pages can show:

- **Edit in GitHub**: Link to open the source file on GitHub and propose edits
- **Log an issue**: Button to report a problem with the page (GitHub or your issue tracker)
- **Copy Markdown**: Button to copy the page content as Markdown

Use the options below to hide any of these actions for specific pages.

## When to Use

Consider hiding these actions when:

- **Edit in GitHub**: Restricted content, auto-generated pages, sensitive docs, legal/compliance pages, or content that requires internal review before edits
- **Log an issue**: Pages not open for public feedback, auto-generated content, or internal-only docs where issues are handled elsewhere
- **Copy Markdown**: Pages where copying source is restricted, sensitive content, or minimal layouts where you want less clutter

You can hide any combination of the three; each option is independent.

## Syntax

Add one or more properties to your page's frontmatter:

```yaml
---
title: Your Page Title
hideEditInGitHub: true
hideLogIssue: true
hideCopyMarkDown: true
---
```

## Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| **hideEditInGitHub** | Boolean | When `true`, hides the "Edit in GitHub" link. Omit or `false` to show it (default). |
| **hideLogIssue** | Boolean | When `true`, hides the "Log an issue" button. Omit or `false` to show it (default). |
| **hideCopyMarkDown** | Boolean | When `true`, hides the "Copy Markdown" button. Omit or `false` to show it (default). |

## Examples

### Hide only Edit in GitHub

```yaml
---
title: Internal Reference
hideEditInGitHub: true
---
```

### Hide only Log an issue

```yaml
---
title: Feedback Page
hideLogIssue: true
---
```

### Hide only Copy Markdown

```yaml
---
title: Read-Only Page
hideCopyMarkDown: true
---
```

### Hide all three actions

```yaml
---
title: Locked Down Page
hideEditInGitHub: true
hideLogIssue: true
hideCopyMarkDown: true
---
```

## Example

This page has all three options enabled. The "Edit in GitHub" link and the "Log an issue" and "Copy Markdown" buttons are not visible in the page action area.

## Best Practices

- Use these options sparingly to keep documentation open and easy to contribute to
- Document internally which pages use these options and why
- Review periodically whether hiding actions is still necessary
