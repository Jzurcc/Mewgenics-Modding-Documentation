# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Spawns & Enemy Pools

> **Associated Files:** `data/spawns.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 550

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`editor`](#object-editor) | Object |  | 550 |
| [`object`](./Enums.md#enum-object) | Enum |  | 543 |
| `value` | Float |  | 377 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 206 |
| `early_spawn` | Boolean |  | 10 |
| [`orientation`](./Enums.md#enum-orientation) | Enum |  | 6 |
| [`tag_location`](./Enums.md#enum-tag_location) | Enum |  | 5 |
| `forced_placement` | Boolean |  | 3 |
| [`trap`](./Enums.md#enum-trap) | Enum |  | 2 |
| [`image`](./Strings.md#string-image) | String |  | 1 |
| [`reserved`](./Enums.md#enum-reserved) | Enum |  | 1 |
| [`utility`](./Enums.md#enum-utility) | Enum |  | 1 |
| [`weather_element_alt`](#object-weather_element_alt) | Object |  | 1 |
| [`element`](./Engine_LogicKeys.md#valid-property-keys) | Enum/String | Specific element type required or applied. | 0 |

</details>

---

### Object: `editor`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 578

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `category` | Integer |  | 551 |
| [`image`](./Arrays.md#array-image) | Array |  | 550 |
| `paint` | Boolean |  | 550 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 538 |
| [`image_tint`](./Arrays.md#array-image_tint) | Array |  | 196 |
| `subcategory` | Integer |  | 9 |
| `layer` | `Number` |  | 0 |

</details>

---

### Object: `weather_element_alt`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

