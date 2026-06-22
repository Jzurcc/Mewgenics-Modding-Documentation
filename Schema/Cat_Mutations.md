# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Cat Mutations

### Context: `passives`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`-2`](./Cat_Mutations.md#context--2), [`1026`](./Cat_Mutations.md#context-1026), [`1029`](./Cat_Mutations.md#context-1029), [`1500`](./Cat_Mutations.md#context-1500), [`300`](./Cat_Mutations.md#context-300), [`301`](./Cat_Mutations.md#context-301), [`302`](./Cat_Mutations.md#context-302), [`303`](./Cat_Mutations.md#context-303), [`304`](./Cat_Mutations.md#context-304), [`305`](./Cat_Mutations.md#context-305), [`306`](./Cat_Mutations.md#context-306), [`307`](./Cat_Mutations.md#context-307), [`308`](./Cat_Mutations.md#context-308), [`309`](./Cat_Mutations.md#context-309), [`310`](./Cat_Mutations.md#context-310), [`311`](./Cat_Mutations.md#context-311), [`312`](./Cat_Mutations.md#context-312), [`313`](./Cat_Mutations.md#context-313), [`314`](./Cat_Mutations.md#context-314), [`315`](./Cat_Mutations.md#context-315), [`316`](./Cat_Mutations.md#context-316), [`317`](./Cat_Mutations.md#context-317), [`318`](./Cat_Mutations.md#context-318), [`319`](./Cat_Mutations.md#context-319), [`320`](./Cat_Mutations.md#context-320), [`321`](./Cat_Mutations.md#context-321), [`322`](./Cat_Mutations.md#context-322), [`323`](./Cat_Mutations.md#context-323), [`324`](./Cat_Mutations.md#context-324), [`325`](./Cat_Mutations.md#context-325), [`326`](./Cat_Mutations.md#context-326), [`327`](./Cat_Mutations.md#context-327), [`328`](./Cat_Mutations.md#context-328), [`329`](./Cat_Mutations.md#context-329), [`330`](./Cat_Mutations.md#context-330), [`331`](./Cat_Mutations.md#context-331), [`332`](./Cat_Mutations.md#context-332), [`333`](./Cat_Mutations.md#context-333), [`334`](./Cat_Mutations.md#context-334), [`335`](./Cat_Mutations.md#context-335), [`336`](./Cat_Mutations.md#context-336), [`337`](./Cat_Mutations.md#context-337), [`338`](./Cat_Mutations.md#context-338), [`339`](./Cat_Mutations.md#context-339), [`340`](./Cat_Mutations.md#context-340), [`341`](./Cat_Mutations.md#context-341), [`342`](./Cat_Mutations.md#context-342), [`343`](./Cat_Mutations.md#context-343), [`344`](./Cat_Mutations.md#context-344), [`345`](./Cat_Mutations.md#context-345), [`346`](./Cat_Mutations.md#context-346), [`347`](./Cat_Mutations.md#context-347), [`348`](./Cat_Mutations.md#context-348), [`349`](./Cat_Mutations.md#context-349), [`351`](./Cat_Mutations.md#context-351), [`352`](./Cat_Mutations.md#context-352), [`353`](./Cat_Mutations.md#context-353), [`442`](./Cat_Mutations.md#context-442), [`702`](./Cat_Mutations.md#context-702), [`703`](./Cat_Mutations.md#context-703), [`704`](./Cat_Mutations.md#context-704), [`705`](./Cat_Mutations.md#context-705), [`706`](./Cat_Mutations.md#context-706), [`707`](./Cat_Mutations.md#context-707), [`750`](./Cat_Mutations.md#context-750), [`751`](./Cat_Mutations.md#context-751), [`752`](./Cat_Mutations.md#context-752), [`753`](./Cat_Mutations.md#context-753), [`754`](./Cat_Mutations.md#context-754), [`755`](./Cat_Mutations.md#context-755), [`756`](./Cat_Mutations.md#context-756), [`757`](./Cat_Mutations.md#context-757), [`758`](./Cat_Mutations.md#context-758), [`759`](./Cat_Mutations.md#context-759), [`760`](./Cat_Mutations.md#context-760), [`761`](./Cat_Mutations.md#context-761), [`762`](./Cat_Mutations.md#context-762), [`763`](./Cat_Mutations.md#context-763), [`900`](./Cat_Mutations.md#context-900), [`PassiveWhenAffectedByElement`](./Cat_Mutations.md#context-passivewhenaffectedbyelement), [`PassiveWhileHasStatus`](./Cat_Mutations.md#context-passivewhilehasstatus)

