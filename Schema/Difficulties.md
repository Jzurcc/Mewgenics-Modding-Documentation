# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Difficulties

> **Associated Files:** `data/difficulties.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 206 |
| [`easy`](#object-easy) | Object |  | 8 |
| [`hard`](#object-hard) | Object |  | 8 |
| `bonus_itemroll_luck` | Integer |  | 8 |
| `boss_health_multiplier` | Float |  | 8 |
| `coins_multiplier` | Float |  | 8 |
| `event_difficulty` | Integer |  | 8 |
| `food_multiplier` | Float |  | 8 |
| `wallet_size` | Integer |  | 8 |
| `boss_elite_buffs` | Integer |  | 7 |

</details>

---

### Object: `easy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `champ_budget` | Float |  | 8 |
| `elite_budget` | Integer |  | 8 |
| `elite_buffs` | Integer |  | 8 |
| `rare_elite_buffs` | Integer |  | 8 |
| `champ_chance_mini` | Float |  | 7 |
| `elite_chance_mini` | Float |  | 6 |

</details>

---

### Object: `hard`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `champ_budget` | Float |  | 8 |
| `champ_chance_mini` | Float |  | 8 |
| `elite_buffs` | Integer |  | 8 |
| `rare_elite_buffs` | Integer |  | 8 |
| `elite_budget` | Integer |  | 7 |
| `elite_chance_mini` | Float |  | 7 |

</details>

---

