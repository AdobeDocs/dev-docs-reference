---
title: Code Overload Example
description: Complex code examples demonstrating multiple features like line highlighting, offsets, and disabling line numbers.
---

# Code Overload Example

Advanced examples showcasing the combination of multiple code block features for complex documentation scenarios.

## Combined Features

You can combine multiple attributes with hyphens:

````
```javascript-disableLineNumbers-data-line="2-4"
code here
```
````

Features you can combine:
- Line highlighting (`data-line`)
- Disable line numbers (`disableLineNumbers`)

## Examples

### Example 1: Highlighting with No Line Numbers

```javascript-disableLineNumbers-data-line="2-3"
function calculateTotal(items) {
  const total = items.reduce((sum, item) => sum + item.price, 0);  // Highlighted
  const tax = total * 0.08;  // Highlighted
  return total + tax;
}
```

### Example 2: Line Offset with Highlighting

```python-data-line="2-3"
def process_data(data):
    cleaned = data.strip()      # Line 11 - Highlighted
    parsed = json.loads(cleaned)  # Line 12 - Highlighted
    return parsed
```

### Example 3: Multiple Features Combined

```bash-disableLineNumbers-data-line="3,5"
# Install dependencies
npm install

# Run tests
npm test

# Build for production
npm run build
```
