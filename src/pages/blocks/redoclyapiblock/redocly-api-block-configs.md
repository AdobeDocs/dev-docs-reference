---
title: Redocly API Block - Custom Configurations
description: Examples of Redocly API Block with custom configuration options including typography, code styling, and behavior settings.
layout: none
---

# Redocly API Block - Custom Configurations

Customize the Redocly API Block with various configuration options to control appearance, behavior, and functionality.

## Overview

The Redocly API Block supports extensive customization through attributes that control:
- Visual styling (typography, colors, spacing)
- Component behavior (search, sidebar, try-it panel)
- Content organization (sorting, expansion levels)
- Code samples and language options

## Default Values

When no options are specified, the component uses these defaults:

```javascript
{
  width: '500px',
  typography: 'fontFamily: `adobe-clean, "Source Sans Pro", sans-serif`',
  codeBlock: 'tokens: { punctuation: { color: "white" }}',
  disableSidebar: false,
  disableSearch: false,
  hideTryItPanel: false,
  scrollYOffset: 0,
  sortOperationsAlphabetically: false,
  sortTagsAlphabetically: false,
  jsonSampleExpandLevel: 2,
  generateCodeSamples: 'languages: [], skipOptionalParameters: false'
}
```

## Available Configuration Options

### Visual Customization

- **width**: Set custom width (default: `"500px"`)
  - Examples: `"600px"`, `"100%"`, `"50vw"`

- **typography**: Font family and size settings (default: adobe-clean font stack)
  - Format: `fontFamily: \`font-name, fallbacks\`, fontSize: 'size'`
  - Example: `fontFamily: \`"Source Sans Pro", sans-serif\`, fontSize: '16px'`

- **codeBlock**: Code block styling and token colors
  - Format: `tokens: { tokenType: { color: 'color' }}`
  - Example: `tokens: { punctuation: { color: 'red' }}`

### UI Components

- **disableSidebar**: Hide the left navigation sidebar (default: `false`)
  - Set to `true` to hide sidebar

- **disableSearch**: Disable the search functionality (default: `false`)
  - Set to `true` to disable search

- **hideTryItPanel**: Hide the interactive try-it-out panel (default: `false`)
  - Set to `true` to hide the try-it panel

- **scrollYOffset**: Offset for fixed headers in pixels (default: `0`)
  - Example: `scrollYOffset={64}` for 64px fixed header

### Content Options

- **sortOperationsAlphabetically**: Sort API operations alphabetically (default: `false`)
  - Set to `true` to enable alphabetical sorting

- **sortTagsAlphabetically**: Sort tags alphabetically (default: `false`)
  - Set to `true` to enable tag sorting

- **jsonSampleExpandLevel**: Control JSON sample expansion (default: `2`)
  - Options: Number (depth level), `"all"` (expand all), `1` (collapse all)

- **generateCodeSamples**: Specify languages for code samples
  - Format: `languages: [{ lang: 'language' }], skipOptionalParameters: true/false`
  - Example: `languages: [{ lang: 'curl' }, { lang: 'Node.js' }, { lang: 'Python' }]`

### Advanced

- **requestInterceptor**: Custom function to intercept API requests (default: empty)
  - Allows you to modify requests before they're sent
  - Use for authentication, logging, or custom headers

## Example

<RedoclyAPIBlock
    src="../../assets/openapi.yaml"
    width="100%"
    typography="fontFamily: `'Source Sans Pro', sans-serif`, fontSize: '16px'"
    codeBlock="tokens: { punctuation: { color: 'red' }}"
    disableSidebar={false}
    disableSearch={true}
    hideTryItPanel={true}
    scrollYOffset={64}
    sortOperationsAlphabetically={true}
    sortTagsAlphabetically={true}
    jsonSampleExpandLevel="all"
    generateCodeSamples="languages: [{ lang: 'curl' }, { lang: 'Node.js' }, { lang: 'JavaScript' }, { lang: 'Python' }], skipOptionalParameters: true"
    requestInterceptor="function(req, operation) { console.log('Request:', req); return req; }"
/>

## Best Practices

- Start with default settings and customize incrementally
- Use typography settings to match your brand guidelines
- Consider disabling sidebar for simpler APIs
- Test code sample languages with your target audience
- Use requestInterceptor for authentication or logging needs

## Related

- [Redocly API Block Default](/blocks/redoclyapiblock/redocly-api-block-default.md) - Default configuration
- [Redocly API Block No Layout](/blocks/redoclyapiblock/redocly-api-block-no-layout.md) - Full-page layout
