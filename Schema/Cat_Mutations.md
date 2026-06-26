# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Cat Mutations

> **Associated Files:** `data/mutations/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 489

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 2985 |  |
| [`desc`](./Strings.md#string-desc) | Enum | Examples: `"MUTATION_BODY_309_DESC", "MUTATION_BODY_312_DESC", "MUTATION_BODY_301_DESC"` | 2423 |  |
| `shield` | Enum / Integer | Examples: `12, 5, 10` | 191 |  |
| `cha` | Enum / Integer | Examples: `2, -1, 1` | 89 |  |
| `con` | Enum / Integer | Examples: `-2, -3, 1` | 79 |  |
| `spd` | Enum / Integer | Examples: `1, -1, -2` | 78 |  |
| `int` | Enum / Integer | Examples: `2, -1, 1` | 66 |  |
| `lck` | Enum / Integer | Examples: `2, -1, 1` | 53 |  |
| `str` | Enum / Integer | Examples: `2, -1, 1` | 45 |  |
| `dex` | Enum / Integer | Examples: `2, -1, -2` | 30 |  |
| `divine_shield` | Integer | Examples: `1` | 20 |  |
| `speed` | Array / Number | Examples: `-4` | 19 |  |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Examples: `common, melted, animal` | 7 |  |
| [`attack`](./Enums.md#enum-attack) | Enum | Examples: `FetusSpit` | 7 |  |

</details>

---

### Object: `passives`


**Definition:** Object listing intrinsic passive modifiers.  
**Total Count:** 284


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenAffectedByElement`](./Cat_Mutations.md#context-passivewhenaffectedbyelement), [`PassiveWhileHasStatus`](./Cat_Mutations.md#context-passivewhilehasstatus), [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 2039 |  |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object || 133 ||
| [`Brace`](./Enums.md) | Integer || 94 | 1 |
| [`Trample`](./Enums.md) | Integer || 88 | 3 |
| [`Thorns`](./Enums.md) | Integer || 65 | 2 |
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object || 59 ||
| [`HealthRegenUp`](./Enums.md) | Integer || 52 | 2 |
| [`StatusEachTurnEnd`](#object-statuseachturnend) | Object || 49 ||
| [`StatusOnBattleEnd`](Abilities_and_Spells.md#object-statusonbattleend) | Object || 45 ||
| [`ElementImmune`](./Enums.md) | Enum || 39 | Ice |
| [`CounterAttack`](#object-counterattack) | Object || 34 ||
| [`StatusImmunity`](./Enums.md) | Array || 34 | [Freeze] |
| [`StatusOnKill`](#object-statusonkill) | Object || 29 ||
| [`StatusOnTookDamage`](#object-statusontookdamage) | Object || 29 ||
| [`SpawnThingOnDamage`](#object-spawnthingondamage) | Object || 28 ||
| [`AbilityReaction`](./Enums.md) | Enum | | 23 | SkunkTail |
| [`DamageUp`](./Enums.md) | Integer || 21 | 2 |
| [`AddMovement`](./Enums.md) | Integer || 20 | 1 |
| [`StatusEachTurnBegin`](#object-statuseachturnbegin) | Object || 18 ||
| [`CritChanceUp`](./Enums.md) | Integer || 16 | 5 |
| [`AddBonusRange`](./Enums.md) | Integer || 15 | 1 |
| [`KineticSpikes`](./Enums.md) | Integer || 15 | 1 |
| [`RevengeDamage`](Abilities_and_Spells.md#object-revengedamage) | Object || 15 ||
| [`SpawnEachTurn`](#object-spawneachturn) | Object || 15 ||
| [`AddCorpseHealth`](./Enums.md) | Integer || 14 | 2 |
| [`AllStatsUp`](./Enums.md) | Integer || 14 | 1 |
| [`DodgeChance`](./Enums.md) | Integer || 14 | 2 |
| [`WaterWalk`](./Enums.md) | Integer || 14 | 1 |
| [`AddManaRegen`](./Enums.md) | Integer || 13 | 1 |
| [`MulticlassLevelUp`](./Enums.md) | Enum || 12 | Hunter |
| [`ReflectProjectiles`](./Enums.md) | Integer || 12 | 10 |
| [`BleedThorns`](./Enums.md) | Integer || 11 | 2 |
| [`ExtraBasicAttacks`](./Enums.md) | Integer || 11 | 2 |
| [`MoveWhenDamaged`](#object-movewhendamaged) | Object || 11 ||
| [`ReplaceBasicMove`](./Enums.md) | Enum || 11 | ToadJump_BasicMove |
| [`AddLevelUpRerolls`](./Enums.md) | Integer || 10 | 1 |
| [`BackstabImmunity`](./Enums.md) | Integer || 9 | 1 |
| [`Bruise`](./Enums.md) | Integer || 9 | 2 |
| [`DepressionAura`](./Enums.md) | Integer || 9 | 1 |
| [`MissChance`](./Enums.md) | Integer || 9 | 20 |
| [`PoisonThorns`](./Enums.md) | Integer || 9 | 2 |
| [`StatusOnDie`](#object-statusondie) | Object || 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |
| [`AddElementsToBasicAttack`](./Enums.md) | Enum || 7 | Ice |
| [`AddInitiative`](./Enums.md) | Integer || 7 | -20 |
| [`AlphaTurns`](./Enums.md) | Integer || 7 | 1 |
| [`Bleed`](./Enums.md) | Array / Integer || 7 | [3] |
| [`ManaCostReduction`](./Enums.md) | Integer || 7 | 1 |
| [`StatusOnEndMove`](#object-statusonendmove) | Object || 7 ||
| [`AddDamageToElementDamage`](#object-adddamagetoelementdamage) | Object || 6 ||
| [`DodgeChance_Status`](./Enums.md) | Integer || 6 | 10 |
| [`IgnoreTiles`](./Enums.md) | Integer || 6 | 1 |
| [`Poison`](./Enums.md) | Integer || 6 | 1 |
| [`Quivered`](./Enums.md) | Array / Integer || 6 | [0.1] |
| [`SpawnOnBattleStartRandomEmptyTile`](#object-spawnonbattlestartrandomemptytile) | Object || 6 ||
| [`StatusOnTookDamageFromAbility`](#object-statusontookdamagefromability) | Object || 6 ||
| [`YOffset`](./Enums.md) | Number || 6 | .25 |
| [`AddBonusMeleeRange`](./Enums.md) | Integer || 5 | 1 |
| [`ClassManaCostReduction`](#object-classmanacostreduction) | Object || 5 ||
| [`KnockbackImmunity`](./Enums.md) | Integer || 5 | 1 |
| [`StatusIfUnusedMovePoints`](#object-statusifunusedmovepoints) | Object || 5 ||
| [`AddKnockbackDamage`](./Enums.md) | Integer || 4 | 1 |
| [`AddTemporaryEffectsToBasicAttack`](#object-addtemporaryeffectstobasicattack) | Object || 4 ||
| [`BoostWeaponDamage`](./Enums.md) | Integer || 4 | 1 |
| [`ChanceToBackflip`](#object-chancetobackflip) | Object || 4 ||
| [`EquipTemporaryItem`](./Enums.md) | Enum || 4 | WaterBottle_Full |
| [`PassiveWhenAffectedByElement`](#object-passivewhenaffectedbyelement) | Object || 4 ||
| [`StatusEveryXSpellCasts`](#object-statuseveryxspellcasts) | Object || 4 ||
| [`StatusOnAllyCatDeath`](#object-statusonallycatdeath) | Object || 4 ||
| [`StatusOnCastSpell`](#object-statusoncastspell) | Object || 4 ||
| [`AbilityWhenTaggedCharacterMovesNear`](#object-abilitywhentaggedcharactermovesnear) | Object || 3 ||
| [`AddStatusToBasicMeleeAttack`](#object-addstatustobasicmeleeattack) | Object || 3 ||
| [`Confusion`](./Enums.md) | Array / Integer || 3 | [2] |
| [`SpawnExtraThingsOnBattleStart`](#object-spawnextrathingsonbattlestart) | Object || 3 ||
| [`StatusOnEatFood`](#object-statusoneatfood) | Object || 3 ||
| [`CanRemoveCursedItems`](./Enums.md) | Integer || 2 | 1 |
| [`FreePathfindElement`](./Enums.md) | Enum || 2 | Water |
| [`MoveAwayFromDamageSource`](./Enums.md) | Enum || 2 | BasicJump |
| [`PassiveWhenAtFullMana`](#object-passivewhenatfullmana) | Object || 2 ||
| [`PassiveWhileHasStatus`](#object-passivewhilehasstatus) | Object || 2 ||
| [`PoopWhenHit`](./Enums.md) | Enum || 2 | Poop |
| [`StatusKilledCharacters`](#object-statuskilledcharacters) | Object || 2 ||
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Object || 1 ||
| [`BasicAttackCantMiss`](./Enums.md) | Integer || 1 | 1 |
| [`BlacklistPickupType`](./Enums.md) | Enum || 1 | catnip |
| [`Blind`](./Enums.md) | Array / Integer || 1 | [.10] |
| [`ConjureBonusAbility`](./Enums.md) | Enum || 1 | random |
| [`DisableAbilitiesWithTag`](./Enums.md) | Enum || 1 | consumable |
| [`HouseFoodRequirementMultiplier`](./Enums.md) | Integer || 1 | 0 |
| [`MakeBasicAttackPull`](./Enums.md) | Integer || 1 | 1 |
| [`ShowHiddenThings`](./Enums.md) | Integer || 1 | 1 |
| [`Slow`](./Enums.md) | Array / Integer || 1 | [.1] |
| [`SpawnOnDowned`](./Enums.md) | Enum || 1 | CharmedFly |
| [`StatusEachRoundEnd`](#object-statuseachroundend) | Object || 1 ||
| [`Vegan`](./Enums.md) | Integer || 1 | 1 |

</details>

---

### Object: `AddStatusToBasicAttack`


**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 52


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 205 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 56 |
| [`Bleed`](./Enums.md) | Array / Integer || 30 | [3] |
| [`Poison`](./Enums.md) | Integer || 29 | 1 |
| [`Knockback`](./Enums.md) | Integer || 24 | 2 |
| [`Burn`](./Enums.md) | Integer || 16 | 1 |
| [`Fear`](./Enums.md) | Array || 13 | [.15] |
| [`Bruise`](./Enums.md) | Integer || 12 | 2 |
| [`ChangeTile`](./Enums.md) | Enum || 10 | WaterTile |
| [`Slow`](./Enums.md) | Array / Integer || 10 | [.1] |
| [`Stun`](./Enums.md) | Array || 8 | [.05] |
| [`Confusion`](./Enums.md) | Array / Integer || 7 | [2] |
| [`Freeze`](./Enums.md) | Array || 4 | [0.15] |
| [`Leeches`](./Enums.md) | Integer || 4 | 1 |
| [`SoulLink`](./Enums.md) | Integer || 4 | 1 |
| [`Charmed`](./Enums.md) | Array || 3 | [.15] |
| [`VisualFXTile`](./Enums.md) | Enum || 2 | fx_windSpell |
| [`FaceAway`](./Enums.md) | Integer || 1 | 1 |
| [`FlatLeech`](./Enums.md) | Integer || 1 | 1 |
| [`Immobile`](./Enums.md) | Array / Integer || 1 | [.05] |
| [`Instakill`](./Enums.md) | Array || 1 | [25] |
| [`Petrify`](./Enums.md) | Array || 1 | [.05] |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object || 1 ||
| [`VaporizeInanimate`](./Enums.md) | Integer || 1 | 1 |
| [`Webbed`](./Enums.md) | Array || 1 | [.1] |

</details>

---

### Object: `PassiveWhenAffectedByElement`


**Definition:** Examples: `{ ... }`  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Examples: `water` | 18 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 18 ||
| [`passives`](#object-passives) | Object || 18 ||

</details>

---

### Object: `effects`
### Object: `effects`

**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Cat_Mutations.md#context-meleerevengedamage), [`RevengeDamage`](./Cat_Mutations.md#context-revengedamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 1695 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 750 |
| [`Confusion`](./Enums.md) | Array / Integer || 37 | [2] |
| [`Fear`](./Enums.md) | Array || 31 | [.15] |
| [`Blind`](./Enums.md) | Array / Integer || 24 | [.10] |
| [`Charmed`](./Enums.md) | Array || 22 | [.15] |
| [`Petrify`](./Enums.md) | Array || 15 | [.05] |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object || 14 ||

</details>

---

### Object: `RevengeDamage`


**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 31 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object || 29 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 29 |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Examples: `0` | 8 ||
| [`type`](./Enums.md#enum-type) | Enum | Examples: `status` | 5 ||

</details>

---

### Object: `MeleeRevengeDamage`


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 70 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 49 |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object || 47 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 43 ||
| `knockback` | Enum / Integer | Examples: `2, 1` | 24 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Examples: `0` | 22 ||
| [`type`](./Enums.md#enum-type) | Enum | Examples: `status` | 10 ||
| [`Freeze`](./Enums.md) | Array || 1 | [0.15] |
| [`Immobile`](./Enums.md) | Array / Integer || 1 | [.05] |

</details>

---

### Object: `SpawnThingOnDamage`


**Definition:** Applies or references the 'SpawnThingOnDamage' effect/state.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Examples: `CharmedFlea, SmallRock, Coin` | 38 ||
| `good` | Boolean | Examples: `false` | 20 ||
| `chance` | Number | Examples: `20, 100, 10` | 12 ||

</details>

---

### Object: `AddStatusToBasicMeleeAttack`


**Definition:** Examples: `{ ... }`  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 9 ||
| [`Bleed`](./Enums.md) | Array / Integer || 2 | [3] |
| [`Knockback`](./Enums.md) | Integer || 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`Immobile`](./Enums.md) | Array / Integer || 1 | [.05] |
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object || 1 ||

</details>

---

### Object: `StatusOnTookDamage`


**Definition:** Event Trigger: Applies nested statuses when took damage.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 38 ||
| [`Charge`](./Enums.md) | Integer || 8 | 2 |
| [`ChangeTilesUnder`](./Enums.md) | Enum || 2 | GlassTile |
| [`LuckUp`](./Enums.md) | Integer || 1 | 1 |

</details>

---

### Object: `StatusEachTurnBegin`


**Definition:** Event Trigger: Applies nested statuses to each turn begin.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 24 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`Quivered`](./Enums.md) | Array / Integer || 2 | [0.1] |
| [`SpeedUp`](./Enums.md) | Integer || 2 | 1 |
| [`MissChance`](./Enums.md) | Integer || 1 | 20 |
| [`MoveQuivered`](./Enums.md) | Array || 1 | [0.1] |

</details>

---

### Object: `RandomStatusFromPool`


**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack), [`StatusOnTookDamageFromAbility`](./Cat_Mutations.md#context-statusontookdamagefromability), [`effects`](./Cat_Mutations.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 33 ||
| [`Shield`](./Enums.md) | Integer || 12 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 12 |
| [`Thorns`](./Enums.md) | Integer || 10 | 2 |
| [`KineticSpikes`](./Enums.md) | Integer || 9 | 1 |
| [`Poison`](./Enums.md) | Integer || 9 | 1 |
| [`Bleed`](./Enums.md) | Array / Integer || 8 | [3] |
| [`Charge`](./Enums.md) | Integer || 8 | 2 |
| [`Weakness`](./Enums.md) | Integer || 8 | 1 |
| [`Blind`](./Enums.md) | Array / Integer || 6 | [.10] |
| [`DiminishingHealthRegen`](./Enums.md) | Integer || 6 | 1 |
| [`Burn`](./Enums.md) | Integer || 5 | 1 |
| [`RandomStatUp`](./Enums.md) | Integer || 5 | 2 |

</details>

---

### Object: `SpawnEachTurn`


**Definition:** Applies or references the 'SpawnEachTurn' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Examples: `RandomPickup, CharmedFly, CharmedMaggot` | 22 ||
| `chance` | Number | Examples: `50, 5, 25` | 20 ||
| `good` | Boolean | Examples: `false` | 2 ||

</details>

---

### Object: `StatusEachTurnEnd`


**Definition:** Applies or references the 'StatusEachTurnEnd' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 55 ||
| [`Shield`](./Enums.md) | Integer || 5 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |
| [`RandomStatUp`](./Enums.md) | Integer || 3 | 2 |
| [`IntelligenceUp`](./Enums.md) | Integer || 2 | 1 |
| [`Charge`](./Enums.md) | Integer || 1 | 2 |
| [`RandomStatDown`](./Enums.md) | Integer || 1 | 1 |

</details>

---

### Object: `SpawnOnBattleStartRandomEmptyTile`


**Definition:** Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Examples: `Coin, RandomFoodPickup` | 11 ||
| [`number`](./Arrays.md#array-number) | Array / Integer | Examples: `[ 1 3 ], 2` | 10 ||

</details>

---

### Object: `Conditional_RandomChance`


**Definition:** Conditional trigger: Executes nested logic based on a flat percentage random roll.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKilledCharacters`](./Cat_Mutations.md#context-statuskilledcharacters)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | Examples: `10` | 4 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`AutoReanimate`](./Enums.md) | Integer || 2 | 50 |

</details>

---

### Object: `StatusEveryXSpellCasts`


**Definition:** Applies or references the 'StatusEveryXSpellCasts' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Examples: `4, 8` | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 8 ||
| [`Charge`](./Enums.md) | Integer || 2 | 2 |
| [`RandomMagicMissile`](./Enums.md) | Integer || 1 | 4 |

</details>

---

### Object: `StatusKilledCharacters`


**Definition:** Event Trigger: Applies nested statuses to killed characters.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnBattleEnd`


**Definition:** Applies the nested status effects when the encounter finishes.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 52 ||
| [`FindItemFromPool`](./Enums.md) | Enum || 8 | consumables |
| [`PermanentIntelligence`](./Enums.md) | Integer || 3 | 1 |

</details>

---

### Object: `StatusOnEndMove`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnTookDamageFromAbility`


**Definition:** Event Trigger: Applies statuses when taking damage from an ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 8 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object || 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Object: `AbilityWhenTaggedCharacterMovesNear`


**Definition:** AI Trigger: Executes an ability when a character with a specific tag moves adjacent.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `move` | 5 ||
| `range` | Enum / Integer | Examples: `2` | 5 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Examples: `food` | 5 ||

</details>

---

### Object: `AddDamageToElementDamage`


**Definition:** Applies or references the 'AddDamageToElementDamage' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Examples: `1` | 9 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Examples: `Electric` | 9 ||

</details>

---

### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** Applies the 'AddTemporaryEffectsToBasicAttack' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fury` | Integer | Examples: `10` | 4 ||

</details>

---

### Object: `BackflipWhenTargeted`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `BackflipDodge` | 7 ||
| `stacks` | Enum / Integer | Examples: `2` | 7 ||

</details>

---

### Object: `ChanceToBackflip`


**Definition:** Applies or references the 'ChanceToBackflip' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `BackflipDodge` | 6 ||
| `chance` | Number | Examples: `10` | 6 ||

</details>

---

### Object: `ClassManaCostReduction`


**Definition:** Applies or references the 'ClassManaCostReduction' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer | Examples: `1` | 7 ||
| [`class`](./Enums.md#enum-class) | Enum | Examples: `Colorless` | 6 ||

</details>

---

### Object: `Conditional_FirstApplicationThisTurn`


**Definition:** Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 8 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 3 | |
| [`Charge`](./Enums.md) | Integer || 1 | 2 |

</details>

---

### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | Examples: `25` | 37 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 37 | |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 28 ||
| [`ChangeTilesUnder`](./Enums.md) | Enum || 1 | GlassTile |

</details>

---

### Object: `CounterAttack`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `ChainLightning` | 5 ||
| `chance` | Number | Examples: `15` | 1 ||

</details>

---

### Object: `KnockUpAndAway`


**Definition:** Displaces the target vertically and horizontally away from the source.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicMeleeAttack`](./Cat_Mutations.md#context-addstatustobasicmeleeattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | Examples: `3` | 24 ||
| `stacks` | Enum / Integer | Examples: `3` | 22 ||

</details>

---

### Object: `MoveWhenDamaged`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Array / Enum | Examples: `chaotic` | 9 ||
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Examples: `MoveOne` | 2 ||

</details>

---

### Object: `PassiveWhenAtFullMana`


**Definition:** State Trigger: Grants nested passives when at full mana.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 5 ||
| [`DamageUp`](./Enums.md) | Integer || 1 | 2 |

</details>

---

### Object: `PassiveWhileHasStatus`


**Definition:** Passive: Activates only while the character has the specified status.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | Examples: `Bleed` | 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 6 ||
| [`passives`](#object-passives) | Object || 6 ||

</details>

---

### Object: `SpawnExtraThingsOnBattleStart`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array / Integer | Examples: `[ 1 2 ]` | 31 ||
| [`object`](./Enums.md#enum-object) | Array / Enum | Examples: `RandomPickup` | 23 ||

</details>

---

### Object: `StatusEachRoundEnd`


**Definition:** Applies or references the 'StatusEachRoundEnd' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 1 ||
| [`UseAbility`](./Enums.md) | Enum || 1 | Spit |

</details>

---

### Object: `StatusEveryXSpellCastsEachTurn`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Examples: `3` | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 1 ||
| [`HealthGain`](./Enums.md) | Integer || 1 | 2 |

</details>

---

### Object: `StatusIfDidntMove`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 1 ||
| [`Charge`](./Enums.md) | Integer || 1 | 2 |

</details>

---

### Object: `StatusIfUnusedMovePoints`


**Definition:** Event Trigger: Applies nested statuses to if unused move points.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 8 ||
| [`ManaGain`](./Enums.md) | Integer || 2 | 3 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StatusOnAllyCatDeath`


**Definition:** Event Trigger: Applies nested statuses when ally cat death.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 6 ||
| [`DamageUp`](./Enums.md) | Integer || 1 | 2 |

</details>

---

### Object: `StatusOnCastSpell`


**Definition:** Event Trigger: Applies nested statuses when cast spell.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 8 ||
| [`Charge`](./Enums.md) | Integer || 4 | 2 |

</details>

---

### Object: `StatusOnDie`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 9 ||
| [`ScatterCoins`](./Enums.md) | Array / Integer || 1 | [.5] |

</details>

---

### Object: `StatusOnEatFood`


**Definition:** Event Trigger: Applies nested statuses when eat food.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 5 ||
| [`HealthRegenUp`](./Enums.md) | Integer || 1 | 2 |

</details>

---

### Object: `StatusOnKill`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 34 ||
| [`RangeUp`](./Enums.md) | Integer || 1 | 1 |

</details>

---


<details>
<summary><b>Conditional_RandomChance</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 34 ||

</details>

<details>
<summary><b>StatusKilledCharacters</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 34 ||

</details>

<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 34 ||

</details>
