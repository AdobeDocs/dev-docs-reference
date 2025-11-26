---
title: Announcement Block
description: Display important announcements and notices to your users with the Announcement block.
---

# Announcement Block

Display important notices, updates, or calls-to-action at the top of your pages.

<InlineAlert variant="info" slots="text" />

Note: The Announcement block replaces the Teaser block that was previously used in Gatsby.

## Syntax

```markdown
<Announcement slots="heading, text, button" />
```

## Parameters

- **slots**: Content structure
  - `"heading, text, button"`: Full announcement with all elements
  - `"button"`: Button-only announcement

- **variant**: Style variant
  - `"primary"`: Bold, prominent (default)
  - `"secondary"`: Subtle

- **position**: `"center"` for centered button-only announcements

## Variants

- [Announcement with Heading](announcement-with-heading.md) - Full announcement with title and description
- [Button-only Announcement](announcement-button-only.md) - Simple call-to-action button

## Best Practices

- Use for important site-wide notices
- Keep text concise and actionable
- Limit to one announcement per page
- Use primary variant for critical updates
