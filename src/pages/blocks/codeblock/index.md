---
title: CodeBlock Component
description: Display multiple code snippets with headings using the CodeBlock component.
---

# CodeBlock Component

Display multiple related code snippets with headings using the `<CodeBlock>` component, ideal for showing request/response examples or comparing different code files.

## Syntax

````
<CodeBlock slots="heading, code" repeat="2" languages="JSON, JSON" />
````

## Parameters

- **slots**: Define the content structure - `"heading, code"` for titled code blocks
- **repeat**: Number of code blocks to display
- **languages**: Optional comma-separated list of language labels for each code block

## Supported Languages

The following language identifiers are supported:

`bash`, `c`, `cpp`, `csharp`, `css`, `git`, `go`, `graphql`, `http`, `java`, `javadoc`, `javascript`, `jsdoc`, `json`, `json5`, `jsx`, `less`, `markdown`, `markup`, `objectc`, `php`, `python`, `regex`, `rest`, `sass`, `sql`, `typescript`, `xml-doc`, `yaml`

## Variants

- [With Language Picker](code-block-with-picklist.md) - Dropdown to switch between languages
- [Without Language Picker](code-block-without-picklist.md) - All blocks visible simultaneously

## When to Use

Use the CodeBlock component when you need to:
- Display multiple related code examples with headings
- Show request/response pairs
- Compare different file contents
- Provide code examples in multiple languages with a picker

For single code snippets, use regular [markdown code blocks](../code/index.md) instead.