| Property Key | Type | Definition | Count (X/52) |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack) | Block |  | 52 |
| `Thorns` | Number |  | 16 |
| [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum/String |  | 13 |
| `HealthRegenUp` | Number |  | 13 |
| `DodgeChance` | Number |  | 12 |
| [`PassiveWhenAffectedByElement`](./Cat_Mutations.md#context-passivewhenaffectedbyelement) | Block |  | 12 |
| [`RevengeDamage`](./Cat_Mutations.md#context-revengedamage) | Block |  | 9 |
| [`MeleeRevengeDamage`](./Cat_Mutations.md#context-meleerevengedamage) | Block |  | 7 |
| [`SpawnOnDowned`](./Enums.md#enum-spawnondowned) | Enum/String |  | 7 |
| [`SpawnThingOnDamage`](./Cat_Mutations.md#context-spawnthingondamage) | Block |  | 7 |
| `AddBonusRange` | Number |  | 6 |
| [`AddStatusToBasicMeleeAttack`](./Cat_Mutations.md#context-addstatustobasicmeleeattack) | Block |  | 6 |
| `Brace` | Number |  | 6 |
| [`StatusOnTookDamage`](./Cat_Mutations.md#context-statusontookdamage) | Block |  | 6 |
| [`StatusEachTurnBegin`](./Cat_Mutations.md#context-statuseachturnbegin) | Block |  | 5 |
| `WaterWalk` | Number |  | 5 |
| [`BlacklistPickupType`](./Enums.md#enum-blacklistpickuptype) | Enum/String |  | 4 |
| `Bleed` | Number |  | 4 |
| `BleedThorns` | Number |  | 4 |
| [`DisableAbilitiesWithTag`](./Enums.md#enum-disableabilitieswithtag) | Enum/String |  | 4 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum/String |  | 4 |
| `IgnoreTiles` | Number |  | 4 |
| [`MulticlassLevelUp`](./Enums.md#enum-multiclasslevelup) | Enum/String |  | 4 |
| [`SpawnEachTurn`](./Cat_Mutations.md#context-spawneachturn) | Block |  | 4 |
| [`StatusEachTurnEnd`](./Cat_Mutations.md#context-statuseachturnend) | Block |  | 4 |
| `AddBonusMeleeRange` | Number |  | 3 |
| `AddCorpseHealth` | Number |  | 3 |
| `AddLevelUpRerolls` | Number |  | 3 |
| `AddManaRegen` | Number |  | 3 |
| `AddMovement` | Number |  | 3 |
| `AllStatsUp` | Number |  | 3 |
| `Blind` | Number |  | 3 |
| `Bruise` | Number |  | 3 |
| `KineticSpikes` | Number |  | 3 |
| `Quivered` | Number |  | 3 |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum/String |  | 3 |
| [`ReplaceBasicMove_Mutation`](./Enums.md#enum-replacebasicmove_mutation) | Enum/String |  | 3 |
| [`SpawnOnBattleStartRandomEmptyTile`](./Cat_Mutations.md#context-spawnonbattlestartrandomemptytile) | Block |  | 3 |
| `Trample` | Number |  | 3 |
| [`YOffset`](./Enums.md#enum-yoffset) | Enum/String |  | 3 |
| `AddKnockbackDamage` | Number |  | 2 |
| `BackstabImmunity` | Number |  | 2 |
| `Confusion` | Number |  | 2 |
| `CritChanceUp` | Number |  | 2 |
| `DamageUp` | Number |  | 2 |
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum/String |  | 2 |
| `HouseFoodRequirementMultiplier` | Number |  | 2 |
| `Immobile` | Number |  | 2 |
| `MissChance` | Number |  | 2 |
| `Poison` | Number |  | 2 |
| `PoisonThorns` | Number |  | 2 |
| [`PoopWhenHit`](./Enums.md#enum-poopwhenhit) | Enum/String |  | 2 |
| `ReflectProjectiles` | Number |  | 2 |
| `ShowHiddenThings` | Number |  | 2 |
| [`StatusEveryXSpellCasts`](./Cat_Mutations.md#context-statuseveryxspellcasts) | Block |  | 2 |
| [`StatusKilledCharacters`](./Cat_Mutations.md#context-statuskilledcharacters) | Block |  | 2 |
| [`StatusOnBattleEnd`](./Cat_Mutations.md#context-statusonbattleend) | Block |  | 2 |
| [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove) | Block |  | 2 |
| [`StatusOnTookDamageFromAbility`](./Cat_Mutations.md#context-statusontookdamagefromability) | Block |  | 2 |
| `Vegan` | Number |  | 2 |
| [`AbilityReaction`](./Enums.md#enum-abilityreaction) | Enum/String |  | 1 |
| [`AbilityWhenTaggedCharacterMovesNear`](./Cat_Mutations.md#context-abilitywhentaggedcharactermovesnear) | Block |  | 1 |
| [`AddDamageToElementDamage`](./Cat_Mutations.md#context-adddamagetoelementdamage) | Block |  | 1 |
| `AddInitiative` | Number |  | 1 |
| `AddLootMultiplier` | Number |  | 1 |
| [`AddTemporaryEffectsToBasicAttack`](./Cat_Mutations.md#context-addtemporaryeffectstobasicattack) | Block |  | 1 |
| `AlphaTurns` | Number |  | 1 |
| [`BackflipWhenTargeted`](./Cat_Mutations.md#context-backflipwhentargeted) | Block |  | 1 |
| `BackstabFront` | Number |  | 1 |
| `BasicAttackCantMiss` | Number |  | 1 |
| `BoostWeaponDamage` | Number |  | 1 |
| `CanRemoveCursedItems` | Number |  | 1 |
| [`ChanceToBackflip`](./Cat_Mutations.md#context-chancetobackflip) | Block |  | 1 |
| [`ClassManaCostReduction`](./Cat_Mutations.md#context-classmanacostreduction) | Block |  | 1 |
| [`ConjureBonusAbility`](./Enums.md#enum-conjurebonusability) | Enum/String |  | 1 |
| [`CounterAttack`](./Cat_Mutations.md#context-counterattack) | Block |  | 1 |
| `DepressionAura` | Number |  | 1 |
| `DodgeChance_Status` | Number |  | 1 |
| `DrinkWater` | Number |  | 1 |
| [`EquipRandomTemporaryItemFromPool`](./Enums.md#enum-equiprandomtemporaryitemfrompool) | Enum/String |  | 1 |
| `ExtraBasicAttacks` | Number |  | 1 |
| `FlatHealWhenDealDamage` | Number |  | 1 |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum/String |  | 1 |
| `GainManaWhenAnythingDies` | Number |  | 1 |
| `KnockbackImmunity` | Number |  | 1 |
| `MakeBasicAttackPull` | Number |  | 1 |
| `ManaCostReduction` | Number |  | 1 |
| [`MoveAwayFromDamageSource`](./Enums.md#enum-moveawayfromdamagesource) | Enum/String |  | 1 |
| [`MoveWhenDamaged`](./Cat_Mutations.md#context-movewhendamaged) | Block |  | 1 |
| [`PassiveWhenAtFullMana`](./Cat_Mutations.md#context-passivewhenatfullmana) | Block |  | 1 |
| [`PassiveWhileHasStatus`](./Cat_Mutations.md#context-passivewhilehasstatus) | Block |  | 1 |
| `RandomStatUp` | Number |  | 1 |
| [`ReplaceBasicAttack_Mutation`](./Enums.md#enum-replacebasicattack_mutation) | Enum/String |  | 1 |
| `Slow` | Number |  | 1 |
| [`SpawnExtraThingsOnBattleStart`](./Cat_Mutations.md#context-spawnextrathingsonbattlestart) | Block |  | 1 |
| [`StatusEachRoundEnd`](./Cat_Mutations.md#context-statuseachroundend) | Block |  | 1 |
| [`StatusEveryXSpellCastsEachTurn`](./Cat_Mutations.md#context-statuseveryxspellcastseachturn) | Block |  | 1 |
| [`StatusIfDidntMove`](./Cat_Mutations.md#context-statusifdidntmove) | Block |  | 1 |
| [`StatusIfUnusedMovePoints`](./Cat_Mutations.md#context-statusifunusedmovepoints) | Block |  | 1 |
| [`StatusImmunity`](./Arrays.md#array-statusimmunity) | Array |  | 1 |
| [`StatusOnAllyCatDeath`](./Cat_Mutations.md#context-statusonallycatdeath) | Block |  | 1 |
| [`StatusOnCastSpell`](./Cat_Mutations.md#context-statusoncastspell) | Block |  | 1 |
| [`StatusOnDie`](./Cat_Mutations.md#context-statusondie) | Block |  | 1 |
| [`StatusOnEatFood`](./Cat_Mutations.md#context-statusoneatfood) | Block |  | 1 |
| [`StatusOnKill`](./Cat_Mutations.md#context-statusonkill) | Block |  | 1 |
| `SwapHighestAndLowestStat` | Number |  | 1 |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String |  | 12 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 12 |

</details>

---

### Context: `400`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `401`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `402`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `403`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `404`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `spd` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `405`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `lck` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `406`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `407`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `dex` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `408`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `con` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `409`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `410`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `411`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `412`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `dex` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `413`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `414`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `dex` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `415`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `416`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `417`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `418`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `419`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `420`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `421`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `422`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `423`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `424`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `con` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `425`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `dex` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `426`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `427`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `int` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `428`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `429`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `430`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `431`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `432`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `433`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `lck` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `434`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `lck` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `435`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `lck` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `436`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `437`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `spd` | Number |  | 9 |
| `str` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `438`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `439`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `440`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `dex` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `441`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `lck` | Number |  | 9 |
| `spd` | Number |  | 9 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |

</details>

---

### Context: `700`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |
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

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 9 |
| `cha` | Number |  | 3 |
| `dex` | Number |  | 2 |
| `int` | Number |  | 2 |
| `spd` | Number |  | 2 |
| `lck` | Number |  | 1 |
| `shield` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| [`effects`](./Cat_Mutations.md#context-effects) | Block |  | 9 |
| `damage` | Number |  | 4 |
| [`type`](./Enums.md#enum-type) | Enum/String |  | 4 |

</details>

---

### Context: `313`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 8 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 8 |
| `divine_shield` | Number |  | 1 |
| `shield` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `314`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum/String |  | 8 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 8 |
| `cha` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `315`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 8 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 8 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `704`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 8 |
| `desc` | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
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

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 7 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 7 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 2 |
| `cha` | Number |  | 1 |
| `lck` | Number |  | 1 |

</details>

---

### Context: `317`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 7 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 7 |
| `con` | Number |  | 1 |

</details>

---

### Context: `319`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 7 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 7 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `703`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 7 |
| `desc` | String |  | 6 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 6 |
| `con` | Number |  | 2 |
| `cha` | Number |  | 1 |
| `int` | Number |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| `chance` | Number |  | 7 |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 7 |
| `good` | Boolean |  | 5 |

</details>

---

### Context: `301`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 6 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 4 |
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

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 6 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 2 |
| `divine_shield` | Number |  | 1 |

</details>

---

### Context: `702`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 6 |
| `int` | Number |  | 3 |
| `cha` | Number |  | 2 |
| `con` | Number |  | 2 |
| `desc` | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `900`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum/String |  | 6 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 6 |
| `spd` | Number |  | 2 |
| `cha` | Number |  | 1 |
| `con` | Number |  | 1 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| `Knockback` | Number |  | 6 |
| `Bleed` | Number |  | 5 |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum/String |  | 5 |
| [`Fear`](./Arrays.md#array-fear) | Array |  | 5 |
| `Poison` | Number |  | 5 |
| `Burn` | Number |  | 4 |
| [`Confusion`](./Arrays.md#array-confusion) | Array |  | 3 |
| [`Stun`](./Arrays.md#array-stun) | Array |  | 3 |
| `Bruise` | Number |  | 2 |
| `Leeches` | Number |  | 2 |
| `Slow` | Number |  | 2 |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum/String |  | 2 |
| [`Charmed`](./Arrays.md#array-charmed) | Array |  | 1 |
| `FaceAway` | Number |  | 1 |
| `FlatLeech` | Number |  | 1 |
| [`Freeze`](./Arrays.md#array-freeze) | Array |  | 1 |
| [`Immobile`](./Arrays.md#array-immobile) | Array |  | 1 |
| [`Instakill`](./Arrays.md#array-instakill) | Array |  | 1 |
| [`Petrify`](./Arrays.md#array-petrify) | Array |  | 1 |
| [`RandomStatusFromPool`](./Cat_Mutations.md#context-randomstatusfrompool) | Block |  | 1 |
| `SoulLink` | Number |  | 1 |
| `VaporizeInanimate` | Number |  | 1 |
| [`Webbed`](./Arrays.md#array-webbed) | Array |  | 1 |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| `ScatterCoins` | Number |  | 6 |

</details>

---

### Context: `-2`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 5 |
| `desc` | String |  | 2 |
| `dex` | Number |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `cha` | Number |  | 1 |

</details>

---

### Context: `302`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 4 |
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

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 4 |
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

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum/String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| `spd` | Number |  | 2 |
| `cha` | Number |  | 1 |
| `int` | Number |  | 1 |
| `shield` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `310`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `cha` | Number |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 2 |
| `int` | Number |  | 1 |
| [`override_move`](./Enums.md#enum-override_move) | Enum/String |  | 1 |
| `shield` | Number |  | 1 |

</details>

---

### Context: `311`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| `con` | Number |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `312`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| `divine_shield` | Number |  | 1 |
| `shield` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Context: `316`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| `cha` | Number |  | 1 |
| `shield` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `326`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |

</details>

---

### Context: `750`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| `cha` | Number |  | 1 |
| `int` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `754`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 5 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 5 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `300`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 4 |
| `desc` | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `str` | Number |  | 3 |
| `con` | Number |  | 2 |
| `cha` | Number |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `304`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 4 |
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

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `cha` | Number |  | 3 |
| `lck` | Number |  | 2 |
| `str` | Number |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 2 |
| `con` | Number |  | 1 |
| `int` | Number |  | 1 |

</details>

---

### Context: `320`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `shield` | Number |  | 1 |

</details>

---

### Context: `321`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `int` | Number |  | 1 |
| `shield` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `323`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `spd` | Number |  | 2 |

</details>

---

### Context: `325`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `spd` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `327`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `cha` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `328`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 2 |

</details>

---

### Context: `329`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `331`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| [`override_move`](./Enums.md#enum-override_move) | Enum/String |  | 1 |

</details>

---

### Context: `332`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `334`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `str` | Number |  | 1 |

</details>

---

### Context: `336`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `337`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `339`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| `spd` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `341`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |

</details>

---

### Context: `705`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 4 |
| `cha` | Number |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `int` | Number |  | 1 |
| `speed` | Number |  | 1 |

</details>

---

### Context: `706`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 4 |
| `desc` | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `cha` | Number |  | 2 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `755`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 4 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 4 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `knockback` | Number |  | 4 |
| `damage` | Number |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum/String |  | 2 |
| [`Freeze`](./Arrays.md#array-freeze) | Array |  | 1 |
| `Immobile` | Number |  | 1 |
| [`effects`](./Cat_Mutations.md#context-effects) | Block |  | 1 |

</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `chance` | Number |  | 4 |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 4 |
| `good` | Boolean |  | 1 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Cat_Mutations.md#context-meleerevengedamage), [`RevengeDamage`](./Cat_Mutations.md#context-revengedamage)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`Fear`](./Arrays.md#array-fear) | Array |  | 4 |
| [`Confusion`](./Arrays.md#array-confusion) | Array |  | 2 |
| [`Blind`](./Arrays.md#array-blind) | Array |  | 1 |
| [`Charmed`](./Arrays.md#array-charmed) | Array |  | 1 |
| [`Petrify`](./Arrays.md#array-petrify) | Array |  | 1 |
| [`RandomStatusFromPool`](./Cat_Mutations.md#context-randomstatusfrompool) | Block |  | 1 |

</details>

---

### Context: `1500`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 3 |
| `desc` | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `dex` | Number |  | 1 |

</details>

---

### Context: `305`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
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

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum/String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `con` | Number |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 2 |
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

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `cha` | Number |  | 1 |
| `con` | Number |  | 1 |
| `str` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `324`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `con` | Number |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `335`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |

</details>

---

### Context: `338`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |

</details>

---

### Context: `342`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `con` | Number |  | 1 |

</details>

---

### Context: `343`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `757`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `int` | Number |  | 1 |

</details>

---

### Context: `759`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 3 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 3 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 3 |
| `number` | Number |  | 2 |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `Charge` | Number |  | 3 |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum/String |  | 2 |
| `LuckUp` | Number |  | 1 |

</details>

---

### Context: `330`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |

</details>

---

### Context: `333`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `shield` | Number |  | 1 |

</details>

---

### Context: `340`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `divine_shield` | Number |  | 1 |

</details>

---

### Context: `344`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |

</details>

---

### Context: `345`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `751`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `con` | Number |  | 1 |

</details>

---

### Context: `752`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `con` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `753`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `shield` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `758`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |
| `con` | Number |  | 1 |

</details>

---

### Context: `760`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 2 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 2 |

</details>

---

### Context: `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number |  | 2 |
| `Knockback` | Number |  | 2 |
| [`Immobile`](./Arrays.md#array-immobile) | Array |  | 1 |
| [`KnockUpAndAway`](./Cat_Mutations.md#context-knockupandaway) | Block |  | 1 |

</details>

---

### Context: `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKilledCharacters`](./Cat_Mutations.md#context-statuskilledcharacters)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AutoReanimate` | Number |  | 2 |
| `odds` | Number |  | 2 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack), [`StatusOnTookDamageFromAbility`](./Cat_Mutations.md#context-statusontookdamagefromability), [`effects`](./Cat_Mutations.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number |  | 2 |
| `Blind` | Number |  | 2 |
| `Burn` | Number |  | 2 |
| `Charge` | Number |  | 2 |
| `DiminishingHealthRegen` | Number |  | 2 |
| `KineticSpikes` | Number |  | 2 |
| `Poison` | Number |  | 2 |
| `RandomStatUp` | Number |  | 2 |
| `Shield` | Number |  | 2 |
| `Thorns` | Number |  | 2 |
| `Weakness` | Number |  | 2 |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Quivered`](./Arrays.md#array-quivered) | Array |  | 2 |
| `MissChance` | Number |  | 1 |
| [`MoveQuivered`](./Arrays.md#array-movequivered) | Array |  | 1 |
| `SpeedUp` | Number |  | 1 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `RandomStatUp` | Number |  | 2 |
| `Charge` | Number |  | 1 |
| `IntelligenceUp` | Number |  | 1 |
| `RandomStatDown` | Number |  | 1 |
| `Shield` | Number |  | 1 |

</details>

---

### Context: `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `stacks` | Number |  | 2 |
| `Charge` | Number |  | 1 |
| `RandomMagicMissile` | Number |  | 1 |

</details>

---

### Context: `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Conditional_RandomChance`](./Cat_Mutations.md#context-conditional_randomchance) | Block |  | 2 |

</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](./Cat_Mutations.md#context-randomstatusfrompool) | Block |  | 2 |

</details>

---

### Context: `1026`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `1029`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `346`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| `shield` | Number |  | 1 |

</details>

---

### Context: `347`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `348`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `349`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `351`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `352`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `353`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `442`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 1 |
| `desc` | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `707`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| `str` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `756`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 1 |
| `int` | Number |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `761`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `762`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `763`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `desc` | String |  | 1 |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String |  | 1 |
| `range` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String |  | 1 |

</details>

---

### Context: `AddDamageToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `damage` | Number |  | 1 |
| [`element`](./Enums.md#enum-element) | Enum/String |  | 1 |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Fury` | Number |  | 1 |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String |  | 1 |
| `stacks` | Number |  | 1 |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String |  | 1 |
| `chance` | Number |  | 1 |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`class`](./Enums.md#enum-class) | Enum/String |  | 1 |
| `reduction` | Number |  | 1 |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Charge` | Number |  | 1 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum/String |  | 1 |
| `odds` | Number |  | 1 |

</details>

---

### Context: `CounterAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String |  | 1 |
| `chance` | Number |  | 1 |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicMeleeAttack`](./Cat_Mutations.md#context-addstatustobasicmeleeattack)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `distance` | Number |  | 1 |
| `stacks` | Number |  | 1 |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum/String |  | 1 |
| [`weights`](./Enums.md#enum-weights) | Enum/String |  | 1 |

</details>

---

### Context: `PassiveWhenAtFullMana`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number |  | 1 |

</details>

---

### Context: `PassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Cat_Mutations.md#context-passives) | Block |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum/String |  | 1 |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 1 |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 1 |

</details>

---

### Context: `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`UseAbility`](./Enums.md#enum-useability) | Enum/String |  | 1 |

</details>

---

### Context: `StatusEveryXSpellCastsEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number |  | 1 |
| `stacks` | Number |  | 1 |

</details>

---

### Context: `StatusIfDidntMove`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Charge` | Number |  | 1 |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number |  | 1 |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number |  | 1 |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum/String |  | 1 |
| `PermanentIntelligence` | Number |  | 1 |

</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Charge` | Number |  | 1 |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Number |  | 1 |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_FirstApplicationThisTurn`](./Cat_Mutations.md#context-conditional_firstapplicationthisturn) | Block |  | 1 |
| [`Conditional_GoodRoll`](./Cat_Mutations.md#context-conditional_goodroll) | Block |  | 1 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `RangeUp` | Number |  | 1 |

</details>

---

