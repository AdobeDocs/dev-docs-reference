---
title: Code Block without Picklist
description: Display multiple code blocks without a language picker dropdown.
---

# Code Block without Picklist

Display multiple code blocks with headings but without a language picker. All code blocks are visible simultaneously without switching between them.

## Syntax

````
<CodeBlock slots="heading, code" repeat="3"/>
````

## Parameters

- **slots**: Define the content structure - `"heading, code"`
- **repeat**: Number of code blocks to display
- **languages**: Omit this parameter to display code blocks without a picker

## Example

<CodeBlock slots="heading, code" repeat="3"/>

#### index.html

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="description" content="Sample web application" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>My Application</title>
        <link rel="stylesheet" href="styles.css" />
    </head>

    <body>
        <div class="container">
            <h1>Welcome</h1>
            <button id="submitBtn">Submit</button>
        </div>
        <script type="module" src="app.js"></script>
    </body>
</html>
```

#### app.js

```js
import { formatDate, validateInput } from "./utils.js";

// Initialize the application
function init() {
    console.log("Application initialized");
    
    const submitBtn = document.getElementById("submitBtn");
    
    submitBtn.addEventListener("click", () => {
        const isValid = validateInput("sample data");
        if (isValid) {
            console.log("Form submitted at:", formatDate(new Date()));
        }
    });
}

document.addEventListener("DOMContentLoaded", init);
```

#### utils.js

```js
// Utility functions for the application

export function formatDate(date) {
    return date.toLocaleDateString("en-US", {
        year: "numeric",
        month: "long",
        day: "numeric"
    });
}

export function validateInput(value) {
    return value && value.trim().length > 0;
}
```