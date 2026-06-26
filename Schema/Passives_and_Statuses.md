# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Passives & Statuses

> **Associated Files:** `data/passives/, data/passive_pools.gon`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 885

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | Enum | Localization key for the passive's display description. | 5441 |  |
| [`name`](./Strings.md#string-name) | Enum | Localization key for the passive's display name. | 5027 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1570 |  |
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 1200 |  |
| [`stats`](./Passives_and_Statuses.md#context-stats) | Object |  | 982 |  |
| `AbilityReaction` | Enum / Object |  | 4 | `SCSneakUp` (Enum), `attack` (Enum), `{ ... }` (Object) |
| `AfterImage` | Object |  | 2 | `PlayerCat_ThiefShade2` (Enum), `PlayerCat_ThiefShade` (Enum), `{ ... }` (Object) |
| `AllyBonusAbilityAura` | Enum / Object |  | 2 | `NubbyToss` (Enum), `{ ... }` (Object) |
| `AllyDodgeChanceAura` | Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `AlphaAllStatsUp` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `AlphaCat` | Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Ammo` | Integer |  |  | `[1 .5]` (Array), `-99999` (Number), `6` (Number), `{ ... }` (Object) |
| `AmplifyStatus` | Enum |  | 8 | `Burn` (Enum), `Poison` (Enum), `{ ... }` (Object) |
| `ArmorPickup` | Object |  |  | `{ ... }` (Object) |
| `AutocastEachTurnBegin` | Enum / Object |  | 2 | `MindCrack_EldritchVisage2` (Enum), `MindCrack_EldritchVisage` (Enum), `{ ... }` (Object) |
| `BackflipWhenTargeted` | Enum / Integer / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `BackstabCritChance` | Number |  | 2 | `1` (Number), `.25` (String) |
| `BaseStatMultiply` | Number |  |  | `.666` (String), `.25` (String) |
| `BasicAttackCritChance` | Number |  |  | `100` (Number), `.1` (String) |
| `Bird` | Enum / Object |  | 6 | `CookedChickenLeg` (Enum), `{ ... }` (Object) |
| `BlastResistance` | Array / Number / Object |  | 6 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `BleedThorns` | Integer |  | 8 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Blind` | Array / Integer |  | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `BoostDamageAura` | Array / Number / Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BoostDamageGlobalAura` | Array / Number / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BoostWeaponDamage` | Object |  | 10 | `5` (Number), `2` (Number), `{ ... }` (Object) |
| `BraceForEachNeighboringEnemy` | Array / Number / Object |  | 2 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Brittle` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BrittleDuringElement` | Enum |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Buddy` | Enum / Object |  |  | `CaveCatDad` (Enum), `Smough` (Enum), `{ ... }` (Object) |
| `BuffImmunity` | Integer / Object |  |  | `1` (Number), `{ ... }` (Object) |
| `Burn` | Array / Enum / Integer |  | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `CanMutateTo` | Array / Enum |  |  | `[Lumpy Leaper]` (Array), `[TumorousMaggot ChargeyMaggot SwappyMaggot]` (Array), `Hyde` (Enum) |
| `CatPartsTransform` | Object |  |  | `{ ... }` (Object) |
| `cha` | Enum / Integer |  | 468 |  |
| `ChainKnockback` | Number / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `ChanceToBlockAndCounter` | Integer / Object |  | 2 | `15` (Number), `33` (Number), `{ ... }` (Object) |
| `ChanceToRevive` | Integer / Object |  | 2 | `100` (Number), `25` (Number), `{ ... }` (Object) |
| `CharmAllFlies` | Array / Number / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `CollectPickupsOnBattleEnd` | Number / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `Conductor` | Boolean (Flag) / Number / Object |  | 2 | `(Flag)` (Boolean (Flag)), `2` (Number), `{ ... }` (Object) |
| `ConjureBonusAbility` | Enum / Object |  | 2 | `Class` (Enum), `Mage` (Enum), `{ ... }` (Object) |
| `Consumed` | Object |  |  | `{ ... }` (Object) |
| `CounterAttack` | Array / Enum / Object |  | 4 | `[attack GSScream]` (Array), `Shove` (Enum), `YeticatSnowball_Counter` (Enum), `{ ... }` (Object) |
| `CounterNextAttacks` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `CritChanceUp` | Integer |  | 36 | `[1 .5]` (Array), `1` (Number), `50` (Number), `{ ... }` (Object) |
| `DamageReductionAura` | Array / Number / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DeathChill` | Number / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `DeathRattle` | Enum / Object |  | 2 | `BoomerCatExplode` (Enum), `BombFlyExplode` (Enum), `{ ... }` (Object) |
| `DeathRattleRevive` | Enum / Object |  |  | `DoNothing` (Enum), `tk_PetrifiedPinky` (Enum), `{ ... }` (Object) |
| `DejaVu` | Number / Object |  | 2 | `10` (Number), `{ ... }` (Object) |
| `DepressionAura` | Integer |  | 2 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DiesToElement` | Enum / Object |  |  | `Wind` (Enum), `{ ... }` (Object) |
| `DirtyClaws` | Number / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `Disguised` | Integer |  |  | `1` (Number) |
| `Doomed` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `DoubleCastSpellsEachTurn_Status` | Integer |  |  | `1` (Number) |
| `DukeOfFlies` | Number / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `Dyslexia` | Array / Object |  |  | `[3 5]` (Array), `[6 9]` (Array), `{ ... }` (Object) |
| `EliteTint` | Array / Enum |  |  | `[.6 .6 .6 .50]` (Array), `[1 .75 .5 .50]` (Array), `red` (Enum) |
| `Empath` | Number / Object |  | 2 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| `EnergyStorm` | Number / Object |  | 2 | `3` (Number), `{ ... }` (Object) |
| `ExtraBasicAttacks_Status` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ExtraBasicMoves_Status` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `FaceLastDamage` | Integer / Object |  |  | `1` (Number), `{ ... }` (Object) |
| `FinalBossHitCountdownBoris` | Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `FinalBossHitCountdownExplosive` | Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `FinalBossHitCountdownHoly` | Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Flammable` | Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `FlyDamageIncrease` | Object |  | 2 | `[1 .5]` (Array), `1` (Number), `4` (Number), `{ ... }` (Object) |
| `Flying` | Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `FollowUp` | Enum / Object |  | 2 | `FollowUpDash` (Enum), `FollowUpDash2` (Enum), `{ ... }` (Object) |
| `Fragile` | Integer |  | 6 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `FragileDuringElement` | Enum |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `FrankBolts` | Boolean (Flag) / Number / Object |  |  | `(Flag)` (Boolean (Flag)), `1` (Number), `{ ... }` (Object) |
| `FullPower` | Number / Object |  | 2 | `3` (Number), `{ ... }` (Object) |
| `GlobalFamiliarDamageBoost` | Array / Number / Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `GlobalFamiliarMoveBoost` | Array / Number / Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `HealingAura` | Number / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `HealthMultiplier` | Number / String |  |  | `1.5` (Number), `.8` (String), `.5` (String) |
| `Hypomania` | Number / Object |  |  | `3` (Number), `{ ... }` (Object) |
| `ImmediateAbilityReaction` | Array / Enum / Object |  |  | `[ManglerFumbleEven ManglerFumbleOdd]` (Array), `NubsGoop` (Enum), `CatGoop` (Enum), `{ ... }` (Object) |
| `Immobile` | Array / Integer |  | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| `ImmortalLeeches` | Number / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `KillsHeal` | Number / Object |  | 2 | `5` (Number), `50` (Number), `{ ... }` (Object) |
| `KineticSpikes` | Integer |  | 6 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `LateBloomer` | Array / Number / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Lifesteal` | Integer |  |  | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `LineOfSightTrueSightAura` | Number / String |  | 2 | `0` (Number), `.5` (String) |
| `LowHealthAllyDodgeChanceAura` | Array / Number / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer |  |  | `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| `Madness` | Array / Enum / Integer / Object |  |  | `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `MegaMinions` | Number / Object |  | 2 | `3` (Number), `{ ... }` (Object) |
| `Metal` | Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `MetalDetector` | Number / Object |  | 2 | `5` (Number), `10` (Number), `{ ... }` (Object) |
| `MissChance` | Integer |  | 24 | `[1 .5]` (Array), `1` (Number), `20` (Number), `{ ... }` (Object) |
| `MoveAwayFromDamageSource` | Object |  | 2 | `MoveOne` (Enum), `BasicJump` (Enum), `{ ... }` (Object) |
| `MoveQuivered` | Integer |  | 6 | `[1 0.1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `MoveSpeedMultiplier` | Number |  |  | `.5` (String) |
| `MoveTowardsDamageSource` | Enum / Object |  | 2 | `MoveOne` (Enum), `{ ... }` (Object) |
| `MoveTowardsKillers` | Enum / Object |  |  | `ReaperRevenge` (Enum), `{ ... }` (Object) |
| `MoveWhenDamaged` | Enum / Object |  | 2 | `TKNG_Hop` (Enum), `move` (Enum), `{ ... }` (Object) |
| `MutateAfterXTurns` | Integer |  |  | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `NoManaRegen` | Array / Number / Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `NonStackingDivineShield` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `NumbingLeeches` | Number / Object |  | 2 | `3` (Number), `{ ... }` (Object) |
| `Paranoia` | Enum / Object |  |  | `ParanoiaBasicMelee` (Enum), `{ ... }` (Object) |
| `PermanentImmobile` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `PermanentMadness` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `PoisonThorns` | Integer |  | 6 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `PoopWhenHit` | Object |  | 4 | `Poop` (Enum), `{ ... }` (Object) |
| `ProtectTargetedAllies` | Object |  | 2 | `SwapPositions_WideLoad2` (Enum), `SwapPositions_WideLoad` (Enum), `{ ... }` (Object) |
| `Quiver` | Number / Object |  | 2 | `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Quivered` | Array / Integer |  | 10 | `[1 0.1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String |  | 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| `ReduceManaCost` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `ReflectProjectiles` | Integer / Object |  | 4 | `1` (Number), `100` (Number), `{ ... }` (Object) |
| `Robot` | Integer / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RockyArmorSalvage` | String |  |  | `.75` (String) |
| `SafeDoomed` | Enum / Integer |  |  | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `SchrodingerDisorder` | Number / Object |  |  | `50` (Number), `{ ... }` (Object) |
| `Scleroderma` | Number / Object |  |  | `1` (Number), `{ ... }` (Object) |
| `SharePickups` | Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `ShoulderCheck` | Number / Object |  | 2 | `100` (Number), `33` (Number), `{ ... }` (Object) |
| `ShovingMatch` | Enum / Object |  | 2 | `attack` (Enum), `{ ... }` (Object) |
| `SizeScale` | Number |  | 4 | `1.1` (Number), `1.3` (Number), `.6` (String), `.75` (String) |
| `SmallRockBehavior` | Integer / Object |  |  | `5` (Number), `0` (Number), `{ ... }` (Object) |
| `SpawnExtraThingsOnBattleStart` | Object |  | 2 | `{ ... }` (Object) |
| `SpawnObjectOnPopCorpse` | Enum / Object |  | 2 | `Coin` (Enum), `Catnip` (Enum), `{ ... }` (Object) |
| `SpawnOnBattleStart` | Enum / Object |  | 24 | `ZombieCatFamiliar` (Enum), `BeefyCharmedLeech` (Enum), `{ ... }` (Object) |
| `SpawnOnDeath` | Enum / Object |  |  | `NonChampionFlySwarm` (Enum), `Maggot` (Enum), `{ ... }` (Object) |
| `spd` | Enum / Integer |  | 424 |  |
| `shield` | Enum / Integer |  | 422 |  |
| `con` | Enum / Integer |  | 416 |  |
| `int` | Enum / Integer |  | 401 |  |
| `lck` | Enum / Integer |  | 351 |  |
| `SpeedUp` | Enum / Integer |  |  | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `SpellDamageUp` | Integer |  |  | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `SproutsGrantMovement` | Integer |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `StatusImmunity` | Array / Enum |  |  | `[Burn]` (Array), `[Freeze Slow]` (Array), `Burn` (Enum), `Webbed` (Enum) |
| `Stealth` | Array / Integer |  | 2 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `str` | Enum / Integer |  | 337 |  |
| `dex` | Enum / Integer |  | 301 |  |
| [`keyword_tooltips`](./Passives_and_Statuses.md#context-keyword_tooltips) | Object | Examples: `{ ... }` | 62 |  |
| `divine_shield` | Integer | Examples: `3, 1` | 54 |  |
| [`lock_item_slot`](./Passives_and_Statuses.md#context-lock_item_slot) | Object |  | 32 |  |
| [`name_mod`](./Strings.md#string-name_mod) | String |  | 22 |  |
| [`desc_multiclass`](./Strings.md#string-desc_multiclass) | String |  | 20 |  |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum |  | 20 |  |
| `auto_plus_signs_on_name` | Boolean |  | 8 |  |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | Flat addition to a base value. | 8 |  |
| [`empty_armor_scaled_stats`](./Passives_and_Statuses.md#context-empty_armor_scaled_stats) | Object | Examples: `{ ... }` | 8 |  |
| [`tags`](./Arrays.md#array-tags) | Array / Enum |  | 8 |  |
| [`icon`](./Enums.md#enum-icon) | Integer | Examples: `DejaVu3, DejaVu2` | 4 |  |
| [`schadenfreude_scaled_stats`](./Passives_and_Statuses.md#context-schadenfreude_scaled_stats) | Object | Examples: `{ ... }` | 4 |  |
| [`grant_ability`](./Enums.md#enum-grant_ability) | Enum |  | 2 |  |
| `StrengthForEachNeighboringEnemy` | Array / Number / Object |  | 2 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `StrengthInNumbersAura` | Number / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `Study` | Number / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `StunImmunity` | Integer / Object |  |  | `1` (Number), `{ ... }` (Object) |
| `SupportFormChangeInsteadOfRun` | Enum / Object |  |  | `Attacker` (Enum), `{ ... }` (Object) |
| `SwapHighestAndLowestStat` | Integer |  | 2 | `1` (Number) |
| `Tech` | Integer |  | 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `TempInitiativeChange` | Integer |  |  | `[1 .5]` (Array), `-999` (Number), `9999` (Number), `{ ... }` (Object) |
| `Thorns` | Integer |  | 36 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `TileDamageMultiplier` | Number / Object |  | 2 | `2` (Number), `{ ... }` (Object) |
| `Trample` | Integer |  | 14 | `[1 .5]` (Array), `[3 X-8]` (Array), `1` (Number), `6` (Number), `{ ... }` (Object) |
| `TransformInXTurns` | Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TransformOnDeath` | Array / Enum |  |  | `[Hive FloatingHive]` (Array), `RatKing` (Enum), `Tatters` (Enum) |
| `TransformOnDeathImmediately` | Enum / Object |  |  | `NoHead` (Enum), `{ ... }` (Object) |
| `Triskaidekaphobia` | Number / Object |  |  | `13` (Number), `{ ... }` (Object) |
| `UseAbility` | Enum / Object |  |  | `GirlDinoPoop` (Enum), `TormentorRuneAbsorb` (Enum), `{ ... }` (Object) |
| `Vegan` | Number / Object |  | 4 | `1` (Number), `{ ... }` (Object) |
| `Vengeful` | Number / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `Weakness` | Array / Integer / Object |  | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `WobblyCat` | Number / Object |  |  | `25` (Number), `{ ... }` (Object) |
| `YOffset` | Number |  | 6 | `-.18` (String), `.25` (String) |
| `Zombie` | Array / Number / Object |  |  | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`passives`](./Enums.md) | Object | | 884 |   |

</details>

---

### Object: `passives`


**Definition:** Object listing intrinsic passive modifiers.  
**Total Count:** 884


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAfterXKills`](./Passives_and_Statuses.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#context-passiveathealththreshold), [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#context-passiveatinjurythreshold), [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold), [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement), [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2827 |  |
| [`AbilityChargeRefundChance`](./Enums.md) | Object | | 1 |   |
| [`AbilityOnBattleStart`](./Enums.md) | Enum | | 7 | neck_ChefsApron |
| [`AbilityReaction`](./Enums.md) | Enum / Object | | 4 | PissYourself |
| [`AbilityWhenTaggedCharacterMovesNear`](./Enums.md) | Object | | 2 |   |
| [`AbsorbManaAura`](./Enums.md) | Integer | | 2 | 1 |
| [`AddAllyNeighborsToAbilityRange`](./Enums.md) | Integer | | 1 | 1 |
| [`AddAllyNeighborsToAttackRange`](./Enums.md) | Integer | | 1 | 1 |
| [`AddBonusMeleeRange`](./Enums.md) | Integer | | 5 | 2 |
| [`AddBonusRange`](./Enums.md) | Integer | | 15 | 2 |
| [`AddChaScalingSpellDamage`](./Enums.md) | Integer | | 1 | 3 |
| [`AddCorpseHealth`](./Enums.md) | Integer | | 7 | 96 |
| [`AddCritMultiplier`](./Enums.md) | Integer | | 23 | 200 |
| [`AddDamageToBasicAttack`](./Enums.md) | Integer | | 4 | 2 |
| [`AddDamageToElementDamage`](./Enums.md) | Object | | 4 |   |
| [`AddElementsToBasicAttack`](./Enums.md) | Enum | | 6 | Ice |
| [`AddHiddenTag`](./Enums.md) | Enum | | 2 | bowling_ball |
| [`AddInitiative`](./Enums.md) | Integer | | 2 | -100 |
| [`AddKnockbackDamage`](./Enums.md) | Integer | | 3 | 2 |
| [`AddKnockbackToEverything`](./Enums.md) | Integer | | 1 | 1 |
| [`AddLevelUpRerolls`](./Enums.md) | Integer | | 4 | 2 |
| [`AddLevelUpStatMultiplier`](./Enums.md) | Integer | | 1 | 1 |
| [`AddManaRegen`](./Enums.md) | Integer | | 5 | 7 |
| [`AddMovement`](./Enums.md) | Integer | | 5 | 20 |
| [`AddPassiveToSpawnedRocks`](./Enums.md) | Object | | 2 |   |
| [`AddPassivesToCharmed`](./Enums.md) | Object | | 4 |   |
| [`AddPassivesToMinions`](./Enums.md) | Object | | 29 |   |
| [`AddPassivesToSummonAbilityMinions`](./Enums.md) | Object | | 2 |   |
| [`AddRangedCritChance`](./Enums.md) | Integer | | 1 | 25 |
| [`AddSelfStatusToBasicAttack`](./Enums.md) | Object | | 3 |   |
| [`AddSelfStatusToWeapons`](./Enums.md) | Object | | 2 |   |
| [`AddSpellDamage`](./Enums.md) | Integer | | 6 | 2 |
| [`AddStartingMana`](./Enums.md) | Integer | | 2 | 20 |
| [`AddStatusToAllDamage`](./Enums.md) | Object | | 5 |   |
| [`AddStatusToAllDamageAbilities`](./Enums.md) | Object | | 2 |   |
| [`AddStatusToBasicAttack`](./Enums.md) | Object | | 92 |   |
| [`AddStatusToBasicAttackWithCooldown`](./Enums.md) | Object | | 2 |   |
| [`AddStatusToBasicMeleeAttack`](./Enums.md) | Object | | 5 |   |
| [`AddStatusToElementAbilities`](./Enums.md) | Object | | 6 |   |
| [`AddStatusToElementDamage`](./Enums.md) | Object | | 4 |   |
| [`AddStatusToExplosions`](./Enums.md) | Object | | 4 |   |
| [`AddStatusToFirstBasicAttack`](./Enums.md) | Object | | 2 |   |
| [`AddStatusToKnockbackDamage`](./Enums.md) | Object | | 1 |   |
| [`AddStatusToMeleeDamage`](./Enums.md) | Object | | 2 |   |
| [`AddStatusToReceivedDamage_ExcludeStatuses`](./Enums.md) | Object | | 1 |   |
| [`AddStatusToSpells`](./Enums.md) | Object | | 1 |   |
| [`AddStatusToTrampleDamage`](./Enums.md) | Object | | 2 |   |
| [`AddStatusToWeapons`](./Enums.md) | Object | | 6 |   |
| [`AddStatusesIfPersistentWeatherElement`](./Enums.md) | Object | | 1 |   |
| [`AddStatusesToReceivedElementalDamage`](./Enums.md) | Object | | 1 |   |
| [`AddTag`](./Enums.md) | Enum | | 3 | rock |
| [`AddTemporaryEffectsToBasicAttack`](./Enums.md) | Object | | 3 |   |
| [`AddTemporaryEffectsToEquipment`](./Enums.md) | Object | | 1 |   |
| [`AddUnfilledMaxHealth`](./Enums.md) | Integer | | 3 | 20 |
| [`AddWeaponScaling`](./Enums.md) | Integer | | 2 | 1 |
| [`AfterImage`](./Enums.md) | Enum | | 3 | PlayerCat_ThiefShade2 |
| [`AllDamageCrits`](./Enums.md) | Integer | | 1 | 1 |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`AlliesAvoidTraps`](./Enums.md) | Integer | | 1 | 1 |
| [`AllowPassTurn`](./Enums.md) | Integer | | 2 | 0 |
| [`AllyBonusAbilityAura`](./Enums.md) | Enum / Object | | 4 | NubbyToss |
| [`AllyChainKnockback`](./Enums.md) | Integer | | 1 | 1 |
| [`AllyDamageReaction`](./Enums.md) | Enum | | 2 | attack |
| [`AllyDamageReduction`](./Enums.md) | Integer | | 3 | 0 |
| [`AllyHealthRegenAura`](./Enums.md) | Object | | 2 |   |
| [`AllyManaRegenAura`](./Enums.md) | Object | | 4 |   |
| [`AllyMoveAbilityAura`](./Enums.md) | Enum | | 2 | CatapultJump2 |
| [`AllyMultiplyKnockbackDamage`](./Enums.md) | Integer | | 2 | 2 |
| [`AllyMultiplyKnockbackDistance`](./Enums.md) | Integer | | 1 | 2 |
| [`AllyUncappedHPAura`](./Enums.md) | Integer | | 1 | 1 |
| [`AlphaCat`](./Enums.md) | Integer | | 3 | 1 |
| [`AlphaTurns`](./Enums.md) | Integer | | 6 | -1 |
| [`AlternateCraftingPools`](./Enums.md) | Object | | 2 |   |
| [`AmplifyKnockback`](./Enums.md) | Integer | | 3 | 2 |
| [`AmplifyNegativeStatus`](./Enums.md) | Integer | | 1 | 1 |
| [`AmplifyPositiveStatus`](./Enums.md) | Integer | | 2 | 2 |
| [`AmplifyStatus`](./Enums.md) | Enum / Object | | 8 | Poison |
| [`ApplyStatusesToRandomEnemiesEachTurn`](./Enums.md) | Object | | 2 |   |
| [`ArmorDodgeChance`](./Enums.md) | Integer | | 1 | 10 |
| [`Autism`](./Enums.md) | Object | | 2 |   |
| [`AutoCritLowDamage`](./Enums.md) | Integer | | 2 | 2 |
| [`AutoEquipConsumables`](./Enums.md) | Integer | | 2 | 1 |
| [`AutocastEachRound`](./Enums.md) | Object | | 4 |   |
| [`AutocastEachTurn`](./Enums.md) | Enum | | 2 | ViolentOutburst |
| [`AutocastEachTurnBegin`](./Enums.md) | Enum / Object | | 3 | MindCrack_EldritchVisage |
| [`BackstabCritChance`](./Enums.md) | Integer | | 4 | 1 |
| [`BackstabImmunity`](./Enums.md) | Integer | | 1 | 1 |
| [`BackstabWeakness`](./Enums.md) | Number | | 1 | 0.75 |
| [`BasicAttackAOEBonus`](./Enums.md) | Integer | | 5 | 2 |
| [`BasicAttackCritChance`](./Enums.md) | Integer | | 2 | 100 |
| [`BasicAttackDamageMultiplier`](./Enums.md) | Number | | 6 | 33.333334 |
| [`BasicAttackStatusCarefulness`](./Enums.md) | Integer | | 2 | 1 |
| [`BasicAttackStatusSwap`](./Enums.md) | Array | | 1 | [TempDamageUp] |
| [`BlacklistPickupType`](./Enums.md) | Enum | | 1 | food |
| [`BlastResistance`](./Enums.md) | Integer | | 7 | 2 |
| [`Bleed`](./Enums.md) | Array / Integer | | 23 | [.1] |
| [`BleedThorns`](./Enums.md) | Integer | | 3 | 2 |
| [`BonusAbility`](./Enums.md) | Enum | | 11 | FighterBonusThrow |
| [`BonusFoodEachBattle`](./Enums.md) | Integer | | 2 | 2 |
| [`BonusHealthRegenBasedOnDex`](./Enums.md) | Integer | | 1 | 5 |
| [`BonusRangeBasedOnDex`](./Enums.md) | Integer | | 1 | 5 |
| [`BoobyTrapItems`](./Enums.md) | Object | | 2 |   |
| [`BoostAllyStatsOnDeath`](./Enums.md) | Integer | | 2 | 2 |
| [`BoostDamageAura`](./Enums.md) | Integer | | 1 | 1 |
| [`BoostDamageGlobalAura`](./Enums.md) | Integer | | 1 | 1 |
| [`BoostHeals`](./Enums.md) | Integer | | 4 | -2 |
| [`BoostRangeAura`](./Enums.md) | Integer | | 1 | 1 |
| [`BoostRangeGlobalAura`](./Enums.md) | Integer | | 1 | 1 |
| [`BoostWeaponDamage`](./Enums.md) | Integer / Object | | 6 | 2 |
| [`BouncyProjectiles`](./Enums.md) | Object | | 2 |   |
| [`Brace`](./Enums.md) | Integer | | 22 | 2 |
| [`BraceForEachNeighboringEnemy`](./Enums.md) | Integer | | 2 | 2 |
| [`Bruise`](./Enums.md) | Integer | | 15 | 2 |
| [`BuffImmunity`](./Enums.md) | Integer | | 1 | 1 |
| [`Burn`](./Enums.md) | Enum / Integer | | 28 | 2 |
| [`CCImmunity`](./Enums.md) | Integer | | 2 | 1 |
| [`CanRemoveCursedItems`](./Enums.md) | Integer | | 1 | 1 |
| [`CantDodge`](./Enums.md) | Integer | | 1 | 1 |
| [`CapDamageFromAllies`](./Enums.md) | Integer | | 2 | 1 |
| [`CapMovementAbilityRange`](./Enums.md) | Integer | | 1 | 1 |
| [`CapTechSpent`](./Enums.md) | Integer | | 1 | 0 |
| [`CatAPultAnimation`](./Enums.md) | Object | | 2 |   |
| [`CatchProjectiles`](./Enums.md) | Object | | 3 |   |
| [`ChainKnockback`](./Enums.md) | Integer | | 3 | 1 |
| [`ChanceToBackflip`](./Enums.md) | Object | | 2 |   |
| [`ChanceToBlockAndCounter`](./Enums.md) | Integer | | 2 | 33 |
| [`ChanceToRevive`](./Enums.md) | Integer / Object | | 2 | 25 |
| [`ChangeTauntPriority`](./Enums.md) | Integer | | 2 | -1 |
| [`CharmAllFlies`](./Enums.md) | Integer | | 2 | 1 |
| [`ClassManaCostReduction`](./Enums.md) | Object | | 2 |   |
| [`CobraReflex`](./Enums.md) | Enum | | 3 | BasicMonkMelee |
| [`CoinsAddDamage`](./Enums.md) | Integer | | 2 | 2 |
| [`CollectPickupsOnBattleEnd`](./Enums.md) | Integer / Object | | 2 | 1 |
| [`Conductor`](./Enums.md) | Integer | | 3 | 2 |
| [`ConductorManaRegen`](./Enums.md) | Integer | | 1 | 2 |
| [`ConfusionEffectOnTaggedAbilities`](./Enums.md) | Enum | | 1 | consumable |
| [`ConjureCastSpellsForAllies`](./Enums.md) | Integer | | 2 | 2 |
| [`ConsumableEffectsMultiplierBonus`](./Enums.md) | Integer | | 2 | 1 |
| [`ConsumablesInfiniteRange`](./Enums.md) | Integer | | 3 | 1 |
| [`ConsumablesMeleeRange`](./Enums.md) | Integer | | 1 | 1 |
| [`CounterAttack`](./Enums.md) | Enum | | 4 | ReflexPunchJab |
| [`CritChanceUp`](./Enums.md) | Integer | | 29 | 80 |
| [`CritsApplyStatus`](./Enums.md) | Object | | 11 |   |
| [`DamageEnemiesOnHeal`](./Enums.md) | Integer | | 2 | 2 |
| [`DamageEnemiesOnKill`](./Enums.md) | Integer | | 2 | 2 |
| [`DamageIfDidntUseSpecificAbility`](./Enums.md) | Object | | 1 |   |
| [`DamageNeighborTilesWhenCastSpell`](./Enums.md) | Object | | 2 |   |
| [`DamageNeighborsAfterMove`](./Enums.md) | Object | | 2 |   |
| [`DamageNeighborsOnEndMove`](./Enums.md) | Object | | 7 |   |
| [`DamageReductionAura`](./Enums.md) | Object | | 2 |   |
| [`DamageUp`](./Enums.md) | Integer | | 26 | 2 |
| [`DeathChill`](./Enums.md) | Integer | | 3 | 1 |
| [`DeathRattle`](./Enums.md) | Enum / Object | | 3 | BoomerCatExplode |
| [`DebuffImmunity`](./Enums.md) | Integer | | 2 | 1 |
| [`DejaVu`](./Enums.md) | Integer | | 3 | 10 |
| [`DepressionAura`](./Enums.md) | Integer | | 1 | 2 |
| [`Diabetes`](./Enums.md) | Object | | 2 |   |
| [`DirtyClaws`](./Enums.md) | Integer | | 3 | 1 |
| [`DisableAbilities`](./Enums.md) | Enum | | 1 | all_items |
| [`DisableAbilitiesWithTag`](./Enums.md) | Enum | | 1 | meat |
| [`DodgeChance`](./Enums.md) | Integer | | 17 | 50 |
| [`Doomed`](./Enums.md) | Integer | | 3 | 3 |
| [`DoubleCastWeapons`](./Enums.md) | Integer | | 2 | 2 |
| [`DukeOfFlies`](./Enums.md) | Integer | | 3 | 1 |
| [`Dyslexia`](./Enums.md) | Array | | 3 | [3] |
| [`EMP`](./Enums.md) | Object | | 5 |   |
| [`EachSpellFreeAtFullMana`](./Enums.md) | Integer | | 1 | 1 |
| [`ElementImmune`](./Enums.md) | Enum | | 7 | Ice |
| [`ElementalAttunement`](./Enums.md) | Object | | 3 |   |
| [`ElementalManaCostReduction`](./Enums.md) | Object | | 3 |   |
| [`Empath`](./Enums.md) | Integer | | 3 | 50 |
| [`EnemiesGetPickupsKnockedOut`](./Enums.md) | Integer | | 2 | 2 |
| [`EnergyStorm`](./Enums.md) | Integer / Object | | 3 | 3 |
| [`EquipRandomTemporaryItemFromPool`](./Enums.md) | Enum | | 1 | weapons |
| [`EquipTemporaryItem`](./Enums.md) | Enum | | 10 | FoodMedium |
| [`EquipmentPassiveMultiplierBonus`](./Enums.md) | Integer | | 2 | 1 |
| [`EquipmentSetBonusBonus`](./Enums.md) | Integer | | 2 | 2 |
| [`EscapeSequence`](./Enums.md) | Object | | 3 |   |
| [`Eternal`](./Enums.md) | Object | | 3 |   |
| [`ExhaustionRoundChange`](./Enums.md) | Integer | | 1 | 3 |
| [`ExplodeOverkilledEnemies`](./Enums.md) | Integer | | 2 | 2 |
| [`ExplosionImmunity`](./Enums.md) | Integer | | 1 | 1 |
| [`ExtraBasicAttacks`](./Enums.md) | Integer | | 9 | 2 |
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer | | 1 | 1 |
| [`ExtraInjuryOnDeath`](./Enums.md) | Integer | | 1 | 1 |
| [`ExtraMovePoints`](./Enums.md) | Integer | | 8 | 1 |
| [`ExtraStatusWhenDealingDamage`](./Enums.md) | Object | | 2 |   |
| [`ExtraTrinketUses`](./Enums.md) | Integer | | 1 | 1 |
| [`ExtraWeaponAttacks`](./Enums.md) | Integer | | 6 | 2 |
| [`FaceArmorPassiveMultiplierBonus`](./Enums.md) | Integer | | 1 | 2 |
| [`FaceShield`](./Enums.md) | Integer | | 2 | 0 |
| [`FamiliarSecondaryDamageImmunity`](./Enums.md) | Integer | | 2 | 1 |
| [`FlowerPowerAuraBrace`](./Enums.md) | Integer | | 2 | 1 |
| [`FlowerPowerAuraStrength`](./Enums.md) | Integer | | 2 | 1 |
| [`FlowersOnEndTurn`](./Enums.md) | Integer | | 2 | 3 |
| [`FlyDamageIncrease`](./Enums.md) | Integer | | 2 | 4 |
| [`Flying`](./Enums.md) | Integer | | 6 | 1 |
| [`FollowUp`](./Enums.md) | Enum | | 3 | FollowUpDash2 |
| [`ForceSpecificInjury`](./Enums.md) | Enum | | 8 | int |
| [`ForceUseAbility`](./Enums.md) | Enum / Object | | 10 | Hallucinate_Disorder |
| [`FreePathfindElement`](./Enums.md) | Enum | | 6 | Grass |
| [`FreeSpellsAtFullMana`](./Enums.md) | Integer | | 1 | 1 |
| [`FreezePiercing`](./Enums.md) | Integer | | 4 | 1 |
| [`FrontstabBasicAttackCritChance`](./Enums.md) | Integer | | 1 | 100 |
| [`FrontstabCritChance`](./Enums.md) | Integer | | 1 | 100 |
| [`FullHeal`](./Enums.md) | Integer | | 6 | 1 |
| [`FullHealthAllStatsUp`](./Enums.md) | Integer | | 1 | 1 |
| [`FullHealthCritChance`](./Enums.md) | Integer | | 2 | 100 |
| [`FullHealthManaRegen`](./Enums.md) | Integer | | 1 | 5 |
| [`FullPower`](./Enums.md) | Integer | | 3 | 3 |
| [`FurnitureStats`](./Enums.md) | Object | | 1 |   |
| [`GainExtraShield`](./Enums.md) | Integer | | 2 | 2 |
| [`GrassTileHealing`](./Enums.md) | Integer | | 2 | 1 |
| [`GravityWell`](./Enums.md) | Object | | 3 |   |
| [`HPGainBlock`](./Enums.md) | Integer | | 1 | 1 |
| [`HeadArmorPassiveMultiplierBonus`](./Enums.md) | Integer | | 2 | 2 |
| [`HealAtStart`](./Enums.md) | Integer | | 1 | 100 |
| [`HealDamagesEnemies`](./Enums.md) | Integer | | 2 | 1 |
| [`HealingAura`](./Enums.md) | Integer | | 2 | 1 |
| [`HealsAlsoRegenMana`](./Enums.md) | Integer | | 2 | 2 |
| [`HealsCanRevive`](./Enums.md) | Integer | | 2 | 3 |
| [`HealthRegenUp`](./Enums.md) | Integer | | 14 | 2 |
| [`HolyDamageMultiplierBonus`](./Enums.md) | Integer | | 1 | 1 |
| [`HolyShieldTransferToTaggedMinions`](./Enums.md) | Enum | | 2 | any |
| [`HouseFoodRequirementMultiplier`](./Enums.md) | Integer | | 1 | 0 |
| [`Hypomania`](./Enums.md) | Integer | | 2 | 3 |
| [`IgnoreTiles`](./Enums.md) | Integer | | 3 | 1 |
| [`ImmortalLeeches`](./Enums.md) | Integer | | 3 | 1 |
| [`IncreaseExplosionDamage`](./Enums.md) | Integer | | 8 | 2 |
| [`IncreaseExplosionSize`](./Enums.md) | Integer | | 4 | 2 |
| [`IncreaseHealingSpellRange`](./Enums.md) | Integer | | 2 | 2 |
| [`IncreaseItemUsesOnEquip`](./Enums.md) | Integer | | 1 | 1 |
| [`IncreaseSpellRange`](./Enums.md) | Integer | | 2 | 5 |
| [`InfiniteRebirth`](./Enums.md) | Object | | 3 |   |
| [`InjuryImmunity`](./Enums.md) | Integer | | 1 | 1 |
| [`InnateElement`](./Enums.md) | Enum | | 8 | Ice |
| [`InvertBrainFaction`](./Enums.md) | Integer | | 1 | 1 |
| [`KillsHeal`](./Enums.md) | Integer | | 3 | 50 |
| [`KillsToMeat`](./Enums.md) | Enum | | 2 | Food |
| [`KnockbackImmunity`](./Enums.md) | Integer | | 4 | 1 |
| [`LateBloomer`](./Enums.md) | Object | | 3 |   |
| [`LevelUpClassOverride`](./Enums.md) | Enum | | 4 | Jester |
| [`LightningAspectCharge`](./Enums.md) | Integer | | 2 | 0 |
| [`LightningRod`](./Enums.md) | Object | | 3 |   |
| [`LimitDamage`](./Enums.md) | Integer | | 1 | 1 |
| [`LimitHeal`](./Enums.md) | Integer | | 1 | 1 |
| [`LimitSelfKnockbackDamage`](./Enums.md) | Integer | | 1 | 1 |
| [`LimitedTileTrail`](./Enums.md) | Enum | | 1 | FlowerTile |
| [`LineOfSightTrueSightAura`](./Enums.md) | Number | | 2 | 0 |
| [`LobbedHook`](./Enums.md) | Integer | | 2 | 2 |
| [`LowHealthAllyDodgeChanceAura`](./Enums.md) | Object | | 2 |   |
| [`Madness`](./Enums.md) | Integer | | 9 | 1 |
| [`MakeBasicAttackPassThroughThings`](./Enums.md) | Integer | | 2 | 1 |
| [`MakeSpellsRequireCharge`](./Enums.md) | Integer | | 4 | 1 |
| [`ManaCostReduction`](./Enums.md) | Integer | | 5 | 2 |
| [`ManaCostReductionTagged`](./Enums.md) | Object | | 6 |   |
| [`ManaRegenMultiplierIfManaEmpty`](./Enums.md) | Integer | | 2 | 2 |
| [`MaxAccuracy`](./Enums.md) | Integer | | 1 | 1 |
| [`MaxStartingMana`](./Enums.md) | Integer | | 1 | 1 |
| [`MegaMinions`](./Enums.md) | Integer / Object | | 3 | 3 |
| [`MeleeRevengeDamage`](./Enums.md) | Object | | 8 |   |
| [`Metal`](./Enums.md) | Integer | | 2 | 1 |
| [`MetalDetector`](./Enums.md) | Integer | | 3 | 5 |
| [`MinimumTech`](./Enums.md) | Integer | | 2 | 1 |
| [`MissChance`](./Enums.md) | Integer | | 14 | 15 |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md) | Enum | | 2 | EatShit |
| [`MoveAwayFromDamageSource`](./Enums.md) | Enum | | 1 | MoveOne |
| [`MoveQuivered`](./Enums.md) | Integer | | 11 | 2 |
| [`MoveRandomly`](./Enums.md) | Integer | | 1 | 1 |
| [`MoveSpeedMultiplier`](./Enums.md) | Number | | 1 | .5 |
| [`MoveTowardsDamageSource`](./Enums.md) | Object | | 3 |   |
| [`MoveWhenDamaged`](./Enums.md) | Object | | 1 |   |
| [`MovementReaction`](./Enums.md) | Object | | 2 |   |
| [`MulticlassLevelUp`](./Enums.md) | Enum | | 24 | Druid |
| [`NeckArmorPassiveMultiplierBonus`](./Enums.md) | Integer | | 1 | 2 |
| [`NoManaRegen`](./Enums.md) | Integer | | 1 | 1 |
| [`NoReflection`](./Enums.md) | Integer | | 2 | 1 |
| [`NubbyTossPriority`](./Enums.md) | Integer | | 2 | 1 |
| [`NumbingLeeches`](./Enums.md) | Integer | | 3 | 3 |
| [`OverhealGainsBothShield`](./Enums.md) | Integer | | 2 | 2 |
| [`OverrideBasicAttack`](./Enums.md) | Enum | | 2 | GerdShot |
| [`OverrideMaxHealth`](./Enums.md) | Integer | | 1 | 1 |
| [`OverrideMaxMana`](./Enums.md) | Integer | | 1 | 1 |
| [`OverridePalette`](./Enums.md) | Integer | | 1 | 87 |
| [`Paranoia`](./Enums.md) | Enum | | 2 | ParanoiaBasicMelee |
| [`ParasitesArentCursed`](./Enums.md) | Integer | | 2 | 1 |
| [`PassiveAfterXKills`](./Enums.md) | Object | | 2 |   |
| [`PassiveAtFullHealth`](./Enums.md) | Object | | 2 |   |
| [`PassiveAtHealthThreshold`](./Enums.md) | Object | | 4 |   |
| [`PassiveAtInjuryThreshold`](./Enums.md) | Object | | 2 |   |
| [`PassiveAtStatThreshold`](./Enums.md) | Object | | 10 |   |
| [`PassiveIfAllArmorEmpty`](./Enums.md) | Object | | 8 |   |
| [`PassiveIfEmptyFace`](./Enums.md) | Object | | 7 |   |
| [`PassiveIfEmptyHead`](./Enums.md) | Object | | 7 |   |
| [`PassiveIfEmptyNeck`](./Enums.md) | Object | | 7 |   |
| [`PassiveLevelScaledStatus`](./Enums.md) | Object | | 1 |   |
| [`PassiveLevelUpAtCombatEnd`](./Enums.md) | Integer | | 10 | 1 |
| [`PassiveUntilCastSpell`](./Enums.md) | Object | | 2 |   |
| [`PassiveUntilGetKill`](./Enums.md) | Object | | 2 |   |
| [`PassiveWhenAffectedByElement`](./Enums.md) | Object | | 4 |   |
| [`PassiveWhenAtFullMana`](./Enums.md) | Object | | 4 |   |
| [`PassiveWhenTheAlpha`](./Enums.md) | Object | | 2 |   |
| [`PassiveWhileInMonkMeleeStance`](./Enums.md) | Object | | 2 |   |
| [`PassiveWhileInMonkRangedStance`](./Enums.md) | Object | | 2 |   |
| [`PassiveWhilePreviewingMonkRangedStance`](./Enums.md) | Object | | 2 |   |
| [`PassiveWhileWearingMetal`](./Enums.md) | Object | | 2 |   |
| [`PermanentImmobile`](./Enums.md) | Integer | | 1 | 1 |
| [`PermanentItems`](./Enums.md) | Integer | | 2 | 2 |
| [`PermanentKitten`](./Enums.md) | Integer | | 1 | 1 |
| [`PermanentMadness`](./Enums.md) | Integer | | 4 | 1 |
| [`Phasing`](./Enums.md) | Integer | | 1 | 1 |
| [`Poison`](./Enums.md) | Array / Enum / Integer | | 22 | [.5] |
| [`PoisonMultiplier`](./Enums.md) | Integer | | 1 | 2 |
| [`PoisonThorns`](./Enums.md) | Integer | | 4 | 2 |
| [`PoopWhenHit`](./Enums.md) | Enum | | 1 | Poop |
| [`ProtectTargetedAllies`](./Enums.md) | Enum | | 2 | SwapPositions_WideLoad2 |
| [`Quiver`](./Enums.md) | Integer | | 3 | 2 |
| [`Quivered`](./Enums.md) | Integer | | 15 | 2 |
| [`RandomPassivePool`](./Enums.md) | Object | | 1 |   |
| [`RangedTrueShot`](./Enums.md) | Integer | | 2 | 1 |
| [`RealTimePressure_OneUnit`](./Enums.md) | Integer | | 1 | 5 |
| [`ReceivedStatusReplacement`](./Enums.md) | Array | | 1 | [Sleep] |
| [`RefreshMoveOnWeaponConnect`](./Enums.md) | Integer | | 1 | 1 |
| [`RemoveLineOfSightRestrictions`](./Enums.md) | Integer | | 2 | 1 |
| [`RemoveOncePerFightRestriction`](./Enums.md) | Integer | | 2 | 1 |
| [`ReplaceBasicAttack`](./Enums.md) | Enum | | 8 | BasicButcherMeleeWideDoubleSpin |
| [`ReplaceBasicAttackWhenCastable`](./Enums.md) | Enum | | 6 | Shank2 |
| [`ReplaceBasicAttackWhenDead`](./Enums.md) | Enum | | 2 | Haunt |
| [`ReplaceBasicMove`](./Enums.md) | Enum | | 6 | ToadJump_BasicMove |
| [`ReplaceBrain`](./Enums.md) | Object | | 1 |   |
| [`ReplaceSpawnedObjects`](./Enums.md) | Array | | 13 | [Boulder] |
| [`ReplaceSpellsWhenDead`](./Enums.md) | Enum | | 1 | Spook |
| [`RevengeDamage`](./Enums.md) | Object | | 9 |   |
| [`ReviveOnWin`](./Enums.md) | Integer | | 2 | 100 |
| [`Robot`](./Enums.md) | Object | | 1 |   |
| [`RobotsInheritArmor`](./Enums.md) | Integer | | 2 | 2 |
| [`RockDetector`](./Enums.md) | Integer | | 2 | 10 |
| [`SafeExplosions`](./Enums.md) | Integer | | 2 | 1 |
| [`ScaledStatusOnBleedDamage`](./Enums.md) | Object | | 1 |   |
| [`ScaledStatusOnLoseShield`](./Enums.md) | Object | | 1 |   |
| [`ScaledStatusOnOverHealed`](./Enums.md) | Object | | 1 |   |
| [`ScaledStatusOnOverMana`](./Enums.md) | Object | | 2 |   |
| [`ScaledStatusOnSpendMana`](./Enums.md) | Object | | 2 |   |
| [`SchrodingerDisorder`](./Enums.md) | Integer | | 2 | 50 |
| [`Scleroderma`](./Enums.md) | Integer | | 2 | 1 |
| [`SecurityBotProtect`](./Enums.md) | Object | | 2 |   |
| [`SelfDamageWhenDealDamage`](./Enums.md) | Object | | 1 |   |
| [`SetDefaultFacePassive`](./Enums.md) | Enum | | 1 | insane |
| [`SetSpellCosts`](./Enums.md) | Integer | | 6 | 3 |
| [`ShareHealthRegen`](./Enums.md) | Integer | | 2 | 1 |
| [`SharePickups`](./Enums.md) | Integer | | 2 | 1 |
| [`ShoulderCheck`](./Enums.md) | Integer | | 3 | 33 |
| [`ShovingMatch`](./Enums.md) | Enum | | 3 | attack |
| [`ShowHiddenThings`](./Enums.md) | Integer | | 2 | 1 |
| [`SizeScale`](./Enums.md) | Number | | 8 | .4 |
| [`Slow`](./Enums.md) | Enum / Integer | | 12 | 2 |
| [`SmallEnemiesIgnoreYou`](./Enums.md) | Integer | | 2 | 1 |
| [`SmallRockBehavior`](./Enums.md) | Integer | | 1 | 5 |
| [`SmiteEnemiesWhoKill`](./Enums.md) | Object | | 2 |   |
| [`SpawnCatCopyOnBattleStart`](./Enums.md) | Object | | 3 |   |
| [`SpawnCreepOnHit`](./Enums.md) | Integer | | 1 | 1 |
| [`SpawnEachTurn`](./Enums.md) | Object | | 6 |   |
| [`SpawnMeatOnMove`](./Enums.md) | Enum | | 1 | Food |
| [`SpawnObjectOnPopCorpse`](./Enums.md) | Enum | | 2 | Food |
| [`SpawnOnBattleStart`](./Enums.md) | Enum / Object | | 21 | CharmedTinySpider |
| [`SpawnOnBattleStartRandomEmptyTile`](./Enums.md) | Object | | 3 |   |
| [`SpawnThingOnDamage`](./Enums.md) | Object | | 6 |   |
| [`SpawnThingOnDeath`](./Enums.md) | Enum | | 4 | CharmedDemonKitten |
| [`SpecialFriends`](./Enums.md) | Object | | 3 |   |
| [`SpeedUp`](./Enums.md) | Integer | | 21 | 2 |
| [`SplittableMove`](./Enums.md) | Integer | | 2 | 3 |
| [`SpreadExtraDebuffs`](./Enums.md) | Integer | | 2 | 2 |
| [`SpreadPainBonus`](./Enums.md) | Integer | | 2 | 2 |
| [`SpreadPainBonusCrit`](./Enums.md) | Integer | | 1 | 1 |
| [`StackingDodgeChanceOnTookDamage`](./Enums.md) | Object | | 1 |   |
| [`StatMinimum`](./Enums.md) | Integer | | 2 | 7 |
| [`StatsAtLowHealth`](./Enums.md) | Object | | 2 |   |
| [`StatusAdjacentOnTheirTurnBegin`](./Enums.md) | Object | | 1 |   |
| [`StatusAfterCastSpell`](./Enums.md) | Object | | 2 |   |
| [`StatusAlliesOnBattleStart`](./Enums.md) | Object | | 2 |   |
| [`StatusAlliesOnDeath`](./Enums.md) | Object | | 7 |   |
| [`StatusAlliesOnGainCoins`](./Enums.md) | Object | | 2 |   |
| [`StatusAlliesOnKill`](./Enums.md) | Object | | 4 |   |
| [`StatusAlliesOnSpendMana`](./Enums.md) | Object | | 1 |   |
| [`StatusAlliesScaledByCursedOnDeath`](./Enums.md) | Object | | 1 |   |
| [`StatusAllyWhenAllySpendsMana`](./Enums.md) | Object | | 2 |   |
| [`StatusAnyCatAllyWhoKills`](./Enums.md) | Object | | 2 |   |
| [`StatusCarefulness`](./Enums.md) | Integer | | 1 | 1 |
| [`StatusDamagers`](./Enums.md) | Object | | 2 |   |
| [`StatusEachTurnBegin`](./Enums.md) | Object | | 12 |   |
| [`StatusEachTurnEnd`](./Enums.md) | Object | | 20 |   |
| [`StatusEachTurnEndForEachTurn`](./Enums.md) | Object | | 2 |   |
| [`StatusEachTurnEndPerEnemyKill`](./Enums.md) | Object | | 2 |   |
| [`StatusEnemiesOnDeath`](./Enums.md) | Object | | 2 |   |
| [`StatusEveryXSpellCasts`](./Enums.md) | Object | | 3 |   |
| [`StatusEveryXTurnBegins`](./Enums.md) | Object | | 2 |   |
| [`StatusIfBattleAlreadyBegan`](./Enums.md) | Object | | 1 |   |
| [`StatusIfUnusedMovePoints`](./Enums.md) | Object | | 4 |   |
| [`StatusImmunity`](./Enums.md) | Array / Enum | | 8 | [Sleep] |
| [`StatusKilledCharacters`](./Enums.md) | Object | | 3 |   |
| [`StatusKillers`](./Enums.md) | Object | | 2 |   |
| [`StatusOnAllyCatDeath`](./Enums.md) | Object | | 3 |   |
| [`StatusOnAnyDeath`](./Enums.md) | Object | | 2 |   |
| [`StatusOnBattleEnd`](./Enums.md) | Object | | 16 |   |
| [`StatusOnBattleEndIfKillThresholdMet`](./Enums.md) | Object | | 2 |   |
| [`StatusOnBattleStart`](./Enums.md) | Object | | 3 |   |
| [`StatusOnBreakItem`](./Enums.md) | Object | | 2 |   |
| [`StatusOnCastSpell`](./Enums.md) | Object | | 5 |   |
| [`StatusOnCollectPickup`](./Enums.md) | Object | | 2 |   |
| [`StatusOnCrit`](./Enums.md) | Object | | 8 |   |
| [`StatusOnDealtDamage`](./Enums.md) | Object | | 2 |   |
| [`StatusOnDealtDamageThreshold`](./Enums.md) | Object | | 2 |   |
| [`StatusOnEatFood`](./Enums.md) | Object | | 3 |   |
| [`StatusOnEatPill`](./Enums.md) | Object | | 1 |   |
| [`StatusOnEndMove`](./Enums.md) | Object | | 2 |   |
| [`StatusOnGainCoins`](./Enums.md) | Object | | 3 |   |
| [`StatusOnGainShield`](./Enums.md) | Object | | 2 |   |
| [`StatusOnHeal`](./Enums.md) | Object | | 2 |   |
| [`StatusOnHealed`](./Enums.md) | Object | | 3 |   |
| [`StatusOnKill`](./Enums.md) | Object | | 16 |   |
| [`StatusOnKillEnemy`](./Enums.md) | Object | | 3 |   |
| [`StatusOnLoseShield`](./Enums.md) | Object | | 1 |   |
| [`StatusOnOverHealed`](./Enums.md) | Object | | 5 |   |
| [`StatusOnOverMana`](./Enums.md) | Object | | 2 |   |
| [`StatusOnPickupCoins`](./Enums.md) | Object | | 2 |   |
| [`StatusOnPopCorpse`](./Enums.md) | Object | | 2 |   |
| [`StatusOnStanceSwitch`](./Enums.md) | Object | | 14 |   |
| [`StatusOnTakeHealthDamage`](./Enums.md) | Object | | 1 |   |
| [`StatusOnTookDamage`](./Enums.md) | Object | | 21 |   |
| [`StatusOnTookDamageFromAbility`](./Enums.md) | Object | | 3 |   |
| [`StatusOnTookDamageFromEnemyAbility`](./Enums.md) | Object | | 2 |   |
| [`StatusOnTriggerTrap`](./Enums.md) | Object | | 2 |   |
| [`StatusOnTurnEndIfCastNSpells`](./Enums.md) | Object | | 4 |   |
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](./Enums.md) | Object | | 1 |   |
| [`StatusOnTurnEndIfManaExact`](./Enums.md) | Object | | 4 |   |
| [`StatusOnTurnEndIfManaOrHealthExact`](./Enums.md) | Object | | 4 |   |
| [`StatusOnUseAbilityWithTag`](./Enums.md) | Object | | 7 |   |
| [`StatusOnUseBasicAttack`](./Enums.md) | Object | | 2 |   |
| [`StatusOnUseElementAbility`](./Enums.md) | Object | | 2 |   |
| [`StatusPerInjury`](./Enums.md) | Object | | 2 |   |
| [`StatusReplacement`](./Enums.md) | Array | | 2 | [Petrify] |
| [`StatusThingsKnockedBack`](./Enums.md) | Object | | 2 |   |
| [`StatusWhenAllySpendsMana`](./Enums.md) | Object | | 2 |   |
| [`Stealth`](./Enums.md) | Integer | | 3 | 1 |
| [`StrengthForEachNeighboringEnemy`](./Enums.md) | Integer | | 2 | 2 |
| [`StrengthInNumbersAura`](./Enums.md) | Integer / Object | | 2 | 1 |
| [`StrengthUp`](./Enums.md) | Integer | | 13 | 2 |
| [`StrictLimitDamage`](./Enums.md) | Integer | | 1 | 1 |
| [`Study`](./Enums.md) | Integer / Object | | 3 | 1 |
| [`TaggedPickupEffectReplacement`](./Enums.md) | Object | | 2 |   |
| [`TauntAlways`](./Enums.md) | Integer | | 3 | 1 |
| [`TauntAtFullHealth`](./Enums.md) | Integer | | 1 | 1 |
| [`Tech`](./Enums.md) | Integer | | 6 | 1 |
| [`TempInitiativeChange`](./Enums.md) | Integer | | 1 | -999 |
| [`TheHunger`](./Enums.md) | Object | | 2 |   |
| [`Thorns`](./Enums.md) | Integer | | 17 | 2 |
| [`TileDamageMultiplier`](./Enums.md) | Integer / Object | | 2 | 2 |
| [`TileTrail`](./Enums.md) | Enum | | 3 | FlowerTile |
| [`TourettesMeows`](./Enums.md) | Object | | 1 |   |
| [`TowerDefense`](./Enums.md) | Object | | 3 |   |
| [`TowerDefenseReflex`](./Enums.md) | Enum | | 2 | BasicRanged_1DMG |
| [`Trample`](./Enums.md) | Array / Integer | | 10 | [3] |
| [`TrapEffectsMultiplier`](./Enums.md) | Integer | | 2 | 2 |
| [`TrinketActiveEffectsMultiplierBonus`](./Enums.md) | Integer | | 3 | 2 |
| [`TrinketPassiveMultiplierBonus`](./Enums.md) | Integer | | 3 | 2 |
| [`Triskaidekaphobia`](./Enums.md) | Integer | | 2 | 13 |
| [`UncappedHP`](./Enums.md) | Integer | | 3 | 1 |
| [`UncappedHPBonusStr`](./Enums.md) | Integer | | 1 | 5 |
| [`UncappedMana`](./Enums.md) | Integer | | 3 | 1 |
| [`UpgradeLevelUpClassActives`](./Enums.md) | Enum | | 2 | Colorless |
| [`UpgradeLevelUpClassPassives`](./Enums.md) | Enum | | 2 | Colorless |
| [`UpgradeSpawnedPickups`](./Enums.md) | Integer | | 2 | 2 |
| [`Vegan`](./Enums.md) | Integer | | 2 | 1 |
| [`Vengeful`](./Enums.md) | Integer | | 3 | 1 |
| [`WaterWalk`](./Enums.md) | Integer | | 4 | 1 |
| [`Weakness`](./Enums.md) | Enum / Integer | | 18 | 2 |
| [`WeaponActiveEffectsMultiplierBonus`](./Enums.md) | Integer | | 1 | 2 |
| [`WeaponCountsAsBasicAttack`](./Enums.md) | Integer | | 2 | 1 |
| [`WeaponDamageMultiplierBonus`](./Enums.md) | Integer | | 2 | 2 |
| [`WeaponPassiveMultiplierBonus`](./Enums.md) | Integer | | 1 | 2 |
| [`WeaponsDontLoseDurability`](./Enums.md) | Integer | | 1 | 0 |
| [`WobblyCat`](./Enums.md) | Integer | | 2 | 25 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `stats`


**Definition:** Core character metrics (Health, Strength, etc.).  
**Total Count:** 97


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `con` | Enum / Integer |  | 65 |  |
| `spd` | Enum / Integer |  | 53 |  |
| `cha` | Enum / Integer |  | 46 |  |
| `int` | Enum / Integer |  | 46 |  |
| `str` | Enum / Integer |  | 42 |  |
| `dex` | Enum / Integer |  | 34 |  |
| `lck` | Enum / Integer |  | 29 |  |

</details>

---

### Object: `AddStatusToBasicAttack`


**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 92


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToCharmed`](./Passives_and_Statuses.md#context-addpassivestocharmed), [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#context-passivewhenatfullmana), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 187 |  |
| [`ApplyStatusIfCrit`](./Enums.md) | Object | | 2 |   |
| [`ApplyToSource`](./Enums.md) | Object | | 2 |   |
| [`BigSplashDamage`](./Enums.md) | Integer | | 1 | 2 |
| [`Bleed`](./Enums.md) | Array / Integer | | 23 | [.1] |
| [`Blind`](./Enums.md) | Integer | | 4 | 1 |
| [`BounceObject`](./Enums.md) | Enum | | 4 | CharmedLeech |
| [`Bruise`](./Enums.md) | Integer | | 15 | 2 |
| [`BurgleCoin`](./Enums.md) | Integer | | 2 | 1 |
| [`Burn`](./Enums.md) | Enum / Integer | | 28 | 2 |
| [`ChangeTile`](./Enums.md) | Enum / Object | | 4 | FloatingGlassTile |
| [`Charmed`](./Enums.md) | Array / Integer | | 14 | [.40] |
| [`Conditional_Adjacent`](./Enums.md) | Object | | 2 |   |
| [`Conditional_Ally`](./Enums.md) | Object | | 11 |   |
| [`Conditional_Enemy`](./Enums.md) | Object | | 7 |   |
| [`Conditional_HasTag`](./Enums.md) | Object | | 2 |   |
| [`Conditional_Shielded`](./Enums.md) | Object | | 2 |   |
| [`Conditional_SourceHasTag`](./Enums.md) | Object | | 1 |   |
| [`Confusion`](./Enums.md) | Integer | | 11 | 2 |
| [`DamageOrHealConditionally`](./Enums.md) | Integer | | 1 | 1 |
| [`DistanceBonusDamage`](./Enums.md) | Object | | 4 |   |
| [`Else`](./Enums.md) | Object | | 6 |   |
| [`Fear`](./Enums.md) | Array / Integer | | 10 | [.15] |
| [`Freeze`](./Enums.md) | Array / Integer | | 12 | [.15] |
| [`KnockOutCoin`](./Enums.md) | Array / Integer | | 2 | [.5] |
| [`Knockback`](./Enums.md) | Integer | | 7 | 3 |
| [`Leech`](./Enums.md) | Integer | | 3 | 1 |
| [`Leeches`](./Enums.md) | Integer | | 2 | 1 |
| [`LuckUp`](./Enums.md) | Integer | | 15 | 2 |
| [`Madness`](./Enums.md) | Integer | | 9 | 1 |
| [`MagicWeakness`](./Enums.md) | Integer | | 5 | 2 |
| [`ManaLeeches`](./Enums.md) | Integer | | 1 | 1 |
| [`OverrideChainKnockback`](./Enums.md) | Integer | | 1 | 0 |
| [`OverrideChainKnockbackDamage`](./Enums.md) | Integer | | 1 | 0 |
| [`Piercing`](./Enums.md) | Integer | | 4 | 1 |
| [`Poison`](./Enums.md) | Array / Enum / Integer | | 22 | [.5] |
| [`Rot`](./Enums.md) | Integer | | 4 | -999999 |
| [`Slow`](./Enums.md) | Enum / Integer | | 12 | 2 |
| [`SoulLink`](./Enums.md) | Integer | | 2 | 1 |
| [`SpawnBearTrapOnMiss`](./Enums.md) | Integer | | 2 | 1 |
| [`SplashDamage`](./Enums.md) | Integer | | 1 | 2 |
| [`SpreadDisease`](./Enums.md) | Object | | 12 |   |
| [`Stun`](./Enums.md) | Array / Integer | | 19 | [.05*X] |
| [`Weakness`](./Enums.md) | Enum / Integer | | 18 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `effects`


**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 30


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#context-damageneighborsaftermove), [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#context-damageneighborsonendmove), [`GravityWell`](./Passives_and_Statuses.md#context-gravitywell), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`RevengeDamage`](./Passives_and_Statuses.md#context-revengedamage), [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#context-smiteenemieswhokill), [`fire`](./Passives_and_Statuses.md#context-fire), [`ice`](./Passives_and_Statuses.md#context-ice), [`lightning`](./Passives_and_Statuses.md#context-lightning), [`triattack`](./Passives_and_Statuses.md#context-triattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1390 |  |
| [`Bleed`](./Enums.md) | Array / Integer | | 23 | [.1] |
| [`Bruise`](./Enums.md) | Integer | | 15 | 2 |
| [`Burn`](./Enums.md) | Enum / Integer | | 28 | 2 |
| [`Charmed`](./Enums.md) | Array / Integer | | 14 | [.40] |
| [`Fear`](./Enums.md) | Array / Integer | | 10 | [.15] |
| [`Freeze`](./Enums.md) | Array / Integer | | 12 | [.15] |
| [`Immobile`](./Enums.md) | Integer | | 4 | 1 |
| [`Leeches`](./Enums.md) | Integer | | 2 | 1 |
| [`Madness`](./Enums.md) | Integer | | 9 | 1 |
| [`Marked`](./Enums.md) | Integer | | 7 | 1 |
| [`Petrify`](./Enums.md) | Array / Integer | | 6 | [.2] |
| [`Poison`](./Enums.md) | Array / Enum / Integer | | 22 | [.5] |
| [`Slow`](./Enums.md) | Enum / Integer | | 12 | 2 |
| [`SpreadDisease`](./Enums.md) | Object | | 12 |   |
| [`Stun`](./Enums.md) | Array / Integer | | 19 | [.05*X] |
| [`VisualFXTile`](./Enums.md) | Enum | | 12 | IcePoof |
| [`Weakness`](./Enums.md) | Enum / Integer | | 18 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AddPassivesToMinions`


**Definition:** Applies the 'AddPassivesToMinions' effect.  
**Total Count:** 29


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 44 |  |
| [`AddMaxHealth`](./Enums.md) | Integer | | 4 | 5 |
| [`AddSpeed`](./Enums.md) | Integer | | 4 | 4 |
| [`AddStatusToBasicAttack`](./Enums.md) | Object | | 92 |   |
| [`AddStatusToExplosions`](./Enums.md) | Object | | 4 |   |
| [`AddUnfilledMaxHealth`](./Enums.md) | Integer | | 3 | 20 |
| [`DamageUp`](./Enums.md) | Integer | | 26 | 2 |
| [`DivineShield`](./Enums.md) | Integer | | 10 | 1 |
| [`EMP`](./Enums.md) | Object | | 5 |   |
| [`FamiliarBonusAbility`](./Enums.md) | Enum | | 2 | FamiliarSelfDestruct |
| [`ForceAttack`](./Enums.md) | Integer | | 4 | 1 |
| [`FreePathfindElement`](./Enums.md) | Enum | | 6 | Grass |
| [`GrassTileHealing`](./Enums.md) | Integer | | 2 | 1 |
| [`HealthGain`](./Enums.md) | Integer / String | | 20 | 2*X |
| [`HealthRegenUp`](./Enums.md) | Integer | | 14 | 2 |
| [`HolyShieldTransferToSpawner`](./Enums.md) | Integer | | 2 | 1 |
| [`IncreaseExplosionDamage`](./Enums.md) | Integer | | 8 | 2 |
| [`IncreaseExplosionSize`](./Enums.md) | Integer | | 4 | 2 |
| [`PassiveWhenAffectedByElement`](./Enums.md) | Object | | 4 |   |
| [`PoisonThorns`](./Enums.md) | Integer | | 4 | 2 |
| [`Quivered`](./Enums.md) | Integer | | 15 | 2 |
| [`SafeExplosions`](./Enums.md) | Integer | | 2 | 1 |
| [`StatusAlliesOnKill`](./Enums.md) | Object | | 4 |   |
| [`StatusOnKill`](./Enums.md) | Object | | 16 |   |
| [`TakeExtraTurn`](./Enums.md) | Integer | | 9 | 1 |
| [`UncappedHP`](./Enums.md) | Integer | | 3 | 1 |
| [`WaterWalk`](./Enums.md) | Integer | | 4 | 1 |
| [`tag_filter`](./Enums.md) | Enum | | 2 | crow |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `SpawnOnBattleStart`


**Definition:** No definition provided.  
**Total Count:** 21


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum |  | 72 |  |
| [`number`](./Arrays.md#array-number) | Array / Integer |  | 48 |  |

</details>

---

### Object: `StatusOnTookDamage`


**Definition:** Event Trigger: Applies nested statuses when took damage.  
**Total Count:** 21


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 40 |  |
| [`Conditional_HasStatus`](./Enums.md) | Object | | 3 |   |
| [`ConstitutionUp`](./Enums.md) | Integer | | 4 | 2 |
| [`Craft`](./Enums.md) | Object | | 2 |   |
| [`DamageUp`](./Enums.md) | Integer | | 26 | 2 |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | | 5 | 2 |
| [`Else`](./Enums.md) | Object | | 6 |   |
| [`IntelligenceUp`](./Enums.md) | Integer | | 11 | -1 |
| [`MovementUp`](./Enums.md) | Integer | | 3 | 2 |
| [`RandomInjury`](./Enums.md) | Integer | | 1 | 1 |
| [`RandomStatUp`](./Enums.md) | Integer | | 11 | 2 |
| [`RandomStatusFromPool`](./Enums.md) | Object | | 8 |   |
| [`Shield`](./Enums.md) | Integer / String | | 21 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | | 21 | 2 |
| [`StrengthUp`](./Enums.md) | Integer | | 13 | 2 |
| [`TempDamageUp`](./Enums.md) | Integer | | 4 | 2 |
| [`TempMovement`](./Enums.md) | Integer | | 1 | 1 |
| [`Temporary`](./Enums.md) | Object | | 11 |   |
| [`Thorns`](./Enums.md) | Integer | | 17 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusEachTurnEnd`


**Definition:** Applies or references the 'StatusEachTurnEnd' effect/state.  
**Total Count:** 20


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 55 |  |
| [`EmptyMana`](./Enums.md) | Integer | | 2 | 1 |
| [`ForceUseAbility`](./Enums.md) | Enum / Object | | 10 | Hallucinate_Disorder |
| [`IntelligenceUp`](./Enums.md) | Integer | | 11 | -1 |
| [`KineticSpikes`](./Enums.md) | Integer | | 10 | 2 |
| [`NonStackingDivineShield`](./Enums.md) | Integer | | 4 | 1 |
| [`ObjectOnHitCharacter`](./Enums.md) | Enum / Object | | 11 | Coin |
| [`PermanentMadness`](./Enums.md) | Integer | | 4 | 1 |
| [`RangeUp`](./Enums.md) | Integer | | 2 | 1 |
| [`SpeedUp`](./Enums.md) | Integer | | 21 | 2 |
| [`StrengthUp`](./Enums.md) | Integer | | 13 | 2 |
| [`UseAbility_Madness`](./Enums.md) | Enum | | 1 | weapon |

</details>

---

### Object: `lock_item_slot`


**Definition:** No definition provided.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum / Integer |  | 20 |  |
| `frame` | Integer |  | 6 |  |

</details>

---

### Object: `StatusOnBattleEnd`


**Definition:** Applies the nested status effects when the encounter finishes.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 58 |  |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 50 |  |
| [`CureDisease`](./Enums.md) | Object | | 6 |   |
| [`FindItemFromPool`](./Enums.md) | Enum / Object | | 5 | consumables |
| [`NextBattleStatus`](./Enums.md) | Object | | 2 |   |
| [`PermanentConstitution`](./Enums.md) | Integer | | 2 | -1 |
| [`PermanentIntelligence`](./Enums.md) | Integer | | 1 | -1 |
| [`PermanentSpeed`](./Enums.md) | Integer | | 2 | -1 |
| [`PermanentStrength`](./Enums.md) | Integer | | 1 | 2 |
| [`RandomMutation`](./Enums.md) | Integer | | 2 | 1 |
| [`RandomPermanentStat`](./Enums.md) | Integer | | 3 | 3 |

</details>

---

### Object: `StatusOnKill`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 36 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`Conditional_FirstApplicationThisTurn`](./Enums.md) | Object | | 4 |   |
| [`DamageUp`](./Enums.md) | Integer | | 26 | 2 |
| [`EquipPermanentItem`](./Enums.md) | Enum | | 2 | BoneClub |
| [`HealthGain`](./Enums.md) | Integer / String | | 20 | 2*X |
| [`LuckUp`](./Enums.md) | Integer | | 15 | 2 |
| [`RandomStatUp`](./Enums.md) | Integer | | 11 | 2 |
| [`RefreshActPoints`](./Enums.md) | Integer | | 5 | 1 |
| [`RefreshMovePoints`](./Enums.md) | Integer | | 7 | 1 |
| [`SpeedUp`](./Enums.md) | Integer | | 21 | 2 |
| [`Stealth`](./Enums.md) | Integer | | 3 | 1 |
| [`StrengthUp`](./Enums.md) | Integer | | 13 | 2 |
| [`TakeBonusTurnWithStatus`](./Enums.md) | Object | | 1 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnStanceSwitch`


**Definition:** Event Trigger: Applies nested statuses when stance switch.  
**Total Count:** 14


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#context-passiveifemptyface), [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#context-passiveifemptyhead), [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#context-passiveifemptyneck), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 |  |
| `NextBasicAttackCritsThisTurn` | `Number` | Guarantees the next basic attack executed this turn will be a critical hit. | 4 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`ForceUseAbility`](./Enums.md) | Enum / Object | | 10 | Hallucinate_Disorder |
| [`PartialCleanse`](./Enums.md) | Integer | | 1 | 1 |
| [`RandomMagicMissile`](./Enums.md) | Integer | | 17 | 2 |
| [`RandomStatUp`](./Enums.md) | Integer | | 11 | 2 |
| [`Shield`](./Enums.md) | Integer / String | | 21 | 2 |

</details>

---

### Object: `SpreadDisease`


**Definition:** Provides a chance to transmit a disease status to adjacent targets.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`effects`](./Passives_and_Statuses.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`disease`](./Enums.md#enum-disease) | Enum | The specific status effect ID representing the disease. | 26 |  |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of transmitting. | 24 |  |
| `can_apply_to_anything` | Boolean |  | 12 |  |

</details>

---

### Object: `StatusEachTurnBegin`


**Definition:** Event Trigger: Applies nested statuses to each turn begin.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |  |
| [`Conditional_BadRoll`](./Enums.md) | Object | | 3 |   |
| [`Conditional_GoodRoll`](./Enums.md) | Object | | 1 |   |
| [`Fear`](./Enums.md) | Array / Integer | | 10 | [.15] |
| [`FillMana`](./Enums.md) | Array / Integer | | 4 | [.25] |
| [`ForceUseAbility`](./Enums.md) | Enum / Object | | 10 | Hallucinate_Disorder |
| [`IntelligenceUp`](./Enums.md) | Integer | | 11 | -1 |
| [`RandomStatUp`](./Enums.md) | Integer | | 11 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `Conditional_Ally`


**Definition:** Conditional trigger: Executes nested logic if the target is friendly to the caster.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#context-conditional_sourcehastag), [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#context-extrastatuswhendealingdamage), [`StatusKilledCharacters`](./Passives_and_Statuses.md#context-statuskilledcharacters)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 30 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 29 |  |
| `Cleanse` | `Number` | Applies the 'Cleanse' effect. | 6 |  |
| [`ApplyToSource`](./Passives_and_Statuses.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 4 |  |
| `ClearNegativeEffects` | `Number` | Applies the 'ClearNegativeEffects' effect. | 4 |  |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object | Selects and applies a random status effect from the provided nested block. | 4 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`DamageUp`](./Enums.md) | Integer | | 26 | 2 |
| [`Shield`](./Enums.md) | Integer / String | | 21 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | | 21 | 2 |
| [`TempSpeedUp`](./Enums.md) | Integer | | 5 | 10 |

</details>

---

### Object: `CritsApplyStatus`


**Definition:** Applies the 'CritsApplyStatus' effect.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 |  |
| [`Bleed`](./Enums.md) | Array / Integer | | 23 | [.1] |
| [`Bruise`](./Enums.md) | Integer | | 15 | 2 |
| [`Conditional_HasStatus`](./Enums.md) | Object | | 3 |   |
| [`Confusion`](./Enums.md) | Integer | | 11 | 2 |
| [`Else`](./Enums.md) | Object | | 6 |   |
| [`Immobile`](./Enums.md) | Integer | | 4 | 1 |
| [`ObjectOnHitCharacter`](./Enums.md) | Enum / Object | | 11 | Coin |
| [`Stun`](./Enums.md) | Array / Integer | | 19 | [.05*X] |
| [`Weakness`](./Enums.md) | Enum / Integer | | 18 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `Temporary`


**Definition:** A wrapper object for applying status effects that automatically expire.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_BadRoll`](./Passives_and_Statuses.md#context-conditional_badroll), [`StatusOnGainShield`](./Passives_and_Statuses.md#context-statusongainshield), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage), [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#context-statusonturnendifmanaorhealthexact)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 114 |  |
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 112 |  |
| `turns` | Array / Integer / Object | Duration in turns. | 104 |  |
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 50 |  |
| `expires_on_end_turn` | Boolean |  | 42 |  |

</details>

---

### Object: `PassiveAtStatThreshold`


**Definition:** Applies the 'PassiveAtStatThreshold' effect.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 33 |  |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 26 |  |
| [`passives`](./Enums.md) | Object | | 884 |   |
| [`threshold`](./Enums.md) | Integer / Object | | 22 | 7 |

</details>

---

### Object: `threshold`


**Definition:** Examples: `4*champion_multiplier, 3*champion_multiplier, 1`  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `int` | Enum / Integer |  | 16 |  |
| `cha` | Enum / Integer |  | 4 |  |
| `spd` | Enum / Integer |  | 4 |  |

</details>

---

### Object: `RevengeDamage`


**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 58 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |  |
| `knockback` | Enum / Integer |  | 6 |  |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `MeleeRevengeDamage`


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 94 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 75 |  |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 44 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 36 |  |
| [`elements`](./Arrays.md#array-elements) | Array |  | 4 |  |
| [`Poison`](./Enums.md) | Array / Enum / Integer | | 22 | [.5] |
| [`SpreadDisease`](./Enums.md) | Object | | 12 |   |
| [`Weakness`](./Enums.md) | Enum / Integer | | 18 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `PassiveIfAllArmorEmpty`


**Definition:** Applies the 'PassiveIfAllArmorEmpty' effect.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |  |
| [`AddSpellDamage`](./Enums.md) | Integer | | 6 | 2 |
| [`CounterAttack`](./Enums.md) | Enum | | 4 | ReflexPunchJab |
| [`CritsApplyStatus`](./Enums.md) | Object | | 11 |   |
| [`ExtraMovePoints`](./Enums.md) | Integer | | 8 | 1 |
| [`Flying`](./Enums.md) | Integer | | 6 | 1 |
| [`ManaCostReduction`](./Enums.md) | Integer | | 5 | 2 |
| [`StatusOnStanceSwitch`](./Enums.md) | Object | | 14 |   |

</details>

---

### Object: `RandomStatusFromPool`


**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`StatusOnGainCoins`](./Passives_and_Statuses.md#context-statusongaincoins), [`StatusOnHealed`](./Passives_and_Statuses.md#context-statusonhealed), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 35 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`Bleed`](./Enums.md) | Array / Integer | | 23 | [.1] |
| [`BleedThorns`](./Enums.md) | Integer | | 3 | 2 |
| [`Blind`](./Enums.md) | Integer | | 4 | 1 |
| [`Brace`](./Enums.md) | Integer | | 22 | 2 |
| [`Bruise`](./Enums.md) | Integer | | 15 | 2 |
| [`Burn`](./Enums.md) | Enum / Integer | | 28 | 2 |
| [`Charge`](./Enums.md) | Integer | | 5 | 2 |
| [`Charmed`](./Enums.md) | Array / Integer | | 14 | [.40] |
| [`Confusion`](./Enums.md) | Integer | | 11 | 2 |
| [`ConstitutionUp`](./Enums.md) | Integer | | 4 | 2 |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | | 5 | 2 |
| [`DivineShield`](./Enums.md) | Integer | | 10 | 1 |
| [`Fear`](./Enums.md) | Array / Integer | | 10 | [.15] |
| [`Freeze`](./Enums.md) | Array / Integer | | 12 | [.15] |
| [`Immobile`](./Enums.md) | Integer | | 4 | 1 |
| [`KineticSpikes`](./Enums.md) | Integer | | 10 | 2 |
| [`Madness`](./Enums.md) | Integer | | 9 | 1 |
| [`MagicWeakness`](./Enums.md) | Integer | | 5 | 2 |
| [`Marked`](./Enums.md) | Integer | | 7 | 1 |
| [`MoveQuivered`](./Enums.md) | Integer | | 11 | 2 |
| [`ObjectOnHitCharacter`](./Enums.md) | Enum / Object | | 11 | Coin |
| [`Petrify`](./Enums.md) | Array / Integer | | 6 | [.2] |
| [`Poison`](./Enums.md) | Array / Enum / Integer | | 22 | [.5] |
| [`Quivered`](./Enums.md) | Integer | | 15 | 2 |
| [`Reflect`](./Enums.md) | Integer | | 2 | 1 |
| [`Shield`](./Enums.md) | Integer / String | | 21 | 2 |
| [`Sleep`](./Enums.md) | Integer | | 5 | 1 |
| [`Slow`](./Enums.md) | Enum / Integer | | 12 | 2 |
| [`SpawnCoinAnywhere`](./Enums.md) | Integer | | 3 | 1 |
| [`SpeedUp`](./Enums.md) | Integer | | 21 | 2 |
| [`StatusGroup`](./Enums.md) | Object | | 3 |   |
| [`StrengthUp`](./Enums.md) | Integer | | 13 | 2 |
| [`Stun`](./Enums.md) | Array / Integer | | 19 | [.05*X] |
| [`Tarred`](./Enums.md) | Integer | | 2 | 1 |
| [`Thorns`](./Enums.md) | Integer | | 17 | 2 |
| [`Weakness`](./Enums.md) | Enum / Integer | | 18 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnCrit`


**Definition:** Event Trigger: Applies nested statuses when crit.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |  |
| [`CritChanceUp`](./Enums.md) | Integer | | 29 | 80 |
| [`DamageUp`](./Enums.md) | Integer | | 26 | 2 |
| [`LuckUp`](./Enums.md) | Integer | | 15 | 2 |
| [`RandomStatUp`](./Enums.md) | Integer | | 11 | 2 |
| [`Shield`](./Enums.md) | Integer / String | | 21 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `Conditional_Enemy`


**Definition:** Conditional trigger: Executes nested logic if the target is hostile to the caster.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_NotBoss`](./Passives_and_Statuses.md#context-conditional_notboss)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 37 |  |
| [`Conditional_PartyMember`](./Enums.md) | Object | | 2 |   |
| [`Confusion`](./Enums.md) | Integer | | 11 | 2 |
| [`Else`](./Enums.md) | Object | | 6 |   |
| [`RandomStatusFromPool`](./Enums.md) | Object | | 8 |   |
| [`Stun`](./Enums.md) | Array / Integer | | 19 | [.05*X] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `DamageNeighborsOnEndMove`


**Definition:** Combat Trigger: Deals damage to neighbors on end move.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 14 |  |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 14 |  |
| `cant_miss` | `Boolean` |  | 12 |  |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 12 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |  |
| `knockback` | Enum / Integer |  | 2 |  |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `ForceUseAbility`


**Definition:** No definition provided.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin), [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 10 |  |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 6 |  |

</details>

---

### Object: `PassiveIfEmptyFace`


**Definition:** Applies the 'PassiveIfEmptyFace' effect.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |  |
| [`AddCritMultiplier`](./Enums.md) | Integer | | 23 | 200 |
| [`CritChanceUp`](./Enums.md) | Integer | | 29 | 80 |
| [`DodgeChance`](./Enums.md) | Integer | | 17 | 50 |
| [`KineticSpikes`](./Enums.md) | Integer | | 10 | 2 |
| [`StatusOnStanceSwitch`](./Enums.md) | Object | | 14 |   |

</details>

---

### Object: `PassiveIfEmptyHead`


**Definition:** Applies the 'PassiveIfEmptyHead' effect.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |  |
| [`AddCritMultiplier`](./Enums.md) | Integer | | 23 | 200 |
| [`CritChanceUp`](./Enums.md) | Integer | | 29 | 80 |
| [`DodgeChance`](./Enums.md) | Integer | | 17 | 50 |
| [`KineticSpikes`](./Enums.md) | Integer | | 10 | 2 |
| [`StatusOnStanceSwitch`](./Enums.md) | Object | | 14 |   |

</details>

---

### Object: `PassiveIfEmptyNeck`


**Definition:** Applies the 'PassiveIfEmptyNeck' effect.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |  |
| [`AddCritMultiplier`](./Enums.md) | Integer | | 23 | 200 |
| [`CritChanceUp`](./Enums.md) | Integer | | 29 | 80 |
| [`DodgeChance`](./Enums.md) | Integer | | 17 | 50 |
| [`KineticSpikes`](./Enums.md) | Integer | | 10 | 2 |
| [`StatusOnStanceSwitch`](./Enums.md) | Object | | 14 |   |

</details>

---

### Object: `StatusAlliesOnDeath`


**Definition:** Event Trigger: Applies nested statuses to allies on death.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |  |
| `triggers_limit` | Number |  | 4 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`Freeze`](./Enums.md) | Array / Integer | | 12 | [.15] |
| [`FullHeal`](./Enums.md) | Integer | | 6 | 1 |
| [`HealAndOverhealToShield`](./Enums.md) | Integer | | 2 | 12 |
| [`Reanimate`](./Enums.md) | Integer | | 2 | 33 |
| [`TakeExtraTurn`](./Enums.md) | Integer | | 9 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnUseAbilityWithTag`


**Definition:** Event Trigger: Applies nested statuses when use ability with tag.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific entity tag required or applied. | 14 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |  |
| `exclude_basicattack` | Boolean |  | 4 |  |
| [`Conditional_FirstApplicationThisTurn`](./Enums.md) | Object | | 4 |   |
| [`DamageUp`](./Enums.md) | Integer | | 26 | 2 |
| [`HealthGain`](./Enums.md) | Integer / String | | 20 | 2*X |
| [`RandomStatUp`](./Enums.md) | Integer | | 11 | 2 |
| [`RefreshActPoints`](./Enums.md) | Integer | | 5 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AddStatusToElementAbilities`


**Definition:** Applies the 'AddStatusToElementAbilities' effect.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type required or applied. | 12 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |  |
| [`Bleed`](./Enums.md) | Array / Integer | | 23 | [.1] |
| [`ChangeTile`](./Enums.md) | Enum / Object | | 4 | FloatingGlassTile |
| [`Conditional_Ally`](./Enums.md) | Object | | 11 |   |
| [`Conditional_Enemy`](./Enums.md) | Object | | 7 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AddStatusToWeapons`


**Definition:** Applies the 'AddStatusToWeapons' effect.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |  |
| [`Bleed`](./Enums.md) | Array / Integer | | 23 | [.1] |
| [`Cleave`](./Enums.md) | Integer | | 3 | 1 |
| [`LeechPercent`](./Enums.md) | Integer | | 2 | 50 |
| [`PullSourceToKnockbackImmuneTarget`](./Enums.md) | Integer | | 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `CureDisease`


**Definition:** Applies the 'CureDisease' effect.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 12 |  |
| [`disease`](./Enums.md#enum-disease) | Enum |  | 12 |  |
| `can_apply_to_anything` | Boolean |  | 2 |  |

</details>

---

### Object: `Else`


**Definition:** Fallback object that executes if the preceding `Conditional_` block evaluated to false.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 76 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 72 |  |
| `CaptureFamiliar` | `Number` | Applies the 'CaptureFamiliar' effect. | 4 |  |
| `FactionConversion` | `Number` | Applies the 'FactionConversion' effect. | 4 |  |
| [`Fear`](./Enums.md) | Array / Integer | | 10 | [.15] |
| [`Marked`](./Enums.md) | Integer | | 7 | 1 |
| [`PermanentCharm`](./Enums.md) | Integer | | 2 | 1 |
| [`TempSpeedUp`](./Enums.md) | Integer | | 5 | 10 |

</details>

---

### Object: `keyword_tooltips`


**Definition:** Forces specific UI tooltips to appear when hovering over the ability.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 18 |  |
| [`Weakness`](./Enums.md) | Enum / Integer | | 18 | 2 |

</details>

---

### Object: `ManaCostReductionTagged`


**Definition:** Applies the 'ManaCostReductionTagged' effect.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer |  | 12 |  |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific entity tag required or applied. | 12 |  |

</details>

---

### Object: `SpawnEachTurn`


**Definition:** Applies or references the 'SpawnEachTurn' effect/state.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 40 |  |
| [`object`](./Arrays.md#array-object) | Array / Enum |  | 34 |  |
| `good` | Boolean |  | 4 |  |
| `number` | Array / Integer |  | 4 |  |

</details>

---

### Object: `SpawnThingOnDamage`


**Definition:** Applies or references the 'SpawnThingOnDamage' effect/state.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum |  | 76 |  |
| `good` | Boolean |  | 40 |  |
| `spawn_on_death_hit` | Boolean |  | 20 |  |
| `consider_all_layers` | Boolean |  | 4 |  |

</details>

---

### Object: `AddStatusToAllDamage`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToBasicMeleeAttack`


**Definition:** Examples: `{ ... }`  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |  |
| [`Bruise`](./Enums.md) | Integer | | 15 | 2 |
| [`Confusion`](./Enums.md) | Integer | | 11 | 2 |
| [`FaceAway`](./Enums.md) | Integer | | 2 | 1 |
| [`SpreadDisease`](./Enums.md) | Object | | 12 |   |
| [`Stun`](./Enums.md) | Array / Integer | | 19 | [.05*X] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnCastSpell`


**Definition:** Event Trigger: Applies nested statuses when cast spell.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |  |
| [`Charge`](./Enums.md) | Integer | | 5 | 2 |
| [`CurrentWeaponDamageUp`](./Enums.md) | Integer | | 3 | 1 |
| [`HealthGain`](./Enums.md) | Integer / String | | 20 | 2*X |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnOverHealed`


**Definition:** Event Trigger: Applies nested statuses when over healed.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| `SpawnScaledRotFly` | Number | Applies the 'SpawnScaledRotFly' effect. | 2 |  |
| [`CurrentWeaponDamageUp`](./Enums.md) | Integer | | 3 | 1 |
| [`ForceUseAbility_NonStack`](./Enums.md) | Enum | | 2 | Indigestion_Fart2 |
| [`StrengthUp`](./Enums.md) | Integer | | 13 | 2 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AddDamageToElementDamage`


**Definition:** Applies or references the 'AddDamageToElementDamage' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 18 |  |
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type required or applied. | 18 |  |

</details>

---

### Object: `AddPassivesToCharmed`


**Definition:** Applies the 'AddPassivesToCharmed' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |  |
| [`AddMaxHealth`](./Enums.md) | Integer | | 4 | 5 |
| [`AddSpeed`](./Enums.md) | Integer | | 4 | 4 |
| [`AddStatusToBasicAttack`](./Enums.md) | Object | | 92 |   |
| [`DamageUp`](./Enums.md) | Integer | | 26 | 2 |

</details>

---

### Object: `AddStatusToElementDamage`


**Definition:** Applies the 'AddStatusToElementDamage' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type required or applied. | 12 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |  |
| [`Burn`](./Enums.md) | Enum / Integer | | 28 | 2 |
| [`Conditional_Corpse`](./Enums.md) | Object | | 2 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AddStatusToExplosions`


**Definition:** Applies the 'AddStatusToExplosions' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddElement`](./Enums.md#enum-addelement) | Enum | Applies the 'AddElement' effect. | 16 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`Burn`](./Enums.md) | Enum / Integer | | 28 | 2 |

</details>

---

### Object: `AllyBonusAbilityAura`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 4 |  |
| `square` | Boolean |  | 4 |  |

</details>

---

### Object: `AllyManaRegenAura`


**Definition:** Applies the 'AllyManaRegenAura' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum / Integer | Distance or area of effect in tiles. | 8 |  |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 8 |  |

</details>

---

### Object: `AmplifyStatus`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `addstacks` | Number |  | 6 |  |
| [`status`](./Enums.md#enum-status) | Enum | The ID of the status effect to check or apply. | 6 |  |

</details>

---

### Object: `AutocastEachRound`


**Definition:** Forces the character to automatically cast a specific ability at the start of each combat round.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 18 |  |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 12 |  |
| `force_display_name` | Boolean |  | 4 |  |

</details>

---

### Object: `Conditional_FirstApplicationThisTurn`


**Definition:** Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill), [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#context-statusonuseabilitywithtag)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`FillMana`](./Enums.md) | Array / Integer | | 4 | [.25] |
| [`ManaGain`](./Enums.md) | Integer | | 6 | 2 |
| [`TakeExtraTurn`](./Enums.md) | Integer | | 9 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `DistanceBonusDamage`


**Definition:** Applies the 'DistanceBonusDamage' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `min_range` | Integer |  | 8 |  |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 8 |  |

</details>

---

### Object: `EMP`


**Definition:** Applies the 'EMP' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spell_graphics_override`](./Passives_and_Statuses.md#context-spell_graphics_override) | Object |  | 8 |  |
| [`status_explosion_override`](./Enums.md#enum-status_explosion_override) | Enum |  | 8 |  |

</details>

---

### Object: `empty_armor_scaled_stats`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cha` | Enum / Integer |  | 2 |  |
| `int` | Enum / Integer |  | 2 |  |
| `spd` | Enum / Integer |  | 2 |  |

</details>

---

### Object: `PassiveAtHealthThreshold`


**Definition:** Applies or references the 'PassiveAtHealthThreshold' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 18 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 |  |
| [`passives`](./Enums.md) | Object | | 884 |   |
| [`threshold`](./Enums.md) | Integer / Object | | 22 | 7 |

</details>

---

### Object: `PassiveWhenAffectedByElement`


**Definition:** Examples: `{ ... }`  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type required or applied. | 36 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 33 |  |
| [`passives`](./Enums.md) | Object | | 884 |   |

</details>

---

### Object: `PassiveWhenAtFullMana`


**Definition:** State Trigger: Grants nested passives when at full mana.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |  |
| [`AddMovement`](./Enums.md) | Integer | | 5 | 20 |
| [`AddStatusToBasicAttack`](./Enums.md) | Object | | 92 |   |
| [`Brace`](./Enums.md) | Integer | | 22 | 2 |
| [`Flying`](./Enums.md) | Integer | | 6 | 1 |
| [`ReplaceBasicMove`](./Enums.md) | Enum | | 6 | ToadJump_BasicMove |

</details>

---

### Object: `spell_graphics_override`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`EMP`](./Passives_and_Statuses.md#context-emp)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum |  | 8 |  |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum |  | 8 |  |
| `palette` | Enum / Integer |  | 8 |  |
| [`particle`](./Enums.md#enum-particle) | Enum |  | 8 |  |

</details>

---

### Object: `StatusAlliesOnKill`


**Definition:** Event Trigger: Applies nested statuses to allies on kill.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`DamageUp`](./Enums.md) | Integer | | 26 | 2 |
| [`HealthGain`](./Enums.md) | Integer / String | | 20 | 2*X |

</details>

---

### Object: `StatusIfUnusedMovePoints`


**Definition:** Event Trigger: Applies nested statuses to if unused move points.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |  |
| [`Brace`](./Enums.md) | Integer | | 22 | 2 |
| [`ConstitutionUp`](./Enums.md) | Integer | | 4 | 2 |
| [`HealthGain`](./Enums.md) | Integer / String | | 20 | 2*X |
| [`ManaGain`](./Enums.md) | Integer | | 6 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | | 11 | 2 |
| [`Shield`](./Enums.md) | Integer / String | | 21 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnTurnEndIfCastNSpells`


**Definition:** Event Trigger: Applies nested statuses when turn end if cast n spells.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spells` | Array |  | 10 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`DoubleCastSpell`](./Enums.md) | Integer | | 2 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | | 11 | 2 |
| [`Quivered`](./Enums.md) | Integer | | 15 | 2 |

</details>

---

### Object: `StatusOnTurnEndIfManaExact`


**Definition:** Event Trigger: Applies nested statuses when turn end if mana exact.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Enum / Integer |  | 8 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`FreeSpell`](./Enums.md) | Integer | | 2 | 1 |
| [`MoveQuivered`](./Enums.md) | Integer | | 11 | 2 |
| [`Quivered`](./Enums.md) | Integer | | 15 | 2 |
| [`SpellDamageUp`](./Enums.md) | Integer | | 7 | 1 |

</details>

---

### Object: `StatusOnTurnEndIfManaOrHealthExact`


**Definition:** Event Trigger: Applies nested statuses when turn end if mana or health exact.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Enum / Integer |  | 8 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |  |
| [`DivineShield`](./Enums.md) | Integer | | 10 | 1 |
| [`HealthGain`](./Enums.md) | Integer / String | | 20 | 2*X |
| [`IntelligenceUp`](./Enums.md) | Integer | | 11 | -1 |
| [`KineticSpikes`](./Enums.md) | Integer | | 10 | 2 |
| [`Shield`](./Enums.md) | Integer / String | | 21 | 2 |
| [`SpellDamageUp`](./Enums.md) | Integer | | 7 | 1 |
| [`Temporary`](./Enums.md) | Object | | 11 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AbilityReaction`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 20 |  |
| `ability_damage_only` | Boolean |  | 14 |  |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |  |

</details>

---

### Object: `AddSelfStatusToBasicAttack`


**Definition:** Applies or references the 'AddSelfStatusToBasicAttack' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |  |
| [`RandomMagicMissile`](./Enums.md) | Integer | | 17 | 2 |

</details>

---

### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** Applies the 'AddTemporaryEffectsToBasicAttack' effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fury` | Integer | Applies the 'Fury' effect. | 8 |  |
| `CastAgain` | Integer / String | Applies the 'CastAgain' effect. | 4 |  |

</details>

---

### Object: `Conditional_BadRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized bad outcome probability.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Number | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 16 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |  |
| [`Temporary`](./Enums.md) | Object | | 11 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `Conditional_HasStatus`


**Definition:** Conditional trigger: Executes nested logic if the target currently has the specified status effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 40 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 24 |  |

</details>

---

### Object: `DeathRattle`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 26 |  |
| `pop_corpse` | Boolean |  | 22 |  |

</details>

---

### Object: `ElementalManaCostReduction`


**Definition:** Applies the 'ElementalManaCostReduction' effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer |  | 10 |  |
| [`element`](./Arrays.md#array-element) | Array / Enum | The specific element type required or applied. | 4 |  |

</details>

---

### Object: `FindItemFromPool`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Number | Probability of finding the item. | 6 |  |
| [`pool`](./Enums.md#enum-pool) | Array / Enum | The item pool to draw from. | 4 |  |

</details>

---

### Object: `MoveTowardsDamageSource`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 10 |  |
| `move_far` | Boolean |  | 8 |  |

</details>

---

### Object: `ObjectOnHitCharacter`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend), [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#context-statuseachturnendperenemykill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | The entity ID of the character to spawn (e.g., CharmedFlea). | 14 |  |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 10 |  |

</details>

---

### Object: `SpawnCatCopyOnBattleStart`


**Definition:** Applies the 'SpawnCatCopyOnBattleStart' effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum |  | 8 |  |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum |  | 8 |  |

</details>

---

### Object: `SpawnOnBattleStartRandomEmptyTile`


**Definition:** Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum |  | 22 |  |
| [`number`](./Arrays.md#array-number) | Array / Integer |  | 6 |  |

</details>

---

### Object: `statuses`


**Definition:** Status effects possessed by the character.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChanceToRevive`](./Passives_and_Statuses.md#context-chancetorevive), [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#context-statusonbattleendifkillthresholdmet)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`FindItemFromPool`](./Enums.md) | Enum / Object | | 5 | consumables |
| [`HealthGain`](./Enums.md) | Integer / String | | 20 | 2*X |
| [`PermanentDexterity`](./Enums.md) | Integer | | 2 | 1 |

</details>

---

### Object: `StatusEveryXSpellCasts`


**Definition:** Applies or references the 'StatusEveryXSpellCasts' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 16 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`ReduceManaCost`](./Enums.md) | Integer | | 1 | 1 |
| [`RepairWeapon`](./Enums.md) | Integer | | 1 | 1 |
| [`RepairWeaponCondition`](./Enums.md) | Integer | | 1 | 1 |
| [`SpellDamageUp`](./Enums.md) | Integer | | 7 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusGroup`


**Definition:** Groups multiple status effects together for batch application.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |  |
| [`DexterityUp`](./Enums.md) | Integer | | 4 | 2 |
| [`LuckUp`](./Enums.md) | Integer | | 15 | 2 |
| [`SpawnCoinAnywhere`](./Enums.md) | Integer | | 3 | 1 |
| [`SpeedUp`](./Enums.md) | Integer | | 21 | 2 |

</details>

---

### Object: `StatusKilledCharacters`


**Definition:** Event Trigger: Applies nested statuses to killed characters.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnAllyCatDeath`


**Definition:** Event Trigger: Applies nested statuses when ally cat death.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`FillMana`](./Enums.md) | Array / Integer | | 4 | [.25] |
| [`HealthGain`](./Enums.md) | Integer / String | | 20 | 2*X |
| [`PercentHeal`](./Enums.md) | Integer | | 1 | 50 |
| [`TakeExtraTurn`](./Enums.md) | Integer | | 9 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnBattleStart`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |  |
| [`FullHeal`](./Enums.md) | Integer | | 6 | 1 |
| [`Sleep`](./Enums.md) | Integer | | 5 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnEatFood`


**Definition:** Event Trigger: Applies nested statuses when eat food.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |  |
| [`Cleanse`](./Enums.md) | Integer | | 4 | 0 |
| [`IntelligenceUp`](./Enums.md) | Integer | | 11 | -1 |
| [`RandomStatUp`](./Enums.md) | Integer | | 11 | 2 |
| [`StrengthUp`](./Enums.md) | Integer | | 13 | 2 |

</details>

---

### Object: `StatusOnGainCoins`


**Definition:** Event Trigger: Applies nested statuses when gain coins.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |  |
| [`DivineShield`](./Enums.md) | Integer | | 10 | 1 |
| [`RandomStatusFromPool`](./Enums.md) | Object | | 8 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnHealed`


**Definition:** Event Trigger: Applies nested statuses when healed.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`ObjectOnHitCharacter`](./Enums.md) | Enum / Object | | 11 | Coin |
| [`RandomStatusFromPool`](./Enums.md) | Object | | 8 |   |
| [`Thorns`](./Enums.md) | Integer | | 17 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnKillEnemy`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |  |
| [`DivineShield`](./Enums.md) | Integer | | 10 | 1 |
| [`HealthGain`](./Enums.md) | Integer / String | | 20 | 2*X |
| [`ManaGain`](./Enums.md) | Integer | | 6 | 2 |
| [`RefreshMovePoints`](./Enums.md) | Integer | | 7 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnTookDamageFromAbility`


**Definition:** Event Trigger: Applies statuses when taking damage from an ability.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |  |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | | 5 | 2 |
| [`Shield`](./Enums.md) | Integer / String | | 21 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AbilityWhenTaggedCharacterMovesNear`


**Definition:** AI Trigger: Executes an ability when a character with a specific tag moves adjacent.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 10 |  |
| [`range`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Mixed | Distance or area of effect in tiles. | 10 |  |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific entity tag required or applied. | 10 |  |

</details>

---

### Object: `AddPassivesToSummonAbilityMinions`


**Definition:** Applies the 'AddPassivesToSummonAbilityMinions' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`DamageUp`](./Enums.md) | Integer | | 26 | 2 |
| [`Doomed`](./Enums.md) | Integer | | 3 | 3 |
| [`MovementUp`](./Enums.md) | Integer | | 3 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AddPassiveToSpawnedRocks`


**Definition:** Applies the 'AddPassiveToSpawnedRocks' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddFilledMaxHealth` | Number | Applies the 'AddFilledMaxHealth' effect. | 4 |  |
| `JoinSpawnerFaction` | Number | Applies the 'JoinSpawnerFaction' effect. | 4 |  |

</details>

---

### Object: `AddSelfStatusToWeapons`


**Definition:** Applies the 'AddSelfStatusToWeapons' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToAllDamageAbilities`


**Definition:** Applies the 'AddStatusToAllDamageAbilities' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`Bleed`](./Enums.md) | Array / Integer | | 23 | [.1] |
| [`Piercing`](./Enums.md) | Integer | | 4 | 1 |
| [`Weakness`](./Enums.md) | Enum / Integer | | 18 | 2 |

</details>

---

### Object: `AddStatusToBasicAttackWithCooldown`


**Definition:** Applies the 'AddStatusToBasicAttackWithCooldown' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CharmedForceAttack` | `Number` | Applies the 'CharmedForceAttack' effect. | 4 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

---

### Object: `AddStatusToFirstBasicAttack`


**Definition:** Applies the 'AddStatusToFirstBasicAttack' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToMeleeDamage`


**Definition:** Applies the 'AddStatusToMeleeDamage' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DelayedWind`](./Passives_and_Statuses.md#context-delayedwind) | Object | Applies the 'DelayedWind' effect. | 2 |  |
| [`DelayedWindCone`](./Enums.md) | Object | | 1 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AddStatusToTrampleDamage`


**Definition:** Applies the 'AddStatusToTrampleDamage' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AllyHealthRegenAura`


**Definition:** Applies the 'AllyHealthRegenAura' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum / Integer | Distance or area of effect in tiles. | 4 |  |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 4 |  |

</details>

---

### Object: `AlternateCraftingPools`


**Definition:** Applies the 'AlternateCraftingPools' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tinkerer_0`](./Enums.md#enum-tinkerer_0) | Enum |  | 4 |  |
| [`tinkerer_1`](./Enums.md#enum-tinkerer_1) | Enum |  | 4 |  |

</details>

---

### Object: `ApplyStatusesToRandomEnemiesEachTurn`


**Definition:** Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | The numerical quantity. | 4 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`Bounty`](./Enums.md) | Integer | | 2 | 3 |

</details>

---

### Object: `ApplyStatusIfCrit`


**Definition:** Conditional trigger: Executes the nested logic only if the triggering action was a critical hit.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |  |
| [`Purge`](./Enums.md) | Integer | | 2 | 0 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `ApplyToSource`


**Definition:** Redirects the nested effects to apply to the caster/source of the ability instead of the target.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 46 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`Shield`](./Enums.md) | Integer / String | | 21 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AutocastEachTurnBegin`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |  |
| `advantage_polarity` | Number |  | 2 |  |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |  |

</details>

---

### Object: `BoobyTrapItems`


**Definition:** Applies the 'BoobyTrapItems' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`on_break`](./Passives_and_Statuses.md#context-on_break) | Object |  | 4 |  |
| [`on_throw`](./Passives_and_Statuses.md#context-on_throw) | Object |  | 4 |  |

</details>

---

### Object: `BoostWeaponDamage`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`crit_chance`](./Engine_DamagingKeys.md#valid-property-keys) | `String` |  | 8 |  |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 8 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |

</details>

---

### Object: `BouncyProjectiles`


**Definition:** Applies the 'BouncyProjectiles' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max_bounces` | Integer |  | 6 |  |
| `max_range` | Enum / Integer |  | 6 |  |

</details>

---

### Object: `CatAPultAnimation`


**Definition:** Applies the 'CatAPultAnimation' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 4 |  |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 4 |  |

</details>

---

### Object: `CatchProjectiles`


**Definition:** Applies or references the 'CatchProjectiles' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ally_chance` | Integer |  | 10 |  |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 10 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`Quivered`](./Enums.md) | Integer | | 15 | 2 |

</details>

---

### Object: `ChanceToBackflip`


**Definition:** Applies or references the 'ChanceToBackflip' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 12 |  |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 12 |  |

</details>

---

### Object: `ChangeTile`


**Definition:** Transforms the terrain tile under the target.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tile`](./Enums.md#enum-tile) | Array / Enum | The specific tile type to change into (e.g., GlassTile). | 22 |  |
| `aoe` | Integer | The area of effect or distance in tiles. | 4 |  |

</details>

---

### Object: `ClassManaCostReduction`


**Definition:** Applies or references the 'ClassManaCostReduction' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer |  | 14 |  |
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 12 |  |

</details>

---

### Object: `Conditional_Adjacent`


**Definition:** Conditional object: Executes nested logic only if the target is/has Adjacent.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`Bleed`](./Enums.md) | Array / Integer | | 23 | [.1] |
| [`BonusCritChance`](./Enums.md) | Integer | | 4 | 50 |
| [`BonusDamage`](./Enums.md) | Integer | | 2 | 2 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `Conditional_Boss`


