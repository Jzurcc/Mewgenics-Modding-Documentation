# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Spawns & Enemy Pools

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/550) |
| :--- | :--- | :--- | :--- |
| [`editor`](./Spawns_and_Enemy_Pools.md#context-editor) | Block |  | 550 |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 543 |
| [`value`](./Enums.md#enum-value) | Enum/String |  | 377 |
| `early_spawn` | Boolean |  | 10 |
| [`orientation`](./Enums.md#enum-orientation) | Enum/String |  | 6 |
| [`tag_location`](./Enums.md#enum-tag_location) | Enum/String |  | 5 |
| `forced_placement` | Boolean |  | 3 |
| [`trap`](./Enums.md#enum-trap) | Enum/String |  | 2 |
| `image` | String |  | 1 |
| `name` | String |  | 1 |
| [`reserved`](./Enums.md#enum-reserved) | Enum/String |  | 1 |
| [`utility`](./Enums.md#enum-utility) | Enum/String |  | 1 |
| [`weather_element_alt`](./Spawns_and_Enemy_Pools.md#context-weather_element_alt) | Block |  | 1 |

</details>

---

### Context: `editor`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Spawns_and_Enemy_Pools.md#context-root)

| Property Key | Type | Definition | Count (X/551) |
| :--- | :--- | :--- | :--- |
| `category` | Number |  | 551 |
| [`image`](./Arrays.md#array-image) | Array |  | 550 |
| `name` | String |  | 550 |
| `paint` | Boolean |  | 550 |
| [`image_tint`](./Arrays.md#array-image_tint) | Array |  | 196 |
| `subcategory` | Number |  | 9 |
| `layer` | Number |  | 3 |

</details>

---

### Context: `weather_element_alt`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Spawns_and_Enemy_Pools.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | Specific element type required or applied. | 1 |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 1 |

</details>

---

