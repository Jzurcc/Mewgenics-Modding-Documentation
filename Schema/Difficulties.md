# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Difficulties

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| `bonus_itemroll_luck` | Number |  | 8 |
| `boss_health_multiplier` | Number |  | 8 |
| `coins_multiplier` | Number |  | 8 |
| [`easy`](./Difficulties.md#context-easy) | Block |  | 8 |
| `event_difficulty` | Number |  | 8 |
| `food_multiplier` | Number |  | 8 |
| [`hard`](./Difficulties.md#context-hard) | Block |  | 8 |
| `wallet_size` | Number |  | 8 |
| `boss_elite_buffs` | Number |  | 7 |

</details>

---

### Context: `easy`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Difficulties.md#context-root)

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| `champ_budget` | Number |  | 8 |
| `elite_budget` | Number |  | 8 |
| `elite_buffs` | Number |  | 8 |
| `rare_elite_buffs` | Number |  | 8 |
| [`champ_chance_mini`](./Enums.md#enum-champ_chance_mini) | Enum/String |  | 7 |
| [`elite_chance_mini`](./Enums.md#enum-elite_chance_mini) | Enum/String |  | 6 |

</details>

---

### Context: `hard`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Difficulties.md#context-root)

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| `champ_budget` | Number |  | 8 |
| [`champ_chance_mini`](./Enums.md#enum-champ_chance_mini) | Enum/String |  | 8 |
| `elite_buffs` | Number |  | 8 |
| `rare_elite_buffs` | Number |  | 8 |
| `elite_budget` | Number |  | 7 |
| [`elite_chance_mini`](./Enums.md#enum-elite_chance_mini) | Enum/String |  | 7 |

</details>

---

