# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Shops

> **Associated Files:** `data/shops/`


### Context: `ROOT` (25 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`meta`](./Shops.md#context-meta) | Block |  | 25 |
| [`breakdown`](./Shops.md#context-breakdown) | Block |  | 24 |
| [`item_groups`](./Shops.md#context-item_groups) | Block |  | 24 |
| [`item_rarity_costs`](./Shops.md#context-item_rarity_costs) | Block |  | 9 |
| `stock_fill_order` | Block |  | 9 |
| [`button_nav`](./Shops.md#context-button_nav) | Block |  | 7 |
| [`breakdown2`](./Shops.md#context-breakdown2) | Block |  | 2 |
| [`breakdown3`](./Shops.md#context-breakdown3) | Block |  | 2 |
| [`breakdown4`](./Shops.md#context-breakdown4) | Block |  | 2 |

</details>

---

### Context: `Item` (37 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common_item`](./Shops.md#context-common_item), [`consumable`](./Shops.md#context-consumable), [`empty`](./Shops.md#context-empty), [`item`](./Shops.md#context-item), [`mandatory`](./Shops.md#context-mandatory), [`mostly_food`](./Shops.md#context-mostly_food), [`pool`](./Shops.md#context-pool), [`treasure`](./Shops.md#context-treasure)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 37 |
| `cost` | Number |  | 21 |
| `mandatory` | Boolean |  | 14 |
| `weight` | Number |  | 2 |

</details>

---

### Context: `meta` (25 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  | 25 |
| `treasure_room` | Boolean |  | 14 |
| `delay_enable_tooltips` | Boolean |  | 7 |
| `keeper` | Number |  | 7 |
| [`npc_script`](./Enums.md#enum-npc_script) | Enum |  | 7 |
| [`shopkeeper_fights`](./Arrays.md#array-shopkeeper_fights) | Array |  | 7 |
| `house_shop` | Boolean |  | 4 |
| [`welcome_message`](./Enums.md#enum-welcome_message) | Enum |  | 2 |
| `pick_n` | Number |  | 1 |

</details>

---

### Context: `breakdown` (24 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `treasure` | Number |  | 14 |
| `pool` | Number |  | 6 |
| `levelup` | Number |  | 3 |
| `mandatory` | Number |  | 3 |
| `consumable` | Number |  | 2 |
| `guaranteed_food` | Number |  | 2 |
| `mostly_food` | Number |  | 2 |
| `empty` | Number |  | 1 |
| `item` | Number |  | 1 |

</details>

---

### Context: `item_groups` (24 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`treasure`](./Shops.md#context-treasure) | Block |  | 14 |
| [`pool`](./Shops.md#context-pool) | Block |  | 6 |
| [`mandatory`](./Shops.md#context-mandatory) | Block |  | 5 |
| [`levelup`](./Shops.md#context-levelup) | Block |  | 3 |
| [`common_item`](./Shops.md#context-common_item) | Block |  | 2 |
| [`consumable`](./Shops.md#context-consumable) | Block |  | 2 |
| [`guaranteed_food`](./Shops.md#context-guaranteed_food) | Block |  | 2 |
| [`item`](./Shops.md#context-item) | Block |  | 2 |
| [`mostly_food`](./Shops.md#context-mostly_food) | Block |  | 2 |
| [`empty`](./Shops.md#context-empty) | Block |  | 1 |

</details>

---

### Context: `treasure` (14 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block |  | 14 |

</details>

---

### Context: `item_rarity_costs` (9 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `common` | Number |  | 9 |
| `consumable_common` | Number |  | 9 |
| `consumable_rare` | Number |  | 9 |
| `consumable_uncommon` | Number |  | 9 |
| `consumable_very_rare` | Number |  | 9 |
| `rare` | Number |  | 9 |
| `uncommon` | Number |  | 9 |
| `very_rare` | Number |  | 9 |

</details>

---

### Context: `button_nav` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`default`](./Characters_and_Bosses.md#context-default) | Block |  | 7 |

</details>

---

### Context: `pool` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block |  | 10 |

</details>

---

### Context: `mandatory` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block |  | 4 |
| `Furniture` | Block |  | 1 |

</details>

---

### Context: `Food` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`guaranteed_food`](./Shops.md#context-guaranteed_food), [`mostly_food`](./Shops.md#context-mostly_food)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allow_duplicates` | Boolean |  | 4 |
| `amount` | Number |  | 4 |
| `cost` | Number |  | 4 |
| `weight` | Number |  | 2 |

</details>

---

### Context: `LevelUp` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`levelup`](./Shops.md#context-levelup)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cost` | Number |  | 3 |

</details>

---

### Context: `levelup` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`LevelUp`](./Shops.md#context-levelup) | Block |  | 3 |

</details>

---

### Context: `breakdown2` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `common_item` | Number |  | 2 |
| `consumable` | Number |  | 2 |
| `guaranteed_food` | Number |  | 2 |
| `mostly_food` | Number |  | 2 |
| `item` | Number |  | 1 |

</details>

---

### Context: `breakdown3` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `common_item` | Number |  | 2 |
| `consumable` | Number |  | 2 |
| `guaranteed_food` | Number |  | 2 |
| `item` | Number |  | 1 |

</details>

---

### Context: `breakdown4` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `common_item` | Number |  | 2 |
| `consumable` | Number |  | 2 |
| `guaranteed_food` | Number |  | 2 |
| `item` | Number |  | 2 |

</details>

---

### Context: `common_item` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block |  | 2 |

</details>

---

### Context: `consumable` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block |  | 2 |

</details>

---

### Context: `guaranteed_food` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Food`](./Shops.md#context-food) | Block |  | 2 |

</details>

---

### Context: `item` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block |  | 2 |

</details>

---

### Context: `mostly_food` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Food`](./Shops.md#context-food) | Block |  | 2 |
| [`Item`](./Shops.md#context-item) | Block |  | 2 |

</details>

---

### Context: `empty` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block |  | 1 |

</details>

---

