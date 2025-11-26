---
title: Accordion Block
description: Learn how to use the Accordion block to create collapsible content sections for organizing information in your documentation.
---

# Accordion Block

Create collapsible content sections to organize information. Each accordion item can be expanded or collapsed individually.

## Syntax

```markdown
<AccordionItem header="Section heading">

Content goes here.

</AccordionItem>
```

## Parameters

- **header**: Title/header of the accordion item (required)
- **slots**: Content structure
  - `"heading, text"`: Basic text content
  - `"heading, text, table"`: Include tables
  - `"heading, text, code"`: Include code blocks

## Variants

- [Basic Accordion](accordion-basic.md) - Simple collapsible text sections
- [Accordion with Table and Code](accordion-with-table-and-code.md) - Complex content with tables and code

## Best Practices

- Use clear, descriptive headings
- Keep individual sections focused
- Group related information together
- Place most important content in first item

## Related

- [Tab](/blocks/tab/index.md) - Tabbed content sections
- [List](/blocks/list/index.md) - Styled lists
