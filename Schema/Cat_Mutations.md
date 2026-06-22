# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** Some keys labeled as `Number` actually support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Cat Mutations

> **Associated Files:** `data/mutations/`


### Context: `passives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 284

> **Referenced by:** [`-2`](#context--2), [`1026`](#context-1026), [`1029`](#context-1029), [`1500`](#context-1500), [`300`](#context-300), [`301`](#context-301), [`302`](#context-302), [`303`](#context-303), [`304`](#context-304), [`305`](#context-305), [`306`](#context-306), [`307`](#context-307), [`308`](#context-308), [`309`](#context-309), [`310`](#context-310), [`311`](#context-311), [`312`](#context-312), [`313`](#context-313), [`314`](#context-314), [`315`](#context-315), [`316`](#context-316), [`317`](#context-317), [`318`](#context-318), [`319`](#context-319), [`320`](#context-320), [`321`](#context-321), [`322`](#context-322), [`323`](#context-323), [`324`](#context-324), [`325`](#context-325), [`326`](#context-326), [`327`](#context-327), [`328`](#context-328), [`329`](#context-329), [`330`](#context-330), [`331`](#context-331), [`332`](#context-332), [`333`](#context-333), [`334`](#context-334), [`335`](#context-335), [`336`](#context-336), [`337`](#context-337), [`338`](#context-338), [`339`](#context-339), [`340`](#context-340), [`341`](#context-341), [`342`](#context-342), [`343`](#context-343), [`344`](#context-344), [`345`](#context-345), [`346`](#context-346), [`347`](#context-347), [`348`](#context-348), [`349`](#context-349), [`351`](#context-351), [`352`](#context-352), [`353`](#context-353), [`442`](#context-442), [`702`](#context-702), [`703`](#context-703), [`704`](#context-704), [`705`](#context-705), [`706`](#context-706), [`707`](#context-707), [`750`](#context-750), [`751`](#context-751), [`752`](#context-752), [`753`](#context-753), [`754`](#context-754), [`755`](#context-755), [`756`](#context-756), [`757`](#context-757), [`758`](#context-758), [`759`](#context-759), [`760`](#context-760), [`761`](#context-761), [`762`](#context-762), [`763`](#context-763), [`900`](#context-900), [`PassiveWhenAffectedByElement`](#context-passivewhenaffectedbyelement), [`PassiveWhileHasStatus`](#context-passivewhilehasstatus)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`AddStatusToBasicAttack`](#context-addstatustobasicattack) | Block |  | 52 |
| [`PassiveWhenAffectedByElement`](#context-passivewhenaffectedbyelement) | Block |  | 12 |
| [`RevengeDamage`](#context-revengedamage) | Block |  | 9 |
| [`MeleeRevengeDamage`](#context-meleerevengedamage) | Block |  | 7 |
| [`AddStatusToBasicMeleeAttack`](#context-addstatustobasicmeleeattack) | Block |  | 6 |
| [`StatusOnTookDamage`](#context-statusontookdamage) | Block |  | 6 |
| [`StatusEachTurnBegin`](#context-statuseachturnbegin) | Block |  | 5 |
| [`StatusEachTurnEnd`](#context-statuseachturnend) | Block |  | 4 |
| [`StatusEveryXSpellCasts`](#context-statuseveryxspellcasts) | Block |  | 2 |
| [`StatusKilledCharacters`](#context-statuskilledcharacters) | Block |  | 2 |
| [`StatusOnBattleEnd`](#context-statusonbattleend) | Block |  | 2 |
| [`StatusOnEndMove`](#context-statusonendmove) | Block |  | 2 |
| [`StatusOnTookDamageFromAbility`](#context-statusontookdamagefromability) | Block |  | 2 |
| [`PassiveWhenAtFullMana`](#context-passivewhenatfullmana) | Block |  | 1 |
| [`PassiveWhileHasStatus`](#context-passivewhilehasstatus) | Block |  | 1 |
| [`StatusEachRoundEnd`](#context-statuseachroundend) | Block |  | 1 |
| [`StatusIfUnusedMovePoints`](#context-statusifunusedmovepoints) | Block |  | 1 |
| [`StatusOnAllyCatDeath`](#context-statusonallycatdeath) | Block |  | 1 |
| [`StatusOnCastSpell`](#context-statusoncastspell) | Block |  | 1 |
| [`StatusOnDie`](#context-statusondie) | Block |  | 1 |
| [`StatusOnEatFood`](#context-statusoneatfood) | Block |  | 1 |
| [`StatusOnKill`](#context-statusonkill) | Block |  | 1 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 52

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block |  | 1 |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum |  | 12 |
| [`passives`](#context-passives) | Block |  | 12 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 10

> **Referenced by:** [`MeleeRevengeDamage`](#context-meleerevengedamage), [`RevengeDamage`](#context-revengedamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`{Effects}`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| [`{Global Modifiers}`](./Engine_GlobalModifiers.md#all-confirmed-global-modifier-id-values) | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |  |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block |  | 1 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](#context-effects) | Block |  | 9 |
| `damage` | Number |  | 4 |
| [`type`](./Enums.md#enum-type) | Enum |  | 4 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `knockback` | Number |  | 4 |
| `damage` | Number |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum |  | 2 |
| [`effects`](#context-effects) | Block |  | 1 |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number |  | 7 |
| [`object`](./Enums.md#enum-object) | Enum |  | 7 |
| `good` | Boolean |  | 5 |

</details>

---

### Context: `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack), [`StatusOnTookDamageFromAbility`](#context-statusontookdamagefromability), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |

</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number |  | 4 |
| [`object`](./Enums.md#enum-object) | Enum |  | 4 |
| `good` | Boolean |  | 1 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 3 |
| `number` | Number |  | 2 |

</details>

---

### Context: `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`StatusKilledCharacters`](#context-statuskilledcharacters)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Effects}`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
| `odds` | Number |  | 2 |

</details>

---

### Context: `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `stacks` | Number |  | 2 |

</details>

---

### Context: `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
 | [`Conditional_RandomChance`](./Cat_Mutations.md#context-conditional_randomchance) | Block |  | 2 | 

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |

</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block |  | 2 |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum |  | 1 |
| `range` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `AddDamageToElementDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number |  | 1 |
| [`element`](./Enums.md#enum-element) | Enum |  | 1 |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fury` | Number |  | 1 |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum |  | 1 |
| `stacks` | Number |  | 1 |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum |  | 1 |
| `chance` | Number |  | 1 |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`class`](./Enums.md#enum-class) | Enum |  | 1 |
| `reduction` | Number |  | 1 |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusOnEndMove`](#context-statusonendmove)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Effects}`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusOnEndMove`](#context-statusonendmove)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Effects}`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
| `odds` | Number |  | 1 |

</details>

---

### Context: `CounterAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum |  | 1 |
| `chance` | Number |  | 1 |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AddStatusToBasicMeleeAttack`](#context-addstatustobasicmeleeattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number |  | 1 |
| `stacks` | Number |  | 1 |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 1 |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 1 |

</details>

---

### Context: `PassiveWhenAtFullMana`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |

</details>

---

### Context: `PassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum |  | 1 |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

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

### Context: `StatusEveryXSpellCastsEachTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `HealthGain` | Number |  | 1 |
| `stacks` | Number |  | 1 |

</details>

---

### Context: `StatusIfDidntMove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Charge` | Number |  | 1 |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |

</details>

---

### Context: `StatusOnCastSpell`

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

### Context: `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |

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

### Numerical Contexts

> The following contexts are numeric keys or array indices.


### Context: `400`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `401`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `402`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `403`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `404`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spd` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `405`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `lck` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `406`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `407`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `dex` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `408`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `con` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `409`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `410`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `411`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `412`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `dex` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `413`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `414`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `dex` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `415`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `416`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `417`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `418`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `419`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `420`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `421`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `422`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `423`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `424`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `con` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `425`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `dex` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `426`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `427`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `428`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `429`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `430`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `431`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `432`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `433`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `434`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `lck` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `435`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `lck` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `436`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `437`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spd` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `438`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `439`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `440`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `441`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `lck` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 9 |

</details>

---

### Context: `700`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

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

### Context: `701`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

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

### Context: `313`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 8 |
| [`passives`](#context-passives) | Block |  | 8 |
| `divine_shield` | Number |  | 1 |
| `shield` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `314`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 8 |
| [`passives`](#context-passives) | Block |  | 8 |
| `cha` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `315`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 8 |
| [`passives`](#context-passives) | Block |  | 8 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `704`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 8 |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](#context-passives) | Block |  | 5 |
| `cha` | Number |  | 2 |
| `str` | Number |  | 2 |
| `con` | Number |  | 1 |
| `lck` | Number |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `309`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 7 |
| [`passives`](#context-passives) | Block |  | 7 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 2 |
| `cha` | Number |  | 1 |
| `lck` | Number |  | 1 |

</details>

---

### Context: `317`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 7 |
| [`passives`](#context-passives) | Block |  | 7 |
| `con` | Number |  | 1 |

</details>

---

### Context: `319`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 7 |
| [`passives`](#context-passives) | Block |  | 7 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `703`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 7 |
| [`desc`](./Strings.md#string-desc) | String |  | 6 |
| [`passives`](#context-passives) | Block |  | 6 |
| `con` | Number |  | 2 |
| `cha` | Number |  | 1 |
| `int` | Number |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `301`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 6 |
| [`passives`](#context-passives) | Block |  | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 4 |
| `int` | Number |  | 2 |
| `con` | Number |  | 1 |
| `dex` | Number |  | 1 |
| `spd` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `318`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 6 |
| [`passives`](#context-passives) | Block |  | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 2 |
| `divine_shield` | Number |  | 1 |

</details>

---

### Context: `702`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 6 |
| `int` | Number |  | 3 |
| `cha` | Number |  | 2 |
| `con` | Number |  | 2 |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `900`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 6 |
| [`passives`](#context-passives) | Block |  | 6 |
| `spd` | Number |  | 2 |
| `cha` | Number |  | 1 |
| `con` | Number |  | 1 |

</details>

---

### Context: `-2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 5 |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| `dex` | Number |  | 2 |
| [`passives`](#context-passives) | Block |  | 2 |
| `cha` | Number |  | 1 |

</details>

---

### Context: `302`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](#context-passives) | Block |  | 5 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 4 |
| `shield` | Number |  | 2 |
| `con` | Number |  | 1 |
| `int` | Number |  | 1 |
| `lck` | Number |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `303`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](#context-passives) | Block |  | 5 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 4 |
| `cha` | Number |  | 2 |
| `int` | Number |  | 2 |
| `shield` | Number |  | 1 |
| `spd` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `307`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](#context-passives) | Block |  | 5 |
| `spd` | Number |  | 2 |
| `cha` | Number |  | 1 |
| `int` | Number |  | 1 |
| `shield` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `310`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](#context-passives) | Block |  | 4 |
| `cha` | Number |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 2 |
| `int` | Number |  | 1 |
| [`override_move`](./Enums.md#enum-override_move) | Enum |  | 1 |
| `shield` | Number |  | 1 |

</details>

---

### Context: `311`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](#context-passives) | Block |  | 5 |
| `con` | Number |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `312`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](#context-passives) | Block |  | 5 |
| `divine_shield` | Number |  | 1 |
| `shield` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `316`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](#context-passives) | Block |  | 5 |
| `cha` | Number |  | 1 |
| `shield` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `326`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](#context-passives) | Block |  | 5 |

</details>

---

### Context: `750`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](#context-passives) | Block |  | 5 |
| `cha` | Number |  | 1 |
| `int` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `754`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 5 |
| [`passives`](#context-passives) | Block |  | 5 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `300`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 4 |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](#context-passives) | Block |  | 3 |
| `str` | Number |  | 3 |
| `con` | Number |  | 2 |
| `cha` | Number |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `304`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 4 |
| `cha` | Number |  | 2 |
| `dex` | Number |  | 2 |
| `int` | Number |  | 1 |
| `spd` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `308`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| `cha` | Number |  | 3 |
| `lck` | Number |  | 2 |
| `str` | Number |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 2 |
| `con` | Number |  | 1 |
| `int` | Number |  | 1 |

</details>

---

### Context: `320`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| `shield` | Number |  | 1 |

</details>

---

### Context: `321`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| `int` | Number |  | 1 |
| `shield` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `323`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| `spd` | Number |  | 2 |

</details>

---

### Context: `325`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| `spd` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `327`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| `cha` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `328`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 2 |

</details>

---

### Context: `329`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `331`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| [`override_move`](./Enums.md#enum-override_move) | Enum |  | 1 |

</details>

---

### Context: `332`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `334`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| `str` | Number |  | 1 |

</details>

---

### Context: `336`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `337`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `339`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| `spd` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `341`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |

</details>

---

### Context: `705`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 4 |
| `cha` | Number |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| `int` | Number |  | 1 |
| `speed` | Number |  | 1 |

</details>

---

### Context: `706`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 4 |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](#context-passives) | Block |  | 3 |
| `cha` | Number |  | 2 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `755`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |

</details>

---

### Context: `1500`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 3 |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](#context-passives) | Block |  | 2 |
| `dex` | Number |  | 1 |

</details>

---

### Context: `305`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](#context-passives) | Block |  | 3 |
| `int` | Number |  | 2 |
| `lck` | Number |  | 2 |
| `cha` | Number |  | 1 |
| `dex` | Number |  | 1 |
| `shield` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `306`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](#context-passives) | Block |  | 3 |
| `con` | Number |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 2 |
| `dex` | Number |  | 1 |
| `int` | Number |  | 1 |
| `shield` | Number |  | 1 |
| `spd` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `322`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](#context-passives) | Block |  | 3 |
| `cha` | Number |  | 1 |
| `con` | Number |  | 1 |
| `str` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `324`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](#context-passives) | Block |  | 3 |
| `con` | Number |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `335`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](#context-passives) | Block |  | 3 |

</details>

---

### Context: `338`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](#context-passives) | Block |  | 3 |

</details>

---

### Context: `342`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](#context-passives) | Block |  | 3 |
| `con` | Number |  | 1 |

</details>

---

### Context: `343`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](#context-passives) | Block |  | 3 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `757`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](#context-passives) | Block |  | 3 |
| `int` | Number |  | 1 |

</details>

---

### Context: `759`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 3 |
| [`passives`](#context-passives) | Block |  | 3 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `330`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](#context-passives) | Block |  | 2 |

</details>

---

### Context: `333`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](#context-passives) | Block |  | 2 |
| `shield` | Number |  | 1 |

</details>

---

### Context: `340`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](#context-passives) | Block |  | 2 |
| `divine_shield` | Number |  | 1 |

</details>

---

### Context: `344`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](#context-passives) | Block |  | 2 |

</details>

---

### Context: `345`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](#context-passives) | Block |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `751`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](#context-passives) | Block |  | 2 |
| `con` | Number |  | 1 |

</details>

---

### Context: `752`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](#context-passives) | Block |  | 2 |
| `con` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `753`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](#context-passives) | Block |  | 2 |
| `shield` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `758`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](#context-passives) | Block |  | 2 |
| `con` | Number |  | 1 |

</details>

---

### Context: `760`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 2 |
| [`passives`](#context-passives) | Block |  | 2 |

</details>

---

### Context: `1026`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `1029`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

### Context: `346`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |
| `shield` | Number |  | 1 |

</details>

---

### Context: `347`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

### Context: `348`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

### Context: `349`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

### Context: `351`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

### Context: `352`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

### Context: `353`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `442`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 1 |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `707`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |
| `str` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `756`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| `int` | Number |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `761`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

### Context: `762`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

### Context: `763`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String |  | 1 |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

