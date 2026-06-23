# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Elite Buffs

> **Associated Files:** `data/elite_buffs.gon, data/boss_elite_buffs.gon`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 54

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 206 |
| `icon_frame` | Integer |  | 54 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1549 |
| `value` | Float |  | 54 |
| `unique` | Boolean |  | 36 |
| `specific_chapter` | Integer |  | 8 |
| [`minion_alt`](./Enums.md#enum-minion_alt) | Enum |  | 5 |
| `rollable` | Boolean |  | 5 |
| `only_at_battle_start` | Boolean |  | 2 |
| `requires_corpse` | Boolean |  | 2 |
| `roll_limit` | Integer |  | 2 |

</details>

---

### Context: `passives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 54

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 173 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2609 |

</details>

---

### Context: `StatusEachRoundBegin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

</details>

---

### Context: `effects`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`DamageNeighborsAfterMove`](#context-damageneighborsaftermove), [`MeleeRevengeDamage`](#context-meleerevengedamage), [`RevengeDamage`](#context-revengedamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1886 |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 59 |
</details>

---

### Context: `DepressionAura`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `aura_effects_allies` | Boolean |  | 4 |
| `range` | Integer |  | 4 |
| `stacks` | Integer |  | 4 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 36 |
| `knockback` | Integer |  | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |

</details>

---

### Context: `ChanceToRevive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Integer |  | 2 |
| `stacks` | Integer |  | 2 |
| [`statuses`](#context-statuses) | Block |  | 2 |

</details>

---

### Context: `DamageNeighborsAfterMove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer |  | 2 |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum |  | 2 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 10 |

</details>

---

### Context: `SpawnOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum |  | 2 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |
</details>

---

### Context: `statuses`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ChanceToRevive`](#context-chancetorevive)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |
</details>
 | `Zombie` | Number |  | 2 | 

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |
</details>

---

### Context: `ReflectProjectiles`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 8 |

</details>

---

### Context: `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |
</details>

---

### Context: `StatusOnEnemyCastSpell`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |
</details>

---

