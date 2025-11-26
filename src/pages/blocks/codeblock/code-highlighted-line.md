---
title: Code with Highlighted Lines
description: Examples of code blocks with specific lines highlighted using data-line and data-line-offset attributes.
---

# Code with Highlighted Lines

Highlight specific lines in code blocks to draw attention to important code sections, changes, or key concepts.

## Syntax

Use `data-line` and `data-line-offset` attributes after the language identifier:

```markdown
```console data-line="1-2, 5, 9-20" data-line-offset="3"
```
```

## Parameters

- **data-line**: Comma-separated list of line numbers or ranges to highlight (e.g., `"1-2, 5, 9-20"`)
- **data-line-offset**: Starting line number for the code block (useful when showing code snippets from a larger file)

## Example

```console data-line="1-2, 5, 9-20" data-line-offset="3"
curl -i -X POST 'https://graffias.adobe.io/graffias/graphql' 
    -H 'Accept-Encoding: gzip, deflate, br' 
    -H 'Content-Type: application/json' 
    -H 'Accept: application/json' 
    -H 'Connection: keep-alive' 
    -H 'x-gw-ims-org-id: [OrgId]@AdobeOrg' 
    -H 'x-gw-ims-user-id: [UserId]@techacct.adobe.com' -H 'x-api-key: [clientId]' 
    -H 'Authorization: Bearer [access token]' 
    -d @introspection.json --compressed
```

## Best Practices

- Highlight only the most important lines to avoid overwhelming the reader
- Use line ranges (e.g., `1-5`) for consecutive lines
- Set `data-line-offset` when showing excerpts from larger files
