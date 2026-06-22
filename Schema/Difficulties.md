# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Difficulties

> **Associated Files:** `data/difficulties.gon`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| `bonus_itemroll_luck` | Integer |  | 8 |
| `boss_health_multiplier` | Float |  | 8 |
| `coins_multiplier` | Float |  | 8 |
| [`easy`](#context-easy) | Block |  | 8 |
| `event_difficulty` | Integer |  | 8 |
| `food_multiplier` | Float |  | 8 |
| [`hard`](#context-hard) | Block |  | 8 |
| `wallet_size` | Integer |  | 8 |
| `boss_elite_buffs` | Integer |  | 7 |

</details>

---

### Context: `easy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `champ_budget` | Float |  | 8 |
| `elite_budget` | Integer |  | 8 |
| `elite_buffs` | Integer |  | 8 |
| `rare_elite_buffs` | Integer |  | 8 |
| `champ_chance_mini` | Float |  | 7 |
| `elite_chance_mini` | Float |  | 6 |

</details>

---

### Context: `hard`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `champ_budget` | Float |  | 8 |
| `champ_chance_mini` | Float |  | 8 |
| `elite_buffs` | Integer |  | 8 |
| `rare_elite_buffs` | Integer |  | 8 |
| `elite_budget` | Integer |  | 7 |
| `elite_chance_mini` | Float |  | 7 |

</details>

---

