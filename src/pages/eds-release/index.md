---
title: EDS Release Notes
description: Release notes and changelog for Edge Delivery Services updates on the Adobe Developer Website, including new features, bug fixes, and improvements.
---

# EDS Release Notes

## 3/19/26 EDS Release:
- **Feat:** topnav dropdown scrollable
  - [DEVSITE-2287](https://jira.corp.adobe.com/browse/DEVSITE-2287)
- **Feat:** iframe enhancements — append parent page hash to iframe src on initial load, add `setHash` and `setQueryParams` Penpal parent methods, notify child via `onHashChange` on browser Back/Forward navigation, and enhance navigation state handling with `popstate` event
  - Updated event listener to notify child of both hash and search parameters on browser Back/Forward navigation
  - Improved `setHash` and `setQueryParams` methods to ensure URL state is accurately reflected
- **Feat:** feedback persistence
- **Fix:** contributor modal mobile overflow
- GetCredential Fixes:
  - **Fix:** get credential CSS issue
    - [DEVSITE-2261](https://jira.corp.adobe.com/browse/DEVSITE-2261)
  - **Fix:** side content design issue
- **Fix:** remove table of content text in sidenav
- **Feat:** enhance AI assistant functionality with stop response feature
  - Updated CSS for the send button to include a stop mode with new styles
  - Added logic to handle aborting ongoing requests and toggling button states
  - Introduced new SVG icons for send and stop actions
  - Improved user experience by showing/hiding the stop button during interactions

## 3/12/26 EDS Release:
- **Feat:** read resource paths from `adp-site-metadata.json` with fallback to direct fetches
  - [DEVSITE-2212](https://jira.corp.adobe.com/browse/DEVSITE-2212)
- **Feat:** dynamic contributors
  - [DEVSITE-2092](https://jira.corp.adobe.com/browse/DEVSITE-2092)
- **Feat:** AI assistant
  - [ADPGENAI-51](https://jira.corp.adobe.com/browse/ADPGENAI-51), [DEVSITE-2146](https://jira.corp.adobe.com/browse/DEVSITE-2146)
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
