---
title: ADP Developer Site - FAQ
description: A guide with FAQ about the ADP Developer Site
---

# ADP Developer Site Best Practices

## How do I host and link PDF files for download?
To host and link PDF files, upload the document directly to your project's GitHub repository and use its raw GitHub URL as the link destination. This allows the file to be served directly, ensuring that when a user clicks the link, the PDF opens in a new tab or prompts a download.

## Where can I upload videos?

To use videos in blocks that accept video attributes, you need to provide a URL. Here are your options for uploading and hosting videos:

**GitHub**: Commit your video to your GitHub repository and copy the raw GitHub URL.

**Google Drive** (with 2-minute limit): Upload your video to Google Drive, open it, use the AEM Sidekick extension to publish, then copy the URL. Videos uploaded to Google Drive have a 2-minute limit.

**YouTube**: Upload videos to YouTube. This option has no time limit restrictions.

## I'm getting a warning about "always-auth" when running npm commands

If you see this warning when running `npm install`, `npm run dev`, or other npm commands:

```
npm warn Unknown user config "always-auth". This will stop working in the next major version of npm.
```

This means your local npm configuration has the deprecated `always-auth` option set. This is not caused by the project — it comes from your `~/.npmrc` file, likely set by an older npm version or onboarding script.

To fix it, run:

```
npm config delete always-auth
```

This is safe to do. The `always-auth` option is no longer needed — modern npm handles registry authentication automatically through scoped `_authToken` entries in your `~/.npmrc`.
