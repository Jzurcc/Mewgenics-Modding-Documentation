# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Cat Mutations

> **Associated Files:** `data/mutations/`


### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 489

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | Examples: `common, melted, animal` | 489 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4118 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1549 |
| `cha` | Number | Examples: `2, -1, 1` | 144 |
| `spd` | Number | Examples: `1, -1, -2` | 133 |
| `int` | Number | Examples: `2, -1, 1` | 132 |
| `con` | Number | Examples: `-2, -3, 1` | 131 |
| `str` | Number | Examples: `2, -1, 1` | 126 |
| `lck` | Number | Examples: `2, -1, 1` | 119 |
| `dex` | Number | Examples: `2, -1, -2` | 118 |
| `shield` | Number | Examples: `12, 5, 10` | 16 |
| `divine_shield` | Number | Examples: `1` | 4 |
| [`override_move`](./Enums.md#enum-override_move) | Enum | Examples: `BasicJump` | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum | Examples: `FetusSpit` | 1 |
| `speed` | Number | Examples: `-4` | 1 |

</details>

---

### Context: `passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 284

> **Referenced by:** [`PassiveWhenAffectedByElement`](./Cat_Mutations.md#context-passivewhenaffectedbyelement), [`PassiveWhileHasStatus`](./Cat_Mutations.md#context-passivewhilehasstatus), [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2609 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 52

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 119 |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Examples: `water` | 12 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 30 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`MeleeRevengeDamage`](./Cat_Mutations.md#context-meleerevengedamage), [`RevengeDamage`](./Cat_Mutations.md#context-revengedamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 552 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 10 |
| `damage` | Number | Examples: `0` | 4 |
| [`type`](./Enums.md#enum-type) | Enum | Examples: `status` | 4 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | Examples: `2, 1` | 4 |
| `damage` | Number | Examples: `0` | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Examples: `status` | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 45 |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 36 |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Examples: `20, 100, 10` | 7 |
| [`object`](./Enums.md#enum-object) | Enum | Examples: `CharmedFlea, SmallRock, Coin` | 7 |
| `good` | Boolean | Examples: `false` | 5 |

</details>

---

### Context: `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 30 |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack), [`StatusOnTookDamageFromAbility`](./Cat_Mutations.md#context-statusontookdamagefromability), [`effects`](./Cat_Mutations.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 31 |

</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Examples: `50, 5, 25` | 4 |
| [`object`](./Enums.md#enum-object) | Enum | Examples: `RandomPickup, CharmedFly, CharmedMaggot` | 4 |
| `good` | Boolean | Examples: `false` | 1 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 42 |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | Examples: `Coin, RandomFoodPickup` | 3 |
| [`number`](./Arrays.md#array-number) | Array | Examples: `[ 1 3 ], 2` | 2 |

</details>

---

### Context: `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusKilledCharacters`](./Cat_Mutations.md#context-statuskilledcharacters)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| `odds` | Number | Examples: `10` | 2 |

</details>

---

### Context: `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Examples: `4, 8` | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 9 |

</details>

---

### Context: `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 56 |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `move` | 1 |
| `range` | Number | Examples: `2` | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | Examples: `food` | 1 |

</details>

---

### Context: `AddDamageToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | Examples: `1` | 1 |
| [`element`](./Enums.md#enum-element) | Enum | Examples: `Electric` | 1 |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fury` | Number | Examples: `10` | 1 |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `BackflipDodge` | 1 |
| `stacks` | Number | Examples: `2` | 1 |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `BackflipDodge` | 1 |
| `chance` | Number | Examples: `10` | 1 |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`class`](./Enums.md#enum-class) | Enum | Examples: `Colorless` | 1 |
| `reduction` | Number | Examples: `1` | 1 |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 14 |
| `odds` | Number | Examples: `25` | 1 |

</details>

---

### Context: `CounterAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `ChainLightning` | 1 |
| `chance` | Number | Examples: `15` | 1 |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToBasicMeleeAttack`](./Cat_Mutations.md#context-addstatustobasicmeleeattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | Examples: `3` | 1 |
| `stacks` | Number | Examples: `3` | 1 |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Examples: `MoveOne` | 1 |
| [`weights`](./Enums.md#enum-weights) | Enum | Examples: `chaotic` | 1 |

</details>

---

### Context: `PassiveWhenAtFullMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `PassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 10 |
| [`status`](./Enums.md#enum-status) | Enum | Examples: `Bleed` | 1 |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array | Examples: `[ 1 2 ]` | 1 |
| [`object`](./Enums.md#enum-object) | Enum | Examples: `RandomPickup` | 1 |

</details>

---

### Context: `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `StatusEveryXSpellCastsEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `stacks` | Number | Examples: `3` | 1 |

</details>

---

### Context: `StatusIfDidntMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |

</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 20 |

</details>

---

