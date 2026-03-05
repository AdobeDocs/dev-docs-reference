---
title: Credential Block - API Key Flow
description: Configure the Get Credential block for API key credentials (API Key, allowed domains, optional code sample download).
---

# Credential Block - API Key Flow

The **API key flow** credential block is used for **API key credentials**. Users get an API Key, allowed domains, and organization info; you can optionally offer a personalized code sample download. Child components only work when used inside the parent GetCredential block.

## Overview

The API key flow uses both **templateId** and **stageTemplateId** at the root and includes:

- **SignIn**: Sign-in prompt
- **Form**: Credential name, AllowedOrigins, Downloads (code sample), products, terms, sidebar (e.g. "API key credential")
- **Card**: Success state with CredentialDetails (APIKey, AllowedOrigins, OrganizationName, ImsOrgID)—no AccessToken
- **Return**: Returning users: project selector, credential details, "create new credential"
- **RequestAccess**: Typically **RestrictedAccess** and **Products** only (no EdgeCase / RequestAccessSide)

Optional block props: **credentialType** (e.g. apiKey), **service**.

## Top-level structure

```json
{
  "GetCredential": {
    "templateId": "***",
    "stageTemplateId": "***",
    "productName": "Your product name",
    "components": {
      "SignIn": { ... },
      "Form": { ... },
      "Card": { ... },
      "Return": { ... },
      "RequestAccess": { ... }
    }
  }
}
```

| Property | Description |
|----------|-------------|
| **templateId** | Production Template ID for the API key credential flow. |
| **stageTemplateId** | Stage template ID. |
| **productName** | Display name of the product. |
| **components** | SignIn, Form, Card, Return, RequestAccess. |

## Components

### SignIn

| Property | Description |
|----------|-------------|
| **title** | Heading (e.g. `"Get credentials"`). |
| **paragraph** | Short description of what credentials are for. |
| **buttonText** | Label for the sign-in button. |

### Form

New-credential form: **CredentialName**, **AllowedOrigins**, **Products**, **Downloads**, **AdobeDeveloperConsole**, **Side**.

| Property | Description |
|----------|-------------|
| **title** | Form heading. |
| **paragraph** | Intro text. |
| **components** | **CredentialName**, **AllowedOrigins**, **Products**, **Downloads**, **AdobeDeveloperConsole**, **Side**. |

**CredentialName**: `label`, `description`, `range` (e.g. `"45"`).

**AllowedOrigins**: `label`, `contextHelp` (boolean), `contextHelpHeading`, `contextHelpText`, `contextHelpLink`, `contextHelpLabelForLink`, `description`, `placeholder` (e.g. `"www.domain-1.com, *.my-domain.com, localhost:5000"`).

**Products**: `label`; `items` array of `Product` with `label` and `icon` URL.

**Downloads**: `label` (e.g. `"Download a personalized code sample"`), `contextHelp`, `contextHelpHeading`, `items` array of `Download` with `title` (e.g. `"JavaScript"`) and `href` (ZIP URL).

**AdobeDeveloperConsole**: `label`, `linkText`, `href`. **Side**: `content.elements` array (same pattern as OAuth).

### Card

Success state. No AccessToken. **CredentialDetails**: APIKey, AllowedOrigins, OrganizationName, ImsOrgID.

| Property | Description |
|----------|-------------|
| **title** | Card heading. |
| **paragraph** | Instructions (e.g. where to find the downloaded ZIP). |
| **nextStepsLabel** | Label for next-steps link. |
| **nextStepsHref** | Full URL for next steps. |
| **isCollapsable** | `"true"` or `"false"`. |
| **components** | **Side**, **Products**, **DevConsoleLink**, **CredentialDetails**. |

**CredentialDetails**: `heading`, `orderBy` (e.g. `"APIKey,OrganizationName,ImsOrgID,AllowedOrigins"`), `components`: **APIKey**, **AllowedOrigins**, **OrganizationName**, each with `heading`.

### Return

Returning-user state. **ManageDeveloperConsole.direction** can be a full URL (e.g. `"https://developer.adobe.com/console/projects"`).

