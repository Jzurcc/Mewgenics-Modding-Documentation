# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Cat Mutations

### Context: `passives`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`-2`](./Cat_Mutations.md#context--2), [`1026`](./Cat_Mutations.md#context-1026), [`1029`](./Cat_Mutations.md#context-1029), [`1500`](./Cat_Mutations.md#context-1500), [`300`](./Cat_Mutations.md#context-300), [`301`](./Cat_Mutations.md#context-301), [`302`](./Cat_Mutations.md#context-302), [`303`](./Cat_Mutations.md#context-303), [`304`](./Cat_Mutations.md#context-304), [`305`](./Cat_Mutations.md#context-305), [`306`](./Cat_Mutations.md#context-306), [`307`](./Cat_Mutations.md#context-307), [`308`](./Cat_Mutations.md#context-308), [`309`](./Cat_Mutations.md#context-309), [`310`](./Cat_Mutations.md#context-310), [`311`](./Cat_Mutations.md#context-311), [`312`](./Cat_Mutations.md#context-312), [`313`](./Cat_Mutations.md#context-313), [`314`](./Cat_Mutations.md#context-314), [`315`](./Cat_Mutations.md#context-315), [`316`](./Cat_Mutations.md#context-316), [`317`](./Cat_Mutations.md#context-317), [`318`](./Cat_Mutations.md#context-318), [`319`](./Cat_Mutations.md#context-319), [`320`](./Cat_Mutations.md#context-320), [`321`](./Cat_Mutations.md#context-321), [`322`](./Cat_Mutations.md#context-322), [`323`](./Cat_Mutations.md#context-323), [`324`](./Cat_Mutations.md#context-324), [`325`](./Cat_Mutations.md#context-325), [`326`](./Cat_Mutations.md#context-326), [`327`](./Cat_Mutations.md#context-327), [`328`](./Cat_Mutations.md#context-328), [`329`](./Cat_Mutations.md#context-329), [`330`](./Cat_Mutations.md#context-330), [`331`](./Cat_Mutations.md#context-331), [`332`](./Cat_Mutations.md#context-332), [`333`](./Cat_Mutations.md#context-333), [`334`](./Cat_Mutations.md#context-334), [`335`](./Cat_Mutations.md#context-335), [`336`](./Cat_Mutations.md#context-336), [`337`](./Cat_Mutations.md#context-337), [`338`](./Cat_Mutations.md#context-338), [`339`](./Cat_Mutations.md#context-339), [`340`](./Cat_Mutations.md#context-340), [`341`](./Cat_Mutations.md#context-341), [`342`](./Cat_Mutations.md#context-342), [`343`](./Cat_Mutations.md#context-343), [`344`](./Cat_Mutations.md#context-344), [`345`](./Cat_Mutations.md#context-345), [`346`](./Cat_Mutations.md#context-346), [`347`](./Cat_Mutations.md#context-347), [`348`](./Cat_Mutations.md#context-348), [`349`](./Cat_Mutations.md#context-349), [`351`](./Cat_Mutations.md#context-351), [`352`](./Cat_Mutations.md#context-352), [`353`](./Cat_Mutations.md#context-353), [`442`](./Cat_Mutations.md#context-442), [`702`](./Cat_Mutations.md#context-702), [`703`](./Cat_Mutations.md#context-703), [`704`](./Cat_Mutations.md#context-704), [`705`](./Cat_Mutations.md#context-705), [`706`](./Cat_Mutations.md#context-706), [`707`](./Cat_Mutations.md#context-707), [`750`](./Cat_Mutations.md#context-750), [`751`](./Cat_Mutations.md#context-751), [`752`](./Cat_Mutations.md#context-752), [`753`](./Cat_Mutations.md#context-753), [`754`](./Cat_Mutations.md#context-754), [`755`](./Cat_Mutations.md#context-755), [`756`](./Cat_Mutations.md#context-756), [`757`](./Cat_Mutations.md#context-757), [`758`](./Cat_Mutations.md#context-758), [`759`](./Cat_Mutations.md#context-759), [`760`](./Cat_Mutations.md#context-760), [`761`](./Cat_Mutations.md#context-761), [`762`](./Cat_Mutations.md#context-762), [`763`](./Cat_Mutations.md#context-763), [`900`](./Cat_Mutations.md#context-900), [`PassiveWhenAffectedByElement`](./Cat_Mutations.md#context-passivewhenaffectedbyelement), [`PassiveWhileHasStatus`](./Cat_Mutations.md#context-passivewhilehasstatus)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddStatusToBasicAttack` | [`Block`](./Cat_Mutations.md#context-addstatustobasicattack) | `{ ... }` |  |
| `Thorns` | Number | `2, 1` |  |
| `AddElementsToBasicAttack` | [`Enum/String`](./Enums.md#enum-addelementstobasicattack) | `Electric, Water, Ice` |  |
| `HealthRegenUp` | Number | `2, 1` |  |
| `DodgeChance` | Number | `5%, 10%, 2%` |  |
| `PassiveWhenAffectedByElement` | [`Block`](./Cat_Mutations.md#context-passivewhenaffectedbyelement) | `{ ... }` |  |
| `RevengeDamage` | [`Block`](./Cat_Mutations.md#context-revengedamage) | `{ ... }` |  |
| `MeleeRevengeDamage` | [`Block`](./Cat_Mutations.md#context-meleerevengedamage) | `{ ... }` |  |
| `SpawnOnDowned` | [`Enum/String`](./Enums.md#enum-spawnondowned) | `CharmedFly, CharmedKitten` |  |
| `SpawnThingOnDamage` | [`Block`](./Cat_Mutations.md#context-spawnthingondamage) | `{ ... }` |  |
| `AddBonusRange` | Number | `1` |  |
| `AddStatusToBasicMeleeAttack` | [`Block`](./Cat_Mutations.md#context-addstatustobasicmeleeattack) | `{ ... }` |  |
| `Brace` | Number | `1` |  |
| `StatusOnTookDamage` | [`Block`](./Cat_Mutations.md#context-statusontookdamage) | `{ ... }` |  |
| `StatusEachTurnBegin` | [`Block`](./Cat_Mutations.md#context-statuseachturnbegin) | `{ ... }` |  |
| `WaterWalk` | Number | `1` |  |
| `BlacklistPickupType` | [`Enum/String`](./Enums.md#enum-blacklistpickuptype) | `catnip, food` |  |
| `Bleed` | Number | `1` |  |
| `BleedThorns` | Number | `2, 1` |  |
| `DisableAbilitiesWithTag` | [`Enum/String`](./Enums.md#enum-disableabilitieswithtag) | `musical, consumable` |  |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Electric, Ice` |  |
| `IgnoreTiles` | Number | `1` |  |
| `MulticlassLevelUp` | [`Enum/String`](./Enums.md#enum-multiclasslevelup) | `Fighter, Mage, Hunter` |  |
| `SpawnEachTurn` | [`Block`](./Cat_Mutations.md#context-spawneachturn) | `{ ... }` |  |
| `StatusEachTurnEnd` | [`Block`](./Cat_Mutations.md#context-statuseachturnend) | `{ ... }` |  |
| `AddBonusMeleeRange` | Number | `1` |  |
| `AddCorpseHealth` | Number | `2, 100` |  |
| `AddLevelUpRerolls` | Number | `1` |  |
| `AddManaRegen` | Number | `1` |  |
| `AddMovement` | Number | `1` |  |
| `AllStatsUp` | Number | `1` |  |
| `Blind` | Number | `-1` |  |
| `Bruise` | Number | `2, 1` |  |
| `KineticSpikes` | Number | `1` |  |
| `Quivered` | Number | `1` |  |
| `ReplaceBasicMove` | [`Enum/String`](./Enums.md#enum-replacebasicmove) | `ToadJump_BasicMove, Shadowstep` |  |
| `ReplaceBasicMove_Mutation` | [`Enum/String`](./Enums.md#enum-replacebasicmove_mutation) | `BasicDig, BasicJump` |  |
| `SpawnOnBattleStartRandomEmptyTile` | [`Block`](./Cat_Mutations.md#context-spawnonbattlestartrandomemptytile) | `{ ... }` |  |
| `Trample` | Number | `3` |  |
| `YOffset` | [`Enum/String`](./Enums.md#enum-yoffset) | `.25` |  |
| `AddKnockbackDamage` | Number | `1` |  |
| `BackstabImmunity` | Number | `1` |  |
| `Confusion` | Number | `2` |  |
| `CritChanceUp` | Number | `10, 5` |  |
| `DamageUp` | Number | `2, 1` |  |
| `EquipTemporaryItem` | [`Enum/String`](./Enums.md#enum-equiptemporaryitem) | `Bottles, WaterBottle_Full` |  |
| `HouseFoodRequirementMultiplier` | Number | `0` |  |
| `Immobile` | Number | `1` |  |
| `MissChance` | Number | `10, 20` |  |
| `Poison` | Number | `1` |  |
| `PoisonThorns` | Number | `2, 1` |  |
| `PoopWhenHit` | [`Enum/String`](./Enums.md#enum-poopwhenhit) | `Poop` |  |
| `ReflectProjectiles` | Number | `25%, 10%` |  |
| `ShowHiddenThings` | Number | `1` |  |
| `StatusEveryXSpellCasts` | [`Block`](./Cat_Mutations.md#context-statuseveryxspellcasts) | `{ ... }` |  |
| `StatusKilledCharacters` | [`Block`](./Cat_Mutations.md#context-statuskilledcharacters) | `{ ... }` |  |
| `StatusOnBattleEnd` | [`Block`](./Cat_Mutations.md#context-statusonbattleend) | `{ ... }` |  |
| `StatusOnEndMove` | [`Block`](./Cat_Mutations.md#context-statusonendmove) | `{ ... }` |  |
| `StatusOnTookDamageFromAbility` | [`Block`](./Cat_Mutations.md#context-statusontookdamagefromability) | `{ ... }` |  |
| `Vegan` | Number | `1` |  |
| `AbilityReaction` | [`Enum/String`](./Enums.md#enum-abilityreaction) | `SkunkTail` |  |
| `AbilityWhenTaggedCharacterMovesNear` | [`Block`](./Cat_Mutations.md#context-abilitywhentaggedcharactermovesnear) | `{ ... }` |  |
| `AddDamageToElementDamage` | [`Block`](./Cat_Mutations.md#context-adddamagetoelementdamage) | `{ ... }` |  |
| `AddInitiative` | Number | `-20` |  |
| `AddLootMultiplier` | Number | `1` |  |
| `AddTemporaryEffectsToBasicAttack` | [`Block`](./Cat_Mutations.md#context-addtemporaryeffectstobasicattack) | `{ ... }` |  |
| `AlphaTurns` | Number | `1` |  |
| `BackflipWhenTargeted` | [`Block`](./Cat_Mutations.md#context-backflipwhentargeted) | `{ ... }` |  |
| `BackstabFront` | Number | `1` |  |
| `BasicAttackCantMiss` | Number | `1` |  |
| `BoostWeaponDamage` | Number | `1` |  |
| `CanRemoveCursedItems` | Number | `1` |  |
| `ChanceToBackflip` | [`Block`](./Cat_Mutations.md#context-chancetobackflip) | `{ ... }` |  |
| `ClassManaCostReduction` | [`Block`](./Cat_Mutations.md#context-classmanacostreduction) | `{ ... }` |  |
| `ConjureBonusAbility` | [`Enum/String`](./Enums.md#enum-conjurebonusability) | `random` |  |
| `CounterAttack` | [`Block`](./Cat_Mutations.md#context-counterattack) | `{ ... }` |  |
| `DepressionAura` | Number | `1` |  |
| `DodgeChance_Status` | Number | `10` |  |
| `DrinkWater` | Number | `1` |  |
| `EquipRandomTemporaryItemFromPool` | [`Enum/String`](./Enums.md#enum-equiprandomtemporaryitemfrompool) | `pills` |  |
| `ExtraBasicAttacks` | Number | `2` |  |
| `FlatHealWhenDealDamage` | Number | `1` |  |
| `FreePathfindElement` | [`Enum/String`](./Enums.md#enum-freepathfindelement) | `Water` |  |
| `GainManaWhenAnythingDies` | Number | `1` |  |
| `KnockbackImmunity` | Number | `1` |  |
| `MakeBasicAttackPull` | Number | `1` |  |
| `ManaCostReduction` | Number | `1` |  |
| `MoveAwayFromDamageSource` | [`Enum/String`](./Enums.md#enum-moveawayfromdamagesource) | `BasicJump` |  |
| `MoveWhenDamaged` | [`Block`](./Cat_Mutations.md#context-movewhendamaged) | `{ ... }` |  |
| `PassiveWhenAtFullMana` | [`Block`](./Cat_Mutations.md#context-passivewhenatfullmana) | `{ ... }` |  |
| `PassiveWhileHasStatus` | [`Block`](./Cat_Mutations.md#context-passivewhilehasstatus) | `{ ... }` |  |
| `RandomStatUp` | Number | `1` |  |
| `ReplaceBasicAttack_Mutation` | [`Enum/String`](./Enums.md#enum-replacebasicattack_mutation) | `FetusSpit` |  |
| `Slow` | Number | `-1` |  |
| `SpawnExtraThingsOnBattleStart` | [`Block`](./Cat_Mutations.md#context-spawnextrathingsonbattlestart) | `{ ... }` |  |
| `StatusEachRoundEnd` | [`Block`](./Cat_Mutations.md#context-statuseachroundend) | `{ ... }` |  |
| `StatusEveryXSpellCastsEachTurn` | [`Block`](./Cat_Mutations.md#context-statuseveryxspellcastseachturn) | `{ ... }` |  |
| `StatusIfDidntMove` | [`Block`](./Cat_Mutations.md#context-statusifdidntmove) | `{ ... }` |  |
| `StatusIfUnusedMovePoints` | [`Block`](./Cat_Mutations.md#context-statusifunusedmovepoints) | `{ ... }` |  |
| `StatusImmunity` | [`Array`](./Arrays.md#array-statusimmunity) | `[ Freeze, Slow ]` |  |
| `StatusOnAllyCatDeath` | [`Block`](./Cat_Mutations.md#context-statusonallycatdeath) | `{ ... }` |  |
| `StatusOnCastSpell` | [`Block`](./Cat_Mutations.md#context-statusoncastspell) | `{ ... }` |  |
| `StatusOnDie` | [`Block`](./Cat_Mutations.md#context-statusondie) | `{ ... }` |  |
| `StatusOnEatFood` | [`Block`](./Cat_Mutations.md#context-statusoneatfood) | `{ ... }` |  |
| `StatusOnKill` | [`Block`](./Cat_Mutations.md#context-statusonkill) | `{ ... }` |  |
| `SwapHighestAndLowestStat` | Number | `1` |  |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Knockback` | Number | `2, 1` |  |
| `Bleed` | [`Array`](./Arrays.md#array-bleed) | `[ 3, .1 ], 1` |  |
| `ChangeTile` | [`Enum/String`](./Enums.md#enum-changetile) | `WaterTile, DirtTile` |  |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1 .1 ], [ 1 .15 ], [ 1, .05 ]` |  |
| `Poison` | Number | `1` |  |
| `Burn` | Number | `1` |  |
| `Confusion` | [`Array`](./Arrays.md#array-confusion) | `[ 3, .1 ], [ 2, .15 ], [ 1, .15 ]` |  |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .05 ], [ 1, .05 ]` |  |
| `Bruise` | Number | `1` |  |
| `Leeches` | Number | `1` |  |
| `Slow` | [`Array`](./Arrays.md#array-slow) | `[ 1 .1 ], 1` |  |
| `VisualFXTile` | [`Enum/String`](./Enums.md#enum-visualfxtile) | `fx_windSpell` |  |
| `Charmed` | [`Array`](./Arrays.md#array-charmed) | `[ 1, .10 ]` |  |
| `FaceAway` | Number | `1` |  |
| `FlatLeech` | Number | `1` |  |
| `Freeze` | [`Array`](./Arrays.md#array-freeze) | `[ 1 .01 ]` |  |
| `Immobile` | [`Array`](./Arrays.md#array-immobile) | `[ 1, .05 ]` |  |
| `Instakill` | [`Array`](./Arrays.md#array-instakill) | `[ 25, .01 ]` |  |
| `Petrify` | [`Array`](./Arrays.md#array-petrify) | `[ 1, .05 ]` |  |
| `RandomStatusFromPool` | [`Block`](./Cat_Mutations.md#context-randomstatusfrompool) | `{ ... }` |  |
| `SoulLink` | Number | `1` |  |
| `VaporizeInanimate` | Number | `1` |  |
| `Webbed` | [`Array`](./Arrays.md#array-webbed) | `[ 1 .1 ]` |  |

</details>

---

### Context: `400`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `-1` |  |
| `str` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `401`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `-1` |  |
| `str` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `402`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `-1` |  |
| `str` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `403`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `-1` |  |
| `str` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `404`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spd` | Number | `-1` |  |
| `str` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `405`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `lck` | Number | `-1` |  |
| `str` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `406`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2` |  |
| `str` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `407`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2` |  |
| `dex` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `408`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `-1` |  |
| `con` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `409`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2` |  |
| `int` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `410`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2` |  |
| `spd` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `411`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2` |  |
| `lck` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `412`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `-1` |  |
| `dex` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `413`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `2` |  |
| `str` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `414`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `-1` |  |
| `dex` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `415`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `2` |  |
| `int` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `416`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `2` |  |
| `spd` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `417`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `2` |  |
| `lck` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `418`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `-1` |  |
| `int` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `419`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `-1` |  |
| `int` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `420`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `-1` |  |
| `int` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `421`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `2` |  |
| `str` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `422`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `2` |  |
| `spd` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `423`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `2` |  |
| `lck` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `424`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2` |  |
| `con` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `425`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2` |  |
| `dex` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `426`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2` |  |
| `str` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `427`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2` |  |
| `int` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `428`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2` |  |
| `spd` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `429`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2` |  |
| `lck` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `430`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `-1` |  |
| `lck` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `431`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `-1` |  |
| `lck` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `432`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `-1` |  |
| `lck` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `433`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `-1` |  |
| `lck` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `434`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `lck` | Number | `2` |  |
| `spd` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `435`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `lck` | Number | `2` |  |
| `str` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `436`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `-1` |  |
| `spd` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `437`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spd` | Number | `2` |  |
| `str` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `438`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `-1` |  |
| `spd` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `439`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `-1` |  |
| `spd` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `440`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `-1` |  |
| `spd` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `441`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `lck` | Number | `-1` |  |
| `spd` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `704`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `desc` | String | `"MUTATION_HEAD_704_DESC", "MUTATION_EYES_704_DESC", "MUTATION_EARS_704_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `-2` |  |
| `str` | Number | `1, -1` |  |
| `con` | Number | `2` |  |
| `lck` | Number | `-2` |  |
| `spd` | Number | `-3` |  |

</details>

---

### Context: `703`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `desc` | String | `"MUTATION_EARS_703_DESC", "MUTATION_HEAD_703_DESC", "MUTATION_BODY_703_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `1` |  |
| `cha` | Number | `-2` |  |
| `int` | Number | `-2` |  |
| `spd` | Number | `-2` |  |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `water` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `301`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_BODY_301_DESC", "MUTATION_LEGS_301_DESC", MUTATION_EYEBROWS_301_DESC` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |
| `int` | Number | `1, -1` |  |
| `con` | Number | `1` |  |
| `dex` | Number | `1` |  |
| `spd` | Number | `1` |  |
| `str` | Number | `1` |  |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack), [`StatusOnTookDamageFromAbility`](./Cat_Mutations.md#context-statusontookdamagefromability), [`effects`](./Cat_Mutations.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` |  |
| `Blind` | Number | `1` |  |
| `Burn` | Number | `1` |  |
| `Charge` | Number | `1` |  |
| `DiminishingHealthRegen` | Number | `1` |  |
| `KineticSpikes` | Number | `1` |  |
| `Poison` | Number | `1` |  |
| `RandomStatUp` | Number | `1` |  |
| `Shield` | Number | `1` |  |
| `Thorns` | Number | `1` |  |
| `Weakness` | Number | `1` |  |

</details>

---

### Context: `303`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_303_DESC", "MUTATION_HEAD_303_DESC", "MUTATION_LEGS_303_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `melted, animal` |  |
| `cha` | Number | `1` |  |
| `int` | Number | `1` |  |
| `shield` | Number | `10` |  |
| `spd` | Number | `-2` |  |
| `str` | Number | `1` |  |

</details>

---

### Context: `701`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `cha` | Number | `-2, -1` |  |
| `dex` | Number | `-2, -1` |  |
| `int` | Number | `-2` |  |
| `spd` | Number | `-2, -1` |  |
| `lck` | Number | `-2` |  |
| `shield` | Number | `1` |  |
| `str` | Number | `-1` |  |

</details>

---

### Context: `302`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_302_DESC", "MUTATION_LEGS_302_DESC", "MUTATION_EYES_302_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |
| `shield` | Number | `2, 5` |  |
| `con` | Number | `-1` |  |
| `int` | Number | `2` |  |
| `lck` | Number | `1` |  |
| `spd` | Number | `-1` |  |

</details>

---

### Context: `304`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_HEAD_304_DESC", "MUTATION_EYES_304_DESC", "MUTATION_MOUTH_304_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `melted, animal` |  |
| `cha` | Number | `-2, 1` |  |
| `dex` | Number | `1` |  |
| `int` | Number | `1` |  |
| `spd` | Number | `1` |  |
| `str` | Number | `1` |  |

</details>

---

### Context: `308`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_308_DESC", "MUTATION_MOUTH_308_DESC", "MUTATION_HEAD_308_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `1, -1` |  |
| `lck` | Number | `1` |  |
| `str` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |
| `con` | Number | `1` |  |
| `int` | Number | `-1` |  |

</details>

---

### Context: `313`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | [`Enum/String`](./Enums.md#enum-desc) | `MUTATION_EYEBROWS_313_DESC, "MUTATION_EARS_313_DESC", "MUTATION_BODY_313_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `divine_shield` | Number | `1` |  |
| `shield` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `20%, 100%, 10%` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `SmallRock, CharmedFlea, Coin` |  |
| `good` | Boolean | `false` |  |

</details>

---

### Context: `309`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_BODY_309_DESC", "MUTATION_EARS_309_DESC", MUTATION_EYEBROWS_309_DESC` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |
| `cha` | Number | `1` |  |
| `lck` | Number | `2` |  |

</details>

---

### Context: `314`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_314_DESC", MUTATION_EYEBROWS_314_DESC, "MUTATION_BODY_314_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `700`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `cha` | Number | `-2` |  |
| `lck` | Number | `-2, -1` |  |
| `con` | Number | `-2` |  |
| `int` | Number | `-2` |  |
| `str` | Number | `-2` |  |

</details>

---

### Context: `300`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal, extra` |  |
| `desc` | String | `"MUTATION_EYES_300_DESC", "MUTATION_TEXTURE_300_DESC", "MUTATION_LEGS_300_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `str` | Number | `1` |  |
| `con` | Number | `1` |  |
| `cha` | Number | `-1` |  |
| `spd` | Number | `1` |  |

</details>

---

### Context: `315`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_BODY_315_DESC", "MUTATION_EARS_315_DESC", MUTATION_EYEBROWS_315_DESC` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `705`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_MOUTH_705_DESC", "MUTATION_EYES_705_DESC", "MUTATION_LEGS_705_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `cha` | Number | `-2, -3` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `FetusSpit` |  |
| `int` | Number | `2` |  |
| `speed` | Number | `-4` |  |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `effects` | [`Block`](./Cat_Mutations.md#context-effects) | `{ ... }` |  |
| `damage` | Number | `0` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status` |  |

</details>

---

### Context: `307`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | [`Enum/String`](./Enums.md#enum-desc) | `MUTATION_EYEBROWS_307_DESC, "MUTATION_EYES_307_DESC", "MUTATION_HEAD_307_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `1` |  |
| `cha` | Number | `1` |  |
| `int` | Number | `1` |  |
| `shield` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `310`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_310_DESC", MUTATION_EYEBROWS_310_DESC, "MUTATION_EYES_310_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal, extra` |  |
| `int` | Number | `1` |  |
| `override_move` | [`Enum/String`](./Enums.md#enum-override_move) | `BasicJump` |  |
| `shield` | Number | `2` |  |

</details>

---

### Context: `702`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `int` | Number | `1, -1` |  |
| `cha` | Number | `1, -1` |  |
| `con` | Number | `-2, -1` |  |
| `desc` | String | `"MUTATION_TEXTURE_702_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `-2` |  |

</details>

---

### Context: `900`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | [`Enum/String`](./Enums.md#enum-desc) | `MUTATION_EYEBROWS_900_DESC, "MUTATION_EYES_900_DESC", "MUTATION_EARS_900_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `1` |  |
| `cha` | Number | `-1` |  |
| `con` | Number | `-2` |  |

</details>

---

### Context: `306`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_MOUTH_306_DESC", "MUTATION_EYES_306_DESC", MUTATION_EYEBROWS_306_DESC` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `1, -3` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |
| `dex` | Number | `1` |  |
| `int` | Number | `1` |  |
| `shield` | Number | `12` |  |
| `spd` | Number | `1` |  |
| `str` | Number | `1` |  |

</details>

---

### Context: `317`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_317_DESC", "MUTATION_BODY_317_DESC", "MUTATION_EARS_317_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `1` |  |

</details>

---

### Context: `318`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_BODY_318_DESC", "MUTATION_EYES_318_DESC", "MUTATION_EARS_318_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |
| `divine_shield` | Number | `1` |  |

</details>

---

### Context: `319`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_BODY_319_DESC", "MUTATION_EARS_319_DESC", "MUTATION_EYES_319_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `305`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_MOUTH_305_DESC", "MUTATION_LEGS_305_DESC", "MUTATION_TAIL_305_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `int` | Number | `1, 3` |  |
| `lck` | Number | `1` |  |
| `cha` | Number | `1` |  |
| `dex` | Number | `-1` |  |
| `shield` | Number | `1` |  |
| `str` | Number | `-1` |  |

</details>

---

### Context: `311`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | [`Enum/String`](./Enums.md#enum-desc) | `MUTATION_EYEBROWS_311_DESC, "MUTATION_HEAD_311_DESC", "MUTATION_EYES_311_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `312`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_312_DESC", "MUTATION_HEAD_312_DESC", "MUTATION_BODY_312_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `divine_shield` | Number | `1` |  |
| `shield` | Number | `1` |  |
| `str` | Number | `1` |  |

</details>

---

### Context: `316`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_316_DESC", "MUTATION_EARS_316_DESC", "MUTATION_HEAD_316_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `-1` |  |
| `shield` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `706`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `desc` | String | `"MUTATION_TEXTURE_706_DESC", "MUTATION_EYES_706_DESC", "MUTATION_HEAD_706_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `-1, -3` |  |
| `spd` | Number | `-1` |  |

</details>

---

### Context: `750`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_HEAD_750_DESC", "MUTATION_EARS_750_DESC", "MUTATION_BODY_750_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `1` |  |
| `int` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `-2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `desc` | String | `"MUTATION_EYES_M2_DESC", "MUTATION_MOUTH_M2_DESC"` |  |
| `dex` | Number | `-2, -1` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `-2` |  |

</details>

---

### Context: `321`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_HEAD_321_DESC", "MUTATION_EARS_321_DESC", "MUTATION_BODY_321_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `int` | Number | `1` |  |
| `shield` | Number | `3` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `extra` |  |

</details>

---

### Context: `754`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_754_DESC", "MUTATION_EARS_754_DESC", "MUTATION_EYES_754_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `1` |  |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | `2, 1` |  |
| `damage` | Number | `0` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status` |  |
| `Freeze` | [`Array`](./Arrays.md#array-freeze) | `[ 1 0.15 ]` |  |
| `Immobile` | Number | `10%` |  |
| `effects` | [`Block`](./Cat_Mutations.md#context-effects) | `{ ... }` |  |

</details>

---

### Context: `322`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_TAIL_322_DESC", "MUTATION_BODY_322_DESC", "MUTATION_MOUTH_322_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `1` |  |
| `con` | Number | `1` |  |
| `str` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `323`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_MOUTH_323_DESC", "MUTATION_BODY_323_DESC", "MUTATION_EARS_323_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `2, -3` |  |

</details>

---

### Context: `325`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_325_DESC", "MUTATION_EARS_325_DESC", "MUTATION_LEGS_325_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `-2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `extra` |  |

</details>

---

### Context: `326`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_326_DESC", "MUTATION_EYES_326_DESC", "MUTATION_LEGS_326_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `327`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_327_DESC", "MUTATION_LEGS_327_DESC", "MUTATION_MOUTH_327_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `328`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_328_DESC", "MUTATION_EYES_328_DESC", "MUTATION_EARS_328_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `339`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_339_DESC", "MUTATION_LEGS_339_DESC", "MUTATION_EYES_339_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `bird` |  |

</details>

---

### Context: `effects`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Cat_Mutations.md#context-meleerevengedamage), [`RevengeDamage`](./Cat_Mutations.md#context-revengedamage)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1, .05 ]` |  |
| `Confusion` | [`Array`](./Arrays.md#array-confusion) | `[ 1, .1 ]` |  |
| `Blind` | [`Array`](./Arrays.md#array-blind) | `[ 1, .10 ]` |  |
| `Charmed` | [`Array`](./Arrays.md#array-charmed) | `[ 1, .15 ]` |  |
| `Petrify` | [`Array`](./Arrays.md#array-petrify) | `[ 1, .05 ]` |  |
| `RandomStatusFromPool` | [`Block`](./Cat_Mutations.md#context-randomstatusfrompool) | `{ ... }` |  |

</details>

---

### Context: `320`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_320_DESC", "MUTATION_EARS_320_DESC", "MUTATION_HEAD_320_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `shield` | Number | `1` |  |

</details>

---

### Context: `329`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_329_DESC", "MUTATION_EARS_329_DESC", "MUTATION_LEGS_329_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `331`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_331_DESC", "MUTATION_LEGS_331_DESC", "MUTATION_EYES_331_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `override_move` | [`Enum/String`](./Enums.md#enum-override_move) | `BasicJump` |  |

</details>

---

### Context: `332`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_332_DESC", "MUTATION_LEGS_332_DESC", "MUTATION_EARS_332_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `-1` |  |

</details>

---

### Context: `334`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_334_DESC", "MUTATION_EYES_334_DESC", "MUTATION_EARS_334_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `str` | Number | `1` |  |

</details>

---

### Context: `336`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_336_DESC", "MUTATION_LEGS_336_DESC", "MUTATION_EARS_336_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `bird` |  |

</details>

---

### Context: `337`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_337_DESC", "MUTATION_EARS_337_DESC", "MUTATION_LEGS_337_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `bird` |  |

</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `5%, 25%, 50%` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `RandomPickup, CharmedFly, CharmedMaggot` |  |
| `good` | Boolean | `false` |  |

</details>

---

### Context: `1500`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |
| `desc` | String | `"MUTATION_EARS_1500_DESC", "MUTATION_MOUTH_1500_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `dex` | Number | `1` |  |

</details>

---

### Context: `324`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_MOUTH_324_DESC", "MUTATION_BODY_324_DESC", "MUTATION_EYES_324_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `1` |  |
| `spd` | Number | `2` |  |

</details>

---

### Context: `341`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_341_DESC", "MUTATION_EARS_341_DESC", "MUTATION_LEGS_341_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `755`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_755_DESC", "MUTATION_EARS_755_DESC", "MUTATION_MOUTH_755_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `342`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_TAIL_342_DESC", "MUTATION_EARS_342_DESC", "MUTATION_EYES_342_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `-1` |  |

</details>

---

### Context: `343`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_343_DESC", "MUTATION_EYES_343_DESC", "MUTATION_EARS_343_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `757`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_TAIL_757_DESC", "MUTATION_MOUTH_757_DESC", "MUTATION_LEGS_757_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `int` | Number | `2` |  |

</details>

---

### Context: `759`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_HEAD_759_DESC", "MUTATION_TAIL_759_DESC", "MUTATION_LEGS_759_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `-2` |  |

</details>

---

### Context: `335`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_335_DESC", "MUTATION_EARS_335_DESC", "MUTATION_EYES_335_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `338`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_338_DESC", "MUTATION_EYES_338_DESC", "MUTATION_TAIL_338_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `752`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_MOUTH_752_DESC", "MUTATION_EARS_752_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `753`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_753_DESC", "MUTATION_HEAD_753_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `shield` | Number | `5` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` |  |
| `Knockback` | Number | `1` |  |
| `Immobile` | [`Array`](./Arrays.md#array-immobile) | `[ 1, .1 ]` |  |
| `KnockUpAndAway` | [`Block`](./Cat_Mutations.md#context-knockupandaway) | `{ ... }` |  |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomStatUp` | Number | `2, 1` |  |
| `Charge` | Number | `1` |  |
| `IntelligenceUp` | Number | `1` |  |
| `RandomStatDown` | Number | `1` |  |
| `Shield` | Number | `1` |  |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ScatterCoins` | [`Array`](./Arrays.md#array-scattercoins) | `[ 1 .5 ], 5` |  |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` |  |
| `ChangeTilesUnder` | [`Enum/String`](./Enums.md#enum-changetilesunder) | `GlassTile` |  |
| `LuckUp` | Number | `1` |  |

</details>

---

### Context: `333`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_333_DESC", "MUTATION_LEGS_333_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `shield` | Number | `3` |  |

</details>

---

### Context: `340`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_340_DESC", "MUTATION_LEGS_340_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `divine_shield` | Number | `1` |  |

</details>

---

### Context: `345`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_345_DESC", "MUTATION_EYES_345_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `751`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_751_DESC", "MUTATION_TAIL_751_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `2` |  |

</details>

---

### Context: `758`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_BODY_758_DESC", "MUTATION_LEGS_758_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `1` |  |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Coin, RandomFoodPickup` |  |
| `number` | Number | `2, [ 1 3 ]` |  |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Quivered` | [`Array`](./Arrays.md#array-quivered) | `[ 1, 0.1 ]` |  |
| `MissChance` | Number | `5` |  |
| `MoveQuivered` | [`Array`](./Arrays.md#array-movequivered) | `[ 1, 0.1 ]` |  |
| `SpeedUp` | Number | `1` |  |

</details>

---

### Context: `330`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_330_DESC", "MUTATION_LEGS_330_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `344`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_344_DESC", "MUTATION_EARS_344_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `442`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `-1` |  |
| `desc` | String | `"MUTATION_EYES_442_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `melted` |  |

</details>

---

### Context: `707`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_707_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `str` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |

</details>

---

### Context: `756`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_TAIL_756_DESC"` |  |
| `int` | Number | `1` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `2` |  |

</details>

---

### Context: `760`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_TAIL_760_DESC", "MUTATION_MOUTH_760_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `Conditional_RandomChance`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusKilledCharacters`](./Cat_Mutations.md#context-statuskilledcharacters)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AutoReanimate` | Number | `50%` |  |
| `odds` | Number | `10%` |  |

</details>

---

### Context: `StatusEveryXSpellCasts`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `8, 4` |  |
| `Charge` | Number | `2` |  |
| `RandomMagicMissile` | Number | `4` |  |

</details>

---

### Context: `1026`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_MOUTH_1026_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `346`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_346_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `shield` | Number | `1` |  |

</details>

---

### Context: `353`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_353_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` |  |
| `range` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `food` |  |

</details>

---

### Context: `1029`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_1029_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `347`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_347_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `348`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_348_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `349`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_349_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `351`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_351_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `352`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_352_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `761`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_761_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `762`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_762_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `763`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_763_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `AddDamageToElementDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `1` |  |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Electric` |  |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `BackflipDodge` |  |
| `stacks` | Number | `2` |  |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `BackflipDodge` |  |
| `chance` | Number | `10%` |  |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `class` | [`Enum/String`](./Enums.md#enum-class) | `Colorless` |  |
| `reduction` | Number | `1` |  |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ChangeTilesUnder` | [`Enum/String`](./Enums.md#enum-changetilesunder) | `TallGrassTile` |  |
| `odds` | Number | `25%` |  |

</details>

---

### Context: `CounterAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `ChainLightning` |  |
| `chance` | Number | `15%` |  |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddStatusToBasicMeleeAttack`](./Cat_Mutations.md#context-addstatustobasicmeleeattack)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `distance` | Number | `3` |  |
| `stacks` | Number | `3` |  |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `MoveOne` |  |
| `weights` | [`Enum/String`](./Enums.md#enum-weights) | `chaotic` |  |

</details>

---

### Context: `PassiveWhileHasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Bleed` |  |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `number` | [`Array`](./Arrays.md#array-number) | `[ 1 2 ]` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `RandomPickup` |  |

</details>

---

### Context: `StatusEveryXSpellCastsEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `2` |  |
| `stacks` | Number | `3` |  |

</details>

---

### Context: `StatusKilledCharacters`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_RandomChance` | [`Block`](./Cat_Mutations.md#context-conditional_randomchance) | `{ ... }` |  |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `consumables` |  |
| `PermanentIntelligence` | Number | `1` |  |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_FirstApplicationThisTurn` | [`Block`](./Cat_Mutations.md#context-conditional_firstapplicationthisturn) | `{ ... }` |  |
| `Conditional_GoodRoll` | [`Block`](./Cat_Mutations.md#context-conditional_goodroll) | `{ ... }` |  |

</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomStatusFromPool` | [`Block`](./Cat_Mutations.md#context-randomstatusfrompool) | `{ ... }` |  |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fury` | Number | `10` |  |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` |  |

</details>

---

### Context: `PassiveWhenAtFullMana`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `2` |  |

</details>

---

### Context: `StatusEachRoundEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `UseAbility` | [`Enum/String`](./Enums.md#enum-useability) | `Spit` |  |

</details>

---

### Context: `StatusIfDidntMove`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `3` |  |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | `3` |  |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `2` |  |

</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` |  |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Number | `1` |  |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RangeUp` | Number | `1` |  |

</details>

---

