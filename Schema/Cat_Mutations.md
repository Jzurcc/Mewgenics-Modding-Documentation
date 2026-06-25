# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Cat Mutations

> **Associated Files:** `data/mutations/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 489

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1733 |
| [`tag`](./Enums.md#enum-tag) | Enum | Examples: `common, melted, animal` | 981 |
| [`desc`](./Strings.md#string-desc) | String | Examples: `"MUTATION_BODY_309_DESC", "MUTATION_BODY_312_DESC", "MUTATION_BODY_301_DESC"` | 5441 |
| `cha` | Number | Examples: `2, -1, 1` | 468 |
| `spd` | Number | Examples: `1, -1, -2` | 424 |
| `int` | Number | Examples: `2, -1, 1` | 401 |
| `con` | Number | Examples: `-2, -3, 1` | 416 |
| `str` | Number | Examples: `2, -1, 1` | 337 |
| `lck` | Number | Examples: `2, -1, 1` | 351 |
| `dex` | Number | Examples: `2, -1, -2` | 301 |
| `shield` | Number | Examples: `12, 5, 10` | 422 |
| `divine_shield` | Number | Examples: `1` | 54 |
| [`override_move`](./Enums.md#enum-override_move) | Enum | Examples: `BasicJump` | 4 |
| [`attack`](./Enums.md#enum-attack) | Enum | Examples: `FetusSpit` | 26 |
| `speed` | Number | Examples: `-4` | 6 |

</details>

---

### Object: `passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 284

