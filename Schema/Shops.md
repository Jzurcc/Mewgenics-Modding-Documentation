# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Shops

> **Associated Files:** `data/shops/`


### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 25

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`meta`](./Shops.md#context-meta) | Block | Examples: `{ ... }` | 25 |
| [`breakdown`](./Shops.md#context-breakdown) | Block | Examples: `{ ... }` | 24 |
| [`item_groups`](./Shops.md#context-item_groups) | Block | Examples: `{ ... }` | 24 |
| [`item_rarity_costs`](./Shops.md#context-item_rarity_costs) | Block | Examples: `{ ... }` | 9 |
| `stock_fill_order` | Block | Examples: `{ ... }` | 9 |
| [`button_nav`](./Shops.md#context-button_nav) | Block | Examples: `{ ... }` | 7 |
| [`breakdown2`](./Shops.md#context-breakdown2) | Block | Examples: `{ ... }` | 2 |
| [`breakdown3`](./Shops.md#context-breakdown3) | Block | Examples: `{ ... }` | 2 |
| [`breakdown4`](./Shops.md#context-breakdown4) | Block | Examples: `{ ... }` | 2 |

</details>

---

### Context: `Item`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 37

> **Referenced by:** [`common_item`](./Shops.md#context-common_item), [`consumable`](./Shops.md#context-consumable), [`empty`](./Shops.md#context-empty), [`item`](./Shops.md#context-item), [`mandatory`](./Shops.md#context-mandatory), [`mostly_food`](./Shops.md#context-mostly_food), [`pool`](./Shops.md#context-pool), [`treasure`](./Shops.md#context-treasure)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum | Examples: `rare, shop_common, treasure_easy` | 37 |
| `cost` | Number | Examples: `0, 15, 10` | 21 |
| `mandatory` | Boolean | Examples: `true` | 14 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `meta`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 25

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2339 |
| `treasure_room` | Boolean | Examples: `true` | 14 |
| `delay_enable_tooltips` | Boolean | Examples: `true` | 7 |
| `keeper` | Number | Examples: `0` | 7 |
| [`npc_script`](./Enums.md#enum-npc_script) | Enum | Examples: `tracy_adventure_shop_script.gon` | 7 |
| [`shopkeeper_fights`](./Arrays.md#array-shopkeeper_fights) | Array | Examples: `[ test.lvl ]` | 7 |
| `house_shop` | Boolean | Examples: `true` | 4 |
| [`welcome_message`](./Enums.md#enum-welcome_message) | Enum | Examples: `welcome_water, welcome_water_cheap` | 2 |
| `pick_n` | Number | Examples: `1` | 1 |

</details>

---

### Context: `breakdown`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `treasure` | Number | Examples: `1` | 14 |
| `pool` | Number | Examples: `3, 2, 5` | 6 |
| `levelup` | Number | Examples: `1` | 3 |
| `mandatory` | Number | Examples: `3, 6, 1` | 3 |
| `consumable` | Number | Examples: `2, 1` | 2 |
| `guaranteed_food` | Number | Examples: `1` | 2 |
| `mostly_food` | Number | Examples: `2, 1` | 2 |
| `empty` | Number | Examples: `1` | 1 |
| `item` | Number | Examples: `1` | 1 |

</details>

---

### Context: `item_groups`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`treasure`](./Shops.md#context-treasure) | Block | Examples: `{ ... }` | 14 |
| [`pool`](./Shops.md#context-pool) | Block | Examples: `{ ... }` | 6 |
| [`mandatory`](./Shops.md#context-mandatory) | Block | Examples: `{ ... }` | 5 |
| [`levelup`](./Shops.md#context-levelup) | Block | Examples: `{ ... }` | 3 |
| [`common_item`](./Shops.md#context-common_item) | Block | Examples: `{ ... }` | 2 |
| [`consumable`](./Shops.md#context-consumable) | Block | Examples: `{ ... }` | 2 |
| [`guaranteed_food`](./Shops.md#context-guaranteed_food) | Block | Examples: `{ ... }` | 2 |
| [`item`](./Shops.md#context-item) | Block | Examples: `{ ... }` | 2 |
| [`mostly_food`](./Shops.md#context-mostly_food) | Block | Examples: `{ ... }` | 2 |
| [`empty`](./Shops.md#context-empty) | Block | Examples: `{ ... }` | 1 |

</details>

---

### Context: `treasure`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block | Examples: `{ ... }` | 14 |

</details>

---

### Context: `item_rarity_costs`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 9 |
| `consumable_common` | Number | Examples: `3, 5, 10` | 9 |
| `consumable_rare` | Number | Examples: `20, 8, 10` | 9 |
| `consumable_uncommon` | Number | Examples: `14, 5, 7` | 9 |
| `consumable_very_rare` | Number | Examples: `12, 40, 20` | 9 |
| `uncommon` | Number | Examples: `20, 8, 10` | 9 |
| `very_rare` | Number | Examples: `80, 40, 15` | 9 |

</details>

---

### Context: `button_nav`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`default`](./Miscellaneous.md#context-default) | Block | Examples: `{ ... }` | 7 |

</details>

---

### Context: `pool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block | Examples: `{ ... }` | 10 |

</details>

---

### Context: `mandatory`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block | Examples: `{ ... }` | 4 |
| `Furniture` | Block | Examples: `{ ... }` | 1 |

</details>

---

### Context: `Food`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`guaranteed_food`](./Shops.md#context-guaranteed_food), [`mostly_food`](./Shops.md#context-mostly_food)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allow_duplicates` | Boolean | Examples: `true` | 4 |
| `amount` | Number | Examples: `10` | 4 |
| `cost` | Number | Examples: `5` | 4 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `LevelUp`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`levelup`](./Shops.md#context-levelup)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cost` | Number | Examples: `10` | 3 |

</details>

---

### Context: `levelup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`LevelUp`](./Shops.md#context-levelup) | Block | Examples: `{ ... }` | 3 |

</details>

---

### Context: `breakdown2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `common_item` | Number | Examples: `1` | 2 |
| `consumable` | Number | Examples: `1` | 2 |
| `guaranteed_food` | Number | Examples: `1` | 2 |
| `mostly_food` | Number | Examples: `1` | 2 |
| `item` | Number | Examples: `1` | 1 |

</details>

---

### Context: `breakdown3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `common_item` | Number | Examples: `2` | 2 |
| `consumable` | Number | Examples: `1` | 2 |
| `guaranteed_food` | Number | Examples: `1` | 2 |
| `item` | Number | Examples: `1` | 1 |

</details>

---

### Context: `breakdown4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `common_item` | Number | Examples: `2` | 2 |
| `consumable` | Number | Examples: `1` | 2 |
| `guaranteed_food` | Number | Examples: `1` | 2 |
| `item` | Number | Examples: `2, 1` | 2 |

</details>

---

### Context: `common_item`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block | Examples: `{ ... }` | 2 |

</details>

---

### Context: `consumable`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block | Examples: `{ ... }` | 2 |

</details>

---

### Context: `guaranteed_food`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Food`](./Shops.md#context-food) | Block | Examples: `{ ... }` | 2 |

</details>

---

### Context: `item`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block | Examples: `{ ... }` | 2 |

</details>

---

### Context: `mostly_food`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Food`](./Shops.md#context-food) | Block | Examples: `{ ... }` | 2 |
| [`Item`](./Shops.md#context-item) | Block | Examples: `{ ... }` | 2 |

</details>

---

### Context: `empty`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Block | Examples: `{ ... }` | 1 |

</details>

---