**Definition:** Conditional trigger: Executes nested logic if the target is a Boss.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 27 |  |
| [`Charmed`](./Enums.md) | Array / Integer | | 14 | [.40] |
| [`Stun`](./Enums.md) | Array / Integer | | 19 | [.05*X] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `Conditional_Corpse`


**Definition:** Conditional trigger: Executes nested logic if the target is a dead body/corpse.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToElementDamage`](./Passives_and_Statuses.md#context-addstatustoelementdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Revive` | `Number` | Applies the 'Revive' effect. | 13 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |  |
| `OverrideDamage` | `Number` | Applies the 'OverrideDamage' effect. | 4 |  |
| `TakeExtraTurn` | `Number` | Applies the 'TakeExtraTurn' effect. | 4 |  |
| [`Charmed`](./Enums.md) | Array / Integer | | 14 | [.40] |
| [`DamageUp`](./Enums.md) | Integer | | 26 | 2 |
| [`SafeDoomed`](./Enums.md) | Integer | | 2 | 1 |
| [`SpeedUp`](./Enums.md) | Integer | | 21 | 2 |

</details>

---

### Object: `Conditional_HasTag`


**Definition:** Conditional trigger: Executes nested logic if the target possesses the specified entity tag.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Passives_and_Statuses.md#context-addstatustoalldamage), [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific string tag to check for. | 91 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 63 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 63 |  |
| `FlatLeechIfDamaged` | `Number` | Applies the 'FlatLeechIfDamaged' effect. | 2 |  |
| [`Charmed`](./Enums.md) | Array / Integer | | 14 | [.40] |

