---
name: 🧩 Composition Action Request
about: Request a new action that chains together existing Starthub actions (a 'Composition').
title: '[Concise name, e.g., get-weather-by-location-name]'
labels: ['action-request', 'composition', 'triage']
assignees: ''
---

The action should...


and the manifest should look like...

```
{
  "name": "<name>",
  "description": "<description>",
  "kind": "composition",
  "inputs": [
    {
      "name": "<name>",
      "description": <description>
      "type": "<type>",
    }
  ],
  "outputs": [
    {
      "name": "<name>",
      "description": "<description>",
      "type": "<type>"
    }
  ],
  "types": <types>
}
```