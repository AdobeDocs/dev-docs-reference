---
title: DevDocs Migration Best Practices
description: Best practices and troubleshooting tips for migrating your documentation from Gatsby to EDS, including file naming, paths, and block replacements.
---

# Best Practices for DevDocs 

## Deployment

- **Deployment**:
  - If first time deploying, select Force deploy all files.
  - If not, optionally include base SHA to use as a baseline - this will only deploy diffs which speeds up deployment.
  - More information: [Deployment Guide](../../../deploy/index.md)

## File and Directory Naming

- **Use kebab-case names for files and directories**:
  - Replace underscore (_) and period (.) with dash (-)
  - Remove special characters
  - Use lowercase letters for file names
  - Find and replace usages of that file in links
  - Why:
    - File paths with unsupported characters will fail to deploy to EDS.
    - Filenames are stricter in that underscores, periods, and uppercase letters are not allowed. Folder names are more lenient in that it allows underscores and uppercase letters, but not periods. For consistency and ease of remembering, it's best to use kebab-case all around.
- **Place assets in `src/pages` (and not static folder)**:
  - Remove images or pdf content from static folder and put in `src/pages` folder
  - HOWEVER, leave any redocly files (yaml or json) in a static folder outside of `src/pages`
- **Assets are reading from the branch it was deployed from**
- **Directly importing content from another repo doesn't work**:
  - Because the file is unable to fetch data from the external repo.

## Paths and Links

