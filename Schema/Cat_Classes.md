# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Cat Classes

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/14) |
| :--- | :--- | :--- | :--- |
| [`ability_pool`](./Arrays.md#array-ability_pool) | Array |  | 14 |
| [`attack_pool`](./Arrays.md#array-attack_pool) | Array |  | 14 |
| [`graphics`](./Cat_Classes.md#context-graphics) | Block |  | 14 |
| [`levelup_stats`](./Arrays.md#array-levelup_stats) | Array |  | 14 |
| [`meta`](./Cat_Classes.md#context-meta) | Block |  | 14 |
| [`passive_pool`](./Arrays.md#array-passive_pool) | Array |  | 14 |
| [`stat_mods`](./Cat_Classes.md#context-stat_mods) | Block |  | 13 |
| [`ability_groups`](./Cat_Classes.md#context-ability_groups) | Block |  | 12 |
| [`starter_abilities`](./Arrays.md#array-starter_abilities) | Array |  | 12 |
| [`complicated_abilities`](./Arrays.md#array-complicated_abilities) | Array |  | 6 |
| [`complicated_passives`](./Arrays.md#array-complicated_passives) | Array |  | 6 |
| [`innate_passives`](./Cat_Classes.md#context-innate_passives) | Block |  | 4 |
| [`innate_items`](./Cat_Classes.md#context-innate_items) | Block |  | 2 |
| [`move_pool`](./Arrays.md#array-move_pool) | Array |  | 1 |
| [`tutorial_levelup_active_pool`](./Arrays.md#array-tutorial_levelup_active_pool) | Array |  | 1 |
| [`tutorial_levelup_active_pool_2`](./Arrays.md#array-tutorial_levelup_active_pool_2) | Array |  | 1 |
| [`tutorial_levelup_passive_pool`](./Arrays.md#array-tutorial_levelup_passive_pool) | Array |  | 1 |

</details>

---

### Context: `graphics`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Definition | Count (X/14) |
| :--- | :--- | :--- | :--- |
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array |  | 14 |
| `palette` | Number |  | 13 |
| [`portrait_face`](./Enums.md#enum-portrait_face) | Enum/String |  | 13 |
| [`default_face`](./Enums.md#enum-default_face) | Enum/String |  | 1 |
| `hud_palette` | Number |  | 1 |

</details>

---

### Context: `meta`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Definition | Count (X/14) |
| :--- | :--- | :--- | :--- |
| `description` | String |  | 14 |
| `name` | String |  | 14 |

</details>

---

### Context: `ability_groups`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`attack`](./Arrays.md#array-attack) | Array |  | 12 |
| [`misc`](./Arrays.md#array-misc) | Array |  | 12 |
| [`move`](./Arrays.md#array-move) | Array |  | 12 |
| [`defense`](./Arrays.md#array-defense) | Array |  | 10 |

</details>

---

### Context: `stat_mods`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Definition | Count (X/9) |
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

### Context: `innate_items`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`weapon`](./Enums.md#enum-weapon) | Enum/String |  | 2 |
| [`trinket`](./Enums.md#enum-trinket) | Enum/String |  | 1 |

</details>

---

### Context: `TinkererBasicAttackSwitching`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`innate_passives`](./Cat_Classes.md#context-innate_passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum/String |  | 1 |
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum/String |  | 1 |

</details>

---

### Context: `innate_passives`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AddStartingMana` | Number |  | 1 |
| [`MonkStances`](./Arrays.md#array-monkstances) | Array |  | 1 |
| [`SpawnOnBattleStart`](./Enums.md#enum-spawnonbattlestart) | Enum/String |  | 1 |
| [`TinkererBasicAttackSwitching`](./Cat_Classes.md#context-tinkererbasicattackswitching) | Block |  | 1 |

</details>

---

