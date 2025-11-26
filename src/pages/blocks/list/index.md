---
title: List Block
description: Create styled lists with icons and various formatting options using the List block.
---

# List Block

Create styled lists with icons and custom colors to highlight features, benefits, or key points.

## Syntax

```markdown
<List slots="text1, text2" repeat="4" iconColor="#2ac3a2" icon="checkmark" variant="fullWidth" />
```

## Parameters

- **slots**: Content structure for each list item
  - `"text1, text2"`: Two text elements per item (e.g., title and description)

- **repeat**: Number of list items to display

- **icon**: Icon type to display (optional)
  - `"checkmark"`: Checkmark icon
  - Other icon options available

- **iconColor**: Hex color for the icon (default: theme color)
  - Example: `"#2ac3a2"`, `"#ff0000"`

- **variant**: Layout variant (optional)
  - `"fullWidth"`: Full-width layout
  - Default: Standard layout

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

## Best Practices

- Keep text concise and scannable
- Limit to 4-8 items for readability
- Use consistent icon colors
- Use checkmarks for positive features
