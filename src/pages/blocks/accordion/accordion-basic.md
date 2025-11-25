---
title: Basic Accordion Block
description: Simple accordion example with collapsible text sections.
---

# Basic Accordion Example

This example shows a simple accordion with just heading and text content, perfect for FAQs or simple collapsible sections.

<AccordionItem slots="heading, text"/>

### What is this accordion component?

This is a collapsible content section that can expand and collapse when users click on the heading. It's useful for organizing large amounts of information in a compact, user-friendly way.

<AccordionItem slots="heading, text"/>

### How does it work?

The accordion component allows you to hide and show content dynamically. When a user clicks on a heading, the corresponding content panel toggles between visible and hidden states.

<AccordionItem slots="heading, text"/>

### Can I use multiple accordions?

Yes, you can include as many accordion items as needed on a single page. Each item operates independently, allowing users to expand or collapse sections based on their interests.

<AccordionItem slots="heading, text"/>

### What are the benefits?

Accordions help reduce page clutter by condensing information into expandable sections. This improves readability and helps users focus on the content that matters most to them.

## Usage

Use `slots` to identify the markdown content:

- `heading` (required) - The title of the accordion item
- `text` (required) - The body content

Each `<AccordionItem>` component creates a collapsible section that users can expand or collapse by clicking on the heading.

