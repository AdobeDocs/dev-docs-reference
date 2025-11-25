---
title: Code Block Component
description: Learn how to use the Code Block component to display multiple code snippets with headings.
---

# Code Block Component

The Code Block component allows you to display multiple related code snippets with headings, making it ideal for showing request/response examples or comparing different code files.

## Syntax

```markdown
<CodeBlock slots="heading, code" repeat="2" languages="JSON, JSON" />
```

## Parameters

- **slots**: Define the content structure - `"heading, code"` for titled code blocks
- **repeat**: Number of code blocks to display
- **languages**: Optional comma-separated list of language labels for each code block

## Example

<CodeBlock slots="heading, code" repeat="2" languages="JSON, JSON" />

#### Payload

```json
{
  "customer": {
    "email": "mshaw@example.com",
    "firstname": "Melanie",
    "lastname": "Shaw"
  }
}
```

#### Response

```json
{
  "id": 13,
  "group_id": 1,
  "created_at": "2017-05-18 16:47:44",
  "updated_at": "2017-05-18 16:47:44",
  "created_in": "Default Store View",
  "email": "mshaw@example.com",
  "firstname": "Melanie",
  "lastname": "Shaw",
  "store_id": 1,
  "website_id": 1,
  "addresses": [],
  "disable_auto_group_change": 0,
  "extension_attributes": {
    "company_attributes": {
      "customer_id": 13,
      "company_id": 0
    }
  }
}
```

## Best Practices

- Use meaningful headings that describe each code block
- Group related code snippets together (e.g., request/response pairs)
- Specify languages for syntax highlighting when possible

## Related

- [Code Block with Picklist](/blocks/codeblock/code-block-with-picklist.md) - Code blocks with language picker
- [Code Block without Picklist](/blocks/codeblock/code-block-without-picklist.md) - Multiple code blocks without language selection
