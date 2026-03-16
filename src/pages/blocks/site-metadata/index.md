---
title: Site Metadata
description: Learn about adp-site-metadata.json, a generated file that consolidates site-wide configuration paths for contributors, credentials, banners, and more.
---

# Site Metadata

`adp-site-metadata.json` is an auto-generated file that acts as a central registry mapping configuration keys to their JSON file paths. Components use it to locate site-wide configuration files (contributors, credentials, banners, etc.) without making redundant requests or causing unnecessary 404 errors.

If the file does not exist, components fall back to looking up each configuration file at its default location — but this results in more 404 requests.

## File Structure

```json
{
  "total": 3,
  "offset": 0,
  "limit": 3,
  "data": [
    {
      "key": "contributors",
      "value": "src/pages/contributors.json"
    },
    {
      "key": "get-credentials",
      "value": "src/pages/credential/getcredential.json"
    },
    {
      "key": "site-wide-banner",
      "value": "src/pages/site-wide-banner.json"
    }
  ],
  ":type": "sheet"
}
```

## Keys

| Key | Description |
| --- | --- |
| `contributors` | Path to the contributors JSON file |
| `get-credentials` | Path to the credential configuration JSON file |
| `site-wide-banner` | Path to the site-wide banner JSON file |

## How It Is Generated

### Local development

`adp-site-metadata.json` is generated automatically when you start the local dev server:

```bash
npm run dev
```

### On pull request

The file is generated automatically by the `Build Auto-Generated Files` GitHub Actions workflow, which runs on every pull request.


### Manual generation

To generate the file on its own:

```bash
npm run buildSiteMetadata
```


## Output Location

The generated file is written to:

```
src/pages/adp-site-metadata.json
```
