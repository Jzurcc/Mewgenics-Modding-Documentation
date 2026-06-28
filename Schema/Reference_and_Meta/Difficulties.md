---
title: "Difficulties Schema"
description: "Scaling multipliers across game difficulty settings."
---

# Difficulties Schema

## Overview
> [!NOTE]
> This schema lists the modifiers that are applied to the engine based on the difficulty tier the player selected.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
easy {
		elite_budget 0
		champ_budget 0

		elite_buffs 1
		rare_elite_buffs 1
	}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Difficulties.md`](../../Directory/System_and_Engine/Difficulties.md)

---

> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see AUDIT_GAPS.md. For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Difficulties

> **Associated Files:** `data/difficulties.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`easy`](./Difficulties.md#object-easy) | Object  | Configuration for easy difficulty, including elite/champ budgets and rewards. | 8 | `{ . . . }` |
| [`hard`](./Difficulties.md#object-hard) | Object  | Configuration for hard difficulty, including elite/champ budgets and rewards. | 8 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `easy`


**Definition:** Configuration for easy difficulty, including elite/champ budgets and rewards.  
**Total Count:** 67

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Difficulties.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---
### Object: `hard`


**Definition:** Configuration for hard difficulty, including elite/champ budgets and rewards.  
**Total Count:** 47

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Difficulties.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---