</details>

---

### Object: `Conditional_NotBoss`


**Definition:** Conditional trigger: Executes nested logic if the target is NOT a Boss.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `Conditional_PartyMember`


**Definition:** Conditional constraint. Nested properties only trigger if this is true.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `Conditional_Shielded`


**Definition:** Conditional trigger: Executes nested logic if the target currently has a Shield status.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusCritChance` | `Number` | Applies the 'BonusCritChance' effect. | 4 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `Craft`


**Definition:** Synthesizes or spawns a new item from a specific pool.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Array / Enum |  | 30 |  |
| [`slot`](./Enums.md#enum-slot) | Enum / Integer |  | 28 |  |

</details>

---

### Object: `DamageNeighborsAfterMove`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Equation | The base damage properties of an attack. | 8 |  |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 8 |  |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 8 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |  |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `DamageNeighborTilesWhenCastSpell`


**Definition:** Combat Trigger: Deals damage to neighbor tiles when cast spell.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`fire`](./Passives_and_Statuses.md#context-fire) | Object |  | 2 |  |
| [`ice`](./Passives_and_Statuses.md#context-ice) | Object |  | 2 |  |
| [`lightning`](./Passives_and_Statuses.md#context-lightning) | Object |  | 2 |  |
| [`triattack`](./Passives_and_Statuses.md#context-triattack) | Object |  | 2 |  |

</details>

---

### Object: `DamageReductionAura`


**Definition:** Combat Trigger: Deals damage to reduction aura.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 4 |  |
| [`range`](./Enums.md#enum-range) | Enum / Integer | Distance or area of effect in tiles. | 4 |  |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 4 |  |

</details>

---

### Object: `Earth`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Equation | The base damage properties of an attack. | 4 |  |

</details>

---

### Object: `Electric`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `ElementalAttunement`


**Definition:** Applies the 'ElementalAttunement' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Earth`](./Passives_and_Statuses.md#context-earth) | Object | Applies the 'Earth' effect. | 4 |  |
| [`Electric`](./Passives_and_Statuses.md#context-electric) | Object | Applies the 'Electric' effect. | 4 |  |
| [`Fire`](./Passives_and_Statuses.md#context-fire) | Integer / Object | Applies the 'Fire' effect. | 4 |  |
| [`Grass`](./Passives_and_Statuses.md#context-grass) | Object | Applies the 'Grass' effect. | 4 |  |
| [`Gravity`](./Passives_and_Statuses.md#context-gravity) | Object | Applies the 'Gravity' effect. | 4 |  |
| [`Holy`](./Passives_and_Statuses.md#context-holy) | Enum / Object | Applies the 'Holy' effect. | 4 |  |
| [`Ice`](./Passives_and_Statuses.md#context-ice) | Object | Applies the 'Ice' effect. | 4 |  |
| [`Shadow`](./Passives_and_Statuses.md#context-shadow) | Object | Applies the 'Shadow' effect. | 4 |  |
| [`Water`](./Passives_and_Statuses.md#context-water) | Object | Applies the 'Water' effect. | 4 |  |
| [`Wind`](./Passives_and_Statuses.md#context-wind) | Object | Applies the 'Wind' effect. | 4 |  |

</details>

---

### Object: `EscapeSequence`


**Definition:** Applies the 'EscapeSequence' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomDistanceDisplace` | `Number` | Displaces the target by a randomized distance. | 4 |  |
| `SafeExplosionIfHitSomething` | Number | Applies the 'SafeExplosionIfHitSomething' effect. | 4 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

---

### Object: `Eternal`


**Definition:** Applies the 'Eternal' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health_percent` | Integer |  | 6 |  |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 6 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`TakeExtraTurn`](./Enums.md) | Integer | | 9 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `ExtraStatusWhenDealingDamage`


**Definition:** Applies or references the 'ExtraStatusWhenDealingDamage' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `Fire`


**Definition:** Character Form: Behavior and stats for the 'Fire' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`Burn`](./Enums.md) | Enum / Integer | | 28 | 2 |

</details>

---

### Object: `Grass`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`Poison`](./Enums.md) | Array / Enum / Integer | | 22 | [.5] |

</details>

---

### Object: `Gravity`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `GravityWell`


**Definition:** Applies the 'GravityWell' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 4 |  |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 4 |  |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |  |
| [`cant_miss`](./Enums.md) | Boolean | | 8 | true |
| [`effects`](./Enums.md) | Object | | 30 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |
| [{Damaging Keys}](./Engine_DamagingKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `HealAlliesEachTurn`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean |  | 4 |  |
| `mana` | Enum / Integer |  | 4 |  |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 4 |  |

</details>

---

### Object: `Holy`


**Definition:** Character Form: Behavior and stats for the \'Holy\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`FlatLeech`](./Enums.md) | Enum | | 2 | X |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `HolyDamageBlessing`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilGetKill`](./Passives_and_Statuses.md#context-passiveuntilgetkill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage_multiplier` | Number |  | 4 |  |
| [`Burn`](./Enums.md) | Enum / Integer | | 28 | 2 |

</details>

---

### Object: `Ice`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `InfiniteRebirth`


**Definition:** Applies the 'InfiniteRebirth' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer |  | 6 |  |
| `playercat_health` | Integer |  | 6 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`TempSpeedUp`](./Enums.md) | Integer | | 5 | 10 |

</details>

---

### Object: `LateBloomer`


**Definition:** Applies the 'LateBloomer' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 4 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |

</details>

---

### Object: `LightningRod`


**Definition:** Applies the 'LightningRod' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`Tech`](./Enums.md) | Integer | | 6 | 1 |

</details>

---

### Object: `LowHealthAllyDodgeChanceAura`


**Definition:** Applies the 'LowHealthAllyDodgeChanceAura' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 4 |  |
| `theshold` | Number |  | 4 |  |

</details>

---

### Object: `MovementReaction`


**Definition:** Reaction: Triggers an effect or ability when forced to move.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 22 |  |
| `enemies_only` | Boolean |  | 14 |  |

</details>

---

### Object: `NextBattleStatus`


**Definition:** Applies the 'NextBattleStatus' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `on_break`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SafeExplosionIfHitSomething` | Number | Applies the 'SafeExplosionIfHitSomething' effect. | 4 |  |

</details>

---

### Object: `on_throw`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HitExplosion` | `Number` | Applies the 'HitExplosion' effect. | 4 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

---

### Object: `PassiveAfterXKills`


**Definition:** Applies or references the 'PassiveAfterXKills' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 8 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |  |
| [`passives`](./Enums.md) | Object | | 884 |   |

</details>

---

### Object: `PassiveAtFullHealth`


**Definition:** Applies the 'PassiveAtFullHealth' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TakeExtraDamage` | Number | Applies the 'TakeExtraDamage' effect. | 4 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`ManaCostReduction`](./Enums.md) | Integer | | 5 | 2 |

</details>

---

### Object: `PassiveAtInjuryThreshold`


**Definition:** Applies the 'PassiveAtInjuryThreshold' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `String` |  | 4 |  |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 4 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`passives`](./Enums.md) | Object | | 884 |   |
| [`threshold`](./Enums.md) | Integer / Object | | 22 | 7 |

</details>

---

### Object: `PassiveGroup`


**Definition:** Passive: A collection of passives grouped together for easier management.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Passives_and_Statuses.md#context-randompassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`CharismaUp`](./Enums.md) | Integer | | 1 | 5 |
| [`IntelligenceUp`](./Enums.md) | Integer | | 11 | -1 |
| [`SetDefaultFace`](./Enums.md) | Enum | | 2 | sad |
| [`SpeedUp`](./Enums.md) | Integer | | 21 | 2 |

</details>

---

### Object: `PassiveUntilCastSpell`


**Definition:** Applies the 'PassiveUntilCastSpell' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`HealAlliesEachTurn`](./Passives_and_Statuses.md#context-healallieseachturn) | Object | Applies the 'HealAlliesEachTurn' effect. | 4 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`StatusAlliesEachTurn`](./Enums.md) | Object | | 1 |   |

</details>

---

### Object: `PassiveUntilGetKill`


**Definition:** Applies the 'PassiveUntilGetKill' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`HolyDamageBlessing`](./Passives_and_Statuses.md#context-holydamageblessing) | Object | Applies the 'HolyDamageBlessing' effect. | 4 |  |

</details>

---

### Object: `PassiveWhenTheAlpha`


**Definition:** State Trigger: Grants nested passives when the alpha.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TogglableRoundEndExtraTurn` | Number | Applies the 'TogglableRoundEndExtraTurn' effect. | 4 |  |

</details>

---

### Object: `PassiveWhileInMonkMeleeStance`


**Definition:** Applies the 'PassiveWhileInMonkMeleeStance' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`Brace`](./Enums.md) | Integer | | 22 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer | | 14 | 2 |

</details>

---

### Object: `PassiveWhileInMonkRangedStance`


**Definition:** Applies the 'PassiveWhileInMonkRangedStance' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`AddBonusRange`](./Enums.md) | Integer | | 15 | 2 |
| [`AddSpellDamage`](./Enums.md) | Integer | | 6 | 2 |
| [`KineticSpikes`](./Enums.md) | Integer | | 10 | 2 |

</details>

---

### Object: `PassiveWhilePreviewingMonkRangedStance`


**Definition:** Applies the 'PassiveWhilePreviewingMonkRangedStance' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`AddBonusRange`](./Enums.md) | Integer | | 15 | 2 |

</details>

---

### Object: `PassiveWhileWearingMetal`


**Definition:** Applies the 'PassiveWhileWearingMetal' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddElementsToWeapon`](./Enums.md#enum-addelementstoweapon) | Enum | Applies the 'AddElementsToWeapon' effect. | 4 |  |

</details>

---

### Object: `RepressedMemoriesMetronome`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#context-scaledstatusonspendmana)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Array / Enum |  | 4 |  |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 4 |  |

</details>

---

### Object: `ScaledStatusOnOverMana`


**Definition:** Applies the 'ScaledStatusOnOverMana' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`Cleanse`](./Enums.md) | Integer | | 4 | 0 |
| [`RandomMagicMissile`](./Enums.md) | Integer | | 17 | 2 |

</details>

---

### Object: `ScaledStatusOnSpendMana`


**Definition:** Applies the 'ScaledStatusOnSpendMana' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RepressedMemoriesMetronome`](./Passives_and_Statuses.md#context-repressedmemoriesmetronome) | Object | Applies the 'RepressedMemoriesMetronome' effect. | 4 |  |

</details>

---

### Object: `schadenfreude_scaled_stats`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `con` | Enum / Integer |  | 2 |  |
| `str` | Enum / Integer |  | 2 |  |
| [`cha`](./Enums.md) | Integer | | 40 | 0 |
| [`dex`](./Enums.md) | Integer | | 24 | 4 |
| [`int`](./Enums.md) | Integer | | 46 | 0 |
| [`lck`](./Enums.md) | Integer | | 24 | 4 |
| [`spd`](./Enums.md) | Integer | | 50 | 0 |

</details>

---

### Object: `SecurityBotProtect`


**Definition:** AI Logic: Guarding behavior for Security Bot units.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 14 |  |
| [`move`](./Enums.md#enum-move) | Enum |  | 10 |  |

</details>

---

### Object: `Shadow`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`crit_chance`](./Engine_DamagingKeys.md#valid-property-keys) | `String` |  | 4 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

---

### Object: `SmiteEnemiesWhoKill`


**Definition:** Applies the 'SmiteEnemiesWhoKill' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 4 |  |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 4 |  |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 2 |  |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `SpecialFriends`


**Definition:** Applies the 'SpecialFriends' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`HealthGain`](./Enums.md) | Integer / String | | 20 | 2*X |

</details>

---

### Object: `StatsAtLowHealth`


**Definition:** Applies the 'StatsAtLowHealth' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `speed` | Array / Number |  | 2 |  |
| `strength` | Integer |  | 2 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`threshold`](./Enums.md) | Integer / Object | | 22 | 7 |

</details>

---

### Object: `StatusAfterCastSpell`


**Definition:** Applies or references the 'StatusAfterCastSpell' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`TempDamageUp`](./Enums.md) | Integer | | 4 | 2 |
| [`TempSpellDamageUp`](./Enums.md) | Integer | | 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusAlliesOnBattleStart`


**Definition:** Applies or references the 'StatusAlliesOnBattleStart' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |  |
| [`EquipTemporaryItem`](./Enums.md) | Enum | | 10 | FoodMedium |

</details>

---

### Object: `StatusAlliesOnGainCoins`


**Definition:** Event Trigger: Applies nested statuses to allies on gain coins.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `scaled` | Boolean |  | 2 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`HealthGain`](./Enums.md) | Integer / String | | 20 | 2*X |
| [`LuckUp`](./Enums.md) | Integer | | 15 | 2 |

</details>

---

### Object: `StatusAllyWhenAllySpendsMana`


**Definition:** Event Trigger: Applies nested statuses to ally when ally spends mana.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`threshold`](./Enums.md) | Integer / Object | | 22 | 7 |

</details>

---

### Object: `StatusAnyCatAllyWhoKills`


**Definition:** Event Trigger: Applies nested statuses to any cat ally who kills.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusDamagers`


**Definition:** Event Trigger: Applies nested statuses to damagers.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`Fear`](./Enums.md) | Array / Integer | | 10 | [.15] |
| [`LuckUp`](./Enums.md) | Integer | | 15 | 2 |

</details>

---

### Object: `StatusEachTurnEndForEachTurn`


**Definition:** Event Trigger: Applies nested statuses to each turn end for each turn.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`RandomMagicMissile`](./Enums.md) | Integer | | 17 | 2 |

