# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Shops

> **Associated Files:** `data/shops/`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 25

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 2372 | `{ . . . }` |
| [`breakdown`](./Shops.md#object-breakdown) | Object  | Defines the breakdown of item pools or rewards for a shop or event. | 24 | `{ . . . }` |
| [`item_groups`](./Shops.md#object-item_groups) | Object  | Defines groups of items that can appear in a shop or loot. | 24 | `{ . . . }` |
| [`item_rarity_costs`](./Shops.md#object-item_rarity_costs) | Object  | Defines the cost multipliers for each item rarity tier in a shop. | 9 | `{ . . . }` |
| `stock_fill_order` | Object | Defines the order in which shop slots are filled from the stock list. | 9 | `{ . . . }` |
| [`button_nav`](./Shops.md#object-button_nav) | Object  | Defines the directional navigation grid for UI button selection, with each button having connections to adjacent buttons. | 7 | `{ . . . }` |
| [`breakdown2`](./Shops.md#object-breakdown2) | Object  | A loot table defining guaranteed item drops for player levels 5 to 9. | 2 | `{ . . . }` |
| [`breakdown3`](./Shops.md#object-breakdown3) | Object  | A loot table defining guaranteed item drops for player levels 10 to 14. | 2 | `{ . . . }` |
| [`breakdown4`](./Shops.md#object-breakdown4) | Object  | A loot table defining guaranteed item drops for player levels 15 and above. | 2 | `{ . . . }` |

</details>


---


### Object: `Item`


**Definition:** No definition provided.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common_item`](./Shops.md#context-common_item), [`consumable`](./Shops.md#context-consumable), [`empty`](./Shops.md#context-empty), [`item`](./Shops.md#context-item), [`mandatory`](./Shops.md#context-mandatory), [`mostly_food`](./Shops.md#context-mostly_food), [`pool`](./Shops.md#context-pool), [`treasure`](./Shops.md#context-treasure)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 37 | `2`<br>`3`<br>`4` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 21 | `{ . . . }` |
| `mandatory` | Boolean | The number of guaranteed items to generate from this group, or an object specifying mandatory selection. | 14 | `1`<br>`3`<br>`6` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 | `common`<br>`rare`<br>`cha` |
| [`weight`](./Enums.md) | Integer | A multiplier or priority value for random selection or effect magnitude. | 2 | `.25`<br>`.5`<br>`1` |

</details>


---


### Object: `meta`


**Definition:** Object defining UI display data (Name, Description, Icon).  
**Total Count:** 25

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 25 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `treasure_room` | Boolean | If true, this level is a treasure room. | 14 | `true` |
| `delay_enable_tooltips` | Boolean | If true, delays the enabling of tooltips in this scene. | 7 | `true` |
| `keeper` | Number | The number of items the shopkeeper keeps from a previous visit. | 7 | `0` |
| [`npc_script`](./Enums.md#enum-npc_script) | Enum | The filename of the script controlling the NPC in this scene. | 7 | `tracy_adventure_shop_script.gon` |
| [`shopkeeper_fights`](./Arrays.md#array-shopkeeper_fights) | Array | Array of references to battles the shopkeeper can fight. | 7 | `[` |
| `house_shop` | Boolean | If true, this shop is a house shop (player enters the house to browse). | 4 | `true` |
| [`welcome_message`](./Enums.md#enum-welcome_message) | Enum | The identifier for the welcome message displayed upon entering this shop. | 2 | `welcome_water`<br>`welcome_water_cheap` |
| `pick_n` | Number | The number of items the player can pick from a selection. | 1 | `1` |

</details>


---


### Object: `breakdown`


**Definition:** No definition provided.  
**Total Count:** 24

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `treasure` | Number | Defines a treasure node containing items or item pools. | 14 | `1` |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 6 | `2`<br>`3`<br>`4` |
| `levelup` | Number | The number of level-up rewards offered, or an object defining their cost and pool. | 3 | `1` |
| `mandatory` | Number | The number of guaranteed items to generate from this group, or an object specifying mandatory selection. | 3 | `1`<br>`3`<br>`6` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 2 | `1`<br>`2`<br>`true` |
| `guaranteed_food` | Number | The number of guaranteed food items, or an object defining their amount, cost, and duplication rules. | 2 | `1` |
| `mostly_food` | Number | The number of mostly-food items offered, or an object defining their amount, cost, weight, and duplication rules. | 2 | `1`<br>`2` |
| `empty` | Number | The number of empty items offered, or an object defining their pool and cost. | 1 | `1` |
| [`item`](./Enums.md#enum-item) | Enum  | Specifies the item to transform into, either by name, a nested item object, or a numeric value. | 1 | `1`<br>`2`<br>`EstusFlask_Full` |

</details>


---


### Object: `item_groups`


**Definition:** No definition provided.  
**Total Count:** 24

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`treasure`](./Shops.md#object-treasure) | Object  | Defines a treasure node containing items or item pools. | 14 | `{ . . . }` |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 6 | `2`<br>`3`<br>`4` |
| [`mandatory`](./Shops.md#object-mandatory) | Object  | The number of guaranteed items to generate from this group, or an object specifying mandatory selection. | 5 | `{ . . . }` |
| [`levelup`](./Shops.md#object-levelup) | Object  | The number of level-up rewards offered, or an object defining their cost and pool. | 3 | `{ . . . }` |
| [`common_item`](./Shops.md#object-common_item) | Object  | The number of common items offered, or an object defining their pool and cost. | 2 | `{ . . . }` |
| [`consumable`](./Shops.md#context-consumable) | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 2 | `1`<br>`2`<br>`true` |
| [`guaranteed_food`](./Shops.md#object-guaranteed_food) | Object  | The number of guaranteed food items, or an object defining their amount, cost, and duplication rules. | 2 | `{ . . . }` |
| [`item`](./Enums.md#enum-item) | Enum  | Specifies the item to transform into, either by name, a nested item object, or a numeric value. | 2 | `1`<br>`2`<br>`EstusFlask_Full` |
| [`mostly_food`](./Shops.md#object-mostly_food) | Object  | The number of mostly-food items offered, or an object defining their amount, cost, weight, and duplication rules. | 2 | `{ . . . }` |
| [`empty`](./Shops.md#object-empty) | Object  | The number of empty items offered, or an object defining their pool and cost. | 1 | `{ . . . }` |

</details>


---


### Object: `treasure`


**Definition:** No definition provided.  
**Total Count:** 14

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 14 | `{ . . . }` |

</details>


---


### Object: `item_rarity_costs`


**Definition:** No definition provided.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `consumable_common` | Number | The cost or quantity for common consumable items in an item shop. | 9 | `10`<br>`3`<br>`5` |
| `consumable_rare` | Number | The cost or quantity for rare consumable items in an item shop. | 9 | `10`<br>`20`<br>`8` |
| `consumable_uncommon` | Number | The cost or quantity for uncommon consumable items in an item shop. | 9 | `14`<br>`5`<br>`7` |
| `consumable_very_rare` | Number | The cost or quantity for very rare consumable items in an item shop. | 9 | `12`<br>`20`<br>`40` |
| `uncommon` | Number | The weight value for uncommon items in a random pool distribution. | 9 | `10`<br>`20`<br>`30` |
| `very_rare` | Number | The weight value for very rare items in a random pool distribution. | 9 | `.01`<br>`1`<br>`15` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 9 | `common`<br>`rare`<br>`cha` |
| [`common`](./Enums.md) | Integer | Defines the common reward block for a boss encounter. | 9 | `100`<br>`14`<br>`5` |
| [`rare`](./Enums.md) | Integer | Defines the rare reward block for a boss encounter. | 9 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `button_nav`


**Definition:** No definition provided.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`default`](./Miscellaneous.md#object-default) | Enum / Object  | The default configuration or value used when no specific override is provided. | 7 | `{ . . . }`<br>`bite1` |

</details>


---


### Object: `pool`


**Definition:** No definition provided.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 6 | `{ . . . }` |

</details>


---


### Object: `mandatory`


**Definition:** No definition provided.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 4 | `{ . . . }` |
| `Furniture` | Object | Defines the group of furniture items available in a shop. | 1 | `{ . . . }` |

</details>


---


### Object: `Food`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`guaranteed_food`](./Shops.md#context-guaranteed_food), [`mostly_food`](./Shops.md#context-mostly_food)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_duplicates` | Boolean | If true, duplicate items of this type can appear in the same shop inventory. | 4 | `true` |
| [`amount`](./Arrays.md#array-amount) | Array  | For ambient light, the target brightness value (as a float or percentage array for RGB). | 4 | `.1`<br>`.25`<br>`.35` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 4 | `{ . . . }` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 | `common`<br>`rare`<br>`cha` |
| [`weight`](./Enums.md) | Integer | A multiplier or priority value for random selection or effect magnitude. | 2 | `.25`<br>`.5`<br>`1` |

</details>


---


### Object: `LevelUp`


**Definition:** No definition provided.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`levelup`](./Shops.md#context-levelup)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 3 | `{ . . . }` |

</details>


---


### Object: `levelup`


**Definition:** No definition provided.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`LevelUp`](./Shops.md#object-levelup) | Object  | Defines the cost and pool for leveling up an item. | 3 | `{ . . . }` |

</details>


---


### Object: `breakdown2`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `common_item` | Number | The number of common items offered, or an object defining their pool and cost. | 2 | `1`<br>`2` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 2 | `1`<br>`2`<br>`true` |
| `guaranteed_food` | Number | The number of guaranteed food items, or an object defining their amount, cost, and duplication rules. | 2 | `1` |
| `mostly_food` | Number | The number of mostly-food items offered, or an object defining their amount, cost, weight, and duplication rules. | 2 | `1`<br>`2` |
| [`item`](./Enums.md#enum-item) | Enum  | Specifies the item to transform into, either by name, a nested item object, or a numeric value. | 1 | `1`<br>`2`<br>`EstusFlask_Full` |

</details>


---


### Object: `breakdown3`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `common_item` | Number | The number of common items offered, or an object defining their pool and cost. | 2 | `1`<br>`2` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 2 | `1`<br>`2`<br>`true` |
| `guaranteed_food` | Number | The number of guaranteed food items, or an object defining their amount, cost, and duplication rules. | 2 | `1` |
| [`item`](./Enums.md#enum-item) | Enum  | Specifies the item to transform into, either by name, a nested item object, or a numeric value. | 1 | `1`<br>`2`<br>`EstusFlask_Full` |

</details>


---


### Object: `breakdown4`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `common_item` | Number | The number of common items offered, or an object defining their pool and cost. | 2 | `1`<br>`2` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 2 | `1`<br>`2`<br>`true` |
| `guaranteed_food` | Number | The number of guaranteed food items, or an object defining their amount, cost, and duplication rules. | 2 | `1` |
| [`item`](./Enums.md#enum-item) | Enum  | Specifies the item to transform into, either by name, a nested item object, or a numeric value. | 2 | `1`<br>`2`<br>`EstusFlask_Full` |

</details>


---


### Object: `common_item`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 2 | `{ . . . }` |

</details>


---


### Object: `consumable`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 2 | `{ . . . }` |

</details>


---


### Object: `guaranteed_food`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Food`](./Shops.md#object-food) | Integer / Object  | The number of food pickups spawned. | 2 | `{ . . . }`<br>`20` |

</details>


---


### Object: `item`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 2 | `{ . . . }` |

</details>


---


### Object: `mostly_food`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Food`](./Shops.md#object-food) | Integer / Object  | The number of food pickups spawned. | 2 | `{ . . . }`<br>`20` |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 2 | `{ . . . }` |

</details>


---


### Object: `empty`


**Definition:** Character Form: Behavior and stats for the \'Empty\' state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 1 | `{ . . . }` |

</details>


---