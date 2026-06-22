# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Shops

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/25) |
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

### Context: `Item`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common_item`](./Shops.md#context-common_item), [`consumable`](./Shops.md#context-consumable), [`empty`](./Shops.md#context-empty), [`item`](./Shops.md#context-item), [`mandatory`](./Shops.md#context-mandatory), [`mostly_food`](./Shops.md#context-mostly_food), [`pool`](./Shops.md#context-pool), [`treasure`](./Shops.md#context-treasure)

| Property Key | Type | Definition | Count (X/37) |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum/String |  | 37 |
| `cost` | Number |  | 21 |
| `mandatory` | Boolean |  | 14 |
| `weight` | Number |  | 2 |

</details>

---

### Context: `meta`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count (X/25) |
| :--- | :--- | :--- | :--- |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum/String |  | 25 |
| `treasure_room` | Boolean |  | 14 |
| `delay_enable_tooltips` | Boolean |  | 7 |
| `keeper` | Number |  | 7 |
| [`npc_script`](./Enums.md#enum-npc_script) | Enum/String |  | 7 |
| [`shopkeeper_fights`](./Arrays.md#array-shopkeeper_fights) | Array |  | 7 |
| `house_shop` | Boolean |  | 4 |
| [`welcome_message`](./Enums.md#enum-welcome_message) | Enum/String |  | 2 |
| `pick_n` | Number |  | 1 |

</details>

---

### Context: `breakdown`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count (X/14) |
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

### Context: `item_groups`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count (X/14) |
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

### Context: `treasure`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count (X/14) |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block |  | 14 |

</details>

---

### Context: `pool`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count (X/10) |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block |  | 10 |

</details>

---

### Context: `item_rarity_costs`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count (X/9) |
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

### Context: `button_nav`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| [`default`](./Characters_and_Bosses.md#context-default) | Block |  | 7 |

</details>

---

### Context: `Food`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`guaranteed_food`](./Shops.md#context-guaranteed_food), [`mostly_food`](./Shops.md#context-mostly_food)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `allow_duplicates` | Boolean |  | 4 |
| `amount` | Number |  | 4 |
| `cost` | Number |  | 4 |
| `weight` | Number |  | 2 |

</details>

---

### Context: `mandatory`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block |  | 4 |
| `Furniture` | Block |  | 1 |

</details>

---

### Context: `LevelUp`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`levelup`](./Shops.md#context-levelup)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `cost` | Number |  | 3 |

</details>

---

### Context: `levelup`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`LevelUp`](./Shops.md#context-levelup) | Block |  | 3 |

</details>

---

### Context: `breakdown2`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `common_item` | Number |  | 2 |
| `consumable` | Number |  | 2 |
| `guaranteed_food` | Number |  | 2 |
| `mostly_food` | Number |  | 2 |
| `item` | Number |  | 1 |

</details>

---

### Context: `breakdown3`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `common_item` | Number |  | 2 |
| `consumable` | Number |  | 2 |
| `guaranteed_food` | Number |  | 2 |
| `item` | Number |  | 1 |

</details>

---

### Context: `breakdown4`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `common_item` | Number |  | 2 |
| `consumable` | Number |  | 2 |
| `guaranteed_food` | Number |  | 2 |
| `item` | Number |  | 2 |

</details>

---

### Context: `common_item`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block |  | 2 |

</details>

---

### Context: `consumable`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block |  | 2 |

</details>

---

### Context: `guaranteed_food`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Food`](./Shops.md#context-food) | Block |  | 2 |

</details>

---

### Context: `item`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block |  | 2 |

</details>

---

### Context: `mostly_food`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Food`](./Shops.md#context-food) | Block |  | 2 |
| [`Item`](./Shops.md#context-item) | Block |  | 2 |

</details>

---

### Context: `empty`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block |  | 1 |

</details>

---

