# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


## Elite Buffs

> **Associated Files:** `data/elite_buffs.gon, data/boss_elite_buffs.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 54

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 2985 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 291 |  |
| `icon_frame` | Integer |  | 74 |  |
| `value` | Float |  | 54 |  |
| `unique` | Boolean |  | 36 |  |
| `specific_chapter` | Integer |  | 8 |  |
| [`minion_alt`](./Enums.md#enum-minion_alt) | Enum |  | 5 |  |
| `rollable` | Boolean |  | 5 |  |
| `only_at_battle_start` | Boolean |  | 2 |  |
| `requires_corpse` | Boolean |  | 2 |  |
| `roll_limit` | Integer |  | 2 |  |

</details>

---

### Object: `passives`


**Definition:** Object listing intrinsic passive modifiers.  
**Total Count:** 2805


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 2039 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |  |

</details>

---

### Object: `effects`


**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 2166


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`DamageNeighborsAfterMove`](#object-damageneighborsaftermove), [`MeleeRevengeDamage`](#object-meleerevengedamage), [`RevengeDamage`](#object-revengedamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 750 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |  |
</details>

---

### Object: `AddStatusToBasicAttack`


**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 248


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
</details>

---

### Object: `MeleeRevengeDamage`


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 73


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 70 |  |
| `knockback` | Enum / Integer |  | 24 |  |
| [`elements`](./Arrays.md#array-elements) | Array |  | 10 |  |

</details>

---

### Object: `StatusEachTurnEnd`


**Definition:** Applies or references the 'StatusEachTurnEnd' effect/state.  
**Total Count:** 57


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
</details>

---

### Object: `StatusOnKill`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 40


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
</details>

---


<details>
<summary><b>AddStatusToBasicAttack</b></summary>

> **Total Count:** 187

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 34 |  |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |  |

</details>

<details>
<summary><b>StatusEachTurnEnd</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |  |

</details>

<details>
<summary><b>StatusOnDie</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 34 |  |

</details>

<details>
<summary><b>StatusOnKill</b></summary>

> **Total Count:** 36

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 34 |  |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |  |

</details>

### Object: `SpawnOnBattleStart`


**Definition:** No definition provided.  
**Total Count:** 38


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum |  | 38 |  |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum |  | 2 |  |

</details>

---

### Object: `RevengeDamage`


**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 31


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 31 |  |

</details>

---

### Object: `statuses`


**Definition:** Status effects possessed by the character.  
**Total Count:** 14


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ChanceToRevive`](#object-chancetorevive)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Zombie` | Number |  | 2 |  |
</details> 

---

### Object: `StatusOnDie`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
</details>

---

### Object: `ReflectProjectiles`


**Definition:** No definition provided.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusEachRoundBegin`


**Definition:** Examples: `{ ... }`  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 8 |  |

</details>

---

### Object: `ChanceToRevive`


**Definition:** No definition provided.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer |  | 5 |  |
| `health` | Integer |  | 4 |  |
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object || 3 ||

</details>

---

### Object: `DepressionAura`


**Definition:** Examples: `1`  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `aura_effects_allies` | Boolean || 4 ||
| `range` | Enum / Integer || 4 ||
| `stacks` | Enum / Integer || 4 ||

</details>

---

### Object: `DamageNeighborsAfterMove`


**Definition:** Examples: `{ ... }`  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object || 4 ||
| [`type`](./Enums.md#enum-type) | Enum || 4 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 4 ||
| [`elements`](./Arrays.md#array-elements) | Array || 4 ||

</details>

---

### Object: `StatusEachRoundEnd`


**Definition:** Applies or references the 'StatusEachRoundEnd' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||
</details>

---

### Object: `StatusOnEnemyCastSpell`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 1 ||

</details>

---
