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
| [`desc`](./Strings.md#string-desc) | Enum | Examples: `"MUTATION_BODY_309_DESC", "MUTATION_BODY_312_DESC", "MUTATION_BODY_301_DESC"` | 5441 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 1570 |  |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Examples: `common, melted, animal` | 981 |  |
| `cha` | Enum / Integer | Examples: `2, -1, 1` | 468 |  |
| `spd` | Enum / Integer | Examples: `1, -1, -2` | 424 |  |
| `shield` | Enum / Integer | Examples: `12, 5, 10` | 422 |  |
| `con` | Enum / Integer | Examples: `-2, -3, 1` | 416 |  |
| `int` | Enum / Integer | Examples: `2, -1, 1` | 401 |  |
| `lck` | Enum / Integer | Examples: `2, -1, 1` | 351 |  |
| `str` | Enum / Integer | Examples: `2, -1, 1` | 337 |  |
| `dex` | Enum / Integer | Examples: `2, -1, -2` | 301 |  |
| `divine_shield` | Integer | Examples: `1` | 54 |  |
| [`attack`](./Enums.md#enum-attack) | Enum | Examples: `FetusSpit` | 26 |  |
| `speed` | Array / Number | Examples: `-4` | 6 |  |
| [`override_move`](./Enums.md#enum-override_move) | Enum | Examples: `BasicJump` | 4 |  |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 2827 |  |
| [`AbilityReaction`](./Enums.md) | Enum | | 1 | SkunkTail |
| [`AbilityWhenTaggedCharacterMovesNear`](#object-abilitywhentaggedcharactermovesnear) | Object || 1 ||
| [`AddBonusMeleeRange`](./Enums.md) | Integer || 3 | 1 |
| [`AddBonusRange`](./Enums.md) | Integer || 6 | 1 |
| [`AddCorpseHealth`](./Enums.md) | Integer || 3 | 2 |
| [`AddDamageToElementDamage`](#object-adddamagetoelementdamage) | Object || 1 ||
| [`AddElementsToBasicAttack`](./Enums.md) | Enum || 13 | Ice |
| [`AddInitiative`](./Enums.md) | Integer || 1 | -20 |
| [`AddKnockbackDamage`](./Enums.md) | Integer || 2 | 1 |
| [`AddLevelUpRerolls`](./Enums.md) | Integer || 3 | 1 |
| [`AddLootMultiplier`](./Enums.md) | Integer || 1 | 1 |
| [`AddManaRegen`](./Enums.md) | Integer || 3 | 1 |
| [`AddMovement`](./Enums.md) | Integer || 3 | 1 |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object || 52 ||
| [`AddStatusToBasicMeleeAttack`](#object-addstatustobasicmeleeattack) | Object || 6 ||
| [`AddTemporaryEffectsToBasicAttack`](#object-addtemporaryeffectstobasicattack) | Object || 1 ||
| [`AllStatsUp`](./Enums.md) | Integer || 3 | 1 |
| [`AlphaTurns`](./Enums.md) | Integer || 1 | 1 |
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Object || 1 ||
| [`BackstabFront`](./Enums.md) | Integer || 1 | 1 |
| [`BackstabImmunity`](./Enums.md) | Integer || 2 | 1 |
| [`BasicAttackCantMiss`](./Enums.md) | Integer || 1 | 1 |
| [`BlacklistPickupType`](./Enums.md) | Enum || 4 | catnip |
| [`Bleed`](./Enums.md) | Array / Integer || 14 | [3] |
| [`BleedThorns`](./Enums.md) | Integer || 4 | 2 |
| [`Blind`](./Enums.md) | Array / Integer || 6 | [.10] |
| [`BoostWeaponDamage`](./Enums.md) | Integer || 1 | 1 |
| [`Brace`](./Enums.md) | Integer || 6 | 1 |
| [`Bruise`](./Enums.md) | Integer || 5 | 2 |
| [`CanRemoveCursedItems`](./Enums.md) | Integer || 1 | 1 |
| [`ChanceToBackflip`](#object-chancetobackflip) | Object || 1 ||
| [`ClassManaCostReduction`](#object-classmanacostreduction) | Object || 1 ||
| [`Confusion`](./Enums.md) | Array / Integer || 7 | [2] |
| [`ConjureBonusAbility`](./Enums.md) | Enum || 1 | random |
| [`CounterAttack`](#object-counterattack) | Object || 2 ||
| [`CritChanceUp`](./Enums.md) | Integer || 2 | 5 |
| [`DamageUp`](./Enums.md) | Integer || 4 | 2 |
| [`DepressionAura`](./Enums.md) | Integer || 1 | 1 |
| [`DisableAbilitiesWithTag`](./Enums.md) | Enum || 4 | consumable |
| [`DodgeChance`](./Enums.md) | Integer || 12 | 2 |
| [`DodgeChance_Status`](./Enums.md) | Integer || 1 | 10 |
| [`DrinkWater`](./Enums.md) | Integer || 1 | 1 |
| [`ElementImmune`](./Enums.md) | Enum || 4 | Ice |
| [`EquipRandomTemporaryItemFromPool`](./Enums.md) | Enum || 1 | pills |
| [`EquipTemporaryItem`](./Enums.md) | Enum || 2 | WaterBottle_Full |
| [`ExtraBasicAttacks`](./Enums.md) | Integer || 1 | 2 |
| [`FlatHealWhenDealDamage`](./Enums.md) | Integer || 1 | 1 |
| [`FreePathfindElement`](./Enums.md) | Enum || 1 | Water |
| [`GainManaWhenAnythingDies`](./Enums.md) | Integer || 1 | 1 |
| [`HealthRegenUp`](./Enums.md) | Integer || 14 | 2 |
| [`HouseFoodRequirementMultiplier`](./Enums.md) | Integer || 2 | 0 |
| [`IgnoreTiles`](./Enums.md) | Integer || 4 | 1 |
| [`Immobile`](./Enums.md) | Array / Integer || 5 | [.05] |
| [`KineticSpikes`](./Enums.md) | Integer || 5 | 1 |
| [`KnockbackImmunity`](./Enums.md) | Integer || 1 | 1 |
| [`MakeBasicAttackPull`](./Enums.md) | Integer || 2 | 1 |
| [`ManaCostReduction`](./Enums.md) | Integer || 1 | 1 |
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object || 7 ||
| [`MissChance`](./Enums.md) | Integer || 3 | 20 |
| [`MoveAwayFromDamageSource`](./Enums.md) | Enum || 1 | BasicJump |
| [`MoveWhenDamaged`](#object-movewhendamaged) | Object || 1 ||
| [`MulticlassLevelUp`](./Enums.md) | Enum || 4 | Hunter |
| [`PassiveWhenAffectedByElement`](#object-passivewhenaffectedbyelement) | Object || 12 ||
| [`PassiveWhenAtFullMana`](#object-passivewhenatfullmana) | Object || 1 ||
| [`PassiveWhileHasStatus`](#object-passivewhilehasstatus) | Object || 1 ||
| [`Poison`](./Enums.md) | Integer || 10 | 1 |
| [`PoisonThorns`](./Enums.md) | Integer || 2 | 2 |
| [`PoopWhenHit`](./Enums.md) | Enum || 2 | Poop |
| [`Quivered`](./Enums.md) | Array / Integer || 5 | [0.1] |
| [`RandomStatUp`](./Enums.md) | Integer || 5 | 2 |
| [`ReflectProjectiles`](./Enums.md) | Integer || 2 | 10 |
| [`ReplaceBasicAttack_Mutation`](./Enums.md) | Enum || 2 | FetusSpit |
| [`ReplaceBasicMove`](./Enums.md) | Enum || 3 | ToadJump_BasicMove |
| [`ReplaceBasicMove_Mutation`](./Enums.md) | Enum || 3 | BasicJump |
| [`RevengeDamage`](Abilities_and_Spells.md#object-revengedamage) | Object || 9 ||
| [`ShowHiddenThings`](./Enums.md) | Integer || 2 | 1 |
| [`Slow`](./Enums.md) | Array / Integer || 4 | [.1] |
| [`SpawnEachTurn`](#object-spawneachturn) | Object || 4 ||
| [`SpawnExtraThingsOnBattleStart`](#object-spawnextrathingsonbattlestart) | Object || 1 ||
| [`SpawnOnBattleStartRandomEmptyTile`](#object-spawnonbattlestartrandomemptytile) | Object || 3 ||
| [`SpawnOnDowned`](./Enums.md) | Enum || 7 | CharmedFly |
| [`SpawnThingOnDamage`](#object-spawnthingondamage) | Object || 7 ||
| [`StatusEachRoundEnd`](#object-statuseachroundend) | Object || 1 ||
| [`StatusEachTurnBegin`](#object-statuseachturnbegin) | Object || 5 ||
| [`StatusEachTurnEnd`](#object-statuseachturnend) | Object || 4 ||
| [`StatusEveryXSpellCasts`](#object-statuseveryxspellcasts) | Object || 2 ||
| [`StatusEveryXSpellCastsEachTurn`](#object-statuseveryxspellcastseachturn) | Object || 1 ||
| [`StatusIfDidntMove`](#object-statusifdidntmove) | Object || 1 ||
| [`StatusIfUnusedMovePoints`](#object-statusifunusedmovepoints) | Object || 1 ||
| [`StatusImmunity`](./Enums.md) | Array || 1 | [Freeze] |
| [`StatusKilledCharacters`](#object-statuskilledcharacters) | Object || 2 ||
| [`StatusOnAllyCatDeath`](#object-statusonallycatdeath) | Object || 1 ||
| [`StatusOnBattleEnd`](Abilities_and_Spells.md#object-statusonbattleend) | Object || 2 ||
| [`StatusOnCastSpell`](#object-statusoncastspell) | Object || 1 ||
| [`StatusOnDie`](#object-statusondie) | Object || 1 ||
| [`StatusOnEatFood`](#object-statusoneatfood) | Object || 1 ||
| [`StatusOnEndMove`](#object-statusonendmove) | Object || 2 ||
| [`StatusOnKill`](#object-statusonkill) | Object || 1 ||
| [`StatusOnTookDamage`](#object-statusontookdamage) | Object || 6 ||
| [`StatusOnTookDamageFromAbility`](#object-statusontookdamagefromability) | Object || 2 ||
| [`SwapHighestAndLowestStat`](./Enums.md) | Integer || 1 | 1 |
| [`Thorns`](./Enums.md) | Integer || 18 | 2 |
| [`Trample`](./Enums.md) | Integer || 3 | 3 |
| [`Vegan`](./Enums.md) | Integer || 2 | 1 |
| [`WaterWalk`](./Enums.md) | Integer || 5 | 1 |
| [`YOffset`](./Enums.md) | Number || 3 | .25 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 187 ||
| [`Bleed`](./Enums.md) | Array / Integer || 14 | [3] |
| [`Bruise`](./Enums.md) | Integer || 5 | 2 |
| [`Burn`](./Enums.md) | Integer || 6 | 1 |
| [`ChangeTile`](./Enums.md) | Enum || 5 | WaterTile |
| [`Charmed`](./Enums.md) | Array || 2 | [.15] |
| [`Confusion`](./Enums.md) | Array / Integer || 7 | [2] |
| [`FaceAway`](./Enums.md) | Integer || 1 | 1 |
| [`Fear`](./Enums.md) | Array || 9 | [.15] |
| [`FlatLeech`](./Enums.md) | Integer || 1 | 1 |
| [`Freeze`](./Enums.md) | Array || 3 | [0.15] |
| [`Immobile`](./Enums.md) | Array / Integer || 5 | [.05] |
| [`Instakill`](./Enums.md) | Array || 1 | [25] |
| [`Knockback`](./Enums.md) | Integer || 8 | 2 |
| [`Leeches`](./Enums.md) | Integer || 2 | 1 |
| [`Petrify`](./Enums.md) | Array || 2 | [.05] |
| [`Poison`](./Enums.md) | Integer || 10 | 1 |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object || 4 ||
| [`Slow`](./Enums.md) | Array / Integer || 4 | [.1] |
| [`SoulLink`](./Enums.md) | Integer || 1 | 1 |
| [`Stun`](./Enums.md) | Array || 3 | [.05] |
| [`VaporizeInanimate`](./Enums.md) | Integer || 1 | 1 |
| [`VisualFXTile`](./Enums.md) | Enum || 2 | fx_windSpell |
| [`Webbed`](./Enums.md) | Array || 1 | [.1] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. ||

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
| [`element`](./Enums.md#enum-element) | Array / Enum | Examples: `water` | 36 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 33 ||
| [`passives`](#object-passives) | Object || 291 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 1390 ||
| [`Blind`](./Enums.md) | Array / Integer || 6 | [.10] |
| [`Charmed`](./Enums.md) | Array || 2 | [.15] |
| [`Confusion`](./Enums.md) | Array / Integer || 7 | [2] |
| [`Fear`](./Enums.md) | Array || 9 | [.15] |
| [`Petrify`](./Enums.md) | Array || 2 | [.05] |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object || 4 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. ||

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Examples: `0` | 16 ||
| [`type`](./Enums.md#enum-type) | Enum | Examples: `status` | 10 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 10 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object || 10 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 75 ||
| `knockback` | Enum / Integer | Examples: `2, 1` | 48 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Examples: `0` | 44 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 36 ||
| [`type`](./Enums.md#enum-type) | Enum | Examples: `status` | 20 ||
| [`Freeze`](./Enums.md) | Array || 3 | [0.15] |
| [`Immobile`](./Enums.md) | Array / Integer || 5 | [.05] |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object || 10 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. ||

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
| [`object`](./Enums.md#enum-object) | Array / Enum | Examples: `CharmedFlea, SmallRock, Coin` | 76 ||
| `good` | Boolean | Examples: `false` | 40 ||
| `chance` | Number | Examples: `20, 100, 10` | 24 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 10 ||
| [`Bleed`](./Enums.md) | Array / Integer || 14 | [3] |
| [`Immobile`](./Enums.md) | Array / Integer || 5 | [.05] |
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object || 1 ||
| [`Knockback`](./Enums.md) | Integer || 8 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 40 ||
| [`ChangeTilesUnder`](./Enums.md) | Enum || 3 | GlassTile |
| [`Charge`](./Enums.md) | Integer || 10 | 2 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 11 ||
| [`MissChance`](./Enums.md) | Integer || 3 | 20 |
| [`MoveQuivered`](./Enums.md) | Array || 1 | [0.1] |
| [`Quivered`](./Enums.md) | Array / Integer || 5 | [0.1] |
| [`SpeedUp`](./Enums.md) | Integer || 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 35 ||
| [`Bleed`](./Enums.md) | Array / Integer || 14 | [3] |
| [`Blind`](./Enums.md) | Array / Integer || 6 | [.10] |
| [`Burn`](./Enums.md) | Integer || 6 | 1 |
| [`Charge`](./Enums.md) | Integer || 10 | 2 |
| [`DiminishingHealthRegen`](./Enums.md) | Integer || 2 | 1 |
| [`KineticSpikes`](./Enums.md) | Integer || 5 | 1 |
| [`Poison`](./Enums.md) | Integer || 10 | 1 |
| [`RandomStatUp`](./Enums.md) | Integer || 5 | 2 |
| [`Shield`](./Enums.md) | Integer || 3 | 1 |
| [`Thorns`](./Enums.md) | Integer || 18 | 2 |
| [`Weakness`](./Enums.md) | Integer || 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. ||

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
| `chance` | Number | Examples: `50, 5, 25` | 40 ||
| [`object`](./Enums.md#enum-object) | Array / Enum | Examples: `RandomPickup, CharmedFly, CharmedMaggot` | 34 ||
| `good` | Boolean | Examples: `false` | 4 ||

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
| [`Charge`](./Enums.md) | Integer || 10 | 2 |
| [`IntelligenceUp`](./Enums.md) | Integer || 1 | 1 |
| [`RandomStatDown`](./Enums.md) | Integer || 1 | 1 |
| [`RandomStatUp`](./Enums.md) | Integer || 5 | 2 |
| [`Shield`](./Enums.md) | Integer || 3 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. ||

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
| [`object`](./Enums.md#enum-object) | Array / Enum | Examples: `Coin, RandomFoodPickup` | 22 ||
| [`number`](./Arrays.md#array-number) | Array / Integer | Examples: `[ 1 3 ], 2` | 6 ||

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
| `odds` | Number | Examples: `10` | 8 ||
| [`AutoReanimate`](./Enums.md) | Integer || 2 | 50 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. ||
| `effects` | Object | Effects to execute. | | |

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
| `stacks` | Enum / Integer | Examples: `4, 8` | 16 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 9 ||
| [`Charge`](./Enums.md) | Integer || 10 | 2 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 58 ||
| [`FindItemFromPool`](./Enums.md) | Enum || 1 | consumables |
| [`PermanentIntelligence`](./Enums.md) | Integer || 1 | 1 |

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
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object || 4 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `move` | 10 ||
| `range` | Enum / Integer | Examples: `2` | 10 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Examples: `food` | 10 ||

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Examples: `1` | 18 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Examples: `Electric` | 18 ||

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
| `Fury` | Integer | Examples: `10` | 8 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `BackflipDodge` | 14 ||
| `stacks` | Enum / Integer | Examples: `2` | 14 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `BackflipDodge` | 12 ||
| `chance` | Number | Examples: `10` | 12 ||

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
| `reduction` | Integer | Examples: `1` | 14 ||
| [`class`](./Enums.md#enum-class) | Enum | Examples: `Colorless` | 12 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 7 ||
| [`Charge`](./Enums.md) | Integer || 10 | 2 |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

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
| `odds` | Number | Examples: `25` | 72 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 30 ||
| [`ChangeTilesUnder`](./Enums.md) | Enum || 3 | GlassTile |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

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
| [`ability`](./Enums.md#enum-ability) | Enum | Examples: `ChainLightning` | 10 ||
| `chance` | Number | Examples: `15` | 2 ||

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
| `distance` | Integer | Examples: `3` | 48 ||
| `stacks` | Enum / Integer | Examples: `3` | 44 ||

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
| [`weights`](./Enums.md#enum-weights) | Array / Enum | Examples: `chaotic` | 18 ||
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Examples: `MoveOne` | 4 ||

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
| [`DamageUp`](./Enums.md) | Integer || 4 | 2 |

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
| [`status`](./Enums.md#enum-status) | Enum | Examples: `Bleed` | 12 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 11 ||
| [`passives`](#object-passives) | Object || 291 ||

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
| [`object`](./Enums.md#enum-object) | Array / Enum | Examples: `RandomPickup` | 19 ||
| [`number`](./Arrays.md#array-number) | Array / Integer | Examples: `[ 1 2 ]` | 3 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 2 ||
| [`UseAbility`](./Enums.md) | Enum || 1 | Spit |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. ||

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
| `stacks` | Enum / Integer | Examples: `3` | 2 ||
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
| [`Charge`](./Enums.md) | Integer || 10 | 2 |

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
| [`ManaGain`](./Enums.md) | Integer || 1 | 3 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. ||

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
| [`DamageUp`](./Enums.md) | Integer || 4 | 2 |

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
| [`Charge`](./Enums.md) | Integer || 10 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 6 ||
| [`ScatterCoins`](./Enums.md) | Array / Integer || 6 | [.5] |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 6 ||
| [`HealthRegenUp`](./Enums.md) | Integer || 14 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 36 ||
| [`RangeUp`](./Enums.md) | Integer || 1 | 1 |

</details>

---


<details>
<summary><b>Conditional_RandomChance</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>StatusKilledCharacters</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 9 ||

</details>
