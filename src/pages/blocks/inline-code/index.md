---
title: Inline Code
description: Format inline code snippets, variable names, function names, and technical terms using backticks.
---

# Inline Code

Format code elements, variable names, and technical terms within your text using backticks.

## Syntax

To create inline code, wrap text with single backticks (`` ` ``):

```markdown
Use the `variableName` variable to store the value.
```

**Result:** Use the `variableName` variable to store the value.

## Common Uses

- Variable names: `count`, `userId`, `isEnabled`
- Function names: `getUserData()`, `calculateTotal()`
- Class names: `UserManager`, `Color`
- File names: `config.json`, `index.md`
- Commands: `-v`, `--help`

## Linking Inline Code

You can combine inline code with links to reference API documentation:

```markdown
Use the [`Color`](https://example.com/api/Color) class to define colors.
```

**Result:** Use the [`Color`](https://example.com/api/Color) class to define colors.

## Example

Colors in the API are created as instances of the [`Color`](https://example.com/api/Color) class: objects with `red`, `green`, `blue`, and `alpha` (optional) values in the range from 0 to 1. The `alpha` value represents the opacity of the color, with 0 being fully transparent and 1 fully opaque.

## Best Practices

- Use inline code for technical terms and code elements only
- Don't overuse it for emphasis
- For multi-line code, use code blocks instead
- Be consistent throughout your documentation