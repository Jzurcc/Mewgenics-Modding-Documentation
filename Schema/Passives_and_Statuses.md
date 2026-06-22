# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Passives & Statuses

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/511) |
| :--- | :--- | :--- | :--- |
| `name` | String | Localization key for the passive's display name. | 511 |
| [`class`](./Enums.md#enum-class) | Enum/String | Character class identifier. | 510 |
| `desc` | String | Localization key for the passive's display description. | 510 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 116 |
| [`stats`](./Passives_and_Statuses.md#context-stats) | Block |  | 35 |
| [`lock_item_slot`](./Passives_and_Statuses.md#context-lock_item_slot) | Block |  | 16 |
| `desc_multiclass` | String |  | 5 |
| `auto_plus_signs_on_name` | Boolean |  | 4 |
| `name_mod` | String |  | 4 |
| [`tags`](./Arrays.md#array-tags) | Array |  | 3 |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum/String |  | 2 |
| `shield` | Number |  | 2 |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | Flat addition to a base value. | 1 |
| [`grant_ability`](./Enums.md#enum-grant_ability) | Enum/String |  | 1 |

</details>

---

### Context: `2`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/372) |
| :--- | :--- | :--- | :--- |
| `desc` | String | Localization key for the passive's display description. | 372 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 369 |
| [`stats`](./Passives_and_Statuses.md#context-stats) | Block |  | 36 |
| `desc_multiclass` | String |  | 5 |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum/String |  | 4 |
| `shield` | Number |  | 4 |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | Flat addition to a base value. | 3 |
| `divine_shield` | Number |  | 3 |
| [`keyword_tooltips`](./Passives_and_Statuses.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear when hovering over the ability. | 3 |
| [`empty_armor_scaled_stats`](./Passives_and_Statuses.md#context-empty_armor_scaled_stats) | Block |  | 2 |
| [`icon`](./Enums.md#enum-icon) | Enum/String |  | 1 |
| [`schadenfreude_scaled_stats`](./Passives_and_Statuses.md#context-schadenfreude_scaled_stats) | Block |  | 1 |

</details>

---

### Context: `1`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/368) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 368 |
| [`stats`](./Passives_and_Statuses.md#context-stats) | Block |  | 26 |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | Flat addition to a base value. | 4 |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum/String |  | 4 |
| `divine_shield` | Number |  | 3 |
| [`keyword_tooltips`](./Passives_and_Statuses.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear when hovering over the ability. | 3 |
| `shield` | Number |  | 3 |
| [`empty_armor_scaled_stats`](./Passives_and_Statuses.md#context-empty_armor_scaled_stats) | Block |  | 2 |
| `desc` | String | Localization key for the passive's display description. | 1 |
| [`schadenfreude_scaled_stats`](./Passives_and_Statuses.md#context-schadenfreude_scaled_stats) | Block |  | 1 |

</details>

---

### Context: `passives`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Passives_and_Statuses.md#context-1), [`10`](./Passives_and_Statuses.md#context-10), [`2`](./Passives_and_Statuses.md#context-2), [`3`](./Passives_and_Statuses.md#context-3), [`4`](./Passives_and_Statuses.md#context-4), [`5`](./Passives_and_Statuses.md#context-5), [`6`](./Passives_and_Statuses.md#context-6), [`7`](./Passives_and_Statuses.md#context-7), [`8`](./Passives_and_Statuses.md#context-8), [`9`](./Passives_and_Statuses.md#context-9), [`PassiveAfterXKills`](./Passives_and_Statuses.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#context-passiveathealththreshold), [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#context-passiveatinjurythreshold), [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold), [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement), [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count (X/80) |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 80 |
| [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions) | Block | Applies the 'AddPassivesToMinions' effect. | 29 |
| [`MulticlassLevelUp`](./Enums.md#enum-multiclasslevelup) | Enum/String | Applies the 'MulticlassLevelUp' effect. | 24 |
| `CritChanceUp` | Number | Applies the 'CritChanceUp' effect. | 22 |
| [`SpawnOnBattleStart`](./Enums.md#enum-spawnonbattlestart) | Enum/String | Applies the 'SpawnOnBattleStart' effect. | 21 |
| [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage) | Block | Event Trigger: Applies nested statuses when took damage. | 21 |
| [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend) | Block | Event Trigger: Applies nested statuses to each turn end. | 20 |
| `AddCritMultiplier` | Number | Applies the 'AddCritMultiplier' effect. | 17 |
| [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend) | Block | Applies the nested status effects when the encounter finishes. | 16 |
| `MissChance` | Number | Applies the 'MissChance' effect. | 14 |
| [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill) | Block | Event Trigger: Applies nested statuses when kill. | 14 |
| [`ReplaceSpawnedObjects`](./Arrays.md#array-replacespawnedobjects) | Array | Applies the 'ReplaceSpawnedObjects' effect. | 13 |
| [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin) | Block | Event Trigger: Applies nested statuses to each turn begin. | 12 |
| `AddBonusRange` | Number | Applies the 'AddBonusRange' effect. | 11 |
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum/String | Applies the 'BonusAbility' effect. | 11 |
| `Brace` | Number | Applies the 'Brace' effect. | 11 |
| `DodgeChance` | Number | Applies the 'DodgeChance' effect. | 11 |
| `HealthRegenUp` | Number | Applies the 'HealthRegenUp' effect. | 11 |
| [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus) | Block | Applies the 'CritsApplyStatus' effect. | 10 |
| [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold) | Block | Applies the 'PassiveAtStatThreshold' effect. | 10 |
| `PassiveLevelUpAtCombatEnd` | Number | Applies the 'PassiveLevelUpAtCombatEnd' effect. | 10 |
| `ExtraBasicAttacks` | Number | Applies the 'ExtraBasicAttacks' effect. | 9 |
| [`RevengeDamage`](./Passives_and_Statuses.md#context-revengedamage) | Block | Reaction trigger: Deals damage to the attacker when hit. | 9 |
| `Trample` | Number | Applies the 'Trample' effect. | 9 |
| [`AmplifyStatus`](./Enums.md#enum-amplifystatus) | Enum/String | Applies the 'AmplifyStatus' effect. | 8 |
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum/String | Applies the 'EquipTemporaryItem' effect. | 8 |
| [`ForceSpecificInjury`](./Enums.md#enum-forcespecificinjury) | Enum/String | Applies the 'ForceSpecificInjury' effect. | 8 |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum/String | Applies the 'InnateElement' effect. | 8 |
| [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage) | Block | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. | 8 |
| [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty) | Block | Applies the 'PassiveIfAllArmorEmpty' effect. | 8 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum/String | Applies the 'ReplaceBasicAttack' effect. | 8 |
| [`SizeScale`](./Enums.md#enum-sizescale) | Enum/String | Applies the 'SizeScale' effect. | 8 |
| [`StatusImmunity`](./Arrays.md#array-statusimmunity) | Array | Event Trigger: Applies nested statuses to immunity. | 8 |
| [`StatusOnCrit`](./Passives_and_Statuses.md#context-statusoncrit) | Block | Event Trigger: Applies nested statuses when crit. | 8 |
| [`AbilityOnBattleStart`](./Enums.md#enum-abilityonbattlestart) | Enum/String | Applies the 'AbilityOnBattleStart' effect. | 7 |
| `AddCorpseHealth` | Number | Applies the 'AddCorpseHealth' effect. | 7 |
| `BlastResistance` | Number | Applies the 'BlastResistance' effect. | 7 |
| [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#context-damageneighborsonendmove) | Block | Combat Trigger: Deals damage to neighbors on end move. | 7 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum/String | Applies the 'ElementImmune' effect. | 7 |
| [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#context-passiveifemptyface) | Block | Applies the 'PassiveIfEmptyFace' effect. | 7 |
| [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#context-passiveifemptyhead) | Block | Applies the 'PassiveIfEmptyHead' effect. | 7 |
| [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#context-passiveifemptyneck) | Block | Applies the 'PassiveIfEmptyNeck' effect. | 7 |
| [`StatusAlliesOnDeath`](./Passives_and_Statuses.md#context-statusalliesondeath) | Block | Event Trigger: Applies nested statuses to allies on death. | 7 |
| [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#context-statusonuseabilitywithtag) | Block | Event Trigger: Applies nested statuses when use ability with tag. | 7 |
| `Thorns` | Number | Applies the 'Thorns' effect. | 7 |
| [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum/String | Applies the 'AddElementsToBasicAttack' effect. | 6 |
| [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities) | Block | Applies the 'AddStatusToElementAbilities' effect. | 6 |
| [`AddStatusToWeapons`](./Passives_and_Statuses.md#context-addstatustoweapons) | Block | Applies the 'AddStatusToWeapons' effect. | 6 |
| `AlphaTurns` | Number | Applies the 'AlphaTurns' effect. | 6 |
| `BasicAttackDamageMultiplier` | Number | Applies the 'BasicAttackDamageMultiplier' effect. | 6 |
| `BoostWeaponDamage` | Number | Applies the 'BoostWeaponDamage' effect. | 6 |
| `ExtraMovePoints` | Number | Applies the 'ExtraMovePoints' effect. | 6 |
| `ExtraWeaponAttacks` | Number | Applies the 'ExtraWeaponAttacks' effect. | 6 |
| [`ManaCostReductionTagged`](./Passives_and_Statuses.md#context-manacostreductiontagged) | Block | Applies the 'ManaCostReductionTagged' effect. | 6 |
| [`ReplaceBasicAttackWhenCastable`](./Enums.md#enum-replacebasicattackwhencastable) | Enum/String | Applies the 'ReplaceBasicAttackWhenCastable' effect. | 6 |
| `SetSpellCosts` | Number | Applies the 'SetSpellCosts' effect. | 6 |
| [`SpawnEachTurn`](./Passives_and_Statuses.md#context-spawneachturn) | Block | Applies the 'SpawnEachTurn' effect. | 6 |
| [`SpawnThingOnDamage`](./Passives_and_Statuses.md#context-spawnthingondamage) | Block | Applies the 'SpawnThingOnDamage' effect. | 6 |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch) | Block | Event Trigger: Applies nested statuses when stance switch. | 6 |
| `AddBonusMeleeRange` | Number | Applies the 'AddBonusMeleeRange' effect. | 5 |
| `AddManaRegen` | Number | Applies the 'AddManaRegen' effect. | 5 |
| [`AddStatusToAllDamage`](./Passives_and_Statuses.md#context-addstatustoalldamage) | Block | Applies the 'AddStatusToAllDamage' effect. | 5 |
| [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack) | Block | Applies the 'AddStatusToBasicMeleeAttack' effect. | 5 |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 5 |
| `BasicAttackAOEBonus` | Number | Applies the 'BasicAttackAOEBonus' effect. | 5 |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum/String | Applies the 'ReplaceBasicMove' effect. | 5 |
| [`StatusOnCastSpell`](./Passives_and_Statuses.md#context-statusoncastspell) | Block | Event Trigger: Applies nested statuses when cast spell. | 5 |
| [`StatusOnOverHealed`](./Passives_and_Statuses.md#context-statusonoverhealed) | Block | Event Trigger: Applies nested statuses when over healed. | 5 |
| [`AbilityReaction`](./Enums.md#enum-abilityreaction) | Enum/String | Applies the 'AbilityReaction' effect. | 4 |
| `AddDamageToBasicAttack` | Number | Applies the 'AddDamageToBasicAttack' effect. | 4 |
| [`AddDamageToElementDamage`](./Passives_and_Statuses.md#context-adddamagetoelementdamage) | Block | Applies the 'AddDamageToElementDamage' effect. | 4 |
| `AddLevelUpRerolls` | Number | Applies the 'AddLevelUpRerolls' effect. | 4 |
| `AddMovement` | Number | Applies the 'AddMovement' effect. | 4 |
| [`AddPassivesToCharmed`](./Passives_and_Statuses.md#context-addpassivestocharmed) | Block | Applies the 'AddPassivesToCharmed' effect. | 4 |
| [`AddStatusToElementDamage`](./Passives_and_Statuses.md#context-addstatustoelementdamage) | Block | Applies the 'AddStatusToElementDamage' effect. | 4 |
| [`AllyBonusAbilityAura`](./Enums.md#enum-allybonusabilityaura) | Enum/String | Applies the 'AllyBonusAbilityAura' effect. | 4 |
| [`AllyManaRegenAura`](./Passives_and_Statuses.md#context-allymanaregenaura) | Block | Applies the 'AllyManaRegenAura' effect. | 4 |
| [`AutocastEachRound`](./Passives_and_Statuses.md#context-autocasteachround) | Block | Forces the character to automatically cast a specific ability at the start of each combat round. | 4 |
| `BackstabCritChance` | Number | Applies the 'BackstabCritChance' effect. | 4 |
| `BoostHeals` | Number | Applies the 'BoostHeals' effect. | 4 |
| `FreezePiercing` | Number | Applies the 'FreezePiercing' effect. | 4 |
| `IncreaseExplosionDamage` | Number | Applies the 'IncreaseExplosionDamage' effect. | 4 |
| `KnockbackImmunity` | Number | Applies the 'KnockbackImmunity' effect. | 4 |
| [`LevelUpClassOverride`](./Enums.md#enum-levelupclassoverride) | Enum/String | Applies the 'LevelUpClassOverride' effect. | 4 |
| `MakeSpellsRequireCharge` | Number | Applies the 'MakeSpellsRequireCharge' effect. | 4 |
| `MoveQuivered` | Number | Applies the 'MoveQuivered' effect. | 4 |
| [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#context-passiveathealththreshold) | Block | Applies the 'PassiveAtHealthThreshold' effect. | 4 |
| [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#context-passivewhenatfullmana) | Block | State Trigger: Grants nested passives when at full mana. | 4 |
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum/String | Applies the 'SpawnThingOnDeath' effect. | 4 |
| [`StatusIfUnusedMovePoints`](./Passives_and_Statuses.md#context-statusifunusedmovepoints) | Block | Event Trigger: Applies nested statuses to if unused move points. | 4 |
| [`StatusOnTurnEndIfCastNSpells`](./Passives_and_Statuses.md#context-statusonturnendifcastnspells) | Block | Event Trigger: Applies nested statuses when turn end if cast n spells. | 4 |
| [`StatusOnTurnEndIfManaExact`](./Passives_and_Statuses.md#context-statusonturnendifmanaexact) | Block | Event Trigger: Applies nested statuses when turn end if mana exact. | 4 |
| [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#context-statusonturnendifmanaorhealthexact) | Block | Event Trigger: Applies nested statuses when turn end if mana or health exact. | 4 |
| `AddKnockbackDamage` | Number | Applies the 'AddKnockbackDamage' effect. | 3 |
| [`AddSelfStatusToBasicAttack`](./Passives_and_Statuses.md#context-addselfstatustobasicattack) | Block | Applies the 'AddSelfStatusToBasicAttack' effect. | 3 |
| [`AddTag`](./Enums.md#enum-addtag) | Enum/String | Applies the 'AddTag' effect. | 3 |
| [`AddTemporaryEffectsToBasicAttack`](./Passives_and_Statuses.md#context-addtemporaryeffectstobasicattack) | Block | Applies the 'AddTemporaryEffectsToBasicAttack' effect. | 3 |
| `AllyDamageReduction` | Number | Applies the 'AllyDamageReduction' effect. | 3 |
| `AmplifyKnockback` | Number | Applies the 'AmplifyKnockback' effect. | 3 |
| [`AutocastEachTurnBegin`](./Enums.md#enum-autocasteachturnbegin) | Enum/String | Applies the 'AutocastEachTurnBegin' effect. | 3 |
| `Bruise` | Number | Applies the 'Bruise' effect. | 3 |
| [`CobraReflex`](./Enums.md#enum-cobrareflex) | Enum/String | Applies the 'CobraReflex' effect. | 3 |
| `ConsumablesInfiniteRange` | Number | Applies the 'ConsumablesInfiniteRange' effect. | 3 |
| `DamageUp` | Number | Combat Trigger: Deals damage to up. | 3 |
| [`DeathRattle`](./Passives_and_Statuses.md#context-deathrattle) | Block | Applies the 'DeathRattle' effect. | 3 |
| [`ElementalManaCostReduction`](./Passives_and_Statuses.md#context-elementalmanacostreduction) | Block | Applies the 'ElementalManaCostReduction' effect. | 3 |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum/String | Applies the 'FreePathfindElement' effect. | 3 |
| `IgnoreTiles` | Number | Applies the 'IgnoreTiles' effect. | 3 |
| [`MoveTowardsDamageSource`](./Passives_and_Statuses.md#context-movetowardsdamagesource) | Block | Applies the 'MoveTowardsDamageSource' effect. | 3 |
| `Quivered` | Number | Applies the 'Quivered' effect. | 3 |
| [`SpawnCatCopyOnBattleStart`](./Passives_and_Statuses.md#context-spawncatcopyonbattlestart) | Block | Applies the 'SpawnCatCopyOnBattleStart' effect. | 3 |
| [`SpawnOnBattleStartRandomEmptyTile`](./Passives_and_Statuses.md#context-spawnonbattlestartrandomemptytile) | Block | Applies the 'SpawnOnBattleStartRandomEmptyTile' effect. | 3 |
| [`StatusEveryXSpellCasts`](./Passives_and_Statuses.md#context-statuseveryxspellcasts) | Block | Event Trigger: Applies nested statuses to every x spell casts. | 3 |
| [`StatusKilledCharacters`](./Passives_and_Statuses.md#context-statuskilledcharacters) | Block | Event Trigger: Applies nested statuses to killed characters. | 3 |
| [`StatusOnAllyCatDeath`](./Passives_and_Statuses.md#context-statusonallycatdeath) | Block | Event Trigger: Applies nested statuses when ally cat death. | 3 |
| [`StatusOnBattleStart`](./Passives_and_Statuses.md#context-statusonbattlestart) | Block | Event Trigger: Applies nested statuses when battle start. | 3 |
| [`StatusOnEatFood`](./Passives_and_Statuses.md#context-statusoneatfood) | Block | Event Trigger: Applies nested statuses when eat food. | 3 |
| [`StatusOnGainCoins`](./Passives_and_Statuses.md#context-statusongaincoins) | Block | Event Trigger: Applies nested statuses when gain coins. | 3 |
| [`StatusOnHealed`](./Passives_and_Statuses.md#context-statusonhealed) | Block | Event Trigger: Applies nested statuses when healed. | 3 |
| [`StatusOnKillEnemy`](./Passives_and_Statuses.md#context-statusonkillenemy) | Block | Event Trigger: Applies nested statuses when kill enemy. | 3 |
| [`StatusOnTookDamageFromAbility`](./Passives_and_Statuses.md#context-statusontookdamagefromability) | Block | Event Trigger: Applies nested statuses when took damage from ability. | 3 |
| `TauntAlways` | Number | Applies the 'TauntAlways' effect. | 3 |
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum/String | Applies the 'TileTrail' effect. | 3 |
| `TrinketActiveEffectsMultiplierBonus` | Number | Applies the 'TrinketActiveEffectsMultiplierBonus' effect. | 3 |
| `TrinketPassiveMultiplierBonus` | Number | Applies the 'TrinketPassiveMultiplierBonus' effect. | 3 |
| `UncappedMana` | Number | Applies the 'UncappedMana' effect. | 3 |
| [`AbilityWhenTaggedCharacterMovesNear`](./Passives_and_Statuses.md#context-abilitywhentaggedcharactermovesnear) | Block | Applies the 'AbilityWhenTaggedCharacterMovesNear' effect. | 2 |
| `AbsorbManaAura` | Number | Applies the 'AbsorbManaAura' effect. | 2 |
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum/String | Applies the 'AddHiddenTag' effect. | 2 |
| `AddInitiative` | Number | Applies the 'AddInitiative' effect. | 2 |
| [`AddPassiveToSpawnedRocks`](./Passives_and_Statuses.md#context-addpassivetospawnedrocks) | Block | Applies the 'AddPassiveToSpawnedRocks' effect. | 2 |
| [`AddPassivesToSummonAbilityMinions`](./Passives_and_Statuses.md#context-addpassivestosummonabilityminions) | Block | Applies the 'AddPassivesToSummonAbilityMinions' effect. | 2 |
| [`AddSelfStatusToWeapons`](./Passives_and_Statuses.md#context-addselfstatustoweapons) | Block | Applies the 'AddSelfStatusToWeapons' effect. | 2 |
| `AddSpellDamage` | Number | Applies the 'AddSpellDamage' effect. | 2 |
| `AddStartingMana` | Number | Applies the 'AddStartingMana' effect. | 2 |
| [`AddStatusToAllDamageAbilities`](./Passives_and_Statuses.md#context-addstatustoalldamageabilities) | Block | Applies the 'AddStatusToAllDamageAbilities' effect. | 2 |
| [`AddStatusToBasicAttackWithCooldown`](./Passives_and_Statuses.md#context-addstatustobasicattackwithcooldown) | Block | Applies the 'AddStatusToBasicAttackWithCooldown' effect. | 2 |
| [`AddStatusToExplosions`](./Passives_and_Statuses.md#context-addstatustoexplosions) | Block | Applies the 'AddStatusToExplosions' effect. | 2 |
| [`AddStatusToFirstBasicAttack`](./Passives_and_Statuses.md#context-addstatustofirstbasicattack) | Block | Applies the 'AddStatusToFirstBasicAttack' effect. | 2 |
| [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage) | Block | Applies the 'AddStatusToMeleeDamage' effect. | 2 |
| [`AddStatusToTrampleDamage`](./Passives_and_Statuses.md#context-addstatustotrampledamage) | Block | Applies the 'AddStatusToTrampleDamage' effect. | 2 |
| `AddUnfilledMaxHealth` | Number | Applies the 'AddUnfilledMaxHealth' effect. | 2 |
| `AddWeaponScaling` | Number | Applies the 'AddWeaponScaling' effect. | 2 |
| [`AfterImage`](./Enums.md#enum-afterimage) | Enum/String | Spawns a visual decoy or shade at the caster's previous location. | 2 |
| `AllowPassTurn` | Number | Applies the 'AllowPassTurn' effect. | 2 |
| [`AllyDamageReaction`](./Enums.md#enum-allydamagereaction) | Enum/String | Applies the 'AllyDamageReaction' effect. | 2 |
| [`AllyHealthRegenAura`](./Passives_and_Statuses.md#context-allyhealthregenaura) | Block | Applies the 'AllyHealthRegenAura' effect. | 2 |
| [`AllyMoveAbilityAura`](./Enums.md#enum-allymoveabilityaura) | Enum/String | Applies the 'AllyMoveAbilityAura' effect. | 2 |
| `AllyMultiplyKnockbackDamage` | Number | Applies the 'AllyMultiplyKnockbackDamage' effect. | 2 |
| [`AlternateCraftingPools`](./Passives_and_Statuses.md#context-alternatecraftingpools) | Block | Applies the 'AlternateCraftingPools' effect. | 2 |
| `AmplifyPositiveStatus` | Number | Applies the 'AmplifyPositiveStatus' effect. | 2 |
| [`ApplyStatusesToRandomEnemiesEachTurn`](./Passives_and_Statuses.md#context-applystatusestorandomenemieseachturn) | Block | Applies the 'ApplyStatusesToRandomEnemiesEachTurn' effect. | 2 |
| `AutoCritLowDamage` | Number | Applies the 'AutoCritLowDamage' effect. | 2 |
| `AutoEquipConsumables` | Number | Applies the 'AutoEquipConsumables' effect. | 2 |
| [`AutocastEachTurn`](./Enums.md#enum-autocasteachturn) | Enum/String | Applies the 'AutocastEachTurn' effect. | 2 |
| `BasicAttackCritChance` | Number | Applies the 'BasicAttackCritChance' effect. | 2 |
| `BasicAttackStatusCarefulness` | Number | Applies the 'BasicAttackStatusCarefulness' effect. | 2 |
| `Bleed` | Number | Applies the 'Bleed' effect. | 2 |
| `BonusFoodEachBattle` | Number | Applies the 'BonusFoodEachBattle' effect. | 2 |
| [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems) | Block | Applies the 'BoobyTrapItems' effect. | 2 |
| `BoostAllyStatsOnDeath` | Number | Applies the 'BoostAllyStatsOnDeath' effect. | 2 |
| [`BouncyProjectiles`](./Passives_and_Statuses.md#context-bouncyprojectiles) | Block | Applies the 'BouncyProjectiles' effect. | 2 |
| `BraceForEachNeighboringEnemy` | Number | Applies the 'BraceForEachNeighboringEnemy' effect. | 2 |
| `CCImmunity` | Number | Applies the 'CCImmunity' effect. | 2 |
| `CapDamageFromAllies` | Number | Applies the 'CapDamageFromAllies' effect. | 2 |
| [`CatAPultAnimation`](./Passives_and_Statuses.md#context-catapultanimation) | Block | Applies the 'CatAPultAnimation' effect. | 2 |
| [`CatchProjectiles`](./Passives_and_Statuses.md#context-catchprojectiles) | Block | Applies the 'CatchProjectiles' effect. | 2 |
| `ChainKnockback` | Number | Applies the 'ChainKnockback' effect. | 2 |
| [`ChanceToBackflip`](./Passives_and_Statuses.md#context-chancetobackflip) | Block | Applies the 'ChanceToBackflip' effect. | 2 |
| `ChanceToBlockAndCounter` | Number | Applies the 'ChanceToBlockAndCounter' effect. | 2 |
| `ChanceToRevive` | Number | Applies the 'ChanceToRevive' effect. | 2 |
| `ChangeTauntPriority` | Number | Applies the 'ChangeTauntPriority' effect. | 2 |
| `CharmAllFlies` | Number | Applies the 'CharmAllFlies' effect. | 2 |
| [`ClassManaCostReduction`](./Passives_and_Statuses.md#context-classmanacostreduction) | Block | Applies the 'ClassManaCostReduction' effect. | 2 |
| `CoinsAddDamage` | Number | Applies the 'CoinsAddDamage' effect. | 2 |
| `CollectPickupsOnBattleEnd` | Number | Applies the 'CollectPickupsOnBattleEnd' effect. | 2 |
| `Conductor` | Number | Applies the 'Conductor' effect. | 2 |
| `ConjureCastSpellsForAllies` | Number | Applies the 'ConjureCastSpellsForAllies' effect. | 2 |
| `ConsumableEffectsMultiplierBonus` | Number | Applies the 'ConsumableEffectsMultiplierBonus' effect. | 2 |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum/String | Applies the 'CounterAttack' effect. | 2 |
| `DamageEnemiesOnHeal` | Number | Combat Trigger: Deals damage to enemies on heal. | 2 |
| `DamageEnemiesOnKill` | Number | Combat Trigger: Deals damage to enemies on kill. | 2 |
| [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell) | Block | Combat Trigger: Deals damage to neighbor tiles when cast spell. | 2 |
| [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#context-damageneighborsaftermove) | Block | Combat Trigger: Deals damage to neighbors after move. | 2 |
| [`DamageReductionAura`](./Passives_and_Statuses.md#context-damagereductionaura) | Block | Combat Trigger: Deals damage to reduction aura. | 2 |
| `DeathChill` | Number | Applies the 'DeathChill' effect. | 2 |
| `DebuffImmunity` | Number | Applies the 'DebuffImmunity' effect. | 2 |
| `DejaVu` | Number | Applies the 'DejaVu' effect. | 2 |
| `DirtyClaws` | Number | Applies the 'DirtyClaws' effect. | 2 |
| `DoubleCastWeapons` | Number | Applies the 'DoubleCastWeapons' effect. | 2 |
| `DukeOfFlies` | Number | Applies the 'DukeOfFlies' effect. | 2 |
| [`Dyslexia`](./Arrays.md#array-dyslexia) | Array | Applies the 'Dyslexia' effect. | 2 |
| [`EMP`](./Passives_and_Statuses.md#context-emp) | Block | Applies the 'EMP' effect. | 2 |
| [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement) | Block | Applies the 'ElementalAttunement' effect. | 2 |
| `Empath` | Number | Applies the 'Empath' effect. | 2 |
| `EnemiesGetPickupsKnockedOut` | Number | Applies the 'EnemiesGetPickupsKnockedOut' effect. | 2 |
| `EnergyStorm` | Number | Applies the 'EnergyStorm' effect. | 2 |
| `EquipmentPassiveMultiplierBonus` | Number | Applies the 'EquipmentPassiveMultiplierBonus' effect. | 2 |
| `EquipmentSetBonusBonus` | Number | Applies the 'EquipmentSetBonusBonus' effect. | 2 |
| [`EscapeSequence`](./Passives_and_Statuses.md#context-escapesequence) | Block | Applies the 'EscapeSequence' effect. | 2 |
| [`Eternal`](./Passives_and_Statuses.md#context-eternal) | Block | Applies the 'Eternal' effect. | 2 |
| `ExplodeOverkilledEnemies` | Number | Applies the 'ExplodeOverkilledEnemies' effect. | 2 |
| [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#context-extrastatuswhendealingdamage) | Block | Applies the 'ExtraStatusWhenDealingDamage' effect. | 2 |
| `FaceShield` | Number | Applies the 'FaceShield' effect. | 2 |
| `FamiliarSecondaryDamageImmunity` | Number | Applies the 'FamiliarSecondaryDamageImmunity' effect. | 2 |
| `FlowerPowerAuraBrace` | Number | Applies the 'FlowerPowerAuraBrace' effect. | 2 |
| `FlowerPowerAuraStrength` | Number | Applies the 'FlowerPowerAuraStrength' effect. | 2 |
| `FlowersOnEndTurn` | Number | Applies the 'FlowersOnEndTurn' effect. | 2 |
| `FlyDamageIncrease` | Number | Applies the 'FlyDamageIncrease' effect. | 2 |
| `Flying` | Number | Applies the 'Flying' effect. | 2 |
| [`FollowUp`](./Enums.md#enum-followup) | Enum/String | Applies the 'FollowUp' effect. | 2 |
| `FullHealthCritChance` | Number | Applies the 'FullHealthCritChance' effect. | 2 |
| `FullPower` | Number | Applies the 'FullPower' effect. | 2 |
| `GainExtraShield` | Number | Applies the 'GainExtraShield' effect. | 2 |
| [`GravityWell`](./Passives_and_Statuses.md#context-gravitywell) | Block | Applies the 'GravityWell' effect. | 2 |
| `HeadArmorPassiveMultiplierBonus` | Number | Applies the 'HeadArmorPassiveMultiplierBonus' effect. | 2 |
| `HealDamagesEnemies` | Number | Applies the 'HealDamagesEnemies' effect. | 2 |
| `HealsAlsoRegenMana` | Number | Applies the 'HealsAlsoRegenMana' effect. | 2 |
| `HealsCanRevive` | Number | Applies the 'HealsCanRevive' effect. | 2 |
| [`HolyShieldTransferToTaggedMinions`](./Enums.md#enum-holyshieldtransfertotaggedminions) | Enum/String | Applies the 'HolyShieldTransferToTaggedMinions' effect. | 2 |
| `ImmortalLeeches` | Number | Applies the 'ImmortalLeeches' effect. | 2 |
| `IncreaseExplosionSize` | Number | Applies the 'IncreaseExplosionSize' effect. | 2 |
| `IncreaseHealingSpellRange` | Number | Applies the 'IncreaseHealingSpellRange' effect. | 2 |
| `IncreaseSpellRange` | Number | Applies the 'IncreaseSpellRange' effect. | 2 |
| [`InfiniteRebirth`](./Passives_and_Statuses.md#context-infiniterebirth) | Block | Applies the 'InfiniteRebirth' effect. | 2 |
| `KillsHeal` | Number | Applies the 'KillsHeal' effect. | 2 |
| [`KillsToMeat`](./Enums.md#enum-killstomeat) | Enum/String | Applies the 'KillsToMeat' effect. | 2 |
| [`LateBloomer`](./Passives_and_Statuses.md#context-latebloomer) | Block | Applies the 'LateBloomer' effect. | 2 |
| `LightningAspectCharge` | Number | Applies the 'LightningAspectCharge' effect. | 2 |
| [`LightningRod`](./Passives_and_Statuses.md#context-lightningrod) | Block | Applies the 'LightningRod' effect. | 2 |
| [`LineOfSightTrueSightAura`](./Enums.md#enum-lineofsighttruesightaura) | Enum/String | Applies the 'LineOfSightTrueSightAura' effect. | 2 |
| `LobbedHook` | Number | Applies the 'LobbedHook' effect. | 2 |
| [`LowHealthAllyDodgeChanceAura`](./Passives_and_Statuses.md#context-lowhealthallydodgechanceaura) | Block | Applies the 'LowHealthAllyDodgeChanceAura' effect. | 2 |
| `MakeBasicAttackPassThroughThings` | Number | Applies the 'MakeBasicAttackPassThroughThings' effect. | 2 |
| `ManaRegenMultiplierIfManaEmpty` | Number | Applies the 'ManaRegenMultiplierIfManaEmpty' effect. | 2 |
| `MegaMinions` | Number | Applies the 'MegaMinions' effect. | 2 |
| `Metal` | Number | Applies the 'Metal' effect. | 2 |
| `MetalDetector` | Number | Applies the 'MetalDetector' effect. | 2 |
| `MinimumTech` | Number | Applies the 'MinimumTech' effect. | 2 |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum/String | Applies the 'MoveAndUseAbilityEachTurnBeginIfPossible' effect. | 2 |
| [`MovementReaction`](./Passives_and_Statuses.md#context-movementreaction) | Block | Applies the 'MovementReaction' effect. | 2 |
| `NoReflection` | Number | Applies the 'NoReflection' effect. | 2 |
| `NubbyTossPriority` | Number | Applies the 'NubbyTossPriority' effect. | 2 |
| `NumbingLeeches` | Number | Applies the 'NumbingLeeches' effect. | 2 |
| `OverhealGainsBothShield` | Number | Applies the 'OverhealGainsBothShield' effect. | 2 |
| [`OverrideBasicAttack`](./Enums.md#enum-overridebasicattack) | Enum/String | Applies the 'OverrideBasicAttack' effect. | 2 |
| `ParasitesArentCursed` | Number | Applies the 'ParasitesArentCursed' effect. | 2 |
| [`PassiveAfterXKills`](./Passives_and_Statuses.md#context-passiveafterxkills) | Block | Applies the 'PassiveAfterXKills' effect. | 2 |
| [`PassiveAtFullHealth`](./Passives_and_Statuses.md#context-passiveatfullhealth) | Block | Applies the 'PassiveAtFullHealth' effect. | 2 |
| [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#context-passiveatinjurythreshold) | Block | Applies the 'PassiveAtInjuryThreshold' effect. | 2 |
| [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell) | Block | Applies the 'PassiveUntilCastSpell' effect. | 2 |
| [`PassiveUntilGetKill`](./Passives_and_Statuses.md#context-passiveuntilgetkill) | Block | Applies the 'PassiveUntilGetKill' effect. | 2 |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement) | Block | State Trigger: Grants nested passives when affected by element. | 2 |
| [`PassiveWhenTheAlpha`](./Passives_and_Statuses.md#context-passivewhenthealpha) | Block | State Trigger: Grants nested passives when the alpha. | 2 |
| [`PassiveWhileInMonkMeleeStance`](./Passives_and_Statuses.md#context-passivewhileinmonkmeleestance) | Block | Applies the 'PassiveWhileInMonkMeleeStance' effect. | 2 |
| [`PassiveWhileInMonkRangedStance`](./Passives_and_Statuses.md#context-passivewhileinmonkrangedstance) | Block | Applies the 'PassiveWhileInMonkRangedStance' effect. | 2 |
| [`PassiveWhilePreviewingMonkRangedStance`](./Passives_and_Statuses.md#context-passivewhilepreviewingmonkrangedstance) | Block | Applies the 'PassiveWhilePreviewingMonkRangedStance' effect. | 2 |
| [`PassiveWhileWearingMetal`](./Passives_and_Statuses.md#context-passivewhilewearingmetal) | Block | Applies the 'PassiveWhileWearingMetal' effect. | 2 |
| `PermanentItems` | Number | Applies the 'PermanentItems' effect. | 2 |
| `PoisonThorns` | Number | Applies the 'PoisonThorns' effect. | 2 |
| [`ProtectTargetedAllies`](./Enums.md#enum-protecttargetedallies) | Enum/String | Applies the 'ProtectTargetedAllies' effect. | 2 |
| `Quiver` | Number | Applies the 'Quiver' effect. | 2 |
| `RangedTrueShot` | Number | Applies the 'RangedTrueShot' effect. | 2 |
| `RemoveLineOfSightRestrictions` | Number | Applies the 'RemoveLineOfSightRestrictions' effect. | 2 |
| `RemoveOncePerFightRestriction` | Number | Applies the 'RemoveOncePerFightRestriction' effect. | 2 |
| [`ReplaceBasicAttackWhenDead`](./Enums.md#enum-replacebasicattackwhendead) | Enum/String | Applies the 'ReplaceBasicAttackWhenDead' effect. | 2 |
| `ReviveOnWin` | Number | Applies the 'ReviveOnWin' effect. | 2 |
| `RobotsInheritArmor` | Number | Applies the 'RobotsInheritArmor' effect. | 2 |
| `RockDetector` | Number | Applies the 'RockDetector' effect. | 2 |
| [`ScaledStatusOnOverMana`](./Passives_and_Statuses.md#context-scaledstatusonovermana) | Block | Applies the 'ScaledStatusOnOverMana' effect. | 2 |
| [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#context-scaledstatusonspendmana) | Block | Applies the 'ScaledStatusOnSpendMana' effect. | 2 |
| [`SecurityBotProtect`](./Passives_and_Statuses.md#context-securitybotprotect) | Block | Applies the 'SecurityBotProtect' effect. | 2 |
| `ShareHealthRegen` | Number | Applies the 'ShareHealthRegen' effect. | 2 |
| `SharePickups` | Number | Applies the 'SharePickups' effect. | 2 |
| `ShoulderCheck` | Number | Applies the 'ShoulderCheck' effect. | 2 |
| [`ShovingMatch`](./Enums.md#enum-shovingmatch) | Enum/String | Applies the 'ShovingMatch' effect. | 2 |
| `ShowHiddenThings` | Number | Applies the 'ShowHiddenThings' effect. | 2 |
| `SmallEnemiesIgnoreYou` | Number | Applies the 'SmallEnemiesIgnoreYou' effect. | 2 |
| [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#context-smiteenemieswhokill) | Block | Applies the 'SmiteEnemiesWhoKill' effect. | 2 |
| [`SpawnObjectOnPopCorpse`](./Enums.md#enum-spawnobjectonpopcorpse) | Enum/String | Applies the 'SpawnObjectOnPopCorpse' effect. | 2 |
| [`SpecialFriends`](./Passives_and_Statuses.md#context-specialfriends) | Block | Applies the 'SpecialFriends' effect. | 2 |
| `SpeedUp` | Number | Applies the 'SpeedUp' effect. | 2 |
| `SplittableMove` | Number | Applies the 'SplittableMove' effect. | 2 |
| `SpreadExtraDebuffs` | Number | Applies the 'SpreadExtraDebuffs' effect. | 2 |
| `SpreadPainBonus` | Number | Applies the 'SpreadPainBonus' effect. | 2 |
| `StatMinimum` | Number | Applies the 'StatMinimum' effect. | 2 |
| [`StatsAtLowHealth`](./Passives_and_Statuses.md#context-statsatlowhealth) | Block | Applies the 'StatsAtLowHealth' effect. | 2 |
| [`StatusAfterCastSpell`](./Passives_and_Statuses.md#context-statusaftercastspell) | Block | Event Trigger: Applies nested statuses to after cast spell. | 2 |
| [`StatusAlliesOnBattleStart`](./Passives_and_Statuses.md#context-statusalliesonbattlestart) | Block | Event Trigger: Applies nested statuses to allies on battle start. | 2 |
| [`StatusAlliesOnGainCoins`](./Passives_and_Statuses.md#context-statusalliesongaincoins) | Block | Event Trigger: Applies nested statuses to allies on gain coins. | 2 |
| [`StatusAlliesOnKill`](./Passives_and_Statuses.md#context-statusalliesonkill) | Block | Event Trigger: Applies nested statuses to allies on kill. | 2 |
| [`StatusAllyWhenAllySpendsMana`](./Passives_and_Statuses.md#context-statusallywhenallyspendsmana) | Block | Event Trigger: Applies nested statuses to ally when ally spends mana. | 2 |
| [`StatusAnyCatAllyWhoKills`](./Passives_and_Statuses.md#context-statusanycatallywhokills) | Block | Event Trigger: Applies nested statuses to any cat ally who kills. | 2 |
| [`StatusDamagers`](./Passives_and_Statuses.md#context-statusdamagers) | Block | Event Trigger: Applies nested statuses to damagers. | 2 |
| [`StatusEachTurnEndForEachTurn`](./Passives_and_Statuses.md#context-statuseachturnendforeachturn) | Block | Event Trigger: Applies nested statuses to each turn end for each turn. | 2 |
| [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#context-statuseachturnendperenemykill) | Block | Event Trigger: Applies nested statuses to each turn end per enemy kill. | 2 |
| [`StatusEnemiesOnDeath`](./Passives_and_Statuses.md#context-statusenemiesondeath) | Block | Event Trigger: Applies nested statuses to enemies on death. | 2 |
| [`StatusEveryXTurnBegins`](./Passives_and_Statuses.md#context-statuseveryxturnbegins) | Block | Event Trigger: Applies nested statuses to every x turn begins. | 2 |
| [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers) | Block | Instantly kills the target if they possess the specified status effects. | 2 |
| [`StatusOnAnyDeath`](./Passives_and_Statuses.md#context-statusonanydeath) | Block | Event Trigger: Applies nested statuses when any death. | 2 |
| [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#context-statusonbattleendifkillthresholdmet) | Block | Event Trigger: Applies nested statuses when battle end if kill threshold met. | 2 |
| [`StatusOnBreakItem`](./Passives_and_Statuses.md#context-statusonbreakitem) | Block | Event Trigger: Applies nested statuses when break item. | 2 |
| [`StatusOnCollectPickup`](./Passives_and_Statuses.md#context-statusoncollectpickup) | Block | Event Trigger: Applies nested statuses when collect pickup. | 2 |
| [`StatusOnDealtDamage`](./Passives_and_Statuses.md#context-statusondealtdamage) | Block | Event Trigger: Applies nested statuses when dealt damage. | 2 |
| [`StatusOnDealtDamageThreshold`](./Passives_and_Statuses.md#context-statusondealtdamagethreshold) | Block | Event Trigger: Applies nested statuses when dealt damage threshold. | 2 |
| [`StatusOnEndMove`](./Passives_and_Statuses.md#context-statusonendmove) | Block | Event Trigger: Applies nested statuses when end move. | 2 |
| [`StatusOnGainShield`](./Passives_and_Statuses.md#context-statusongainshield) | Block | Event Trigger: Applies nested statuses when gain shield. | 2 |
| [`StatusOnHeal`](./Passives_and_Statuses.md#context-statusonheal) | Block | Event Trigger: Applies nested statuses when heal. | 2 |
| [`StatusOnOverMana`](./Passives_and_Statuses.md#context-statusonovermana) | Block | Event Trigger: Applies nested statuses when over mana. | 2 |
| [`StatusOnPickupCoins`](./Passives_and_Statuses.md#context-statusonpickupcoins) | Block | Event Trigger: Applies nested statuses when pickup coins. | 2 |
| [`StatusOnPopCorpse`](./Passives_and_Statuses.md#context-statusonpopcorpse) | Block | Event Trigger: Applies nested statuses when pop corpse. | 2 |
| [`StatusOnTookDamageFromEnemyAbility`](./Passives_and_Statuses.md#context-statusontookdamagefromenemyability) | Block | Event Trigger: Applies nested statuses when took damage from enemy ability. | 2 |
| [`StatusOnTriggerTrap`](./Passives_and_Statuses.md#context-statusontriggertrap) | Block | Event Trigger: Applies nested statuses when trigger trap. | 2 |
| [`StatusOnUseBasicAttack`](./Passives_and_Statuses.md#context-statusonusebasicattack) | Block | Event Trigger: Applies nested statuses when use basic attack. | 2 |
| [`StatusOnUseElementAbility`](./Passives_and_Statuses.md#context-statusonuseelementability) | Block | Event Trigger: Applies nested statuses when use element ability. | 2 |
| [`StatusPerInjury`](./Passives_and_Statuses.md#context-statusperinjury) | Block | Event Trigger: Applies nested statuses to per injury. | 2 |
| [`StatusReplacement`](./Arrays.md#array-statusreplacement) | Array | Event Trigger: Applies nested statuses to replacement. | 2 |
| [`StatusThingsKnockedBack`](./Passives_and_Statuses.md#context-statusthingsknockedback) | Block | Event Trigger: Applies nested statuses to things knocked back. | 2 |
| [`StatusWhenAllySpendsMana`](./Passives_and_Statuses.md#context-statuswhenallyspendsmana) | Block | Event Trigger: Applies nested statuses to when ally spends mana. | 2 |
| `Stealth` | Number | Applies the 'Stealth' effect. | 2 |
| `StrengthForEachNeighboringEnemy` | Number | Applies the 'StrengthForEachNeighboringEnemy' effect. | 2 |
| `StrengthInNumbersAura` | Number | Applies the 'StrengthInNumbersAura' effect. | 2 |
| `StrengthUp` | Number | Applies the 'StrengthUp' effect. | 2 |
| `Study` | Number | Applies the 'Study' effect. | 2 |
| [`TaggedPickupEffectReplacement`](./Passives_and_Statuses.md#context-taggedpickupeffectreplacement) | Block | Applies the 'TaggedPickupEffectReplacement' effect. | 2 |
| `Tech` | Number | Applies the 'Tech' effect. | 2 |
| `TileDamageMultiplier` | Number | Applies the 'TileDamageMultiplier' effect. | 2 |
| [`TowerDefense`](./Passives_and_Statuses.md#context-towerdefense) | Block | Applies the 'TowerDefense' effect. | 2 |
| [`TowerDefenseReflex`](./Enums.md#enum-towerdefensereflex) | Enum/String | Applies the 'TowerDefenseReflex' effect. | 2 |
| `TrapEffectsMultiplier` | Number | Applies the 'TrapEffectsMultiplier' effect. | 2 |
| `UncappedHP` | Number | Applies the 'UncappedHP' effect. | 2 |
| [`UpgradeLevelUpClassActives`](./Enums.md#enum-upgradelevelupclassactives) | Enum/String | Applies the 'UpgradeLevelUpClassActives' effect. | 2 |
| [`UpgradeLevelUpClassPassives`](./Enums.md#enum-upgradelevelupclasspassives) | Enum/String | Applies the 'UpgradeLevelUpClassPassives' effect. | 2 |
| `UpgradeSpawnedPickups` | Number | Applies the 'UpgradeSpawnedPickups' effect. | 2 |
| `Vengeful` | Number | Applies the 'Vengeful' effect. | 2 |
| `WaterWalk` | Number | Applies the 'WaterWalk' effect. | 2 |
| `Weakness` | Number | Applies the 'Weakness' effect. | 2 |
| `WeaponCountsAsBasicAttack` | Number | Applies the 'WeaponCountsAsBasicAttack' effect. | 2 |
| `WeaponDamageMultiplierBonus` | Number | Applies the 'WeaponDamageMultiplierBonus' effect. | 2 |
| [`AbilityChargeRefundChance`](./Passives_and_Statuses.md#context-abilitychargerefundchance) | Block | Applies the 'AbilityChargeRefundChance' effect. | 1 |
| `AddAllyNeighborsToAbilityRange` | Number | Applies the 'AddAllyNeighborsToAbilityRange' effect. | 1 |
| `AddAllyNeighborsToAttackRange` | Number | Applies the 'AddAllyNeighborsToAttackRange' effect. | 1 |
| `AddChaScalingSpellDamage` | Number | Applies the 'AddChaScalingSpellDamage' effect. | 1 |
| `AddKnockbackToEverything` | Number | Applies the 'AddKnockbackToEverything' effect. | 1 |
| `AddLevelUpStatMultiplier` | Number | Applies the 'AddLevelUpStatMultiplier' effect. | 1 |
| `AddRangedCritChance` | Number | Applies the 'AddRangedCritChance' effect. | 1 |
| [`AddStatusToKnockbackDamage`](./Passives_and_Statuses.md#context-addstatustoknockbackdamage) | Block | Applies the 'AddStatusToKnockbackDamage' effect. | 1 |
| [`AddStatusToReceivedDamage_ExcludeStatuses`](./Passives_and_Statuses.md#context-addstatustoreceiveddamage_excludestatuses) | Block | Applies the 'AddStatusToReceivedDamage_ExcludeStatuses' effect. | 1 |
| [`AddStatusToSpells`](./Passives_and_Statuses.md#context-addstatustospells) | Block | Applies the 'AddStatusToSpells' effect. | 1 |
| [`AddStatusesIfPersistentWeatherElement`](./Passives_and_Statuses.md#context-addstatusesifpersistentweatherelement) | Block | Applies the 'AddStatusesIfPersistentWeatherElement' effect. | 1 |
| [`AddStatusesToReceivedElementalDamage`](./Passives_and_Statuses.md#context-addstatusestoreceivedelementaldamage) | Block | Applies the 'AddStatusesToReceivedElementalDamage' effect. | 1 |
| [`AddTemporaryEffectsToEquipment`](./Passives_and_Statuses.md#context-addtemporaryeffectstoequipment) | Block | Applies the 'AddTemporaryEffectsToEquipment' effect. | 1 |
| `AllDamageCrits` | Number | Applies the 'AllDamageCrits' effect. | 1 |
| `AlliesAvoidTraps` | Number | Applies the 'AlliesAvoidTraps' effect. | 1 |
| `AllyChainKnockback` | Number | Applies the 'AllyChainKnockback' effect. | 1 |
| `AllyMultiplyKnockbackDistance` | Number | Applies the 'AllyMultiplyKnockbackDistance' effect. | 1 |
| `AllyUncappedHPAura` | Number | Applies the 'AllyUncappedHPAura' effect. | 1 |
| `AlphaCat` | Number | Applies the 'AlphaCat' effect. | 1 |
| `AmplifyNegativeStatus` | Number | Applies the 'AmplifyNegativeStatus' effect. | 1 |
| `ArmorDodgeChance` | Number | Applies the 'ArmorDodgeChance' effect. | 1 |
| [`Autism`](./Passives_and_Statuses.md#context-autism) | Block | Applies the 'Autism' effect. | 1 |
| `BackstabImmunity` | Number | Applies the 'BackstabImmunity' effect. | 1 |
| `BackstabWeakness` | Number | Applies the 'BackstabWeakness' effect. | 1 |
| [`BasicAttackStatusSwap`](./Arrays.md#array-basicattackstatusswap) | Array | Applies the 'BasicAttackStatusSwap' effect. | 1 |
| [`BlacklistPickupType`](./Enums.md#enum-blacklistpickuptype) | Enum/String | Applies the 'BlacklistPickupType' effect. | 1 |
| `BleedThorns` | Number | Applies the 'BleedThorns' effect. | 1 |
| `BonusHealthRegenBasedOnDex` | Number | Applies the 'BonusHealthRegenBasedOnDex' effect. | 1 |
| `BonusRangeBasedOnDex` | Number | Applies the 'BonusRangeBasedOnDex' effect. | 1 |
| `BoostDamageAura` | Number | Applies the 'BoostDamageAura' effect. | 1 |
| `BoostDamageGlobalAura` | Number | Applies the 'BoostDamageGlobalAura' effect. | 1 |
| `BoostRangeAura` | Number | Applies the 'BoostRangeAura' effect. | 1 |
| `BoostRangeGlobalAura` | Number | Applies the 'BoostRangeGlobalAura' effect. | 1 |
| `BuffImmunity` | Number | Applies the 'BuffImmunity' effect. | 1 |
| `Burn` | Number | Applies the 'Burn' effect. | 1 |
| `CanRemoveCursedItems` | Number | Applies the 'CanRemoveCursedItems' effect. | 1 |
| `CantDodge` | Number | Applies the 'CantDodge' effect. | 1 |
| `CapMovementAbilityRange` | Number | Applies the 'CapMovementAbilityRange' effect. | 1 |
| `CapTechSpent` | Number | Applies the 'CapTechSpent' effect. | 1 |
| `ConductorManaRegen` | Number | Applies the 'ConductorManaRegen' effect. | 1 |
| [`ConfusionEffectOnTaggedAbilities`](./Enums.md#enum-confusioneffectontaggedabilities) | Enum/String | Applies the 'ConfusionEffectOnTaggedAbilities' effect. | 1 |
| `ConsumablesMeleeRange` | Number | Applies the 'ConsumablesMeleeRange' effect. | 1 |
| [`DamageIfDidntUseSpecificAbility`](./Passives_and_Statuses.md#context-damageifdidntusespecificability) | Block | Combat Trigger: Deals damage to if didnt use specific ability. | 1 |
| `DepressionAura` | Number | Applies the 'DepressionAura' effect. | 1 |
| [`Diabetes`](./Passives_and_Statuses.md#context-diabetes) | Block | Applies the 'Diabetes' effect. | 1 |
| [`DisableAbilities`](./Enums.md#enum-disableabilities) | Enum/String | Applies the 'DisableAbilities' effect. | 1 |
| [`DisableAbilitiesWithTag`](./Enums.md#enum-disableabilitieswithtag) | Enum/String | Applies the 'DisableAbilitiesWithTag' effect. | 1 |
| `Doomed` | Number | Applies the 'Doomed' effect. | 1 |
| `EachSpellFreeAtFullMana` | Number | Applies the 'EachSpellFreeAtFullMana' effect. | 1 |
| [`EquipRandomTemporaryItemFromPool`](./Enums.md#enum-equiprandomtemporaryitemfrompool) | Enum/String | Applies the 'EquipRandomTemporaryItemFromPool' effect. | 1 |
| `ExhaustionRoundChange` | Number | Applies the 'ExhaustionRoundChange' effect. | 1 |
| `ExplosionImmunity` | Number | Applies the 'ExplosionImmunity' effect. | 1 |
| `ExtraBasicMoves_Status` | Number | Applies the 'ExtraBasicMoves_Status' effect. | 1 |
| `ExtraInjuryOnDeath` | Number | Applies the 'ExtraInjuryOnDeath' effect. | 1 |
| `ExtraTrinketUses` | Number | Applies the 'ExtraTrinketUses' effect. | 1 |
| `FaceArmorPassiveMultiplierBonus` | Number | Applies the 'FaceArmorPassiveMultiplierBonus' effect. | 1 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Applies the 'ForceUseAbility' effect. | 1 |
| `FreeSpellsAtFullMana` | Number | Applies the 'FreeSpellsAtFullMana' effect. | 1 |
| `FrontstabBasicAttackCritChance` | Number | Applies the 'FrontstabBasicAttackCritChance' effect. | 1 |
| `FrontstabCritChance` | Number | Applies the 'FrontstabCritChance' effect. | 1 |
| `FullHeal` | Number | Applies the 'FullHeal' effect. | 1 |
| `FullHealthAllStatsUp` | Number | Applies the 'FullHealthAllStatsUp' effect. | 1 |
| `FullHealthManaRegen` | Number | Applies the 'FullHealthManaRegen' effect. | 1 |
| [`FurnitureStats`](./Passives_and_Statuses.md#context-furniturestats) | Block | Applies the 'FurnitureStats' effect. | 1 |
| `GrassTileHealing` | Number | Applies the 'GrassTileHealing' effect. | 1 |
| `HPGainBlock` | Number | Applies the 'HPGainBlock' effect. | 1 |
| `HealAtStart` | Number | Applies the 'HealAtStart' effect. | 1 |
| `HealingAura` | Number | Applies the 'HealingAura' effect. | 1 |
| `HolyDamageMultiplierBonus` | Number | Applies the 'HolyDamageMultiplierBonus' effect. | 1 |
| `HouseFoodRequirementMultiplier` | Number | Applies the 'HouseFoodRequirementMultiplier' effect. | 1 |
| `Hypomania` | Number | Applies the 'Hypomania' effect. | 1 |
| `IncreaseItemUsesOnEquip` | Number | Applies the 'IncreaseItemUsesOnEquip' effect. | 1 |
| `InjuryImmunity` | Number | Applies the 'InjuryImmunity' effect. | 1 |
| `InvertBrainFaction` | Number | Applies the 'InvertBrainFaction' effect. | 1 |
| `LimitDamage` | Number | Applies the 'LimitDamage' effect. | 1 |
| `LimitHeal` | Number | Applies the 'LimitHeal' effect. | 1 |
| `LimitSelfKnockbackDamage` | Number | Applies the 'LimitSelfKnockbackDamage' effect. | 1 |
| [`LimitedTileTrail`](./Enums.md#enum-limitedtiletrail) | Enum/String | Applies the 'LimitedTileTrail' effect. | 1 |
| `Madness` | Number | Applies the Madness debuff/status effect. | 1 |
| `ManaCostReduction` | Number | Applies the 'ManaCostReduction' effect. | 1 |
| `MaxAccuracy` | Number | Applies the 'MaxAccuracy' effect. | 1 |
| `MaxStartingMana` | Number | Applies the 'MaxStartingMana' effect. | 1 |
| [`MoveAwayFromDamageSource`](./Enums.md#enum-moveawayfromdamagesource) | Enum/String | Applies the 'MoveAwayFromDamageSource' effect. | 1 |
| `MoveRandomly` | Number | Applies the 'MoveRandomly' effect. | 1 |
| [`MoveSpeedMultiplier`](./Enums.md#enum-movespeedmultiplier) | Enum/String | Applies the 'MoveSpeedMultiplier' effect. | 1 |
| [`MoveWhenDamaged`](./Passives_and_Statuses.md#context-movewhendamaged) | Block | Applies the 'MoveWhenDamaged' effect. | 1 |
| `NeckArmorPassiveMultiplierBonus` | Number | Applies the 'NeckArmorPassiveMultiplierBonus' effect. | 1 |
| `NoManaRegen` | Number | Applies the 'NoManaRegen' effect. | 1 |
| `OverrideMaxHealth` | Number | Applies the 'OverrideMaxHealth' effect. | 1 |
| `OverrideMaxMana` | Number | Applies the 'OverrideMaxMana' effect. | 1 |
| `OverridePalette` | Number | Applies the 'OverridePalette' effect. | 1 |
| [`Paranoia`](./Enums.md#enum-paranoia) | Enum/String | Applies the 'Paranoia' effect. | 1 |
| [`PassiveLevelScaledStatus`](./Passives_and_Statuses.md#context-passivelevelscaledstatus) | Block | Applies the 'PassiveLevelScaledStatus' effect. | 1 |
| `PermanentImmobile` | Number | Applies the 'PermanentImmobile' effect. | 1 |
| `PermanentKitten` | Number | Applies the 'PermanentKitten' effect. | 1 |
| `PermanentMadness` | Number | Applies the 'PermanentMadness' effect. | 1 |
| `Phasing` | Number | Applies the 'Phasing' effect. | 1 |
| `Poison` | Number | Applies the 'Poison' effect. | 1 |
| `PoisonMultiplier` | Number | Applies the 'PoisonMultiplier' effect. | 1 |
| [`PoopWhenHit`](./Enums.md#enum-poopwhenhit) | Enum/String | Applies the 'PoopWhenHit' effect. | 1 |
| [`RandomPassivePool`](./Passives_and_Statuses.md#context-randompassivepool) | Block | Applies the 'RandomPassivePool' effect. | 1 |
| `RealTimePressure_OneUnit` | Number | Applies the 'RealTimePressure_OneUnit' effect. | 1 |
| [`ReceivedStatusReplacement`](./Arrays.md#array-receivedstatusreplacement) | Array | Applies the 'ReceivedStatusReplacement' effect. | 1 |
| `RefreshMoveOnWeaponConnect` | Number | Applies the 'RefreshMoveOnWeaponConnect' effect. | 1 |
| [`ReplaceBrain`](./Passives_and_Statuses.md#context-replacebrain) | Block | Applies the 'ReplaceBrain' effect. | 1 |
| [`ReplaceSpellsWhenDead`](./Enums.md#enum-replacespellswhendead) | Enum/String | Applies the 'ReplaceSpellsWhenDead' effect. | 1 |
| [`Robot`](./Passives_and_Statuses.md#context-robot) | Block | Applies the 'Robot' effect. | 1 |
| `SafeExplosions` | Number | Applies the 'SafeExplosions' effect. | 1 |
| [`ScaledStatusOnBleedDamage`](./Passives_and_Statuses.md#context-scaledstatusonbleeddamage) | Block | Applies the 'ScaledStatusOnBleedDamage' effect. | 1 |
| [`ScaledStatusOnLoseShield`](./Passives_and_Statuses.md#context-scaledstatusonloseshield) | Block | Applies the 'ScaledStatusOnLoseShield' effect. | 1 |
| [`ScaledStatusOnOverHealed`](./Passives_and_Statuses.md#context-scaledstatusonoverhealed) | Block | Applies the 'ScaledStatusOnOverHealed' effect. | 1 |
| `SchrodingerDisorder` | Number | Applies the 'SchrodingerDisorder' effect. | 1 |
| `Scleroderma` | Number | Applies the 'Scleroderma' effect. | 1 |
| [`SelfDamageWhenDealDamage`](./Passives_and_Statuses.md#context-selfdamagewhendealdamage) | Block | Applies the 'SelfDamageWhenDealDamage' effect. | 1 |
| [`SetDefaultFacePassive`](./Enums.md#enum-setdefaultfacepassive) | Enum/String | Applies the 'SetDefaultFacePassive' effect. | 1 |
| `Slow` | Number | Applies the 'Slow' effect. | 1 |
| `SmallRockBehavior` | Number | Applies the 'SmallRockBehavior' effect. | 1 |
| `SpawnCreepOnHit` | Number | Applies the 'SpawnCreepOnHit' effect. | 1 |
| [`SpawnMeatOnMove`](./Enums.md#enum-spawnmeatonmove) | Enum/String | Applies the 'SpawnMeatOnMove' effect. | 1 |
| `SpreadPainBonusCrit` | Number | Applies the 'SpreadPainBonusCrit' effect. | 1 |
| [`StackingDodgeChanceOnTookDamage`](./Passives_and_Statuses.md#context-stackingdodgechanceontookdamage) | Block | Applies the 'StackingDodgeChanceOnTookDamage' effect. | 1 |
| [`StatusAdjacentOnTheirTurnBegin`](./Passives_and_Statuses.md#context-statusadjacentontheirturnbegin) | Block | Event Trigger: Applies nested statuses to adjacent on their turn begin. | 1 |
| [`StatusAlliesOnSpendMana`](./Passives_and_Statuses.md#context-statusalliesonspendmana) | Block | Event Trigger: Applies nested statuses to allies on spend mana. | 1 |
| [`StatusAlliesScaledByCursedOnDeath`](./Passives_and_Statuses.md#context-statusalliesscaledbycursedondeath) | Block | Event Trigger: Applies nested statuses to allies scaled by cursed on death. | 1 |
| `StatusCarefulness` | Number | Event Trigger: Applies nested statuses to carefulness. | 1 |
| [`StatusIfBattleAlreadyBegan`](./Passives_and_Statuses.md#context-statusifbattlealreadybegan) | Block | Event Trigger: Applies nested statuses to if battle already began. | 1 |
| [`StatusOnEatPill`](./Passives_and_Statuses.md#context-statusoneatpill) | Block | Event Trigger: Applies nested statuses when eat pill. | 1 |
| [`StatusOnLoseShield`](./Passives_and_Statuses.md#context-statusonloseshield) | Block | Event Trigger: Applies nested statuses when lose shield. | 1 |
| [`StatusOnTakeHealthDamage`](./Passives_and_Statuses.md#context-statusontakehealthdamage) | Block | Event Trigger: Applies nested statuses when take health damage. | 1 |
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](./Passives_and_Statuses.md#context-statusonturnendifdidntcastabilitytypes) | Block | Event Trigger: Applies nested statuses when turn end if didnt cast ability types. | 1 |
| `StrictLimitDamage` | Number | Applies the 'StrictLimitDamage' effect. | 1 |
| `TauntAtFullHealth` | Number | Applies the 'TauntAtFullHealth' effect. | 1 |
| `TempInitiativeChange` | Number | Applies the 'TempInitiativeChange' effect. | 1 |
| [`TheHunger`](./Passives_and_Statuses.md#context-thehunger) | Block | Applies the 'TheHunger' effect. | 1 |
| [`TourettesMeows`](./Passives_and_Statuses.md#context-tourettesmeows) | Block | Applies the 'TourettesMeows' effect. | 1 |
| `Triskaidekaphobia` | Number | Applies the 'Triskaidekaphobia' effect. | 1 |
| `UncappedHPBonusStr` | Number | Applies the 'UncappedHPBonusStr' effect. | 1 |
| `Vegan` | Number | Applies the 'Vegan' effect. | 1 |
| `WeaponActiveEffectsMultiplierBonus` | Number | Applies the 'WeaponActiveEffectsMultiplierBonus' effect. | 1 |
| `WeaponPassiveMultiplierBonus` | Number | Applies the 'WeaponPassiveMultiplierBonus' effect. | 1 |
| `WeaponsDontLoseDurability` | Number | Applies the 'WeaponsDontLoseDurability' effect. | 1 |
| `WobblyCat` | Number | Applies the 'WobblyCat' effect. | 1 |

</details>

---

### Context: `stats`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Passives_and_Statuses.md#context-1), [`2`](./Passives_and_Statuses.md#context-2), [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count (X/48) |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 48 |
| `spd` | Number |  | 41 |
| `cha` | Number |  | 33 |
| `int` | Number |  | 32 |
| `str` | Number |  | 31 |
| `dex` | Number |  | 23 |
| `lck` | Number |  | 21 |

</details>

---

### Context: `lock_item_slot`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count (X/16) |
| :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum/String |  | 16 |
| `frame` | Number |  | 3 |

</details>

---

### Context: `SpawnOnBattleStart`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/14) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 14 |
| `number` | Number |  | 13 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToCharmed`](./Passives_and_Statuses.md#context-addpassivestocharmed), [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#context-passivewhenatfullmana), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| `Poison` | Number | Applies the 'Poison' effect. | 12 |
| `Bleed` | Number | Applies the 'Bleed' effect. | 8 |
| `Knockback` | Number | Applies the 'Knockback' effect. | 7 |
| `Bruise` | Number | Applies the 'Bruise' effect. | 5 |
| [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally) | Block | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 5 |
| [`BounceObject`](./Enums.md#enum-bounceobject) | Enum/String | Spawns a physics object that visually bounces off the target. | 4 |
| [`DistanceBonusDamage`](./Passives_and_Statuses.md#context-distancebonusdamage) | Block | Applies the 'DistanceBonusDamage' effect. | 4 |
| `Weakness` | Number | Applies the 'Weakness' effect. | 4 |
| `Burn` | Number | Applies the 'Burn' effect. | 3 |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy) | Block | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 3 |
| `Leech` | Number | Applies the 'Leech' effect. | 3 |
| `Piercing` | Number | Applies the 'Piercing' effect. | 3 |
| `Slow` | Number | Applies the 'Slow' effect. | 3 |
| [`SpreadDisease`](./Passives_and_Statuses.md#context-spreaddisease) | Block | Provides a chance to transmit a disease status to adjacent targets. | 3 |
| [`ApplyStatusIfCrit`](./Passives_and_Statuses.md#context-applystatusifcrit) | Block | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. | 2 |
| `BurgleCoin` | Number | Applies the 'BurgleCoin' effect. | 2 |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum/String | Transforms the terrain tile under the target. | 2 |
| [`Charmed`](./Arrays.md#array-charmed) | Array | Applies the 'Charmed' effect. | 2 |
| [`Conditional_Adjacent`](./Passives_and_Statuses.md#context-conditional_adjacent) | Block | Conditional block: Executes nested logic only if the target is/has Adjacent. | 2 |
| [`Conditional_Shielded`](./Passives_and_Statuses.md#context-conditional_shielded) | Block | Conditional trigger: Executes nested logic if the target currently has a Shield status. | 2 |
| [`Fear`](./Arrays.md#array-fear) | Array | Applies the 'Fear' effect. | 2 |
| [`Freeze`](./Arrays.md#array-freeze) | Array | Applies the 'Freeze' effect. | 2 |
| `KnockOutCoin` | Number | Forces the target to drop coins. | 2 |
| `LuckUp` | Number | Applies the 'LuckUp' effect. | 2 |
| `Madness` | Number | Applies the Madness debuff/status effect. | 2 |
| `MagicWeakness` | Number | Applies the 'MagicWeakness' effect. | 2 |
| `Rot` | Number | Applies the 'Rot' effect. | 2 |
| `SoulLink` | Number | Applies the 'SoulLink' effect. | 2 |
| `SpawnBearTrapOnMiss` | Number | Applies the 'SpawnBearTrapOnMiss' effect. | 2 |
| [`Stun`](./Arrays.md#array-stun) | Array | Applies the 'Stun' effect. | 2 |
| [`ApplyToSource`](./Passives_and_Statuses.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| `BigSplashDamage` | Number | Applies the 'BigSplashDamage' effect. | 1 |
| `Blind` | Number | Applies the 'Blind' effect. | 1 |
| [`Conditional_HasTag`](./Passives_and_Statuses.md#context-conditional_hastag) | Block | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 1 |
| [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#context-conditional_sourcehastag) | Block | Conditional block: Executes nested logic only if the target is/has SourceHasTag. | 1 |
| `Confusion` | Number | Applies the 'Confusion' effect. | 1 |
| `DamageOrHealConditionally` | Number | Combat Trigger: Deals damage to or heal conditionally. | 1 |
| [`Else`](./Passives_and_Statuses.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |
| `Leeches` | Number | Applies the 'Leeches' effect. | 1 |
| `ManaLeeches` | Number | Applies the 'ManaLeeches' effect. | 1 |
| `OverrideChainKnockback` | Number | Applies the 'OverrideChainKnockback' effect. | 1 |
| `OverrideChainKnockbackDamage` | Number | Applies the 'OverrideChainKnockbackDamage' effect. | 1 |
| `SplashDamage` | Number | Applies the 'SplashDamage' effect. | 1 |

</details>

---

### Context: `SpreadDisease`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`effects`](./Passives_and_Statuses.md#context-effects)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`disease`](./Enums.md#enum-disease) | Enum/String | The specific status effect ID representing the disease. | 12 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of transmitting. | 11 |
| `can_apply_to_anything` | Boolean |  | 6 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#context-damageneighborsaftermove), [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#context-damageneighborsonendmove), [`GravityWell`](./Passives_and_Statuses.md#context-gravitywell), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`RevengeDamage`](./Passives_and_Statuses.md#context-revengedamage), [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#context-smiteenemieswhokill), [`fire`](./Passives_and_Statuses.md#context-fire), [`ice`](./Passives_and_Statuses.md#context-ice), [`lightning`](./Passives_and_Statuses.md#context-lightning), [`triattack`](./Passives_and_Statuses.md#context-triattack)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum/String | Applies the 'VisualFXTile' effect. | 12 |
| [`SpreadDisease`](./Passives_and_Statuses.md#context-spreaddisease) | Block | Provides a chance to transmit a disease status to adjacent targets. | 7 |
| `Stun` | Number | Applies the 'Stun' effect. | 6 |
| [`Freeze`](./Arrays.md#array-freeze) | Array | Applies the 'Freeze' effect. | 3 |
| `Burn` | Number | Applies the 'Burn' effect. | 2 |
| [`Charmed`](./Arrays.md#array-charmed) | Array | Applies the 'Charmed' effect. | 2 |
| [`Petrify`](./Arrays.md#array-petrify) | Array | Applies the 'Petrify' effect. | 2 |
| `Poison` | Number | Applies the 'Poison' effect. | 2 |
| `Slow` | Number | Applies the 'Slow' effect. | 2 |
| `Bleed` | Number | Applies the 'Bleed' effect. | 1 |
| `Bruise` | Number | Applies the 'Bruise' effect. | 1 |
| `Fear` | Number | Applies the 'Fear' effect. | 1 |
| `Immobile` | Number | Applies the 'Immobile' effect. | 1 |
| `Leeches` | Number | Applies the 'Leeches' effect. | 1 |
| `Madness` | Number | Applies the Madness debuff/status effect. | 1 |
| `Marked` | Number | Applies the 'Marked' effect. | 1 |
| `Weakness` | Number | Applies the 'Weakness' effect. | 1 |

</details>

---

### Context: `Temporary`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_BadRoll`](./Passives_and_Statuses.md#context-conditional_badroll), [`StatusOnGainShield`](./Passives_and_Statuses.md#context-statusongainshield), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage), [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#context-statusonturnendifmanaorhealthexact)

| Property Key | Type | Definition | Count (X/11) |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 11 |
| [`status`](./Enums.md#enum-status) | Enum/String | The status effect to apply. | 11 |
| `turns` | Number | Duration in turns. | 8 |
| `expires_on_end_turn` | Boolean |  | 6 |
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 5 |

</details>

---

### Context: `PassiveAtStatThreshold`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/10) |
| :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum/String |  | 10 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 10 |
| [`threshold`](./Passives_and_Statuses.md#context-threshold) | Block |  | 10 |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/10) |
| :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 10 |
| [`CureDisease`](./Passives_and_Statuses.md#context-curedisease) | Block | Applies the 'CureDisease' effect. | 6 |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum/String | Generates an item drop from the specified loot pool. | 3 |
| `RandomPermanentStat` | Number | Applies the 'RandomPermanentStat' effect. | 3 |
| [`NextBattleStatus`](./Passives_and_Statuses.md#context-nextbattlestatus) | Block | Applies the 'NextBattleStatus' effect. | 2 |
| `PermanentSpeed` | Number | Applies the 'PermanentSpeed' effect. | 2 |
| `RandomMutation` | Number | Applies the 'RandomMutation' effect. | 2 |
| `PermanentConstitution` | Number | Applies the 'PermanentConstitution' effect. | 1 |
| `PermanentIntelligence` | Number | Applies the 'PermanentIntelligence' effect. | 1 |
| `PermanentStrength` | Number | Applies the 'PermanentStrength' effect. | 1 |

</details>

---

### Context: `AddStatusToExplosions`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| [`AddElement`](./Enums.md#enum-addelement) | Enum/String | Applies the 'AddElement' effect. | 8 |
| `Burn` | Number | Applies the 'Burn' effect. | 4 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 8 |
| `knockback` | Number |  | 2 |

</details>

---

### Context: `AddSelfStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. | 7 |

</details>

---

### Context: `DamageNeighborsOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 7 |
| [`type`](./Enums.md#enum-type) | Enum/String | The classification type (e.g., damage type or element). | 7 |
| `cant_miss` | Boolean |  | 6 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 6 |
| `knockback` | Number |  | 1 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 7 |
| `damage` | Number | The base damage properties of an attack. | 4 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 4 |
| `Poison` | Number | Applies the 'Poison' effect. | 1 |
| [`SpreadDisease`](./Passives_and_Statuses.md#context-spreaddisease) | Block | Provides a chance to transmit a disease status to adjacent targets. | 1 |
| `Weakness` | Number | Applies the 'Weakness' effect. | 1 |

</details>

---

### Context: `StatusOnUseAbilityWithTag`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum/String | The specific entity tag required or applied. | 7 |
| `RefreshActPoints` | Number | Applies the 'RefreshActPoints' effect. | 3 |
| [`Conditional_FirstApplicationThisTurn`](./Passives_and_Statuses.md#context-conditional_firstapplicationthisturn) | Block | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 2 |
| `DamageUp` | Number | Combat Trigger: Deals damage to up. | 2 |
| `exclude_basicattack` | Boolean |  | 2 |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 1 |
| `RandomStatUp` | Number | Applies the 'RandomStatUp' effect. | 1 |

</details>

---

### Context: `AddStatusToElementAbilities`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | The specific element type required or applied. | 6 |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum/String | Transforms the terrain tile under the target. | 2 |
| [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally) | Block | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 2 |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy) | Block | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 2 |
| `Bleed` | Number | Applies the 'Bleed' effect. | 1 |

</details>

---

### Context: `CureDisease`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 6 |
| [`disease`](./Enums.md#enum-disease) | Enum/String |  | 6 |
| `can_apply_to_anything` | Boolean |  | 1 |

</details>

---

### Context: `ManaCostReductionTagged`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| `reduction` | Number |  | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum/String | The specific entity tag required or applied. | 6 |

</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 6 |
| [`chance`](./Enums.md#enum-chance) | Enum/String | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 5 |
| `number` | Number |  | 2 |
| `good` | Boolean |  | 1 |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 6 |
| `good` | Boolean |  | 3 |
| `spawn_on_death_hit` | Boolean |  | 2 |
| `consider_all_layers` | Boolean |  | 1 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Applies the 'ForceUseAbility' effect. | 6 |
| `NonStackingDivineShield` | Number | Applies the 'NonStackingDivineShield' effect. | 4 |
| `SpeedUp` | Number | Applies the 'SpeedUp' effect. | 4 |
| `EmptyMana` | Number | Applies the 'EmptyMana' effect. | 2 |
| `RangeUp` | Number | Applies the 'RangeUp' effect. | 2 |
| `IntelligenceUp` | Number | Applies the 'IntelligenceUp' effect. | 1 |
| `KineticSpikes` | Number | Applies the 'KineticSpikes' effect. | 1 |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#context-objectonhitcharacter) | Block | Spawns a specific character or entity upon impact. | 1 |
| `PermanentMadness` | Number | Applies the 'PermanentMadness' effect. | 1 |
| `StrengthUp` | Number | Applies the 'StrengthUp' effect. | 1 |
| [`UseAbility_Madness`](./Enums.md#enum-useability_madness) | Enum/String | Applies the 'UseAbility_Madness' effect. | 1 |

</details>

---

### Context: `StatusOnStanceSwitch`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#context-passiveifemptyface), [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#context-passiveifemptyhead), [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#context-passiveifemptyneck), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. | 6 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Applies the 'ForceUseAbility' effect. | 2 |
| `NextBasicAttackCritsThisTurn` | Number | Guarantees the next basic attack executed this turn will be a critical hit. | 2 |
| `RandomStatUp` | Number | Applies the 'RandomStatUp' effect. | 2 |
| `Shield` | Number | Applies the 'Shield' effect. | 2 |
| `PartialCleanse` | Number | Applies the 'PartialCleanse' effect. | 1 |

</details>

---

### Context: `threshold`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 6 |
| `cha` | Number |  | 2 |
| `spd` | Number |  | 2 |

</details>

---

### Context: `AddPassivesToCharmed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 5 |
| `AddMaxHealth` | Number | Applies the 'AddMaxHealth' effect. | 2 |
| `AddSpeed` | Number | Applies the 'AddSpeed' effect. | 2 |
| `DamageUp` | Number | Combat Trigger: Deals damage to up. | 2 |

</details>

---

### Context: `AddPassivesToMinions`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 5 |
| `DamageUp` | Number | Combat Trigger: Deals damage to up. | 4 |
| `IncreaseExplosionDamage` | Number | Applies the 'IncreaseExplosionDamage' effect. | 4 |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum/String | Applies the 'FreePathfindElement' effect. | 3 |
| `AddMaxHealth` | Number | Applies the 'AddMaxHealth' effect. | 2 |
| `AddSpeed` | Number | Applies the 'AddSpeed' effect. | 2 |
| [`AddStatusToExplosions`](./Passives_and_Statuses.md#context-addstatustoexplosions) | Block | Applies the 'AddStatusToExplosions' effect. | 2 |
| [`EMP`](./Passives_and_Statuses.md#context-emp) | Block | Applies the 'EMP' effect. | 2 |
| [`FamiliarBonusAbility`](./Enums.md#enum-familiarbonusability) | Enum/String | Applies the 'FamiliarBonusAbility' effect. | 2 |
| `ForceAttack` | Number | Forces the character to execute an immediate attack. | 2 |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 2 |
| `HealthRegenUp` | Number | Applies the 'HealthRegenUp' effect. | 2 |
| `HolyShieldTransferToSpawner` | Number | Applies the 'HolyShieldTransferToSpawner' effect. | 2 |
| `IncreaseExplosionSize` | Number | Applies the 'IncreaseExplosionSize' effect. | 2 |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement) | Block | State Trigger: Grants nested passives when affected by element. | 2 |
| `PoisonThorns` | Number | Applies the 'PoisonThorns' effect. | 2 |
| [`StatusAlliesOnKill`](./Passives_and_Statuses.md#context-statusalliesonkill) | Block | Event Trigger: Applies nested statuses to allies on kill. | 2 |
| [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill) | Block | Event Trigger: Applies nested statuses when kill. | 2 |
| `WaterWalk` | Number | Applies the 'WaterWalk' effect. | 2 |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum/String |  | 2 |
| `AddUnfilledMaxHealth` | Number | Applies the 'AddUnfilledMaxHealth' effect. | 1 |
| `DivineShield` | Number | Applies the 'DivineShield' effect. | 1 |
| `GrassTileHealing` | Number | Applies the 'GrassTileHealing' effect. | 1 |
| `Quivered` | Number | Applies the 'Quivered' effect. | 1 |
| `SafeExplosions` | Number | Applies the 'SafeExplosions' effect. | 1 |
| `TakeExtraTurn` | Number | Applies the 'TakeExtraTurn' effect. | 1 |
| `UncappedHP` | Number | Applies the 'UncappedHP' effect. | 1 |

</details>

---

### Context: `CritsApplyStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum/String | Spawns a specific character or entity upon impact. | 5 |
| `Stun` | Number | Applies the 'Stun' effect. | 3 |
| `Weakness` | Number | Applies the 'Weakness' effect. | 3 |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#context-conditional_hasstatus) | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 2 |
| [`Else`](./Passives_and_Statuses.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 2 |
| `Bleed` | Number | Applies the 'Bleed' effect. | 1 |
| `Bruise` | Number | Applies the 'Bruise' effect. | 1 |
| `Confusion` | Number | Applies the 'Confusion' effect. | 1 |
| `Immobile` | Number | Applies the 'Immobile' effect. | 1 |

</details>

---

### Context: `AddDamageToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 4 |
| [`element`](./Enums.md#enum-element) | Enum/String | The specific element type required or applied. | 4 |

</details>

---

### Context: `AddStatusToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | The specific element type required or applied. | 4 |
| `Burn` | Number | Applies the 'Burn' effect. | 2 |
| [`Conditional_Corpse`](./Passives_and_Statuses.md#context-conditional_corpse) | Block | Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 2 |

</details>

---

### Context: `AllyManaRegenAura`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum/String | Distance or area of effect in tiles. | 4 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 4 |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to autocast. | 4 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 2 |
| `force_display_name` | Boolean |  | 2 |

</details>

---

### Context: `DistanceBonusDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `min_range` | Number |  | 4 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 4 |

</details>

---

### Context: `EMP`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`spell_graphics_override`](./Passives_and_Statuses.md#context-spell_graphics_override) | Block |  | 4 |
| [`status_explosion_override`](./Enums.md#enum-status_explosion_override) | Enum/String |  | 4 |

</details>

---

### Context: `PassiveAtHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum/String |  | 4 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 4 |
| `threshold` | Number |  | 4 |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | The specific element type required or applied. | 4 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 4 |

</details>

---

### Context: `StatusOnTurnEndIfCastNSpells`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `spells` | Number |  | 4 |
| `DoubleCastSpell` | Number | Applies the 'DoubleCastSpell' effect. | 2 |
| `Quivered` | Number | Applies the 'Quivered' effect. | 2 |
| `MoveQuivered` | Number | Applies the 'MoveQuivered' effect. | 1 |

</details>

---

### Context: `StatusOnTurnEndIfManaExact`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `mana` | Number |  | 4 |
| `FreeSpell` | Number | Applies the 'FreeSpell' effect. | 2 |
| `Quivered` | Number | Applies the 'Quivered' effect. | 2 |
| `MoveQuivered` | Number | Applies the 'MoveQuivered' effect. | 1 |
| `SpellDamageUp` | Number | Applies the 'SpellDamageUp' effect. | 1 |

</details>

---

### Context: `StatusOnTurnEndIfManaOrHealthExact`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `mana` | Number |  | 4 |
| [`Temporary`](./Passives_and_Statuses.md#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 3 |
| `IntelligenceUp` | Number | Applies the 'IntelligenceUp' effect. | 2 |
| `Shield` | Number | Applies the 'Shield' effect. | 2 |
| `SpellDamageUp` | Number | Applies the 'SpellDamageUp' effect. | 2 |
| `DivineShield` | Number | Applies the 'DivineShield' effect. | 1 |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 1 |
| `KineticSpikes` | Number | Applies the 'KineticSpikes' effect. | 1 |

</details>

---

### Context: `spell_graphics_override`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`EMP`](./Passives_and_Statuses.md#context-emp)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum/String |  | 4 |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum/String |  | 4 |
| `palette` | Number |  | 4 |
| [`particle`](./Enums.md#enum-particle) | Enum/String |  | 4 |

</details>

---

### Context: `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | Applies the 'Confusion' effect. | 3 |
| `Bruise` | Number | Applies the 'Bruise' effect. | 2 |
| `FaceAway` | Number | Applies the 'FaceAway' effect. | 2 |
| [`Stun`](./Arrays.md#array-stun) | Array | Applies the 'Stun' effect. | 2 |
| [`SpreadDisease`](./Passives_and_Statuses.md#context-spreaddisease) | Block | Provides a chance to transmit a disease status to adjacent targets. | 1 |

</details>

---

### Context: `AmplifyStatus`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `addstacks` | Number |  | 3 |
| [`status`](./Enums.md#enum-status) | Enum/String | The ID of the status effect to check or apply. | 3 |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`Temporary`](./Passives_and_Statuses.md#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 3 |
| [`odds`](./Enums.md#enum-odds) | Enum/String | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 3 |

</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_NotBoss`](./Passives_and_Statuses.md#context-conditional_notboss)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | Applies the 'Confusion' effect. | 3 |
| [`Conditional_PartyMember`](./Passives_and_Statuses.md#context-conditional_partymember) | Block | Conditional block: Executes nested logic only if the target is/has PartyMember. | 2 |
| [`Else`](./Passives_and_Statuses.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 2 |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 2 |
| [`Stun`](./Arrays.md#array-stun) | Array | Applies the 'Stun' effect. | 1 |

</details>

---

### Context: `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum/String | The specific status ID to check for. | 3 |

</details>

---

### Context: `ElementalManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | The specific element type required or applied. | 3 |
| `reduction` | Number |  | 3 |

</details>

---

### Context: `ForceUseAbility`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to trigger or reference. | 3 |
| [`chance`](./Enums.md#enum-chance) | Enum/String | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 3 |

</details>

---

### Context: `MoveTowardsDamageSource`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum/String |  | 3 |
| `move_far` | Boolean |  | 3 |

</details>

---

### Context: `ObjectOnHitCharacter`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend), [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#context-statuseachturnendperenemykill)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String | The entity ID of the character to spawn (e.g., CharmedFlea). | 3 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 3 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`StatusOnGainCoins`](./Passives_and_Statuses.md#context-statusongaincoins), [`StatusOnHealed`](./Passives_and_Statuses.md#context-statusonhealed), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 3 |
| [`StatusGroup`](./Passives_and_Statuses.md#context-statusgroup) | Block | Groups multiple status effects together for batch application. | 3 |
| `Bleed` | Number | Applies the 'Bleed' effect. | 2 |
| `BleedThorns` | Number | Applies the 'BleedThorns' effect. | 2 |
| `Blind` | Number | Applies the 'Blind' effect. | 2 |
| `Brace` | Number | Applies the 'Brace' effect. | 2 |
| `Bruise` | Number | Applies the 'Bruise' effect. | 2 |
| `Burn` | Number | Applies the 'Burn' effect. | 2 |
| `Charge` | Number | Applies the 'Charge' effect. | 2 |
| `Charmed` | Number | Applies the 'Charmed' effect. | 2 |
| `Confusion` | Number | Applies the 'Confusion' effect. | 2 |
| `DiminishingHealthRegen` | Number | Applies the 'DiminishingHealthRegen' effect. | 2 |
| `DivineShield` | Number | Applies the 'DivineShield' effect. | 2 |
| `Fear` | Number | Applies the 'Fear' effect. | 2 |
| `Freeze` | Number | Applies the 'Freeze' effect. | 2 |
| `Immobile` | Number | Applies the 'Immobile' effect. | 2 |
| `KineticSpikes` | Number | Applies the 'KineticSpikes' effect. | 2 |
| `Madness` | Number | Applies the Madness debuff/status effect. | 2 |
| `MagicWeakness` | Number | Applies the 'MagicWeakness' effect. | 2 |
| `Marked` | Number | Applies the 'Marked' effect. | 2 |
| `MoveQuivered` | Number | Applies the 'MoveQuivered' effect. | 2 |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum/String | Spawns a specific character or entity upon impact. | 2 |
| `Petrify` | Number | Applies the 'Petrify' effect. | 2 |
| `Poison` | Number | Applies the 'Poison' effect. | 2 |
| `Quivered` | Number | Applies the 'Quivered' effect. | 2 |
| `Reflect` | Number | Applies the 'Reflect' effect. | 2 |
| `Shield` | Number | Applies the 'Shield' effect. | 2 |
| `Sleep` | Number | Applies the 'Sleep' effect. | 2 |
| `Slow` | Number | Applies the 'Slow' effect. | 2 |
| `Stun` | Number | Applies the 'Stun' effect. | 2 |
| `Tarred` | Number | Applies the 'Tarred' effect. | 2 |
| `Thorns` | Number | Applies the 'Thorns' effect. | 2 |
| `Weakness` | Number | Applies the 'Weakness' effect. | 2 |
| `ConstitutionUp` | Number | Applies the 'ConstitutionUp' effect. | 1 |
| `SpawnCoinAnywhere` | Number | Applies the 'SpawnCoinAnywhere' effect. | 1 |
| `SpeedUp` | Number | Applies the 'SpeedUp' effect. | 1 |
| `StrengthUp` | Number | Applies the 'StrengthUp' effect. | 1 |

</details>

---

### Context: `SpawnCatCopyOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 3 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum/String |  | 3 |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 3 |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 3 |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`Conditional_BadRoll`](./Passives_and_Statuses.md#context-conditional_badroll) | Block | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. | 3 |
| [`FillMana`](./Arrays.md#array-fillmana) | Array | Applies the 'FillMana' effect. | 2 |
| `IntelligenceUp` | Number | Applies the 'IntelligenceUp' effect. | 2 |
| `RandomStatUp` | Number | Applies the 'RandomStatUp' effect. | 2 |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#context-conditional_goodroll) | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 1 |
| [`Fear`](./Arrays.md#array-fear) | Array | Applies the 'Fear' effect. | 1 |
| [`ForceUseAbility`](./Passives_and_Statuses.md#context-forceuseability) | Block | Applies the 'ForceUseAbility' effect. | 1 |

</details>

---

### Context: `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 3 |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `SpellDamageUp` | Number | Applies the 'SpellDamageUp' effect. | 2 |
| `ReduceManaCost` | Number | Applies the 'ReduceManaCost' effect. | 1 |
| `RepairWeapon` | Number | Applies the 'RepairWeapon' effect. | 1 |
| `RepairWeaponCondition` | Number | Applies the 'RepairWeaponCondition' effect. | 1 |

</details>

---

### Context: `StatusOnCrit`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | Applies the 'LuckUp' effect. | 3 |
| `DamageUp` | Number | Combat Trigger: Deals damage to up. | 2 |
| `Shield` | Number | Applies the 'Shield' effect. | 2 |
| `CritChanceUp` | Number | Applies the 'CritChanceUp' effect. | 1 |
| `RandomStatUp` | Number | Applies the 'RandomStatUp' effect. | 1 |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | Applies the 'SpeedUp' effect. | 3 |
| [`Temporary`](./Passives_and_Statuses.md#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 3 |
| `ConstitutionUp` | Number | Applies the 'ConstitutionUp' effect. | 2 |
| [`Craft`](./Passives_and_Statuses.md#context-craft) | Block | Synthesizes or spawns a new item from a specific pool. | 2 |
| `DamageUp` | Number | Combat Trigger: Deals damage to up. | 2 |
| `IntelligenceUp` | Number | Applies the 'IntelligenceUp' effect. | 2 |
| `Shield` | Number | Applies the 'Shield' effect. | 2 |
| `StrengthUp` | Number | Applies the 'StrengthUp' effect. | 2 |
| `TempDamageUp` | Number | Applies the 'TempDamageUp' effect. | 2 |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#context-conditional_hasstatus) | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 1 |
| `DiminishingHealthRegen` | Number | Applies the 'DiminishingHealthRegen' effect. | 1 |
| [`Else`](./Passives_and_Statuses.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |
| `MovementUp` | Number | Applies the 'MovementUp' effect. | 1 |
| `RandomInjury` | Number | Applies the 'RandomInjury' effect. | 1 |
| `RandomStatUp` | Number | Applies the 'RandomStatUp' effect. | 1 |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |
| `TempMovement` | Number | Applies the 'TempMovement' effect. | 1 |
| `Thorns` | Number | Applies the 'Thorns' effect. | 1 |

</details>

---

### Context: `3`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 2 |
| `desc` | String | Localization key for the passive's display description. | 1 |
| [`icon`](./Enums.md#enum-icon) | Enum/String |  | 1 |
| `name` | String | Localization key for the passive's display name. | 1 |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to trigger or reference. | 2 |
| `range` | Number | Distance or area of effect in tiles. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum/String | The specific entity tag required or applied. | 2 |

</details>

---

### Context: `AddPassiveToSpawnedRocks`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AddFilledMaxHealth` | Number | Applies the 'AddFilledMaxHealth' effect. | 2 |
| `JoinSpawnerFaction` | Number | Applies the 'JoinSpawnerFaction' effect. | 2 |

</details>

---

### Context: `AddPassivesToSummonAbilityMinions`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | Combat Trigger: Deals damage to up. | 2 |
| `Doomed` | Number | Applies the 'Doomed' effect. | 2 |
| `MovementUp` | Number | Applies the 'MovementUp' effect. | 2 |

</details>

---

### Context: `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `ChanceToBreak` | Number | Applies the 'ChanceToBreak' effect. | 2 |

</details>

---

### Context: `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `LeaveBehindRockOnKnockback` | Number | Applies the 'LeaveBehindRockOnKnockback' effect. | 2 |
| `Blind` | Number | Applies the 'Blind' effect. | 1 |
| [`Conditional_HasTag`](./Passives_and_Statuses.md#context-conditional_hastag) | Block | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 1 |
| `NonLethal` | Number | Applies the 'NonLethal' effect. | 1 |

</details>

---

### Context: `AddStatusToBasicAttackWithCooldown`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `CharmedForceAttack` | Number | Applies the 'CharmedForceAttack' effect. | 2 |

</details>

---

### Context: `AddStatusToFirstBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | Applies the 'Charmed' effect. | 2 |

</details>

---

### Context: `AddStatusToTrampleDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Cleave` | Number | Causes the attack to hit adjacent enemies alongside the primary target. | 2 |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | Applies the 'Bleed' effect. | 2 |
| `PullSourceToKnockbackImmuneTarget` | Number | Applies the 'PullSourceToKnockbackImmuneTarget' effect. | 2 |
| `Cleave` | Number | Causes the attack to hit adjacent enemies alongside the primary target. | 1 |
| `LeechPercent` | Number | Applies the 'LeechPercent' effect. | 1 |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | Applies the 'CastAgain' effect. | 2 |
| `Fury` | Number | Applies the 'Fury' effect. | 1 |

</details>

---

### Context: `AllyBonusAbilityAura`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to trigger or reference. | 2 |
| `square` | Boolean |  | 2 |

</details>

---

### Context: `AllyHealthRegenAura`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum/String | Distance or area of effect in tiles. | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `AlternateCraftingPools`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`tinkerer_0`](./Enums.md#enum-tinkerer_0) | Enum/String |  | 2 |
| [`tinkerer_1`](./Enums.md#enum-tinkerer_1) | Enum/String |  | 2 |

</details>

---

### Context: `ApplyStatusIfCrit`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Purge` | Number | Applies the 'Purge' effect. | 2 |

</details>

---

### Context: `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Bounty` | Number | Applies the 'Bounty' effect. | 2 |
| `count` | Number | The numerical quantity. | 1 |

</details>

---

### Context: `BoobyTrapItems`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`on_break`](./Passives_and_Statuses.md#context-on_break) | Block |  | 2 |
| [`on_throw`](./Passives_and_Statuses.md#context-on_throw) | Block |  | 2 |

</details>

---

### Context: `BoostWeaponDamage`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`crit_chance`](./Enums.md#enum-crit_chance) | Enum/String |  | 2 |
| `damage` | Number | The base damage properties of an attack. | 2 |

</details>

---

### Context: `BouncyProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number |  | 2 |
| `max_range` | Number |  | 2 |

</details>

---

### Context: `CatAPultAnimation`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to trigger or reference. | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum/String |  | 2 |

</details>

---

### Context: `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | Applies the 'Quivered' effect. | 2 |
| `ally_chance` | Number |  | 2 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 1 |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to trigger or reference. | 2 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`class`](./Enums.md#enum-class) | Enum/String | Character class identifier. | 2 |
| `reduction` | Number |  | 2 |

</details>

---

### Context: `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | Applies the 'Bleed' effect. | 2 |
| `BonusCritChance` | Number | Applies the 'BonusCritChance' effect. | 2 |
| `BonusDamage` | Number | Applies the 'BonusDamage' effect. | 2 |

</details>

---

### Context: `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#context-conditional_sourcehastag), [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#context-extrastatuswhendealingdamage), [`StatusKilledCharacters`](./Passives_and_Statuses.md#context-statuskilledcharacters)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `Cleanse` | Number | Applies the 'Cleanse' effect. | 2 |
| `ClearNegativeEffects` | Number | Applies the 'ClearNegativeEffects' effect. | 2 |
| `DamageUp` | Number | Combat Trigger: Deals damage to up. | 2 |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 2 |
| `Shield` | Number | Applies the 'Shield' effect. | 2 |
| `TempSpeedUp` | Number | Applies the 'TempSpeedUp' effect. | 2 |
| [`ApplyToSource`](./Passives_and_Statuses.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| `SpeedUp` | Number | Applies the 'SpeedUp' effect. | 1 |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToElementDamage`](./Passives_and_Statuses.md#context-addstatustoelementdamage)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | Applies the 'Charmed' effect. | 2 |
| `OverrideDamage` | Number | Applies the 'OverrideDamage' effect. | 2 |
| `Revive` | Number | Applies the 'Revive' effect. | 2 |
| `SafeDoomed` | Number | Applies the 'SafeDoomed' effect. | 2 |
| `TakeExtraTurn` | Number | Applies the 'TakeExtraTurn' effect. | 2 |
| `DamageUp` | Number | Combat Trigger: Deals damage to up. | 1 |
| `SpeedUp` | Number | Applies the 'SpeedUp' effect. | 1 |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill), [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#context-statusonuseabilitywithtag)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `TakeExtraTurn` | Number | Applies the 'TakeExtraTurn' effect. | 2 |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 1 |
| `FillMana` | Number | Applies the 'FillMana' effect. | 1 |
| `ManaGain` | Number | Applies the 'ManaGain' effect. | 1 |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Passives_and_Statuses.md#context-addstatustoalldamage), [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum/String | The specific string tag to check for. | 2 |
| `Charmed` | Number | Applies the 'Charmed' effect. | 1 |
| `FlatLeechIfDamaged` | Number | Applies the 'FlatLeechIfDamaged' effect. | 1 |

</details>

---

### Context: `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy) | Block | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 2 |

</details>

---

### Context: `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | Applies the 'Charmed' effect. | 2 |

</details>

---

### Context: `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `BonusCritChance` | Number | Applies the 'BonusCritChance' effect. | 2 |

</details>

---

### Context: `Craft`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum/String |  | 2 |
| [`slot`](./Enums.md#enum-slot) | Enum/String |  | 2 |

</details>

---

### Context: `DamageNeighborsAfterMove`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`damage`](./Enums.md#enum-damage) | Enum/String | The base damage properties of an attack. | 2 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum/String | The classification type (e.g., damage type or element). | 2 |

</details>

---

### Context: `DamageReductionAura`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 2 |
| [`range`](./Enums.md#enum-range) | Enum/String | Distance or area of effect in tiles. | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `DeathRattle`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to trigger or reference. | 2 |
| `pop_corpse` | Boolean |  | 2 |

</details>

---

### Context: `Earth`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`damage`](./Enums.md#enum-damage) | Enum/String | The base damage properties of an attack. | 2 |

</details>

---

### Context: `Electric`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Stun`](./Arrays.md#array-stun) | Array | Applies the 'Stun' effect. | 2 |

</details>

---

### Context: `ElementalAttunement`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Earth`](./Passives_and_Statuses.md#context-earth) | Block | Applies the 'Earth' effect. | 2 |
| [`Electric`](./Passives_and_Statuses.md#context-electric) | Block | Applies the 'Electric' effect. | 2 |
| [`Fire`](./Passives_and_Statuses.md#context-fire) | Block | Applies the 'Fire' effect. | 2 |
| [`Grass`](./Passives_and_Statuses.md#context-grass) | Block | Applies the 'Grass' effect. | 2 |
| [`Gravity`](./Passives_and_Statuses.md#context-gravity) | Block | Applies the 'Gravity' effect. | 2 |
| [`Holy`](./Passives_and_Statuses.md#context-holy) | Block | Applies the 'Holy' effect. | 2 |
| [`Ice`](./Passives_and_Statuses.md#context-ice) | Block | Applies the 'Ice' effect. | 2 |
| [`Shadow`](./Passives_and_Statuses.md#context-shadow) | Block | Applies the 'Shadow' effect. | 2 |
| [`Water`](./Passives_and_Statuses.md#context-water) | Block | Applies the 'Water' effect. | 2 |
| [`Wind`](./Passives_and_Statuses.md#context-wind) | Block | Applies the 'Wind' effect. | 2 |

</details>

---

### Context: `Else`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Number | Applies the 'CaptureFamiliar' effect. | 2 |
| `FactionConversion` | Number | Applies the 'FactionConversion' effect. | 2 |
| `Marked` | Number | Applies the 'Marked' effect. | 2 |
| `PermanentCharm` | Number | Applies the 'PermanentCharm' effect. | 2 |
| `Fear` | Number | Applies the 'Fear' effect. | 1 |
| `TempSpeedUp` | Number | Applies the 'TempSpeedUp' effect. | 1 |

</details>

---

### Context: `EscapeSequence`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `RandomDistanceDisplace` | Number | Displaces the target by a randomized distance. | 2 |
| `SafeExplosionIfHitSomething` | Number | Applies the 'SafeExplosionIfHitSomething' effect. | 2 |

</details>

---

### Context: `Eternal`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `health_percent` | Number |  | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 1 |
| `TakeExtraTurn` | Number | Applies the 'TakeExtraTurn' effect. | 1 |

</details>

---

### Context: `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally) | Block | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 2 |

</details>

---

### Context: `Fire`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Burn`](./Enums.md#enum-burn) | Enum/String | Applies the 'Burn' effect. | 2 |

</details>

---

### Context: `Grass`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Poison`](./Enums.md#enum-poison) | Enum/String | Applies the 'Poison' effect. | 2 |

</details>

---

### Context: `Gravity`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Weakness`](./Enums.md#enum-weakness) | Enum/String | Applies the 'Weakness' effect. | 2 |

</details>

---

### Context: `GravityWell`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean |  | 2 |
| `damage` | Number | The base damage properties of an attack. | 2 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum/String | The classification type (e.g., damage type or element). | 2 |

</details>

---

### Context: `HealAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean |  | 2 |
| `mana` | Number |  | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `Holy`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`FlatLeech`](./Enums.md#enum-flatleech) | Enum/String | Applies the 'FlatLeech' effect. | 2 |

</details>

---

### Context: `HolyDamageBlessing`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilGetKill`](./Passives_and_Statuses.md#context-passiveuntilgetkill)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | Applies the 'Burn' effect. | 2 |
| `damage_multiplier` | Number |  | 2 |

</details>

---

### Context: `Ice`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Slow`](./Enums.md#enum-slow) | Enum/String | Applies the 'Slow' effect. | 2 |

</details>

---

### Context: `InfiniteRebirth`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `TempSpeedUp` | Number | Applies the 'TempSpeedUp' effect. | 2 |
| `health` | Number |  | 2 |
| `playercat_health` | Number |  | 2 |

</details>

---

### Context: `LateBloomer`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `LightningRod`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | Applies the 'Tech' effect. | 2 |

</details>

---

### Context: `LowHealthAllyDodgeChanceAura`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |
| `theshold` | Number |  | 2 |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to trigger or reference. | 2 |
| `enemies_only` | Boolean |  | 2 |

</details>

---

### Context: `NextBattleStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `FullHeal` | Number | Applies the 'FullHeal' effect. | 2 |

</details>

---

### Context: `PassiveAfterXKills`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `PassiveAtFullHealth`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `ManaCostReduction` | Number | Applies the 'ManaCostReduction' effect. | 2 |
| `TakeExtraDamage` | Number | Applies the 'TakeExtraDamage' effect. | 2 |

</details>

---

### Context: `PassiveAtInjuryThreshold`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`injury`](./Enums.md#enum-injury) | Enum/String |  | 2 |
| [`mode`](./Enums.md#enum-mode) | Enum/String |  | 2 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 2 |
| `threshold` | Number |  | 2 |

</details>

---

### Context: `PassiveGroup`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Passives_and_Statuses.md#context-randompassivepool)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`SetDefaultFace`](./Enums.md#enum-setdefaultface) | Enum/String | Applies the 'SetDefaultFace' effect. | 2 |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 1 |
| `CharismaUp` | Number | Applies the 'CharismaUp' effect. | 1 |
| `IntelligenceUp` | Number | Applies the 'IntelligenceUp' effect. | 1 |
| `SpeedUp` | Number | Applies the 'SpeedUp' effect. | 1 |

</details>

---

### Context: `PassiveIfAllArmorEmpty`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AddSpellDamage` | Number | Applies the 'AddSpellDamage' effect. | 2 |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum/String | Applies the 'CounterAttack' effect. | 2 |
| `ExtraMovePoints` | Number | Applies the 'ExtraMovePoints' effect. | 2 |
| `ManaCostReduction` | Number | Applies the 'ManaCostReduction' effect. | 2 |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch) | Block | Event Trigger: Applies nested statuses when stance switch. | 2 |
| [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus) | Block | Applies the 'CritsApplyStatus' effect. | 1 |
| `Flying` | Number | Applies the 'Flying' effect. | 1 |

</details>

---

### Context: `PassiveIfEmptyFace`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | Applies the 'AddCritMultiplier' effect. | 2 |
| `CritChanceUp` | Number | Applies the 'CritChanceUp' effect. | 2 |
| `DodgeChance` | Number | Applies the 'DodgeChance' effect. | 2 |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch) | Block | Event Trigger: Applies nested statuses when stance switch. | 2 |
| `KineticSpikes` | Number | Applies the 'KineticSpikes' effect. | 1 |

</details>

---

### Context: `PassiveIfEmptyHead`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | Applies the 'AddCritMultiplier' effect. | 2 |
| `CritChanceUp` | Number | Applies the 'CritChanceUp' effect. | 2 |
| `DodgeChance` | Number | Applies the 'DodgeChance' effect. | 2 |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch) | Block | Event Trigger: Applies nested statuses when stance switch. | 2 |
| `KineticSpikes` | Number | Applies the 'KineticSpikes' effect. | 1 |

</details>

---

### Context: `PassiveIfEmptyNeck`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | Applies the 'AddCritMultiplier' effect. | 2 |
| `CritChanceUp` | Number | Applies the 'CritChanceUp' effect. | 2 |
| `DodgeChance` | Number | Applies the 'DodgeChance' effect. | 2 |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch) | Block | Event Trigger: Applies nested statuses when stance switch. | 2 |
| `KineticSpikes` | Number | Applies the 'KineticSpikes' effect. | 1 |

</details>

---

### Context: `PassiveUntilCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`HealAlliesEachTurn`](./Passives_and_Statuses.md#context-healallieseachturn) | Block | Applies the 'HealAlliesEachTurn' effect. | 2 |
| [`StatusAlliesEachTurn`](./Passives_and_Statuses.md#context-statusallieseachturn) | Block | Event Trigger: Applies nested statuses to allies each turn. | 1 |

</details>

---

### Context: `PassiveUntilGetKill`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`HolyDamageBlessing`](./Passives_and_Statuses.md#context-holydamageblessing) | Block | Applies the 'HolyDamageBlessing' effect. | 2 |

</details>

---

### Context: `PassiveWhenAtFullMana`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 2 |
| `Brace` | Number | Applies the 'Brace' effect. | 2 |
| `Flying` | Number | Applies the 'Flying' effect. | 2 |
| `AddMovement` | Number | Applies the 'AddMovement' effect. | 1 |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum/String | Applies the 'ReplaceBasicMove' effect. | 1 |

</details>

---

### Context: `PassiveWhenTheAlpha`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `TogglableRoundEndExtraTurn` | Number | Applies the 'TogglableRoundEndExtraTurn' effect. | 2 |

</details>

---

### Context: `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | Applies the 'Brace' effect. | 2 |
| `HealthRegenUp` | Number | Applies the 'HealthRegenUp' effect. | 1 |

</details>

---

### Context: `PassiveWhileInMonkRangedStance`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AddBonusRange` | Number | Applies the 'AddBonusRange' effect. | 2 |
| `AddSpellDamage` | Number | Applies the 'AddSpellDamage' effect. | 2 |
| `KineticSpikes` | Number | Applies the 'KineticSpikes' effect. | 1 |

</details>

---

### Context: `PassiveWhilePreviewingMonkRangedStance`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AddBonusRange` | Number | Applies the 'AddBonusRange' effect. | 2 |

</details>

---

### Context: `PassiveWhileWearingMetal`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`AddElementsToWeapon`](./Enums.md#enum-addelementstoweapon) | Enum/String | Applies the 'AddElementsToWeapon' effect. | 2 |

</details>

---

### Context: `RandomPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`PassiveGroup`](./Passives_and_Statuses.md#context-passivegroup) | Block | Applies the 'PassiveGroup' effect. | 2 |

</details>

---

### Context: `RepressedMemoriesMetronome`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#context-scaledstatusonspendmana)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum/String |  | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `ScaledStatusOnOverMana`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. | 2 |
| `Cleanse` | Number | Applies the 'Cleanse' effect. | 1 |

</details>

---

### Context: `ScaledStatusOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`RepressedMemoriesMetronome`](./Passives_and_Statuses.md#context-repressedmemoriesmetronome) | Block | Applies the 'RepressedMemoriesMetronome' effect. | 2 |

</details>

---

### Context: `SecurityBotProtect`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to trigger or reference. | 2 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 2 |

</details>

---

### Context: `Shadow`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`crit_chance`](./Enums.md#enum-crit_chance) | Enum/String |  | 2 |

</details>

---

### Context: `SmiteEnemiesWhoKill`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum/String | The classification type (e.g., damage type or element). | 2 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |

</details>

---

### Context: `SpecialFriends`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 2 |

</details>

---

### Context: `StatsAtLowHealth`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `threshold` | Number |  | 2 |
| `speed` | Number |  | 1 |
| `strength` | Number |  | 1 |

</details>

---

### Context: `StatusAfterCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `TempSpellDamageUp` | Number | Applies the 'TempSpellDamageUp' effect. | 2 |
| `TempDamageUp` | Number | Applies the 'TempDamageUp' effect. | 1 |

</details>

---

### Context: `StatusAlliesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum/String | Applies the 'EquipTemporaryItem' effect. | 2 |

</details>

---

### Context: `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `HealAndOverhealToShield` | Number | Applies the 'HealAndOverhealToShield' effect. | 2 |
| `Reanimate` | Number | Applies the 'Reanimate' effect. | 2 |
| `TakeExtraTurn` | Number | Applies the 'TakeExtraTurn' effect. | 2 |
| `triggers_limit` | Number |  | 2 |
| `Freeze` | Number | Applies the 'Freeze' effect. | 1 |
| `FullHeal` | Number | Applies the 'FullHeal' effect. | 1 |

</details>

---

### Context: `StatusAlliesOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 2 |
| `LuckUp` | Number | Applies the 'LuckUp' effect. | 2 |
| `scaled` | Boolean |  | 1 |

</details>

---

### Context: `StatusAlliesOnKill`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `DamageUp` | Number | Combat Trigger: Deals damage to up. | 2 |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 1 |

</details>

---

### Context: `StatusAllyWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `threshold` | Number |  | 2 |

</details>

---

### Context: `StatusAnyCatAllyWhoKills`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AlphaCat` | Number | Applies the 'AlphaCat' effect. | 2 |

</details>

---

### Context: `StatusDamagers`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | Applies the 'LuckUp' effect. | 2 |
| [`Fear`](./Arrays.md#array-fear) | Array | Applies the 'Fear' effect. | 1 |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. | 2 |

</details>

---

### Context: `StatusEachTurnEndPerEnemyKill`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#context-objectonhitcharacter) | Block | Spawns a specific character or entity upon impact. | 2 |

</details>

---

### Context: `StatusEnemiesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `Freeze` | Number | Applies the 'Freeze' effect. | 2 |

</details>

---

### Context: `StatusEveryXTurnBegins`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | Applies the 'DivineShield' effect. | 2 |
| `turns` | Number | The duration of the effect in turns. | 2 |

</details>

---

### Context: `StatusGroup`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | Applies the 'LuckUp' effect. | 2 |
| `SpawnCoinAnywhere` | Number | Applies the 'SpawnCoinAnywhere' effect. | 2 |
| `SpeedUp` | Number | Applies the 'SpeedUp' effect. | 2 |
| `DexterityUp` | Number | Applies the 'DexterityUp' effect. | 1 |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 2 |
| `MoveQuivered` | Number | Applies the 'MoveQuivered' effect. | 2 |
| `Brace` | Number | Applies the 'Brace' effect. | 1 |
| `ConstitutionUp` | Number | Applies the 'ConstitutionUp' effect. | 1 |
| `ManaGain` | Number | Applies the 'ManaGain' effect. | 1 |
| `Shield` | Number | Applies the 'Shield' effect. | 1 |

</details>

---

### Context: `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AutoReanimate` | Number | Applies the 'AutoReanimate' effect. | 2 |
| [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally) | Block | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 1 |

</details>

---

### Context: `StatusKillers`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Conditional_Boss`](./Passives_and_Statuses.md#context-conditional_boss) | Block | Conditional trigger: Executes nested logic if the target is a Boss. | 2 |
| [`Conditional_NotBoss`](./Passives_and_Statuses.md#context-conditional_notboss) | Block | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 2 |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `FillMana` | Number | Applies the 'FillMana' effect. | 1 |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 1 |
| `PercentHeal` | Number | Applies the 'PercentHeal' effect. | 1 |
| `TakeExtraTurn` | Number | Applies the 'TakeExtraTurn' effect. | 1 |

</details>

---

### Context: `StatusOnAnyDeath`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | Applies the 'LuckUp' effect. | 2 |

</details>

---

### Context: `StatusOnBattleEndIfKillThresholdMet`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `kills` | Number |  | 2 |
| [`statuses`](./Passives_and_Statuses.md#context-statuses) | Block |  | 2 |

</details>

---

### Context: `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `FullHeal` | Number | Applies the 'FullHeal' effect. | 2 |
| `Sleep` | Number | Applies the 'Sleep' effect. | 1 |

</details>

---

### Context: `StatusOnBreakItem`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | Applies the 'Thorns' effect. | 2 |
| `Shield` | Number | Applies the 'Shield' effect. | 1 |

</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | Applies the 'Charge' effect. | 2 |
| `CurrentWeaponDamageUp` | Number | Applies the 'CurrentWeaponDamageUp' effect. | 2 |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 1 |

</details>

---

### Context: `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | Applies the 'Tech' effect. | 2 |

</details>

---

### Context: `StatusOnDealtDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `TempDexterityUp` | Number | Applies the 'TempDexterityUp' effect. | 2 |
| `TempStrengthUp` | Number | Applies the 'TempStrengthUp' effect. | 2 |
| `TempLuckUp` | Number | Applies the 'TempLuckUp' effect. | 1 |

</details>

---

### Context: `StatusOnDealtDamageThreshold`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `RefreshMovePoints` | Number | Applies the 'RefreshMovePoints' effect. | 2 |
| `Shield` | Number | Applies the 'Shield' effect. | 2 |
| `count_overkill` | Boolean |  | 2 |
| `ignore_during_movement` | Boolean |  | 2 |
| `threshold` | Number |  | 2 |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 1 |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `StrengthUp` | Number | Applies the 'StrengthUp' effect. | 2 |
| `Cleanse` | Number | Applies the 'Cleanse' effect. | 1 |
| `IntelligenceUp` | Number | Applies the 'IntelligenceUp' effect. | 1 |
| `RandomStatUp` | Number | Applies the 'RandomStatUp' effect. | 1 |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `ForceAttack` | Number | Forces the character to execute an immediate attack. | 2 |

</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 2 |
| `DivineShield` | Number | Applies the 'DivineShield' effect. | 1 |

</details>

---

### Context: `StatusOnGainShield`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Temporary`](./Passives_and_Statuses.md#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 2 |

</details>

---

### Context: `StatusOnHeal`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | Applies the 'SpeedUp' effect. | 2 |
| `RandomStatUp` | Number | Applies the 'RandomStatUp' effect. | 1 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Conditional_FirstApplicationThisTurn`](./Passives_and_Statuses.md#context-conditional_firstapplicationthisturn) | Block | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 2 |
| `DamageUp` | Number | Combat Trigger: Deals damage to up. | 2 |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum/String | Applies the 'EquipPermanentItem' effect. | 2 |
| `RefreshActPoints` | Number | Applies the 'RefreshActPoints' effect. | 2 |
| `RefreshMovePoints` | Number | Applies the 'RefreshMovePoints' effect. | 2 |
| `StrengthUp` | Number | Applies the 'StrengthUp' effect. | 2 |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 1 |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 1 |
| `LuckUp` | Number | Applies the 'LuckUp' effect. | 1 |
| `RandomStatUp` | Number | Applies the 'RandomStatUp' effect. | 1 |
| `SpeedUp` | Number | Applies the 'SpeedUp' effect. | 1 |
| `Stealth` | Number | Applies the 'Stealth' effect. | 1 |
| [`TakeBonusTurnWithStatus`](./Passives_and_Statuses.md#context-takebonusturnwithstatus) | Block | Grants the character an immediate extra turn while afflicted with specific statuses. | 1 |

</details>

---

### Context: `StatusOnKillEnemy`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | Applies the 'DivineShield' effect. | 2 |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 1 |
| `ManaGain` | Number | Applies the 'ManaGain' effect. | 1 |
| `RefreshMovePoints` | Number | Applies the 'RefreshMovePoints' effect. | 1 |

</details>

---

### Context: `StatusOnOverHealed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility_NonStack`](./Enums.md#enum-forceuseability_nonstack) | Enum/String | Applies the 'ForceUseAbility_NonStack' effect. | 2 |
| `StrengthUp` | Number | Applies the 'StrengthUp' effect. | 2 |
| `CurrentWeaponDamageUp` | Number | Applies the 'CurrentWeaponDamageUp' effect. | 1 |
| `SpawnScaledRotFly` | Number | Applies the 'SpawnScaledRotFly' effect. | 1 |

</details>

---

### Context: `StatusOnOverMana`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `IntelligenceUp` | Number | Applies the 'IntelligenceUp' effect. | 2 |
| `SpellDamageUp` | Number | Applies the 'SpellDamageUp' effect. | 2 |
| `DivineShield` | Number | Applies the 'DivineShield' effect. | 1 |

</details>

---

### Context: `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `RefreshMovePoints` | Number | Applies the 'RefreshMovePoints' effect. | 2 |
| `DexterityUp` | Number | Applies the 'DexterityUp' effect. | 1 |
| `SpeedUp` | Number | Applies the 'SpeedUp' effect. | 1 |

</details>

---

### Context: `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 2 |

</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `DiminishingHealthRegen` | Number | Applies the 'DiminishingHealthRegen' effect. | 2 |
| `Shield` | Number | Applies the 'Shield' effect. | 1 |

</details>

---

### Context: `StatusOnTookDamageFromEnemyAbility`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | Applies the 'Quivered' effect. | 2 |
| `MoveQuivered` | Number | Applies the 'MoveQuivered' effect. | 1 |

</details>

---

### Context: `StatusOnTriggerTrap`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `DexterityUp` | Number | Applies the 'DexterityUp' effect. | 2 |
| `Quivered` | Number | Applies the 'Quivered' effect. | 1 |

</details>

---

### Context: `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `FlippedFacingForceAttack` | Number | Applies the 'FlippedFacingForceAttack' effect. | 2 |

</details>

---

### Context: `StatusOnUseElementAbility`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | Applies the 'SpeedUp' effect. | 2 |
| [`element`](./Enums.md#enum-element) | Enum/String | The specific element type required or applied. | 2 |

</details>

---

### Context: `StatusPerInjury`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | Applies the 'Shield' effect. | 2 |
| `cap` | Number |  | 2 |
| [`injury`](./Enums.md#enum-injury) | Enum/String |  | 2 |
| `StrengthUp` | Number | Applies the 'StrengthUp' effect. | 1 |

</details>

---

### Context: `StatusThingsKnockedBack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Drag` | Number | Applies the 'Drag' effect. | 2 |

</details>

---

### Context: `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `OneUseSpellDamageUp` | Number | Applies the 'OneUseSpellDamageUp' effect. | 2 |
| `ManaGain` | Number | Applies the 'ManaGain' effect. | 1 |

</details>

---

### Context: `TaggedPickupEffectReplacement`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`HealthGain`](./Enums.md#enum-healthgain) | Enum/String | Applies the 'HealthGain' effect. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum/String | The specific entity tag required or applied. | 2 |

</details>

---

### Context: `TowerDefense`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 2 |
| `range` | Number | Distance or area of effect in tiles. | 2 |

</details>

---

### Context: `Water`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`AOEPuddle`](./Enums.md#enum-aoepuddle) | Enum/String | Applies the 'AOEPuddle' effect. | 2 |

</details>

---

### Context: `Wind`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`knockback`](./Enums.md#enum-knockback) | Enum/String |  | 2 |

</details>

---

### Context: `empty_armor_scaled_stats`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Passives_and_Statuses.md#context-1), [`2`](./Passives_and_Statuses.md#context-2)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 2 |
| `int` | Number |  | 2 |
| `spd` | Number |  | 2 |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Passives_and_Statuses.md#context-1), [`2`](./Passives_and_Statuses.md#context-2)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Weakness` | Number | Applies the 'Weakness' effect. | 2 |
| `MagicWeakness` | Number | Applies the 'MagicWeakness' effect. | 1 |

</details>

---

### Context: `on_break`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `SafeExplosionIfHitSomething` | Number | Applies the 'SafeExplosionIfHitSomething' effect. | 2 |

</details>

---

### Context: `on_throw`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `HitExplosion` | Number | Applies the 'HitExplosion' effect. | 2 |

</details>

---

### Context: `schadenfreude_scaled_stats`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Passives_and_Statuses.md#context-1), [`2`](./Passives_and_Statuses.md#context-2)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 2 |
| `str` | Number |  | 2 |
| `cha` | Number |  | 1 |
| `dex` | Number |  | 1 |
| `int` | Number |  | 1 |
| `lck` | Number |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Context: `statuses`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChanceToRevive`](./Passives_and_Statuses.md#context-chancetorevive), [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#context-statusonbattleendifkillthresholdmet)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum/String | Generates an item drop from the specified loot pool. | 2 |
| `PermanentDexterity` | Number | Applies the 'PermanentDexterity' effect. | 2 |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 1 |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 1 |

</details>

---

### Context: `10`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `desc` | String | Localization key for the passive's display description. | 1 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `4`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `5`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `6`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `7`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `8`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `9`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `AbilityChargeRefundChance`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `advantage_softcap` | Number |  | 1 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 1 |

</details>

---

### Context: `AbilityReaction`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to trigger or reference. | 1 |
| `ability_damage_only` | Boolean |  | 1 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 1 |

</details>

---

### Context: `AddStatusToAllDamageAbilities`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | Applies the 'Bleed' effect. | 1 |
| `Piercing` | Number | Applies the 'Piercing' effect. | 1 |
| `Weakness` | Number | Applies the 'Weakness' effect. | 1 |

</details>

---

### Context: `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | Applies the 'Bruise' effect. | 1 |

</details>

---

### Context: `AddStatusToMeleeDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`DelayedWind`](./Passives_and_Statuses.md#context-delayedwind) | Block | Applies the 'DelayedWind' effect. | 1 |
| [`DelayedWindCone`](./Passives_and_Statuses.md#context-delayedwindcone) | Block | Creates a delayed Area of Effect cone. | 1 |

</details>

---

### Context: `AddStatusToReceivedDamage_ExcludeStatuses`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_DoesDamage`](./Passives_and_Statuses.md#context-conditional_doesdamage) | Block | Conditional block: Executes nested logic only if the target is/has DoesDamage. | 1 |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `LeechPercent` | Number | Applies the 'LeechPercent' effect. | 1 |

</details>

---

### Context: `AddStatusesIfPersistentWeatherElement`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | Applies the 'Burn' effect. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |

</details>

---

### Context: `AddStatusesToReceivedElementalDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | Applies the 'Burn' effect. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |

</details>

---

### Context: `AddTemporaryEffectsToEquipment`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | Applies the 'CastAgain' effect. | 1 |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 1 |
| `Shield` | Number | Applies the 'Shield' effect. | 1 |

</details>

---

### Context: `Autism`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `innate` | Number |  | 1 |
| `learned` | Number |  | 1 |

</details>

---

### Context: `AutocastEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to trigger or reference. | 1 |
| `advantage_polarity` | Number |  | 1 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 1 |

</details>

---

### Context: `ChanceToRevive`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 1 |
| [`statuses`](./Passives_and_Statuses.md#context-statuses) | Block |  | 1 |

</details>

---

### Context: `ChangeTile`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `aoe` | Number | The area of effect or distance in tiles. | 1 |
| [`tile`](./Enums.md#enum-tile) | Enum/String | The specific tile type to change into (e.g., GlassTile). | 1 |

</details>

---

### Context: `CollectPickupsOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `pop_corpses` | Boolean |  | 1 |

</details>

---

### Context: `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | Applies the 'Charmed' effect. | 1 |
| `Stun` | Number | Applies the 'Stun' effect. | 1 |

</details>

---

### Context: `Conditional_DoesDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage_ExcludeStatuses`](./Passives_and_Statuses.md#context-addstatustoreceiveddamage_excludestatuses)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Bleed`](./Arrays.md#array-bleed) | Array | Applies the 'Bleed' effect. | 1 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `UseRandomSpell_Madness` | Number | Applies the 'UseRandomSpell_Madness' effect. | 1 |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 1 |

</details>

---

### Context: `Conditional_SourceHasTag`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally) | Block | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String | The specific entity tag required or applied. | 1 |

</details>

---

### Context: `DamageIfDidntUseSpecificAbility`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to trigger or reference. | 1 |
| `damage` | Number | The base damage properties of an attack. | 1 |

</details>

---

### Context: `DamageNeighborTilesWhenCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`fire`](./Passives_and_Statuses.md#context-fire) | Block |  | 1 |
| [`ice`](./Passives_and_Statuses.md#context-ice) | Block |  | 1 |
| [`lightning`](./Passives_and_Statuses.md#context-lightning) | Block |  | 1 |
| [`triattack`](./Passives_and_Statuses.md#context-triattack) | Block |  | 1 |

</details>

---

### Context: `DelayedWind`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `distance` | Number | The area of effect or distance in tiles. | 1 |

</details>

---

### Context: `DelayedWindCone`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `distance` | Number | The area of effect or distance in tiles. | 1 |

</details>

---

### Context: `Diabetes`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 1 |
| `Confusion` | Number | Applies the 'Confusion' effect. | 1 |

</details>

---

### Context: `EnergyStorm`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number |  | 1 |
| `period` | Number |  | 1 |

</details>

---

### Context: `FindItemFromPool`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum/String | Probability of finding the item. | 1 |
| [`pool`](./Enums.md#enum-pool) | Enum/String | The item pool to draw from. | 1 |

</details>

---

### Context: `ForceMoveAway`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusAdjacentOnTheirTurnBegin`](./Passives_and_Statuses.md#context-statusadjacentontheirturnbegin)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `free` | Boolean |  | 1 |

</details>

---

### Context: `FurnitureStats`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Appeal` | Number | Applies the 'Appeal' effect. | 1 |
| `Comfort` | Number | Applies the 'Comfort' effect. | 1 |
| `Stimulation` | Number | Applies the 'Stimulation' effect. | 1 |

</details>

---

### Context: `MegaMinions`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number |  | 1 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 1 |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum/String |  | 1 |

</details>

---

### Context: `PassiveLevelScaledStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Shield` | String | Applies the 'Shield' effect. | 1 |
| `SizeScalePercent` | String | Applies the 'SizeScalePercent' effect. | 1 |
| [`Trample`](./Arrays.md#array-trample) | Array | Applies the 'Trample' effect. | 1 |

</details>

---

### Context: `ReplaceBrain`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum/String |  | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum/String |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `Robot`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean |  | 1 |

</details>

---

### Context: `ScaledStatusOnBleedDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | Applies the 'Charge' effect. | 1 |

</details>

---

### Context: `ScaledStatusOnLoseShield`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | Applies the 'Thorns' effect. | 1 |

</details>

---

### Context: `ScaledStatusOnOverHealed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `SpawnScaledRotFly` | Number | Applies the 'SpawnScaledRotFly' effect. | 1 |

</details>

---

### Context: `SelfDamageWhenDealDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Context: `StackingDodgeChanceOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `amount` | Number | The numerical quantity. | 1 |
| `cap` | Number |  | 1 |

</details>

---

### Context: `StatusAdjacentOnTheirTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ForceMoveAway`](./Passives_and_Statuses.md#context-forcemoveaway) | Block | Applies the 'ForceMoveAway' effect. | 1 |

</details>

---

### Context: `StatusAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `RandomStatUp` | Number | Applies the 'RandomStatUp' effect. | 1 |
| `exclude_self` | Boolean |  | 1 |

</details>

---

### Context: `StatusAlliesOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | Applies the 'ManaGain' effect. | 1 |

</details>

---

### Context: `StatusAlliesScaledByCursedOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | Applies the 'LuckUp' effect. | 1 |

</details>

---

### Context: `StatusIfBattleAlreadyBegan`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `PermanentMadness` | Number | Applies the 'PermanentMadness' effect. | 1 |

</details>

---

### Context: `StatusOnEatPill`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 1 |

</details>

---

### Context: `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum/String | Spawns a specific character or entity upon impact. | 1 |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |
| `Thorns` | Number | Applies the 'Thorns' effect. | 1 |

</details>

---

### Context: `StatusOnLoseShield`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | Applies the 'Thorns' effect. | 1 |

</details>

---

### Context: `StatusOnTakeHealthDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `PermanentConstitution` | Number | Applies the 'PermanentConstitution' effect. | 1 |

</details>

---

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | Applies the 'ManaGain' effect. | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Context: `StrengthInNumbersAura`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `count_self` | Boolean |  | 1 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 1 |

</details>

---

### Context: `Study`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `marked` | Number |  | 1 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 1 |

</details>

---

### Context: `TakeBonusTurnWithStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | Applies the Madness debuff/status effect. | 1 |

</details>

---

### Context: `TheHunger`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | Applies the Madness debuff/status effect. | 1 |

</details>

---

### Context: `TileDamageMultiplier`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `ally_multiplier` | Number |  | 1 |
| `multiplier` | Number | Multiplicative modifier to a base value. | 1 |

</details>

---

### Context: `TourettesMeows`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`cooldown`](./Arrays.md#array-cooldown) | Array |  | 1 |
| [`pool`](./Arrays.md#array-pool) | Array |  | 1 |

</details>

---

### Context: `fire`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Context: `ice`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Context: `lightning`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Context: `triattack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | The classification type (e.g., damage type or element). | 1 |

</details>

---

