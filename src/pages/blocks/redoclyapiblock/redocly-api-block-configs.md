---
title: Redocly API Block - Custom Configurations
description: Examples of Redocly API Block with custom configuration options including typography, code styling, and behavior settings.
layout: none
---

# Redocly API Block - Custom Configurations

Customize the Redocly API Block with configuration options to control appearance and behavior.

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

## Configuration Options

### Visual Options
- **width**: Custom width (default: `"500px"`)
- **typography**: Font family and size settings
- **codeBlock**: Code block styling and token colors

### UI Options
- **disableSidebar**: Hide left sidebar (default: `false`)
- **disableSearch**: Disable search (default: `false`)
- **hideTryItPanel**: Hide try-it panel (default: `false`)
- **scrollYOffset**: Offset for fixed headers (default: `0`)

### Content Options
- **sortOperationsAlphabetically**: Sort operations (default: `false`)
- **sortTagsAlphabetically**: Sort tags (default: `false`)
- **jsonSampleExpandLevel**: JSON expansion depth (default: `2`)
- **generateCodeSamples**: Specify code sample languages

### Advanced
- **requestInterceptor**: Custom function to intercept requests

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

- Start with default settings and customize as needed
- Use typography to match your brand
- Consider disabling sidebar for simpler APIs
- Test code sample languages with your audience

## Related

- [Redocly API Block Default](/blocks/redoclyapiblock/redocly-api-block-default.md) - Default configuration
- [Redocly API Block No Sidebar](/blocks/redoclyapiblock/redocly-api-block-no-sidebar.md) - Without sidebar
