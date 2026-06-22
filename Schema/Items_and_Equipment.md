# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Items & Equipment

> **Associated Files:** `data/items/, data/item_setbonuses.gon`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1217

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the item's desc. | 1217 |
| [`name`](./Strings.md#string-name) | String | Localization key for the item's name. | 1206 |
| `frame` | Integer |  | 1106 |
| [`kind`](./Enums.md#enum-kind) | Enum |  | 1106 |
| [`rarity`](./Enums.md#enum-rarity) | Enum |  | 967 |
| [`passives`](#context-passives) | Block | Passives granted by equipping this. | 823 |
| [`set`](./Enums.md#enum-set) | Enum |  | 765 |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 365 |
| `shield` | Integer |  | 186 |
| `durability` | Integer | Maximum uses before breaking. | 171 |
| `pieces_required` | Integer |  | 101 |
| `cursed` | Boolean |  | 77 |
| `cha` | Integer |  | 75 |
| `consumable` | Boolean |  | 64 |
| `spd` | Integer |  | 60 |
| `con` | Integer |  | 57 |
| `int` | Integer |  | 54 |
| `lck` | Integer |  | 44 |
| `quest_item` | Boolean |  | 40 |
| `parasite` | Boolean |  | 36 |
| `aux` | Integer |  | 33 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum |  | 29 |
| `str` | Integer |  | 28 |
| `dex` | Integer |  | 22 |
| [`quest_reward_item`](./Enums.md#enum-quest_reward_item) | Enum |  | 22 |
| `indestructible` | Boolean |  | 20 |
| `divine_shield` | Integer |  | 17 |
| `legacy_quest` | Boolean |  | 17 |
| [`hint_destination`](./Enums.md#enum-hint_destination) | Enum |  | 16 |
| [`str_aux_initialize`](./Enums.md#enum-str_aux_initialize) | Enum |  | 15 |
| `dont_destroy_on_0` | Boolean |  | 13 |
| [`global_tags`](./Arrays.md#array-global_tags) | Array |  | 12 |
| `max_durability` | Integer |  | 11 |
| [`on_store`](./Enums.md#enum-on_store) | Enum |  | 8 |
| [`name_mod`](./Strings.md#string-name_mod) | String |  | 7 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 6 |
| [`hint_prerequisite_flag`](./Enums.md#enum-hint_prerequisite_flag) | Enum |  | 5 |
| `failable` | Boolean |  | 4 |
| [`global_passives`](#context-global_passives) | Block |  | 4 |
| `randomize_piece_frames` | Boolean |  | 4 |
| `str_aux_is_copy_passive` | Boolean |  | 4 |
| `fragile` | Boolean |  | 3 |
| [`icon_hint`](./Enums.md#enum-icon_hint) | String |  | 3 |
| `max_health` | Integer |  | 3 |
| `reset_aux_on_store` | Integer |  | 3 |
| `sticky` | Boolean |  | 3 |
| `weightless` | Boolean |  | 3 |
| [`keyword_tooltips`](#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear when hovering over the ability. | 2 |
| [`passive`](#context-passive) | Block |  | 2 |
| `prevent_level_up` | Boolean |  | 2 |
| [`quest_item_alias`](./Enums.md#enum-quest_item_alias) | Enum |  | 2 |
| `speed` | Float |  | 2 |
| [`str_aux_is_copy_ability`](#context-str_aux_is_copy_ability) | Block |  | 2 |
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

### Context: `passives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 848

> **Referenced by:** [`PassiveAfterXKills`](#context-passiveafterxkills), [`PassiveAtHealthThreshold`](#context-passiveathealththreshold), [`PassiveAtStatThreshold`](#context-passiveatstatthreshold), [`PassiveIfStrAuxEquals`](#context-passiveifstrauxequals), [`PassiveWhenAffectedByElement`](#context-passivewhenaffectedbyelement), [`PassiveWhenOnTile`](#context-passivewhenontile), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`AddStatusToBasicAttack`](#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 68 |
| [`MeleeRevengeDamage`](#context-meleerevengedamage) | Block | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. | 34 |
| [`StatusOnBattleEnd`](#context-statusonbattleend) | Block | Applies the nested status effects when the encounter finishes. | 30 |
| [`StatusEachTurnEnd`](#context-statuseachturnend) | Block | Applies or references the 'StatusEachTurnEnd' effect/state. | 27 |
| [`StatusOnBreak`](#context-statusonbreak) | Block | Event Trigger: Applies statuses when this action occurs. | 22 |
| [`StatusOnKill`](#context-statusonkill) | Block | Event Trigger: Applies statuses when this action occurs. | 18 |
| [`StatusOnTookDamage`](#context-statusontookdamage) | Block | Event Trigger: Applies statuses when this action occurs. | 17 |
| [`StatusOnBattleStart`](#context-statusonbattlestart) | Block | Event Trigger: Applies statuses when this action occurs. | 13 |
| [`RevengeDamage`](#context-revengedamage) | Block | Reaction trigger: Deals damage to the attacker when hit. | 9 |
| [`StatusEachTurnBegin`](#context-statuseachturnbegin) | Block | Applies or references the 'StatusEachTurnBegin' effect/state. | 9 |
| [`AddSelfStatusToBasicAttack`](#context-addselfstatustobasicattack) | Block | Applies or references the 'AddSelfStatusToBasicAttack' effect/state. | 8 |
| [`AddStatusToAllDamage`](#context-addstatustoalldamage) | Block | Modifier: Injects a status effect into a specific action. | 8 |
| [`StatusAlliesOnBattleStart`](#context-statusalliesonbattlestart) | Block | Applies or references the 'StatusAlliesOnBattleStart' effect/state. | 8 |
| [`StatusOnKillEnemy`](#context-statusonkillenemy) | Block | Event Trigger: Applies statuses when this action occurs. | 8 |
| [`AddPassivesToMinions`](#context-addpassivestominions) | Block | Applies or references the 'AddPassivesToMinions' effect/state. | 7 |
| [`StatusOnDie`](#context-statusondie) | Block | Event Trigger: Applies statuses when this action occurs. | 6 |
| [`PassiveAtHealthThreshold`](#context-passiveathealththreshold) | Block | Applies or references the 'PassiveAtHealthThreshold' effect/state. | 5 |
| [`StatusOnEndMove`](#context-statusonendmove) | Block | Event Trigger: Applies statuses when this action occurs. | 5 |
| [`StatusRandomEnemiesOnBattleStart`](#context-statusrandomenemiesonbattlestart) | Block | Applies or references the 'StatusRandomEnemiesOnBattleStart' effect/state. | 4 |
| [`CatchProjectiles`](#context-catchprojectiles) | Block | Applies or references the 'CatchProjectiles' effect/state. | 3 |
| [`ExtraStatusWhenDealingDamage`](#context-extrastatuswhendealingdamage) | Block | Applies or references the 'ExtraStatusWhenDealingDamage' effect/state. | 3 |
| [`PassiveAtStatThreshold`](#context-passiveatstatthreshold) | Block | Applies or references the 'PassiveAtStatThreshold' effect/state. | 3 |
| [`PassiveWhenDead`](#context-passivewhendead) | Block | State Trigger: Grants passives when this condition is met. | 3 |
| [`StatusAllCharactersOnSpawn`](#context-statusallcharactersonspawn) | Block | Applies or references the 'StatusAllCharactersOnSpawn' effect/state. | 3 |
| [`StatusEveryXSpellCasts`](#context-statuseveryxspellcasts) | Block | Applies or references the 'StatusEveryXSpellCasts' effect/state. | 3 |
| [`StatusIfUnusedMovePoints`](#context-statusifunusedmovepoints) | Block | Applies or references the 'StatusIfUnusedMovePoints' effect/state. | 3 |
| [`StatusOnPopCorpse`](#context-statusonpopcorpse) | Block | Event Trigger: Applies statuses when this action occurs. | 3 |
| [`AddStatusToElementDamage`](#context-addstatustoelementdamage) | Block | Modifier: Injects a status effect into a specific action. | 2 |
| [`AddStatusToKnockbackDamage`](#context-addstatustoknockbackdamage) | Block | Modifier: Injects a status effect into a specific action. | 2 |
| [`AddStatusToSpells`](#context-addstatustospells) | Block | Modifier: Injects a status effect into a specific action. | 2 |
| [`ApplyStatusesToRandomEnemiesEachTurn`](#context-applystatusestorandomenemieseachturn) | Block | Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state. | 2 |
| [`PassiveAfterXKills`](#context-passiveafterxkills) | Block | Applies or references the 'PassiveAfterXKills' effect/state. | 2 |
| [`StatusAfterCastSpell`](#context-statusaftercastspell) | Block | Applies or references the 'StatusAfterCastSpell' effect/state. | 2 |
| [`StatusOnAllyCatDeath`](#context-statusonallycatdeath) | Block | Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnBreakItem`](#context-statusonbreakitem) | Block | Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnCastSpell`](#context-statusoncastspell) | Block | Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnGainCoins`](#context-statusongaincoins) | Block | Event Trigger: Applies statuses when this action occurs. | 2 |
| [`AddPassivesToCharmed`](#context-addpassivestocharmed) | Block | Applies or references the 'AddPassivesToCharmed' effect/state. | 1 |
| [`AddSelfStatusToWeapons`](#context-addselfstatustoweapons) | Block | Applies or references the 'AddSelfStatusToWeapons' effect/state. | 1 |
| [`AddStatusToWeapons`](#context-addstatustoweapons) | Block | Modifier: Injects a status effect into a specific action. | 1 |
| [`CreateGlobalModifiers`](#context-createglobalmodifiers) | Block | Generates global map or encounter rules/modifiers. | 1 |
| [`CritsApplyStatus`](#context-critsapplystatus) | Block | Applies or references the 'CritsApplyStatus' effect/state. | 1 |
| [`PassiveWhenAffectedByElement`](#context-passivewhenaffectedbyelement) | Block | State Trigger: Grants passives when this condition is met. | 1 |
| [`PassiveWhileInMonkMeleeStance`](#context-passivewhileinmonkmeleestance) | Block | Applies or references the 'PassiveWhileInMonkMeleeStance' effect/state. | 1 |
| [`StatusAfterXTurns`](#context-statusafterxturns) | Block | Applies or references the 'StatusAfterXTurns' effect/state. | 1 |
| [`StatusAlliesEachTurn`](#context-statusallieseachturn) | Block | Applies or references the 'StatusAlliesEachTurn' effect/state. | 1 |
| [`StatusAlliesOnDeath`](#context-statusalliesondeath) | Block | Applies or references the 'StatusAlliesOnDeath' effect/state. | 1 |
| [`StatusEachTurnEndForEachTurn`](#context-statuseachturnendforeachturn) | Block | Applies or references the 'StatusEachTurnEndForEachTurn' effect/state. | 1 |
| [`StatusOnCollectPickup`](#context-statusoncollectpickup) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnEatFood`](#context-statusoneatfood) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnEatPill`](#context-statusoneatpill) | Block |  | 1 |
| [`StatusOnHealed`](#context-statusonhealed) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnPickupCoins`](#context-statusonpickupcoins) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnUseBasicAttack`](#context-statusonusebasicattack) | Block | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusWhenAllySpendsMana`](#context-statuswhenallyspendsmana) | Block | Applies or references the 'StatusWhenAllySpendsMana' effect/state. | 1 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 69

> **Referenced by:** [`AddPassivesToMinions`](#context-addpassivestominions), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |

</details>

---

### Context: `effects`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 37

> **Referenced by:** [`DoDamage`](#context-dodamage), [`MeleeRevengeDamage`](#context-meleerevengedamage), [`RevengeDamage`](#context-revengedamage), [`damage_instance`](#context-damage_instance)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 34

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 25 |
| `knockback` | Integer |  | 9 |
| `damage` | Integer | The base damage properties of an attack. | 5 |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 31

> **Referenced by:** [`ApplyPassives`](#context-applypassives), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 12 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 27

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Conditional_HasCleansableDebuffs`](#context-conditional_hascleansabledebuffs) | Block |  | 1 |

</details>

---

### Context: `SpawnOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 22

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 22 |
| [`number`](./Arrays.md#array-number) | Integer |  | 16 |

</details>

---

### Context: `StatusOnBreak`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 22

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ApplyToRandomPartyMemberIfPossible`](#context-applytorandompartymemberifpossible) | Block | Redirects the nested effects to apply to a random living member of the player's party. | 1 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 19

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack), [`StatusEachTurnEnd`](#context-statuseachturnend), [`StatusOnBattleEnd`](#context-statusonbattleend), [`StatusOnKill`](#context-statusonkill), [`StatusOnTakeHealthOrShieldDamage`](#context-statusontakehealthorshielddamage), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `odds` | Float | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 19 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 18

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 17

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 13

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 13 |
| `good` | Boolean |  | 4 |
| `shield_only` | Boolean |  | 2 |
| `spawn_on_death_hit` | Boolean |  | 2 |
| [`chance`](./Math_Equations.md) | Equation | Probability (0.0 to 1.0 or percentage) of this occurring. (Must be float values) | 1 |
| `number` | Integer |  | 1 |

</details>

---

### Context: `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 13

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Enum |  | 12 |
| [`chance`](./Math_Equations.md) | Equation | Probability (0.0 to 1.0 or percentage) of this occurring. (Must be float values) | 11 |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum |  | 5 |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 10

> **Referenced by:** [`PassiveWhenDead`](#context-passivewhendead), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 9 |
| `damage` | Integer | The base damage properties of an attack. | 3 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |

</details>

---

### Context: `AddSelfStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `must_do_damage` | Boolean |  | 3 |

</details>

---

### Context: `StatusAlliesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnKillEnemy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `AddPassivesToMinions`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`AddStatusToBasicAttack`](#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 1 |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum |  | 1 |

</details>

---

### Context: `DurabilityTransform`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eq`](./Arrays.md#array-eq) | Array |  | 11 |
| [`ge`](./Arrays.md#array-ge) | Array |  | 4 |

</details>

---

### Context: `GainCoinsRange`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`StatusOnBattleEnd`](#context-statusonbattleend), [`StatusOnBreak`](#context-statusonbreak), [`StatusOnDie`](#context-statusondie)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Integer | Maximum coins granted. | 7 |
| `min` | Integer | Minimum coins granted. | 7 |

</details>

---

### Context: `PassiveIfStrAuxEquals`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Passives granted by equipping this. | 7 |
| [`value`](./Math_Equations.md) | Float |  | 7 |

</details>

---

### Context: `PassiveWhenOnTile`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Passives granted by equipping this. | 7 |
| [`tile`](./Arrays.md#array-tile) | Array |  | 7 |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack), [`Conditional_HasStatus`](#context-conditional_hasstatus), [`Else`](#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `ItemAuxTransform`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`le`](./Arrays.md#array-le) | Array |  | 6 |
| [`ge`](./Arrays.md#array-ge) | Array |  | 2 |
| [`lt`](./Arrays.md#array-lt) | Array |  | 1 |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`CreateGlobalModifiers`](#context-createglobalmodifiers) | Block | Generates global map or encounter rules/modifiers. | 1 |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `DelayedAutoRevive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Integer |  | 5 |
| `rounds` | Integer |  | 5 |

</details>

---

### Context: `PassiveAtHealthThreshold`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 5 |
| [`passives`](#context-passives) | Block | Passives granted by equipping this. | 5 |
| `threshold` | Integer |  | 5 |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 5 |
| [`object`](./Enums.md#enum-object) | Enum |  | 5 |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Temporary`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`Conditional_BadRoll`](#context-conditional_badroll), [`StatusEachTurnBegin`](#context-statuseachturnbegin), [`StatusOnTookDamage`](#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Integer | Number of stacks or intensity to apply. | 5 |
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 5 |
| `expires_on_end_turn` | Boolean |  | 4 |
| `turns` | Integer | Duration in turns. | 4 |
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 1 |

</details>

---

### Context: `TransformItemOnElementInfluence`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 5 |
| `full_repair` | Boolean |  | 5 |
| [`item`](./Enums.md#enum-item) | Enum | Item ID to reference. | 5 |

</details>

---

### Context: `AddDamageToElementDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer | The base damage properties of an attack. | 4 |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 4 |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reduction` | Integer |  | 4 |
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 3 |

</details>

---

### Context: `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`AddStatusToAllDamage`](#context-addstatustoalldamage), [`StatusOnTookDamage`](#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 4 |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 2 |

</details>

---

### Context: `Craft`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`StatusIfUnusedActPoints`](#context-statusifunusedactpoints), [`StatusOnBattleStart`](#context-statusonbattlestart)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 4 |
| [`slot`](./Enums.md#enum-slot) | Enum | Equipment slot (weapon, hat, face, chest, etc.). | 4 |
| `works_with_tech` | Boolean |  | 3 |

</details>

---

### Context: `Else`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`AddStatusToFirstSpellEachTurn`](#context-addstatustofirstspelleachturn), [`Conditional_PartyMember`](#context-conditional_partymember)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 |

</details>

---

### Context: `StatusOnTakeHealthOrShieldDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array | Applies or references the 'DivineShield' effect/state. | 2 |
| [`Conditional_GoodRoll`](#context-conditional_goodroll) | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 1 |
| `Metronome` | Integer | Executes a random musical or metronome ability. | 1 |

</details>

---

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 4 |
| `AllStatsUp` | Integer |  | 1 |
| `Charge` | Integer | Applies or references the 'Charge' effect/state. | 1 |
| `DamageUp` | Integer | Applies or references the 'DamageUp' effect/state. | 1 |
| `HealthRegenUp` | Integer | Applies or references the 'HealthRegenUp' effect/state. | 1 |
| `Shield` | Integer | Applies or references the 'Shield' effect/state. | 1 |
| `SpellDamageUp` | Integer | Applies or references the 'SpellDamageUp' effect/state. | 1 |
| `Thorns` | Integer | Applies or references the 'Thorns' effect/state. | 1 |

</details>

---

### Context: `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `count` | Integer | Quantity. | 4 |

</details>

---

### Context: `global_passives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Global Modifiers}`](./Engine_GlobalModifiers.md#all-confirmed-global-modifier-id-values) | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |  |
| `GlobalEnemyAutoRevive` | Integer | Applies or references the 'GlobalEnemyAutoRevive' effect/state. | 2 |
| `NoCorpses` | Integer | Applies or references the 'NoCorpses' effect/state. | 1 |
| `RealTimePressure` | Integer | Applies or references the 'RealTimePressure' effect/state. | 1 |

</details>

---

### Context: `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `ally_chance` | Integer |  | 3 |
| `chance` | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 3 |
 | `Quivered` | Number | Applies or references the 'Quivered' effect/state. | 3 | 

</details>

---

### Context: `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`ExtraStatusWhenDealingDamage`](#context-extrastatuswhendealingdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Else`](#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 3 |

</details>

---

### Context: `CounterAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 3 |
| `melee_only` | Boolean |  | 1 |
| `ranged_only` | Boolean |  | 1 |

</details>

---

### Context: `DeathRattle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum |  | 3 |
| `pop_corpse` | Boolean |  | 3 |

</details>

---

### Context: `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
</details>

---

### Context: `PassiveAtStatThreshold`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 3 |
| [`passives`](#context-passives) | Block | Passives granted by equipping this. | 3 |
| [`threshold`](#context-threshold) | Block |  | 3 |

</details>

---

### Context: `PassiveWhenDead`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`StatusEachRoundEnd`](#context-statuseachroundend) | Block | Applies or references the 'StatusEachRoundEnd' effect/state. | 1 |
| [`StatusEachTurnBegin`](#context-statuseachturnbegin) | Block | Applies or references the 'StatusEachTurnBegin' effect/state. | 1 |

</details>

---

### Context: `SetItemAux`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`Conditional_Shielded`](#context-conditional_shielded), [`StatusOnBattleEnd`](#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum | Equipment slot (weapon, hat, face, chest, etc.). | 3 |
| [`value`](./Math_Equations.md) | Float |  | 3 |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `number` | Integer |  | 3 |
| [`object`](./Enums.md#enum-object) | Enum |  | 3 |

</details>

---

### Context: `StackingFlowerTrail`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum |  | 3 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 3 |

</details>

---

### Context: `StatusAllCharactersOnSpawn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `stacks` | Integer | Number of stacks or intensity to apply. | 3 |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `threshold`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`PassiveAtStatThreshold`](#context-passiveatstatthreshold)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Integer |  | 2 |
| `con` | Integer |  | 1 |

</details>

---

### Context: `AddStatusToElementDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 2 |

</details>

---

### Context: `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `count` | Integer | Quantity. | 1 |

</details>

---

### Context: `ArmorBreakOnHit`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance_to_break` | Integer |  | 2 |
| `durability_loss` | Integer |  | 2 |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`PassiveWhenDead`](#context-passivewhendead), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 2 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 2 |

</details>

---

### Context: `BoostWeaponDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `crit_chance` | Float |  | 2 |
| `damage` | Integer | The base damage properties of an attack. | 2 |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 2 |
| `chance` | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |

</details>

---

### Context: `ChanceToBlockAndCounter`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean |  | 1 |
| `chance` | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Context: `ChanceToRevive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Integer |  | 2 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ScaledStatusAlliesOnSpendMana`](#context-scaledstatusalliesonspendmana), [`StatusAlliesEachTurn`](#context-statusallieseachturn)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`StatusEachTurnBegin`](#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`odds`](./Math_Equations.md) | Equation | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. (Must be float values) | 2 |

</details>

---

### Context: `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`StatusAllCharactersOnSpawn`](#context-statusallcharactersonspawn)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`AddStatusToAllDamage`](#context-addstatustoalldamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. | 2 |

</details>

---

### Context: `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`Conditional_HealthThreshold`](#context-conditional_healththreshold), [`StatusOnFullMana`](#context-statusonfullmana)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`key`](./Enums.md#enum-key) | Enum |  | 1 |

</details>

---

### Context: `CreateGlobalModifiers`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`StatusOnDie`](#context-statusondie), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Global Modifiers}`](./Engine_GlobalModifiers.md#all-confirmed-global-modifier-id-values) | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |  |
</details>

---

### Context: `DoDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`StatusEachRoundEnd`](#context-statuseachroundend), [`StatusOnBreakItem`](#context-statusonbreakitem)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer | The flat damage amount. | 2 |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum |  | 2 |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification of the damage (e.g., spell, melee). | 2 |

</details>

---

### Context: `ElementalManaCostReduction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array | Specific element type required or applied. | 2 |
| `reduction` | Integer |  | 2 |

</details>

---

### Context: `ModifyAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`bonus_passives`](#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cost`](#context-cost) | Block | Currency value in shops/merchants. | 2 |
| [`meta`](#context-meta) | Block |  | 2 |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`PassiveWhileHasDurability`](#context-passivewhilehasdurability), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 2 |
| `create_temp_ability` | Boolean |  | 2 |
| `enemies_only` | Boolean |  | 2 |
| `on_self_move_too` | Boolean |  | 1 |

</details>

---

### Context: `ObjectOnHitCharacter`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`StatusEveryXSpellCasts`](#context-statuseveryxspellcasts), [`StatusOnBattleStart`](#context-statusonbattlestart)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the character to spawn (e.g., CharmedFlea). | 2 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `PassiveAfterXKills`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Passives granted by equipping this. | 2 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `PassiveIfWeaponIsUsable`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Brace` | Integer | Applies or references the 'Brace' effect/state. | 2 |

</details>

---

### Context: `RefreshEquipmentAbilityOnElement`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 2 |
| [`text`](./Strings.md#string-text) | String |  | 2 |

</details>

---

### Context: `SpawnCatCopyWhenDowned`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum |  | 2 |

</details>

---

### Context: `SpawnItemLinkedFamiliar`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean |  | 2 |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |

</details>

---

### Context: `StatusAfterCastSpell`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusAfterXStacks`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ScaledStatusOnSpendMana`](#context-scaledstatusonspendmana), [`StatusOnCollectPickup`](#context-statusoncollectpickup)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum |  | 2 |
| `threshold` | Integer |  | 2 |
| `ExtraBasicMoves_Status` | Integer | Applies or references the 'ExtraBasicMoves_Status' effect/state. | 1 |
| `RefreshActPoints` | Integer | Applies or references the 'RefreshActPoints' effect/state. | 1 |
| `expires_on_end_turn` | Boolean |  | 1 |

</details>

---

### Context: `StatusIfUnusedActPoints`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`BackflipWhenTargeted`](./Math_Equations.md) | Enum | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. | 1 |
| [`Craft`](#context-craft) | Block | Synthesizes or spawns a new item from a specific pool. | 1 |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnBackstab`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `HealthGain` | Integer | Applies or references the 'HealthGain' effect/state. | 1 |
| `SerratedClaws` | Integer | Applies or references the 'SerratedClaws' effect/state. | 1 |

</details>

---

### Context: `StatusOnBreakItem`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnSetPieceBreak`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum |  | 1 |
| `PermanentCharisma` | Integer |  | 1 |
| `PermanentConstitution` | Integer |  | 1 |
| `PermanentDexterity` | Integer |  | 1 |
| `PermanentIntelligence` | Integer |  | 1 |
| `PermanentLuck` | Integer |  | 1 |
| `PermanentSpeed` | Integer |  | 1 |
| `PermanentStrength` | Integer |  | 1 |
| [`set`](./Enums.md#enum-set) | Enum |  | 1 |

</details>

---

### Context: `bonus_passives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`str_aux_is_copy_ability`](#context-str_aux_is_copy_ability)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `cost`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ModifyAbility`](#context-modifyability)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `charge` | Integer |  | 2 |
| `mana` | Integer |  | 2 |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`[keyword_id]`](./Engine_Statuses.md#all-confirmed-keyword_id-values) | String | A Status or Keyword ID whose tooltip text is defined here. See Engine_Statuses.md for all IDs. |  |
</details>

---

### Context: `meta`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ModifyAbility`](#context-modifyability)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `is_basic_attack` | Boolean |  | 2 |
| `is_weapon` | Boolean |  | 2 |

</details>

---

### Context: `passive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Metal` | Integer | Applies or references the 'Metal' effect/state. | 2 |

</details>

---

### Context: `str_aux_is_copy_ability`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bonus_passives`](#context-bonus_passives) | Block | Passives granted to the character while this ability is equipped. | 2 |

</details>

---

### Context: `AIControlNextTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean |  | 1 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `AbilityHealthThreshold`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 1 |
| `aux` | Integer |  | 1 |
| `even_if_stunned` | Boolean |  | 1 |
| `immediate` | Boolean |  | 1 |
| [`threshold`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `AbilityOnRoundEndOnce`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 1 |
| `even_of_stunned` | Boolean |  | 1 |

</details>

---

### Context: `AddAdvantageToEvent`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `add` | Integer |  | 1 |
| [`options`](./Arrays.md#array-options) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

### Context: `AddPassivesToCharmed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `AddStatusToBackstabs`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Bleed` | Integer | Applies or references the 'Bleed' effect/state. | 1 |

</details>

---

### Context: `AddStatusToFirstSpellEachTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Conditional_IsSelf`](./Abilities_and_Spells.md#context-conditional_isself) | Block |  | 1 |
| [`Else`](#context-else) | Block |  | 1 |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CastAgainWithStatus`](#context-castagainwithstatus) | Block | Applies or references the 'CastAgainWithStatus' effect/state. | 1 |

</details>

---

### Context: `AlluringDoodieEater`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| [`damage_instance`](#context-damage_instance) | Block |  | 1 |

</details>

---

### Context: `AllyDodgeChanceAura`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| `range` | Integer | Distance or area of effect in tiles. | 1 |

</details>

---

### Context: `ApplyPassives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`Conditional_RandomChance`](#context-conditional_randomchance)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`StatusOnBattleEnd`](#context-statusonbattleend) | Block | Applies the nested status effects when the encounter finishes. | 1 |

</details>

---

### Context: `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusOnBreak`](#context-statusonbreak)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific dodge ability to trigger (e.g., DestroyerDodge). | 1 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `BouncyProjectiles`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Integer |  | 1 |
| `max_range` | Integer |  | 1 |

</details>

---

### Context: `BuffImmunity`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exclude`](./Enums.md#enum-exclude) | Enum |  | 1 |

</details>

---

### Context: `CastAgainWithStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AddTemporaryEffectsToBasicAttack`](#context-addtemporaryeffectstobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| `OverrideDamage` | Integer | Applies or references the 'OverrideDamage' effect/state. | 1 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `CatPartsSizeScale`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `head` | Float |  | 1 |

</details>

---

### Context: `ChanceToForceEvent`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| [`event`](./Enums.md#enum-event) | Enum |  | 1 |

</details>

---

### Context: `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`Conditional_Adjacent`](#context-conditional_adjacent)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusOnBattleEnd`](#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AddStatusToSpells`](#context-addstatustospells)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_HasCleansableDebuffs`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusEachTurnEnd`](#context-statuseachturnend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`VisualFX`](./Enums.md#enum-visualfx) | Enum |  | 1 |

</details>

---

### Context: `Conditional_HealthThreshold`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusOnTookDamage`](#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `threshold_flat` | Integer | A flat numerical health value threshold. | 1 |

</details>

---

### Context: `Conditional_ManaThreshold`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusEachTurnEnd`](#context-statuseachturnend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `threshold_flat` | Integer |  | 1 |

</details>

---

### Context: `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`Conditional_Adjacent`](#context-conditional_adjacent)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusOnDie`](#context-statusondie)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ApplyPassives`](#context-applypassives) | Block | Grants the nested passive abilities dynamically. | 1 |
| `odds` | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Context: `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusOnBattleEnd`](#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `ConvertDamageToScaledStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `DelayedPain` | Integer | Applies or references the 'DelayedPain' effect/state. | 1 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `CritsApplyStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `CyborgTurns`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`TakeBonusTurnWithAIControl`](#context-takebonusturnwithaicontrol) | Block |  | 1 |
| `stacks` | Integer |  | 1 |

</details>

---

### Context: `DestroyEquipmentAndAttachParasite`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusOnBattleStart`](#context-statusonbattlestart)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Math_Equations.md) | Equation | Probability (0.0 to 1.0 or percentage) of this occurring. (Must be float values) | 1 |
| [`pool`](./Arrays.md#array-pool) | Array | The item pool to draw the parasite from. | 1 |

</details>

---

### Context: `Eternal`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `health_percent` | Integer |  | 1 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `FlyDamageIncrease`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 1 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `ForceUseAbilityOnTarget`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 1 |
| `chance` | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Context: `GlobalFlowerTrapperAura`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Tangled`](./Arrays.md#array-tangled) | Array |  | 1 |

</details>

---

### Context: `GlobalMeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `knockback` | Integer |  | 1 |

</details>

---

### Context: `ImmediateUseAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 1 |
| `even_if_stunned` | Boolean |  | 1 |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Integer | The distance in tiles to knock the target away. | 1 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `KnockbackIfCrit`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AddStatusToAllDamage`](#context-addstatustoalldamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `knockback` | Integer |  | 1 |
| `override_chain_knockback` | Integer |  | 1 |

</details>

---

### Context: `ManaGainRange`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusEachTurnBegin`](#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Integer |  | 1 |
| `min` | Integer |  | 1 |

</details>

---

### Context: `ObjectDetector`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 1 |
| [`passives`](#context-passives) | Block | Passives granted by equipping this. | 1 |

</details>

---

### Context: `PassiveWhileHasDurability`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`MovementReaction`](#context-movementreaction) | Block | Applies or references the 'MovementReaction' effect/state. | 1 |

</details>

---

### Context: `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `PassiveWhileShielded`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `HealthRegenUp` | Integer | Applies or references the 'HealthRegenUp' effect/state. | 1 |

</details>

---

### Context: `PoopWhenHit`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

### Context: `RandomPermanentStatsDistinct`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusOnEatPill`](#context-statusoneatpill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`stats`](./Arrays.md#array-stats) | Array |  | 1 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusOnDie`](#context-statusondie)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `RemoveStatusStacks`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`Conditional_HasStatus`](#context-conditional_hasstatus)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Integer | The number of stacks to remove. | 1 |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 1 |

</details>

---

### Context: `ReviveNextRound`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusOnBattleStart`](#context-statusonbattlestart)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Shield` | Integer | Applies or references the 'Shield' effect/state. | 1 |
| `revive_health` | Integer | The flat amount of health to revive with. | 1 |

</details>

---

### Context: `Robot`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean |  | 1 |

</details>

---

### Context: `ScaldingOrbMoonBossOneShot`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum | Applies or references the 'CompleteItemQuest' effect/state. | 1 |
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum | Applies or references the 'RemoveItem' effect/state. | 1 |

</details>

---

### Context: `ScaledStatusAlliesOnSpendMana`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Adjacent`](#context-conditional_adjacent) | Block | Conditional constraint. Nested properties only trigger if this is true. | 1 |

</details>

---

### Context: `ScaledStatusOnHolyShieldBlock`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `RandomMagicMissile` | Integer | Fires a randomized number of magic missiles. | 1 |

</details>

---

### Context: `ScaledStatusOnSpendMana`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`StatusAfterXStacks`](#context-statusafterxstacks) | Block | Applies or references the 'StatusAfterXStacks' effect/state. | 1 |

</details>

---

### Context: `SpawnCatCopyOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum |  | 1 |

</details>

---

### Context: `SpawnObjectOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Integer | Quantity. | 1 |
| `except_tiny` | Boolean |  | 1 |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

### Context: `SpawnOnDeath`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 1 |
| [`obj`](./Enums.md#enum-obj) | Enum |  | 1 |

</details>

---

### Context: `SpawnRandomPickupsOnTaggedUnitKilled`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array | Quantity. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 1 |

</details>

---

### Context: `StatDependentPassive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`AddDamageToBasicAttack`](./Math_Equations.md) | Equation | Applies or references the 'AddDamageToBasicAttack' effect/state. | 1 |

</details>

---

### Context: `StatusAdjacentOnTheirTurnEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| `ForceMoveAway` | Integer | Applies or references the 'ForceMoveAway' effect/state. | 1 |

</details>

---

### Context: `StatusAfterXTurns`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `StatusAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`PassiveWhenDead`](#context-passivewhendead)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnDodge`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `DodgeChance_Status` | Integer | Applies or references the 'DodgeChance_Status' effect/state. | 1 |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnEatPill`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnEnemyDeath`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Charge` | Integer | Applies or references the 'Charge' effect/state. | 1 |

</details>

---

### Context: `StatusOnFallAsleep`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AllStatsUp` | Integer | Applies or references the 'AllStatsUp' effect/state. | 1 |
| `FillMana` | Integer | Applies or references the 'FillMana' effect/state. | 1 |
| `HealRandomInjury` | Integer | Applies or references the 'HealRandomInjury' effect/state. | 1 |

</details>

---

### Context: `StatusOnFullMana`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](#context-conditional_onceperbattle) | Block | Conditional trigger: Executes nested logic only once per encounter/battle. | 1 |

</details>

---

### Context: `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnTurnEndIfCastNSpells`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `DoubleCastSpell` | Integer |  | 1 |
| `spells` | Integer |  | 1 |

</details>

---

### Context: `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `TakeBonusTurnWithAIControl`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`CyborgTurns`](#context-cyborgturns)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `end_of_round` | Boolean |  | 1 |
| `include_spells` | Boolean |  | 1 |

</details>

---

### Context: `TempPassiveUntilSettled`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusOnEatFood`](#context-statusoneatfood)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `LimitHeal` | Integer | Applies or references the 'LimitHeal' effect/state. | 1 |

</details>

---

### Context: `TintItem`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`add`](./Arrays.md#array-add) | Array |  | 1 |
| [`ignore_if_str_aux_equals`](./Enums.md#enum-ignore_if_str_aux_equals) | Enum |  | 1 |
| [`mul`](./Arrays.md#array-mul) | Array |  | 1 |

</details>

---

### Context: `TransformWeapon`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusOnBattleEnd`](#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | The original weapon ID. | 1 |
| [`to`](./Enums.md#enum-to) | Enum | The transformed weapon ID. | 1 |

</details>

---

### Context: `TunnelVision`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `crit_chance` | Float |  | 1 |

</details>

---

### Context: `damage_instance`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AlluringDoodieEater`](#context-alluringdoodieeater)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damage Blocks}`](./Engine_Damage.md#all-confirmed-damage-instance-values) | Block | A damage hit definition. See Engine_Damage.md for the full schema. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `damage` | Integer | The base damage properties of an attack. | 1 |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 1 |

</details>

---

