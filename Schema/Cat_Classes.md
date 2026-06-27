# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Cat Classes

> **Associated Files:** `data/classes/`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 2609 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 2372 | `{ . . . }` |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array | An array of ability names available in the class's ability pool. | 14 | `[` |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array | An array of attack ability names available in the class's attack pool. | 14 | `[` |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array | An array of stat abbreviations that are randomly increased upon leveling up. | 14 | `[cha int con]`<br>`[cha int str]`<br>`[con str lck]` |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array | An array of passive ability names available in the class's passive pool. | 14 | `[` |
| [`stat_mods`](./Miscellaneous.md#object-stat_mods) | Object  | An object defining base stat modifiers for the class, with stat names as keys and integer adjustments as values. | 13 | `{ . . . }` |
| [`ability_groups`](./Miscellaneous.md#object-ability_groups) | Object  | An object grouping ability names into categories (e.g., attack, passive) for the class's ability selection. | 12 | `{ . . . }` |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array | An array of ability names that the class starts with at level 1. | 12 | `[` |
| [`complicated_abilities`](./Arrays.md#array-complicated_abilities) | Array | An array of ability names flagged as complicated, possibly for UI filtering or tutorial. | 6 | `[` |
| [`complicated_passives`](./Arrays.md#array-complicated_passives) | Array | An array of passive ability names flagged as complicated. | 6 | `[` |
| [`innate_passives`](./Miscellaneous.md#object-innate_passives) | Object  | An object defining innate passive abilities or effects that the class always possesses. | 4 | `{ . . . }` |
| [`innate_items`](./Miscellaneous.md#object-innate_items) | Object  | An object specifying the class's starting equipment, with item slot names as keys. | 2 | `{ . . . }` |
| [`move_pool`](./Arrays.md#array-move_pool) | Array | An array of movement ability names available to the class. | 1 | `[` |
| [`tutorial_levelup_active_pool`](./Arrays.md#array-tutorial_levelup_active_pool) | Array | An array of active ability names presented during tutorial level-up. | 1 | `[` |
| [`tutorial_levelup_active_pool_2`](./Arrays.md#array-tutorial_levelup_active_pool_2) | Array | An array of active ability names presented in a second tutorial level-up. | 1 | `[` |
| [`tutorial_levelup_passive_pool`](./Arrays.md#array-tutorial_levelup_passive_pool) | Array | An array of passive ability names presented during tutorial level-up. | 1 | `[` |

</details>


---


### Object: `graphics`


**Definition:** Object defining visual animations and sequence timings.  
**Total Count:** 2609

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array | An array of alternative animation state replacements, each as [state, animation_name]. | 47 | `[`<br>`[[idle girlyIdle]]` |
| [`palette`](./Enums.md#enum-palette) | Enum / Integer  | Specifies the color palette index for the ability's visuals. | 34 | `-1`<br>`0`<br>`1` |
| [`portrait_face`](./Enums.md#enum-portrait_face) | Enum | Specifies the portrait image to use for the class in the UI. | 13 | `butcher_portrait`<br>`druid_portrait`<br>`fighter_portrait` |
| [`default_face`](./Enums.md#enum-default_face) | Enum | Specifies the default facial expression for the unit's portrait. | 1 | `angry`<br>`happy`<br>`mad` |
| `hud_palette` | Number | The HUD color palette index used for the class's UI elements. | 1 | `11` |

</details>


---


### Object: `meta`


**Definition:** Object defining UI display data (Name, Description, Icon).  
**Total Count:** 2374

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1611 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`description`](./Strings.md#string-description) | String | A string key for the localized description of the class. | 14 | `"CAT_CLASS_BUTCHER_DESC"`<br>`"CAT_CLASS_COLORLESS_DESC"`<br>`"CAT_CLASS_DRUID_DESC"` |

</details>


---


### Object: `stat_mods`


**Definition:** Examples: `{ ... }`  
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`con`](./Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 9 | `-1`<br>`-2`<br>`-3` |
| [`cha`](./Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 7 | `+1`<br>`-1`<br>`-2` |
| [`int`](./Enums.md#enum-int) | Enum / Integer  | The Intelligence stat value or modifier. | 6 | `-1`<br>`-10`<br>`-2` |
| [`spd`](./Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 6 | `-1`<br>`-10`<br>`-2` |
| [`str`](./Enums.md#enum-str) | Enum / Integer  | The Strength stat value or modifier. | 6 | `-1`<br>`-2`<br>`-3` |
| [`dex`](./Enums.md#enum-dex) | Enum / Integer  | The Dexterity stat value or modifier. | 4 | `-1`<br>`-2`<br>`-3` |
| [`lck`](./Enums.md#enum-lck) | Enum / Integer  | The Luck stat value or modifier. | 4 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `ability_groups`


**Definition:** Examples: `{ ... }`  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 12 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`misc`](./Arrays.md#array-misc) | Array | A list of ability names that do not fit into other categories. | 12 | `[` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 12 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`defense`](./Arrays.md#array-defense) | Array | An array of defensive ability names. | 10 | `[` |

</details>


---


### Object: `innate_passives`


**Definition:** Examples: `{ ... }`  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`MonkStances`](./Arrays.md#array-monkstances) | Array | An array of stance ability names the Monk can switch between. | 1 | `[BasicMonkMelee BasicMonkRanged]` |
| [`AddStartingMana`](./Enums.md) | Integer | The amount of bonus mana the unit starts each battle with. | 1 | `20`<br>`5` |
| [`SpawnOnBattleStart`](./Enums.md#enum-spawnonbattlestart) | Enum  | Specifies the object that spawns adjacent to the unit at the start of battle. | 1 | `BeefyCharmedLeech`<br>`BuffCharmedKitten`<br>`CharmedCultist` |
| [`TinkererBasicAttackSwitching`](./Passives_and_Statuses.md#object-tinkererbasicattackswitching) | Object  | Defines the abilities used for the Tinkerer's basic attack switching mechanic. | 1 | `{ . . . }` |

</details>


---


### Object: `innate_items`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weapon`](./Enums.md#enum-weapon) | Enum | The name of the weapon item the unit starts with. | 2 | `AstroTaser`<br>`ButcherHook`<br>`CaveCatClub` |
| [`trinket`](./Enums.md#enum-trinket) | Enum | The name of the trinket item the unit starts with. | 1 | `MCHadouken`<br>`MonkStyleChanger` |

</details>


---


### Object: `TinkererBasicAttackSwitching`


**Definition:** Logic: Allows Tinkerer to swap basic attacks.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`innate_passives`](./Cat_Classes.md#object-innate_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum | The ability used for the craft action in the Tinkerer's basic attack switching. | 3 | `TinkererCraft` |
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum | The ability used for the throw action in the Tinkerer's basic attack switching. | 3 | `TinkererThrow` |

</details>


---