---
title: Links
description: Learn how to create links between documentation pages using relative and absolute paths.
---

# Links

Create links between documentation pages using standard markdown link syntax with relative or absolute paths.

## How Links Work

All links are resolved relative to the `src/pages/` directory. You can use either relative paths (from your current location) or absolute paths (from the root).

## Syntax

```markdown
[Link Text](path/to/page.md)
```

## Path Types

### Relative Paths

Relative paths are based on your current page location.

**Example:** If you're on `src/pages/blocks/links/index.md` and want to link to `src/pages/blocks/column/index.md`:

```markdown
[Column Block](../column/index.md)
```

- `..` moves up one directory level (from `links/` to `blocks/`)
- Then navigates to `column/index.md`

**Another example:** From `src/pages/blocks/index.md` to `src/pages/blocks/column/index.md`:

```markdown
[Column Block](column/index.md)
```

### Absolute Paths

Absolute paths start from the `src/pages/` directory with a leading `/`.

**Example:** From any page to `src/pages/blocks/column/index.md`:

```markdown
[Column Block](/blocks/column/index.md)
```

The leading `/` indicates the path starts from `src/pages/`.

## Examples

### Linking Within the Same Directory

If you're in `src/pages/blocks/` and want to link to another file in the same directory:

```markdown
[Accordion](accordion/index.md)
[Tab Block](tab/index.md)
```

### Linking to Parent Directory

From `src/pages/blocks/column/index.md` to `src/pages/blocks/index.md`:

```markdown
[Back to Blocks](../index.md)
```

### Linking Across Directories

From `src/pages/blocks/column/index.md` to `src/pages/blocks/superhero/index.md`:

```markdown
[Superhero Block](../superhero/index.md)
```

### Using Absolute Paths

From anywhere in the documentation:

```markdown
[Column Block](/blocks/column/index.md)
[Home Page](/index.md)
[Configuration](/config.md)
```

## Path Resolution Table

| Current Page Location | Target Page | Relative Path | Absolute Path |
| --- | --- | --- | --- |
| `blocks/links/index.md` | `blocks/column/index.md` | `../column/index.md` | `/blocks/column/index.md` |
| `blocks/index.md` | `blocks/column/index.md` | `column/index.md` | `/blocks/column/index.md` |
| `blocks/column/index.md` | `blocks/index.md` | `../index.md` | `/blocks/index.md` |
| `blocks/column/index.md` | `index.md` (root) | `../../index.md` | `/index.md` |

## Best Practices

- Use relative paths when linking between pages in the same section
- Use absolute paths when linking from deeply nested pages to other sections
- Always include the `.md` file extension
- Link to `index.md` files directly (e.g., `column/index.md` not just `column/`)
- Test your links to ensure they resolve correctly

## External Links

For external URLs, use standard markdown syntax:

```markdown
[External Site](https://example.com)
```

External links will open in the same window by default.

