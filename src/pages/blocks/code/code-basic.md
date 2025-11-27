---
title: Basic Code Block
description: Simple examples of basic code blocks without special features.
---

# Basic Code Block

Simple code blocks for displaying code snippets without advanced features like line highlighting or offsets.

## Syntax

Use triple backticks with a language identifier:

````
```javascript
const message = "Hello World";
```
````

## Examples

### API Request Example

```bash
curl -i -X POST 'https://api.example.com/graphql' \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer [access_token]' \
    -d '{"query": "{ users { id name } }"}'
```

### Command Examples

```bash
npm install
npm start
```

### JavaScript Example

```javascript
function greet(name) {
    return `Hello, ${name}!`;
}

console.log(greet("World"));
```

## Best Practices

- Always specify a language for syntax highlighting
- Use for straightforward code examples
- Keep code blocks concise and focused
