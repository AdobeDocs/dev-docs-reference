---
title: Code in Tables
description: Examples of inline code and code formatting within table cells.
---

# Code in Tables

Use inline code formatting within tables to document API parameters, properties, methods, and types in a structured format.

## Syntax

Use backticks for inline code in table cells:

```markdown
| Name | Type | Description |
| --- | --- | --- |
| `propertyName` | `string` | Description text |
```

## Example

#### SignatureOptions : `object`

**Properties**

| Name | Type | Description |
| --- | --- | --- |
| [digiSignature1] | `string` | Value of digital signature retrieved from the x-adobe-digital-signature1 header |
| [digiSignature2] | `string` | Value of digital signature retrieved from the x-adobe-digital-signature2 header |
| [publicKeyPath1] | `string` | Relative path of ioevents public key retrieved from the x-adobe-public-key1-path header |
| [publicKeyPath2] | `string` | Relative path of ioevents public key retrieved from the x-adobe-public-key2-path header |

## Best Practices

- Use inline code for property names, types, and values
- Keep table formatting clean and aligned
- Ideal for API reference documentation