- **Paths**:
  - Use absolute paths when linking to other repos
  - Use absolute paths when linking to DevBiz
  - Use relative paths when linking within repo
  - Relative paths should be relative to path prefix
  - Relative links should include file name and extension (ex: `index.md` or other `.md` file)
    - except for anchor links that are in the current page (e.g. `[description](#anchor)`)
  - To open link as external, use the query string `?aio_external` in your URL:
    - Example: [https://github.com/AdobeDocs/adp-devsite-github-actions-test/blob/main/src/pages/test/test-hr-0.md?plain=1#L13](https://github.com/AdobeDocs/adp-devsite-github-actions-test/blob/main/src/pages/test/test-hr-0.md?plain=1#L13)
    - This will have to open the external link manually.
- **Config paths**:
  - Use absolute prod path for home 
    - e.g. `[Home](https://developer.adobe.com/your-product/)`
  - Relative paths should be relative to path prefix and not start with "/"
    - e.g.  `[Getting Started](guides/getting-started/index.md)`
    - In HTML, paths that start with '/' are treated as relative to domain. However, DevDocs doesn't handle this yet.
  - Landing page (the page of the path-prefix) will not have side nav.
  - On any parent section page (like `/guides/`, `/community/`, etc.), the sidebar navigation automatically displays all the child pages within that section. For example, in the config.md, if there is any subpages (eg. /guides/code-contribution) which is within the same parent section, the sidenav will show up.  This contextual sidebar appears for any page that has sub-pages, helping users easily navigate through related content without having to go back to higher-level pages.
    - Example: [https://developer-stage.adobe.com/dev-docs-reference/blocks/](https://developer-stage.adobe.com/dev-docs-reference/blocks/)
- **Remove unnecessary trailing slashes from paths**:
  - In Gatsby, invalid URLs that have unnecessary trailing slashes will work. However, in EDS they won't work
  - `redirects.json` will redirect Gatsby bookmarks (from invalid form to correct form). It's best to do this for a limited period of time, around 4-6 weeks.

- **Links to other file types than .md and .json needs to use raw github links for now**:
  - example: [https://github.com/AdobeDocs/adp-devsite-github-actions-test/blob/ced7a472d45d7d911f391f79706a3e00b7bad46a/src/pages/test/mp4.md?plain=1#L1](https://github.com/AdobeDocs/adp-devsite-github-actions-test/blob/ced7a472d45d7d911f391f79706a3e00b7bad46a/src/pages/test/mp4.md?plain=1#L1)
    - mp4 file: `https://raw.githubusercontent.com/AdobeDocs/adp-devsite-github-actions-test/refs/heads/main/src/pages/assets/example-video.mp4`
  - We have a ticket open to fix this
- **Fix dead links**:
  - `$npm run link:deadlinkonly`: lists dead links. Run to prevent 404s. Check your `package.json` file for more linting scripts
  - More information: [Linting Guide](../../../deploy/lint.md)

## Markdown Syntax Rules

- **Links should use square brackets '[ ]' and not angle brackets '< >'**
- **Quotes should match**
- **Table number of columns should be the same on all rows**:
  - Table won't render otherwise
- **Use languages properly in the code block**
- **Don't nest blocks**:
  - Don't nest a block within another block. For example, a code block cannot be within a table block.
  - Direct nesting of blocks in the source document is not a supported or recommended practice in AEM Edge Delivery Services
- **HTML tags nor custom CSS are supported:**
  - **Avoid `<br />` tag - Change any html characters with an escape character before**:
    - Example: `\<br /\>` will work.  or `\{ \}` or `\<li\>`
  - **Escape any html tags within a table**:
    - Example: `\<li /\>` within a table will render
- **`---`, `* * *`, nor `<hr>` are supported as a horizontal ruler. Replace with `<HorizontalLine />`**

## Config.md

- **Config.md**:
  - In Gatsby, Home is optional and overwrites Products
  - In EDS, Products is always displayed and Home must be the first path under Pages

## Block Replacements

- **New Block Names and Replacements**:
  - Replace `Hero` default variant with [Superhero](../../../blocks/superhero/index.md) default variant
  - Replace `Hero` halfwidth variant with [Superhero](../../../blocks/superhero/halfwidth/index.md) halfWidth variant
  - Replace `Hero` fullwidth variant with [Superhero](../../../blocks/superhero/centered/index.md) centered variant
  - Replace `Teaser` with [Announcement](../../../blocks/announcement/index.md)
  - Replace `TextBlock` with [Cards](../../../blocks/cards/index.md) or [Columns](../../../blocks/columns/index.md)
  - Replace `AnnouncementBlock` with [Announcement](../../../blocks/announcement/index.md)
  - In [InlineAlert](../../../blocks/inline-alert/index.md) block replace `header` slot with `heading` slot
  - Remove extra `Accordion` tags and only use: [AccordionItem](../../../blocks/accordion/index.md) and rearrange so header is not in the tag
  - Replace `ListBlock` with [List](../../../blocks/list/index.md)
  - Replace `TabsBlock` with [Tab](../../../blocks/tab/index.md)
  - Replace `Media` with [Embed](../../../blocks/embed/index.md). `Embed` urls shouldn't be wrapped in angle brackets `< >`:
    - example: `<Embed slots="video"/>` not -> `<Media slots="video"/>`
    - Why:
      - Media and Embed were dupes. Only Embed exists now
      - Embed syntax doesn't call for angle brackets around the url
  - Replace `openAPISpec` with [RedoclyAPIBlock](../../../blocks/redoclyapiblock/redocly-api-block-default.md):
    - `<RedoclyAPIBlock src="/{pathPrefix}/{pathToFileRelativeToStaticFolder}" />`
    - notice path includes `pathPrefix` but excludes `static`
    - petstore.json is in static folder!
  - Replace `Details` HTML element with [Details](../../../blocks/details/index.md) EDS block:
    - replace:
    ```javascript
    <details>
      <summary>Text Description of Details</summary>
    - Workflow A:
      1. Step one
      2. Step two
      3. Step three
    </details>
    ```
    - with:
    ```javascript
    <Details slots="heading , list" repeat="1" summary = "Text Description of Detail Block" subText="Diagram listing common use cases:"/>

    - Developer Distribution (Start with the listing metadata):
      1. Step one
      2. Step two
      3. Step three
    ```
    - EDS does not support Details HTML element. Use the Details EDS block instead.
- **Fragments**:
  - [Use fragment](../../../blocks/fragment/index.md)
  - [Example](https://github.com/AdobeDocs/adp-devsite-github-actions-test/blob/main/src/pages/fragment.md?plain=1#L5)
  - Imports are now fragments. The connector will ensure imports are now fragments. 
- **SiteWidebanner**:
  - Example: Add a file named site-wide-banner.json in the path:
    - /src/pages/site-wide-banner.json
    - Publish the page or deploy the file in the EDS branch, and it will be reflected automatically.
    - Example: [https://github.com/AdobeDocs/adp-devsite-github-actions-test/blob/main/src/pages/sitewidebanner.json](https://github.com/AdobeDocs/adp-devsite-github-actions-test/blob/main/src/pages/sitewidebanner.json)
  - This new announcement banner component visually will be more similar to Spectrum's alert banner. The alert banner is typically used for high-signal messages – they're meant to prompt the user to take action. The announcement banner is the dev site's version of the alert banner.
