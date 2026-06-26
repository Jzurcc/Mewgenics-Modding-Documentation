# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


## Difficulties

> **Associated Files:** `data/difficulties.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 206 |  |
| [`hard`](Combat_Rewards.md#object-hard) | Object || 42 ||
| `bonus_itemroll_luck` | Integer || 16 ||
| `boss_health_multiplier` | Float || 16 ||
| `coins_multiplier` | Float || 16 ||
| [`easy`](#object-easy) | Object || 16 ||
| `event_difficulty` | Integer || 16 ||
| `food_multiplier` | Float || 16 ||
| `wallet_size` | Integer || 16 ||
| `boss_elite_buffs` | Integer || 14 ||

</details>

---

### Object: `hard`


**Definition:** No definition provided.  
**Total Count:** 21


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `champ_budget` | Float || 16 ||
| `champ_chance_mini` | Float || 16 ||
| `elite_buffs` | Integer || 16 ||
| `rare_elite_buffs` | Integer || 16 ||
| `elite_budget` | Integer || 14 ||
| `elite_chance_mini` | Float || 14 ||

</details>

---


### Object: `easy`


**Definition:** No definition provided.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `champ_budget` | Float || 16 ||
| `elite_budget` | Integer || 16 ||
| `elite_buffs` | Integer || 16 ||
| `rare_elite_buffs` | Integer || 16 ||
| `champ_chance_mini` | Float || 14 ||
| `elite_chance_mini` | Float || 12 ||

</details>

---
