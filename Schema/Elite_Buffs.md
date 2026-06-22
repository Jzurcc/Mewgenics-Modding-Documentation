# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Elite Buffs

> **Associated Files:** `data/elite_buffs.gon, data/boss_elite_buffs.gon`


### Context: `ROOT` (54 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  | 54 |
| [`passives`](./Elite_Buffs.md#context-passives) | Block |  | 54 |
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

### Context: `passives` (54 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Elite_Buffs.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |
| [`MeleeRevengeDamage`](./Elite_Buffs.md#context-meleerevengedamage) | Block |  | 3 |
| [`RevengeDamage`](./Elite_Buffs.md#context-revengedamage) | Block |  | 2 |
| [`StatusEachTurnEnd`](./Elite_Buffs.md#context-statuseachturnend) | Block |  | 2 |
| [`AddStatusToBasicAttack`](./Elite_Buffs.md#context-addstatustobasicattack) | Block |  | 1 |
| [`StatusEachRoundEnd`](./Elite_Buffs.md#context-statuseachroundend) | Block |  | 1 |
| [`StatusOnDie`](./Elite_Buffs.md#context-statusondie) | Block |  | 1 |
| [`StatusOnKill`](./Elite_Buffs.md#context-statusonkill) | Block |  | 1 |

</details>

---

### Context: `StatusEachRoundBegin` (8 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `NonStackingShield` | Number |  | 8 |

</details>

---

### Context: `effects` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborsAfterMove`](./Elite_Buffs.md#context-damageneighborsaftermove), [`MeleeRevengeDamage`](./Elite_Buffs.md#context-meleerevengedamage), [`RevengeDamage`](./Elite_Buffs.md#context-revengedamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
</details>

---

### Context: `DepressionAura` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `aura_effects_allies` | Boolean |  | 4 |
| `range` | Number |  | 4 |
| `stacks` | Number |  | 4 |

</details>

---

### Context: `MeleeRevengeDamage` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| `knockback` | Number |  | 2 |
| [`effects`](./Elite_Buffs.md#context-effects) | Block |  | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |

</details>

---

### Context: `ChanceToRevive` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 2 |
| `stacks` | Number |  | 2 |
| [`statuses`](./Elite_Buffs.md#context-statuses) | Block |  | 2 |

</details>

---

### Context: `DamageNeighborsAfterMove` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number |  | 2 |
| [`effects`](./Elite_Buffs.md#context-effects) | Block |  | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum |  | 2 |

</details>

---

### Context: `RevengeDamage` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| [`effects`](./Elite_Buffs.md#context-effects) | Block |  | 2 |

</details>

---

### Context: `SpawnOnBattleStart` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum |  | 2 |

</details>

---

### Context: `StatusEachTurnEnd` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `statuses` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChanceToRevive`](./Elite_Buffs.md#context-chancetorevive)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `AddStatusToBasicAttack` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `ReflectProjectiles` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `self_damage` | Number |  | 1 |

</details>

---

### Context: `StatusEachRoundEnd` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnDie` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnEnemyCastSpell` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number |  | 1 |
| `HealthGain` | Number |  | 1 |

</details>

---

### Context: `StatusOnKill` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

