---
title: ADP Developer Site - Local Development
description: A guide on how to use local development to help build your site
---

# DevDoc Local Development

## Overview

Authors can use local development in order to launch their sites locally to edit and preview their changes.

## Requirements

In order to use local development, authors must have these three repos cloned to their machines:
- [https://github.com/AdobeDocs/adp-devsite](https://github.com/AdobeDocs/adp-devsite): ADP DevSite's code repo
- [https://github.com/aemsites/devsite-runtime-connector](https://github.com/aemsites/devsite-runtime-connector): ADP DevSite Runtime connector
- Your content repo

## How to use

<InlineAlert slots="text" />

**Prerequisite**: Node.js version 24 or higher is required to run EDS in a local environment.

1. **Pull the latest changes**

    In both repositories below, make sure you are on the `main` branch and pull down the latest changes.

        - [https://github.com/AdobeDocs/adp-devsite](https://github.com/AdobeDocs/adp-devsite)
        - [https://github.com/aemsites/devsite-runtime-connector](https://github.com/aemsites/devsite-runtime-connector)

2. **Install dependencies**

    In each repository, run:

    -  `npm install`

3. **Switch to your preview branch**

    In your content repository, switch to the branch you want to preview locally.

4. **Start the dev servers — in this order**

    Run `npm run dev` in each repository, strictly in the following order:

    - Content repo
    - adp-devsite
    - devsite-runtime-connector

5. **Open your local preview**

    In your browser, navigate to: `http://localhost:3000/yourPathPrefix` -  Replace yourPathPrefix with the path you want to land on.

6. **Reload to see file changes**

    Manually reload the page in your browser to see any subsequent changes made to your files.

### Video

Intial requirements for setup:
<Embed slots="video" />
https://main--adp-devsite-stage--adobedocs.aem.page/devsite/local-dev-part-1.mp4

Using local development:
<Embed slots="video" />
https://main--adp-devsite-stage--adobedocs.aem.page/devsite/local-dev-part-2.mp4

## Best Practices

*   **Content Location:** Place content in `/src/pages/`, except for Redocly API JSON files, which must reside in `/static/` or outside the `/src/pages/`.
*   **The deployed stage environment (developer-stage.adobe.com) is the Source of Truth:** Local development provides a fast feedback loop while drafting content, but it may not perfectly replicate the final environment. Always use the stage environment for validation before publishing.
*   **Ongoing Refinements:** We are continuously improving the local development experience. If you notice any discrepancies between local and stage, please report them to the DevSite team.