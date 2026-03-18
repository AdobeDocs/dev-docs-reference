---
title: Contributors
description: Learn about the Contributors block and contributors.json, an auto-generated file that powers per-page contributor avatars and last-updated dates.
---

# Contributors

The Contributors block displays contributor avatars, a last-updated date, and a "Was this helpful?" feedback prompt at the bottom of a page. Clicking Yes or No fires an analytics event (`Feedback-Yes` or `Feedback-No`). It is automatically injected into pages — authors do not need to add it to their markdown.

The block reads from `contributors.json`, an auto-generated file that maps page paths to their GitHub contributors and last-modified dates. If a page has no entry in `contributors.json`, the block does not render.

The path to `contributors.json` is registered in [`adp-site-metadata.json`](/blocks/site-metadata/index.md) under the `contributors` key. If `adp-site-metadata.json` does not define a path, the block falls back to `{pathPrefix}/contributors.json`.

## contributors.json Structure

```json
{
  "total": 148,
  "offset": 0,
  "limit": 148,
  "data": [
    {
      "page": "/",
      "avatars": [
        "https://avatars.githubusercontent.com/u/120194874?v=4",
        "https://avatars.githubusercontent.com/u/41382203?v=4"
      ],
      "lastUpdated": "3/13/2026"
    },
    {
      "page": "/api/",
      "avatars": [
        "https://avatars.githubusercontent.com/u/120194874?v=4"
      ],
      "lastUpdated": "8/22/2024"
    }
  ],
  ":type": "sheet"
}
```

### Fields

| Field | Description |
| --- | --- |
| `page` | Page path to match against the current URL (relative to `pathPrefix`) |
| `avatars` | Array of GitHub avatar URLs for contributors to that page |
| `lastUpdated` | Date of the last commit to that page, in `M/D/YYYY` format |

## Feedback Persistence

To prevent duplicate feedback submissions and reduce survey fatigue, the block persists the user's selection in `localStorage` using the current page path as the key (`feedback:/your/page/path`). On subsequent visits, the saved selection is restored and the feedback section is dimmed, with the chosen button highlighted.

## How It Is Generated

`contributors.json` is auto-generated — do not edit it manually.

### Local development

`contributors.json` is generated automatically when you start the local dev server:

```bash
npm run dev
```

### On pull request

The file is generated automatically by the `Build Auto-Generated Files` GitHub Actions workflow, which runs on every pull request.

### Manual generation

To generate the file on its own:

```bash
npm run buildContributors
```

To force a full rebuild of all pages (see [Build behavior](#build-behavior) below):

```bash
npm run buildContributors -- --all
```

## Build behavior

The build script has three modes depending on what has changed:

| Scenario | What happens |
| --- | --- |
| `--all` flag is passed | Full build — all markdown files in `src/pages/` are processed |
| No `contributors.json` exists yet | Full build — treated as a first-time setup |
| Markdown files were added, modified, or renamed | Incremental build — only the changed files are processed and merged into the existing data; deleted pages are removed |
| No markdown files changed | Skipped — the existing `contributors.json` is left unchanged |

## Output Location

The generated file is written to:

```
src/pages/contributors.json
```
