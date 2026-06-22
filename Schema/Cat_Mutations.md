# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Cat Mutations

> **Associated Files:** `data/mutations/`


### Context: `passives` (284 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`-2`](./Cat_Mutations.md#context--2), [`1026`](./Cat_Mutations.md#context-1026), [`1029`](./Cat_Mutations.md#context-1029), [`1500`](./Cat_Mutations.md#context-1500), [`300`](./Cat_Mutations.md#context-300), [`301`](./Cat_Mutations.md#context-301), [`302`](./Cat_Mutations.md#context-302), [`303`](./Cat_Mutations.md#context-303), [`304`](./Cat_Mutations.md#context-304), [`305`](./Cat_Mutations.md#context-305), [`306`](./Cat_Mutations.md#context-306), [`307`](./Cat_Mutations.md#context-307), [`308`](./Cat_Mutations.md#context-308), [`309`](./Cat_Mutations.md#context-309), [`310`](./Cat_Mutations.md#context-310), [`311`](./Cat_Mutations.md#context-311), [`312`](./Cat_Mutations.md#context-312), [`313`](./Cat_Mutations.md#context-313), [`314`](./Cat_Mutations.md#context-314), [`315`](./Cat_Mutations.md#context-315), [`316`](./Cat_Mutations.md#context-316), [`317`](./Cat_Mutations.md#context-317), [`318`](./Cat_Mutations.md#context-318), [`319`](./Cat_Mutations.md#context-319), [`320`](./Cat_Mutations.md#context-320), [`321`](./Cat_Mutations.md#context-321), [`322`](./Cat_Mutations.md#context-322), [`323`](./Cat_Mutations.md#context-323), [`324`](./Cat_Mutations.md#context-324), [`325`](./Cat_Mutations.md#context-325), [`326`](./Cat_Mutations.md#context-326), [`327`](./Cat_Mutations.md#context-327), [`328`](./Cat_Mutations.md#context-328), [`329`](./Cat_Mutations.md#context-329), [`330`](./Cat_Mutations.md#context-330), [`331`](./Cat_Mutations.md#context-331), [`332`](./Cat_Mutations.md#context-332), [`333`](./Cat_Mutations.md#context-333), [`334`](./Cat_Mutations.md#context-334), [`335`](./Cat_Mutations.md#context-335), [`336`](./Cat_Mutations.md#context-336), [`337`](./Cat_Mutations.md#context-337), [`338`](./Cat_Mutations.md#context-338), [`339`](./Cat_Mutations.md#context-339), [`340`](./Cat_Mutations.md#context-340), [`341`](./Cat_Mutations.md#context-341), [`342`](./Cat_Mutations.md#context-342), [`343`](./Cat_Mutations.md#context-343), [`344`](./Cat_Mutations.md#context-344), [`345`](./Cat_Mutations.md#context-345), [`346`](./Cat_Mutations.md#context-346), [`347`](./Cat_Mutations.md#context-347), [`348`](./Cat_Mutations.md#context-348), [`349`](./Cat_Mutations.md#context-349), [`351`](./Cat_Mutations.md#context-351), [`352`](./Cat_Mutations.md#context-352), [`353`](./Cat_Mutations.md#context-353), [`442`](./Cat_Mutations.md#context-442), [`702`](./Cat_Mutations.md#context-702), [`703`](./Cat_Mutations.md#context-703), [`704`](./Cat_Mutations.md#context-704), [`705`](./Cat_Mutations.md#context-705), [`706`](./Cat_Mutations.md#context-706), [`707`](./Cat_Mutations.md#context-707), [`750`](./Cat_Mutations.md#context-750), [`751`](./Cat_Mutations.md#context-751), [`752`](./Cat_Mutations.md#context-752), [`753`](./Cat_Mutations.md#context-753), [`754`](./Cat_Mutations.md#context-754), [`755`](./Cat_Mutations.md#context-755), [`756`](./Cat_Mutations.md#context-756), [`757`](./Cat_Mutations.md#context-757), [`758`](./Cat_Mutations.md#context-758), [`759`](./Cat_Mutations.md#context-759), [`760`](./Cat_Mutations.md#context-760), [`761`](./Cat_Mutations.md#context-761), [`762`](./Cat_Mutations.md#context-762), [`763`](./Cat_Mutations.md#context-763), [`900`](./Cat_Mutations.md#context-900), [`PassiveWhenAffectedByElement`](./Cat_Mutations.md#context-passivewhenaffectedbyelement), [`PassiveWhileHasStatus`](./Cat_Mutations.md#context-passivewhilehasstatus)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |
| [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack) | Block |  | 52 |
| [`PassiveWhenAffectedByElement`](./Cat_Mutations.md#context-passivewhenaffectedbyelement) | Block |  | 12 |
| [`RevengeDamage`](./Cat_Mutations.md#context-revengedamage) | Block |  | 9 |
| [`MeleeRevengeDamage`](./Cat_Mutations.md#context-meleerevengedamage) | Block |  | 7 |
| [`AddStatusToBasicMeleeAttack`](./Cat_Mutations.md#context-addstatustobasicmeleeattack) | Block |  | 6 |
| [`StatusOnTookDamage`](./Cat_Mutations.md#context-statusontookdamage) | Block |  | 6 |
| [`StatusEachTurnBegin`](./Cat_Mutations.md#context-statuseachturnbegin) | Block |  | 5 |
| [`StatusEachTurnEnd`](./Cat_Mutations.md#context-statuseachturnend) | Block |  | 4 |
| [`StatusEveryXSpellCasts`](./Cat_Mutations.md#context-statuseveryxspellcasts) | Block |  | 2 |
| [`StatusKilledCharacters`](./Cat_Mutations.md#context-statuskilledcharacters) | Block |  | 2 |
| [`StatusOnBattleEnd`](./Cat_Mutations.md#context-statusonbattleend) | Block |  | 2 |
| [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove) | Block |  | 2 |
| [`StatusOnTookDamageFromAbility`](./Cat_Mutations.md#context-statusontookdamagefromability) | Block |  | 2 |
| [`PassiveWhenAtFullMana`](./Cat_Mutations.md#context-passivewhenatfullmana) | Block |  | 1 |
| [`PassiveWhileHasStatus`](./Cat_Mutations.md#context-passivewhilehasstatus) | Block |  | 1 |
| [`StatusEachRoundEnd`](./Cat_Mutations.md#context-statuseachroundend) | Block |  | 1 |
| [`StatusIfUnusedMovePoints`](./Cat_Mutations.md#context-statusifunusedmovepoints) | Block |  | 1 |
| [`StatusOnAllyCatDeath`](./Cat_Mutations.md#context-statusonallycatdeath) | Block |  | 1 |
| [`StatusOnCastSpell`](./Cat_Mutations.md#context-statusoncastspell) | Block |  | 1 |
| [`StatusOnDie`](./Cat_Mutations.md#context-statusondie) | Block |  | 1 |
| [`StatusOnEatFood`](./Cat_Mutations.md#context-statusoneatfood) | Block |  | 1 |
| [`StatusOnKill`](./Cat_Mutations.md#context-statusonkill) | Block |  | 1 |

</details>

---

### Context: `AddStatusToBasicAttack` (52 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| [`RandomStatusFromPool`](./Cat_Mutations.md#context-randomstatusfrompool) | Block |  | 1 |

</details>

---

### Context: `PassiveWhenAffectedByElement` (12 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |
| [`element`](./Enums.md#enum-element) | Enum |  | 12 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 12 |

</details>

---

### Context: `effects` (10 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Cat_Mutations.md#context-meleerevengedamage), [`RevengeDamage`](./Cat_Mutations.md#context-revengedamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| [`RandomStatusFromPool`](./Cat_Mutations.md#context-randomstatusfrompool) | Block |  | 1 |

</details>

---

### Context: `RevengeDamage` (9 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| [`effects`](./Cat_Mutations.md#context-effects) | Block |  | 9 |
| `damage` | Number |  | 4 |
| [`type`](./Enums.md#enum-type) | Enum |  | 4 |

</details>

---

### Context: `MeleeRevengeDamage` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| `knockback` | Number |  | 4 |
| `damage` | Number |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum |  | 2 |
| [`effects`](./Cat_Mutations.md#context-effects) | Block |  | 1 |

</details>

---

### Context: `SpawnThingOnDamage` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number |  | 7 |
| [`object`](./Enums.md#enum-object) | Enum |  | 7 |
| `good` | Boolean |  | 5 |

</details>

---

### Context: `AddStatusToBasicMeleeAttack` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |

</details>

---

### Context: `StatusOnTookDamage` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |

</details>

---

### Context: `StatusEachTurnBegin` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |

</details>

---

### Context: `RandomStatusFromPool` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack), [`StatusOnTookDamageFromAbility`](./Cat_Mutations.md#context-statusontookdamagefromability), [`effects`](./Cat_Mutations.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |

</details>

---

### Context: `SpawnEachTurn` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number |  | 4 |
| [`object`](./Enums.md#enum-object) | Enum |  | 4 |
| `good` | Boolean |  | 1 |

</details>

---

### Context: `StatusEachTurnEnd` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 3 |
| `number` | Number |  | 2 |

</details>

---

### Context: `Conditional_RandomChance` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKilledCharacters`](./Cat_Mutations.md#context-statuskilledcharacters)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| `odds` | Number |  | 2 |

</details>

---

### Context: `StatusEveryXSpellCasts` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| `stacks` | Number |  | 2 |

</details>

---

### Context: `StatusKilledCharacters` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Evaluates the nested condition before applying. |  |

</details>

---

### Context: `StatusOnBattleEnd` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |

</details>

---

### Context: `StatusOnEndMove` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Evaluates the nested condition before applying. |  |

</details>

---

### Context: `StatusOnTookDamageFromAbility` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| [`RandomStatusFromPool`](./Cat_Mutations.md#context-randomstatusfrompool) | Block |  | 2 |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum |  | 1 |
| `range` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `AddDamageToElementDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number |  | 1 |
| [`element`](./Enums.md#enum-element) | Enum |  | 1 |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fury` | Number |  | 1 |

</details>

---

### Context: `BackflipWhenTargeted` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum |  | 1 |
| `stacks` | Number |  | 1 |

</details>

---

### Context: `ChanceToBackflip` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum |  | 1 |
| `chance` | Number |  | 1 |

</details>

---

### Context: `ClassManaCostReduction` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`class`](./Enums.md#enum-class) | Enum |  | 1 |
| `reduction` | Number |  | 1 |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |

</details>

---

### Context: `Conditional_GoodRoll` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| `odds` | Number |  | 1 |

</details>

---

### Context: `CounterAttack` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum |  | 1 |
| `chance` | Number |  | 1 |

</details>

---

### Context: `KnockUpAndAway` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicMeleeAttack`](./Cat_Mutations.md#context-addstatustobasicmeleeattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number |  | 1 |
| `stacks` | Number |  | 1 |

</details>

---

### Context: `MoveWhenDamaged` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 1 |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 1 |

</details>

---

### Context: `PassiveWhenAtFullMana` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |

</details>

---

### Context: `PassiveWhileHasStatus` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum |  | 1 |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

### Context: `StatusEachRoundEnd` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |

</details>

---

### Context: `StatusEveryXSpellCastsEachTurn` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number |  | 1 |
| `stacks` | Number |  | 1 |

</details>

---

### Context: `StatusIfDidntMove` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number |  | 1 |

</details>

---

### Context: `StatusIfUnusedMovePoints` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |

</details>

---

### Context: `StatusOnAllyCatDeath` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |

</details>

---

### Context: `StatusOnCastSpell` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |

</details>

---

### Context: `StatusOnDie` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |

</details>

---

### Context: `StatusOnEatFood` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |

</details>

---

### Context: `StatusOnKill` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |

</details>

---

### Numerical Contexts

> The following contexts are numeric keys or array indices.


### Context: `400` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `401` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `402` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `403` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `404` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spd` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `405` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `lck` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `406` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `407` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `dex` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `408` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `con` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `409` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `410` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `411` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `412` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `dex` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `413` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `414` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `dex` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `415` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `416` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `417` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `418` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `419` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `420` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `421` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `422` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `423` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `424` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `con` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `425` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `dex` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `426` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `427` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `428` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `429` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `430` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `431` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `432` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `433` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `434` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `lck` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `435` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `lck` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `436` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `437` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spd` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `438` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `439` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `440` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `441` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `lck` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `700` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |
| `cha` | Number |  | 3 |
| `lck` | Number |  | 3 |
| `con` | Number |  | 1 |
| `int` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `701` (9 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |
| `cha` | Number |  | 3 |
| `dex` | Number |  | 2 |
| `int` | Number |  | 2 |
| `spd` | Number |  | 2 |
| `lck` | Number |  | 1 |
| `shield` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `313` (8 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 8 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 8 |
| `divine_shield` | Number |  | 1 |
| `shield` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `314` (8 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | String |  | 8 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 8 |
| `cha` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `315` (8 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 8 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 8 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `704` (8 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 8 |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| `cha` | Number |  | 2 |
| `str` | Number |  | 2 |
| `con` | Number |  | 1 |
| `lck` | Number |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `309` (7 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 7 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 7 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 2 |
| `cha` | Number |  | 1 |
| `lck` | Number |  | 1 |

</details>

---

### Context: `317` (7 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 7 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 7 |
| `con` | Number |  | 1 |

</details>

---

### Context: `319` (7 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 7 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 7 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `703` (7 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 7 |
| [`desc`](./Strings.md#string-desc) | String |  | 6 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 6 |
| `con` | Number |  | 2 |
| `cha` | Number |  | 1 |
| `int` | Number |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `301` (6 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 6 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 4 |
| `int` | Number |  | 2 |
| `con` | Number |  | 1 |
| `dex` | Number |  | 1 |
| `spd` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `318` (6 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 6 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 2 |
| `divine_shield` | Number |  | 1 |

</details>

---

### Context: `702` (6 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 6 |
| `int` | Number |  | 3 |
| `cha` | Number |  | 2 |
| `con` | Number |  | 2 |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `900` (6 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 6 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 6 |
| `spd` | Number |  | 2 |
| `cha` | Number |  | 1 |
| `con` | Number |  | 1 |

</details>

---

### Context: `-2` (5 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 5 |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| `dex` | Number |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `cha` | Number |  | 1 |

</details>

---

### Context: `302` (5 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 4 |
| `shield` | Number |  | 2 |
| `con` | Number |  | 1 |
| `int` | Number |  | 1 |
| `lck` | Number |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `303` (5 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 4 |
| `cha` | Number |  | 2 |
| `int` | Number |  | 2 |
| `shield` | Number |  | 1 |
| `spd` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `307` (5 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| `spd` | Number |  | 2 |
| `cha` | Number |  | 1 |
| `int` | Number |  | 1 |
| `shield` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `310` (5 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `cha` | Number |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 2 |
| `int` | Number |  | 1 |
| [`override_move`](./Enums.md#enum-override_move) | Enum |  | 1 |
| `shield` | Number |  | 1 |

</details>

---

### Context: `311` (5 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| `con` | Number |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `312` (5 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| `divine_shield` | Number |  | 1 |
| `shield` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `316` (5 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| `cha` | Number |  | 1 |
| `shield` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `326` (5 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |

</details>

---

### Context: `750` (5 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| `cha` | Number |  | 1 |
| `int` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `754` (5 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `300` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 4 |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `str` | Number |  | 3 |
| `con` | Number |  | 2 |
| `cha` | Number |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `304` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 4 |
| `cha` | Number |  | 2 |
| `dex` | Number |  | 2 |
| `int` | Number |  | 1 |
| `spd` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `308` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `cha` | Number |  | 3 |
| `lck` | Number |  | 2 |
| `str` | Number |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 2 |
| `con` | Number |  | 1 |
| `int` | Number |  | 1 |

</details>

---

### Context: `320` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `shield` | Number |  | 1 |

</details>

---

### Context: `321` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `int` | Number |  | 1 |
| `shield` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `323` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `spd` | Number |  | 2 |

</details>

---

### Context: `325` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `spd` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `327` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `cha` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `328` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 2 |

</details>

---

### Context: `329` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `331` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| [`override_move`](./Enums.md#enum-override_move) | Enum |  | 1 |

</details>

---

### Context: `332` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `334` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `str` | Number |  | 1 |

</details>

---

### Context: `336` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `337` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `339` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `spd` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `341` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |

</details>

---

### Context: `705` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 4 |
| `cha` | Number |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| `int` | Number |  | 1 |
| `speed` | Number |  | 1 |

</details>

---

### Context: `706` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 4 |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `cha` | Number |  | 2 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `755` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |

</details>

---

### Context: `1500` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 3 |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `dex` | Number |  | 1 |

</details>

---

### Context: `305` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `int` | Number |  | 2 |
| `lck` | Number |  | 2 |
| `cha` | Number |  | 1 |
| `dex` | Number |  | 1 |
| `shield` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `306` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `con` | Number |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 2 |
| `dex` | Number |  | 1 |
| `int` | Number |  | 1 |
| `shield` | Number |  | 1 |
| `spd` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `322` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `cha` | Number |  | 1 |
| `con` | Number |  | 1 |
| `str` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `324` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `con` | Number |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `335` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |

</details>

---

### Context: `338` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |

</details>

---

### Context: `342` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `con` | Number |  | 1 |

</details>

---

### Context: `343` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `757` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `int` | Number |  | 1 |

</details>

---

### Context: `759` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `330` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |

</details>

---

### Context: `333` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `shield` | Number |  | 1 |

</details>

---

### Context: `340` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `divine_shield` | Number |  | 1 |

</details>

---

### Context: `344` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |

</details>

---

### Context: `345` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `751` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `con` | Number |  | 1 |

</details>

---

### Context: `752` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `con` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `753` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `shield` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `758` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `con` | Number |  | 1 |

</details>

---

### Context: `760` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |

</details>

---

### Context: `1026` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `1029` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `346` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| `shield` | Number |  | 1 |

</details>

---

### Context: `347` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `348` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `349` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `351` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `352` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `353` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `442` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 1 |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `707` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| `str` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `756` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| `int` | Number |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `761` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `762` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `763` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

