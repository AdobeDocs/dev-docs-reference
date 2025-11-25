---
title: List Block
description: Create styled lists with icons and various formatting options using the List block.
---

# List Block

The List block creates visually styled lists with icons, custom colors, and layout options to highlight features, benefits, or key points.

## Overview

The List block is useful for:
- Feature lists with checkmarks or icons
- Pricing tiers and included benefits
- Step-by-step instructions
- Product highlights
- Requirements or prerequisites

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

500 free Document Transactions per month

Volume and multi-product discounts

Access to all 15+ PDF Services including PDF Extract, PDF Accessibility Auto-Tag API, and Document Generation

Access to all 15+ PDF Services including PDF Extract, PDF Accessibility Auto-Tag API, and Document Generation

Easy to sign up and create credentials in minutes

Technical Support included (different tiers available)

No credit card or commitment required

Scalable for high volume needs.

## Best Practices

- Use icons to reinforce positive features (checkmarks for included features)
- Keep text concise and scannable
- Limit to 4-8 items for optimal readability
- Use consistent icon colors that match your brand
- Pair with clear headings to provide context

## Common Use Cases

- **Feature Lists**: Highlight product capabilities
- **Pricing Plans**: Show what's included in each tier
- **Benefits**: Showcase advantages and value propositions
- **Requirements**: List prerequisites or specifications
- **Checklists**: Display steps or items to complete

## Related

- [Inline Code](/blocks/inline-code/index.md) - For technical terms in lists
- [Accordion](/blocks/accordion/index.md) - Collapsible list sections