</details>

---

### Object: `StatusEachTurnEndPerEnemyKill`


**Definition:** Event Trigger: Applies nested statuses to each turn end per enemy kill.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`ObjectOnHitCharacter`](./Enums.md) | Enum / Object | | 11 | Coin |

</details>

---

### Object: `StatusEnemiesOnDeath`


**Definition:** Event Trigger: Applies nested statuses to enemies on death.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusEveryXTurnBegins`


**Definition:** Event Trigger: Applies nested statuses to every x turn begins.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `turns` | Array / Integer / Object | The duration of the effect in turns. | 4 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`DivineShield`](./Enums.md) | Integer | | 10 | 1 |

</details>

---

### Object: `StatusKillers`


**Definition:** Instantly kills the target if they possess the specified status effects.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnAnyDeath`


**Definition:** Event Trigger: Applies nested statuses when any death.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`LuckUp`](./Enums.md) | Integer | | 15 | 2 |

</details>

---

### Object: `StatusOnBattleEndIfKillThresholdMet`


**Definition:** Event Trigger: Applies nested statuses when battle end if kill threshold met.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `kills` | Number |  | 4 |  |
| [`statuses`](./Passives_and_Statuses.md#context-statuses) | Object |  | 4 |  |

</details>

---

### Object: `StatusOnBreakItem`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`Shield`](./Enums.md) | Integer / String | | 21 | 2 |
| [`Thorns`](./Enums.md) | Integer | | 17 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnCollectPickup`


**Definition:** Event Trigger: Applies nested statuses when collect pickup.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`Tech`](./Enums.md) | Integer | | 6 | 1 |

</details>

---

### Object: `StatusOnDealtDamage`


**Definition:** Event Trigger: Applies nested statuses when dealt damage.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`TempDexterityUp`](./Enums.md) | Integer | | 2 | 2 |
| [`TempLuckUp`](./Enums.md) | Integer | | 1 | 2 |
| [`TempStrengthUp`](./Enums.md) | Integer | | 2 | 2 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnDealtDamageThreshold`


**Definition:** Event Trigger: Applies nested statuses when dealt damage threshold.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count_overkill` | Boolean |  | 4 |  |
| `ignore_during_movement` | Boolean |  | 4 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`RefreshMovePoints`](./Enums.md) | Integer | | 7 | 1 |
| [`Shield`](./Enums.md) | Integer / String | | 21 | 2 |
| [`threshold`](./Enums.md) | Integer / Object | | 22 | 7 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnEndMove`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnGainShield`


**Definition:** Event Trigger: Applies nested statuses when gain shield.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`Temporary`](./Enums.md) | Object | | 11 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnHeal`


**Definition:** Event Trigger: Applies nested statuses when heal.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`RandomStatUp`](./Enums.md) | Integer | | 11 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | | 21 | 2 |

