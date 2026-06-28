---
title: "Cat Classes Schema"
description: "Defines the progression and stats of cat classes."
---

# Cat Classes Schema

## Overview
> [!NOTE]
> This schema dictates the stat scaling, ability pools, and visual outfits associated with a specific class of cat (like Hunter, Mage, etc).

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
Hunter {
    meta {
        name "CAT_CLASS_HUNTER_NAME"
        description "CAT_CLASS_HUNTER_DESC"
    }
    graphics {
        palette 50
        alt_animations [
            [idle, HunterIdle]
        ]
        portrait_face hunter_portrait
    }
    attack_pool [ BasicRanged_Hunter ]
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Classes.md`](../../Directory/Cats_and_Classes/Classes.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Cat Classes

> **Associated Files:** `data/classes/`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 2609 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 2372 | `{ . . . }` |
| [`ability_pool`](../Reference_and_Meta/Arrays.md#array-ability_pool) | Array | An array of ability names available in the class's ability pool. | 14 | `[` |
| [`attack_pool`](../Reference_and_Meta/Arrays.md#array-attack_pool) | Array | An array of attack ability names available in the class's attack pool. | 14 | `[` |
| [`levelup_stats`](../Reference_and_Meta/Arrays.md#array-levelup_stats) | Array | An array of stat abbreviations that are randomly increased upon leveling up. | 14 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](../Reference_and_Meta/Arrays.md#array-passive_pool) | Array | An array of passive ability names available in the class's passive pool. | 14 | `[` |
| [`stat_mods`](../Reference_and_Meta/Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. | 13 | `{ . . . }` |
| [`ability_groups`](../Reference_and_Meta/Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. | 12 | `{ . . . }` |
| [`starter_abilities`](../Reference_and_Meta/Arrays.md#array-starter_abilities) | Array | An array of ability names that the class starts with at level 1. | 12 | `[` |
| [`complicated_abilities`](../Reference_and_Meta/Arrays.md#array-complicated_abilities) | Array | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. | 6 | `[` |
| [`complicated_passives`](../Reference_and_Meta/Arrays.md#array-complicated_passives) | Array | An array of passive ability names flagged as complicated. | 6 | `[` |
| [`innate_passives`](../Reference_and_Meta/Miscellaneous.md#object-innate_passives) | Object  | An object defining innate passive abilities or effects that the class always possesses. | 4 | `{ . . . }` |
| [`innate_items`](../Reference_and_Meta/Miscellaneous.md#object-innate_items) | Object  | An object specifying the class's starting equipment, with item slot names as keys. | 2 | `{ . . . }` |
| [`move_pool`](../Reference_and_Meta/Arrays.md#array-move_pool) | Array | An array of movement ability names available to the class. | 1 | `[` |
| [`tutorial_levelup_active_pool`](../Reference_and_Meta/Arrays.md#array-tutorial_levelup_active_pool) | Array | An array of active ability names presented during tutorial level-up. | 1 | `[` |
| [`tutorial_levelup_active_pool_2`](../Reference_and_Meta/Arrays.md#array-tutorial_levelup_active_pool_2) | Array | An array of active ability names presented in a second tutorial level-up. | 1 | `[` |
| [`tutorial_levelup_passive_pool`](../Reference_and_Meta/Arrays.md#array-tutorial_levelup_passive_pool) | Array | An array of passive ability names presented during tutorial level-up. | 1 | `[` |

</details>


---


### Object: `graphics`


**Definition:** An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects.
**Total Count:** 2609

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_animations`](../Reference_and_Meta/Arrays.md#array-alt_animations) | Array | An array of alternative animation state replacements, each as [state, animation_name]. | 47 | `[`<br>`[[idle girlyIdle]]` |
| [`palette`](../Reference_and_Meta/Enums.md#enum-palette) | Enum / Integer  | Specifies the color palette index for the ability's visuals. | 34 | `-1`<br>`0`<br>`1` |
| [`portrait_face`](../Reference_and_Meta/Enums.md#enum-portrait_face) | Enum | Specifies the portrait image to use for the class in the UI. | 13 | `butcher_portrait`<br>`druid_portrait`<br>`fighter_portrait` |
| [`default_face`](../Reference_and_Meta/Enums.md#enum-default_face) | Enum | Specifies the default facial expression for the unit's portrait. | 1 | `angry`<br>`happy`<br>`mad` |
| `hud_palette` | Number | The HUD color palette index used for the class's UI elements. | 1 | `11` |

</details>


---


### Object: `meta`


**Definition:** Contains metadata for the ability including name, description, class, and type icon.
**Total Count:** 2374

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1611 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`description`](../Assets_and_Localization/Strings.md#string-description) | String | A string key for the localized description of the class. | 14 | `"CAT_CLASS_BUTCHER_DESC"`<br>`"CAT_CLASS_COLORLESS_DESC"`<br>`"CAT_CLASS_DRUID_DESC"` |

</details>


---


### Object: `stat_mods`


**Definition:** An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values.
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`con`](../Reference_and_Meta/Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 9 | `-1`<br>`-2`<br>`-3` |
| [`cha`](../Reference_and_Meta/Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 7 | `+1`<br>`-1`<br>`-2` |
| [`int`](../Reference_and_Meta/Enums.md#enum-int) | Enum / Integer  | The Intelligence stat value or modifier. | 6 | `-1`<br>`-10`<br>`-2` |
| [`spd`](../Reference_and_Meta/Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 6 | `-1`<br>`-10`<br>`-2` |
| [`str`](../Reference_and_Meta/Enums.md#enum-str) | Enum / Integer  | The Strength stat value or modifier. | 6 | `-1`<br>`-2`<br>`-3` |
| [`dex`](../Reference_and_Meta/Enums.md#enum-dex) | Enum / Integer  | The Dexterity stat value or modifier. | 4 | `-1`<br>`-2`<br>`-3` |
| [`lck`](../Reference_and_Meta/Enums.md#enum-lck) | Enum / Integer  | The Luck stat value or modifier. | 4 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `ability_groups`


**Definition:** An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection.
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 12 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`misc`](../Reference_and_Meta/Arrays.md#array-misc) | Array | A list of ability names that do not fit into other categories. | 12 | `[` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 12 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`defense`](../Reference_and_Meta/Arrays.md#array-defense) | Array | An array of defensive ability names. | 10 | `[` |

</details>


---


### Object: `innate_passives`


**Definition:** An object defining innate passive abilities or effects that the class always possesses.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`MonkStances`](../Reference_and_Meta/Arrays.md#array-monkstances) | Array | An array of stance ability names the Monk can switch between. | 1 | `[BasicMonkMelee BasicMonkRanged]` |
| `AddStartingMana` | Integer | The amount of bonus mana the unit starts each battle with. | 1 | `20`<br>`5` |
| [`SpawnOnBattleStart`](../Reference_and_Meta/Enums.md#enum-spawnonbattlestart) | Enum  | Specifies the object that spawns adjacent to the unit at the start of battle. | 1 | `BeefyCharmedLeech`<br>`BuffCharmedKitten`<br>`CharmedCultist` |
| [`TinkererBasicAttackSwitching`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-tinkererbasicattackswitching) | Object  | Defines the abilities used for the Tinkerer's basic attack switching mechanic. | 1 | `{ . . . }` |

</details>


---


### Object: `innate_items`


**Definition:** An object specifying the class's starting equipment, with item slot names as keys.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weapon`](../Reference_and_Meta/Enums.md#enum-weapon) | Enum | The name of the weapon item the unit starts with. | 2 | `AstroTaser`<br>`ButcherHook`<br>`CaveCatClub` |
| [`trinket`](../Reference_and_Meta/Enums.md#enum-trinket) | Enum | The name of the trinket item the unit starts with. | 1 | `MCHadouken`<br>`MonkStyleChanger` |

</details>


---


### Object: `TinkererBasicAttackSwitching`


**Definition:** Defines the abilities used for the Tinkerer's basic attack switching mechanic.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`innate_passives`](./Cat_Classes.md#object-innate_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`craft_ability`](../Reference_and_Meta/Enums.md#enum-craft_ability) | Enum | The ability used for the craft action in the Tinkerer's basic attack switching. | 3 | `TinkererCraft` |
| [`throw_ability`](../Reference_and_Meta/Enums.md#enum-throw_ability) | Enum | The ability used for the throw action in the Tinkerer's basic attack switching. | 3 | `TinkererThrow` |

</details>


---