# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Passives & Statuses

> **Associated Files:** `data/passives/, data/passive_pools.gon`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 511

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`name`](./Strings.md#string-name) | String | Localization key for the passive's display name. | 511 |
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 510 |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the passive's display description. | 510 |
| [`passives`](#context-passives) | Block |  | 116 |
| [`stats`](#context-stats) | Block |  | 35 |
| [`lock_item_slot`](#context-lock_item_slot) | Block |  | 16 |
| [`desc_multiclass`](./Strings.md#string-desc_multiclass) | String |  | 5 |
| `auto_plus_signs_on_name` | Boolean |  | 4 |
| [`name_mod`](./Strings.md#string-name_mod) | String |  | 4 |
| [`tags`](./Arrays.md#array-tags) | Array |  | 3 |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum |  | 2 |
| `shield` | Integer |  | 2 |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | Flat addition to a base value. | 1 |
| [`grant_ability`](./Enums.md#enum-grant_ability) | Enum |  | 1 |

</details>

---

### Context: `passives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 884

> **Referenced by:** [`1`](#context-1), [`10`](#context-10), [`2`](#context-2), [`3`](#context-3), [`4`](#context-4), [`5`](#context-5), [`6`](#context-6), [`7`](#context-7), [`8`](#context-8), [`9`](#context-9), [`PassiveAfterXKills`](#context-passiveafterxkills), [`PassiveAtHealthThreshold`](#context-passiveathealththreshold), [`PassiveAtInjuryThreshold`](#context-passiveatinjurythreshold), [`PassiveAtStatThreshold`](#context-passiveatstatthreshold), [`PassiveWhenAffectedByElement`](#context-passivewhenaffectedbyelement), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`AddStatusToBasicAttack`](#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 80 |
| [`AddPassivesToMinions`](#context-addpassivestominions) | Block | Applies the 'AddPassivesToMinions' effect. | 29 |
| [`StatusOnTookDamage`](#context-statusontookdamage) | Block | Event Trigger: Applies nested statuses when took damage. | 21 |
| [`StatusEachTurnEnd`](#context-statuseachturnend) | Block | Event Trigger: Applies nested statuses to each turn end. | 20 |
| [`StatusOnBattleEnd`](#context-statusonbattleend) | Block | Applies the nested status effects when the encounter finishes. | 16 |
| [`StatusOnKill`](#context-statusonkill) | Block | Event Trigger: Applies nested statuses when kill. | 14 |
| [`StatusEachTurnBegin`](#context-statuseachturnbegin) | Block | Event Trigger: Applies nested statuses to each turn begin. | 12 |
| [`CritsApplyStatus`](#context-critsapplystatus) | Block | Applies the 'CritsApplyStatus' effect. | 10 |
| [`PassiveAtStatThreshold`](#context-passiveatstatthreshold) | Block | Applies the 'PassiveAtStatThreshold' effect. | 10 |
| [`RevengeDamage`](#context-revengedamage) | Block | Reaction trigger: Deals damage to the attacker when hit. | 9 |
| [`MeleeRevengeDamage`](#context-meleerevengedamage) | Block | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. | 8 |
| [`StatusAlliesOnDeath`](#context-statusalliesondeath) | Block | Event Trigger: Applies nested statuses to allies on death. | 7 |
| [`AddStatusToWeapons`](#context-addstatustoweapons) | Block | Applies the 'AddStatusToWeapons' effect. | 6 |
| [`AddStatusToAllDamage`](#context-addstatustoalldamage) | Block | Applies the 'AddStatusToAllDamage' effect. | 5 |
| [`AddStatusToBasicMeleeAttack`](#context-addstatustobasicmeleeattack) | Block | Applies the 'AddStatusToBasicMeleeAttack' effect. | 5 |
| [`StatusOnCastSpell`](#context-statusoncastspell) | Block | Event Trigger: Applies nested statuses when cast spell. | 5 |
| [`AddPassivesToCharmed`](#context-addpassivestocharmed) | Block | Applies the 'AddPassivesToCharmed' effect. | 4 |
| [`AddStatusToElementDamage`](#context-addstatustoelementdamage) | Block | Applies the 'AddStatusToElementDamage' effect. | 4 |
| [`PassiveAtHealthThreshold`](#context-passiveathealththreshold) | Block | Applies the 'PassiveAtHealthThreshold' effect. | 4 |
| [`PassiveWhenAtFullMana`](#context-passivewhenatfullmana) | Block | State Trigger: Grants nested passives when at full mana. | 4 |
| [`StatusIfUnusedMovePoints`](#context-statusifunusedmovepoints) | Block | Event Trigger: Applies nested statuses to if unused move points. | 4 |
| [`AddSelfStatusToBasicAttack`](#context-addselfstatustobasicattack) | Block | Applies the 'AddSelfStatusToBasicAttack' effect. | 3 |
| [`StatusEveryXSpellCasts`](#context-statuseveryxspellcasts) | Block | Event Trigger: Applies nested statuses to every x spell casts. | 3 |
| [`StatusKilledCharacters`](#context-statuskilledcharacters) | Block | Event Trigger: Applies nested statuses to killed characters. | 3 |
| [`StatusOnAllyCatDeath`](#context-statusonallycatdeath) | Block | Event Trigger: Applies nested statuses when ally cat death. | 3 |
| [`StatusOnBattleStart`](#context-statusonbattlestart) | Block | Event Trigger: Applies nested statuses when battle start. | 3 |
| [`StatusOnEatFood`](#context-statusoneatfood) | Block | Event Trigger: Applies nested statuses when eat food. | 3 |
| [`StatusOnGainCoins`](#context-statusongaincoins) | Block | Event Trigger: Applies nested statuses when gain coins. | 3 |
| [`StatusOnHealed`](#context-statusonhealed) | Block | Event Trigger: Applies nested statuses when healed. | 3 |
| [`StatusOnKillEnemy`](#context-statusonkillenemy) | Block | Event Trigger: Applies nested statuses when kill enemy. | 3 |
| [`StatusOnTookDamageFromAbility`](#context-statusontookdamagefromability) | Block | Event Trigger: Applies nested statuses when took damage from ability. | 3 |
| [`AddSelfStatusToWeapons`](#context-addselfstatustoweapons) | Block | Applies the 'AddSelfStatusToWeapons' effect. | 2 |
| [`AddStatusToTrampleDamage`](#context-addstatustotrampledamage) | Block | Applies the 'AddStatusToTrampleDamage' effect. | 2 |
| [`ApplyStatusesToRandomEnemiesEachTurn`](#context-applystatusestorandomenemieseachturn) | Block | Applies the 'ApplyStatusesToRandomEnemiesEachTurn' effect. | 2 |
| [`CatchProjectiles`](#context-catchprojectiles) | Block | Applies the 'CatchProjectiles' effect. | 2 |
| [`ExtraStatusWhenDealingDamage`](#context-extrastatuswhendealingdamage) | Block | Applies the 'ExtraStatusWhenDealingDamage' effect. | 2 |
| [`PassiveAfterXKills`](#context-passiveafterxkills) | Block | Applies the 'PassiveAfterXKills' effect. | 2 |
| [`PassiveWhenAffectedByElement`](#context-passivewhenaffectedbyelement) | Block | State Trigger: Grants nested passives when affected by element. | 2 |
| [`PassiveWhileInMonkMeleeStance`](#context-passivewhileinmonkmeleestance) | Block | Applies the 'PassiveWhileInMonkMeleeStance' effect. | 2 |
| [`StatusAfterCastSpell`](#context-statusaftercastspell) | Block | Event Trigger: Applies nested statuses to after cast spell. | 2 |
| [`StatusAlliesOnBattleStart`](#context-statusalliesonbattlestart) | Block | Event Trigger: Applies nested statuses to allies on battle start. | 2 |
| [`StatusEachTurnEndForEachTurn`](#context-statuseachturnendforeachturn) | Block | Event Trigger: Applies nested statuses to each turn end for each turn. | 2 |
| [`StatusKillers`](#context-statuskillers) | Block | Instantly kills the target if they possess the specified status effects. | 2 |
| [`StatusOnBreakItem`](#context-statusonbreakitem) | Block | Event Trigger: Applies nested statuses when break item. | 2 |
| [`StatusOnCollectPickup`](#context-statusoncollectpickup) | Block | Event Trigger: Applies nested statuses when collect pickup. | 2 |
| [`StatusOnEndMove`](#context-statusonendmove) | Block | Event Trigger: Applies nested statuses when end move. | 2 |
| [`StatusOnPickupCoins`](#context-statusonpickupcoins) | Block | Event Trigger: Applies nested statuses when pickup coins. | 2 |
| [`StatusOnPopCorpse`](#context-statusonpopcorpse) | Block | Event Trigger: Applies nested statuses when pop corpse. | 2 |
| [`StatusOnUseBasicAttack`](#context-statusonusebasicattack) | Block | Event Trigger: Applies nested statuses when use basic attack. | 2 |
| [`StatusWhenAllySpendsMana`](#context-statuswhenallyspendsmana) | Block | Event Trigger: Applies nested statuses to when ally spends mana. | 2 |
| [`AddStatusToKnockbackDamage`](#context-addstatustoknockbackdamage) | Block | Applies the 'AddStatusToKnockbackDamage' effect. | 1 |
| [`AddStatusToSpells`](#context-addstatustospells) | Block | Applies the 'AddStatusToSpells' effect. | 1 |
| [`RandomPassivePool`](#context-randompassivepool) | Block | Applies the 'RandomPassivePool' effect. | 1 |
| [`StatusOnEatPill`](#context-statusoneatpill) | Block | Event Trigger: Applies nested statuses when eat pill. | 1 |

</details>

---

### Context: `stats`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 97

> **Referenced by:** [`1`](#context-1), [`2`](#context-2), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Integer |  | 48 |
| `spd` | Integer |  | 41 |
| `cha` | Integer |  | 33 |
| `int` | Integer |  | 32 |
| `str` | Integer |  | 31 |
| `dex` | Integer |  | 23 |
| `lck` | Integer |  | 21 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 92

> **Referenced by:** [`AddPassivesToCharmed`](#context-addpassivestocharmed), [`AddPassivesToMinions`](#context-addpassivestominions), [`PassiveWhenAtFullMana`](#context-passivewhenatfullmana), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ApplyStatusIfCrit`](#context-applystatusifcrit) | Block | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. | 2 |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`Else`](#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |

</details>

---

### Context: `effects`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 30

> **Referenced by:** [`DamageNeighborsAfterMove`](#context-damageneighborsaftermove), [`DamageNeighborsOnEndMove`](#context-damageneighborsonendmove), [`GravityWell`](#context-gravitywell), [`MeleeRevengeDamage`](#context-meleerevengedamage), [`RevengeDamage`](#context-revengedamage), [`SmiteEnemiesWhoKill`](#context-smiteenemieswhokill), [`fire`](#context-fire), [`ice`](#context-ice), [`lightning`](#context-lightning), [`triattack`](#context-triattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `AddPassivesToMinions`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 29

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`AddStatusToBasicAttack`](#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 5 |
| [`PassiveWhenAffectedByElement`](#context-passivewhenaffectedbyelement) | Block | State Trigger: Grants nested passives when affected by element. | 2 |
| [`StatusOnKill`](#context-statusonkill) | Block | Event Trigger: Applies nested statuses when kill. | 2 |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum |  | 2 |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 21

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Else`](#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 20

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 16

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 10 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 16

> **Referenced by:** [`AddPassivesToMinions`](#context-addpassivestominions), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`TakeBonusTurnWithStatus`](#context-takebonusturnwithstatus) | Block | Grants the character an immediate extra turn while afflicted with specific statuses. | 1 |

</details>

---

### Context: `lock_item_slot`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 16

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum |  | 16 |
| `frame` | Integer |  | 3 |

</details>

---

### Context: `SpawnOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 14

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Enum |  | 14 |
| [`number`](./Arrays.md#array-number) | Integer |  | 13 |

</details>

---

### Context: `StatusOnStanceSwitch`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 14

> **Referenced by:** [`PassiveIfAllArmorEmpty`](#context-passiveifallarmorempty), [`PassiveIfEmptyFace`](#context-passiveifemptyface), [`PassiveIfEmptyHead`](#context-passiveifemptyhead), [`PassiveIfEmptyNeck`](#context-passiveifemptyneck), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `RandomMagicMissile` | Integer | Fires a randomized number of magic missiles. | 6 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | Applies the 'ForceUseAbility' effect. | 2 |
| `NextBasicAttackCritsThisTurn` | Integer | Guarantees the next basic attack executed this turn will be a critical hit. | 2 |
| `RandomStatUp` | Integer | Applies the 'RandomStatUp' effect. | 2 |
| `Shield` | Integer | Applies the 'Shield' effect. | 2 |
| `PartialCleanse` | Integer | Applies the 'PartialCleanse' effect. | 1 |

</details>

---

### Context: `SpreadDisease`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack), [`AddStatusToBasicMeleeAttack`](#context-addstatustobasicmeleeattack), [`MeleeRevengeDamage`](#context-meleerevengedamage), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`disease`](./Enums.md#enum-disease) | Enum | The specific status effect ID representing the disease. | 12 |
| `chance` | Float | Probability (0.0 to 1.0 or percentage) of transmitting. | 11 |
| `can_apply_to_anything` | Boolean |  | 6 |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 11

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack), [`AddStatusToElementAbilities`](#context-addstatustoelementabilities), [`Conditional_SourceHasTag`](#context-conditional_sourcehastag), [`ExtraStatusWhenDealingDamage`](#context-extrastatuswhendealingdamage), [`StatusKilledCharacters`](#context-statuskilledcharacters)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 2 |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |

</details>

---

### Context: `CritsApplyStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 11

> **Referenced by:** [`PassiveIfAllArmorEmpty`](#context-passiveifallarmorempty), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Else`](#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 2 |

</details>

---

### Context: `Temporary`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 11

> **Referenced by:** [`Conditional_BadRoll`](#context-conditional_badroll), [`StatusOnGainShield`](#context-statusongainshield), [`StatusOnTookDamage`](#context-statusontookdamage), [`StatusOnTurnEndIfManaOrHealthExact`](#context-statusonturnendifmanaorhealthexact)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 11 |
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 11 |
| `turns` | Integer | Duration in turns. | 8 |
| `expires_on_end_turn` | Boolean |  | 6 |
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 5 |

</details>

---

### Context: `PassiveAtStatThreshold`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 10

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 10 |
| [`passives`](#context-passives) | Block |  | 10 |
| [`threshold`](#context-threshold) | Block |  | 10 |

</details>

---

### Context: `threshold`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 10

> **Referenced by:** [`PassiveAtStatThreshold`](#context-passiveatstatthreshold)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Integer |  | 6 |
| `cha` | Integer |  | 2 |
| `spd` | Integer |  | 2 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 8 |
| `knockback` | Integer |  | 2 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 7 |
| `damage` | Integer | The base damage properties of an attack. | 4 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 4 |

</details>

---

### Context: `PassiveIfAllArmorEmpty`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AddSpellDamage` | Integer | Applies the 'AddSpellDamage' effect. | 2 |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum | Applies the 'CounterAttack' effect. | 2 |
| `ExtraMovePoints` | Integer | Applies the 'ExtraMovePoints' effect. | 2 |
| `ManaCostReduction` | Integer | Applies the 'ManaCostReduction' effect. | 2 |
| [`StatusOnStanceSwitch`](#context-statusonstanceswitch) | Block | Event Trigger: Applies nested statuses when stance switch. | 2 |
| [`CritsApplyStatus`](#context-critsapplystatus) | Block | Applies the 'CritsApplyStatus' effect. | 1 |
| `Flying` | Integer | Applies the 'Flying' effect. | 1 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`Conditional_Ally`](#context-conditional_ally), [`Conditional_Enemy`](#context-conditional_enemy), [`StatusOnGainCoins`](#context-statusongaincoins), [`StatusOnHealed`](#context-statusonhealed), [`StatusOnTookDamage`](#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`StatusGroup`](#context-statusgroup) | Block | Groups multiple status effects together for batch application. | 3 |

</details>

---

### Context: `StatusOnCrit`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `LuckUp` | Integer | Applies the 'LuckUp' effect. | 3 |
| `DamageUp` | Integer | Combat Trigger: Deals damage to up. | 2 |
| `Shield` | Integer | Applies the 'Shield' effect. | 2 |
| `CritChanceUp` | Integer | Applies the 'CritChanceUp' effect. | 1 |
| `RandomStatUp` | Integer | Applies the 'RandomStatUp' effect. | 1 |

</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack), [`AddStatusToElementAbilities`](#context-addstatustoelementabilities), [`Conditional_NotBoss`](#context-conditional_notboss)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Else`](#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 2 |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 2 |

</details>

---

### Context: `DamageNeighborsOnEndMove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer | The base damage properties of an attack. | 7 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 7 |
| `cant_miss` | Boolean |  | 6 |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 6 |
| `knockback` | Integer |  | 1 |

</details>

---

### Context: `PassiveIfEmptyFace`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AddCritMultiplier` | Integer | Applies the 'AddCritMultiplier' effect. | 2 |
| `CritChanceUp` | Integer | Applies the 'CritChanceUp' effect. | 2 |
| `DodgeChance` | Integer | Applies the 'DodgeChance' effect. | 2 |
| [`StatusOnStanceSwitch`](#context-statusonstanceswitch) | Block | Event Trigger: Applies nested statuses when stance switch. | 2 |
| `KineticSpikes` | Integer | Applies the 'KineticSpikes' effect. | 1 |

</details>

---

### Context: `PassiveIfEmptyHead`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AddCritMultiplier` | Integer | Applies the 'AddCritMultiplier' effect. | 2 |
| `CritChanceUp` | Integer | Applies the 'CritChanceUp' effect. | 2 |
| `DodgeChance` | Integer | Applies the 'DodgeChance' effect. | 2 |
| [`StatusOnStanceSwitch`](#context-statusonstanceswitch) | Block | Event Trigger: Applies nested statuses when stance switch. | 2 |
| `KineticSpikes` | Integer | Applies the 'KineticSpikes' effect. | 1 |

</details>

---

### Context: `PassiveIfEmptyNeck`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AddCritMultiplier` | Integer | Applies the 'AddCritMultiplier' effect. | 2 |
| `CritChanceUp` | Integer | Applies the 'CritChanceUp' effect. | 2 |
| `DodgeChance` | Integer | Applies the 'DodgeChance' effect. | 2 |
| [`StatusOnStanceSwitch`](#context-statusonstanceswitch) | Block | Event Trigger: Applies nested statuses when stance switch. | 2 |
| `KineticSpikes` | Integer | Applies the 'KineticSpikes' effect. | 1 |

</details>

---

### Context: `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `triggers_limit` | Integer |  | 2 |

</details>

---

### Context: `StatusOnUseAbilityWithTag`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 7 |
| `RefreshActPoints` | Integer | Applies the 'RefreshActPoints' effect. | 3 |
| [`Conditional_FirstApplicationThisTurn`](#context-conditional_firstapplicationthisturn) | Block | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 2 |
| `DamageUp` | Integer | Combat Trigger: Deals damage to up. | 2 |
| `exclude_basicattack` | Boolean |  | 2 |
| `HealthGain` | Integer | Applies the 'HealthGain' effect. | 1 |
| `RandomStatUp` | Integer | Applies the 'RandomStatUp' effect. | 1 |

</details>

---

### Context: `AddStatusToElementAbilities`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 6 |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum | Transforms the terrain tile under the target. | 2 |
| [`Conditional_Ally`](#context-conditional_ally) | Block | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 2 |
| [`Conditional_Enemy`](#context-conditional_enemy) | Block | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 2 |
| `Bleed` | Integer | Applies the 'Bleed' effect. | 1 |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `CureDisease`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`StatusOnBattleEnd`](#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Float | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 6 |
| [`disease`](./Enums.md#enum-disease) | Enum |  | 6 |
| `can_apply_to_anything` | Boolean |  | 1 |

</details>

---

### Context: `Else`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack), [`Conditional_Enemy`](#context-conditional_enemy), [`CritsApplyStatus`](#context-critsapplystatus), [`StatusOnTookDamage`](#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `ManaCostReductionTagged`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reduction` | Integer |  | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 6 |

</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Enum |  | 6 |
| [`chance`](./Math_Equations.md) | Equation | The probability (0.0 to 1.0 or percentage) of this effect triggering. (Must be float values) | 5 |
| `number` | Integer |  | 2 |
| `good` | Boolean |  | 1 |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 6 |
| `good` | Boolean |  | 3 |
| `spawn_on_death_hit` | Boolean |  | 2 |
| `consider_all_layers` | Boolean |  | 1 |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`1`](#context-1), [`2`](#context-2)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`[keyword_id]`](./Engine_Statuses.md#all-confirmed-keyword_id-values) | String | A Status or Keyword ID whose tooltip text is defined here. See Engine_Statuses.md for all IDs. |  |
</details>

---

### Context: `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnOverHealed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ForceUseAbility_NonStack`](./Enums.md#enum-forceuseability_nonstack) | Enum | Applies the 'ForceUseAbility_NonStack' effect. | 2 |
| `StrengthUp` | Integer | Applies the 'StrengthUp' effect. | 2 |
| `CurrentWeaponDamageUp` | Integer | Applies the 'CurrentWeaponDamageUp' effect. | 1 |
| `SpawnScaledRotFly` | Integer | Applies the 'SpawnScaledRotFly' effect. | 1 |

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
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 4 |

</details>

---

### Context: `AddPassivesToCharmed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`AddStatusToBasicAttack`](#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 5 |

</details>

---

### Context: `AddStatusToElementDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 4 |

</details>

---

### Context: `AddStatusToExplosions`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](#context-addpassivestominions), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`AddElement`](./Enums.md#enum-addelement) | Enum | Applies the 'AddElement' effect. | 8 |
| `Burn` | Integer | Applies the 'Burn' effect. | 4 |

</details>

---

### Context: `AllyManaRegenAura`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 4 |
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 4 |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 4 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 2 |
| `force_display_name` | Boolean |  | 2 |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`StatusOnKill`](#context-statusonkill), [`StatusOnUseAbilityWithTag`](#context-statusonuseabilitywithtag)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `DistanceBonusDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `min_range` | Integer |  | 4 |
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 4 |

</details>

---

### Context: `EMP`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](#context-addpassivestominions), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`spell_graphics_override`](#context-spell_graphics_override) | Block |  | 4 |
| [`status_explosion_override`](./Enums.md#enum-status_explosion_override) | Enum |  | 4 |

</details>

---

### Context: `PassiveAtHealthThreshold`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 4 |
| [`passives`](#context-passives) | Block |  | 4 |
| `threshold` | Integer |  | 4 |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](#context-addpassivestominions), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 4 |
| [`passives`](#context-passives) | Block |  | 4 |

</details>

---

### Context: `PassiveWhenAtFullMana`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`AddStatusToBasicAttack`](#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 2 |

</details>

---

### Context: `StatusAlliesOnKill`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](#context-addpassivestominions), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AllStatsUp` | Integer | Applies the 'AllStatsUp' effect. | 2 |
| `DamageUp` | Integer | Combat Trigger: Deals damage to up. | 2 |
| `HealthGain` | Integer | Applies the 'HealthGain' effect. | 1 |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnTurnEndIfCastNSpells`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `spells` | Integer |  | 4 |
| `DoubleCastSpell` | Integer | Applies the 'DoubleCastSpell' effect. | 2 |
| `Quivered` | Integer | Applies the 'Quivered' effect. | 2 |
| `MoveQuivered` | Integer | Applies the 'MoveQuivered' effect. | 1 |

</details>

---

### Context: `StatusOnTurnEndIfManaExact`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `mana` | Integer |  | 4 |
| `FreeSpell` | Integer | Applies the 'FreeSpell' effect. | 2 |
| `Quivered` | Integer | Applies the 'Quivered' effect. | 2 |
| `MoveQuivered` | Integer | Applies the 'MoveQuivered' effect. | 1 |
| `SpellDamageUp` | Integer | Applies the 'SpellDamageUp' effect. | 1 |

</details>

---

### Context: `StatusOnTurnEndIfManaOrHealthExact`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `mana` | Integer |  | 4 |
| [`Temporary`](#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 3 |
| `IntelligenceUp` | Integer | Applies the 'IntelligenceUp' effect. | 2 |
| `Shield` | Integer | Applies the 'Shield' effect. | 2 |
| `SpellDamageUp` | Integer | Applies the 'SpellDamageUp' effect. | 2 |
| `DivineShield` | Integer | Applies the 'DivineShield' effect. | 1 |
| `HealthGain` | Integer | Applies the 'HealthGain' effect. | 1 |
| `KineticSpikes` | Integer | Applies the 'KineticSpikes' effect. | 1 |

</details>

---

### Context: `empty_armor_scaled_stats`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`1`](#context-1), [`2`](#context-2)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Integer |  | 2 |
| `int` | Integer |  | 2 |
| `spd` | Integer |  | 2 |

</details>

---

### Context: `spell_graphics_override`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`EMP`](#context-emp)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum |  | 4 |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum |  | 4 |
| `palette` | Integer |  | 4 |
| [`particle`](./Enums.md#enum-particle) | Enum |  | 4 |

</details>

---

### Context: `AddSelfStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Integer | Applies the 'CastAgain' effect. | 2 |
| `Fury` | Integer | Applies the 'Fury' effect. | 1 |

</details>

---

### Context: `AmplifyStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `addstacks` | Integer |  | 3 |
| [`status`](./Enums.md#enum-status) | Enum | The ID of the status effect to check or apply. | 3 |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`StatusEachTurnBegin`](#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`odds`](./Math_Equations.md) | Equation | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. (Must be float values) | 3 |

</details>

---

### Context: `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`CritsApplyStatus`](#context-critsapplystatus), [`StatusOnTookDamage`](#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 3 |

</details>

---

### Context: `DeathRattle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `pop_corpse` | Boolean |  | 2 |

</details>

---

### Context: `ElementalManaCostReduction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Enum | The specific element type required or applied. | 3 |
| `reduction` | Integer |  | 3 |

</details>

---

### Context: `MoveTowardsDamageSource`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 3 |
| `move_far` | Boolean |  | 3 |

</details>

---

### Context: `ObjectOnHitCharacter`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`StatusEachTurnEnd`](#context-statuseachturnend), [`StatusEachTurnEndPerEnemyKill`](#context-statuseachturnendperenemykill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the character to spawn (e.g., CharmedFlea). | 3 |
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 3 |

</details>

---

### Context: `SpawnCatCopyOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 3 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum |  | 3 |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 3 |
| [`object`](./Enums.md#enum-object) | Enum |  | 3 |

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
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 3 |

</details>

---

### Context: `StatusGroup`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`RandomStatusFromPool`](#context-randomstatusfrompool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>
 | `AutoReanimate` | Number | Applies the 'AutoReanimate' effect. | 2 | 
 | [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally) | Block | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 1 | 

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 2 |

</details>

---

### Context: `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `StatusOnKillEnemy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `statuses`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`ChanceToRevive`](#context-chancetorevive), [`StatusOnBattleEndIfKillThresholdMet`](#context-statusonbattleendifkillthresholdmet)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>
 | [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum/String | Generates an item drop from the specified loot pool. | 2 | 
 | `PermanentDexterity` | Number | Applies the 'PermanentDexterity' effect. | 2 | 
 | `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 1 | 
 | `HealthGain` | Number | Applies the 'HealthGain' effect. | 1 | 

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `range` | Integer | Distance or area of effect in tiles. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 2 |

</details>

---

### Context: `AddPassiveToSpawnedRocks`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddFilledMaxHealth` | Integer | Applies the 'AddFilledMaxHealth' effect. | 2 |
| `JoinSpawnerFaction` | Integer | Applies the 'JoinSpawnerFaction' effect. | 2 |

</details>

---

### Context: `AddPassivesToSummonAbilityMinions`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `DamageUp` | Integer | Combat Trigger: Deals damage to up. | 2 |
| `Doomed` | Integer | Applies the 'Doomed' effect. | 2 |
| `MovementUp` | Integer | Applies the 'MovementUp' effect. | 2 |

</details>

---

### Context: `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `AddStatusToAllDamageAbilities`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Bleed` | Integer | Applies the 'Bleed' effect. | 1 |
| `Piercing` | Integer | Applies the 'Piercing' effect. | 1 |
| `Weakness` | Integer | Applies the 'Weakness' effect. | 1 |

</details>

---

### Context: `AddStatusToBasicAttackWithCooldown`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| `CharmedForceAttack` | Integer | Applies the 'CharmedForceAttack' effect. | 2 |

</details>

---

### Context: `AddStatusToFirstBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Charmed` | Integer | Applies the 'Charmed' effect. | 2 |

</details>

---

### Context: `AddStatusToMeleeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`DelayedWind`](#context-delayedwind) | Block | Applies the 'DelayedWind' effect. | 1 |
| [`DelayedWindCone`](#context-delayedwindcone) | Block | Creates a delayed Area of Effect cone. | 1 |

</details>

---

### Context: `AddStatusToTrampleDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `AllyBonusAbilityAura`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `square` | Boolean |  | 2 |

</details>

---

### Context: `AllyHealthRegenAura`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 2 |
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `AlternateCraftingPools`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tinkerer_0`](./Enums.md#enum-tinkerer_0) | Enum |  | 2 |
| [`tinkerer_1`](./Enums.md#enum-tinkerer_1) | Enum |  | 2 |

</details>

---

### Context: `ApplyStatusIfCrit`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack)

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
| `count` | Integer | The numerical quantity. | 1 |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack), [`Conditional_Ally`](#context-conditional_ally)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `BoobyTrapItems`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`on_break`](#context-on_break) | Block |  | 2 |
| [`on_throw`](#context-on_throw) | Block |  | 2 |

</details>

---

### Context: `BoostWeaponDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`crit_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 2 |
| `damage` | Integer | The base damage properties of an attack. | 2 |

</details>

---

### Context: `BouncyProjectiles`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Integer |  | 2 |
| `max_range` | Integer |  | 2 |

</details>

---

### Context: `CatAPultAnimation`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |

</details>

---

### Context: `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `ally_chance` | Integer |  | 2 |
| `chance` | Float | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |
 | `Quivered` | Number | Applies the 'Quivered' effect. | 2 | 
 | `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 1 | 

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `chance` | Float | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 2 |
| `reduction` | Integer |  | 2 |

</details>

---

### Context: `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`StatusKillers`](#context-statuskillers)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`AddStatusToElementDamage`](#context-addstatustoelementdamage)

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

> **Referenced by:** [`AddStatusToAllDamage`](#context-addstatustoalldamage), [`AddStatusToBasicAttack`](#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. | 2 |

</details>

---

### Context: `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`StatusKillers`](#context-statuskillers)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`Conditional_Enemy`](#context-conditional_enemy)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Craft`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`StatusOnTookDamage`](#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 2 |
| [`slot`](./Enums.md#enum-slot) | Enum |  | 2 |

</details>

---

### Context: `DamageNeighborTilesWhenCastSpell`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`fire`](#context-fire) | Block |  | 1 |
| [`ice`](#context-ice) | Block |  | 1 |
| [`lightning`](#context-lightning) | Block |  | 1 |
| [`triattack`](#context-triattack) | Block |  | 1 |

</details>

---

### Context: `DamageNeighborsAfterMove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Enum | The base damage properties of an attack. | 2 |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |

</details>

---

### Context: `DamageReductionAura`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 2 |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 2 |
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `Earth`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Enum | The base damage properties of an attack. | 2 |

</details>

---

### Context: `Electric`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Stun`](./Arrays.md#array-stun) | Array | Applies the 'Stun' effect. | 2 |

</details>

---

### Context: `ElementalAttunement`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Earth`](#context-earth) | Block | Applies the 'Earth' effect. | 2 |
| [`Electric`](#context-electric) | Block | Applies the 'Electric' effect. | 2 |
| [`Fire`](#context-fire) | Block | Applies the 'Fire' effect. | 2 |
| [`Grass`](#context-grass) | Block | Applies the 'Grass' effect. | 2 |
| [`Gravity`](#context-gravity) | Block | Applies the 'Gravity' effect. | 2 |
| [`Holy`](#context-holy) | Block | Applies the 'Holy' effect. | 2 |
| [`Ice`](#context-ice) | Block | Applies the 'Ice' effect. | 2 |
| [`Shadow`](#context-shadow) | Block | Applies the 'Shadow' effect. | 2 |
| [`Water`](#context-water) | Block | Applies the 'Water' effect. | 2 |
| [`Wind`](#context-wind) | Block | Applies the 'Wind' effect. | 2 |

</details>

---

### Context: `EscapeSequence`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| `RandomDistanceDisplace` | Integer | Displaces the target by a randomized distance. | 2 |
| `SafeExplosionIfHitSomething` | Integer | Applies the 'SafeExplosionIfHitSomething' effect. | 2 |

</details>

---

### Context: `Eternal`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `health_percent` | Integer |  | 2 |
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 2 |
| `AllStatsUp` | Integer | Applies the 'AllStatsUp' effect. | 1 |
| `TakeExtraTurn` | Integer | Applies the 'TakeExtraTurn' effect. | 1 |

</details>

---

### Context: `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
</details>

---

### Context: `Fire`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Burn`](./Math_Equations.md) | Enum | Applies the 'Burn' effect. | 2 |

</details>

---

### Context: `Grass`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Poison`](./Math_Equations.md) | Enum | Applies the 'Poison' effect. | 2 |

</details>

---

### Context: `Gravity`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Weakness`](./Math_Equations.md) | Enum | Applies the 'Weakness' effect. | 2 |

</details>

---

### Context: `GravityWell`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean |  | 2 |
| `damage` | Integer | The base damage properties of an attack. | 2 |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |

</details>

---

### Context: `HealAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`PassiveUntilCastSpell`](#context-passiveuntilcastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean |  | 2 |
| `mana` | Integer |  | 2 |
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `Holy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`FlatLeech`](./Math_Equations.md) | Enum | Applies the 'FlatLeech' effect. | 2 |

</details>

---

### Context: `HolyDamageBlessing`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`PassiveUntilGetKill`](#context-passiveuntilgetkill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Burn` | Integer | Applies the 'Burn' effect. | 2 |
| `damage_multiplier` | Integer |  | 2 |

</details>

---

### Context: `Ice`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Slow`](./Math_Equations.md) | Enum | Applies the 'Slow' effect. | 2 |

</details>

---

### Context: `InfiniteRebirth`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| `TempSpeedUp` | Integer | Applies the 'TempSpeedUp' effect. | 2 |
| `health` | Integer |  | 2 |
| `playercat_health` | Integer |  | 2 |

</details>

---

### Context: `LateBloomer`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AllStatsUp` | Integer | Applies the 'AllStatsUp' effect. | 2 |
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `LightningRod`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Tech` | Integer | Applies the 'Tech' effect. | 2 |

</details>

---

### Context: `LowHealthAllyDodgeChanceAura`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Float | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |
| `theshold` | Integer |  | 2 |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `enemies_only` | Boolean |  | 2 |

</details>

---

### Context: `NextBattleStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`StatusOnBattleEnd`](#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AllStatsUp` | Integer | Applies the 'AllStatsUp' effect. | 2 |
| `FullHeal` | Integer | Applies the 'FullHeal' effect. | 2 |

</details>

---

### Context: `PassiveAfterXKills`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block |  | 2 |
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `PassiveAtFullHealth`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `ManaCostReduction` | Integer | Applies the 'ManaCostReduction' effect. | 2 |
| `TakeExtraDamage` | Integer | Applies the 'TakeExtraDamage' effect. | 2 |

</details>

---

### Context: `PassiveAtInjuryThreshold`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`injury`](./Math_Equations.md) | Enum |  | 2 |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 2 |
| [`passives`](#context-passives) | Block |  | 2 |
| `threshold` | Integer |  | 2 |

</details>

---

### Context: `PassiveGroup`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`RandomPassivePool`](#context-randompassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `PassiveUntilCastSpell`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`HealAlliesEachTurn`](#context-healallieseachturn) | Block | Applies the 'HealAlliesEachTurn' effect. | 2 |
| [`StatusAlliesEachTurn`](#context-statusallieseachturn) | Block | Event Trigger: Applies nested statuses to allies each turn. | 1 |

</details>

---

### Context: `PassiveUntilGetKill`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`HolyDamageBlessing`](#context-holydamageblessing) | Block | Applies the 'HolyDamageBlessing' effect. | 2 |

</details>

---

### Context: `PassiveWhenTheAlpha`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TogglableRoundEndExtraTurn` | Integer | Applies the 'TogglableRoundEndExtraTurn' effect. | 2 |

</details>

---

### Context: `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `PassiveWhileInMonkRangedStance`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AddBonusRange` | Integer | Applies the 'AddBonusRange' effect. | 2 |
| `AddSpellDamage` | Integer | Applies the 'AddSpellDamage' effect. | 2 |
| `KineticSpikes` | Integer | Applies the 'KineticSpikes' effect. | 1 |

</details>

---

### Context: `PassiveWhilePreviewingMonkRangedStance`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AddBonusRange` | Integer | Applies the 'AddBonusRange' effect. | 2 |

</details>

---

### Context: `PassiveWhileWearingMetal`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddElementsToWeapon`](./Enums.md#enum-addelementstoweapon) | Enum | Applies the 'AddElementsToWeapon' effect. | 2 |

</details>

---

### Context: `RepressedMemoriesMetronome`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ScaledStatusOnSpendMana`](#context-scaledstatusonspendmana)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 2 |
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `ScaledStatusOnOverMana`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `RandomMagicMissile` | Integer | Fires a randomized number of magic missiles. | 2 |
| `Cleanse` | Integer | Applies the 'Cleanse' effect. | 1 |

</details>

---

### Context: `ScaledStatusOnSpendMana`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`RepressedMemoriesMetronome`](#context-repressedmemoriesmetronome) | Block | Applies the 'RepressedMemoriesMetronome' effect. | 2 |

</details>

---

### Context: `SecurityBotProtect`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |

</details>

---

### Context: `Shadow`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`crit_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 2 |

</details>

---

### Context: `SmiteEnemiesWhoKill`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer | The base damage properties of an attack. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |

</details>

---

### Context: `SpecialFriends`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AllStatsUp` | Integer | Applies the 'AllStatsUp' effect. | 2 |
| `HealthGain` | Integer | Applies the 'HealthGain' effect. | 2 |

</details>

---

### Context: `StatsAtLowHealth`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `threshold` | Integer |  | 2 |
| `speed` | Float |  | 1 |
| `strength` | Integer |  | 1 |

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

### Context: `StatusAlliesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusAlliesOnGainCoins`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `HealthGain` | Integer | Applies the 'HealthGain' effect. | 2 |
| `LuckUp` | Integer | Applies the 'LuckUp' effect. | 2 |
| `scaled` | Boolean |  | 1 |

</details>

---

### Context: `StatusAllyWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AllStatsUp` | Integer | Applies the 'AllStatsUp' effect. | 2 |
| `threshold` | Integer |  | 2 |

</details>

---

### Context: `StatusAnyCatAllyWhoKills`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AlphaCat` | Integer | Applies the 'AlphaCat' effect. | 2 |

</details>

---

### Context: `StatusDamagers`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `LuckUp` | Integer | Applies the 'LuckUp' effect. | 2 |
| [`Fear`](./Arrays.md#array-fear) | Array | Applies the 'Fear' effect. | 1 |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusEachTurnEndPerEnemyKill`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ObjectOnHitCharacter`](#context-objectonhitcharacter) | Block | Spawns a specific character or entity upon impact. | 2 |

</details>

---

### Context: `StatusEnemiesOnDeath`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AllStatsUp` | Integer | Applies the 'AllStatsUp' effect. | 2 |
| `Freeze` | Integer | Applies the 'Freeze' effect. | 2 |

</details>

---

### Context: `StatusEveryXTurnBegins`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `DivineShield` | Integer | Applies the 'DivineShield' effect. | 2 |
| `turns` | Integer | The duration of the effect in turns. | 2 |

</details>

---

### Context: `StatusKillers`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>
 | [`Conditional_Boss`](./Passives_and_Statuses.md#context-conditional_boss) | Block | Conditional trigger: Executes nested logic if the target is a Boss. | 2 | 
 | [`Conditional_NotBoss`](./Passives_and_Statuses.md#context-conditional_notboss) | Block | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 2 | 

---

### Context: `StatusOnAnyDeath`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `LuckUp` | Integer | Applies the 'LuckUp' effect. | 2 |

</details>

---

### Context: `StatusOnBattleEndIfKillThresholdMet`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `kills` | Integer |  | 2 |
| [`statuses`](#context-statuses) | Block |  | 2 |

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

### Context: `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnDealtDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `TempDexterityUp` | Integer | Applies the 'TempDexterityUp' effect. | 2 |
| `TempStrengthUp` | Integer | Applies the 'TempStrengthUp' effect. | 2 |
| `TempLuckUp` | Integer | Applies the 'TempLuckUp' effect. | 1 |

</details>

---

### Context: `StatusOnDealtDamageThreshold`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `RefreshMovePoints` | Integer | Applies the 'RefreshMovePoints' effect. | 2 |
| `Shield` | Integer | Applies the 'Shield' effect. | 2 |
| `count_overkill` | Boolean |  | 2 |
| `ignore_during_movement` | Boolean |  | 2 |
| `threshold` | Integer |  | 2 |
| `AllStatsUp` | Integer | Applies the 'AllStatsUp' effect. | 1 |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnGainShield`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Temporary`](#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 2 |

</details>

---

### Context: `StatusOnHeal`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `SpeedUp` | Integer | Applies the 'SpeedUp' effect. | 2 |
| `RandomStatUp` | Integer | Applies the 'RandomStatUp' effect. | 1 |

</details>

---

### Context: `StatusOnOverMana`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `IntelligenceUp` | Integer | Applies the 'IntelligenceUp' effect. | 2 |
| `SpellDamageUp` | Integer | Applies the 'SpellDamageUp' effect. | 2 |
| `DivineShield` | Integer | Applies the 'DivineShield' effect. | 1 |

</details>

---

### Context: `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnTookDamageFromEnemyAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Quivered` | Integer | Applies the 'Quivered' effect. | 2 |
| `MoveQuivered` | Integer | Applies the 'MoveQuivered' effect. | 1 |

</details>

---

### Context: `StatusOnTriggerTrap`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `DexterityUp` | Integer | Applies the 'DexterityUp' effect. | 2 |
| `Quivered` | Integer | Applies the 'Quivered' effect. | 1 |

</details>

---

### Context: `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusOnUseElementAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `SpeedUp` | Integer | Applies the 'SpeedUp' effect. | 2 |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 2 |

</details>

---

### Context: `StatusPerInjury`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Shield` | Integer | Applies the 'Shield' effect. | 2 |
| `cap` | Integer |  | 2 |
| [`injury`](./Math_Equations.md) | Enum |  | 2 |
| `StrengthUp` | Integer | Applies the 'StrengthUp' effect. | 1 |

</details>

---

### Context: `StatusThingsKnockedBack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Drag` | Integer | Applies the 'Drag' effect. | 2 |

</details>

---

### Context: `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `TaggedPickupEffectReplacement`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`HealthGain`](./Math_Equations.md) | Enum | Applies the 'HealthGain' effect. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 2 |

</details>

---

### Context: `TowerDefense`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer | The base damage properties of an attack. | 2 |
| `range` | Integer | Distance or area of effect in tiles. | 2 |

</details>

---

### Context: `Water`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AOEPuddle`](./Math_Equations.md) | Enum | Applies the 'AOEPuddle' effect. | 2 |

</details>

---

### Context: `Wind`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`knockback`](./Math_Equations.md) | Enum |  | 2 |

</details>

---

### Context: `on_break`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`BoobyTrapItems`](#context-boobytrapitems)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SafeExplosionIfHitSomething` | Integer | Applies the 'SafeExplosionIfHitSomething' effect. | 2 |

</details>

---

### Context: `on_throw`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`BoobyTrapItems`](#context-boobytrapitems)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| `HitExplosion` | Integer | Applies the 'HitExplosion' effect. | 2 |

</details>

---

### Context: `schadenfreude_scaled_stats`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`1`](#context-1), [`2`](#context-2)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Integer |  | 2 |
| `str` | Integer |  | 2 |
| `cha` | Integer |  | 1 |
| `dex` | Integer |  | 1 |
| `int` | Integer |  | 1 |
| `lck` | Integer |  | 1 |
| `spd` | Integer |  | 1 |

</details>

---

### Context: `AbilityChargeRefundChance`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `advantage_softcap` | Float |  | 1 |
| `chance` | Float | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 1 |

</details>

---

### Context: `AbilityReaction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 1 |
| `ability_damage_only` | Boolean |  | 1 |
| `chance` | Float | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 1 |

</details>

---

### Context: `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `AddStatusToReceivedDamage_ExcludeStatuses`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_DoesDamage`](#context-conditional_doesdamage) | Block | Conditional block: Executes nested logic only if the target is/has DoesDamage. | 1 |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `AddStatusesIfPersistentWeatherElement`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Burn` | Integer | Applies the 'Burn' effect. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |

</details>

---

### Context: `AddStatusesToReceivedElementalDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Burn` | Integer | Applies the 'Burn' effect. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |

</details>

---

### Context: `AddTemporaryEffectsToEquipment`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Integer | Applies the 'CastAgain' effect. | 1 |

</details>

---

### Context: `Autism`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `innate` | Integer |  | 1 |
| `learned` | Integer |  | 1 |

</details>

---

### Context: `AutocastEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 1 |
| `advantage_polarity` | Integer |  | 1 |
| `chance` | Float | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 1 |

</details>

---

### Context: `ChanceToRevive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 1 |
| [`statuses`](#context-statuses) | Block |  | 1 |

</details>

---

### Context: `ChangeTile`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `aoe` | Integer | The area of effect or distance in tiles. | 1 |
| [`tile`](./Enums.md#enum-tile) | Enum | The specific tile type to change into (e.g., GlassTile). | 1 |

</details>

---

### Context: `CollectPickupsOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `pop_corpses` | Boolean |  | 1 |

</details>

---

### Context: `Conditional_DoesDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AddStatusToReceivedDamage_ExcludeStatuses`](#context-addstatustoreceiveddamage_excludestatuses)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Bleed`](./Arrays.md#array-bleed) | Array | Applies the 'Bleed' effect. | 1 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusEachTurnBegin`](#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `odds` | Float | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 1 |

</details>

---

### Context: `Conditional_SourceHasTag`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 1 |

</details>

---

### Context: `DamageIfDidntUseSpecificAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 1 |
| `damage` | Integer | The base damage properties of an attack. | 1 |

</details>

---

### Context: `DelayedWind`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AddStatusToMeleeDamage`](#context-addstatustomeleedamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Integer | The area of effect or distance in tiles. | 1 |

</details>

---

### Context: `DelayedWindCone`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AddStatusToMeleeDamage`](#context-addstatustomeleedamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Integer | The area of effect or distance in tiles. | 1 |

</details>

---

### Context: `Diabetes`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `AllStatsUp` | Integer | Applies the 'AllStatsUp' effect. | 1 |
| `Confusion` | Integer | Applies the 'Confusion' effect. | 1 |

</details>

---

### Context: `EnergyStorm`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Integer |  | 1 |
| `period` | Integer |  | 1 |

</details>

---

### Context: `FindItemFromPool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Math_Equations.md) | Equation | Probability of finding the item. (Must be float values) | 1 |
| [`pool`](./Enums.md#enum-pool) | Enum | The item pool to draw from. | 1 |

</details>

---

### Context: `ForceMoveAway`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusAdjacentOnTheirTurnBegin`](#context-statusadjacentontheirturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `free` | Boolean |  | 1 |

</details>

---

### Context: `ForceUseAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusEachTurnBegin`](#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 3 |
| [`chance`](./Math_Equations.md) | Equation | The probability (0.0 to 1.0 or percentage) of this effect triggering. (Must be float values) | 3 |

</details>

---

### Context: `FurnitureStats`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Appeal` | Integer | Applies the 'Appeal' effect. | 1 |
| `Comfort` | Integer | Applies the 'Comfort' effect. | 1 |
| `Stimulation` | Integer | Applies the 'Stimulation' effect. | 1 |

</details>

---

### Context: `MegaMinions`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Integer |  | 1 |
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 1 |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 1 |

</details>

---

### Context: `PassiveLevelScaledStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Shield`](./Math_Equations.md) | String | Applies the 'Shield' effect. | 1 |
| [`SizeScalePercent`](./Math_Equations.md) | String | Applies the 'SizeScalePercent' effect. | 1 |
| [`Trample`](./Arrays.md#array-trample) | Array | Applies the 'Trample' effect. | 1 |

</details>

---

### Context: `RandomPassivePool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`PassiveGroup`](#context-passivegroup) | Block | Applies the 'PassiveGroup' effect. | 2 |

</details>

---

### Context: `ReplaceBrain`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

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

### Context: `ScaledStatusOnBleedDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Charge` | Integer | Applies the 'Charge' effect. | 1 |

</details>

---

### Context: `ScaledStatusOnLoseShield`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Thorns` | Integer | Applies the 'Thorns' effect. | 1 |

</details>

---

### Context: `ScaledStatusOnOverHealed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnScaledRotFly` | Integer | Applies the 'SpawnScaledRotFly' effect. | 1 |

</details>

---

### Context: `SelfDamageWhenDealDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer | The base damage properties of an attack. | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Context: `StackingDodgeChanceOnTookDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `amount` | Float | The numerical quantity. | 1 |
| `cap` | Integer |  | 1 |

</details>

---

### Context: `StatusAdjacentOnTheirTurnBegin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`ForceMoveAway`](#context-forcemoveaway) | Block | Applies the 'ForceMoveAway' effect. | 1 |

</details>

---

### Context: `StatusAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`PassiveUntilCastSpell`](#context-passiveuntilcastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `exclude_self` | Boolean |  | 1 |

</details>

---

### Context: `StatusAlliesOnSpendMana`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `ManaGain` | Integer | Applies the 'ManaGain' effect. | 1 |

</details>

---

### Context: `StatusAlliesScaledByCursedOnDeath`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `LuckUp` | Integer | Applies the 'LuckUp' effect. | 1 |

</details>

---

### Context: `StatusIfBattleAlreadyBegan`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `PermanentMadness` | Integer | Applies the 'PermanentMadness' effect. | 1 |

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

### Context: `StatusOnLoseShield`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Thorns` | Integer | Applies the 'Thorns' effect. | 1 |

</details>

---

### Context: `StatusOnTakeHealthDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `PermanentConstitution` | Integer | Applies the 'PermanentConstitution' effect. | 1 |

</details>

---

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `ManaGain` | Integer | Applies the 'ManaGain' effect. | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Context: `StrengthInNumbersAura`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count_self` | Boolean |  | 1 |
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 1 |

</details>

---

### Context: `Study`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `marked` | Integer |  | 1 |
| `stacks` | Integer | The number of stacks, duration, or intensity to apply. | 1 |

</details>

---

### Context: `TakeBonusTurnWithStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusOnKill`](#context-statusonkill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `TheHunger`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Madness` | Integer | Applies the Madness debuff/status effect. | 1 |

</details>

---

### Context: `TileDamageMultiplier`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ally_multiplier` | Integer |  | 1 |
| `multiplier` | Integer | Multiplicative modifier to a base value. | 1 |

</details>

---

### Context: `TourettesMeows`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cooldown`](./Arrays.md#array-cooldown) | Array |  | 1 |
| [`pool`](./Arrays.md#array-pool) | Array |  | 1 |

</details>

---

### Context: `fire`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer | The base damage properties of an attack. | 1 |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Context: `ice`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer | The base damage properties of an attack. | 1 |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Context: `lightning`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer | The base damage properties of an attack. | 1 |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Context: `triattack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer | The base damage properties of an attack. | 1 |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Numerical Contexts

> The following contexts are numeric keys or array indices.

### Context: `2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 372

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the passive's display description. | 372 |
| [`passives`](#context-passives) | Block |  | 369 |
| [`stats`](#context-stats) | Block |  | 36 |
| [`desc_multiclass`](./Strings.md#string-desc_multiclass) | String |  | 5 |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum |  | 4 |
| `shield` | Integer |  | 4 |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | Flat addition to a base value. | 3 |
| `divine_shield` | Integer |  | 3 |
| [`keyword_tooltips`](#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear when hovering over the ability. | 3 |
| [`empty_armor_scaled_stats`](#context-empty_armor_scaled_stats) | Block |  | 2 |
| [`icon`](./Enums.md#enum-icon) | String |  | 1 |
| [`schadenfreude_scaled_stats`](#context-schadenfreude_scaled_stats) | Block |  | 1 |

</details>

---

### Context: `1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 368

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block |  | 368 |
| [`stats`](#context-stats) | Block |  | 26 |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | Flat addition to a base value. | 4 |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum |  | 4 |
| `divine_shield` | Integer |  | 3 |
| [`keyword_tooltips`](#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear when hovering over the ability. | 3 |
| `shield` | Integer |  | 3 |
| [`empty_armor_scaled_stats`](#context-empty_armor_scaled_stats) | Block |  | 2 |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the passive's display description. | 1 |
| [`schadenfreude_scaled_stats`](#context-schadenfreude_scaled_stats) | Block |  | 1 |

</details>

---

### Context: `3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block |  | 2 |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the passive's display description. | 1 |
| [`icon`](./Enums.md#enum-icon) | String |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the passive's display name. | 1 |

</details>

---

### Context: `10`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the passive's display description. | 1 |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

### Context: `4`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

### Context: `5`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

### Context: `6`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

### Context: `7`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

### Context: `8`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

### Context: `9`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block |  | 1 |

</details>

---

