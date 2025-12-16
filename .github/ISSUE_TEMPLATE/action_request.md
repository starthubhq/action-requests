---
name: 🧩 Composition Action Request
about: Request a new action that chains together existing Starthub actions (a 'Composition').
title: 'COMPOSITION: [Concise name, e.g., get-weather-by-location-name]'
labels: ['action-request', 'composition', 'triage']
assignees: ''
---

```
{
  "name": "<name>",
  "description": "<description>",
  "version": "0.0.1",
  "kind": "composition",
  "manifest_version": 1,
  "repository": "<repository>",
  "license": "<license>",
  "inputs": [
    {
      "name": "<name>",
      "description": <description>
      "type": "<type>",
    }
  ],
  "steps": {
    <TODO>
  },
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