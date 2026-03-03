---
title: Credential Block - OAuth Flow
description: Configure the Get Credential block for OAuth 2.0 server-to-server credentials (Client ID, Client Secret, Scopes, access tokens).
---

# Credential Block - OAuth Flow

The **OAuth flow** credential block is used for **OAuth 2.0 client credentials** (server-to-server). Users get Client ID, Client Secret, Scopes, IMS Organization ID, and can generate access tokens. Child components only work when used inside the parent GetCredential block.

## Overview

The OAuth flow uses both **templateId** and **stageTemplateId** at the root and includes:

- **SignIn**: Sign-in prompt
- **Form**: Credential name, products, terms, sidebar (e.g. "OAuth server-to-server credential")
- **Card**: Success state with **AccessToken**, **CredentialDetails** (ClientId, ClientSecret, Scopes, ImsOrgID), next steps
- **Return**: Returning users: project selector, credential details, "create new credential," **AccessToken**
- **RequestAccess**: **EdgeCase** (NoProduct, Type1User, NotMember, NotSignUp), **RestrictedAccess**, **RequestAccessSide**
- **UnknownError**: Error state with help link

Optional block props: **credentialType** (OAuth), **service**.

## Top-level structure

```json
{
  "GetCredential": {
    "templateId": "***",
    "stageTemplateId": "***",
    "productName": "Firefly Services",
    "components": {
      "SignIn": { ... },
      "Form": { ... },
      "Card": { ... },
      "Return": { ... },
      "RequestAccess": { ... },
      "UnknownError": { ... }
    }
  }
}
```

| Property | Description |
|----------|-------------|
| **templateId** | Production template ID for the OAuth credential flow. |
| **stageTemplateId** | Stage template ID for the OAuth credential flow. |
| **productName** | Display name of the product. |
| **components** | SignIn, Form, Card, Return, RequestAccess, UnknownError. |

## Components

### SignIn

| Property | Description |
|----------|-------------|
| **title** | Heading (e.g. `"Get credentials"`). |
| **paragraph** | Short description of what credentials are for. |
| **buttonText** | Label for the sign-in button (e.g. `"Sign in to create credentials"`). |

### Form

New-credential form: **CredentialName**, **Products**, **AdobeDeveloperConsole**, **Side**.

| Property | Description |
|----------|-------------|
| **title** | Form heading. |
| **paragraph** | Intro text. |
| **components** | **CredentialName**, **Products**, **AdobeDeveloperConsole**, **Side**. |

- **CredentialName**: `label`, `description`, `range` (max length, e.g. `"45"`).
- **Products**: `label`; `items` array of `Product` with `label` and `icon` URL.
- **AdobeDeveloperConsole**: `label`, `linkText`, `href` (e.g. terms of use PDF).
- **Side**: `content.elements` array of objects with `type` (e.g. `h3`, `p`, `a`), `className`, `text` or `href`, optional `style`.

### Card

Success state after credential creation. Includes **AccessToken** and **CredentialDetails** (ClientId, ClientSecret, Scopes, ImsOrgID).

| Property | Description |
|----------|-------------|
| **title** | Card heading (e.g. `"Your credential is ready to use"`). |
| **paragraph** | Instructions (e.g. where to find the downloaded ZIP). |
| **devConsoleDirection** | Path to Developer Console (e.g. `"/console"`). |
| **nextStepsLabel** | Label for next-steps link. |
| **nextStepsHref** | URL for next steps. |
| **developerConsoleManage** | Label for "Manage on Developer Console". |
| **isCollapsable** | `"true"` or `"false"`. |
| **components** | **Side**, **Products**, **ProjectsDropdown**, **ManageDeveloperConsole**, **DevConsoleLink**, **AccessToken**, **CredentialDetails**. |

**CredentialDetails**: `heading`, `orderBy` (e.g. `"ClientId,Scopes,ClientSecret,ImsOrgID"`), `components`: **ClientId**, **ClientSecret** (`buttonLabel`), **Scopes** (`scope`), **ImsOrgID**, each with `heading`.

**AccessToken**: `heading`, `helpText`, `buttonLabel` (e.g. `"Generate and copy token"`).

### Return

Returning-user state: project selector, credential details, "create new credential," **AccessToken**.

| Property | Description |
|----------|-------------|
| **title** | Section title (e.g. `"Previously created projects"`). |
| **paragraph** | Short description. |
| **devConsoleDirection** | Path to Developer Console. |
| **nextStepsLabel**, **nextStepsHref** | Next-steps link. |
| **developerConsoleManage** | Label for manage link. |
| **isCollapsable**| Same as Card. |
| **components** | **Side** (with **Custom** and **NewCredential**), **CredentialDetails**, **ProjectsDropdown**, **ManageDeveloperConsole**, **AccessToken**, **DevConsoleLink**, **Products**. |

