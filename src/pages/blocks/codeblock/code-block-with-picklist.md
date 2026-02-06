---
title: Code Block with Picklist
description: Display code blocks with a language picker dropdown menu for switching between different code examples.
---

# Code Block with Picklist

Display multiple code blocks with a language picker dropdown that allows users to switch between different code examples or file types.

## Syntax

````
<CodeBlock slots="heading, code" repeat="3" languages="index.html, app.js, utils.js"/>
````

## Parameters

- **slots**: Define the content structure - `"heading, code"`
- **repeat**: Number of code blocks
- **languages**: Comma-separated list of language/file labels - creates a picker dropdown for users to switch between code blocks

## Example

<CodeBlock slots="heading, code" repeat="3" languages="index.html, app.js, utils.js"/>

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
