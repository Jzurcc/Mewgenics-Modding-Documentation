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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1549 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 206 |
| `icon_frame` | Integer |  | 128 |
| `value` | Float |  | 485 |
| `unique` | Boolean |  | 72 |
| `specific_chapter` | Integer |  | 16 |
| [`minion_alt`](./Enums.md#enum-minion_alt) | Enum |  | 10 |
| `rollable` | Boolean |  | 10 |
| `only_at_battle_start` | Boolean |  | 4 |
| `requires_corpse` | Boolean |  | 4 |
| `roll_limit` | Integer |  | 4 |

</details>

---

### Object: `passives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2805

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 2609 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 173 |

</details>

---

### Object: `StatusEachRoundBegin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 8 |

</details>

---

### Object: `effects`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2166

> **Referenced by:** [`DamageNeighborsAfterMove`](#object-damageneighborsaftermove), [`MeleeRevengeDamage`](#object-meleerevengedamage), [`RevengeDamage`](#object-revengedamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1886 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 59 |
</details>

---

### Object: `DepressionAura`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `aura_effects_allies` | Boolean |  | 8 |
| `range` | Integer |  | 8 |
| `stacks` | Integer |  | 8 |

</details>

---

### Object: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 73

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 49 |
| `knockback` | Integer |  | 48 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |

</details>

---

### Object: `ChanceToRevive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`statuses`](#object-statuses) | Object |  | 6 |
| `health` | Integer |  | 8 |
| `stacks` | Integer |  | 10 |

</details>

---

### Object: `DamageNeighborsAfterMove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 18 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum |  | 8 |
| `damage` | Integer |  | 8 |

</details>

---

### Object: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 31

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 10 |

</details>

---

### Object: `SpawnOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 38

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 72 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum |  | 4 |

</details>

---

### Object: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 57

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
</details>

---

### Object: `statuses`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 14

> **Referenced by:** [`ChanceToRevive`](#object-chancetorevive)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
 | `Zombie` | Number |  | 2 | 
</details> 

---

### Object: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 248

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
</details>

---

### Object: `ReflectProjectiles`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1 |
</details>

---

### Object: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
</details>

---

### Object: `StatusOnEnemyCastSpell`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1 |

</details>

---

### Object: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 40

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
</details>

---

