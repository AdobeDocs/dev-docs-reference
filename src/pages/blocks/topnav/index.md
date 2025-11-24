---
title: Top Navigation
description: Learn how to configure top navigation in config.md for your documentation site.
---

# Top Navigation

Top Navigation is configured in the `config.md` file and controls how pages appear in the main navigation bar of your site. The navigation structure is based on the directory structure under `src/pages/`.

## Configuration Example

```yaml
- pathPrefix:
    - /dev-docs-reference/

- pages:
    - [Home](index.md)
    - [Documentation](docs/index.md)
    - [API Reference](api/index.md)
```

## How It Works

The configuration consists of two main components:

### pathPrefix

The `pathPrefix` is the base URL path for your content repository. This prefix is prepended to all page routes.

```yaml
- pathPrefix:
    - /dev-docs-reference/
```

With this configuration, your pages will be accessible at:
- `/dev-docs-reference/` → Home page
- `/dev-docs-reference/docs/` → Documentation page
- `/dev-docs-reference/api/` → API Reference page

### pages

The `pages` array defines the top navigation items that appear in the main navigation bar.

```yaml
- pages:
    - [Home](index.md)
    - [Documentation](docs/index.md)
    - [API Reference](api/index.md)
```

**Format:** `[Display Text](relative/path.md)`

- `[Home]` - The text displayed in the navigation bar
- `(index.md)` - The relative path to the page under `src/pages/`

## Visual Result

The above configuration creates a navigation bar at the top of your site with the specified items displayed horizontally.

In addition to the pages defined in your config, the navigation bar includes:
- **Adobe Developer** (logo/home link) - Links to https://developer.adobe.com/
- **Products** - Links to https://developer.adobe.com/apis

These are followed by your custom pages defined in the `pages` array.

![Top Navigation Example](../../assets/topnav.png)

## Path Resolution

All paths are relative to `src/pages/`:

| Config Path | Actual File Location |
| --- | --- |
| `index.md` | `src/pages/index.md` |
| `docs/index.md` | `src/pages/docs/index.md` |
| `api/index.md` | `src/pages/api/index.md` |

## Best Practices

- Keep top navigation items to 3-5 main sections
- Use clear, concise labels for navigation items
- Ensure all paths point to existing files under `src/pages/`
- The pathPrefix should match your repository or deployment path

## Related

For configuring sidebar navigation, see the [SideNav](/blocks/sidenav/index.md) documentation.
