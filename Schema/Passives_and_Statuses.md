# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Passives & Statuses

> **Associated Files:** `data/passives/, data/passive_pools.gon`


### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 885

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String | {'type': '`String`', 'df': "Localization key for the passive's display description."} | 885 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block | {'type': '`Block`', 'df': " | 862 |
| [`name`](./Strings.md#string-name) | String | {'type': '`String`', 'df': "Localization key for the passive's display name."} | 512 |
| [`class`](./Enums.md#enum-class) | Enum | {'type': '`Enum/String`', 'df': 'Character class identifier.'} | 510 |
| [`stats`](./Passives_and_Statuses.md#context-stats) | Block | {'type': '`Block`', 'df': ' | 97 |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack) | Block | {'type': 'Block', 'df': 'Injects a status effect payload that applies whenever the character performs a basic attack.'} | 38 |
| `con` | Number | {'type': 'Number', 'df': ''} | 18 |
| `spd` | Number | {'type': 'Number', 'df': ''} | 17 |
| `CritChanceUp` | Number | {'type': 'Number', 'df': "Applies the 'CritChanceUp' effect."} | 16 |
| [`lock_item_slot`](./Passives_and_Statuses.md#context-lock_item_slot) | Block | {'type': '`Block`', 'df': ' | 16 |
| [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions) | Block | {'type': 'Block', 'df': "Applies the 'AddPassivesToMinions' effect."} | 15 |
| `AddCritMultiplier` | Number | {'type': 'Number', 'df': "Applies the 'AddCritMultiplier' effect."} | 14 |
| `cha` | Number | {'type': 'Number', 'df': ''} | 13 |
| [`MulticlassLevelUp`](./Enums.md#enum-multiclasslevelup) | Enum | {'type': 'Enum/String', 'df': "Applies the 'MulticlassLevelUp' effect."} | 12 |
| [`SpawnOnBattleStart`](./Passives_and_Statuses.md#context-spawnonbattlestart) | Block | {'type': 'Enum/String', 'df': "Applies the 'SpawnOnBattleStart' effect."} | 12 |
| `int` | Number | {'type': 'Number', 'df': ''} | 12 |
| `str` | Number | {'type': 'Number', 'df': ''} | 12 |
| [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when took damage.'} | 11 |
| `MissChance` | Number | {'type': 'Number', 'df': "Applies the 'MissChance' effect."} | 10 |
| [`desc_multiclass`](./Strings.md#string-desc_multiclass) | String | {'type': '`String`', 'df': ''} | 10 |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 10 |
| `lck` | Number | {'type': 'Number', 'df': ''} | 9 |
| `shield` | Number | {'type': '`Number`', 'df': ''} | 9 |
| `PassiveLevelUpAtCombatEnd` | Number | {'type': 'Number', 'df': "Applies the 'PassiveLevelUpAtCombatEnd' effect."} | 8 |
| [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when kill.'} | 8 |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | {'type': '`Array`', 'df': 'Flat addition to a base value.'} | 8 |
| `dex` | Number | {'type': 'Number', 'df': ''} | 8 |
| `AddBonusRange` | Number | {'type': 'Number', 'df': "Applies the 'AddBonusRange' effect."} | 7 |
| [`ReplaceSpawnedObjects`](./Arrays.md#array-replacespawnedobjects) | Array | {'type': 'Array', 'df': "Applies the 'ReplaceSpawnedObjects' effect."} | 7 |
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum | {'type': 'Enum/String', 'df': "Applies the 'BonusAbility' effect."} | 6 |
| [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus) | Block | {'type': 'Block', 'df': "Applies the 'CritsApplyStatus' effect."} | 6 |
| `HealthRegenUp` | Number | {'type': 'Number', 'df': "Applies the 'HealthRegenUp' effect."} | 6 |
| [`RevengeDamage`](./Passives_and_Statuses.md#context-revengedamage) | Block | {'type': 'Block', 'df': 'Reaction trigger: Deals damage to the attacker when hit.'} | 6 |
| `divine_shield` | Number | Examples: `3, 1` | 6 |
| [`keyword_tooltips`](./Passives_and_Statuses.md#context-keyword_tooltips) | Block | Examples: `{ ... }` | 6 |
| `Brace` | Number | {'type': 'Number', 'df': "Applies the 'Brace' effect."} | 5 |
| `ExtraMovePoints` | Number | {'type': 'Number', 'df': "Applies the 'ExtraMovePoints' effect."} | 5 |
| [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold) | Block | {'type': 'Block', 'df': "Applies the 'PassiveAtStatThreshold' effect."} | 5 |
| [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to each turn end.'} | 5 |
| [`StatusOnCrit`](./Passives_and_Statuses.md#context-statusoncrit) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when crit.'} | 5 |
| [`AddStatusToWeapons`](./Passives_and_Statuses.md#context-addstatustoweapons) | Block | {'type': 'Block', 'df': "Applies the 'AddStatusToWeapons' effect."} | 4 |
| [`AmplifyStatus`](./Passives_and_Statuses.md#context-amplifystatus) | Block | {'type': 'Enum/String', 'df': "Applies the 'AmplifyStatus' effect."} | 4 |
| `BoostWeaponDamage` | Number | {'type': 'Number', 'df': "Applies the 'BoostWeaponDamage' effect."} | 4 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | {'type': 'Enum/String', 'df': "Applies the 'ElementImmune' effect."} | 4 |
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum | {'type': 'Enum/String', 'df': "Applies the 'EquipTemporaryItem' effect."} | 4 |
| `ExtraWeaponAttacks` | Number | {'type': 'Number', 'df': "Applies the 'ExtraWeaponAttacks' effect."} | 4 |
| [`ForceSpecificInjury`](./Math_Equations.md) | Equation | {'type': 'Enum/String', 'df': "Applies the 'ForceSpecificInjury' effect."} | 4 |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum | {'type': 'Enum/String', 'df': "Applies the 'InnateElement' effect."} | 4 |
| [`ManaCostReductionTagged`](./Passives_and_Statuses.md#context-manacostreductiontagged) | Block | {'type': 'Block', 'df': "Applies the 'ManaCostReductionTagged' effect."} | 4 |
| [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty) | Block | {'type': 'Block', 'df': "Applies the 'PassiveIfAllArmorEmpty' effect."} | 4 |
| [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#context-passiveifemptyface) | Block | {'type': 'Block', 'df': "Applies the 'PassiveIfEmptyFace' effect."} | 4 |
| [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#context-passiveifemptyhead) | Block | {'type': 'Block', 'df': "Applies the 'PassiveIfEmptyHead' effect."} | 4 |
| [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#context-passiveifemptyneck) | Block | {'type': 'Block', 'df': "Applies the 'PassiveIfEmptyNeck' effect."} | 4 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | {'type': 'Enum/String', 'df': "Applies the 'ReplaceBasicAttack' effect."} | 4 |
| [`StatusAlliesOnDeath`](./Passives_and_Statuses.md#context-statusalliesondeath) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to allies on death.'} | 4 |
| [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#context-statusonuseabilitywithtag) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when use ability with tag.'} | 4 |
| `Trample` | Number | {'type': 'Number', 'df': "Applies the 'Trample' effect."} | 4 |
| `auto_plus_signs_on_name` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| [`empty_armor_scaled_stats`](./Passives_and_Statuses.md#context-empty_armor_scaled_stats) | Block | Examples: `{ ... }` | 4 |
| [`name_mod`](./Strings.md#string-name_mod) | String | {'type': '`String`', 'df': ''} | 4 |
| [`AbilityOnBattleStart`](./Enums.md#enum-abilityonbattlestart) | Enum | {'type': 'Enum/String', 'df': "Applies the 'AbilityOnBattleStart' effect."} | 3 |
| `AddBonusMeleeRange` | Number | {'type': 'Number', 'df': "Applies the 'AddBonusMeleeRange' effect."} | 3 |
| `AddCorpseHealth` | Number | {'type': 'Number', 'df': "Applies the 'AddCorpseHealth' effect."} | 3 |
| [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum | {'type': 'Enum/String', 'df': "Applies the 'AddElementsToBasicAttack' effect."} | 3 |
| [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities) | Block | {'type': 'Block', 'df': "Applies the 'AddStatusToElementAbilities' effect."} | 3 |
| `AlphaTurns` | Number | {'type': 'Number', 'df': "Applies the 'AlphaTurns' effect."} | 3 |
| `BasicAttackAOEBonus` | Number | {'type': 'Number', 'df': "Applies the 'BasicAttackAOEBonus' effect."} | 3 |
| `BasicAttackDamageMultiplier` | Number | {'type': 'Number', 'df': "Applies the 'BasicAttackDamageMultiplier' effect."} | 3 |
| `BlastResistance` | Number | {'type': 'Number', 'df': "Applies the 'BlastResistance' effect."} | 3 |
| `DodgeChance` | Number | {'type': 'Number', 'df': "Applies the 'DodgeChance' effect."} | 3 |
| [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage) | Block | {'type': 'Block', 'df': 'Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.'} | 3 |
| `MoveQuivered` | Number | {'type': 'Number', 'df': "Applies the 'MoveQuivered' effect."} | 3 |
| [`ReplaceBasicAttackWhenCastable`](./Enums.md#enum-replacebasicattackwhencastable) | Enum | {'type': 'Enum/String', 'df': "Applies the 'ReplaceBasicAttackWhenCastable' effect."} | 3 |
| [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to each turn begin.'} | 3 |
| [`StatusImmunity`](./Arrays.md#array-statusimmunity) | Array | {'type': 'Array', 'df': 'Event Trigger: Applies nested statuses to immunity.'} | 3 |
| [`StatusOnCastSpell`](./Passives_and_Statuses.md#context-statusoncastspell) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when cast spell.'} | 3 |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when stance switch.'} | 3 |
| [`tags`](./Arrays.md#array-tags) | Array | {'type': '`Array`', 'df': ''} | 3 |
| `AddDamageToBasicAttack` | Number | {'type': 'Number', 'df': "Applies the 'AddDamageToBasicAttack' effect."} | 2 |
| [`AddDamageToElementDamage`](./Passives_and_Statuses.md#context-adddamagetoelementdamage) | Block | {'type': 'Block', 'df': "Applies the 'AddDamageToElementDamage' effect."} | 2 |
| `AddKnockbackDamage` | Number | {'type': 'Number', 'df': "Applies the 'AddKnockbackDamage' effect."} | 2 |
| `AddMovement` | Number | {'type': 'Number', 'df': "Applies the 'AddMovement' effect."} | 2 |
| [`AddPassivesToCharmed`](./Passives_and_Statuses.md#context-addpassivestocharmed) | Block | {'type': 'Block', 'df': "Applies the 'AddPassivesToCharmed' effect."} | 2 |
| [`AddSelfStatusToBasicAttack`](./Passives_and_Statuses.md#context-addselfstatustobasicattack) | Block | {'type': 'Block', 'df': "Applies the 'AddSelfStatusToBasicAttack' effect."} | 2 |
| [`AddStatusToAllDamage`](./Passives_and_Statuses.md#context-addstatustoalldamage) | Block | {'type': 'Block', 'df': "Applies the 'AddStatusToAllDamage' effect."} | 2 |
| [`AddStatusToAllDamageAbilities`](./Passives_and_Statuses.md#context-addstatustoalldamageabilities) | Block | {'type': 'Block', 'df': "Applies the 'AddStatusToAllDamageAbilities' effect."} | 2 |
| [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack) | Block | {'type': 'Block', 'df': "Applies the 'AddStatusToBasicMeleeAttack' effect."} | 2 |
| [`AddStatusToElementDamage`](./Passives_and_Statuses.md#context-addstatustoelementdamage) | Block | {'type': 'Block', 'df': "Applies the 'AddStatusToElementDamage' effect."} | 2 |
| [`AddTemporaryEffectsToBasicAttack`](./Passives_and_Statuses.md#context-addtemporaryeffectstobasicattack) | Block | {'type': 'Block', 'df': "Applies the 'AddTemporaryEffectsToBasicAttack' effect."} | 2 |
| `AllyDamageReduction` | Number | {'type': 'Number', 'df': "Applies the 'AllyDamageReduction' effect."} | 2 |
| [`AllyManaRegenAura`](./Passives_and_Statuses.md#context-allymanaregenaura) | Block | {'type': 'Block', 'df': "Applies the 'AllyManaRegenAura' effect."} | 2 |
| `AmplifyKnockback` | Number | {'type': 'Number', 'df': "Applies the 'AmplifyKnockback' effect."} | 2 |
| [`AutocastEachRound`](./Passives_and_Statuses.md#context-autocasteachround) | Block | {'type': 'Block', 'df': 'Forces the character to automatically cast a specific ability at the start of each combat round.'} | 2 |
| [`CobraReflex`](./Enums.md#enum-cobrareflex) | Enum | {'type': 'Enum/String', 'df': "Applies the 'CobraReflex' effect."} | 2 |
| `ConsumablesInfiniteRange` | Number | {'type': 'Number', 'df': "Applies the 'ConsumablesInfiniteRange' effect."} | 2 |
| `DamageUp` | Number | {'type': 'Number', 'df': 'Combat Trigger: Deals damage to up.'} | 2 |
| [`ElementalManaCostReduction`](./Passives_and_Statuses.md#context-elementalmanacostreduction) | Block | {'type': 'Block', 'df': "Applies the 'ElementalManaCostReduction' effect."} | 2 |
| `ExtraBasicAttacks` | Number | {'type': 'Number', 'df': "Applies the 'ExtraBasicAttacks' effect."} | 2 |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum | {'type': 'Enum/String', 'df': "Applies the 'FreePathfindElement' effect."} | 2 |
| `FreezePiercing` | Number | {'type': 'Number', 'df': "Applies the 'FreezePiercing' effect."} | 2 |
| `IgnoreTiles` | Number | {'type': 'Number', 'df': "Applies the 'IgnoreTiles' effect."} | 2 |
| `IncreaseExplosionDamage` | Number | {'type': 'Number', 'df': "Applies the 'IncreaseExplosionDamage' effect."} | 2 |
| `KnockbackImmunity` | Number | {'type': 'Number', 'df': "Applies the 'KnockbackImmunity' effect."} | 2 |
| [`LevelUpClassOverride`](./Enums.md#enum-levelupclassoverride) | Enum | {'type': 'Enum/String', 'df': "Applies the 'LevelUpClassOverride' effect."} | 2 |
| [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#context-passiveathealththreshold) | Block | {'type': 'Block', 'df': "Applies the 'PassiveAtHealthThreshold' effect."} | 2 |
| [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#context-passivewhenatfullmana) | Block | {'type': 'Block', 'df': 'State Trigger: Grants nested passives when at full mana.'} | 2 |
| `Quivered` | Number | {'type': 'Number', 'df': "Applies the 'Quivered' effect."} | 2 |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum | {'type': 'Enum/String', 'df': "Applies the 'ReplaceBasicMove' effect."} | 2 |
| `SizeScale` | Mixed | {'type': 'Enum/String', 'df': "Applies the 'SizeScale' effect."} | 2 |
| [`SpawnCatCopyOnBattleStart`](./Passives_and_Statuses.md#context-spawncatcopyonbattlestart) | Block | {'type': 'Block', 'df': "Applies the 'SpawnCatCopyOnBattleStart' effect."} | 2 |
| [`SpawnEachTurn`](./Passives_and_Statuses.md#context-spawneachturn) | Block | {'type': 'Block', 'df': "Applies the 'SpawnEachTurn' effect."} | 2 |
| [`SpawnOnBattleStartRandomEmptyTile`](./Passives_and_Statuses.md#context-spawnonbattlestartrandomemptytile) | Block | {'type': 'Block', 'df': "Applies the 'SpawnOnBattleStartRandomEmptyTile' effect."} | 2 |
| [`SpawnThingOnDamage`](./Passives_and_Statuses.md#context-spawnthingondamage) | Block | {'type': 'Block', 'df': "Applies the 'SpawnThingOnDamage' effect."} | 2 |
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum | {'type': 'Enum/String', 'df': "Applies the 'SpawnThingOnDeath' effect."} | 2 |
| [`StatusEveryXSpellCasts`](./Passives_and_Statuses.md#context-statuseveryxspellcasts) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to every x spell casts.'} | 2 |
| [`StatusIfUnusedMovePoints`](./Passives_and_Statuses.md#context-statusifunusedmovepoints) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to if unused move points.'} | 2 |
| [`StatusOnGainCoins`](./Passives_and_Statuses.md#context-statusongaincoins) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when gain coins.'} | 2 |
| [`StatusOnHealed`](./Passives_and_Statuses.md#context-statusonhealed) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when healed.'} | 2 |
| [`StatusOnOverHealed`](./Passives_and_Statuses.md#context-statusonoverhealed) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when over healed.'} | 2 |
| [`StatusOnTurnEndIfCastNSpells`](./Passives_and_Statuses.md#context-statusonturnendifcastnspells) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when turn end if cast n spells.'} | 2 |
| [`StatusOnTurnEndIfManaExact`](./Passives_and_Statuses.md#context-statusonturnendifmanaexact) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when turn end if mana exact.'} | 2 |
| [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#context-statusonturnendifmanaorhealthexact) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when turn end if mana or health exact.'} | 2 |
| `TauntAlways` | Number | {'type': 'Number', 'df': "Applies the 'TauntAlways' effect."} | 2 |
| `Thorns` | Number | {'type': 'Number', 'df': "Applies the 'Thorns' effect."} | 2 |
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum | {'type': 'Enum/String', 'df': "Applies the 'TileTrail' effect."} | 2 |
| `UncappedMana` | Number | {'type': 'Number', 'df': "Applies the 'UncappedMana' effect."} | 2 |
| [`icon`](./Enums.md#enum-icon) | Enum | Examples: `DejaVu3, DejaVu2` | 2 |
| [`schadenfreude_scaled_stats`](./Passives_and_Statuses.md#context-schadenfreude_scaled_stats) | Block | Examples: `{ ... }` | 2 |
| [`AbilityChargeRefundChance`](./Passives_and_Statuses.md#context-abilitychargerefundchance) | Block | {'type': 'Block', 'df': "Applies the 'AbilityChargeRefundChance' effect."} | 1 |
| [`AbilityReaction`](./Enums.md#enum-abilityreaction) | Enum | {'type': 'Enum/String', 'df': "Applies the 'AbilityReaction' effect."} | 1 |
| [`AbilityWhenTaggedCharacterMovesNear`](./Passives_and_Statuses.md#context-abilitywhentaggedcharactermovesnear) | Block | {'type': 'Block', 'df': "Applies the 'AbilityWhenTaggedCharacterMovesNear' effect."} | 1 |
| `AbsorbManaAura` | Number | {'type': 'Number', 'df': "Applies the 'AbsorbManaAura' effect."} | 1 |
| `AddAllyNeighborsToAbilityRange` | Number | {'type': 'Number', 'df': "Applies the 'AddAllyNeighborsToAbilityRange' effect."} | 1 |
| `AddChaScalingSpellDamage` | Number | {'type': 'Number', 'df': "Applies the 'AddChaScalingSpellDamage' effect."} | 1 |
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum | {'type': 'Enum/String', 'df': "Applies the 'AddHiddenTag' effect."} | 1 |
| `AddKnockbackToEverything` | Number | {'type': 'Number', 'df': "Applies the 'AddKnockbackToEverything' effect."} | 1 |
| `AddLevelUpRerolls` | Number | {'type': 'Number', 'df': "Applies the 'AddLevelUpRerolls' effect."} | 1 |
| `AddManaRegen` | Number | {'type': 'Number', 'df': "Applies the 'AddManaRegen' effect."} | 1 |
| [`AddPassiveToSpawnedRocks`](./Passives_and_Statuses.md#context-addpassivetospawnedrocks) | Block | {'type': 'Block', 'df': "Applies the 'AddPassiveToSpawnedRocks' effect."} | 1 |
| [`AddPassivesToSummonAbilityMinions`](./Passives_and_Statuses.md#context-addpassivestosummonabilityminions) | Block | {'type': 'Block', 'df': "Applies the 'AddPassivesToSummonAbilityMinions' effect."} | 1 |
| `AddRangedCritChance` | Number | {'type': 'Number', 'df': "Applies the 'AddRangedCritChance' effect."} | 1 |
| [`AddSelfStatusToWeapons`](./Passives_and_Statuses.md#context-addselfstatustoweapons) | Block | {'type': 'Block', 'df': "Applies the 'AddSelfStatusToWeapons' effect."} | 1 |
| `AddSpellDamage` | Number | {'type': 'Number', 'df': "Applies the 'AddSpellDamage' effect."} | 1 |
| `AddStartingMana` | Number | {'type': 'Number', 'df': "Applies the 'AddStartingMana' effect."} | 1 |
| [`AddStatusToBasicAttackWithCooldown`](./Passives_and_Statuses.md#context-addstatustobasicattackwithcooldown) | Block | {'type': 'Block', 'df': "Applies the 'AddStatusToBasicAttackWithCooldown' effect."} | 1 |
| [`AddStatusToExplosions`](./Passives_and_Statuses.md#context-addstatustoexplosions) | Block | {'type': 'Block', 'df': "Applies the 'AddStatusToExplosions' effect."} | 1 |
| [`AddStatusToFirstBasicAttack`](./Passives_and_Statuses.md#context-addstatustofirstbasicattack) | Block | {'type': 'Block', 'df': "Applies the 'AddStatusToFirstBasicAttack' effect."} | 1 |
| [`AddStatusToKnockbackDamage`](./Passives_and_Statuses.md#context-addstatustoknockbackdamage) | Block | {'type': 'Block', 'df': "Applies the 'AddStatusToKnockbackDamage' effect."} | 1 |
| [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage) | Block | {'type': 'Block', 'df': "Applies the 'AddStatusToMeleeDamage' effect."} | 1 |
| [`AddStatusToSpells`](./Passives_and_Statuses.md#context-addstatustospells) | Block | {'type': 'Block', 'df': "Applies the 'AddStatusToSpells' effect."} | 1 |
| [`AddStatusToTrampleDamage`](./Passives_and_Statuses.md#context-addstatustotrampledamage) | Block | {'type': 'Block', 'df': "Applies the 'AddStatusToTrampleDamage' effect."} | 1 |
| [`AddTag`](./Enums.md#enum-addtag) | Enum | {'type': 'Enum/String', 'df': "Applies the 'AddTag' effect."} | 1 |
| [`AddTemporaryEffectsToEquipment`](./Passives_and_Statuses.md#context-addtemporaryeffectstoequipment) | Block | {'type': 'Block', 'df': "Applies the 'AddTemporaryEffectsToEquipment' effect."} | 1 |
| `AddUnfilledMaxHealth` | Number | {'type': 'Number', 'df': "Applies the 'AddUnfilledMaxHealth' effect."} | 1 |
| `AddWeaponScaling` | Number | {'type': 'Number', 'df': "Applies the 'AddWeaponScaling' effect."} | 1 |
| [`AfterImage`](./Enums.md#enum-afterimage) | Enum | {'type': 'Enum/String', 'df': "Spawns a visual decoy or shade at the caster's previous location."} | 1 |
| `AllDamageCrits` | Number | {'type': 'Number', 'df': "Applies the 'AllDamageCrits' effect."} | 1 |
| `AlliesAvoidTraps` | Number | {'type': 'Number', 'df': "Applies the 'AlliesAvoidTraps' effect."} | 1 |
| `AllowPassTurn` | Number | {'type': 'Number', 'df': "Applies the 'AllowPassTurn' effect."} | 1 |
| [`AllyBonusAbilityAura`](./Passives_and_Statuses.md#context-allybonusabilityaura) | Block | {'type': 'Enum/String', 'df': "Applies the 'AllyBonusAbilityAura' effect."} | 1 |
| `AllyChainKnockback` | Number | {'type': 'Number', 'df': "Applies the 'AllyChainKnockback' effect."} | 1 |
| [`AllyDamageReaction`](./Enums.md#enum-allydamagereaction) | Enum | {'type': 'Enum/String', 'df': "Applies the 'AllyDamageReaction' effect."} | 1 |
| [`AllyHealthRegenAura`](./Passives_and_Statuses.md#context-allyhealthregenaura) | Block | {'type': 'Block', 'df': "Applies the 'AllyHealthRegenAura' effect."} | 1 |
| [`AllyMoveAbilityAura`](./Enums.md#enum-allymoveabilityaura) | Enum | {'type': 'Enum/String', 'df': "Applies the 'AllyMoveAbilityAura' effect."} | 1 |
| `AllyMultiplyKnockbackDamage` | Number | {'type': 'Number', 'df': "Applies the 'AllyMultiplyKnockbackDamage' effect."} | 1 |
| `AllyMultiplyKnockbackDistance` | Number | {'type': 'Number', 'df': "Applies the 'AllyMultiplyKnockbackDistance' effect."} | 1 |
| `AllyUncappedHPAura` | Number | {'type': 'Number', 'df': "Applies the 'AllyUncappedHPAura' effect."} | 1 |
| `AlphaCat` | Number | {'type': 'Number', 'df': "Applies the 'AlphaCat' effect."} | 1 |
| [`AlternateCraftingPools`](./Passives_and_Statuses.md#context-alternatecraftingpools) | Block | {'type': 'Block', 'df': "Applies the 'AlternateCraftingPools' effect."} | 1 |
| `AmplifyNegativeStatus` | Number | {'type': 'Number', 'df': "Applies the 'AmplifyNegativeStatus' effect."} | 1 |
| `AmplifyPositiveStatus` | Number | {'type': 'Number', 'df': "Applies the 'AmplifyPositiveStatus' effect."} | 1 |
| [`ApplyStatusesToRandomEnemiesEachTurn`](./Passives_and_Statuses.md#context-applystatusestorandomenemieseachturn) | Block | {'type': 'Block', 'df': "Applies the 'ApplyStatusesToRandomEnemiesEachTurn' effect."} | 1 |
| `ArmorDodgeChance` | Number | {'type': 'Number', 'df': "Applies the 'ArmorDodgeChance' effect."} | 1 |
| `AutoCritLowDamage` | Number | {'type': 'Number', 'df': "Applies the 'AutoCritLowDamage' effect."} | 1 |
| `AutoEquipConsumables` | Number | {'type': 'Number', 'df': "Applies the 'AutoEquipConsumables' effect."} | 1 |
| [`AutocastEachTurnBegin`](./Enums.md#enum-autocasteachturnbegin) | Enum | {'type': 'Enum/String', 'df': "Applies the 'AutocastEachTurnBegin' effect."} | 1 |
| `BackstabCritChance` | Number | {'type': 'Number', 'df': "Applies the 'BackstabCritChance' effect."} | 1 |
| `BackstabImmunity` | Number | {'type': 'Number', 'df': "Applies the 'BackstabImmunity' effect."} | 1 |
| `BasicAttackStatusCarefulness` | Number | {'type': 'Number', 'df': "Applies the 'BasicAttackStatusCarefulness' effect."} | 1 |
| [`BasicAttackStatusSwap`](./Arrays.md#array-basicattackstatusswap) | Array | {'type': 'Array', 'df': "Applies the 'BasicAttackStatusSwap' effect."} | 1 |
| `BonusFoodEachBattle` | Number | {'type': 'Number', 'df': "Applies the 'BonusFoodEachBattle' effect."} | 1 |
| `BonusHealthRegenBasedOnDex` | Number | {'type': 'Number', 'df': "Applies the 'BonusHealthRegenBasedOnDex' effect."} | 1 |
| `BonusRangeBasedOnDex` | Number | {'type': 'Number', 'df': "Applies the 'BonusRangeBasedOnDex' effect."} | 1 |
| [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems) | Block | {'type': 'Block', 'df': "Applies the 'BoobyTrapItems' effect."} | 1 |
| `BoostAllyStatsOnDeath` | Number | {'type': 'Number', 'df': "Applies the 'BoostAllyStatsOnDeath' effect."} | 1 |
| `BoostDamageGlobalAura` | Number | {'type': 'Number', 'df': "Applies the 'BoostDamageGlobalAura' effect."} | 1 |
| `BoostHeals` | Number | {'type': 'Number', 'df': "Applies the 'BoostHeals' effect."} | 1 |
| `BoostRangeGlobalAura` | Number | {'type': 'Number', 'df': "Applies the 'BoostRangeGlobalAura' effect."} | 1 |
| [`BouncyProjectiles`](./Passives_and_Statuses.md#context-bouncyprojectiles) | Block | {'type': 'Block', 'df': "Applies the 'BouncyProjectiles' effect."} | 1 |
| `BraceForEachNeighboringEnemy` | Number | {'type': 'Number', 'df': "Applies the 'BraceForEachNeighboringEnemy' effect."} | 1 |
| `CCImmunity` | Number | {'type': 'Number', 'df': "Applies the 'CCImmunity' effect."} | 1 |
| `CapDamageFromAllies` | Number | {'type': 'Number', 'df': "Applies the 'CapDamageFromAllies' effect."} | 1 |
| `CapTechSpent` | Number | {'type': 'Number', 'df': "Applies the 'CapTechSpent' effect."} | 1 |
| [`CatAPultAnimation`](./Passives_and_Statuses.md#context-catapultanimation) | Block | {'type': 'Block', 'df': "Applies the 'CatAPultAnimation' effect."} | 1 |
| [`CatchProjectiles`](./Passives_and_Statuses.md#context-catchprojectiles) | Block | {'type': 'Block', 'df': "Applies the 'CatchProjectiles' effect."} | 1 |
| `ChainKnockback` | Number | {'type': 'Number', 'df': "Applies the 'ChainKnockback' effect."} | 1 |
| [`ChanceToBackflip`](./Passives_and_Statuses.md#context-chancetobackflip) | Block | {'type': 'Block', 'df': "Applies the 'ChanceToBackflip' effect."} | 1 |
| `ChanceToBlockAndCounter` | Number | {'type': 'Number', 'df': "Applies the 'ChanceToBlockAndCounter' effect."} | 1 |
| [`ChanceToRevive`](./Passives_and_Statuses.md#context-chancetorevive) | Block | {'type': 'Number', 'df': "Applies the 'ChanceToRevive' effect."} | 1 |
| `CharmAllFlies` | Number | {'type': 'Number', 'df': "Applies the 'CharmAllFlies' effect."} | 1 |
| [`ClassManaCostReduction`](./Passives_and_Statuses.md#context-classmanacostreduction) | Block | {'type': 'Block', 'df': "Applies the 'ClassManaCostReduction' effect."} | 1 |
| `CoinsAddDamage` | Number | {'type': 'Number', 'df': "Applies the 'CoinsAddDamage' effect."} | 1 |
| [`CollectPickupsOnBattleEnd`](./Passives_and_Statuses.md#context-collectpickupsonbattleend) | Block | {'type': 'Number', 'df': "Applies the 'CollectPickupsOnBattleEnd' effect."} | 1 |
| `Conductor` | Number | {'type': 'Number', 'df': "Applies the 'Conductor' effect."} | 1 |
| `ConductorManaRegen` | Number | {'type': 'Number', 'df': "Applies the 'ConductorManaRegen' effect."} | 1 |
| `ConjureCastSpellsForAllies` | Number | {'type': 'Number', 'df': "Applies the 'ConjureCastSpellsForAllies' effect."} | 1 |
| `ConsumableEffectsMultiplierBonus` | Number | {'type': 'Number', 'df': "Applies the 'ConsumableEffectsMultiplierBonus' effect."} | 1 |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum | {'type': 'Enum/String', 'df': "Applies the 'CounterAttack' effect."} | 1 |
| `DamageEnemiesOnHeal` | Number | {'type': 'Number', 'df': 'Combat Trigger: Deals damage to enemies on heal.'} | 1 |
| `DamageEnemiesOnKill` | Number | {'type': 'Number', 'df': 'Combat Trigger: Deals damage to enemies on kill.'} | 1 |
| [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell) | Block | {'type': 'Block', 'df': 'Combat Trigger: Deals damage to neighbor tiles when cast spell.'} | 1 |
| [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#context-damageneighborsaftermove) | Block | {'type': 'Block', 'df': 'Combat Trigger: Deals damage to neighbors after move.'} | 1 |
| [`DamageReductionAura`](./Passives_and_Statuses.md#context-damagereductionaura) | Block | {'type': 'Block', 'df': 'Combat Trigger: Deals damage to reduction aura.'} | 1 |
| `DeathChill` | Number | {'type': 'Number', 'df': "Applies the 'DeathChill' effect."} | 1 |
| [`DeathRattle`](./Passives_and_Statuses.md#context-deathrattle) | Block | {'type': 'Block', 'df': "Applies the 'DeathRattle' effect."} | 1 |
| `DebuffImmunity` | Number | {'type': 'Number', 'df': "Applies the 'DebuffImmunity' effect."} | 1 |
| `DejaVu` | Number | {'type': 'Number', 'df': "Applies the 'DejaVu' effect."} | 1 |
| `DirtyClaws` | Number | {'type': 'Number', 'df': "Applies the 'DirtyClaws' effect."} | 1 |
| `DoubleCastWeapons` | Number | {'type': 'Number', 'df': "Applies the 'DoubleCastWeapons' effect."} | 1 |
| `DukeOfFlies` | Number | {'type': 'Number', 'df': "Applies the 'DukeOfFlies' effect."} | 1 |
| [`EMP`](./Passives_and_Statuses.md#context-emp) | Block | {'type': 'Block', 'df': "Applies the 'EMP' effect."} | 1 |
| `EachSpellFreeAtFullMana` | Number | {'type': 'Number', 'df': "Applies the 'EachSpellFreeAtFullMana' effect."} | 1 |
| [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement) | Block | {'type': 'Block', 'df': "Applies the 'ElementalAttunement' effect."} | 1 |
| `Empath` | Number | {'type': 'Number', 'df': "Applies the 'Empath' effect."} | 1 |
| `EnemiesGetPickupsKnockedOut` | Number | {'type': 'Number', 'df': "Applies the 'EnemiesGetPickupsKnockedOut' effect."} | 1 |
| [`EnergyStorm`](./Passives_and_Statuses.md#context-energystorm) | Block | {'type': 'Number', 'df': "Applies the 'EnergyStorm' effect."} | 1 |
| [`EquipRandomTemporaryItemFromPool`](./Enums.md#enum-equiprandomtemporaryitemfrompool) | Enum | {'type': 'Enum/String', 'df': "Applies the 'EquipRandomTemporaryItemFromPool' effect."} | 1 |
| `EquipmentPassiveMultiplierBonus` | Number | {'type': 'Number', 'df': "Applies the 'EquipmentPassiveMultiplierBonus' effect."} | 1 |
| `EquipmentSetBonusBonus` | Number | {'type': 'Number', 'df': "Applies the 'EquipmentSetBonusBonus' effect."} | 1 |
| [`EscapeSequence`](./Passives_and_Statuses.md#context-escapesequence) | Block | {'type': 'Block', 'df': "Applies the 'EscapeSequence' effect."} | 1 |
| [`Eternal`](./Passives_and_Statuses.md#context-eternal) | Block | {'type': 'Block', 'df': "Applies the 'Eternal' effect."} | 1 |
| `ExplodeOverkilledEnemies` | Number | {'type': 'Number', 'df': "Applies the 'ExplodeOverkilledEnemies' effect."} | 1 |
| `ExplosionImmunity` | Number | {'type': 'Number', 'df': "Applies the 'ExplosionImmunity' effect."} | 1 |
| [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#context-extrastatuswhendealingdamage) | Block | {'type': 'Block', 'df': "Applies the 'ExtraStatusWhenDealingDamage' effect."} | 1 |
| `ExtraTrinketUses` | Number | {'type': 'Number', 'df': "Applies the 'ExtraTrinketUses' effect."} | 1 |
| `FaceShield` | Number | {'type': 'Number', 'df': "Applies the 'FaceShield' effect."} | 1 |
| `FamiliarSecondaryDamageImmunity` | Number | {'type': 'Number', 'df': "Applies the 'FamiliarSecondaryDamageImmunity' effect."} | 1 |
| `FlowerPowerAuraBrace` | Number | {'type': 'Number', 'df': "Applies the 'FlowerPowerAuraBrace' effect."} | 1 |
| `FlowerPowerAuraStrength` | Number | {'type': 'Number', 'df': "Applies the 'FlowerPowerAuraStrength' effect."} | 1 |
| `FlowersOnEndTurn` | Number | {'type': 'Number', 'df': "Applies the 'FlowersOnEndTurn' effect."} | 1 |
| `FlyDamageIncrease` | Number | {'type': 'Number', 'df': "Applies the 'FlyDamageIncrease' effect."} | 1 |
| `Flying` | Number | {'type': 'Number', 'df': "Applies the 'Flying' effect."} | 1 |
| [`FollowUp`](./Enums.md#enum-followup) | Enum | {'type': 'Enum/String', 'df': "Applies the 'FollowUp' effect."} | 1 |
| `FrontstabCritChance` | Number | {'type': 'Number', 'df': "Applies the 'FrontstabCritChance' effect."} | 1 |
| `FullHealthAllStatsUp` | Number | {'type': 'Number', 'df': "Applies the 'FullHealthAllStatsUp' effect."} | 1 |
| `FullHealthCritChance` | Number | {'type': 'Number', 'df': "Applies the 'FullHealthCritChance' effect."} | 1 |
| `FullHealthManaRegen` | Number | {'type': 'Number', 'df': "Applies the 'FullHealthManaRegen' effect."} | 1 |
| `FullPower` | Number | {'type': 'Number', 'df': "Applies the 'FullPower' effect."} | 1 |
| `GainExtraShield` | Number | {'type': 'Number', 'df': "Applies the 'GainExtraShield' effect."} | 1 |
| `GrassTileHealing` | Number | {'type': 'Number', 'df': "Applies the 'GrassTileHealing' effect."} | 1 |
| [`GravityWell`](./Passives_and_Statuses.md#context-gravitywell) | Block | {'type': 'Block', 'df': "Applies the 'GravityWell' effect."} | 1 |
| `HealAtStart` | Number | {'type': 'Number', 'df': "Applies the 'HealAtStart' effect."} | 1 |
| `HealDamagesEnemies` | Number | {'type': 'Number', 'df': "Applies the 'HealDamagesEnemies' effect."} | 1 |
| `HealingAura` | Number | {'type': 'Number', 'df': "Applies the 'HealingAura' effect."} | 1 |
| `HealsAlsoRegenMana` | Number | {'type': 'Number', 'df': "Applies the 'HealsAlsoRegenMana' effect."} | 1 |
| `HealsCanRevive` | Number | {'type': 'Number', 'df': "Applies the 'HealsCanRevive' effect."} | 1 |
| `HolyDamageMultiplierBonus` | Number | {'type': 'Number', 'df': "Applies the 'HolyDamageMultiplierBonus' effect."} | 1 |
| [`HolyShieldTransferToTaggedMinions`](./Enums.md#enum-holyshieldtransfertotaggedminions) | Enum | {'type': 'Enum/String', 'df': "Applies the 'HolyShieldTransferToTaggedMinions' effect."} | 1 |
| `ImmortalLeeches` | Number | {'type': 'Number', 'df': "Applies the 'ImmortalLeeches' effect."} | 1 |
| `IncreaseExplosionSize` | Number | {'type': 'Number', 'df': "Applies the 'IncreaseExplosionSize' effect."} | 1 |
| `IncreaseHealingSpellRange` | Number | {'type': 'Number', 'df': "Applies the 'IncreaseHealingSpellRange' effect."} | 1 |
| `IncreaseItemUsesOnEquip` | Number | {'type': 'Number', 'df': "Applies the 'IncreaseItemUsesOnEquip' effect."} | 1 |
| `IncreaseSpellRange` | Number | {'type': 'Number', 'df': "Applies the 'IncreaseSpellRange' effect."} | 1 |
| [`InfiniteRebirth`](./Passives_and_Statuses.md#context-infiniterebirth) | Block | {'type': 'Block', 'df': "Applies the 'InfiniteRebirth' effect."} | 1 |
| `InjuryImmunity` | Number | {'type': 'Number', 'df': "Applies the 'InjuryImmunity' effect."} | 1 |
| `KillsHeal` | Number | {'type': 'Number', 'df': "Applies the 'KillsHeal' effect."} | 1 |
| [`KillsToMeat`](./Enums.md#enum-killstomeat) | Enum | {'type': 'Enum/String', 'df': "Applies the 'KillsToMeat' effect."} | 1 |
| [`LateBloomer`](./Passives_and_Statuses.md#context-latebloomer) | Block | {'type': 'Block', 'df': "Applies the 'LateBloomer' effect."} | 1 |
| `LightningAspectCharge` | Number | {'type': 'Number', 'df': "Applies the 'LightningAspectCharge' effect."} | 1 |
| [`LightningRod`](./Passives_and_Statuses.md#context-lightningrod) | Block | {'type': 'Block', 'df': "Applies the 'LightningRod' effect."} | 1 |
| [`LineOfSightTrueSightAura`](./Enums.md#enum-lineofsighttruesightaura) | Enum | {'type': 'Number', 'df': "Applies the 'LineOfSightTrueSightAura' effect."} | 1 |
| `LobbedHook` | Number | {'type': 'Number', 'df': "Applies the 'LobbedHook' effect."} | 1 |
| [`LowHealthAllyDodgeChanceAura`](./Passives_and_Statuses.md#context-lowhealthallydodgechanceaura) | Block | {'type': 'Block', 'df': "Applies the 'LowHealthAllyDodgeChanceAura' effect."} | 1 |
| `MakeBasicAttackPassThroughThings` | Number | {'type': 'Number', 'df': "Applies the 'MakeBasicAttackPassThroughThings' effect."} | 1 |
| `MakeSpellsRequireCharge` | Number | {'type': 'Number', 'df': "Applies the 'MakeSpellsRequireCharge' effect."} | 1 |
| `ManaCostReduction` | Number | {'type': 'Number', 'df': "Applies the 'ManaCostReduction' effect."} | 1 |
| `ManaRegenMultiplierIfManaEmpty` | Number | {'type': 'Number', 'df': "Applies the 'ManaRegenMultiplierIfManaEmpty' effect."} | 1 |
| [`MegaMinions`](./Passives_and_Statuses.md#context-megaminions) | Block | {'type': 'Number', 'df': "Applies the 'MegaMinions' effect."} | 1 |
| `Metal` | Number | {'type': 'Number', 'df': "Applies the 'Metal' effect."} | 1 |
| `MetalDetector` | Number | {'type': 'Number', 'df': "Applies the 'MetalDetector' effect."} | 1 |
| `MinimumTech` | Number | {'type': 'Number', 'df': "Applies the 'MinimumTech' effect."} | 1 |
| `MoveRandomly` | Number | {'type': 'Number', 'df': "Applies the 'MoveRandomly' effect."} | 1 |
| [`MoveTowardsDamageSource`](./Passives_and_Statuses.md#context-movetowardsdamagesource) | Block | {'type': 'Block', 'df': "Applies the 'MoveTowardsDamageSource' effect."} | 1 |
| [`MovementReaction`](./Passives_and_Statuses.md#context-movementreaction) | Block | {'type': 'Block', 'df': "Applies the 'MovementReaction' effect."} | 1 |
| `NoReflection` | Number | {'type': 'Number', 'df': "Applies the 'NoReflection' effect."} | 1 |
| `NumbingLeeches` | Number | {'type': 'Number', 'df': "Applies the 'NumbingLeeches' effect."} | 1 |
| `OverhealGainsBothShield` | Number | {'type': 'Number', 'df': "Applies the 'OverhealGainsBothShield' effect."} | 1 |
| `ParasitesArentCursed` | Number | {'type': 'Number', 'df': "Applies the 'ParasitesArentCursed' effect."} | 1 |
| [`PassiveAfterXKills`](./Passives_and_Statuses.md#context-passiveafterxkills) | Block | {'type': 'Block', 'df': "Applies the 'PassiveAfterXKills' effect."} | 1 |
| [`PassiveAtFullHealth`](./Passives_and_Statuses.md#context-passiveatfullhealth) | Block | {'type': 'Block', 'df': "Applies the 'PassiveAtFullHealth' effect."} | 1 |
| [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#context-passiveatinjurythreshold) | Block | {'type': 'Block', 'df': "Applies the 'PassiveAtInjuryThreshold' effect."} | 1 |
| [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell) | Block | {'type': 'Block', 'df': "Applies the 'PassiveUntilCastSpell' effect."} | 1 |
| [`PassiveUntilGetKill`](./Passives_and_Statuses.md#context-passiveuntilgetkill) | Block | {'type': 'Block', 'df': "Applies the 'PassiveUntilGetKill' effect."} | 1 |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement) | Block | {'type': 'Block', 'df': 'State Trigger: Grants nested passives when affected by element.'} | 1 |
| [`PassiveWhenTheAlpha`](./Passives_and_Statuses.md#context-passivewhenthealpha) | Block | {'type': 'Block', 'df': 'State Trigger: Grants nested passives when the alpha.'} | 1 |
| [`PassiveWhileInMonkMeleeStance`](./Passives_and_Statuses.md#context-passivewhileinmonkmeleestance) | Block | {'type': 'Block', 'df': "Applies the 'PassiveWhileInMonkMeleeStance' effect."} | 1 |
| [`PassiveWhileInMonkRangedStance`](./Passives_and_Statuses.md#context-passivewhileinmonkrangedstance) | Block | {'type': 'Block', 'df': "Applies the 'PassiveWhileInMonkRangedStance' effect."} | 1 |
| [`PassiveWhilePreviewingMonkRangedStance`](./Passives_and_Statuses.md#context-passivewhilepreviewingmonkrangedstance) | Block | {'type': 'Block', 'df': "Applies the 'PassiveWhilePreviewingMonkRangedStance' effect."} | 1 |
| [`PassiveWhileWearingMetal`](./Passives_and_Statuses.md#context-passivewhilewearingmetal) | Block | {'type': 'Block', 'df': "Applies the 'PassiveWhileWearingMetal' effect."} | 1 |
| `PermanentItems` | Number | {'type': 'Number', 'df': "Applies the 'PermanentItems' effect."} | 1 |
| `Phasing` | Number | {'type': 'Number', 'df': "Applies the 'Phasing' effect."} | 1 |
| `PoisonMultiplier` | Number | {'type': 'Number', 'df': "Applies the 'PoisonMultiplier' effect."} | 1 |
| `PoisonThorns` | Number | {'type': 'Number', 'df': "Applies the 'PoisonThorns' effect."} | 1 |
| [`ProtectTargetedAllies`](./Enums.md#enum-protecttargetedallies) | Enum | {'type': 'Enum/String', 'df': "Applies the 'ProtectTargetedAllies' effect."} | 1 |
| `Quiver` | Number | {'type': 'Number', 'df': "Applies the 'Quiver' effect."} | 1 |
| `RangedTrueShot` | Number | {'type': 'Number', 'df': "Applies the 'RangedTrueShot' effect."} | 1 |
| `RefreshMoveOnWeaponConnect` | Number | {'type': 'Number', 'df': "Applies the 'RefreshMoveOnWeaponConnect' effect."} | 1 |
| `RemoveLineOfSightRestrictions` | Number | {'type': 'Number', 'df': "Applies the 'RemoveLineOfSightRestrictions' effect."} | 1 |
| `RemoveOncePerFightRestriction` | Number | {'type': 'Number', 'df': "Applies the 'RemoveOncePerFightRestriction' effect."} | 1 |
| [`ReplaceBasicAttackWhenDead`](./Enums.md#enum-replacebasicattackwhendead) | Enum | {'type': 'Enum/String', 'df': "Applies the 'ReplaceBasicAttackWhenDead' effect."} | 1 |
| [`ReplaceBrain`](./Passives_and_Statuses.md#context-replacebrain) | Block | {'type': 'Block', 'df': "Applies the 'ReplaceBrain' effect."} | 1 |
| [`ReplaceSpellsWhenDead`](./Enums.md#enum-replacespellswhendead) | Enum | {'type': 'Enum/String', 'df': "Applies the 'ReplaceSpellsWhenDead' effect."} | 1 |
| `ReviveOnWin` | Number | {'type': 'Number', 'df': "Applies the 'ReviveOnWin' effect."} | 1 |
| [`Robot`](./Passives_and_Statuses.md#context-robot) | Block | {'type': 'Block', 'df': "Applies the 'Robot' effect."} | 1 |
| `RobotsInheritArmor` | Number | {'type': 'Number', 'df': "Applies the 'RobotsInheritArmor' effect."} | 1 |
| `RockDetector` | Number | {'type': 'Number', 'df': "Applies the 'RockDetector' effect."} | 1 |
| `SafeExplosions` | Number | {'type': 'Number', 'df': "Applies the 'SafeExplosions' effect."} | 1 |
| [`ScaledStatusOnLoseShield`](./Passives_and_Statuses.md#context-scaledstatusonloseshield) | Block | {'type': 'Block', 'df': "Applies the 'ScaledStatusOnLoseShield' effect."} | 1 |
| [`ScaledStatusOnOverHealed`](./Passives_and_Statuses.md#context-scaledstatusonoverhealed) | Block | {'type': 'Block', 'df': "Applies the 'ScaledStatusOnOverHealed' effect."} | 1 |
| [`ScaledStatusOnOverMana`](./Passives_and_Statuses.md#context-scaledstatusonovermana) | Block | {'type': 'Block', 'df': "Applies the 'ScaledStatusOnOverMana' effect."} | 1 |
| [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#context-scaledstatusonspendmana) | Block | {'type': 'Block', 'df': "Applies the 'ScaledStatusOnSpendMana' effect."} | 1 |
| [`SecurityBotProtect`](./Passives_and_Statuses.md#context-securitybotprotect) | Block | {'type': 'Block', 'df': "Applies the 'SecurityBotProtect' effect."} | 1 |
| `SetSpellCosts` | Number | {'type': 'Number', 'df': "Applies the 'SetSpellCosts' effect."} | 1 |
| `ShareHealthRegen` | Number | {'type': 'Number', 'df': "Applies the 'ShareHealthRegen' effect."} | 1 |
| `SharePickups` | Number | {'type': 'Number', 'df': "Applies the 'SharePickups' effect."} | 1 |
| `ShoulderCheck` | Number | {'type': 'Number', 'df': "Applies the 'ShoulderCheck' effect."} | 1 |
| [`ShovingMatch`](./Enums.md#enum-shovingmatch) | Enum | {'type': 'Enum/String', 'df': "Applies the 'ShovingMatch' effect."} | 1 |
| `ShowHiddenThings` | Number | {'type': 'Number', 'df': "Applies the 'ShowHiddenThings' effect."} | 1 |
| `SmallEnemiesIgnoreYou` | Number | {'type': 'Number', 'df': "Applies the 'SmallEnemiesIgnoreYou' effect."} | 1 |
| [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#context-smiteenemieswhokill) | Block | {'type': 'Block', 'df': "Applies the 'SmiteEnemiesWhoKill' effect."} | 1 |
| [`SpawnMeatOnMove`](./Enums.md#enum-spawnmeatonmove) | Enum | {'type': 'Enum/String', 'df': "Applies the 'SpawnMeatOnMove' effect."} | 1 |
| [`SpawnObjectOnPopCorpse`](./Enums.md#enum-spawnobjectonpopcorpse) | Enum | {'type': 'Enum/String', 'df': "Applies the 'SpawnObjectOnPopCorpse' effect."} | 1 |
| [`SpecialFriends`](./Passives_and_Statuses.md#context-specialfriends) | Block | {'type': 'Block', 'df': "Applies the 'SpecialFriends' effect."} | 1 |
| `SplittableMove` | Number | {'type': 'Number', 'df': "Applies the 'SplittableMove' effect."} | 1 |
| `SpreadExtraDebuffs` | Number | {'type': 'Number', 'df': "Applies the 'SpreadExtraDebuffs' effect."} | 1 |
| `SpreadPainBonus` | Number | {'type': 'Number', 'df': "Applies the 'SpreadPainBonus' effect."} | 1 |
| `SpreadPainBonusCrit` | Number | {'type': 'Number', 'df': "Applies the 'SpreadPainBonusCrit' effect."} | 1 |
| [`StackingDodgeChanceOnTookDamage`](./Passives_and_Statuses.md#context-stackingdodgechanceontookdamage) | Block | {'type': 'Block', 'df': "Applies the 'StackingDodgeChanceOnTookDamage' effect."} | 1 |
| `StatMinimum` | Number | {'type': 'Number', 'df': "Applies the 'StatMinimum' effect."} | 1 |
| [`StatusAfterCastSpell`](./Passives_and_Statuses.md#context-statusaftercastspell) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to after cast spell.'} | 1 |
| [`StatusAlliesOnBattleStart`](./Passives_and_Statuses.md#context-statusalliesonbattlestart) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to allies on battle start.'} | 1 |
| [`StatusAlliesOnGainCoins`](./Passives_and_Statuses.md#context-statusalliesongaincoins) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to allies on gain coins.'} | 1 |
| [`StatusAlliesOnKill`](./Passives_and_Statuses.md#context-statusalliesonkill) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to allies on kill.'} | 1 |
| [`StatusAlliesOnSpendMana`](./Passives_and_Statuses.md#context-statusalliesonspendmana) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to allies on spend mana.'} | 1 |
| [`StatusAlliesScaledByCursedOnDeath`](./Passives_and_Statuses.md#context-statusalliesscaledbycursedondeath) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to allies scaled by cursed on death.'} | 1 |
| [`StatusAllyWhenAllySpendsMana`](./Passives_and_Statuses.md#context-statusallywhenallyspendsmana) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to ally when ally spends mana.'} | 1 |
| [`StatusAnyCatAllyWhoKills`](./Passives_and_Statuses.md#context-statusanycatallywhokills) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to any cat ally who kills.'} | 1 |
| `StatusCarefulness` | Number | {'type': 'Number', 'df': 'Event Trigger: Applies nested statuses to carefulness.'} | 1 |
| [`StatusDamagers`](./Passives_and_Statuses.md#context-statusdamagers) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to damagers.'} | 1 |
| [`StatusEachTurnEndForEachTurn`](./Passives_and_Statuses.md#context-statuseachturnendforeachturn) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to each turn end for each turn.'} | 1 |
| [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#context-statuseachturnendperenemykill) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to each turn end per enemy kill.'} | 1 |
| [`StatusEnemiesOnDeath`](./Passives_and_Statuses.md#context-statusenemiesondeath) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to enemies on death.'} | 1 |
| [`StatusEveryXTurnBegins`](./Passives_and_Statuses.md#context-statuseveryxturnbegins) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to every x turn begins.'} | 1 |
| [`StatusKilledCharacters`](./Passives_and_Statuses.md#context-statuskilledcharacters) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to killed characters.'} | 1 |
| [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers) | Block | {'type': 'Block', 'df': 'Instantly kills the target if they possess the specified status effects.'} | 1 |
| [`StatusOnAllyCatDeath`](./Passives_and_Statuses.md#context-statusonallycatdeath) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when ally cat death.'} | 1 |
| [`StatusOnAnyDeath`](./Passives_and_Statuses.md#context-statusonanydeath) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when any death.'} | 1 |
| [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend) | Block | {'type': 'Block', 'df': 'Applies the nested status effects when the encounter finishes.'} | 1 |
| [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#context-statusonbattleendifkillthresholdmet) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when battle end if kill threshold met.'} | 1 |
| [`StatusOnBattleStart`](./Passives_and_Statuses.md#context-statusonbattlestart) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when battle start.'} | 1 |
| [`StatusOnBreakItem`](./Passives_and_Statuses.md#context-statusonbreakitem) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when break item.'} | 1 |
| [`StatusOnCollectPickup`](./Passives_and_Statuses.md#context-statusoncollectpickup) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when collect pickup.'} | 1 |
| [`StatusOnDealtDamage`](./Passives_and_Statuses.md#context-statusondealtdamage) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when dealt damage.'} | 1 |
| [`StatusOnDealtDamageThreshold`](./Passives_and_Statuses.md#context-statusondealtdamagethreshold) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when dealt damage threshold.'} | 1 |
| [`StatusOnEatFood`](./Passives_and_Statuses.md#context-statusoneatfood) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when eat food.'} | 1 |
| [`StatusOnEndMove`](./Passives_and_Statuses.md#context-statusonendmove) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when end move.'} | 1 |
| [`StatusOnGainShield`](./Passives_and_Statuses.md#context-statusongainshield) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when gain shield.'} | 1 |
| [`StatusOnHeal`](./Passives_and_Statuses.md#context-statusonheal) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when heal.'} | 1 |
| [`StatusOnKillEnemy`](./Passives_and_Statuses.md#context-statusonkillenemy) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when kill enemy.'} | 1 |
| [`StatusOnOverMana`](./Passives_and_Statuses.md#context-statusonovermana) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when over mana.'} | 1 |
| [`StatusOnPickupCoins`](./Passives_and_Statuses.md#context-statusonpickupcoins) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when pickup coins.'} | 1 |
| [`StatusOnPopCorpse`](./Passives_and_Statuses.md#context-statusonpopcorpse) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when pop corpse.'} | 1 |
| [`StatusOnTookDamageFromAbility`](./Passives_and_Statuses.md#context-statusontookdamagefromability) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when took damage from ability.'} | 1 |
| [`StatusOnTookDamageFromEnemyAbility`](./Passives_and_Statuses.md#context-statusontookdamagefromenemyability) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when took damage from enemy ability.'} | 1 |
| [`StatusOnTriggerTrap`](./Passives_and_Statuses.md#context-statusontriggertrap) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when trigger trap.'} | 1 |
| [`StatusOnUseBasicAttack`](./Passives_and_Statuses.md#context-statusonusebasicattack) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when use basic attack.'} | 1 |
| [`StatusOnUseElementAbility`](./Passives_and_Statuses.md#context-statusonuseelementability) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses when use element ability.'} | 1 |
| [`StatusPerInjury`](./Passives_and_Statuses.md#context-statusperinjury) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to per injury.'} | 1 |
| [`StatusReplacement`](./Arrays.md#array-statusreplacement) | Array | {'type': 'Array', 'df': 'Event Trigger: Applies nested statuses to replacement.'} | 1 |
| [`StatusThingsKnockedBack`](./Passives_and_Statuses.md#context-statusthingsknockedback) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to things knocked back.'} | 1 |
| [`StatusWhenAllySpendsMana`](./Passives_and_Statuses.md#context-statuswhenallyspendsmana) | Block | {'type': 'Block', 'df': 'Event Trigger: Applies nested statuses to when ally spends mana.'} | 1 |
| `Stealth` | Number | {'type': 'Number', 'df': "Applies the 'Stealth' effect."} | 1 |
| `StrengthForEachNeighboringEnemy` | Number | {'type': 'Number', 'df': "Applies the 'StrengthForEachNeighboringEnemy' effect."} | 1 |
| [`StrengthInNumbersAura`](./Passives_and_Statuses.md#context-strengthinnumbersaura) | Block | {'type': 'Number', 'df': "Applies the 'StrengthInNumbersAura' effect."} | 1 |
| [`Study`](./Passives_and_Statuses.md#context-study) | Block | {'type': 'Number', 'df': "Applies the 'Study' effect."} | 1 |
| `Tech` | Number | {'type': 'Number', 'df': "Applies the 'Tech' effect."} | 1 |
| [`TileDamageMultiplier`](./Passives_and_Statuses.md#context-tiledamagemultiplier) | Block | {'type': 'Number', 'df': "Applies the 'TileDamageMultiplier' effect."} | 1 |
| [`TowerDefense`](./Passives_and_Statuses.md#context-towerdefense) | Block | {'type': 'Block', 'df': "Applies the 'TowerDefense' effect."} | 1 |
| [`TowerDefenseReflex`](./Enums.md#enum-towerdefensereflex) | Enum | {'type': 'Enum/String', 'df': "Applies the 'TowerDefenseReflex' effect."} | 1 |
| `TrapEffectsMultiplier` | Number | {'type': 'Number', 'df': "Applies the 'TrapEffectsMultiplier' effect."} | 1 |
| `TrinketActiveEffectsMultiplierBonus` | Number | {'type': 'Number', 'df': "Applies the 'TrinketActiveEffectsMultiplierBonus' effect."} | 1 |
| `TrinketPassiveMultiplierBonus` | Number | {'type': 'Number', 'df': "Applies the 'TrinketPassiveMultiplierBonus' effect."} | 1 |
| `UncappedHP` | Number | {'type': 'Number', 'df': "Applies the 'UncappedHP' effect."} | 1 |
| `UncappedHPBonusStr` | Number | {'type': 'Number', 'df': "Applies the 'UncappedHPBonusStr' effect."} | 1 |
| [`UpgradeLevelUpClassActives`](./Enums.md#enum-upgradelevelupclassactives) | Enum | {'type': 'Enum/String', 'df': "Applies the 'UpgradeLevelUpClassActives' effect."} | 1 |
| [`UpgradeLevelUpClassPassives`](./Enums.md#enum-upgradelevelupclasspassives) | Enum | {'type': 'Enum/String', 'df': "Applies the 'UpgradeLevelUpClassPassives' effect."} | 1 |
| `UpgradeSpawnedPickups` | Number | {'type': 'Number', 'df': "Applies the 'UpgradeSpawnedPickups' effect."} | 1 |
| `Vengeful` | Number | {'type': 'Number', 'df': "Applies the 'Vengeful' effect."} | 1 |
| `WaterWalk` | Number | {'type': 'Number', 'df': "Applies the 'WaterWalk' effect."} | 1 |
| `Weakness` | Number | {'type': 'Number', 'df': "Applies the 'Weakness' effect."} | 1 |
| `WeaponCountsAsBasicAttack` | Number | {'type': 'Number', 'df': "Applies the 'WeaponCountsAsBasicAttack' effect."} | 1 |
| `WeaponDamageMultiplierBonus` | Number | {'type': 'Number', 'df': "Applies the 'WeaponDamageMultiplierBonus' effect."} | 1 |
| `WeaponsDontLoseDurability` | Number | {'type': 'Number', 'df': "Applies the 'WeaponsDontLoseDurability' effect."} | 1 |
| [`grant_ability`](./Enums.md#enum-grant_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 884

> **Referenced by:** [`PassiveAfterXKills`](./Passives_and_Statuses.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#context-passiveathealththreshold), [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#context-passiveatinjurythreshold), [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold), [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement), [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack) | Block | {'type': 'Block', 'df': 'Injects a status effect payload that applies whenever the character performs a basic attack.'} | 42 |
| [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to each turn end. | 15 |
| [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend) | Block | {'type': '`Block`', 'df': "Applies the nested status effects when the encounter finishes. | 15 |
| [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions) | Block | {'type': '`Block`', 'df': "Applies the 'AddPassivesToMinions' effect. | 14 |
| [`MulticlassLevelUp`](./Enums.md#enum-multiclasslevelup) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'MulticlassLevelUp' effect."} | 12 |
| [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when took damage. | 10 |
| [`SpawnOnBattleStart`](./Passives_and_Statuses.md#context-spawnonbattlestart) | Block | {'type': '`Enum/String`', 'df': "Applies the 'SpawnOnBattleStart' effect."} | 9 |
| [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to each turn begin. | 9 |
| `DodgeChance` | Number | {'type': 'Number', 'df': "Applies the 'DodgeChance' effect."} | 8 |
| [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#context-damageneighborsonendmove) | Block | {'type': '`Block`', 'df': 'Combat Trigger: Deals damage to neighbors on end move. | 7 |
| `ExtraBasicAttacks` | Number | {'type': '`Number`', 'df': "Applies the 'ExtraBasicAttacks' effect."} | 7 |
| `Brace` | Number | {'type': 'Number', 'df': "Applies the 'Brace' effect."} | 6 |
| `CritChanceUp` | Number | {'type': 'Number', 'df': "Applies the 'CritChanceUp' effect."} | 6 |
| [`ReplaceSpawnedObjects`](./Arrays.md#array-replacespawnedobjects) | Array | {'type': '`Array`', 'df': "Applies the 'ReplaceSpawnedObjects' effect."} | 6 |
| `SizeScale` | Mixed | {'type': '`Enum/String`', 'df': "Applies the 'SizeScale' effect."} | 6 |
| [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill) | Block | {'type': '`Block`', 'df': 'Event Trigger: Applies nested statuses when kill.'} | 6 |
| `AllStatsUp` | Number | {'type': 'Number', 'df': "Applies the 'AllStatsUp' effect."} | 5 |
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'BonusAbility' effect."} | 5 |
| `HealthRegenUp` | Number | {'type': 'Number', 'df': "Applies the 'HealthRegenUp' effect."} | 5 |
| [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage) | Block | {'type': '`Block`', 'df': "Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. | 5 |
| [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveAtStatThreshold' effect. | 5 |
| `SetSpellCosts` | Number | {'type': '`Number`', 'df': "Applies the 'SetSpellCosts' effect."} | 5 |
| [`StatusImmunity`](./Arrays.md#array-statusimmunity) | Array | {'type': '`Array`', 'df': 'Event Trigger: Applies nested statuses to immunity.'} | 5 |
| `Thorns` | Number | {'type': '`Number`', 'df': "Applies the 'Thorns' effect."} | 5 |
| `Trample` | Number | {'type': '`Number`', 'df': "Applies the 'Trample' effect."} | 5 |
| [`AbilityOnBattleStart`](./Enums.md#enum-abilityonbattlestart) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'AbilityOnBattleStart' effect."} | 4 |
| `AddBonusRange` | Number | {'type': 'Number', 'df': "Applies the 'AddBonusRange' effect."} | 4 |
| `AddCorpseHealth` | Number | {'type': '`Number`', 'df': "Applies the 'AddCorpseHealth' effect."} | 4 |
| `AddManaRegen` | Number | {'type': '`Number`', 'df': "Applies the 'AddManaRegen' effect."} | 4 |
| [`AmplifyStatus`](./Enums.md#enum-amplifystatus) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'AmplifyStatus' effect."} | 4 |
| `BlastResistance` | Number | {'type': '`Number`', 'df': "Applies the 'BlastResistance' effect."} | 4 |
| [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus) | Block | {'type': 'Block', 'df': "Applies the 'CritsApplyStatus' effect."} | 4 |
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum | {'type': 'Enum/String', 'df': "Applies the 'EquipTemporaryItem' effect."} | 4 |
| [`ForceSpecificInjury`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies the 'ForceSpecificInjury' effect."} | 4 |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'InnateElement' effect."} | 4 |
| `MissChance` | Number | {'type': '`Number`', 'df': "Applies the 'MissChance' effect."} | 4 |
| [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveIfAllArmorEmpty' effect. | 4 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'ReplaceBasicAttack' effect."} | 4 |
| [`SpawnEachTurn`](./Passives_and_Statuses.md#context-spawneachturn) | Block | {'type': '`Block`', 'df': "Applies the 'SpawnEachTurn' effect. | 4 |
| [`SpawnThingOnDamage`](./Passives_and_Statuses.md#context-spawnthingondamage) | Block | {'type': '`Block`', 'df': "Applies the 'SpawnThingOnDamage' effect. | 4 |
| [`AbilityReaction`](./Passives_and_Statuses.md#context-abilityreaction) | Block | {'type': '`Enum/String`', 'df': "Applies the 'AbilityReaction' effect."} | 3 |
| `AddCritMultiplier` | Number | {'type': 'Number', 'df': "Applies the 'AddCritMultiplier' effect."} | 3 |
| [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'AddElementsToBasicAttack' effect."} | 3 |
| `AddLevelUpRerolls` | Number | {'type': '`Number`', 'df': "Applies the 'AddLevelUpRerolls' effect."} | 3 |
| [`AddStatusToAllDamage`](./Passives_and_Statuses.md#context-addstatustoalldamage) | Block | {'type': '`Block`', 'df': "Applies the 'AddStatusToAllDamage' effect. | 3 |
| [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack) | Block | {'type': '`Block`', 'df': "Applies the 'AddStatusToBasicMeleeAttack' effect. | 3 |
| [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities) | Block | {'type': '`Block`', 'df': "Applies the 'AddStatusToElementAbilities' effect. | 3 |
| [`AllyBonusAbilityAura`](./Passives_and_Statuses.md#context-allybonusabilityaura) | Block | {'type': '`Enum/String`', 'df': "Applies the 'AllyBonusAbilityAura' effect."} | 3 |
| `AlphaTurns` | Number | {'type': '`Number`', 'df': "Applies the 'AlphaTurns' effect."} | 3 |
| `BackstabCritChance` | Number | {'type': '`Number`', 'df': "Applies the 'BackstabCritChance' effect."} | 3 |
| `BasicAttackDamageMultiplier` | Number | {'type': '`Number`', 'df': "Applies the 'BasicAttackDamageMultiplier' effect."} | 3 |
| `BoostHeals` | Number | {'type': '`Number`', 'df': "Applies the 'BoostHeals' effect."} | 3 |
| `Bruise` | Number | {'type': 'Number', 'df': "Applies the 'Bruise' effect."} | 3 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'ElementImmune' effect."} | 3 |
| `MakeSpellsRequireCharge` | Number | {'type': '`Number`', 'df': "Applies the 'MakeSpellsRequireCharge' effect."} | 3 |
| [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#context-passiveifemptyface) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveIfEmptyFace' effect. | 3 |
| [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#context-passiveifemptyhead) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveIfEmptyHead' effect. | 3 |
| [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#context-passiveifemptyneck) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveIfEmptyNeck' effect. | 3 |
| [`ReplaceBasicAttackWhenCastable`](./Enums.md#enum-replacebasicattackwhencastable) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'ReplaceBasicAttackWhenCastable' effect."} | 3 |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'ReplaceBasicMove' effect."} | 3 |
| [`RevengeDamage`](./Passives_and_Statuses.md#context-revengedamage) | Block | {'type': '`Block`', 'df': 'Reaction trigger: Deals damage to the attacker when hit. | 3 |
| [`StatusAlliesOnDeath`](./Passives_and_Statuses.md#context-statusalliesondeath) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to allies on death. | 3 |
| [`StatusOnCrit`](./Passives_and_Statuses.md#context-statusoncrit) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when crit. | 3 |
| [`StatusOnOverHealed`](./Passives_and_Statuses.md#context-statusonoverhealed) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when over healed. | 3 |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch) | Block | {'type': '`Block`', 'df': 'Event Trigger: Applies nested statuses when stance switch.'} | 3 |
| [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#context-statusonuseabilitywithtag) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when use ability with tag. | 3 |
| `AddBonusMeleeRange` | Number | {'type': '`Number`', 'df': "Applies the 'AddBonusMeleeRange' effect."} | 2 |
| `AddDamageToBasicAttack` | Number | {'type': '`Number`', 'df': "Applies the 'AddDamageToBasicAttack' effect."} | 2 |
| [`AddDamageToElementDamage`](./Passives_and_Statuses.md#context-adddamagetoelementdamage) | Block | {'type': '`Block`', 'df': "Applies the 'AddDamageToElementDamage' effect. | 2 |
| `AddInitiative` | Number | {'type': '`Number`', 'df': "Applies the 'AddInitiative' effect."} | 2 |
| `AddMovement` | Number | {'type': 'Number', 'df': "Applies the 'AddMovement' effect."} | 2 |
| [`AddPassivesToCharmed`](./Passives_and_Statuses.md#context-addpassivestocharmed) | Block | {'type': '`Block`', 'df': "Applies the 'AddPassivesToCharmed' effect. | 2 |
| [`AddStatusToElementDamage`](./Passives_and_Statuses.md#context-addstatustoelementdamage) | Block | {'type': '`Block`', 'df': "Applies the 'AddStatusToElementDamage' effect. | 2 |
| [`AddStatusToWeapons`](./Passives_and_Statuses.md#context-addstatustoweapons) | Block | {'type': '`Block`', 'df': "Applies the 'AddStatusToWeapons' effect. | 2 |
| [`AddTag`](./Enums.md#enum-addtag) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'AddTag' effect."} | 2 |
| [`AllyManaRegenAura`](./Passives_and_Statuses.md#context-allymanaregenaura) | Block | {'type': '`Block`', 'df': "Applies the 'AllyManaRegenAura' effect. | 2 |
| [`AutocastEachRound`](./Passives_and_Statuses.md#context-autocasteachround) | Block | {'type': '`Block`', 'df': 'Forces the character to automatically cast a specific ability at the start of each combat round. | 2 |
| [`AutocastEachTurn`](./Enums.md#enum-autocasteachturn) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'AutocastEachTurn' effect."} | 2 |
| [`AutocastEachTurnBegin`](./Passives_and_Statuses.md#context-autocasteachturnbegin) | Block | {'type': '`Enum/String`', 'df': "Applies the 'AutocastEachTurnBegin' effect."} | 2 |
| `BasicAttackAOEBonus` | Number | {'type': '`Number`', 'df': "Applies the 'BasicAttackAOEBonus' effect."} | 2 |
| `BasicAttackCritChance` | Number | {'type': '`Number`', 'df': "Applies the 'BasicAttackCritChance' effect."} | 2 |
| `Bleed` | Number | {'type': 'Number', 'df': "Applies the 'Bleed' effect."} | 2 |
| [`BoostWeaponDamage`](./Passives_and_Statuses.md#context-boostweapondamage) | Block | {'type': '`Number`', 'df': "Applies the 'BoostWeaponDamage' effect."} | 2 |
| `ChangeTauntPriority` | Number | {'type': '`Number`', 'df': "Applies the 'ChangeTauntPriority' effect."} | 2 |
| [`DeathRattle`](./Passives_and_Statuses.md#context-deathrattle) | Block | {'type': '`Block`', 'df': "Applies the 'DeathRattle' effect. | 2 |
| [`Dyslexia`](./Arrays.md#array-dyslexia) | Array | {'type': '`Array`', 'df': "Applies the 'Dyslexia' effect."} | 2 |
| `ExtraWeaponAttacks` | Number | {'type': '`Number`', 'df': "Applies the 'ExtraWeaponAttacks' effect."} | 2 |
| `FreezePiercing` | Number | {'type': '`Number`', 'df': "Applies the 'FreezePiercing' effect."} | 2 |
| `HeadArmorPassiveMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies the 'HeadArmorPassiveMultiplierBonus' effect."} | 2 |
| `IncreaseExplosionDamage` | Number | {'type': '`Number`', 'df': "Applies the 'IncreaseExplosionDamage' effect."} | 2 |
| `KnockbackImmunity` | Number | {'type': '`Number`', 'df': "Applies the 'KnockbackImmunity' effect."} | 2 |
| [`LevelUpClassOverride`](./Enums.md#enum-levelupclassoverride) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'LevelUpClassOverride' effect."} | 2 |
| [`ManaCostReductionTagged`](./Passives_and_Statuses.md#context-manacostreductiontagged) | Block | {'type': '`Block`', 'df': "Applies the 'ManaCostReductionTagged' effect. | 2 |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'MoveAndUseAbilityEachTurnBeginIfPossible' effect."} | 2 |
| [`MoveTowardsDamageSource`](./Passives_and_Statuses.md#context-movetowardsdamagesource) | Block | {'type': '`Block`', 'df': "Applies the 'MoveTowardsDamageSource' effect. | 2 |
| `NubbyTossPriority` | Number | {'type': '`Number`', 'df': "Applies the 'NubbyTossPriority' effect."} | 2 |
| [`OverrideBasicAttack`](./Enums.md#enum-overridebasicattack) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'OverrideBasicAttack' effect."} | 2 |
| [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#context-passiveathealththreshold) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveAtHealthThreshold' effect. | 2 |
| `PassiveLevelUpAtCombatEnd` | Number | {'type': '`Number`', 'df': "Applies the 'PassiveLevelUpAtCombatEnd' effect."} | 2 |
| [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#context-passivewhenatfullmana) | Block | {'type': '`Block`', 'df': "State Trigger: Grants nested passives when at full mana. | 2 |
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'SpawnThingOnDeath' effect."} | 2 |
| `SpeedUp` | Number | {'type': 'Number', 'df': "Applies the 'SpeedUp' effect."} | 2 |
| [`StatsAtLowHealth`](./Passives_and_Statuses.md#context-statsatlowhealth) | Block | {'type': '`Block`', 'df': "Applies the 'StatsAtLowHealth' effect. | 2 |
| [`StatusIfUnusedMovePoints`](./Passives_and_Statuses.md#context-statusifunusedmovepoints) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to if unused move points. | 2 |
| [`StatusKilledCharacters`](./Passives_and_Statuses.md#context-statuskilledcharacters) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to killed characters. | 2 |
| [`StatusOnAllyCatDeath`](./Passives_and_Statuses.md#context-statusonallycatdeath) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when ally cat death. | 2 |
| [`StatusOnBattleStart`](./Passives_and_Statuses.md#context-statusonbattlestart) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when battle start. | 2 |
| [`StatusOnCastSpell`](./Passives_and_Statuses.md#context-statusoncastspell) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when cast spell. | 2 |
| [`StatusOnEatFood`](./Passives_and_Statuses.md#context-statusoneatfood) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when eat food. | 2 |
| [`StatusOnKillEnemy`](./Passives_and_Statuses.md#context-statusonkillenemy) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when kill enemy. | 2 |
| [`StatusOnTookDamageFromAbility`](./Passives_and_Statuses.md#context-statusontookdamagefromability) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when took damage from ability. | 2 |
| [`StatusOnTurnEndIfCastNSpells`](./Passives_and_Statuses.md#context-statusonturnendifcastnspells) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when turn end if cast n spells. | 2 |
| [`StatusOnTurnEndIfManaExact`](./Passives_and_Statuses.md#context-statusonturnendifmanaexact) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when turn end if mana exact. | 2 |
| [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#context-statusonturnendifmanaorhealthexact) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when turn end if mana or health exact. | 2 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies the 'StrengthUp' effect."} | 2 |
| [`TaggedPickupEffectReplacement`](./Passives_and_Statuses.md#context-taggedpickupeffectreplacement) | Block | {'type': '`Block`', 'df': "Applies the 'TaggedPickupEffectReplacement' effect. | 2 |
| `TrinketActiveEffectsMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies the 'TrinketActiveEffectsMultiplierBonus' effect."} | 2 |
| `TrinketPassiveMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies the 'TrinketPassiveMultiplierBonus' effect."} | 2 |
| `Weakness` | Number | {'type': '`Number`', 'df': "Applies the 'Weakness' effect."} | 2 |
| [`AbilityWhenTaggedCharacterMovesNear`](./Passives_and_Statuses.md#context-abilitywhentaggedcharactermovesnear) | Block | {'type': '`Block`', 'df': "Applies the 'AbilityWhenTaggedCharacterMovesNear' effect. | 1 |
| `AbsorbManaAura` | Number | {'type': '`Number`', 'df': "Applies the 'AbsorbManaAura' effect."} | 1 |
| `AddAllyNeighborsToAttackRange` | Number | {'type': '`Number`', 'df': "Applies the 'AddAllyNeighborsToAttackRange' effect."} | 1 |
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'AddHiddenTag' effect."} | 1 |
| `AddKnockbackDamage` | Number | {'type': '`Number`', 'df': "Applies the 'AddKnockbackDamage' effect."} | 1 |
| `AddLevelUpStatMultiplier` | Number | {'type': '`Number`', 'df': "Applies the 'AddLevelUpStatMultiplier' effect."} | 1 |
| [`AddPassiveToSpawnedRocks`](./Passives_and_Statuses.md#context-addpassivetospawnedrocks) | Block | {'type': '`Block`', 'df': "Applies the 'AddPassiveToSpawnedRocks' effect. | 1 |
| [`AddPassivesToSummonAbilityMinions`](./Passives_and_Statuses.md#context-addpassivestosummonabilityminions) | Block | {'type': '`Block`', 'df': "Applies the 'AddPassivesToSummonAbilityMinions' effect. | 1 |
| [`AddSelfStatusToBasicAttack`](./Passives_and_Statuses.md#context-addselfstatustobasicattack) | Block | {'type': '`Block`', 'df': "Applies the 'AddSelfStatusToBasicAttack' effect. | 1 |
| [`AddSelfStatusToWeapons`](./Passives_and_Statuses.md#context-addselfstatustoweapons) | Block | {'type': '`Block`', 'df': "Applies the 'AddSelfStatusToWeapons' effect. | 1 |
| `AddSpellDamage` | Number | {'type': 'Number', 'df': "Applies the 'AddSpellDamage' effect."} | 1 |
| `AddStartingMana` | Number | {'type': '`Number`', 'df': "Applies the 'AddStartingMana' effect."} | 1 |
| [`AddStatusToBasicAttackWithCooldown`](./Passives_and_Statuses.md#context-addstatustobasicattackwithcooldown) | Block | {'type': '`Block`', 'df': "Applies the 'AddStatusToBasicAttackWithCooldown' effect. | 1 |
| [`AddStatusToExplosions`](./Passives_and_Statuses.md#context-addstatustoexplosions) | Block | {'type': '`Block`', 'df': "Applies the 'AddStatusToExplosions' effect."} | 1 |
| [`AddStatusToFirstBasicAttack`](./Passives_and_Statuses.md#context-addstatustofirstbasicattack) | Block | {'type': '`Block`', 'df': "Applies the 'AddStatusToFirstBasicAttack' effect. | 1 |
| [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage) | Block | {'type': '`Block`', 'df': "Applies the 'AddStatusToMeleeDamage' effect. | 1 |
| [`AddStatusToReceivedDamage_ExcludeStatuses`](./Passives_and_Statuses.md#context-addstatustoreceiveddamage_excludestatuses) | Block | {'type': '`Block`', 'df': "Applies the 'AddStatusToReceivedDamage_ExcludeStatuses' effect. | 1 |
| [`AddStatusToTrampleDamage`](./Passives_and_Statuses.md#context-addstatustotrampledamage) | Block | {'type': '`Block`', 'df': "Applies the 'AddStatusToTrampleDamage' effect. | 1 |
| [`AddStatusesIfPersistentWeatherElement`](./Passives_and_Statuses.md#context-addstatusesifpersistentweatherelement) | Block | {'type': '`Block`', 'df': "Applies the 'AddStatusesIfPersistentWeatherElement' effect. | 1 |
| [`AddStatusesToReceivedElementalDamage`](./Passives_and_Statuses.md#context-addstatusestoreceivedelementaldamage) | Block | {'type': '`Block`', 'df': "Applies the 'AddStatusesToReceivedElementalDamage' effect. | 1 |
| [`AddTemporaryEffectsToBasicAttack`](./Passives_and_Statuses.md#context-addtemporaryeffectstobasicattack) | Block | {'type': '`Block`', 'df': "Applies the 'AddTemporaryEffectsToBasicAttack' effect. | 1 |
| `AddUnfilledMaxHealth` | Number | {'type': '`Number`', 'df': "Applies the 'AddUnfilledMaxHealth' effect."} | 1 |
| `AddWeaponScaling` | Number | {'type': '`Number`', 'df': "Applies the 'AddWeaponScaling' effect."} | 1 |
| [`AfterImage`](./Enums.md#enum-afterimage) | Enum | {'type': '`Enum/String`', 'df': "Spawns a visual decoy or shade at the caster's previous location."} | 1 |
| `AllowPassTurn` | Number | {'type': '`Number`', 'df': "Applies the 'AllowPassTurn' effect."} | 1 |
| [`AllyDamageReaction`](./Enums.md#enum-allydamagereaction) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'AllyDamageReaction' effect."} | 1 |
| `AllyDamageReduction` | Number | {'type': '`Number`', 'df': "Applies the 'AllyDamageReduction' effect."} | 1 |
| [`AllyHealthRegenAura`](./Passives_and_Statuses.md#context-allyhealthregenaura) | Block | {'type': '`Block`', 'df': "Applies the 'AllyHealthRegenAura' effect. | 1 |
| [`AllyMoveAbilityAura`](./Enums.md#enum-allymoveabilityaura) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'AllyMoveAbilityAura' effect."} | 1 |
| `AllyMultiplyKnockbackDamage` | Number | {'type': '`Number`', 'df': "Applies the 'AllyMultiplyKnockbackDamage' effect."} | 1 |
| [`AlternateCraftingPools`](./Passives_and_Statuses.md#context-alternatecraftingpools) | Block | {'type': '`Block`', 'df': "Applies the 'AlternateCraftingPools' effect. | 1 |
| `AmplifyKnockback` | Number | {'type': '`Number`', 'df': "Applies the 'AmplifyKnockback' effect."} | 1 |
| `AmplifyPositiveStatus` | Number | {'type': '`Number`', 'df': "Applies the 'AmplifyPositiveStatus' effect."} | 1 |
| [`ApplyStatusesToRandomEnemiesEachTurn`](./Passives_and_Statuses.md#context-applystatusestorandomenemieseachturn) | Block | {'type': '`Block`', 'df': "Applies the 'ApplyStatusesToRandomEnemiesEachTurn' effect. | 1 |
| [`Autism`](./Passives_and_Statuses.md#context-autism) | Block | {'type': '`Block`', 'df': "Applies the 'Autism' effect. | 1 |
| `AutoCritLowDamage` | Number | {'type': '`Number`', 'df': "Applies the 'AutoCritLowDamage' effect."} | 1 |
| `AutoEquipConsumables` | Number | {'type': '`Number`', 'df': "Applies the 'AutoEquipConsumables' effect."} | 1 |
| `BackstabWeakness` | Number | {'type': '`Number`', 'df': "Applies the 'BackstabWeakness' effect."} | 1 |
| `BasicAttackStatusCarefulness` | Number | {'type': '`Number`', 'df': "Applies the 'BasicAttackStatusCarefulness' effect."} | 1 |
| [`BlacklistPickupType`](./Enums.md#enum-blacklistpickuptype) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'BlacklistPickupType' effect."} | 1 |
| `BleedThorns` | Number | {'type': '`Number`', 'df': "Applies the 'BleedThorns' effect."} | 1 |
| `BonusFoodEachBattle` | Number | {'type': '`Number`', 'df': "Applies the 'BonusFoodEachBattle' effect."} | 1 |
| [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems) | Block | {'type': '`Block`', 'df': "Applies the 'BoobyTrapItems' effect. | 1 |
| `BoostAllyStatsOnDeath` | Number | {'type': '`Number`', 'df': "Applies the 'BoostAllyStatsOnDeath' effect."} | 1 |
| `BoostDamageAura` | Number | {'type': '`Number`', 'df': "Applies the 'BoostDamageAura' effect."} | 1 |
| `BoostRangeAura` | Number | {'type': '`Number`', 'df': "Applies the 'BoostRangeAura' effect."} | 1 |
| [`BouncyProjectiles`](./Passives_and_Statuses.md#context-bouncyprojectiles) | Block | {'type': '`Block`', 'df': "Applies the 'BouncyProjectiles' effect. | 1 |
| `BraceForEachNeighboringEnemy` | Number | {'type': '`Number`', 'df': "Applies the 'BraceForEachNeighboringEnemy' effect."} | 1 |
| `BuffImmunity` | Number | {'type': '`Number`', 'df': "Applies the 'BuffImmunity' effect."} | 1 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies the 'Burn' effect."} | 1 |
| `CCImmunity` | Number | {'type': '`Number`', 'df': "Applies the 'CCImmunity' effect."} | 1 |
| `CanRemoveCursedItems` | Number | {'type': '`Number`', 'df': "Applies the 'CanRemoveCursedItems' effect."} | 1 |
| `CantDodge` | Number | {'type': '`Number`', 'df': "Applies the 'CantDodge' effect."} | 1 |
| `CapDamageFromAllies` | Number | {'type': '`Number`', 'df': "Applies the 'CapDamageFromAllies' effect."} | 1 |
| `CapMovementAbilityRange` | Number | {'type': '`Number`', 'df': "Applies the 'CapMovementAbilityRange' effect."} | 1 |
| [`CatAPultAnimation`](./Passives_and_Statuses.md#context-catapultanimation) | Block | {'type': '`Block`', 'df': "Applies the 'CatAPultAnimation' effect. | 1 |
| [`CatchProjectiles`](./Passives_and_Statuses.md#context-catchprojectiles) | Block | {'type': '`Block`', 'df': "Applies the 'CatchProjectiles' effect. | 1 |
| `ChainKnockback` | Number | {'type': '`Number`', 'df': "Applies the 'ChainKnockback' effect."} | 1 |
| [`ChanceToBackflip`](./Passives_and_Statuses.md#context-chancetobackflip) | Block | {'type': '`Block`', 'df': "Applies the 'ChanceToBackflip' effect. | 1 |
| `ChanceToBlockAndCounter` | Number | {'type': '`Number`', 'df': "Applies the 'ChanceToBlockAndCounter' effect."} | 1 |
| `ChanceToRevive` | Number | {'type': '`Number`', 'df': "Applies the 'ChanceToRevive' effect."} | 1 |
| `CharmAllFlies` | Number | {'type': '`Number`', 'df': "Applies the 'CharmAllFlies' effect."} | 1 |
| [`ClassManaCostReduction`](./Passives_and_Statuses.md#context-classmanacostreduction) | Block | {'type': '`Block`', 'df': "Applies the 'ClassManaCostReduction' effect. | 1 |
| [`CobraReflex`](./Enums.md#enum-cobrareflex) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'CobraReflex' effect."} | 1 |
| `CoinsAddDamage` | Number | {'type': '`Number`', 'df': "Applies the 'CoinsAddDamage' effect."} | 1 |
| `CollectPickupsOnBattleEnd` | Number | {'type': '`Number`', 'df': "Applies the 'CollectPickupsOnBattleEnd' effect."} | 1 |
| `Conductor` | Number | {'type': '`Number`', 'df': "Applies the 'Conductor' effect."} | 1 |
| [`ConfusionEffectOnTaggedAbilities`](./Enums.md#enum-confusioneffectontaggedabilities) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'ConfusionEffectOnTaggedAbilities' effect."} | 1 |
| `ConjureCastSpellsForAllies` | Number | {'type': '`Number`', 'df': "Applies the 'ConjureCastSpellsForAllies' effect."} | 1 |
| `ConsumableEffectsMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies the 'ConsumableEffectsMultiplierBonus' effect."} | 1 |
| `ConsumablesInfiniteRange` | Number | {'type': '`Number`', 'df': "Applies the 'ConsumablesInfiniteRange' effect."} | 1 |
| `ConsumablesMeleeRange` | Number | {'type': '`Number`', 'df': "Applies the 'ConsumablesMeleeRange' effect."} | 1 |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum | {'type': 'Enum/String', 'df': "Applies the 'CounterAttack' effect."} | 1 |
| `DamageEnemiesOnHeal` | Number | {'type': '`Number`', 'df': 'Combat Trigger: Deals damage to enemies on heal.'} | 1 |
| `DamageEnemiesOnKill` | Number | {'type': '`Number`', 'df': 'Combat Trigger: Deals damage to enemies on kill.'} | 1 |
| [`DamageIfDidntUseSpecificAbility`](./Passives_and_Statuses.md#context-damageifdidntusespecificability) | Block | {'type': '`Block`', 'df': 'Combat Trigger: Deals damage to if didnt use specific ability. | 1 |
| [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell) | Block | {'type': '`Block`', 'df': 'Combat Trigger: Deals damage to neighbor tiles when cast spell. | 1 |
| [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#context-damageneighborsaftermove) | Block | {'type': '`Block`', 'df': 'Combat Trigger: Deals damage to neighbors after move. | 1 |
| [`DamageReductionAura`](./Passives_and_Statuses.md#context-damagereductionaura) | Block | {'type': '`Block`', 'df': 'Combat Trigger: Deals damage to reduction aura. | 1 |
| `DamageUp` | Number | {'type': 'Number', 'df': 'Combat Trigger: Deals damage to up.'} | 1 |
| `DeathChill` | Number | {'type': '`Number`', 'df': "Applies the 'DeathChill' effect."} | 1 |
| `DebuffImmunity` | Number | {'type': '`Number`', 'df': "Applies the 'DebuffImmunity' effect."} | 1 |
| `DejaVu` | Number | {'type': '`Number`', 'df': "Applies the 'DejaVu' effect."} | 1 |
| `DepressionAura` | Number | {'type': '`Number`', 'df': "Applies the 'DepressionAura' effect."} | 1 |
| [`Diabetes`](./Passives_and_Statuses.md#context-diabetes) | Block | {'type': '`Block`', 'df': "Applies the 'Diabetes' effect. | 1 |
| `DirtyClaws` | Number | {'type': '`Number`', 'df': "Applies the 'DirtyClaws' effect."} | 1 |
| [`DisableAbilities`](./Enums.md#enum-disableabilities) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'DisableAbilities' effect."} | 1 |
| [`DisableAbilitiesWithTag`](./Enums.md#enum-disableabilitieswithtag) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'DisableAbilitiesWithTag' effect."} | 1 |
| `Doomed` | Number | {'type': '`Number`', 'df': "Applies the 'Doomed' effect."} | 1 |
| `DoubleCastWeapons` | Number | {'type': '`Number`', 'df': "Applies the 'DoubleCastWeapons' effect."} | 1 |
| `DukeOfFlies` | Number | {'type': '`Number`', 'df': "Applies the 'DukeOfFlies' effect."} | 1 |
| [`EMP`](./Passives_and_Statuses.md#context-emp) | Block | {'type': '`Block`', 'df': "Applies the 'EMP' effect."} | 1 |
| [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement) | Block | {'type': '`Block`', 'df': "Applies the 'ElementalAttunement' effect. | 1 |
| [`ElementalManaCostReduction`](./Passives_and_Statuses.md#context-elementalmanacostreduction) | Block | {'type': '`Block`', 'df': "Applies the 'ElementalManaCostReduction' effect. | 1 |
| `Empath` | Number | {'type': '`Number`', 'df': "Applies the 'Empath' effect."} | 1 |
| `EnemiesGetPickupsKnockedOut` | Number | {'type': '`Number`', 'df': "Applies the 'EnemiesGetPickupsKnockedOut' effect."} | 1 |
| `EnergyStorm` | Number | {'type': '`Number`', 'df': "Applies the 'EnergyStorm' effect."} | 1 |
| `EquipmentPassiveMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies the 'EquipmentPassiveMultiplierBonus' effect."} | 1 |
| `EquipmentSetBonusBonus` | Number | {'type': '`Number`', 'df': "Applies the 'EquipmentSetBonusBonus' effect."} | 1 |
| [`EscapeSequence`](./Passives_and_Statuses.md#context-escapesequence) | Block | {'type': '`Block`', 'df': "Applies the 'EscapeSequence' effect. | 1 |
| [`Eternal`](./Passives_and_Statuses.md#context-eternal) | Block | {'type': '`Block`', 'df': "Applies the 'Eternal' effect. | 1 |
| `ExhaustionRoundChange` | Number | {'type': '`Number`', 'df': "Applies the 'ExhaustionRoundChange' effect."} | 1 |
| `ExplodeOverkilledEnemies` | Number | {'type': '`Number`', 'df': "Applies the 'ExplodeOverkilledEnemies' effect."} | 1 |
| `ExtraBasicMoves_Status` | Number | {'type': '`Number`', 'df': "Applies the 'ExtraBasicMoves_Status' effect."} | 1 |
| `ExtraInjuryOnDeath` | Number | {'type': '`Number`', 'df': "Applies the 'ExtraInjuryOnDeath' effect."} | 1 |
| `ExtraMovePoints` | Number | {'type': 'Number', 'df': "Applies the 'ExtraMovePoints' effect."} | 1 |
| [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#context-extrastatuswhendealingdamage) | Block | {'type': '`Block`', 'df': "Applies the 'ExtraStatusWhenDealingDamage' effect. | 1 |
| `FaceArmorPassiveMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies the 'FaceArmorPassiveMultiplierBonus' effect."} | 1 |
| `FaceShield` | Number | {'type': '`Number`', 'df': "Applies the 'FaceShield' effect."} | 1 |
| `FamiliarSecondaryDamageImmunity` | Number | {'type': '`Number`', 'df': "Applies the 'FamiliarSecondaryDamageImmunity' effect."} | 1 |
| `FlowerPowerAuraBrace` | Number | {'type': '`Number`', 'df': "Applies the 'FlowerPowerAuraBrace' effect."} | 1 |
| `FlowerPowerAuraStrength` | Number | {'type': '`Number`', 'df': "Applies the 'FlowerPowerAuraStrength' effect."} | 1 |
| `FlowersOnEndTurn` | Number | {'type': '`Number`', 'df': "Applies the 'FlowersOnEndTurn' effect."} | 1 |
| `FlyDamageIncrease` | Number | {'type': '`Number`', 'df': "Applies the 'FlyDamageIncrease' effect."} | 1 |
| `Flying` | Number | {'type': 'Number', 'df': "Applies the 'Flying' effect."} | 1 |
| [`FollowUp`](./Enums.md#enum-followup) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'FollowUp' effect."} | 1 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | {'type': 'Enum/String', 'df': "Applies the 'ForceUseAbility' effect."} | 1 |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'FreePathfindElement' effect."} | 1 |
| `FreeSpellsAtFullMana` | Number | {'type': '`Number`', 'df': "Applies the 'FreeSpellsAtFullMana' effect."} | 1 |
| `FrontstabBasicAttackCritChance` | Number | {'type': '`Number`', 'df': "Applies the 'FrontstabBasicAttackCritChance' effect."} | 1 |
| `FullHeal` | Number | {'type': 'Number', 'df': "Applies the 'FullHeal' effect."} | 1 |
| `FullHealthCritChance` | Number | {'type': '`Number`', 'df': "Applies the 'FullHealthCritChance' effect."} | 1 |
| `FullPower` | Number | {'type': '`Number`', 'df': "Applies the 'FullPower' effect."} | 1 |
| [`FurnitureStats`](./Passives_and_Statuses.md#context-furniturestats) | Block | {'type': '`Block`', 'df': "Applies the 'FurnitureStats' effect. | 1 |
| `GainExtraShield` | Number | {'type': '`Number`', 'df': "Applies the 'GainExtraShield' effect."} | 1 |
| [`GravityWell`](./Passives_and_Statuses.md#context-gravitywell) | Block | {'type': '`Block`', 'df': "Applies the 'GravityWell' effect. | 1 |
| `HPGainBlock` | Number | {'type': '`Number`', 'df': "Applies the 'HPGainBlock' effect."} | 1 |
| `HealDamagesEnemies` | Number | {'type': '`Number`', 'df': "Applies the 'HealDamagesEnemies' effect."} | 1 |
| `HealsAlsoRegenMana` | Number | {'type': '`Number`', 'df': "Applies the 'HealsAlsoRegenMana' effect."} | 1 |
| `HealsCanRevive` | Number | {'type': '`Number`', 'df': "Applies the 'HealsCanRevive' effect."} | 1 |
| [`HolyShieldTransferToTaggedMinions`](./Enums.md#enum-holyshieldtransfertotaggedminions) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'HolyShieldTransferToTaggedMinions' effect."} | 1 |
| `HouseFoodRequirementMultiplier` | Number | {'type': '`Number`', 'df': "Applies the 'HouseFoodRequirementMultiplier' effect."} | 1 |
| `Hypomania` | Number | {'type': '`Number`', 'df': "Applies the 'Hypomania' effect."} | 1 |
| `IgnoreTiles` | Number | {'type': '`Number`', 'df': "Applies the 'IgnoreTiles' effect."} | 1 |
| `ImmortalLeeches` | Number | {'type': '`Number`', 'df': "Applies the 'ImmortalLeeches' effect."} | 1 |
| `IncreaseExplosionSize` | Number | {'type': '`Number`', 'df': "Applies the 'IncreaseExplosionSize' effect."} | 1 |
| `IncreaseHealingSpellRange` | Number | {'type': '`Number`', 'df': "Applies the 'IncreaseHealingSpellRange' effect."} | 1 |
| `IncreaseSpellRange` | Number | {'type': '`Number`', 'df': "Applies the 'IncreaseSpellRange' effect."} | 1 |
| [`InfiniteRebirth`](./Passives_and_Statuses.md#context-infiniterebirth) | Block | {'type': '`Block`', 'df': "Applies the 'InfiniteRebirth' effect. | 1 |
| `InvertBrainFaction` | Number | {'type': '`Number`', 'df': "Applies the 'InvertBrainFaction' effect."} | 1 |
| `KillsHeal` | Number | {'type': '`Number`', 'df': "Applies the 'KillsHeal' effect."} | 1 |
| [`KillsToMeat`](./Enums.md#enum-killstomeat) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'KillsToMeat' effect."} | 1 |
| [`LateBloomer`](./Passives_and_Statuses.md#context-latebloomer) | Block | {'type': '`Block`', 'df': "Applies the 'LateBloomer' effect. | 1 |
| `LightningAspectCharge` | Number | {'type': '`Number`', 'df': "Applies the 'LightningAspectCharge' effect."} | 1 |
| [`LightningRod`](./Passives_and_Statuses.md#context-lightningrod) | Block | {'type': '`Block`', 'df': "Applies the 'LightningRod' effect. | 1 |
| `LimitDamage` | Number | {'type': '`Number`', 'df': "Applies the 'LimitDamage' effect."} | 1 |
| `LimitHeal` | Number | {'type': '`Number`', 'df': "Applies the 'LimitHeal' effect."} | 1 |
| `LimitSelfKnockbackDamage` | Number | {'type': '`Number`', 'df': "Applies the 'LimitSelfKnockbackDamage' effect."} | 1 |
| [`LimitedTileTrail`](./Enums.md#enum-limitedtiletrail) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'LimitedTileTrail' effect."} | 1 |
| `LineOfSightTrueSightAura` | Number | {'type': '`Number`', 'df': "Applies the 'LineOfSightTrueSightAura' effect."} | 1 |
| `LobbedHook` | Number | {'type': '`Number`', 'df': "Applies the 'LobbedHook' effect."} | 1 |
| [`LowHealthAllyDodgeChanceAura`](./Passives_and_Statuses.md#context-lowhealthallydodgechanceaura) | Block | {'type': '`Block`', 'df': "Applies the 'LowHealthAllyDodgeChanceAura' effect. | 1 |
| `Madness` | Number | {'type': 'Number', 'df': 'Applies the Madness debuff/status effect.'} | 1 |
| `MakeBasicAttackPassThroughThings` | Number | {'type': '`Number`', 'df': "Applies the 'MakeBasicAttackPassThroughThings' effect."} | 1 |
| `ManaRegenMultiplierIfManaEmpty` | Number | {'type': '`Number`', 'df': "Applies the 'ManaRegenMultiplierIfManaEmpty' effect."} | 1 |
| `MaxAccuracy` | Number | {'type': '`Number`', 'df': "Applies the 'MaxAccuracy' effect."} | 1 |
| `MaxStartingMana` | Number | {'type': '`Number`', 'df': "Applies the 'MaxStartingMana' effect."} | 1 |
| `MegaMinions` | Number | {'type': '`Number`', 'df': "Applies the 'MegaMinions' effect."} | 1 |
| `Metal` | Number | {'type': '`Number`', 'df': "Applies the 'Metal' effect."} | 1 |
| `MetalDetector` | Number | {'type': '`Number`', 'df': "Applies the 'MetalDetector' effect."} | 1 |
| `MinimumTech` | Number | {'type': '`Number`', 'df': "Applies the 'MinimumTech' effect."} | 1 |
| [`MoveAwayFromDamageSource`](./Enums.md#enum-moveawayfromdamagesource) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'MoveAwayFromDamageSource' effect."} | 1 |
| `MoveQuivered` | Number | {'type': 'Number', 'df': "Applies the 'MoveQuivered' effect."} | 1 |
| [`MoveSpeedMultiplier`](./Enums.md#enum-movespeedmultiplier) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'MoveSpeedMultiplier' effect."} | 1 |
| [`MoveWhenDamaged`](./Passives_and_Statuses.md#context-movewhendamaged) | Block | {'type': '`Block`', 'df': "Applies the 'MoveWhenDamaged' effect. | 1 |
| [`MovementReaction`](./Passives_and_Statuses.md#context-movementreaction) | Block | {'type': '`Block`', 'df': "Applies the 'MovementReaction' effect. | 1 |
| `NeckArmorPassiveMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies the 'NeckArmorPassiveMultiplierBonus' effect."} | 1 |
| `NoManaRegen` | Number | {'type': '`Number`', 'df': "Applies the 'NoManaRegen' effect."} | 1 |
| `NoReflection` | Number | {'type': '`Number`', 'df': "Applies the 'NoReflection' effect."} | 1 |
| `NumbingLeeches` | Number | {'type': '`Number`', 'df': "Applies the 'NumbingLeeches' effect."} | 1 |
| `OverhealGainsBothShield` | Number | {'type': '`Number`', 'df': "Applies the 'OverhealGainsBothShield' effect."} | 1 |
| `OverrideMaxHealth` | Number | {'type': '`Number`', 'df': "Applies the 'OverrideMaxHealth' effect."} | 1 |
| `OverrideMaxMana` | Number | {'type': '`Number`', 'df': "Applies the 'OverrideMaxMana' effect."} | 1 |
| `OverridePalette` | Number | {'type': '`Number`', 'df': "Applies the 'OverridePalette' effect."} | 1 |
| [`Paranoia`](./Enums.md#enum-paranoia) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'Paranoia' effect."} | 1 |
| `ParasitesArentCursed` | Number | {'type': '`Number`', 'df': "Applies the 'ParasitesArentCursed' effect."} | 1 |
| [`PassiveAfterXKills`](./Passives_and_Statuses.md#context-passiveafterxkills) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveAfterXKills' effect. | 1 |
| [`PassiveAtFullHealth`](./Passives_and_Statuses.md#context-passiveatfullhealth) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveAtFullHealth' effect. | 1 |
| [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#context-passiveatinjurythreshold) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveAtInjuryThreshold' effect. | 1 |
| [`PassiveLevelScaledStatus`](./Passives_and_Statuses.md#context-passivelevelscaledstatus) | Block | {'type': '`Block`', 'df': 'Applies the \'PassiveLevelScaledStatus\' effect. | 1 |
| [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveUntilCastSpell' effect. | 1 |
| [`PassiveUntilGetKill`](./Passives_and_Statuses.md#context-passiveuntilgetkill) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveUntilGetKill' effect. | 1 |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement) | Block | {'type': '`Block`', 'df': 'State Trigger: Grants nested passives when affected by element.'} | 1 |
| [`PassiveWhenTheAlpha`](./Passives_and_Statuses.md#context-passivewhenthealpha) | Block | {'type': '`Block`', 'df': "State Trigger: Grants nested passives when the alpha. | 1 |
| [`PassiveWhileInMonkMeleeStance`](./Passives_and_Statuses.md#context-passivewhileinmonkmeleestance) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveWhileInMonkMeleeStance' effect. | 1 |
| [`PassiveWhileInMonkRangedStance`](./Passives_and_Statuses.md#context-passivewhileinmonkrangedstance) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveWhileInMonkRangedStance' effect. | 1 |
| [`PassiveWhilePreviewingMonkRangedStance`](./Passives_and_Statuses.md#context-passivewhilepreviewingmonkrangedstance) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveWhilePreviewingMonkRangedStance' effect. | 1 |
| [`PassiveWhileWearingMetal`](./Passives_and_Statuses.md#context-passivewhilewearingmetal) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveWhileWearingMetal' effect. | 1 |
| `PermanentImmobile` | Number | {'type': '`Number`', 'df': "Applies the 'PermanentImmobile' effect."} | 1 |
| `PermanentItems` | Number | {'type': '`Number`', 'df': "Applies the 'PermanentItems' effect."} | 1 |
| `PermanentKitten` | Number | {'type': '`Number`', 'df': "Applies the 'PermanentKitten' effect."} | 1 |
| `PermanentMadness` | Number | {'type': 'Number', 'df': "Applies the 'PermanentMadness' effect."} | 1 |
| `Poison` | Number | {'type': '`Number`', 'df': "Applies the 'Poison' effect."} | 1 |
| `PoisonThorns` | Number | {'type': '`Number`', 'df': "Applies the 'PoisonThorns' effect."} | 1 |
| [`PoopWhenHit`](./Enums.md#enum-poopwhenhit) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'PoopWhenHit' effect."} | 1 |
| [`ProtectTargetedAllies`](./Enums.md#enum-protecttargetedallies) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'ProtectTargetedAllies' effect."} | 1 |
| `Quiver` | Number | {'type': '`Number`', 'df': "Applies the 'Quiver' effect."} | 1 |
| `Quivered` | Number | {'type': 'Number', 'df': "Applies the 'Quivered' effect."} | 1 |
| [`RandomPassivePool`](./Passives_and_Statuses.md#context-randompassivepool) | Block | {'type': '`Block`', 'df': "Applies the 'RandomPassivePool' effect. | 1 |
| `RangedTrueShot` | Number | {'type': '`Number`', 'df': "Applies the 'RangedTrueShot' effect."} | 1 |
| `RealTimePressure_OneUnit` | Number | {'type': '`Number`', 'df': "Applies the 'RealTimePressure_OneUnit' effect."} | 1 |
| [`ReceivedStatusReplacement`](./Arrays.md#array-receivedstatusreplacement) | Array | {'type': '`Array`', 'df': "Applies the 'ReceivedStatusReplacement' effect."} | 1 |
| `RemoveLineOfSightRestrictions` | Number | {'type': '`Number`', 'df': "Applies the 'RemoveLineOfSightRestrictions' effect."} | 1 |
| `RemoveOncePerFightRestriction` | Number | {'type': '`Number`', 'df': "Applies the 'RemoveOncePerFightRestriction' effect."} | 1 |
| [`ReplaceBasicAttackWhenDead`](./Enums.md#enum-replacebasicattackwhendead) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'ReplaceBasicAttackWhenDead' effect."} | 1 |
| `ReviveOnWin` | Number | {'type': '`Number`', 'df': "Applies the 'ReviveOnWin' effect."} | 1 |
| `RobotsInheritArmor` | Number | {'type': '`Number`', 'df': "Applies the 'RobotsInheritArmor' effect."} | 1 |
| `RockDetector` | Number | {'type': '`Number`', 'df': "Applies the 'RockDetector' effect."} | 1 |
| [`ScaledStatusOnBleedDamage`](./Passives_and_Statuses.md#context-scaledstatusonbleeddamage) | Block | {'type': '`Block`', 'df': "Applies the 'ScaledStatusOnBleedDamage' effect. | 1 |
| [`ScaledStatusOnOverMana`](./Passives_and_Statuses.md#context-scaledstatusonovermana) | Block | {'type': '`Block`', 'df': "Applies the 'ScaledStatusOnOverMana' effect. | 1 |
| [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#context-scaledstatusonspendmana) | Block | {'type': '`Block`', 'df': "Applies the 'ScaledStatusOnSpendMana' effect. | 1 |
| `SchrodingerDisorder` | Number | {'type': '`Number`', 'df': "Applies the 'SchrodingerDisorder' effect."} | 1 |
| `Scleroderma` | Number | {'type': '`Number`', 'df': "Applies the 'Scleroderma' effect."} | 1 |
| [`SecurityBotProtect`](./Passives_and_Statuses.md#context-securitybotprotect) | Block | {'type': '`Block`', 'df': "Applies the 'SecurityBotProtect' effect. | 1 |
| [`SelfDamageWhenDealDamage`](./Passives_and_Statuses.md#context-selfdamagewhendealdamage) | Block | {'type': '`Block`', 'df': "Applies the 'SelfDamageWhenDealDamage' effect. | 1 |
| [`SetDefaultFacePassive`](./Enums.md#enum-setdefaultfacepassive) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'SetDefaultFacePassive' effect."} | 1 |
| `ShareHealthRegen` | Number | {'type': '`Number`', 'df': "Applies the 'ShareHealthRegen' effect."} | 1 |
| `SharePickups` | Number | {'type': '`Number`', 'df': "Applies the 'SharePickups' effect."} | 1 |
| `ShoulderCheck` | Number | {'type': '`Number`', 'df': "Applies the 'ShoulderCheck' effect."} | 1 |
| [`ShovingMatch`](./Enums.md#enum-shovingmatch) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'ShovingMatch' effect."} | 1 |
| `ShowHiddenThings` | Number | {'type': '`Number`', 'df': "Applies the 'ShowHiddenThings' effect."} | 1 |
| `Slow` | Number | {'type': '`Number`', 'df': "Applies the 'Slow' effect."} | 1 |
| `SmallEnemiesIgnoreYou` | Number | {'type': '`Number`', 'df': "Applies the 'SmallEnemiesIgnoreYou' effect."} | 1 |
| `SmallRockBehavior` | Number | {'type': '`Number`', 'df': "Applies the 'SmallRockBehavior' effect."} | 1 |
| [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#context-smiteenemieswhokill) | Block | {'type': '`Block`', 'df': "Applies the 'SmiteEnemiesWhoKill' effect. | 1 |
| [`SpawnCatCopyOnBattleStart`](./Passives_and_Statuses.md#context-spawncatcopyonbattlestart) | Block | {'type': '`Block`', 'df': "Applies the 'SpawnCatCopyOnBattleStart' effect. | 1 |
| `SpawnCreepOnHit` | Number | {'type': '`Number`', 'df': "Applies the 'SpawnCreepOnHit' effect."} | 1 |
| [`SpawnObjectOnPopCorpse`](./Enums.md#enum-spawnobjectonpopcorpse) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'SpawnObjectOnPopCorpse' effect."} | 1 |
| [`SpawnOnBattleStartRandomEmptyTile`](./Passives_and_Statuses.md#context-spawnonbattlestartrandomemptytile) | Block | {'type': '`Block`', 'df': "Applies the 'SpawnOnBattleStartRandomEmptyTile' effect. | 1 |
| [`SpecialFriends`](./Passives_and_Statuses.md#context-specialfriends) | Block | {'type': '`Block`', 'df': "Applies the 'SpecialFriends' effect. | 1 |
| `SplittableMove` | Number | {'type': '`Number`', 'df': "Applies the 'SplittableMove' effect."} | 1 |
| `SpreadExtraDebuffs` | Number | {'type': '`Number`', 'df': "Applies the 'SpreadExtraDebuffs' effect."} | 1 |
| `SpreadPainBonus` | Number | {'type': '`Number`', 'df': "Applies the 'SpreadPainBonus' effect."} | 1 |
| `StatMinimum` | Number | {'type': '`Number`', 'df': "Applies the 'StatMinimum' effect."} | 1 |
| [`StatusAdjacentOnTheirTurnBegin`](./Passives_and_Statuses.md#context-statusadjacentontheirturnbegin) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to adjacent on their turn begin. | 1 |
| [`StatusAfterCastSpell`](./Passives_and_Statuses.md#context-statusaftercastspell) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to after cast spell. | 1 |
| [`StatusAlliesOnBattleStart`](./Passives_and_Statuses.md#context-statusalliesonbattlestart) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to allies on battle start. | 1 |
| [`StatusAlliesOnGainCoins`](./Passives_and_Statuses.md#context-statusalliesongaincoins) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to allies on gain coins. | 1 |
| [`StatusAlliesOnKill`](./Passives_and_Statuses.md#context-statusalliesonkill) | Block | {'type': '`Block`', 'df': 'Event Trigger: Applies nested statuses to allies on kill.'} | 1 |
| [`StatusAllyWhenAllySpendsMana`](./Passives_and_Statuses.md#context-statusallywhenallyspendsmana) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to ally when ally spends mana. | 1 |
| [`StatusAnyCatAllyWhoKills`](./Passives_and_Statuses.md#context-statusanycatallywhokills) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to any cat ally who kills. | 1 |
| [`StatusDamagers`](./Passives_and_Statuses.md#context-statusdamagers) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to damagers. | 1 |
| [`StatusEachTurnEndForEachTurn`](./Passives_and_Statuses.md#context-statuseachturnendforeachturn) | Block | {'type': '`Block`', 'df': 'Event Trigger: Applies nested statuses to each turn end for each turn. | 1 |
| [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#context-statuseachturnendperenemykill) | Block | {'type': '`Block`', 'df': 'Event Trigger: Applies nested statuses to each turn end per enemy kill. | 1 |
| [`StatusEnemiesOnDeath`](./Passives_and_Statuses.md#context-statusenemiesondeath) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to enemies on death. | 1 |
| [`StatusEveryXSpellCasts`](./Passives_and_Statuses.md#context-statuseveryxspellcasts) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to every x spell casts. | 1 |
| [`StatusEveryXTurnBegins`](./Passives_and_Statuses.md#context-statuseveryxturnbegins) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to every x turn begins. | 1 |
| [`StatusIfBattleAlreadyBegan`](./Passives_and_Statuses.md#context-statusifbattlealreadybegan) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to if battle already began. | 1 |
| [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers) | Block | {'type': '`Block`', 'df': 'Instantly kills the target if they possess the specified status effects. | 1 |
| [`StatusOnAnyDeath`](./Passives_and_Statuses.md#context-statusonanydeath) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when any death. | 1 |
| [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#context-statusonbattleendifkillthresholdmet) | Block | {'type': '`Block`', 'df': 'Event Trigger: Applies nested statuses when battle end if kill threshold met. | 1 |
| [`StatusOnBreakItem`](./Passives_and_Statuses.md#context-statusonbreakitem) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when break item. | 1 |
| [`StatusOnCollectPickup`](./Passives_and_Statuses.md#context-statusoncollectpickup) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when collect pickup. | 1 |
| [`StatusOnDealtDamage`](./Passives_and_Statuses.md#context-statusondealtdamage) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when dealt damage. | 1 |
| [`StatusOnDealtDamageThreshold`](./Passives_and_Statuses.md#context-statusondealtdamagethreshold) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when dealt damage threshold. | 1 |
| [`StatusOnEatPill`](./Passives_and_Statuses.md#context-statusoneatpill) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when eat pill. | 1 |
| [`StatusOnEndMove`](./Passives_and_Statuses.md#context-statusonendmove) | Block | {'type': '`Block`', 'df': 'Event Trigger: Applies nested statuses when end move. | 1 |
| [`StatusOnGainCoins`](./Passives_and_Statuses.md#context-statusongaincoins) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when gain coins. | 1 |
| [`StatusOnGainShield`](./Passives_and_Statuses.md#context-statusongainshield) | Block | {'type': '`Block`', 'df': 'Event Trigger: Applies nested statuses when gain shield. | 1 |
| [`StatusOnHeal`](./Passives_and_Statuses.md#context-statusonheal) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when heal. | 1 |
| [`StatusOnHealed`](./Passives_and_Statuses.md#context-statusonhealed) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when healed. | 1 |
| [`StatusOnLoseShield`](./Passives_and_Statuses.md#context-statusonloseshield) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when lose shield. | 1 |
| [`StatusOnOverMana`](./Passives_and_Statuses.md#context-statusonovermana) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when over mana. | 1 |
| [`StatusOnPickupCoins`](./Passives_and_Statuses.md#context-statusonpickupcoins) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when pickup coins. | 1 |
| [`StatusOnPopCorpse`](./Passives_and_Statuses.md#context-statusonpopcorpse) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when pop corpse. | 1 |
| [`StatusOnTakeHealthDamage`](./Passives_and_Statuses.md#context-statusontakehealthdamage) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when take health damage. | 1 |
| [`StatusOnTookDamageFromEnemyAbility`](./Passives_and_Statuses.md#context-statusontookdamagefromenemyability) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when took damage from enemy ability. | 1 |
| [`StatusOnTriggerTrap`](./Passives_and_Statuses.md#context-statusontriggertrap) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when trigger trap. | 1 |
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](./Passives_and_Statuses.md#context-statusonturnendifdidntcastabilitytypes) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when turn end if didnt cast ability types. | 1 |
| [`StatusOnUseBasicAttack`](./Passives_and_Statuses.md#context-statusonusebasicattack) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when use basic attack. | 1 |
| [`StatusOnUseElementAbility`](./Passives_and_Statuses.md#context-statusonuseelementability) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when use element ability. | 1 |
| [`StatusPerInjury`](./Passives_and_Statuses.md#context-statusperinjury) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to per injury. | 1 |
| [`StatusReplacement`](./Arrays.md#array-statusreplacement) | Array | {'type': '`Array`', 'df': 'Event Trigger: Applies nested statuses to replacement.'} | 1 |
| [`StatusThingsKnockedBack`](./Passives_and_Statuses.md#context-statusthingsknockedback) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to things knocked back. | 1 |
| [`StatusWhenAllySpendsMana`](./Passives_and_Statuses.md#context-statuswhenallyspendsmana) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to when ally spends mana. | 1 |
| `Stealth` | Number | {'type': '`Number`', 'df': "Applies the 'Stealth' effect."} | 1 |
| `StrengthForEachNeighboringEnemy` | Number | {'type': '`Number`', 'df': "Applies the 'StrengthForEachNeighboringEnemy' effect."} | 1 |
| `StrengthInNumbersAura` | Number | {'type': '`Number`', 'df': "Applies the 'StrengthInNumbersAura' effect."} | 1 |
| `StrictLimitDamage` | Number | {'type': '`Number`', 'df': "Applies the 'StrictLimitDamage' effect."} | 1 |
| `Study` | Number | {'type': '`Number`', 'df': "Applies the 'Study' effect."} | 1 |
| `TauntAlways` | Number | {'type': '`Number`', 'df': "Applies the 'TauntAlways' effect."} | 1 |
| `TauntAtFullHealth` | Number | {'type': '`Number`', 'df': "Applies the 'TauntAtFullHealth' effect."} | 1 |
| `Tech` | Number | {'type': '`Number`', 'df': "Applies the 'Tech' effect."} | 1 |
| `TempInitiativeChange` | Number | {'type': '`Number`', 'df': "Applies the 'TempInitiativeChange' effect."} | 1 |
| [`TheHunger`](./Passives_and_Statuses.md#context-thehunger) | Block | {'type': '`Block`', 'df': "Applies the 'TheHunger' effect. | 1 |
| `TileDamageMultiplier` | Number | {'type': '`Number`', 'df': "Applies the 'TileDamageMultiplier' effect."} | 1 |
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'TileTrail' effect."} | 1 |
| [`TourettesMeows`](./Passives_and_Statuses.md#context-tourettesmeows) | Block | {'type': '`Block`', 'df': "Applies the 'TourettesMeows' effect. | 1 |
| [`TowerDefense`](./Passives_and_Statuses.md#context-towerdefense) | Block | {'type': '`Block`', 'df': "Applies the 'TowerDefense' effect. | 1 |
| [`TowerDefenseReflex`](./Enums.md#enum-towerdefensereflex) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'TowerDefenseReflex' effect."} | 1 |
| `TrapEffectsMultiplier` | Number | {'type': '`Number`', 'df': "Applies the 'TrapEffectsMultiplier' effect."} | 1 |
| `Triskaidekaphobia` | Number | {'type': '`Number`', 'df': "Applies the 'Triskaidekaphobia' effect."} | 1 |
| `UncappedHP` | Number | {'type': '`Number`', 'df': "Applies the 'UncappedHP' effect."} | 1 |
| `UncappedMana` | Number | {'type': '`Number`', 'df': "Applies the 'UncappedMana' effect."} | 1 |
| [`UpgradeLevelUpClassActives`](./Enums.md#enum-upgradelevelupclassactives) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'UpgradeLevelUpClassActives' effect."} | 1 |
| [`UpgradeLevelUpClassPassives`](./Enums.md#enum-upgradelevelupclasspassives) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'UpgradeLevelUpClassPassives' effect."} | 1 |
| `UpgradeSpawnedPickups` | Number | {'type': '`Number`', 'df': "Applies the 'UpgradeSpawnedPickups' effect."} | 1 |
| `Vegan` | Number | {'type': '`Number`', 'df': "Applies the 'Vegan' effect."} | 1 |
| `Vengeful` | Number | {'type': '`Number`', 'df': "Applies the 'Vengeful' effect."} | 1 |
| `WaterWalk` | Number | {'type': '`Number`', 'df': "Applies the 'WaterWalk' effect."} | 1 |
| `WeaponActiveEffectsMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies the 'WeaponActiveEffectsMultiplierBonus' effect."} | 1 |
| `WeaponCountsAsBasicAttack` | Number | {'type': '`Number`', 'df': "Applies the 'WeaponCountsAsBasicAttack' effect."} | 1 |
| `WeaponDamageMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies the 'WeaponDamageMultiplierBonus' effect."} | 1 |
| `WeaponPassiveMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies the 'WeaponPassiveMultiplierBonus' effect."} | 1 |
| `WobblyCat` | Number | {'type': '`Number`', 'df': "Applies the 'WobblyCat' effect."} | 1 |

</details>

---

### Context: `stats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 97

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number | {'type': '`Number`', 'df': ''} | 31 |
| `spd` | Number | {'type': '`Number`', 'df': ''} | 26 |
| `cha` | Number | {'type': '`Number`', 'df': ''} | 22 |
| `int` | Number | {'type': '`Number`', 'df': ''} | 22 |
| `str` | Number | {'type': '`Number`', 'df': ''} | 20 |
| `dex` | Number | {'type': '`Number`', 'df': ''} | 16 |
| `lck` | Number | {'type': '`Number`', 'df': ''} | 13 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 92

> **Referenced by:** [`AddPassivesToCharmed`](./Passives_and_Statuses.md#context-addpassivestocharmed), [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#context-passivewhenatfullmana), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Poison`](./Arrays.md#array-poison) | Array | {'type': '`Number`', 'df': "Applies the 'Poison' effect."} | 12 |
| `Bleed` | Number | {'type': 'Number', 'df': "Applies the 'Bleed' effect."} | 8 |
| `Knockback` | Number | {'type': '`Number`', 'df': "Applies the 'Knockback' effect."} | 7 |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies the 'Bruise' effect."} | 5 |
| [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally) | Block | {'type': 'Block', 'df': 'Conditional trigger: Executes nested logic if the target is friendly to the caster.'} | 5 |
| [`BounceObject`](./Enums.md#enum-bounceobject) | Enum | {'type': '`Enum/String`', 'df': 'Spawns a physics object that visually bounces off the target.'} | 4 |
| [`DistanceBonusDamage`](./Passives_and_Statuses.md#context-distancebonusdamage) | Block | {'type': '`Block`', 'df': "Applies the 'DistanceBonusDamage' effect. | 4 |
| `Weakness` | Number | {'type': '`Number`', 'df': "Applies the 'Weakness' effect."} | 4 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies the 'Burn' effect."} | 3 |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is hostile to the caster. | 3 |
| `Leech` | Number | {'type': '`Number`', 'df': "Applies the 'Leech' effect."} | 3 |
| `Piercing` | Number | {'type': '`Number`', 'df': "Applies the 'Piercing' effect."} | 3 |
| `Slow` | Number | {'type': '`Number`', 'df': "Applies the 'Slow' effect."} | 3 |
| [`SpreadDisease`](./Passives_and_Statuses.md#context-spreaddisease) | Block | {'type': '`Block`', 'df': 'Provides a chance to transmit a disease status to adjacent targets. | 3 |
| [`ApplyStatusIfCrit`](./Passives_and_Statuses.md#context-applystatusifcrit) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. | 2 |
| `BurgleCoin` | Number | {'type': '`Number`', 'df': "Applies the 'BurgleCoin' effect."} | 2 |
| [`ChangeTile`](./Passives_and_Statuses.md#context-changetile) | Block | {'type': '`Enum/String`', 'df': 'Transforms the terrain tile under the target.'} | 2 |
| [`Charmed`](./Arrays.md#array-charmed) | Array | {'type': 'Number', 'df': "Applies the 'Charmed' effect."} | 2 |
| [`Conditional_Adjacent`](./Passives_and_Statuses.md#context-conditional_adjacent) | Block | {'type': '`Block`', 'df': "Conditional block: Executes nested logic only if the target is/has Adjacent. | 2 |
| [`Conditional_Shielded`](./Passives_and_Statuses.md#context-conditional_shielded) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target currently has a Shield status. | 2 |
| [`Fear`](./Arrays.md#array-fear) | Array | {'type': '`Array`', 'df': "Applies the 'Fear' effect."} | 2 |
| [`Freeze`](./Arrays.md#array-freeze) | Array | {'type': '`Array`', 'df': "Applies the 'Freeze' effect."} | 2 |
| [`KnockOutCoin`](./Arrays.md#array-knockoutcoin) | Array | {'type': '`Number`', 'df': 'Forces the target to drop coins.'} | 2 |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies the 'LuckUp' effect."} | 2 |
| `Madness` | Number | {'type': '`Number`', 'df': 'Applies the Madness debuff/status effect.'} | 2 |
| `MagicWeakness` | Number | {'type': '`Number`', 'df': "Applies the 'MagicWeakness' effect."} | 2 |
| `Rot` | Number | {'type': '`Number`', 'df': "Applies the 'Rot' effect."} | 2 |
| `SoulLink` | Number | {'type': '`Number`', 'df': "Applies the 'SoulLink' effect."} | 2 |
| `SpawnBearTrapOnMiss` | Number | {'type': '`Number`', 'df': "Applies the 'SpawnBearTrapOnMiss' effect."} | 2 |
| [`Stun`](./Arrays.md#array-stun) | Array | {'type': '`Array`', 'df': "Applies the 'Stun' effect."} | 2 |
| [`ApplyToSource`](./Passives_and_Statuses.md#context-applytosource) | Block | {'type': 'Block', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target.'} | 1 |
| `BigSplashDamage` | Number | {'type': '`Number`', 'df': "Applies the 'BigSplashDamage' effect."} | 1 |
| `Blind` | Number | {'type': '`Number`', 'df': "Applies the 'Blind' effect."} | 1 |
| [`Conditional_HasTag`](./Passives_and_Statuses.md#context-conditional_hastag) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 1 |
| [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#context-conditional_sourcehastag) | Block | {'type': '`Block`', 'df': 'Conditional block: Executes nested logic only if the target is/has SourceHasTag. | 1 |
| `Confusion` | Number | {'type': '`Number`', 'df': "Applies the 'Confusion' effect."} | 1 |
| `DamageOrHealConditionally` | Number | {'type': '`Number`', 'df': 'Combat Trigger: Deals damage to or heal conditionally.'} | 1 |
| [`Else`](./Passives_and_Statuses.md#context-else) | Block | {'type': '`Block`', 'df': 'Fallback block that executes if the preceding `Conditional_` block evaluated to false.'} | 1 |
| `Leeches` | Number | {'type': '`Number`', 'df': "Applies the 'Leeches' effect."} | 1 |
| `ManaLeeches` | Number | {'type': '`Number`', 'df': "Applies the 'ManaLeeches' effect."} | 1 |
| `OverrideChainKnockback` | Number | {'type': '`Number`', 'df': "Applies the 'OverrideChainKnockback' effect."} | 1 |
| `OverrideChainKnockbackDamage` | Number | {'type': '`Number`', 'df': "Applies the 'OverrideChainKnockbackDamage' effect."} | 1 |
| `SplashDamage` | Number | {'type': '`Number`', 'df': "Applies the 'SplashDamage' effect."} | 1 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 30

> **Referenced by:** [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#context-damageneighborsaftermove), [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#context-damageneighborsonendmove), [`GravityWell`](./Passives_and_Statuses.md#context-gravitywell), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`RevengeDamage`](./Passives_and_Statuses.md#context-revengedamage), [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#context-smiteenemieswhokill), [`fire`](./Passives_and_Statuses.md#context-fire), [`ice`](./Passives_and_Statuses.md#context-ice), [`lightning`](./Passives_and_Statuses.md#context-lightning), [`triattack`](./Passives_and_Statuses.md#context-triattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'VisualFXTile' effect."} | 12 |
| [`SpreadDisease`](./Passives_and_Statuses.md#context-spreaddisease) | Block | {'type': '`Block`', 'df': 'Provides a chance to transmit a disease status to adjacent targets. | 7 |
| [`Stun`](./Arrays.md#array-stun) | Array | {'type': '`Number`', 'df': "Applies the 'Stun' effect."} | 6 |
| [`Freeze`](./Arrays.md#array-freeze) | Array | {'type': '`Array`', 'df': "Applies the 'Freeze' effect."} | 3 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies the 'Burn' effect."} | 2 |
| [`Charmed`](./Arrays.md#array-charmed) | Array | {'type': '`Array`', 'df': "Applies the 'Charmed' effect."} | 2 |
| [`Petrify`](./Arrays.md#array-petrify) | Array | {'type': '`Array`', 'df': "Applies the 'Petrify' effect."} | 2 |
| `Poison` | Number | {'type': '`Number`', 'df': "Applies the 'Poison' effect."} | 2 |
| `Slow` | Number | {'type': '`Number`', 'df': "Applies the 'Slow' effect."} | 2 |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies the 'Bleed' effect."} | 1 |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies the 'Bruise' effect."} | 1 |
| `Fear` | Number | {'type': '`Number`', 'df': "Applies the 'Fear' effect."} | 1 |
| `Immobile` | Number | {'type': '`Number`', 'df': "Applies the 'Immobile' effect."} | 1 |
| `Leeches` | Number | {'type': '`Number`', 'df': "Applies the 'Leeches' effect."} | 1 |
| `Madness` | Number | {'type': '`Number`', 'df': 'Applies the Madness debuff/status effect.'} | 1 |
| `Marked` | Number | {'type': '`Number`', 'df': "Applies the 'Marked' effect."} | 1 |
| `Weakness` | Number | {'type': '`Number`', 'df': "Applies the 'Weakness' effect."} | 1 |

</details>

---

### Context: `AddPassivesToMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 29

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack) | Block | {'type': '`Block`', 'df': "Injects a status effect payload that applies whenever the character performs a basic attack. | 5 |
| `DamageUp` | Number | {'type': 'Number', 'df': 'Combat Trigger: Deals damage to up.'} | 4 |
| `IncreaseExplosionDamage` | Number | {'type': '`Number`', 'df': "Applies the 'IncreaseExplosionDamage' effect."} | 4 |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'FreePathfindElement' effect."} | 3 |
| `AddMaxHealth` | Number | {'type': '`Number`', 'df': "Applies the 'AddMaxHealth' effect."} | 2 |
| `AddSpeed` | Number | {'type': '`Number`', 'df': "Applies the 'AddSpeed' effect."} | 2 |
| [`AddStatusToExplosions`](./Passives_and_Statuses.md#context-addstatustoexplosions) | Block | {'type': '`Block`', 'df': "Applies the 'AddStatusToExplosions' effect. | 2 |
| [`EMP`](./Passives_and_Statuses.md#context-emp) | Block | {'type': '`Block`', 'df': "Applies the 'EMP' effect. | 2 |
| [`FamiliarBonusAbility`](./Enums.md#enum-familiarbonusability) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'FamiliarBonusAbility' effect."} | 2 |
| `ForceAttack` | Number | {'type': '`Number`', 'df': 'Forces the character to execute an immediate attack.'} | 2 |
| `HealthGain` | Number | {'type': 'Number', 'df': "Applies the 'HealthGain' effect."} | 2 |
| `HealthRegenUp` | Number | {'type': '`Number`', 'df': "Applies the 'HealthRegenUp' effect."} | 2 |
| `HolyShieldTransferToSpawner` | Number | {'type': '`Number`', 'df': "Applies the 'HolyShieldTransferToSpawner' effect."} | 2 |
| `IncreaseExplosionSize` | Number | {'type': '`Number`', 'df': "Applies the 'IncreaseExplosionSize' effect."} | 2 |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement) | Block | {'type': '`Block`', 'df': 'State Trigger: Grants nested passives when affected by element. | 2 |
| `PoisonThorns` | Number | {'type': '`Number`', 'df': "Applies the 'PoisonThorns' effect."} | 2 |
| [`StatusAlliesOnKill`](./Passives_and_Statuses.md#context-statusalliesonkill) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to allies on kill. | 2 |
| [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when kill. | 2 |
| `WaterWalk` | Number | {'type': '`Number`', 'df': "Applies the 'WaterWalk' effect."} | 2 |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| `AddUnfilledMaxHealth` | Number | {'type': '`Number`', 'df': "Applies the 'AddUnfilledMaxHealth' effect."} | 1 |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies the 'DivineShield' effect."} | 1 |
| `GrassTileHealing` | Number | {'type': '`Number`', 'df': "Applies the 'GrassTileHealing' effect."} | 1 |
| `Quivered` | Number | {'type': '`Number`', 'df': "Applies the 'Quivered' effect."} | 1 |
| `SafeExplosions` | Number | {'type': '`Number`', 'df': "Applies the 'SafeExplosions' effect."} | 1 |
| `TakeExtraTurn` | Number | {'type': '`Number`', 'df': "Applies the 'TakeExtraTurn' effect."} | 1 |
| `UncappedHP` | Number | {'type': '`Number`', 'df': "Applies the 'UncappedHP' effect."} | 1 |

</details>

---

### Context: `SpawnOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array | {'type': '`Enum/String`', 'df': ''} | 14 |
| [`number`](./Arrays.md#array-number) | Array | {'type': '`Number`', 'df': ''} | 13 |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies the 'SpeedUp' effect."} | 3 |
| [`Temporary`](./Passives_and_Statuses.md#context-temporary) | Block | {'type': '`Block`', 'df': 'A wrapper block for applying status effects that automatically expire. | 3 |
| `ConstitutionUp` | Number | {'type': 'Number', 'df': "Applies the 'ConstitutionUp' effect."} | 2 |
| [`Craft`](./Passives_and_Statuses.md#context-craft) | Block | {'type': '`Block`', 'df': 'Synthesizes or spawns a new item from a specific pool. | 2 |
| `DamageUp` | Number | {'type': '`Number`', 'df': 'Combat Trigger: Deals damage to up.'} | 2 |
| `IntelligenceUp` | Number | {'type': '`Number`', 'df': "Applies the 'IntelligenceUp' effect."} | 2 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies the 'Shield' effect."} | 2 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies the 'StrengthUp' effect."} | 2 |
| `TempDamageUp` | Number | {'type': '`Number`', 'df': "Applies the 'TempDamageUp' effect."} | 2 |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#context-conditional_hasstatus) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 1 |
| `DiminishingHealthRegen` | Number | {'type': 'Number', 'df': "Applies the 'DiminishingHealthRegen' effect."} | 1 |
| [`Else`](./Passives_and_Statuses.md#context-else) | Block | {'type': '`Block`', 'df': "Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |
| `MovementUp` | Number | {'type': '`Number`', 'df': "Applies the 'MovementUp' effect."} | 1 |
| `RandomInjury` | Number | {'type': '`Number`', 'df': "Applies the 'RandomInjury' effect."} | 1 |
| `RandomStatUp` | Number | {'type': '`Number`', 'df': "Applies the 'RandomStatUp' effect."} | 1 |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool) | Block | {'type': '`Block`', 'df': "Selects and applies a random status effect from the provided nested block. | 1 |
| `TempMovement` | Number | {'type': '`Number`', 'df': "Applies the 'TempMovement' effect."} | 1 |
| `Thorns` | Number | {'type': '`Number`', 'df': "Applies the 'Thorns' effect."} | 1 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Passives_and_Statuses.md#context-forceuseability) | Block | {'type': '`Enum/String`', 'df': "Applies the 'ForceUseAbility' effect."} | 6 |
| `NonStackingDivineShield` | Number | {'type': '`Number`', 'df': "Applies the 'NonStackingDivineShield' effect."} | 4 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies the 'SpeedUp' effect."} | 4 |
| `EmptyMana` | Number | {'type': '`Number`', 'df': "Applies the 'EmptyMana' effect."} | 2 |
| `RangeUp` | Number | {'type': '`Number`', 'df': "Applies the 'RangeUp' effect."} | 2 |
| `IntelligenceUp` | Number | {'type': '`Number`', 'df': "Applies the 'IntelligenceUp' effect."} | 1 |
| `KineticSpikes` | Number | {'type': '`Number`', 'df': "Applies the 'KineticSpikes' effect."} | 1 |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#context-objectonhitcharacter) | Block | {'type': '`Block`', 'df': 'Spawns a specific character or entity upon impact. | 1 |
| `PermanentMadness` | Number | {'type': '`Number`', 'df': "Applies the 'PermanentMadness' effect."} | 1 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies the 'StrengthUp' effect."} | 1 |
| [`UseAbility_Madness`](./Enums.md#enum-useability_madness) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'UseAbility_Madness' effect."} | 1 |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | {'type': '`Boolean`', 'df': 'If true, triggers the effect even if the character died during the battle.'} | 10 |
| [`CureDisease`](./Passives_and_Statuses.md#context-curedisease) | Block | {'type': '`Block`', 'df': "Applies the 'CureDisease' effect. | 6 |
| [`FindItemFromPool`](./Passives_and_Statuses.md#context-finditemfrompool) | Block | {'type': '`Enum/String`', 'df': 'Generates an item drop from the specified loot pool.'} | 3 |
| `RandomPermanentStat` | Number | {'type': '`Number`', 'df': "Applies the 'RandomPermanentStat' effect."} | 3 |
| [`NextBattleStatus`](./Passives_and_Statuses.md#context-nextbattlestatus) | Block | {'type': '`Block`', 'df': "Applies the 'NextBattleStatus' effect. | 2 |
| `PermanentSpeed` | Number | {'type': '`Number`', 'df': "Applies the 'PermanentSpeed' effect."} | 2 |
| `RandomMutation` | Number | {'type': '`Number`', 'df': "Applies the 'RandomMutation' effect."} | 2 |
| `PermanentConstitution` | Number | {'type': '`Number`', 'df': "Applies the 'PermanentConstitution' effect."} | 1 |
| `PermanentIntelligence` | Number | {'type': '`Number`', 'df': "Applies the 'PermanentIntelligence' effect."} | 1 |
| `PermanentStrength` | Number | {'type': '`Number`', 'df': "Applies the 'PermanentStrength' effect."} | 1 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_FirstApplicationThisTurn`](./Passives_and_Statuses.md#context-conditional_firstapplicationthisturn) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 2 |
| `DamageUp` | Number | {'type': '`Number`', 'df': 'Combat Trigger: Deals damage to up.'} | 2 |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'EquipPermanentItem' effect."} | 2 |
| `RefreshActPoints` | Number | {'type': '`Number`', 'df': "Applies the 'RefreshActPoints' effect."} | 2 |
| `RefreshMovePoints` | Number | {'type': '`Number`', 'df': "Applies the 'RefreshMovePoints' effect."} | 2 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies the 'StrengthUp' effect."} | 2 |
| `AllStatsUp` | Number | {'type': 'Number', 'df': "Applies the 'AllStatsUp' effect."} | 1 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies the 'HealthGain' effect."} | 1 |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies the 'LuckUp' effect."} | 1 |
| `RandomStatUp` | Number | {'type': '`Number`', 'df': "Applies the 'RandomStatUp' effect."} | 1 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies the 'SpeedUp' effect."} | 1 |
| `Stealth` | Number | {'type': '`Number`', 'df': "Applies the 'Stealth' effect."} | 1 |
| [`TakeBonusTurnWithStatus`](./Passives_and_Statuses.md#context-takebonusturnwithstatus) | Block | {'type': '`Block`', 'df': 'Grants the character an immediate extra turn while afflicted with specific statuses. | 1 |

</details>

---

### Context: `lock_item_slot`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum | {'type': '`Enum/String`', 'df': ''} | 16 |
| `frame` | Number | {'type': '`Number`', 'df': ''} | 3 |

</details>

---

### Context: `StatusOnStanceSwitch`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#context-passiveifemptyface), [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#context-passiveifemptyhead), [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#context-passiveifemptyneck), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | {'type': '`Number`', 'df': 'Fires a randomized number of magic missiles.'} | 6 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'ForceUseAbility' effect."} | 2 |
| `NextBasicAttackCritsThisTurn` | Number | {'type': '`Number`', 'df': 'Guarantees the next basic attack executed this turn will be a critical hit.'} | 2 |
| `RandomStatUp` | Number | {'type': '`Number`', 'df': "Applies the 'RandomStatUp' effect."} | 2 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies the 'Shield' effect."} | 2 |
| `PartialCleanse` | Number | {'type': '`Number`', 'df': "Applies the 'PartialCleanse' effect."} | 1 |

</details>

---

### Context: `SpreadDisease`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`effects`](./Passives_and_Statuses.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`disease`](./Enums.md#enum-disease) | Enum | {'type': '`Enum/String`', 'df': 'The specific status effect ID representing the disease.'} | 12 |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of transmitting.'} | 11 |
| `can_apply_to_anything` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_BadRoll`](./Passives_and_Statuses.md#context-conditional_badroll) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic based on a randomized bad outcome probability. | 3 |
| [`FillMana`](./Arrays.md#array-fillmana) | Array | {'type': '`Array`', 'df': "Applies the 'FillMana' effect."} | 2 |
| `IntelligenceUp` | Number | {'type': '`Number`', 'df': "Applies the 'IntelligenceUp' effect."} | 2 |
| `RandomStatUp` | Number | {'type': '`Number`', 'df': "Applies the 'RandomStatUp' effect."} | 2 |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#context-conditional_goodroll) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 1 |
| [`Fear`](./Arrays.md#array-fear) | Array | {'type': '`Array`', 'df': "Applies the 'Fear' effect."} | 1 |
| [`ForceUseAbility`](./Passives_and_Statuses.md#context-forceuseability) | Block | {'type': '`Block`', 'df': "Applies the 'ForceUseAbility' effect. | 1 |

</details>

---

### Context: `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#context-conditional_sourcehastag), [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#context-extrastatuswhendealingdamage), [`StatusKilledCharacters`](./Passives_and_Statuses.md#context-statuskilledcharacters)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array | {'type': 'Number', 'df': "Applies the 'AllStatsUp' effect."} | 2 |
| `Cleanse` | Number | {'type': '`Number`', 'df': "Applies the 'Cleanse' effect."} | 2 |
| `ClearNegativeEffects` | Number | {'type': '`Number`', 'df': "Applies the 'ClearNegativeEffects' effect."} | 2 |
| `DamageUp` | Number | {'type': '`Number`', 'df': 'Combat Trigger: Deals damage to up.'} | 2 |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool) | Block | {'type': '`Block`', 'df': "Selects and applies a random status effect from the provided nested block. | 2 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies the 'Shield' effect."} | 2 |
| `TempSpeedUp` | Number | {'type': '`Number`', 'df': "Applies the 'TempSpeedUp' effect."} | 2 |
| [`ApplyToSource`](./Passives_and_Statuses.md#context-applytosource) | Block | {'type': '`Block`', 'df': "Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies the 'SpeedUp' effect."} | 1 |

</details>

---

### Context: `CritsApplyStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum | {'type': '`Enum/String`', 'df': 'Spawns a specific character or entity upon impact.'} | 5 |
| [`Stun`](./Arrays.md#array-stun) | Array | {'type': '`Number`', 'df': "Applies the 'Stun' effect."} | 3 |
| `Weakness` | Number | {'type': '`Number`', 'df': "Applies the 'Weakness' effect."} | 3 |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#context-conditional_hasstatus) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 2 |
| [`Else`](./Passives_and_Statuses.md#context-else) | Block | {'type': '`Block`', 'df': "Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 2 |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies the 'Bleed' effect."} | 1 |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies the 'Bruise' effect."} | 1 |
| `Confusion` | Number | {'type': '`Number`', 'df': "Applies the 'Confusion' effect."} | 1 |
| `Immobile` | Number | {'type': '`Number`', 'df': "Applies the 'Immobile' effect."} | 1 |

</details>

---

### Context: `Temporary`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`Conditional_BadRoll`](./Passives_and_Statuses.md#context-conditional_badroll), [`StatusOnGainShield`](./Passives_and_Statuses.md#context-statusongainshield), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage), [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#context-statusonturnendifmanaorhealthexact)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 11 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The status effect to apply.'} | 11 |
| `turns` | Number | {'type': '`Number`', 'df': 'Duration in turns.'} | 8 |
| `expires_on_end_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| `expires_on_begin_turn` | Boolean | {'type': '`Boolean`', 'df': 'If true, ticks down at the start of the turn rather than the end.'} | 5 |

</details>

---

### Context: `PassiveAtStatThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum | {'type': '`Enum/String`', 'df': ''} | 10 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block | {'type': '`Block`', 'df': " | 10 |
| [`threshold`](./Passives_and_Statuses.md#context-threshold) | Block | {'type': '`Block`', 'df': ' | 10 |

</details>

---

### Context: `threshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number | {'type': '`Number`', 'df': ''} | 6 |
| `cha` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `spd` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | {'type': '`Block`', 'df': "Non-damaging status applications and logic triggers executed on impact. | 8 |
| `knockback` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | {'type': '`Block`', 'df': "Non-damaging status applications and logic triggers executed on impact. | 7 |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 4 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 4 |
| `Poison` | Number | {'type': 'Number', 'df': "Applies the 'Poison' effect."} | 1 |
| [`SpreadDisease`](./Passives_and_Statuses.md#context-spreaddisease) | Block | {'type': 'Block', 'df': 'Provides a chance to transmit a disease status to adjacent targets.'} | 1 |
| `Weakness` | Number | {'type': 'Number', 'df': "Applies the 'Weakness' effect."} | 1 |

</details>

---

### Context: `PassiveIfAllArmorEmpty`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddSpellDamage` | Number | {'type': '`Number`', 'df': "Applies the 'AddSpellDamage' effect."} | 2 |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'CounterAttack' effect."} | 2 |
| `ExtraMovePoints` | Number | {'type': '`Number`', 'df': "Applies the 'ExtraMovePoints' effect."} | 2 |
| `ManaCostReduction` | Number | {'type': '`Number`', 'df': "Applies the 'ManaCostReduction' effect."} | 2 |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when stance switch. | 2 |
| [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus) | Block | {'type': '`Block`', 'df': "Applies the 'CritsApplyStatus' effect. | 1 |
| `Flying` | Number | {'type': '`Number`', 'df': "Applies the 'Flying' effect."} | 1 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`StatusOnGainCoins`](./Passives_and_Statuses.md#context-statusongaincoins), [`StatusOnHealed`](./Passives_and_Statuses.md#context-statusonhealed), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 3 |
| [`StatusGroup`](./Passives_and_Statuses.md#context-statusgroup) | Block | {'type': '`Block`', 'df': "Groups multiple status effects together for batch application. | 3 |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies the 'Bleed' effect."} | 2 |
| `BleedThorns` | Number | {'type': '`Number`', 'df': "Applies the 'BleedThorns' effect."} | 2 |
| `Blind` | Number | {'type': '`Number`', 'df': "Applies the 'Blind' effect."} | 2 |
| `Brace` | Number | {'type': '`Number`', 'df': "Applies the 'Brace' effect."} | 2 |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies the 'Bruise' effect."} | 2 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies the 'Burn' effect."} | 2 |
| `Charge` | Number | {'type': '`Number`', 'df': "Applies the 'Charge' effect."} | 2 |
| `Charmed` | Number | {'type': '`Number`', 'df': "Applies the 'Charmed' effect."} | 2 |
| `Confusion` | Number | {'type': '`Number`', 'df': "Applies the 'Confusion' effect."} | 2 |
| `DiminishingHealthRegen` | Number | {'type': '`Number`', 'df': "Applies the 'DiminishingHealthRegen' effect."} | 2 |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies the 'DivineShield' effect."} | 2 |
| `Fear` | Number | {'type': '`Number`', 'df': "Applies the 'Fear' effect."} | 2 |
| `Freeze` | Number | {'type': '`Number`', 'df': "Applies the 'Freeze' effect."} | 2 |
| `Immobile` | Number | {'type': '`Number`', 'df': "Applies the 'Immobile' effect."} | 2 |
| `KineticSpikes` | Number | {'type': '`Number`', 'df': "Applies the 'KineticSpikes' effect."} | 2 |
| `Madness` | Number | {'type': '`Number`', 'df': 'Applies the Madness debuff/status effect.'} | 2 |
| `MagicWeakness` | Number | {'type': '`Number`', 'df': "Applies the 'MagicWeakness' effect."} | 2 |
| `Marked` | Number | {'type': '`Number`', 'df': "Applies the 'Marked' effect."} | 2 |
| `MoveQuivered` | Number | {'type': '`Number`', 'df': "Applies the 'MoveQuivered' effect."} | 2 |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum | {'type': '`Enum/String`', 'df': 'Spawns a specific character or entity upon impact.'} | 2 |
| `Petrify` | Number | {'type': '`Number`', 'df': "Applies the 'Petrify' effect."} | 2 |
| `Poison` | Number | {'type': '`Number`', 'df': "Applies the 'Poison' effect."} | 2 |
| `Quivered` | Number | {'type': '`Number`', 'df': "Applies the 'Quivered' effect."} | 2 |
| `Reflect` | Number | {'type': '`Number`', 'df': "Applies the 'Reflect' effect."} | 2 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies the 'Shield' effect."} | 2 |
| `Sleep` | Number | {'type': '`Number`', 'df': "Applies the 'Sleep' effect."} | 2 |
| `Slow` | Number | {'type': '`Number`', 'df': "Applies the 'Slow' effect."} | 2 |
| `Stun` | Number | {'type': '`Number`', 'df': "Applies the 'Stun' effect."} | 2 |
| `Tarred` | Number | {'type': '`Number`', 'df': "Applies the 'Tarred' effect."} | 2 |
| `Thorns` | Number | {'type': '`Number`', 'df': "Applies the 'Thorns' effect."} | 2 |
| `Weakness` | Number | {'type': '`Number`', 'df': "Applies the 'Weakness' effect."} | 2 |
| `ConstitutionUp` | Number | {'type': '`Number`', 'df': "Applies the 'ConstitutionUp' effect."} | 1 |
| `SpawnCoinAnywhere` | Number | {'type': 'Number', 'df': "Applies the 'SpawnCoinAnywhere' effect."} | 1 |
| `SpeedUp` | Number | {'type': 'Number', 'df': "Applies the 'SpeedUp' effect."} | 1 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies the 'StrengthUp' effect."} | 1 |

</details>

---

### Context: `StatusOnCrit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies the 'LuckUp' effect."} | 3 |
| `DamageUp` | Number | {'type': '`Number`', 'df': 'Combat Trigger: Deals damage to up.'} | 2 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies the 'Shield' effect."} | 2 |
| `CritChanceUp` | Number | {'type': '`Number`', 'df': "Applies the 'CritChanceUp' effect."} | 1 |
| `RandomStatUp` | Number | {'type': '`Number`', 'df': "Applies the 'RandomStatUp' effect."} | 1 |

</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_NotBoss`](./Passives_and_Statuses.md#context-conditional_notboss)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | {'type': 'Number', 'df': "Applies the 'Confusion' effect."} | 3 |
| [`Conditional_PartyMember`](./Passives_and_Statuses.md#context-conditional_partymember) | Block | {'type': '`Block`', 'df': "Conditional block: Executes nested logic only if the target is/has PartyMember. | 2 |
| [`Else`](./Passives_and_Statuses.md#context-else) | Block | {'type': '`Block`', 'df': "Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 2 |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool) | Block | {'type': '`Block`', 'df': "Selects and applies a random status effect from the provided nested block. | 2 |
| [`Stun`](./Arrays.md#array-stun) | Array | {'type': '`Array`', 'df': "Applies the 'Stun' effect."} | 1 |

</details>

---

### Context: `DamageNeighborsOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 7 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 7 |
| `cant_miss` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | {'type': '`Block`', 'df': "Non-damaging status applications and logic triggers executed on impact. | 6 |
| `knockback` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `ForceUseAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin), [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 3 |
| `chance` | Mixed | {'type': '`Enum/String`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 3 |

</details>

---

### Context: `PassiveIfEmptyFace`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | {'type': '`Number`', 'df': "Applies the 'AddCritMultiplier' effect."} | 2 |
| `CritChanceUp` | Number | {'type': '`Number`', 'df': "Applies the 'CritChanceUp' effect."} | 2 |
| `DodgeChance` | Number | {'type': '`Number`', 'df': "Applies the 'DodgeChance' effect."} | 2 |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when stance switch. | 2 |
| `KineticSpikes` | Number | {'type': '`Number`', 'df': "Applies the 'KineticSpikes' effect."} | 1 |

</details>

---

### Context: `PassiveIfEmptyHead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | {'type': '`Number`', 'df': "Applies the 'AddCritMultiplier' effect."} | 2 |
| `CritChanceUp` | Number | {'type': '`Number`', 'df': "Applies the 'CritChanceUp' effect."} | 2 |
| `DodgeChance` | Number | {'type': '`Number`', 'df': "Applies the 'DodgeChance' effect."} | 2 |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when stance switch. | 2 |
| `KineticSpikes` | Number | {'type': '`Number`', 'df': "Applies the 'KineticSpikes' effect."} | 1 |

</details>

---

### Context: `PassiveIfEmptyNeck`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | {'type': '`Number`', 'df': "Applies the 'AddCritMultiplier' effect."} | 2 |
| `CritChanceUp` | Number | {'type': '`Number`', 'df': "Applies the 'CritChanceUp' effect."} | 2 |
| `DodgeChance` | Number | {'type': '`Number`', 'df': "Applies the 'DodgeChance' effect."} | 2 |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses when stance switch. | 2 |
| `KineticSpikes` | Number | {'type': '`Number`', 'df': "Applies the 'KineticSpikes' effect."} | 1 |

</details>

---

### Context: `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 2 |
| `HealAndOverhealToShield` | Number | {'type': '`Number`', 'df': "Applies the 'HealAndOverhealToShield' effect."} | 2 |
| `Reanimate` | Number | {'type': '`Number`', 'df': "Applies the 'Reanimate' effect."} | 2 |
| `TakeExtraTurn` | Number | {'type': '`Number`', 'df': "Applies the 'TakeExtraTurn' effect."} | 2 |
| `triggers_limit` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `Freeze` | Number | {'type': '`Number`', 'df': "Applies the 'Freeze' effect."} | 1 |
| `FullHeal` | Number | {'type': '`Number`', 'df': "Applies the 'FullHeal' effect."} | 1 |

</details>

---

### Context: `StatusOnUseAbilityWithTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The specific entity tag required or applied.'} | 7 |
| `RefreshActPoints` | Number | {'type': '`Number`', 'df': "Applies the 'RefreshActPoints' effect."} | 3 |
| [`Conditional_FirstApplicationThisTurn`](./Passives_and_Statuses.md#context-conditional_firstapplicationthisturn) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 2 |
| `DamageUp` | Number | {'type': '`Number`', 'df': 'Combat Trigger: Deals damage to up.'} | 2 |
| `exclude_basicattack` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies the 'HealthGain' effect."} | 1 |
| `RandomStatUp` | Number | {'type': '`Number`', 'df': "Applies the 'RandomStatUp' effect."} | 1 |

</details>

---

### Context: `AddStatusToElementAbilities`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'The specific element type required or applied.'} | 6 |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum | {'type': '`Enum/String`', 'df': 'Transforms the terrain tile under the target.'} | 2 |
| [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is friendly to the caster. | 2 |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is hostile to the caster. | 2 |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies the 'Bleed' effect."} | 1 |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies the 'Bleed' effect."} | 2 |
| `PullSourceToKnockbackImmuneTarget` | Number | {'type': '`Number`', 'df': "Applies the 'PullSourceToKnockbackImmuneTarget' effect."} | 2 |
| `Cleave` | Number | {'type': '`Number`', 'df': 'Causes the attack to hit adjacent enemies alongside the primary target.'} | 1 |
| `LeechPercent` | Number | {'type': '`Number`', 'df': "Applies the 'LeechPercent' effect."} | 1 |

</details>

---

### Context: `CureDisease`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 6 |
| [`disease`](./Enums.md#enum-disease) | Enum | {'type': '`Enum/String`', 'df': ''} | 6 |
| `can_apply_to_anything` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Number | {'type': '`Number`', 'df': "Applies the 'CaptureFamiliar' effect."} | 2 |
| `FactionConversion` | Number | {'type': '`Number`', 'df': "Applies the 'FactionConversion' effect."} | 2 |
| `Marked` | Number | {'type': '`Number`', 'df': "Applies the 'Marked' effect."} | 2 |
| `PermanentCharm` | Number | {'type': '`Number`', 'df': "Applies the 'PermanentCharm' effect."} | 2 |
| `Fear` | Number | {'type': '`Number`', 'df': "Applies the 'Fear' effect."} | 1 |
| `TempSpeedUp` | Number | {'type': '`Number`', 'df': "Applies the 'TempSpeedUp' effect."} | 1 |

</details>

---

### Context: `ManaCostReductionTagged`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reduction` | Number | {'type': '`Number`', 'df': ''} | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The specific entity tag required or applied.'} | 6 |

</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array | {'type': '`Enum/String`', 'df': ''} | 6 |
| `chance` | Mixed | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 5 |
| `number` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `good` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 6 |
| `good` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| `spawn_on_death_hit` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `consider_all_layers` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Weakness` | Number | {'type': '`Number`', 'df': "Applies the 'Weakness' effect."} | 1 |

</details>

---

### Context: `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LeaveBehindRockOnKnockback` | Number | {'type': '`Number`', 'df': "Applies the 'LeaveBehindRockOnKnockback' effect."} | 2 |
| `Blind` | Number | {'type': '`Number`', 'df': "Applies the 'Blind' effect."} | 1 |
| [`Conditional_HasTag`](./Passives_and_Statuses.md#context-conditional_hastag) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 1 |
| `NonLethal` | Number | {'type': '`Number`', 'df': "Applies the 'NonLethal' effect."} | 1 |

</details>

---

### Context: `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | {'type': '`Number`', 'df': "Applies the 'Confusion' effect."} | 3 |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies the 'Bruise' effect."} | 2 |
| `FaceAway` | Number | {'type': '`Number`', 'df': "Applies the 'FaceAway' effect."} | 2 |
| [`Stun`](./Arrays.md#array-stun) | Array | {'type': '`Array`', 'df': "Applies the 'Stun' effect."} | 2 |
| [`SpreadDisease`](./Passives_and_Statuses.md#context-spreaddisease) | Block | {'type': '`Block`', 'df': 'Provides a chance to transmit a disease status to adjacent targets. | 1 |

</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | {'type': '`Number`', 'df': "Applies the 'Charge' effect."} | 2 |
| `CurrentWeaponDamageUp` | Number | {'type': '`Number`', 'df': "Applies the 'CurrentWeaponDamageUp' effect."} | 2 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies the 'HealthGain' effect."} | 1 |

</details>

---

### Context: `StatusOnOverHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility_NonStack`](./Enums.md#enum-forceuseability_nonstack) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'ForceUseAbility_NonStack' effect."} | 2 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies the 'StrengthUp' effect."} | 2 |
| `CurrentWeaponDamageUp` | Number | {'type': '`Number`', 'df': "Applies the 'CurrentWeaponDamageUp' effect."} | 1 |
| `SpawnScaledRotFly` | Number | {'type': '`Number`', 'df': "Applies the 'SpawnScaledRotFly' effect."} | 1 |

</details>

---

### Context: `AddDamageToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 4 |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'The specific element type required or applied.'} | 4 |

</details>

---

### Context: `AddPassivesToCharmed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack) | Block | {'type': '`Block`', 'df': "Injects a status effect payload that applies whenever the character performs a basic attack. | 5 |
| `AddMaxHealth` | Number | {'type': '`Number`', 'df': "Applies the 'AddMaxHealth' effect."} | 2 |
| `AddSpeed` | Number | {'type': '`Number`', 'df': "Applies the 'AddSpeed' effect."} | 2 |
| `DamageUp` | Number | {'type': '`Number`', 'df': 'Combat Trigger: Deals damage to up.'} | 2 |

</details>

---

### Context: `AddStatusToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'The specific element type required or applied.'} | 4 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies the 'Burn' effect."} | 2 |
| [`Conditional_Corpse`](./Passives_and_Statuses.md#context-conditional_corpse) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 2 |

</details>

---

### Context: `AddStatusToExplosions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddElement`](./Enums.md#enum-addelement) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'AddElement' effect."} | 8 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies the 'Burn' effect."} | 4 |

</details>

---

### Context: `AllyBonusAbilityAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 2 |
| `square` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `AllyManaRegenAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum | {'type': '`Enum/String`', 'df': 'Distance or area of effect in tiles.'} | 4 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 4 |

</details>

---

### Context: `AmplifyStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `addstacks` | Number | {'type': '`Number`', 'df': ''} | 3 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the status effect to check or apply.'} | 3 |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to autocast.'} | 4 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': 'If true, bypasses stun and hard-CC restrictions to cast anyway.'} | 2 |
| `force_display_name` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill), [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#context-statusonuseabilitywithtag)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TakeExtraTurn` | Number | {'type': '`Number`', 'df': "Applies the 'TakeExtraTurn' effect."} | 2 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 1 |
| `FillMana` | Number | {'type': '`Number`', 'df': "Applies the 'FillMana' effect."} | 1 |
| `ManaGain` | Number | {'type': '`Number`', 'df': "Applies the 'ManaGain' effect."} | 1 |

</details>

---

### Context: `DistanceBonusDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `min_range` | Number | {'type': '`Number`', 'df': ''} | 4 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 4 |

</details>

---

### Context: `EMP`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`spell_graphics_override`](./Passives_and_Statuses.md#context-spell_graphics_override) | Block | {'type': '`Block`', 'df': ' | 4 |
| [`status_explosion_override`](./Enums.md#enum-status_explosion_override) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |

</details>

---

### Context: `PassiveAtHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block | {'type': '`Block`', 'df': " | 4 |
| `threshold` | Number | {'type': '`Number`', 'df': ''} | 4 |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'The specific element type required or applied.'} | 4 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block | {'type': '`Block`', 'df': " | 4 |

</details>

---

### Context: `PassiveWhenAtFullMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack) | Block | {'type': '`Block`', 'df': "Injects a status effect payload that applies whenever the character performs a basic attack. | 2 |
| `Brace` | Number | {'type': '`Number`', 'df': "Applies the 'Brace' effect."} | 2 |
| `Flying` | Number | {'type': '`Number`', 'df': "Applies the 'Flying' effect."} | 2 |
| `AddMovement` | Number | {'type': '`Number`', 'df': "Applies the 'AddMovement' effect."} | 1 |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'ReplaceBasicMove' effect."} | 1 |

</details>

---

### Context: `StatusAlliesOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 2 |
| `DamageUp` | Number | {'type': '`Number`', 'df': 'Combat Trigger: Deals damage to up.'} | 2 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies the 'HealthGain' effect."} | 1 |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies the 'HealthGain' effect."} | 2 |
| `MoveQuivered` | Number | {'type': '`Number`', 'df': "Applies the 'MoveQuivered' effect."} | 2 |
| `Brace` | Number | {'type': '`Number`', 'df': "Applies the 'Brace' effect."} | 1 |
| `ConstitutionUp` | Number | {'type': '`Number`', 'df': "Applies the 'ConstitutionUp' effect."} | 1 |
| `ManaGain` | Number | {'type': '`Number`', 'df': "Applies the 'ManaGain' effect."} | 1 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies the 'Shield' effect."} | 1 |

</details>

---

### Context: `StatusOnTurnEndIfCastNSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spells` | Number | {'type': '`Number`', 'df': ''} | 4 |
| `DoubleCastSpell` | Number | {'type': '`Number`', 'df': "Applies the 'DoubleCastSpell' effect."} | 2 |
| `Quivered` | Number | {'type': '`Number`', 'df': "Applies the 'Quivered' effect."} | 2 |
| `MoveQuivered` | Number | {'type': '`Number`', 'df': "Applies the 'MoveQuivered' effect."} | 1 |

</details>

---

### Context: `StatusOnTurnEndIfManaExact`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `mana` | Number | {'type': '`Number`', 'df': ''} | 4 |
| `FreeSpell` | Number | {'type': '`Number`', 'df': "Applies the 'FreeSpell' effect."} | 2 |
| `Quivered` | Number | {'type': '`Number`', 'df': "Applies the 'Quivered' effect."} | 2 |
| `MoveQuivered` | Number | {'type': '`Number`', 'df': "Applies the 'MoveQuivered' effect."} | 1 |
| `SpellDamageUp` | Number | {'type': '`Number`', 'df': "Applies the 'SpellDamageUp' effect."} | 1 |

</details>

---

### Context: `StatusOnTurnEndIfManaOrHealthExact`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `mana` | Number | {'type': '`Number`', 'df': ''} | 4 |
| [`Temporary`](./Passives_and_Statuses.md#context-temporary) | Block | {'type': '`Block`', 'df': 'A wrapper block for applying status effects that automatically expire. | 3 |
| `IntelligenceUp` | Number | {'type': '`Number`', 'df': "Applies the 'IntelligenceUp' effect."} | 2 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies the 'Shield' effect."} | 2 |
| `SpellDamageUp` | Number | {'type': '`Number`', 'df': "Applies the 'SpellDamageUp' effect."} | 2 |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies the 'DivineShield' effect."} | 1 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies the 'HealthGain' effect."} | 1 |
| `KineticSpikes` | Number | {'type': '`Number`', 'df': "Applies the 'KineticSpikes' effect."} | 1 |

</details>

---

### Context: `empty_armor_scaled_stats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `int` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `spd` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `spell_graphics_override`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`EMP`](./Passives_and_Statuses.md#context-emp)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |
| `palette` | Number | {'type': '`Number`', 'df': ''} | 4 |
| [`particle`](./Enums.md#enum-particle) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |

</details>

---

### Context: `AbilityReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 1 |
| `ability_damage_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `chance` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 1 |

</details>

---

### Context: `AddSelfStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | {'type': '`Number`', 'df': 'Fires a randomized number of magic missiles.'} | 7 |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | {'type': '`Number`', 'df': "Applies the 'CastAgain' effect."} | 2 |
| `Fury` | Number | {'type': '`Number`', 'df': "Applies the 'Fury' effect."} | 1 |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Temporary`](./Passives_and_Statuses.md#context-temporary) | Block | {'type': '`Block`', 'df': 'A wrapper block for applying status effects that automatically expire. | 3 |
| [`odds`](./Enums.md#enum-odds) | Enum | {'type': '`Enum/String`', 'df': "The probability (0.0 to 1.0) of triggering the 'bad roll' failure state."} | 3 |

</details>

---

### Context: `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The specific status ID to check for.'} | 3 |

</details>

---

### Context: `DeathRattle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 2 |
| `pop_corpse` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `ElementalManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array | {'type': '`Enum/String`', 'df': 'The specific element type required or applied.'} | 3 |
| `reduction` | Number | {'type': '`Number`', 'df': ''} | 3 |

</details>

---

### Context: `FindItemFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | {'type': '`Enum/String`', 'df': 'Probability of finding the item.'} | 1 |
| [`pool`](./Enums.md#enum-pool) | Enum | {'type': '`Enum/String`', 'df': 'The item pool to draw from.'} | 1 |

</details>

---

### Context: `MoveTowardsDamageSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| `move_far` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |

</details>

---

### Context: `ObjectOnHitCharacter`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend), [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#context-statuseachturnendperenemykill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': 'The entity ID of the character to spawn (e.g., CharmedFlea).'} | 3 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 3 |

</details>

---

### Context: `SpawnCatCopyOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array | {'type': '`Array`', 'df': ''} | 3 |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |

</details>

---

### Context: `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 3 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 2 |
| `SpellDamageUp` | Number | {'type': '`Number`', 'df': "Applies the 'SpellDamageUp' effect."} | 2 |
| `ReduceManaCost` | Number | {'type': '`Number`', 'df': "Applies the 'ReduceManaCost' effect."} | 1 |
| `RepairWeapon` | Number | {'type': '`Number`', 'df': "Applies the 'RepairWeapon' effect."} | 1 |
| `RepairWeaponCondition` | Number | {'type': '`Number`', 'df': "Applies the 'RepairWeaponCondition' effect."} | 1 |

</details>

---

### Context: `StatusGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies the 'LuckUp' effect."} | 2 |
| `SpawnCoinAnywhere` | Number | {'type': '`Number`', 'df': "Applies the 'SpawnCoinAnywhere' effect."} | 2 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies the 'SpeedUp' effect."} | 2 |
| `DexterityUp` | Number | {'type': '`Number`', 'df': "Applies the 'DexterityUp' effect."} | 1 |

</details>

---

### Context: `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AutoReanimate` | Number | {'type': '`Number`', 'df': "Applies the 'AutoReanimate' effect."} | 2 |
| [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is friendly to the caster. | 1 |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 2 |
| `FillMana` | Number | {'type': '`Number`', 'df': "Applies the 'FillMana' effect."} | 1 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies the 'HealthGain' effect."} | 1 |
| `PercentHeal` | Number | {'type': '`Number`', 'df': "Applies the 'PercentHeal' effect."} | 1 |
| `TakeExtraTurn` | Number | {'type': '`Number`', 'df': "Applies the 'TakeExtraTurn' effect."} | 1 |

</details>

---

### Context: `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FullHeal` | Number | {'type': '`Number`', 'df': "Applies the 'FullHeal' effect."} | 2 |
| `Sleep` | Number | {'type': '`Number`', 'df': "Applies the 'Sleep' effect."} | 1 |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies the 'StrengthUp' effect."} | 2 |
| `Cleanse` | Number | {'type': '`Number`', 'df': "Applies the 'Cleanse' effect."} | 1 |
| `IntelligenceUp` | Number | {'type': '`Number`', 'df': "Applies the 'IntelligenceUp' effect."} | 1 |
| `RandomStatUp` | Number | {'type': '`Number`', 'df': "Applies the 'RandomStatUp' effect."} | 1 |

</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool) | Block | {'type': '`Block`', 'df': "Selects and applies a random status effect from the provided nested block. | 2 |
| `DivineShield` | Number | {'type': 'Number', 'df': "Applies the 'DivineShield' effect."} | 1 |

</details>

---

### Context: `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum | {'type': 'Enum/String', 'df': 'Spawns a specific character or entity upon impact.'} | 1 |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool) | Block | {'type': '`Block`', 'df': "Selects and applies a random status effect from the provided nested block. | 1 |
| `Thorns` | Number | {'type': '`Number`', 'df': "Applies the 'Thorns' effect."} | 1 |

</details>

---

### Context: `StatusOnKillEnemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies the 'DivineShield' effect."} | 2 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies the 'HealthGain' effect."} | 1 |
| `ManaGain` | Number | {'type': '`Number`', 'df': "Applies the 'ManaGain' effect."} | 1 |
| `RefreshMovePoints` | Number | {'type': '`Number`', 'df': "Applies the 'RefreshMovePoints' effect."} | 1 |

</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DiminishingHealthRegen` | Number | {'type': '`Number`', 'df': "Applies the 'DiminishingHealthRegen' effect."} | 2 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies the 'Shield' effect."} | 1 |

</details>

---

### Context: `statuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ChanceToRevive`](./Passives_and_Statuses.md#context-chancetorevive), [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#context-statusonbattleendifkillthresholdmet)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum | {'type': '`Enum/String`', 'df': 'Generates an item drop from the specified loot pool.'} | 2 |
| `PermanentDexterity` | Number | {'type': '`Number`', 'df': "Applies the 'PermanentDexterity' effect."} | 2 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 1 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies the 'HealthGain' effect."} | 1 |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 2 |
| `range` | Mixed | {'type': '`Enum/String`', 'df': 'Distance or area of effect in tiles.'} | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The specific entity tag required or applied.'} | 2 |

</details>

---

### Context: `AddPassiveToSpawnedRocks`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddFilledMaxHealth` | Number | {'type': '`Number`', 'df': "Applies the 'AddFilledMaxHealth' effect."} | 2 |
| `JoinSpawnerFaction` | Number | {'type': '`Number`', 'df': "Applies the 'JoinSpawnerFaction' effect."} | 2 |

</details>

---

### Context: `AddPassivesToSummonAbilityMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | {'type': '`Number`', 'df': 'Combat Trigger: Deals damage to up.'} | 2 |
| `Doomed` | Number | {'type': '`Number`', 'df': "Applies the 'Doomed' effect."} | 2 |
| `MovementUp` | Number | {'type': '`Number`', 'df': "Applies the 'MovementUp' effect."} | 2 |

</details>

---

### Context: `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ChanceToBreak` | Number | {'type': '`Number`', 'df': "Applies the 'ChanceToBreak' effect."} | 2 |

</details>

---

### Context: `AddStatusToAllDamageAbilities`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies the 'Bleed' effect."} | 1 |
| `Piercing` | Number | {'type': '`Number`', 'df': "Applies the 'Piercing' effect."} | 1 |
| `Weakness` | Number | {'type': '`Number`', 'df': "Applies the 'Weakness' effect."} | 1 |

</details>

---

### Context: `AddStatusToBasicAttackWithCooldown`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CharmedForceAttack` | Number | {'type': '`Number`', 'df': "Applies the 'CharmedForceAttack' effect."} | 2 |

</details>

---

### Context: `AddStatusToFirstBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | {'type': '`Number`', 'df': "Applies the 'Charmed' effect."} | 2 |

</details>

---

### Context: `AddStatusToMeleeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DelayedWind`](./Passives_and_Statuses.md#context-delayedwind) | Block | {'type': '`Block`', 'df': "Applies the 'DelayedWind' effect. | 1 |
| [`DelayedWindCone`](./Passives_and_Statuses.md#context-delayedwindcone) | Block | {'type': '`Block`', 'df': 'Creates a delayed Area of Effect cone. | 1 |

</details>

---

### Context: `AddStatusToTrampleDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Cleave` | Number | {'type': '`Number`', 'df': 'Causes the attack to hit adjacent enemies alongside the primary target.'} | 2 |

</details>

---

### Context: `AllyHealthRegenAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum | {'type': '`Enum/String`', 'df': 'Distance or area of effect in tiles.'} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 2 |

</details>

---

### Context: `AlternateCraftingPools`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tinkerer_0`](./Enums.md#enum-tinkerer_0) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`tinkerer_1`](./Enums.md#enum-tinkerer_1) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `ApplyStatusIfCrit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Purge` | Number | {'type': '`Number`', 'df': "Applies the 'Purge' effect."} | 2 |

</details>

---

### Context: `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bounty` | Number | {'type': '`Number`', 'df': "Applies the 'Bounty' effect."} | 2 |
| `count` | Number | {'type': '`Number`', 'df': 'The numerical quantity.'} | 1 |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 1 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies the 'Shield' effect."} | 1 |

</details>

---

### Context: `AutocastEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 1 |
| `advantage_polarity` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `chance` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 1 |

</details>

---

### Context: `BoobyTrapItems`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`on_break`](./Passives_and_Statuses.md#context-on_break) | Block | {'type': '`Block`', 'df': " | 2 |
| [`on_throw`](./Passives_and_Statuses.md#context-on_throw) | Block | {'type': '`Block`', 'df': " | 2 |

</details>

---

### Context: `BoostWeaponDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`crit_chance`](./Enums.md#enum-crit_chance) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 2 |

</details>

---

### Context: `BouncyProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `max_range` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `CatAPultAnimation`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | {'type': '`Number`', 'df': "Applies the 'Quivered' effect."} | 2 |
| `ally_chance` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `chance` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 2 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 1 |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 2 |
| `chance` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 2 |

</details>

---

### Context: `ChangeTile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `aoe` | Number | {'type': '`Number`', 'df': 'The area of effect or distance in tiles.'} | 1 |
| [`tile`](./Enums.md#enum-tile) | Enum | {'type': '`Enum/String`', 'df': 'The specific tile type to change into (e.g., GlassTile).'} | 1 |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`class`](./Enums.md#enum-class) | Enum | {'type': '`Enum/String`', 'df': 'Character class identifier.'} | 2 |
| `reduction` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies the 'Bleed' effect."} | 2 |
| `BonusCritChance` | Number | {'type': '`Number`', 'df': "Applies the 'BonusCritChance' effect."} | 2 |
| `BonusDamage` | Number | {'type': '`Number`', 'df': "Applies the 'BonusDamage' effect."} | 2 |

</details>

---

### Context: `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | {'type': '`Number`', 'df': "Applies the 'Charmed' effect."} | 1 |
| `Stun` | Number | {'type': '`Number`', 'df': "Applies the 'Stun' effect."} | 1 |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToElementDamage`](./Passives_and_Statuses.md#context-addstatustoelementdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | {'type': '`Number`', 'df': "Applies the 'Charmed' effect."} | 2 |
| `OverrideDamage` | Number | {'type': '`Number`', 'df': "Applies the 'OverrideDamage' effect."} | 2 |
| `Revive` | Number | {'type': '`Number`', 'df': "Applies the 'Revive' effect."} | 2 |
| `SafeDoomed` | Number | {'type': '`Number`', 'df': "Applies the 'SafeDoomed' effect."} | 2 |
| `TakeExtraTurn` | Number | {'type': '`Number`', 'df': "Applies the 'TakeExtraTurn' effect."} | 2 |
| `DamageUp` | Number | {'type': '`Number`', 'df': 'Combat Trigger: Deals damage to up.'} | 1 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies the 'SpeedUp' effect."} | 1 |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToAllDamage`](./Passives_and_Statuses.md#context-addstatustoalldamage), [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The specific string tag to check for.'} | 2 |
| `Charmed` | Number | {'type': '`Number`', 'df': "Applies the 'Charmed' effect."} | 1 |
| `FlatLeechIfDamaged` | Number | {'type': '`Number`', 'df': "Applies the 'FlatLeechIfDamaged' effect."} | 1 |

</details>

---

### Context: `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is hostile to the caster. | 2 |

</details>

---

### Context: `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | {'type': '`Number`', 'df': "Applies the 'Charmed' effect."} | 2 |

</details>

---

### Context: `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BonusCritChance` | Number | {'type': '`Number`', 'df': "Applies the 'BonusCritChance' effect."} | 2 |

</details>

---

### Context: `Craft`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`slot`](./Enums.md#enum-slot) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `DamageNeighborTilesWhenCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`fire`](./Passives_and_Statuses.md#context-fire) | Block | {'type': '`Block`', 'df': ' | 1 |
| [`ice`](./Passives_and_Statuses.md#context-ice) | Block | {'type': '`Block`', 'df': ' | 1 |
| [`lightning`](./Passives_and_Statuses.md#context-lightning) | Block | {'type': '`Block`', 'df': ' | 1 |
| [`triattack`](./Passives_and_Statuses.md#context-triattack) | Block | {'type': '`Block`', 'df': ' | 1 |

</details>

---

### Context: `DamageNeighborsAfterMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': 'The base damage properties of an attack.'} | 2 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | {'type': '`Block`', 'df': "Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 2 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 2 |

</details>

---

### Context: `DamageReductionAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| [`range`](./Enums.md#enum-range) | Enum | {'type': '`Enum/String`', 'df': 'Distance or area of effect in tiles.'} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 2 |

</details>

---

### Context: `Earth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': 'The base damage properties of an attack.'} | 2 |

</details>

---

### Context: `Electric`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Stun`](./Arrays.md#array-stun) | Array | {'type': '`Array`', 'df': "Applies the 'Stun' effect."} | 2 |

</details>

---

### Context: `ElementalAttunement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Earth`](./Passives_and_Statuses.md#context-earth) | Block | {'type': '`Block`', 'df': "Applies the 'Earth' effect. | 2 |
| [`Electric`](./Passives_and_Statuses.md#context-electric) | Block | {'type': '`Block`', 'df': "Applies the 'Electric' effect. | 2 |
| [`Fire`](./Passives_and_Statuses.md#context-fire) | Block | {'type': '`Block`', 'df': "Applies the 'Fire' effect. | 2 |
| [`Grass`](./Passives_and_Statuses.md#context-grass) | Block | {'type': '`Block`', 'df': "Applies the 'Grass' effect. | 2 |
| [`Gravity`](./Passives_and_Statuses.md#context-gravity) | Block | {'type': '`Block`', 'df': "Applies the 'Gravity' effect. | 2 |
| [`Holy`](./Passives_and_Statuses.md#context-holy) | Block | {'type': '`Block`', 'df': "Applies the 'Holy' effect. | 2 |
| [`Ice`](./Passives_and_Statuses.md#context-ice) | Block | {'type': '`Block`', 'df': "Applies the 'Ice' effect. | 2 |
| [`Shadow`](./Passives_and_Statuses.md#context-shadow) | Block | {'type': '`Block`', 'df': "Applies the 'Shadow' effect. | 2 |
| [`Water`](./Passives_and_Statuses.md#context-water) | Block | {'type': '`Block`', 'df': "Applies the 'Water' effect. | 2 |
| [`Wind`](./Passives_and_Statuses.md#context-wind) | Block | {'type': '`Block`', 'df': "Applies the 'Wind' effect. | 2 |

</details>

---

### Context: `EscapeSequence`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomDistanceDisplace` | Number | {'type': '`Number`', 'df': 'Displaces the target by a randomized distance.'} | 2 |
| `SafeExplosionIfHitSomething` | Number | {'type': '`Number`', 'df': "Applies the 'SafeExplosionIfHitSomething' effect."} | 2 |

</details>

---

### Context: `Eternal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health_percent` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 2 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 1 |
| `TakeExtraTurn` | Number | {'type': '`Number`', 'df': "Applies the 'TakeExtraTurn' effect."} | 1 |

</details>

---

### Context: `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is friendly to the caster. | 2 |

</details>

---

### Context: `Fire`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Burn`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies the 'Burn' effect."} | 2 |

</details>

---

### Context: `Grass`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Poison`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies the 'Poison' effect."} | 2 |

</details>

---

### Context: `Gravity`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Weakness`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies the 'Weakness' effect."} | 2 |

</details>

---

### Context: `GravityWell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 2 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | {'type': '`Block`', 'df': "Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 2 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 2 |

</details>

---

### Context: `HealAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `mana` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 2 |

</details>

---

### Context: `Holy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`FlatLeech`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies the 'FlatLeech' effect."} | 2 |

</details>

---

### Context: `HolyDamageBlessing`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`PassiveUntilGetKill`](./Passives_and_Statuses.md#context-passiveuntilgetkill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies the 'Burn' effect."} | 2 |
| `damage_multiplier` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `Ice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Slow`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies the 'Slow' effect."} | 2 |

</details>

---

### Context: `InfiniteRebirth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempSpeedUp` | Number | {'type': '`Number`', 'df': "Applies the 'TempSpeedUp' effect."} | 2 |
| `health` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `playercat_health` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `LateBloomer`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 2 |

</details>

---

### Context: `LightningRod`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | {'type': '`Number`', 'df': "Applies the 'Tech' effect."} | 2 |

</details>

---

### Context: `LowHealthAllyDodgeChanceAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 2 |
| `theshold` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 2 |
| `enemies_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `NextBattleStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 2 |
| `FullHeal` | Number | {'type': '`Number`', 'df': "Applies the 'FullHeal' effect."} | 2 |

</details>

---

### Context: `PassiveAfterXKills`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block | {'type': '`Block`', 'df': " | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 2 |

</details>

---

### Context: `PassiveAtFullHealth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ManaCostReduction` | Number | {'type': '`Number`', 'df': "Applies the 'ManaCostReduction' effect."} | 2 |
| `TakeExtraDamage` | Number | {'type': '`Number`', 'df': "Applies the 'TakeExtraDamage' effect."} | 2 |

</details>

---

### Context: `PassiveAtInjuryThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`injury`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`mode`](./Enums.md#enum-mode) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block | {'type': '`Block`', 'df': " | 2 |
| `threshold` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `PassiveGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`RandomPassivePool`](./Passives_and_Statuses.md#context-randompassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`SetDefaultFace`](./Enums.md#enum-setdefaultface) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'SetDefaultFace' effect."} | 2 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 1 |
| `CharismaUp` | Number | {'type': '`Number`', 'df': "Applies the 'CharismaUp' effect."} | 1 |
| `IntelligenceUp` | Number | {'type': '`Number`', 'df': "Applies the 'IntelligenceUp' effect."} | 1 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies the 'SpeedUp' effect."} | 1 |

</details>

---

### Context: `PassiveUntilCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`HealAlliesEachTurn`](./Passives_and_Statuses.md#context-healallieseachturn) | Block | {'type': '`Block`', 'df': "Applies the 'HealAlliesEachTurn' effect. | 2 |
| [`StatusAlliesEachTurn`](./Passives_and_Statuses.md#context-statusallieseachturn) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies nested statuses to allies each turn. | 1 |

</details>

---

### Context: `PassiveUntilGetKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`HolyDamageBlessing`](./Passives_and_Statuses.md#context-holydamageblessing) | Block | {'type': '`Block`', 'df': "Applies the 'HolyDamageBlessing' effect. | 2 |

</details>

---

### Context: `PassiveWhenTheAlpha`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TogglableRoundEndExtraTurn` | Number | {'type': '`Number`', 'df': "Applies the 'TogglableRoundEndExtraTurn' effect."} | 2 |

</details>

---

### Context: `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | {'type': '`Number`', 'df': "Applies the 'Brace' effect."} | 2 |
| `HealthRegenUp` | Number | {'type': '`Number`', 'df': "Applies the 'HealthRegenUp' effect."} | 1 |

</details>

---

### Context: `PassiveWhileInMonkRangedStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddBonusRange` | Number | {'type': '`Number`', 'df': "Applies the 'AddBonusRange' effect."} | 2 |
| `AddSpellDamage` | Number | {'type': '`Number`', 'df': "Applies the 'AddSpellDamage' effect."} | 2 |
| `KineticSpikes` | Number | {'type': '`Number`', 'df': "Applies the 'KineticSpikes' effect."} | 1 |

</details>

---

### Context: `PassiveWhilePreviewingMonkRangedStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddBonusRange` | Number | {'type': '`Number`', 'df': "Applies the 'AddBonusRange' effect."} | 2 |

</details>

---

### Context: `PassiveWhileWearingMetal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddElementsToWeapon`](./Enums.md#enum-addelementstoweapon) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'AddElementsToWeapon' effect."} | 2 |

</details>

---

### Context: `RepressedMemoriesMetronome`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#context-scaledstatusonspendmana)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 2 |

</details>

---

### Context: `ScaledStatusOnOverMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | {'type': '`Number`', 'df': 'Fires a randomized number of magic missiles.'} | 2 |
| `Cleanse` | Number | {'type': '`Number`', 'df': "Applies the 'Cleanse' effect."} | 1 |

</details>

---

### Context: `ScaledStatusOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RepressedMemoriesMetronome`](./Passives_and_Statuses.md#context-repressedmemoriesmetronome) | Block | {'type': '`Block`', 'df': "Applies the 'RepressedMemoriesMetronome' effect. | 2 |

</details>

---

### Context: `SecurityBotProtect`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 2 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `Shadow`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`crit_chance`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `SmiteEnemiesWhoKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 2 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 2 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 2 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | {'type': '`Block`', 'df': "Non-damaging status applications and logic triggers executed on impact. | 1 |

</details>

---

### Context: `SpecialFriends`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 2 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies the 'HealthGain' effect."} | 2 |

</details>

---

### Context: `StatsAtLowHealth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `threshold` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `speed` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `strength` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `StatusAfterCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempSpellDamageUp` | Number | {'type': '`Number`', 'df': "Applies the 'TempSpellDamageUp' effect."} | 2 |
| `TempDamageUp` | Number | {'type': '`Number`', 'df': "Applies the 'TempDamageUp' effect."} | 1 |

</details>

---

### Context: `StatusAlliesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'EquipTemporaryItem' effect."} | 2 |

</details>

---

### Context: `StatusAlliesOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies the 'HealthGain' effect."} | 2 |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies the 'LuckUp' effect."} | 2 |
| `scaled` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `StatusAllyWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 2 |
| `threshold` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `StatusAnyCatAllyWhoKills`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AlphaCat` | Number | {'type': '`Number`', 'df': "Applies the 'AlphaCat' effect."} | 2 |

</details>

---

### Context: `StatusDamagers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies the 'LuckUp' effect."} | 2 |
| [`Fear`](./Arrays.md#array-fear) | Array | {'type': '`Array`', 'df': "Applies the 'Fear' effect."} | 1 |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | {'type': '`Number`', 'df': 'Fires a randomized number of magic missiles.'} | 2 |

</details>

---

### Context: `StatusEachTurnEndPerEnemyKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#context-objectonhitcharacter) | Block | {'type': '`Block`', 'df': 'Spawns a specific character or entity upon impact. | 2 |

</details>

---

### Context: `StatusEnemiesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 2 |
| `Freeze` | Number | {'type': '`Number`', 'df': "Applies the 'Freeze' effect."} | 2 |

</details>

---

### Context: `StatusEveryXTurnBegins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies the 'DivineShield' effect."} | 2 |
| `turns` | Number | {'type': '`Number`', 'df': 'The duration of the effect in turns.'} | 2 |

</details>

---

### Context: `StatusKillers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Boss`](./Passives_and_Statuses.md#context-conditional_boss) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is a Boss. | 2 |
| [`Conditional_NotBoss`](./Passives_and_Statuses.md#context-conditional_notboss) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic if the target is NOT a Boss. | 2 |

</details>

---

### Context: `StatusOnAnyDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies the 'LuckUp' effect."} | 2 |

</details>

---

### Context: `StatusOnBattleEndIfKillThresholdMet`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `kills` | Number | {'type': '`Number`', 'df': ''} | 2 |
| [`statuses`](./Passives_and_Statuses.md#context-statuses) | Block | {'type': '`Block`', 'df': " | 2 |

</details>

---

### Context: `StatusOnBreakItem`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | {'type': '`Number`', 'df': "Applies the 'Thorns' effect."} | 2 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies the 'Shield' effect."} | 1 |

</details>

---

### Context: `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | {'type': '`Number`', 'df': "Applies the 'Tech' effect."} | 2 |

</details>

---

### Context: `StatusOnDealtDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempDexterityUp` | Number | {'type': '`Number`', 'df': "Applies the 'TempDexterityUp' effect."} | 2 |
| `TempStrengthUp` | Number | {'type': '`Number`', 'df': "Applies the 'TempStrengthUp' effect."} | 2 |
| `TempLuckUp` | Number | {'type': '`Number`', 'df': "Applies the 'TempLuckUp' effect."} | 1 |

</details>

---

### Context: `StatusOnDealtDamageThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RefreshMovePoints` | Number | {'type': '`Number`', 'df': "Applies the 'RefreshMovePoints' effect."} | 2 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies the 'Shield' effect."} | 2 |
| `count_overkill` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `ignore_during_movement` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `threshold` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 1 |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceAttack` | Number | {'type': '`Number`', 'df': 'Forces the character to execute an immediate attack.'} | 2 |

</details>

---

### Context: `StatusOnGainShield`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Temporary`](./Passives_and_Statuses.md#context-temporary) | Block | {'type': '`Block`', 'df': 'A wrapper block for applying status effects that automatically expire. | 2 |

</details>

---

### Context: `StatusOnHeal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies the 'SpeedUp' effect."} | 2 |
| `RandomStatUp` | Number | {'type': '`Number`', 'df': "Applies the 'RandomStatUp' effect."} | 1 |

</details>

---

### Context: `StatusOnOverMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `IntelligenceUp` | Number | {'type': '`Number`', 'df': "Applies the 'IntelligenceUp' effect."} | 2 |
| `SpellDamageUp` | Number | {'type': '`Number`', 'df': "Applies the 'SpellDamageUp' effect."} | 2 |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies the 'DivineShield' effect."} | 1 |

</details>

---

### Context: `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RefreshMovePoints` | Number | {'type': '`Number`', 'df': "Applies the 'RefreshMovePoints' effect."} | 2 |
| `DexterityUp` | Number | {'type': '`Number`', 'df': "Applies the 'DexterityUp' effect."} | 1 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies the 'SpeedUp' effect."} | 1 |

</details>

---

### Context: `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies the 'HealthGain' effect."} | 2 |

</details>

---

### Context: `StatusOnTookDamageFromEnemyAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | {'type': '`Number`', 'df': "Applies the 'Quivered' effect."} | 2 |
| `MoveQuivered` | Number | {'type': '`Number`', 'df': "Applies the 'MoveQuivered' effect."} | 1 |

</details>

---

### Context: `StatusOnTriggerTrap`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DexterityUp` | Number | {'type': '`Number`', 'df': "Applies the 'DexterityUp' effect."} | 2 |
| `Quivered` | Number | {'type': '`Number`', 'df': "Applies the 'Quivered' effect."} | 1 |

</details>

---

### Context: `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FlippedFacingForceAttack` | Number | {'type': '`Number`', 'df': "Applies the 'FlippedFacingForceAttack' effect."} | 2 |

</details>

---

### Context: `StatusOnUseElementAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies the 'SpeedUp' effect."} | 2 |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'The specific element type required or applied.'} | 2 |

</details>

---

### Context: `StatusPerInjury`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies the 'Shield' effect."} | 2 |
| `cap` | Number | {'type': '`Number`', 'df': ''} | 2 |
| [`injury`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': ''} | 2 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies the 'StrengthUp' effect."} | 1 |

</details>

---

### Context: `StatusThingsKnockedBack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Drag` | Number | {'type': '`Number`', 'df': "Applies the 'Drag' effect."} | 2 |

</details>

---

### Context: `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `OneUseSpellDamageUp` | Number | {'type': '`Number`', 'df': "Applies the 'OneUseSpellDamageUp' effect."} | 2 |
| `ManaGain` | Number | {'type': '`Number`', 'df': "Applies the 'ManaGain' effect."} | 1 |

</details>

---

### Context: `TaggedPickupEffectReplacement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`HealthGain`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies the 'HealthGain' effect."} | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The specific entity tag required or applied.'} | 2 |

</details>

---

### Context: `TowerDefense`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 2 |
| `range` | Number | {'type': '`Number`', 'df': 'Distance or area of effect in tiles.'} | 2 |

</details>

---

### Context: `Water`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AOEPuddle`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies the 'AOEPuddle' effect."} | 2 |

</details>

---

### Context: `Wind`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`knockback`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `on_break`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SafeExplosionIfHitSomething` | Number | {'type': '`Number`', 'df': "Applies the 'SafeExplosionIfHitSomething' effect."} | 2 |

</details>

---

### Context: `on_throw`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HitExplosion` | Number | {'type': '`Number`', 'df': "Applies the 'HitExplosion' effect."} | 2 |

</details>

---

### Context: `schadenfreude_scaled_stats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `str` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `AbilityChargeRefundChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `advantage_softcap` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `chance` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 1 |

</details>

---

### Context: `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies the 'Bruise' effect."} | 1 |

</details>

---

### Context: `AddStatusToReceivedDamage_ExcludeStatuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_DoesDamage`](./Passives_and_Statuses.md#context-conditional_doesdamage) | Block | {'type': '`Block`', 'df': "Conditional block: Executes nested logic only if the target is/has DoesDamage. | 1 |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LeechPercent` | Number | {'type': '`Number`', 'df': "Applies the 'LeechPercent' effect."} | 1 |

</details>

---

### Context: `AddStatusesIfPersistentWeatherElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies the 'Burn' effect."} | 1 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `AddStatusesToReceivedElementalDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies the 'Burn' effect."} | 1 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `AddTemporaryEffectsToEquipment`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | {'type': '`Number`', 'df': "Applies the 'CastAgain' effect."} | 1 |

</details>

---

### Context: `Autism`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `innate` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `learned` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `ChanceToRevive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 1 |
| [`statuses`](./Passives_and_Statuses.md#context-statuses) | Block | {'type': '`Block`', 'df': " | 1 |

</details>

---

### Context: `CollectPickupsOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `pop_corpses` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `Conditional_DoesDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToReceivedDamage_ExcludeStatuses`](./Passives_and_Statuses.md#context-addstatustoreceiveddamage_excludestatuses)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Bleed`](./Arrays.md#array-bleed) | Array | {'type': '`Array`', 'df': "Applies the 'Bleed' effect."} | 1 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `UseRandomSpell_Madness` | Number | {'type': '`Number`', 'df': "Applies the 'UseRandomSpell_Madness' effect."} | 1 |
| `odds` | Number | {'type': '`Number`', 'df': "The probability (0.0 to 1.0) of triggering the 'good roll' success state."} | 1 |

</details>

---

### Context: `Conditional_SourceHasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is friendly to the caster. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The specific entity tag required or applied.'} | 1 |

</details>

---

### Context: `DamageIfDidntUseSpecificAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 1 |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |

</details>

---

### Context: `DelayedWind`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | {'type': '`Number`', 'df': 'The area of effect or distance in tiles.'} | 1 |

</details>

---

### Context: `DelayedWindCone`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | {'type': '`Number`', 'df': 'The area of effect or distance in tiles.'} | 1 |

</details>

---

### Context: `Diabetes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 1 |
| `Confusion` | Number | {'type': '`Number`', 'df': "Applies the 'Confusion' effect."} | 1 |

</details>

---

### Context: `EnergyStorm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `period` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `ForceMoveAway`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusAdjacentOnTheirTurnBegin`](./Passives_and_Statuses.md#context-statusadjacentontheirturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `free` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `FurnitureStats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Appeal` | Number | {'type': '`Number`', 'df': "Applies the 'Appeal' effect."} | 1 |
| `Comfort` | Number | {'type': '`Number`', 'df': "Applies the 'Comfort' effect."} | 1 |
| `Stimulation` | Number | {'type': '`Number`', 'df': "Applies the 'Stimulation' effect."} | 1 |

</details>

---

### Context: `MegaMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 1 |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `PassiveLevelScaledStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Shield`](./Math_Equations.md) | Equation | {'type': '`String`', 'df': "Applies the 'Shield' effect."} | 1 |
| [`SizeScalePercent`](./Math_Equations.md) | Equation | {'type': '`String`', 'df': "Applies the 'SizeScalePercent' effect."} | 1 |
| [`Trample`](./Arrays.md#array-trample) | Array | {'type': '`Array`', 'df': "Applies the 'Trample' effect."} | 1 |

</details>

---

### Context: `RandomPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`PassiveGroup`](./Passives_and_Statuses.md#context-passivegroup) | Block | {'type': '`Block`', 'df': "Applies the 'PassiveGroup' effect. | 2 |

</details>

---

### Context: `ReplaceBrain`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Robot`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `ScaledStatusOnBleedDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | {'type': '`Number`', 'df': "Applies the 'Charge' effect."} | 1 |

</details>

---

### Context: `ScaledStatusOnLoseShield`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | {'type': '`Number`', 'df': "Applies the 'Thorns' effect."} | 1 |

</details>

---

### Context: `ScaledStatusOnOverHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnScaledRotFly` | Number | {'type': '`Number`', 'df': "Applies the 'SpawnScaledRotFly' effect."} | 1 |

</details>

---

### Context: `SelfDamageWhenDealDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 1 |

</details>

---

### Context: `StackingDodgeChanceOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `amount` | Number | {'type': '`Number`', 'df': 'The numerical quantity.'} | 1 |
| `cap` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `StatusAdjacentOnTheirTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceMoveAway`](./Passives_and_Statuses.md#context-forcemoveaway) | Block | {'type': '`Block`', 'df': "Applies the 'ForceMoveAway' effect. | 1 |

</details>

---

### Context: `StatusAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomStatUp` | Number | {'type': '`Number`', 'df': "Applies the 'RandomStatUp' effect."} | 1 |
| `exclude_self` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `StatusAlliesOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | {'type': '`Number`', 'df': "Applies the 'ManaGain' effect."} | 1 |

</details>

---

### Context: `StatusAlliesScaledByCursedOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies the 'LuckUp' effect."} | 1 |

</details>

---

### Context: `StatusIfBattleAlreadyBegan`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PermanentMadness` | Number | {'type': '`Number`', 'df': "Applies the 'PermanentMadness' effect."} | 1 |

</details>

---

### Context: `StatusOnEatPill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies the 'AllStatsUp' effect."} | 1 |

</details>

---

### Context: `StatusOnLoseShield`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | {'type': '`Number`', 'df': "Applies the 'Thorns' effect."} | 1 |

</details>

---

### Context: `StatusOnTakeHealthDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PermanentConstitution` | Number | {'type': '`Number`', 'df': "Applies the 'PermanentConstitution' effect."} | 1 |

</details>

---

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | {'type': '`Number`', 'df': "Applies the 'ManaGain' effect."} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 1 |

</details>

---

### Context: `StrengthInNumbersAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count_self` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 1 |

</details>

---

### Context: `Study`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `marked` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 1 |

</details>

---

### Context: `TakeBonusTurnWithStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | {'type': '`Number`', 'df': 'Applies the Madness debuff/status effect.'} | 1 |

</details>

---

### Context: `TheHunger`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | {'type': '`Number`', 'df': 'Applies the Madness debuff/status effect.'} | 1 |

</details>

---

### Context: `TileDamageMultiplier`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ally_multiplier` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `multiplier` | Number | {'type': '`Number`', 'df': 'Multiplicative modifier to a base value.'} | 1 |

</details>

---

### Context: `TourettesMeows`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cooldown`](./Arrays.md#array-cooldown) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`pool`](./Arrays.md#array-pool) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `fire`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | {'type': '`Block`', 'df': "Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 1 |

</details>

---

### Context: `ice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | {'type': '`Block`', 'df': "Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 1 |

</details>

---

### Context: `lightning`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | {'type': '`Block`', 'df': "Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 1 |

</details>

---

### Context: `triattack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | {'type': '`Block`', 'df': "Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 1 |

</details>

---

