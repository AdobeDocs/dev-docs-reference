---
title: List Block
description: Create styled lists with icons and various formatting options using the List block.
---

# List Block

Styled lists with icons.

## Syntax

```markdown
<List slots="text1, text2" repeat="2" iconColor="#2ac3a2" icon="checkmark" variant="fullWidth" />

Item 1 title

Item 1 description

Item 2 title

Item 2 description

```

## Parameters

- **slots**: `"text1, text2"` - Two text elements per item

- **repeat**: Number of items

- **icon**: Icon type (optional)
  - `"checkmark"` - Checkmark
  - Other options available

- **iconColor**: Hex color (optional)
  - Example: `"#2ac3a2"`

- **variant**: Layout (optional)
  - `"fullWidth"` - Full-width
  - Default: Standard

## Example

<List slots="text1, text2" repeat="4" iconColor="#2ac3a2" icon="checkmark" variant="fullWidth" />

Free tier available for development

Volume pricing and discounts

Access to comprehensive API suite

Quick signup and credential creation

Technical support included

No credit card required

Scalable for enterprise needs

Built for high performance
