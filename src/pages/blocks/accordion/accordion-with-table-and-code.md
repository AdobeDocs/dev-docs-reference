---
title: Accordion Block with Table and Code
description: Complex accordion example with tables and code blocks for detailed technical documentation.
---

# Accordion with Table and Code Example

This example demonstrates a complex accordion with multiple content types including tables, text descriptions, and code blocks. This is ideal for displaying structured data or step-by-step processes.

Each step shown in the following accordion is described in detail below. Each description includes sample data that demonstrates the different content types available.

## Accordion Heading

<AccordionItem slots="heading, table, text, code"/>

### 1. Initial Setup 

| Step | Description | Duration | Status | Endpoint |
| --- | --- | --- | --- | --- |
| 1 | User initiates the process and the system begins loading resources | 0s | Starting | `/api/initialize` |

This action represents the beginning of a workflow. The system state transitions from idle to active. A unique identifier is generated and returned to the client for tracking purposes. This identifier will be used in subsequent steps.

```json
{
  "eventType": "process.start",
  "timestamp": "2024-01-15T10:00:00.000Z",
  "data": {
    "sessionId": "abc123",
    "config": {
      "name": "Sample Process",
      "timeout": 60,
      "mode": "standard",
      "version": "1.0.0"
    }
  }
}
```

<AccordionItem slots="heading, table, text, code" />

### 2. Loading Phase

| Step | Description | Duration | Status | Endpoint |
| --- | --- | --- | --- | --- |
| 2 | System enters loading state while gathering resources | 1s | Loading | `/api/loading` |

The process enters a waiting state while necessary resources are retrieved. Progress indicators may be displayed to the user during this phase.

```json
{
  "eventType": "state.loading",
  "timestamp": "2024-01-15T10:00:01.000Z",
  "data": {
    "sessionId": "abc123",
    "progress": 0
  }
}
```

<AccordionItem slots="heading, table, text"/>

### 3. Status Check

| Step | Description | Duration | Status | Endpoint |
| --- | --- | --- | --- | --- |
| 3 | Periodic status update is transmitted | 10s | Active | `/api/heartbeat` |

A routine status signal is sent to maintain the connection and confirm system health.


<AccordionItem slots="heading, table, text, code"/>

### 4. User Pause

| Step | Description | Duration | Status | Endpoint |
| --- | --- | --- | --- | --- |
| 4 | User initiates a pause action | 15s | Paused | `/api/pause` |

The user triggers a pause action, temporarily halting the current process.

```json
{
  "eventType": "action.pause",
  "timestamp": "2024-01-15T10:00:15.000Z",
  "data": {
    "sessionId": "abc123",
    "counter": 12
  }
}
```

<AccordionItem slots="heading, table, text, code"/>

### 5. End Session

| Step | Description | Duration | Status | Endpoint |
| --- | --- | --- | --- | --- |
| 5 | User terminates the session before completion | 29s | Ended | `/api/end` |

The user exits the application. A termination signal is sent to close the session immediately.

```json
{
  "eventType": "process.end",
  "timestamp": "2024-01-15T10:00:29Z",
  "data": {
    "sessionId": "abc123",
    "counter": 17
  }
}
```

## Usage

Use `slots` to identify the markdown content for each `<AccordionItem>`:

- `heading` (required) - The title of the accordion item
- `table` (optional) - Tabular data
- `text` (optional) - Body text with descriptions
- `code` (optional) - Code blocks with examples

You can mix and match slots based on your content needs. Each accordion item can have different slot combinations.

