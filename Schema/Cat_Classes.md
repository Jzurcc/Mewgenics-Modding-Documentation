# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** Some keys labeled as `Number` actually support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Cat Classes

> **Associated Files:** `data/classes/`


### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 14

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array |  | 14 |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array |  | 14 |
| [`graphics`](#context-graphics) | Block |  | 14 |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array |  | 14 |
| [`meta`](#context-meta) | Block |  | 14 |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array |  | 14 |
| [`stat_mods`](#context-stat_mods) | Block |  | 13 |
| [`ability_groups`](#context-ability_groups) | Block |  | 12 |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array |  | 12 |
| [`complicated_abilities`](./Arrays.md#array-complicated_abilities) | Array |  | 6 |
| [`complicated_passives`](./Arrays.md#array-complicated_passives) | Array |  | 6 |
| [`innate_passives`](#context-innate_passives) | Block |  | 4 |
| [`innate_items`](#context-innate_items) | Block |  | 2 |
| [`move_pool`](./Arrays.md#array-move_pool) | Array |  | 1 |
| [`tutorial_levelup_active_pool`](./Arrays.md#array-tutorial_levelup_active_pool) | Array |  | 1 |
| [`tutorial_levelup_active_pool_2`](./Arrays.md#array-tutorial_levelup_active_pool_2) | Array |  | 1 |
| [`tutorial_levelup_passive_pool`](./Arrays.md#array-tutorial_levelup_passive_pool) | Array |  | 1 |

</details>

---

### Context: `graphics`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 14

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Graphic Blocks}`](./Engine_Graphics.md) | Block | **(Supports Multiple)** A visual/animation configuration. See Engine_Graphics.md. |  |
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array |  | 14 |
| `palette` | Number |  | 13 |
| [`portrait_face`](./Enums.md#enum-portrait_face) | Enum |  | 13 |
| [`default_face`](./Enums.md#enum-default_face) | Enum |  | 1 |
| `hud_palette` | Number |  | 1 |

</details>

---

### Context: `meta`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 14

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`description`](./Strings.md#string-description) | String |  | 14 |
| [`name`](./Strings.md#string-name) | String |  | 14 |

</details>

---

### Context: `stat_mods`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 13

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `cha` | Number |  | 7 |
| `int` | Number |  | 6 |
| `spd` | Number |  | 6 |
| `str` | Number |  | 6 |
| `dex` | Number |  | 4 |
| `lck` | Number |  | 4 |

</details>

---

### Context: `ability_groups`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Arrays.md#array-attack) | Array |  | 12 |
| [`misc`](./Arrays.md#array-misc) | Array |  | 12 |
| [`move`](./Arrays.md#array-move) | Array |  | 12 |
| [`defense`](./Arrays.md#array-defense) | Array |  | 10 |

</details>

---

### Context: `innate_passives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddStartingMana` | Number |  | 1 |
| [`MonkStances`](./Arrays.md#array-monkstances) | Array |  | 1 |
| [`SpawnOnBattleStart`](./Enums.md#enum-spawnonbattlestart) | Enum |  | 1 |
| [`TinkererBasicAttackSwitching`](#context-tinkererbasicattackswitching) | Block |  | 1 |

</details>

---

### Context: `innate_items`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weapon`](./Enums.md#enum-weapon) | Enum |  | 2 |
| [`trinket`](./Enums.md#enum-trinket) | Enum |  | 1 |

</details>

---

### Context: `TinkererBasicAttackSwitching`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`innate_passives`](#context-innate_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum |  | 1 |
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum |  | 1 |

</details>

---

