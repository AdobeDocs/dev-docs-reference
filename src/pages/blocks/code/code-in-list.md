---
title: Code in Lists
description: Examples of code blocks embedded within list items and ordered/unordered lists.
---

# Code in Lists

Embed code blocks within ordered or unordered lists to create step-by-step tutorials, guides, or instructions with code examples.

## Syntax

Indent code blocks with 4 spaces (or 1 tab) to nest them within list items:

````
1. First step description

    ```bash
    command here
    ```

2. Second step description
````

## Example

## Installation Steps

Follow these steps to set up your development environment:

1. Install Node.js and npm on your system

    ```bash
    node --version
    npm --version
    ```

1. Clone the repository to your local machine

    ```bash
    git clone https://github.com/example/project.git
    cd project
    ```

1. Install project dependencies

    ```bash
    npm install
    ```

1. Configure environment variables by creating a `.env` file

    ```bash
    cp .env.example .env
    ```

1. Start the development server

    ```bash
    npm run dev
    ```

1. Open your browser and navigate to `http://localhost:3000`

## Best Practices

- Indent code blocks with 4 spaces or 1 tab to nest within list items
- Use for step-by-step tutorials and installation guides
- Add explanatory text before and after code blocks for context
