---
title: Tab Block
description: Organize related content using tabbed layouts with the Tab block component.
---

# Tab Block

Organize content in tabs.

## Syntax

```markdown
<Tab orientation="horizontal" slots="heading, content" repeat="2"/>
```

## Parameters

- **orientation**: Tab layout direction
  - `"horizontal"` (default): Tabs appear horizontally across the top
  - `"vertical"`: Tabs appear vertically on the left side

- **slots**: Content structure for each tab
  - `"heading, content"`: Tab with heading and text content
  - `"heading, image, content"`: Tab with heading, image, and content
  - `"heading, code"`: Tab with heading and code block

- **repeat**: Number of tabs to display (e.g., `2`, `3`)

## Supported Languages for Code Tabs

When using code blocks within tabs, the following language identifiers are supported:

`bash`, `c`, `cpp`, `csharp`, `css`, `git`, `go`, `graphql`, `http`, `java`, `javadoc`, `javascript`, `jsdoc`, `json`, `json5`, `jsx`, `less`, `markdown`, `markup`, `objectc`, `php`, `python`, `regex`, `rest`, `sass`, `sql`, `typescript`, `xml-doc`, `yaml`

## Examples

### Horizontal Tabs (Request/Response)

<Tab orientation="horizontal" slots="heading, content" repeat="2"/>

### Request

```graphql
mutation {
  createCustomerV2(
    input: {
      firstname: "Bob"
      lastname: "Loblaw"
      email: "bobloblaw@example.com"
      password: "b0bl0bl@w"
      is_subscribed: true
    }
  ) {
    customer {
      firstname
      lastname
      email
      is_subscribed
    }
  }
}
```

### Response

```json
{
  "data": {
    "createCustomer": {
      "customer": {
        "firstname": "Bob",
        "lastname": "Loblaw",
        "email": "bobloblaw@example.com",
        "is_subscribed": true
      }
    }
  }
}
```

### Vertical Tabs with Image

Vertical tabs are useful for step-by-step guides or when you need more vertical space:

<Tab orientation="vertical" slots="heading, image, content" repeat="3" />

## Tab 1

![icon](../../assets/test-icon.png)

content tab 1

## Tab 2

![icon](../../assets/test-icon.png)

content tab 2

## Tab 3

![icon](../../assets/test-icon.png)

content tab 3
