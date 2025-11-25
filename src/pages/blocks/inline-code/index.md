---
title: Inline Code
description: Format inline code snippets, variable names, function names, and technical terms using backticks.
---

# Inline Code

Use inline code formatting to highlight code elements, variable names, function names, class names, file names, and technical terms within your documentation text.

## Syntax

To create inline code, wrap text with single backticks (`` ` ``):

```markdown
Use the `variableName` variable to store the value.
```

**Result:** Use the `variableName` variable to store the value.

## Common Uses

Inline code is typically used for:

- **Variable names**: `count`, `userId`, `isEnabled`
- **Function/method names**: `getUserData()`, `calculateTotal()`
- **Class names**: `UserManager`, `Color`
- **Properties**: `red`, `green`, `blue`, `alpha`
- **File names**: `config.json`, `/src/pages/index.md`
- **Short commands**: `-v`, `--help`

## Linking Inline Code

You can combine inline code with links to reference API documentation:

```markdown
Use the [`Color`](https://example.com/api/Color) class to define colors.
```

**Result:** Use the [`Color`](https://example.com/api/Color) class to define colors.

## Example

Colors in Adobe Express are created as instances of the [`Color`](https://stage--adp-devsite-stage--adobedocs.aem.page/express/add-ons/docs/references/document-sandbox/document-apis/interfaces/color) class: objects with `red`, `green`, `blue`, and `alpha` (optional) values in the range from 0 to 1. The `alpha` value represents the opacity of the color, with 0 being fully transparent and 1 fully opaque.

## Best Practices

- Use inline code for technical terms and code elements only
- Don't overuse it for emphasis
- For multi-line code, use code blocks instead
- Be consistent throughout your documentation

## Related

- [Code Block](/blocks/codeblock/code-block.md) - For multi-line code snippets
- [Code Block with Picklist](/blocks/codeblock/code-block-with-picklist.md) - For code examples in multiple languages