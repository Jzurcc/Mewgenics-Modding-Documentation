# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Shops

> **Associated Files:** `data/shops/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 25

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`meta`](./Shops.md#context-meta) | Object | Examples: `{ ... }` | 4719 |
| [`breakdown`](./Shops.md#context-breakdown) | Object | Examples: `{ ... }` | 24 |
| [`item_groups`](./Shops.md#context-item_groups) | Object | Examples: `{ ... }` | 24 |
| [`item_rarity_costs`](./Shops.md#context-item_rarity_costs) | Object | Examples: `{ ... }` | 9 |
| `stock_fill_order` | Object | Examples: `{ ... }` | 9 |
| [`button_nav`](./Shops.md#context-button_nav) | Object | Examples: `{ ... }` | 7 |
| [`breakdown2`](./Shops.md#context-breakdown2) | Object | Examples: `{ ... }` | 2 |
| [`breakdown3`](./Shops.md#context-breakdown3) | Object | Examples: `{ ... }` | 2 |
| [`breakdown4`](./Shops.md#context-breakdown4) | Object | Examples: `{ ... }` | 2 |

</details>

---

### Object: `Item`


**Definition:** No definition provided.  
**Total Count:** 37


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common_item`](./Shops.md#context-common_item), [`consumable`](./Shops.md#context-consumable), [`empty`](./Shops.md#context-empty), [`item`](./Shops.md#context-item), [`mandatory`](./Shops.md#context-mandatory), [`mostly_food`](./Shops.md#context-mostly_food), [`pool`](./Shops.md#context-pool), [`treasure`](./Shops.md#context-treasure)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cost` | Number | Examples: `0, 15, 10` | 21 |
| [`pool`](./Enums.md#enum-pool) | Enum | Examples: `rare, shop_common, treasure_easy` | 18 |
| `mandatory` | Boolean | Examples: `true` | 14 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 2 |

</details>

---

### Object: `meta`


**Definition:** Object defining UI display data (Name, Description, Icon).  
**Total Count:** 25


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum | Examples: `Shop, JackOffice, TreasureRoom` | 25 |
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

### Object: `breakdown`


**Definition:** No definition provided.  
**Total Count:** 24


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count |
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

### Object: `item_groups`


**Definition:** No definition provided.  
**Total Count:** 24


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`treasure`](./Shops.md#context-treasure) | Object | Examples: `{ ... }` | 14 |
| [`pool`](./Shops.md#context-pool) | Object | Examples: `{ ... }` | 6 |
| [`mandatory`](./Shops.md#context-mandatory) | Object | Examples: `{ ... }` | 5 |
| [`levelup`](./Shops.md#context-levelup) | Object | Examples: `{ ... }` | 3 |
| [`common_item`](./Shops.md#context-common_item) | Object | Examples: `{ ... }` | 2 |
| [`consumable`](./Shops.md#context-consumable) | Object | Examples: `{ ... }` | 2 |
| [`guaranteed_food`](./Shops.md#context-guaranteed_food) | Object | Examples: `{ ... }` | 2 |
| [`item`](./Shops.md#context-item) | Object | Examples: `{ ... }` | 2 |
| [`mostly_food`](./Shops.md#context-mostly_food) | Object | Examples: `{ ... }` | 2 |
| [`empty`](./Shops.md#context-empty) | Object | Examples: `{ ... }` | 1 |

</details>

---

### Object: `treasure`


**Definition:** No definition provided.  
**Total Count:** 14


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Object | Examples: `{ ... }` | 14 |

</details>

---

### Object: `item_rarity_costs`


**Definition:** No definition provided.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `consumable_common` | Number | Examples: `3, 5, 10` | 9 |
| `consumable_rare` | Number | Examples: `20, 8, 10` | 9 |
| `consumable_uncommon` | Number | Examples: `14, 5, 7` | 9 |
| `consumable_very_rare` | Number | Examples: `12, 40, 20` | 9 |
| `uncommon` | Number | Examples: `20, 8, 10` | 9 |
| `very_rare` | Number | Examples: `80, 40, 15` | 9 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 9 |

</details>

---

### Object: `button_nav`


**Definition:** No definition provided.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`default`](./Miscellaneous.md#context-default) | Object | Examples: `{ ... }` | 7 |

</details>

---

### Object: `pool`


**Definition:** No definition provided.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Object | Examples: `{ ... }` | 10 |

</details>

---

### Object: `mandatory`


**Definition:** No definition provided.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Object | Examples: `{ ... }` | 4 |
| `Furniture` | Object | Examples: `{ ... }` | 1 |

</details>

---

### Object: `Food`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`guaranteed_food`](./Shops.md#context-guaranteed_food), [`mostly_food`](./Shops.md#context-mostly_food)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allow_duplicates` | Boolean | Examples: `true` | 4 |
| `amount` | Number | Examples: `10` | 4 |
| `cost` | Number | Examples: `5` | 4 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 2 |

</details>

---

### Object: `LevelUp`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`levelup`](./Shops.md#context-levelup)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cost` | Number | Examples: `10` | 3 |

</details>

---

### Object: `levelup`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`LevelUp`](./Shops.md#context-levelup) | Object | Examples: `{ ... }` | 3 |

</details>

---

### Object: `breakdown2`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `common_item` | Number | Examples: `1` | 2 |
| `consumable` | Number | Examples: `1` | 2 |
| `guaranteed_food` | Number | Examples: `1` | 2 |
| `mostly_food` | Number | Examples: `1` | 2 |
| `item` | Number | Examples: `1` | 1 |

</details>

---

### Object: `breakdown3`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `common_item` | Number | Examples: `2` | 2 |
| `consumable` | Number | Examples: `1` | 2 |
| `guaranteed_food` | Number | Examples: `1` | 2 |
| `item` | Number | Examples: `1` | 1 |

</details>

---

### Object: `breakdown4`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `common_item` | Number | Examples: `2` | 2 |
| `consumable` | Number | Examples: `1` | 2 |
| `guaranteed_food` | Number | Examples: `1` | 2 |
| `item` | Number | Examples: `2, 1` | 2 |

</details>

---

### Object: `common_item`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Object | Examples: `{ ... }` | 2 |

</details>

---

### Object: `consumable`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Object | Examples: `{ ... }` | 2 |

</details>

---

### Object: `guaranteed_food`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Food`](./Shops.md#context-food) | Object | Examples: `{ ... }` | 2 |

</details>

---

### Object: `item`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Object | Examples: `{ ... }` | 2 |

</details>

---

### Object: `mostly_food`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Food`](./Shops.md#context-food) | Object | Examples: `{ ... }` | 2 |
| [`Item`](./Shops.md#context-item) | Object | Examples: `{ ... }` | 2 |

</details>

---

### Object: `empty`


**Definition:** Character Form: Behavior and stats for the \'Empty\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#context-item) | Object | Examples: `{ ... }` | 1 |

</details>

---