| Property | Description |
|----------|-------------|
| **title** | Section title. |
| **paragraph** | Short description. |
| **nextStepsLabel**, **nextStepsHref** | Next-steps link. |
| **isCollapsable** | Same as Card. |
| **components** | **Side** (with **Custom**, **NewCredential**), **CredentialDetails**, **ProjectsDropdown**, **ManageDeveloperConsole**, **DevConsoleLink**, **Products**. |

**ProjectsDropdown**: `label`, `subHeading`. **NewCredential**: `heading`, `buttonLabel`.

### RequestAccess

API key flow typically uses only **RestrictedAccess** and **Products**.

**RestrictedAccess**: `title` (e.g. `"Restricted Access"`), `buttonLabel` (e.g. `"Request access"`), **Products** (same structure as Form).

## Example (Express Embed SDK)

```json
{
  "GetCredential": {
    "templateId": "***",
    "stageTemplateId": "***",
    "productName": "Express Embed SDK",
    "components": {
      "SignIn": {
        "title": "Get credentials",
        "paragraph": "Create unique credentials that you will use to call Adobe Express Embed SDK from your application.",
        "buttonText": "Sign in to create credentials"
      },
      "Form": {
        "title": "Get credentials",
        "paragraph": "Create unique credentials that you will use to call Adobe Express Embed SDK from your application.",
        "components": {
          "CredentialName": {
            "label": "Credential name",
            "description": "Credential name must be unique and between 6 and 45 characters long and must not contain any special characters. A project will be automatically created with the same name in Adobe Developer Console.",
            "range": "45"
          },
          "AllowedOrigins": {
            "label": "Allowed domains (up to 5)",
            "contextHelp": true,
            "contextHelpHeading": "What are allowed domains",
            "placeholder": "Example: www.domain-1.com, www.domain-2.com, *.my-domain.com, localhost:5000",
            "contextHelpText": "To prevent a third party from using your client ID on their own website, the use of your client ID is restricted to a list of domains that you specifically authorize.",
            "contextHelpLink": "https://www.adobe.com/",
            "contextHelpLabelForLink": "Learn more in our documentation",
            "description": "Use wildcards to enter multiple subdomains (*.my-domain.com) or commas to separate multiple domains. During local development, you can include ports greater than 1023 with localhost (e.g. localhost:3000)."
          },
          "Products": {
            "label": "Included products and services",
            "items": [{ "Product": { "label": "Adobe Express Embed SDK", "icon": "https://example.com/cc-icon.png" } }]
          },
          "Downloads": {
            "label": "Download a personalized code sample",
            "contextHelp": true,
            "contextHelpHeading": "Select Language",
            "items": [{ "Download": { "title": "JavaScript", "href": "https://example.com/DemoCode.zip" } }]
          },
          "AdobeDeveloperConsole": {
            "label": "By checking this box, you agree to",
            "linkText": "Adobe Developer Terms of Use",
            "href": "https://wwwimages2.adobe.com/content/dam/cc/en/legal/servicetou/Adobe-Developer-Additional-Terms_en-US_20230822.pdf"
          },
          "Side": {
            "content": {
              "style": { "display": "flex", "gap": "16px", "flexDirection": "column" },
              "elements": [
                { "type": "h3", "className": "spectrum-Heading spectrum-Heading--sizeS side-header", "text": "API key credential" },
                { "type": "p", "className": "spectrum-Body spectrum-Body--sizeM", "text": "Submitting this form creates an API Key credential. The API key credential identifies your application to Adobe servers and can help accept or reject requests originating from certain domains." },
                { "type": "h3", "className": "spectrum-Heading spectrum-Heading--sizeS side-header", "text": "Learn more" },
                { "type": "a", "className": "side-documentation", "style": { "color": "#0265DC" }, "href": "https://example.com/", "text": "Quickstart guide" },
                { "type": "a", "className": "side-documentation", "style": { "color": "#0265DC" }, "href": "https://example.com/", "text": "Adobe Express Embed SDK documentation" }
              ]
            }
          }
        }
      },
      "Card": {
        "title": "Your credential is ready to use",
        "paragraph": "Check the downloads section of your browser for the ZIP file, or find it where you save downloads on your machine.",
        "nextStepsLabel": "Next steps",
        "nextStepsHref": "https://example.com/",
        "isCollapsable": "true",
        "components": {
          "Side": { "content": { "style": { "display": "flex", "gap": "16px", "flexDirection": "column" }, "elements": [
            { "type": "h3", "className": "spectrum-Heading spectrum-Heading--sizeS side-header", "text": "API key credential" },
            { "type": "p", "className": "spectrum-Body spectrum-Body--sizeM", "text": "An API Key credential was created." },
            { "type": "h3", "className": "spectrum-Heading spectrum-Heading--sizeS side-header", "text": "Learn more" },
            { "type": "a", "className": "side-documentation", "style": { "color": "#0265DC" }, "href": "https://example.com/", "text": "Quickstart guide" }
          ] } },
          "Products": { "label": "Included products and services", "items": [{ "Product": { "label": "Adobe Express Embed SDK", "icon": "https://example.com/cc-icon.png" } }] },
          "DevConsoleLink": { "heading": "Developer Console Project" },
          "CredentialDetails": {
            "heading": "Credential details",
            "orderBy": "APIKey,OrganizationName,ImsOrgID,AllowedOrigins",
            "components": {
              "APIKey": { "heading": "API Key" },
              "AllowedOrigins": { "heading": "Allowed domains" },
              "OrganizationName": { "heading": "Organization" }
            }
          }
        }
      },
      "Return": {
        "title": "Previously created projects",
        "paragraph": "Select a project and access your existing credentials for Adobe Express Embed SDK.",
        "nextStepsLabel": "Next steps",
        "nextStepsHref": "https://example.com/",
        "isCollapsable": "true",
        "components": {
          "Side": {
            "components": {
              "Custom": {
                "content": {
                  "style": { "display": "flex", "gap": "15px", "flexDirection": "column", "width": "100%" },
                  "elements": [
                    { "type": "h3", "className": "spectrum-Heading spectrum-Heading--sizeM", "text": "Welcome back" },
                    { "type": "p", "className": "spectrum-Body spectrum-Body--sizeM", "text": "View your existing Adobe Express Embed SDK credentials and generate new ones." }
                  ]
                }
              },
              "NewCredential": { "heading": "Need another credential?", "buttonLabel": "Create new credential" }
            }
          },
          "CredentialDetails": {
            "heading": "Credential details",
            "orderBy": "APIKey,OrganizationName,ImsOrgID,AllowedOrigins",
            "components": {
              "APIKey": { "heading": "API Key" },
              "AllowedOrigins": { "heading": "Allowed domains" },
              "OrganizationName": { "heading": "Organization" }
            }
          },
          "ProjectsDropdown": { "label": "Projects", "subHeading": "Only your projects that contain credentials are shown" },
          "ManageDeveloperConsole": { "label": "Manage all your projects and credentials on Adobe Developer Console", "direction": "https://example.com/" },
          "DevConsoleLink": { "heading": "Developer Console Project" },
          "Products": { "label": "Included products and services", "items": [{ "Product": { "label": "Adobe Express Embed SDK", "icon": "https://example.com/cc-icon.png" } }] }
        }
      },
      "RequestAccess": {
        "title": "Get credentials",
        "paragraph": "Create unique credentials that you will use to call Adobe Express Embed SDK from your application.",
        "components": {
          "RestrictedAccess": {
            "title": "Restricted Access",
            "buttonLabel": "Request access",
            "components": {
              "Products": {
                "label": "Included products and services",
                "items": [{ "Product": { "label": "Adobe Express Embed SDK", "icon": "https://example.com/cc-icon.png" } }]
              }
            }
          }
        }
      }
    }
  }
}
```

## Best practices

- Keep **productName** and **Products** in sync with Adobe Developer Console and your backend.
- Use **templateId** and **stageTemplateId** from your environment (stage vs production).
- Explain **AllowedOrigins** clearly (wildcards, comma-separated, localhost:port) and use **contextHelp** where helpful.
- Set **nextStepsHref** to real documentation (e.g. quickstart).

## Related

- [Credential Block](index.md) – Overview and credential types.
- [Credential Block - OAuth Flow](oauth.md) – OAuth server-to-server flow.
- [Create Credentials](/getting_started/features/create-credentials/index.md) – Feature overview.
