# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Shops

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `meta` | [`Block`](./Shops.md#context-meta) | `{ ... }` |  |
| `breakdown` | [`Block`](./Shops.md#context-breakdown) | `{ ... }` |  |
| `item_groups` | [`Block`](./Shops.md#context-item_groups) | `{ ... }` |  |
| `item_rarity_costs` | [`Block`](./Shops.md#context-item_rarity_costs) | `{ ... }` |  |
| `stock_fill_order` | Block | `{ ... }` |  |
| `button_nav` | [`Block`](./Shops.md#context-button_nav) | `{ ... }` |  |
| `breakdown2` | [`Block`](./Shops.md#context-breakdown2) | `{ ... }` |  |
| `breakdown3` | [`Block`](./Shops.md#context-breakdown3) | `{ ... }` |  |
| `breakdown4` | [`Block`](./Shops.md#context-breakdown4) | `{ ... }` |  |

</details>

---

### Context: `Item`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`common_item`](./Shops.md#context-common_item), [`consumable`](./Shops.md#context-consumable), [`empty`](./Shops.md#context-empty), [`item`](./Shops.md#context-item), [`mandatory`](./Shops.md#context-mandatory), [`mostly_food`](./Shops.md#context-mostly_food), [`pool`](./Shops.md#context-pool), [`treasure`](./Shops.md#context-treasure)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `shop_common, treasure_easy, rare` |  |
| `cost` | Number | `10, 0, 15` |  |
| `mandatory` | Boolean | `true` |  |
| `weight` | Number | `1` |  |

</details>

---

### Context: `meta`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `movieclip` | [`Enum/String`](./Enums.md#enum-movieclip) | `Shop, JackOffice, TreasureRoom` |  |
| `treasure_room` | Boolean | `true` |  |
| `delay_enable_tooltips` | Boolean | `true` |  |
| `keeper` | Number | `0` |  |
| `npc_script` | [`Enum/String`](./Enums.md#enum-npc_script) | `tracy_adventure_shop_script.gon` |  |
| `shopkeeper_fights` | [`Array`](./Arrays.md#array-shopkeeper_fights) | `[ test.lvl ]` |  |
| `house_shop` | Boolean | `true` |  |
| `welcome_message` | [`Enum/String`](./Enums.md#enum-welcome_message) | `welcome_water_cheap, welcome_water` |  |
| `pick_n` | Number | `1` |  |

</details>

---

### Context: `item_rarity_costs`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `common` | Number | `7, 14, 5` |  |
| `consumable_common` | Number | `10, 5, 3` |  |
| `consumable_rare` | Number | `8, 10, 20` |  |
| `consumable_uncommon` | Number | `7, 14, 5` |  |
| `consumable_very_rare` | Number | `40, 12, 20` |  |
| `rare` | Number | `40, 10, 20` |  |
| `uncommon` | Number | `8, 10, 20` |  |
| `very_rare` | Number | `80, 40, 15` |  |

</details>

---

### Context: `item_groups`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `treasure` | [`Block`](./Shops.md#context-treasure) | `{ ... }` |  |
| `pool` | [`Block`](./Shops.md#context-pool) | `{ ... }` |  |
| `mandatory` | [`Block`](./Shops.md#context-mandatory) | `{ ... }` |  |
| `levelup` | [`Block`](./Shops.md#context-levelup) | `{ ... }` |  |
| `common_item` | [`Block`](./Shops.md#context-common_item) | `{ ... }` |  |
| `consumable` | [`Block`](./Shops.md#context-consumable) | `{ ... }` |  |
| `guaranteed_food` | [`Block`](./Shops.md#context-guaranteed_food) | `{ ... }` |  |
| `item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |
| `mostly_food` | [`Block`](./Shops.md#context-mostly_food) | `{ ... }` |  |
| `empty` | [`Block`](./Shops.md#context-empty) | `{ ... }` |  |

</details>

---

### Context: `breakdown`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `treasure` | Number | `1` |  |
| `pool` | Number | `2, 5, 3` |  |
| `levelup` | Number | `1` |  |
| `mandatory` | Number | `6, 1, 3` |  |
| `consumable` | Number | `2, 1` |  |
| `guaranteed_food` | Number | `1` |  |
| `mostly_food` | Number | `2, 1` |  |
| `empty` | Number | `1` |  |
| `item` | Number | `1` |  |

</details>

---

### Context: `Food`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`guaranteed_food`](./Shops.md#context-guaranteed_food), [`mostly_food`](./Shops.md#context-mostly_food)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allow_duplicates` | Boolean | `true` |  |
| `amount` | Number | `10` |  |
| `cost` | Number | `5` |  |
| `weight` | Number | `5` |  |

</details>

---

### Context: `treasure`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |

</details>

---

### Context: `pool`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |

</details>

---

### Context: `breakdown2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `common_item` | Number | `1` |  |
| `consumable` | Number | `1` |  |
| `guaranteed_food` | Number | `1` |  |
| `mostly_food` | Number | `1` |  |
| `item` | Number | `1` |  |

</details>

---

### Context: `breakdown4`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `common_item` | Number | `2` |  |
| `consumable` | Number | `1` |  |
| `guaranteed_food` | Number | `1` |  |
| `item` | Number | `2, 1` |  |

</details>

---

### Context: `breakdown3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `common_item` | Number | `2` |  |
| `consumable` | Number | `1` |  |
| `guaranteed_food` | Number | `1` |  |
| `item` | Number | `1` |  |

</details>

---

### Context: `button_nav`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `default` | Block | `{ ... }` |  |

</details>

---

### Context: `mandatory`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |
| `Furniture` | Block | `{ ... }` |  |

</details>

---

### Context: `mostly_food`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Food` | [`Block`](./Shops.md#context-food) | `{ ... }` |  |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |

</details>

---

### Context: `LevelUp`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`levelup`](./Shops.md#context-levelup)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cost` | Number | `10` |  |

</details>

---

### Context: `levelup`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LevelUp` | [`Block`](./Shops.md#context-levelup) | `{ ... }` |  |

</details>

---

### Context: `common_item`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |

</details>

---

### Context: `consumable`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |

</details>

---

### Context: `guaranteed_food`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Food` | [`Block`](./Shops.md#context-food) | `{ ... }` |  |

</details>

---

### Context: `item`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |

</details>

---

### Context: `empty`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |

</details>

---

