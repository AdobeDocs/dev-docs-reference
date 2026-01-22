---
title: Hide Edit in GitHub
description: Control the visibility of the "Edit in GitHub" link on your documentation pages using the hideEditInGitHub frontmatter option.
hideEditInGitHub: true
---

# Hide Edit in GitHub

Control the visibility of the "Edit in GitHub" link that appears on documentation pages. This feature allows you to selectively hide the GitHub edit link for specific pages where external contributions are not desired or appropriate.

## Overview

By default, all documentation pages include an "Edit in GitHub" link that enables users to quickly navigate to the source file on GitHub and propose edits. The `hideEditInGitHub` frontmatter option provides control over this functionality on a per-page basis.

## When to Use

Consider hiding the "Edit in GitHub" link in these scenarios:

- **Restricted content**: Pages that should not be edited by external contributors
- **Auto-generated pages**: Content generated from other sources where direct edits would be overwritten
- **Sensitive documentation**: Internal documentation that shouldn't expose the repository structure
- **Legal or compliance pages**: Terms of service, privacy policies, or other legal documents
- **Protected content**: Pages that require internal review processes before modifications

## Syntax

Add the `hideEditInGitHub` property to your page's frontmatter:

```yaml
---
title: Your Page Title
hideEditInGitHub: true
---
```

## Parameters

- **hideEditInGitHub**: Boolean value (`true`)
  - `true`: Hides the "Edit in GitHub" link from the page

## Example

This page demonstrates the `hideEditInGitHub` option in action. Notice that the "Edit in GitHub" link is not visible in the page.

```yaml
---
title: Hide Edit in GitHub
description: Control the visibility of the "Edit in GitHub" link on your documentation pages.
hideEditInGitHub: true
---
```