</details>

---

### Object: `StatusOnOverMana`


**Definition:** Event Trigger: Applies nested statuses when over mana.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`DivineShield`](./Enums.md) | Integer | | 10 | 1 |
| [`IntelligenceUp`](./Enums.md) | Integer | | 11 | -1 |
| [`SpellDamageUp`](./Enums.md) | Integer | | 7 | 1 |

</details>

---

### Object: `StatusOnPickupCoins`


**Definition:** Event Trigger: Applies nested statuses when pickup coins.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`DexterityUp`](./Enums.md) | Integer | | 4 | 2 |
| [`RefreshMovePoints`](./Enums.md) | Integer | | 7 | 1 |
| [`SpeedUp`](./Enums.md) | Integer | | 21 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnPopCorpse`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |  |
| [`HealthGain`](./Enums.md) | Integer / String | | 20 | 2*X |

</details>

---

### Object: `StatusOnTookDamageFromEnemyAbility`


**Definition:** Event Trigger: Applies nested statuses when took damage from enemy ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`MoveQuivered`](./Enums.md) | Integer | | 11 | 2 |
| [`Quivered`](./Enums.md) | Integer | | 15 | 2 |

</details>

---

### Object: `StatusOnTriggerTrap`


**Definition:** Event Trigger: Applies nested statuses when trigger trap.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`DexterityUp`](./Enums.md) | Integer | | 4 | 2 |
| [`Quivered`](./Enums.md) | Integer | | 15 | 2 |

</details>

---

### Object: `StatusOnUseBasicAttack`


**Definition:** Event Trigger: Applies nested statuses when use basic attack.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`FlippedFacingForceAttack`](./Enums.md) | Integer | | 2 | 1 |

</details>

---

### Object: `StatusOnUseElementAbility`


**Definition:** Event Trigger: Applies nested statuses when use element ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type required or applied. | 4 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`SpeedUp`](./Enums.md) | Integer | | 21 | 2 |

</details>

---

### Object: `StatusPerInjury`


**Definition:** Event Trigger: Applies nested statuses to per injury.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cap` | Number |  | 4 |  |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `String` |  | 4 |  |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`Shield`](./Enums.md) | Integer / String | | 21 | 2 |
| [`StrengthUp`](./Enums.md) | Integer | | 13 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusThingsKnockedBack`


**Definition:** Event Trigger: Applies nested statuses to things knocked back.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Drag` | Number | Applies the 'Drag' effect. | 4 |  |

</details>

---

### Object: `StatusWhenAllySpendsMana`


**Definition:** Event Trigger: Applies nested statuses to when ally spends mana.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`ManaGain`](./Enums.md) | Integer | | 6 | 2 |
| [`OneUseSpellDamageUp`](./Enums.md) | Integer | | 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `TaggedPickupEffectReplacement`


**Definition:** Applies the 'TaggedPickupEffectReplacement' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific entity tag required or applied. | 4 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`HealthGain`](./Enums.md) | Integer / String | | 20 | 2*X |

</details>

---

### Object: `TowerDefense`


**Definition:** Applies the 'TowerDefense' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 4 |  |
| `range` | Enum / Integer | Distance or area of effect in tiles. | 4 |  |

</details>

---

### Object: `Water`


**Definition:** Character Form: Behavior and stats for the \'Water\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AOEPuddle`](./Math_Equations.md) | Equation | Applies the 'AOEPuddle' effect. | 4 |  |

</details>

---

### Object: `Wind`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`knockback`](./Math_Equations.md) | Equation |  | 4 |  |

</details>

---

### Object: `AbilityChargeRefundChance`


**Definition:** Applies the 'AbilityChargeRefundChance' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `advantage_softcap` | Number |  | 2 |  |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |  |

</details>

---

### Object: `AddStatusesIfPersistentWeatherElement`


**Definition:** Applies the 'AddStatusesIfPersistentWeatherElement' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`Burn`](./Enums.md) | Enum / Integer | | 28 | 2 |

</details>

---

### Object: `AddStatusesToReceivedElementalDamage`


**Definition:** Applies the 'AddStatusesToReceivedElementalDamage' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`Burn`](./Enums.md) | Enum / Integer | | 28 | 2 |

</details>

---

### Object: `AddStatusToKnockbackDamage`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToReceivedDamage_ExcludeStatuses`


**Definition:** Applies the 'AddStatusToReceivedDamage_ExcludeStatuses' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToSpells`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddTemporaryEffectsToEquipment`


**Definition:** Applies the 'AddTemporaryEffectsToEquipment' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CastAgain` | Integer / String | Applies the 'CastAgain' effect. | 2 |  |

</details>

---

### Object: `Autism`


**Definition:** Applies the 'Autism' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `innate` | Number |  | 2 |  |
| `learned` | Number |  | 2 |  |

</details>

---

### Object: `ChanceToRevive`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 10 |  |
| [`statuses`](./Passives_and_Statuses.md#context-statuses) | Object |  | 6 |  |

</details>

---

### Object: `CollectPickupsOnBattleEnd`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pop_corpses` | Boolean |  | 2 |  |

</details>

---

### Object: `Conditional_DoesDamage`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage_ExcludeStatuses`](./Passives_and_Statuses.md#context-addstatustoreceiveddamage_excludestatuses)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 72 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 40 |  |
| `UseRandomSpell_Madness` | `Number` | Applies the 'UseRandomSpell_Madness' effect. | 2 |  |

</details>

---

### Object: `Conditional_SourceHasTag`


**Definition:** Conditional object: Executes nested logic only if the target is/has SourceHasTag.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific entity tag required or applied. | 2 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`Conditional_Ally`](./Enums.md) | Object | | 11 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `DamageIfDidntUseSpecificAbility`


**Definition:** Combat Trigger: Deals damage to if didnt use specific ability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |  |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 2 |  |

</details>

---

### Object: `DelayedWind`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The area of effect or distance in tiles. | 2 |  |

</details>

---

### Object: `DelayedWindCone`


**Definition:** Creates a delayed Area of Effect cone.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The area of effect or distance in tiles. | 4 |  |

</details>

---

### Object: `Diabetes`


**Definition:** Applies the 'Diabetes' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`AllStatsUp`](./Enums.md) | Array / Integer | | 38 | [.5] |
| [`Confusion`](./Enums.md) | Integer | | 11 | 2 |

</details>

---

### Object: `EnergyStorm`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cycle_start` | Number |  | 2 |  |
| `period` | Number |  | 2 |  |

</details>

---

### Object: `fire`


**Definition:** Character Form: Behavior and stats for the 'Fire' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 2 |  |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 2 |  |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |  |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `ForceMoveAway`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusAdjacentOnTheirTurnBegin`](./Passives_and_Statuses.md#context-statusadjacentontheirturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `free` | Boolean |  | 2 |  |

</details>

---

### Object: `FurnitureStats`


**Definition:** Applies the 'FurnitureStats' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Appeal` | Number | Applies the 'Appeal' effect. | 2 |  |
| `Comfort` | Number | Applies the 'Comfort' effect. | 2 |  |
| `Stimulation` | Number | Applies the 'Stimulation' effect. | 2 |  |

</details>

---

### Object: `ice`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 2 |  |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 2 |  |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |  |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `lightning`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 2 |  |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 2 |  |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |  |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `MegaMinions`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cycle_start` | Number |  | 2 |  |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 2 |  |

</details>

---

### Object: `MoveWhenDamaged`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Array / Enum |  | 18 |  |

</details>

---

### Object: `PassiveLevelScaledStatus`


**Definition:** Applies the 'PassiveLevelScaledStatus' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SizeScalePercent`](./Math_Equations.md) | Equation | Applies the 'SizeScalePercent' effect. | 2 |  |
| [`Shield`](./Enums.md) | Integer / String | | 21 | 2 |
| [`Trample`](./Enums.md) | Array / Integer | | 10 | [3] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `RandomPassivePool`


**Definition:** Logic: Grants a random passive from the specified pool upon spawning.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 26 |  |
| [`PassiveGroup`](./Enums.md) | Object | | 2 |   |

</details>

---

### Object: `ReplaceBrain`


**Definition:** Applies the 'ReplaceBrain' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 8 |  |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 8 |  |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 8 |  |

</details>

---

### Object: `Robot`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean |  | 4 |  |

</details>

---

### Object: `ScaledStatusOnBleedDamage`


**Definition:** Applies the 'ScaledStatusOnBleedDamage' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`Charge`](./Enums.md) | Integer | | 5 | 2 |

</details>

---

### Object: `ScaledStatusOnLoseShield`


**Definition:** Applies the 'ScaledStatusOnLoseShield' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`Thorns`](./Enums.md) | Integer | | 17 | 2 |

</details>

---

### Object: `ScaledStatusOnOverHealed`


**Definition:** Applies the 'ScaledStatusOnOverHealed' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpawnScaledRotFly` | Number | Applies the 'SpawnScaledRotFly' effect. | 2 |  |

</details>

---

### Object: `SelfDamageWhenDealDamage`


**Definition:** Applies the 'SelfDamageWhenDealDamage' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 2 |  |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |  |

</details>

---

### Object: `StackingDodgeChanceOnTookDamage`


**Definition:** Applies the 'StackingDodgeChanceOnTookDamage' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `amount` | Array | The numerical quantity. | 2 |  |
| `cap` | Number |  | 2 |  |

</details>

---

### Object: `StatusAdjacentOnTheirTurnBegin`


**Definition:** Event Trigger: Applies nested statuses to adjacent on their turn begin.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusAlliesEachTurn`


**Definition:** Applies or references the 'StatusAlliesEachTurn' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean |  | 2 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`RandomStatUp`](./Enums.md) | Integer | | 11 | 2 |

</details>

---

### Object: `StatusAlliesOnSpendMana`


**Definition:** Event Trigger: Applies nested statuses to allies on spend mana.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusAlliesScaledByCursedOnDeath`


**Definition:** Event Trigger: Applies nested statuses to allies scaled by cursed on death.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`LuckUp`](./Enums.md) | Integer | | 15 | 2 |

</details>

---

### Object: `StatusIfBattleAlreadyBegan`


**Definition:** Event Trigger: Applies nested statuses to if battle already began.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`PermanentMadness`](./Enums.md) | Integer | | 4 | 1 |

</details>

---

### Object: `StatusOnEatPill`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnLoseShield`


**Definition:** Event Trigger: Applies nested statuses when lose shield.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`Thorns`](./Enums.md) | Integer | | 17 | 2 |

</details>

---

### Object: `StatusOnTakeHealthDamage`


**Definition:** Event Trigger: Applies nested statuses when take health damage.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`PermanentConstitution`](./Enums.md) | Integer | | 2 | -1 |

</details>

---

### Object: `StatusOnTurnEndIfDidntCastAbilityTypes`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 8 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |  |
| [`ManaGain`](./Enums.md) | Integer | | 6 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StrengthInNumbersAura`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count_self` | Boolean |  | 2 |  |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 2 |  |

</details>

---

### Object: `Study`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `marked` | Number |  | 2 |  |
| `stacks` | Enum / Integer | The number of stacks, duration, or intensity to apply. | 2 |  |

</details>

---

### Object: `TakeBonusTurnWithStatus`


**Definition:** Grants the character an immediate extra turn while afflicted with specific statuses.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |  |
| [`Madness`](./Enums.md) | Integer | | 9 | 1 |

</details>

---

### Object: `TheHunger`


**Definition:** Applies the 'TheHunger' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`Madness`](./Enums.md) | Integer | | 9 | 1 |

</details>

---

### Object: `TileDamageMultiplier`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ally_multiplier` | Number |  | 2 |  |
| `multiplier` | Number | Multiplicative modifier to a base value. | 2 |  |

</details>

---

### Object: `TourettesMeows`


**Definition:** Applies the 'TourettesMeows' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cooldown`](./Arrays.md#array-cooldown) | Array |  | 1 |  |
| [`pool`](./Arrays.md#array-pool) | Array / Enum |  | 1 |  |

</details>

---

### Object: `triattack`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 2 |  |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 2 |  |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |  |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |

</details>

---


<details>
<summary><b>AddSelfStatusToWeapons</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

<details>
<summary><b>AddStatusToAllDamage</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 |  |

</details>

<details>
<summary><b>AddStatusToBasicAttackWithCooldown</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |  |

</details>

<details>
<summary><b>AddStatusToFirstBasicAttack</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

<details>
<summary><b>AddStatusToKnockbackDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

<details>
<summary><b>AddStatusToMeleeDamage</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |  |

</details>

<details>
<summary><b>AddStatusToReceivedDamage_ExcludeStatuses</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |  |

</details>

<details>
<summary><b>AddStatusToSpells</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |

</details>

<details>
<summary><b>AddStatusToTrampleDamage</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |

</details>

<details>
<summary><b>Conditional_Adjacent</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |

</details>

<details>
<summary><b>Conditional_DoesDamage</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |  |

</details>

<details>
<summary><b>Conditional_GoodRoll</b></summary>

> **Total Count:** 30

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 30 |  |

</details>

<details>
<summary><b>Conditional_NotBoss</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 13 |  |

</details>

<details>
<summary><b>Conditional_PartyMember</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

<details>
<summary><b>Conditional_Shielded</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |

</details>

<details>
<summary><b>ExtraStatusWhenDealingDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

<details>
<summary><b>NextBattleStatus</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

<details>
<summary><b>PassiveLevelScaledStatus</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |

</details>

<details>
<summary><b>StatusAdjacentOnTheirTurnBegin</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |  |

</details>

<details>
<summary><b>StatusAlliesOnSpendMana</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |

</details>

<details>
<summary><b>StatusAnyCatAllyWhoKills</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

<details>
<summary><b>StatusEnemiesOnDeath</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

<details>
<summary><b>StatusKilledCharacters</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |  |

</details>

<details>
<summary><b>StatusKillers</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |

</details>

<details>
<summary><b>StatusOnDealtDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

<details>
<summary><b>StatusOnEatPill</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |

</details>

<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |  |

</details>

<details>
<summary><b>StatusOnOverHealed</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |

</details>


## Discovered Objects

> These tables were auto-generated by the schema audit tool. They document objects found in the `.gon` files that were not previously documented.

### Object: `AIControlNextTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_spells` | Boolean |  | 2 | `true` (Boolean) |
| `stacks` | Enum / Integer |  | 2 | `1` (Number) |


### Object: `AbilityHealthThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 26 | `FormShrinkFour` (Enum), `DybbukPossess` (Enum) |
| `also_use_if_buddy_is_dead` | Boolean |  | 2 | `true` (Boolean) |
| `aux` | Integer |  | 2 | `25` (Number) |
| `even_if_stunned` | Boolean |  | 14 | `true` (Boolean) |
| `immediate` | Boolean |  | 12 | `true` (Boolean) |
| `threshold` | Enum / Integer / Object |  | 24 | `1*champion_multiplier` (Enum), `3*champion_multiplier` (Enum), `200` (Number), `1` (Number), `"max(X*.33, 5)"` (String), `"max(X*.5, 1)"` (String) |
| `threshold_min` | Enum |  | 2 | `X` (Enum) |
| `use_ai` | Boolean |  | 4 | `true` (Boolean) |


### Object: `AbilityOnRoundEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `DestroyerRaise` (Enum) |
| `force_display_name` | Boolean |  | 4 | `true` (Boolean) |


### Object: `AbilityOnRoundEndOnce`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `wp_SignalAmplifierSpawnTerminator` (Enum) |
| `even_of_stunned` | Boolean |  | 2 | `true` (Boolean) |


### Object: `AddAdvantageToEvent`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `add` | Array / Integer |  | 2 | `5` (Number) |
| `options` | Array |  |  | `[smash bash open]` (Array) |
| `type` | Enum |  | 2 | `treasure_box` (Enum) |


### Object: `AddStatusToBackstabs`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer |  | 2 | `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |


### Object: `AddStatusToFirstSpellEachTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Conditional_IsSelf` | Object |  | 2 | `{ ... }` (Object) |
| `Else` | Object |  | 2 | `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `AddStatusToReceivedDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Conditional_IsPhysicalAttack` | Object |  | 2 | `{ ... }` (Object) |
| `Else` | Object |  | 2 | `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `AfterImage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Thief` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_AFTERIMAGE_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_AFTERIMAGE_NAME"` (String) |
| `object` | Array / Enum |  | 4 | `PlayerCat_ThiefShade` (Enum) |
| `skilltemp` | Boolean |  | 4 | `true` (Boolean) |


### Object: `AggroTargetIsGovernedByHitEffect`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean |  | 2 | `false` (Boolean) |


### Object: `AllStatsAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `aura_requires_tag` | Enum |  | 2 | `humanoid` (Enum) |
| `range` | Enum / Integer |  | 2 | `global` (Enum) |
| `stacks` | Enum / Integer |  | 2 | `1` (Number) |


### Object: `AllStatsUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_ALLSTATSUP_NAME"` (String) |
| `name_stacks_neg` | String |  |  | `"KEYWORD_ALLSTATSDOWN_NAME"` (String) |
| `tooltip_stackless` | Enum |  |  | `none` (Enum) |
| `tooltip_stacks_neg` | String |  |  | `"KEYWORD_ALLSTATSDOWN_DESC"` (String) |
| `tooltip_stacks_pos` | String |  |  | `"KEYWORD_ALLSTATSUP_DESC"` (String) |


### Object: `AlluringDoodieEater`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number |  | 2 | `10` (Number) |
| `damage_instance` | Object |  | 2 | `{ ... }` (Object) |


### Object: `AllyDodgeChanceAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `DodgeChance_Status` (Enum) |
| `chance` | Number |  | 2 | `25` (Number) |
| `range` | Enum / Integer |  | 2 | `1` (Number) |


### Object: `AlphaAllStatsUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `AllStatsUp` (Enum) |


### Object: `AlphaCat`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_ALPHA_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_ALPHA_DESC"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_ALPHA_DESC_STACKLESS"` (String) |


### Object: `Ammo`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_AMMO_NAME"` (String) |
| `tooltip_stackless` | Enum |  |  | `none` (Enum) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_AMMO_DESC"` (String) |


### Object: `ArmorBreakOnHit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance_to_break` | Integer |  | 4 | `10` (Number), `5` (Number) |
| `durability_loss` | Integer |  | 4 | `0` (Number) |


### Object: `ArmorPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `frame_range` | Array |  |  | `[6 6]` (Array), `[1 2]` (Array) |
| `stacks` | Enum / Integer |  | 6 | `4` (Number), `6` (Number) |


### Object: `BackflipWhenTargeted`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 14 | `Teleport` (Enum), `SZBBackflipDodge` (Enum) |
| `name` | Enum |  |  | `"KEYWORD_BACKFLIP_NAME"` (String) |
| `stacks` | Enum / Integer |  | 14 | `4` (Number), `1` (Number) |
| `tooltip` | Enum |  |  | `"KEYWORD_BACKFLIP_DESC"` (String) |


### Object: `BaitAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `range` | Enum / Integer |  | 8 | `3` (Number) |


### Object: `BattlefieldUniqueRandomPassive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DemonicGlyph_Bounce` | Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DemonicGlyph_Fire` | Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DemonicGlyph_Movement` | Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DemonicGlyph_Summon` | Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |


### Object: `Bird`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_spawn_pool` | Object |  |  | `{ ... }` (Object) |
| `properties` | Object |  |  | `{ ... }` (Object) |


### Object: `BirdRewards`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ally_rewards` | Object |  | 36 | `{ ... }` (Object) |
| `statuses` | Object |  | 10 | `{ ... }` (Object) |


### Object: `BlastResistance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_BLASTRESISTANCE_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_BLASTRESISTANCE_DESC"` (String) |


### Object: `Bleed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_BLEED_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_BLEED_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_BLEED_DESC"` (String) |


### Object: `BleedThorns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_BLEEDTHORNS_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_BLEEDTHORNS_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_BLEEDTHORNS_DESC"` (String) |


### Object: `Blind`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_BLIND_NAME"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_BLIND_DESC"` (String) |
| `tooltip_stacks_neg` | String |  |  | `"KEYWORD_PERMABLIND_DESC"` (String) |
| `tooltip_stacks_singular` | String |  |  | `"KEYWORD_BLIND_DESC_STACKLESS"` (String) |


### Object: `BoostDamageAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `DamageUp` (Enum) |


### Object: `BoostDamageGlobalAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `DamageUp` (Enum) |


### Object: `BossRewards`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `common` | Enum |  | 40 | `RatBomb` (Enum), `ChubsCollar` (Enum) |
| `rare` | Enum |  | 32 | `BorisBrain` (Enum), `JohnnysStool` (Enum) |


### Object: `Brace`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"KEYWORD_BRACE_NAME"` (String) |
| `template` | Enum |  |  | `self_buff` (Enum) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_BRACE_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_BRACE_DESC"` (String) |


### Object: `BraceForEachNeighboringEnemy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `Brace` (Enum) |


### Object: `Brittle`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `150` (Number) |
| `name` | Enum |  |  | `"KEYWORD_BRITTLE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_BRITTLE_DESC"` (String) |


### Object: `BrittleDuringElement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `Brittle` (Enum) |


### Object: `Bruise`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"KEYWORD_BRUISE_NAME"` (String) |
| `template` | Enum |  |  | `self_buff` (Enum) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_BRUISE_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_BRUISE_DESC"` (String) |


### Object: `Buddy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 6 | `false` (Boolean) |
| `obj` | Array / Enum |  | 6 | `ZaratanaVS` (Enum), `PyrophinaVS` (Enum) |
| `reclaim_if_lost` | Boolean |  | 2 | `true` (Boolean) |


### Object: `BuffImmunity`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exclude` | Enum |  | 2 | `SpellDamageUp` (Enum) |


### Object: `BungaCheers`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ally_damage` | Enum |  | 2 | `littleboo` (Enum) |
| `ally_dead` | Enum |  | 2 | `bigboo` (Enum) |
| `enemy_damage` | Enum |  | 2 | `littlecheer` (Enum) |
| `enemy_dead` | Enum |  | 2 | `bigcheer` (Enum) |
| `warrior_tag` | Enum |  | 2 | `bungawarrior` (Enum) |


### Object: `BungaEntrance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `BungaEntrance` (Enum), `BecomeTheDestroyer` (Enum) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `even_if_stunned` | Boolean |  | 4 | `true` (Boolean) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `health_threshold` | Integer |  | 4 | `150` (Number), `-1` (Number) |
| `self_damage` | Boolean / Integer / Object |  |  | `{ ... }` (Object) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `jump_attack` (Enum) |
| `temporary_effects` | Object |  |  | `{ ... }` (Object) |
| `warrior_tag` | Enum |  | 4 | `bungawarrior` (Enum), `finalboss_clonecat` (Enum) |


### Object: `Burn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_BURN_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_BURN_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_BURN_DESC"` (String) |


### Object: `CatPartsSizeScale`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `head` | Enum / Number |  | 2 | `1.3` (Number) |


### Object: `CatPartsTransform`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `arm1` | Number |  | 20 | `1043` (Number), `1013` (Number) |
| `arm2` | Number |  | 22 | `1013` (Number), `1501` (Number) |
| `body` | Number |  | 10 | `31` (Number), `1029` (Number) |
| `ear1` | Integer |  | 26 | `1501` (Number), `343` (Number) |
| `ear2` | Integer |  | 20 | `1005` (Number), `1501` (Number) |
| `eye1` | Integer |  | 6 | `1013` (Number), `1069` (Number) |
| `eye2` | Integer |  | 6 | `1013` (Number), `1069` (Number) |
| `eyebrow1` | Integer |  | 2 | `1069` (Number) |
| `eyebrow2` | Integer |  | 2 | `1070` (Number) |
| `head` | Enum / Number |  | 12 | `1027` (Number), `1504` (Number) |
| `leg1` | Integer |  | 16 | `41` (Number), `1043` (Number) |
| `leg2` | Integer |  | 16 | `41` (Number), `1043` (Number) |
| `mouth` | Number |  | 16 | `1005` (Number), `1069` (Number) |
| `palette` | Enum / Integer |  | 34 | `Fighter` (Enum), `Medic` (Enum), `76` (Number), `78` (Number) |
| `tail` | Integer |  | 26 | `1504` (Number), `1503` (Number) |
| `texture` | Integer |  | 12 | `322` (Number), `19` (Number) |


### Object: `CaveFamilyEnrage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 12 | `CaveCatEnrageTwo` (Enum), `CaveCatEnrageOne` (Enum) |
| `count` | Array / Integer |  | 12 | `1` (Number), `0` (Number) |
| `tag` | Array / Enum |  | 12 | `cavefamily` (Enum) |


### Object: `CerberubsAggroTargetBehavior`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alert_form` | Enum |  | 2 | `Alert` (Enum) |
| `default_form` | Enum |  | 2 | `Normal` (Enum) |


### Object: `ChainKnockback`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Tank` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_CHAINKNOCKBACK_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_CHAINKNOCKBACK_NAME"` (String) |


### Object: `ChanceToBlockAndCounter`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean |  | 2 | `true` (Boolean) |
| `chance` | Number |  | 2 | `100` (Number) |


### Object: `ChanceToForceEvent`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number |  | 2 | `25` (Number) |
| `event` | Enum |  | 2 | `Blessing` (Enum) |


### Object: `ChanceToFormChangeOnAbilityDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number |  | 2 | `15` (Number) |
| `form` | Enum / Integer |  | 2 | `Flop2` (Enum) |


### Object: `ChanceToSpitOnDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 14 | `MoonHandDrop` (Enum), `SpewerSpit` (Enum) |
| `backstabs_only` | Boolean |  | 2 | `true` (Boolean) |
| `chance_per_damage` | Integer |  | 6 | `0` (Number), `2` (Number) |
| `even_on_0_damage_if_knockback` | Boolean |  | 2 | `true` (Boolean) |
| `flat_chance` | Integer |  | 10 | `100` (Number), `50` (Number) |


### Object: `ChaosBossFormChangeGuide`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `active_pieces` | Array |  |  | `[Johnny Throb Flush]` (Array) |
| `passive_pieces` | Array |  |  | `[Host Nettle Bubs]` (Array) |
| `passives_health_threshold` | Integer |  | 2 | `50` (Number) |


### Object: `ChaosBossPieces`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `active_pieces` | Array |  |  | `[Johnny Throb Flush]` (Array) |
| `passive_pieces` | Array |  |  | `[Host Nettle Bubs]` (Array) |


### Object: `ChaosHeadDropIn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `ChaosSpawnIn` (Enum) |
| `new_music` | Enum |  | 2 | `chaos_boss_part2` (Enum) |
| `tag` | Array / Enum |  | 2 | `riftheadguardian` (Enum) |


### Object: `CharacterLightSource`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `color` | Array |  |  | `[.7 .8 .9]` (Array), `[1 1 1]` (Array) |
| `glow` | Array |  |  | `[1 .75 .5 .5]` (Array), `[1 1 1 1]` (Array) |
| `size` | Enum / Number |  | 32 | `1.7` (Number), `8` (Number) |


### Object: `Charge`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_CHARGE_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_CHARGE_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_CHARGE_DESC"` (String) |


### Object: `CharmAllFlies`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `Charmed` (Enum) |


### Object: `CherubimReaction`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Leave` | Enum / Object |  | 4 | `LELeave` (Enum), `CherubimLeave` (Enum), `{ ... }` (Object) |
| `Return` | Enum / Object |  | 4 | `CherubimReturn` (Enum), `LEReturn` (Enum), `{ ... }` (Object) |


### Object: `Conductor`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Tinkerer` (Enum) |
| `desc` | Enum |  |  | `"ITEM_CONDUCTOR_DESC"` (String), `"PASSIVE_CONDUCTOR_DESC"` (String) |
| `frame` | Integer |  |  | `62` (Number) |
| `kind` | Enum |  |  | `trinket` (Enum) |
| `name` | Enum |  |  | `"ITEM_CONDUCTOR_NAME"` (String), `"PASSIVE_CONDUCTOR_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `uncommon` (Enum) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `Confusion`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"KEYWORD_CONFUSION_NAME"` (String) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spell` (Enum) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_CONFUSION_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_CONFUSION_DESC"` (String) |


### Object: `ConjureBonusAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `Class` (Enum), `Colorless` (Enum) |
| `upgraded` | Boolean |  | 4 | `true` (Boolean) |


### Object: `Consumed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `drop_on_death` | Boolean / Enum |  | 22 | `false` (Boolean), `true` (Boolean), `deferred` (Enum) |
| `mount_mode` | Boolean / Enum |  | 24 | `true` (Boolean), `auto` (Enum) |


### Object: `ConvertDamageToScaledStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DelayedPain` | Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `stacks` | Enum / Integer |  | 2 | `3` (Number) |


### Object: `CounterAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 10 | `StegoTailSwipe` (Enum), `neck_TentacleArmorCounter` (Enum) |
| `chance` | Number |  | 2 | `15` (Number) |
| `melee_only` | Boolean |  | 2 | `true` (Boolean) |
| `ranged_only` | Boolean |  | 2 | `true` (Boolean) |
| `without_orienting` | Boolean |  | 2 | `true` (Boolean) |


### Object: `CounterNextAttacks`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_COUNTER_NAME"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_COUNTER_DESC_STACKS"` (String) |
| `tooltip_stacks_singular` | String |  |  | `"KEYWORD_COUNTER_DESC"` (String) |


### Object: `CreateGlobalModifiers`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BloodRain` | Integer / Object |  | 6 | `1` (Number), `{ ... }` (Object) |
| `LowerAmbientLight` | Object |  | 6 | `50` (Number), `33` (Number), `{ ... }` (Object) |


### Object: `CritChanceUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_CRITCHANCE_NAME"` (String) |
| `tooltip_stackless` | Enum |  |  | `none` (Enum) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_CRITCHANCE_DESC"` (String) |


### Object: `CyborgTurns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TakeBonusTurnWithAIControl` | Object |  | 2 | `{ ... }` (Object) |
| `stacks` | Enum / Integer |  | 2 | `1` (Number) |


### Object: `DamageUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_DAMAGEUP_NAME"` (String) |
| `name_stacks_neg` | String |  |  | `"KEYWORD_DAMAGEDOWN_NAME"` (String) |
| `tooltip_stackless_neg` | String |  |  | `"KEYWORD_DAMAGEDOWN_DESC_STACKLESS"` (String) |
| `tooltip_stackless_pos` | String |  |  | `"KEYWORD_DAMAGEUP_DESC_STACKLESS"` (String) |
| `tooltip_stacks_neg` | String |  |  | `"KEYWORD_DAMAGEDOWN_DESC"` (String) |
| `tooltip_stacks_pos` | String |  |  | `"KEYWORD_DAMAGEUP_DESC"` (String) |


### Object: `DeathChill`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Mage` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_DEATHCHILL_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_DEATHCHILL_NAME"` (String) |


### Object: `DeathRattleRevive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 16 | `HitlerPulp2` (Enum), `HitlerPulp4` (Enum) |
| `even_if_stunned` | Boolean |  | 16 | `true` (Boolean) |


### Object: `DejaVu`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `auto_plus_signs_on_name` | Boolean |  |  | `false` (Boolean) |
| `class` | Enum |  |  | `Disorder` (Enum) |
| `name` | Enum |  |  | `"DISORDER_DEJAVU_NAME"` (String) |


### Object: `DelayedAutoRevive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer |  | 12 | `30` (Number), `15` (Number) |
| `rounds` | Integer |  | 12 | `1` (Number), `2` (Number) |


### Object: `DepressionAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `AllStatsUp` (Enum) |
| `aura_effects_allies` | Boolean |  | 8 | `false` (Boolean) |
| `range` | Enum / Integer |  | 8 | `global` (Enum), `1` (Number) |
| `stacks` | Enum / Integer |  | 8 | `1` (Number) |


### Object: `DiceBehavior`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dice_size` | Integer |  | 2 | `6` (Number) |
| `knockback_damage` | Integer |  | 2 | `5` (Number) |


### Object: `DiesToElement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum |  | 2 | `Fire` (Enum) |
| `instant` | Boolean |  | 2 | `true` (Boolean) |


### Object: `DiesToPiercingAndSpikes`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deferred` | Boolean |  | 2 | `true` (Boolean) |


### Object: `DirtyClaws`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Colorless` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_DIRTYCLAWS_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_DIRTYCLAWS_NAME"` (String) |


### Object: `DivineShield`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `141` (Number) |
| `name` | Enum |  |  | `"KEYWORD_DIVINESHIELD_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_DIVINESHIELD_DESC"` (String) |


### Object: `DodgeChance_Status`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_DODGECHANCE_NAME"` (String) |
| `tooltip_stackless` | Enum |  |  | `none` (Enum) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_DODGECHANCE_DESC"` (String) |


### Object: `DodgeWhenTargeted`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `ShadowstepDodge` (Enum) |


### Object: `Doomed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_DOOMED_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_DOOMED_DESC"` (String) |


### Object: `DukeOfFlies`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Butcher` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_DUKEOFFLIES_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_DUKEOFFLIES_NAME"` (String) |


### Object: `DurabilityTransform`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `eq` | Array |  |  | `[2 EstusFlask_Half]` (Array), `[0 JarOfNothing]` (Array) |
| `ge` | Array |  |  | `[3 EstusFlask_Full]` (Array), `[2 WaterBottle_Full]` (Array) |


### Object: `DybbukPossessionFallback`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exit_ability` | Enum |  | 2 | `DybbukReturn` (Enum) |
| `form` | Enum / Integer |  | 2 | `Possessing` (Enum) |


### Object: `Dyslexia`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Disorder` (Enum) |
| `desc` | Enum |  |  | `"DISORDER_DYSLEXIA_DESC"` (String) |
| `name` | Enum |  |  | `"DISORDER_DYSLEXIA_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `Empath`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Disorder` (Enum) |
| `desc` | Enum |  |  | `"DISORDER_EMPATH_DESC"` (String) |
| `name` | Enum |  |  | `"DISORDER_EMPATH_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `ExtraBasicAttacks_Status`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_EXTRAATTACK_NAME"` (String) |
| `tooltip_stackless` | Enum |  |  | `none` (Enum) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_EXTRAATTACK_DESC"` (String) |


### Object: `ExtraBasicMoves_Status`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_EXTRAMOVE_NAME"` (String) |
| `tooltip_stackless` | Enum |  |  | `none` (Enum) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_EXTRAMOVE_DESC"` (String) |


### Object: `FaceAwayLastDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean |  | 2 | `true` (Boolean) |
| `override_hit_animation` | Boolean |  | 2 | `true` (Boolean) |
| `use_turn_animations` | Boolean |  | 2 | `true` (Boolean) |


### Object: `FaceLastDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean |  | 2 | `true` (Boolean) |


### Object: `FinalBossBeamQueue`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `queue` | Enum |  | 2 | `TheChild_TargetBeam` (Enum) |
| `release` | Enum |  | 2 | `TheChild_ReleaseBeams` (Enum) |
| `transform` | Enum |  | 2 | `TheChild_TransformBoris` (Enum) |


### Object: `FinalBossBecomeTheChild`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GlobalSpawnCharacter` | Enum |  | 2 | `MegaGuppy` (Enum) |
| `PlayBackground` | Integer |  | 2 | `1` (Number), `0` (Number) |
| `SwitchMusic` | Object |  | 2 | `{ ... }` (Object) |


### Object: `FinalBossHitCountdownBoris`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceUseAbility` | Enum / Object |  | 4 | `neck_ChefsApron` (Enum), `TheChild_TransformExplosive` (Enum), `{ ... }` (Object) |
| `icon` | Integer |  | 2 | `802` (Number) |
| `icon_ready` | Integer |  | 2 | `803` (Number) |
| `name` | Enum |  |  | `"KEYWORD_CHILDPULSE_NAME"` (String) |
| `stacks` | Enum / Integer |  | 2 | `7` (Number) |
| `tooltip` | Enum |  |  | `"KEYWORD_CHILDPULSE_DESC"` (String) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `FinalBossHitCountdownExplosive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceUseAbility` | Enum / Object |  | 4 | `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |
| `icon` | Integer |  | 2 | `800` (Number) |
| `icon_ready` | Integer |  | 2 | `801` (Number) |
| `name` | Enum |  |  | `"KEYWORD_CHILDWRATH_NAME"` (String) |
| `stacks` | Enum / Integer |  | 2 | `7` (Number) |
| `tooltip` | Enum |  |  | `"KEYWORD_CHILDWRATH_DESC"` (String) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `FinalBossHitCountdownHoly`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon` | Integer |  | 2 | `804` (Number) |
| `icon_ready` | Integer |  | 2 | `805` (Number) |
| `name` | Enum |  |  | `"KEYWORD_CHILDHOLY_NAME"` (String) |
| `stacks` | Enum / Integer |  | 2 | `7` (Number) |
| `tooltip` | Enum |  |  | `"KEYWORD_CHILDHOLY_DESC"` (String) |


### Object: `FinalBossPupils`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `look_at_offset` | Array |  |  | `[0 2.5 0]` (Array) |
| `radius` | Array / Integer |  | 2 | `13` (Number) |
| `reset_center_because_no_target_halflife` | Number |  | 2 | `.1` (String) |
| `reset_center_because_of_animation_halflife` | Number |  | 2 | `.05` (String) |
| `teleport_tracking_halflife` | Number |  | 2 | `.01` (String) |
| `tracking_acquisition_halflife` | Number |  | 2 | `.1` (String) |
| `virtual_head_position` | Array |  |  | `[11 2 11]` (Array) |


### Object: `FinalBossShieldHealth`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `break_ability` | Enum |  | 2 | `DestroyerBreakShield` (Enum) |
| `state_health` | Array |  |  | `[0 35 35 35 35 0]` (Array) |


### Object: `FinalBossSyncAnimations`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `other_character` | Enum |  | 2 | `MegaGuppy` (Enum) |
| `other_form_change_abilities` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Flammable`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `148` (Number) |
| `name` | Enum |  |  | `"KEYWORD_FLAMMABLE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_FLAMMABLE_DESC"` (String) |


### Object: `FlyDamageIncrease`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `DamageUp` (Enum) |
| `allies_only` | Boolean |  | 2 | `true` (Boolean) |
| `stacks` | Enum / Integer |  | 2 | `2` (Number) |


### Object: `Flying`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Psychic` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_FLYING_DESC"` (String) |
| `icon_frame` | Number |  |  | `157` (Number) |
| `name` | Enum |  |  | `"KEYWORD_FLYING_NAME"` (String), `"PASSIVE_FLYING_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_FLYING_DESC"` (String) |


### Object: `FollowUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Tank` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_FOLLOWUP_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_FOLLOWUP_NAME"` (String) |


### Object: `FormChangeDuringWeatherElement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum |  | 4 | `Water` (Enum) |
| `form` | Enum / Integer |  | 4 | `Rain` (Enum) |


### Object: `FormChangeHealthThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count_shield` | Boolean |  | 2 | `true` (Boolean) |
| `form_above` | Enum |  | 6 | `Default` (Enum), `Full` (Enum) |
| `form_below` | Enum |  | 6 | `DesireMech` (Enum), `Standing2` (Enum) |
| `threshold` | Enum / Integer / Object |  | 6 | `X-4` (Enum), `25` (Number), `50` (Number) |


### Object: `FormChangeOffMap`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form_offmap` | Enum |  | 16 | `Insane_Ceiling` (Enum), `SpawningPhase` (Enum) |
| `form_onmap` | Enum |  | 16 | `Default_Ground` (Enum), `Insane_Ground` (Enum) |


### Object: `FormChangeOnElementInfluence`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum |  | 16 | `[fire]` (Array), `water` (Enum), `wind` (Enum) |
| `exclude` | Enum |  | 10 | `water` (Enum), `fire` (Enum) |
| `form` | Enum / Integer |  | 18 | `hot` (Enum), `default` (Enum) |
| `particle` | Enum |  | 10 | `FireExtinguish` (Enum) |
| `sfx` | Enum |  | 10 | `FireExtinguish` (Enum) |


### Object: `FormChangeWhileHasStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form_has` | Enum |  | 50 | `Primed` (Enum), `Full` (Enum) |
| `form_hasnot` | Enum |  | 60 | `Default` (Enum), `Empty` (Enum) |
| `status` | Enum |  | 70 | `T2CopyCatInternal` (Enum), `Grappling` (Enum) |


### Object: `FormChangeWhilePrimingAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `not_priming` | Enum |  | 12 | `DualSword` (Enum), `SwordAndShield` (Enum) |
| `priming` | Enum |  | 16 | `DualSword_Primed` (Enum), `Priming` (Enum) |