> **Referenced by:** [`PassiveWhenAffectedByElement`](./Cat_Mutations.md#context-passivewhenaffectedbyelement), [`PassiveWhileHasStatus`](./Cat_Mutations.md#context-passivewhilehasstatus), [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 2609 |

</details>

---

### Object: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 52

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 119 |

</details>

---

### Object: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 36 |
| [`element`](./Enums.md#enum-element) | Enum | Examples: `water` | 36 |

</details>

---

### Object: `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`MeleeRevengeDamage`](./Cat_Mutations.md#context-meleerevengedamage), [`RevengeDamage`](./Cat_Mutations.md#context-revengedamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 552 |

</details>

---

### Object: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 26 |
| [`type`](./Enums.md#enum-type) | Enum | Examples: `status` | 10 |
| `damage` | Number | Examples: `0` | 16 |
  | [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. | 0 |

</details>

---

### Object: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 112 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 112 |
| `knockback` | Number | Examples: `2, 1` | 48 |
| [`type`](./Enums.md#enum-type) | Enum | Examples: `status` | 20 |
| `damage` | Number | Examples: `0` | 44 |
  | [`AddDamageToElementDamage`](#adddamagetoelementdamage) | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 0 |
  | [`AddStatusToElementDamage`](#addstatustoelementdamage) | Object | Applies the 'AddStatusToElementDamage' effect. | 0 |
  | [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. | 0 |
  | [`StatusImmunity`](./Enums.md#enum-statusimmunity) | Enum | Applies or references the 'StatusImmunity' effect/state. | 0 |

</details>

---

### Object: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | Examples: `CharmedFlea, SmallRock, Coin` | 76 |
| `chance` | Number | Examples: `20, 100, 10` | 24 |
| `good` | Boolean | Examples: `false` | 40 |

</details>

---

### Object: `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 6 |

</details>

---

### Object: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 30 |

</details>

---

### Object: `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 8 |

</details>

---

### Object: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack), [`StatusOnTookDamageFromAbility`](./Cat_Mutations.md#context-statusontookdamagefromability), [`effects`](./Cat_Mutations.md#context-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 31 |

</details>

---

### Object: `SpawnEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | Examples: `RandomPickup, CharmedFly, CharmedMaggot` | 34 |
| `chance` | Number | Examples: `50, 5, 25` | 40 |
| `good` | Boolean | Examples: `false` | 4 |

</details>

---

### Object: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 42 |

</details>

---

### Object: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | Examples: `Coin, RandomFoodPickup` | 22 |
| [`number`](./Arrays.md#array-number) | Array | Examples: `[ 1 3 ], 2` | 6 |

</details>

---

### Object: `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusKilledCharacters`](./Cat_Mutations.md#context-statuskilledcharacters)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
| `odds` | Number | Examples: `10` | 8 |
  | `AutoReanimate` | Number | Examples: `50` | 0 |
  | [`ApplyPassives`](#applypassives) | Object | Grants the nested passive abilities dynamically. | 0 |

</details>

---

### Object: `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 16 |
| `stacks` | Number | Examples: `4, 8` | 16 |

</details>

---

### Object: `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
  | `AutoReanimate` | Number | Examples: `50` | 0 |
  | [`Conditional_Ally`](#conditionalally) | Object | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 0 |
  | [`Conditional_RandomChance`](#conditional_randomchance) | Object | Conditional trigger: Executes nested logic based on a flat percentage random roll. | 0 |

</details>

---

### Object: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 56 |

</details>

---

### Object: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
  | `RemoveStatusStacks` | Object | Removes a specific number of stacks of a status effect. | 0 |
  | [`Conditional_FirstApplicationThisTurn`](#conditionalfirstapplicationthisturn) | Object | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 0 |
  | [`DivineShield`](./Arrays.md#array-divineshield) | Number | Applies or references the 'DivineShield' effect/state. | 0 |
  | [`Conditional_GoodRoll`](#conditional_goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 0 |
  | [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | Applies or references the 'ImmediateUseAbility' effect/state. | 0 |
  | `Charge` | Number | Applies or references the 'Charge' effect/state. | 0 |
  | `SpeedUp_WithoutInitiative` | Integer | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. | 0 |
  | `ForceAttack` | Object | Forces the character to execute an immediate attack. | 0 |
  | `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 0 |

</details>

---

### Object: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 6 |

</details>

---

### Object: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `move` | 10 |
| [`tag`](./Enums.md#enum-tag) | Enum | Examples: `food` | 10 |
| `range` | Number | Examples: `2` | 10 |

</details>

---

### Object: `AddDamageToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Examples: `Electric` | 18 |
| `damage` | Number | Examples: `1` | 18 |

</details>

---

### Object: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fury` | Number | Examples: `10` | 8 |

</details>

---

### Object: `BackflipWhenTargeted`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `BackflipDodge` | 14 |
| `stacks` | Number | Examples: `2` | 14 |

</details>

---

### Object: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `BackflipDodge` | 12 |
| `chance` | Number | Examples: `10` | 12 |

</details>

---

### Object: `ClassManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`class`](./Enums.md#enum-class) | Enum | Examples: `Colorless` | 12 |
| `reduction` | Number | Examples: `1` | 14 |

</details>

---

### Object: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 3 |

</details>

---

### Object: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 14 |
| `odds` | Number | Examples: `25` | 72 |

</details>

---

### Object: `CounterAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `ChainLightning` | 10 |
| `chance` | Number | Examples: `15` | 2 |

</details>

---

### Object: `KnockUpAndAway`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToBasicMeleeAttack`](./Cat_Mutations.md#context-addstatustobasicmeleeattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | Examples: `3` | 48 |
| `stacks` | Number | Examples: `3` | 44 |

</details>

---

### Object: `MoveWhenDamaged`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Examples: `MoveOne` | 4 |
| [`weights`](./Enums.md#enum-weights) | Enum | Examples: `chaotic` | 18 |

</details>

---

### Object: `PassiveWhenAtFullMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 3 |

</details>

---

### Object: `PassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 12 |
| [`status`](./Enums.md#enum-status) | Enum | Examples: `Bleed` | 12 |

</details>

---

### Object: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array | Examples: `[ 1 2 ]` | 3 |
| [`object`](./Enums.md#enum-object) | Enum | Examples: `RandomPickup` | 19 |

</details>

---

### Object: `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 2 |

</details>

---

### Object: `StatusEveryXSpellCastsEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 2 |
| `stacks` | Number | Examples: `3` | 2 |

</details>

---

### Object: `StatusIfDidntMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1 |

</details>

---

### Object: `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 7 |

</details>

---

### Object: `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 5 |

</details>

---

### Object: `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 5 |

</details>

---

### Object: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 4 |

</details>

---

### Object: `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 4 |

</details>

---

### Object: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 20 |
  | `BrittleCharismaUp` | Integer | Applies or references the 'BrittleCharismaUp' effect/state. | 0 |
  | `BrittleConstitutionUp` | Integer | Applies or references the 'BrittleConstitutionUp' effect/state. | 0 |
  | `BrittleDexterityUp` | Integer | Applies or references the 'BrittleDexterityUp' effect/state. | 0 |
  | `BrittleIntelligenceUp` | Integer | Applies or references the 'BrittleIntelligenceUp' effect/state. | 0 |
  | `BrittleLuckUp` | Integer | Applies or references the 'BrittleLuckUp' effect/state. | 0 |
  | `BrittleSpeedUp` | Integer | Applies or references the 'BrittleSpeedUp' effect/state. | 0 |
  | `BrittleStrengthUp` | Integer | Applies or references the 'BrittleStrengthUp' effect/state. | 0 |
  | [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum | Applies or references the 'UseAbility_NonStack' effect/state. | 0 |

</details>

---

