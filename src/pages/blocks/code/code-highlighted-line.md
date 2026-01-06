---
title: Code with Highlighted Lines
description: Examples of code blocks with specific lines highlighted using data-line attribute.
---

# Code with Highlighted Lines

Highlight specific lines in code blocks to draw attention to important code sections, changes, or key concepts.

## Syntax

Use `data-line` attribute after the language identifier:

````
```console data-line="1-2, 5, 9-20"
```
````

## Parameters

- **data-line**: Comma-separated list of line numbers or ranges to highlight (e.g., `"1-2, 5, 9-20"`)

## Example

```javascript data-line="2-3, 6"
function processData(input) {
    const cleaned = input.trim();        // Highlighted
    const parsed = JSON.parse(cleaned);  // Highlighted
    
    if (parsed.valid) {
        return parsed.data;  // Highlighted
    }
    
    return null;
}
```
