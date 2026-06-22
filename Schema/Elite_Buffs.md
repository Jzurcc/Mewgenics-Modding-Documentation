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
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| `icon_frame` | Number |  | 54 |
| [`passives`](#context-passives) | Block |  | 54 |
| `value` | Number |  | 54 |
| `unique` | Boolean |  | 36 |
| `specific_chapter` | Number |  | 8 |
| [`minion_alt`](./Enums.md#enum-minion_alt) | Enum |  | 5 |
| `rollable` | Boolean |  | 5 |
| `only_at_battle_start` | Boolean |  | 2 |
| `requires_corpse` | Boolean |  | 2 |
| `roll_limit` | Number |  | 2 |

</details>

---

### Context: `passives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 54

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`MeleeRevengeDamage`](#context-meleerevengedamage) | Block |  | 3 |
| [`RevengeDamage`](#context-revengedamage) | Block |  | 2 |
| [`StatusEachTurnEnd`](#context-statuseachturnend) | Block |  | 2 |
| [`AddStatusToBasicAttack`](#context-addstatustobasicattack) | Block |  | 1 |
| [`StatusEachRoundEnd`](#context-statuseachroundend) | Block |  | 1 |
| [`StatusOnDie`](#context-statusondie) | Block |  | 1 |
| [`StatusOnKill`](#context-statusonkill) | Block |  | 1 |

</details>

---

### Context: `StatusEachRoundBegin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `NonStackingShield` | Number |  | 8 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`DamageNeighborsAfterMove`](#context-damageneighborsaftermove), [`MeleeRevengeDamage`](#context-meleerevengedamage), [`RevengeDamage`](#context-revengedamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`{Global Modifiers}`](./Engine_GlobalModifiers.md#all-confirmed-global-modifier-id-values) | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |  |
| [`{Global Modifiers}`](./Engine_GlobalModifiers.md#all-confirmed-global-modifier-id-values) | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |  |
| [`{Global Modifiers}`](./Engine_GlobalModifiers.md#all-confirmed-global-modifier-id-values) | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |  |
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
| `range` | Number |  | 4 |
| `stacks` | Number |  | 4 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `knockback` | Number |  | 2 |
| [`effects`](#context-effects) | Block |  | 1 |
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
| `health` | Number |  | 2 |
| `stacks` | Number |  | 2 |
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
| `damage` | Number |  | 2 |
| [`effects`](#context-effects) | Block |  | 2 |
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
| [`effects`](#context-effects) | Block |  | 2 |

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
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `statuses`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ChanceToRevive`](#context-chancetorevive)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
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
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `ReflectProjectiles`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `self_damage` | Number |  | 1 |

</details>

---

### Context: `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnEnemyCastSpell`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AllStatsUp` | Number |  | 1 |
| `HealthGain` | Number |  | 1 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

