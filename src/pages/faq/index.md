---
title: ADP Developer Site - FAQ
description: A guide with FAQ about the ADP Developer Site
---

# ADP Developer Site Best Practices

## Why is my link returning a 404?

A few common causes:

- **Trailing slash** — pages served from `index.md` files require a trailing slash. The no-slash version won't redirect unless a redirect is explicitly configured. See [Paths and Links](../getting-started/dev-docs/best-practices/index.md#paths-and-links).
- **Path characters** — paths use hyphens, not underscores or periods. See [File and Directory Naming](../getting-started/dev-docs/best-practices/index.md#file-and-directory-naming).
- **Expired redirects** — after migrating from Gatsby, we add temporary redirects to cover old bookmarks. Those are removed after ~6 weeks. New pages never get them, so there's no fallback. See [Why were the redirects to my old Gatsby pages removed?](#why-were-the-redirects-to-my-old-gatsby-pages-removed) and [Paths and Links](../getting-started/dev-docs/best-practices/index.md#paths-and-links).

To detect 404s in your repo, run the link checker commands in your [`package.json`](https://github.com/AdobeDocs/dev-docs-template/blob/d67b86f4dca4f30ecb9825fe7dd08b392475ad4b/package.json#L27-L28).

## Why were the redirects to my old Gatsby pages removed?

When pages migrate from Gatsby to the DevSite EDS platform, we add temporary redirects so existing bookmarks land on the new pages. These redirects are removed after ~6 weeks, because keeping redirects on all of your pages has a negative impact on Google search indexing, SEO, and LLMs.

After the redirects expire, the new pages can still be found via search and re-bookmarked. Note that the EDS platform handles the trailing slash (`/`) differently from Gatsby — see [Paths and Links](../getting-started/dev-docs/best-practices/index.md#paths-and-links).

## How do I link PDF or ZIP files for download or viewing?
To host and link PDF files (or other files like `ZIP` or `.d.ts`), use a URL and use relative path to file within `src/pages`:

`[ZIP](./assets/process.zip)` \<br/\> 
`[PDF for download](./assets/example.pdf)` \<br/\> 

## How do I link JSON files?

`JSON` files in `src/pages` must be in AEM EDS format or deployments will fail. JSON files that aren't in AEM EDS format (such as Redocly API spec files) must be placed in the `static` folder and can be linked using a relative path: \<br/\>

`[example JSON file](../../../static/petstore.json)`

**In a `RedoclyAPIBlock`**: Relative paths don't work — use `src="/{pathPrefix}/{filename}"` (include pathPrefix, exclude the `static` segment): \<br/\>

`<RedoclyAPIBlock src="/your-pathPrefix/petstore.json" />`

## Where can I upload videos?

To use videos in blocks that accept video attributes, you need to provide a URL or if uploaded under `src/pages` they can use a relative path. Here are your options for uploading and hosting videos:

**GitHub**: Commit your video to your GitHub repository and link to it using a relative path. [See Superhero with video](../blocks/superhero/halfwidth/with-background-image-and-video.md)

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

## Why did my deployment fail? The branch name has a slash.

Branch names cannot include slashes (e.g., `feature/my-branch`). EDS deployment will fail if you deploy from a branch that contains a slash. Use branch names without slashes, such as `feature-my-branch`.

## Why are the Contributors, SideNav, or Get Credentials blocks missing on my private repo?

On private repos, `contributors.json` and `adp-site-metadata.json` are not auto-generated (unlike public repos), so blocks that depend on them won't render. Before deploying, run the **Build Auto-Generated Files** workflow manually:

Actions → Build Auto-Generated Files → Run workflow

This is a known limitation tracked in [DEVSITE-2395](https://jira.corp.adobe.com/browse/DEVSITE-2395).

## I deployed from a new branch but my changes aren't showing on Stage

Deployments are incremental by default: the workflow finds the **last successful deploy on the same branch** and uploads only the files that changed since then. A brand-new branch has no previous successful deploy to compare against, so change detection falls back to diffing only the latest commit — anything committed earlier on the branch isn't detected and never gets deployed.

Re-run the workflow with **Force deploy all files** checked. This skips change detection and uploads every file in `src/pages/`, so the whole branch renders. This is the expected step when testing a new branch.

Actions → Staging → Run workflow → check **Force deploy all files** → Run workflow

See [Full Deployment (deployAll: true)](../deploy/index.md#full-deployment-deployall-true).

## Why do I see "Invalid license key: host not allowed" on a `RedoclyAPIBlock`?

The block only renders on hostnames in the Redocly license's allowed-domains list, and the page you're viewing isn't one of them (`main--...aem.page` preview URLs are a common case). View the page on an allowed host instead — for example, `https://developer-stage.adobe.com/...` — or on your local dev server (`http://localhost:3000/...`).

See [Redocly API Block](../getting-started/features/redocly/index.md#where-the-block-renders) for the full list of allowed domains.

## Why are the `Build Contributors` or `Build Site Metadata` checks failing with a push rejection?

The deploy workflow auto-generates `contributors.json` and `adp-site-metadata.json` and pushes them to main using the `adp-devsite-app` bot. If your repo has branch protection rules, the bot needs to be added as a bypass actor.

Settings → Branches → edit ruleset → Bypass list → add [`adp-devsite-app`](https://github.com/apps/adp-devsite-app).
