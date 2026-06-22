# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Items & Equipment

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1217) |
| :--- | :--- | :--- | :--- |
| `desc` | String | Localization key for the item's desc. | 1217 |
| `name` | String | Localization key for the item's name. | 1206 |
| `frame` | Number |  | 1106 |
| [`kind`](./Enums.md#enum-kind) | Enum/String |  | 1106 |
| [`rarity`](./Enums.md#enum-rarity) | Enum/String |  | 967 |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | Passives granted by equipping this. | 823 |
| [`set`](./Enums.md#enum-set) | Enum/String |  | 765 |
| [`ability`](./Enums.md#enum-ability) | Enum/String | ID of the ability to trigger or reference. | 365 |
| `shield` | Number |  | 186 |
| `durability` | Number | Maximum uses before breaking. | 171 |
| `pieces_required` | Number |  | 101 |
| `cursed` | Boolean |  | 77 |
| `cha` | Number |  | 75 |
| `consumable` | Boolean |  | 64 |
| `spd` | Number |  | 60 |
| `con` | Number |  | 57 |
| `int` | Number |  | 54 |
| `lck` | Number |  | 44 |
| `quest_item` | Boolean |  | 40 |
| `parasite` | Boolean |  | 36 |
| `aux` | Number |  | 33 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum/String |  | 29 |
| `str` | Number |  | 28 |
| `dex` | Number |  | 22 |
| [`quest_reward_item`](./Enums.md#enum-quest_reward_item) | Enum/String |  | 22 |
| `indestructible` | Boolean |  | 20 |
| `divine_shield` | Number |  | 17 |
| `legacy_quest` | Boolean |  | 17 |
| [`hint_destination`](./Enums.md#enum-hint_destination) | Enum/String |  | 16 |
| [`str_aux_initialize`](./Enums.md#enum-str_aux_initialize) | Enum/String |  | 15 |
| `dont_destroy_on_0` | Boolean |  | 13 |
| [`global_tags`](./Arrays.md#array-global_tags) | Array |  | 12 |
| `max_durability` | Number |  | 11 |
| [`on_store`](./Enums.md#enum-on_store) | Enum/String |  | 8 |
| `name_mod` | String |  | 7 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 6 |
| [`hint_prerequisite_flag`](./Enums.md#enum-hint_prerequisite_flag) | Enum/String |  | 5 |
| `failable` | Boolean |  | 4 |
| [`global_passives`](./Items_and_Equipment.md#context-global_passives) | Block |  | 4 |
| `randomize_piece_frames` | Boolean |  | 4 |
| `str_aux_is_copy_passive` | Boolean |  | 4 |
| `fragile` | Boolean |  | 3 |
| [`icon_hint`](./Enums.md#enum-icon_hint) | Enum/String |  | 3 |
| `max_health` | Number |  | 3 |
| `reset_aux_on_store` | Number |  | 3 |
| `sticky` | Boolean |  | 3 |
| `weightless` | Boolean |  | 3 |
| [`keyword_tooltips`](./Items_and_Equipment.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear when hovering over the ability. | 2 |
| [`passive`](./Items_and_Equipment.md#context-passive) | Block |  | 2 |
| `prevent_level_up` | Boolean |  | 2 |
| [`quest_item_alias`](./Enums.md#enum-quest_item_alias) | Enum/String |  | 2 |
| `speed` | Number |  | 2 |
| [`str_aux_is_copy_ability`](./Items_and_Equipment.md#context-str_aux_is_copy_ability) | Block |  | 2 |
| `str_aux_is_copy_item_passive` | Boolean |  | 2 |
| [`Set`](./Enums.md#enum-set) | Enum/String | Applies or references the 'Set' effect/state. | 1 |
| `aux_is_catid` | Boolean |  | 1 |
| `cant_equip_to_colorless` | Boolean |  | 1 |
| `degrade_after_adventure` | Boolean |  | 1 |
| [`equip_sound`](./Enums.md#enum-equip_sound) | Enum/String |  | 1 |
| `force_sticky` | Boolean |  | 1 |
| [`reset_str_aux_on_store`](./Enums.md#enum-reset_str_aux_on_store) | Enum/String |  | 1 |
| [`str_aux`](./Enums.md#enum-str_aux) | Enum/String |  | 1 |
| `str_aux_is_copy_item_active` | Boolean |  | 1 |
| `str_aux_is_copy_item_icon` | Boolean |  | 1 |

</details>

---

### Context: `passives`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAfterXKills`](./Items_and_Equipment.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Items_and_Equipment.md#context-passiveathealththreshold), [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold), [`PassiveIfStrAuxEquals`](./Items_and_Equipment.md#context-passiveifstrauxequals), [`PassiveWhenAffectedByElement`](./Items_and_Equipment.md#context-passivewhenaffectedbyelement), [`PassiveWhenOnTile`](./Items_and_Equipment.md#context-passivewhenontile), [`ROOT`](./Items_and_Equipment.md#context-root)

| Property Key | Type | Definition | Count (X/89) |
| :--- | :--- | :--- | :--- |
| `Metal` | Number | Applies or references the 'Metal' effect/state. | 89 |
| [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 68 |
| `Brace` | Number | Applies or references the 'Brace' effect/state. | 47 |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. | 44 |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 38 |
| [`MeleeRevengeDamage`](./Items_and_Equipment.md#context-meleerevengedamage) | Block | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. | 34 |
| [`SpawnOnBattleStart`](./Enums.md#enum-spawnonbattlestart) | Enum/String | Applies or references the 'SpawnOnBattleStart' effect/state. | 30 |
| [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend) | Block | Applies the nested status effects when the encounter finishes. | 30 |
| [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend) | Block | Applies or references the 'StatusEachTurnEnd' effect/state. | 27 |
| `Brittle` | Number | Applies or references the 'Brittle' effect/state. | 24 |
| `Fragile` | Number | Applies or references the 'Fragile' effect/state. | 22 |
| [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak) | Block | Event Trigger: Applies statuses when this action occurs. | 22 |
| `ArmorDodgeChance` | Number | Applies or references the 'ArmorDodgeChance' effect/state. | 19 |
| [`StatusOnKill`](./Items_and_Equipment.md#context-statusonkill) | Block | Event Trigger: Applies statuses when this action occurs. | 18 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 17 |
| [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage) | Block | Event Trigger: Applies statuses when this action occurs. | 17 |
| `Flammable` | Number | Applies or references the 'Flammable' effect/state. | 13 |
| [`SpawnThingOnDamage`](./Items_and_Equipment.md#context-spawnthingondamage) | Block | Applies or references the 'SpawnThingOnDamage' effect/state. | 13 |
| [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart) | Block | Event Trigger: Applies statuses when this action occurs. | 13 |
| [`SpawnEachTurn`](./Items_and_Equipment.md#context-spawneachturn) | Block | Applies or references the 'SpawnEachTurn' effect/state. | 12 |
| `AddBonusRange` | Number | Applies or references the 'AddBonusRange' effect/state. | 11 |
| `BleedThorns` | Number | Applies or references the 'BleedThorns' effect/state. | 10 |
| [`StatusImmunity`](./Arrays.md#array-statusimmunity) | Array | Applies or references the 'StatusImmunity' effect/state. | 10 |
| [`RevengeDamage`](./Items_and_Equipment.md#context-revengedamage) | Block | Reaction trigger: Deals damage to the attacker when hit. | 9 |
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum/String | Applies or references the 'SpawnThingOnDeath' effect/state. | 9 |
| [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin) | Block | Applies or references the 'StatusEachTurnBegin' effect/state. | 9 |
| [`AddSelfStatusToBasicAttack`](./Items_and_Equipment.md#context-addselfstatustobasicattack) | Block | Applies or references the 'AddSelfStatusToBasicAttack' effect/state. | 8 |
| [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage) | Block | Modifier: Injects a status effect into a specific action. | 8 |
| `CritChanceUp` | Number | Applies or references the 'CritChanceUp' effect/state. | 8 |
| `KineticSpikes` | Number | Applies or references the 'KineticSpikes' effect/state. | 8 |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum/String | Applies or references the 'ReplaceBasicMove' effect/state. | 8 |
| [`StatusAlliesOnBattleStart`](./Items_and_Equipment.md#context-statusalliesonbattlestart) | Block | Applies or references the 'StatusAlliesOnBattleStart' effect/state. | 8 |
| [`StatusOnKillEnemy`](./Items_and_Equipment.md#context-statusonkillenemy) | Block | Event Trigger: Applies statuses when this action occurs. | 8 |
| [`AbilityOnBattleStart`](./Enums.md#enum-abilityonbattlestart) | Enum/String | Applies or references the 'AbilityOnBattleStart' effect/state. | 7 |
| `AddLevelUpRerolls` | Number | Applies or references the 'AddLevelUpRerolls' effect/state. | 7 |
| `AddManaRegen` | Number | Applies or references the 'AddManaRegen' effect/state. | 7 |
| [`AddPassivesToMinions`](./Items_and_Equipment.md#context-addpassivestominions) | Block | Applies or references the 'AddPassivesToMinions' effect/state. | 7 |
| [`BrittleDuringElement`](./Enums.md#enum-brittleduringelement) | Enum/String | Applies or references the 'BrittleDuringElement' effect/state. | 7 |
| [`DurabilityTransform`](./Items_and_Equipment.md#context-durabilitytransform) | Block | Applies or references the 'DurabilityTransform' effect/state. | 7 |
| `ManaCostReduction` | Number | Applies or references the 'ManaCostReduction' effect/state. | 7 |
| [`PassiveIfStrAuxEquals`](./Items_and_Equipment.md#context-passiveifstrauxequals) | Block | Applies or references the 'PassiveIfStrAuxEquals' effect/state. | 7 |
| [`PassiveWhenOnTile`](./Items_and_Equipment.md#context-passivewhenontile) | Block | State Trigger: Grants passives when this condition is met. | 7 |
| `PoisonThorns` | Number | Applies or references the 'PoisonThorns' effect/state. | 7 |
| [`SetFragileImmune`](./Enums.md#enum-setfragileimmune) | Enum/String | Applies or references the 'SetFragileImmune' effect/state. | 7 |
| `TrinketPassiveMultiplierBonus` | Number | Applies or references the 'TrinketPassiveMultiplierBonus' effect/state. | 7 |
| `AddCorpseHealth` | Number | Applies or references the 'AddCorpseHealth' effect/state. | 6 |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 6 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum/String | Applies or references the 'ElementImmune' effect/state. | 6 |
| `Flying` | Number | Applies or references the 'Flying' effect/state. | 6 |
| [`ItemAuxTransform`](./Items_and_Equipment.md#context-itemauxtransform) | Block | Applies or references the 'ItemAuxTransform' effect/state. | 6 |
| [`SetBrittleImmune`](./Enums.md#enum-setbrittleimmune) | Enum/String | Applies or references the 'SetBrittleImmune' effect/state. | 6 |
| [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie) | Block | Event Trigger: Applies statuses when this action occurs. | 6 |
| `Trample` | Number | Applies or references the 'Trample' effect/state. | 6 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 5 |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. | 5 |
| `BoostHeals` | Number | Applies or references the 'BoostHeals' effect/state. | 5 |
| `ChanceToRevive` | Number | Applies or references the 'ChanceToRevive' effect/state. | 5 |
| [`DelayedAutoRevive`](./Items_and_Equipment.md#context-delayedautorevive) | Block | Applies or references the 'DelayedAutoRevive' effect/state. | 5 |
| [`OverrideBasicAttack`](./Enums.md#enum-overridebasicattack) | Enum/String | Applies or references the 'OverrideBasicAttack' effect/state. | 5 |
| [`PassiveAtHealthThreshold`](./Items_and_Equipment.md#context-passiveathealththreshold) | Block | Applies or references the 'PassiveAtHealthThreshold' effect/state. | 5 |
| `Poison` | Number | Applies or references the 'Poison' effect/state. | 5 |
| `Quivered` | Number | Applies or references the 'Quivered' effect/state. | 5 |
| [`SpawnOnBattleStartRandomEmptyTile`](./Items_and_Equipment.md#context-spawnonbattlestartrandomemptytile) | Block | Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state. | 5 |
| `SpellDamageUp` | Number | Applies or references the 'SpellDamageUp' effect/state. | 5 |
| [`StatusOnEndMove`](./Items_and_Equipment.md#context-statusonendmove) | Block | Event Trigger: Applies statuses when this action occurs. | 5 |
| [`TransformItemOnElementInfluence`](./Items_and_Equipment.md#context-transformitemonelementinfluence) | Block | Applies or references the 'TransformItemOnElementInfluence' effect/state. | 5 |
| [`AddDamageToElementDamage`](./Items_and_Equipment.md#context-adddamagetoelementdamage) | Block | Applies or references the 'AddDamageToElementDamage' effect/state. | 4 |
| [`AddTag`](./Enums.md#enum-addtag) | Enum/String | Applies or references the 'AddTag' effect/state. | 4 |
| [`AmplifyStatus`](./Enums.md#enum-amplifystatus) | Enum/String | Applies or references the 'AmplifyStatus' effect/state. | 4 |
| `BreakAtAux` | Number | Applies or references the 'BreakAtAux' effect/state. | 4 |
| [`ClassManaCostReduction`](./Items_and_Equipment.md#context-classmanacostreduction) | Block | Applies or references the 'ClassManaCostReduction' effect/state. | 4 |
| [`DeathRattle`](./Items_and_Equipment.md#context-deathrattle) | Block | Applies or references the 'DeathRattle' effect/state. | 4 |
| `DepressionAura` | Number | Applies or references the 'DepressionAura' effect/state. | 4 |
| `DodgeChance_Status` | Number | Applies or references the 'DodgeChance_Status' effect/state. | 4 |
| `ExtraBasicAttacks` | Number | Applies or references the 'ExtraBasicAttacks' effect/state. | 4 |
| `ExtraWeaponAttacks` | Number | Applies or references the 'ExtraWeaponAttacks' effect/state. | 4 |
| [`FragileDuringElement`](./Enums.md#enum-fragileduringelement) | Enum/String | Applies or references the 'FragileDuringElement' effect/state. | 4 |
| `MissChance` | Number | Applies or references the 'MissChance' effect/state. | 4 |
| `PermanentMadness` | Number | Applies or references the 'PermanentMadness' effect/state. | 4 |
| [`RandomSeededStatModifier`](./Arrays.md#array-randomseededstatmodifier) | Array | Applies or references the 'RandomSeededStatModifier' effect/state. | 4 |
| [`SpawnObjectOnPopCorpse`](./Enums.md#enum-spawnobjectonpopcorpse) | Enum/String | Applies or references the 'SpawnObjectOnPopCorpse' effect/state. | 4 |
| [`StatusOnTakeHealthOrShieldDamage`](./Items_and_Equipment.md#context-statusontakehealthorshielddamage) | Block | Event Trigger: Applies statuses when this action occurs. | 4 |
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](./Items_and_Equipment.md#context-statusonturnendifdidntcastabilitytypes) | Block | Event Trigger: Applies statuses when this action occurs. | 4 |
| [`StatusRandomEnemiesOnBattleStart`](./Items_and_Equipment.md#context-statusrandomenemiesonbattlestart) | Block | Applies or references the 'StatusRandomEnemiesOnBattleStart' effect/state. | 4 |
| `AddBonusMeleeRange` | Number | Applies or references the 'AddBonusMeleeRange' effect/state. | 3 |
| [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum/String | Applies or references the 'AddElementsToBasicAttack' effect/state. | 3 |
| `AddEndOfCombatRegen` | Number | Applies or references the 'AddEndOfCombatRegen' effect/state. | 3 |
| `AddKnockbackDamage` | Number | Applies or references the 'AddKnockbackDamage' effect/state. | 3 |
| `AllStatsUpPerDisorder` | Number | Applies or references the 'AllStatsUpPerDisorder' effect/state. | 3 |
| `AlphaTurns` | Number | Applies or references the 'AlphaTurns' effect/state. | 3 |
| `BoneArmorPassive` | Number | Applies or references the 'BoneArmorPassive' effect/state. | 3 |
| [`BreakOnElement`](./Enums.md#enum-breakonelement) | Enum/String | Applies or references the 'BreakOnElement' effect/state. | 3 |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 3 |
| `CantCatchDiseases` | Number | Applies or references the 'CantCatchDiseases' effect/state. | 3 |
| `CantSpreadDiseases` | Number | Applies or references the 'CantSpreadDiseases' effect/state. | 3 |
| [`CatchProjectiles`](./Items_and_Equipment.md#context-catchprojectiles) | Block | Applies or references the 'CatchProjectiles' effect/state. | 3 |
| `ChanceToBlock` | Number | Applies or references the 'ChanceToBlock' effect/state. | 3 |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 3 |
| `CopyPassiveSlot` | Number | Applies or references the 'CopyPassiveSlot' effect/state. | 3 |
| [`CounterAttack`](./Items_and_Equipment.md#context-counterattack) | Block | Applies or references the 'CounterAttack' effect/state. | 3 |
| [`DeathRattleRevive`](./Enums.md#enum-deathrattlerevive) | Enum/String | Applies or references the 'DeathRattleRevive' effect/state. | 3 |
| [`DisableAbilities`](./Enums.md#enum-disableabilities) | Enum/String | Applies or references the 'DisableAbilities' effect/state. | 3 |
| [`DropAsFamiliarOnArmorBreak`](./Enums.md#enum-dropasfamiliaronarmorbreak) | Enum/String | Applies or references the 'DropAsFamiliarOnArmorBreak' effect/state. | 3 |
| [`ExtraStatusWhenDealingDamage`](./Items_and_Equipment.md#context-extrastatuswhendealingdamage) | Block | Applies or references the 'ExtraStatusWhenDealingDamage' effect/state. | 3 |
| `FaceArmorPassiveMultiplierBonus` | Number | Applies or references the 'FaceArmorPassiveMultiplierBonus' effect/state. | 3 |
| `HeadArmorPassiveMultiplierBonus` | Number | Applies or references the 'HeadArmorPassiveMultiplierBonus' effect/state. | 3 |
| `IncreaseExplosionSize` | Number | Applies or references the 'IncreaseExplosionSize' effect/state. | 3 |
| [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold) | Block | Applies or references the 'PassiveAtStatThreshold' effect/state. | 3 |
| [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead) | Block | State Trigger: Grants passives when this condition is met. | 3 |
| `RockyArmorPassive` | Number | Applies or references the 'RockyArmorPassive' effect/state. | 3 |
| [`SpawnExtraThingsOnBattleStart`](./Items_and_Equipment.md#context-spawnextrathingsonbattlestart) | Block | Applies or references the 'SpawnExtraThingsOnBattleStart' effect/state. | 3 |
| [`StackingFlowerTrail`](./Items_and_Equipment.md#context-stackingflowertrail) | Block | Applies or references the 'StackingFlowerTrail' effect/state. | 3 |
| [`StatusAllCharactersOnSpawn`](./Items_and_Equipment.md#context-statusallcharactersonspawn) | Block | Applies or references the 'StatusAllCharactersOnSpawn' effect/state. | 3 |
| [`StatusEveryXSpellCasts`](./Items_and_Equipment.md#context-statuseveryxspellcasts) | Block | Applies or references the 'StatusEveryXSpellCasts' effect/state. | 3 |
| [`StatusIfUnusedMovePoints`](./Items_and_Equipment.md#context-statusifunusedmovepoints) | Block | Applies or references the 'StatusIfUnusedMovePoints' effect/state. | 3 |
| [`StatusOnPopCorpse`](./Items_and_Equipment.md#context-statusonpopcorpse) | Block | Event Trigger: Applies statuses when this action occurs. | 3 |
| `TrinketActiveEffectsMultiplierBonus` | Number | Applies or references the 'TrinketActiveEffectsMultiplierBonus' effect/state. | 3 |
| `TrueShot` | Number | Applies or references the 'TrueShot' effect/state. | 3 |
| `AddInitiative` | Number | Applies or references the 'AddInitiative' effect/state. | 2 |
| [`AddStatusToElementDamage`](./Items_and_Equipment.md#context-addstatustoelementdamage) | Block | Modifier: Injects a status effect into a specific action. | 2 |
| [`AddStatusToKnockbackDamage`](./Items_and_Equipment.md#context-addstatustoknockbackdamage) | Block | Modifier: Injects a status effect into a specific action. | 2 |
| [`AddStatusToSpells`](./Items_and_Equipment.md#context-addstatustospells) | Block | Modifier: Injects a status effect into a specific action. | 2 |
| `AmplifyKnockback` | Number | Applies or references the 'AmplifyKnockback' effect/state. | 2 |
| [`ApplyStatusesToRandomEnemiesEachTurn`](./Items_and_Equipment.md#context-applystatusestorandomenemieseachturn) | Block | Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state. | 2 |
| [`ArmorBreakOnHit`](./Items_and_Equipment.md#context-armorbreakonhit) | Block | Applies or references the 'ArmorBreakOnHit' effect/state. | 2 |
| `AutoEquipConsumables` | Number | Applies or references the 'AutoEquipConsumables' effect/state. | 2 |
| [`BackstabCritChance`](./Enums.md#enum-backstabcritchance) | Enum/String | Applies or references the 'BackstabCritChance' effect/state. | 2 |
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum/String | Applies or references the 'BonusAbility' effect/state. | 2 |
| [`BoostWeaponDamage`](./Items_and_Equipment.md#context-boostweapondamage) | Block | Applies or references the 'BoostWeaponDamage' effect/state. | 2 |
| `BreakWhenNoShield` | Number | Applies or references the 'BreakWhenNoShield' effect/state. | 2 |
| `CanLevelUpWhenDead` | Number | Applies or references the 'CanLevelUpWhenDead' effect/state. | 2 |
| [`ChanceToBackflip`](./Items_and_Equipment.md#context-chancetobackflip) | Block | Applies or references the 'ChanceToBackflip' effect/state. | 2 |
| `ChanceToBlockAndCounter` | Number | Applies or references the 'ChanceToBlockAndCounter' effect/state. | 2 |
| `DisablePassiveSlot` | Number | Applies or references the 'DisablePassiveSlot' effect/state. | 2 |
| `DodgeChance` | Number | Applies or references the 'DodgeChance' effect/state. | 2 |
| [`ElementalManaCostReduction`](./Items_and_Equipment.md#context-elementalmanacostreduction) | Block | Applies or references the 'ElementalManaCostReduction' effect/state. | 2 |
| `ExtraBasicMoves_Status` | Number | Applies or references the 'ExtraBasicMoves_Status' effect/state. | 2 |
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md#enum-findextraitemfrompoolonbattleend) | Enum/String | Applies or references the 'FindExtraItemFromPoolOnBattleEnd' effect/state. | 2 |
| `FlowersOnEndTurn` | Number | Applies or references the 'FlowersOnEndTurn' effect/state. | 2 |
| `FreezePiercing` | Number | Applies or references the 'FreezePiercing' effect/state. | 2 |
| `IncreaseExplosionDamage` | Number | Applies or references the 'IncreaseExplosionDamage' effect/state. | 2 |
| `IncreaseSpellRange` | Number | Applies or references the 'IncreaseSpellRange' effect/state. | 2 |
| `InjuryImmunity` | Number | Applies or references the 'InjuryImmunity' effect/state. | 2 |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum/String | Applies or references the 'InnateElement' effect/state. | 2 |
| [`KillsToMeat`](./Enums.md#enum-killstomeat) | Enum/String | Applies or references the 'KillsToMeat' effect/state. | 2 |
| `KnockbackImmunity` | Number | Applies or references the 'KnockbackImmunity' effect/state. | 2 |
| [`LeaveBehindOnceEachMove`](./Enums.md#enum-leavebehindonceeachmove) | Enum/String | Applies or references the 'LeaveBehindOnceEachMove' effect/state. | 2 |
| [`LevelUpClassOverride`](./Enums.md#enum-levelupclassoverride) | Enum/String | Applies or references the 'LevelUpClassOverride' effect/state. | 2 |
| `MoveQuivered` | Number | Applies or references the 'MoveQuivered' effect/state. | 2 |
| `NeckArmorPassiveMultiplierBonus` | Number | Applies or references the 'NeckArmorPassiveMultiplierBonus' effect/state. | 2 |
| [`PassiveAfterXKills`](./Items_and_Equipment.md#context-passiveafterxkills) | Block | Applies or references the 'PassiveAfterXKills' effect/state. | 2 |
| [`PassiveIfWeaponIsUsable`](./Items_and_Equipment.md#context-passiveifweaponisusable) | Block | Applies or references the 'PassiveIfWeaponIsUsable' effect/state. | 2 |
| `RangedTrueShot` | Number | Applies or references the 'RangedTrueShot' effect/state. | 2 |
| `ReflectProjectiles` | Number | Applies or references the 'ReflectProjectiles' effect/state. | 2 |
| [`RefreshEquipmentAbilityOnElement`](./Items_and_Equipment.md#context-refreshequipmentabilityonelement) | Block | Applies or references the 'RefreshEquipmentAbilityOnElement' effect/state. | 2 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum/String | Applies or references the 'ReplaceBasicAttack' effect/state. | 2 |
| [`ReplaceSpawnedObjects`](./Arrays.md#array-replacespawnedobjects) | Array | Applies or references the 'ReplaceSpawnedObjects' effect/state. | 2 |
| [`SetDefaultFacePassive`](./Enums.md#enum-setdefaultfacepassive) | Enum/String | Applies or references the 'SetDefaultFacePassive' effect/state. | 2 |
| [`SpawnCatCopyWhenDowned`](./Items_and_Equipment.md#context-spawncatcopywhendowned) | Block |  | 2 |
| [`SpawnItemLinkedFamiliar`](./Items_and_Equipment.md#context-spawnitemlinkedfamiliar) | Block | Applies or references the 'SpawnItemLinkedFamiliar' effect/state. | 2 |
| `SpawnNearEnemies` | Number | Applies or references the 'SpawnNearEnemies' effect/state. | 2 |
| [`StatusAfterCastSpell`](./Items_and_Equipment.md#context-statusaftercastspell) | Block | Applies or references the 'StatusAfterCastSpell' effect/state. | 2 |
| [`StatusIfUnusedActPoints`](./Items_and_Equipment.md#context-statusifunusedactpoints) | Block | Applies or references the 'StatusIfUnusedActPoints' effect/state. | 2 |
| [`StatusOnAllyCatDeath`](./Items_and_Equipment.md#context-statusonallycatdeath) | Block | Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnBackstab`](./Items_and_Equipment.md#context-statusonbackstab) | Block | Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnBreakItem`](./Items_and_Equipment.md#context-statusonbreakitem) | Block | Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnCastSpell`](./Items_and_Equipment.md#context-statusoncastspell) | Block | Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnGainCoins`](./Items_and_Equipment.md#context-statusongaincoins) | Block | Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnSetPieceBreak`](./Items_and_Equipment.md#context-statusonsetpiecebreak) | Block |  | 2 |
| `Uncontrollable` | Number | Applies or references the 'Uncontrollable' effect/state. | 2 |
| [`UpgradeTaggedSpawnsToChampions`](./Enums.md#enum-upgradetaggedspawnstochampions) | Enum/String |  | 2 |
| [`AIControlNextTurn`](./Items_and_Equipment.md#context-aicontrolnextturn) | Block | Applies or references the 'AIControlNextTurn' effect/state. | 1 |
| `AOEBonus` | Number | Applies or references the 'AOEBonus' effect/state. | 1 |
| [`AbilityHealthThreshold`](./Items_and_Equipment.md#context-abilityhealththreshold) | Block | Applies or references the 'AbilityHealthThreshold' effect/state. | 1 |
| [`AbilityOnRoundEndOnce`](./Items_and_Equipment.md#context-abilityonroundendonce) | Block | Applies or references the 'AbilityOnRoundEndOnce' effect/state. | 1 |
| [`AbilityReaction`](./Enums.md#enum-abilityreaction) | Enum/String | Applies or references the 'AbilityReaction' effect/state. | 1 |
| [`AddAdvantageToEvent`](./Items_and_Equipment.md#context-addadvantagetoevent) | Block | Applies or references the 'AddAdvantageToEvent' effect/state. | 1 |
| `AddConstitution` | Number |  | 1 |
| `AddCritMultiplier` | Number | Applies or references the 'AddCritMultiplier' effect/state. | 1 |
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum/String | Applies or references the 'AddHiddenTag' effect/state. | 1 |
| [`AddPassivesToCharmed`](./Items_and_Equipment.md#context-addpassivestocharmed) | Block | Applies or references the 'AddPassivesToCharmed' effect/state. | 1 |
| [`AddSelfStatusToWeapons`](./Items_and_Equipment.md#context-addselfstatustoweapons) | Block | Applies or references the 'AddSelfStatusToWeapons' effect/state. | 1 |
| `AddStartingMana` | Number |  | 1 |
| [`AddStatusToBackstabs`](./Items_and_Equipment.md#context-addstatustobackstabs) | Block | Modifier: Injects a status effect into a specific action. | 1 |
| [`AddStatusToFirstSpellEachTurn`](./Items_and_Equipment.md#context-addstatustofirstspelleachturn) | Block |  | 1 |
| [`AddStatusToWeapons`](./Items_and_Equipment.md#context-addstatustoweapons) | Block | Modifier: Injects a status effect into a specific action. | 1 |
| [`AddTemporaryEffectsToBasicAttack`](./Items_and_Equipment.md#context-addtemporaryeffectstobasicattack) | Block | Applies or references the 'AddTemporaryEffectsToBasicAttack' effect/state. | 1 |
| `AllSpellsCostCharge` | Number | Applies or references the 'AllSpellsCostCharge' effect/state. | 1 |
| `AllUnitsExplodeOnDeath` | Number | Applies or references the 'AllUnitsExplodeOnDeath' effect/state. | 1 |
| `AlliesScrambleSpellAfterCast` | Number | Applies or references the 'AlliesScrambleSpellAfterCast' effect/state. | 1 |
| [`AlluringDoodieEater`](./Items_and_Equipment.md#context-alluringdoodieeater) | Block | Applies or references the 'AlluringDoodieEater' effect/state. | 1 |
| `AllyDamageReduction` | Number | Applies or references the 'AllyDamageReduction' effect/state. | 1 |
| [`AllyDodgeChanceAura`](./Items_and_Equipment.md#context-allydodgechanceaura) | Block | Applies or references the 'AllyDodgeChanceAura' effect/state. | 1 |
| `AlphaAllStatsUp` | Number | Applies or references the 'AlphaAllStatsUp' effect/state. | 1 |
| `AlphaCat` | Number | Applies or references the 'AlphaCat' effect/state. | 1 |
| `AlwaysChosenForLevelUp` | Number | Applies or references the 'AlwaysChosenForLevelUp' effect/state. | 1 |
| [`AutocastEachRound`](./Items_and_Equipment.md#context-autocasteachround) | Block | Forces the character to automatically cast a specific ability at the start of each combat round. | 1 |
| [`BackflipWhenTargeted`](./Items_and_Equipment.md#context-backflipwhentargeted) | Block | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. | 1 |
| `BackstabImmunity` | Number |  | 1 |
| `BalanceStats` | Number | Applies or references the 'BalanceStats' effect/state. | 1 |
| `BasicAttackCantMiss` | Number | Applies or references the 'BasicAttackCantMiss' effect/state. | 1 |
| [`BasicAttackCritChance`](./Enums.md#enum-basicattackcritchance) | Enum/String | Applies or references the 'BasicAttackCritChance' effect/state. | 1 |
| `Blind` | Number | Applies or references the 'Blind' effect/state. | 1 |
| `BlockDamageUnderThreshold` | Number | Applies or references the 'BlockDamageUnderThreshold' effect/state. | 1 |
| `BlockNegativeStatus` | Number | Applies or references the 'BlockNegativeStatus' effect/state. | 1 |
| `BonusHealthRegenPerDisorder` | Number |  | 1 |
| `BoostReceivedHealing` | Number | Applies or references the 'BoostReceivedHealing' effect/state. | 1 |
| [`BouncyProjectiles`](./Items_and_Equipment.md#context-bouncyprojectiles) | Block | Applies or references the 'BouncyProjectiles' effect/state. | 1 |
| [`BuffImmunity`](./Items_and_Equipment.md#context-buffimmunity) | Block | Applies or references the 'BuffImmunity' effect/state. | 1 |
| `CanRemoveCursedItems` | Number | Applies or references the 'CanRemoveCursedItems' effect/state. | 1 |
| `CapBasicAttackDamage` | Number | Applies or references the 'CapBasicAttackDamage' effect/state. | 1 |
| `CapMovementAbilityRange` | Number | Applies or references the 'CapMovementAbilityRange' effect/state. | 1 |
| [`CatPartsSizeScale`](./Items_and_Equipment.md#context-catpartssizescale) | Block | Applies or references the 'CatPartsSizeScale' effect/state. | 1 |
| `ChanceToAmbush` | Number | Applies or references the 'ChanceToAmbush' effect/state. | 1 |
| [`ChanceToForceEvent`](./Items_and_Equipment.md#context-chancetoforceevent) | Block | Applies or references the 'ChanceToForceEvent' effect/state. | 1 |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 1 |
| `CharismaIsMaxStat` | Number | Applies or references the 'CharismaIsMaxStat' effect/state. | 1 |
| `CharmImmunity` | Number | Applies or references the 'CharmImmunity' effect/state. | 1 |
| `ConsumableEffectsMultiplierBonus` | Number | Applies or references the 'ConsumableEffectsMultiplierBonus' effect/state. | 1 |
| [`ConvertDamageToScaledStatus`](./Items_and_Equipment.md#context-convertdamagetoscaledstatus) | Block | Applies or references the 'ConvertDamageToScaledStatus' effect/state. | 1 |
| `CounterNextAttacks` | Number | Applies or references the 'CounterNextAttacks' effect/state. | 1 |
| [`CreateGlobalModifiers`](./Items_and_Equipment.md#context-createglobalmodifiers) | Block | Generates global map or encounter rules/modifiers. | 1 |
| [`CritsApplyStatus`](./Items_and_Equipment.md#context-critsapplystatus) | Block | Applies or references the 'CritsApplyStatus' effect/state. | 1 |
| [`CyborgTurns`](./Items_and_Equipment.md#context-cyborgturns) | Block |  | 1 |
| `DebuffImmunity` | Number | Applies or references the 'DebuffImmunity' effect/state. | 1 |
| `DoubleCastSpellIfManaCostUnderThreshold` | Number | Applies or references the 'DoubleCastSpellIfManaCostUnderThreshold' effect/state. | 1 |
| `DoubleCastSpellsEachTurn_Status` | Number |  | 1 |
| [`DoubleCastTaggedSpells`](./Enums.md#enum-doublecasttaggedspells) | Enum/String | Applies or references the 'DoubleCastTaggedSpells' effect/state. | 1 |
| `DoubleCastWeapons` | Number | Applies or references the 'DoubleCastWeapons' effect/state. | 1 |
| `DoubleReceivedNegativeStatus` | Number | Applies or references the 'DoubleReceivedNegativeStatus' effect/state. | 1 |
| `DoubleReceivedPositiveStatus` | Number | Applies or references the 'DoubleReceivedPositiveStatus' effect/state. | 1 |
| [`DropAsFamiliarOnTookDamage`](./Enums.md#enum-dropasfamiliarontookdamage) | Enum/String | Applies or references the 'DropAsFamiliarOnTookDamage' effect/state. | 1 |
| [`DropSoulJarOnDeath`](./Enums.md#enum-dropsouljarondeath) | Enum/String | Applies or references the 'DropSoulJarOnDeath' effect/state. | 1 |
| [`Eternal`](./Items_and_Equipment.md#context-eternal) | Block | Applies or references the 'Eternal' effect/state. | 1 |
| [`ExcludeFromEvents`](./Enums.md#enum-excludefromevents) | Enum/String | Applies or references the 'ExcludeFromEvents' effect/state. | 1 |
| `ExplosionImmunity` | Number | Applies or references the 'ExplosionImmunity' effect/state. | 1 |
| `ExtraBasicAttacks_Status` | Number | Applies or references the 'ExtraBasicAttacks_Status' effect/state. | 1 |
| `ExtraMovePoints` | Number | Applies or references the 'ExtraMovePoints' effect/state. | 1 |
| `ExtraTrinketUses` | Number | Applies or references the 'ExtraTrinketUses' effect/state. | 1 |
| `FaceShield` | Number | Applies or references the 'FaceShield' effect/state. | 1 |
| [`FlyDamageIncrease`](./Items_and_Equipment.md#context-flydamageincrease) | Block | Applies or references the 'FlyDamageIncrease' effect/state. | 1 |
| `FrankBolts` | Number | Applies or references the 'FrankBolts' effect/state. | 1 |
| `GainExtraShield` | Number | Applies or references the 'GainExtraShield' effect/state. | 1 |
| `GlobalFamiliarDamageBoost` | Number |  | 1 |
| `GlobalFamiliarMoveBoost` | Number |  | 1 |
| [`GlobalFlowerTrapperAura`](./Items_and_Equipment.md#context-globalflowertrapperaura) | Block |  | 1 |
| [`GlobalMeleeRevengeDamage`](./Items_and_Equipment.md#context-globalmeleerevengedamage) | Block | Applies or references the 'GlobalMeleeRevengeDamage' effect/state. | 1 |
| `HPGainBlock` | Number | Applies or references the 'HPGainBlock' effect/state. | 1 |
| `HideSomeHudStuff` | Number | Applies or references the 'HideSomeHudStuff' effect/state. | 1 |
| `IgnoreTiles` | Number | Applies or references the 'IgnoreTiles' effect/state. | 1 |
| `JesterLevelUpRerolls` | Number | Applies or references the 'JesterLevelUpRerolls' effect/state. | 1 |
| `Lifesteal` | Number | Applies or references the 'Lifesteal' effect/state. | 1 |
| `LuckUp` | Number | Applies or references the 'LuckUp' effect/state. | 1 |
| `MakeBasicAttackPull` | Number | Applies or references the 'MakeBasicAttackPull' effect/state. | 1 |
| `MakeSpellsRequireCharge` | Number | Applies or references the 'MakeSpellsRequireCharge' effect/state. | 1 |
| `ModelingClayPassive` | Number | Applies or references the 'ModelingClayPassive' effect/state. | 1 |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum/String | Applies or references the 'MoveAndUseAbilityEachTurnBeginIfPossible' effect/state. | 1 |
| [`MoveSpeedMultiplier`](./Enums.md#enum-movespeedmultiplier) | Enum/String | Applies or references the 'MoveSpeedMultiplier' effect/state. | 1 |
| [`MoveTowardsDamageSource`](./Enums.md#enum-movetowardsdamagesource) | Enum/String | Applies or references the 'MoveTowardsDamageSource' effect/state. | 1 |
| [`MovementReaction`](./Items_and_Equipment.md#context-movementreaction) | Block | Applies or references the 'MovementReaction' effect/state. | 1 |
| `MultiplyCoinsOnBattleStart` | Number | Applies or references the 'MultiplyCoinsOnBattleStart' effect/state. | 1 |
| `MultiplyReceivedHealing` | Number | Applies or references the 'MultiplyReceivedHealing' effect/state. | 1 |
| [`ObjectDetector`](./Items_and_Equipment.md#context-objectdetector) | Block | Applies or references the 'ObjectDetector' effect/state. | 1 |
| `OverManaReducesManaCosts` | Number |  | 1 |
| [`PassiveWhenAffectedByElement`](./Items_and_Equipment.md#context-passivewhenaffectedbyelement) | Block | State Trigger: Grants passives when this condition is met. | 1 |
| [`PassiveWhileHasDurability`](./Items_and_Equipment.md#context-passivewhilehasdurability) | Block | Applies or references the 'PassiveWhileHasDurability' effect/state. | 1 |
| [`PassiveWhileInMonkMeleeStance`](./Items_and_Equipment.md#context-passivewhileinmonkmeleestance) | Block | Applies or references the 'PassiveWhileInMonkMeleeStance' effect/state. | 1 |
| [`PassiveWhileShielded`](./Items_and_Equipment.md#context-passivewhileshielded) | Block | Applies or references the 'PassiveWhileShielded' effect/state. | 1 |
| `PhysicalAttacksMiss` | Number | Applies or references the 'PhysicalAttacksMiss' effect/state. | 1 |
| [`PoopWhenHit`](./Items_and_Equipment.md#context-poopwhenhit) | Block | Applies or references the 'PoopWhenHit' effect/state. | 1 |
| [`PreventSpecificInjury`](./Enums.md#enum-preventspecificinjury) | Enum/String | Applies or references the 'PreventSpecificInjury' effect/state. | 1 |
| `ReclaimItemOnBreak` | Number | Applies or references the 'ReclaimItemOnBreak' effect/state. | 1 |
| `ReduceManaCost` | Number | Applies or references the 'ReduceManaCost' effect/state. | 1 |
| `ReduceSpellCostsPerDisorder` | Number | Applies or references the 'ReduceSpellCostsPerDisorder' effect/state. | 1 |
| `ReduceSpellCostsPerParasite` | Number | Applies or references the 'ReduceSpellCostsPerParasite' effect/state. | 1 |
| `RemoveLineOfSightRestrictions` | Number | Applies or references the 'RemoveLineOfSightRestrictions' effect/state. | 1 |
| [`ReplaceBlankTilesOnBattleStart`](./Enums.md#enum-replaceblanktilesonbattlestart) | Enum/String | Applies or references the 'ReplaceBlankTilesOnBattleStart' effect/state. | 1 |
| `RerollItemsOnBattleEnd` | Number | Applies or references the 'RerollItemsOnBattleEnd' effect/state. | 1 |
| [`Robot`](./Items_and_Equipment.md#context-robot) | Block |  | 1 |
| [`RockyArmorSalvage`](./Enums.md#enum-rockyarmorsalvage) | Enum/String |  | 1 |
| [`ScaldingOrbMoonBossOneShot`](./Items_and_Equipment.md#context-scaldingorbmoonbossoneshot) | Block | Applies or references the 'ScaldingOrbMoonBossOneShot' effect/state. | 1 |
| [`ScaledStatusAlliesOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusalliesonspendmana) | Block | Applies or references the 'ScaledStatusAlliesOnSpendMana' effect/state. | 1 |
| [`ScaledStatusOnHolyShieldBlock`](./Items_and_Equipment.md#context-scaledstatusonholyshieldblock) | Block | Applies or references the 'ScaledStatusOnHolyShieldBlock' effect/state. | 1 |
| [`ScaledStatusOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusonspendmana) | Block | Applies or references the 'ScaledStatusOnSpendMana' effect/state. | 1 |
| [`SetFaction`](./Enums.md#enum-setfaction) | Enum/String | Applies or references the 'SetFaction' effect/state. | 1 |
| `SetSpellCosts` | Number | Applies or references the 'SetSpellCosts' effect/state. | 1 |
| `SharkySmellsBlood` | Number | Applies or references the 'SharkySmellsBlood' effect/state. | 1 |
| `SpawnCatCloneOnCorpsePopped` | Number | Applies or references the 'SpawnCatCloneOnCorpsePopped' effect/state. | 1 |
| [`SpawnCatCopyOnBattleStart`](./Items_and_Equipment.md#context-spawncatcopyonbattlestart) | Block |  | 1 |
| [`SpawnOnDeath`](./Items_and_Equipment.md#context-spawnondeath) | Block | Applies or references the 'SpawnOnDeath' effect/state. | 1 |
| [`SpawnOnDowned`](./Enums.md#enum-spawnondowned) | Enum/String | Applies or references the 'SpawnOnDowned' effect/state. | 1 |
| [`SpawnRandomPickupsOnTaggedUnitKilled`](./Items_and_Equipment.md#context-spawnrandompickupsontaggedunitkilled) | Block | Applies or references the 'SpawnRandomPickupsOnTaggedUnitKilled' effect/state. | 1 |
| [`StatDependentPassive`](./Items_and_Equipment.md#context-statdependentpassive) | Block | Applies or references the 'StatDependentPassive' effect/state. | 1 |
| [`StatusAdjacentOnTheirTurnEnd`](./Items_and_Equipment.md#context-statusadjacentontheirturnend) | Block | Applies or references the 'StatusAdjacentOnTheirTurnEnd' effect/state. | 1 |
| [`StatusAfterXTurns`](./Items_and_Equipment.md#context-statusafterxturns) | Block | Applies or references the 'StatusAfterXTurns' effect/state. | 1 |
| [`StatusAlliesEachTurn`](./Items_and_Equipment.md#context-statusallieseachturn) | Block | Applies or references the 'StatusAlliesEachTurn' effect/state. | 1 |
| [`StatusAlliesOnDeath`](./Items_and_Equipment.md#context-statusalliesondeath) | Block | Applies or references the 'StatusAlliesOnDeath' effect/state. | 1 |
| [`StatusEachTurnEndForEachTurn`](./Items_and_Equipment.md#context-statuseachturnendforeachturn) | Block | Applies or references the 'StatusEachTurnEndForEachTurn' effect/state. | 1 |
| [`StatusOnCollectPickup`](./Items_and_Equipment.md#context-statusoncollectpickup) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnDodge`](./Items_and_Equipment.md#context-statusondodge) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnEatFood`](./Items_and_Equipment.md#context-statusoneatfood) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnEatPill`](./Items_and_Equipment.md#context-statusoneatpill) | Block |  | 1 |
| [`StatusOnEnemyDeath`](./Items_and_Equipment.md#context-statusonenemydeath) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnFallAsleep`](./Items_and_Equipment.md#context-statusonfallasleep) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnFullMana`](./Items_and_Equipment.md#context-statusonfullmana) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnHealed`](./Items_and_Equipment.md#context-statusonhealed) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnPickupCoins`](./Items_and_Equipment.md#context-statusonpickupcoins) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnTurnEndIfCastNSpells`](./Items_and_Equipment.md#context-statusonturnendifcastnspells) | Block |  | 1 |
| [`StatusOnUseBasicAttack`](./Items_and_Equipment.md#context-statusonusebasicattack) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusWhenAllySpendsMana`](./Items_and_Equipment.md#context-statuswhenallyspendsmana) | Block | Applies or references the 'StatusWhenAllySpendsMana' effect/state. | 1 |
| `StevenBolts` | Number | Applies or references the 'StevenBolts' effect/state. | 1 |
| `StripKnockback` | Number | Applies or references the 'StripKnockback' effect/state. | 1 |
| `TauntAlways` | Number | Applies or references the 'TauntAlways' effect/state. | 1 |
| [`TintItem`](./Items_and_Equipment.md#context-tintitem) | Block | Applies or references the 'TintItem' effect/state. | 1 |
| `TriggerBleedOnBleed` | Number |  | 1 |
| [`TunnelVision`](./Items_and_Equipment.md#context-tunnelvision) | Block | Applies or references the 'TunnelVision' effect/state. | 1 |
| `Undead` | Number | Applies or references the 'Undead' effect/state. | 1 |
| `UpgradeSpawnedPickups` | Number |  | 1 |
| `WeaponActiveEffectsMultiplierBonus` | Number |  | 1 |
| `WeaponDamageMultiplierBonus` | Number | Applies or references the 'WeaponDamageMultiplierBonus' effect/state. | 1 |
| `WeaponPassiveMultiplierBonus` | Number |  | 1 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/25) |
| :--- | :--- | :--- | :--- |
| [`effects`](./Items_and_Equipment.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 25 |
| `knockback` | Number |  | 9 |
| `damage` | Number | The base damage properties of an attack. | 5 |

</details>

---

### Context: `SpawnOnBattleStart`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/22) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 22 |
| `number` | Number |  | 16 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend), [`StatusOnKill`](./Items_and_Equipment.md#context-statusonkill), [`StatusOnTakeHealthOrShieldDamage`](./Items_and_Equipment.md#context-statusontakehealthorshielddamage), [`effects`](./Items_and_Equipment.md#context-effects)

| Property Key | Type | Definition | Count (X/19) |
| :--- | :--- | :--- | :--- |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 19 |
| `Freeze` | Number | Applies or references the 'Freeze' effect/state. | 6 |
| [`ForceUseAbility_NonStack`](./Enums.md#enum-forceuseability_nonstack) | Enum/String | Applies or references the 'ForceUseAbility_NonStack' effect/state. | 4 |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum/String | Generates an item drop from the specified loot pool. | 3 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Applies or references the 'ForceUseAbility' effect/state. | 3 |
| `RandomMutation` | Number | Applies or references the 'RandomMutation' effect/state. | 3 |
| `DestroyTrinket` | Number | Applies or references the 'DestroyTrinket' effect/state. | 1 |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/13) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 13 |
| `good` | Boolean |  | 4 |
| `shield_only` | Boolean |  | 2 |
| `spawn_on_death_hit` | Boolean |  | 2 |
| [`chance`](./Enums.md#enum-chance) | Enum/String | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| `number` | Number |  | 1 |

</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 12 |
| [`chance`](./Enums.md#enum-chance) | Enum/String | Probability (0.0 to 1.0 or percentage) of this occurring. | 11 |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum/String |  | 5 |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./Items_and_Equipment.md#context-applypassives), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 12 |
| `RandomPermanentStat` | Number | Applies or references the 'RandomPermanentStat' effect/state. | 7 |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll) | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 6 |
| `RandomMutation` | Number | Applies or references the 'RandomMutation' effect/state. | 5 |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum/String | Generates an item drop from the specified loot pool. | 4 |
| `GainCoins` | Number | Applies or references the 'GainCoins' effect/state. | 2 |
| `RepairTrinket` | Number | Applies or references the 'RepairTrinket' effect/state. | 2 |
| [`SetItemAux`](./Items_and_Equipment.md#context-setitemaux) | Block | Applies or references the 'SetItemAux' effect/state. | 2 |
| [`Conditional_Corpse`](./Items_and_Equipment.md#context-conditional_corpse) | Block | Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 1 |
| [`Conditional_Shielded`](./Items_and_Equipment.md#context-conditional_shielded) | Block | Conditional trigger: Executes nested logic if the target currently has a Shield status. | 1 |
| [`FindItem`](./Enums.md#enum-finditem) | Enum/String |  | 1 |
| [`GainCoinsRange`](./Items_and_Equipment.md#context-gaincoinsrange) | Block |  | 1 |
| `PermanentConstitution` | Number | Applies or references the 'PermanentConstitution' effect/state. | 1 |
| `PermanentIntelligence` | Number | Applies or references the 'PermanentIntelligence' effect/state. | 1 |
| `RepairAll` | Number | Applies or references the 'RepairAll' effect/state. | 1 |
| `RepairWeapon` | Number | Applies or references the 'RepairWeapon' effect/state. | 1 |
| [`TransformWeapon`](./Items_and_Equipment.md#context-transformweapon) | Block | Transforms the equipped weapon into another specific weapon state. | 1 |

</details>

---

### Context: `DurabilityTransform`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/11) |
| :--- | :--- | :--- | :--- |
| [`eq`](./Arrays.md#array-eq) | Array |  | 11 |
| [`ge`](./Arrays.md#array-ge) | Array |  | 4 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Items_and_Equipment.md#context-addpassivestominions), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/10) |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. | 10 |
| `Knockback` | Number | Applies or references the 'Knockback' effect/state. | 10 |
| `Poison` | Number | Applies or references the 'Poison' effect/state. | 7 |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 5 |
| [`Fear`](./Arrays.md#array-fear) | Array | Applies or references the 'Fear' effect/state. | 4 |
| `Slow` | Number | Applies or references the 'Slow' effect/state. | 4 |
| [`Tangled`](./Arrays.md#array-tangled) | Array | Applies a tangled/ensnared status effect, often modifying visual sprites. | 4 |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum/String | Transforms the terrain tile under the target. | 3 |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll) | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 3 |
| `DamageOrHealConditionally` | Number | Applies or references the 'DamageOrHealConditionally' effect/state. | 3 |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 2 |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 2 |
| `Rot` | Number | Applies or references the 'Rot' effect/state. | 2 |
| `SpiderInfested` | Number | Applies or references the 'SpiderInfested' effect/state. | 2 |
| [`Stun`](./Arrays.md#array-stun) | Array | Applies or references the 'Stun' effect/state. | 2 |
| `Weakness` | Number | Applies or references the 'Weakness' effect/state. | 2 |
| [`ApplyToSource`](./Items_and_Equipment.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| `Blind` | Number | Applies or references the 'Blind' effect/state. | 1 |
| [`ForceUseAbilityOnTarget`](./Items_and_Equipment.md#context-forceuseabilityontarget) | Block | Applies or references the 'ForceUseAbilityOnTarget' effect/state. | 1 |
| [`Freeze`](./Arrays.md#array-freeze) | Array | Applies or references the 'Freeze' effect/state. | 1 |
| `KnockOutCoin` | Number | Forces the target to drop coins. | 1 |
| [`KnockUpAndAway`](./Items_and_Equipment.md#context-knockupandaway) | Block | Displaces the target vertically and horizontally away from the source. | 1 |
| `Leech` | Number | Applies or references the 'Leech' effect/state. | 1 |
| `Leeches` | Number | Applies or references the 'Leeches' effect/state. | 1 |
| `MagicWeakness` | Number | Applies or references the 'MagicWeakness' effect/state. | 1 |
| `ManaLeeches` | Number | Applies or references the 'ManaLeeches' effect/state. | 1 |
| `Marked` | Number | Applies or references the 'Marked' effect/state. | 1 |
| `OverrideChainKnockback` | Number | Applies or references the 'OverrideChainKnockback' effect/state. | 1 |
| `PullSourceToTarget` | Number | Applies or references the 'PullSourceToTarget' effect/state. | 1 |
| `SoulLink` | Number | Applies or references the 'SoulLink' effect/state. | 1 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| [`effects`](./Items_and_Equipment.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 9 |
| `damage` | Number | The base damage properties of an attack. | 3 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](./Items_and_Equipment.md#context-dodamage), [`MeleeRevengeDamage`](./Items_and_Equipment.md#context-meleerevengedamage), [`RevengeDamage`](./Items_and_Equipment.md#context-revengedamage), [`damage_instance`](./Items_and_Equipment.md#context-damage_instance)

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 9 |
| [`BounceObject`](./Enums.md#enum-bounceobject) | Enum/String | Spawns a physics object that visually bounces off the target. | 4 |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 4 |
| [`Fear`](./Arrays.md#array-fear) | Array | Applies or references the 'Fear' effect/state. | 4 |
| [`Grappled`](./Arrays.md#array-grappled) | Array | Applies or references the 'Grappled' effect/state. | 4 |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll) | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 3 |
| `Immobile` | Number | Applies or references the 'Immobile' effect/state. | 3 |
| `Slow` | Number | Applies or references the 'Slow' effect/state. | 3 |
| `Poison` | Number | Applies or references the 'Poison' effect/state. | 2 |
| [`Stun`](./Arrays.md#array-stun) | Array | Applies or references the 'Stun' effect/state. | 2 |
| `Blind` | Number | Applies or references the 'Blind' effect/state. | 1 |
| `Cleave` | Number | Causes the attack to hit adjacent enemies alongside the primary target. | 1 |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 1 |
| [`Freeze`](./Arrays.md#array-freeze) | Array | Applies or references the 'Freeze' effect/state. | 1 |
| [`VisualFX`](./Enums.md#enum-visualfx) | Enum/String | Applies or references the 'VisualFX' effect/state. | 1 |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum/String | Applies or references the 'VisualFXTile' effect/state. | 1 |

</details>

---

### Context: `GainCoinsRange`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend), [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak), [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| `max` | Number | Maximum coins granted. | 7 |
| `min` | Number | Minimum coins granted. | 7 |

</details>

---

### Context: `PassiveIfStrAuxEquals`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | Passives granted by equipping this. | 7 |
| [`value`](./Enums.md#enum-value) | Enum/String |  | 7 |

</details>

---

### Context: `PassiveWhenOnTile`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | Passives granted by equipping this. | 7 |
| [`tile`](./Arrays.md#array-tile) | Array |  | 7 |

</details>

---

### Context: `ItemAuxTransform`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| [`le`](./Arrays.md#array-le) | Array |  | 6 |
| [`ge`](./Arrays.md#array-ge) | Array |  | 2 |
| [`lt`](./Arrays.md#array-lt) | Array |  | 1 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Applies or references the 'ForceUseAbility' effect/state. | 6 |
| `PartialCleanse` | Number | Applies or references the 'PartialCleanse' effect/state. | 4 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 4 |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll) | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 2 |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum/String | Applies or references the 'ImmediateUseAbility' effect/state. | 2 |
| `SpawnCoinAnywhere` | Number | Applies or references the 'SpawnCoinAnywhere' effect/state. | 2 |
| `AddWeaponAux` | Number | Applies or references the 'AddWeaponAux' effect/state. | 1 |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 1 |
| `Cleanse` | Number |  | 1 |
| [`Conditional_HasCleansableDebuffs`](./Items_and_Equipment.md#context-conditional_hascleansabledebuffs) | Block |  | 1 |
| [`Conditional_ManaThreshold`](./Items_and_Equipment.md#context-conditional_manathreshold) | Block | Conditional constraint. Nested properties only trigger if this is true. | 1 |
| `ConstitutionUp` | Number | Applies or references the 'ConstitutionUp' effect/state. | 1 |
| `PreEmptiveCounterNextAttacks` | Number | Applies or references the 'PreEmptiveCounterNextAttacks' effect/state. | 1 |
| `RandomStatUp` | Number |  | 1 |
| [`Stealth`](./Arrays.md#array-stealth) | Array | Applies or references the 'Stealth' effect/state. | 1 |

</details>

---

### Context: `AddPassivesToMinions`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 5 |
| `AddMaxHealth` | Number | Applies or references the 'AddMaxHealth' effect/state. | 4 |
| `DamageUp` | Number |  | 3 |
| [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 1 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 1 |
| [`Buddy`](./Enums.md#enum-buddy) | Enum/String |  | 1 |
| `ReturnBoundItemOnBattleEnd` | Number |  | 1 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 1 |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum/String |  | 1 |

</details>

---

### Context: `DelayedAutoRevive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 5 |
| `rounds` | Number |  | 5 |

</details>

---

### Context: `PassiveAtHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum/String |  | 5 |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | Passives granted by equipping this. | 5 |
| `threshold` | Number |  | 5 |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 5 |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 5 |

</details>

---

### Context: `StatusOnBreak`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| [`GainCoinsRange`](./Items_and_Equipment.md#context-gaincoinsrange) | Block | Grants the player a randomized amount of coins within a min/max range. | 5 |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 3 |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum/String | Applies or references the 'ChangeTilesUnder' effect/state. | 3 |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum/String | Generates an item drop from the specified loot pool. | 3 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 3 |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 3 |
| `PermanentConstitution` | Number | Applies or references the 'PermanentConstitution' effect/state. | 3 |
| [`ApplyToRandomPartyMemberIfPossible`](./Items_and_Equipment.md#context-applytorandompartymemberifpossible) | Block | Redirects the nested effects to apply to a random living member of the player's party. | 1 |
| `ConstitutionUp` | Number | Applies or references the 'ConstitutionUp' effect/state. | 1 |
| `DexterityUp` | Number | Applies or references the 'DexterityUp' effect/state. | 1 |
| [`FindItem`](./Enums.md#enum-finditem) | Enum/String | Applies or references the 'FindItem' effect/state. | 1 |
| [`GainDisorder`](./Enums.md#enum-gaindisorder) | Enum/String | Applies or references the 'GainDisorder' effect/state. | 1 |
| `IntelligenceUp` | Number | Applies or references the 'IntelligenceUp' effect/state. | 1 |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum/String | Spawns a specific character or entity upon impact. | 1 |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. | 1 |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 5 |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. | 2 |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. | 1 |
| [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus) | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 1 |
| [`Conditional_HealthThreshold`](./Items_and_Equipment.md#context-conditional_healththreshold) | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 1 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 1 |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array | Applies or references the 'DivineShield' effect/state. | 1 |
| `DodgeChance_Status` | Number | Applies or references the 'DodgeChance_Status' effect/state. | 1 |
| `RandomStatUp` | Number |  | 1 |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 1 |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. | 1 |
| [`Temporary`](./Items_and_Equipment.md#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 1 |

</details>

---

### Context: `Temporary`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_BadRoll`](./Items_and_Equipment.md#context-conditional_badroll), [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin), [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 5 |
| [`status`](./Enums.md#enum-status) | Enum/String | The status effect to apply. | 5 |
| `expires_on_end_turn` | Boolean |  | 4 |
| `turns` | Number | Duration in turns. | 4 |
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 1 |

</details>

---

### Context: `TransformItemOnElementInfluence`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | Specific element type required or applied. | 5 |
| `full_repair` | Boolean |  | 5 |
| [`item`](./Enums.md#enum-item) | Enum/String | Item ID to reference. | 5 |

</details>

---

### Context: `AddDamageToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 4 |
| [`element`](./Enums.md#enum-element) | Enum/String | Specific element type required or applied. | 4 |

</details>

---

### Context: `AddSelfStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. | 4 |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. | 1 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Applies or references the 'ForceUseAbility' effect/state. | 1 |
| [`Quivered`](./Arrays.md#array-quivered) | Array | Applies or references the 'Quivered' effect/state. | 1 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 1 |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `reduction` | Number |  | 4 |
| [`class`](./Enums.md#enum-class) | Enum/String | Character class identifier. | 3 |

</details>

---

### Context: `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage), [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum/String | The specific status effect ID to remove. | 4 |
| [`ApplyToSource`](./Items_and_Equipment.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 2 |
| `FlatLeechIfDamaged` | Number | Applies or references the 'FlatLeechIfDamaged' effect/state. | 1 |
| [`ImmediateUseAbility_Instant`](./Enums.md#enum-immediateuseability_instant) | Enum/String | Applies or references the 'ImmediateUseAbility_Instant' effect/state. | 1 |
| [`RemoveStatusStacks`](./Items_and_Equipment.md#context-removestatusstacks) | Block | Removes a specific number of stacks of a status effect. | 1 |

</details>

---

### Context: `Craft`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusIfUnusedActPoints`](./Items_and_Equipment.md#context-statusifunusedactpoints), [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum/String |  | 4 |
| [`slot`](./Enums.md#enum-slot) | Enum/String | Equipment slot (weapon, hat, face, chest, etc.). | 4 |
| `works_with_tech` | Boolean |  | 3 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll) | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 4 |
| `BrittleCharismaUp` | Number | Applies or references the 'BrittleCharismaUp' effect/state. | 1 |
| `BrittleConstitutionUp` | Number | Applies or references the 'BrittleConstitutionUp' effect/state. | 1 |
| `BrittleDexterityUp` | Number | Applies or references the 'BrittleDexterityUp' effect/state. | 1 |
| `BrittleIntelligenceUp` | Number | Applies or references the 'BrittleIntelligenceUp' effect/state. | 1 |
| `BrittleLuckUp` | Number | Applies or references the 'BrittleLuckUp' effect/state. | 1 |
| `BrittleSpeedUp` | Number | Applies or references the 'BrittleSpeedUp' effect/state. | 1 |
| `BrittleStrengthUp` | Number | Applies or references the 'BrittleStrengthUp' effect/state. | 1 |
| `CharismaUp` | Number | Applies or references the 'CharismaUp' effect/state. | 1 |
| `ConstitutionUp` | Number | Applies or references the 'ConstitutionUp' effect/state. | 1 |
| `DexterityUp` | Number | Applies or references the 'DexterityUp' effect/state. | 1 |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum/String | Applies or references the 'EquipPermanentItem' effect/state. | 1 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 1 |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 1 |
| `IntelligenceUp` | Number | Applies or references the 'IntelligenceUp' effect/state. | 1 |
| `LuckUp` | Number | Applies or references the 'LuckUp' effect/state. | 1 |
| `Shield` | Number |  | 1 |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 1 |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. | 1 |

</details>

---

### Context: `StatusOnKillEnemy`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 4 |
| `Brace` | Number | Applies or references the 'Brace' effect/state. | 1 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Applies or references the 'ForceUseAbility' effect/state. | 1 |
| `LuckUp` | Number | Applies or references the 'LuckUp' effect/state. | 1 |
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 1 |

</details>

---

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 4 |
| `AllStatsUp` | Number |  | 1 |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 1 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 1 |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 1 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 1 |
| `SpellDamageUp` | Number | Applies or references the 'SpellDamageUp' effect/state. | 1 |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. | 1 |

</details>

---

### Context: `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `count` | Number | Quantity. | 4 |
| `Charmed` | Number | Applies or references the 'Charmed' effect/state. | 1 |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 1 |
| `Fear` | Number | Applies or references the 'Fear' effect/state. | 1 |
| `Freeze` | Number | Applies or references the 'Freeze' effect/state. | 1 |

</details>

---

### Context: `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus) | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 3 |
| `must_do_damage` | Boolean |  | 3 |
| [`Conditional_HasTag`](./Items_and_Equipment.md#context-conditional_hastag) | Block | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 2 |
| `BonusKnockbackDamage` | Number | Applies or references the 'BonusKnockbackDamage' effect/state. | 1 |
| [`KnockbackIfCrit`](./Items_and_Equipment.md#context-knockbackifcrit) | Block | Applies or references the 'KnockbackIfCrit' effect/state. | 1 |
| `Rot` | Number | Applies or references the 'Rot' effect/state. | 1 |

</details>

---

### Context: `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | Applies or references the 'Quivered' effect/state. | 3 |
| `ally_chance` | Number |  | 3 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 3 |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`Temporary`](./Items_and_Equipment.md#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 3 |
| [`odds`](./Enums.md#enum-odds) | Enum/String | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 2 |

</details>

---

### Context: `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ExtraStatusWhenDealingDamage`](./Items_and_Equipment.md#context-extrastatuswhendealingdamage)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`Conditional_IsSelf`](./Abilities_and_Spells.md#context-conditional_isself) | Block | Conditional trigger: Executes nested logic if the target is the caster themselves. | 3 |
| [`Else`](./Items_and_Equipment.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 3 |

</details>

---

### Context: `CounterAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | ID of the ability to trigger or reference. | 3 |
| `melee_only` | Boolean |  | 1 |
| `ranged_only` | Boolean |  | 1 |

</details>

---

### Context: `DeathRattle`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String |  | 3 |
| `pop_corpse` | Boolean |  | 3 |

</details>

---

### Context: `Else`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToFirstSpellEachTurn`](./Items_and_Equipment.md#context-addstatustofirstspelleachturn), [`Conditional_PartyMember`](./Items_and_Equipment.md#context-conditional_partymember)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`ApplyToSource`](./Items_and_Equipment.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 |
| `Webbed` | Number |  | 1 |

</details>

---

### Context: `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`Conditional_PartyMember`](./Items_and_Equipment.md#context-conditional_partymember) | Block | Conditional constraint. Nested properties only trigger if this is true. | 3 |

</details>

---

### Context: `PassiveAtStatThreshold`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum/String |  | 3 |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | Passives granted by equipping this. | 3 |
| [`threshold`](./Items_and_Equipment.md#context-threshold) | Block |  | 3 |

</details>

---

### Context: `SetItemAux`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Shielded`](./Items_and_Equipment.md#context-conditional_shielded), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum/String | Equipment slot (weapon, hat, face, chest, etc.). | 3 |
| [`value`](./Enums.md#enum-value) | Enum/String |  | 3 |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `number` | Number |  | 3 |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 3 |

</details>

---

### Context: `StackingFlowerTrail`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum/String |  | 3 |
| `stacks` | Number | Number of stacks or intensity to apply. | 3 |

</details>

---

### Context: `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 3 |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 1 |
| `IntelligenceUp` | Number | Applies or references the 'IntelligenceUp' effect/state. | 1 |
| [`ObjectOnHitCharacter`](./Items_and_Equipment.md#context-objectonhitcharacter) | Block | Spawns a specific character or entity upon impact. | 1 |

</details>

---

### Context: `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`Craft`](./Items_and_Equipment.md#context-craft) | Block | Synthesizes or spawns a new item from a specific pool. | 3 |
| `SafeDie` | Number | Applies or references the 'SafeDie' effect/state. | 2 |
| [`Brace`](./Enums.md#enum-brace) | Enum/String | Applies or references the 'Brace' effect/state. | 1 |
| [`DestroyEquipmentAndAttachParasite`](./Items_and_Equipment.md#context-destroyequipmentandattachparasite) | Block | Removes an equipped item and replaces it with a parasite from a specified pool. | 1 |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum/String | Generates an item drop from the specified loot pool. | 1 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Applies or references the 'ForceUseAbility' effect/state. | 1 |
| [`ObjectOnHitCharacter`](./Items_and_Equipment.md#context-objectonhitcharacter) | Block | Spawns a specific character or entity upon impact. | 1 |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. | 1 |
| [`ReviveNextRound`](./Items_and_Equipment.md#context-revivenextround) | Block | Queues the character to be resurrected at the start of the next combat round. | 1 |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. | 1 |
| `StealthUntilBasicAttack` | Number | Applies or references the 'StealthUntilBasicAttack' effect/state. | 1 |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 3 |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 3 |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 1 |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum/String | Applies or references the 'ImmediateUseAbility' effect/state. | 1 |

</details>

---

### Context: `AddStatusToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | Specific element type required or applied. | 2 |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 1 |
| [`Stun`](./Arrays.md#array-stun) | Array | Applies or references the 'Stun' effect/state. | 1 |

</details>

---

### Context: `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`GainDisorderFromPool`](./Enums.md#enum-gaindisorderfrompool) | Enum/String | Applies or references the 'GainDisorderFromPool' effect/state. | 2 |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus), [`Else`](./Items_and_Equipment.md#context-else)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 2 |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 2 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 1 |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 1 |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. | 1 |

</details>

---

### Context: `ArmorBreakOnHit`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `chance_to_break` | Number |  | 2 |
| `durability_loss` | Number |  | 2 |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to autocast. | 2 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 2 |

</details>

---

### Context: `BoostWeaponDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `crit_chance` | Number |  | 2 |
| `damage` | Number | The base damage properties of an attack. | 2 |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | ID of the ability to trigger or reference. | 2 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |

</details>

---

### Context: `ChanceToRevive`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusAllCharactersOnSpawn`](./Items_and_Equipment.md#context-statusallcharactersonspawn)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 2 |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum/String | The specific string tag to check for. | 2 |
| `BonusCritChance` | Number |  | 1 |
| `BonusKnockbackDamage` | Number | Applies or references the 'BonusKnockbackDamage' effect/state. | 1 |
| `OverrideChainKnockback` | Number | Applies or references the 'OverrideChainKnockback' effect/state. | 1 |

</details>

---

### Context: `DoDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachRoundEnd`](./Items_and_Equipment.md#context-statuseachroundend), [`StatusOnBreakItem`](./Items_and_Equipment.md#context-statusonbreakitem)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The flat damage amount. | 2 |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum/String |  | 2 |
| [`effects`](./Items_and_Equipment.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`type`](./Enums.md#enum-type) | Enum/String | The classification of the damage (e.g., spell, melee). | 2 |

</details>

---

### Context: `ElementalManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array | Specific element type required or applied. | 2 |
| `reduction` | Number |  | 2 |

</details>

---

### Context: `ModifyAbility`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Items_and_Equipment.md#context-bonus_passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`cost`](./Items_and_Equipment.md#context-cost) | Block | Currency value in shops/merchants. | 2 |
| [`meta`](./Items_and_Equipment.md#context-meta) | Block |  | 2 |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhileHasDurability`](./Items_and_Equipment.md#context-passivewhilehasdurability), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | ID of the ability to trigger or reference. | 2 |
| `create_temp_ability` | Boolean |  | 2 |
| `enemies_only` | Boolean |  | 2 |
| `on_self_move_too` | Boolean |  | 1 |

</details>

---

### Context: `ObjectOnHitCharacter`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEveryXSpellCasts`](./Items_and_Equipment.md#context-statuseveryxspellcasts), [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String | The entity ID of the character to spawn (e.g., CharmedFlea). | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `PassiveAfterXKills`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | Passives granted by equipping this. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `PassiveIfWeaponIsUsable`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | Applies or references the 'Brace' effect/state. | 2 |

</details>

---

### Context: `RefreshEquipmentAbilityOnElement`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | Specific element type required or applied. | 2 |
| `text` | String |  | 2 |

</details>

---

### Context: `SpawnCatCopyWhenDowned`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 2 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum/String |  | 2 |

</details>

---

### Context: `SpawnItemLinkedFamiliar`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean |  | 2 |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 2 |

</details>

---

### Context: `StatusAfterXStacks`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusonspendmana), [`StatusOnCollectPickup`](./Items_and_Equipment.md#context-statusoncollectpickup)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum/String |  | 2 |
| `threshold` | Number |  | 2 |
| `ExtraBasicMoves_Status` | Number | Applies or references the 'ExtraBasicMoves_Status' effect/state. | 1 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 1 |
| `expires_on_end_turn` | Boolean |  | 1 |

</details>

---

### Context: `StatusAllCharactersOnSpawn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Conditional_Boss`](./Items_and_Equipment.md#context-conditional_boss) | Block | Conditional trigger: Executes nested logic if the target is a Boss. | 2 |
| `Poison` | Number | Applies or references the 'Poison' effect/state. | 1 |

</details>

---

### Context: `StatusAlliesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 2 |
| `Brace` | Number | Applies or references the 'Brace' effect/state. | 1 |
| `ConstitutionUp` | Number | Applies or references the 'ConstitutionUp' effect/state. | 1 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 1 |
| `IntelligenceUp` | Number |  | 1 |
| `LuckUp` | Number |  | 1 |
| `Shield` | Number |  | 1 |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. | 1 |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Conditional_BadRoll`](./Items_and_Equipment.md#context-conditional_badroll) | Block | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. | 2 |
| `BlessingOfPeace` | Number | Applies or references the 'BlessingOfPeace' effect/state. | 1 |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 1 |
| `DestroyTrinket` | Number | Applies or references the 'DestroyTrinket' effect/state. | 1 |
| `DoubleCastSpellThisTurn` | Number | Applies or references the 'DoubleCastSpellThisTurn' effect/state. | 1 |
| `DrinkWater` | Number | Applies or references the 'DrinkWater' effect/state. | 1 |
| [`ManaGainRange`](./Items_and_Equipment.md#context-managainrange) | Block | Applies or references the 'ManaGainRange' effect/state. | 1 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 1 |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 1 |
| [`Temporary`](./Items_and_Equipment.md#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 1 |
| [`UseAbility`](./Enums.md#enum-useability) | Enum/String | Forces the character or target to instantly use a specified ability. | 1 |
| `Wet` | Number | Applies or references the 'Wet' effect/state. | 1 |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 2 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 2 |
| `DivineShield` | Number |  | 1 |

</details>

---

### Context: `StatusOnTakeHealthOrShieldDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array | Applies or references the 'DivineShield' effect/state. | 2 |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll) | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 1 |
| `Metronome` | Number | Executes a random musical or metronome ability. | 1 |

</details>

---

### Context: `bonus_passives`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`str_aux_is_copy_ability`](./Items_and_Equipment.md#context-str_aux_is_copy_ability)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ModifyAbility`](./Items_and_Equipment.md#context-modifyability) | Block | Applies or references the 'ModifyAbility' effect/state. | 2 |

</details>

---

### Context: `cost`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ModifyAbility`](./Items_and_Equipment.md#context-modifyability)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `charge` | Number |  | 2 |
| `mana` | Number |  | 2 |

</details>

---

### Context: `global_passives`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `GlobalEnemyAutoRevive` | Number | Applies or references the 'GlobalEnemyAutoRevive' effect/state. | 2 |
| `NoCorpses` | Number | Applies or references the 'NoCorpses' effect/state. | 1 |
| `RealTimePressure` | Number | Applies or references the 'RealTimePressure' effect/state. | 1 |

</details>

---

### Context: `meta`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ModifyAbility`](./Items_and_Equipment.md#context-modifyability)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `is_basic_attack` | Boolean |  | 2 |
| `is_weapon` | Boolean |  | 2 |

</details>

---

### Context: `passive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Metal` | Number | Applies or references the 'Metal' effect/state. | 2 |

</details>

---

### Context: `str_aux_is_copy_ability`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`bonus_passives`](./Items_and_Equipment.md#context-bonus_passives) | Block | Passives granted to the character while this ability is equipped. | 2 |

</details>

---

### Context: `threshold`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 2 |
| `con` | Number |  | 1 |

</details>

---

### Context: `AIControlNextTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `AbilityHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | ID of the ability to trigger or reference. | 1 |
| `aux` | Number |  | 1 |
| `even_if_stunned` | Boolean |  | 1 |
| `immediate` | Boolean |  | 1 |
| [`threshold`](./Enums.md#enum-math_equation) | Equation |  | 1 |

</details>

---

### Context: `AbilityOnRoundEndOnce`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | ID of the ability to trigger or reference. | 1 |
| `even_of_stunned` | Boolean |  | 1 |

</details>

---

### Context: `AddAdvantageToEvent`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `add` | Number |  | 1 |
| [`options`](./Arrays.md#array-options) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `AddPassivesToCharmed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 1 |

</details>

---

### Context: `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array | Applies or references the 'RepairWeapon' effect/state. | 1 |

</details>

---

### Context: `AddStatusToBackstabs`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. | 1 |

</details>

---

### Context: `AddStatusToFirstSpellEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_IsSelf`](./Abilities_and_Spells.md#context-conditional_isself) | Block |  | 1 |
| [`Else`](./Items_and_Equipment.md#context-else) | Block |  | 1 |

</details>

---

### Context: `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 1 |
| [`Stun`](./Arrays.md#array-stun) | Array | Applies or references the 'Stun' effect/state. | 1 |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_Enemy`](./Items_and_Equipment.md#context-conditional_enemy) | Block | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 1 |
| `Leech` | Number | Applies or references the 'Leech' effect/state. | 1 |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Leech` | Number | Applies or references the 'Leech' effect/state. | 1 |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`CastAgainWithStatus`](./Items_and_Equipment.md#context-castagainwithstatus) | Block | Applies or references the 'CastAgainWithStatus' effect/state. | 1 |

</details>

---

### Context: `AlluringDoodieEater`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| [`damage_instance`](./Items_and_Equipment.md#context-damage_instance) | Block |  | 1 |

</details>

---

### Context: `AllyDodgeChanceAura`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| `range` | Number | Distance or area of effect in tiles. | 1 |

</details>

---

### Context: `ApplyPassives`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_RandomChance`](./Items_and_Equipment.md#context-conditional_randomchance)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend) | Block | Applies the nested status effects when the encounter finishes. | 1 |

</details>

---

### Context: `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Bounty` | Number | Applies or references the 'Bounty' effect/state. | 1 |
| `Marked` | Number | Applies or references the 'Marked' effect/state. | 1 |
| `count` | Number | Quantity. | 1 |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific dodge ability to trigger (e.g., DestroyerDodge). | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `BouncyProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number |  | 1 |
| `max_range` | Number |  | 1 |

</details>

---

### Context: `BuffImmunity`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`exclude`](./Enums.md#enum-exclude) | Enum/String |  | 1 |

</details>

---

### Context: `CastAgainWithStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddTemporaryEffectsToBasicAttack`](./Items_and_Equipment.md#context-addtemporaryeffectstobasicattack)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | Number | Applies or references the 'OverrideDamage' effect/state. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `CatPartsSizeScale`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `head` | Number |  | 1 |

</details>

---

### Context: `ChanceToBlockAndCounter`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean |  | 1 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Context: `ChanceToForceEvent`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| [`event`](./Enums.md#enum-event) | Enum/String |  | 1 |

</details>

---

### Context: `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusAlliesOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusalliesonspendmana), [`StatusAlliesEachTurn`](./Items_and_Equipment.md#context-statusallieseachturn)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_Ally`](./Items_and_Equipment.md#context-conditional_ally) | Block | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 1 |
| [`Conditional_PlayerCat`](./Items_and_Equipment.md#context-conditional_playercat) | Block | Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 1 |

</details>

---

### Context: `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 1 |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `RandomMutation` | Number | Applies or references the 'RandomMutation' effect/state. | 1 |

</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToSpells`](./Items_and_Equipment.md#context-addstatustospells)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Leeches` | Number | Applies or references the 'Leeches' effect/state. | 1 |

</details>

---

### Context: `Conditional_HasCleansableDebuffs`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`VisualFX`](./Enums.md#enum-visualfx) | Enum/String |  | 1 |

</details>

---

### Context: `Conditional_HealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](./Items_and_Equipment.md#context-conditional_onceperbattle) | Block | Conditional trigger: Executes nested logic only once per encounter/battle. | 1 |
| `threshold_flat` | Number | A flat numerical health value threshold. | 1 |

</details>

---

### Context: `Conditional_ManaThreshold`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `RepairTrinket` | Number | Applies or references the 'RepairTrinket' effect/state. | 1 |
| `threshold_flat` | Number |  | 1 |

</details>

---

### Context: `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HealthThreshold`](./Items_and_Equipment.md#context-conditional_healththreshold), [`StatusOnFullMana`](./Items_and_Equipment.md#context-statusonfullmana)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `ReduceManaCost` | Number | Applies or references the 'ReduceManaCost' effect/state. | 1 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 1 |
| `ShowText` | String | Applies or references the 'ShowText' effect/state. | 1 |
| `SpellDamageUp` | Number | Applies or references the 'SpellDamageUp' effect/state. | 1 |
| [`key`](./Enums.md#enum-key) | Enum/String |  | 1 |

</details>

---

### Context: `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 1 |

</details>

---

### Context: `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ApplyPassives`](./Items_and_Equipment.md#context-applypassives) | Block | Grants the nested passive abilities dynamically. | 1 |
| `odds` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Context: `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`SetItemAux`](./Items_and_Equipment.md#context-setitemaux) | Block | Applies or references the 'SetItemAux' effect/state. | 1 |

</details>

---

### Context: `ConvertDamageToScaledStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `DelayedPain` | Number | Applies or references the 'DelayedPain' effect/state. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `CreateGlobalModifiers`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `NextPlayerCatTakesExtraTurn` | Number | Applies or references the 'NextPlayerCatTakesExtraTurn' effect/state. | 1 |
| `NoCorpses` | Number | Applies or references the 'NoCorpses' effect/state. | 1 |

</details>

---

### Context: `CritsApplyStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Fear` | Number | Applies or references the 'Fear' effect/state. | 1 |

</details>

---

### Context: `CyborgTurns`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`TakeBonusTurnWithAIControl`](./Items_and_Equipment.md#context-takebonusturnwithaicontrol) | Block |  | 1 |
| `stacks` | Number |  | 1 |

</details>

---

### Context: `DestroyEquipmentAndAttachParasite`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum/String | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| [`pool`](./Arrays.md#array-pool) | Array | The item pool to draw the parasite from. | 1 |

</details>

---

### Context: `Eternal`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `health_percent` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `FlyDamageIncrease`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `ForceUseAbilityOnTarget`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | ID of the ability to trigger or reference. | 1 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Context: `GlobalFlowerTrapperAura`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Tangled`](./Arrays.md#array-tangled) | Array |  | 1 |

</details>

---

### Context: `GlobalMeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `knockback` | Number |  | 1 |

</details>

---

### Context: `ImmediateUseAbility`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | ID of the ability to trigger or reference. | 1 |
| `even_if_stunned` | Boolean |  | 1 |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `distance` | Number | The distance in tiles to knock the target away. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `KnockbackIfCrit`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `knockback` | Number |  | 1 |
| `override_chain_knockback` | Number |  | 1 |

</details>

---

### Context: `ManaGainRange`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `max` | Number |  | 1 |
| `min` | Number |  | 1 |

</details>

---

### Context: `ObjectDetector`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 1 |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | Specific element type required or applied. | 1 |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | Passives granted by equipping this. | 1 |

</details>

---

### Context: `PassiveWhenDead`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`AutocastEachRound`](./Items_and_Equipment.md#context-autocasteachround) | Block | Forces the character to automatically cast a specific ability at the start of each combat round. | 1 |
| [`StatusEachRoundEnd`](./Items_and_Equipment.md#context-statuseachroundend) | Block | Applies or references the 'StatusEachRoundEnd' effect/state. | 1 |
| [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin) | Block | Applies or references the 'StatusEachTurnBegin' effect/state. | 1 |

</details>

---

### Context: `PassiveWhileHasDurability`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`MovementReaction`](./Items_and_Equipment.md#context-movementreaction) | Block | Applies or references the 'MovementReaction' effect/state. | 1 |

</details>

---

### Context: `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | Applies or references the 'Brace' effect/state. | 1 |

</details>

---

### Context: `PassiveWhileShielded`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 1 |

</details>

---

### Context: `PoopWhenHit`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 1 |

</details>

---

### Context: `RandomPermanentStatsDistinct`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEatPill`](./Items_and_Equipment.md#context-statusoneatpill)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`stats`](./Arrays.md#array-stats) | Array |  | 1 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `PermanentCharisma` | Number | Applies or references the 'PermanentCharisma' effect/state. | 1 |
| `PermanentConstitution` | Number | Applies or references the 'PermanentConstitution' effect/state. | 1 |
| `PermanentDexterity` | Number | Applies or references the 'PermanentDexterity' effect/state. | 1 |
| `PermanentIntelligence` | Number | Applies or references the 'PermanentIntelligence' effect/state. | 1 |
| `PermanentLuck` | Number | Applies or references the 'PermanentLuck' effect/state. | 1 |
| `PermanentSpeed` | Number | Applies or references the 'PermanentSpeed' effect/state. | 1 |
| `PermanentStrength` | Number | Applies or references the 'PermanentStrength' effect/state. | 1 |

</details>

---

### Context: `RemoveStatusStacks`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks to remove. | 1 |
| [`status`](./Enums.md#enum-status) | Enum/String | The specific status effect ID to remove. | 1 |

</details>

---

### Context: `ReviveNextRound`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 1 |
| `revive_health` | Number | The flat amount of health to revive with. | 1 |

</details>

---

### Context: `Robot`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean |  | 1 |

</details>

---

### Context: `ScaldingOrbMoonBossOneShot`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum/String | Applies or references the 'CompleteItemQuest' effect/state. | 1 |
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum/String | Applies or references the 'RemoveItem' effect/state. | 1 |

</details>

---

### Context: `ScaledStatusAlliesOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent) | Block | Conditional constraint. Nested properties only trigger if this is true. | 1 |

</details>

---

### Context: `ScaledStatusOnHolyShieldBlock`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. | 1 |

</details>

---

### Context: `ScaledStatusOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`StatusAfterXStacks`](./Items_and_Equipment.md#context-statusafterxstacks) | Block | Applies or references the 'StatusAfterXStacks' effect/state. | 1 |

</details>

---

### Context: `SpawnCatCopyOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 1 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum/String |  | 1 |

</details>

---

### Context: `SpawnObjectOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `count` | Number | Quantity. | 1 |
| `except_tiny` | Boolean |  | 1 |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 1 |

</details>

---

### Context: `SpawnOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum/String |  | 1 |
| [`obj`](./Enums.md#enum-obj) | Enum/String |  | 1 |

</details>

---

### Context: `SpawnRandomPickupsOnTaggedUnitKilled`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array | Quantity. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String | Specific entity tag required. | 1 |

</details>

---

### Context: `StatDependentPassive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`AddDamageToBasicAttack`](./Enums.md#enum-math_equation) | Equation | Applies or references the 'AddDamageToBasicAttack' effect/state. | 1 |

</details>

---

### Context: `StatusAdjacentOnTheirTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `ForceMoveAway` | Number | Applies or references the 'ForceMoveAway' effect/state. | 1 |

</details>

---

### Context: `StatusAfterCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `TempMeleeRangeUp` | Number | Applies or references the 'TempMeleeRangeUp' effect/state. | 1 |
| `TempRangeUp` | Number | Applies or references the 'TempRangeUp' effect/state. | 1 |
| [`UseAbility`](./Enums.md#enum-useability) | Enum/String | Forces the character or target to instantly use a specified ability. | 1 |

</details>

---

### Context: `StatusAfterXTurns`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Applies or references the 'ForceUseAbility' effect/state. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `StatusAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent) | Block | Conditional constraint. Nested properties only trigger if this is true. | 1 |

</details>

---

### Context: `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 1 |

</details>

---

### Context: `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`DoDamage`](./Items_and_Equipment.md#context-dodamage) | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 1 |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Applies or references the 'ForceUseAbility' effect/state. | 1 |

</details>

---

### Context: `StatusIfUnusedActPoints`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`BackflipWhenTargeted`](./Enums.md#enum-backflipwhentargeted) | Enum/String | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. | 1 |
| [`Craft`](./Items_and_Equipment.md#context-craft) | Block | Synthesizes or spawns a new item from a specific pool. | 1 |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 1 |
| `RepairTrinket` | Number | Applies or references the 'RepairTrinket' effect/state. | 1 |

</details>

---

### Context: `StatusOnBackstab`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 1 |
| `SerratedClaws` | Number | Applies or references the 'SerratedClaws' effect/state. | 1 |

</details>

---

### Context: `StatusOnBreakItem`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`DoDamage`](./Items_and_Equipment.md#context-dodamage) | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 1 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 1 |

</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 1 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 1 |

</details>

---

### Context: `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`StatusAfterXStacks`](./Items_and_Equipment.md#context-statusafterxstacks) | Block | Applies or references the 'StatusAfterXStacks' effect/state. | 1 |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_RandomChance`](./Items_and_Equipment.md#context-conditional_randomchance) | Block | Conditional trigger: Executes nested logic based on a flat percentage random roll. | 1 |
| [`CreateGlobalModifiers`](./Items_and_Equipment.md#context-createglobalmodifiers) | Block | Generates global map or encounter rules/modifiers. | 1 |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum/String | Generates an item drop from the specified loot pool. | 1 |
| [`GainCoinsRange`](./Items_and_Equipment.md#context-gaincoinsrange) | Block | Grants the player a randomized amount of coins within a min/max range. | 1 |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. | 1 |
| [`RandomStatusFromPool`](./Items_and_Equipment.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `StatusOnDodge`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Number | Applies or references the 'DodgeChance_Status' effect/state. | 1 |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `RepairTrinket` | Number | Applies or references the 'RepairTrinket' effect/state. | 1 |
| [`TempPassiveUntilSettled`](./Items_and_Equipment.md#context-temppassiveuntilsettled) | Block | Applies or references the 'TempPassiveUntilSettled' effect/state. | 1 |

</details>

---

### Context: `StatusOnEatPill`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`RandomPermanentStatsDistinct`](./Items_and_Equipment.md#context-randompermanentstatsdistinct) | Block |  | 1 |

</details>

---

### Context: `StatusOnEnemyDeath`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 1 |

</details>

---

### Context: `StatusOnFallAsleep`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 1 |
| `FillMana` | Number | Applies or references the 'FillMana' effect/state. | 1 |
| `HealRandomInjury` | Number | Applies or references the 'HealRandomInjury' effect/state. | 1 |

</details>

---

### Context: `StatusOnFullMana`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](./Items_and_Equipment.md#context-conditional_onceperbattle) | Block | Conditional trigger: Executes nested logic only once per encounter/battle. | 1 |

</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | Applies or references the 'LuckUp' effect/state. | 1 |
| [`Shield`](./Enums.md#enum-shield) | Enum/String | Applies or references the 'Shield' effect/state. | 1 |

</details>

---

### Context: `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 1 |

</details>

---

### Context: `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `GainCoins` | Number | Applies or references the 'GainCoins' effect/state. | 1 |

</details>

---

### Context: `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 1 |
| `RepairTrinket` | Number | Applies or references the 'RepairTrinket' effect/state. | 1 |
| `RepairWeapon` | Number | Applies or references the 'RepairWeapon' effect/state. | 1 |

</details>

---

### Context: `StatusOnSetPieceBreak`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum/String |  | 1 |
| `PermanentCharisma` | Number |  | 1 |
| `PermanentConstitution` | Number |  | 1 |
| `PermanentDexterity` | Number |  | 1 |
| `PermanentIntelligence` | Number |  | 1 |
| `PermanentLuck` | Number |  | 1 |
| `PermanentSpeed` | Number |  | 1 |
| `PermanentStrength` | Number |  | 1 |
| [`set`](./Enums.md#enum-set) | Enum/String |  | 1 |

</details>

---

### Context: `StatusOnTurnEndIfCastNSpells`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `DoubleCastSpell` | Number |  | 1 |
| `spells` | Number |  | 1 |

</details>

---

### Context: `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 1 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 1 |

</details>

---

### Context: `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 1 |

</details>

---

### Context: `TakeBonusTurnWithAIControl`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CyborgTurns`](./Items_and_Equipment.md#context-cyborgturns)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `end_of_round` | Boolean |  | 1 |
| `include_spells` | Boolean |  | 1 |

</details>

---

### Context: `TempPassiveUntilSettled`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEatFood`](./Items_and_Equipment.md#context-statusoneatfood)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `LimitHeal` | Number | Applies or references the 'LimitHeal' effect/state. | 1 |

</details>

---

### Context: `TintItem`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`add`](./Arrays.md#array-add) | Array |  | 1 |
| [`ignore_if_str_aux_equals`](./Enums.md#enum-ignore_if_str_aux_equals) | Enum/String |  | 1 |
| [`mul`](./Arrays.md#array-mul) | Array |  | 1 |

</details>

---

### Context: `TransformWeapon`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum/String | The original weapon ID. | 1 |
| [`to`](./Enums.md#enum-to) | Enum/String | The transformed weapon ID. | 1 |

</details>

---

### Context: `TunnelVision`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `crit_chance` | Number |  | 1 |

</details>

---

### Context: `damage_instance`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AlluringDoodieEater`](./Items_and_Equipment.md#context-alluringdoodieeater)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Items_and_Equipment.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification type. | 1 |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 1 |
| `Immobile` | Number | Applies or references the 'Immobile' effect/state. | 1 |

</details>

---

