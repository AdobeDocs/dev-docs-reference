---
title: ADP Developer Site - Getting Started
description: A guide introducing the Next Generation Developer Website and the transition from Gatsby to Edge Delivery Services
---

# Welcome to the new Developer Website!

Greetings prospective user of Adobe Developer Website!

Today, the Developer Website uses Edge Delivery Services (EDS)/Franklin and Gatsby. EDS/Franklin is used mainly for marketing material with content from Google Drive. Gatsby is mainly used for documentation with content from GitHub. Out of the 70+ repos on the Developer Website, 90% of the users utilize Gatsby.

The Next Generation Developer Website is the effort to unite the Developer Website under Edge Delivery Services as the technology stack.

## Why the change from Gatsby to EDS?

Microsites on the Developer Website have become large and complex. As a result, there is an increased maintenance and support load that is unsustainable for the size of our team. Additionally, Gatsby has been acquired recently and support for its framework is unknown.

The Developer Website team supports the platform for product teams to deploy documentation and marketing pages. Because we support teams across Adobe, we need to maintain the look and feel of the Website in a similar environment for the Developer Experience. When a change to the Global Navigation or Footer is needed, or an update across the whole platform, we need to push out a site wide theme update which is difficult to do with the current Gatsby setup.

## EDS to the rescue

EDS is an Adobe product; thus giving us better access and insight to the product team. EDS recently launched a new feature where content can live in GitHub repos.
This means Gatsby users can keep their repos and the same markdown content.

There are also some immediate tangible benefits to product teams that will be available:

* Optimized content blocks for performance, analytics, accessibility and mobile responsiveness.
* Additional features such as A/B testing and RUM analytics will be offered by EDS.
* No more React, less dependency to node modules Gatsby/React ecosystem, pure vanilla JS and CSS.
* Currently, when pushing a deployment on Gatsby, there is downtime from 1-5 minutes as the changes are being pushed to production. In EDS, there will be no downtime and deployments will not cause their microsite to 404 while the new changes are pushed to production.

## Architecture

Gatsby EDS Architecture:

![GatsbyEDSArchitecture](../assets/gatsby_eds_architecture.png)

Next Gen Architecture:

![NextGenArchitecture](../assets/next_gen_architecture.png)
