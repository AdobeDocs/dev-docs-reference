---
title: Accordion Block
description: Learn how to use the Accordion block to create collapsible content sections for organizing information in your documentation.
---

# Accordion Block

Collapsible content sections.

## Syntax

```markdown
<AccordionItem slots="heading, text"/>

### Section heading

Content goes here.
```

## Parameters

- **slots**: Content types
  - `"heading, text"` - Text only
  - `"heading, text, table"` - With tables
  - `"heading, text, code"` - With code blocks
  - Mix and match as needed

## Examples

### Basic Accordion

<AccordionItem slots="heading, text"/>

#### What is this accordion component?

This is a collapsible content section that can expand and collapse when users click on the heading. It's useful for organizing large amounts of information in a compact, user-friendly way.

<AccordionItem slots="heading, text"/>

#### How does it work?

The accordion component allows you to hide and show content dynamically. When a user clicks on a heading, the corresponding content panel toggles between visible and hidden states.

<AccordionItem slots="heading, text"/>

#### Can I use multiple accordions?

Yes, you can include as many accordion items as needed on a single page. Each item operates independently, allowing users to expand or collapse sections based on their interests.

### With Table and Code

<AccordionItem slots="heading, table, text, code"/>

#### 1. Initial Setup 

| Step | Description | Duration | Status | Endpoint |
| --- | --- | --- | --- | --- |
| 1 | User initiates the process and the system begins loading resources | 0s | Starting | `/api/initialize` |

This action represents the beginning of a workflow. The system state transitions from idle to active.

```json
{
  "eventType": "process.start",
  "timestamp": "2024-01-15T10:00:00.000Z",
  "data": {
    "sessionId": "abc123",
    "config": {
      "name": "Sample Process",
      "timeout": 60
    }
  }
}
```

<AccordionItem slots="heading, table, text"/>

#### 2. Status Check

| Step | Description | Duration | Status | Endpoint |
| --- | --- | --- | --- | --- |
| 3 | Periodic status update is transmitted | 10s | Active | `/api/heartbeat` |

A routine status signal is sent to maintain the connection and confirm system health.
