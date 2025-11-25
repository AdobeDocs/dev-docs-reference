---
title: Code in Lists
description: Examples of code blocks embedded within list items and ordered/unordered lists.
---

# Code in Lists

Embed code blocks within ordered or unordered lists to create step-by-step tutorials, guides, or instructions with code examples.

## Syntax

Indent code blocks with 4 spaces (or 1 tab) to nest them within list items:

```markdown
1. First step description

    ```bash
    command here
    ```

2. Second step description
```

## Example

## 3. Sign in from CLI

Once your project is set up in [Adobe Developer Console](/console), let's move onto your local environment. You can always go back to [Adobe Developer Console](/console) to modify your project later.

1. On your machine, navigate to the Terminal and enter

    ```bash
    aio login
    ```

1. A browser window should open, asking you to sign in with your Adobe ID. If the window did not automatically open, you can also copy paste the URL printed in your browser to log in.

    ```bash
    $ aio login
    Visit this url to log in:
    https://aio-login.adobeioruntime.net/api/v1/web/default/applogin?xxxxxxxx
    ```

1. Once you've logged in, you can close the browser window and go back to Terminal. You will see a string printed in the terminal. This is your user token. It is automatically stored in [CLI](https://github.com/adobe/aio-cli) config, allowing the [CLI](https://github.com/adobe/aio-cli) to use the token to talk to [Adobe Developer Console](/console).

    ```bash
    eyJ4NXUiOixxxxxxxxxxxxxxxxxxx
    ```

1. Now you can start building App Builder Applications with the [CLI](https://github.com/adobe/aio-cli)!

## Best Practices

- Indent code blocks with 4 spaces or 1 tab to nest within list items
- Use for step-by-step tutorials and installation guides
- Add explanatory text before and after code blocks for context

## Related

- [Code Block](/blocks/codeblock/code-block.md) - Basic code block component
- [Inline Code](/blocks/inline-code/index.md) - For inline code within text
