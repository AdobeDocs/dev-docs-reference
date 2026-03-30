---
title: Create and Fill Rectangle Example
description: Interactive code example demonstrating how to create a rectangle with custom dimensions and color fill using the editor API.
---

# Code with try playground

Create interactive code examples with a "Try" button that allows users to execute code in a playground environment. This feature is ideal for API demonstrations, tutorials, and hands-on examples where users can experiment with code directly.

## Syntax

Use the following data attributes after the language identifier:

```
---
javascript-data-playground-session-id="sessionName"-data-playground-mode="playground"-data-playground-session="new"-data-playground-execution-mode="script"-data-playground-url="https://example.com"
// your code here
---
```

## Parameters

- **data-playground-session-id**: Unique identifier for the playground session (e.g., `"createAndFillRectangle"`)
- **data-playground-mode**: Mode of the playground (typically `"playground"`)
- **data-playground-session**: Session state, usually `"new"` to create a fresh session
- **data-playground-execution-mode**: Execution mode, typically `"script"` for script execution
- **data-playground-url**: Prod URL of the playground environment where code will be executed
- **data-playground-url-stage**: Stage URL of the playground environment where code will be executed

<InlineAlert slots="header, text1, text2, text3, text4"/>

**Note**

You can use two types of playground URLs. If you want to use a common playground for all code playground blocks, you can configure it globally by defining it in the `adp-sitemetadata.json`.

First, create a `code-playground.json` file as shown below:

```json
{
  "total": 2,
  "offset": 0,
  "limit": 2,
  "data": [
    {
      "key": "code-playground-staging-url",
      "value": "https://stage.projectx.corp.adobe.com/"
    },
    {
      "key": "code-playground-production-url",
      "value": "https://projectx.corp.adobe.com/"
    }
  ],
  ":type": "sheet"
}
```

If you need different playground URLs, you can use the attributes **data-playground-url and data-playground-url-stage**.

## Example for attribute

```js-data-playground-session-id="createAndFillRectangle"-data-playground-mode="playground"-data-playground-session="new"-data-playground-execution-mode="script"-data-playground-url="https://example.com/new"
const insertionParent = editor.context.insertionParent; // get node to insert content into

const rectangle = editor.createRectangle();
rectangle.width = 100;
rectangle.height = 100;
rectangle.translation = { x: 100, y: 200 };
console.log(rectangle); // for debugging purpose

const [red, green, blue, alpha] = [0.4, 0.6, 0.2, 0.4];
// Note: alpha param is optional
const aColor = colorUtils.fromRGB(red, green, blue, alpha);
const rectangleFill = editor.makeColorFill(aColor);
rectangle.fill = rectangleFill;

insertionParent.children.append(rectangle);
```
