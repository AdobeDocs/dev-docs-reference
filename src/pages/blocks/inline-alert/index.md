---
title: Inline Alert Block
description: Display inline alert messages for warnings, tips, and notes using the Inline Alert block.
---

# Inline Alert

Alert messages for important information.

## Syntax

```markdown
<InlineAlert slots="text" variant="info" />

Your alert message here.
```

## Parameters

- **slots**: 
  - `heading` (optional) - Only one title per alert block.
  - `text` (required)
  - `text1, text2, text[n]` (optional) - Additional text slots to display multiple paragraphs.

- **variant**: Determines the icon and border color of the alert
  - `info` (default) — Use to add helpful information.
  - `help` - Use to add brief steps from or links to other help topics.
  - `error` - Use to highlight errors that may result from an action.
  - `success` - Use to highlight success messages that may be displayed after an action.
  - `warning` - Use to focus attention on a potential problem that could occur.
  - `neutral` - Use as an all-purpose callout that displays a black border and no icon.

## Examples

### Info (Default)

<InlineAlert slots="text" />

This is an info alert.

### Help

<InlineAlert slots="text" variant="help"/>

This is an help alert.

### Error

<InlineAlert slots="text" variant="error"/>

This is an error alert.

### Success

<InlineAlert slots="text" variant="success"/>

This is a success alert.

### Warning

<InlineAlert slots="text" variant="warning"/>

This is a warning alert.

### Neutral

<InlineAlert slots="text" variant="neutral"/>

This is a neutral alert.

### Richer Inline Alert

<InlineAlert variant="help" slots="heading, text1, text2, text3, text4" />

Alternative steps:

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