**ProjectsDropdown**: `label`, `subHeading`. **NewCredential**: `heading`, `buttonLabel`.

### RequestAccess

OAuth supports **EdgeCase**, **RestrictedAccess**, and **RequestAccessSide**.

**EdgeCase** (each with `title`, `buttonLabel`, `buttonLink`):

- **NoProduct**: Organization does not have access.
- **Type1User**: Access only for enterprise accounts.
- **NotMember**: Access not available.
- **NotSignUp**: Beta sign-up or log in required.

**RestrictedAccess**: `title` (e.g. `"Restricted Access"`), `buttonLabel` (e.g. `"Request access"`), **Products** (same structure as Form).

**RequestAccessSide**: Same pattern as **Form** **Side**—`content.elements` with `type`, `className`, `text` or `href`, optional `style`.

### UnknownError

| Property | Description |
|----------|-------------|
| **helpLink** | URL for help. |
| **helpLinkText** | Link label (e.g. `"Get Help"`). |

## Example (Firefly Services)

```json
{
  "GetCredential": {
    "templateId": "***",
    "stageTemplateId": "***",
    "productName": "Firefly Services",
    "components": {
      "SignIn": {
        "title": "Get credentials",
        "paragraph": "Create unique credentials that you will use to call multiple APIs from your application.",
        "buttonText": "Sign in to create credentials"
      },
      "Form": {
        "title": "Get credentials",
        "paragraph": "Create unique credentials that you will use to call multiple APIs from your application.",
        "components": {
          "CredentialName": {
            "label": "Credential name",
            "description": "Credential name must be unique and between 6 and 45 characters long and must not contain any special characters. A project will be automatically created with the same name in Adobe Developer Console.",
            "range": "45"
          },
          "Products": {
            "label": "Included products and services",
            "items": [
              {
                "Product": {
                  "label": "Firefly - Firefly Services",
                  "icon": "https://example.icon.png"
                }
              },
              {
                "Product": {
                  "label": "Adobe Photoshop - Firefly Services",
                  "icon": "https://example.icon.png"
                }
              }
            ]
          },
          "AdobeDeveloperConsole": {
            "label": "By checking this box, you agree to",
            "linkText": "Adobe Developer Terms of Use",
            "href": "https://wwwimages2.adobe.com/content/dam/cc/en/legal/servicetou/Adobe-Developer-Additional-Terms_en-US_20230822.pdf"
          },
          "Side": {
            "content": {
              "style": {
                "display": "flex",
                "gap": "16px",
                "flexDirection": "column"
              },
              "elements": [
                {
                  "type": "h3",
                  "className": "spectrum-Heading spectrum-Heading--sizeS side-header",
                  "text": "OAuth server-to-server credential"
                },
                {
                  "type": "p",
                  "className": "spectrum-Body spectrum-Body--sizeM",
                  "text": "This credential allows you to use industry standard OAuth2.0 libraries to generate access tokens using the OAuth 2.0 client credentials grant type."
                },
                {
                  "type": "h3",
                  "className": "spectrum-Heading spectrum-Heading--sizeS side-header",
                  "text": "Learn more"
                },
                {
                  "type": "a",
                  "className": "side-documentation",
                  "style": { "color": "#0265DC" },
                  "href": "https://some_help_link",
                  "text": "Authentication documentation"
                },
                {
                  "type": "a",
                  "className": "side-documentation",
                  "style": { "color": "#0265DC" },
                  "href": "https://some_help_link",
                  "text": "Firefly - Firefly and Creative Cloud Automation API documentation"
                },
                {
                  "type": "a",
                  "className": "side-documentation",
                  "style": { "color": "#0265DC" },
                  "href": "https://some_help_link",
                  "text": "Adobe Photoshop API documentation"
                },
                {
                  "type": "a",
                  "className": "side-documentation",
                  "style": { "color": "#0265DC" },
                  "href": "https://some_help_link",
                  "text": "Quota usage guide"
                }
              ]
            }
          }
        }
      },
      "UnknownError": {
        "helpLink": "https://some_help_link",
        "helpLinkText": "Get Help"
      },
      "Card": {
        "title": "Your credential is ready to use",
        "paragraph": "Check the downloads section of your browser for the ZIP file, or find it where you save downloads on your machine.",
        "devConsoleDirection": "/console",
        "nextStepsLabel": "Next steps",
        "nextStepsHref": "/credentials/nextsteps",
        "developerConsoleManage": "Manage on Developer Console",
        "isCollapsable": "true",
        "components": {
          "Side": {
            "content": {
              "style": {
                "display": "flex",
                "gap": "16px",
                "flexDirection": "column"
              },
              "elements": [
                {
                  "type": "h3",
                  "className": "spectrum-Heading spectrum-Heading--sizeS side-header",
                  "text": "OAuth server-to-server credential"
                },
                {
                  "type": "p",
                  "className": "spectrum-Body spectrum-Body--sizeM",
                  "text": "This credential allows you to use industry standard OAuth2.0 libraries to generate access tokens using the OAuth 2.0 client credentials grant type."
                },
                {
                  "type": "h3",
                  "className": "spectrum-Heading spectrum-Heading--sizeS side-header",
                  "text": "Learn more"
                },
                {
                  "type": "a",
                  "className": "side-documentation",
                  "style": { "color": "#0265DC" },
                  "href": "https://some_help_link",
                  "text": "Authentication documentation"
                },
                {
                  "type": "a",
                  "className": "side-documentation",
                  "style": { "color": "#0265DC" },
                  "href": "https://some_help_link",
                  "text": "Firefly - Firefly and Creative Cloud Automation API documentation"
                },
                {
                  "type": "a",
                  "className": "side-documentation",
                  "style": { "color": "#0265DC" },
                  "href": "https://some_help_link",
                  "text": "Adobe Photoshop API documentation"
                },
                {
                  "type": "a",
                  "className": "side-documentation",
                  "style": { "color": "#0265DC" },
                  "href": "https://some_help_link",
                  "text": "Quota usage guide"
                }
              ]
            }
          },
          "Products": {
            "label": "Included products and services",
            "items": [
              {
                "Product": {
                  "label": "Firefly - Firefly Services",
                  "icon": "https://example.icon.png"
                }
              },
              {
                "Product": {
                  "label": "Photoshop - Firefly Services",
                  "icon": "https://example.icon.png"
                }
              }
            ]
          },
          "ProjectsDropdown": {
            "label": "Projects",
            "subHeading": "Only your projects that contain credentials are shown"
          },
          "ManageDeveloperConsole": {
            "label": "Manage all your projects and credentials on Adobe Developer Console",
            "direction": "/console"
          },
          "DevConsoleLink": {
            "heading": "Developer Console Project"
          },
          "AccessToken": {
            "heading": "Access Token",
            "helpText": "",
            "buttonLabel": "Generate and copy token"
          },
          "CredentialDetails": {
            "heading": "Credential details",
            "orderBy": "ClientId,Scopes,ClientSecret,ImsOrgID",
            "components": {
              "ClientId": { "heading": "ClientId" },
              "ClientSecret": {
                "heading": "Client Secret",
                "buttonLabel": "Retrieve and copy client secret"
              },
              "Scopes": {
                "heading": "Scopes",
                "scope": "openid, AdobeID, read_organizations, firefly_api, ff_apis"
              },
              "ImsOrgID": { "heading": "IMS Organization ID" }
            }
          }
        }
      },
      "Return": {
        "title": "Previously created projects",
        "paragraph": "Select a project and access your existing credentials for Firefly - Firefly and Creative Cloud Automation.",
        "devConsoleDirection": "/console",
        "nextStepsLabel": "Next steps",
        "nextStepsHref": "/credentials/nextsteps",
        "developerConsoleManage": "Manage on Developer Console",
        "isCollapsable": "true",
        "components": {
          "Side": {
            "components": {
              "Custom": {
                "content": {
                  "style": {
                    "display": "flex",
                    "gap": "15px",
                    "flexDirection": "column",
                    "width": "100%"
                  },
                  "elements": [
                    {
                      "type": "h3",
                      "className": "spectrum-Heading spectrum-Heading--sizeM",
                      "text": "Welcome back"
                    },
                    {
                      "type": "p",
                      "className": "spectrum-Body spectrum-Body--sizeM",
                      "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation."
                    }
                  ]
                }
              },
              "NewCredential": {
                "heading": "Need another credential?",
                "buttonLabel": "Create new credential"
              }
            }
          },
          "CredentialDetails": {
            "heading": "Credential details",
            "orderBy": "ClientId,Scopes,ClientSecret,ImsOrgID",
            "components": {
              "ClientId": { "heading": "ClientId" },
              "ClientSecret": {
                "heading": "Client Secret",
                "buttonLabel": "Retrieve and copy client secret"
              },
              "Scopes": {
                "heading": "Scopes",
                "scope": "openid, AdobeID, read_organizations, firefly_api, ff_apis"
              },
              "ImsOrgID": { "heading": "IMS Organization ID" }
            }
          },
          "ProjectsDropdown": {
            "label": "Projects",
            "subHeading": "Only your projects that contain credentials are shown"
          },
          "ManageDeveloperConsole": {
            "label": "Manage all your projects and credentials on Adobe Developer Console",
            "direction": "/console/projects"
          },
          "AccessToken": {
            "heading": "Access Token",
            "helpText": "",
            "buttonLabel": "Generate and copy token"
          },
          "DevConsoleLink": {
            "heading": "Developer Console Project"
          },
          "Products": {
            "label": "Included products and services",
            "items": [
              {
                "Product": {
                  "label": "Firefly - Firefly Services",
                  "icon": "https://example.icon.png"
                }
              },
              {
                "Product": {
                  "label": "Adobe Photoshop - Firefly Services",
                  "icon": "https://raw.githubusercontent.com/AdobeDocs/cc-everywhere/main/src/pages/assets/cc-icon.png"
                }
              }
            ]
          }
        }
      },
      "RequestAccess": {
        "title": "Get credentials",
        "paragraph": "Create unique credentials that you will use to call multiple APIs from your application.",
        "components": {
          "EdgeCase": {
            "components": {
              "NoProduct": {
                "title": "Your organization does not have access to Firefly Services",
                "buttonLabel": "Contact us to learn more",
                "buttonLink": "#someLink"
              },
              "Type1User": {
                "title": "Access to Firefly Services is only available to enterprise accounts at this time.",
                "buttonLabel": "Learn more about Firefly Services",
                "buttonLink": "#someLink"
              },
              "NotMember": {
                "title": "Access to Firefly Services APIs is not available at this time.",
                "buttonLabel": "Learn more about Firefly Services",
                "buttonLink": "#someLink"
              },
              "NotSignUp": {
                "title": "Firefly Services APIs is available as part of the beta program. Sign up for the program or log in to an account that has access.",
                "buttonLabel": "Sign up for the beta",
                "buttonLink": "#someLink"
              }
            }
          },
          "RestrictedAccess": {
            "title": "Restricted Access",
            "buttonLabel": "Request access",
            "components": {
              "Products": {
                "label": "Included products and services",
                "items": [
                  {
                    "Product": {
                      "label": "Firefly API - Firefly Services",
                      "icon": "https://example.icon.png"
                    }
                  },
                  {
                    "Product": {
                      "label": "Adobe Photoshop API - Firefly Services",
                      "icon": "https://example.icon.png"
                    }
                  }
                ]
              }
            }
          },
          "RequestAccessSide": {
            "content": {
              "style": {
                "display": "flex",
                "gap": "16px",
                "flexDirection": "column"
              },
              "elements": [
                {
                  "type": "h3",
                  "className": "spectrum-Heading spectrum-Heading--sizeS side-header",
                  "text": "OAuth server-to-server credential"
                },
                {
                  "type": "p",
                  "className": "spectrum-Body spectrum-Body--sizeM",
                  "text": "This credential allows you to use industry standard OAuth2.0 libraries to generate access tokens using the OAuth 2.0 client credentials grant type."
                },
                {
                  "type": "h3",
                  "className": "spectrum-Heading spectrum-Heading--sizeS side-header",
                  "text": "Learn more"
                },
                {
                  "type": "a",
                  "className": "side-documentation",
                  "style": { "color": "#0265DC" },
                  "href": "https://some_help_link",
                  "text": "Authentication documentation"
                },
                {
                  "type": "a",
                  "className": "side-documentation",
                  "style": { "color": "#0265DC" },
                  "href": "https://some_help_link",
                  "text": "Firefly - Firefly and Creative Cloud Automation API documentation"
                },
                {
                  "type": "a",
                  "className": "side-documentation",
                  "style": { "color": "#0265DC" },
                  "href": "https://some_help_link",
                  "text": "Adobe Photoshop API documentation"
                },
                {
                  "type": "a",
                  "className": "side-documentation",
                  "style": { "color": "#0265DC" },
                  "href": "https://some_help_link",
                  "text": "Quota usage guide"
                }
              ]
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
- Provide clear **paragraph** and **description** text (e.g. credential name length).
- Set **nextStepsHref** and **helpLink** to real docs or support pages.

## Related

- [Credential Block](index.md) – Overview and credential types.
- [Credential Block - API Key](api-key.md) – API key flow.
- [Create Credentials](/getting_started/features/create-credentials/index.md) – Feature overview.
