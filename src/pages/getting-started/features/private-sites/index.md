---
title: Private Beta and Secured Websites
description: Publish developer documentation and marketing content behind authentication gates for beta programs and premium customer experiences on developer.adobe.com.
---

# Private Beta and Secured Websites

Publish developer documentation and marketing content behind authentication gates for beta programs

The Private Beta and Secured Websites feature addresses a critical need for Adobe product teams to publish high-quality developer documentation and marketing content for beta programs and premium customer experiences behind authentication gates on developer.adobe.com. Previously, product teams like CCXT had to resort to distributing beta documentation as PDF files via email to NDA-approved developers—a workflow that created significant friction for both teams and developers. This manual process required extra effort to convert documentation to PDFs, degraded the developer experience by forcing users to search through email folders and potentially install additional software, and made updates nearly impossible without resending files to the entire group. The initiative was driven by CCXT's requirement to support Firefly beta websites and provides a scalable, durable mechanism for teams to iterate on new features and gather detailed feedback from select groups while maintaining confidentiality.

The solution provides architecture and infrastructure for secured websites that integrate with Adobe's pre-release program (Sofia/Floodgate) to verify access based on Adobe ID membership in product-maintained lists. When developers sign in, the system checks their eligibility against the pre-release program list to determine access to private beta content, enabling product teams to control who sees what documentation without managing separate distribution channels. Beyond private beta use cases, this feature also enables product teams to create logged-in customer experiences with premium content exclusively for their customers, giving teams flexibility in how they surface and deliver content. This approach provides a consistent, seamless developer journey directly on developer.adobe.com, eliminates the PDF distribution workflow, and allows teams to make real-time updates to documentation while maintaining the security and confidentiality required for pre-release products.

For more information about how to connet your pre release program to your secured site reach out to the DevSite team at `#adobe-developer-website`

## Steps to take to implement Private Beta and Secured Websites