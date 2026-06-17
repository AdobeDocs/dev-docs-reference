---
title: EDS Release Notes
description: Release notes and changelog for Edge Delivery Services updates on the Adobe Developer Website, including new features, bug fixes, and improvements.
---

# EDS Release Notes

## June 17, 2026

- [Devsite 1269 text](https://github.com/AdobeDocs/adp-devsite/pull/653) — Adds a collapsible toggle to the CodeBlock block, allowing users to show or hide code with either an icon or text label.
- [fix(discoverblock): exclude AI assistant headings from default styles](https://github.com/AdobeDocs/adp-devsite/pull/647) — Scopes discoverblock heading selectors to prevent style conflicts with headings rendered inside the AI assistant.
- [feat: enable ai assistant by default on stage](https://github.com/AdobeDocs/adp-devsite/pull/655) — Enables the AI assistant to appear by default on the developer site, scoped to the stage environment only.
- [feat(ai-assistant): add BETA badge with animated hide/show logic](https://github.com/AdobeDocs/adp-devsite/pull/656) — Adds a "BETA" badge to the AI assistant chat button that hides when the chat window opens and reappears after it closes.
- [Devsite 1996 - fixed inconsistency of external-icon](https://github.com/AdobeDocs/adp-devsite/pull/657) — Fixes external link icon rendering by correcting the HTML attribute and adding styles for icons inside list elements.
- [discoverblock update](https://github.com/AdobeDocs/adp-devsite/pull/658) — Fixes two discoverblock layout issues: a double horizontal line under h2 headings and an overlapping element problem when resizing.
- [feat(ai-assistant): add support for codeblocks](https://github.com/AdobeDocs/adp-devsite/pull/650) — Adds syntax-highlighted code block rendering inside AI assistant chat bubbles.
- [feat(ai-assistant): initial prompts and persistance for suggested questions](https://github.com/AdobeDocs/adp-devsite/pull/660) — Changes the AI assistant's initial suggested questions to a static list and persists them across page navigations using sessionStorage.
- [fix: explicitly set charset to utf-8](https://github.com/AdobeDocs/adp-devsite/pull/661) — Explicitly sets charset=utf-8 in the page head to prevent legacy charset fallback issues.

## 4/30/26 EDS Release:

- **Fix:** Discovery Interface [devsite-2327](https://jira.corp.adobe.com/browse/DEVSITE-2327)
- **Fix:** Removed `fetchMetadata` from the discovery interface
- **Fix:** Added ability to dismiss the contributor block
- **Fix:** Info Card Block [devsite-2338](https://jira.corp.adobe.com/browse/DEVSITE-2338)
- **Fix:** Added new info card variant with articles
- **Fix:** Introduced `wide` variant (replaces previous `ratio` naming)
- **Fix:** Addressed PR review feedback

## 4/9/26 EDS Release:

- **Fix:** updates to discovery interface
- **Fix:** No new tab for local dev. When the repo is running on local dev, every click on tab nav will open a new tab. Added local host and local IP to the no tab list
  - [DEVSITE-2220](https://jira.corp.adobe.com/browse/DEVSITE-2220)
- **Fix:** top offsite - two scroll-offset mechanisms were double-counting
  - [DEVSITE-2221](https://jira.corp.adobe.com/browse/DEVSITE-2221)
- **Fix:** Add support for private organization paths in getResourceUrl function to allow RedoclyBlock to fetch protected API files
  - [DEVSITE-2329](https://jira.corp.adobe.com/browse/DEVSITE-2329)

## 4/2/26 EDS Release:

- **Fix:** inline alert code slot support

  - [DEVSITE-2323](https://jira.corp.adobe.com/browse/DEVSITE-2323)

## 3/30/26 EDS Release:

- GetCredential Fixes:

  - **Fix:** credential design issue

  - **Fix:** sign-in component problem

  - **Fix:** component loading issue

  - **Fix:** populate `templateData.apis` from the template response before credential creation (template install / license configuration)

    - `fetchTemplateEntitlement()` loads the full template, including APIs with `licenseConfigs`, but that data was not always stored on `templateData`, leaving `templateData.apis` undefined.
    - The `/install` endpoint could receive an empty `apis` array and fail with errors such as “Service CJA SDK requires selection of a product”.
    - Ensures `fetchTemplateEntitlement()` runs in the relevant auth flows so API data is available, and maps only the required `licenseConfig` fields (`id`, `productId`, `op`) in the install request payload.

- **Fix:** “On this page” styles

- Data Playground Fixes:

  - **Fix:** code playground metadata and script updates

    - [DEVSITE-2304](https://jira.corp.adobe.com/browse/DEVSITE-2304)

- **Fix:** dropdown width, selector, and description max width

  - [DEVSITE-2295](https://jira.corp.adobe.com/browse/DEVSITE-2295), [DEVSITE-2305](https://jira.corp.adobe.com/browse/DEVSITE-2305)

- **Feat:** enforce Node 24+ via `.npmrc` and the `engines` field

  - [DEVSITE-2296](https://jira.corp.adobe.com/browse/DEVSITE-2296)

- **Fix:** reverse image and text order in columns

  - [DEVSITE-2301](https://jira.corp.adobe.com/browse/DEVSITE-2301), [DEVSITE-2303](https://jira.corp.adobe.com/browse/DEVSITE-2303)

- **Fix:** rename `B_app_PremierePro.svg` to `premierepro.svg`

- Embed and media fixes:

  - **Fix:** embed layout and related design issues

    - [DEVSITE-2276](https://jira.corp.adobe.com/browse/DEVSITE-2276), [DEVSITE-2303](https://jira.corp.adobe.com/browse/DEVSITE-2303)

  - **Fix:** video layout (including extra letterboxing) and shorts vs video behavior

    - [DEVSITE-2276](https://jira.corp.adobe.com/browse/DEVSITE-2276), [DEVSITE-2303](https://jira.corp.adobe.com/browse/DEVSITE-2303)

  - **Fix:** remove stray console logging in embed/video paths

## 3/19/26 EDS Release:
- **Feat:** topnav dropdown scrollable
  - [DEVSITE-2287](https://jira.corp.adobe.com/browse/DEVSITE-2287)
- **Feat:** iframe enhancements — append parent page hash to iframe src on initial load, add `setHash` and `setQueryParams` Penpal parent methods, notify child via `onHashChange` on browser Back/Forward navigation, and enhance navigation state handling with `popstate` event
  - Updated event listener to notify child of both hash and search parameters on browser Back/Forward navigation
  - Improved `setHash` and `setQueryParams` methods to ensure URL state is accurately reflected
- **Feat:** feedback persistence
- **Fix:** contributor modal mobile overflow
- GetCredential Fixes:
  - **Fix:** sign-in component problem
    - [DEVSITE-2261](https://jira.corp.adobe.com/browse/DEVSITE-2261)
  - **Fix:** side content design issue
- **Fix:** remove table of content text in sidenav
- **Feat:** enhance AI assistant functionality with stop response feature
  - Updated CSS for the send button to include a stop mode with new styles
  - Added logic to handle aborting ongoing requests and toggling button states
  - Introduced new SVGs icons for send and stop actions
  - Improved user experience by showing/hiding the stop button during interactions

## 3/12/26 EDS Release:
- **Feat:** read resource paths from `adp-site-metadata.json` with fallback to direct fetches
  - [DEVSITE-2212](https://jira.corp.adobe.com/browse/DEVSITE-2212)
- **Feat:** dynamic contributors
  - [DEVSITE-2092](https://jira.corp.adobe.com/browse/DEVSITE-2092)
- **Feat:** AI assistant
  - [ADPFGENAI-51](https://jira.corp.adobe.com/browse/ADPGENAI-51), [DEVSITE-2146](https://jira.corp.adobe.com/browse/DEVSITE-2146)
- GetCredential Fixes:
  - **Fix:** org dropdown issue
  - **Fix:** fetch entitlement
  - **Fix:** disabled button state and styling
- **Fix:** IS_DEV_DOCS rendering of Embed blocks 
  - [DEVSITE-2122](https://jira.corp.adobe.com/browse/DEVSITE-2122)
- Data Playground Fixes:
  - **Fix:** playground URL for stage environment
    - [DEVSITE-2244](https://jira.corp.adobe.com/browse/DEVSITE-2244)
  - **Fix:** codeblock "Try in Playground" issue
    - [DEVSITE-2244](https://jira.corp.adobe.com/browse/DEVSITE-2244)
- Analytics:
  - **Fix:** add analytics `daa-lh` attribute to side nav
  - **Feat:** custom analytics for Try It Playground
    - [EXTDEVEX-302](https://jira.corp.adobe.com/browse/EXTDEVEX-302)

## 2/19/26 EDS Release:
- **Fix:** update how to load the title
  - [DEVSITE-2101](https://jira.corp.adobe.com/browse/DEVSITE-2101)
- **Fix:** header clicking issue
  - [DEVSITE 2198](https://jira.corp.adobe.com/browse/DEVSITE-2198)
- **Feat:** grey fill on feedback button hover
  - [DEVSITE-2090](https://jira.corp.adobe.com/browse/DEVSITE-2090)
- **Fix:** remove extra loading functions with privacy


## 2/12/26 EDS Release:
- **Fix:** change header description look
  - [DEVSITE-2109](https://jira.corp.adobe.com/browse/DEVSITE-2109)
- **Fix:** loading order, loading multiple analytics and ims wasn't loading correctly
- **Fix:** add prism grammars for kotlin and swift
  - [DEVSITE-2172](https://jira.corp.adobe.com/browse/DEVSITE-2172)

- GetCredential Fixes:
  - **Fix:** getCredential Initial Org Id Error
    - [DEVSITE-2163](https://jira.corp.adobe.com/browse/DEVSITE-2163)
  - **Fix:** hide log issue & copy markdown
    - [DEVSITE-2164](https://jira.corp.adobe.com/browse/DEVSITE-2164)
  - **Fix:** stageTemplateDid key is added for testing.
    - [DEVSITE -2165](https://jira.corp.adobe.com/browse/DEVSITE-2165)

## 2/5/26 EDS Release:

- **feature:** show contributors when available and **fix:** place contributors in front of other blocks and **fix:** contributor styles
  - [DEVSITE-1663](https://jira.corp.adobe.com/browse/DEVSITE-1663), [DEVSITE-2087](https://jira.corp.adobe.com/browse/DEVSITE-2087)
- **feature:** constrain image dimensions within table cells
  - [DEVSITE-2140](https://jira.corp.adobe.com/browse/DEVSITE-2140)
- **feature:** add in get credentials component
- **fix:** replace getMetadata with IS_DEV_DOCS for documentation checks
  - [DEVSITE-2122](https://jira.corp.adobe.com/browse/DEVSITE-2122)
- **fix:** Fix the problem with jumpy scrolling and opening all the paths correctly
  - [DEVSITE-2110](https://jira.corp.adobe.com/browse/DEVSITE-2110)
- **fix:** added adobeio_api to ims scope
- **fix:** for privacy cookie and clicking on privacy cookie settings
  - [DEVSITE-2144](https://jira.corp.adobe.com/browse/DEVSITE-2144)

## 1/29/26 EDS Release:

- **fix:** columns images in dev docs get resized properly and dont overlap, support mp4 in columns
  - [DEVSITE-2125](https://jira.corp.adobe.com/browse/DEVSITE-2125), [DEVSITE-2116](https://jira.corp.adobe.com/browse/DEVSITE-2116), [DEVSITE-2126](https://jira.corp.adobe.com/browse/DEVSITE-2126)
- **fix:** no last breadcrumb in dev docs
  - [DEVSITE-2112](https://jira.corp.adobe.com/browse/DEVSITE-2112)
- **fix:** fixed alignment in Sort By API Browser
  - [DEVSITE-2070](https://jira.corp.adobe.com/browse/DEVSITE-2070)
