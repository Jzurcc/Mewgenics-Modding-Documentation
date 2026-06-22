# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Items & Equipment

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"ARMOR_SCRAPMETALARMOR_DESC", "ARMOR_SCRAPMETALHAT_DESC", "ARMOR_SCRAPMETALMASK_DESC"` | Localization key for the item's desc. |
| `name` | String | `"ARMOR_SCRAPMETALARMOR_NAME", "ARMOR_SCRAPMETALMASK_NAME", "ARMOR_SCRAPMETALHAT_NAME"` | Localization key for the item's name. |
| `frame` | Number | `2, 23, 12` |  |
| `kind` | [`Enum/String`](./Enums.md#enum-kind) | `neck, face, head` |  |
| `rarity` | [`Enum/String`](./Enums.md#enum-rarity) | `common, uncommon, rare` |  |
| `set` | [`Enum/String`](./Enums.md#enum-set) | `Scrap, Leather, Rag` |  |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `wp_PartyDetonatorFixed, wp_PersuasionDevice, wp_PartyDetonator` | ID of the ability to trigger or reference. |
| `shield` | Number | `2, 1, 4` |  |
| `durability` | Number | `2, 1, 3` | Maximum uses before breaking. |
| `pieces_required` | Number | `3` |  |
| `cursed` | Boolean | `true` |  |
| `cha` | Number | `2, 1, -1` |  |
| `consumable` | Boolean | `true` |  |
| `spd` | Number | `-4, 3, -1` |  |
| `con` | Number | `2, 1, 3` |  |
| `int` | Number | `7, 1, -1` |  |
| `lck` | Number | `2, 1, -3` |  |
| `quest_item` | Boolean | `false, true` |  |
| `parasite` | Boolean | `true` |  |
| `aux` | Number | `24, 10, 12` |  |
| `variant_of` | [`Enum/String`](./Enums.md#enum-variant_of) | `RedCap, PoundOfFlesh, CrimsonMask` |  |
| `str` | [`Enum/String`](./Enums.md#enum-str) | `aux, 2, 1` |  |
| `dex` | Number | `1, 3, -1` |  |
| `quest_reward_item` | [`Enum/String`](./Enums.md#enum-quest_reward_item) | `PersuasionDevice_Fixed, MagicMirror_Fixed, ChaosDevice_Fixed` |  |
| `indestructible` | Boolean | `true` |  |
| `divine_shield` | Number | `2, 1, 3` |  |
| `legacy_quest` | Boolean | `true` |  |
| `hint_destination` | [`Enum/String`](./Enums.md#enum-hint_destination) | `caves, boneyard, meatworld` |  |
| `str_aux_initialize` | [`Enum/String`](./Enums.md#enum-str_aux_initialize) | `random_seed, random_stat, random_class_passive` |  |
| `dont_destroy_on_0` | Boolean | `true` |  |
| `global_tags` | [`Array`](./Arrays.md#array-global_tags) | `[ all_cats_are_jester ], [ fail_all_events ], [ always_ambushed ]` |  |
| `max_durability` | Number | `2, 9, 3` |  |
| `on_store` | [`Enum/String`](./Enums.md#enum-on_store) | `become_rare_furniture, become_furniture, become_aux_coins` |  |
| `name_mod` | String | `"CAT_NAME_MOD_AMOEBA", "CAT_NAME_MOD_MAN", "CAT_NAME_MOD_COOL"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicTankMelee, BasicSpin, IsaacBasicAttack` |  |
| `hint_prerequisite_flag` | [`Enum/String`](./Enums.md#enum-hint_prerequisite_flag) | `mapflag_MeatWorldUnlocked, mapflag_BothObelisksUnlocked, mapflag_MeatWorldUnlockedFull` |  |
| `failable` | Boolean | `true` |  |
| `randomize_piece_frames` | Boolean | `true` |  |
| `str_aux_is_copy_passive` | Boolean | `true` |  |
| `fragile` | Boolean | `true` |  |
| `icon_hint` | [`Enum/String`](./Enums.md#enum-icon_hint) | `passive_syringe, ability_syringe` |  |
| `max_health` | Number | `-1` |  |
| `reset_aux_on_store` | Number | `1` |  |
| `sticky` | Boolean | `true` |  |
| `weightless` | Boolean | `true` |  |
| `prevent_level_up` | Boolean | `true` |  |
| `quest_item_alias` | [`Enum/String`](./Enums.md#enum-quest_item_alias) | `BlackShard, NuclearKnife` |  |
| `speed` | Number | `1` |  |
| `str_aux_is_copy_item_passive` | Boolean | `true` |  |
| `Set` | [`Enum/String`](./Enums.md#enum-set) | `Monk` | Applies or references the 'Set' effect/state. |
| `aux_is_catid` | Boolean | `true` |  |
| `cant_equip_to_colorless` | Boolean | `true` |  |
| `degrade_after_adventure` | Boolean | `false` |  |
| `equip_sound` | [`Enum/String`](./Enums.md#enum-equip_sound) | `SE_CatWeaponPoke_Chainsaw` |  |
| `force_sticky` | Boolean | `true` |  |
| `reset_str_aux_on_store` | [`Enum/String`](./Enums.md#enum-reset_str_aux_on_store) | `ModelingClay_Default` |  |
| `str_aux` | [`Enum/String`](./Enums.md#enum-str_aux) | `ModelingClay_Default` |  |
| `str_aux_is_copy_item_active` | Boolean | `true` |  |
| `str_aux_is_copy_item_icon` | Boolean | `true` |  |

</details>

---

### Context: `passives`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Metal` | Number | `1` | Applies or references the 'Metal' effect/state. |
| `AddStatusToBasicAttack` | [`Block`](./Items_and_Equipment.md#context-addstatustobasicattack) | `{ ... }` | Injects a status effect payload that applies whenever the character performs a basic attack. |
| `Brace` | Number | `2, 1, 3` | Applies or references the 'Brace' effect/state. |
| `Thorns` | Number | `2, 1, 3` | Applies or references the 'Thorns' effect/state. |
| `HealthRegenUp` | Number | `2, 1, 3` | Applies or references the 'HealthRegenUp' effect/state. |
| `SpawnOnBattleStart` | [`Block`](./Items_and_Equipment.md#context-spawnonbattlestart) | `{ ... }, CharmedCultist, CharmedGamete` | Applies or references the 'SpawnOnBattleStart' effect/state. |
| `Brittle` | Number | `1` | Applies or references the 'Brittle' effect/state. |
| `Fragile` | Number | `1` | Applies or references the 'Fragile' effect/state. |
| `ArmorDodgeChance` | Number | `10%, 5%, 15%` | Applies or references the 'ArmorDodgeChance' effect/state. |
| `DamageUp` | Number | `6, -2, 1` | Applies or references the 'DamageUp' effect/state. |
| `Flammable` | Number | `2, 1` | Applies or references the 'Flammable' effect/state. |
| `AddBonusRange` | Number | `2, 1, 10` | Applies or references the 'AddBonusRange' effect/state. |
| `BleedThorns` | Number | `6, 1, 3` | Applies or references the 'BleedThorns' effect/state. |
| `StatusImmunity` | [`Array`](./Arrays.md#array-statusimmunity) | `[ Fear Confusion PermanentConfusion ], [ Freeze, Slow ], Poison` | Applies or references the 'StatusImmunity' effect/state. |
| `SpawnThingOnDeath` | [`Enum/String`](./Enums.md#enum-spawnthingondeath) | `CharmedPooter, CharmedTinyTumor, TheIntruder` | Applies or references the 'SpawnThingOnDeath' effect/state. |
| `StatusEachTurnBegin` | [`Block`](./Items_and_Equipment.md#context-statuseachturnbegin) | `{ ... }` | Applies or references the 'StatusEachTurnBegin' effect/state. |
| `CritChanceUp` | Number | `10, 100, 5` | Applies or references the 'CritChanceUp' effect/state. |
| `KineticSpikes` | Number | `1, 3` | Applies or references the 'KineticSpikes' effect/state. |
| `ReplaceBasicMove` | [`Enum/String`](./Enums.md#enum-replacebasicmove) | `BellyFlop_BasicMove, head_HeadBrandJump, BasicJump` | Applies or references the 'ReplaceBasicMove' effect/state. |
| `AbilityOnBattleStart` | [`Enum/String`](./Enums.md#enum-abilityonbattlestart) | `face_FartFace, head_SpiderInjector, face_FartFaceFixed` | Applies or references the 'AbilityOnBattleStart' effect/state. |
| `AddLevelUpRerolls` | Number | `2, 1, 3` | Applies or references the 'AddLevelUpRerolls' effect/state. |
| `AddManaRegen` | Number | `2, 1, 3` | Applies or references the 'AddManaRegen' effect/state. |
| `BrittleDuringElement` | [`Enum/String`](./Enums.md#enum-brittleduringelement) | `water` | Applies or references the 'BrittleDuringElement' effect/state. |
| `ManaCostReduction` | Number | `2, -2, 1` | Applies or references the 'ManaCostReduction' effect/state. |
| `PoisonThorns` | Number | `2, 1` | Applies or references the 'PoisonThorns' effect/state. |
| `SetFragileImmune` | [`Enum/String`](./Enums.md#enum-setfragileimmune) | `Paper, Cool, ""` | Applies or references the 'SetFragileImmune' effect/state. |
| `TrinketPassiveMultiplierBonus` | Number | `2, 1` | Applies or references the 'TrinketPassiveMultiplierBonus' effect/state. |
| `AddCorpseHealth` | Number | `6, -999999` | Applies or references the 'AddCorpseHealth' effect/state. |
| `Bruise` | Number | `2, 1` | Applies or references the 'Bruise' effect/state. |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Fire, Ice` | Applies or references the 'ElementImmune' effect/state. |
| `Flying` | Number | `1` | Applies or references the 'Flying' effect/state. |
| `SetBrittleImmune` | [`Enum/String`](./Enums.md#enum-setbrittleimmune) | `Paper, JankAlloy, ""` | Applies or references the 'SetBrittleImmune' effect/state. |
| `Trample` | Number | `9, 3` | Applies or references the 'Trample' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `Bleed` | Number | `6, 1, 3` | Applies or references the 'Bleed' effect/state. |
| `BoostHeals` | Number | `2, 1` | Applies or references the 'BoostHeals' effect/state. |
| `ChanceToRevive` | [`Block`](./Items_and_Equipment.md#context-chancetorevive) | `{ ... }, 100, 25` | Applies or references the 'ChanceToRevive' effect/state. |
| `OverrideBasicAttack` | [`Enum/String`](./Enums.md#enum-overridebasicattack) | `BasicTankMelee, BasicSpin, IsaacBasicAttack` | Applies or references the 'OverrideBasicAttack' effect/state. |
| `Poison` | Number | `2, 1, 3` | Applies or references the 'Poison' effect/state. |
| `Quivered` | Number | `2, 1` | Applies or references the 'Quivered' effect/state. |
| `SpellDamageUp` | Number | `1, 3` | Applies or references the 'SpellDamageUp' effect/state. |
| `AddTag` | [`Enum/String`](./Enums.md#enum-addtag) | `rock, bug` | Applies or references the 'AddTag' effect/state. |
| `AmplifyStatus` | [`Enum/String`](./Enums.md#enum-amplifystatus) | `Bleed, Poison` | Applies or references the 'AmplifyStatus' effect/state. |
| `BreakAtAux` | Number | `0` | Applies or references the 'BreakAtAux' effect/state. |
| `DeathRattle` | [`Block`](./Items_and_Equipment.md#context-deathrattle) | `{ ... }, neck_NukeExplode` | Applies or references the 'DeathRattle' effect/state. |
| `DepressionAura` | Number | `2, 1` | Applies or references the 'DepressionAura' effect/state. |
| `DodgeChance_Status` | Number | `10, 40, 15` | Applies or references the 'DodgeChance_Status' effect/state. |
| `ExtraBasicAttacks` | Number | `2, 1` | Applies or references the 'ExtraBasicAttacks' effect/state. |
| `ExtraWeaponAttacks` | Number | `2, 1` | Applies or references the 'ExtraWeaponAttacks' effect/state. |
| `FragileDuringElement` | [`Enum/String`](./Enums.md#enum-fragileduringelement) | `water` | Applies or references the 'FragileDuringElement' effect/state. |
| `MissChance` | Number | `10` | Applies or references the 'MissChance' effect/state. |
| `PermanentMadness` | Number | `1` | Applies or references the 'PermanentMadness' effect/state. |
| `RandomSeededStatModifier` | [`Array`](./Arrays.md#array-randomseededstatmodifier) | `[ 2 -1 ]` | Applies or references the 'RandomSeededStatModifier' effect/state. |
| `SpawnObjectOnPopCorpse` | [`Block`](./Items_and_Equipment.md#context-spawnobjectonpopcorpse) | `{ ... }, Food, Coin` | Applies or references the 'SpawnObjectOnPopCorpse' effect/state. |
| `AddBonusMeleeRange` | Number | `1` | Applies or references the 'AddBonusMeleeRange' effect/state. |
| `AddElementsToBasicAttack` | [`Enum/String`](./Enums.md#enum-addelementstobasicattack) | `Holy, Electric` | Applies or references the 'AddElementsToBasicAttack' effect/state. |
| `AddEndOfCombatRegen` | Number | `12, 999999` | Applies or references the 'AddEndOfCombatRegen' effect/state. |
| `AddKnockbackDamage` | Number | `1` | Applies or references the 'AddKnockbackDamage' effect/state. |
| `AllStatsUpPerDisorder` | Number | `1` | Applies or references the 'AllStatsUpPerDisorder' effect/state. |
| `AlphaTurns` | Number | `1, -1` | Applies or references the 'AlphaTurns' effect/state. |
| `BoneArmorPassive` | Number | `1` | Applies or references the 'BoneArmorPassive' effect/state. |
| `BreakOnElement` | [`Enum/String`](./Enums.md#enum-breakonelement) | `water` | Applies or references the 'BreakOnElement' effect/state. |
| `Burn` | Number | `2` | Applies or references the 'Burn' effect/state. |
| `CantCatchDiseases` | Number | `1` | Applies or references the 'CantCatchDiseases' effect/state. |
| `CantSpreadDiseases` | Number | `1` | Applies or references the 'CantSpreadDiseases' effect/state. |
| `ChanceToBlock` | Number | `10%` | Applies or references the 'ChanceToBlock' effect/state. |
| `Confusion` | Number | `99, 2, 3` | Applies or references the 'Confusion' effect/state. |
| `CopyPassiveSlot` | Number | `1, 0` | Applies or references the 'CopyPassiveSlot' effect/state. |
| `DeathRattleRevive` | [`Enum/String`](./Enums.md#enum-deathrattlerevive) | `DoNothing, tk_PetrifiedPinky` | Applies or references the 'DeathRattleRevive' effect/state. |
| `DisableAbilities` | [`Enum/String`](./Enums.md#enum-disableabilities) | `all_items, basic_attack, all_spells` | Applies or references the 'DisableAbilities' effect/state. |
| `DropAsFamiliarOnArmorBreak` | [`Enum/String`](./Enums.md#enum-dropasfamiliaronarmorbreak) | `FaceGrubFamiliar, HeadGrubFamiliar, NeckGrubFamiliar` | Applies or references the 'DropAsFamiliarOnArmorBreak' effect/state. |
| `FaceArmorPassiveMultiplierBonus` | Number | `2, 1` | Applies or references the 'FaceArmorPassiveMultiplierBonus' effect/state. |
| `HeadArmorPassiveMultiplierBonus` | Number | `2, 1` | Applies or references the 'HeadArmorPassiveMultiplierBonus' effect/state. |
| `IncreaseExplosionSize` | Number | `7, 1` | Applies or references the 'IncreaseExplosionSize' effect/state. |
| `RockyArmorPassive` | Number | `1` | Applies or references the 'RockyArmorPassive' effect/state. |
| `TrinketActiveEffectsMultiplierBonus` | Number | `2, 1` | Applies or references the 'TrinketActiveEffectsMultiplierBonus' effect/state. |
| `TrueShot` | Number | `1` | Applies or references the 'TrueShot' effect/state. |
| `AddInitiative` | Number | `100, -20` | Applies or references the 'AddInitiative' effect/state. |
| `AmplifyKnockback` | Number | `2, 10` | Applies or references the 'AmplifyKnockback' effect/state. |
| `AutoEquipConsumables` | Number | `1` | Applies or references the 'AutoEquipConsumables' effect/state. |
| `BackstabCritChance` | Number | `1, .25` | Applies or references the 'BackstabCritChance' effect/state. |
| `BonusAbility` | [`Enum/String`](./Enums.md#enum-bonusability) | `WasteTime, neck_NukeBonus` | Applies or references the 'BonusAbility' effect/state. |
| `BreakWhenNoShield` | Number | `1` | Applies or references the 'BreakWhenNoShield' effect/state. |
| `CanLevelUpWhenDead` | Number | `1` | Applies or references the 'CanLevelUpWhenDead' effect/state. |
| `ChanceToBlockAndCounter` | [`Block`](./Items_and_Equipment.md#context-chancetoblockandcounter) | `{ ... }, 25%` | Applies or references the 'ChanceToBlockAndCounter' effect/state. |
| `DisablePassiveSlot` | Number | `1, 0` | Applies or references the 'DisablePassiveSlot' effect/state. |
| `DodgeChance` | Number | `25%, 15%` | Applies or references the 'DodgeChance' effect/state. |
| `ExtraBasicMoves_Status` | Number | `1` | Applies or references the 'ExtraBasicMoves_Status' effect/state. |
| `FindExtraItemFromPoolOnBattleEnd` | [`Enum/String`](./Enums.md#enum-findextraitemfrompoolonbattleend) | `pills, combat_reward_easy` | Applies or references the 'FindExtraItemFromPoolOnBattleEnd' effect/state. |
| `FlowersOnEndTurn` | Number | `1` | Applies or references the 'FlowersOnEndTurn' effect/state. |
| `FreezePiercing` | Number | `1` | Applies or references the 'FreezePiercing' effect/state. |
| `IncreaseExplosionDamage` | Number | `2, 1` | Applies or references the 'IncreaseExplosionDamage' effect/state. |
| `IncreaseSpellRange` | Number | `2, 20` | Applies or references the 'IncreaseSpellRange' effect/state. |
| `InjuryImmunity` | Number | `1` | Applies or references the 'InjuryImmunity' effect/state. |
| `InnateElement` | [`Enum/String`](./Enums.md#enum-innateelement) | `Fire, Ice` | Applies or references the 'InnateElement' effect/state. |
| `KillsToMeat` | [`Enum/String`](./Enums.md#enum-killstomeat) | `Food` | Applies or references the 'KillsToMeat' effect/state. |
| `KnockbackImmunity` | Number | `1` | Applies or references the 'KnockbackImmunity' effect/state. |
| `LeaveBehindOnceEachMove` | [`Enum/String`](./Enums.md#enum-leavebehindonceeachmove) | `Scrap, Poop` | Applies or references the 'LeaveBehindOnceEachMove' effect/state. |
| `LevelUpClassOverride` | [`Enum/String`](./Enums.md#enum-levelupclassoverride) | `Jester` | Applies or references the 'LevelUpClassOverride' effect/state. |
| `MoveQuivered` | Number | `2, 1` | Applies or references the 'MoveQuivered' effect/state. |
| `NeckArmorPassiveMultiplierBonus` | Number | `1` | Applies or references the 'NeckArmorPassiveMultiplierBonus' effect/state. |
| `RangedTrueShot` | Number | `1` | Applies or references the 'RangedTrueShot' effect/state. |
| `ReflectProjectiles` | Number | `20%, 25%` | Applies or references the 'ReflectProjectiles' effect/state. |
| `ReplaceBasicAttack` | [`Enum/String`](./Enums.md#enum-replacebasicattack) | `BasicPoke, head_Pestilence` | Applies or references the 'ReplaceBasicAttack' effect/state. |
| `ReplaceSpawnedObjects` | [`Array`](./Arrays.md#array-replacespawnedobjects) | `[ FlamingPoop RandomLivingPoop ], [ Poop RandomLivingPoop ]` | Applies or references the 'ReplaceSpawnedObjects' effect/state. |
| `SetDefaultFacePassive` | [`Enum/String`](./Enums.md#enum-setdefaultfacepassive) | `euphoric` | Applies or references the 'SetDefaultFacePassive' effect/state. |
| `SpawnCatCopyWhenDowned` | [`Block`](./Items_and_Equipment.md#context-spawncatcopywhendowned) | `{ ... }` |  |
| `SpawnNearEnemies` | Number | `1` | Applies or references the 'SpawnNearEnemies' effect/state. |
| `StatusOnSetPieceBreak` | [`Block`](./Items_and_Equipment.md#context-statusonsetpiecebreak) | `{ ... }` |  |
| `Uncontrollable` | Number | `1` | Applies or references the 'Uncontrollable' effect/state. |
| `UpgradeTaggedSpawnsToChampions` | [`Enum/String`](./Enums.md#enum-upgradetaggedspawnstochampions) | `worm, bug` |  |
| `AOEBonus` | Number | `1` | Applies or references the 'AOEBonus' effect/state. |
| `AbilityReaction` | [`Enum/String`](./Enums.md#enum-abilityreaction) | `head_EmoSong` | Applies or references the 'AbilityReaction' effect/state. |
| `AddConstitution` | Number | `2` |  |
| `AddCritMultiplier` | Number | `33%` | Applies or references the 'AddCritMultiplier' effect/state. |
| `AddHiddenTag` | [`Enum/String`](./Enums.md#enum-addhiddentag) | `the_nuke_bearer` | Applies or references the 'AddHiddenTag' effect/state. |
| `AddStartingMana` | Number | `5` |  |
| `AddStatusToFirstSpellEachTurn` | [`Block`](./Items_and_Equipment.md#context-addstatustofirstspelleachturn) | `{ ... }` |  |
| `AllSpellsCostCharge` | Number | `1` | Applies or references the 'AllSpellsCostCharge' effect/state. |
| `AllUnitsExplodeOnDeath` | Number | `5` | Applies or references the 'AllUnitsExplodeOnDeath' effect/state. |
| `AlliesScrambleSpellAfterCast` | Number | `1` | Applies or references the 'AlliesScrambleSpellAfterCast' effect/state. |
| `AllyDamageReduction` | Number | `0` | Applies or references the 'AllyDamageReduction' effect/state. |
| `AlphaAllStatsUp` | Number | `1` | Applies or references the 'AlphaAllStatsUp' effect/state. |
| `AlphaCat` | Number | `1` | Applies or references the 'AlphaCat' effect/state. |
| `AlwaysChosenForLevelUp` | Number | `1` | Applies or references the 'AlwaysChosenForLevelUp' effect/state. |
| `AutocastEachRound` | [`Block`](./Items_and_Equipment.md#context-autocasteachround) | `{ ... }` | Forces the character to automatically cast a specific ability at the start of each combat round. |
| `BackflipWhenTargeted` | [`Block`](./Items_and_Equipment.md#context-backflipwhentargeted) | `{ ... }` | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |
| `BackstabImmunity` | Number | `1` |  |
| `BalanceStats` | Number | `1` | Applies or references the 'BalanceStats' effect/state. |
| `BasicAttackCantMiss` | Number | `1` | Applies or references the 'BasicAttackCantMiss' effect/state. |
| `BasicAttackCritChance` | [`Enum/String`](./Enums.md#enum-basicattackcritchance) | `.1` | Applies or references the 'BasicAttackCritChance' effect/state. |
| `Blind` | Number | `-1` | Applies or references the 'Blind' effect/state. |
| `BlockDamageUnderThreshold` | Number | `1` | Applies or references the 'BlockDamageUnderThreshold' effect/state. |
| `BlockNegativeStatus` | Number | `30%` | Applies or references the 'BlockNegativeStatus' effect/state. |
| `BonusHealthRegenPerDisorder` | Number | `1` |  |
| `BoostReceivedHealing` | Number | `2` | Applies or references the 'BoostReceivedHealing' effect/state. |
| `CanRemoveCursedItems` | Number | `1` | Applies or references the 'CanRemoveCursedItems' effect/state. |
| `CapBasicAttackDamage` | Number | `1` | Applies or references the 'CapBasicAttackDamage' effect/state. |
| `CapMovementAbilityRange` | Number | `1` | Applies or references the 'CapMovementAbilityRange' effect/state. |
| `ChanceToAmbush` | Number | `25%` | Applies or references the 'ChanceToAmbush' effect/state. |
| `Charge` | Number | `5` | Applies or references the 'Charge' effect/state. |
| `CharismaIsMaxStat` | Number | `1` | Applies or references the 'CharismaIsMaxStat' effect/state. |
| `CharmImmunity` | Number | `1` | Applies or references the 'CharmImmunity' effect/state. |
| `ConsumableEffectsMultiplierBonus` | Number | `1` | Applies or references the 'ConsumableEffectsMultiplierBonus' effect/state. |
| `CounterNextAttacks` | Number | `2` | Applies or references the 'CounterNextAttacks' effect/state. |
| `CreateGlobalModifiers` | [`Block`](./Items_and_Equipment.md#context-createglobalmodifiers) | `{ ... }` | Generates global map or encounter rules/modifiers. |
| `CyborgTurns` | [`Block`](./Items_and_Equipment.md#context-cyborgturns) | `{ ... }` |  |
| `DebuffImmunity` | Number | `1` | Applies or references the 'DebuffImmunity' effect/state. |
| `DoubleCastSpellIfManaCostUnderThreshold` | Number | `3` | Applies or references the 'DoubleCastSpellIfManaCostUnderThreshold' effect/state. |
| `DoubleCastSpellsEachTurn_Status` | Number | `1` |  |
| `DoubleCastTaggedSpells` | [`Enum/String`](./Enums.md#enum-doublecasttaggedspells) | `musical` | Applies or references the 'DoubleCastTaggedSpells' effect/state. |
| `DoubleCastWeapons` | Number | `1` | Applies or references the 'DoubleCastWeapons' effect/state. |
| `DoubleReceivedNegativeStatus` | Number | `1` | Applies or references the 'DoubleReceivedNegativeStatus' effect/state. |
| `DoubleReceivedPositiveStatus` | Number | `1` | Applies or references the 'DoubleReceivedPositiveStatus' effect/state. |
| `DropAsFamiliarOnTookDamage` | [`Enum/String`](./Enums.md#enum-dropasfamiliarontookdamage) | `PhantomMaskRock` | Applies or references the 'DropAsFamiliarOnTookDamage' effect/state. |
| `DropSoulJarOnDeath` | [`Enum/String`](./Enums.md#enum-dropsouljarondeath) | `SoulJar_Full` | Applies or references the 'DropSoulJarOnDeath' effect/state. |
| `ExcludeFromEvents` | [`Enum/String`](./Enums.md#enum-excludefromevents) | `Tragedy` | Applies or references the 'ExcludeFromEvents' effect/state. |
| `ExplosionImmunity` | Number | `1` | Applies or references the 'ExplosionImmunity' effect/state. |
| `ExtraBasicAttacks_Status` | Number | `1` | Applies or references the 'ExtraBasicAttacks_Status' effect/state. |
| `ExtraMovePoints` | Number | `1` | Applies or references the 'ExtraMovePoints' effect/state. |
| `ExtraTrinketUses` | Number | `10` | Applies or references the 'ExtraTrinketUses' effect/state. |
| `FaceShield` | Number | `1` | Applies or references the 'FaceShield' effect/state. |
| `FrankBolts` | Number | `1` | Applies or references the 'FrankBolts' effect/state. |
| `GainExtraShield` | Number | `4` | Applies or references the 'GainExtraShield' effect/state. |
| `GlobalFamiliarDamageBoost` | Number | `1` |  |
| `GlobalFamiliarMoveBoost` | Number | `1` |  |
| `GlobalFlowerTrapperAura` | [`Block`](./Items_and_Equipment.md#context-globalflowertrapperaura) | `{ ... }` |  |
| `HPGainBlock` | Number | `1` | Applies or references the 'HPGainBlock' effect/state. |
| `HideSomeHudStuff` | Number | `1` | Applies or references the 'HideSomeHudStuff' effect/state. |
| `IgnoreTiles` | Number | `1` | Applies or references the 'IgnoreTiles' effect/state. |
| `JesterLevelUpRerolls` | Number | `1` | Applies or references the 'JesterLevelUpRerolls' effect/state. |
| `Lifesteal` | Number | `1` | Applies or references the 'Lifesteal' effect/state. |
| `LuckUp` | Number | `222` | Applies or references the 'LuckUp' effect/state. |
| `MakeBasicAttackPull` | Number | `1` | Applies or references the 'MakeBasicAttackPull' effect/state. |
| `MakeSpellsRequireCharge` | Number | `1` | Applies or references the 'MakeSpellsRequireCharge' effect/state. |
| `ModelingClayPassive` | Number | `1` | Applies or references the 'ModelingClayPassive' effect/state. |
| `MoveAndUseAbilityEachTurnBeginIfPossible` | [`Enum/String`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | `face_EatNeverstone` | Applies or references the 'MoveAndUseAbilityEachTurnBeginIfPossible' effect/state. |
| `MoveSpeedMultiplier` | [`Enum/String`](./Enums.md#enum-movespeedmultiplier) | `.5` | Applies or references the 'MoveSpeedMultiplier' effect/state. |
| `MoveTowardsDamageSource` | [`Enum/String`](./Enums.md#enum-movetowardsdamagesource) | `MoveOne` | Applies or references the 'MoveTowardsDamageSource' effect/state. |
| `MovementReaction` | [`Block`](./Items_and_Equipment.md#context-movementreaction) | `{ ... }` | Applies or references the 'MovementReaction' effect/state. |
| `MultiplyCoinsOnBattleStart` | Number | `2` | Applies or references the 'MultiplyCoinsOnBattleStart' effect/state. |
| `MultiplyReceivedHealing` | Number | `2` | Applies or references the 'MultiplyReceivedHealing' effect/state. |
| `OverManaReducesManaCosts` | Number | `1` |  |
| `PhysicalAttacksMiss` | Number | `1` | Applies or references the 'PhysicalAttacksMiss' effect/state. |
| `PreventSpecificInjury` | [`Enum/String`](./Enums.md#enum-preventspecificinjury) | `int` | Applies or references the 'PreventSpecificInjury' effect/state. |
| `ReclaimItemOnBreak` | Number | `1` | Applies or references the 'ReclaimItemOnBreak' effect/state. |
| `ReduceManaCost` | Number | `2` | Applies or references the 'ReduceManaCost' effect/state. |
| `ReduceSpellCostsPerDisorder` | Number | `1` | Applies or references the 'ReduceSpellCostsPerDisorder' effect/state. |
| `ReduceSpellCostsPerParasite` | Number | `1` | Applies or references the 'ReduceSpellCostsPerParasite' effect/state. |
| `RemoveLineOfSightRestrictions` | Number | `1` | Applies or references the 'RemoveLineOfSightRestrictions' effect/state. |
| `ReplaceBlankTilesOnBattleStart` | [`Enum/String`](./Enums.md#enum-replaceblanktilesonbattlestart) | `GlassTile` | Applies or references the 'ReplaceBlankTilesOnBattleStart' effect/state. |
| `RerollItemsOnBattleEnd` | Number | `1` | Applies or references the 'RerollItemsOnBattleEnd' effect/state. |
| `Robot` | [`Block`](./Items_and_Equipment.md#context-robot) | `{ ... }` |  |
| `RockyArmorSalvage` | [`Enum/String`](./Enums.md#enum-rockyarmorsalvage) | `.75` |  |
| `SetFaction` | [`Enum/String`](./Enums.md#enum-setfaction) | `enemies` | Applies or references the 'SetFaction' effect/state. |
| `SetSpellCosts` | Number | `0` | Applies or references the 'SetSpellCosts' effect/state. |
| `SharkySmellsBlood` | Number | `1` | Applies or references the 'SharkySmellsBlood' effect/state. |
| `SpawnCatCloneOnCorpsePopped` | Number | `1` | Applies or references the 'SpawnCatCloneOnCorpsePopped' effect/state. |
| `SpawnCatCopyOnBattleStart` | [`Block`](./Items_and_Equipment.md#context-spawncatcopyonbattlestart) | `{ ... }` |  |
| `SpawnOnDowned` | [`Enum/String`](./Enums.md#enum-spawnondowned) | `CharmedSpookie` | Applies or references the 'SpawnOnDowned' effect/state. |
| `StatusOnEatPill` | [`Block`](./Items_and_Equipment.md#context-statusoneatpill) | `{ ... }` |  |
| `StatusOnTurnEndIfCastNSpells` | [`Block`](./Items_and_Equipment.md#context-statusonturnendifcastnspells) | `{ ... }` |  |
| `StevenBolts` | Number | `1` | Applies or references the 'StevenBolts' effect/state. |
| `StripKnockback` | Number | `1` | Applies or references the 'StripKnockback' effect/state. |
| `TauntAlways` | Number | `1` | Applies or references the 'TauntAlways' effect/state. |
| `TriggerBleedOnBleed` | Number | `1` |  |
| `Undead` | Number | `1` | Applies or references the 'Undead' effect/state. |
| `UpgradeSpawnedPickups` | Number | `1` |  |
| `WeaponActiveEffectsMultiplierBonus` | Number | `2` |  |
| `WeaponDamageMultiplierBonus` | Number | `1` | Applies or references the 'WeaponDamageMultiplierBonus' effect/state. |
| `WeaponPassiveMultiplierBonus` | Number | `2` |  |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `Knockback` | Number | `2, 1` | Applies or references the 'Knockback' effect/state. |
| `Poison` | Number | `2, 1` | Applies or references the 'Poison' effect/state. |
| `Burn` | Number | `1` | Applies or references the 'Burn' effect/state. |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1 .1 ], [ 1 .15 ], [ 1, .25 ]` | Applies or references the 'Fear' effect/state. |
| `Slow` | Number | `1` | Applies or references the 'Slow' effect/state. |
| `Tangled` | [`Array`](./Arrays.md#array-tangled) | `[ 1, .05 ], [ 1, .33 ]` | Applies a tangled/ensnared status effect, often modifying visual sprites. |
| `ChangeTile` | [`Enum/String`](./Enums.md#enum-changetile) | `TallGrassTile, GlassTile, BrambleTile` | Transforms the terrain tile under the target. |
| `DamageOrHealConditionally` | Number | `1` | Applies or references the 'DamageOrHealConditionally' effect/state. |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |
| `Rot` | Number | `1` | Applies or references the 'Rot' effect/state. |
| `SpiderInfested` | Number | `1` | Applies or references the 'SpiderInfested' effect/state. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .1 ], [ 1, .1 ]` | Applies or references the 'Stun' effect/state. |
| `Weakness` | Number | `1, 3` | Applies or references the 'Weakness' effect/state. |
| `Blind` | Number | `1` | Applies or references the 'Blind' effect/state. |
| `Freeze` | [`Array`](./Arrays.md#array-freeze) | `[ 1 .1 ]` | Applies or references the 'Freeze' effect/state. |
| `KnockOutCoin` | Number | `1` | Forces the target to drop coins. |
| `Leech` | Number | `1` | Applies or references the 'Leech' effect/state. |
| `Leeches` | Number | `1` | Applies or references the 'Leeches' effect/state. |
| `MagicWeakness` | Number | `1` | Applies or references the 'MagicWeakness' effect/state. |
| `ManaLeeches` | Number | `1` | Applies or references the 'ManaLeeches' effect/state. |
| `Marked` | Number | `1` | Applies or references the 'Marked' effect/state. |
| `OverrideChainKnockback` | Number | `1` | Applies or references the 'OverrideChainKnockback' effect/state. |
| `PullSourceToTarget` | Number | `1` | Applies or references the 'PullSourceToTarget' effect/state. |
| `SoulLink` | Number | `1` | Applies or references the 'SoulLink' effect/state. |

</details>

---

### Context: `effects`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `BounceObject` | [`Enum/String`](./Enums.md#enum-bounceobject) | `RandomPickup, CharmedDip` | Spawns a physics object that visually bounces off the target. |
| `Burn` | Number | `1` | Applies or references the 'Burn' effect/state. |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1, .5 ], [ 1, .25 ], [ 1, .15 ]` | Applies or references the 'Fear' effect/state. |
| `Grappled` | [`Array`](./Arrays.md#array-grappled) | `[ 1, .50 ], [ 1, .75 ]` | Applies or references the 'Grappled' effect/state. |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |
| `Slow` | Number | `1` | Applies or references the 'Slow' effect/state. |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1, .1 ], [ 1, .25 ]` | Applies or references the 'Stun' effect/state. |
| `Blind` | Number | `1` | Applies or references the 'Blind' effect/state. |
| `Cleave` | Number | `1` | Causes the attack to hit adjacent enemies alongside the primary target. |
| `Confusion` | Number | `2` | Applies or references the 'Confusion' effect/state. |
| `Freeze` | [`Array`](./Arrays.md#array-freeze) | `[ 1, .25 ]` | Applies or references the 'Freeze' effect/state. |
| `VisualFX` | [`Enum/String`](./Enums.md#enum-visualfx) | `Bolt` | Applies or references the 'VisualFX' effect/state. |
| `VisualFXTile` | [`Enum/String`](./Enums.md#enum-visualfxtile) | `WaterConduct` | Applies or references the 'VisualFXTile' effect/state. |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | `true` | If true, triggers the effect even if the character died during the battle. |
| `RandomPermanentStat` | Number | `-1, 1, -3` | Applies or references the 'RandomPermanentStat' effect/state. |
| `RandomMutation` | Number | `1` | Applies or references the 'RandomMutation' effect/state. |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `pills, chapter_specific_item, common_bones` | Generates an item drop from the specified loot pool. |
| `GainCoins` | Number | `1, [ 3 5 ]` | Applies or references the 'GainCoins' effect/state. |
| `RepairTrinket` | Number | `99` | Applies or references the 'RepairTrinket' effect/state. |
| `SetItemAux` | [`Block`](./Items_and_Equipment.md#context-setitemaux) | `{ ... }` | Applies or references the 'SetItemAux' effect/state. |
| `FindItem` | [`Enum/String`](./Enums.md#enum-finditem) | `BoneClub` |  |
| `GainCoinsRange` | [`Block`](./Items_and_Equipment.md#context-gaincoinsrange) | `{ ... }` |  |
| `PermanentConstitution` | Number | `-1` | Applies or references the 'PermanentConstitution' effect/state. |
| `PermanentIntelligence` | Number | `-1` | Applies or references the 'PermanentIntelligence' effect/state. |
| `RepairAll` | Number | `1` | Applies or references the 'RepairAll' effect/state. |
| `RepairWeapon` | Number | `6` | Applies or references the 'RepairWeapon' effect/state. |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `odds` | Number | `1%, 10%, 15%` | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |
| `Freeze` | Number | `1` | Applies or references the 'Freeze' effect/state. |
| `ForceUseAbility_NonStack` | [`Enum/String`](./Enums.md#enum-forceuseability_nonstack) | `Endeavor_Auto` | Applies or references the 'ForceUseAbility_NonStack' effect/state. |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `consumables, parasites` | Generates an item drop from the specified loot pool. |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `tk_WeirdEgg_Spawn, tk_Asteroid, cm_RaptorEggSpawn` | Applies or references the 'ForceUseAbility' effect/state. |
| `RandomMutation` | Number | `1` | Applies or references the 'RandomMutation' effect/state. |
| `DestroyTrinket` | Number | `1` | Applies or references the 'DestroyTrinket' effect/state. |

</details>

---

### Context: `SpawnOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Food, CharmedPinky, CharmedTinyTumor` |  |
| `number` | Number | `1, [ 1, 3 ], 4` |  |

</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Array`](./Arrays.md#array-object) | `[ CharmedFly CharmedMaggot ], CharmedAmoeba, CharmedFlea` |  |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.2, 5%, 100%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `stack_key` | [`Enum/String`](./Enums.md#enum-stack_key) | `CATHIDE` |  |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `tk_SuckStone, head_HitlersToupe, tk_JarOfRadiation` | Applies or references the 'ForceUseAbility' effect/state. |
| `PartialCleanse` | Number | `1` | Applies or references the 'PartialCleanse' effect/state. |
| `Shield` | Number | `2, 1, 3` | Applies or references the 'Shield' effect/state. |
| `ImmediateUseAbility` | [`Block`](./Items_and_Equipment.md#context-immediateuseability) | `{ ... }, head_ThrobbingCrown` | Applies or references the 'ImmediateUseAbility' effect/state. |
| `SpawnCoinAnywhere` | Number | `1` | Applies or references the 'SpawnCoinAnywhere' effect/state. |
| `AddWeaponAux` | Number | `1` | Applies or references the 'AddWeaponAux' effect/state. |
| `Burn` | Number | `3` | Applies or references the 'Burn' effect/state. |
| `Cleanse` | Number | `0` |  |
| `Conditional_HasCleansableDebuffs` | [`Block`](./Items_and_Equipment.md#context-conditional_hascleansabledebuffs) | `{ ... }` |  |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `PreEmptiveCounterNextAttacks` | Number | `1` | Applies or references the 'PreEmptiveCounterNextAttacks' effect/state. |
| `RandomStatUp` | Number | `3` |  |
| `Stealth` | [`Array`](./Arrays.md#array-stealth) | `[ 1 .1 ]` | Applies or references the 'Stealth' effect/state. |

</details>

---

### Context: `StatusOnBreak`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `3` | Applies or references the 'Bruise' effect/state. |
| `ChangeTilesUnder` | [`Enum/String`](./Enums.md#enum-changetilesunder) | `WaterTile` | Applies or references the 'ChangeTilesUnder' effect/state. |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `common` | Generates an item drop from the specified loot pool. |
| `HealthGain` | Number | `10` | Applies or references the 'HealthGain' effect/state. |
| `HealthRegenUp` | Number | `3` | Applies or references the 'HealthRegenUp' effect/state. |
| `PermanentConstitution` | Number | `2` | Applies or references the 'PermanentConstitution' effect/state. |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `DexterityUp` | Number | `1` | Applies or references the 'DexterityUp' effect/state. |
| `FindItem` | [`Enum/String`](./Enums.md#enum-finditem) | `Pearl` | Applies or references the 'FindItem' effect/state. |
| `GainDisorder` | [`Enum/String`](./Enums.md#enum-gaindisorder) | `Psychosis` | Applies or references the 'GainDisorder' effect/state. |
| `IntelligenceUp` | Number | `1` | Applies or references the 'IntelligenceUp' effect/state. |
| `ObjectOnHitCharacter` | [`Enum/String`](./Enums.md#enum-objectonhitcharacter) | `BestBud` | Spawns a specific character or entity upon impact. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Scrap, Catnip, CharmedTinySpider` |  |
| `good` | Boolean | `false` |  |
| `shield_only` | Boolean | `true` |  |
| `spawn_on_death_hit` | Boolean | `false` |  |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.25` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `number` | Number | `1` |  |

</details>

---

### Context: `Temporary`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `2, 1, 3` | Number of stacks or intensity to apply. |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Brace, FreeSpell, SpeedUp` | The status effect to apply. |
| `expires_on_end_turn` | Boolean | `true` |  |
| `turns` | Number | `1` | Duration in turns. |
| `expires_on_begin_turn` | Boolean | `true` | If true, ticks down at the start of the turn rather than the end. |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `BrittleCharismaUp` | Number | `2` | Applies or references the 'BrittleCharismaUp' effect/state. |
| `BrittleConstitutionUp` | Number | `2` | Applies or references the 'BrittleConstitutionUp' effect/state. |
| `BrittleDexterityUp` | Number | `2` | Applies or references the 'BrittleDexterityUp' effect/state. |
| `BrittleIntelligenceUp` | Number | `2` | Applies or references the 'BrittleIntelligenceUp' effect/state. |
| `BrittleLuckUp` | Number | `2` | Applies or references the 'BrittleLuckUp' effect/state. |
| `BrittleSpeedUp` | Number | `2` | Applies or references the 'BrittleSpeedUp' effect/state. |
| `BrittleStrengthUp` | Number | `2` | Applies or references the 'BrittleStrengthUp' effect/state. |
| `CharismaUp` | Number | `1` | Applies or references the 'CharismaUp' effect/state. |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `DexterityUp` | Number | `1` | Applies or references the 'DexterityUp' effect/state. |
| `EquipPermanentItem` | [`Enum/String`](./Enums.md#enum-equippermanentitem) | `BoneClub` | Applies or references the 'EquipPermanentItem' effect/state. |
| `HealthGain` | Number | `5` | Applies or references the 'HealthGain' effect/state. |
| `HealthRegenUp` | Number | `1` | Applies or references the 'HealthRegenUp' effect/state. |
| `IntelligenceUp` | Number | `1` | Applies or references the 'IntelligenceUp' effect/state. |
| `LuckUp` | Number | `1` | Applies or references the 'LuckUp' effect/state. |
| `Shield` | Number | `6` |  |
| `SpeedUp` | Number | `1` | Applies or references the 'SpeedUp' effect/state. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |

</details>

---

### Context: `AddPassivesToMinions`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `2, 5, 4` | Applies or references the 'HealthGain' effect/state. |
| `AddMaxHealth` | Number | `2, 5, 4` | Applies or references the 'AddMaxHealth' effect/state. |
| `DamageUp` | Number | `2, 1` |  |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `Buddy` | [`Enum/String`](./Enums.md#enum-buddy) | `spawner` |  |
| `ReturnBoundItemOnBattleEnd` | Number | `1` |  |
| `Shield` | Number | `2` | Applies or references the 'Shield' effect/state. |
| `tag_filter` | [`Enum/String`](./Enums.md#enum-tag_filter) | `grub_familiar` |  |

</details>

---

### Context: `DurabilityTransform`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `eq` | [`Array`](./Arrays.md#array-eq) | `[ 1 WaterBottle_Half ], [ 0 JarOfNothing ], [ 0 WaterBottle_Empty ]` |  |
| `ge` | [`Array`](./Arrays.md#array-ge) | `[ 3 EstusFlask_Full ], [ 2 WaterBottle_Full ]` |  |

</details>

---

### Context: `TransformItemOnElementInfluence`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Greater_Water, Fire` | Specific element type required or applied. |
| `full_repair` | Boolean | `true` |  |
| `item` | [`Enum/String`](./Enums.md#enum-item) | `EstusFlask_Full, WaterBottle_Full, GallonOfWater` | Item ID to reference. |

</details>

---

### Context: `GainCoinsRange`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `max` | Number | `30, 60, 25` | Maximum coins granted. |
| `min` | Number | `30, 1, 15` | Minimum coins granted. |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | `2, 1, 10` |  |
| `damage` | Number | `0` | The base damage properties of an attack. |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `2, 1` | Applies or references the 'Charge' effect/state. |
| `Thorns` | Number | `1` | Applies or references the 'Thorns' effect/state. |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `DamageUp` | Number | `2` | Applies or references the 'DamageUp' effect/state. |
| `DivineShield` | [`Array`](./Arrays.md#array-divineshield) | `[ 1, .33 ]` | Applies or references the 'DivineShield' effect/state. |
| `DodgeChance_Status` | Number | `5` | Applies or references the 'DodgeChance_Status' effect/state. |
| `RandomStatUp` | Number | `1` |  |
| `RemoveStatus` | [`Enum/String`](./Enums.md#enum-removestatus) | `AlphaCat` | Applies or references the 'RemoveStatus' effect/state. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |

</details>

---

### Context: `Craft`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `bombs, tinkerer_default` |  |
| `slot` | [`Enum/String`](./Enums.md#enum-slot) | `weapon` | Equipment slot (weapon, hat, face, chest, etc.). |
| `works_with_tech` | Boolean | `true` |  |

</details>

---

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `move, spell, attack` | Classification type. |
| `AllStatsUp` | Number | `1` |  |
| `Charge` | Number | `1` | Applies or references the 'Charge' effect/state. |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `HealthRegenUp` | Number | `1` | Applies or references the 'HealthRegenUp' effect/state. |
| `Shield` | Number | `1` | Applies or references the 'Shield' effect/state. |
| `SpellDamageUp` | Number | `1` | Applies or references the 'SpellDamageUp' effect/state. |
| `Thorns` | Number | `1` | Applies or references the 'Thorns' effect/state. |

</details>

---

### Context: `DelayedAutoRevive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `health` | Number | `50%, 30%, 15%` |  |
| `rounds` | Number | `2, 1` |  |

</details>

---

### Context: `PassiveAtHealthThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `mode` | [`Enum/String`](./Enums.md#enum-mode) | `less_or_equal, greater, equal` |  |
| `threshold` | Number | `10, 1, 5` |  |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `number` | [`Array`](./Arrays.md#array-number) | `2, [ 3 6 ], [ 0 1 ]` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `RandomPickup, Bird, Coin` |  |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `BlessingOfPeace` | Number | `1` | Applies or references the 'BlessingOfPeace' effect/state. |
| `Burn` | Number | `1` | Applies or references the 'Burn' effect/state. |
| `DestroyTrinket` | Number | `1` | Applies or references the 'DestroyTrinket' effect/state. |
| `DoubleCastSpellThisTurn` | Number | `1` | Applies or references the 'DoubleCastSpellThisTurn' effect/state. |
| `DrinkWater` | Number | `1` | Applies or references the 'DrinkWater' effect/state. |
| `Revive` | Number | `1` | Applies or references the 'Revive' effect/state. |
| `SpeedUp` | Number | `2` | Applies or references the 'SpeedUp' effect/state. |
| `Temporary` | [`Block`](./Items_and_Equipment.md#context-temporary) | `{ ... }` | A wrapper block for applying status effects that automatically expire. |
| `UseAbility` | [`Enum/String`](./Enums.md#enum-useability) | `neck_DarkFriend` | Forces the character or target to instantly use a specified ability. |
| `Wet` | Number | `1` | Applies or references the 'Wet' effect/state. |

</details>

---

### Context: `CatchProjectiles`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | `1` | Applies or references the 'Quivered' effect/state. |
| `ally_chance` | Number | `15%` |  |
| `chance` | Number | `15%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

### Context: `ItemAuxTransform`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `le` | [`Array`](./Arrays.md#array-le) | `[ 50 MoneyBag_Large ], [ 10 MoneyBag_Small ], [ 25 MoneyBag_Medium ]` |  |
| `ge` | [`Array`](./Arrays.md#array-ge) | `[ 20 BlackShard_Glowing ], [ 10 NuclearKnife_Glowing ]` |  |
| `lt` | [`Array`](./Arrays.md#array-lt) | `[ 10 NuclearKnife ]` |  |

</details>

---

### Context: `StatusAlliesOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | `2, 1` | Applies or references the 'SpeedUp' effect/state. |
| `Brace` | Number | `1` | Applies or references the 'Brace' effect/state. |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `IntelligenceUp` | Number | `1` |  |
| `LuckUp` | Number | `1` |  |
| `Shield` | Number | `5` |  |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |

</details>

---

### Context: `StatusOnSetPieceBreak`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `rare` |  |
| `PermanentCharisma` | Number | `1` |  |
| `PermanentConstitution` | Number | `1` |  |
| `PermanentDexterity` | Number | `1` |  |
| `PermanentIntelligence` | Number | `1` |  |
| `PermanentLuck` | Number | `1` |  |
| `PermanentSpeed` | Number | `1` |  |
| `PermanentStrength` | Number | `1` |  |
| `set` | [`Enum/String`](./Enums.md#enum-set) | `Recycled` |  |

</details>

---

### Context: `AddDamageToElementDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `2, 1` | The base damage properties of an attack. |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Electric, Fire, Ice` | Specific element type required or applied. |

</details>

---

### Context: `AddSelfStatusToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `2, 1, 3` | Fires a randomized number of magic missiles. |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `DustDash` | Applies or references the 'ForceUseAbility' effect/state. |
| `Quivered` | [`Array`](./Arrays.md#array-quivered) | `[ 1 .10 ]` | Applies or references the 'Quivered' effect/state. |
| `Shield` | Number | `1` | Applies or references the 'Shield' effect/state. |

</details>

---

### Context: `StatusOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SafeDie` | Number | `1` | Applies or references the 'SafeDie' effect/state. |
| `Brace` | [`Enum/String`](./Enums.md#enum-brace) | `item_aux` | Applies or references the 'Brace' effect/state. |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `common` | Generates an item drop from the specified loot pool. |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `tk_DybbuksRib` | Applies or references the 'ForceUseAbility' effect/state. |
| `RandomMagicMissile` | Number | `4` | Fires a randomized number of magic missiles. |
| `SetHealth` | Number | `50%` | Applies or references the 'SetHealth' effect/state. |
| `StealthUntilBasicAttack` | Number | `1` | Applies or references the 'StealthUntilBasicAttack' effect/state. |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `2` | Applies or references the 'Charge' effect/state. |
| `SpeedUp` | Number | `1` | Applies or references the 'SpeedUp' effect/state. |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `ImmediateUseAbility` | [`Enum/String`](./Enums.md#enum-immediateuseability) | `head_MagnetoAttract` | Applies or references the 'ImmediateUseAbility' effect/state. |

</details>

---

### Context: `StatusOnKillEnemy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `Brace` | Number | `1` | Applies or references the 'Brace' effect/state. |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `head_CatChestPound` | Applies or references the 'ForceUseAbility' effect/state. |
| `LuckUp` | Number | `1` | Applies or references the 'LuckUp' effect/state. |
| `ManaGain` | Number | `2` | Applies or references the 'ManaGain' effect/state. |

</details>

---

### Context: `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `99, 1` | Quantity. |
| `Charmed` | Number | `2` | Applies or references the 'Charmed' effect/state. |
| `Confusion` | Number | `2` | Applies or references the 'Confusion' effect/state. |
| `Fear` | Number | `2` | Applies or references the 'Fear' effect/state. |
| `Freeze` | Number | `2` | Applies or references the 'Freeze' effect/state. |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `Charge` | Number | `1, 3` | Applies or references the 'Charge' effect/state. |
| `HealthGain` | Number | `3` | Applies or references the 'HealthGain' effect/state. |
| `SpeedUp` | Number | `1` | Applies or references the 'SpeedUp' effect/state. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `reduction` | Number | `2, 1` |  |
| `class` | [`Enum/String`](./Enums.md#enum-class) | `Colorless` | Character class identifier. |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `wp_Blackjack_Auto, wp_ZodiacsSixshooter_Auto` | ID of the ability to trigger or reference. |
| `create_temp_ability` | Boolean | `true` |  |
| `enemies_only` | Boolean | `true` |  |
| `on_self_move_too` | Boolean | `true` |  |

</details>

---

### Context: `PassiveIfStrAuxEquals`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `value` | [`Enum/String`](./Enums.md#enum-value) | `dex, str, con` |  |

</details>

---

### Context: `PassiveWhenOnTile`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tile` | [`Array`](./Arrays.md#array-tile) | `[ WaterTile ], [ TallGrassTile TallFlowerTile ]` |  |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `PermanentCharisma` | Number | `1` | Applies or references the 'PermanentCharisma' effect/state. |
| `PermanentConstitution` | Number | `1` | Applies or references the 'PermanentConstitution' effect/state. |
| `PermanentDexterity` | Number | `1` | Applies or references the 'PermanentDexterity' effect/state. |
| `PermanentIntelligence` | Number | `1` | Applies or references the 'PermanentIntelligence' effect/state. |
| `PermanentLuck` | Number | `1` | Applies or references the 'PermanentLuck' effect/state. |
| `PermanentSpeed` | Number | `1` | Applies or references the 'PermanentSpeed' effect/state. |
| `PermanentStrength` | Number | `1` | Applies or references the 'PermanentStrength' effect/state. |

</details>

---

### Context: `StatusAfterXStacks`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stack_key` | [`Enum/String`](./Enums.md#enum-stack_key) | `FANNY_PACK, EMPTY_GENERATOR` |  |
| `threshold` | Number | `12, 3` |  |
| `ExtraBasicMoves_Status` | Number | `1` | Applies or references the 'ExtraBasicMoves_Status' effect/state. |
| `RefreshActPoints` | Number | `1` | Applies or references the 'RefreshActPoints' effect/state. |
| `expires_on_end_turn` | Boolean | `true` |  |

</details>

---

### Context: `Conditional_HasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Thorns, Bleed` | The specific status effect ID to remove. |
| `FlatLeechIfDamaged` | Number | `3` | Applies or references the 'FlatLeechIfDamaged' effect/state. |
| `ImmediateUseAbility_Instant` | [`Enum/String`](./Enums.md#enum-immediateuseability_instant) | `head_CrownOfHorns` | Applies or references the 'ImmediateUseAbility_Instant' effect/state. |

</details>

---

### Context: `DeathRattle`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `set_HumanFleshSetCurse, set_MummySetCurse, MiniNukeExplodey` |  |
| `pop_corpse` | Boolean | `false` |  |

</details>

---

### Context: `DoDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0` | The flat damage amount. |
| `damage_tiles` | [`Enum/String`](./Enums.md#enum-damage_tiles) | `all` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` | The classification of the damage (e.g., spell, melee). |

</details>

---

### Context: `SetItemAux`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `slot` | [`Enum/String`](./Enums.md#enum-slot) | `face, trinket, head` | Equipment slot (weapon, hat, face, chest, etc.). |
| `value` | [`Enum/String`](./Enums.md#enum-value) | `item_aux-1, item_aux+1, item_aux+2` |  |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `number` | Number | `3, [ 1 2 ]` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `RandomPickup` |  |

</details>

---

### Context: `StackingFlowerTrail`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stack_key` | [`Enum/String`](./Enums.md#enum-stack_key) | `FLOWER_SET` |  |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `AbilityHealthThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `cm_HealPercent_Auto` | ID of the ability to trigger or reference. |
| `aux` | Number | `25` |  |
| `even_if_stunned` | Boolean | `true` |  |
| `immediate` | Boolean | `true` |  |
| `threshold` | [`Equation`](./Enums.md#enum-mathequation) | `"max(X*.5, 1)"` |  |

</details>

---

### Context: `AddStatusToAllDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `must_do_damage` | Boolean | `true` |  |
| `BonusKnockbackDamage` | Number | `3` | Applies or references the 'BonusKnockbackDamage' effect/state. |
| `Rot` | Number | `1` | Applies or references the 'Rot' effect/state. |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `rock, humanoid` | The specific string tag to check for. |
| `BonusCritChance` | Number | `50` |  |
| `BonusKnockbackDamage` | Number | `5` | Applies or references the 'BonusKnockbackDamage' effect/state. |
| `OverrideChainKnockback` | Number | `0` | Applies or references the 'OverrideChainKnockback' effect/state. |

</details>

---

### Context: `Conditional_OncePerBattle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ReduceManaCost` | Number | `1` | Applies or references the 'ReduceManaCost' effect/state. |
| `Shield` | Number | `3` | Applies or references the 'Shield' effect/state. |
| `ShowText` | String | `"COMBAT_POPUP_BRAINSTORM"` | Applies or references the 'ShowText' effect/state. |
| `SpellDamageUp` | Number | `1` | Applies or references the 'SpellDamageUp' effect/state. |
| `key` | [`Enum/String`](./Enums.md#enum-key) | `JewelOfDrog` |  |

</details>

---

### Context: `CounterAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `head_IronJaw, attack, neck_TentacleArmorCounter` | ID of the ability to trigger or reference. |
| `melee_only` | Boolean | `true` |  |
| `ranged_only` | Boolean | `true` |  |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0, 1` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Electric ]` |  |

</details>

---

### Context: `StatusEveryXSpellCasts`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `3, 4` | Number of stacks or intensity to apply. |
| `Charge` | Number | `3` | Applies or references the 'Charge' effect/state. |
| `IntelligenceUp` | Number | `2` | Applies or references the 'IntelligenceUp' effect/state. |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `3` | Applies or references the 'Charge' effect/state. |
| `HealthGain` | Number | `3` | Applies or references the 'HealthGain' effect/state. |
| `DivineShield` | Number | `1` |  |

</details>

---

### Context: `AddStatusToElementDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Electric, Fire` | Specific element type required or applied. |
| `Burn` | Number | `1` | Applies or references the 'Burn' effect/state. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .1 ]` | Applies or references the 'Stun' effect/state. |

</details>

---

### Context: `ArmorBreakOnHit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance_to_break` | Number | `5%, 10%` |  |
| `durability_loss` | Number | `0` |  |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `set_PlanetSetGravity, face_StevenMask2` | The ID of the ability to autocast. |
| `even_if_stunned` | Boolean | `true` | If true, bypasses stun and hard-CC restrictions to cast anyway. |

</details>

---

### Context: `BoostWeaponDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `crit_chance` | [`Enum/String`](./Enums.md#enum-crit_chance) | `.5, 1` |  |
| `damage` | Number | `0` | The base damage properties of an attack. |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `ShadowstepDodge, BlinkDodge` | ID of the ability to trigger or reference. |
| `chance` | Number | `33%, 10%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

### Context: `ChanceToRevive`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `health` | Number | `50%, 34%` |  |
| `stacks` | Number | `100, 50` | Number of stacks or intensity to apply. |

</details>

---

### Context: `ElementalManaCostReduction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Array`](./Arrays.md#array-element) | `[ Holy ], [ Fire Earth ]` | Specific element type required or applied. |
| `reduction` | Number | `1` |  |

</details>

---

### Context: `ObjectOnHitCharacter`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CharmedLeech, CharmedTinySpider` | The entity ID of the character to spawn (e.g., CharmedFlea). |
| `stacks` | Number | `1, "floor(lck/4)"` | Number of stacks or intensity to apply. |

</details>

---

### Context: `RefreshEquipmentAbilityOnElement`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Electric` | Specific element type required or applied. |
| `text` | String | `"COMBAT_POPUP_RECHARGED"` |  |

</details>

---

### Context: `SpawnCatCopyWhenDowned`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `PlayerCat_AncestralShade, PlayerCat_NecroShade` |  |
| `prevent_chain_tag` | [`Enum/String`](./Enums.md#enum-prevent_chain_tag) | `ancestorset_shade, necroset_shade` |  |

</details>

---

### Context: `SpawnItemLinkedFamiliar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean | `true` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `ZaratanaFamiliar, PyrophinaFamiliar` |  |

</details>

---

### Context: `cost`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `charge` | Number | `1` |  |
| `mana` | Number | `0` |  |

</details>

---

### Context: `global_passives`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `GlobalEnemyAutoRevive` | Number | `100%, 30%` | Applies or references the 'GlobalEnemyAutoRevive' effect/state. |
| `NoCorpses` | Number | `1` | Applies or references the 'NoCorpses' effect/state. |
| `RealTimePressure` | Number | `5` | Applies or references the 'RealTimePressure' effect/state. |

</details>

---

### Context: `meta`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `is_basic_attack` | Boolean | `false` |  |
| `is_weapon` | Boolean | `true` |  |

</details>

---

### Context: `AddAdvantageToEvent`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `add` | Number | `5` |  |
| `options` | [`Array`](./Arrays.md#array-options) | `[ smash bash open ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `treasure_box` | Classification type. |

</details>

---

### Context: `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bounty` | Number | `1` | Applies or references the 'Bounty' effect/state. |
| `Marked` | Number | `1` | Applies or references the 'Marked' effect/state. |
| `count` | Number | `1` | Quantity. |

</details>

---

### Context: `Conditional_PartyMember`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_IsSelf` | [`Block`](./Abilities_and_Spells.md#context-conditional_isself) | `{ ... }` | Conditional trigger: Executes nested logic if the target is the caster themselves. |

</details>

---

### Context: `PassiveAtStatThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `mode` | [`Enum/String`](./Enums.md#enum-mode) | `less_or_equal` |  |

</details>

---

### Context: `SpawnObjectOnPopCorpse`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `2` | Quantity. |
| `except_tiny` | Boolean | `true` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CharmedTinySpider` |  |

</details>

---

### Context: `StatusAfterCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TempMeleeRangeUp` | Number | `1` | Applies or references the 'TempMeleeRangeUp' effect/state. |
| `TempRangeUp` | Number | `1` | Applies or references the 'TempRangeUp' effect/state. |
| `UseAbility` | [`Enum/String`](./Enums.md#enum-useability) | `neck_DarkFriend` | Forces the character or target to instantly use a specified ability. |

</details>

---

### Context: `StatusOnFallAsleep`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `FillMana` | Number | `1` | Applies or references the 'FillMana' effect/state. |
| `HealRandomInjury` | Number | `1` | Applies or references the 'HealRandomInjury' effect/state. |

</details>

---

### Context: `StatusOnPopCorpse`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `5` | Applies or references the 'HealthGain' effect/state. |
| `RepairTrinket` | Number | `1` | Applies or references the 'RepairTrinket' effect/state. |
| `RepairWeapon` | Number | `1` | Applies or references the 'RepairWeapon' effect/state. |

</details>

---

### Context: `StatusOnTakeHealthOrShieldDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | [`Array`](./Arrays.md#array-divineshield) | `[ 1 .33 ], [ 1 .5 ]` | Applies or references the 'DivineShield' effect/state. |
| `Metronome` | Number | `1` | Executes a random musical or metronome ability. |

</details>

---

### Context: `TintItem`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `add` | [`Array`](./Arrays.md#array-add) | `[ 0.05 0.05 0.05 ]` |  |
| `ignore_if_str_aux_equals` | [`Enum/String`](./Enums.md#enum-ignore_if_str_aux_equals) | `ModelingClay_Default` |  |
| `mul` | [`Array`](./Arrays.md#array-mul) | `[ 0.45 0.3 0.25 ]` |  |

</details>

---

### Context: `threshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `1, 0` |  |
| `con` | Number | `0` |  |

</details>

---

### Context: `AIControlNextTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | `true` |  |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `AbilityOnRoundEndOnce`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `wp_SignalAmplifierSpawnTerminator` | ID of the ability to trigger or reference. |
| `even_of_stunned` | Boolean | `true` |  |

</details>

---

### Context: `AddStatusToFirstSpellEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_IsSelf` | [`Block`](./Abilities_and_Spells.md#context-conditional_isself) | `{ ... }` |  |
| `Else` | [`Block`](./Items_and_Equipment.md#context-else) | `{ ... }` |  |

</details>

---

### Context: `AddStatusToKnockbackDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1, .1 ]` | Applies or references the 'Stun' effect/state. |

</details>

---

### Context: `AllyDodgeChanceAura`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `25%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `range` | Number | `1` | Distance or area of effect in tiles. |

</details>

---

### Context: `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `GainDisorderFromPool` | [`Enum/String`](./Enums.md#enum-gaindisorderfrompool) | `all_disorders` | Applies or references the 'GainDisorderFromPool' effect/state. |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `BackflipDodge` | The specific dodge ability to trigger (e.g., DestroyerDodge). |
| `stacks` | Number | `2` | Number of stacks or intensity to apply. |

</details>

---

### Context: `BouncyProjectiles`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number | `1` |  |
| `max_range` | Number | `2` |  |

</details>

---

### Context: `CastAgainWithStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | Number | `1` | Applies or references the 'OverrideDamage' effect/state. |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `ChanceToBlockAndCounter`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean | `true` |  |
| `chance` | Number | `100%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

### Context: `ChanceToForceEvent`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `25%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `event` | [`Enum/String`](./Enums.md#enum-event) | `Blessing` |  |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `odds` | [`Enum/String`](./Enums.md#enum-odds) | `.3, .1` | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. |

</details>

---

### Context: `Conditional_Boss`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `-2, -1` | Applies or references the 'AllStatsUp' effect/state. |

</details>

---

### Context: `Conditional_ManaThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RepairTrinket` | Number | `1` | Applies or references the 'RepairTrinket' effect/state. |
| `threshold_flat` | Number | `0` |  |

</details>

---

### Context: `ConvertDamageToScaledStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DelayedPain` | Number | `1` | Applies or references the 'DelayedPain' effect/state. |
| `stacks` | Number | `3` | Number of stacks or intensity to apply. |

</details>

---

### Context: `CreateGlobalModifiers`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `NextPlayerCatTakesExtraTurn` | Number | `1` | Applies or references the 'NextPlayerCatTakesExtraTurn' effect/state. |
| `NoCorpses` | Number | `1` | Applies or references the 'NoCorpses' effect/state. |

</details>

---

### Context: `CyborgTurns`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TakeBonusTurnWithAIControl` | [`Block`](./Items_and_Equipment.md#context-takebonusturnwithaicontrol) | `{ ... }` |  |
| `stacks` | Number | `1` |  |

</details>

---

### Context: `DestroyEquipmentAndAttachParasite`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.75` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `pool` | [`Array`](./Arrays.md#array-pool) | `[ FaceGrub HeadGrub NeckGrub ]` | The item pool to draw the parasite from. |

</details>

---

### Context: `Eternal`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `health_percent` | Number | `100%` |  |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `FlyDamageIncrease`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | `true` |  |
| `stacks` | Number | `2` | Number of stacks or intensity to apply. |

</details>

---

### Context: `ForceUseAbilityOnTarget`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `head_MiniMoonArmorAsteroid` | ID of the ability to trigger or reference. |
| `chance` | Number | `25%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

### Context: `ImmediateUseAbility`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `wp_NuclearKnifeExplode` | ID of the ability to trigger or reference. |
| `even_if_stunned` | Boolean | `true` |  |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `distance` | Number | `3` | The distance in tiles to knock the target away. |
| `stacks` | Number | `5` | Number of stacks or intensity to apply. |

</details>

---

### Context: `KnockbackIfCrit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | `10` |  |
| `override_chain_knockback` | Number | `10` |  |

</details>

---

### Context: `ManaGainRange`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `max` | Number | `4` |  |
| `min` | Number | `0` |  |

</details>

---

### Context: `ObjectDetector`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `10%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CharmedDip` |  |

</details>

---

### Context: `PassiveAfterXKills`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `3` | Number of stacks or intensity to apply. |

</details>

---

### Context: `PassiveIfWeaponIsUsable`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `2, 1` | Applies or references the 'Brace' effect/state. |

</details>

---

### Context: `PoopWhenHit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `25%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Poop` |  |

</details>

---

### Context: `RemoveStatusStacks`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `1` | The number of stacks to remove. |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Thorns` | The specific status effect ID to remove. |

</details>

---

### Context: `ReviveNextRound`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | `2` | Applies or references the 'Shield' effect/state. |
| `revive_health` | Number | `100%` | The flat amount of health to revive with. |

</details>

---

### Context: `ScaldingOrbMoonBossOneShot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CompleteItemQuest` | [`Enum/String`](./Enums.md#enum-completeitemquest) | `ScaldingOrb` | Applies or references the 'CompleteItemQuest' effect/state. |
| `RemoveItem` | [`Enum/String`](./Enums.md#enum-removeitem) | `ScaldingOrb` | Applies or references the 'RemoveItem' effect/state. |

</details>

---

### Context: `SpawnCatCopyOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `PlayerCat_MiniMiniMe` |  |
| `prevent_chain_tag` | [`Enum/String`](./Enums.md#enum-prevent_chain_tag) | `minime_clone` |  |

</details>

---

### Context: `SpawnOnDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `faction` | [`Enum/String`](./Enums.md#enum-faction) | `solitary_enemies` |  |
| `obj` | [`Enum/String`](./Enums.md#enum-obj) | `BeefyCharmedLeech` |  |

</details>

---

### Context: `SpawnRandomPickupsOnTaggedUnitKilled`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | [`Array`](./Arrays.md#array-count) | `[ 2 3 ]` | Quantity. |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `poop` | Specific entity tag required. |

</details>

---

### Context: `StatusAfterXTurns`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `tk_MadGhost_Spawn` | Applies or references the 'ForceUseAbility' effect/state. |
| `stacks` | Number | `3` | Number of stacks or intensity to apply. |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `RepairTrinket` | Number | `1` | Applies or references the 'RepairTrinket' effect/state. |

</details>

---

### Context: `StatusOnBackstab`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `2` | Applies or references the 'HealthGain' effect/state. |
| `SerratedClaws` | Number | `1` | Applies or references the 'SerratedClaws' effect/state. |

</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` | Applies or references the 'Charge' effect/state. |
| `Shield` | Number | `1` | Applies or references the 'Shield' effect/state. |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `chapter_common` | Generates an item drop from the specified loot pool. |
| `RandomMagicMissile` | Number | `6` | Fires a randomized number of magic missiles. |

</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | `2` | Applies or references the 'LuckUp' effect/state. |
| `Shield` | [`Enum/String`](./Enums.md#enum-shield) | `X` | Applies or references the 'Shield' effect/state. |

</details>

---

### Context: `StatusOnTurnEndIfCastNSpells`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DoubleCastSpell` | Number | `1` |  |
| `spells` | Number | `5` |  |

</details>

---

### Context: `StatusOnUseBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `HealthGain` | Number | `1` | Applies or references the 'HealthGain' effect/state. |

</details>

---

### Context: `TakeBonusTurnWithAIControl`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`CyborgTurns`](./Items_and_Equipment.md#context-cyborgturns)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `end_of_round` | Boolean | `true` |  |
| `include_spells` | Boolean | `true` |  |

</details>

---

### Context: `TransformWeapon`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `from` | [`Enum/String`](./Enums.md#enum-from) | `Necro_SoulDagger_Charged` | The original weapon ID. |
| `to` | [`Enum/String`](./Enums.md#enum-to) | `Necro_SoulDagger_Uncharged` | The transformed weapon ID. |

</details>

---

### Context: `damage_instance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status` | Classification type. |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |

</details>

---

### Context: `passive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Metal` | Number | `1` | Applies or references the 'Metal' effect/state. |

</details>

---

### Context: `AddPassivesToCharmed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |

</details>

---

### Context: `AddSelfStatusToWeapons`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RepairWeapon` | [`Array`](./Arrays.md#array-repairweapon) | `[ 1 .25 ]` | Applies or references the 'RepairWeapon' effect/state. |

</details>

---

### Context: `AddStatusToBackstabs`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Leech` | Number | `1` | Applies or references the 'Leech' effect/state. |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Leech` | Number | `1` | Applies or references the 'Leech' effect/state. |

</details>

---

### Context: `AlluringDoodieEater`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `10%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

### Context: `BuffImmunity`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `exclude` | [`Enum/String`](./Enums.md#enum-exclude) | `SpellDamageUp` |  |

</details>

---

### Context: `CatPartsSizeScale`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `head` | Number | `1.3` |  |

</details>

---

### Context: `Conditional_Ally`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | `1` | Applies or references the 'ManaGain' effect/state. |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMutation` | Number | `1` | Applies or references the 'RandomMutation' effect/state. |

</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Leeches` | Number | `1` | Applies or references the 'Leeches' effect/state. |

</details>

---

### Context: `Conditional_HasCleansableDebuffs`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `VisualFX` | [`Enum/String`](./Enums.md#enum-visualfx) | `Cleanse` |  |

</details>

---

### Context: `Conditional_HealthThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `threshold_flat` | Number | `3` | A flat numerical health value threshold. |

</details>

---

### Context: `Conditional_PlayerCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` | Applies or references the 'Charge' effect/state. |

</details>

---

### Context: `Conditional_RandomChance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `odds` | Number | `20%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

### Context: `CritsApplyStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |

</details>

---

### Context: `Else`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddStatusToFirstSpellEachTurn`](./Items_and_Equipment.md#context-addstatustofirstspelleachturn)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Webbed` | Number | `1` |  |

</details>

---

### Context: `GlobalFlowerTrapperAura`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Tangled` | [`Array`](./Arrays.md#array-tangled) | `[ 1, .1 ]` |  |

</details>

---

### Context: `GlobalMeleeRevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | `5` |  |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `water` | Specific element type required or applied. |

</details>

---

### Context: `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `1` | Applies or references the 'Brace' effect/state. |

</details>

---

### Context: `PassiveWhileShielded`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Number | `3` | Applies or references the 'HealthRegenUp' effect/state. |

</details>

---

### Context: `RandomPermanentStatsDistinct`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusOnEatPill`](./Items_and_Equipment.md#context-statusoneatpill)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stats` | [`Array`](./Arrays.md#array-stats) | `[ 1 -1 ]` |  |

</details>

---

### Context: `Robot`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean | `true` |  |

</details>

---

### Context: `ScaledStatusOnHolyShieldBlock`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |

</details>

---

### Context: `StatDependentPassive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddDamageToBasicAttack` | [`Equation`](./Enums.md#enum-mathequation) | `"min(min(min(min(min(min(str,dex),int),con),lck),spd),cha...` | Applies or references the 'AddDamageToBasicAttack' effect/state. |

</details>

---

### Context: `StatusAdjacentOnTheirTurnEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceMoveAway` | Number | `1` | Applies or references the 'ForceMoveAway' effect/state. |

</details>

---

### Context: `StatusAllCharactersOnSpawn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |

</details>

---

### Context: `StatusAlliesOnDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `2` | Applies or references the 'DivineShield' effect/state. |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `face_FartFace` | Applies or references the 'ForceUseAbility' effect/state. |

</details>

---

### Context: `StatusIfUnusedActPoints`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `BackflipWhenTargeted` | [`Enum/String`](./Enums.md#enum-backflipwhentargeted) | `X` | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |

</details>

---

### Context: `StatusOnBreakItem`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | `3` | Applies or references the 'Shield' effect/state. |

</details>

---

### Context: `StatusOnDodge`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Number | `2` | Applies or references the 'DodgeChance_Status' effect/state. |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RepairTrinket` | Number | `1` | Applies or references the 'RepairTrinket' effect/state. |

</details>

---

### Context: `StatusOnEatPill`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomPermanentStatsDistinct` | [`Block`](./Items_and_Equipment.md#context-randompermanentstatsdistinct) | `{ ... }` |  |

</details>

---

### Context: `StatusOnEnemyDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` | Applies or references the 'Charge' effect/state. |

</details>

---

### Context: `StatusOnHealed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | `1` | Applies or references the 'Shield' effect/state. |

</details>

---

### Context: `StatusOnPickupCoins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `GainCoins` | Number | `1` | Applies or references the 'GainCoins' effect/state. |

</details>

---

### Context: `StatusWhenAllySpendsMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `2` | Applies or references the 'Charge' effect/state. |

</details>

---

### Context: `TempPassiveUntilSettled`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LimitHeal` | Number | `0` | Applies or references the 'LimitHeal' effect/state. |

</details>

---

### Context: `TunnelVision`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `crit_chance` | Number | `50%` |  |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ApplyPassives`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Conditional_Adjacent`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Conditional_Shielded`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ModifyAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `PassiveWhenDead`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `PassiveWhileHasDurability`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ScaledStatusAlliesOnSpendMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ScaledStatusOnSpendMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusAlliesEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusEachRoundEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusOnCollectPickup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusOnFullMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `bonus_passives`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `str_aux_is_copy_ability`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

