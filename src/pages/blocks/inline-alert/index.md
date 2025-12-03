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
  - `"text"` - Simple text
  - `"header, text1, text2"` - With header and sections

- **variant**: Alert type (default: `info`)
  - `"info"` - Blue
  - `"help"` - Purple
  - `"warning"` - Orange
  - `"error"` - Red
  - `"success"` - Green
  - `"neutral"` - Gray

## Examples

### Info (Default)

<InlineAlert slots="text" />

This is an info alert.

### Warning

<InlineAlert slots="text" variant="warning"/>

This is a warning alert.

### Error

<InlineAlert slots="text" variant="error"/>

This is an error alert.

### Success

<InlineAlert slots="text" variant="success"/>

This is a success alert.
