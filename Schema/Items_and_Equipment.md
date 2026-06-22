# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Items & Equipment

> **Associated Files:** `data/items/, data/item_setbonuses.gon`


### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1116

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String | {'type': '`String`', 'df': "Localization key for the item's desc."} | 1116 |
| `frame` | Number | {'type': '`Number`', 'df': ''} | 1106 |
| [`kind`](./Enums.md#enum-kind) | Enum | {'type': '`Enum/String`', 'df': ''} | 1106 |
| [`name`](./Strings.md#string-name) | String | {'type': '`String`', 'df': "Localization key for the item's name."} | 1105 |
| [`rarity`](./Enums.md#enum-rarity) | Enum | {'type': '`Enum/String`', 'df': ''} | 967 |
| [`set`](./Enums.md#enum-set) | Enum | {'type': '`Enum/String`', 'df': ''} | 765 |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | {'type': '`Block`', 'df': 'Passives granted by equipping this. | 727 |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'ID of the ability to trigger or reference.'} | 365 |
| `shield` | Number | {'type': '`Number`', 'df': ''} | 178 |
| `durability` | Number | {'type': '`Number`', 'df': 'Maximum uses before breaking.'} | 171 |
| `cursed` | Boolean | {'type': '`Boolean`', 'df': ''} | 77 |
| `cha` | Number | {'type': '`Number`', 'df': ''} | 74 |
| `consumable` | Boolean | {'type': '`Boolean`', 'df': ''} | 64 |
| `spd` | Number | {'type': '`Number`', 'df': ''} | 57 |
| `con` | Number | {'type': '`Number`', 'df': ''} | 53 |
| `int` | Number | {'type': '`Number`', 'df': ''} | 53 |
| `lck` | Number | {'type': '`Number`', 'df': ''} | 41 |
| `quest_item` | Boolean | {'type': '`Boolean`', 'df': ''} | 40 |
| `parasite` | Boolean | {'type': '`Boolean`', 'df': ''} | 36 |
| `aux` | Number | {'type': '`Number`', 'df': ''} | 33 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum | {'type': '`Enum/String`', 'df': ''} | 29 |
| `str` | Mixed | {'type': '`Number`', 'df': ''} | 28 |
| `dex` | Number | {'type': '`Number`', 'df': ''} | 22 |
| [`quest_reward_item`](./Enums.md#enum-quest_reward_item) | Enum | {'type': '`Enum/String`', 'df': ''} | 22 |
| `indestructible` | Boolean | {'type': '`Boolean`', 'df': ''} | 20 |
| `legacy_quest` | Boolean | {'type': '`Boolean`', 'df': ''} | 17 |
| [`hint_destination`](./Enums.md#enum-hint_destination) | Enum | {'type': '`Enum/String`', 'df': ''} | 16 |
| `divine_shield` | Number | {'type': '`Number`', 'df': ''} | 15 |
| [`str_aux_initialize`](./Enums.md#enum-str_aux_initialize) | Enum | {'type': '`Enum/String`', 'df': ''} | 15 |
| `dont_destroy_on_0` | Boolean | {'type': '`Boolean`', 'df': ''} | 13 |
| [`global_tags`](./Arrays.md#array-global_tags) | Array | {'type': '`Array`', 'df': ''} | 12 |
| `max_durability` | Number | {'type': '`Number`', 'df': ''} | 11 |
| [`on_store`](./Enums.md#enum-on_store) | Enum | {'type': '`Enum/String`', 'df': ''} | 8 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 6 |
| [`hint_prerequisite_flag`](./Enums.md#enum-hint_prerequisite_flag) | Enum | {'type': '`Enum/String`', 'df': ''} | 5 |
| `failable` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| [`global_passives`](./Items_and_Equipment.md#context-global_passives) | Block | {'type': '`Block`', 'df': " | 4 |
| `randomize_piece_frames` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| `str_aux_is_copy_passive` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| `fragile` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| [`icon_hint`](./Enums.md#enum-icon_hint) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| `max_health` | Number | {'type': '`Number`', 'df': ''} | 3 |
| `reset_aux_on_store` | Number | {'type': '`Number`', 'df': ''} | 3 |
| `sticky` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| `weightless` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| [`keyword_tooltips`](./Items_and_Equipment.md#context-keyword_tooltips) | Block | {'type': '`Block`', 'df': "Forces specific UI tooltips to appear when hovering over the ability. | 2 |
| [`passive`](./Items_and_Equipment.md#context-passive) | Block | {'type': '`Block`', 'df': " | 2 |
| `prevent_level_up` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| [`quest_item_alias`](./Enums.md#enum-quest_item_alias) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| `speed` | Number | {'type': '`Number`', 'df': ''} | 2 |
| [`str_aux_is_copy_ability`](./Items_and_Equipment.md#context-str_aux_is_copy_ability) | Block | {'type': '`Block`', 'df': ' | 2 |
| `str_aux_is_copy_item_passive` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| [`Set`](./Enums.md#enum-set) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'Set' effect/state."} | 1 |
| `aux_is_catid` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `cant_equip_to_colorless` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `degrade_after_adventure` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`equip_sound`](./Enums.md#enum-equip_sound) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `force_sticky` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`reset_str_aux_on_store`](./Enums.md#enum-reset_str_aux_on_store) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`str_aux`](./Enums.md#enum-str_aux) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `str_aux_is_copy_item_active` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `str_aux_is_copy_item_icon` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 748

> **Referenced by:** [`PassiveAfterXKills`](./Items_and_Equipment.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Items_and_Equipment.md#context-passiveathealththreshold), [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold), [`PassiveIfStrAuxEquals`](./Items_and_Equipment.md#context-passiveifstrauxequals), [`PassiveWhenAffectedByElement`](./Items_and_Equipment.md#context-passivewhenaffectedbyelement), [`PassiveWhenOnTile`](./Items_and_Equipment.md#context-passivewhenontile), [`ROOT`](./Items_and_Equipment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Metal` | Number | {'type': '`Number`', 'df': "Applies or references the 'Metal' effect/state."} | 89 |
| [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack) | Block | {'type': '`Block`', 'df': 'Injects a status effect payload that applies whenever the character performs a basic attack.'} | 64 |
| `Brace` | Number | {'type': 'Number', 'df': "Applies or references the 'Brace' effect/state."} | 44 |
| `Thorns` | Number | {'type': '`Number`', 'df': "Applies or references the 'Thorns' effect/state."} | 41 |
| `HealthRegenUp` | Number | {'type': 'Number', 'df': "Applies or references the 'HealthRegenUp' effect/state."} | 36 |
| [`MeleeRevengeDamage`](./Items_and_Equipment.md#context-meleerevengedamage) | Block | {'type': '`Block`', 'df': 'Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. | 32 |
| `Brittle` | Number | {'type': '`Number`', 'df': "Applies or references the 'Brittle' effect/state."} | 24 |
| [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend) | Block | {'type': '`Block`', 'df': "Applies the nested status effects when the encounter finishes. | 24 |
| `Fragile` | Number | {'type': '`Number`', 'df': "Applies or references the 'Fragile' effect/state."} | 22 |
| [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusEachTurnEnd' effect/state. | 22 |
| [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 22 |
| [`SpawnOnBattleStart`](./Items_and_Equipment.md#context-spawnonbattlestart) | Block | {'type': '`Enum/String`', 'df': "Applies or references the 'SpawnOnBattleStart' effect/state."} | 21 |
| `ArmorDodgeChance` | Number | {'type': '`Number`', 'df': "Applies or references the 'ArmorDodgeChance' effect/state."} | 17 |
| `DamageUp` | Number | {'type': 'Number', 'df': "Applies or references the 'DamageUp' effect/state."} | 16 |
| [`StatusOnKill`](./Items_and_Equipment.md#context-statusonkill) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 16 |
| [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 16 |
| `Flammable` | Number | {'type': '`Number`', 'df': "Applies or references the 'Flammable' effect/state."} | 13 |
| [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 13 |
| `AddBonusRange` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddBonusRange' effect/state."} | 11 |
| [`SpawnThingOnDamage`](./Items_and_Equipment.md#context-spawnthingondamage) | Block | {'type': '`Block`', 'df': "Applies or references the 'SpawnThingOnDamage' effect/state. | 11 |
| [`SpawnEachTurn`](./Items_and_Equipment.md#context-spawneachturn) | Block | {'type': '`Block`', 'df': "Applies or references the 'SpawnEachTurn' effect/state. | 10 |
| `BleedThorns` | Number | {'type': '`Number`', 'df': "Applies or references the 'BleedThorns' effect/state."} | 9 |
| [`RevengeDamage`](./Items_and_Equipment.md#context-revengedamage) | Block | {'type': '`Block`', 'df': 'Reaction trigger: Deals damage to the attacker when hit. | 9 |
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'SpawnThingOnDeath' effect/state."} | 9 |
| [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusEachTurnBegin' effect/state."} | 9 |
| [`StatusImmunity`](./Arrays.md#array-statusimmunity) | Array | {'type': '`Enum/String`', 'df': "Applies or references the 'StatusImmunity' effect/state."} | 9 |
| [`AddSelfStatusToBasicAttack`](./Items_and_Equipment.md#context-addselfstatustobasicattack) | Block | {'type': '`Block`', 'df': "Applies or references the 'AddSelfStatusToBasicAttack' effect/state. | 8 |
| `KineticSpikes` | Number | {'type': '`Number`', 'df': "Applies or references the 'KineticSpikes' effect/state."} | 8 |
| [`AbilityOnBattleStart`](./Enums.md#enum-abilityonbattlestart) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'AbilityOnBattleStart' effect/state."} | 7 |
| `AddManaRegen` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddManaRegen' effect/state."} | 7 |
| [`BrittleDuringElement`](./Enums.md#enum-brittleduringelement) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'BrittleDuringElement' effect/state."} | 7 |
| [`DurabilityTransform`](./Items_and_Equipment.md#context-durabilitytransform) | Block | {'type': '`Block`', 'df': "Applies or references the 'DurabilityTransform' effect/state. | 7 |
| `ManaCostReduction` | Number | {'type': '`Number`', 'df': "Applies or references the 'ManaCostReduction' effect/state."} | 7 |
| [`PassiveIfStrAuxEquals`](./Items_and_Equipment.md#context-passiveifstrauxequals) | Block | {'type': '`Block`', 'df': "Applies or references the 'PassiveIfStrAuxEquals' effect/state. | 7 |
| [`StatusOnKillEnemy`](./Items_and_Equipment.md#context-statusonkillenemy) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 7 |
| `AddCorpseHealth` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddCorpseHealth' effect/state."} | 6 |
| `AddLevelUpRerolls` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddLevelUpRerolls' effect/state."} | 6 |
| [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage) | Block | {'type': '`Block`', 'df': "Modifier: Injects a status effect into a specific action. | 6 |
| `CritChanceUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'CritChanceUp' effect/state."} | 6 |
| [`ItemAuxTransform`](./Items_and_Equipment.md#context-itemauxtransform) | Block | {'type': '`Block`', 'df': "Applies or references the 'ItemAuxTransform' effect/state. | 6 |
| [`PassiveWhenOnTile`](./Items_and_Equipment.md#context-passivewhenontile) | Block | {'type': '`Block`', 'df': 'State Trigger: Grants passives when this condition is met. | 6 |
| [`StatusAlliesOnBattleStart`](./Items_and_Equipment.md#context-statusalliesonbattlestart) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusAlliesOnBattleStart' effect/state. | 6 |
| [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie) | Block | {'type': '`Block`', 'df': 'Event Trigger: Applies statuses when this action occurs. | 6 |
| `AllStatsUp` | Number | {'type': 'Number', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 5 |
| `BoostHeals` | Number | {'type': '`Number`', 'df': "Applies or references the 'BoostHeals' effect/state."} | 5 |
| `Bruise` | Number | {'type': 'Number', 'df': "Applies or references the 'Bruise' effect/state."} | 5 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ElementImmune' effect/state."} | 5 |
| [`OverrideBasicAttack`](./Enums.md#enum-overridebasicattack) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'OverrideBasicAttack' effect/state."} | 5 |
| `PoisonThorns` | Number | {'type': '`Number`', 'df': "Applies or references the 'PoisonThorns' effect/state."} | 5 |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ReplaceBasicMove' effect/state."} | 5 |
| `SpellDamageUp` | Number | {'type': 'Number', 'df': "Applies or references the 'SpellDamageUp' effect/state."} | 5 |
| [`StatusOnEndMove`](./Items_and_Equipment.md#context-statusonendmove) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 5 |
| `Trample` | Number | {'type': '`Number`', 'df': "Applies or references the 'Trample' effect/state."} | 5 |
| [`TransformItemOnElementInfluence`](./Items_and_Equipment.md#context-transformitemonelementinfluence) | Block | {'type': '`Block`', 'df': "Applies or references the 'TransformItemOnElementInfluence' effect/state. | 5 |
| `TrinketPassiveMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies or references the 'TrinketPassiveMultiplierBonus' effect/state."} | 5 |
| [`AddDamageToElementDamage`](./Items_and_Equipment.md#context-adddamagetoelementdamage) | Block | {'type': '`Block`', 'df': "Applies or references the 'AddDamageToElementDamage' effect/state. | 4 |
| [`AddPassivesToMinions`](./Items_and_Equipment.md#context-addpassivestominions) | Block | {'type': '`Block`', 'df': "Applies or references the 'AddPassivesToMinions' effect/state. | 4 |
| [`AddTag`](./Enums.md#enum-addtag) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'AddTag' effect/state."} | 4 |
| [`AmplifyStatus`](./Enums.md#enum-amplifystatus) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'AmplifyStatus' effect/state."} | 4 |
| `Bleed` | Number | {'type': 'Number', 'df': "Applies or references the 'Bleed' effect/state."} | 4 |
| `BreakAtAux` | Number | {'type': '`Number`', 'df': "Applies or references the 'BreakAtAux' effect/state."} | 4 |
| [`ChanceToRevive`](./Items_and_Equipment.md#context-chancetorevive) | Block | {'type': '`Number`', 'df': "Applies or references the 'ChanceToRevive' effect/state."} | 4 |
| [`DelayedAutoRevive`](./Items_and_Equipment.md#context-delayedautorevive) | Block | {'type': '`Block`', 'df': "Applies or references the 'DelayedAutoRevive' effect/state. | 4 |
| `DepressionAura` | Number | {'type': '`Number`', 'df': "Applies or references the 'DepressionAura' effect/state."} | 4 |
| `DodgeChance_Status` | Number | {'type': 'Number', 'df': "Applies or references the 'DodgeChance_Status' effect/state."} | 4 |
| `ExtraBasicAttacks` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExtraBasicAttacks' effect/state."} | 4 |
| `ExtraWeaponAttacks` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExtraWeaponAttacks' effect/state."} | 4 |
| [`FragileDuringElement`](./Enums.md#enum-fragileduringelement) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'FragileDuringElement' effect/state."} | 4 |
| `MissChance` | Number | {'type': '`Number`', 'df': "Applies or references the 'MissChance' effect/state."} | 4 |
| [`PassiveAtHealthThreshold`](./Items_and_Equipment.md#context-passiveathealththreshold) | Block | {'type': '`Block`', 'df': "Applies or references the 'PassiveAtHealthThreshold' effect/state. | 4 |
| `Poison` | Number | {'type': 'Number', 'df': "Applies or references the 'Poison' effect/state."} | 4 |
| `Quivered` | Number | {'type': '`Number`', 'df': "Applies or references the 'Quivered' effect/state."} | 4 |
| [`RandomSeededStatModifier`](./Arrays.md#array-randomseededstatmodifier) | Array | {'type': '`Array`', 'df': "Applies or references the 'RandomSeededStatModifier' effect/state."} | 4 |
| [`SpawnObjectOnPopCorpse`](./Items_and_Equipment.md#context-spawnobjectonpopcorpse) | Block | {'type': '`Enum/String`', 'df': "Applies or references the 'SpawnObjectOnPopCorpse' effect/state."} | 4 |
| [`StatusOnTakeHealthOrShieldDamage`](./Items_and_Equipment.md#context-statusontakehealthorshielddamage) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 4 |
| [`StatusRandomEnemiesOnBattleStart`](./Items_and_Equipment.md#context-statusrandomenemiesonbattlestart) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusRandomEnemiesOnBattleStart' effect/state. | 4 |
| `AddBonusMeleeRange` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddBonusMeleeRange' effect/state."} | 3 |
| `AddEndOfCombatRegen` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddEndOfCombatRegen' effect/state."} | 3 |
| `AllStatsUpPerDisorder` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUpPerDisorder' effect/state."} | 3 |
| `AlphaTurns` | Number | {'type': '`Number`', 'df': "Applies or references the 'AlphaTurns' effect/state."} | 3 |
| `BoneArmorPassive` | Number | {'type': '`Number`', 'df': "Applies or references the 'BoneArmorPassive' effect/state."} | 3 |
| [`BreakOnElement`](./Enums.md#enum-breakonelement) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'BreakOnElement' effect/state."} | 3 |
| `Burn` | Number | {'type': 'Number', 'df': "Applies or references the 'Burn' effect/state."} | 3 |
| `CantCatchDiseases` | Number | {'type': '`Number`', 'df': "Applies or references the 'CantCatchDiseases' effect/state."} | 3 |
| `CantSpreadDiseases` | Number | {'type': '`Number`', 'df': "Applies or references the 'CantSpreadDiseases' effect/state."} | 3 |
| [`CatchProjectiles`](./Items_and_Equipment.md#context-catchprojectiles) | Block | {'type': '`Block`', 'df': "Applies or references the 'CatchProjectiles' effect/state. | 3 |
| `ChanceToBlock` | Number | {'type': '`Number`', 'df': "Applies or references the 'ChanceToBlock' effect/state."} | 3 |
| [`ClassManaCostReduction`](./Items_and_Equipment.md#context-classmanacostreduction) | Block | {'type': '`Block`', 'df': "Applies or references the 'ClassManaCostReduction' effect/state. | 3 |
| `Confusion` | Number | {'type': 'Number', 'df': "Applies or references the 'Confusion' effect/state."} | 3 |
| `CopyPassiveSlot` | Number | {'type': '`Number`', 'df': "Applies or references the 'CopyPassiveSlot' effect/state."} | 3 |
| [`CounterAttack`](./Items_and_Equipment.md#context-counterattack) | Block | {'type': '`Block`', 'df': "Applies or references the 'CounterAttack' effect/state. | 3 |
| [`DisableAbilities`](./Enums.md#enum-disableabilities) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'DisableAbilities' effect/state."} | 3 |
| [`DropAsFamiliarOnArmorBreak`](./Enums.md#enum-dropasfamiliaronarmorbreak) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'DropAsFamiliarOnArmorBreak' effect/state."} | 3 |
| [`ExtraStatusWhenDealingDamage`](./Items_and_Equipment.md#context-extrastatuswhendealingdamage) | Block | {'type': '`Block`', 'df': "Applies or references the 'ExtraStatusWhenDealingDamage' effect/state. | 3 |
| `FaceArmorPassiveMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies or references the 'FaceArmorPassiveMultiplierBonus' effect/state."} | 3 |
| `HeadArmorPassiveMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies or references the 'HeadArmorPassiveMultiplierBonus' effect/state."} | 3 |
| `IncreaseExplosionSize` | Number | {'type': '`Number`', 'df': "Applies or references the 'IncreaseExplosionSize' effect/state."} | 3 |
| [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead) | Block | {'type': '`Block`', 'df': "State Trigger: Grants passives when this condition is met. | 3 |
| `RockyArmorPassive` | Number | {'type': '`Number`', 'df': "Applies or references the 'RockyArmorPassive' effect/state."} | 3 |
| [`SpawnExtraThingsOnBattleStart`](./Items_and_Equipment.md#context-spawnextrathingsonbattlestart) | Block | {'type': '`Block`', 'df': "Applies or references the 'SpawnExtraThingsOnBattleStart' effect/state. | 3 |
| [`SpawnOnBattleStartRandomEmptyTile`](./Items_and_Equipment.md#context-spawnonbattlestartrandomemptytile) | Block | {'type': '`Block`', 'df': "Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state. | 3 |
| [`StackingFlowerTrail`](./Items_and_Equipment.md#context-stackingflowertrail) | Block | {'type': '`Block`', 'df': "Applies or references the 'StackingFlowerTrail' effect/state. | 3 |
| [`StatusAllCharactersOnSpawn`](./Items_and_Equipment.md#context-statusallcharactersonspawn) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusAllCharactersOnSpawn' effect/state. | 3 |
| [`StatusEveryXSpellCasts`](./Items_and_Equipment.md#context-statuseveryxspellcasts) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusEveryXSpellCasts' effect/state. | 3 |
| [`StatusOnPopCorpse`](./Items_and_Equipment.md#context-statusonpopcorpse) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 3 |
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](./Items_and_Equipment.md#context-statusonturnendifdidntcastabilitytypes) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 3 |
| `TrueShot` | Number | {'type': '`Number`', 'df': "Applies or references the 'TrueShot' effect/state."} | 3 |
| `AddInitiative` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddInitiative' effect/state."} | 2 |
| `AddKnockbackDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddKnockbackDamage' effect/state."} | 2 |
| [`AddStatusToElementDamage`](./Items_and_Equipment.md#context-addstatustoelementdamage) | Block | {'type': '`Block`', 'df': "Modifier: Injects a status effect into a specific action. | 2 |
| [`AddStatusToKnockbackDamage`](./Items_and_Equipment.md#context-addstatustoknockbackdamage) | Block | {'type': '`Block`', 'df': "Modifier: Injects a status effect into a specific action. | 2 |
| [`AddStatusToSpells`](./Items_and_Equipment.md#context-addstatustospells) | Block | {'type': '`Block`', 'df': "Modifier: Injects a status effect into a specific action. | 2 |
| `AmplifyKnockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'AmplifyKnockback' effect/state."} | 2 |
| [`ApplyStatusesToRandomEnemiesEachTurn`](./Items_and_Equipment.md#context-applystatusestorandomenemieseachturn) | Block | {'type': '`Block`', 'df': "Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state. | 2 |
| [`ArmorBreakOnHit`](./Items_and_Equipment.md#context-armorbreakonhit) | Block | {'type': '`Block`', 'df': "Applies or references the 'ArmorBreakOnHit' effect/state. | 2 |
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'BonusAbility' effect/state."} | 2 |
| [`BoostWeaponDamage`](./Items_and_Equipment.md#context-boostweapondamage) | Block | {'type': '`Block`', 'df': "Applies or references the 'BoostWeaponDamage' effect/state. | 2 |
| `BreakWhenNoShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'BreakWhenNoShield' effect/state."} | 2 |
| `CanLevelUpWhenDead` | Number | {'type': '`Number`', 'df': "Applies or references the 'CanLevelUpWhenDead' effect/state."} | 2 |
| [`ChanceToBackflip`](./Items_and_Equipment.md#context-chancetobackflip) | Block | {'type': '`Block`', 'df': "Applies or references the 'ChanceToBackflip' effect/state. | 2 |
| [`ChanceToBlockAndCounter`](./Items_and_Equipment.md#context-chancetoblockandcounter) | Block | {'type': '`Number`', 'df': "Applies or references the 'ChanceToBlockAndCounter' effect/state."} | 2 |
| [`DeathRattleRevive`](./Enums.md#enum-deathrattlerevive) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'DeathRattleRevive' effect/state."} | 2 |
| `DisablePassiveSlot` | Number | {'type': '`Number`', 'df': "Applies or references the 'DisablePassiveSlot' effect/state."} | 2 |
| `DodgeChance` | Number | {'type': '`Number`', 'df': "Applies or references the 'DodgeChance' effect/state."} | 2 |
| [`ElementalManaCostReduction`](./Items_and_Equipment.md#context-elementalmanacostreduction) | Block | {'type': '`Block`', 'df': "Applies or references the 'ElementalManaCostReduction' effect/state. | 2 |
| `Flying` | Number | {'type': '`Number`', 'df': "Applies or references the 'Flying' effect/state."} | 2 |
| `IncreaseExplosionDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'IncreaseExplosionDamage' effect/state."} | 2 |
| `InjuryImmunity` | Number | {'type': '`Number`', 'df': "Applies or references the 'InjuryImmunity' effect/state."} | 2 |
| [`KillsToMeat`](./Enums.md#enum-killstomeat) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'KillsToMeat' effect/state."} | 2 |
| [`LeaveBehindOnceEachMove`](./Enums.md#enum-leavebehindonceeachmove) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'LeaveBehindOnceEachMove' effect/state."} | 2 |
| [`LevelUpClassOverride`](./Enums.md#enum-levelupclassoverride) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'LevelUpClassOverride' effect/state."} | 2 |
| `MoveQuivered` | Number | {'type': '`Number`', 'df': "Applies or references the 'MoveQuivered' effect/state."} | 2 |
| `NeckArmorPassiveMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies or references the 'NeckArmorPassiveMultiplierBonus' effect/state."} | 2 |
| [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold) | Block | {'type': '`Block`', 'df': "Applies or references the 'PassiveAtStatThreshold' effect/state. | 2 |
| [`PassiveIfWeaponIsUsable`](./Items_and_Equipment.md#context-passiveifweaponisusable) | Block | {'type': '`Block`', 'df': "Applies or references the 'PassiveIfWeaponIsUsable' effect/state. | 2 |
| `PermanentMadness` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentMadness' effect/state."} | 2 |
| `RangedTrueShot` | Number | {'type': '`Number`', 'df': "Applies or references the 'RangedTrueShot' effect/state."} | 2 |
| `ReflectProjectiles` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReflectProjectiles' effect/state."} | 2 |
| [`RefreshEquipmentAbilityOnElement`](./Items_and_Equipment.md#context-refreshequipmentabilityonelement) | Block | {'type': '`Block`', 'df': 'Applies or references the \'RefreshEquipmentAbilityOnElement\' effect/state. | 2 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ReplaceBasicAttack' effect/state."} | 2 |
| [`ReplaceSpawnedObjects`](./Arrays.md#array-replacespawnedobjects) | Array | {'type': '`Array`', 'df': "Applies or references the 'ReplaceSpawnedObjects' effect/state."} | 2 |
| [`SetDefaultFacePassive`](./Enums.md#enum-setdefaultfacepassive) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'SetDefaultFacePassive' effect/state."} | 2 |
| [`SpawnItemLinkedFamiliar`](./Items_and_Equipment.md#context-spawnitemlinkedfamiliar) | Block | {'type': '`Block`', 'df': "Applies or references the 'SpawnItemLinkedFamiliar' effect/state. | 2 |
| `SpawnNearEnemies` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpawnNearEnemies' effect/state."} | 2 |
| [`StatusAfterCastSpell`](./Items_and_Equipment.md#context-statusaftercastspell) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusAfterCastSpell' effect/state. | 2 |
| [`StatusIfUnusedActPoints`](./Items_and_Equipment.md#context-statusifunusedactpoints) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusIfUnusedActPoints' effect/state. | 2 |
| [`StatusOnAllyCatDeath`](./Items_and_Equipment.md#context-statusonallycatdeath) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnBackstab`](./Items_and_Equipment.md#context-statusonbackstab) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnBreakItem`](./Items_and_Equipment.md#context-statusonbreakitem) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnCastSpell`](./Items_and_Equipment.md#context-statusoncastspell) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnGainCoins`](./Items_and_Equipment.md#context-statusongaincoins) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 2 |
| `TrinketActiveEffectsMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies or references the 'TrinketActiveEffectsMultiplierBonus' effect/state."} | 2 |
| `Uncontrollable` | Number | {'type': '`Number`', 'df': "Applies or references the 'Uncontrollable' effect/state."} | 2 |
| [`AIControlNextTurn`](./Items_and_Equipment.md#context-aicontrolnextturn) | Block | {'type': '`Block`', 'df': "Applies or references the 'AIControlNextTurn' effect/state. | 1 |
| `AOEBonus` | Number | {'type': '`Number`', 'df': "Applies or references the 'AOEBonus' effect/state."} | 1 |
| [`AbilityHealthThreshold`](./Items_and_Equipment.md#context-abilityhealththreshold) | Block | {'type': '`Block`', 'df': 'Applies or references the \'AbilityHealthThreshold\' effect/state. | 1 |
| [`AbilityOnRoundEndOnce`](./Items_and_Equipment.md#context-abilityonroundendonce) | Block | {'type': '`Block`', 'df': "Applies or references the 'AbilityOnRoundEndOnce' effect/state. | 1 |
| [`AbilityReaction`](./Enums.md#enum-abilityreaction) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'AbilityReaction' effect/state."} | 1 |
| [`AddAdvantageToEvent`](./Items_and_Equipment.md#context-addadvantagetoevent) | Block | {'type': '`Block`', 'df': "Applies or references the 'AddAdvantageToEvent' effect/state. | 1 |
| `AddCritMultiplier` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddCritMultiplier' effect/state."} | 1 |
| [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'AddElementsToBasicAttack' effect/state."} | 1 |
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'AddHiddenTag' effect/state."} | 1 |
| [`AddPassivesToCharmed`](./Items_and_Equipment.md#context-addpassivestocharmed) | Block | {'type': '`Block`', 'df': "Applies or references the 'AddPassivesToCharmed' effect/state. | 1 |
| [`AddSelfStatusToWeapons`](./Items_and_Equipment.md#context-addselfstatustoweapons) | Block | {'type': '`Block`', 'df': "Applies or references the 'AddSelfStatusToWeapons' effect/state. | 1 |
| [`AddStatusToBackstabs`](./Items_and_Equipment.md#context-addstatustobackstabs) | Block | {'type': '`Block`', 'df': "Modifier: Injects a status effect into a specific action. | 1 |
| [`AddStatusToWeapons`](./Items_and_Equipment.md#context-addstatustoweapons) | Block | {'type': '`Block`', 'df': "Modifier: Injects a status effect into a specific action. | 1 |
| [`AddTemporaryEffectsToBasicAttack`](./Items_and_Equipment.md#context-addtemporaryeffectstobasicattack) | Block | {'type': '`Block`', 'df': "Applies or references the 'AddTemporaryEffectsToBasicAttack' effect/state. | 1 |
| `AllSpellsCostCharge` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllSpellsCostCharge' effect/state."} | 1 |
| `AllUnitsExplodeOnDeath` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllUnitsExplodeOnDeath' effect/state."} | 1 |
| `AlliesScrambleSpellAfterCast` | Number | {'type': '`Number`', 'df': "Applies or references the 'AlliesScrambleSpellAfterCast' effect/state."} | 1 |
| [`AlluringDoodieEater`](./Items_and_Equipment.md#context-alluringdoodieeater) | Block | {'type': '`Block`', 'df': "Applies or references the 'AlluringDoodieEater' effect/state. | 1 |
| `AllyDamageReduction` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllyDamageReduction' effect/state."} | 1 |
| [`AllyDodgeChanceAura`](./Items_and_Equipment.md#context-allydodgechanceaura) | Block | {'type': '`Block`', 'df': "Applies or references the 'AllyDodgeChanceAura' effect/state. | 1 |
| `AlphaAllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AlphaAllStatsUp' effect/state."} | 1 |
| `AlphaCat` | Number | {'type': '`Number`', 'df': "Applies or references the 'AlphaCat' effect/state."} | 1 |
| `AlwaysChosenForLevelUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AlwaysChosenForLevelUp' effect/state."} | 1 |
| `AutoEquipConsumables` | Number | {'type': '`Number`', 'df': "Applies or references the 'AutoEquipConsumables' effect/state."} | 1 |
| [`BackflipWhenTargeted`](./Items_and_Equipment.md#context-backflipwhentargeted) | Block | {'type': 'Enum/String', 'df': 'Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack.'} | 1 |
| [`BackstabCritChance`](./Enums.md#enum-backstabcritchance) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'BackstabCritChance' effect/state."} | 1 |
| `BalanceStats` | Number | {'type': '`Number`', 'df': "Applies or references the 'BalanceStats' effect/state."} | 1 |
| `BasicAttackCantMiss` | Number | {'type': '`Number`', 'df': "Applies or references the 'BasicAttackCantMiss' effect/state."} | 1 |
| [`BasicAttackCritChance`](./Enums.md#enum-basicattackcritchance) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'BasicAttackCritChance' effect/state."} | 1 |
| `Blind` | Number | {'type': '`Number`', 'df': "Applies or references the 'Blind' effect/state."} | 1 |
| `BlockDamageUnderThreshold` | Number | {'type': '`Number`', 'df': "Applies or references the 'BlockDamageUnderThreshold' effect/state."} | 1 |
| `BlockNegativeStatus` | Number | {'type': '`Number`', 'df': "Applies or references the 'BlockNegativeStatus' effect/state."} | 1 |
| `BoostReceivedHealing` | Number | {'type': '`Number`', 'df': "Applies or references the 'BoostReceivedHealing' effect/state."} | 1 |
| [`BouncyProjectiles`](./Items_and_Equipment.md#context-bouncyprojectiles) | Block | {'type': '`Block`', 'df': "Applies or references the 'BouncyProjectiles' effect/state. | 1 |
| [`BuffImmunity`](./Items_and_Equipment.md#context-buffimmunity) | Block | {'type': '`Block`', 'df': "Applies or references the 'BuffImmunity' effect/state. | 1 |
| `CanRemoveCursedItems` | Number | {'type': '`Number`', 'df': "Applies or references the 'CanRemoveCursedItems' effect/state."} | 1 |
| `CapBasicAttackDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'CapBasicAttackDamage' effect/state."} | 1 |
| `CapMovementAbilityRange` | Number | {'type': '`Number`', 'df': "Applies or references the 'CapMovementAbilityRange' effect/state."} | 1 |
| [`CatPartsSizeScale`](./Items_and_Equipment.md#context-catpartssizescale) | Block | {'type': '`Block`', 'df': "Applies or references the 'CatPartsSizeScale' effect/state. | 1 |
| `ChanceToAmbush` | Number | {'type': '`Number`', 'df': "Applies or references the 'ChanceToAmbush' effect/state."} | 1 |
| [`ChanceToForceEvent`](./Items_and_Equipment.md#context-chancetoforceevent) | Block | {'type': '`Block`', 'df': "Applies or references the 'ChanceToForceEvent' effect/state. | 1 |
| `Charge` | Number | {'type': 'Number', 'df': "Applies or references the 'Charge' effect/state."} | 1 |
| `CharismaIsMaxStat` | Number | {'type': '`Number`', 'df': "Applies or references the 'CharismaIsMaxStat' effect/state."} | 1 |
| `CharmImmunity` | Number | {'type': '`Number`', 'df': "Applies or references the 'CharmImmunity' effect/state."} | 1 |
| `ConsumableEffectsMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies or references the 'ConsumableEffectsMultiplierBonus' effect/state."} | 1 |
| [`ConvertDamageToScaledStatus`](./Items_and_Equipment.md#context-convertdamagetoscaledstatus) | Block | {'type': '`Block`', 'df': "Applies or references the 'ConvertDamageToScaledStatus' effect/state. | 1 |
| `CounterNextAttacks` | Number | {'type': '`Number`', 'df': "Applies or references the 'CounterNextAttacks' effect/state."} | 1 |
| [`CreateGlobalModifiers`](./Items_and_Equipment.md#context-createglobalmodifiers) | Block | {'type': 'Block', 'df': 'Generates global map or encounter rules/modifiers.'} | 1 |
| [`CritsApplyStatus`](./Items_and_Equipment.md#context-critsapplystatus) | Block | {'type': '`Block`', 'df': "Applies or references the 'CritsApplyStatus' effect/state. | 1 |
| [`DeathRattle`](./Enums.md#enum-deathrattle) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'DeathRattle' effect/state."} | 1 |
| `DebuffImmunity` | Number | {'type': '`Number`', 'df': "Applies or references the 'DebuffImmunity' effect/state."} | 1 |
| `DoubleCastSpellIfManaCostUnderThreshold` | Number | {'type': '`Number`', 'df': "Applies or references the 'DoubleCastSpellIfManaCostUnderThreshold' effect/state."} | 1 |
| [`DoubleCastTaggedSpells`](./Enums.md#enum-doublecasttaggedspells) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'DoubleCastTaggedSpells' effect/state."} | 1 |
| `DoubleCastWeapons` | Number | {'type': '`Number`', 'df': "Applies or references the 'DoubleCastWeapons' effect/state."} | 1 |
| `DoubleReceivedNegativeStatus` | Number | {'type': '`Number`', 'df': "Applies or references the 'DoubleReceivedNegativeStatus' effect/state."} | 1 |
| `DoubleReceivedPositiveStatus` | Number | {'type': '`Number`', 'df': "Applies or references the 'DoubleReceivedPositiveStatus' effect/state."} | 1 |
| [`DropAsFamiliarOnTookDamage`](./Enums.md#enum-dropasfamiliarontookdamage) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'DropAsFamiliarOnTookDamage' effect/state."} | 1 |
| [`DropSoulJarOnDeath`](./Enums.md#enum-dropsouljarondeath) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'DropSoulJarOnDeath' effect/state."} | 1 |
| [`Eternal`](./Items_and_Equipment.md#context-eternal) | Block | {'type': '`Block`', 'df': "Applies or references the 'Eternal' effect/state. | 1 |
| [`ExcludeFromEvents`](./Enums.md#enum-excludefromevents) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ExcludeFromEvents' effect/state."} | 1 |
| `ExplosionImmunity` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExplosionImmunity' effect/state."} | 1 |
| `ExtraBasicAttacks_Status` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExtraBasicAttacks_Status' effect/state."} | 1 |
| `ExtraBasicMoves_Status` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExtraBasicMoves_Status' effect/state."} | 1 |
| `ExtraMovePoints` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExtraMovePoints' effect/state."} | 1 |
| `ExtraTrinketUses` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExtraTrinketUses' effect/state."} | 1 |
| `FaceShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'FaceShield' effect/state."} | 1 |
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md#enum-findextraitemfrompoolonbattleend) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'FindExtraItemFromPoolOnBattleEnd' effect/state."} | 1 |
| `FlowersOnEndTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'FlowersOnEndTurn' effect/state."} | 1 |
| [`FlyDamageIncrease`](./Items_and_Equipment.md#context-flydamageincrease) | Block | {'type': '`Block`', 'df': "Applies or references the 'FlyDamageIncrease' effect/state. | 1 |
| `FrankBolts` | Number | {'type': '`Number`', 'df': "Applies or references the 'FrankBolts' effect/state."} | 1 |
| `FreezePiercing` | Number | {'type': '`Number`', 'df': "Applies or references the 'FreezePiercing' effect/state."} | 1 |
| `GainExtraShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'GainExtraShield' effect/state."} | 1 |
| [`GlobalMeleeRevengeDamage`](./Items_and_Equipment.md#context-globalmeleerevengedamage) | Block | {'type': '`Block`', 'df': "Applies or references the 'GlobalMeleeRevengeDamage' effect/state. | 1 |
| `HPGainBlock` | Number | {'type': '`Number`', 'df': "Applies or references the 'HPGainBlock' effect/state."} | 1 |
| `HideSomeHudStuff` | Number | {'type': '`Number`', 'df': "Applies or references the 'HideSomeHudStuff' effect/state."} | 1 |
| `IgnoreTiles` | Number | {'type': '`Number`', 'df': "Applies or references the 'IgnoreTiles' effect/state."} | 1 |
| `IncreaseSpellRange` | Number | {'type': '`Number`', 'df': "Applies or references the 'IncreaseSpellRange' effect/state."} | 1 |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'InnateElement' effect/state."} | 1 |
| `JesterLevelUpRerolls` | Number | {'type': '`Number`', 'df': "Applies or references the 'JesterLevelUpRerolls' effect/state."} | 1 |
| `KnockbackImmunity` | Number | {'type': '`Number`', 'df': "Applies or references the 'KnockbackImmunity' effect/state."} | 1 |
| `Lifesteal` | Number | {'type': '`Number`', 'df': "Applies or references the 'Lifesteal' effect/state."} | 1 |
| `LuckUp` | Number | {'type': 'Number', 'df': "Applies or references the 'LuckUp' effect/state."} | 1 |
| `MakeBasicAttackPull` | Number | {'type': '`Number`', 'df': "Applies or references the 'MakeBasicAttackPull' effect/state."} | 1 |
| `MakeSpellsRequireCharge` | Number | {'type': '`Number`', 'df': "Applies or references the 'MakeSpellsRequireCharge' effect/state."} | 1 |
| `ModelingClayPassive` | Number | {'type': '`Number`', 'df': "Applies or references the 'ModelingClayPassive' effect/state."} | 1 |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'MoveAndUseAbilityEachTurnBeginIfPossible' effect/state."} | 1 |
| [`MoveSpeedMultiplier`](./Enums.md#enum-movespeedmultiplier) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'MoveSpeedMultiplier' effect/state."} | 1 |
| [`MoveTowardsDamageSource`](./Enums.md#enum-movetowardsdamagesource) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'MoveTowardsDamageSource' effect/state."} | 1 |
| [`MovementReaction`](./Items_and_Equipment.md#context-movementreaction) | Block | {'type': 'Block', 'df': "Applies or references the 'MovementReaction' effect/state."} | 1 |
| `MultiplyCoinsOnBattleStart` | Number | {'type': '`Number`', 'df': "Applies or references the 'MultiplyCoinsOnBattleStart' effect/state."} | 1 |
| `MultiplyReceivedHealing` | Number | {'type': '`Number`', 'df': "Applies or references the 'MultiplyReceivedHealing' effect/state."} | 1 |
| [`ObjectDetector`](./Items_and_Equipment.md#context-objectdetector) | Block | {'type': '`Block`', 'df': "Applies or references the 'ObjectDetector' effect/state. | 1 |
| [`PassiveAfterXKills`](./Items_and_Equipment.md#context-passiveafterxkills) | Block | {'type': '`Block`', 'df': "Applies or references the 'PassiveAfterXKills' effect/state. | 1 |
| [`PassiveWhenAffectedByElement`](./Items_and_Equipment.md#context-passivewhenaffectedbyelement) | Block | {'type': '`Block`', 'df': 'State Trigger: Grants passives when this condition is met. | 1 |
| [`PassiveWhileHasDurability`](./Items_and_Equipment.md#context-passivewhilehasdurability) | Block | {'type': '`Block`', 'df': "Applies or references the 'PassiveWhileHasDurability' effect/state. | 1 |
| [`PassiveWhileInMonkMeleeStance`](./Items_and_Equipment.md#context-passivewhileinmonkmeleestance) | Block | {'type': '`Block`', 'df': "Applies or references the 'PassiveWhileInMonkMeleeStance' effect/state. | 1 |
| [`PassiveWhileShielded`](./Items_and_Equipment.md#context-passivewhileshielded) | Block | {'type': '`Block`', 'df': "Applies or references the 'PassiveWhileShielded' effect/state. | 1 |
| `PhysicalAttacksMiss` | Number | {'type': '`Number`', 'df': "Applies or references the 'PhysicalAttacksMiss' effect/state."} | 1 |
| [`PoopWhenHit`](./Items_and_Equipment.md#context-poopwhenhit) | Block | {'type': '`Block`', 'df': "Applies or references the 'PoopWhenHit' effect/state. | 1 |
| [`PreventSpecificInjury`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'PreventSpecificInjury' effect/state."} | 1 |
| `ReclaimItemOnBreak` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReclaimItemOnBreak' effect/state."} | 1 |
| `ReduceManaCost` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReduceManaCost' effect/state."} | 1 |
| `ReduceSpellCostsPerDisorder` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReduceSpellCostsPerDisorder' effect/state."} | 1 |
| `ReduceSpellCostsPerParasite` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReduceSpellCostsPerParasite' effect/state."} | 1 |
| `RemoveLineOfSightRestrictions` | Number | {'type': '`Number`', 'df': "Applies or references the 'RemoveLineOfSightRestrictions' effect/state."} | 1 |
| [`ReplaceBlankTilesOnBattleStart`](./Enums.md#enum-replaceblanktilesonbattlestart) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ReplaceBlankTilesOnBattleStart' effect/state."} | 1 |
| `RerollItemsOnBattleEnd` | Number | {'type': '`Number`', 'df': "Applies or references the 'RerollItemsOnBattleEnd' effect/state."} | 1 |
| [`ScaldingOrbMoonBossOneShot`](./Items_and_Equipment.md#context-scaldingorbmoonbossoneshot) | Block | {'type': '`Block`', 'df': "Applies or references the 'ScaldingOrbMoonBossOneShot' effect/state. | 1 |
| [`ScaledStatusAlliesOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusalliesonspendmana) | Block | {'type': '`Block`', 'df': "Applies or references the 'ScaledStatusAlliesOnSpendMana' effect/state. | 1 |
| [`ScaledStatusOnHolyShieldBlock`](./Items_and_Equipment.md#context-scaledstatusonholyshieldblock) | Block | {'type': '`Block`', 'df': "Applies or references the 'ScaledStatusOnHolyShieldBlock' effect/state. | 1 |
| [`ScaledStatusOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusonspendmana) | Block | {'type': '`Block`', 'df': "Applies or references the 'ScaledStatusOnSpendMana' effect/state. | 1 |
| [`SetBrittleImmune`](./Strings.md#string-setbrittleimmune) | String | {'type': '`String`', 'df': "Applies or references the 'SetBrittleImmune' effect/state."} | 1 |
| [`SetFaction`](./Enums.md#enum-setfaction) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'SetFaction' effect/state."} | 1 |
| [`SetFragileImmune`](./Strings.md#string-setfragileimmune) | String | {'type': '`String`', 'df': "Applies or references the 'SetFragileImmune' effect/state."} | 1 |
| `SetSpellCosts` | Number | {'type': '`Number`', 'df': "Applies or references the 'SetSpellCosts' effect/state."} | 1 |
| `SharkySmellsBlood` | Number | {'type': '`Number`', 'df': "Applies or references the 'SharkySmellsBlood' effect/state."} | 1 |
| `SpawnCatCloneOnCorpsePopped` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpawnCatCloneOnCorpsePopped' effect/state."} | 1 |
| [`SpawnOnDeath`](./Items_and_Equipment.md#context-spawnondeath) | Block | {'type': '`Block`', 'df': "Applies or references the 'SpawnOnDeath' effect/state. | 1 |
| [`SpawnOnDowned`](./Enums.md#enum-spawnondowned) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'SpawnOnDowned' effect/state."} | 1 |
| [`SpawnRandomPickupsOnTaggedUnitKilled`](./Items_and_Equipment.md#context-spawnrandompickupsontaggedunitkilled) | Block | {'type': '`Block`', 'df': "Applies or references the 'SpawnRandomPickupsOnTaggedUnitKilled' effect/state. | 1 |
| [`StatDependentPassive`](./Items_and_Equipment.md#context-statdependentpassive) | Block | {'type': '`Block`', 'df': 'Applies or references the \'StatDependentPassive\' effect/state. | 1 |
| [`StatusAdjacentOnTheirTurnEnd`](./Items_and_Equipment.md#context-statusadjacentontheirturnend) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusAdjacentOnTheirTurnEnd' effect/state. | 1 |
| [`StatusAfterXTurns`](./Items_and_Equipment.md#context-statusafterxturns) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusAfterXTurns' effect/state. | 1 |
| [`StatusAlliesEachTurn`](./Items_and_Equipment.md#context-statusallieseachturn) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusAlliesEachTurn' effect/state. | 1 |
| [`StatusAlliesOnDeath`](./Items_and_Equipment.md#context-statusalliesondeath) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusAlliesOnDeath' effect/state. | 1 |
| [`StatusEachTurnEndForEachTurn`](./Items_and_Equipment.md#context-statuseachturnendforeachturn) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusEachTurnEndForEachTurn' effect/state. | 1 |
| [`StatusIfUnusedMovePoints`](./Items_and_Equipment.md#context-statusifunusedmovepoints) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusIfUnusedMovePoints' effect/state. | 1 |
| [`StatusOnCollectPickup`](./Items_and_Equipment.md#context-statusoncollectpickup) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnDodge`](./Items_and_Equipment.md#context-statusondodge) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnEatFood`](./Items_and_Equipment.md#context-statusoneatfood) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnEnemyDeath`](./Items_and_Equipment.md#context-statusonenemydeath) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnFallAsleep`](./Items_and_Equipment.md#context-statusonfallasleep) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnFullMana`](./Items_and_Equipment.md#context-statusonfullmana) | Block | {'type': '`Block`', 'df': 'Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnHealed`](./Items_and_Equipment.md#context-statusonhealed) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnPickupCoins`](./Items_and_Equipment.md#context-statusonpickupcoins) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnUseBasicAttack`](./Items_and_Equipment.md#context-statusonusebasicattack) | Block | {'type': '`Block`', 'df': "Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusWhenAllySpendsMana`](./Items_and_Equipment.md#context-statuswhenallyspendsmana) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusWhenAllySpendsMana' effect/state. | 1 |
| `StevenBolts` | Number | {'type': '`Number`', 'df': "Applies or references the 'StevenBolts' effect/state."} | 1 |
| `StripKnockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'StripKnockback' effect/state."} | 1 |
| `TauntAlways` | Number | {'type': '`Number`', 'df': "Applies or references the 'TauntAlways' effect/state."} | 1 |
| [`TintItem`](./Items_and_Equipment.md#context-tintitem) | Block | {'type': '`Block`', 'df': "Applies or references the 'TintItem' effect/state. | 1 |
| [`TunnelVision`](./Items_and_Equipment.md#context-tunnelvision) | Block | {'type': '`Block`', 'df': "Applies or references the 'TunnelVision' effect/state. | 1 |
| `Undead` | Number | {'type': '`Number`', 'df': "Applies or references the 'Undead' effect/state."} | 1 |
| `WeaponDamageMultiplierBonus` | Number | {'type': '`Number`', 'df': "Applies or references the 'WeaponDamageMultiplierBonus' effect/state."} | 1 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 65

> **Referenced by:** [`AddPassivesToMinions`](./Items_and_Equipment.md#context-addpassivestominions), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Knockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'Knockback' effect/state."} | 10 |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bleed' effect/state."} | 9 |
| `Poison` | Number | {'type': '`Number`', 'df': "Applies or references the 'Poison' effect/state."} | 6 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies or references the 'Burn' effect/state."} | 5 |
| [`Fear`](./Arrays.md#array-fear) | Array | {'type': '`Array`', 'df': "Applies or references the 'Fear' effect/state."} | 4 |
| `Slow` | Number | {'type': '`Number`', 'df': "Applies or references the 'Slow' effect/state."} | 4 |
| [`Tangled`](./Arrays.md#array-tangled) | Array | {'type': '`Array`', 'df': 'Applies a tangled/ensnared status effect, often modifying visual sprites.'} | 4 |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum | {'type': '`Enum/String`', 'df': 'Transforms the terrain tile under the target.'} | 3 |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 3 |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bruise' effect/state."} | 2 |
| `Confusion` | Number | {'type': '`Number`', 'df': "Applies or references the 'Confusion' effect/state."} | 2 |
| `DamageOrHealConditionally` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageOrHealConditionally' effect/state."} | 2 |
| `Rot` | Number | {'type': '`Number`', 'df': "Applies or references the 'Rot' effect/state."} | 2 |
| `SpiderInfested` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpiderInfested' effect/state."} | 2 |
| `Weakness` | Number | {'type': '`Number`', 'df': "Applies or references the 'Weakness' effect/state."} | 2 |
| [`ApplyToSource`](./Items_and_Equipment.md#context-applytosource) | Block | {'type': '`Block`', 'df': "Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| `Blind` | Number | {'type': '`Number`', 'df': "Applies or references the 'Blind' effect/state."} | 1 |
| [`ForceUseAbilityOnTarget`](./Items_and_Equipment.md#context-forceuseabilityontarget) | Block | {'type': '`Block`', 'df': "Applies or references the 'ForceUseAbilityOnTarget' effect/state. | 1 |
| [`Freeze`](./Arrays.md#array-freeze) | Array | {'type': '`Array`', 'df': "Applies or references the 'Freeze' effect/state."} | 1 |
| `KnockOutCoin` | Number | {'type': '`Number`', 'df': 'Forces the target to drop coins.'} | 1 |
| [`KnockUpAndAway`](./Items_and_Equipment.md#context-knockupandaway) | Block | {'type': '`Block`', 'df': 'Displaces the target vertically and horizontally away from the source. | 1 |
| `Leech` | Number | {'type': '`Number`', 'df': "Applies or references the 'Leech' effect/state."} | 1 |
| `Leeches` | Number | {'type': '`Number`', 'df': "Applies or references the 'Leeches' effect/state."} | 1 |
| `MagicWeakness` | Number | {'type': '`Number`', 'df': "Applies or references the 'MagicWeakness' effect/state."} | 1 |
| `ManaLeeches` | Number | {'type': '`Number`', 'df': "Applies or references the 'ManaLeeches' effect/state."} | 1 |
| `Marked` | Number | {'type': '`Number`', 'df': "Applies or references the 'Marked' effect/state."} | 1 |
| `OverrideChainKnockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'OverrideChainKnockback' effect/state."} | 1 |
| `PullSourceToTarget` | Number | {'type': '`Number`', 'df': "Applies or references the 'PullSourceToTarget' effect/state."} | 1 |
| `SoulLink` | Number | {'type': '`Number`', 'df': "Applies or references the 'SoulLink' effect/state."} | 1 |
| [`Stun`](./Arrays.md#array-stun) | Array | {'type': '`Array`', 'df': "Applies or references the 'Stun' effect/state."} | 1 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

> **Referenced by:** [`DoDamage`](./Items_and_Equipment.md#context-dodamage), [`MeleeRevengeDamage`](./Items_and_Equipment.md#context-meleerevengedamage), [`RevengeDamage`](./Items_and_Equipment.md#context-revengedamage), [`damage_instance`](./Items_and_Equipment.md#context-damage_instance)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bruise' effect/state."} | 7 |
| [`BounceObject`](./Enums.md#enum-bounceobject) | Enum | {'type': '`Enum/String`', 'df': 'Spawns a physics object that visually bounces off the target.'} | 4 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies or references the 'Burn' effect/state."} | 4 |
| [`Fear`](./Arrays.md#array-fear) | Array | {'type': '`Array`', 'df': "Applies or references the 'Fear' effect/state."} | 4 |
| [`Grappled`](./Arrays.md#array-grappled) | Array | {'type': '`Array`', 'df': "Applies or references the 'Grappled' effect/state."} | 4 |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 3 |
| `Immobile` | Number | {'type': '`Number`', 'df': "Applies or references the 'Immobile' effect/state."} | 3 |
| `Slow` | Number | {'type': '`Number`', 'df': "Applies or references the 'Slow' effect/state."} | 3 |
| `Poison` | Number | {'type': '`Number`', 'df': "Applies or references the 'Poison' effect/state."} | 2 |
| [`Stun`](./Arrays.md#array-stun) | Array | {'type': '`Array`', 'df': "Applies or references the 'Stun' effect/state."} | 2 |
| `Blind` | Number | {'type': '`Number`', 'df': "Applies or references the 'Blind' effect/state."} | 1 |
| `Cleave` | Number | {'type': '`Number`', 'df': 'Causes the attack to hit adjacent enemies alongside the primary target.'} | 1 |
| `Confusion` | Number | {'type': '`Number`', 'df': "Applies or references the 'Confusion' effect/state."} | 1 |
| [`Freeze`](./Arrays.md#array-freeze) | Array | {'type': '`Array`', 'df': "Applies or references the 'Freeze' effect/state."} | 1 |
| [`VisualFX`](./Enums.md#enum-visualfx) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'VisualFX' effect/state."} | 1 |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'VisualFXTile' effect/state."} | 1 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 32

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Items_and_Equipment.md#context-effects) | Block | {'type': '`Block`', 'df': "Non-damaging status applications and logic triggers executed on impact. | 23 |
| `knockback` | Number | {'type': '`Number`', 'df': ''} | 9 |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 4 |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 25

> **Referenced by:** [`ApplyPassives`](./Items_and_Equipment.md#context-applypassives), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | {'type': '`Boolean`', 'df': 'If true, triggers the effect even if the character died during the battle.'} | 11 |
| `RandomPermanentStat` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomPermanentStat' effect/state."} | 6 |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 5 |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum | {'type': '`Enum/String`', 'df': 'Generates an item drop from the specified loot pool.'} | 3 |
| `RandomMutation` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomMutation' effect/state."} | 3 |
| [`GainCoins`](./Arrays.md#array-gaincoins) | Array | {'type': '`Number`', 'df': "Applies or references the 'GainCoins' effect/state."} | 2 |
| `RepairTrinket` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairTrinket' effect/state."} | 2 |
| [`SetItemAux`](./Items_and_Equipment.md#context-setitemaux) | Block | {'type': '`Block`', 'df': "Applies or references the 'SetItemAux' effect/state."} | 2 |
| [`Conditional_Corpse`](./Items_and_Equipment.md#context-conditional_corpse) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 1 |
| [`Conditional_Shielded`](./Items_and_Equipment.md#context-conditional_shielded) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target currently has a Shield status. | 1 |
| `PermanentConstitution` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentConstitution' effect/state."} | 1 |
| `PermanentIntelligence` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentIntelligence' effect/state."} | 1 |
| `RepairAll` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairAll' effect/state."} | 1 |
| `RepairWeapon` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairWeapon' effect/state."} | 1 |
| [`TransformWeapon`](./Items_and_Equipment.md#context-transformweapon) | Block | {'type': '`Block`', 'df': 'Transforms the equipped weapon into another specific weapon state. | 1 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ForceUseAbility' effect/state."} | 6 |
| `PartialCleanse` | Number | {'type': '`Number`', 'df': "Applies or references the 'PartialCleanse' effect/state."} | 4 |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 2 |
| [`ImmediateUseAbility`](./Items_and_Equipment.md#context-immediateuseability) | Block | {'type': '`Enum/String`', 'df': "Applies or references the 'ImmediateUseAbility' effect/state."} | 2 |
| `SpawnCoinAnywhere` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpawnCoinAnywhere' effect/state."} | 2 |
| `AddWeaponAux` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddWeaponAux' effect/state."} | 1 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies or references the 'Burn' effect/state."} | 1 |
| [`Conditional_ManaThreshold`](./Items_and_Equipment.md#context-conditional_manathreshold) | Block | {'type': '`Block`', 'df': "Conditional constraint. Nested properties only trigger if this is true. | 1 |
| `ConstitutionUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'ConstitutionUp' effect/state."} | 1 |
| `PreEmptiveCounterNextAttacks` | Number | {'type': '`Number`', 'df': "Applies or references the 'PreEmptiveCounterNextAttacks' effect/state."} | 1 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 1 |
| [`Stealth`](./Arrays.md#array-stealth) | Array | {'type': '`Array`', 'df': "Applies or references the 'Stealth' effect/state."} | 1 |

</details>

---

### Context: `StatusOnBreak`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`GainCoinsRange`](./Items_and_Equipment.md#context-gaincoinsrange) | Block | {'type': '`Block`', 'df': 'Grants the player a randomized amount of coins within a min/max range. | 5 |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bruise' effect/state."} | 3 |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ChangeTilesUnder' effect/state."} | 3 |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum | {'type': '`Enum/String`', 'df': 'Generates an item drop from the specified loot pool.'} | 3 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 3 |
| `HealthRegenUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthRegenUp' effect/state."} | 3 |
| `PermanentConstitution` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentConstitution' effect/state."} | 3 |
| [`ApplyToRandomPartyMemberIfPossible`](./Items_and_Equipment.md#context-applytorandompartymemberifpossible) | Block | {'type': '`Block`', 'df': "Redirects the nested effects to apply to a random living member of the player's party. | 1 |
| `ConstitutionUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'ConstitutionUp' effect/state."} | 1 |
| `DexterityUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DexterityUp' effect/state."} | 1 |
| [`FindItem`](./Enums.md#enum-finditem) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'FindItem' effect/state."} | 1 |
| [`GainDisorder`](./Enums.md#enum-gaindisorder) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'GainDisorder' effect/state."} | 1 |
| `IntelligenceUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'IntelligenceUp' effect/state."} | 1 |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum | {'type': '`Enum/String`', 'df': 'Spawns a specific character or entity upon impact.'} | 1 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'StrengthUp' effect/state."} | 1 |

</details>

---

### Context: `SpawnOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 17 |
| [`number`](./Arrays.md#array-number) | Array | {'type': '`Number`', 'df': ''} | 11 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 17

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend), [`StatusOnKill`](./Items_and_Equipment.md#context-statusonkill), [`StatusOnTakeHealthOrShieldDamage`](./Items_and_Equipment.md#context-statusontakehealthorshielddamage), [`effects`](./Items_and_Equipment.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `odds` | Number | {'type': '`Number`', 'df': "The probability (0.0 to 1.0) of triggering the 'good roll' success state."} | 17 |
| `Freeze` | Number | {'type': '`Number`', 'df': "Applies or references the 'Freeze' effect/state."} | 6 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ForceUseAbility' effect/state."} | 3 |
| [`ForceUseAbility_NonStack`](./Enums.md#enum-forceuseability_nonstack) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ForceUseAbility_NonStack' effect/state."} | 3 |
| `RandomMutation` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomMutation' effect/state."} | 3 |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum | {'type': '`Enum/String`', 'df': 'Generates an item drop from the specified loot pool.'} | 2 |
| `DestroyTrinket` | Number | {'type': '`Number`', 'df': "Applies or references the 'DestroyTrinket' effect/state."} | 1 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 3 |
| `BrittleCharismaUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'BrittleCharismaUp' effect/state."} | 1 |
| `BrittleConstitutionUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'BrittleConstitutionUp' effect/state."} | 1 |
| `BrittleDexterityUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'BrittleDexterityUp' effect/state."} | 1 |
| `BrittleIntelligenceUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'BrittleIntelligenceUp' effect/state."} | 1 |
| `BrittleLuckUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'BrittleLuckUp' effect/state."} | 1 |
| `BrittleSpeedUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'BrittleSpeedUp' effect/state."} | 1 |
| `BrittleStrengthUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'BrittleStrengthUp' effect/state."} | 1 |
| `CharismaUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'CharismaUp' effect/state."} | 1 |
| `ConstitutionUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'ConstitutionUp' effect/state."} | 1 |
| `DexterityUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DexterityUp' effect/state."} | 1 |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'EquipPermanentItem' effect/state."} | 1 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 1 |
| `HealthRegenUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthRegenUp' effect/state."} | 1 |
| `IntelligenceUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'IntelligenceUp' effect/state."} | 1 |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'LuckUp' effect/state."} | 1 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpeedUp' effect/state."} | 1 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'StrengthUp' effect/state."} | 1 |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charge' effect/state."} | 5 |
| `Thorns` | Number | {'type': '`Number`', 'df': "Applies or references the 'Thorns' effect/state."} | 2 |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bleed' effect/state."} | 1 |
| [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 1 |
| [`Conditional_HealthThreshold`](./Items_and_Equipment.md#context-conditional_healththreshold) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 1 |
| `DamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageUp' effect/state."} | 1 |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array | {'type': '`Array`', 'df': "Applies or references the 'DivineShield' effect/state."} | 1 |
| `DodgeChance_Status` | Number | {'type': '`Number`', 'df': "Applies or references the 'DodgeChance_Status' effect/state."} | 1 |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'RemoveStatus' effect/state."} | 1 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'StrengthUp' effect/state."} | 1 |
| [`Temporary`](./Items_and_Equipment.md#context-temporary) | Block | {'type': '`Block`', 'df': 'A wrapper block for applying status effects that automatically expire. | 1 |

</details>

---

### Context: `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Craft`](./Items_and_Equipment.md#context-craft) | Block | {'type': '`Block`', 'df': 'Synthesizes or spawns a new item from a specific pool. | 3 |
| `SafeDie` | Number | {'type': '`Number`', 'df': "Applies or references the 'SafeDie' effect/state."} | 2 |
| [`Brace`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'Brace' effect/state."} | 1 |
| [`DestroyEquipmentAndAttachParasite`](./Items_and_Equipment.md#context-destroyequipmentandattachparasite) | Block | {'type': '`Block`', 'df': 'Removes an equipped item and replaces it with a parasite from a specified pool. | 1 |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum | {'type': '`Enum/String`', 'df': 'Generates an item drop from the specified loot pool.'} | 1 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ForceUseAbility' effect/state."} | 1 |
| [`ObjectOnHitCharacter`](./Items_and_Equipment.md#context-objectonhitcharacter) | Block | {'type': '`Block`', 'df': 'Spawns a specific character or entity upon impact. | 1 |
| `RandomMagicMissile` | Number | {'type': '`Number`', 'df': 'Fires a randomized number of magic missiles.'} | 1 |
| [`ReviveNextRound`](./Items_and_Equipment.md#context-revivenextround) | Block | {'type': '`Block`', 'df': "Queues the character to be resurrected at the start of the next combat round. | 1 |
| `SetHealth` | Number | {'type': '`Number`', 'df': "Applies or references the 'SetHealth' effect/state."} | 1 |
| `StealthUntilBasicAttack` | Number | {'type': '`Number`', 'df': "Applies or references the 'StealthUntilBasicAttack' effect/state."} | 1 |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 11 |
| `good` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| `spawn_on_death_hit` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| [`chance`](./Enums.md#enum-chance) | Enum | {'type': '`Enum/String`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |
| `number` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array | {'type': '`Enum/String`', 'df': ''} | 10 |
| `chance` | Mixed | {'type': '`Enum/String`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 9 |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_BadRoll`](./Items_and_Equipment.md#context-conditional_badroll) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic based on a randomized bad outcome probability. | 2 |
| `BlessingOfPeace` | Number | {'type': '`Number`', 'df': "Applies or references the 'BlessingOfPeace' effect/state."} | 1 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies or references the 'Burn' effect/state."} | 1 |
| `DestroyTrinket` | Number | {'type': '`Number`', 'df': "Applies or references the 'DestroyTrinket' effect/state."} | 1 |
| `DoubleCastSpellThisTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'DoubleCastSpellThisTurn' effect/state."} | 1 |
| `DrinkWater` | Number | {'type': '`Number`', 'df': "Applies or references the 'DrinkWater' effect/state."} | 1 |
| [`ManaGainRange`](./Items_and_Equipment.md#context-managainrange) | Block | {'type': '`Block`', 'df': "Applies or references the 'ManaGainRange' effect/state. | 1 |
| `Revive` | Number | {'type': '`Number`', 'df': "Applies or references the 'Revive' effect/state."} | 1 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpeedUp' effect/state."} | 1 |
| [`Temporary`](./Items_and_Equipment.md#context-temporary) | Block | {'type': '`Block`', 'df': 'A wrapper block for applying status effects that automatically expire.'} | 1 |
| [`UseAbility`](./Enums.md#enum-useability) | Enum | {'type': '`Enum/String`', 'df': 'Forces the character or target to instantly use a specified ability.'} | 1 |
| `Wet` | Number | {'type': '`Number`', 'df': "Applies or references the 'Wet' effect/state."} | 1 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Items_and_Equipment.md#context-effects) | Block | {'type': '`Block`', 'df': "Non-damaging status applications and logic triggers executed on impact. | 9 |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 3 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 2 |

</details>

---

### Context: `AddSelfStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | {'type': '`Number`', 'df': 'Fires a randomized number of magic missiles.'} | 4 |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bleed' effect/state."} | 1 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ForceUseAbility' effect/state."} | 1 |
| [`Quivered`](./Arrays.md#array-quivered) | Array | {'type': '`Array`', 'df': "Applies or references the 'Quivered' effect/state."} | 1 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 1 |

</details>

---

### Context: `DurabilityTransform`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eq`](./Arrays.md#array-eq) | Array | {'type': '`Array`', 'df': ''} | 11 |
| [`ge`](./Arrays.md#array-ge) | Array | {'type': '`Array`', 'df': ''} | 4 |

</details>

---

### Context: `PassiveIfStrAuxEquals`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | {'type': '`Block`', 'df': 'Passives granted by equipping this. | 7 |
| [`value`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': ''} | 7 |

</details>

---

### Context: `StatusOnKillEnemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageUp' effect/state."} | 3 |
| `Brace` | Number | {'type': '`Number`', 'df': "Applies or references the 'Brace' effect/state."} | 1 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ForceUseAbility' effect/state."} | 1 |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'LuckUp' effect/state."} | 1 |
| `ManaGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'ManaGain' effect/state."} | 1 |

</details>

---

### Context: `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 3 |
| `must_do_damage` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| [`Conditional_HasTag`](./Items_and_Equipment.md#context-conditional_hastag) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 1 |
| [`KnockbackIfCrit`](./Items_and_Equipment.md#context-knockbackifcrit) | Block | {'type': '`Block`', 'df': "Applies or references the 'KnockbackIfCrit' effect/state. | 1 |
| `Rot` | Number | {'type': '`Number`', 'df': "Applies or references the 'Rot' effect/state."} | 1 |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus), [`Else`](./Items_and_Equipment.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 2 |
| `Charge` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charge' effect/state."} | 2 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 1 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpeedUp' effect/state."} | 1 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'StrengthUp' effect/state."} | 1 |

</details>

---

### Context: `GainCoinsRange`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak), [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number | {'type': '`Number`', 'df': 'Maximum coins granted.'} | 6 |
| `min` | Number | {'type': '`Number`', 'df': 'Minimum coins granted.'} | 6 |

</details>

---

### Context: `ItemAuxTransform`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`le`](./Arrays.md#array-le) | Array | {'type': '`Array`', 'df': ''} | 6 |
| [`ge`](./Arrays.md#array-ge) | Array | {'type': '`Array`', 'df': ''} | 2 |
| [`lt`](./Arrays.md#array-lt) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `PassiveWhenOnTile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | {'type': '`Block`', 'df': 'Passives granted by equipping this. | 6 |
| [`tile`](./Arrays.md#array-tile) | Array | {'type': '`Array`', 'df': ''} | 6 |

</details>

---

### Context: `StatusAlliesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpeedUp' effect/state."} | 2 |
| `Brace` | Number | {'type': '`Number`', 'df': "Applies or references the 'Brace' effect/state."} | 1 |
| `ConstitutionUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'ConstitutionUp' effect/state."} | 1 |
| `DamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageUp' effect/state."} | 1 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'StrengthUp' effect/state."} | 1 |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_RandomChance`](./Items_and_Equipment.md#context-conditional_randomchance) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic based on a flat percentage random roll. | 1 |
| [`CreateGlobalModifiers`](./Items_and_Equipment.md#context-createglobalmodifiers) | Block | {'type': '`Block`', 'df': "Generates global map or encounter rules/modifiers. | 1 |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum | {'type': '`Enum/String`', 'df': 'Generates an item drop from the specified loot pool.'} | 1 |
| [`GainCoinsRange`](./Items_and_Equipment.md#context-gaincoinsrange) | Block | {'type': '`Block`', 'df': 'Grants the player a randomized amount of coins within a min/max range. | 1 |
| `RandomMagicMissile` | Number | {'type': '`Number`', 'df': 'Fires a randomized number of magic missiles.'} | 1 |
| [`RandomStatusFromPool`](./Items_and_Equipment.md#context-randomstatusfrompool) | Block | {'type': '`Block`', 'df': "Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charge' effect/state."} | 3 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpeedUp' effect/state."} | 3 |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'DivineShield' effect/state."} | 1 |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ImmediateUseAbility' effect/state."} | 1 |

</details>

---

### Context: `Temporary`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`Conditional_BadRoll`](./Items_and_Equipment.md#context-conditional_badroll), [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin), [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 5 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The status effect to apply.'} | 5 |
| `expires_on_end_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| `turns` | Number | {'type': '`Number`', 'df': 'Duration in turns.'} | 4 |
| `expires_on_begin_turn` | Boolean | {'type': '`Boolean`', 'df': 'If true, ticks down at the start of the turn rather than the end.'} | 1 |

</details>

---

### Context: `TransformItemOnElementInfluence`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 5 |
| `full_repair` | Boolean | {'type': '`Boolean`', 'df': ''} | 5 |
| [`item`](./Enums.md#enum-item) | Enum | {'type': '`Enum/String`', 'df': 'Item ID to reference.'} | 5 |

</details>

---

### Context: `AddDamageToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 4 |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 4 |

</details>

---

### Context: `AddPassivesToMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 2 |
| `AddMaxHealth` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddMaxHealth' effect/state."} | 1 |
| [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack) | Block | {'type': '`Block`', 'df': "Injects a status effect payload that applies whenever the character performs a basic attack. | 1 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 1 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 1 |

</details>

---

### Context: `ChanceToRevive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage), [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The specific status effect ID to remove.'} | 4 |
| [`ApplyToSource`](./Items_and_Equipment.md#context-applytosource) | Block | {'type': '`Block`', 'df': "Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 2 |
| `FlatLeechIfDamaged` | Number | {'type': '`Number`', 'df': "Applies or references the 'FlatLeechIfDamaged' effect/state."} | 1 |
| [`ImmediateUseAbility_Instant`](./Enums.md#enum-immediateuseability_instant) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ImmediateUseAbility_Instant' effect/state."} | 1 |
| [`RemoveStatusStacks`](./Items_and_Equipment.md#context-removestatusstacks) | Block | {'type': '`Block`', 'df': 'Removes a specific number of stacks of a status effect. | 1 |

</details>

---

### Context: `Craft`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`StatusIfUnusedActPoints`](./Items_and_Equipment.md#context-statusifunusedactpoints), [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |
| [`slot`](./Enums.md#enum-slot) | Enum | {'type': '`Enum/String`', 'df': 'Equipment slot (weapon, hat, face, chest, etc.).'} | 4 |
| `works_with_tech` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |

</details>

---

### Context: `DelayedAutoRevive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number | {'type': '`Number`', 'df': ''} | 4 |
| `rounds` | Number | {'type': '`Number`', 'df': ''} | 4 |

</details>

---

### Context: `PassiveAtHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | {'type': '`Block`', 'df': 'Passives granted by equipping this. | 4 |
| `threshold` | Number | {'type': '`Number`', 'df': ''} | 4 |

</details>

---

### Context: `SpawnObjectOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Number | {'type': '`Number`', 'df': 'Quantity.'} | 1 |
| `except_tiny` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `StatusOnTakeHealthOrShieldDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array | {'type': '`Array`', 'df': "Applies or references the 'DivineShield' effect/state."} | 2 |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 1 |
| `Metronome` | Number | {'type': '`Number`', 'df': 'Executes a random musical or metronome ability.'} | 1 |

</details>

---

### Context: `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Number | {'type': '`Number`', 'df': 'Quantity.'} | 4 |
| `Charmed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charmed' effect/state."} | 1 |
| `Confusion` | Number | {'type': '`Number`', 'df': "Applies or references the 'Confusion' effect/state."} | 1 |
| `Fear` | Number | {'type': '`Number`', 'df': "Applies or references the 'Fear' effect/state."} | 1 |
| `Freeze` | Number | {'type': '`Number`', 'df': "Applies or references the 'Freeze' effect/state."} | 1 |

</details>

---

### Context: `global_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GlobalEnemyAutoRevive` | Number | {'type': '`Number`', 'df': "Applies or references the 'GlobalEnemyAutoRevive' effect/state."} | 2 |
| `NoCorpses` | Number | {'type': '`Number`', 'df': "Applies or references the 'NoCorpses' effect/state."} | 1 |
| `RealTimePressure` | Number | {'type': '`Number`', 'df': "Applies or references the 'RealTimePressure' effect/state."} | 1 |

</details>

---

### Context: `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | {'type': '`Number`', 'df': "Applies or references the 'Quivered' effect/state."} | 3 |
| `ally_chance` | Number | {'type': '`Number`', 'df': ''} | 3 |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 3 |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reduction` | Number | {'type': '`Number`', 'df': ''} | 3 |
| [`class`](./Enums.md#enum-class) | Enum | {'type': '`Enum/String`', 'df': 'Character class identifier.'} | 2 |

</details>

---

### Context: `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ExtraStatusWhenDealingDamage`](./Items_and_Equipment.md#context-extrastatuswhendealingdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_IsSelf`](./Abilities_and_Spells.md#context-conditional_isself) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic if the target is the caster themselves.'} | 3 |
| [`Else`](./Items_and_Equipment.md#context-else) | Block | {'type': '`Block`', 'df': 'Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 3 |

</details>

---

### Context: `CounterAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'ID of the ability to trigger or reference.'} | 3 |
| `melee_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `ranged_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`Conditional_PartyMember`](./Items_and_Equipment.md#context-conditional_partymember)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ApplyToSource`](./Items_and_Equipment.md#context-applytosource) | Block | {'type': '`Block`', 'df': "Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 |

</details>

---

### Context: `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_PartyMember`](./Items_and_Equipment.md#context-conditional_partymember) | Block | {'type': '`Block`', 'df': 'Conditional constraint. Nested properties only trigger if this is true. | 3 |

</details>

---

### Context: `PassiveWhenDead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AutocastEachRound`](./Items_and_Equipment.md#context-autocasteachround) | Block | {'type': '`Block`', 'df': 'Forces the character to automatically cast a specific ability at the start of each combat round. | 1 |
| [`StatusEachRoundEnd`](./Items_and_Equipment.md#context-statuseachroundend) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusEachRoundEnd' effect/state. | 1 |
| [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusEachTurnBegin' effect/state. | 1 |

</details>

---

### Context: `SetItemAux`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`Conditional_Shielded`](./Items_and_Equipment.md#context-conditional_shielded), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum | {'type': '`Enum/String`', 'df': 'Equipment slot (weapon, hat, face, chest, etc.).'} | 3 |
| [`value`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': ''} | 3 |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array | {'type': '`Number`', 'df': ''} | 3 |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array | {'type': '`Array`', 'df': ''} | 3 |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |

</details>

---

### Context: `StackingFlowerTrail`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 3 |

</details>

---

### Context: `StatusAllCharactersOnSpawn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Boss`](./Items_and_Equipment.md#context-conditional_boss) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is a Boss. | 2 |
| `Poison` | Number | {'type': '`Number`', 'df': "Applies or references the 'Poison' effect/state."} | 1 |

</details>

---

### Context: `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 3 |
| `Charge` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charge' effect/state."} | 1 |
| `IntelligenceUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'IntelligenceUp' effect/state."} | 1 |
| [`ObjectOnHitCharacter`](./Items_and_Equipment.md#context-objectonhitcharacter) | Block | {'type': '`Block`', 'df': 'Spawns a specific character or entity upon impact. | 1 |

</details>

---

### Context: `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 1 |
| `RepairTrinket` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairTrinket' effect/state."} | 1 |
| `RepairWeapon` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairWeapon' effect/state."} | 1 |

</details>

---

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'Classification type.'} | 3 |
| `Charge` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charge' effect/state."} | 1 |
| `DamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageUp' effect/state."} | 1 |
| `HealthRegenUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthRegenUp' effect/state."} | 1 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 1 |
| `SpellDamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpellDamageUp' effect/state."} | 1 |
| `Thorns` | Number | {'type': '`Number`', 'df': "Applies or references the 'Thorns' effect/state."} | 1 |

</details>

---

### Context: `AddStatusToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 2 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies or references the 'Burn' effect/state."} | 1 |
| [`Stun`](./Arrays.md#array-stun) | Array | {'type': '`Array`', 'df': "Applies or references the 'Stun' effect/state."} | 1 |

</details>

---

### Context: `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bruise' effect/state."} | 1 |
| [`Stun`](./Arrays.md#array-stun) | Array | {'type': '`Array`', 'df': "Applies or references the 'Stun' effect/state."} | 1 |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Enemy`](./Items_and_Equipment.md#context-conditional_enemy) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is hostile to the caster. | 1 |
| `Leech` | Number | {'type': '`Number`', 'df': "Applies or references the 'Leech' effect/state."} | 1 |

</details>

---

### Context: `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bounty` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bounty' effect/state."} | 1 |
| `Marked` | Number | {'type': '`Number`', 'df': "Applies or references the 'Marked' effect/state."} | 1 |
| `count` | Number | {'type': '`Number`', 'df': 'Quantity.'} | 1 |

</details>

---

### Context: `ArmorBreakOnHit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance_to_break` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `durability_loss` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `BoostWeaponDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `crit_chance` | Mixed | {'type': '`Number`', 'df': ''} | 2 |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 2 |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'ID of the ability to trigger or reference.'} | 2 |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 2 |

</details>

---

### Context: `ChanceToBlockAndCounter`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |

</details>

---

### Context: `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ScaledStatusAlliesOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusalliesonspendmana), [`StatusAlliesEachTurn`](./Items_and_Equipment.md#context-statusallieseachturn)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Ally`](./Items_and_Equipment.md#context-conditional_ally) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is friendly to the caster. | 1 |
| [`Conditional_PlayerCat`](./Items_and_Equipment.md#context-conditional_playercat) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 1 |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Temporary`](./Items_and_Equipment.md#context-temporary) | Block | {'type': '`Block`', 'df': 'A wrapper block for applying status effects that automatically expire. | 3 |
| [`odds`](./Enums.md#enum-odds) | Enum | {'type': '`Enum/String`', 'df': "The probability (0.0 to 1.0) of triggering the 'bad roll' failure state."} | 2 |

</details>

---

### Context: `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusAllCharactersOnSpawn`](./Items_and_Equipment.md#context-statusallcharactersonspawn)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 2 |

</details>

---

### Context: `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_HealthThreshold`](./Items_and_Equipment.md#context-conditional_healththreshold), [`StatusOnFullMana`](./Items_and_Equipment.md#context-statusonfullmana)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReduceManaCost` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReduceManaCost' effect/state."} | 1 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 1 |
| [`ShowText`](./Strings.md#string-showtext) | String | {'type': '`String`', 'df': "Applies or references the 'ShowText' effect/state."} | 1 |
| `SpellDamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpellDamageUp' effect/state."} | 1 |
| [`key`](./Enums.md#enum-key) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `CreateGlobalModifiers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `NextPlayerCatTakesExtraTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'NextPlayerCatTakesExtraTurn' effect/state."} | 1 |
| `NoCorpses` | Number | {'type': '`Number`', 'df': "Applies or references the 'NoCorpses' effect/state."} | 1 |

</details>

---

### Context: `DoDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusEachRoundEnd`](./Items_and_Equipment.md#context-statuseachroundend), [`StatusOnBreakItem`](./Items_and_Equipment.md#context-statusonbreakitem)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The flat damage amount.'} | 2 |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`effects`](./Items_and_Equipment.md#context-effects) | Block | {'type': '`Block`', 'df': "Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification of the damage (e.g., spell, melee).'} | 2 |

</details>

---

### Context: `ElementalManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array | {'type': '`Array`', 'df': 'Specific element type required or applied.'} | 2 |
| `reduction` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `ImmediateUseAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'ID of the ability to trigger or reference.'} | 1 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `ModifyAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bonus_passives`](./Items_and_Equipment.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cost`](./Items_and_Equipment.md#context-cost) | Block | {'type': '`Block`', 'df': 'Currency value in shops/merchants. | 2 |
| [`meta`](./Items_and_Equipment.md#context-meta) | Block | {'type': '`Block`', 'df': ' | 2 |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`PassiveWhileHasDurability`](./Items_and_Equipment.md#context-passivewhilehasdurability), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'ID of the ability to trigger or reference.'} | 2 |
| `create_temp_ability` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `enemies_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `on_self_move_too` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `ObjectOnHitCharacter`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusEveryXSpellCasts`](./Items_and_Equipment.md#context-statuseveryxspellcasts), [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': 'The entity ID of the character to spawn (e.g., CharmedFlea).'} | 2 |
| `stacks` | Mixed | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 2 |

</details>

---

### Context: `PassiveAtStatThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | {'type': '`Block`', 'df': 'Passives granted by equipping this. | 2 |
| [`threshold`](./Items_and_Equipment.md#context-threshold) | Block | {'type': '`Block`', 'df': ' | 2 |

</details>

---

### Context: `PassiveIfWeaponIsUsable`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | {'type': '`Number`', 'df': "Applies or references the 'Brace' effect/state."} | 2 |

</details>

---

### Context: `RefreshEquipmentAbilityOnElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 2 |
| [`text`](./Strings.md#string-text) | String | {'type': '`String`', 'df': ''} | 2 |

</details>

---

### Context: `SpawnItemLinkedFamiliar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `StatusAfterCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempMeleeRangeUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempMeleeRangeUp' effect/state."} | 1 |
| `TempRangeUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempRangeUp' effect/state."} | 1 |
| [`UseAbility`](./Enums.md#enum-useability) | Enum | {'type': '`Enum/String`', 'df': 'Forces the character or target to instantly use a specified ability.'} | 1 |

</details>

---

### Context: `StatusAfterXStacks`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusonspendmana), [`StatusOnCollectPickup`](./Items_and_Equipment.md#context-statusoncollectpickup)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| `threshold` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `ExtraBasicMoves_Status` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExtraBasicMoves_Status' effect/state."} | 1 |
| `RefreshActPoints` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshActPoints' effect/state."} | 1 |
| `expires_on_end_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `StatusIfUnusedActPoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`BackflipWhenTargeted`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': 'Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack.'} | 1 |
| [`Craft`](./Items_and_Equipment.md#context-craft) | Block | {'type': '`Block`', 'df': 'Synthesizes or spawns a new item from a specific pool. | 1 |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'DivineShield' effect/state."} | 1 |
| `RepairTrinket` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairTrinket' effect/state."} | 1 |

</details>

---

### Context: `StatusOnBackstab`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 1 |
| `SerratedClaws` | Number | {'type': '`Number`', 'df': "Applies or references the 'SerratedClaws' effect/state."} | 1 |

</details>

---

### Context: `StatusOnBreakItem`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DoDamage`](./Items_and_Equipment.md#context-dodamage) | Block | {'type': '`Block`', 'df': 'Explicitly triggers a secondary damage instance independent of the main attack. | 1 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 1 |

</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charge' effect/state."} | 1 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 1 |

</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'LuckUp' effect/state."} | 1 |
| [`Shield`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'Shield' effect/state."} | 1 |

</details>

---

### Context: `bonus_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`str_aux_is_copy_ability`](./Items_and_Equipment.md#context-str_aux_is_copy_ability)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ModifyAbility`](./Items_and_Equipment.md#context-modifyability) | Block | {'type': '`Block`', 'df': "Applies or references the 'ModifyAbility' effect/state. | 2 |

</details>

---

### Context: `cost`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ModifyAbility`](./Items_and_Equipment.md#context-modifyability)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `charge` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `mana` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'DivineShield' effect/state."} | 1 |
| `Immobile` | Number | {'type': '`Number`', 'df': "Applies or references the 'Immobile' effect/state."} | 1 |

</details>

---

### Context: `meta`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ModifyAbility`](./Items_and_Equipment.md#context-modifyability)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `is_basic_attack` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `is_weapon` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `passive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Metal` | Number | {'type': '`Number`', 'df': "Applies or references the 'Metal' effect/state."} | 2 |

</details>

---

### Context: `str_aux_is_copy_ability`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bonus_passives`](./Items_and_Equipment.md#context-bonus_passives) | Block | {'type': '`Block`', 'df': "Passives granted to the character while this ability is equipped. | 2 |

</details>

---

### Context: `threshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `int` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `AIControlNextTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `AbilityHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'ID of the ability to trigger or reference.'} | 1 |
| `aux` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `immediate` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`threshold`](./Math_Equations.md) | Equation | {'type': '`String`', 'df': ''} | 1 |

</details>

---

### Context: `AbilityOnRoundEndOnce`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'ID of the ability to trigger or reference.'} | 1 |
| `even_of_stunned` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `AddAdvantageToEvent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `add` | Number | {'type': '`Number`', 'df': ''} | 1 |
| [`options`](./Arrays.md#array-options) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'Classification type.'} | 1 |

</details>

---

### Context: `AddPassivesToCharmed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 1 |

</details>

---

### Context: `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array | {'type': '`Array`', 'df': "Applies or references the 'RepairWeapon' effect/state."} | 1 |

</details>

---

### Context: `AddStatusToBackstabs`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bleed' effect/state."} | 1 |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Leech` | Number | {'type': '`Number`', 'df': "Applies or references the 'Leech' effect/state."} | 1 |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CastAgainWithStatus`](./Items_and_Equipment.md#context-castagainwithstatus) | Block | {'type': '`Block`', 'df': "Applies or references the 'CastAgainWithStatus' effect/state. | 1 |

</details>

---

### Context: `AlluringDoodieEater`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |
| [`damage_instance`](./Items_and_Equipment.md#context-damage_instance) | Block | {'type': '`Block`', 'df': ' | 1 |

</details>

---

### Context: `AllyDodgeChanceAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |
| `range` | Number | {'type': '`Number`', 'df': 'Distance or area of effect in tiles.'} | 1 |

</details>

---

### Context: `ApplyPassives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_RandomChance`](./Items_and_Equipment.md#context-conditional_randomchance)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend) | Block | {'type': '`Block`', 'df': "Applies the nested status effects when the encounter finishes. | 1 |

</details>

---

### Context: `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`GainDisorderFromPool`](./Enums.md#enum-gaindisorderfrompool) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'GainDisorderFromPool' effect/state."} | 2 |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to autocast.'} | 1 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': 'If true, bypasses stun and hard-CC restrictions to cast anyway.'} | 1 |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific dodge ability to trigger (e.g., DestroyerDodge).'} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `BouncyProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `max_range` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `BuffImmunity`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exclude`](./Enums.md#enum-exclude) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `CastAgainWithStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddTemporaryEffectsToBasicAttack`](./Items_and_Equipment.md#context-addtemporaryeffectstobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'OverrideDamage' effect/state."} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `CatPartsSizeScale`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `head` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `ChanceToForceEvent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |
| [`event`](./Enums.md#enum-event) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'ManaGain' effect/state."} | 1 |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomMutation` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomMutation' effect/state."} | 1 |

</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToSpells`](./Items_and_Equipment.md#context-addstatustospells)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Leeches` | Number | {'type': '`Number`', 'df': "Applies or references the 'Leeches' effect/state."} | 1 |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BonusKnockbackDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'BonusKnockbackDamage' effect/state."} | 1 |
| `OverrideChainKnockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'OverrideChainKnockback' effect/state."} | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The specific string tag to check for.'} | 1 |

</details>

---

### Context: `Conditional_HealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](./Items_and_Equipment.md#context-conditional_onceperbattle) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic only once per encounter/battle. | 1 |
| `threshold_flat` | Number | {'type': '`Number`', 'df': 'A flat numerical health value threshold.'} | 1 |

</details>

---

### Context: `Conditional_ManaThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RepairTrinket` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairTrinket' effect/state."} | 1 |
| `threshold_flat` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charge' effect/state."} | 1 |

</details>

---

### Context: `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ApplyPassives`](./Items_and_Equipment.md#context-applypassives) | Block | {'type': '`Block`', 'df': 'Grants the nested passive abilities dynamically. | 1 |
| `odds` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |

</details>

---

### Context: `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`SetItemAux`](./Items_and_Equipment.md#context-setitemaux) | Block | {'type': '`Block`', 'df': "Applies or references the 'SetItemAux' effect/state. | 1 |

</details>

---

### Context: `ConvertDamageToScaledStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DelayedPain` | Number | {'type': '`Number`', 'df': "Applies or references the 'DelayedPain' effect/state."} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `CritsApplyStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fear` | Number | {'type': '`Number`', 'df': "Applies or references the 'Fear' effect/state."} | 1 |

</details>

---

### Context: `DestroyEquipmentAndAttachParasite`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | {'type': '`Enum/String`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |
| [`pool`](./Arrays.md#array-pool) | Array | {'type': '`Array`', 'df': 'The item pool to draw the parasite from.'} | 1 |

</details>

---

### Context: `Eternal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health_percent` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `FlyDamageIncrease`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `ForceUseAbilityOnTarget`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'ID of the ability to trigger or reference.'} | 1 |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |

</details>

---

### Context: `GlobalMeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | {'type': '`Number`', 'df': 'The distance in tiles to knock the target away.'} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `KnockbackIfCrit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `override_chain_knockback` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `ManaGainRange`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `min` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `ObjectDetector`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `PassiveAfterXKills`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | {'type': '`Block`', 'df': 'Passives granted by equipping this. | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 1 |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | {'type': '`Block`', 'df': 'Passives granted by equipping this. | 1 |

</details>

---

### Context: `PassiveWhileHasDurability`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`MovementReaction`](./Items_and_Equipment.md#context-movementreaction) | Block | {'type': '`Block`', 'df': "Applies or references the 'MovementReaction' effect/state. | 1 |

</details>

---

### Context: `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | {'type': '`Number`', 'df': "Applies or references the 'Brace' effect/state."} | 1 |

</details>

---

### Context: `PassiveWhileShielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthRegenUp' effect/state."} | 1 |

</details>

---

### Context: `PoopWhenHit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PermanentCharisma` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentCharisma' effect/state."} | 1 |
| `PermanentConstitution` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentConstitution' effect/state."} | 1 |
| `PermanentDexterity` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentDexterity' effect/state."} | 1 |
| `PermanentIntelligence` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentIntelligence' effect/state."} | 1 |
| `PermanentLuck` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentLuck' effect/state."} | 1 |
| `PermanentSpeed` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentSpeed' effect/state."} | 1 |
| `PermanentStrength` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentStrength' effect/state."} | 1 |

</details>

---

### Context: `RemoveStatusStacks`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks to remove.'} | 1 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The specific status effect ID to remove.'} | 1 |

</details>

---

### Context: `ReviveNextRound`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 1 |
| `revive_health` | Number | {'type': '`Number`', 'df': 'The flat amount of health to revive with.'} | 1 |

</details>

---

### Context: `ScaldingOrbMoonBossOneShot`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'CompleteItemQuest' effect/state."} | 1 |
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'RemoveItem' effect/state."} | 1 |

</details>

---

### Context: `ScaledStatusAlliesOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent) | Block | {'type': '`Block`', 'df': 'Conditional constraint. Nested properties only trigger if this is true. | 1 |

</details>

---

### Context: `ScaledStatusOnHolyShieldBlock`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | {'type': '`Number`', 'df': 'Fires a randomized number of magic missiles.'} | 1 |

</details>

---

### Context: `ScaledStatusOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`StatusAfterXStacks`](./Items_and_Equipment.md#context-statusafterxstacks) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusAfterXStacks' effect/state. | 1 |

</details>

---

### Context: `SpawnOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`obj`](./Enums.md#enum-obj) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `SpawnRandomPickupsOnTaggedUnitKilled`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array | {'type': '`Array`', 'df': 'Quantity.'} | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'Specific entity tag required.'} | 1 |

</details>

---

### Context: `StatDependentPassive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddDamageToBasicAttack`](./Math_Equations.md) | Equation | {'type': '`String`', 'df': "Applies or references the 'AddDamageToBasicAttack' effect/state."} | 1 |

</details>

---

### Context: `StatusAdjacentOnTheirTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceMoveAway` | Number | {'type': '`Number`', 'df': "Applies or references the 'ForceMoveAway' effect/state."} | 1 |

</details>

---

### Context: `StatusAfterXTurns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ForceUseAbility' effect/state."} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `StatusAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent) | Block | {'type': '`Block`', 'df': 'Conditional constraint. Nested properties only trigger if this is true. | 1 |

</details>

---

### Context: `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'DivineShield' effect/state."} | 1 |

</details>

---

### Context: `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DoDamage`](./Items_and_Equipment.md#context-dodamage) | Block | {'type': '`Block`', 'df': 'Explicitly triggers a secondary damage instance independent of the main attack. | 1 |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ForceUseAbility' effect/state."} | 1 |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charge' effect/state."} | 1 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 1 |

</details>

---

### Context: `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`StatusAfterXStacks`](./Items_and_Equipment.md#context-statusafterxstacks) | Block | {'type': '`Block`', 'df': "Applies or references the 'StatusAfterXStacks' effect/state. | 1 |

</details>

---

### Context: `StatusOnDodge`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Number | {'type': '`Number`', 'df': "Applies or references the 'DodgeChance_Status' effect/state."} | 1 |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RepairTrinket` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairTrinket' effect/state."} | 1 |
| [`TempPassiveUntilSettled`](./Items_and_Equipment.md#context-temppassiveuntilsettled) | Block | {'type': '`Block`', 'df': "Applies or references the 'TempPassiveUntilSettled' effect/state. | 1 |

</details>

---

### Context: `StatusOnEnemyDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charge' effect/state."} | 1 |

</details>

---

### Context: `StatusOnFallAsleep`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 1 |
| `FillMana` | Number | {'type': '`Number`', 'df': "Applies or references the 'FillMana' effect/state."} | 1 |
| `HealRandomInjury` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealRandomInjury' effect/state."} | 1 |

</details>

---

### Context: `StatusOnFullMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](./Items_and_Equipment.md#context-conditional_onceperbattle) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic only once per encounter/battle. | 1 |

</details>

---

### Context: `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 1 |

</details>

---

### Context: `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GainCoins` | Number | {'type': '`Number`', 'df': "Applies or references the 'GainCoins' effect/state."} | 1 |

</details>

---

### Context: `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageUp' effect/state."} | 1 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 1 |

</details>

---

### Context: `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charge' effect/state."} | 1 |

</details>

---

### Context: `TempPassiveUntilSettled`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnEatFood`](./Items_and_Equipment.md#context-statusoneatfood)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LimitHeal` | Number | {'type': '`Number`', 'df': "Applies or references the 'LimitHeal' effect/state."} | 1 |

</details>

---

### Context: `TintItem`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`add`](./Arrays.md#array-add) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`ignore_if_str_aux_equals`](./Enums.md#enum-ignore_if_str_aux_equals) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`mul`](./Arrays.md#array-mul) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `TransformWeapon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | {'type': '`Enum/String`', 'df': 'The original weapon ID.'} | 1 |
| [`to`](./Enums.md#enum-to) | Enum | {'type': '`Enum/String`', 'df': 'The transformed weapon ID.'} | 1 |

</details>

---

### Context: `TunnelVision`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `crit_chance` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `damage_instance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AlluringDoodieEater`](./Items_and_Equipment.md#context-alluringdoodieeater)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| [`effects`](./Items_and_Equipment.md#context-effects) | Block | {'type': '`Block`', 'df': "Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'Classification type.'} | 1 |

</details>

---

