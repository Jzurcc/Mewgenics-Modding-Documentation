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
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Examples: `{ ... }` | 2609 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Examples: `{ ... }` | 2372 ||
| [`stat_mods`](#object-stat_mods) | Object | Examples: `{ ... }` | 13 ||
| [`ability_groups`](#object-ability_groups) | Object | Examples: `{ ... }` | 12 ||
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array | Examples: `[ HogRush Burp SelfMutilate ForceFeed Fartoom Mutilate Sk..., [ Propell Hadou...` | 14 ||
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array | Examples: `[ BasicButcherMelee ], [ BasicDruidAbility ], [ BasicMonkMelee ]` | 14 ||
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array | Examples: `[ int str lck ], [ con str lck ], [ cha int str ]` | 14 ||
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array | Examples: `[ Putrefy NeverFull MainCourse FreshMeat Masochist Glutto..., [ SafeSwitching...` | 14 ||
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array | Examples: `[ SummonSquirrel SummonToad Encourage Protection SongOfSp..., [ Succ HogRush ...` | 12 ||
| [`innate_passives`](#object-innate_passives) | Object | Examples: `{ ... }` | 4 ||
| [`complicated_abilities`](./Arrays.md#array-complicated_abilities) | Array | Examples: `[ FalconPunch Exert Challenge Stoopzerk Grapple ThinkTooH..., [ DealWithTheDe...` | 6 ||
| [`complicated_passives`](./Arrays.md#array-complicated_passives) | Array | Examples: `[ ElementalAttunement LatentEnergy MagicGuru One Two Four..., [ ShoulderCheck...` | 6 ||
| [`innate_items`](#object-innate_items) | Object | Examples: `{ ... }` | 2 ||
| [`move_pool`](./Arrays.md#array-move_pool) | Array | Examples: `[ DefaultMove ]` | 1 ||
| [`tutorial_levelup_active_pool`](./Arrays.md#array-tutorial_levelup_active_pool) | Array | Examples: `[ Block LickHeal Dump ]` | 1 ||
| [`tutorial_levelup_active_pool_2`](./Arrays.md#array-tutorial_levelup_active_pool_2) | Array | Examples: `[ GainThorns ButtScoot Burst HireHitman ]` | 1 ||
| [`tutorial_levelup_passive_pool`](./Arrays.md#array-tutorial_levelup_passive_pool) | Array | Examples: `[ Furious PressurePoints LateBloomer ZenkaiBoost ]` | 1 ||

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
| `palette` | Enum / Integer || 34 ||
| [`portrait_face`](./Enums.md#enum-portrait_face) | Enum || 13 ||
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array || 47 ||
| [`default_face`](./Enums.md#enum-default_face) | Enum || 1 ||
| `hud_palette` | Number || 1 ||

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
| [`name`](./Strings.md#string-name) | Enum | Examples: `"CAT_CLASS_MONK_NAME", "CAT_CLASS_BUTCHER_NAME", "CAT_CLASS_DRUID_NAME"` | 1611 ||
| [`description`](./Strings.md#string-description) | String | Examples: `"CAT_CLASS_DRUID_DESC", "CAT_CLASS_MONK_DESC", "CAT_CLASS_BUTCHER_DESC"` | 14 ||

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
| `con` | Enum / Integer | Examples: `3, 2, -2` | 9 ||
| `cha` | Enum / Integer | Examples: `3, 2, -1` | 7 ||
| `int` | Enum / Integer | Examples: `4, 2, 1` | 6 ||
| `spd` | Enum / Integer | Examples: `1, -1, -2` | 6 ||
| `str` | Enum / Integer | Examples: `2, -1, -2` | 6 ||
| `dex` | Enum / Integer | Examples: `3, -1` | 4 ||
| `lck` | Enum / Integer | Examples: `2, -1, 1` | 4 ||

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
| [`attack`](./Arrays.md#array-attack) | Enum | Examples: `[ Fartoom Mutilate SkullBash Shred Chomp BodySlam SliceAn..., [ SquirrelSquad...` | 12 ||
| [`misc`](./Arrays.md#array-misc) | Array | Examples: `[ SelfMutilate Succ Consume BloodMagic SmellBlood Vurp Li..., [ StoneFists Br...` | 12 ||
| [`move`](./Arrays.md#array-move) | Enum | Examples: `[ DruidSwap FlowerFeet ThornyFeet RaccoonForm HydroPump C..., [ HogRush Trudg...` | 12 ||
| [`defense`](./Arrays.md#array-defense) | Array | Examples: `[ SongOfSpring SummonTurtle PullToSafety Protection Safet..., [ Burp ForceFee...` | 10 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`MonkStances`](./Arrays.md#array-monkstances) | Array | Examples: `[ BasicMonkMelee BasicMonkRanged ]` | 1 ||
| [`AddStartingMana`](./Enums.md) | Integer || 1 | 5 |
| [`SpawnOnBattleStart`](./Enums.md) | Enum || 1 | Crow |
| [`TinkererBasicAttackSwitching`](#object-tinkererbasicattackswitching) | Object || 1 ||

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
| [`weapon`](./Enums.md#enum-weapon) | Enum | Examples: `MonkFist, ButcherHook` | 2 ||
| [`trinket`](./Enums.md#enum-trinket) | Enum | Examples: `MonkStyleChanger` | 1 ||

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
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum | Examples: `TinkererCraft` | 3 ||
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum | Examples: `TinkererThrow` | 3 ||

</details>

---

