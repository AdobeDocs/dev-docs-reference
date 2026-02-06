---
title: Redocly API Block
description: Generate and display interactive API reference documentation directly on the Adobe Developer Website using OpenAPI specifications with the RedoclyAPIBlock component.
---

# Redocly API Block

Generate and display interactive API reference documentation directly on the Adobe Developer Website using OpenAPI specifications with the RedoclyAPIBlock component.

The Redocly API Block enables product teams to generate and display interactive API reference documentation directly on the Adobe Developer Website without relying on iframes or external hosting. By using the `<RedoclyAPIBlock>` component with a URL pointing to an OpenAPI YAML file, teams can host their own API specifications and have them rendered seamlessly by Redocly within the site's native experience. This approach provides a more integrated developer experience, allowing API documentation to maintain consistent styling with the Developer Website while leveraging Redocly's robust API documentation features. The component requires an on-premise license key (managed by the dev-site team) to be added to the repository's deploy.yml file, with all public repos in the AdobeDocs organization having automatic access to this development environment secret.

The component offers customization options including adjustable right panel width (defaults to 500px) and typography controls for font family and size, ensuring flexibility to match specific product needs. While local development testing is limited due to how Redocly API works—requiring teams to temporarily deploy to stage for testing—the component supports best practices like using Redocly's `x-summary` specification extension for long API response descriptions to prevent text truncation and layout issues. Teams can also implement full-width pages using custom layouts, providing maximum flexibility for presenting complex API documentation. This solution streamlines the process of publishing professional, interactive API references while maintaining the cohesive Adobe Developer Website experience.

## Steps to take to implement Redocly and learn more about Redocly

Go to our [Redocly Block information](../../../blocks/redoclyapiblock/redocly-api-block-default.md)