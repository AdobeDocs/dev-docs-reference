---
title: Details Block
description: Create expandable/collapsible sections to organize content with a summary heading and nested lists or steps.
---

# Details Block

Create expandable/collapsible sections with a summary heading and detailed content. Useful for FAQs, step-by-step workflows, or organizing large amounts of content.

## Syntax

```markdown
<Details slots="heading, list" repeat="2" summary="Summary of details" subText="Description text:"/>

- First item heading:
  1. Step one
  2. Step two
  3. Step three
- Second item heading:
  1. Step one
  2. Step two
  3. Step three
```

## Parameters

- **slots**: Content structure
  - `"heading, list"` - Header with nested list content

- **repeat**: Number of list groups to display
  - Set to match the number of top-level list items provided

- **summary**: The clickable summary text displayed when collapsed
  - This is the main heading users click to expand/collapse

- **subText**: Optional descriptive text shown below the summary
  - Provides additional context about the content inside

## Example

<Details slots="heading, list" repeat="2" summary="Getting Started Workflows" subText="Choose your workflow:"/>

- Workflow A:
  1. Step one
  2. Step two
  3. Step three
- Workflow B:
  1. Step one
  2. Step two
  3. Step three