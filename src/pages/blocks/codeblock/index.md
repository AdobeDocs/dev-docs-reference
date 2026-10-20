---
title: CodeBlock Component
description: Display multiple code snippets with headings using the CodeBlock component.
---

# CodeBlock Component

Use `<CodeBlock>` to organize related code examples in one place while showing one panel at a time, like requests and responses, or implementations in different languages.

## Syntax

````markdown
<CodeBlock slots="heading, code" repeat="4" languages="cURL, JavaScript, JSON, XML" />

#### Request

```bash
# cURL request
```

#### Request

```javascript
// JavaScript request
```

#### Response

```json
{}
```

#### Response

```markup
<response />
```
````

## Example

<CodeBlock slots="heading, code" repeat="4" languages="cURL, JavaScript, JSON, XML" />

#### Request

```bash
curl -X POST 'https://api.example.com/items' \
  -H 'Content-Type: application/json' \
  -d '{"name":"example"}'
```

#### Request

```javascript
const response = await fetch('https://api.example.com/items', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ name: 'example' }),
});
const result = await response.json();
```

#### Response

```json
{
  "id": 42,
  "name": "example",
  "status": "created"
}
```

#### Response

```markup
<item>
  <id>42</id>
  <name>example</name>
  <status>created</status>
</item>
```

The **Request** tab groups the cURL and JavaScript panels; the **Response** tab groups the JSON and XML panels. Choose a tab first, then use the picker to switch between that tab's code choices.

## Parameters

- **slots**: Defines each panel's content structure - `"heading, code"`
- **repeat**: Number of authored code panels. Should equal the number of heading/code pairs; when `languages` is supplied, provide one label per panel.
- **languages**: Optional comma-separated display-label list, with one entry for each authored code panel in authored order. Supplying it enables the picker, and each entry labels the corresponding code panel. Repeated heading values group their panels under one tab

Without `languages`, the component still presents heading tabs, but hides the picker. Selecting a tab displays its panel; it does not show all panels simultaneously.

## Supported Languages

The following language identifiers are supported:

`bash`, `c`, `cpp`, `csharp`, `css`, `git`, `go`, `graphql`, `http`, `java`, `javadoc`, `javascript`, `jsdoc`, `json`, `json5`, `jsx`, `kotlin`, `less`, `markdown`, `markup`, `objectivec`, `php`, `python`, `regex`, `rest`, `sass`, `sql`, `swift`, `typescript`, `xml-doc`, `yaml`

Common aliases are also accepted (for example, `html` for `markup`, `js` for `javascript`). See the [Prism supported languages](https://prismjs.com/#supported-languages) list for each language's aliases.

Use these with the code block syntax, not the `languages` param.

## Variants

- [With Language Picker](code-block-with-picklist.md) - Switch by tab and picker
- [Without Language Picker](code-block-without-picklist.md) - Switch by tab

## When to Use

Use the CodeBlock component when you need to:
- Display multiple related code examples with headings
- Show request/response pairs
- Compare different code files
- Offer alternate representations within a heading tab

For single code snippets, use regular [markdown code blocks](../code/index.md) instead.
