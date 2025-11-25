---
title: On This Page
description: Automatic table of contents sidebar that displays H2 and H3 headings for easy page navigation.
---

# On This Page

The "On This Page" component is an automatically generated table of contents that appears on the right side of documentation pages, providing quick navigation to different sections within the current page.

## Overview

The "On This Page" component is **automatically generated** based on the heading structure of your markdown content. It requires no configuration or special setup - it dynamically creates navigation links for all H2 (`##`) and H3 (`###`) headings on the page.

## How It Works

The component scans your markdown file and:

1. Detects all H2 and H3 headings
2. Creates anchor links for each heading
3. Displays them in a hierarchical sidebar on the right
4. Updates the active link as users scroll through the page

### Heading Levels Included

- **H2 headings (`##`)**: Displayed as top-level items
- **H3 headings (`###`)**: Displayed as nested items under their parent H2

### Heading Levels Excluded

- **H1 (`#`)**: Not included (typically the page title)
- **H4 and below (`####`)**: Not included to maintain clarity

## Example Structure

If your markdown contains:

```markdown
# Page Title

## Introduction

This is the intro section.

## Getting Started

### Installation

Instructions here.

### Configuration

Setup details here.

## Advanced Topics

### Performance Optimization

Tips and tricks.
```

The "On This Page" sidebar will display:

![onthispage](../../assets/onthispage.png)

## Best Practices

- **Use descriptive headings**: Heading text appears directly in the navigation
- **Maintain logical hierarchy**: Structure content with clear H2 sections and H3 subsections
- **Keep headings concise**: Long headings may be truncated in the sidebar
- **Avoid deep nesting**: Stick to H2 and H3 for optimal readability
- **Use consistent formatting**: Follow standard heading syntax with proper spacing

## Writing Effective Headings

### Good Examples

```markdown
## Installation
### Prerequisites
### Step-by-Step Guide

## API Reference
### Methods
### Properties
```

### Avoid

```markdown
## This Is An Extremely Long Heading That Will Be Difficult to Read in the Sidebar Navigation
### too-many-hyphens-and-underscores_in_heading
```

## Technical Details

- Headings are automatically converted to URL-safe anchor IDs
- Clicking a link in the sidebar smoothly scrolls to that section
- The active section is highlighted as users scroll
- Works seamlessly with all markdown content

