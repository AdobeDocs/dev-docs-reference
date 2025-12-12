---
title: ADP Developer Site - Deploy
description: A guide on how to deploy your site 
---

# DevDoc Deployment Guide

This guide explains how to set up and use the Adobe Developer Platform (ADP) deployment workflow for your developer site.

## Overview

The ADP developer site uses a reusable GitHub Actions workflow that handles deployments with:
- **Automatic deployments** - Push to main branch deploys to production
- **Manual deployments** - Trigger deployments via GitHub UI with custom options
- **Incremental updates** - Deploy only changed files for faster builds
- **Full site deployments** - Force deploy all files when needed
- **Multi-environment support** - Deploy to stage, production, or both

## Quick Start

To enable deployments for your repository, ensure your repo has the workflow file at `.github/workflows/deploy.yml` and `.github/workflows/stage.yml`. Both shuld point to the re-useable workflow file `AdobeDocs/adp-devsite-workflow/.github/workflows/deploy.yml@main`:

This configuration enables both automatic and manual deployments for your site.

## Deployment Methods

### Automatic Production Deployment

**Trigger:** Push commits to the `main` branch

When you merge a pull request or push directly to `main`, the workflow automatically:
1. Detects all changed files in `src/pages/`
2. Deploys only those changes to production
3. Clears cache to ensure visitors see the latest content

This is the recommended approach for regular content updates and ensures your site stays in sync with your repository.

### Manual Production Deployment

**Trigger:** GitHub Actions UI > Run workflow

Navigate to **Actions** > **Deployment** > **Run workflow** to access manual deployment options:

#### Deployment Options

**Environment Selection**
- `prod` - Deploy to production only
- `stage & prod` - Deploy to both staging and production environments (can only stage content from the `main` branch when used)

**Base SHA** (optional)
- Leave empty to compare against the last successful commit
- Provide a specific commit SHA to compare against a different point in history
- Useful for deploying a range of changes or recovering from issues

**Deploy All Files**
- Unchecked (default) - Deploy only changed files
- Checked - Deploy all files in `src/pages/` regardless of changes
- Use when you need to ensure complete environment consistency

### Manual Staging Deployment From a Branch

**Trigger:** GitHub Actions UI > Run workflow

Navigate to **Actions** > **Staging** > **Run workflow** to access manual staging deployment options:

#### Deployment Options

**Branch Selection**
- use the branch selector dropdown to pick which branch you want to use

**Base SHA** (optional)
- Leave empty to compare against the successful commit
- Provide a specific commit SHA to compare against a different point in history
- Useful for deploying a range of changes or recovering from issues

**Deploy All Files**
- Unchecked (default) - Deploy only changed files
- Checked - Deploy all files in `src/pages/` regardless of changes
- Use when you need to ensure complete environment consistency


## Deployment Workflows

### Production Deployment

Production deployments follow this process:

1. **Change Detection**
   - Compares current commit with the last successful deploy on `main`
   - Identifies modified files in `src/pages/**`
   - Tracks deleted files for cleanup
   - If unable to find the last successful deploy, it will attempt to compare the changes between the last commit and the current commit on `main`

2. **Preview Stage** (Step 1 of 2)
   - Uploads content to production environment in preview mode
   - Content is staged but on the `https://stage--adp-devsite-stage--adobedocs.aem.page/pathPrefix/` and `developer-stage.adobe.com/pathPrefix/` url
   - Allows for validation before going live
   - content for production always must be `Preview` before it appears on `Live'

3. **Live Stage** (Step 2 of 2)
   - Activates the previewed content after a 60-second delay
   - Content becomes publicly accessible on the `https://main--adp-devsite--adobedocs.aem.page/pathPrefix/` and the `developer.adobe.com/pathPreix/`
   - Cache is cleared to ensure fresh content delivery

**Important note**:
 - If the repo has never had a production commit on the EDS system, one should select the `deployAll` function to initally deploy

### Stage Deployment ###

When deploying to the stage environment:

1. **Stage Deployment**
   - Deploys changes to staging environment based on the last successful commit to the staging environment
   - Clears stage cache
   - Allows for testing in a production-like environment

2. **Preview Stage** (Step 1 of 2)
   - Uploads content to production environment in preview mode
   - Content is staged but on the `https://stage--adp-devsite-stage--adobedocs.aem.page/pathPrefix/` and `developer-stage.adobe.com/pathPrefix/` url
   - Allows for validation before going live

