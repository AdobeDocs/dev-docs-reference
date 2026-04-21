---
title: Table
description: Create structured data tables using markdown syntax, including formatting tips for bullet lists in cells.
---

# Table

Display structured data in rows and columns using standard markdown table syntax.

## Syntax

```markdown
| Column 1 | Column 2 | Column 3 |
| -------- | -------- | -------- |
| Value 1  | Value 2  | Value 3  |
```

## Example

| Month    | Savings |
| -------- | ------- |
| January  | $250    |
| February | $80     |
| March    | $420    |

## Bullets in Cells

Markdown does not support bullet lists inside table cells. Use the bullet point character `•` (Unicode U+2022) with escaped `\<br/>` for line breaks.

**Syntax:**

```markdown
| Parameter | Values                    |
| --------- | ------------------------- |
| color     | • red\<br/>• green\<br/>• blue |
```

**Example:**

| Parameter | Values                       |
| --------- | ---------------------------- |
| color     | • red\<br/>• green\<br/>• blue |
| size      | • small\<br/>• medium\<br/>• large |

