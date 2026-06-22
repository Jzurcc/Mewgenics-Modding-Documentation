# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Difficulties

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `bonus_itemroll_luck` | Number | `8, 0, 16` |  |
| `boss_health_multiplier` | Number | `1.4, 1, 1.2` |  |
| `coins_multiplier` | Number | `1, 1.5, 1.25` |  |
| `easy` | [`Block`](./Difficulties.md#context-easy) | `{ ... }` |  |
| `event_difficulty` | Number | `1, 2, 0` |  |
| `food_multiplier` | Number | `1, 1.5, 1.25` |  |
| `hard` | [`Block`](./Difficulties.md#context-hard) | `{ ... }` |  |
| `wallet_size` | Number | `99` |  |
| `boss_elite_buffs` | Number | `2, 1, 3` |  |

</details>

---

### Context: `hard`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Difficulties.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `champ_budget` | Number | `2, 1, 1.5` |  |
| `champ_chance_mini` | Number | `1, .5, .25` |  |
| `elite_buffs` | Number | `2, 1, 3` |  |
| `rare_elite_buffs` | Number | `2, 1, 3` |  |
| `elite_budget` | Number | `2, 1, 3` |  |
| `elite_chance_mini` | Number | `1, .5, .25` |  |

</details>

---

### Context: `easy`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Difficulties.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `champ_budget` | Number | `1, 0, 999` |  |
| `elite_budget` | Number | `1, 2, 0` |  |
| `elite_buffs` | Number | `2, 1, 3` |  |
| `rare_elite_buffs` | Number | `2, 1, 3` |  |
| `champ_chance_mini` | Number | `1, .5, .25` |  |
| `elite_chance_mini` | Number | `1, .5, .25` |  |

</details>

---

