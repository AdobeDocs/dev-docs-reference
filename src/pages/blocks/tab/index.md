---
title: Tab Block
description: Organize related content using tabbed layouts with the Tab block component.
---

# Tab Block

Organize related content into tabbed sections for easy switching between different views.

## Syntax

```markdown
<Tab orientation="horizontal" slots="heading, content" repeat="2" theme="light"/>
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

- **theme**: Visual theme (optional)
  - `"light"` (default): Light theme
  - `"dark"`: Dark theme

- **className**: Optional CSS class for custom styling

## Examples

### Horizontal Tabs (Request/Response)

<Tab orientation="horizontal" slots="heading, content" repeat="2" theme="light"/>

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

### Vertical Tabs with Images

Vertical tabs are useful for step-by-step guides or when you need more vertical space:

<Tab orientation="vertical" slots="heading, image, content" repeat="3"  theme="dark" className='bgBlue ' />

## Tab 1

![Code for initializing SDK](src/pages/images/adobe-express.svg)

content tab 1

## Tab 2

![Code to invoke full editor](src/pages/images/adobe-express.svg)

content tab 2

## Tab 3

![Code to invoke quick actions](src/pages/images/adobe-express.svg)

content tab 3

### Simple Tabs with Dark Theme

Basic tabs with just headings and content:

<Tab slots="heading, content" repeat="2"  theme="dark" className='bgBlue ' />

## Tab 1

content tab 1

## Tab 2

content tab 2

## Best Practices

- Use clear, concise tab labels
- Limit to 3-7 tabs for usability
- Group related content together
- Place most important content in the first tab
