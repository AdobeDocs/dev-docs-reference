---
title: Code Block with Picklist
description: Display code blocks grouped into heading tabs with a picker for choosing a panel.
---

# Code Block with Picklist

The heading tab selects a group of code panels, and the language picker selects which panel in that group is visible. Repeat a heading when its tab should offer multiple language or file choices.

## Syntax

````markdown
<CodeBlock slots="heading, code" repeat="4" languages="client.js, client.py, server.js, server.py" />

#### Client

```javascript
// client.js
```

#### Client

```python
# client.py
```

#### Server

```javascript
// server.js
```

#### Server

```python
# server.py
```
````

## Parameters

- **slots**: Defines each panel's content structure - `"heading, code"`
- **repeat**: Number of authored code panels; here it matches four heading/code pairs and four labels
- **languages**: Comma-separated display labels, with one entry per authored code panel in order. Each label (for example, a language name or filename) appears as a picker option for its group.

## Example

<CodeBlock slots="heading, code" repeat="4" languages="client.js, client.py, server.js, server.py" />

#### Client

```javascript
const response = await fetch('/api/items');
const items = await response.json();
console.log(items);
```

#### Client

```python
from urllib.request import urlopen
import json

with urlopen('/api/items') as response:
    items = json.load(response)
    print(items)
```

#### Server

```javascript
app.get('/api/items', async (request, response) => {
  const items = await getItems();
  response.json(items);
});
```

#### Server

```python
@app.get('/api/items')
def list_items():
    return jsonify(get_items())
```

The **Client** tab offers `client.js` and `client.py`; the **Server** tab offers `server.js` and `server.py`. The displayed tab controls the picker choices, and the selected file label controls which code panel is shown.
