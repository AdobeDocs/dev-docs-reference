---
title: ADP Developer Site - FAQ
description: A guide with FAQ about the ADP Developer Site
---

# ADP Developer Site Best Practices

## How do I link PDF or ZIP files for download or viewing?
To host and link PDF files (or other files like `ZIP` or `.d.ts`), use a URL and use relative path to file within `src/pages`:

`[ZIP](./assets/process.zip)` \<br/\> 
`[PDF for download](./assets/example.pdf)` \<br/\> 

`JSON` files in `src/pages` must be in AEM EDS format or deployments will fail. JSON files that aren't in AEM EDS format (such as Redocly API spec files) must be placed in the `static` folder and can be linked using a relative path: \<br/\> 

`[example JSON file](../../static/petstore.json)
`
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

## Why are the `Build Contributors` or `Build Site Metadata` checks failing on a PR from a fork?

PRs opened from forks may fail the `Build Contributors / build-contributors` or `Build Site Metadata / build-site-metadata` checks. This was fixed in v2 workflows, but existing repos are still on v1 and will be updated via the retro repo update process ([DEVSITE-2249](https://jira.corp.adobe.com/browse/DEVSITE-2249)).

Until your repo is updated to v2 workflows:
1. Go to Actions → Build Auto-Generated Files → Run workflow and wait for it to complete
2. Merge the PR and ignore the failed check

## Why are the `Build Contributors` or `Build Site Metadata` checks failing with a push rejection?

This applies to repos on v2 workflows. When a PR is merged, the deploy workflow auto-generates `contributors.json` and `adp-site-metadata.json` and pushes them to main using the `adp-devsite-app` bot. If your repo has branch protection rules, the bot needs to be added as a bypass actor.

Settings → Branches → edit ruleset → Bypass list → add [`adp-devsite-app`](https://github.com/apps/adp-devsite-app).