### Incremental Deployment (Default)

**When to use:**
- Regular content updates
- Documentation additions or edits
- Bug fixes
- Daily/frequent deployments

**How it works:**
- Compares current commit against the last successful commit
- Deploys only files that have changed
- Removes deleted files from the site

**Benefits:**
- Faster deployment times (seconds vs. minutes)
- Lower resource usage
- Reduced risk of unintended side effects
- Clear audit trail of what changed

#### Full Deployment (`deployAll: true`)

**When to use:**
- Initial site setup or migration
- Testing a new branch
- Major restructuring or reorganization
- Template or component updates affecting multiple pages
- Recovery from deployment issues
- Ensuring complete synchronization after workflow changes

**How it works:**
- Selects all files in `src/pages/**`
- Deploys entire site content
- Ignores change detection

**Caution:** Full deployments take significantly longer and consume more resources. Use sparingly for the scenarios listed above.

## Best Practices

### Recommended Workflow

1. **Develop in a feature branch**
   - Create branches for new features or content updates
   - Test locally using the development server

2. **Create a pull request**
   - Request review from team members
   - Your repo also comes with auto PR validators which will help your lint your files

3. **Merge to main**
   - Automatically triggers production deployment
   - Monitor deployment in GitHub Actions

4. **Verify changes**
   - Check your live site after deployment
   - Cache clearing ensures changes are immediately visible

### When to Use Manual Deployments

**Stage & Prod deployment** - Use when:
- You want to validate changes in staging before they go live
- Testing integrations or dynamic features
- Coordinating with other team activities

**Custom base SHA** - Use when:
- Recovering from a failed deployment
- Rolling back to a known good state
- Deploying a specific range of commits

**Deploy all files** - Use when:
- Setting up a new environment
- Applying global template changes
- Troubleshooting inconsistencies
- Major version updates or migrations

### Deployment Monitoring

After triggering a deployment:

1. **Navigate to GitHub Actions**
   - Go to your repository's Actions tab
   - Click on the running workflow

2. **Monitor progress**
   - View real-time logs for each step
   - Check for any errors or warnings
   - Verify which files are being deployed

3. **Validate deployment**
   - Visit your site after completion
   - Check that changes are visible
   - Test affected pages and features

4. **Deployment overview**
  - After a deployment, you can quickly check the overview of the deployment without having to go into each workflow in the Github action. The overview page will tell you which pages failed to upload or succeeded. 

## Troubleshooting

### Common Issues

#### No Files Deployed

**Symptoms:** Workflow completes successfully but site hasn't changed

**Solutions:**
- Verify that changes were made in `src/pages/` directory
- Check that files were committed and pushed to the correct branch
- Review the workflow logs to see which files were detected
- Try using `deployAll: true` to force deployment
- Ensure base SHA is set correctly (or leave empty for automatic detection)

#### Stale Content Visible

**Symptoms:** Deployment succeeded but old content still shows

**Solutions:**
- Wait for automatic cache clearing (30-60 seconds after deployment)
- Clear your browser cache
- Try opening the site in an incognito/private window
- Check cache clearing logs in the workflow run

#### Stale Content On Navigation

**Symptoms:** Deployment succeeded but old navigation shows on site after deployment

**Solutions:**
- the site uses session storage to store navigation 
- you can either close the browser session and re-open the site in a new window
- or you can manually clear the storage by using the `sesssionStorage.clear()` in the web inspector console

### Getting Help

If you encounter issues not covered in this guide:

1. Review the workflow logs in GitHub Actions for detailed error messages
2. Contact your Adobe Developer Platform support team in the slack channel #adobe-developer-website

## Additional Resources

- [ADP DevSite Workflow Repository](https://github.com/AdobeDocs/adp-devsite-workflow) - Reusable workflow source code
- [ADP DevSite Scripts Repository](https://github.com/AdobeDocs/adp-devsite-scripts) - Deployment scripts and utilities
- [GitHub Actions Documentation](https://docs.github.com/en/actions) - General workflow documentation
- [Example Implementation](https://github.com/AdobeDocs/dev-docs-template/blob/main/.github/workflows/deploy.yml) - Reference workflow configuration