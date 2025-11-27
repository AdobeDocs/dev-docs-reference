---
title: Code in Tables
description: Examples of inline code and code formatting within table cells.
---

# Code in Tables

Use inline code formatting within tables to document API parameters, properties, methods, and types in a structured format.

## Syntax

Use backticks for inline code in table cells:

````
| Name | Type | Description |
| --- | --- | --- |
| `propertyName` | `string` | Description text |
````

## Example

#### UserOptions : `object`

**Properties**

| Name | Type | Description |
| --- | --- | --- |
| `id` | `string` | Unique identifier for the user |
| `username` | `string` | User's display name |
| `email` | `string` | User's email address |
| `createdAt` | `Date` | Timestamp when the user was created |
| `isActive` | `boolean` | Whether the user account is active |

## Best Practices

- Use inline code for property names, types, and values
- Keep table formatting clean and aligned
- Ideal for API reference documentation
