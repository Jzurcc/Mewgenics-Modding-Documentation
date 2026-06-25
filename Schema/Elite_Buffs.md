# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


## Elite Buffs

> **Associated Files:** `data/elite_buffs.gon, data/boss_elite_buffs.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 54

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `value` | Float |  | 485 |
| `icon_frame` | Integer |  | 128 |
| `unique` | Boolean |  | 72 |
| `specific_chapter` | Integer |  | 16 |
| [`minion_alt`](./Enums.md#enum-minion_alt) | Enum |  | 10 |
| `rollable` | Boolean |  | 10 |
| `only_at_battle_start` | Boolean |  | 4 |
| `requires_corpse` | Boolean |  | 4 |
| `roll_limit` | Integer |  | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |

</details>

---

### Object: `passives`


**Definition:** Object listing intrinsic passive modifiers.  
**Total Count:** 2805


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |

</details>

---

### Object: `effects`


**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 2166


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`DamageNeighborsAfterMove`](#object-damageneighborsaftermove), [`MeleeRevengeDamage`](#object-meleerevengedamage), [`RevengeDamage`](#object-revengedamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
</details>

---

### Object: `AddStatusToBasicAttack`


**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 248


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
</details>

---

### Object: `MeleeRevengeDamage`


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 73


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `knockback` | Integer |  | 48 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |

</details>

---

### Object: `StatusEachTurnEnd`


**Definition:** Applies or references the 'StatusEachTurnEnd' effect/state.  
**Total Count:** 57


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
</details>

---

### Object: `StatusOnKill`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 40


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
</details>

---


<details>
<summary><b>AddStatusToBasicAttack</b></summary>

> **Total Count:** 187

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 187 |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>StatusEachTurnEnd</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>StatusOnDie</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 6 |

</details>

<details>
<summary><b>StatusOnKill</b></summary>

> **Total Count:** 36

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 36 |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

### Object: `SpawnOnBattleStart`


**Definition:** No definition provided.  
**Total Count:** 38


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 72 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum |  | 4 |

</details>

---

### Object: `RevengeDamage`


**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 31


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |

</details>

---

### Object: `statuses`


**Definition:** Status effects possessed by the character.  
**Total Count:** 14


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ChanceToRevive`](#object-chancetorevive)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
 | `Zombie` | Number |  | 2 | 
</details> 

---

### Object: `StatusOnDie`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
</details>

---

### Object: `ReflectProjectiles`


**Definition:** No definition provided.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusEachRoundBegin`


**Definition:** Examples: `{ ... }`  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |

</details>

---

### Object: `ChanceToRevive`


**Definition:** No definition provided.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Integer |  | 10 |
| `health` | Integer |  | 8 |
| [`statuses`](#object-statuses) | Object |  | 6 |

</details>

---

### Object: `DepressionAura`


**Definition:** Examples: `1`  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `aura_effects_allies` | Boolean |  | 8 |
| `range` | Integer |  | 8 |
| `stacks` | Integer |  | 8 |

</details>

---

### Object: `DamageNeighborsAfterMove`


**Definition:** Examples: `{ ... }`  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer |  | 8 |
| [`type`](./Enums.md#enum-type) | Enum |  | 8 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |

</details>

---

### Object: `StatusEachRoundEnd`


**Definition:** Applies or references the 'StatusEachRoundEnd' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
</details>

---

### Object: `StatusOnEnemyCastSpell`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |

</details>

---
