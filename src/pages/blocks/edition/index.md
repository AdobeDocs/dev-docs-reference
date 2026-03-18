---
title: Edition Block
description: Display edition-specific content using the Edition block component.
---

# Edition Block

Display edition or platform labels.

## Syntax

```markdown
<Edition slots="text" />

Enterprise Edition
```

## Parameters

- **slots**: `"text"` - Edition text or link

- **backgroundcolor**: Background color (optional)
  - Default (red) - No attribute needed
  - `"blue"` - Blue background
  - `"green"` - Green background

## Examples

### Default (Red)

<Edition slots="text"/>

PaaS Only

### Blue Background

<Edition slots="text" backgroundColor="blue" />

Enterprise Edition

### Green Background

<Edition slots="text" backgroundColor="green" />

Premium Edition

### With Link

<Edition slots="text"/>

[Enterprise Edition](https://example.com/editions)
