---
title: "Shops Schema"
description: "Vendor inventories and pricing multipliers."
---

# Shops Schema


<details open>
<summary><strong>Quick Navigation</strong></summary>

<table>
  <tr>
    <td width="22%"><strong>Core Entities & Combat</strong></td>
    <td><a href="../Core_Entities_and_Combat/Abilities_and_Spells.md">Abilities & Spells</a> • <a href="../Core_Entities_and_Combat/Characters_and_Bosses.md">Characters & Bosses</a> • <a href="../Core_Entities_and_Combat/Items_and_Equipment.md">Items & Equipment</a> • <a href="../Core_Entities_and_Combat/Passives_and_Statuses.md">Passives & Statuses</a> • <a href="../Core_Entities_and_Combat/Elite_Buffs.md">Elite Buffs</a> • <a href="../Core_Entities_and_Combat/Enemy_AI.md">Enemy AI</a> • <a href="../Core_Entities_and_Combat/Status_Effect_Keywords.md">Status Keywords</a></td>
  </tr>
  <tr>
    <td><strong>Engine Scripts & Logic</strong></td>
    <td><a href="../Engine_Scripts_and_Logic/Engine_LogicKeys.md">Logic Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_EventKeys.md">Event Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_DamagingKeys.md">Damaging Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md">Status & Passive Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md">Global Modifiers</a> • <a href="../Engine_Scripts_and_Logic/Math_Equations.md">Math Equations</a></td>
  </tr>
  <tr>
    <td><strong>Player Progression & Cats</strong></td>
    <td><a href="../Player_Progression_and_Cats/Cat_Classes.md">Cat Classes</a> • <a href="../Player_Progression_and_Cats/Cat_Mutations.md">Cat Mutations</a> • <a href="../Player_Progression_and_Cats/Custom_Cats.md">Custom Cats</a> • <a href="../Player_Progression_and_Cats/Injuries.md">Injuries</a> • <a href="../Player_Progression_and_Cats/Progression_Unlocks.md">Progression Unlocks</a> • <a href="../Player_Progression_and_Cats/Combat_Rewards.md">Combat Rewards</a></td>
  </tr>
  <tr>
    <td><strong>World, Maps & Events</strong></td>
    <td><a href="../World_Maps_and_Events/Events_and_Encounters.md">Events & Encounters</a> • <a href="../World_Maps_and_Events/House_and_Environment.md">House & Environment</a> • <a href="../World_Maps_and_Events/Map_Generation_and_Routing.md">Map Gen & Routing</a> • <a href="../World_Maps_and_Events/Furniture_and_Metaprogression.md">Furniture & Meta</a> • <a href="../World_Maps_and_Events/Shops.md">Shops</a> • <a href="../World_Maps_and_Events/Spawns_and_Enemy_Pools.md">Spawns & Enemy Pools</a> • <a href="../World_Maps_and_Events/Boss_Cutscene_Info.md">Boss Cutscenes</a> • <a href="../World_Maps_and_Events/NPC_Scripts.md">NPC Scripts</a></td>
  </tr>
  <tr>
    <td><strong>Assets & Localization</strong></td>
    <td><a href="../Assets_and_Localization/Audio_SFX_Dictionary.md">Audio SFX</a> • <a href="../Assets_and_Localization/Particles_and_VFX_Dictionary.md">Particles & VFX</a> • <a href="../Assets_and_Localization/Damage_Text_Styles.md">Damage Text</a> • <a href="../Assets_and_Localization/Localization_Guide.md">Localization Guide</a> • <a href="../Assets_and_Localization/Text_Formatting_and_Effects.md">Text Formatting</a> • <a href="../Assets_and_Localization/Strings.md">Strings</a></td>
  </tr>
  <tr>
    <td><strong>Reference & Meta</strong></td>
    <td><a href="../Reference_and_Meta/Enums.md">Enums</a> • <a href="../Reference_and_Meta/Arrays.md">Arrays</a> • <a href="../Reference_and_Meta/Item_Pools.md">Item Pools</a> • <a href="../Reference_and_Meta/Difficulties.md">Difficulties</a> • <a href="../Reference_and_Meta/Engine_Hidden_Passives_and_Statuses.md">Hidden Passives</a> • <a href="../Reference_and_Meta/Passive_Identifiers_Audit.md">Passive Audit</a> • <a href="../Reference_and_Meta/Engine_Uncategorized_Resources.md">Uncategorized Keys</a> • <a href="../Reference_and_Meta/Miscellaneous.md">Miscellaneous</a></td>
  </tr>
