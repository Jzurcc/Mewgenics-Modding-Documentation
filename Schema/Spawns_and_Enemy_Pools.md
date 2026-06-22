# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Spawns & Enemy Pools

> **Associated Files:** `data/spawns.gon`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 550

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`editor`](#context-editor) | Block |  | 550 |
| [`object`](./Enums.md#enum-object) | Enum |  | 543 |
| `value` | Float |  | 377 |
| `early_spawn` | Boolean |  | 10 |
| [`orientation`](./Enums.md#enum-orientation) | Enum |  | 6 |
| [`tag_location`](./Enums.md#enum-tag_location) | Enum |  | 5 |
| `forced_placement` | Boolean |  | 3 |
| [`trap`](./Enums.md#enum-trap) | Enum |  | 2 |
| [`image`](./Strings.md#string-image) | String |  | 1 |
| [`name`](./Strings.md#string-name) | String |  | 1 |
| [`reserved`](./Enums.md#enum-reserved) | Enum |  | 1 |
| [`utility`](./Enums.md#enum-utility) | Enum |  | 1 |
| [`weather_element_alt`](#context-weather_element_alt) | Block |  | 1 |

</details>

---

### Context: `editor`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 550

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `category` | Integer |  | 551 |
| [`image`](./Arrays.md#array-image) | Array |  | 550 |
| [`name`](./Strings.md#string-name) | String |  | 550 |
| `paint` | Boolean |  | 550 |
| [`image_tint`](./Arrays.md#array-image_tint) | Array |  | 196 |
| `subcategory` | Integer |  | 9 |
| `layer` | Integer |  | 3 |

</details>

---

### Context: `weather_element_alt`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