### Object: `FormChanger`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Alert` | Object |  | 2 | `{ ... }` (Object) |
| `AllAlive` | Object |  | 6 | `{ ... }` (Object) |
| `Angry` | Object |  | 2 | `{ ... }` (Object) |
| `Attacker` | Object |  | 2 | `{ ... }` (Object) |
| `BellyFull` | Object |  | 2 | `{ ... }` (Object) |
| `Big` | Object |  | 4 | `{ ... }` (Object) |
| `BigHolding` | Object |  | 2 | `{ ... }` (Object) |
| `BigHoldingCat` | Object |  | 2 | `{ ... }` (Object) |
| `Bishop` | Boolean (Flag) / Object |  | 2 | `(Flag)` (Boolean (Flag)), `{ ... }` (Object) |
| `BlackHole` | Object |  | 2 | `{ ... }` (Object) |
| `Bomb` | Boolean (Flag) / Object |  | 2 | `(Flag)` (Boolean (Flag)), `{ ... }` (Object) |
| `Boris` | Enum / Object |  | 4 | `MegaGuppy_TransformBoris` (Enum), `{ ... }` (Object) |
| `Bully` | Object |  | 2 | `{ ... }` (Object) |
| `Butcher` | Object |  | 2 | `[CAT_EMBARK_QUOTES_BUTCHER_1 CAT_EMBARK_QUOTES_BUTCHER_2 CAT_EMBARK_QUOTES_BUTCHER_3 CAT_EMBARK_QUOTES_BUTCHER_4 CAT_EMBARK_QUOTES_BUTCHER_5 CAT_EMBARK_QUOTES_BUTCHER_6 CAT_EMBARK_QUOTES_BUTCHER_7 CAT_EMBARK_QUOTES_BUTCHER_8 CAT_EMBARK_QUOTES_BUTCHER_9 CAT_EMBARK_QUOTES_BUTCHER_10]` (Array), `[CAT_RETURN_EARLY_QUOTES_BUTCHER_1 CAT_RETURN_EARLY_QUOTES_BUTCHER_2 CAT_RETURN_EARLY_QUOTES_BUTCHER_3 CAT_RETURN_EARLY_QUOTES_BUTCHER_4 CAT_RETURN_EARLY_QUOTES_BUTCHER_5]` (Array), `{ ... }` (Object) |
| `CaveBaby` | Object |  | 2 | `{ ... }` (Object) |
| `CaveMan` | Object |  | 4 | `{ ... }` (Object) |
| `CaveManSpear` | Object |  | 4 | `{ ... }` (Object) |
| `CaveWoman` | Object |  | 2 | `{ ... }` (Object) |
| `CaveWomanHasCat` | Object |  | 2 | `{ ... }` (Object) |
| `Charging` | Object |  | 2 | `{ ... }` (Object) |
| `Close` | Object |  | 2 | `{ ... }` (Object) |
| `Colorless` | Array / Object |  | 2 | `[CAT_RETURN_EARLY_QUOTES_COLORLESS_1 CAT_RETURN_EARLY_QUOTES_COLORLESS_2 CAT_RETURN_EARLY_QUOTES_COLORLESS_3 CAT_RETURN_EARLY_QUOTES_COLORLESS_4 CAT_RETURN_EARLY_QUOTES_COLORLESS_5]` (Array), `[CAT_EMBARK_QUOTES_COLORLESS_1 CAT_EMBARK_QUOTES_COLORLESS_2 CAT_EMBARK_QUOTES_COLORLESS_3 CAT_EMBARK_QUOTES_COLORLESS_4 CAT_EMBARK_QUOTES_COLORLESS_5 CAT_EMBARK_QUOTES_COLORLESS_6 CAT_EMBARK_QUOTES_COLORLESS_7 CAT_EMBARK_QUOTES_COLORLESS_8]` (Array), `{ ... }` (Object) |
| `Cultist` | Object |  | 2 | `{ ... }` (Object) |
| `Damaged` | Object |  | 2 | `{ ... }` (Object) |
| `Default` | Enum / Object |  | 82 | `release` (Enum), `{ ... }` (Object) |
| `Default_Ceiling` | Object |  | 2 | `{ ... }` (Object) |
| `Default_Ground` | Object |  | 2 | `{ ... }` (Object) |
| `DesireMech` | Object |  | 2 | `{ ... }` (Object) |
| `Die` | Integer / Object |  | 2 | `6` (Number), `1` (Number), `{ ... }` (Object) |
| `Down` | Object |  | 6 | `{ ... }` (Object) |
| `Druid` | Array / Object |  | 2 | `[CAT_RETURN_EARLY_QUOTES_DRUID_1 CAT_RETURN_EARLY_QUOTES_DRUID_2 CAT_RETURN_EARLY_QUOTES_DRUID_3 CAT_RETURN_EARLY_QUOTES_DRUID_4 CAT_RETURN_EARLY_QUOTES_DRUID_5]` (Array), `[CAT_VS_BOSS_QUOTES_DRUID_1 CAT_VS_BOSS_QUOTES_DRUID_2 CAT_VS_BOSS_QUOTES_DRUID_3 CAT_VS_BOSS_QUOTES_DRUID_4 CAT_VS_BOSS_QUOTES_DRUID_5 CAT_VS_BOSS_QUOTES_DRUID_6 CAT_VS_BOSS_QUOTES_DRUID_7 CAT_VS_BOSS_QUOTES_DRUID_8 CAT_VS_BOSS_QUOTES_DRUID_9]` (Array), `{ ... }` (Object) |
| `Drunker` | Object |  | 2 | `{ ... }` (Object) |
| `DualSword` | Object |  | 2 | `{ ... }` (Object) |
| `DualSword_Primed` | Object |  | 2 | `{ ... }` (Object) |
| `Dumb` | Integer / Object |  | 2 | `3` (Number), `{ ... }` (Object) |
| `Empty` | Object |  | 4 | `{ ... }` (Object) |
| `Explody` | Object |  | 2 | `{ ... }` (Object) |
| `Explosive` | Enum / Object |  | 4 | `MegaGuppy_TransformExplosive` (Enum), `{ ... }` (Object) |
| `FightPhase` | Object |  | 2 | `{ ... }` (Object) |
| `Fighter` | Array / Object |  | 2 | `[CAT_VS_BOSS_QUOTES_FIGHTER_1 CAT_VS_BOSS_QUOTES_FIGHTER_2 CAT_VS_BOSS_QUOTES_FIGHTER_3 CAT_VS_BOSS_QUOTES_FIGHTER_4 CAT_VS_BOSS_QUOTES_FIGHTER_5 CAT_VS_BOSS_QUOTES_FIGHTER_6 CAT_VS_BOSS_QUOTES_FIGHTER_7 CAT_VS_BOSS_QUOTES_FIGHTER_8 CAT_VS_BOSS_QUOTES_FIGHTER_9]` (Array), `[CAT_RETURN_EARLY_QUOTES_FIGHTER_1 CAT_RETURN_EARLY_QUOTES_FIGHTER_2 CAT_RETURN_EARLY_QUOTES_FIGHTER_3 CAT_RETURN_EARLY_QUOTES_FIGHTER_4 CAT_RETURN_EARLY_QUOTES_FIGHTER_5 CAT_RETURN_EARLY_QUOTES_FIGHTER_6]` (Array), `{ ... }` (Object) |
| `Fire` | Integer / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `FireFull` | Integer / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `Flop` | Object |  | 2 | `{ ... }` (Object) |
| `Flop2` | Object |  | 2 | `{ ... }` (Object) |
| `Flush` | Object |  | 2 | `{ ... }` (Object) |
| `FlushBubs` | Object |  | 2 | `{ ... }` (Object) |
| `FlushHost` | Object |  | 2 | `{ ... }` (Object) |
| `FlushNettle` | Object |  | 2 | `{ ... }` (Object) |
| `Full` | Object |  | 6 | `{ ... }` (Object) |
| `Grappling` | Object |  | 2 | `{ ... }` (Object) |
| `Grown` | Object |  | 2 | `{ ... }` (Object) |
| `GuaranteedJackpot` | Object |  | 2 | `{ ... }` (Object) |
| `Guarding` | Object |  | 2 | `{ ... }` (Object) |
| `HalfDead` | Object |  | 2 | `{ ... }` (Object) |
| `HasCat` | Object |  | 10 | `{ ... }` (Object) |
| `HasDeadCat` | Object |  | 2 | `{ ... }` (Object) |
| `HasRock` | Object |  | 2 | `{ ... }` (Object) |
| `Headless` | Object |  | 2 | `{ ... }` (Object) |
| `Hint_CrackedVisuals` | Object |  | 2 | `{ ... }` (Object) |
| `Hint_CrackedVisuals2` | Object |  | 2 | `{ ... }` (Object) |
| `Hint_CrackedVisuals3` | Object |  | 2 | `{ ... }` (Object) |
| `Holding` | Object |  | 4 | `{ ... }` (Object) |
| `Holy` | Enum / Object |  | 4 | `MegaGuppy_TransformHoly` (Enum), `{ ... }` (Object) |
| `HumanDead` | Object |  | 2 | `{ ... }` (Object) |
| `Hunter` | Array / Object |  | 2 | `[CAT_RETURN_EARLY_QUOTES_HUNTER_1 CAT_RETURN_EARLY_QUOTES_HUNTER_2 CAT_RETURN_EARLY_QUOTES_HUNTER_3 CAT_RETURN_EARLY_QUOTES_HUNTER_4 CAT_RETURN_EARLY_QUOTES_HUNTER_5]` (Array), `[CAT_EMBARK_QUOTES_HUNTER_1 CAT_EMBARK_QUOTES_HUNTER_2 CAT_EMBARK_QUOTES_HUNTER_3 CAT_EMBARK_QUOTES_HUNTER_4 CAT_EMBARK_QUOTES_HUNTER_5 CAT_EMBARK_QUOTES_HUNTER_6 CAT_EMBARK_QUOTES_HUNTER_7 CAT_EMBARK_QUOTES_HUNTER_8 CAT_EMBARK_QUOTES_HUNTER_9 CAT_EMBARK_QUOTES_HUNTER_10]` (Array), `{ ... }` (Object) |
| `InitialPhase` | Object |  | 2 | `{ ... }` (Object) |
| `Insane_Ceiling` | Object |  | 2 | `{ ... }` (Object) |
| `Insane_Ground` | Object |  | 2 | `{ ... }` (Object) |
| `Johnny` | Object |  | 2 | `{ ... }` (Object) |
| `JohnnyBubs` | Object |  | 2 | `{ ... }` (Object) |
| `JohnnyHost` | Object |  | 2 | `{ ... }` (Object) |
| `JohnnyNettle` | Object |  | 2 | `{ ... }` (Object) |
| `Joystick` | Object |  | 2 | `{ ... }` (Object) |
| `LastHit` | Object |  | 2 | `{ ... }` (Object) |
| `Lifted` | Object |  | 2 | `{ ... }` (Object) |
| `Lit` | Object |  | 2 | `{ ... }` (Object) |
| `Mage` | Array / Object |  | 2 | `[CAT_VS_BOSS_QUOTES_MAGE_1 CAT_VS_BOSS_QUOTES_MAGE_2 CAT_VS_BOSS_QUOTES_MAGE_3 CAT_VS_BOSS_QUOTES_MAGE_4 CAT_VS_BOSS_QUOTES_MAGE_5 CAT_VS_BOSS_QUOTES_MAGE_6 CAT_VS_BOSS_QUOTES_MAGE_7]` (Array), `[CAT_RETURN_EARLY_QUOTES_MAGE_1 CAT_RETURN_EARLY_QUOTES_MAGE_2 CAT_RETURN_EARLY_QUOTES_MAGE_3 CAT_RETURN_EARLY_QUOTES_MAGE_4 CAT_RETURN_EARLY_QUOTES_MAGE_5]` (Array), `{ ... }` (Object) |
| `Medic` | Array / Object |  | 2 | `[CAT_EMBARK_QUOTES_MEDIC_1 CAT_EMBARK_QUOTES_MEDIC_2 CAT_EMBARK_QUOTES_MEDIC_3 CAT_EMBARK_QUOTES_MEDIC_4 CAT_EMBARK_QUOTES_MEDIC_5 CAT_EMBARK_QUOTES_MEDIC_6 CAT_EMBARK_QUOTES_MEDIC_7 CAT_EMBARK_QUOTES_MEDIC_8 CAT_EMBARK_QUOTES_MEDIC_9 CAT_EMBARK_QUOTES_MEDIC_10...]` (Array), `[CAT_VS_BOSS_QUOTES_MEDIC_1 CAT_VS_BOSS_QUOTES_MEDIC_2 CAT_VS_BOSS_QUOTES_MEDIC_3 CAT_VS_BOSS_QUOTES_MEDIC_4 CAT_VS_BOSS_QUOTES_MEDIC_5 CAT_VS_BOSS_QUOTES_MEDIC_6]` (Array), `{ ... }` (Object) |
| `Monk` | Array / Object |  | 2 | `[CAT_EMBARK_QUOTES_MONK_1 CAT_EMBARK_QUOTES_MONK_2 CAT_EMBARK_QUOTES_MONK_3 CAT_EMBARK_QUOTES_MONK_4 CAT_EMBARK_QUOTES_MONK_5 CAT_EMBARK_QUOTES_MONK_6 CAT_EMBARK_QUOTES_MONK_7 CAT_EMBARK_QUOTES_MONK_8]` (Array), `[CAT_RETURN_QUOTES_MONK_1 CAT_RETURN_QUOTES_MONK_2 CAT_RETURN_QUOTES_MONK_3 CAT_RETURN_QUOTES_MONK_4 CAT_RETURN_QUOTES_MONK_5]` (Array), `{ ... }` (Object) |
| `Mounted` | Object |  | 2 | `{ ... }` (Object) |
| `MouthFull` | Object |  | 2 | `{ ... }` (Object) |
| `Mutant` | Integer / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `Necromancer` | Array / Object |  | 2 | `[CAT_RETURN_EARLY_QUOTES_NECROMANCER_1 CAT_RETURN_EARLY_QUOTES_NECROMANCER_2 CAT_RETURN_EARLY_QUOTES_NECROMANCER_3 CAT_RETURN_EARLY_QUOTES_NECROMANCER_4 CAT_RETURN_EARLY_QUOTES_NECROMANCER_5 CAT_RETURN_EARLY_QUOTES_NECROMANCER_6]` (Array), `[CAT_EMBARK_QUOTES_NECROMANCER_1 CAT_EMBARK_QUOTES_NECROMANCER_2 CAT_EMBARK_QUOTES_NECROMANCER_3 CAT_EMBARK_QUOTES_NECROMANCER_4 CAT_EMBARK_QUOTES_NECROMANCER_5 CAT_EMBARK_QUOTES_NECROMANCER_6 CAT_EMBARK_QUOTES_NECROMANCER_7 CAT_EMBARK_QUOTES_NECROMANCER_8 CAT_EMBARK_QUOTES_NECROMANCER_9 CAT_EMBARK_QUOTES_NECROMANCER_10...]` (Array), `{ ... }` (Object) |
| `NeutronStar` | Object |  | 2 | `{ ... }` (Object) |
| `NoDeathRattle` | Object |  | 2 | `{ ... }` (Object) |
| `NoEyes` | Object |  | 2 | `{ ... }` (Object) |
| `NoStick` | Object |  | 2 | `{ ... }` (Object) |
| `Normal` | Integer / Object |  | 22 | `0` (Number), `{ ... }` (Object) |
| `NormalFull` | Integer / Object |  | 2 | `0` (Number), `{ ... }` (Object) |
| `NotPriming` | Object |  | 4 | `{ ... }` (Object) |
| `Nuke` | Object |  | 2 | `{ ... }` (Object) |
| `Obey` | Integer / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `Off` | Object |  | 2 | `{ ... }` (Object) |
| `OffMap` | Object |  | 8 | `{ ... }` (Object) |
| `OffScreen` | Object |  | 2 | `{ ... }` (Object) |
| `OneAlive` | Object |  | 6 | `{ ... }` (Object) |
| `OneEye` | Object |  | 2 | `{ ... }` (Object) |
| `Open` | Object |  | 2 | `{ ... }` (Object) |
| `OpenCat` | Object |  | 2 | `{ ... }` (Object) |
| `Out` | Object |  | 2 | `{ ... }` (Object) |
| `Possessing` | Object |  | 2 | `{ ... }` (Object) |
| `Primed` | Object |  | 2 | `{ ... }` (Object) |
| `Priming` | Object |  | 4 | `{ ... }` (Object) |
| `Psychic` | Array / Object |  | 2 | `[CAT_EMBARK_QUOTES_PSYCHIC_1 CAT_EMBARK_QUOTES_PSYCHIC_2 CAT_EMBARK_QUOTES_PSYCHIC_3 CAT_EMBARK_QUOTES_PSYCHIC_4 CAT_EMBARK_QUOTES_PSYCHIC_5 CAT_EMBARK_QUOTES_PSYCHIC_6 CAT_EMBARK_QUOTES_PSYCHIC_7 CAT_EMBARK_QUOTES_PSYCHIC_8 CAT_EMBARK_QUOTES_PSYCHIC_9 CAT_EMBARK_QUOTES_PSYCHIC_10]` (Array), `[CAT_RETURN_QUOTES_PSYCHIC_1 CAT_RETURN_QUOTES_PSYCHIC_2 CAT_RETURN_QUOTES_PSYCHIC_3 CAT_RETURN_QUOTES_PSYCHIC_4 CAT_RETURN_QUOTES_PSYCHIC_5]` (Array), `{ ... }` (Object) |
| `Pulp2` | Object |  | 2 | `{ ... }` (Object) |
| `Pulp3` | Object |  | 2 | `{ ... }` (Object) |
| `Pulp4` | Object |  | 2 | `{ ... }` (Object) |
| `Pulp5` | Object |  | 2 | `{ ... }` (Object) |
| `Pulp6` | Object |  | 2 | `{ ... }` (Object) |
| `Pulp7` | Object |  | 2 | `{ ... }` (Object) |
| `Rage` | Object |  | 20 | `{ ... }` (Object) |
| `Rain` | Object |  | 4 | `4` (Number), `1` (Number), `{ ... }` (Object) |
| `Sitting` | Object |  | 2 | `{ ... }` (Object) |
| `Small` | Object |  | 4 | `{ ... }` (Object) |
| `SmallHolding` | Object |  | 2 | `{ ... }` (Object) |
| `SmallHoldingCat` | Object |  | 2 | `{ ... }` (Object) |
| `SpawningPhase` | Object |  | 2 | `{ ... }` (Object) |
| `SquirrelForm` | Object |  | 4 | `{ ... }` (Object) |
| `Standing` | Object |  | 2 | `{ ... }` (Object) |
| `Standing2` | Object |  | 2 | `{ ... }` (Object) |
| `Start_Ceiling` | Object |  | 2 | `{ ... }` (Object) |
| `Stop` | Integer / Object |  | 2 | `2` (Number), `{ ... }` (Object) |
| `SwordAndShield` | Object |  | 2 | `{ ... }` (Object) |
| `SwordAndShield_Primed` | Object |  | 2 | `{ ... }` (Object) |
| `Tank` | Array / Object |  | 2 | `[CAT_EMBARK_QUOTES_TANK_1 CAT_EMBARK_QUOTES_TANK_2 CAT_EMBARK_QUOTES_TANK_3 CAT_EMBARK_QUOTES_TANK_4 CAT_EMBARK_QUOTES_TANK_5 CAT_EMBARK_QUOTES_TANK_6 CAT_EMBARK_QUOTES_TANK_7 CAT_EMBARK_QUOTES_TANK_8 CAT_EMBARK_QUOTES_TANK_9 CAT_EMBARK_QUOTES_TANK_10...]` (Array), `[CAT_RETURN_QUOTES_TANK_1 CAT_RETURN_QUOTES_TANK_2 CAT_RETURN_QUOTES_TANK_3 CAT_RETURN_QUOTES_TANK_4 CAT_RETURN_QUOTES_TANK_5]` (Array), `{ ... }` (Object) |
| `Tar` | Integer / Object |  | 2 | `2` (Number), `{ ... }` (Object) |
| `TarFull` | Integer / Object |  | 2 | `2` (Number), `{ ... }` (Object) |
| `Thief` | Array / Object |  | 2 | `[CAT_VS_BOSS_QUOTES_THIEF_1 CAT_VS_BOSS_QUOTES_THIEF_2 CAT_VS_BOSS_QUOTES_THIEF_3 CAT_VS_BOSS_QUOTES_THIEF_4 CAT_VS_BOSS_QUOTES_THIEF_5 CAT_VS_BOSS_QUOTES_THIEF_6]` (Array), `[CAT_RETURN_QUOTES_THIEF_1 CAT_RETURN_QUOTES_THIEF_2 CAT_RETURN_QUOTES_THIEF_3 CAT_RETURN_QUOTES_THIEF_4 CAT_RETURN_QUOTES_THIEF_5]` (Array), `{ ... }` (Object) |
| `Throb` | Object |  | 2 | `{ ... }` (Object) |
| `ThrobBubs` | Object |  | 2 | `{ ... }` (Object) |
| `ThrobHost` | Object |  | 2 | `{ ... }` (Object) |
| `ThrobNettle` | Object |  | 2 | `{ ... }` (Object) |
| `Tinkerer` | Array / Object |  | 2 | `[CAT_EMBARK_QUOTES_TINKERER_1 CAT_EMBARK_QUOTES_TINKERER_2 CAT_EMBARK_QUOTES_TINKERER_3 CAT_EMBARK_QUOTES_TINKERER_4 CAT_EMBARK_QUOTES_TINKERER_5 CAT_EMBARK_QUOTES_TINKERER_6 CAT_EMBARK_QUOTES_TINKERER_7 CAT_EMBARK_QUOTES_TINKERER_8 CAT_EMBARK_QUOTES_TINKERER_9 CAT_EMBARK_QUOTES_TINKERER_10]` (Array), `[CAT_RETURN_EARLY_QUOTES_TINKERER_1 CAT_RETURN_EARLY_QUOTES_TINKERER_2 CAT_RETURN_EARLY_QUOTES_TINKERER_3]` (Array), `{ ... }` (Object) |
| `Transformed` | Object |  | 2 | `{ ... }` (Object) |
| `Turtled` | Object |  | 4 | `{ ... }` (Object) |
| `TwoAlive` | Object |  | 6 | `{ ... }` (Object) |
| `TwoEyes` | Object |  | 2 | `{ ... }` (Object) |
| `Unlit` | Object |  | 2 | `{ ... }` (Object) |
| `Unmounted` | Object |  | 2 | `{ ... }` (Object) |
| `Unwashed` | Object |  | 2 | `{ ... }` (Object) |
| `Up` | Object |  | 6 | `{ ... }` (Object) |
| `Washed` | Object |  | 2 | `{ ... }` (Object) |
| `Washer` | Object |  | 2 | `{ ... }` (Object) |
| `Water` | Object |  | 2 | `{ ... }` (Object) |
| `WereMan` | Object |  | 2 | `{ ... }` (Object) |
| `Zealot` | Object |  | 2 | `{ ... }` (Object) |
| `ZealotBomb` | Object |  | 2 | `{ ... }` (Object) |
| `active` | Object |  | 4 | `{ ... }` (Object) |
| `default` | Enum / Object |  | 82 | `{ ... }` (Object) |
| `hot` | Object |  | 8 | `{ ... }` (Object) |
| `initial_form` | Enum / Integer |  | 112 | `Default` (Enum), `Normal` (Enum), `1` (Number), `5` (Number) |
| `passive` | Object |  | 4 | `{ ... }` (Object) |
| `sync_brain_patterns` | Boolean |  | 2 | `true` (Boolean) |


### Object: `Fragile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `149` (Number) |
| `name` | Enum |  |  | `"KEYWORD_FRAGILE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_FRAGILE_DESC"` (String) |


### Object: `FragileDuringElement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `Fragile` (Enum) |


### Object: `FrankBolts`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum |  |  | `"ARMOR_FRANKBOLTS_DESC"` (String) |
| `frame` | Integer |  |  | `21` (Number) |
| `kind` | Enum |  |  | `neck` (Enum) |
| `name` | Enum |  |  | `"ARMOR_FRANKBOLTS_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `rarity` | Enum |  |  | `uncommon` (Enum) |
| `set` | Array / Enum |  |  | `[Bionic Cyborg]` (Array) |
| `shield` | Enum / Integer |  |  | `[1 .5]` (Array), `2` (Number) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `FullPower`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Psychic` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_FULLPOWER_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_FULLPOWER_NAME"` (String) |


### Object: `GlobalFamiliarDamageBoost`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `DamageUp` (Enum) |


### Object: `GlobalFamiliarMoveBoost`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `MovementUp` (Enum) |


### Object: `GlobalFlowerTrapperAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Tangled` | Array / Integer / Object |  |  | `[1 .1]` (Array), `[1 .33]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |


### Object: `GlobalMeleeRevengeDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Enum / Integer |  | 2 | `5` (Number) |


### Object: `HPAltStates`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `clipname` | Enum |  | 2 | `poopmain` (Enum) |
| `thresholds` | Array |  |  | `[[ 1 0 ] [ 0 3 ]]` (Array) |


### Object: `HealNeighborsEachTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 2 | `true` (Boolean) |
| `stacks` | Enum / Integer |  | 2 | `3` (Number) |


### Object: `HealingAura`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Medic` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_HEALINGAURA_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_HEALINGAURA_NAME"` (String) |


### Object: `HealthPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `anything_eats` | Boolean |  | 8 | `true` (Boolean) |
| `force_frame` | Integer |  | 2 | `12` (Number) |
| `frame_range` | Array |  |  | `[1 2]` (Array), `[5 5]` (Array) |
| `stacks` | Enum / Integer |  | 30 | `7` (Number), `10` (Number) |
| `stored_food_value` | Integer |  | 30 | `4` (Number), `2` (Number) |


### Object: `HealthRegenUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_HEALTHREGEN_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_HEALTHREGEN_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_HEALTHREGEN_DESC"` (String) |


### Object: `HitlerExecute`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `HitlerShoot` (Enum) |
| `tag` | Array / Enum |  | 2 | `grown_hitler_clone` (Enum) |
| `threshold` | Enum / Integer / Object |  | 2 | `15` (Number) |


### Object: `Hypomania`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Disorder` (Enum) |
| `desc` | Enum |  |  | `"DISORDER_HYPOMANIA_DESC"` (String) |
| `name` | Enum |  |  | `"DISORDER_HYPOMANIA_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `ImmediateAbilityReaction`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 26 | `FormShrinkTwoSnakey` (Enum), `ButtWeb_AlreadyEnraged` (Enum) |
| `ability_damage_only` | Boolean |  | 12 | `true` (Boolean) |
| `backstabs_only` | Boolean |  | 4 | `true` (Boolean) |
| `buddy_damage_only` | Boolean |  | 2 | `true` (Boolean) |
| `damage_threshold` | Integer |  | 4 | `10` (Number) |
| `even_if_blocked` | Boolean |  | 4 | `true` (Boolean) |
| `even_if_stunned` | Boolean |  | 4 | `true` (Boolean) |
| `health_threshold` | Integer |  | 4 | `50` (Number), `70` (Number) |
| `target_furthest_valid` | Boolean |  | 2 | `true` (Boolean) |


### Object: `Immobile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_IMMOBILE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_IMMOBILE_DESC"` (String) |


### Object: `ImmortalLeeches`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Necromancer` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_IMMORTALLEECHES_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_IMMORTALLEECHES_NAME"` (String) |


### Object: `ItemAuxTransform`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ge` | Array |  |  | `[20 BlackShard_Glowing]` (Array), `[10 NuclearKnife_Glowing]` (Array) |
| `le` | Array |  |  | `[50 MoneyBag_Large]` (Array), `[10 MoneyBag_Small]` (Array) |
| `lt` | Array |  |  | `[10 NuclearKnife]` (Array) |


### Object: `JohnnyNeedsWashing`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form_unwashed` | Enum |  | 2 | `Unwashed` (Enum) |
| `form_washed` | Enum |  | 2 | `Washed` (Enum) |


### Object: `KillsHeal`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Fighter` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_FERVOR_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_FERVOR_NAME"` (String) |


### Object: `KineticSpikes`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_KINETICSPPIKES_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_KINETICSPPIKES_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_KINETICSPPIKES_DESC"` (String) |
| `tooltip_stacks_singular` | String |  |  | `"KEYWORD_KINETICSPPIKES_DESC_SINGULAR"` (String) |


### Object: `Lifesteal`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_LIFESTEAL_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_LIFESTEAL_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_LIFESTEAL_DESC"` (String) |


### Object: `LuckUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_LCKUP_NAME"` (String) |
| `name_stacks_neg` | String |  |  | `"KEYWORD_LCKDOWN_NAME"` (String) |
| `tooltip_stackless` | Enum |  |  | `none` (Enum) |
| `tooltip_stacks_neg` | String |  |  | `"KEYWORD_LCKDOWN_DESC"` (String) |
| `tooltip_stacks_pos` | String |  |  | `"KEYWORD_LCKUP_DESC"` (String) |


### Object: `Madness`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_MADNESS_NAME"` (String) |
| `stacks` | Enum / Integer |  | 2 | `1` (Number) |
| `tickdown_this_turn` | Boolean |  | 2 | `true` (Boolean) |
| `tooltip` | Enum |  |  | `"KEYWORD_MADNESS_DESC"` (String) |


### Object: `ManaPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `frame_range` | Array |  |  | `[6 6]` (Array), `[1 2]` (Array) |
| `stacks` | Enum / Integer |  | 6 | `4` (Number), `6` (Number) |


### Object: `MegaDinoDropController`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `head_drop` | Enum |  | 2 | `MD_HeadDrop` (Enum) |
| `leg_leave` | Enum |  | 2 | `MD_LegLeave` (Enum) |
| `leg_return` | Enum |  | 2 | `MD_LegReturn` (Enum) |
| `stable_legs` | Integer |  | 2 | `3` (Number) |


### Object: `Metal`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `151` (Number) |
| `name` | Enum |  |  | `"KEYWORD_METAL_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_METAL_DESC"` (String) |


### Object: `MetalDetector`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Colorless` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_METALDETECTOR_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_METALDETECTOR_NAME"` (String) |


### Object: `MissChance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_MISSCHANCE_NAME"` (String) |
| `tooltip_stackless` | Enum |  |  | `none` (Enum) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_MISSCHANCE_DESC"` (String) |


### Object: `ModularPickup`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Cleanse` | Integer / Object |  | 2 | `1` (Number), `0` (Number), `{ ... }` (Object) |
| `sound_event` | Enum |  | 2 | `EatAntidote` (Enum) |


### Object: `MonkCatReactionAbilities`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `attack` | Enum |  | 6 | `attack` (Enum) |
| `move` | Enum |  | 4 | `move` (Enum) |
| `spell` | Enum |  | 2 | `MCHadouken` (Enum) |
| `trinket` | Enum |  | 2 | `MCHadouken` (Enum) |
| `weapon` | Enum |  | 2 | `attack` (Enum) |


### Object: `MotherGrowController`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `eat_damage` | Object |  | 2 | `{ ... }` (Object) |
| `tumor_object` | Enum |  | 2 | `MotherTumor` (Enum) |


### Object: `MotherTumorPassive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Cat` | Object |  | 2 | `{ ... }` (Object) |
| `NonCat` | Object |  | 2 | `{ ... }` (Object) |
| `considered_forms` | Array |  |  | `[Big BigHolding BigHoldingCat]` (Array) |
| `grow_ability` | Enum |  | 2 | `MotherTumorGrow` (Enum) |
| `pass_ani` | Enum |  | 2 | `pass` (Enum) |
| `receive_ani` | Enum |  | 2 | `receive` (Enum) |


### Object: `MotherTumorSpawnInCapture`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Cat` | Object |  | 4 | `{ ... }` (Object) |
| `NonCat` | Object |  | 4 | `{ ... }` (Object) |
| `Nothing` | Object |  | 2 | `{ ... }` (Object) |


