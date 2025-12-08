---
title: Announcement Block
description: Display important announcements and notices to your users with the Announcement block.
---

# Announcement Block

Display notices, updates, or calls-to-action.

## Syntax

```markdown
<Announcement slots="heading, text, button" variant="secondary" backgroundColor="background-color-gray"/>
```

## Parameters

- **slots**: 
  - `"heading, text, button"` - Full announcement
  - `"button"` - Button only

- **variant**: Style
  - `"primary"` - Bold (default)
  - `"secondary"` - Subtle

- **backgroundColor**: Background
  - `"background-color-gray"` 
  - `"background-color-white"` (default)

## Examples

### Full Announcement

<Announcement slots="heading, text, button" variant="secondary" backgroundColor="background-color-gray" />

#### New Release Available

Check out the latest features and improvements in version 2.0.

- [Read more](https://example.com)

### Button Only

<Announcement slots="button"/>

- [Get Started](https://example.com)

### Primary Variant

<Announcement slots="heading, text, button" variant="primary"/>

#### Important Update

Review these changes before your next deployment.

- [View details](https://example.com)
