# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Shops

> **Associated Files:** `data/shops/`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 25

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`meta`](#context-meta) | Block |  | 25 |
| [`breakdown`](#context-breakdown) | Block |  | 24 |
| [`item_groups`](#context-item_groups) | Block |  | 24 |
| [`item_rarity_costs`](#context-item_rarity_costs) | Block |  | 9 |
| `stock_fill_order` | Block |  | 9 |
| [`button_nav`](#context-button_nav) | Block |  | 7 |
| [`breakdown2`](#context-breakdown2) | Block |  | 2 |
| [`breakdown3`](#context-breakdown3) | Block |  | 2 |
| [`breakdown4`](#context-breakdown4) | Block |  | 2 |

</details>

---

### Context: `Item`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 37

> **Referenced by:** [`common_item`](#context-common_item), [`consumable`](#context-consumable), [`empty`](#context-empty), [`item`](#context-item), [`mandatory`](#context-mandatory), [`mostly_food`](#context-mostly_food), [`pool`](#context-pool), [`treasure`](#context-treasure)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 37 |
| `cost` | Integer |  | 21 |
| `mandatory` | Boolean |  | 14 |
| `weight` | Float |  | 2 |

</details>

---

### Context: `meta`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 25

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  | 25 |
| `treasure_room` | Boolean |  | 14 |
| `delay_enable_tooltips` | Boolean |  | 7 |
| `keeper` | Integer |  | 7 |
| [`npc_script`](./Enums.md#enum-npc_script) | Enum |  | 7 |
| [`shopkeeper_fights`](./Arrays.md#array-shopkeeper_fights) | Array |  | 7 |
| `house_shop` | Boolean |  | 4 |
| [`welcome_message`](./Enums.md#enum-welcome_message) | Enum |  | 2 |
| `pick_n` | Integer |  | 1 |

</details>

---

### Context: `breakdown`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 24

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `treasure` | Integer |  | 14 |
| `pool` | Integer |  | 6 |
| `levelup` | Integer |  | 3 |
| `mandatory` | Integer |  | 3 |
| `consumable` | Integer |  | 2 |
| `guaranteed_food` | Integer |  | 2 |
| `mostly_food` | Integer |  | 2 |
| `empty` | Integer |  | 1 |
| `item` | Integer |  | 1 |

</details>

---

### Context: `item_groups`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 24

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`treasure`](#context-treasure) | Block |  | 14 |
| [`pool`](#context-pool) | Block |  | 6 |
| [`mandatory`](#context-mandatory) | Block |  | 5 |
| [`levelup`](#context-levelup) | Block |  | 3 |
| [`common_item`](#context-common_item) | Block |  | 2 |
| [`consumable`](#context-consumable) | Block |  | 2 |
| [`guaranteed_food`](#context-guaranteed_food) | Block |  | 2 |
| [`item`](#context-item) | Block |  | 2 |
| [`mostly_food`](#context-mostly_food) | Block |  | 2 |
| [`empty`](#context-empty) | Block |  | 1 |

</details>

---

### Context: `treasure`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 14

> **Referenced by:** [`item_groups`](#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](#context-item) | Block |  | 14 |

</details>

---

### Context: `item_rarity_costs`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `common` | Integer |  | 9 |
| `consumable_common` | Integer |  | 9 |
| `consumable_rare` | Integer |  | 9 |
| `consumable_uncommon` | Integer |  | 9 |
| `consumable_very_rare` | Integer |  | 9 |
| `rare` | Integer |  | 9 |
| `uncommon` | Integer |  | 9 |
| `very_rare` | Float |  | 9 |

</details>

---

### Context: `button_nav`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`default`](./Characters_and_Bosses.md#context-default) | Block |  | 7 |

</details>

---

### Context: `pool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`item_groups`](#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](#context-item) | Block |  | 10 |

</details>

---

### Context: `mandatory`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`item_groups`](#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](#context-item) | Block |  | 4 |
| `Furniture` | Block |  | 1 |

</details>

---

### Context: `Food`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`guaranteed_food`](#context-guaranteed_food), [`mostly_food`](#context-mostly_food)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allow_duplicates` | Boolean |  | 4 |
| `amount` | Float |  | 4 |
| `cost` | Integer |  | 4 |
| `weight` | Float |  | 2 |

</details>

---

### Context: `LevelUp`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`levelup`](#context-levelup)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cost` | Integer |  | 3 |

</details>

---

### Context: `levelup`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`item_groups`](#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`LevelUp`](#context-levelup) | Block |  | 3 |

</details>

---

### Context: `breakdown2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `common_item` | Integer |  | 2 |
| `consumable` | Integer |  | 2 |
| `guaranteed_food` | Integer |  | 2 |
| `mostly_food` | Integer |  | 2 |
| `item` | Integer |  | 1 |

</details>

---

### Context: `breakdown3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `common_item` | Integer |  | 2 |
| `consumable` | Integer |  | 2 |
| `guaranteed_food` | Integer |  | 2 |
| `item` | Integer |  | 1 |

</details>

---

### Context: `breakdown4`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `common_item` | Integer |  | 2 |
| `consumable` | Integer |  | 2 |
| `guaranteed_food` | Integer |  | 2 |
| `item` | Integer |  | 2 |

</details>

---

### Context: `common_item`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`item_groups`](#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](#context-item) | Block |  | 2 |

</details>

---

### Context: `consumable`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`item_groups`](#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](#context-item) | Block |  | 2 |

</details>

---

### Context: `guaranteed_food`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`item_groups`](#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Food`](#context-food) | Block |  | 2 |

</details>

---

### Context: `item`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`item_groups`](#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](#context-item) | Block |  | 2 |

</details>

---

### Context: `mostly_food`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`item_groups`](#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Food`](#context-food) | Block |  | 2 |
| [`Item`](#context-item) | Block |  | 2 |

</details>

---

### Context: `empty`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`item_groups`](#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](#context-item) | Block |  | 1 |

</details>

---

