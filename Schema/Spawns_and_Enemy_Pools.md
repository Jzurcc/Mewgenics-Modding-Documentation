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
| [`editor`](#context-editor) | Block |  | 550 |
| [`object`](./Enums.md#enum-object) | Enum |  | 543 |
| `value` | Float |  | 377 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 206 |
| `early_spawn` | Boolean |  | 10 |
| [`orientation`](./Enums.md#enum-orientation) | Enum |  | 6 |
| [`tag_location`](./Enums.md#enum-tag_location) | Enum |  | 5 |
| `forced_placement` | Boolean |  | 3 |
| [`trap`](./Enums.md#enum-trap) | Enum |  | 2 |
| [`image`](./Strings.md#string-image) | String |  | 1 |
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
| `paint` | Boolean |  | 550 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 538 |
| [`image_tint`](./Arrays.md#array-image_tint) | Array |  | 196 |
| `subcategory` | Integer |  | 9 |

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

