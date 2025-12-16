---
name: 🧩 Composition Action Request
about: Request a new action that chains together existing Starthub actions (a 'Composition').
title: 'COMPOSITION: [Concise name, e.g., get-weather-by-location-name]'
labels: ['action-request', 'composition', 'triage']
assignees: ''
---

## 🎯 Action Goal and Description

**What is the name of the Action?**
(Corresponds to the `"name"` and `"description"` fields in the manifest)

**Briefly describe the final goal and value proposition of this Composition:**
(e.g., Combines Geo-location and Weather API calls to simplify data retrieval.)

---

## 💻 Input Schema (`"inputs"` and `"types"`)

**What information must the user provide to run this action?**
(List all required input fields and their expected type, similar to the `WeatherConfig` in your example)

| Input Name | Type | Description / Example |
| :--- | :--- | :--- |
| `[e.g., location_name]` | `[e.g., string]` | `[e.g., The name of the city to get weather for]` |
| `[e.g., api_key]` | `[e.g., string]` | `[e.g., The API key for the service]` |
| | | |

---

## ⛓️ Action Steps (`"steps"`)

**What are the individual steps (sub-actions) that must be chained together?**
(This is the core of the Composition. You need to identify the existing Starthub actions to use.) 

### Step 1: Sub-Action Name

* **Sub-Action Used (`"uses"`):** `[e.g., tgirotto/openweather-coordinates-by-location-name:0.0.1]`
* **Purpose:** `[e.g., To convert the user's location name into latitude and longitude.]`
* **How does it get its input?** `[e.g., From the top-level inputs (e.g., {{inputs[0].location_name}})]`

### Step 2: Sub-Action Name

* **Sub-Action Used (`"uses"`):** `[e.g., tgirotto/openweather-current-weather:0.0.1]`
* **Purpose:** `[e.g., To fetch the current weather data.]`
* **How does it get its input?** `[e.g., From the output of Step 1 (e.g., {{steps.get_coordinates.outputs[0].lat}})]`

*(Add more steps as necessary)*

---

## 📤 Output Schema (`"outputs"`)

**What is the simplified, final output that the user should receive?**
(Define the output structure and how its values are derived from the step outputs.)

| Output Name | Type | Description | Value Derived From |
| :--- | :--- | :--- | :--- |
| `[e.g., response]` | `[e.g., CustomWeatherResponse]` | `[e.g., Simplified weather info]` | `[e.g., {{steps.get_weather.outputs[0].weather[0].description}}]` |
| | | | |

---

## ⬆️ Priority and Value

**How important is this action to your current project?**
(Rate 1-5, where 5 is critical.)

* 1 - Nice-to-have / Exploration
* 2 - Low
* 3 - Moderate
* 4 - High
* 5 - Critical / Project Blocker