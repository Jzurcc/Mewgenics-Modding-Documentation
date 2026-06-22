# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Spawns & Enemy Pools

> **Associated Files:** `data/spawns.gon`


### Context: `ROOT` (550 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`editor`](./Spawns_and_Enemy_Pools.md#context-editor) | Block |  | 550 |
| [`object`](./Enums.md#enum-object) | Enum |  | 543 |
| `value` | Number |  | 377 |
| `early_spawn` | Boolean |  | 10 |
| [`orientation`](./Enums.md#enum-orientation) | Enum |  | 6 |
| [`tag_location`](./Enums.md#enum-tag_location) | Enum |  | 5 |
| `forced_placement` | Boolean |  | 3 |
| [`trap`](./Enums.md#enum-trap) | Enum |  | 2 |
| [`image`](./Strings.md#string-image) | String |  | 1 |
| [`name`](./Strings.md#string-name) | String |  | 1 |
| [`reserved`](./Enums.md#enum-reserved) | Enum |  | 1 |
| [`utility`](./Enums.md#enum-utility) | Enum |  | 1 |
| [`weather_element_alt`](./Spawns_and_Enemy_Pools.md#context-weather_element_alt) | Block |  | 1 |

</details>

---

### Context: `editor` (550 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Spawns_and_Enemy_Pools.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `category` | Number |  | 551 |
| [`image`](./Arrays.md#array-image) | Array |  | 550 |
| [`name`](./Strings.md#string-name) | String |  | 550 |
| `paint` | Boolean |  | 550 |
| [`image_tint`](./Arrays.md#array-image_tint) | Array |  | 196 |
| `subcategory` | Number |  | 9 |
| `layer` | Number |  | 3 |

</details>

---

### Context: `weather_element_alt` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Spawns_and_Enemy_Pools.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

