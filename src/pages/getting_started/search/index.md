---
title: EDS Search
description: Learn how to optimize your EDS pages for DevSite Search and Google SEO, including how the search indexer works and content best practices.
---

# EDS Search
For the best EDS DevSite Search and Google SEO search results we recommend that each product team follow the best practices when creating a page.

Content is king for the best results ensure specifically all Marketing pages and high level Documentation pages and guides incorporate keywords, titles and descriptions. 

For the best DevSite Search and Google SEO search results we recommend that each product team focus on creating high-quality, user-friendly content that incorporates Keywords, Title and Descriptions.

## Keyword Research
Identify relevant keywords your target audience uses when searching for your products or services.
- **Content Optimization:**
  - **Create high-quality, original content:** Focus on providing valuable and informative content that satisfies user needs.
  - **Use keywords strategically:** Incorporate relevant keywords naturally within your content, titles, descriptions, and alt text.
  - **Optimize images:** Use descriptive alt text for images to help search engines understand their content.
  - **Improve page speed:** Optimize images, minimize code, and use a fast hosting provider to ensure your website loads quickly.
  - **Ensure mobile-friendliness:** Make sure your website is responsive and looks good on all devices.

## How the Search Indexer Works

Understanding how the DevSite search indexer processes your content can help you create more discoverable pages.

### What Gets Indexed

The search indexer extracts and indexes the following fields from your EDS pages:

| Field | Description |
|-------|-------------|
| **Title** | Page title from metadata or H1 heading |
| **Description** | Meta description or first paragraph content |
| **Content** | Full page content, segmented by headings |
| **Headings** | Array of all headings (H1-H4) found on the page |
| **Hierarchy** | Structured heading levels (lvl0, lvl1, lvl2) for navigation |
| **Keywords** | Keywords from page metadata |
| **Last Modified** | Content modification date from sitemap |

### Content Segmentation

Pages are automatically segmented into searchable chunks based on heading structure:
- Each section under an H2, H3, or H4 becomes a separate searchable record
- This allows users to find specific sections within long pages
- Proper heading hierarchy improves search relevance

### When Indexing Happens

- **Automated updates:** The indexer runs nightly at midnight UTC
- **Timestamp-based updates:** Only pages with newer `lastmod` timestamps in the sitemap are re-indexed
- **New repos/micro-sites:** Must be explicitly added to the indexer configuration

<InlineAlert variant="info" slots="text"/>

Changes to your content will typically appear in search results within 24 hours. If you have a new repository or micro-site, please request it be added to the indexer once deployed to production (see below).

## Requesting Indexing for New Content

If you have a new repository or micro-site that needs to be indexed:

1. Deploy your content to production
2. Verify your pages appear in the sitemap
3. Contact the Adobe Developer Website team in Slack `#adobe-developer-website` to request your content be added to the indexer configuration
4. Indexing will begin with the next nightly run (midnight UTC)

## EDS Search Best Practices
- **Use natural keywords in content**
  - Think about how users would search for the content and include those words in the body text and headings.
- **Use clear, specific titles**
  - The page title and H1 are used in search. Make sure they describe the topic (e.g., “Install Adobe SDK on Android” instead of “Getting Started”).
- **Write a helpful first paragraph**
  - The intro is used as the search snippet. It should quickly explain what the page is about and include useful terms.
- **Check metadata is set**
  - EDS usually creates metadata like title and description, but it's good to verify that EDS identified good, descriptive title and summary for each page in the preview or front matter.
- **Use headings to structure content**
  - The indexer uses H2–H4s to break pages into sections. Use them properly, don’t skip levels or overload a single section with too much content.
- **Keep pages focused and scannable**
  - Split long content into sections. Avoid giant walls of text under one heading as each section becomes a separate searchable item.
- **Avoid duplicate content across pages**
  - Reusing the same content on multiple pages can mess with search relevance. 

## On-Page SEO Optimization
- **Keyword Research:** Identify relevant keywords your target audience uses when searching online and incorporate into the content. 
- **Content Creation:** Write engaging, high-quality content that answers user search queries and provides value. 
- **Title Tags and Meta Descriptions:** Optimize these elements to be clear, concise, and keyword-rich. 
- **Image Optimization:** Compress images and add descriptive alt text to improve loading speed and search engine understanding. 
- **Internal Linking:** Use internal links to connect different pages on your site, improving user experience and SEO. 
- **Mobile Optimization:** Ensure your website is fully responsive and user-friendly on mobile devices. 
- **Internal Linking:** Link to other relevant pages on your website to help search engines understand the structure and hierarchy of your content.