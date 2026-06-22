# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** Some keys labeled as `Number` actually support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Difficulties

> **Associated Files:** `data/difficulties.gon`


### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
| `bonus_itemroll_luck` | Number |  | 8 |
| `boss_health_multiplier` | Number |  | 8 |
| `coins_multiplier` | Number |  | 8 |
| [`easy`](#context-easy) | Block |  | 8 |
| `event_difficulty` | Number |  | 8 |
| `food_multiplier` | Number |  | 8 |
| [`hard`](#context-hard) | Block |  | 8 |
| `wallet_size` | Number |  | 8 |
| `boss_elite_buffs` | Number |  | 7 |

</details>

---

### Context: `easy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `champ_budget` | Number |  | 8 |
| `elite_budget` | Number |  | 8 |
| `elite_buffs` | Number |  | 8 |
| `rare_elite_buffs` | Number |  | 8 |
| [`champ_chance_mini`](./Enums.md#enum-champ_chance_mini) | Enum |  | 7 |
| [`elite_chance_mini`](./Enums.md#enum-elite_chance_mini) | Enum |  | 6 |

</details>

---

### Context: `hard`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `champ_budget` | Number |  | 8 |
| [`champ_chance_mini`](./Enums.md#enum-champ_chance_mini) | Enum |  | 8 |
| `elite_buffs` | Number |  | 8 |
| `rare_elite_buffs` | Number |  | 8 |
| `elite_budget` | Number |  | 7 |
| [`elite_chance_mini`](./Enums.md#enum-elite_chance_mini) | Enum |  | 7 |

</details>

---

