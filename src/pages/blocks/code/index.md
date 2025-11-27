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

`bash`, `c`, `cpp`, `csharp`, `css`, `git`, `go`, `graphql`, `http`, `java`, `javadoc`, `javascript`, `jsdoc`, `json`, `json5`, `jsx`, `less`, `markdown`, `markup`, `objectc`, `php`, `python`, `regex`, `rest`, `sass`, `sql`, `typescript`, `xml-doc`, `yaml`

## Advanced Features

### Line Highlighting

Highlight specific lines using `data-line`:

````markdown
```javascript data-line="2,4"
function example() {
  const x = 1;  // Highlighted
  const y = 2;
  return x + y; // Highlighted
}
```
````

### Line Number Offset

Start line numbers from a specific number using `data-line-offset`:

````markdown
```javascript data-line-offset="10"
// This will show as line 10
const value = "example";
```
````

### Disable Line Numbers

Remove line numbers for cleaner display using `disableLineNumbers`:

````markdown
```bash disableLineNumbers
npm install
npm start
```
````

## Examples

See detailed examples and use cases:

- [Basic Code Blocks](code-basic.md) - Simple code examples
- [Highlighted Lines](code-highlighted-line.md) - Specific line highlighting examples
- [Code in Lists](code-in-list.md) - Code blocks nested in lists
- [Code in Tables](code-in-table.md) - Inline code in table cells
- [Combined Features](code-overload.md) - Multiple features together

## Best Practices

- Always specify a language for proper syntax highlighting
- Use `data-line` to highlight important code sections
- Use `disableLineNumbers` for short, simple commands
- Set `data-line-offset` when showing code excerpts from larger files
- Keep code snippets concise and focused

