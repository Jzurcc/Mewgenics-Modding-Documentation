# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Items & Equipment

> **Associated Files:** `data/items/, data/item_setbonuses.gon`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1116

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | Enum | Localization key for the item's desc. | 5441 |  |
| [`name`](./Strings.md#string-name) | Enum | Localization key for the item's name. | 5027 |  |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum |  | 2364 |  |
| `frame` | Integer |  | 2212 |  |
| [`kind`](./Enums.md#enum-kind) | Enum |  | 2212 |  |
| [`rarity`](./Enums.md#enum-rarity) | Enum |  | 1934 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1570 |  |
| [`set`](./Enums.md#enum-set) | Array / Enum |  | 1504 |  |
| [`Set`](./Enums.md#enum-set) | Enum | Applies or references the 'Set' effect/state. | 1504 |  |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 730 |  |
| `cha` | Enum / Integer |  | 468 |  |
| `spd` | Enum / Integer |  | 424 |  |
| `shield` | Enum / Integer |  | 422 |  |
| `con` | Enum / Integer |  | 416 |  |
| `int` | Enum / Integer |  | 401 |  |
| `lck` | Enum / Integer |  | 351 |  |
| [`str`](./Engine_DamagingKeys.md#valid-property-keys) | Mixed |  | 337 |  |
| `dex` | Enum / Integer |  | 301 |  |
| `durability` | Array / Integer | Maximum uses before breaking. | 264 |  |
| `cursed` | Boolean |  | 154 |  |
| `consumable` | Boolean |  | 140 |  |
| `parasite` | Boolean |  | 102 |  |
| `aux` | Integer |  | 82 |  |
| `quest_item` | Boolean |  | 80 |  |
| [`keyword_tooltips`](./Items_and_Equipment.md#context-keyword_tooltips) | Object | Forces specific UI tooltips to appear when hovering over the ability. | 62 |  |
| `divine_shield` | Integer |  | 54 |  |
| [`quest_reward_item`](./Enums.md#enum-quest_reward_item) | Enum |  | 44 |  |
| `indestructible` | Boolean |  | 40 |  |
| `legacy_quest` | Boolean |  | 34 |  |
| [`hint_destination`](./Enums.md#enum-hint_destination) | Enum |  | 32 |  |
| [`str_aux_initialize`](./Enums.md#enum-str_aux_initialize) | Enum |  | 30 |  |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 26 |  |
| `dont_destroy_on_0` | Boolean |  | 26 |  |
| `max_durability` | Integer |  | 22 |  |
| [`on_store`](./Enums.md#enum-on_store) | Enum |  | 16 |  |
| [`global_tags`](./Arrays.md#array-global_tags) | Array |  | 12 |  |
| [`hint_prerequisite_flag`](./Enums.md#enum-hint_prerequisite_flag) | Enum |  | 10 |  |
| `failable` | Boolean |  | 8 |  |
| [`global_passives`](./Items_and_Equipment.md#context-global_passives) | Object |  | 8 |  |
| `randomize_piece_frames` | Boolean |  | 8 |  |
| `str_aux_is_copy_passive` | Boolean |  | 8 |  |
| `fragile` | Boolean |  | 6 |  |
| [`icon_hint`](./Enums.md#enum-icon_hint) | Enum |  | 6 |  |
| `max_health` | Integer |  | 6 |  |
| `reset_aux_on_store` | Integer |  | 6 |  |
| `speed` | Array / Number |  | 6 |  |
| `sticky` | Boolean |  | 6 |  |
| `weightless` | Boolean |  | 6 |  |
| [`passive`](./Items_and_Equipment.md#context-passive) | Object |  | 4 |  |
| `prevent_level_up` | Boolean |  | 4 |  |
| [`quest_item_alias`](./Enums.md#enum-quest_item_alias) | Enum |  | 4 |  |
| [`str_aux_is_copy_ability`](./Items_and_Equipment.md#context-str_aux_is_copy_ability) | Object |  | 4 |  |
| `str_aux_is_copy_item_passive` | Boolean |  | 4 |  |
| `aux_is_catid` | Boolean |  | 2 |  |
| `cant_equip_to_colorless` | Boolean |  | 2 |  |
| `degrade_after_adventure` | Boolean |  | 2 |  |
| [`equip_sound`](./Enums.md#enum-equip_sound) | Enum |  | 2 |  |
| `force_sticky` | Boolean |  | 2 |  |
| [`reset_str_aux_on_store`](./Enums.md#enum-reset_str_aux_on_store) | Enum |  | 2 |  |
| [`str_aux`](./Enums.md#enum-str_aux) | Enum |  | 2 |  |
| `str_aux_is_copy_item_active` | Boolean |  | 2 |  |
| `str_aux_is_copy_item_icon` | Boolean |  | 2 |  |
| [`passives`](./Enums.md) | Object | | 750 |   |

</details>

---

### Object: `passives`


**Definition:** Object listing intrinsic passive modifiers.  
**Total Count:** 748


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAfterXKills`](./Items_and_Equipment.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Items_and_Equipment.md#context-passiveathealththreshold), [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold), [`PassiveIfStrAuxEquals`](./Items_and_Equipment.md#context-passiveifstrauxequals), [`PassiveWhenAffectedByElement`](./Items_and_Equipment.md#context-passivewhenaffectedbyelement), [`PassiveWhenOnTile`](./Items_and_Equipment.md#context-passivewhenontile), [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2827 |  |
| [`AIControlNextTurn`](./Enums.md) | Object | | 1 |   |
| [`AOEBonus`](./Enums.md) | Integer | | 1 | 1 |
| [`AbilityHealthThreshold`](./Enums.md) | Object | | 1 |   |
| [`AbilityOnBattleStart`](./Enums.md) | Enum | | 7 | head_SpiderInjector |
| [`AbilityOnRoundEndOnce`](./Enums.md) | Object | | 1 |   |
| [`AbilityReaction`](./Enums.md) | Enum | | 1 | head_EmoSong |
| [`AddAdvantageToEvent`](./Enums.md) | Object | | 1 |   |
| [`AddBonusMeleeRange`](./Enums.md) | Integer | | 3 | 1 |
| [`AddBonusRange`](./Enums.md) | Integer | | 11 | 2 |
| [`AddCorpseHealth`](./Enums.md) | Integer | | 6 | 6 |
| [`AddCritMultiplier`](./Enums.md) | Integer | | 1 | 33 |
| [`AddDamageToElementDamage`](./Enums.md) | Object | | 4 |   |
| [`AddElementsToBasicAttack`](./Enums.md) | Enum | | 1 | Holy |
| [`AddEndOfCombatRegen`](./Enums.md) | Integer | | 3 | 999999 |
| [`AddHiddenTag`](./Enums.md) | Enum | | 1 | the_nuke_bearer |
| [`AddInitiative`](./Enums.md) | Integer | | 2 | -20 |
| [`AddKnockbackDamage`](./Enums.md) | Integer | | 2 | 1 |
| [`AddLevelUpRerolls`](./Enums.md) | Integer | | 6 | 3 |
| [`AddManaRegen`](./Enums.md) | Integer | | 7 | 2 |
| [`AddPassivesToCharmed`](./Enums.md) | Object | | 1 |   |
| [`AddPassivesToMinions`](./Enums.md) | Object | | 4 |   |
| [`AddSelfStatusToBasicAttack`](./Enums.md) | Object | | 8 |   |
| [`AddSelfStatusToWeapons`](./Enums.md) | Object | | 1 |   |
| [`AddStatusToAllDamage`](./Enums.md) | Object | | 6 |   |
| [`AddStatusToBackstabs`](./Enums.md) | Object | | 1 |   |
| [`AddStatusToBasicAttack`](./Enums.md) | Object | | 65 |   |
| [`AddStatusToElementDamage`](./Enums.md) | Object | | 2 |   |
| [`AddStatusToKnockbackDamage`](./Enums.md) | Object | | 2 |   |
| [`AddStatusToSpells`](./Enums.md) | Object | | 2 |   |
| [`AddStatusToWeapons`](./Enums.md) | Object | | 1 |   |
| [`AddTag`](./Enums.md) | Enum | | 4 | rock |
| [`AddTemporaryEffectsToBasicAttack`](./Enums.md) | Object | | 1 |   |
| [`AllSpellsCostCharge`](./Enums.md) | Integer | | 1 | 1 |
| [`AllStatsUp`](./Enums.md) | Integer | | 12 | -2 |
| [`AllStatsUpPerDisorder`](./Enums.md) | Integer | | 3 | 1 |
| [`AllUnitsExplodeOnDeath`](./Enums.md) | Integer | | 1 | 5 |
| [`AlliesScrambleSpellAfterCast`](./Enums.md) | Integer | | 1 | 1 |
| [`AlluringDoodieEater`](./Enums.md) | Object | | 1 |   |
| [`AllyDamageReduction`](./Enums.md) | Integer | | 1 | 0 |
| [`AllyDodgeChanceAura`](./Enums.md) | Object | | 1 |   |
| [`AlphaAllStatsUp`](./Enums.md) | Integer | | 1 | 1 |
| [`AlphaCat`](./Enums.md) | Integer | | 2 | 1 |
| [`AlphaTurns`](./Enums.md) | Integer | | 3 | -1 |
| [`AlwaysChosenForLevelUp`](./Enums.md) | Integer | | 1 | 1 |
| [`AmplifyKnockback`](./Enums.md) | Integer | | 2 | 2 |
| [`AmplifyStatus`](./Enums.md) | Enum | | 4 | Poison |
| [`ApplyStatusesToRandomEnemiesEachTurn`](./Enums.md) | Object | | 2 |   |
| [`ArmorBreakOnHit`](./Enums.md) | Object | | 2 |   |
| [`ArmorDodgeChance`](./Enums.md) | Integer | | 17 | 5 |
| [`AutoEquipConsumables`](./Enums.md) | Integer | | 1 | 1 |
| [`BackflipWhenTargeted`](./Enums.md) | Enum / Object | | 2 | X |
| [`BackstabCritChance`](./Enums.md) | Number | | 1 | .25 |
| [`BalanceStats`](./Enums.md) | Integer | | 1 | 1 |
| [`BasicAttackCantMiss`](./Enums.md) | Integer | | 1 | 1 |
| [`BasicAttackCritChance`](./Enums.md) | Number | | 1 | .1 |
| [`Bleed`](./Enums.md) | Integer | | 20 | 3 |
| [`BleedThorns`](./Enums.md) | Integer | | 9 | 3 |
| [`Blind`](./Enums.md) | Integer | | 3 | -1 |
| [`BlockDamageUnderThreshold`](./Enums.md) | Integer | | 1 | 1 |
| [`BlockNegativeStatus`](./Enums.md) | Integer | | 1 | 30 |
| [`BoneArmorPassive`](./Enums.md) | Integer | | 3 | 1 |
| [`BonusAbility`](./Enums.md) | Enum | | 2 | neck_NukeBonus |
| [`BoostHeals`](./Enums.md) | Integer | | 5 | 2 |
| [`BoostReceivedHealing`](./Enums.md) | Integer | | 1 | 2 |
| [`BoostWeaponDamage`](./Enums.md) | Object | | 2 |   |
| [`BouncyProjectiles`](./Enums.md) | Object | | 1 |   |
| [`Brace`](./Enums.md) | Enum / Integer | | 52 | 2 |
| [`BreakAtAux`](./Enums.md) | Integer | | 4 | 0 |
| [`BreakOnElement`](./Enums.md) | Enum | | 3 | water |
| [`BreakWhenNoShield`](./Enums.md) | Integer | | 2 | 1 |
| [`Brittle`](./Enums.md) | Integer | | 24 | 1 |
| [`BrittleDuringElement`](./Enums.md) | Enum | | 7 | water |
| [`Bruise`](./Enums.md) | Integer | | 18 | 2 |
| [`BuffImmunity`](./Enums.md) | Object | | 1 |   |
| [`Burn`](./Enums.md) | Integer | | 16 | 2 |
| [`CanLevelUpWhenDead`](./Enums.md) | Integer | | 2 | 1 |
| [`CanRemoveCursedItems`](./Enums.md) | Integer | | 1 | 1 |
| [`CantCatchDiseases`](./Enums.md) | Integer | | 3 | 1 |
| [`CantSpreadDiseases`](./Enums.md) | Integer | | 3 | 1 |
| [`CapBasicAttackDamage`](./Enums.md) | Integer | | 1 | 1 |
| [`CapMovementAbilityRange`](./Enums.md) | Integer | | 1 | 1 |
| [`CatPartsSizeScale`](./Enums.md) | Object | | 1 |   |
| [`CatchProjectiles`](./Enums.md) | Object | | 3 |   |
| [`ChanceToAmbush`](./Enums.md) | Integer | | 1 | 25 |
| [`ChanceToBackflip`](./Enums.md) | Object | | 2 |   |
| [`ChanceToBlock`](./Enums.md) | Integer | | 3 | 10 |
| [`ChanceToBlockAndCounter`](./Enums.md) | Integer / Object | | 2 | 25 |
| [`ChanceToForceEvent`](./Enums.md) | Object | | 1 |   |
| [`ChanceToRevive`](./Enums.md) | Integer / Object | | 4 | 100 |
| [`Charge`](./Enums.md) | Integer | | 18 | 2 |
| [`CharismaIsMaxStat`](./Enums.md) | Integer | | 1 | 1 |
| [`CharmImmunity`](./Enums.md) | Integer | | 1 | 1 |
| [`ClassManaCostReduction`](./Enums.md) | Object | | 3 |   |
| [`Confusion`](./Enums.md) | Integer | | 8 | 2 |
| [`ConsumableEffectsMultiplierBonus`](./Enums.md) | Integer | | 1 | 1 |
| [`ConvertDamageToScaledStatus`](./Enums.md) | Object | | 1 |   |
| [`CopyPassiveSlot`](./Enums.md) | Integer | | 3 | 0 |
| [`CounterAttack`](./Enums.md) | Object | | 3 |   |
| [`CounterNextAttacks`](./Enums.md) | Integer | | 1 | 2 |
| [`CreateGlobalModifiers`](./Enums.md) | Object | | 2 |   |
| [`CritChanceUp`](./Enums.md) | Integer | | 6 | 20 |
| [`CritsApplyStatus`](./Enums.md) | Object | | 1 |   |
| [`DamageUp`](./Enums.md) | Integer | | 23 | 2 |
| [`DeathRattle`](./Enums.md) | Enum | | 1 | neck_NukeExplode |
| [`DeathRattleRevive`](./Enums.md) | Enum | | 2 | tk_PetrifiedPinky |
| [`DebuffImmunity`](./Enums.md) | Integer | | 1 | 1 |
| [`DelayedAutoRevive`](./Enums.md) | Object | | 4 |   |
| [`DepressionAura`](./Enums.md) | Integer | | 4 | 2 |
| [`DisableAbilities`](./Enums.md) | Enum | | 3 | all_items |
| [`DisablePassiveSlot`](./Enums.md) | Integer | | 2 | 0 |
| [`DodgeChance`](./Enums.md) | Integer | | 2 | 25 |
| [`DodgeChance_Status`](./Enums.md) | Integer | | 6 | 2 |
| [`DoubleCastSpellIfManaCostUnderThreshold`](./Enums.md) | Integer | | 1 | 3 |
| [`DoubleCastTaggedSpells`](./Enums.md) | Enum | | 1 | musical |
| [`DoubleCastWeapons`](./Enums.md) | Integer | | 1 | 1 |
| [`DoubleReceivedNegativeStatus`](./Enums.md) | Integer | | 1 | 1 |
| [`DoubleReceivedPositiveStatus`](./Enums.md) | Integer | | 1 | 1 |
| [`DropAsFamiliarOnArmorBreak`](./Enums.md) | Enum | | 3 | FaceGrubFamiliar |
| [`DropAsFamiliarOnTookDamage`](./Enums.md) | Enum | | 1 | PhantomMaskRock |
| [`DropSoulJarOnDeath`](./Enums.md) | Enum | | 1 | SoulJar_Full |
| [`DurabilityTransform`](./Enums.md) | Object | | 7 |   |
| [`ElementImmune`](./Enums.md) | Enum | | 5 | Ice |
| [`ElementalManaCostReduction`](./Enums.md) | Object | | 2 |   |
| [`Eternal`](./Enums.md) | Object | | 1 |   |
| [`ExcludeFromEvents`](./Enums.md) | Enum | | 1 | Tragedy |
| [`ExplosionImmunity`](./Enums.md) | Integer | | 1 | 1 |
| [`ExtraBasicAttacks`](./Enums.md) | Integer | | 4 | 2 |
| [`ExtraBasicAttacks_Status`](./Enums.md) | Integer | | 1 | 1 |
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer | | 2 | 1 |
| [`ExtraMovePoints`](./Enums.md) | Integer | | 1 | 1 |
| [`ExtraStatusWhenDealingDamage`](./Enums.md) | Object | | 3 |   |
| [`ExtraTrinketUses`](./Enums.md) | Integer | | 1 | 10 |
| [`ExtraWeaponAttacks`](./Enums.md) | Integer | | 4 | 2 |
| [`FaceArmorPassiveMultiplierBonus`](./Enums.md) | Integer | | 3 | 2 |
| [`FaceShield`](./Enums.md) | Integer | | 1 | 1 |
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md) | Enum | | 1 | combat_reward_easy |
| [`Flammable`](./Enums.md) | Integer | | 13 | 2 |
| [`FlowersOnEndTurn`](./Enums.md) | Integer | | 1 | 1 |
| [`FlyDamageIncrease`](./Enums.md) | Object | | 1 |   |
| [`Flying`](./Enums.md) | Integer | | 2 | 1 |
| [`Fragile`](./Enums.md) | Integer | | 22 | 1 |
| [`FragileDuringElement`](./Enums.md) | Enum | | 4 | water |
| [`FrankBolts`](./Enums.md) | Integer | | 2 | 1 |
| [`FreezePiercing`](./Enums.md) | Integer | | 1 | 1 |
| [`GainExtraShield`](./Enums.md) | Integer | | 1 | 4 |
| [`GlobalMeleeRevengeDamage`](./Enums.md) | Object | | 1 |   |
| [`HPGainBlock`](./Enums.md) | Integer | | 1 | 1 |
| [`HeadArmorPassiveMultiplierBonus`](./Enums.md) | Integer | | 3 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer | | 42 | 2 |
| [`HideSomeHudStuff`](./Enums.md) | Integer | | 1 | 1 |
| [`IgnoreTiles`](./Enums.md) | Integer | | 1 | 1 |
| [`IncreaseExplosionDamage`](./Enums.md) | Integer | | 2 | 2 |
| [`IncreaseExplosionSize`](./Enums.md) | Integer | | 3 | 7 |
| [`IncreaseSpellRange`](./Enums.md) | Integer | | 1 | 2 |
| [`InjuryImmunity`](./Enums.md) | Integer | | 2 | 1 |
| [`InnateElement`](./Enums.md) | Enum | | 1 | Ice |
| [`ItemAuxTransform`](./Enums.md) | Object | | 6 |   |
| [`JesterLevelUpRerolls`](./Enums.md) | Integer | | 1 | 1 |
| [`KillsToMeat`](./Enums.md) | Enum | | 2 | Food |
| [`KineticSpikes`](./Enums.md) | Integer | | 8 | 3 |
| [`KnockbackImmunity`](./Enums.md) | Integer | | 1 | 1 |
| [`LeaveBehindOnceEachMove`](./Enums.md) | Enum | | 2 | Scrap |
| [`LevelUpClassOverride`](./Enums.md) | Enum | | 2 | Jester |
| [`Lifesteal`](./Enums.md) | Integer | | 1 | 1 |
| [`LuckUp`](./Enums.md) | Integer | | 4 | 2 |
| [`MakeBasicAttackPull`](./Enums.md) | Integer | | 1 | 1 |
| [`MakeSpellsRequireCharge`](./Enums.md) | Integer | | 1 | 1 |
| [`ManaCostReduction`](./Enums.md) | Integer | | 7 | -2 |
| [`MeleeRevengeDamage`](./Enums.md) | Object | | 32 |   |
| [`Metal`](./Enums.md) | Integer | | 91 | 1 |
| [`MissChance`](./Enums.md) | Integer | | 4 | 10 |
| [`ModelingClayPassive`](./Enums.md) | Integer | | 1 | 1 |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md) | Enum | | 1 | face_EatNeverstone |
| [`MoveQuivered`](./Enums.md) | Integer | | 2 | 2 |
| [`MoveSpeedMultiplier`](./Enums.md) | Number | | 1 | .5 |
| [`MoveTowardsDamageSource`](./Enums.md) | Enum | | 1 | MoveOne |
| [`MovementReaction`](./Enums.md) | Object | | 2 |   |
| [`MultiplyCoinsOnBattleStart`](./Enums.md) | Integer | | 1 | 2 |
| [`MultiplyReceivedHealing`](./Enums.md) | Integer | | 1 | 2 |
| [`NeckArmorPassiveMultiplierBonus`](./Enums.md) | Integer | | 2 | 1 |
| [`ObjectDetector`](./Enums.md) | Object | | 1 |   |
| [`OverrideBasicAttack`](./Enums.md) | Enum | | 5 | IsaacBasicAttack |
| [`PassiveAfterXKills`](./Enums.md) | Object | | 1 |   |
| [`PassiveAtHealthThreshold`](./Enums.md) | Object | | 4 |   |
| [`PassiveAtStatThreshold`](./Enums.md) | Object | | 2 |   |
| [`PassiveIfStrAuxEquals`](./Enums.md) | Object | | 7 |   |
| [`PassiveIfWeaponIsUsable`](./Enums.md) | Object | | 2 |   |
| [`PassiveWhenAffectedByElement`](./Enums.md) | Object | | 1 |   |
| [`PassiveWhenDead`](./Enums.md) | Object | | 3 |   |
| [`PassiveWhenOnTile`](./Enums.md) | Object | | 6 |   |
| [`PassiveWhileHasDurability`](./Enums.md) | Object | | 1 |   |
| [`PassiveWhileInMonkMeleeStance`](./Enums.md) | Object | | 1 |   |
| [`PassiveWhileShielded`](./Enums.md) | Object | | 1 |   |
| [`PermanentMadness`](./Enums.md) | Integer | | 2 | 1 |
| [`PhysicalAttacksMiss`](./Enums.md) | Integer | | 1 | 1 |
| [`Poison`](./Enums.md) | Integer | | 18 | 2 |
| [`PoisonThorns`](./Enums.md) | Integer | | 5 | 1 |
| [`PoopWhenHit`](./Enums.md) | Object | | 1 |   |
| [`PreventSpecificInjury`](./Enums.md) | Enum | | 1 | int |
| [`Quivered`](./Enums.md) | Array / Integer | | 8 | [.10] |
| [`RandomSeededStatModifier`](./Enums.md) | Array | | 4 | [2] |
| [`RangedTrueShot`](./Enums.md) | Integer | | 2 | 1 |
| [`ReclaimItemOnBreak`](./Enums.md) | Integer | | 1 | 1 |
| [`ReduceManaCost`](./Enums.md) | Integer | | 2 | 2 |
| [`ReduceSpellCostsPerDisorder`](./Enums.md) | Integer | | 1 | 1 |
| [`ReduceSpellCostsPerParasite`](./Enums.md) | Integer | | 1 | 1 |
| [`ReflectProjectiles`](./Enums.md) | Integer | | 2 | 20 |
| [`RefreshEquipmentAbilityOnElement`](./Enums.md) | Object | | 2 |   |
| [`RemoveLineOfSightRestrictions`](./Enums.md) | Integer | | 1 | 1 |
| [`ReplaceBasicAttack`](./Enums.md) | Enum | | 2 | BasicPoke |
| [`ReplaceBasicMove`](./Enums.md) | Enum | | 5 | head_HeadBrandJump |
| [`ReplaceBlankTilesOnBattleStart`](./Enums.md) | Enum | | 1 | GlassTile |
| [`ReplaceSpawnedObjects`](./Enums.md) | Array | | 2 | [Poop] |
| [`RerollItemsOnBattleEnd`](./Enums.md) | Integer | | 1 | 1 |
| [`RevengeDamage`](./Enums.md) | Object | | 9 |   |
| [`RockyArmorPassive`](./Enums.md) | Integer | | 3 | 1 |
| [`ScaldingOrbMoonBossOneShot`](./Enums.md) | Object | | 1 |   |
| [`ScaledStatusAlliesOnSpendMana`](./Enums.md) | Object | | 1 |   |
| [`ScaledStatusOnHolyShieldBlock`](./Enums.md) | Object | | 1 |   |
| [`ScaledStatusOnSpendMana`](./Enums.md) | Object | | 1 |   |
| [`SetBrittleImmune`](./Enums.md) | Variable | | 1 |   |
| [`SetDefaultFacePassive`](./Enums.md) | Enum | | 2 | euphoric |
| [`SetFaction`](./Enums.md) | Enum | | 1 | enemies |
| [`SetFragileImmune`](./Enums.md) | Variable | | 1 |   |
| [`SetSpellCosts`](./Enums.md) | Integer | | 1 | 0 |
| [`SharkySmellsBlood`](./Enums.md) | Integer | | 1 | 1 |
| [`SpawnCatCloneOnCorpsePopped`](./Enums.md) | Integer | | 1 | 1 |
| [`SpawnEachTurn`](./Enums.md) | Object | | 10 |   |
| [`SpawnExtraThingsOnBattleStart`](./Enums.md) | Object | | 3 |   |
| [`SpawnItemLinkedFamiliar`](./Enums.md) | Object | | 2 |   |
| [`SpawnNearEnemies`](./Enums.md) | Integer | | 2 | 1 |
| [`SpawnObjectOnPopCorpse`](./Enums.md) | Enum / Object | | 4 | Coin |
| [`SpawnOnBattleStart`](./Enums.md) | Enum / Object | | 21 | BuffCharmedKitten |
| [`SpawnOnBattleStartRandomEmptyTile`](./Enums.md) | Object | | 3 |   |
| [`SpawnOnDeath`](./Enums.md) | Object | | 1 |   |
| [`SpawnOnDowned`](./Enums.md) | Enum | | 1 | CharmedSpookie |
| [`SpawnRandomPickupsOnTaggedUnitKilled`](./Enums.md) | Object | | 1 |   |
| [`SpawnThingOnDamage`](./Enums.md) | Object | | 11 |   |
| [`SpawnThingOnDeath`](./Enums.md) | Enum | | 9 | CharmedTinyTumor |
| [`SpellDamageUp`](./Enums.md) | Integer | | 8 | 3 |
| [`StackingFlowerTrail`](./Enums.md) | Object | | 3 |   |
| [`StatDependentPassive`](./Enums.md) | Object | | 1 |   |
| [`StatusAdjacentOnTheirTurnEnd`](./Enums.md) | Object | | 1 |   |
| [`StatusAfterCastSpell`](./Enums.md) | Object | | 2 |   |
| [`StatusAfterXTurns`](./Enums.md) | Object | | 1 |   |
| [`StatusAllCharactersOnSpawn`](./Enums.md) | Object | | 3 |   |
| [`StatusAlliesEachTurn`](./Enums.md) | Object | | 1 |   |
| [`StatusAlliesOnBattleStart`](./Enums.md) | Object | | 6 |   |
| [`StatusAlliesOnDeath`](./Enums.md) | Object | | 1 |   |
| [`StatusEachTurnBegin`](./Enums.md) | Object | | 10 |   |
| [`StatusEachTurnEnd`](./Enums.md) | Object | | 22 |   |
| [`StatusEachTurnEndForEachTurn`](./Enums.md) | Object | | 1 |   |
| [`StatusEveryXSpellCasts`](./Enums.md) | Object | | 3 |   |
| [`StatusIfUnusedActPoints`](./Enums.md) | Object | | 2 |   |
| [`StatusIfUnusedMovePoints`](./Enums.md) | Object | | 1 |   |
| [`StatusImmunity`](./Enums.md) | Array / Enum | | 9 | [Confusion] |
| [`StatusOnAllyCatDeath`](./Enums.md) | Object | | 2 |   |
| [`StatusOnBackstab`](./Enums.md) | Object | | 2 |   |
| [`StatusOnBattleEnd`](./Enums.md) | Object | | 25 |   |
| [`StatusOnBattleStart`](./Enums.md) | Object | | 13 |   |
| [`StatusOnBreak`](./Enums.md) | Object | | 22 |   |
| [`StatusOnBreakItem`](./Enums.md) | Object | | 2 |   |
| [`StatusOnCastSpell`](./Enums.md) | Object | | 2 |   |
| [`StatusOnCollectPickup`](./Enums.md) | Object | | 1 |   |
| [`StatusOnDie`](./Enums.md) | Object | | 6 |   |
| [`StatusOnDodge`](./Enums.md) | Object | | 1 |   |
| [`StatusOnEatFood`](./Enums.md) | Object | | 1 |   |
| [`StatusOnEndMove`](./Enums.md) | Object | | 5 |   |
| [`StatusOnEnemyDeath`](./Enums.md) | Object | | 1 |   |
| [`StatusOnFallAsleep`](./Enums.md) | Object | | 1 |   |
| [`StatusOnFullMana`](./Enums.md) | Object | | 1 |   |
| [`StatusOnGainCoins`](./Enums.md) | Object | | 2 |   |
| [`StatusOnHealed`](./Enums.md) | Object | | 1 |   |
| [`StatusOnKill`](./Enums.md) | Object | | 16 |   |
| [`StatusOnKillEnemy`](./Enums.md) | Object | | 7 |   |
| [`StatusOnPickupCoins`](./Enums.md) | Object | | 1 |   |
| [`StatusOnPopCorpse`](./Enums.md) | Object | | 3 |   |
| [`StatusOnTakeHealthOrShieldDamage`](./Enums.md) | Object | | 4 |   |
| [`StatusOnTookDamage`](./Enums.md) | Object | | 16 |   |
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](./Enums.md) | Object | | 3 |   |
| [`StatusOnUseBasicAttack`](./Enums.md) | Object | | 1 |   |
| [`StatusRandomEnemiesOnBattleStart`](./Enums.md) | Object | | 4 |   |
| [`StatusWhenAllySpendsMana`](./Enums.md) | Object | | 1 |   |
| [`StevenBolts`](./Enums.md) | Integer | | 1 | 1 |
| [`StripKnockback`](./Enums.md) | Integer | | 1 | 1 |
| [`TauntAlways`](./Enums.md) | Integer | | 1 | 1 |
| [`Thorns`](./Enums.md) | Integer | | 46 | 2 |
| [`TintItem`](./Enums.md) | Object | | 1 |   |
| [`Trample`](./Enums.md) | Integer | | 5 | 3 |
| [`TransformItemOnElementInfluence`](./Enums.md) | Object | | 5 |   |
| [`TrinketActiveEffectsMultiplierBonus`](./Enums.md) | Integer | | 2 | 2 |
| [`TrinketPassiveMultiplierBonus`](./Enums.md) | Integer | | 5 | 2 |
| [`TrueShot`](./Enums.md) | Integer | | 3 | 1 |
| [`TunnelVision`](./Enums.md) | Object | | 1 |   |
| [`Uncontrollable`](./Enums.md) | Integer | | 3 | 1 |
| [`Undead`](./Enums.md) | Integer | | 1 | 1 |
| [`WeaponDamageMultiplierBonus`](./Enums.md) | Integer | | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AddStatusToBasicAttack`


**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 65


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Items_and_Equipment.md#context-addpassivestominions), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 187 |  |
| [`ApplyToSource`](./Enums.md) | Object | | 6 |   |
| [`Bleed`](./Enums.md) | Integer | | 20 | 3 |
| [`Blind`](./Enums.md) | Integer | | 3 | -1 |
| [`Bruise`](./Enums.md) | Integer | | 18 | 2 |
| [`Burn`](./Enums.md) | Integer | | 16 | 2 |
| [`ChangeTile`](./Enums.md) | Enum | | 3 | GlassTile |
| [`Conditional_GoodRoll`](./Enums.md) | Object | | 17 |   |
| [`Confusion`](./Enums.md) | Integer | | 8 | 2 |
| [`DamageOrHealConditionally`](./Enums.md) | Integer | | 2 | 1 |
| [`Fear`](./Enums.md) | Array / Integer | | 11 | [.15] |
| [`ForceUseAbilityOnTarget`](./Enums.md) | Object | | 1 |   |
| [`Freeze`](./Enums.md) | Array / Integer | | 14 | [.1] |
| [`KnockOutCoin`](./Enums.md) | Integer | | 1 | 1 |
| [`KnockUpAndAway`](./Enums.md) | Object | | 1 |   |
| [`Knockback`](./Enums.md) | Integer | | 10 | 2 |
| [`Leech`](./Enums.md) | Integer | | 8 | 1 |
| [`Leeches`](./Enums.md) | Integer | | 2 | 1 |
| [`MagicWeakness`](./Enums.md) | Integer | | 1 | 1 |
| [`ManaLeeches`](./Enums.md) | Integer | | 1 | 1 |
| [`Marked`](./Enums.md) | Integer | | 2 | 1 |
| [`OverrideChainKnockback`](./Enums.md) | Integer | | 2 | 0 |
| [`Poison`](./Enums.md) | Integer | | 18 | 2 |
| [`PullSourceToTarget`](./Enums.md) | Integer | | 1 | 1 |
| [`Rot`](./Enums.md) | Integer | | 3 | 1 |
| [`Slow`](./Enums.md) | Integer | | 12 | 1 |
| [`SoulLink`](./Enums.md) | Integer | | 1 | 1 |
| [`SpiderInfested`](./Enums.md) | Integer | | 2 | 1 |
| [`Stun`](./Enums.md) | Array | | 5 | [.1] |
| [`Tangled`](./Enums.md) | Array | | 4 | [.05] |
| [`Weakness`](./Enums.md) | Integer | | 2 | 3 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 37


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend), [`StatusOnKill`](./Items_and_Equipment.md#context-statusonkill), [`StatusOnTakeHealthOrShieldDamage`](./Items_and_Equipment.md#context-statusontakehealthorshielddamage), [`effects`](./Items_and_Equipment.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 72 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 40 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 30 |  |
| [`ForceUseAbility_NonStack`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ForceUseAbility_NonStack' effect/state. | 8 |  |
| `DestroyTrinket` | `Number` | Applies or references the 'DestroyTrinket' effect/state. | 2 |  |
| [`FindItemFromPool`](./Enums.md) | Enum | | 10 | consumables |
| [`ForceUseAbility`](./Enums.md) | Enum | | 14 | tk_SuckStone |
| [`Freeze`](./Enums.md) | Array / Integer | | 14 | [.1] |
| [`RandomMutation`](./Enums.md) | Integer | | 7 | 1 |

</details>

---

### Object: `effects`


**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 35


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](./Items_and_Equipment.md#context-dodamage), [`MeleeRevengeDamage`](./Items_and_Equipment.md#context-meleerevengedamage), [`RevengeDamage`](./Items_and_Equipment.md#context-revengedamage), [`damage_instance`](./Items_and_Equipment.md#context-damage_instance)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1888 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1390 |  |
| [`VisualFXTile`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'VisualFXTile' effect/state. | 72 |  |
| [`BounceObject`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Spawns a physics object that visually bounces off the target. | 70 |  |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#object-conditional-goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 28 |  |
| [`VisualFX`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'VisualFX' effect/state. | 20 |  |
| `DestroyTrinket` | Integer | Applies or references the 'DestroyTrinket' effect/state. | 6 |  |
| [`Blind`](./Enums.md) | Integer | | 3 | -1 |
| [`Bruise`](./Enums.md) | Integer | | 18 | 2 |
| [`Burn`](./Enums.md) | Integer | | 16 | 2 |
| [`Cleave`](./Enums.md) | Integer | | 1 | 1 |
| [`Confusion`](./Enums.md) | Integer | | 8 | 2 |
| [`Fear`](./Enums.md) | Array / Integer | | 11 | [.15] |
| [`Freeze`](./Enums.md) | Array / Integer | | 14 | [.1] |
| [`Grappled`](./Enums.md) | Array | | 4 | [.50] |
| [`Immobile`](./Enums.md) | Integer | | 4 | 1 |
| [`Poison`](./Enums.md) | Integer | | 18 | 2 |
| [`Slow`](./Enums.md) | Integer | | 12 | 1 |
| [`Stun`](./Enums.md) | Array | | 5 | [.1] |

</details>

---

### Object: `MeleeRevengeDamage`


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 32


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](./Items_and_Equipment.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 94 |  |
| `knockback` | Enum / Integer |  | 48 |  |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 44 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 36 |  |

</details>

---

### Object: `StatusOnBattleEnd`


**Definition:** Applies the nested status effects when the encounter finishes.  
**Total Count:** 25


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./Items_and_Equipment.md#context-applypassives), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 58 |  |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 50 |  |
| [`Conditional_Corpse`](./Enums.md) | Object | | 1 |   |
| [`Conditional_GoodRoll`](./Enums.md) | Object | | 17 |   |
| [`Conditional_Shielded`](./Enums.md) | Object | | 1 |   |
| [`FindItemFromPool`](./Enums.md) | Enum | | 10 | consumables |
| [`GainCoins`](./Enums.md) | Array / Integer | | 3 | [3] |
| [`PermanentConstitution`](./Enums.md) | Integer | | 5 | 2 |
| [`PermanentIntelligence`](./Enums.md) | Integer | | 2 | -1 |
| [`RandomMutation`](./Enums.md) | Integer | | 7 | 1 |
| [`RandomPermanentStat`](./Enums.md) | Integer | | 6 | 2 |
| [`RepairAll`](./Enums.md) | Integer | | 1 | 1 |
| [`RepairTrinket`](./Enums.md) | Integer | | 6 | 99 |
| [`RepairWeapon`](./Enums.md) | Array / Integer | | 3 | [.25] |
| [`SetItemAux`](./Enums.md) | Object | | 3 |   |
| [`TransformWeapon`](./Enums.md) | Object | | 1 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusEachTurnEnd`


**Definition:** Applies or references the 'StatusEachTurnEnd' effect/state.  
**Total Count:** 22


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 55 |  |
| [`AddWeaponAux`](./Enums.md) | Integer | | 1 | 1 |
| [`Burn`](./Enums.md) | Integer | | 16 | 2 |
| [`Conditional_GoodRoll`](./Enums.md) | Object | | 17 |   |
| [`Conditional_ManaThreshold`](./Enums.md) | Object | | 1 |   |
| [`ConstitutionUp`](./Enums.md) | Integer | | 4 | 1 |
| [`ForceUseAbility`](./Enums.md) | Enum | | 14 | tk_SuckStone |
| [`ImmediateUseAbility`](./Enums.md) | Enum / Object | | 3 | head_MagnetoAttract |
| [`PartialCleanse`](./Enums.md) | Integer | | 4 | 1 |
| [`PreEmptiveCounterNextAttacks`](./Enums.md) | Integer | | 1 | 1 |
| [`Shield`](./Enums.md) | Enum / Integer | | 10 | 2 |
| [`SpawnCoinAnywhere`](./Enums.md) | Integer | | 2 | 1 |
| [`Stealth`](./Enums.md) | Array | | 1 | [.1] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnBreak`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 22


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 15 |  |
| [`ApplyToRandomPartyMemberIfPossible`](./Enums.md) | Object | | 1 |   |
| [`Bruise`](./Enums.md) | Integer | | 18 | 2 |
| [`ChangeTilesUnder`](./Enums.md) | Enum | | 3 | WaterTile |
| [`ConstitutionUp`](./Enums.md) | Integer | | 4 | 1 |
| [`DexterityUp`](./Enums.md) | Integer | | 2 | 1 |
| [`FindItem`](./Enums.md) | Enum | | 1 | Pearl |
| [`FindItemFromPool`](./Enums.md) | Enum | | 10 | consumables |
| [`GainCoinsRange`](./Enums.md) | Object | | 6 |   |
| [`GainDisorder`](./Enums.md) | Enum | | 1 | Psychosis |
| [`HealthGain`](./Enums.md) | Integer | | 11 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer | | 42 | 2 |
| [`IntelligenceUp`](./Enums.md) | Integer | | 3 | 2 |
| [`ObjectOnHitCharacter`](./Enums.md) | Enum / Object | | 3 | BestBud |
| [`PermanentConstitution`](./Enums.md) | Integer | | 5 | 2 |
| [`StrengthUp`](./Enums.md) | Integer | | 5 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `SpawnOnBattleStart`


**Definition:** No definition provided.  
**Total Count:** 21


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum |  | 72 |  |
| [`number`](./Arrays.md#array-number) | Array / Integer |  | 48 |  |

</details>

---

### Object: `StatusOnKill`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 36 |  |
| [`BrittleCharismaUp`](./Enums.md) | Integer | | 1 | 2 |
| [`BrittleConstitutionUp`](./Enums.md) | Integer | | 1 | 2 |
| [`BrittleDexterityUp`](./Enums.md) | Integer | | 1 | 2 |
| [`BrittleIntelligenceUp`](./Enums.md) | Integer | | 1 | 2 |
| [`BrittleLuckUp`](./Enums.md) | Integer | | 1 | 2 |
| [`BrittleSpeedUp`](./Enums.md) | Integer | | 1 | 2 |
| [`BrittleStrengthUp`](./Enums.md) | Integer | | 1 | 2 |
| [`CharismaUp`](./Enums.md) | Integer | | 1 | 1 |
| [`Conditional_GoodRoll`](./Enums.md) | Object | | 17 |   |
| [`ConstitutionUp`](./Enums.md) | Integer | | 4 | 1 |
| [`DexterityUp`](./Enums.md) | Integer | | 2 | 1 |
| [`EquipPermanentItem`](./Enums.md) | Enum | | 1 | BoneClub |
| [`HealthGain`](./Enums.md) | Integer | | 11 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer | | 42 | 2 |
| [`IntelligenceUp`](./Enums.md) | Integer | | 3 | 2 |
| [`LuckUp`](./Enums.md) | Integer | | 4 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | | 9 | 2 |
| [`StrengthUp`](./Enums.md) | Integer | | 5 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnTookDamage`


**Definition:** Event Trigger: Applies nested statuses when took damage.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 40 |  |
| [`Bleed`](./Enums.md) | Integer | | 20 | 3 |
| [`Charge`](./Enums.md) | Integer | | 18 | 2 |
| [`Conditional_HasStatus`](./Enums.md) | Object | | 4 |   |
| [`Conditional_HealthThreshold`](./Enums.md) | Object | | 1 |   |
| [`DamageUp`](./Enums.md) | Integer | | 23 | 2 |
| [`DivineShield`](./Enums.md) | Array / Integer | | 7 | [.5] |
| [`DodgeChance_Status`](./Enums.md) | Integer | | 6 | 2 |
| [`RemoveStatus`](./Enums.md) | Enum | | 1 | AlphaCat |
| [`StrengthUp`](./Enums.md) | Integer | | 5 | 1 |
| [`Temporary`](./Enums.md) | Object | | 5 |   |
| [`Thorns`](./Enums.md) | Integer | | 46 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnBattleStart`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 13


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |  |
| [`Brace`](./Enums.md) | Enum / Integer | | 52 | 2 |
| [`Craft`](./Enums.md) | Object | | 4 |   |
| [`DestroyEquipmentAndAttachParasite`](./Enums.md) | Object | | 1 |   |
| [`FindItemFromPool`](./Enums.md) | Enum | | 10 | consumables |
| [`ForceUseAbility`](./Enums.md) | Enum | | 14 | tk_SuckStone |
| [`ObjectOnHitCharacter`](./Enums.md) | Enum / Object | | 3 | BestBud |
| [`RandomMagicMissile`](./Enums.md) | Integer | | 7 | 2 |
| [`ReviveNextRound`](./Enums.md) | Object | | 1 |   |
| [`SafeDie`](./Enums.md) | Integer | | 2 | 1 |
| [`SetHealth`](./Enums.md) | Integer | | 1 | 50 |
| [`StealthUntilBasicAttack`](./Enums.md) | Integer | | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `SpawnThingOnDamage`


**Definition:** Applies or references the 'SpawnThingOnDamage' effect/state.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum |  | 76 |  |
| `good` | Boolean |  | 40 |  |
| [`chance`](./Enums.md#enum-chance) | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 24 |  |
| `spawn_on_death_hit` | Boolean |  | 20 |  |
| `number` | Array / Integer |  | 2 |  |

</details>

---

### Object: `SpawnEachTurn`


**Definition:** Applies or references the 'SpawnEachTurn' effect/state.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Probability (0.0 to 1.0 or percentage) of this occurring. | 40 |  |
| [`object`](./Arrays.md#array-object) | Array / Enum |  | 34 |  |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum |  | 10 |  |

</details>

---

### Object: `StatusEachTurnBegin`


**Definition:** Event Trigger: Applies nested statuses to each turn begin.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |  |
| [`BlessingOfPeace`](./Enums.md) | Integer | | 1 | 1 |
| [`Burn`](./Enums.md) | Integer | | 16 | 2 |
| [`Conditional_BadRoll`](./Enums.md) | Object | | 2 |   |
| [`DestroyTrinket`](./Enums.md) | Integer | | 2 | 1 |
| [`DoubleCastSpellThisTurn`](./Enums.md) | Integer | | 1 | 1 |
| [`DrinkWater`](./Enums.md) | Integer | | 1 | 1 |
| [`ManaGainRange`](./Enums.md) | Object | | 1 |   |
| [`Revive`](./Enums.md) | Integer | | 1 | 1 |
| [`SpeedUp`](./Enums.md) | Integer | | 9 | 2 |
| [`Temporary`](./Enums.md) | Object | | 5 |   |
| [`UseAbility`](./Enums.md) | Enum | | 2 | neck_DarkFriend |
| [`Wet`](./Enums.md) | Integer | | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `RevengeDamage`


**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](./Items_and_Equipment.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 58 |  |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 16 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |  |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |  |

</details>

---

### Object: `AddSelfStatusToBasicAttack`


**Definition:** Applies or references the 'AddSelfStatusToBasicAttack' effect/state.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |  |
| [`Bleed`](./Enums.md) | Integer | | 20 | 3 |
| [`ForceUseAbility`](./Enums.md) | Enum | | 14 | tk_SuckStone |
| [`Quivered`](./Enums.md) | Array / Integer | | 8 | [.10] |
| [`RandomMagicMissile`](./Enums.md) | Integer | | 7 | 2 |
| [`Shield`](./Enums.md) | Enum / Integer | | 10 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `DurabilityTransform`


**Definition:** Applies or references the 'DurabilityTransform' effect/state.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eq`](./Arrays.md#array-eq) | Array |  | 11 |  |
| [`ge`](./Arrays.md#array-ge) | Array |  | 4 |  |

</details>

---

### Object: `PassiveIfStrAuxEquals`


**Definition:** Applies or references the 'PassiveIfStrAuxEquals' effect/state.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`value`](./Math_Equations.md) | Equation |  | 14 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`passives`](./Enums.md) | Object | | 750 |   |

</details>

---

### Object: `StatusOnKillEnemy`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |  |
| [`Brace`](./Enums.md) | Enum / Integer | | 52 | 2 |
| [`DamageUp`](./Enums.md) | Integer | | 23 | 2 |
| [`ForceUseAbility`](./Enums.md) | Enum | | 14 | tk_SuckStone |
| [`LuckUp`](./Enums.md) | Integer | | 4 | 2 |
| [`ManaGain`](./Enums.md) | Integer | | 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AddStatusToAllDamage`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 |  |
| `must_do_damage` | Boolean |  | 6 |  |
| [`Conditional_HasStatus`](./Enums.md) | Object | | 4 |   |
| [`Conditional_HasTag`](./Enums.md) | Object | | 1 |   |
| [`KnockbackIfCrit`](./Enums.md) | Object | | 1 |   |
| [`Rot`](./Enums.md) | Integer | | 3 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `ApplyToSource`


**Definition:** Redirects the nested effects to apply to the caster/source of the ability instead of the target.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus), [`Else`](./Items_and_Equipment.md#context-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 46 |  |
| [`AllStatsUp`](./Enums.md) | Integer | | 12 | -2 |
| [`Charge`](./Enums.md) | Integer | | 18 | 2 |
| [`HealthGain`](./Enums.md) | Integer | | 11 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | | 9 | 2 |
| [`StrengthUp`](./Enums.md) | Integer | | 5 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `GainCoinsRange`


**Definition:** No definition provided.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak), [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | Maximum coins granted. | 22 |  |
| `min` | Integer | Minimum coins granted. | 22 |  |

</details>

---

### Object: `ItemAuxTransform`


**Definition:** Applies or references the 'ItemAuxTransform' effect/state.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`le`](./Arrays.md#array-le) | Array |  | 6 |  |
| [`ge`](./Arrays.md#array-ge) | Array |  | 2 |  |
| [`lt`](./Arrays.md#array-lt) | Array |  | 1 |  |

</details>

---

### Object: `PassiveWhenOnTile`


**Definition:** State Trigger: Grants passives when this condition is met.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |  |
| [`tile`](./Arrays.md#array-tile) | Array / Enum |  | 6 |  |
| [`passives`](./Enums.md) | Object | | 750 |   |

</details>

---

### Object: `StatusAlliesOnBattleStart`


**Definition:** Applies or references the 'StatusAlliesOnBattleStart' effect/state.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |  |
| [`Brace`](./Enums.md) | Enum / Integer | | 52 | 2 |
| [`ConstitutionUp`](./Enums.md) | Integer | | 4 | 1 |
| [`DamageUp`](./Enums.md) | Integer | | 23 | 2 |
| [`SpeedUp`](./Enums.md) | Integer | | 9 | 2 |
| [`StrengthUp`](./Enums.md) | Integer | | 5 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnDie`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |  |
| [`Conditional_RandomChance`](./Enums.md) | Object | | 1 |   |
| [`CreateGlobalModifiers`](./Enums.md) | Object | | 2 |   |
| [`FindItemFromPool`](./Enums.md) | Enum | | 10 | consumables |
| [`GainCoinsRange`](./Enums.md) | Object | | 6 |   |
| [`RandomMagicMissile`](./Enums.md) | Integer | | 7 | 2 |
| [`RandomStatusFromPool`](./Enums.md) | Object | | 1 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnEndMove`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `Temporary`


**Definition:** A wrapper object for applying status effects that automatically expire.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_BadRoll`](./Items_and_Equipment.md#context-conditional_badroll), [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin), [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 114 |  |
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 112 |  |
| `turns` | Array / Integer / Object | Duration in turns. | 104 |  |
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 50 |  |
| `expires_on_end_turn` | Boolean |  | 42 |  |

</details>

---

### Object: `TransformItemOnElementInfluence`


**Definition:** Applies or references the 'TransformItemOnElementInfluence' effect/state.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 10 |  |
| `full_repair` | Boolean |  | 10 |  |
| [`item`](./Enums.md#enum-item) | Enum | Item ID to reference. | 10 |  |

</details>

---

### Object: `AddDamageToElementDamage`


**Definition:** Applies or references the 'AddDamageToElementDamage' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 18 |  |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 18 |  |

</details>

---

### Object: `AddPassivesToMinions`


**Definition:** Applies the 'AddPassivesToMinions' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 44 |  |
| [`AddMaxHealth`](./Enums.md) | Integer | | 1 | 2 |
| [`AddStatusToBasicAttack`](./Enums.md) | Object | | 65 |   |
| [`AllStatsUp`](./Enums.md) | Integer | | 12 | -2 |
| [`HealthGain`](./Enums.md) | Integer | | 11 | 2 |
| [`Shield`](./Enums.md) | Enum / Integer | | 10 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `ChanceToRevive`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 10 |  |
| `health` | Integer |  | 8 |  |

</details>

---

### Object: `Conditional_HasStatus`


**Definition:** Conditional trigger: Executes nested logic if the target currently has the specified status effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage), [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 40 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 24 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 23 |  |
| [`ApplyToSource`](./Items_and_Equipment.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 6 |  |
| `FlatLeechIfDamaged` | `Number` | Applies or references the 'FlatLeechIfDamaged' effect/state. | 2 |  |
| [`RemoveStatusStacks`](./Items_and_Equipment.md#object-removestatusstacks) | Object | Removes a specific number of stacks of a status effect. | 2 |  |
| [`ImmediateUseAbility_Instant`](./Enums.md) | Enum | | 1 | head_CrownOfHorns |

</details>

---

### Object: `Conditional_OncePerBattle`


**Definition:** Conditional trigger: Executes nested logic only once per encounter/battle.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HealthThreshold`](./Items_and_Equipment.md#context-conditional_healththreshold), [`StatusOnFullMana`](./Items_and_Equipment.md#context-statusonfullmana)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`key`](./Enums.md#enum-key) | Enum |  | 6 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`ShowText`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ShowText' effect/state. | 2 |  |
| [`ReduceManaCost`](./Enums.md) | Integer | | 2 | 2 |
| [`Shield`](./Enums.md) | Enum / Integer | | 10 | 2 |
| [`SpellDamageUp`](./Enums.md) | Integer | | 8 | 3 |

</details>

---

### Object: `Craft`


**Definition:** Synthesizes or spawns a new item from a specific pool.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusIfUnusedActPoints`](./Items_and_Equipment.md#context-statusifunusedactpoints), [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Array / Enum |  | 30 |  |
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Equipment slot (weapon, hat, face, chest, etc.). | 28 |  |
| `works_with_tech` | Boolean |  | 8 |  |

</details>

---

### Object: `DelayedAutoRevive`


**Definition:** Applies or references the 'DelayedAutoRevive' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer |  | 12 |  |
| `rounds` | Integer |  | 12 |  |

</details>

---

### Object: `global_passives`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GlobalEnemyAutoRevive` | Integer | Applies or references the 'GlobalEnemyAutoRevive' effect/state. | 4 |  |
| `NoCorpses` | `Number` | Applies or references the 'NoCorpses' effect/state. | 2 |  |
| `RealTimePressure` | Integer | Applies or references the 'RealTimePressure' effect/state. | 2 |  |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |

</details>

---

### Object: `PassiveAtHealthThreshold`


**Definition:** Applies or references the 'PassiveAtHealthThreshold' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 18 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 |  |
| [`passives`](./Enums.md) | Object | | 750 |   |
| [`threshold`](./Enums.md) | Enum / Integer / Object | | 9 | 2 |

</details>

---

### Object: `SpawnObjectOnPopCorpse`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | Quantity. | 2 |  |
| `except_tiny` | Boolean |  | 2 |  |
| [`object`](./Enums.md#enum-object) | Array / Enum |  | 2 |  |

</details>

---

### Object: `StatusOnTakeHealthOrShieldDamage`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#object-conditional-goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 2 |  |
| `Metronome` | `Number` | Executes a random musical or metronome ability. | 2 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`DivineShield`](./Enums.md) | Array / Integer | | 7 | [.5] |

</details>

---

### Object: `StatusRandomEnemiesOnBattleStart`


**Definition:** Applies or references the 'StatusRandomEnemiesOnBattleStart' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | Quantity. | 11 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |  |
| [`Charmed`](./Enums.md) | Integer | | 1 | 2 |
| [`Confusion`](./Enums.md) | Integer | | 8 | 2 |
| [`Fear`](./Enums.md) | Array / Integer | | 11 | [.15] |
| [`Freeze`](./Enums.md) | Array / Integer | | 14 | [.1] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `CatchProjectiles`


**Definition:** Applies or references the 'CatchProjectiles' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ally_chance` | Integer |  | 10 |  |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 10 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |  |
| [`Quivered`](./Enums.md) | Array / Integer | | 8 | [.10] |

</details>

---

### Object: `ClassManaCostReduction`


**Definition:** Applies or references the 'ClassManaCostReduction' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer |  | 14 |  |
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 12 |  |

</details>

---

### Object: `Conditional_PartyMember`


**Definition:** Conditional constraint. Nested properties only trigger if this is true.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ExtraStatusWhenDealingDamage`](./Items_and_Equipment.md#context-extrastatuswhendealingdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `CounterAttack`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 10 |  |
| `melee_only` | Boolean |  | 2 |  |
| `ranged_only` | Boolean |  | 2 |  |

</details>

---

### Object: `Else`


**Definition:** Fallback object that executes if the preceding `Conditional_` block evaluated to false.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_PartyMember`](./Items_and_Equipment.md#context-conditional_partymember)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 76 |  |
| [`ApplyToSource`](./Enums.md) | Object | | 6 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `ExtraStatusWhenDealingDamage`


**Definition:** Applies or references the 'ExtraStatusWhenDealingDamage' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `PassiveWhenDead`


**Definition:** State Trigger: Grants passives when this condition is met.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `SetItemAux`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Shielded`](./Items_and_Equipment.md#context-conditional_shielded), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Equipment slot (weapon, hat, face, chest, etc.). | 6 |  |
| [`value`](./Math_Equations.md) | Equation |  | 6 |  |

</details>

---

### Object: `SpawnExtraThingsOnBattleStart`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum |  | 19 |  |
| [`number`](./Arrays.md#array-number) | Array / Integer |  | 3 |  |

</details>

---

### Object: `SpawnOnBattleStartRandomEmptyTile`


**Definition:** Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum |  | 22 |  |
| [`number`](./Arrays.md#array-number) | Array / Integer |  | 6 |  |

</details>

---

### Object: `StackingFlowerTrail`


**Definition:** Applies or references the 'StackingFlowerTrail' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum |  | 6 |  |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 6 |  |

</details>

---

### Object: `StatusAllCharactersOnSpawn`


**Definition:** Applies or references the 'StatusAllCharactersOnSpawn' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`Conditional_Boss`](./Enums.md) | Object | | 2 |   |
| [`Poison`](./Enums.md) | Integer | | 18 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusEveryXSpellCasts`


**Definition:** Applies or references the 'StatusEveryXSpellCasts' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 16 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |  |
| [`Charge`](./Enums.md) | Integer | | 18 | 2 |
| [`IntelligenceUp`](./Enums.md) | Integer | | 3 | 2 |
| [`ObjectOnHitCharacter`](./Enums.md) | Enum / Object | | 3 | BestBud |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnPopCorpse`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |  |
| [`HealthGain`](./Enums.md) | Integer | | 11 | 2 |
| [`RepairTrinket`](./Enums.md) | Integer | | 6 | 99 |
| [`RepairWeapon`](./Enums.md) | Array / Integer | | 3 | [.25] |

</details>

---

### Object: `StatusOnTurnEndIfDidntCastAbilityTypes`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 8 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |  |
| [`Charge`](./Enums.md) | Integer | | 18 | 2 |
| [`DamageUp`](./Enums.md) | Integer | | 23 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer | | 42 | 2 |
| [`Shield`](./Enums.md) | Enum / Integer | | 10 | 2 |
| [`SpellDamageUp`](./Enums.md) | Integer | | 8 | 3 |
| [`Thorns`](./Enums.md) | Integer | | 46 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AddStatusToElementDamage`


**Definition:** Applies the 'AddStatusToElementDamage' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 12 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |  |
| [`Burn`](./Enums.md) | Integer | | 16 | 2 |
| [`Stun`](./Enums.md) | Array | | 5 | [.1] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AddStatusToKnockbackDamage`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToSpells`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `ApplyStatusesToRandomEnemiesEachTurn`


**Definition:** Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count` | Array / Integer | Quantity. | 4 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`Bounty`](./Enums.md) | Integer | | 1 | 1 |
| [`Marked`](./Enums.md) | Integer | | 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `ArmorBreakOnHit`


**Definition:** Applies or references the 'ArmorBreakOnHit' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance_to_break` | Integer |  | 4 |  |
| `durability_loss` | Integer |  | 4 |  |

</details>

---

### Object: `bonus_passives`


**Definition:** Passives granted to the character while this ability is equipped.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`str_aux_is_copy_ability`](./Items_and_Equipment.md#context-str_aux_is_copy_ability)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 126 |  |
| [`ModifyAbility`](./Enums.md) | Object | | 2 |   |

</details>

---

### Object: `BoostWeaponDamage`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | `Number` |  | 8 |  |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 8 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |

</details>

---

### Object: `ChanceToBackflip`


**Definition:** Applies or references the 'ChanceToBackflip' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 12 |  |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 12 |  |

</details>

---

### Object: `ChanceToBlockAndCounter`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean |  | 2 |  |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |  |

</details>

---

### Object: `Conditional_Adjacent`


**Definition:** Conditional object: Executes nested logic only if the target is/has Adjacent.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusAlliesOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusalliesonspendmana), [`StatusAlliesEachTurn`](./Items_and_Equipment.md#context-statusallieseachturn)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`Conditional_Ally`](./Enums.md) | Object | | 1 |   |
| [`Conditional_PlayerCat`](./Enums.md) | Object | | 1 |   |

</details>

---

### Object: `Conditional_BadRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized bad outcome probability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Number | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 16 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |  |
| [`Temporary`](./Enums.md) | Object | | 5 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `Conditional_Boss`


**Definition:** Conditional trigger: Executes nested logic if the target is a Boss.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusAllCharactersOnSpawn`](./Items_and_Equipment.md#context-statusallcharactersonspawn)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 27 |  |
| [`AllStatsUp`](./Enums.md) | Integer | | 12 | -2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `cost`


**Definition:** Object defining resource requirements (Mana, Act Points, Moves) needed to cast.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ModifyAbility`](./Items_and_Equipment.md#context-modifyability)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Enum / Integer |  | 3210 |  |
| `charge` | Integer / String |  | 36 |  |

</details>

---

### Object: `CreateGlobalModifiers`


**Definition:** Generates global map or encounter rules/modifiers.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |  |
| `NextPlayerCatTakesExtraTurn` | `Number` | Applies or references the 'NextPlayerCatTakesExtraTurn' effect/state. | 2 |  |
| `NoCorpses` | `Number` | Applies or references the 'NoCorpses' effect/state. | 2 |  |

</details>

---

### Object: `DoDamage`


**Definition:** Explicitly triggers a secondary damage instance independent of the main attack.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachRoundEnd`](./Items_and_Equipment.md#context-statuseachroundend), [`StatusOnBreakItem`](./Items_and_Equipment.md#context-statusonbreakitem)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Enum / Integer / Object | The flat damage amount. | 14 |  |
| [`type`](./Enums.md#enum-type) | Enum | The classification of the damage (e.g., spell, melee). | 14 |  |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum |  | 8 |  |
| [`effects`](./Items_and_Equipment.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 8 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |  |

</details>

---

### Object: `ElementalManaCostReduction`


**Definition:** Applies the 'ElementalManaCostReduction' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer |  | 10 |  |
| [`element`](./Arrays.md#array-element) | Array / Enum | Specific element type required or applied. | 4 |  |

</details>

---

### Object: `ImmediateUseAbility`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 2 |  |
| `even_if_stunned` | Boolean |  | 2 |  |

</details>

---

### Object: `keyword_tooltips`


**Definition:** Forces specific UI tooltips to appear when hovering over the ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 18 |  |
| [`DivineShield`](./Enums.md) | Array / Integer | | 7 | [.5] |
| [`Immobile`](./Enums.md) | Integer | | 4 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `meta`


**Definition:** Object defining UI display data (Name, Description, Icon).  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ModifyAbility`](./Items_and_Equipment.md#context-modifyability)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `is_basic_attack` | Boolean |  | 12 |  |
| `is_weapon` | Boolean |  | 8 |  |

</details>

---

### Object: `ModifyAbility`


**Definition:** Applies or references the 'ModifyAbility' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Items_and_Equipment.md#context-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Items_and_Equipment.md#context-cost) | Object | Currency value in shops/merchants. | 4 |  |
| [`meta`](./Items_and_Equipment.md#context-meta) | Object |  | 4 |  |

</details>

---

### Object: `MovementReaction`


**Definition:** Reaction: Triggers an effect or ability when forced to move.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhileHasDurability`](./Items_and_Equipment.md#context-passivewhilehasdurability), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 22 |  |
| `enemies_only` | Boolean |  | 14 |  |
| `on_self_move_too` | Boolean |  | 6 |  |
| `create_temp_ability` | Boolean |  | 4 |  |

</details>

---

### Object: `ObjectOnHitCharacter`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEveryXSpellCasts`](./Items_and_Equipment.md#context-statuseveryxspellcasts), [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | The entity ID of the character to spawn (e.g., CharmedFlea). | 14 |  |
| [`stacks`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Number of stacks or intensity to apply. | 10 |  |

</details>

---

### Object: `passive`


**Definition:** Intrinsic passive modifier.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`Metal`](./Enums.md) | Integer | | 91 | 1 |

</details>

---

### Object: `PassiveAtStatThreshold`


**Definition:** Applies the 'PassiveAtStatThreshold' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 33 |  |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 26 |  |
| [`passives`](./Enums.md) | Object | | 750 |   |
| [`threshold`](./Enums.md) | Enum / Integer / Object | | 9 | 2 |

</details>

---

### Object: `PassiveIfWeaponIsUsable`


**Definition:** Applies or references the 'PassiveIfWeaponIsUsable' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`Brace`](./Enums.md) | Enum / Integer | | 52 | 2 |

</details>

---

### Object: `RefreshEquipmentAbilityOnElement`


**Definition:** Applies or references the 'RefreshEquipmentAbilityOnElement' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 4 |  |
| [`text`](./Strings.md#string-text) | String |  | 4 |  |

</details>

---

### Object: `SpawnItemLinkedFamiliar`


**Definition:** Applies or references the 'SpawnItemLinkedFamiliar' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean |  | 4 |  |
| [`object`](./Enums.md#enum-object) | Array / Enum |  | 4 |  |

</details>

---

### Object: `StatusAfterCastSpell`


**Definition:** Applies or references the 'StatusAfterCastSpell' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`TempMeleeRangeUp`](./Enums.md) | Integer | | 1 | 1 |
| [`TempRangeUp`](./Enums.md) | Integer | | 1 | 1 |
| [`UseAbility`](./Enums.md) | Enum | | 2 | neck_DarkFriend |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusAfterXStacks`


**Definition:** Applies or references the 'StatusAfterXStacks' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusonspendmana), [`StatusOnCollectPickup`](./Items_and_Equipment.md#context-statusoncollectpickup)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum |  | 4 |  |
| `expires_on_end_turn` | Boolean |  | 2 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer | | 2 | 1 |
| [`RefreshActPoints`](./Enums.md) | Integer | | 1 | 1 |
| [`threshold`](./Enums.md) | Enum / Integer / Object | | 9 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusIfUnusedActPoints`


**Definition:** Applies or references the 'StatusIfUnusedActPoints' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnAllyCatDeath`


**Definition:** Event Trigger: Applies nested statuses when ally cat death.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |  |
| [`DivineShield`](./Enums.md) | Array / Integer | | 7 | [.5] |
| [`RepairTrinket`](./Enums.md) | Integer | | 6 | 99 |

</details>

---

### Object: `StatusOnBackstab`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SerratedClaws` | Integer | Applies or references the 'SerratedClaws' effect/state. | 2 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`HealthGain`](./Enums.md) | Integer | | 11 | 2 |

</details>

---

### Object: `StatusOnBreakItem`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`DoDamage`](./Enums.md) | Object | | 2 |   |
| [`Shield`](./Enums.md) | Enum / Integer | | 10 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnCastSpell`


**Definition:** Event Trigger: Applies nested statuses when cast spell.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |  |
| [`Charge`](./Enums.md) | Integer | | 18 | 2 |
| [`Shield`](./Enums.md) | Enum / Integer | | 10 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnGainCoins`


**Definition:** Event Trigger: Applies nested statuses when gain coins.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |  |
| [`LuckUp`](./Enums.md) | Integer | | 4 | 2 |
| [`Shield`](./Enums.md) | Enum / Integer | | 10 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `str_aux_is_copy_ability`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](./Items_and_Equipment.md#context-bonus_passives) | Object | Passives granted to the character while this ability is equipped. | 4 |  |

</details>

---

### Object: `threshold`


**Definition:** Examples: `4*champion_multiplier, 3*champion_multiplier, 1`  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `int` | Enum / Integer |  | 16 |  |
| `con` | Enum / Integer |  | 2 |  |

</details>

---

### Object: `AbilityHealthThreshold`


**Definition:** AI Trigger: Executes an ability when health drops below a specific threshold.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 26 |  |
| `even_if_stunned` | Boolean |  | 14 |  |
| `immediate` | Boolean |  | 12 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 |  |
| `aux` | Integer |  | 2 |  |
| [`threshold`](./Enums.md) | Enum / Integer / Object | | 9 | 2 |

</details>

---

### Object: `AbilityOnRoundEndOnce`


**Definition:** Applies or references the 'AbilityOnRoundEndOnce' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 2 |  |
| `even_of_stunned` | Boolean |  | 2 |  |

</details>

---

### Object: `AddAdvantageToEvent`


**Definition:** Applies or references the 'AddAdvantageToEvent' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `add` | Array / Integer |  | 2 |  |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |  |
| [`options`](./Enums.md) | Array | | 1 | [smash] |

</details>

---

### Object: `AddPassivesToCharmed`


**Definition:** Applies the 'AddPassivesToCharmed' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |  |
| [`AllStatsUp`](./Enums.md) | Integer | | 12 | -2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AddSelfStatusToWeapons`


**Definition:** Applies the 'AddSelfStatusToWeapons' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToBackstabs`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`Bleed`](./Enums.md) | Integer | | 20 | 3 |

</details>

---

### Object: `AddStatusToWeapons`


**Definition:** Applies the 'AddStatusToWeapons' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |  |
| [`Leech`](./Enums.md) | Integer | | 8 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** Applies the 'AddTemporaryEffectsToBasicAttack' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CastAgainWithStatus`](./Items_and_Equipment.md#context-castagainwithstatus) | Object | Applies or references the 'CastAgainWithStatus' effect/state. | 2 |  |

</details>

---

### Object: `AIControlNextTurn`


**Definition:** Applies or references the 'AIControlNextTurn' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_spells` | Boolean |  | 2 |  |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 2 |  |

</details>

---

### Object: `AlluringDoodieEater`


**Definition:** Applies or references the 'AlluringDoodieEater' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |  |
| [`damage_instance`](./Items_and_Equipment.md#context-damage_instance) | Object |  | 2 |  |

</details>

---

### Object: `AllyDodgeChanceAura`


**Definition:** Applies or references the 'AllyDodgeChanceAura' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |  |
| `range` | Enum / Integer | Distance or area of effect in tiles. | 2 |  |

</details>

---

### Object: `ApplyPassives`


**Definition:** Grants the nested passive abilities dynamically.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_RandomChance`](./Items_and_Equipment.md#context-conditional_randomchance)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 13 |  |
| [`StatusOnBattleEnd`](./Enums.md) | Object | | 25 |   |

</details>

---

### Object: `ApplyToRandomPartyMemberIfPossible`


**Definition:** Redirects the nested effects to apply to a random living member of the player's party.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AutocastEachRound`


**Definition:** Forces the character to automatically cast a specific ability at the start of each combat round.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 18 |  |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 12 |  |

</details>

---

### Object: `BackflipWhenTargeted`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific dodge ability to trigger (e.g., DestroyerDodge). | 14 |  |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 14 |  |

</details>

---

### Object: `BouncyProjectiles`


**Definition:** Applies the 'BouncyProjectiles' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max_bounces` | Integer |  | 6 |  |
| `max_range` | Enum / Integer |  | 6 |  |

</details>

---

### Object: `BuffImmunity`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exclude`](./Enums.md#enum-exclude) | Enum |  | 2 |  |

</details>

---

### Object: `CastAgainWithStatus`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddTemporaryEffectsToBasicAttack`](./Items_and_Equipment.md#context-addtemporaryeffectstobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 2 |  |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 2 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |

</details>

---

### Object: `CatPartsSizeScale`


**Definition:** Applies or references the 'CatPartsSizeScale' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `head` | Enum / Number |  | 2 |  |

</details>

---

### Object: `ChanceToForceEvent`


**Definition:** Applies or references the 'ChanceToForceEvent' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |  |
| [`event`](./Enums.md#enum-event) | Enum |  | 2 |  |

</details>

---

### Object: `Conditional_Ally`


**Definition:** Conditional trigger: Executes nested logic if the target is friendly to the caster.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 30 |  |
| [`ManaGain`](./Enums.md) | Integer | | 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `Conditional_Corpse`


**Definition:** Conditional trigger: Executes nested logic if the target is a dead body/corpse.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |  |
| [`RandomMutation`](./Enums.md) | Integer | | 7 | 1 |

</details>

---

### Object: `Conditional_Enemy`


**Definition:** Conditional trigger: Executes nested logic if the target is hostile to the caster.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToSpells`](./Items_and_Equipment.md#context-addstatustospells)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 37 |  |
| [`Leeches`](./Enums.md) | Integer | | 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `Conditional_HasTag`


**Definition:** Conditional trigger: Executes nested logic if the target possesses the specified entity tag.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | The specific string tag to check for. | 91 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 63 |  |
| [`BonusKnockbackDamage`](./Enums.md) | Integer | | 1 | 5 |
| [`OverrideChainKnockback`](./Enums.md) | Integer | | 2 | 0 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `Conditional_HealthThreshold`


**Definition:** Conditional trigger: Executes nested logic if the target's health falls below the specified threshold.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `threshold_flat` | Integer | A flat numerical health value threshold. | 10 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |  |
| [`Conditional_OncePerBattle`](./Items_and_Equipment.md#object-conditional-onceperbattle) | Object | Conditional trigger: Executes nested logic only once per encounter/battle. | 2 |  |

</details>

---

### Object: `Conditional_ManaThreshold`


**Definition:** Conditional constraint. Nested properties only trigger if this is true.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `threshold_flat` | Integer |  | 2 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`RepairTrinket`](./Enums.md) | Integer | | 6 | 99 |

</details>

---

### Object: `Conditional_PlayerCat`


**Definition:** Conditional trigger: Executes nested logic if the target is a player-controlled cat.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |  |
| [`Charge`](./Enums.md) | Integer | | 18 | 2 |

</details>

---

### Object: `Conditional_RandomChance`


**Definition:** Conditional trigger: Executes nested logic based on a flat percentage random roll.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 8 |  |
| [`ApplyPassives`](./Items_and_Equipment.md#object-applypassives) | Object | Grants the nested passive abilities dynamically. | 4 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |  |

</details>

---

### Object: `Conditional_Shielded`


**Definition:** Conditional trigger: Executes nested logic if the target currently has a Shield status.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `ConvertDamageToScaledStatus`


**Definition:** Applies or references the 'ConvertDamageToScaledStatus' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 2 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`DelayedPain`](./Enums.md) | Integer | | 1 | 1 |

</details>

---

### Object: `CritsApplyStatus`


**Definition:** Applies the 'CritsApplyStatus' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 |  |
| [`Fear`](./Enums.md) | Array / Integer | | 11 | [.15] |

</details>

---

### Object: `damage_instance`


**Definition:** Object defining the combat math and status effects applied upon successful hit.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AlluringDoodieEater`](./Items_and_Equipment.md#context-alluringdoodieeater)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](./Items_and_Equipment.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 3574 |  |
| `damage` | Enum / Integer / Object | The base damage properties of an attack. | 2894 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1731 |  |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 718 |  |

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
<summary><b>AddStatusToKnockbackDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

<details>
<summary><b>AddStatusToSpells</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |

</details>

<details>
<summary><b>ApplyToRandomPartyMemberIfPossible</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

<details>
<summary><b>Conditional_Adjacent</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |

</details>

<details>
<summary><b>Conditional_HealthThreshold</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |  |

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
<summary><b>PassiveWhenDead</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |

</details>

<details>
<summary><b>PassiveWhileHasDurability</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |  |

</details>

<details>
<summary><b>ScaledStatusAlliesOnSpendMana</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |  |

</details>

<details>
<summary><b>StatusAlliesEachTurn</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |

</details>

<details>
<summary><b>StatusIfUnusedActPoints</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |  |

</details>

<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |  |

</details>

<details>
<summary><b>StatusOnFallAsleep</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |

</details>

### Object: `DestroyEquipmentAndAttachParasite`


**Definition:** Removes an equipped item and replaces it with a parasite from a specified pool.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 8 |  |
| [`pool`](./Arrays.md#array-pool) | Array / Enum | The item pool to draw the parasite from. | 4 |  |

</details>

---

### Object: `Eternal`


**Definition:** Applies the 'Eternal' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health_percent` | Integer |  | 6 |  |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 6 |  |

</details>

---

### Object: `FlyDamageIncrease`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 2 |  |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 2 |  |

</details>

---

### Object: `ForceUseAbilityOnTarget`


**Definition:** Applies or references the 'ForceUseAbilityOnTarget' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 2 |  |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |  |

</details>

---

### Object: `GlobalMeleeRevengeDamage`


**Definition:** Applies or references the 'GlobalMeleeRevengeDamage' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Enum / Integer |  | 2 |  |

</details>

---

### Object: `KnockbackIfCrit`


**Definition:** Applies or references the 'KnockbackIfCrit' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Enum / Integer |  | 2 |  |
| `override_chain_knockback` | Integer |  | 2 |  |

</details>

---

### Object: `KnockUpAndAway`


**Definition:** Displaces the target vertically and horizontally away from the source.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The distance in tiles to knock the target away. | 48 |  |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 44 |  |

</details>

---

### Object: `ManaGainRange`


**Definition:** Applies or references the 'ManaGainRange' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer |  | 2 |  |
| `min` | Integer |  | 2 |  |

</details>

---

### Object: `ObjectDetector`


**Definition:** Applies or references the 'ObjectDetector' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |  |
| [`object`](./Enums.md#enum-object) | Array / Enum |  | 2 |  |

</details>

---

### Object: `PassiveAfterXKills`


**Definition:** Applies or references the 'PassiveAfterXKills' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 8 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |  |
| [`passives`](./Enums.md) | Object | | 750 |   |

</details>

---

### Object: `PassiveWhenAffectedByElement`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 36 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 33 |  |
| [`passives`](./Enums.md) | Object | | 750 |   |

</details>

---

### Object: `PassiveWhileHasDurability`


**Definition:** Applies or references the 'PassiveWhileHasDurability' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `PassiveWhileInMonkMeleeStance`


**Definition:** Applies the 'PassiveWhileInMonkMeleeStance' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`Brace`](./Enums.md) | Enum / Integer | | 52 | 2 |

</details>

---

### Object: `PassiveWhileShielded`


**Definition:** Applies or references the 'PassiveWhileShielded' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`HealthRegenUp`](./Enums.md) | Integer | | 42 | 2 |

</details>

---

### Object: `PoopWhenHit`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |  |
| [`object`](./Enums.md#enum-object) | Array / Enum |  | 2 |  |

</details>

---

### Object: `RandomStatusFromPool`


**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 35 |  |
| [`PermanentCharisma`](./Enums.md) | Integer | | 1 | 1 |
| [`PermanentConstitution`](./Enums.md) | Integer | | 5 | 2 |
| [`PermanentDexterity`](./Enums.md) | Integer | | 1 | 1 |
| [`PermanentIntelligence`](./Enums.md) | Integer | | 2 | -1 |
| [`PermanentLuck`](./Enums.md) | Integer | | 1 | 1 |
| [`PermanentSpeed`](./Enums.md) | Integer | | 1 | 1 |
| [`PermanentStrength`](./Enums.md) | Integer | | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `RemoveStatusStacks`


**Definition:** Removes a specific number of stacks of a status effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks to remove. | 8 |  |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 8 |  |

</details>

---

### Object: `ReviveNextRound`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `revive_health` | Integer | The flat amount of health to revive with. | 8 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`Shield`](./Enums.md) | Enum / Integer | | 10 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `ScaldingOrbMoonBossOneShot`


**Definition:** Applies or references the 'ScaldingOrbMoonBossOneShot' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CompleteItemQuest`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'CompleteItemQuest' effect/state. | 2 |  |
| [`RemoveItem`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'RemoveItem' effect/state. | 2 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |

</details>

---

### Object: `ScaledStatusAlliesOnSpendMana`


**Definition:** Applies or references the 'ScaledStatusAlliesOnSpendMana' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `ScaledStatusOnHolyShieldBlock`


**Definition:** Applies or references the 'ScaledStatusOnHolyShieldBlock' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`RandomMagicMissile`](./Enums.md) | Integer | | 7 | 2 |

</details>

---

### Object: `ScaledStatusOnSpendMana`


**Definition:** Applies the 'ScaledStatusOnSpendMana' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`StatusAfterXStacks`](./Enums.md) | Object | | 2 |   |

</details>

---

### Object: `SpawnOnDeath`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 8 |  |
| [`obj`](./Enums.md#enum-obj) | Array / Enum |  | 4 |  |

</details>

---

### Object: `SpawnRandomPickupsOnTaggedUnitKilled`


**Definition:** Applies or references the 'SpawnRandomPickupsOnTaggedUnitKilled' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 2 |  |
| [`count`](./Arrays.md#array-count) | Array / Integer | Quantity. | 1 |  |

</details>

---

### Object: `StatDependentPassive`


**Definition:** Applies or references the 'StatDependentPassive' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`AddDamageToBasicAttack`](./Enums.md) | Enum | | 1 | min(min(min(min(min(min(str,dex),int),con),lck),spd),cha)-2 |

</details>

---

### Object: `StatusAdjacentOnTheirTurnEnd`


**Definition:** Applies or references the 'StatusAdjacentOnTheirTurnEnd' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveAway` | `Number` | Applies or references the 'ForceMoveAway' effect/state. | 2 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |

</details>

---

### Object: `StatusAfterXTurns`


**Definition:** Event Trigger: Applies a status effect after X turns have passed.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 4 |  |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`ForceUseAbility`](./Enums.md) | Enum | | 14 | tk_SuckStone |

</details>

---

### Object: `StatusAlliesEachTurn`


**Definition:** Applies or references the 'StatusAlliesEachTurn' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusAlliesOnDeath`


**Definition:** Event Trigger: Applies nested statuses to allies on death.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |  |
| [`DivineShield`](./Enums.md) | Array / Integer | | 7 | [.5] |

</details>

---

### Object: `StatusEachRoundEnd`


**Definition:** Applies or references the 'StatusEachRoundEnd' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |  |
| [`DoDamage`](./Enums.md) | Object | | 2 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusEachTurnEndForEachTurn`


**Definition:** Event Trigger: Applies nested statuses to each turn end for each turn.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`ForceUseAbility`](./Enums.md) | Enum | | 14 | tk_SuckStone |

</details>

---

### Object: `StatusIfUnusedMovePoints`


**Definition:** Event Trigger: Applies nested statuses to if unused move points.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |  |
| [`Charge`](./Enums.md) | Integer | | 18 | 2 |
| [`HealthGain`](./Enums.md) | Integer | | 11 | 2 |

</details>

---

### Object: `StatusOnCollectPickup`


**Definition:** Event Trigger: Applies nested statuses when collect pickup.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`StatusAfterXStacks`](./Enums.md) | Object | | 2 |   |

</details>

---

### Object: `StatusOnDodge`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`DodgeChance_Status`](./Enums.md) | Integer | | 6 | 2 |

</details>

---

### Object: `StatusOnEatFood`


**Definition:** Event Trigger: Applies nested statuses when eat food.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |  |
| [`RepairTrinket`](./Enums.md) | Integer | | 6 | 99 |
| [`TempPassiveUntilSettled`](./Enums.md) | Object | | 1 |   |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnEnemyDeath`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`Charge`](./Enums.md) | Integer | | 18 | 2 |

</details>

---

### Object: `StatusOnFallAsleep`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`AllStatsUp`](./Enums.md) | Integer | | 12 | -2 |
| [`FillMana`](./Enums.md) | Integer | | 1 | 1 |
| [`HealRandomInjury`](./Enums.md) | Integer | | 1 | 1 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnFullMana`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](./Items_and_Equipment.md#object-conditional-onceperbattle) | Object | Conditional trigger: Executes nested logic only once per encounter/battle. | 2 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |

</details>

---

### Object: `StatusOnHealed`


**Definition:** Event Trigger: Applies nested statuses when healed.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |  |
| [`Shield`](./Enums.md) | Enum / Integer | | 10 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | |

</details>

---

### Object: `StatusOnPickupCoins`


**Definition:** Event Trigger: Applies nested statuses when pickup coins.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`GainCoins`](./Enums.md) | Array / Integer | | 3 | [3] |

</details>

---

### Object: `StatusOnUseBasicAttack`


**Definition:** Event Trigger: Applies nested statuses when use basic attack.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`DamageUp`](./Enums.md) | Integer | | 23 | 2 |
| [`HealthGain`](./Enums.md) | Integer | | 11 | 2 |

</details>

---

### Object: `StatusWhenAllySpendsMana`


**Definition:** Event Trigger: Applies nested statuses to when ally spends mana.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |  |
| [`Charge`](./Enums.md) | Integer | | 18 | 2 |

</details>

---

### Object: `TempPassiveUntilSettled`


**Definition:** Passive: Active only until the physics engine stops moving the character.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEatFood`](./Items_and_Equipment.md#context-statusoneatfood)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |
| [`LimitHeal`](./Enums.md) | Integer | | 1 | 0 |

</details>

---

### Object: `TintItem`


**Definition:** Applies or references the 'TintItem' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ignore_if_str_aux_equals`](./Enums.md#enum-ignore_if_str_aux_equals) | Enum |  | 2 |  |
| [`add`](./Arrays.md#array-add) | Array / Integer |  | 1 |  |
| [`mul`](./Arrays.md#array-mul) | Array |  | 1 |  |

</details>

---

### Object: `TransformWeapon`


**Definition:** Transforms the equipped weapon into another specific weapon state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | The original weapon ID. | 4 |  |
| [`to`](./Enums.md#enum-to) | Enum | The transformed weapon ID. | 4 |  |

</details>

---

### Object: `TunnelVision`


**Definition:** Applies or references the 'TunnelVision' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | `Number` |  | 2 |  |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |  |

</details>

---
