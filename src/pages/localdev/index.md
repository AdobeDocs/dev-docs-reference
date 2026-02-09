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

1. In the repos `https://github.com/AdobeDocs/adp-devsite` and `https://github.com/aemsites/devsite-runtime-connector`, make sure to be on the `main` branch and pull down the latest changes. 
2. In each repo, run the command `npm install`
3. In your content repo, switch to the branch that you want to preview locally
4. In each repo, run the command `npm run dev`
5. In your browser, navigate to `http://localhost:3000/yourPathPrefix` 
6. Manually reload the page to see any subsequent changes you make to your files
    - To see `config.md` changes reflected on side nav, restart the local servers, or open a new incognito tab (which clears `sessionStorage`)

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