---
title: Inline Alert Block
description: Display inline alert messages for warnings, tips, and notes using the Inline Alert block.
---

# Inline Alert

Display contextual alert messages within your documentation to highlight important information, warnings, tips, or errors.

## Overview

Inline Alerts are useful for:
- Important notices and warnings
- Helpful tips and best practices
- Error messages and troubleshooting
- Success confirmations
- Additional context or information

## Syntax

```markdown
<InlineAlert slots="text" variant="info" />

Your alert message here.
```

## Parameters

- **slots**: Content structure
  - `"text"`: Simple alert with text only
  - `"header, text1, text2, ..."`: Alert with header and multiple text sections

- **variant**: Alert type (default: `info`)
  - `"info"`: Information (blue) - default
  - `"help"`: Help or tips (purple)
  - `"warning"`: Warning messages (orange)
  - `"error"`: Error messages (red)
  - `"success"`: Success messages (green)
  - `"neutral"`: Neutral messages (gray)

## Examples

### Info Alert (Default)

<InlineAlert slots="text" />

This is the text that displays within the default alert variant — info.

### Help Alert

<InlineAlert variant="help" slots="header, text1, text2, text3, text4" />

### Alternative steps:

**Step 1:** This is faux step text for the `text1` slot.
This is faux step text for the `text1` slot.
This is faux step text for the `text1` slot.
This is faux step text for the `text1` slot.
This is faux step text for the `text1` slot.

**Step 2:** This is faux step text for the `text2` slot.
This is faux step text for the `text2` slot.
This is faux step text for the `text2` slot.

**Step 3:** This is faux step text for the `text3` slot.

**Step 4:** This is faux step text for the `text4` slot.
This is faux step text for the `text3` slot.

### Warning Alert

<InlineAlert slots="text" variant="warning"/>

This is an inline alert warning.

### Error Alert

<InlineAlert slots="text" variant="error"/>

This is an inline alert error.

### Success Alert

<InlineAlert slots="text" variant="success"/>

This is an inline alert success.

### Neutral Alert

<InlineAlert slots="text" variant="neutral"/>

This is an inline alert neutral.

## Best Practices

- **Choose the right variant**: Use appropriate alert types for the context
  - `info`: General information or notes
  - `help`: Tips, suggestions, or helpful guidance
  - `warning`: Cautions or important considerations
  - `error`: Errors or problems that need attention
  - `success`: Positive confirmations or completions
  - `neutral`: Neutral information without emphasis

- **Keep messages concise**: Write clear, actionable messages
- **Use header slot**: For complex alerts with multiple sections
- **Don't overuse**: Too many alerts can overwhelm readers
- **Place strategically**: Position alerts near relevant content

## Common Use Cases

- **Prerequisites**: Alert users to requirements before starting
- **Breaking changes**: Warn about API or feature changes
- **Deprecation notices**: Inform about deprecated features
- **Tips and tricks**: Share helpful shortcuts or best practices
- **Security warnings**: Highlight security considerations
- **Success messages**: Confirm successful operations

## Related

- [Announcement](/blocks/announcement/index.md) - Page-level announcements
- [Inline Code](/blocks/inline-code/index.md) - For code references in alerts
