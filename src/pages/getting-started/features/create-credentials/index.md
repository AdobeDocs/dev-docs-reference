---
title: Create Credentials Component
description: Generate API credentials directly on the Adobe Developer Website without redirecting to the Developer Console, supporting API Key and OAuth Server-to-Server credential types.
---

# Create Credentials Component 

Generate API credentials directly on the Adobe Developer Website without redirecting to the Developer Console

The Create Credentials component eliminates a major friction point in the Adobe developer experience by enabling developers to generate API credentials directly on the Adobe Developer Website without redirecting to the Developer Console. Previously, developers reading documentation, API references, or tutorials had to navigate to a separate experience, sign in again, and become familiar with the Developer Console interface just to obtain credentials—a workflow that product teams identified as a significant barrier to API adoption. This component was developed in collaboration with the Developer Console and App Builder teams to streamline credential creation and reduce time-to-first-API-call for developers.

The component supports multiple APIs, both API Key and OAuth Server-to-Server credential types, and includes enhanced features like a return flow experience, request access workflows, and a newly designed Org Switcher. Combined with the Try It functionality, developers can now complete their entire workflow on a single page: navigate to API reference documentation, create or retrieve authentication credentials, paste them into the Try It block, and execute API calls—replacing the previous multi-step process that required toggling between Developer Console, documentation sites, and tools like Postman. The component is currently live supporting the AEP Platform API and is available for other product teams to implement by coordinating with the Developer Website and Console teams via the #create-credentials Slack channel.

## Steps to take to implement CC 
