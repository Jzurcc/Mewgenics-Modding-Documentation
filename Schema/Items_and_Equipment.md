# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Items & Equipment

> **Associated Files:** `data/items/, data/item_setbonuses.gon`


### Context: `ROOT` (1217 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the item's desc. | 1217 |
| [`name`](./Strings.md#string-name) | String | Localization key for the item's name. | 1206 |
| `frame` | Number |  | 1106 |
| [`kind`](./Enums.md#enum-kind) | Enum |  | 1106 |
| [`rarity`](./Enums.md#enum-rarity) | Enum |  | 967 |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | Passives granted by equipping this. | 823 |
| [`set`](./Enums.md#enum-set) | Enum |  | 765 |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 365 |
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
| [`variant_of`](./Enums.md#enum-variant_of) | Enum |  | 29 |
| `str` | Number |  | 28 |
| `dex` | Number |  | 22 |
| [`quest_reward_item`](./Enums.md#enum-quest_reward_item) | Enum |  | 22 |
| `indestructible` | Boolean |  | 20 |
| `divine_shield` | Number |  | 17 |
| `legacy_quest` | Boolean |  | 17 |
| [`hint_destination`](./Enums.md#enum-hint_destination) | Enum |  | 16 |
| [`str_aux_initialize`](./Enums.md#enum-str_aux_initialize) | Enum |  | 15 |
| `dont_destroy_on_0` | Boolean |  | 13 |
| [`global_tags`](./Arrays.md#array-global_tags) | Array |  | 12 |
| `max_durability` | Number |  | 11 |
| [`on_store`](./Enums.md#enum-on_store) | Enum |  | 8 |
| [`name_mod`](./Strings.md#string-name_mod) | String |  | 7 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 6 |
| [`hint_prerequisite_flag`](./Enums.md#enum-hint_prerequisite_flag) | Enum |  | 5 |
| `failable` | Boolean |  | 4 |
| [`global_passives`](./Items_and_Equipment.md#context-global_passives) | Block |  | 4 |
| `randomize_piece_frames` | Boolean |  | 4 |
| `str_aux_is_copy_passive` | Boolean |  | 4 |
| `fragile` | Boolean |  | 3 |
| [`icon_hint`](./Enums.md#enum-icon_hint) | String |  | 3 |
| `max_health` | Number |  | 3 |
| `reset_aux_on_store` | Number |  | 3 |
| `sticky` | Boolean |  | 3 |
| `weightless` | Boolean |  | 3 |
| [`keyword_tooltips`](./Items_and_Equipment.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear when hovering over the ability. | 2 |
| [`passive`](./Items_and_Equipment.md#context-passive) | Block |  | 2 |
| `prevent_level_up` | Boolean |  | 2 |
| [`quest_item_alias`](./Enums.md#enum-quest_item_alias) | Enum |  | 2 |
| `speed` | Number |  | 2 |
| [`str_aux_is_copy_ability`](./Items_and_Equipment.md#context-str_aux_is_copy_ability) | Block |  | 2 |
| `str_aux_is_copy_item_passive` | Boolean |  | 2 |
| [`Set`](./Enums.md#enum-set) | Enum | Applies or references the 'Set' effect/state. | 1 |
| `aux_is_catid` | Boolean |  | 1 |
| `cant_equip_to_colorless` | Boolean |  | 1 |
| `degrade_after_adventure` | Boolean |  | 1 |
| [`equip_sound`](./Enums.md#enum-equip_sound) | Enum |  | 1 |
| `force_sticky` | Boolean |  | 1 |
| [`reset_str_aux_on_store`](./Enums.md#enum-reset_str_aux_on_store) | Enum |  | 1 |
| [`str_aux`](./Enums.md#enum-str_aux) | Enum |  | 1 |
| `str_aux_is_copy_item_active` | Boolean |  | 1 |
| `str_aux_is_copy_item_icon` | Boolean |  | 1 |

</details>

---

### Context: `passives` (848 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAfterXKills`](./Items_and_Equipment.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Items_and_Equipment.md#context-passiveathealththreshold), [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold), [`PassiveIfStrAuxEquals`](./Items_and_Equipment.md#context-passiveifstrauxequals), [`PassiveWhenAffectedByElement`](./Items_and_Equipment.md#context-passivewhenaffectedbyelement), [`PassiveWhenOnTile`](./Items_and_Equipment.md#context-passivewhenontile), [`ROOT`](./Items_and_Equipment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |
| [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 68 |
| [`MeleeRevengeDamage`](./Items_and_Equipment.md#context-meleerevengedamage) | Block | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. | 34 |
| [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend) | Block | Applies the nested status effects when the encounter finishes. | 30 |
| [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend) | Block | Applies or references the 'StatusEachTurnEnd' effect/state. | 27 |
| [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak) | Block | Event Trigger: Applies statuses when this action occurs. | 22 |
| [`StatusOnKill`](./Items_and_Equipment.md#context-statusonkill) | Block | Event Trigger: Applies statuses when this action occurs. | 18 |
| [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage) | Block | Event Trigger: Applies statuses when this action occurs. | 17 |
| [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart) | Block | Event Trigger: Applies statuses when this action occurs. | 13 |
| [`RevengeDamage`](./Items_and_Equipment.md#context-revengedamage) | Block | Reaction trigger: Deals damage to the attacker when hit. | 9 |
| [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin) | Block | Applies or references the 'StatusEachTurnBegin' effect/state. | 9 |
| [`AddSelfStatusToBasicAttack`](./Items_and_Equipment.md#context-addselfstatustobasicattack) | Block | Applies or references the 'AddSelfStatusToBasicAttack' effect/state. | 8 |
| [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage) | Block | Modifier: Injects a status effect into a specific action. | 8 |
| [`StatusAlliesOnBattleStart`](./Items_and_Equipment.md#context-statusalliesonbattlestart) | Block | Applies or references the 'StatusAlliesOnBattleStart' effect/state. | 8 |
| [`StatusOnKillEnemy`](./Items_and_Equipment.md#context-statusonkillenemy) | Block | Event Trigger: Applies statuses when this action occurs. | 8 |
| [`AddPassivesToMinions`](./Items_and_Equipment.md#context-addpassivestominions) | Block | Applies or references the 'AddPassivesToMinions' effect/state. | 7 |
| [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie) | Block | Event Trigger: Applies statuses when this action occurs. | 6 |
| [`PassiveAtHealthThreshold`](./Items_and_Equipment.md#context-passiveathealththreshold) | Block | Applies or references the 'PassiveAtHealthThreshold' effect/state. | 5 |
| [`StatusOnEndMove`](./Items_and_Equipment.md#context-statusonendmove) | Block | Event Trigger: Applies statuses when this action occurs. | 5 |
| [`StatusRandomEnemiesOnBattleStart`](./Items_and_Equipment.md#context-statusrandomenemiesonbattlestart) | Block | Applies or references the 'StatusRandomEnemiesOnBattleStart' effect/state. | 4 |
| [`CatchProjectiles`](./Items_and_Equipment.md#context-catchprojectiles) | Block | Applies or references the 'CatchProjectiles' effect/state. | 3 |
| [`ExtraStatusWhenDealingDamage`](./Items_and_Equipment.md#context-extrastatuswhendealingdamage) | Block | Applies or references the 'ExtraStatusWhenDealingDamage' effect/state. | 3 |
| [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold) | Block | Applies or references the 'PassiveAtStatThreshold' effect/state. | 3 |
| [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead) | Block | State Trigger: Grants passives when this condition is met. | 3 |
| [`StatusAllCharactersOnSpawn`](./Items_and_Equipment.md#context-statusallcharactersonspawn) | Block | Applies or references the 'StatusAllCharactersOnSpawn' effect/state. | 3 |
| [`StatusEveryXSpellCasts`](./Items_and_Equipment.md#context-statuseveryxspellcasts) | Block | Applies or references the 'StatusEveryXSpellCasts' effect/state. | 3 |
| [`StatusIfUnusedMovePoints`](./Items_and_Equipment.md#context-statusifunusedmovepoints) | Block | Applies or references the 'StatusIfUnusedMovePoints' effect/state. | 3 |
| [`StatusOnPopCorpse`](./Items_and_Equipment.md#context-statusonpopcorpse) | Block | Event Trigger: Applies statuses when this action occurs. | 3 |
| [`AddStatusToElementDamage`](./Items_and_Equipment.md#context-addstatustoelementdamage) | Block | Modifier: Injects a status effect into a specific action. | 2 |
| [`AddStatusToKnockbackDamage`](./Items_and_Equipment.md#context-addstatustoknockbackdamage) | Block | Modifier: Injects a status effect into a specific action. | 2 |
| [`AddStatusToSpells`](./Items_and_Equipment.md#context-addstatustospells) | Block | Modifier: Injects a status effect into a specific action. | 2 |
| [`ApplyStatusesToRandomEnemiesEachTurn`](./Items_and_Equipment.md#context-applystatusestorandomenemieseachturn) | Block | Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state. | 2 |
| [`PassiveAfterXKills`](./Items_and_Equipment.md#context-passiveafterxkills) | Block | Applies or references the 'PassiveAfterXKills' effect/state. | 2 |
| [`StatusAfterCastSpell`](./Items_and_Equipment.md#context-statusaftercastspell) | Block | Applies or references the 'StatusAfterCastSpell' effect/state. | 2 |
| [`StatusOnAllyCatDeath`](./Items_and_Equipment.md#context-statusonallycatdeath) | Block | Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnBreakItem`](./Items_and_Equipment.md#context-statusonbreakitem) | Block | Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnCastSpell`](./Items_and_Equipment.md#context-statusoncastspell) | Block | Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnGainCoins`](./Items_and_Equipment.md#context-statusongaincoins) | Block | Event Trigger: Applies statuses when this action occurs. | 2 |
| [`AddPassivesToCharmed`](./Items_and_Equipment.md#context-addpassivestocharmed) | Block | Applies or references the 'AddPassivesToCharmed' effect/state. | 1 |
| [`AddSelfStatusToWeapons`](./Items_and_Equipment.md#context-addselfstatustoweapons) | Block | Applies or references the 'AddSelfStatusToWeapons' effect/state. | 1 |
| [`AddStatusToWeapons`](./Items_and_Equipment.md#context-addstatustoweapons) | Block | Modifier: Injects a status effect into a specific action. | 1 |
| [`CreateGlobalModifiers`](./Items_and_Equipment.md#context-createglobalmodifiers) | Block | Generates global map or encounter rules/modifiers. | 1 |
| [`CritsApplyStatus`](./Items_and_Equipment.md#context-critsapplystatus) | Block | Applies or references the 'CritsApplyStatus' effect/state. | 1 |
| [`PassiveWhenAffectedByElement`](./Items_and_Equipment.md#context-passivewhenaffectedbyelement) | Block | State Trigger: Grants passives when this condition is met. | 1 |
| [`PassiveWhileInMonkMeleeStance`](./Items_and_Equipment.md#context-passivewhileinmonkmeleestance) | Block | Applies or references the 'PassiveWhileInMonkMeleeStance' effect/state. | 1 |
| [`StatusAfterXTurns`](./Items_and_Equipment.md#context-statusafterxturns) | Block | Applies or references the 'StatusAfterXTurns' effect/state. | 1 |
| [`StatusAlliesEachTurn`](./Items_and_Equipment.md#context-statusallieseachturn) | Block | Applies or references the 'StatusAlliesEachTurn' effect/state. | 1 |
| [`StatusAlliesOnDeath`](./Items_and_Equipment.md#context-statusalliesondeath) | Block | Applies or references the 'StatusAlliesOnDeath' effect/state. | 1 |
| [`StatusEachTurnEndForEachTurn`](./Items_and_Equipment.md#context-statuseachturnendforeachturn) | Block | Applies or references the 'StatusEachTurnEndForEachTurn' effect/state. | 1 |
| [`StatusOnCollectPickup`](./Items_and_Equipment.md#context-statusoncollectpickup) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnEatFood`](./Items_and_Equipment.md#context-statusoneatfood) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnEatPill`](./Items_and_Equipment.md#context-statusoneatpill) | Block |  | 1 |
| [`StatusOnHealed`](./Items_and_Equipment.md#context-statusonhealed) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnPickupCoins`](./Items_and_Equipment.md#context-statusonpickupcoins) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnUseBasicAttack`](./Items_and_Equipment.md#context-statusonusebasicattack) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusWhenAllySpendsMana`](./Items_and_Equipment.md#context-statuswhenallyspendsmana) | Block | Applies or references the 'StatusWhenAllySpendsMana' effect/state. | 1 |

</details>

---

### Context: `AddStatusToBasicAttack` (69 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Items_and_Equipment.md#context-addpassivestominions), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| [`ApplyToSource`](./Items_and_Equipment.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |

</details>

---

### Context: `effects` (37 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](./Items_and_Equipment.md#context-dodamage), [`MeleeRevengeDamage`](./Items_and_Equipment.md#context-meleerevengedamage), [`RevengeDamage`](./Items_and_Equipment.md#context-revengedamage), [`damage_instance`](./Items_and_Equipment.md#context-damage_instance)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
</details>

---

### Context: `MeleeRevengeDamage` (34 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| [`effects`](./Items_and_Equipment.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 25 |
| `knockback` | Number |  | 9 |
| `damage` | Number | The base damage properties of an attack. | 5 |

</details>

---

### Context: `StatusOnBattleEnd` (31 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./Items_and_Equipment.md#context-applypassives), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 12 |

</details>

---

### Context: `StatusEachTurnEnd` (27 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| [`Conditional_HasCleansableDebuffs`](./Items_and_Equipment.md#context-conditional_hascleansabledebuffs) | Block |  | 1 |

</details>

---

### Context: `SpawnOnBattleStart` (22 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 22 |
| [`number`](./Arrays.md#array-number) | Number |  | 16 |

</details>

---

### Context: `StatusOnBreak` (22 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| [`ApplyToRandomPartyMemberIfPossible`](./Items_and_Equipment.md#context-applytorandompartymemberifpossible) | Block | Redirects the nested effects to apply to a random living member of the player's party. | 1 |

</details>

---

### Context: `Conditional_GoodRoll` (19 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend), [`StatusOnKill`](./Items_and_Equipment.md#context-statusonkill), [`StatusOnTakeHealthOrShieldDamage`](./Items_and_Equipment.md#context-statusontakehealthorshielddamage), [`effects`](./Items_and_Equipment.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 19 |

</details>

---

### Context: `StatusOnKill` (18 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnTookDamage` (17 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `SpawnThingOnDamage` (13 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 13 |
| `good` | Boolean |  | 4 |
| `shield_only` | Boolean |  | 2 |
| `spawn_on_death_hit` | Boolean |  | 2 |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| `number` | Number |  | 1 |

</details>

---

### Context: `StatusOnBattleStart` (13 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `SpawnEachTurn` (12 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Enum |  | 12 |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0 or percentage) of this occurring. | 11 |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum |  | 5 |

</details>

---

### Context: `StatusEachTurnBegin` (10 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `RevengeDamage` (9 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| [`effects`](./Items_and_Equipment.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 9 |
| `damage` | Number | The base damage properties of an attack. | 3 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |

</details>

---

### Context: `AddSelfStatusToBasicAttack` (8 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `AddStatusToAllDamage` (8 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| `must_do_damage` | Boolean |  | 3 |

</details>

---

### Context: `StatusAlliesOnBattleStart` (8 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnKillEnemy` (8 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `AddPassivesToMinions` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |
| [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 1 |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum |  | 1 |

</details>

---

### Context: `DurabilityTransform` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eq`](./Arrays.md#array-eq) | Array |  | 11 |
| [`ge`](./Arrays.md#array-ge) | Array |  | 4 |

</details>

---

### Context: `GainCoinsRange` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend), [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak), [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number | Maximum coins granted. | 7 |
| `min` | Number | Minimum coins granted. | 7 |

</details>

---

### Context: `PassiveIfStrAuxEquals` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | Passives granted by equipping this. | 7 |
| [`value`](./Math_Equations.md) | Enum |  | 7 |

</details>

---

### Context: `PassiveWhenOnTile` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | Passives granted by equipping this. | 7 |
| [`tile`](./Arrays.md#array-tile) | Array |  | 7 |

</details>

---

### Context: `ApplyToSource` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus), [`Else`](./Items_and_Equipment.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
</details>

---

### Context: `ItemAuxTransform` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`le`](./Arrays.md#array-le) | Array |  | 6 |
| [`ge`](./Arrays.md#array-ge) | Array |  | 2 |
| [`lt`](./Arrays.md#array-lt) | Array |  | 1 |

</details>

---

### Context: `StatusOnDie` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| [`CreateGlobalModifiers`](./Items_and_Equipment.md#context-createglobalmodifiers) | Block | Generates global map or encounter rules/modifiers. | 1 |
| [`RandomStatusFromPool`](./Items_and_Equipment.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `DelayedAutoRevive` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 5 |
| `rounds` | Number |  | 5 |

</details>

---

### Context: `PassiveAtHealthThreshold` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 5 |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | Passives granted by equipping this. | 5 |
| `threshold` | Number |  | 5 |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 5 |
| [`object`](./Enums.md#enum-object) | Enum |  | 5 |

</details>

---

### Context: `StatusOnEndMove` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `Temporary` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_BadRoll`](./Items_and_Equipment.md#context-conditional_badroll), [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin), [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 5 |
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 5 |
| `expires_on_end_turn` | Boolean |  | 4 |
| `turns` | Number | Duration in turns. | 4 |
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 1 |

</details>

---

### Context: `TransformItemOnElementInfluence` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 5 |
| `full_repair` | Boolean |  | 5 |
| [`item`](./Enums.md#enum-item) | Enum | Item ID to reference. | 5 |

</details>

---

### Context: `AddDamageToElementDamage` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 4 |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 4 |

</details>

---

### Context: `ClassManaCostReduction` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reduction` | Number |  | 4 |
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 3 |

</details>

---

### Context: `Conditional_HasStatus` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage), [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 4 |
| [`ApplyToSource`](./Items_and_Equipment.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 2 |

</details>

---

### Context: `Craft` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusIfUnusedActPoints`](./Items_and_Equipment.md#context-statusifunusedactpoints), [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 4 |
| [`slot`](./Enums.md#enum-slot) | Enum | Equipment slot (weapon, hat, face, chest, etc.). | 4 |
| `works_with_tech` | Boolean |  | 3 |

</details>

---

### Context: `Else` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToFirstSpellEachTurn`](./Items_and_Equipment.md#context-addstatustofirstspelleachturn), [`Conditional_PartyMember`](./Items_and_Equipment.md#context-conditional_partymember)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| [`ApplyToSource`](./Items_and_Equipment.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 |

</details>

---

### Context: `StatusOnTakeHealthOrShieldDamage` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array | Applies or references the 'DivineShield' effect/state. | 2 |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll) | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 1 |
| `Metronome` | Number | Executes a random musical or metronome ability. | 1 |

</details>

---

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 4 |
| `AllStatsUp` | Number |  | 1 |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 1 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 1 |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 1 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 1 |
| `SpellDamageUp` | Number | Applies or references the 'SpellDamageUp' effect/state. | 1 |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. | 1 |

</details>

---

### Context: `StatusRandomEnemiesOnBattleStart` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| `count` | Number | Quantity. | 4 |

</details>

---

### Context: `global_passives` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GlobalEnemyAutoRevive` | Number | Applies or references the 'GlobalEnemyAutoRevive' effect/state. | 2 |
| `NoCorpses` | Number | Applies or references the 'NoCorpses' effect/state. | 1 |
| `RealTimePressure` | Number | Applies or references the 'RealTimePressure' effect/state. | 1 |

</details>

---

### Context: `CatchProjectiles` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| `ally_chance` | Number |  | 3 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 3 |

</details>

---

### Context: `Conditional_PartyMember` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ExtraStatusWhenDealingDamage`](./Items_and_Equipment.md#context-extrastatuswhendealingdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| [`Else`](./Items_and_Equipment.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 3 |

</details>

---

### Context: `CounterAttack` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 3 |
| `melee_only` | Boolean |  | 1 |
| `ranged_only` | Boolean |  | 1 |

</details>

---

### Context: `DeathRattle` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum |  | 3 |
| `pop_corpse` | Boolean |  | 3 |

</details>

---

### Context: `ExtraStatusWhenDealingDamage` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `PassiveAtStatThreshold` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 3 |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | Passives granted by equipping this. | 3 |
| [`threshold`](./Items_and_Equipment.md#context-threshold) | Block |  | 3 |

</details>

---

### Context: `PassiveWhenDead` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |
| [`StatusEachRoundEnd`](./Items_and_Equipment.md#context-statuseachroundend) | Block | Applies or references the 'StatusEachRoundEnd' effect/state. | 1 |
| [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin) | Block | Applies or references the 'StatusEachTurnBegin' effect/state. | 1 |

</details>

---

### Context: `SetItemAux` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Shielded`](./Items_and_Equipment.md#context-conditional_shielded), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum | Equipment slot (weapon, hat, face, chest, etc.). | 3 |
| [`value`](./Math_Equations.md) | Enum |  | 3 |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `number` | Number |  | 3 |
| [`object`](./Enums.md#enum-object) | Enum |  | 3 |

</details>

---

### Context: `StackingFlowerTrail` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum |  | 3 |
| `stacks` | Number | Number of stacks or intensity to apply. | 3 |

</details>

---

### Context: `StatusAllCharactersOnSpawn` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusEveryXSpellCasts` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| `stacks` | Number | Number of stacks or intensity to apply. | 3 |

</details>

---

### Context: `StatusIfUnusedMovePoints` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnPopCorpse` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `threshold` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 2 |
| `con` | Number |  | 1 |

</details>

---

### Context: `AddStatusToElementDamage` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 2 |

</details>

---

### Context: `AddStatusToKnockbackDamage` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `AddStatusToSpells` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `ApplyStatusesToRandomEnemiesEachTurn` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| `count` | Number | Quantity. | 1 |

</details>

---

### Context: `ArmorBreakOnHit` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance_to_break` | Number |  | 2 |
| `durability_loss` | Number |  | 2 |

</details>

---

### Context: `AutocastEachRound` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 2 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 2 |

</details>

---

### Context: `BoostWeaponDamage` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `crit_chance` | Number |  | 2 |
| `damage` | Number | The base damage properties of an attack. | 2 |

</details>

---

### Context: `ChanceToBackflip` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 2 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |

</details>

---

### Context: `ChanceToBlockAndCounter` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean |  | 1 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Context: `ChanceToRevive` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `Conditional_Adjacent` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusAlliesOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusalliesonspendmana), [`StatusAlliesEachTurn`](./Items_and_Equipment.md#context-statusallieseachturn)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
</details>

---

### Context: `Conditional_BadRoll` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| [`odds`](./Enums.md#enum-odds) | Enum | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 2 |

</details>

---

### Context: `Conditional_Boss` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusAllCharactersOnSpawn`](./Items_and_Equipment.md#context-statusallcharactersonspawn)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
</details>

---

### Context: `Conditional_HasTag` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. | 2 |

</details>

---

### Context: `Conditional_OncePerBattle` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HealthThreshold`](./Items_and_Equipment.md#context-conditional_healththreshold), [`StatusOnFullMana`](./Items_and_Equipment.md#context-statusonfullmana)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| [`key`](./Enums.md#enum-key) | Enum |  | 1 |

</details>

---

### Context: `CreateGlobalModifiers` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[global_modifier_id]`](./Engine_GlobalModifiers.md#all-confirmed-global-modifier-id-values) | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |  |
</details>

---

### Context: `DoDamage` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachRoundEnd`](./Items_and_Equipment.md#context-statuseachroundend), [`StatusOnBreakItem`](./Items_and_Equipment.md#context-statusonbreakitem)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The flat damage amount. | 2 |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum |  | 2 |
| [`effects`](./Items_and_Equipment.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification of the damage (e.g., spell, melee). | 2 |

</details>

---

### Context: `ElementalManaCostReduction` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array | Specific element type required or applied. | 2 |
| `reduction` | Number |  | 2 |

</details>

---

### Context: `ModifyAbility` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Items_and_Equipment.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cost`](./Items_and_Equipment.md#context-cost) | Block | Currency value in shops/merchants. | 2 |
| [`meta`](./Items_and_Equipment.md#context-meta) | Block |  | 2 |

</details>

---

### Context: `MovementReaction` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhileHasDurability`](./Items_and_Equipment.md#context-passivewhilehasdurability), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 2 |
| `create_temp_ability` | Boolean |  | 2 |
| `enemies_only` | Boolean |  | 2 |
| `on_self_move_too` | Boolean |  | 1 |

</details>

---

### Context: `ObjectOnHitCharacter` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEveryXSpellCasts`](./Items_and_Equipment.md#context-statuseveryxspellcasts), [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the character to spawn (e.g., CharmedFlea). | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `PassiveAfterXKills` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | Passives granted by equipping this. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `PassiveIfWeaponIsUsable` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | Applies or references the 'Brace' effect/state. | 2 |

</details>

---

### Context: `RefreshEquipmentAbilityOnElement` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 2 |
| [`text`](./Strings.md#string-text) | String |  | 2 |

</details>

---

### Context: `SpawnCatCopyWhenDowned` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum |  | 2 |

</details>

---

### Context: `SpawnItemLinkedFamiliar` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean |  | 2 |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |

</details>

---

### Context: `StatusAfterCastSpell` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusAfterXStacks` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusonspendmana), [`StatusOnCollectPickup`](./Items_and_Equipment.md#context-statusoncollectpickup)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum |  | 2 |
| `threshold` | Number |  | 2 |
| `ExtraBasicMoves_Status` | Number | Applies or references the 'ExtraBasicMoves_Status' effect/state. | 1 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 1 |
| `expires_on_end_turn` | Boolean |  | 1 |

</details>

---

### Context: `StatusIfUnusedActPoints` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`BackflipWhenTargeted`](./Math_Equations.md) | Enum | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. | 1 |
| [`Craft`](./Items_and_Equipment.md#context-craft) | Block | Synthesizes or spawns a new item from a specific pool. | 1 |

</details>

---

### Context: `StatusOnAllyCatDeath` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnBackstab` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 1 |
| `SerratedClaws` | Number | Applies or references the 'SerratedClaws' effect/state. | 1 |

</details>

---

### Context: `StatusOnBreakItem` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnCastSpell` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnGainCoins` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnSetPieceBreak` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum |  | 1 |
| `PermanentCharisma` | Number |  | 1 |
| `PermanentConstitution` | Number |  | 1 |
| `PermanentDexterity` | Number |  | 1 |
| `PermanentIntelligence` | Number |  | 1 |
| `PermanentLuck` | Number |  | 1 |
| `PermanentSpeed` | Number |  | 1 |
| `PermanentStrength` | Number |  | 1 |
| [`set`](./Enums.md#enum-set) | Enum |  | 1 |

</details>

---

### Context: `bonus_passives` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`str_aux_is_copy_ability`](./Items_and_Equipment.md#context-str_aux_is_copy_ability)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `cost` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ModifyAbility`](./Items_and_Equipment.md#context-modifyability)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `charge` | Number |  | 2 |
| `mana` | Number |  | 2 |

</details>

---

### Context: `keyword_tooltips` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[keyword_id]`](./Engine_Statuses.md#all-confirmed-keyword-id-values) | String | A Status or Keyword ID whose tooltip text is defined here. See Engine_Statuses.md for all IDs. |  |
</details>

---

### Context: `meta` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ModifyAbility`](./Items_and_Equipment.md#context-modifyability)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `is_basic_attack` | Boolean |  | 2 |
| `is_weapon` | Boolean |  | 2 |

</details>

---

### Context: `passive` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Metal` | Number | Applies or references the 'Metal' effect/state. | 2 |

</details>

---

### Context: `str_aux_is_copy_ability` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bonus_passives`](./Items_and_Equipment.md#context-bonus_passives) | Block | Passives granted to the character while this ability is equipped. | 2 |

</details>

---

### Context: `AIControlNextTurn` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `AbilityHealthThreshold` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 1 |
| `aux` | Number |  | 1 |
| `even_if_stunned` | Boolean |  | 1 |
| `immediate` | Boolean |  | 1 |
| [`threshold`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `AbilityOnRoundEndOnce` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 1 |
| `even_of_stunned` | Boolean |  | 1 |

</details>

---

### Context: `AddAdvantageToEvent` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `add` | Number |  | 1 |
| [`options`](./Arrays.md#array-options) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `AddPassivesToCharmed` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `AddSelfStatusToWeapons` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `AddStatusToBackstabs` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. | 1 |

</details>

---

### Context: `AddStatusToFirstSpellEachTurn` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_IsSelf`](./Abilities_and_Spells.md#context-conditional_isself) | Block |  | 1 |
| [`Else`](./Items_and_Equipment.md#context-else) | Block |  | 1 |

</details>

---

### Context: `AddStatusToWeapons` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `AddTemporaryEffectsToBasicAttack` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CastAgainWithStatus`](./Items_and_Equipment.md#context-castagainwithstatus) | Block | Applies or references the 'CastAgainWithStatus' effect/state. | 1 |

</details>

---

### Context: `AlluringDoodieEater` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| [`damage_instance`](./Items_and_Equipment.md#context-damage_instance) | Block |  | 1 |

</details>

---

### Context: `AllyDodgeChanceAura` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| `range` | Number | Distance or area of effect in tiles. | 1 |

</details>

---

### Context: `ApplyPassives` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_RandomChance`](./Items_and_Equipment.md#context-conditional_randomchance)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |
| [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend) | Block | Applies the nested status effects when the encounter finishes. | 1 |

</details>

---

### Context: `ApplyToRandomPartyMemberIfPossible` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
</details>

---

### Context: `BackflipWhenTargeted` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific dodge ability to trigger (e.g., DestroyerDodge). | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `BouncyProjectiles` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number |  | 1 |
| `max_range` | Number |  | 1 |

</details>

---

### Context: `BuffImmunity` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exclude`](./Enums.md#enum-exclude) | Enum |  | 1 |

</details>

---

### Context: `CastAgainWithStatus` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddTemporaryEffectsToBasicAttack`](./Items_and_Equipment.md#context-addtemporaryeffectstobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | Number | Applies or references the 'OverrideDamage' effect/state. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `CatPartsSizeScale` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `head` | Number |  | 1 |

</details>

---

### Context: `ChanceToForceEvent` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| [`event`](./Enums.md#enum-event) | Enum |  | 1 |

</details>

---

### Context: `Conditional_Ally` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
</details>

---

### Context: `Conditional_Corpse` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
</details>

---

### Context: `Conditional_Enemy` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToSpells`](./Items_and_Equipment.md#context-addstatustospells)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
</details>

---

### Context: `Conditional_HasCleansableDebuffs` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`VisualFX`](./Enums.md#enum-visualfx) | Enum |  | 1 |

</details>

---

### Context: `Conditional_HealthThreshold` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| `threshold_flat` | Number | A flat numerical health value threshold. | 1 |

</details>

---

### Context: `Conditional_ManaThreshold` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| `threshold_flat` | Number |  | 1 |

</details>

---

### Context: `Conditional_PlayerCat` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
</details>

---

### Context: `Conditional_RandomChance` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
| [`ApplyPassives`](./Items_and_Equipment.md#context-applypassives) | Block | Grants the nested passive abilities dynamically. | 1 |
| `odds` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Context: `Conditional_Shielded` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |  |
</details>

---

### Context: `ConvertDamageToScaledStatus` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DelayedPain` | Number | Applies or references the 'DelayedPain' effect/state. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `CritsApplyStatus` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `CyborgTurns` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`TakeBonusTurnWithAIControl`](./Items_and_Equipment.md#context-takebonusturnwithaicontrol) | Block |  | 1 |
| `stacks` | Number |  | 1 |

</details>

---

### Context: `DestroyEquipmentAndAttachParasite` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| [`pool`](./Arrays.md#array-pool) | Array | The item pool to draw the parasite from. | 1 |

</details>

---

### Context: `Eternal` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health_percent` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `FlyDamageIncrease` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `ForceUseAbilityOnTarget` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 1 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Context: `GlobalFlowerTrapperAura` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Tangled`](./Arrays.md#array-tangled) | Array |  | 1 |

</details>

---

### Context: `GlobalMeleeRevengeDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `knockback` | Number |  | 1 |

</details>

---

### Context: `ImmediateUseAbility` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 1 |
| `even_if_stunned` | Boolean |  | 1 |

</details>

---

### Context: `KnockUpAndAway` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | The distance in tiles to knock the target away. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `KnockbackIfCrit` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `knockback` | Number |  | 1 |
| `override_chain_knockback` | Number |  | 1 |

</details>

---

### Context: `ManaGainRange` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number |  | 1 |
| `min` | Number |  | 1 |

</details>

---

### Context: `ObjectDetector` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

### Context: `PassiveWhenAffectedByElement` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 1 |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | Passives granted by equipping this. | 1 |

</details>

---

### Context: `PassiveWhileHasDurability` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`MovementReaction`](./Items_and_Equipment.md#context-movementreaction) | Block | Applies or references the 'MovementReaction' effect/state. | 1 |

</details>

---

### Context: `PassiveWhileInMonkMeleeStance` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean / Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `PassiveWhileShielded` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 1 |

</details>

---

### Context: `PoopWhenHit` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

### Context: `RandomPermanentStatsDistinct` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEatPill`](./Items_and_Equipment.md#context-statusoneatpill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`stats`](./Arrays.md#array-stats) | Array |  | 1 |

</details>

---

### Context: `RandomStatusFromPool` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `RemoveStatusStacks` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks to remove. | 1 |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 1 |

</details>

---

### Context: `ReviveNextRound` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 1 |
| `revive_health` | Number | The flat amount of health to revive with. | 1 |

</details>

---

### Context: `Robot` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean |  | 1 |

</details>

---

### Context: `ScaldingOrbMoonBossOneShot` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum | Applies or references the 'CompleteItemQuest' effect/state. | 1 |
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum | Applies or references the 'RemoveItem' effect/state. | 1 |

</details>

---

### Context: `ScaledStatusAlliesOnSpendMana` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent) | Block | Conditional constraint. Nested properties only trigger if this is true. | 1 |

</details>

---

### Context: `ScaledStatusOnHolyShieldBlock` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. | 1 |

</details>

---

### Context: `ScaledStatusOnSpendMana` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`StatusAfterXStacks`](./Items_and_Equipment.md#context-statusafterxstacks) | Block | Applies or references the 'StatusAfterXStacks' effect/state. | 1 |

</details>

---

### Context: `SpawnCatCopyOnBattleStart` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum |  | 1 |

</details>

---

### Context: `SpawnObjectOnPopCorpse` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Number | Quantity. | 1 |
| `except_tiny` | Boolean |  | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

### Context: `SpawnOnDeath` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 1 |
| [`obj`](./Enums.md#enum-obj) | Enum |  | 1 |

</details>

---

### Context: `SpawnRandomPickupsOnTaggedUnitKilled` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array | Quantity. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 1 |

</details>

---

### Context: `StatDependentPassive` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddDamageToBasicAttack`](./Math_Equations.md) | Equation | Applies or references the 'AddDamageToBasicAttack' effect/state. | 1 |

</details>

---

### Context: `StatusAdjacentOnTheirTurnEnd` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceMoveAway` | Number | Applies or references the 'ForceMoveAway' effect/state. | 1 |

</details>

---

### Context: `StatusAfterXTurns` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `StatusAlliesEachTurn` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusAlliesOnDeath` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusEachRoundEnd` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusEachTurnEndForEachTurn` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnCollectPickup` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnDodge` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Number | Applies or references the 'DodgeChance_Status' effect/state. | 1 |

</details>

---

### Context: `StatusOnEatFood` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnEatPill` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnEnemyDeath` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 1 |

</details>

---

### Context: `StatusOnFallAsleep` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 1 |
| `FillMana` | Number | Applies or references the 'FillMana' effect/state. | 1 |
| `HealRandomInjury` | Number | Applies or references the 'HealRandomInjury' effect/state. | 1 |

</details>

---

### Context: `StatusOnFullMana` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](./Items_and_Equipment.md#context-conditional_onceperbattle) | Block | Conditional trigger: Executes nested logic only once per encounter/battle. | 1 |

</details>

---

### Context: `StatusOnHealed` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnPickupCoins` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnTurnEndIfCastNSpells` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DoubleCastSpell` | Number |  | 1 |
| `spells` | Number |  | 1 |

</details>

---

### Context: `StatusOnUseBasicAttack` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusWhenAllySpendsMana` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
</details>

---

### Context: `TakeBonusTurnWithAIControl` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CyborgTurns`](./Items_and_Equipment.md#context-cyborgturns)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number / Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |  |
| `end_of_round` | Boolean |  | 1 |
| `include_spells` | Boolean |  | 1 |

</details>

---

### Context: `TempPassiveUntilSettled` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEatFood`](./Items_and_Equipment.md#context-statusoneatfood)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LimitHeal` | Number | Applies or references the 'LimitHeal' effect/state. | 1 |

</details>

---

### Context: `TintItem` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`add`](./Arrays.md#array-add) | Array |  | 1 |
| [`ignore_if_str_aux_equals`](./Enums.md#enum-ignore_if_str_aux_equals) | Enum |  | 1 |
| [`mul`](./Arrays.md#array-mul) | Array |  | 1 |

</details>

---

### Context: `TransformWeapon` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | The original weapon ID. | 1 |
| [`to`](./Enums.md#enum-to) | Enum | The transformed weapon ID. | 1 |

</details>

---

### Context: `TunnelVision` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `crit_chance` | Number |  | 1 |

</details>

---

### Context: `damage_instance` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AlluringDoodieEater`](./Items_and_Equipment.md#context-alluringdoodieeater)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[damage_instance]`](./Engine_Damage.md#all-confirmed-damage-instance-values) | Block | A damage hit definition. See Engine_Damage.md for the full schema. |  |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Items_and_Equipment.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

