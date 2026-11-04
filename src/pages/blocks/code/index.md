---
title: Code
description: Display code snippets using standard markdown code blocks with syntax highlighting and advanced features.
---

# Code

Display code snippets in your documentation using standard markdown code blocks (triple backticks) with syntax highlighting and advanced features.

## Syntax

Use triple backticks with a language identifier:

````markdown
```javascript
const greeting = "Hello World";
console.log(greeting);
```
````

## Supported Languages

The following language identifiers are supported for syntax highlighting:

`bash`, `c`, `cpp`, `csharp`, `css`, `git`, `go`, `graphql`, `http`, `java`, `javadoc`, `javascript`, `jsdoc`, `json`, `json5`, `jsx`, `kotlin`, `less`, `markdown`, `markup`, `objectivec`, `php`, `python`, `regex`, `rest`, `sass`, `sql`, `swift`, `typescript`, `yaml`

## Advanced Features

### Line Highlighting

Highlight specific lines using `data-line`:

````markdown
```javascript-data-line="2,4"
function example() {
  const x = 1;  // Highlighted
  const y = 2;
  return x + y; // Highlighted
}
```
````

```javascript-data-line="2,4"
function example() {
  const x = 1;  // Highlighted
  const y = 2;
  return x + y; // Highlighted
}
```

### Disable Line Numbers

Remove line numbers for cleaner display using `disableLineNumbers`:

````markdown
```bash-disableLineNumbers
npm install
npm start
```
````

```bash-disableLineNumbers
npm install
npm start
```

### Option rules

- Combine options after the language with dashes, in any order, for example `javascript-disableLineNumbers-data-line="2,4"`.
- Put attribute values in quotes, for example `data-line="2,4"`. Values can't contain spaces.
- Misspelled or unsupported options that start with `disable` or `data-`, and unquoted values, are ignored with a warning in the browser console. The code is still highlighted.
- Anything else right after the language, like `javascript-foo`, is read as part of the language name, so the code isn't highlighted.

## Examples

See detailed examples and use cases:

- [Basic Code Blocks](code-basic.md) - Simple code examples
- [Highlighted Lines](code-highlighted-line.md) - Specific line highlighting examples
- [Code in Lists](code-in-list.md) - Code blocks nested in lists
- [Code in Tables](code-in-table.md) - Inline code in table cells
- [Combined Features](code-overload.md) - Multiple features together