### Object: `Mount`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `eject_ability` | Enum |  | 2 | `MechSuitEject` (Enum) |
| `enter_ability` | Enum |  | 2 | `EnterMech` (Enum) |


### Object: `MoveAfterAnyAttemptedAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `weights` | Array / Enum |  | 2 | `bat_chaos_runaway` (Enum) |


### Object: `MoveAwayFromDamageSource`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `move_ability` | Enum |  | 2 | `BirdFly` (Enum) |


### Object: `MoveAwayWhenEnemyAdjacent`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `move_ability` | Enum |  | 2 | `YA_Jetpack` (Enum) |
| `once_per_turn` | Boolean |  | 2 | `true` (Boolean) |
| `weights` | Array / Enum |  | 2 | `stay_far_always_move` (Enum) |


### Object: `MoveQuivered`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_BONUSMOVE_NAME"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_BONUSMOVE_DESC_STACKS"` (String) |
| `tooltip_stacks_singular` | String |  |  | `"KEYWORD_BONUSMOVE_DESC"` (String) |


### Object: `MoveTowardsKillers`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `character_filter` | Array |  |  | `[SpiderCat TallSpiderCat]` (Array) |
| `move_ability` | Enum |  | 6 | `SpiderReturn` (Enum) |


### Object: `MultiSpawnOnDeath`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer |  |  | `[0 2]` (Array) |
| `obj` | Array / Enum |  | 2 | `Maggot` (Enum) |


### Object: `MutateAfterXTurns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `TransformInXTurns` (Enum) |


### Object: `NoManaRegen`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_NOMANAREGEN_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_NOMANAREGEN_DESC"` (String) |


### Object: `NonStackingDivineShield`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `DivineShield` (Enum) |


### Object: `NumbingLeeches`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Necromancer` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_NUMBINGLEECHES_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_NUMBINGLEECHES_NAME"` (String) |


### Object: `ObjectDetector`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number |  | 2 | `10` (Number) |
| `object` | Array / Enum |  | 2 | `CharmedDip` (Enum) |


### Object: `Paranoia`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Disorder` (Enum) |
| `desc` | Enum |  |  | `"DISORDER_PARANOIA_DESC"` (String) |
| `name` | Enum |  |  | `"DISORDER_PARANOIA_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `PassiveIfStrAuxEquals`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 14 | `{ ... }` (Object) |
| `value` | Enum |  | 14 | `int` (Enum), `spd` (Enum) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `PassiveIfWeaponIsUsable`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Brace` | Enum / Integer / Object |  | 4 | `[1 .5]` (Array), `10` (Number), `4` (Number), `{ ... }` (Object) |


### Object: `PassiveWhenDead`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AutocastEachRound` | Enum / Object |  | 2 | `SpiderReturn` (Enum), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `PassiveWhenOnTile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 14 | `{ ... }` (Object) |
| `tile` | Array / Enum |  |  | `[WaterTile]` (Array), `[TallGrassTile TallFlowerTile]` (Array) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `PassiveWhileHasDurability`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MovementReaction` | Object |  | 2 | `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `PassiveWhileNotHasStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives` | Object |  | 4 | `{ ... }` (Object) |
| `status` | Enum |  | 4 | `DemonicGlyph_Movement` (Enum), `ExistUntilIdleUpkeep` (Enum) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `PassiveWhileShielded`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer |  | 2 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |


### Object: `PermanentImmobile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `Immobile` (Enum) |


### Object: `PermanentMadness`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `Madness` (Enum) |


### Object: `Poison`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_POISON_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_POISON_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_POISON_DESC"` (String) |


### Object: `PoisonThorns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_POISONOUS_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_POISONOUS_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_POISONOUS_DESC"` (String) |


### Object: `PoopWhenHit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number |  | 2 | `25` (Number) |
| `object` | Array / Enum |  | 2 | `Poop` (Enum) |


### Object: `ProtectTargetedAllies`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `SwapPositions_TankCat` (Enum) |
| `target_filter` | Enum |  | 4 | `any` (Enum), `Kitten` (Enum) |


### Object: `Quiver`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Hunter` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_QUIVER_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_QUIVER_NAME"` (String) |


### Object: `Quivered`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_QUIVERED_NAME"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_QUIVERED_DESC"` (String) |
| `tooltip_stacks_singular` | String |  |  | `"KEYWORD_QUIVERED_DESC_STACKLESS"` (String) |


### Object: `ReduceManaCost`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_REDUCEMANACOST_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_REDUCEMANACOST_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_REDUCEMANACOST_DESC"` (String) |


### Object: `ReflectProjectiles`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `self_damage` | Boolean / Integer / Object |  | 16 | `2` (Number) |


### Object: `RefreshEquipmentAbilityOnElement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum |  | 4 | `Electric` (Enum) |
| `text` | String |  | 4 | `"COMBAT_POPUP_RECHARGED"` (String) |


### Object: `RunWhenLastPlayerCatIsCharmed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean |  | 2 | `true` (Boolean) |
| `legacy_savekey` | Enum |  | 2 | `Legacy_Marshmallow_StolenCatID` (Enum) |


### Object: `SafeDoomed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_SAFEDOOMED_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_SAFEDOOMED_DESC"` (String) |


### Object: `ScaldingOrbMoonBossOneShot`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CompleteItemQuest` | Enum |  | 2 | `Nuke` (Enum), `ScaldingOrb` (Enum) |
| `RemoveItem` | Enum |  | 2 | `BlackShard_Glowing` (Enum), `ScaldingOrb` (Enum) |


### Object: `ScaledStatusAlliesOnSpendMana`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Conditional_Adjacent` | Object |  | 2 | `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `ScaledStatusOnHolyShieldBlock`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Integer / Object |  | 2 | `[1 .5]` (Array), `6` (Number), `10` (Number), `{ ... }` (Object) |


### Object: `ScalingAttackAnimation`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `default` | Enum / Object |  | 2 | `bite1` (Enum) |
| `thresholds` | Array |  |  | `[[ 5 bite2 ] [ 10 bite3 ]]` (Array) |


### Object: `SchrodingerDisorder`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Disorder` (Enum) |
| `desc` | Enum |  |  | `"DISORDER_SCHRODINGERDISORDER_DESC"` (String) |
| `name` | Enum |  |  | `"DISORDER_SCHRODINGERDISORDER_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `Scleroderma`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Disorder` (Enum) |
| `desc` | Enum |  |  | `"DISORDER_SCLERODERMA_DESC"` (String) |
| `name` | Enum |  |  | `"DISORDER_SCLERODERMA_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `SharePickups`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_coins` | Boolean |  | 2 | `true` (Boolean) |


### Object: `ShoulderCheck`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Fighter` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_SHOULDERCHECK_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_SHOULDERCHECK_NAME"` (String) |


### Object: `ShovingMatch`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Tank` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_SHOVINGMATCH_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_SHOVINGMATCH_NAME"` (String) |


### Object: `SkipFirstRounds`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pop_chance` | Integer |  | 2 | `50` (Number) |
| `stacks` | Enum / Integer |  | 2 | `2` (Number) |


### Object: `SlotMachineRollPool`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SlotResult_Explode` | Integer / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `SlotResult_Jackpot_Coins` | Integer / Object |  | 4 | `1` (Number), `{ ... }` (Object) |
| `SlotResult_Nothing` | Integer / Object |  | 2 | `7` (Number), `{ ... }` (Object) |
| `SlotResult_RandomPickup` | Integer / Object |  | 2 | `11` (Number), `{ ... }` (Object) |


### Object: `Slow`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"KEYWORD_SLOW_NAME"` (String) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `spell` (Enum) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_SLOW_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_SLOW_DESC"` (String) |
| `tooltip_stacks_neg` | String |  |  | `"KEYWORD_SLOW_DESC_STACKLESS"` (String) |


### Object: `SmallRockBehavior`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chain` | Boolean |  | 4 | `true` (Boolean) |
| `damage` | Equation |  | 8 | `9` (Equation), `5` (Equation) |
| `knockback` | Enum / Integer |  | 8 | `1` (Number), `5` (Number) |


### Object: `SpawnCatCopyWhenDowned`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum |  | 4 | `PlayerCat_NecroShade` (Enum), `PlayerCat_AncestralShade` (Enum) |
| `prevent_chain_tag` | Enum |  | 4 | `necroset_shade` (Enum), `ancestorset_shade` (Enum) |


### Object: `SpawnExtraThingsOnBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `number` | Array / Integer |  | 3 | `[3 8]` (Array), `[0 2]` (Array), `3` (Number), `1` (Number) |
| `object` | Array / Enum |  | 19 | `[Spookie Scary Tatters Wisp Wisp Wisp]` (Array), `[Bombchu Deathbot RoboVacuum TinkererTurret]` (Array), `NeutralToad` (Enum), `Poop` (Enum) |
| `tile` | Array / Enum |  | 7 | `TallGrassTile` (Enum), `FireTile` (Enum) |
| `trap` | Enum |  | 2 | `BearTrap` (Enum), `LandMine` (Enum) |


### Object: `SpawnItemLinkedFamiliar`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean |  | 4 | `true` (Boolean) |
| `object` | Array / Enum |  | 4 | `PyrophinaFamiliar` (Enum), `ZaratanaFamiliar` (Enum) |


### Object: `SpawnObjectOnPopCorpse`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer |  | 2 | `2` (Number) |
| `except_tiny` | Boolean |  | 2 | `true` (Boolean) |
| `object` | Array / Enum |  | 2 | `CharmedTinySpider` (Enum) |


### Object: `SpawnOnDeath`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `additional_statuses` | Object |  | 2 | `{ ... }` (Object) |
| `faction` | Enum |  | 8 | `enemies` (Enum), `allies` (Enum) |
| `obj` | Array / Enum |  | 4 | `[Spookie Spookie Scary Coin2 Coin3 Coin4]` (Array), `[Kitten Kitten TomTom TomTom Mangy Mangy CatCaller CatCaller GlassSpitter SpiderCat...]` (Array), `BeefyCharmedLeech` (Enum), `RiftKitten` (Enum) |


### Object: `SpawnRandomPickupsOnTaggedUnitKilled`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer |  |  | `[2 3]` (Array) |
| `tag` | Array / Enum |  | 2 | `poop` (Enum) |


### Object: `SpeedUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_SPDUP_NAME"` (String) |
| `name_stacks_neg` | String |  |  | `"KEYWORD_SPDDOWN_NAME"` (String) |
| `tooltip_stackless` | Enum |  |  | `none` (Enum) |
| `tooltip_stacks_neg` | String |  |  | `"KEYWORD_SPWDDOWN_DESC"` (String) |
| `tooltip_stacks_pos` | String |  |  | `"KEYWORD_SPDUP_DESC"` (String) |


### Object: `SpellDamageUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_MAGICDMGUP_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_MAGICDMGUP_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_MAGICDMGUP_DESC"` (String) |


### Object: `SpewerAltGraphics`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fire` | Integer / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `FireFull` | Integer / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `Normal` | Integer / Object |  | 2 | `0` (Number), `{ ... }` (Object) |
| `NormalFull` | Integer / Object |  | 2 | `0` (Number), `{ ... }` (Object) |
| `Tar` | Integer / Object |  | 2 | `2` (Number), `{ ... }` (Object) |
| `TarFull` | Integer / Object |  | 2 | `2` (Number), `{ ... }` (Object) |


### Object: `SproutsGrantMovement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `MovementUp` (Enum) |


### Object: `StackingFlowerTrail`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stack_key` | Enum |  | 6 | `FLOWER_SET` (String) |
| `stacks` | Enum / Integer |  | 6 | `1` (Number) |


### Object: `StatDependentPassive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddDamageToBasicAttack` | String |  | 2 | `4` (Number), `1` (Number), `"min(min(min(min(min(min(str,dex),int),con),lck),spd),cha)-2"` (String) |


### Object: `StatusAdjacentOnTheirTurnEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveAway` | Integer |  | 2 | `1` (Number), `{ ... }` (Object) |


### Object: `StatusAfterXTurns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceUseAbility` | Enum / Object |  | 4 | `neck_ChefsApron` (Enum), `CancerExplode` (Enum), `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `StatusAllCharactersOnSpawn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Else` | Object |  | 1 | `{ ... }` (Object) |
| `Poison` | Array / Integer |  | 2 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `StatusCollector`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer |  | 8 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| `Slow` | Array / Enum / Integer / Object |  | 8 | `[1 .1]` (Array), `[1 .25]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer |  | 14 | `[1 .5]` (Array), `4` (Number), `-2` (Number), `{ ... }` (Object) |


### Object: `StatusEachRoundBegin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NonStackingShield` | Number |  | 16 | `3` (Number), `8` (Number) |


### Object: `StatusEachRoundEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DoDamage` | Object |  | 2 | `{ ... }` (Object) |
| `UseAbility` | Enum / Object |  | 2 | `GirlDinoPoop` (Enum), `Spit` (Enum), `{ ... }` (Object) |


### Object: `StatusEachTurnBeginIfHasStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer |  | 2 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String |  | 2 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer |  | 2 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `animation` | Enum |  | 2 | `pulse3` (Enum) |
| `consume` | Boolean |  | 2 | `true` (Boolean) |
| `status` | Enum |  | 2 | `Counterspell` (Enum) |


### Object: `StatusEachTurnEndIfEnabledAtStartOfTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceUseAbility` | Enum / Object |  | 2 | `neck_ChefsApron` (Enum), `T2UnClone` (Enum), `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `StatusEveryXSpellCastsEachTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer |  | 2 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `stacks` | Enum / Integer |  | 2 | `3` (Number) |


### Object: `StatusIfDidntMove`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Integer |  | 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |


### Object: `StatusIfUnusedActPoints`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BackflipWhenTargeted` | Enum / Integer / Object |  | 2 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Craft` | Object |  | 2 | `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `StatusOnBackstab`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer |  | 2 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `SerratedClaws` | Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |


### Object: `StatusOnBreak`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ApplyToRandomPartyMemberIfPossible` | Object |  | 2 | `{ ... }` (Object) |
| `Bruise` | Array / Integer / Object |  | 6 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer |  | 2 | `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DexterityUp` | Enum / Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `FindItemFromPool` | Enum / Object |  | 6 | `chapter_specific_item` (Enum), `chapter_common` (Enum), `{ ... }` (Object) |
| `HealthGain` | Integer |  | 6 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `HealthRegenUp` | Integer |  | 6 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer |  | 2 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `ObjectOnHitCharacter` | Enum / Object |  | 2 | `BestBud` (Enum), `Maggot` (Enum), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer |  | 2 | `[1 .5]` (Array), `4` (Number), `-2` (Number), `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `StatusOnDie`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FindItemFromPool` | Enum / Object |  | 2 | `chapter_specific_item` (Enum), `chapter_common` (Enum), `{ ... }` (Object) |
| `RandomMagicMissile` | Integer / Object |  | 2 | `[1 .5]` (Array), `10` (Number), `6` (Number), `{ ... }` (Object) |
| `RemoveAmbientLightEffects` | Number |  | 2 | `4` (Number), `.5` (String) |
| `ScatterCoins` | Object |  | 2 | `[1 .5]` (Array), `5` (Number), `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `StatusOnDodge`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Integer |  | 2 | `[1 .5]` (Array), `15` (Number), `66` (Number), `{ ... }` (Object) |


### Object: `StatusOnEnemyCastSpell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer |  | 2 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer |  | 2 | `2*X` (Enum), `3*X` (Enum), `8` (Number), `10` (Number) |


### Object: `StatusOnEnemyConfused`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ImmediateUseAbility` | Enum / Object |  | 2 | `cm_Lard_Impl` (Enum), `tk_ButterBean_Mega` (Enum), `{ ... }` (Object) |


### Object: `StatusOnEnemyDeath`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Integer |  | 2 | `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |


### Object: `StatusOnFallAsleep`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer |  | 2 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `FillMana` | Integer |  | 2 | `[1 .25]` (Array), `[1 .10]` (Array), `1` (Number) |
| `HealRandomInjury` | Integer |  | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |


### Object: `StatusOnFullMana`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Conditional_OncePerBattle` | Object |  | 2 | `{ ... }` (Object) |


### Object: `StatusOnSetPieceBreak`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FindItemFromPool` | Enum / Object |  | 2 | `chapter_specific_item` (Enum), `consumables` (Enum), `{ ... }` (Object) |
| `PermanentCharisma` | Integer |  | 2 | `1` (Number), `2` (Number) |
| `PermanentConstitution` | Integer |  | 2 | `-1` (Number), `-2` (Number) |
| `PermanentDexterity` | Integer |  | 2 | `1` (Number), `2` (Number) |
| `PermanentIntelligence` | Integer |  | 2 | `1` (Number), `2` (Number) |
| `PermanentLuck` | Integer |  | 2 | `1` (Number), `2` (Number) |
| `PermanentSpeed` | Integer |  | 2 | `1` (Number), `2` (Number) |
| `PermanentStrength` | Integer |  | 2 | `1` (Number), `2` (Number) |
| `set` | Array / Enum |  | 2 | `Recycled` (Enum) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `StatusOnSpawnIn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Integer |  | 2 | `1` (Number) |
| `SetHealth` | Integer |  | 2 | `100` (Number), `50` (Number) |


### Object: `StatusOnTakeHealthOrShieldDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Conditional_GoodRoll` | Object |  | 2 | `{ ... }` (Object) |
| `DivineShield` | Array / Integer |  |  | `[1 .33]` (Array), `[1 .5]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `Metronome` | Boolean (Flag) / Number / Object |  | 2 | `(Flag)` (Boolean (Flag)), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `StatusOverlappingCharactersAndDie`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer |  | 2 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |


### Object: `StatusRandomEnemiesOnBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer |  | 1 | `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer |  | 2 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `Confusion` | Array / Integer / Object |  | 2 | `[2 .15]` (Array), `[1 .1]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer |  | 4 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Freeze` | Array / Integer |  | 2 | `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |


### Object: `StatusWhenStatusCompletelyRemoved`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `UseAbility` | Enum / Object |  | 2 | `GirlDinoPoop` (Enum), `TormentorRuneAbsorb` (Enum), `{ ... }` (Object) |
| `status` | Enum |  | 2 | `BackflipWhenTargeted` (Enum) |


### Object: `Stealth`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_STEALTH_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_STEALTH_DESC"` (String) |


### Object: `StrengthForEachNeighboringEnemy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum |  |  | `StrengthUp` (Enum) |


### Object: `StrengthUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_STRUP_NAME"` (String) |
| `name_stacks_neg` | String |  |  | `"KEYWORD_STRDOWN_NAME"` (String) |
| `tooltip_stackless` | Enum |  |  | `none` (Enum) |
| `tooltip_stacks_neg` | String |  |  | `"KEYWORD_STRDOWN_DESC"` (String) |
| `tooltip_stacks_pos` | String |  |  | `"KEYWORD_STRUP_DESC"` (String) |


### Object: `StunImmunity`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean |  | 2 | `false` (Boolean) |


### Object: `SupportDieInsteadOfRun`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_dead_ani` | Enum |  | 2 | `off` (Enum) |
| `alt_dying_ani` | Enum |  | 2 | `shutdown` (Enum) |


### Object: `SupportFormChangeInsteadOfRun`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `TVChangeDie` (Enum), `SBotAnger` (Enum) |
| `wait_till_turn` | Boolean |  | 2 | `true` (Boolean) |


### Object: `SwimmingFormChange`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form_in` | Enum |  | 2 | `Water` (Enum) |
| `form_out` | Enum |  | 2 | `Out` (Enum) |


### Object: `SyncFormsWithBuddy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `no_buddy` | Enum |  | 2 | `Rage` (Enum) |


### Object: `T3HitlerSpawningPhase`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spell_use_groups` | Array |  |  | `[[ T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Tank...]` (Array) |


### Object: `TVBotScreen`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Die` | Integer / Object |  | 2 | `6` (Number), `1` (Number), `{ ... }` (Object) |
| `Dumb` | Integer / Object |  | 2 | `3` (Number), `{ ... }` (Object) |
| `Fuck` | Integer |  | 2 | `5` (Number) |
| `Obey` | Integer / Object |  | 2 | `1` (Number), `{ ... }` (Object) |
| `Shit` | Integer |  | 2 | `4` (Number) |
| `Stop` | Integer / Object |  | 2 | `2` (Number), `{ ... }` (Object) |


### Object: `Tech`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_TECH_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_TECH_DESC"` (String) |


### Object: `TempInitiativeChange`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_TEMPINIT_NAME"` (String) |
| `name_stacks_neg` | String |  |  | `"KEYWORD_TEMPINITDOWN_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_TEMPINIT_DESC"` (String) |
| `tooltip_stackless_neg` | String |  |  | `"KEYWORD_TEMPINITDOWN_DESC"` (String) |
| `tooltip_stacks_neg` | String |  |  | `"KEYWORD_TEMPINITDOWN_DESC"` (String) |


### Object: `Terminator2Run`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `move_ability` | Enum |  | 2 | `T2GoopRun` (Enum) |
| `move_weights` | Enum |  | 2 | `stay_far_always_move` (Enum) |


### Object: `TerminatorChase`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `T1ChokeReaction` (Enum) |
| `move` | Enum |  | 2 | `MoveOne` (Enum) |


### Object: `TerminatorSkin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `groups` | Array |  |  | `[{ stacks 48 ParticleBurst Gibs_terminatorskin CatPartsTransform { head 1057 }...]` (Array) |
| `status` | Enum |  | 2 | `Brace` (Enum) |


### Object: `Thorns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Tank` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_THORNS_DESC"` (String) |
| `name` | Enum |  |  | `"KEYWORD_THORNS_NAME"` (String), `"PASSIVE_THORNS_NAME"` (String) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_THORNS_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_THORNS_DESC"` (String) |


### Object: `TinkererBasicAttackSwitching`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `craft_ability` | Enum |  | 6 | `TinkererCraft` (Enum) |
| `throw_ability` | Enum |  | 6 | `TinkererThrow` (Enum) |


### Object: `TintItem`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `add` | Array / Integer |  |  | `[0.05 0.05 0.05]` (Array) |
| `ignore_if_str_aux_equals` | Enum |  | 2 | `ModelingClay_Default` (Enum) |
| `mul` | Array |  |  | `[0.45 0.3 0.25]` (Array) |


### Object: `Trample`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  |  | `153` (Number) |
| `name` | Enum |  |  | `"KEYWORD_TRAMPLE_NAME"` (String) |
| `tooltip` | Enum |  |  | `None` (Enum) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_TRAMPLE_DESC_STACKLESS"` (String) |


### Object: `TransformInXTurns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation` | Enum |  | 4 | `hatch` (Enum) |
| `initiative` | Enum / Integer |  | 8 | `keep_turns_end_turn` (Enum) |
| `name` | Enum |  |  | `"KEYWORD_TRANSFORM_NAME"` (String) |
| `object` | Array / Enum |  | 12 | `[YellowBlaster GreyAlien GreenProber Amoeba MoonWorm Waggle KirbyFetus BrainDrain Fetus FetusGusher]` (Array), `[Squirrel Crow Snake Turtle Toad Catepillar]` (Array), `HuskG` (Enum), `SkeletonCatRevivedFamiliar` (Enum) |
| `stacks` | Enum / Integer |  | 16 | `3` (Number), `1` (Number) |
| `tooltip` | Enum |  |  | `"KEYWORD_TRANSFORM_DESC"` (String) |
| `turns` | Array / Integer / Object |  |  | `[1 4]` (Array) |


### Object: `TransformItemOnElementInfluence`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum |  | 10 | `Fire` (Enum), `Greater_Water` (Enum) |
| `full_repair` | Boolean |  | 10 | `true` (Boolean) |
| `item` | Enum |  | 10 | `WaterBottle_Full` (Enum), `GallonOfWater` (Enum) |


### Object: `TransformOnDeathImmediately`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `first_turn` | Enum |  | 8 | `keep_turns` (Enum) |
| `obj` | Array / Enum |  | 8 | `TallSkeletonCatCorpse` (Enum), `SkeletonCatCorpseFamiliar` (Enum) |


### Object: `TransformOnElementInfluence`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum |  | 18 | `Holy` (Enum), `Fire` (Enum) |
| `object` | Array / Enum |  | 18 | `CookedBiggestFood` (Enum), `CookedBait` (Enum) |


### Object: `TransformOnElementInfluencex`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `element` | Array / Enum |  | 4 | `Holy` (Enum) |
| `object` | Array / Enum |  | 4 | `Bait` (Enum), `PurifiedPoisonFood` (Enum) |


### Object: `TransformOnStatusThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum |  | 2 | `Moth` (Enum) |
| `status` | Enum |  | 2 | `AllStatsUp` (Enum) |
| `threshold` | Enum / Integer / Object |  | 2 | `5` (Number) |


### Object: `Trapper`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 8 | `RattleSnakeTrap` (Enum), `BloatSideLaser` (Enum) |
| `cancel_movement` | Boolean |  | 4 | `false` (Boolean) |
| `pathfinding_avoidance` | Integer |  | 4 | `250` (Number) |
| `range` | Enum / Integer |  | 4 | `10` (Number) |


### Object: `Triskaidekaphobia`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `auto_plus_signs_on_name` | Boolean |  |  | `false` (Boolean) |
| `class` | Enum |  |  | `Disorder` (Enum) |
| `desc` | Enum |  |  | `"DISORDER_TRISKAIDEKAPHOBIA_DESC"` (String) |
| `name` | Enum |  |  | `"DISORDER_TRISKAIDEKAPHOBIA_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `TunnelVision`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | Number |  | 2 | `50` (Number) |


### Object: `TwisterFling`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation |  | 2 | `5` (Equation) |
| `max_dist` | Integer |  | 2 | `5` (Number) |
| `min_dist` | Integer |  | 2 | `3` (Number) |


### Object: `UnlimitedDeathRattleRevive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `MD_Lift` (Enum) |
| `even_if_stunned` | Boolean |  | 2 | `true` (Boolean) |


### Object: `UseAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 4 | `Destroyer2HolyAttack` (Enum), `T3Pebbles_BoulderDrop` (Enum) |
| `respect_prime` | Boolean |  | 4 | `true` (Boolean) |


### Object: `UseAbilityWhenOutOfStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum |  | 2 | `QueenHippoHeartAttack` (Enum) |
| `status` | Enum |  | 2 | `Brace` (Enum) |


### Object: `Vegan`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Disorder` (Enum) |
| `desc` | Enum |  |  | `"DISORDER_VEGAN_DESC"` (String) |
| `name` | Enum |  |  | `"DISORDER_VEGAN_NAME"` (String) |
| `name_mod` | String |  |  | `"CAT_NAME_MOD_VEGAN"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `Vengeful`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Fighter` (Enum) |
| `desc` | Enum |  |  | `"PASSIVE_VENGEFUL_DESC"` (String) |
| `name` | Enum |  |  | `"PASSIVE_VENGEFUL_NAME"` (String) |


### Object: `Weakness`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cost` | Object |  |  | `{ ... }` (Object) |
| `damage_instance` | Object |  |  | `{ ... }` (Object) |
| `graphics` | Object |  |  | `{ ... }` (Object) |
| `meta` | Object |  |  | `{ ... }` (Object) |
| `name` | Enum |  |  | `"KEYWORD_WEAKNESS_NAME"` (String) |
| `target` | Object |  |  | `{ ... }` (Object) |
| `template` | Enum |  |  | `targeted_status` (Enum) |
| `tooltip_stackless` | String |  |  | `"KEYWORD_WEAKNESS_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String |  |  | `"KEYWORD_WEAKNESS_DESC"` (String) |
| `tooltip_stacks_singular` | String |  |  | `"KEYWORD_WEAKNESS_DESC_SINGULAR"` (String) |


### Object: `WobblyCat`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum |  |  | `Disorder` (Enum) |
| `desc` | Enum |  |  | `"DISORDER_WOBBLYCATSYNDROME_DESC"` (String) |
| `name` | Enum |  |  | `"DISORDER_WOBBLYCATSYNDROME_NAME"` (String) |
| `passives` | Object |  |  | `{ ... }` (Object) |
| `stats` | Object |  |  | `{ ... }` (Object) |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |


### Object: `Zombie`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum |  |  | `"KEYWORD_ZOMBIE_NAME"` (String) |
| `tooltip` | Enum |  |  | `"KEYWORD_ZOMBIE_DESC"` (String) |