</table>

</details>

## Overview
> [!NOTE]
> This schema governs NPCs who sell items. It specifies which item pools they draw from and how heavily they mark up their prices.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
ItemShopSmall {
    meta {
        movieclip Shop
        npc_script tracy_adventure_shop_script.gon
        delay_enable_tooltips true
        keeper 0
        shopkeeper_fights [
            test.lvl
        ]
    }

    item_rarity_costs {
        consumable_common 5
        consumable_uncommon 7
        consumable_rare 10
        consumable_very_rare 20
        common 7
        uncommon 10
        rare 20
        very_rare 40
    }

    item_groups {
        mandatory {
            Item {
                pool rare 
            }
        }
        levelup {
            LevelUp {
                cost 10
            }
        }
        pool {
            Item {
                pool shop_common
            }
        }
    }

    breakdown {
        levelup 1
        pool 2
    }

    stock_fill_order {
        //0 1 2
        // 3 4

        1 [1]
        2 [0 2]
        3 [1 3 4]
        4 [0 2 3 4]
        5 [1 0 2 3 4]
    }

    button_nav {
        //up down left right, x = no connection
        default {
            0 [x 3 x 1]
            1 [x 3 0 2]
            2 [x 4 1 x]
            3 [0 x x 4]
            4 [2 x 3 x]
        }
        //stock fill overrides
        3 { //if exactly 3 items in stock
            3 [1 x x 4]
            4 [1 x 3 x]
        }
    }
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Shops.md`](../../Directory/World_and_Events/Shops.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Shops

> **Associated Files:** `data/shops/`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 25

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 25 | `{ . . . }` |
| [`breakdown`](./Shops.md#object-breakdown) | Object  | Defines the breakdown of item pools or rewards for a shop or event. | 24 | `{ . . . }` |
| [`item_groups`](./Shops.md#object-item_groups) | Object  | Defines groups of items that can appear in a shop or loot. | 24 | `{ . . . }` |
| [`item_rarity_costs`](./Shops.md#object-item_rarity_costs) | Object  | Defines the cost multipliers for each item rarity tier in a shop. | 9 | `{ . . . }` |
| `stock_fill_order` | Object | Defines the order in which shop slots are filled from the stock list. | 9 | `{ . . . }` |
| [`button_nav`](./Shops.md#object-button_nav) | Object  | Defines the directional navigation grid for UI button selection, with each button having connections to adjacent buttons. | 7 | `{ . . . }` |
| [`breakdown2`](./Shops.md#object-breakdown2) | Object  | A loot table defining guaranteed item drops for player levels 5 to 9. | 2 | `{ . . . }` |
| [`breakdown3`](./Shops.md#object-breakdown3) | Object  | A loot table defining guaranteed item drops for player levels 10 to 14. | 2 | `{ . . . }` |
| [`breakdown4`](./Shops.md#object-breakdown4) | Object  | A loot table defining guaranteed item drops for player levels 15 and above. | 2 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `meta`


**Definition:** Contains metadata for the ability including name, description, class, and type icon.  
**Total Count:** 2374

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 25 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `treasure_room` | Boolean | If true, this level is a treasure room. | 14 | `true` |
| `delay_enable_tooltips` | Boolean | If true, delays the enabling of tooltips in this scene. | 7 | `true` |
| `keeper` | Number | The number of items the shopkeeper keeps from a previous visit. | 7 | `0` |
| [`npc_script`](../Reference_and_Meta/Enums.md#enum-npc_script) | Enum | The filename of the script controlling the NPC in this scene. | 7 | `tracy_adventure_shop_script.gon` |
| [`shopkeeper_fights`](../Reference_and_Meta/Arrays.md#array-shopkeeper_fights) | Array | Array of references to battles the shopkeeper can fight. | 7 | `[` |
| `house_shop` | Boolean | If true, this shop is a house shop (player enters the house to browse). | 4 | `true` |
| [`welcome_message`](../Reference_and_Meta/Enums.md#enum-welcome_message) | Enum | The identifier for the welcome message displayed upon entering this shop. | 2 | `welcome_water`<br>`welcome_water_cheap` |
| `pick_n` | Number | The number of items the player can pick from a selection. | 1 | `1` |

</details>


---


### Object: `pool`


**Definition:** Specifies the name of the pool from which an ability is learned or an item is crafted.  
**Total Count:** 154

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#object-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 10 | `{ . . . }` |

</details>


---


### Object: `consumable`


**Definition:** If true, the item is consumed on use. Can also specify a number of uses or an item pool.  
**Total Count:** 124

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#object-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 2 | `{ . . . }` |

</details>


---


### Object: `treasure`


**Definition:** Defines a treasure node containing items or item pools.  
**Total Count:** 45

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#object-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 14 | `{ . . . }` |

</details>


---


### Object: `Item`


**Definition:** An object defining the item pool, cost, weight, and mandatory flag used in an item group.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common_item`](./Shops.md#object-common_item), [`consumable`](./Shops.md#object-consumable), [`empty`](./Shops.md#object-empty), [`item`](./Shops.md#object-item), [`mandatory`](./Shops.md#object-mandatory), [`mostly_food`](./Shops.md#object-mostly_food), [`pool`](./Shops.md#object-pool), [`treasure`](./Shops.md#object-treasure)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 37 | `2`<br>`3`<br>`4` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 21 | `{ . . . }` |
| `mandatory` | Boolean | The number of guaranteed items to generate from this group, or an object specifying mandatory selection. | 14 | `1`<br>`3`<br>`6` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 6 | `common`<br>`rare`<br>`cha` |
| `weight` | Float | A multiplier or priority value for random selection or effect magnitude. | 2 | `.25`<br>`.5`<br>`1` |

</details>


---


### Object: `Food`


**Definition:** The number of food pickups spawned.  
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`guaranteed_food`](./Shops.md#object-guaranteed_food), [`mostly_food`](./Shops.md#object-mostly_food)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 4 | `{ . . . }` |
| `amount` | Array / Float | For ambient light, the target brightness value (as a float or percentage array for RGB). | 4 | `.1`<br>`.25`<br>`.35` |
| `allow_duplicates` | Boolean | If true, duplicate items of this type can appear in the same shop inventory. | 4 | `true` |
| `weight` | Float | A multiplier or priority value for random selection or effect magnitude. | 2 | `.25`<br>`.5`<br>`1` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `item_groups`


**Definition:** Defines groups of items that can appear in a shop or loot.  
**Total Count:** 24

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`treasure`](./Shops.md#object-treasure) | Object  | Defines a treasure node containing items or item pools. | 14 | `{ . . . }` |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 6 | `2`<br>`3`<br>`4` |
| [`mandatory`](./Shops.md#object-mandatory) | Object  | The number of guaranteed items to generate from this group, or an object specifying mandatory selection. | 5 | `{ . . . }` |
| [`levelup`](./Shops.md#object-levelup) | Object  | The number of level-up rewards offered, or an object defining their cost and pool. | 3 | `{ . . . }` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 2 | `1`<br>`2`<br>`true` |
| [`item`](../Reference_and_Meta/Enums.md#enum-item) | Enum  | Specifies the item to transform into, either by name, a nested item object, or a numeric value. | 2 | `1`<br>`2`<br>`EstusFlask_Full` |
| [`guaranteed_food`](./Shops.md#object-guaranteed_food) | Object  | The number of guaranteed food items, or an object defining their amount, cost, and duplication rules. | 2 | `{ . . . }` |
| [`common_item`](./Shops.md#object-common_item) | Object  | The number of common items offered, or an object defining their pool and cost. | 2 | `{ . . . }` |
| [`mostly_food`](./Shops.md#object-mostly_food) | Object  | The number of mostly-food items offered, or an object defining their amount, cost, weight, and duplication rules. | 2 | `{ . . . }` |
| [`empty`](./Shops.md#object-empty) | Object  | The number of empty items offered, or an object defining their pool and cost. | 1 | `{ . . . }` |

</details>


---


### Object: `breakdown`


**Definition:** Defines the breakdown of item pools or rewards for a shop or event.  
**Total Count:** 24

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `treasure` | Number | Defines a treasure node containing items or item pools. | 14 | `1` |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 6 | `2`<br>`3`<br>`4` |
| `mandatory` | Number | The number of guaranteed items to generate from this group, or an object specifying mandatory selection. | 3 | `1`<br>`3`<br>`6` |
| `levelup` | Number | The number of level-up rewards offered, or an object defining their cost and pool. | 3 | `1` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 2 | `1`<br>`2`<br>`true` |
| `guaranteed_food` | Number | The number of guaranteed food items, or an object defining their amount, cost, and duplication rules. | 2 | `1` |
| `mostly_food` | Number | The number of mostly-food items offered, or an object defining their amount, cost, weight, and duplication rules. | 2 | `1`<br>`2` |
| `empty` | Number | The number of empty items offered, or an object defining their pool and cost. | 1 | `1` |
| [`item`](../Reference_and_Meta/Enums.md#enum-item) | Enum  | Specifies the item to transform into, either by name, a nested item object, or a numeric value. | 1 | `1`<br>`2`<br>`EstusFlask_Full` |

</details>


---


### Object: `mandatory`


**Definition:** The number of guaranteed items to generate from this group, or an object specifying mandatory selection.  
**Total Count:** 22

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#object-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 4 | `{ . . . }` |
| `Furniture` | Object | Defines the group of furniture items available in a shop. | 1 | `{ . . . }` |

</details>


---


### Object: `empty`


**Definition:** The number of empty items offered, or an object defining their pool and cost.  
**Total Count:** 15

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#object-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 1 | `{ . . . }` |

</details>


---
### Object: `item`


**Definition:** Specifies the item to transform into, either by name, a nested item object, or a numeric value.  
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#object-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 2 | `{ . . . }` |

</details>


---


### Object: `guaranteed_food`


**Definition:** The number of guaranteed food items, or an object defining their amount, cost, and duplication rules.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#object-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Food`](./Shops.md#object-food) | Integer / Object  | The number of food pickups spawned. | 2 | `{ . . . }`<br>`20` |

</details>


---


### Object: `item_rarity_costs`


**Definition:** Defines the cost multipliers for each item rarity tier in a shop.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `common` | Integer | Defines the common reward block for a boss encounter. | 9 | `100`<br>`14`<br>`5` |
| `rare` | Integer | Defines the rare reward block for a boss encounter. | 9 | `1`<br>`10`<br>`15` |
| `uncommon` | Number | The weight value for uncommon items in a random pool distribution. | 9 | `10`<br>`20`<br>`30` |
| `very_rare` | Float | The weight value for very rare items in a random pool distribution. | 9 | `.01`<br>`1`<br>`15` |
| `consumable_common` | Number | The cost or quantity for common consumable items in an item shop. | 9 | `10`<br>`3`<br>`5` |
| `consumable_rare` | Number | The cost or quantity for rare consumable items in an item shop. | 9 | `10`<br>`20`<br>`8` |
| `consumable_uncommon` | Number | The cost or quantity for uncommon consumable items in an item shop. | 9 | `14`<br>`5`<br>`7` |
| `consumable_very_rare` | Number | The cost or quantity for very rare consumable items in an item shop. | 9 | `12`<br>`20`<br>`40` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 9 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `common_item`


**Definition:** The number of common items offered, or an object defining their pool and cost.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#object-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 2 | `{ . . . }` |

</details>


---


### Object: `button_nav`


**Definition:** Defines the directional navigation grid for UI button selection, with each button having connections to adjacent buttons.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`default`](../Reference_and_Meta/Miscellaneous.md#object-default) | Enum / Object  | The default configuration or value used when no specific override is provided. | 7 | `{ . . . }`<br>`bite1` |

</details>


---


### Object: `mostly_food`


**Definition:** The number of mostly-food items offered, or an object defining their amount, cost, weight, and duplication rules.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#object-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Item`](./Shops.md#object-item) | Object  | An object defining the item pool, cost, weight, and mandatory flag used in an item group. | 2 | `{ . . . }` |
| [`Food`](./Shops.md#object-food) | Integer / Object  | The number of food pickups spawned. | 2 | `{ . . . }`<br>`20` |

</details>


---


### Object: `levelup`


**Definition:** The number of level-up rewards offered, or an object defining their cost and pool.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#object-item_groups)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`LevelUp`](./Shops.md#object-levelup) | Object  | Defines the cost and pool for leveling up an item. | 3 | `{ . . . }` |

</details>


---


### Object: `LevelUp`


**Definition:** Defines the cost and pool for leveling up an item.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`levelup`](./Shops.md#object-levelup)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 3 | `{ . . . }` |

</details>


---


### Object: `breakdown4`


**Definition:** A loot table defining guaranteed item drops for player levels 15 and above.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 2 | `1`<br>`2`<br>`true` |
| [`item`](../Reference_and_Meta/Enums.md#enum-item) | Enum  | Specifies the item to transform into, either by name, a nested item object, or a numeric value. | 2 | `1`<br>`2`<br>`EstusFlask_Full` |
| `guaranteed_food` | Number | The number of guaranteed food items, or an object defining their amount, cost, and duplication rules. | 2 | `1` |
| `common_item` | Number | The number of common items offered, or an object defining their pool and cost. | 2 | `1`<br>`2` |

</details>


---


### Object: `breakdown3`


**Definition:** A loot table defining guaranteed item drops for player levels 10 to 14.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 2 | `1`<br>`2`<br>`true` |
| `guaranteed_food` | Number | The number of guaranteed food items, or an object defining their amount, cost, and duplication rules. | 2 | `1` |
| `common_item` | Number | The number of common items offered, or an object defining their pool and cost. | 2 | `1`<br>`2` |
| [`item`](../Reference_and_Meta/Enums.md#enum-item) | Enum  | Specifies the item to transform into, either by name, a nested item object, or a numeric value. | 1 | `1`<br>`2`<br>`EstusFlask_Full` |

</details>


---


### Object: `breakdown2`


**Definition:** A loot table defining guaranteed item drops for player levels 5 to 9.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 2 | `1`<br>`2`<br>`true` |
| `guaranteed_food` | Number | The number of guaranteed food items, or an object defining their amount, cost, and duplication rules. | 2 | `1` |
| `common_item` | Number | The number of common items offered, or an object defining their pool and cost. | 2 | `1`<br>`2` |
| `mostly_food` | Number | The number of mostly-food items offered, or an object defining their amount, cost, weight, and duplication rules. | 2 | `1`<br>`2` |
| [`item`](../Reference_and_Meta/Enums.md#enum-item) | Enum  | Specifies the item to transform into, either by name, a nested item object, or a numeric value. | 1 | `1`<br>`2`<br>`EstusFlask_Full` |

</details>


---

