---
title: Credential Block
description: Embed the Get Credential flow so users can create and manage API credentials from your documentation. Supports OAuth (server-to-server) and API key credential types.
---

# Credential Block

The **Get Credential** block lets you add credential creation and management to your developer docs. Users can sign in, create credentials, view existing credentials, and request access—all driven by a JSON configuration. Child components only work when used inside the parent GetCredential block.

## Credential types

The block supports two flows, each with a different JSON shape:

| Aspect | OAuth flow | API key flow |
|--------|------------|--------------|
| **Use case** | OAuth 2.0 client credentials (server-to-server). Client ID, Client Secret, Scopes, access tokens. | API key credentials. API Key, allowed domains, optional code sample download. |
| **Root IDs** | `templateId` and `stageTemplateId`  | `templateId` and `stageTemplateId` |
| **Form** | CredentialName, Products, AdobeDeveloperConsole, Side | Same, plus **AllowedOrigins**, **Downloads** (code sample) |
| **Card / Return** | **AccessToken**, CredentialDetails: ClientId, ClientSecret, Scopes, ImsOrgID | CredentialDetails: APIKey, AllowedOrigins, OrganizationName, ImsOrgID (no AccessToken) |
| **RequestAccess** | EdgeCase (NoProduct, Type1User, NotMember, NotSignUp), RestrictedAccess, RequestAccessSide | Typically **RestrictedAccess** and **Products** only |

Use the **credentialType** prop (or equivalent) to choose the flow;

## Documentation

- **[OAuth Flow](oauth.md)** – OAuth 2.0 server-to-server credentials (Client ID, Client Secret, Scopes, access tokens).
- **[API Key Flow](api-key.md)** – API key credentials (API Key, allowed domains, optional code sample).

## Block props

Optional props on the Get Credential block itself:

- **credentialType**: Type of credential (e.g. OAuth vs API key).
- **service**: Adobe product or service.
