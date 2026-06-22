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
| [`desc`](./Strings.md#string-desc) | String | Examples: `"MUTATION_BODY_309_DESC", "MUTATION_BODY_312_DESC", "MUTATION_BODY_301_DESC"` | 272 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block | Examples: `{ ... }` | 271 |
| `cha` | Number | Examples: `2, -1, 1` | 144 |
| `spd` | Number | Examples: `1, -1, -2` | 133 |
| `int` | Number | Examples: `2, -1, 1` | 132 |
| `con` | Number | Examples: `-2, -3, 1` | 131 |
| `str` | Number | Examples: `2, -1, 1` | 126 |
| `lck` | Number | Examples: `2, -1, 1` | 119 |
| `dex` | Number | Examples: `2, -1, -2` | 118 |
| [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack) | Block | Examples: `{ ... }` | 51 |
| `Thorns` | Number | Examples: `2, 1` | 16 |
| `shield` | Number | Examples: `12, 5, 10` | 16 |
| [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum | Examples: `Ice, Electric, Water` | 13 |
| `DodgeChance` | Number | Examples: `2, 5, 10` | 12 |
| [`PassiveWhenAffectedByElement`](./Cat_Mutations.md#context-passivewhenaffectedbyelement) | Block | Examples: `{ ... }` | 11 |
| [`RevengeDamage`](./Cat_Mutations.md#context-revengedamage) | Block | Examples: `{ ... }` | 9 |
| `HealthRegenUp` | Number | Examples: `2, 1` | 7 |
| [`MeleeRevengeDamage`](./Cat_Mutations.md#context-meleerevengedamage) | Block | Examples: `{ ... }` | 7 |
| [`SpawnOnDowned`](./Enums.md#enum-spawnondowned) | Enum | Examples: `CharmedKitten, CharmedFly` | 7 |
| [`SpawnThingOnDamage`](./Cat_Mutations.md#context-spawnthingondamage) | Block | Examples: `{ ... }` | 7 |
| `AddBonusRange` | Number | Examples: `1` | 6 |
| [`AddStatusToBasicMeleeAttack`](./Cat_Mutations.md#context-addstatustobasicmeleeattack) | Block | Examples: `{ ... }` | 6 |
| [`StatusOnTookDamage`](./Cat_Mutations.md#context-statusontookdamage) | Block | Examples: `{ ... }` | 6 |
| `Brace` | Number | Examples: `1` | 5 |
| [`StatusEachTurnBegin`](./Cat_Mutations.md#context-statuseachturnbegin) | Block | Examples: `{ ... }` | 5 |
| [`BlacklistPickupType`](./Enums.md#enum-blacklistpickuptype) | Enum | Examples: `food, catnip` | 4 |
| `Bleed` | Number | Examples: `1` | 4 |
| `BleedThorns` | Number | Examples: `2, 1` | 4 |
| [`DisableAbilitiesWithTag`](./Enums.md#enum-disableabilitieswithtag) | Enum | Examples: `musical, consumable` | 4 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | Examples: `Ice, Electric` | 4 |
| `IgnoreTiles` | Number | Examples: `1` | 4 |
| [`MulticlassLevelUp`](./Enums.md#enum-multiclasslevelup) | Enum | Examples: `Fighter, Mage, Hunter` | 4 |
| [`SpawnEachTurn`](./Cat_Mutations.md#context-spawneachturn) | Block | Examples: `{ ... }` | 4 |
| `WaterWalk` | Number | Examples: `1` | 4 |
| `divine_shield` | Number | Examples: `1` | 4 |
| `AddBonusMeleeRange` | Number | Examples: `1` | 3 |
| `AddCorpseHealth` | Number | Examples: `2, 100` | 3 |
| `AddLevelUpRerolls` | Number | Examples: `1` | 3 |
| `Blind` | Number | Examples: `-1` | 3 |
| `Bruise` | Number | Examples: `2, 1` | 3 |
| `KineticSpikes` | Number | Examples: `1` | 3 |
| `Quivered` | Number | Examples: `1` | 3 |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum | Examples: `Shadowstep, ToadJump_BasicMove` | 3 |
| [`ReplaceBasicMove_Mutation`](./Enums.md#enum-replacebasicmove_mutation) | Enum | Examples: `BasicJump, BasicDig` | 3 |
| [`SpawnOnBattleStartRandomEmptyTile`](./Cat_Mutations.md#context-spawnonbattlestartrandomemptytile) | Block | Examples: `{ ... }` | 3 |
| [`StatusEachTurnEnd`](./Cat_Mutations.md#context-statuseachturnend) | Block | Examples: `{ ... }` | 3 |
| `Trample` | Number | Examples: `3` | 3 |
| [`YOffset`](./Enums.md#enum-yoffset) | Enum | Examples: `.25` | 3 |
| `AddKnockbackDamage` | Number | Examples: `1` | 2 |
| `BackstabImmunity` | Number | Examples: `1` | 2 |
| `Confusion` | Number | Examples: `2` | 2 |
| `CritChanceUp` | Number | Examples: `5, 10` | 2 |
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum | Examples: `Bottles, WaterBottle_Full` | 2 |
| `HouseFoodRequirementMultiplier` | Number | Examples: `0` | 2 |
| `Immobile` | Number | Examples: `1` | 2 |
| `MissChance` | Number | Examples: `20, 10` | 2 |
| `Poison` | Number | Examples: `1` | 2 |
| `PoisonThorns` | Number | Examples: `2, 1` | 2 |
| [`PoopWhenHit`](./Enums.md#enum-poopwhenhit) | Enum | Examples: `Poop` | 2 |
| `ReflectProjectiles` | Number | Examples: `25, 10` | 2 |
| `ShowHiddenThings` | Number | Examples: `1` | 2 |
| [`StatusEveryXSpellCasts`](./Cat_Mutations.md#context-statuseveryxspellcasts) | Block | Examples: `{ ... }` | 2 |
| [`StatusKilledCharacters`](./Cat_Mutations.md#context-statuskilledcharacters) | Block | Examples: `{ ... }` | 2 |
| [`StatusOnBattleEnd`](./Cat_Mutations.md#context-statusonbattleend) | Block | Examples: `{ ... }` | 2 |
| [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove) | Block | Examples: `{ ... }` | 2 |
| [`StatusOnTookDamageFromAbility`](./Cat_Mutations.md#context-statusontookdamagefromability) | Block | Examples: `{ ... }` | 2 |
| `Vegan` | Number | Examples: `1` | 2 |
| [`override_move`](./Enums.md#enum-override_move) | Enum | Examples: `BasicJump` | 2 |
| [`AbilityReaction`](./Enums.md#enum-abilityreaction) | Enum | Examples: `SkunkTail` | 1 |
| [`AbilityWhenTaggedCharacterMovesNear`](./Cat_Mutations.md#context-abilitywhentaggedcharactermovesnear) | Block | Examples: `{ ... }` | 1 |
| [`AddDamageToElementDamage`](./Cat_Mutations.md#context-adddamagetoelementdamage) | Block | Examples: `{ ... }` | 1 |
| `AddInitiative` | Number | Examples: `-20` | 1 |
| `AddLootMultiplier` | Number | Examples: `1` | 1 |
| `AddManaRegen` | Number | Examples: `1` | 1 |
| `AddMovement` | Number | Examples: `1` | 1 |
| [`AddTemporaryEffectsToBasicAttack`](./Cat_Mutations.md#context-addtemporaryeffectstobasicattack) | Block | Examples: `{ ... }` | 1 |
| `AlphaTurns` | Number | Examples: `1` | 1 |
| [`BackflipWhenTargeted`](./Cat_Mutations.md#context-backflipwhentargeted) | Block | Examples: `{ ... }` | 1 |
| `BackstabFront` | Number | Examples: `1` | 1 |
| `BasicAttackCantMiss` | Number | Examples: `1` | 1 |
| `BoostWeaponDamage` | Number | Examples: `1` | 1 |
| `CanRemoveCursedItems` | Number | Examples: `1` | 1 |
| [`ChanceToBackflip`](./Cat_Mutations.md#context-chancetobackflip) | Block | Examples: `{ ... }` | 1 |
| [`ClassManaCostReduction`](./Cat_Mutations.md#context-classmanacostreduction) | Block | Examples: `{ ... }` | 1 |
| [`ConjureBonusAbility`](./Enums.md#enum-conjurebonusability) | Enum | Examples: `random` | 1 |
| [`CounterAttack`](./Cat_Mutations.md#context-counterattack) | Block | Examples: `{ ... }` | 1 |
| `DamageUp` | Number | Examples: `1` | 1 |
| `DepressionAura` | Number | Examples: `1` | 1 |
| `DodgeChance_Status` | Number | Examples: `10` | 1 |
| `DrinkWater` | Number | Examples: `1` | 1 |
| [`EquipRandomTemporaryItemFromPool`](./Enums.md#enum-equiprandomtemporaryitemfrompool) | Enum | Examples: `pills` | 1 |
| `ExtraBasicAttacks` | Number | Examples: `2` | 1 |
| `FlatHealWhenDealDamage` | Number | Examples: `1` | 1 |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum | Examples: `Water` | 1 |
| `GainManaWhenAnythingDies` | Number | Examples: `1` | 1 |
| `KnockbackImmunity` | Number | Examples: `1` | 1 |
| `MakeBasicAttackPull` | Number | Examples: `1` | 1 |
| `ManaCostReduction` | Number | Examples: `1` | 1 |
| [`MoveAwayFromDamageSource`](./Enums.md#enum-moveawayfromdamagesource) | Enum | Examples: `BasicJump` | 1 |
| [`MoveWhenDamaged`](./Cat_Mutations.md#context-movewhendamaged) | Block | Examples: `{ ... }` | 1 |
| [`PassiveWhenAtFullMana`](./Cat_Mutations.md#context-passivewhenatfullmana) | Block | Examples: `{ ... }` | 1 |
| [`PassiveWhileHasStatus`](./Cat_Mutations.md#context-passivewhilehasstatus) | Block | Examples: `{ ... }` | 1 |
| `RandomStatUp` | Number | Examples: `1` | 1 |
| [`ReplaceBasicAttack_Mutation`](./Enums.md#enum-replacebasicattack_mutation) | Enum | Examples: `FetusSpit` | 1 |
| `Slow` | Number | Examples: `-1` | 1 |
| [`SpawnExtraThingsOnBattleStart`](./Cat_Mutations.md#context-spawnextrathingsonbattlestart) | Block | Examples: `{ ... }` | 1 |
| [`StatusEachRoundEnd`](./Cat_Mutations.md#context-statuseachroundend) | Block | Examples: `{ ... }` | 1 |
| [`StatusEveryXSpellCastsEachTurn`](./Cat_Mutations.md#context-statuseveryxspellcastseachturn) | Block | Examples: `{ ... }` | 1 |
| [`StatusIfDidntMove`](./Cat_Mutations.md#context-statusifdidntmove) | Block | Examples: `{ ... }` | 1 |
| [`StatusIfUnusedMovePoints`](./Cat_Mutations.md#context-statusifunusedmovepoints) | Block | Examples: `{ ... }` | 1 |
| [`StatusImmunity`](./Arrays.md#array-statusimmunity) | Array | Examples: `[ Freeze Slow ]` | 1 |
| [`StatusOnAllyCatDeath`](./Cat_Mutations.md#context-statusonallycatdeath) | Block | Examples: `{ ... }` | 1 |
| [`StatusOnCastSpell`](./Cat_Mutations.md#context-statusoncastspell) | Block | Examples: `{ ... }` | 1 |
| [`StatusOnDie`](./Cat_Mutations.md#context-statusondie) | Block | Examples: `{ ... }` | 1 |
| [`StatusOnEatFood`](./Cat_Mutations.md#context-statusoneatfood) | Block | Examples: `{ ... }` | 1 |
| [`StatusOnKill`](./Cat_Mutations.md#context-statusonkill) | Block | Examples: `{ ... }` | 1 |
| `SwapHighestAndLowestStat` | Number | Examples: `1` | 1 |
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
| `HealthRegenUp` | Number | Examples: `2, 1` | 6 |
| `AllStatsUp` | Number | Examples: `1` | 3 |
| `AddManaRegen` | Number | Examples: `1` | 2 |
| `AddMovement` | Number | Examples: `1` | 2 |
| [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack) | Block | Examples: `{ ... }` | 1 |
| `Brace` | Number | Examples: `1` | 1 |
| `DamageUp` | Number | Examples: `2` | 1 |
| [`PassiveWhenAffectedByElement`](./Cat_Mutations.md#context-passivewhenaffectedbyelement) | Block | Examples: `{ ... }` | 1 |
| [`StatusEachTurnEnd`](./Cat_Mutations.md#context-statuseachturnend) | Block | Examples: `{ ... }` | 1 |
| `WaterWalk` | Number | Examples: `1` | 1 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 52

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Knockback` | Number | Examples: `2, 1` | 6 |
| [`Bleed`](./Arrays.md#array-bleed) | Array | Examples: `[ 3 .1 ], 1` | 5 |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum | Examples: `WaterTile, DirtTile` | 5 |
| [`Fear`](./Arrays.md#array-fear) | Array | Examples: `[ 1 .1 ], [ 1 .15 ], [ 1 .05 ]` | 5 |
| `Poison` | Number | Examples: `1` | 5 |
| `Burn` | Number | Examples: `1` | 4 |
| [`Confusion`](./Arrays.md#array-confusion) | Array | Examples: `[ 3 .1 ], [ 1 .15 ], [ 2 .15 ]` | 3 |
| [`Stun`](./Arrays.md#array-stun) | Array | Examples: `[ 1 .05 ]` | 3 |
| `Bruise` | Number | Examples: `1` | 2 |
| `Leeches` | Number | Examples: `1` | 2 |
| [`Slow`](./Arrays.md#array-slow) | Array | Examples: `[ 1 .1 ], 1` | 2 |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum | Examples: `fx_windSpell` | 2 |
| [`Charmed`](./Arrays.md#array-charmed) | Array | Examples: `[ 1 .10 ]` | 1 |
| `FaceAway` | Number | Examples: `1` | 1 |
| `FlatLeech` | Number | Examples: `1` | 1 |
| [`Freeze`](./Arrays.md#array-freeze) | Array | Examples: `[ 1 .01 ]` | 1 |
| [`Immobile`](./Arrays.md#array-immobile) | Array | Examples: `[ 1 .05 ]` | 1 |
| [`Instakill`](./Arrays.md#array-instakill) | Array | Examples: `[ 25 .01 ]` | 1 |
| [`Petrify`](./Arrays.md#array-petrify) | Array | Examples: `[ 1 .05 ]` | 1 |
| [`RandomStatusFromPool`](./Cat_Mutations.md#context-randomstatusfrompool) | Block | Examples: `{ ... }` | 1 |
| `SoulLink` | Number | Examples: `1` | 1 |
| `VaporizeInanimate` | Number | Examples: `1` | 1 |
| [`Webbed`](./Arrays.md#array-webbed) | Array | Examples: `[ 1 .1 ]` | 1 |

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
| [`passives`](./Cat_Mutations.md#context-passives) | Block | Examples: `{ ... }` | 12 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`MeleeRevengeDamage`](./Cat_Mutations.md#context-meleerevengedamage), [`RevengeDamage`](./Cat_Mutations.md#context-revengedamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Fear`](./Arrays.md#array-fear) | Array | Examples: `[ 1 .05 ]` | 4 |
| [`Confusion`](./Arrays.md#array-confusion) | Array | Examples: `[ 1 .1 ]` | 2 |
| [`Blind`](./Arrays.md#array-blind) | Array | Examples: `[ 1 .10 ]` | 1 |
| [`Charmed`](./Arrays.md#array-charmed) | Array | Examples: `[ 1 .15 ]` | 1 |
| [`Petrify`](./Arrays.md#array-petrify) | Array | Examples: `[ 1 .05 ]` | 1 |
| [`RandomStatusFromPool`](./Cat_Mutations.md#context-randomstatusfrompool) | Block | Examples: `{ ... }` | 1 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Cat_Mutations.md#context-effects) | Block | Examples: `{ ... }` | 9 |
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
| [`Freeze`](./Arrays.md#array-freeze) | Array | Examples: `[ 1 0.15 ]` | 1 |
| `Immobile` | Number | Examples: `10` | 1 |
| [`effects`](./Cat_Mutations.md#context-effects) | Block | Examples: `{ ... }` | 1 |

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
| `Bleed` | Number | Examples: `1` | 2 |
| `Knockback` | Number | Examples: `1` | 2 |
| [`Immobile`](./Arrays.md#array-immobile) | Array | Examples: `[ 1 .1 ]` | 1 |
| [`KnockUpAndAway`](./Cat_Mutations.md#context-knockupandaway) | Block | Examples: `{ ... }` | 1 |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | Examples: `1` | 3 |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | Examples: `GlassTile` | 2 |
| `LuckUp` | Number | Examples: `1` | 1 |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Quivered`](./Arrays.md#array-quivered) | Array | Examples: `[ 1 0.1 ]` | 2 |
| `MissChance` | Number | Examples: `5` | 1 |
| [`MoveQuivered`](./Arrays.md#array-movequivered) | Array | Examples: `[ 1 0.1 ]` | 1 |
| `SpeedUp` | Number | Examples: `1` | 1 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack), [`StatusOnTookDamageFromAbility`](./Cat_Mutations.md#context-statusontookdamagefromability), [`effects`](./Cat_Mutations.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | Examples: `1` | 2 |
| `Blind` | Number | Examples: `1` | 2 |
| `Burn` | Number | Examples: `1` | 2 |
| `Charge` | Number | Examples: `1` | 2 |
| `DiminishingHealthRegen` | Number | Examples: `1` | 2 |
| `KineticSpikes` | Number | Examples: `1` | 2 |
| `Poison` | Number | Examples: `1` | 2 |
| `RandomStatUp` | Number | Examples: `1` | 2 |
| `Shield` | Number | Examples: `1` | 2 |
| `Thorns` | Number | Examples: `1` | 2 |
| `Weakness` | Number | Examples: `1` | 2 |

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
| `RandomStatUp` | Number | Examples: `2, 1` | 2 |
| `Charge` | Number | Examples: `1` | 1 |
| `IntelligenceUp` | Number | Examples: `1` | 1 |
| `RandomStatDown` | Number | Examples: `1` | 1 |
| `Shield` | Number | Examples: `1` | 1 |

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
| `AutoReanimate` | Number | Examples: `50` | 2 |
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
| `Charge` | Number | Examples: `2` | 1 |
| `RandomMagicMissile` | Number | Examples: `4` | 1 |

</details>

---

### Context: `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_RandomChance`](./Cat_Mutations.md#context-conditional_randomchance) | Block | Examples: `{ ... }` | 2 |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum | Examples: `consumables` | 1 |
| `PermanentIntelligence` | Number | Examples: `1` | 1 |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_FirstApplicationThisTurn`](./Cat_Mutations.md#context-conditional_firstapplicationthisturn) | Block | Examples: `{ ... }` | 1 |
| [`Conditional_GoodRoll`](./Cat_Mutations.md#context-conditional_goodroll) | Block | Examples: `{ ... }` | 1 |

</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](./Cat_Mutations.md#context-randomstatusfrompool) | Block | Examples: `{ ... }` | 2 |

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
| `Charge` | Number | Examples: `1` | 1 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | Examples: `TallGrassTile` | 1 |
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
| `DamageUp` | Number | Examples: `2` | 1 |

</details>

---

### Context: `PassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Cat_Mutations.md#context-passives) | Block | Examples: `{ ... }` | 1 |
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
| [`UseAbility`](./Enums.md#enum-useability) | Enum | Examples: `Spit` | 1 |

</details>

---

### Context: `StatusEveryXSpellCastsEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | Examples: `2` | 1 |
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
| `Charge` | Number | Examples: `3` | 1 |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | Examples: `3` | 1 |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | Examples: `2` | 1 |

</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | Examples: `1` | 1 |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ScatterCoins`](./Arrays.md#array-scattercoins) | Array | Examples: `5, [ 1 .5 ]` | 6 |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Number | Examples: `1` | 1 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RangeUp` | Number | Examples: `1` | 1 |

</details>

---

