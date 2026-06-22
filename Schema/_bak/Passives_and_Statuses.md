# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Passives & Statuses

> **Associated Files:** `data/passives/, data/passive_pools.gon`


### Context: `ROOT` (511 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`name`](./Strings.md#string-name) | String | Localization key for the passive's display name. | 511 |
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 510 |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the passive's display description. | 510 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 116 |
| [`stats`](./Passives_and_Statuses.md#context-stats) | Block |  | 35 |
| [`lock_item_slot`](./Passives_and_Statuses.md#context-lock_item_slot) | Block |  | 16 |
| [`desc_multiclass`](./Strings.md#string-desc_multiclass) | String |  | 5 |
| `auto_plus_signs_on_name` | Boolean |  | 4 |
| [`name_mod`](./Strings.md#string-name_mod) | String |  | 4 |
| [`tags`](./Arrays.md#array-tags) | Array |  | 3 |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum |  | 2 |
| `shield` | Number |  | 2 |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | Flat addition to a base value. | 1 |
| [`grant_ability`](./Enums.md#enum-grant_ability) | Enum |  | 1 |

</details>

---

### Context: `passives` (884 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Passives_and_Statuses.md#context-1), [`10`](./Passives_and_Statuses.md#context-10), [`2`](./Passives_and_Statuses.md#context-2), [`3`](./Passives_and_Statuses.md#context-3), [`4`](./Passives_and_Statuses.md#context-4), [`5`](./Passives_and_Statuses.md#context-5), [`6`](./Passives_and_Statuses.md#context-6), [`7`](./Passives_and_Statuses.md#context-7), [`8`](./Passives_and_Statuses.md#context-8), [`9`](./Passives_and_Statuses.md#context-9), [`PassiveAfterXKills`](./Passives_and_Statuses.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#context-passiveathealththreshold), [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#context-passiveatinjurythreshold), [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold), [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement), [`ROOT`](./Passives_and_Statuses.md#context-root)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 80 |
| [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions) | Block | Applies the 'AddPassivesToMinions' effect. | 29 |
| [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage) | Block | Event Trigger: Applies nested statuses when took damage. | 21 |
| [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend) | Block | Event Trigger: Applies nested statuses to each turn end. | 20 |
| [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend) | Block | Applies the nested status effects when the encounter finishes. | 16 |
| [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill) | Block | Event Trigger: Applies nested statuses when kill. | 14 |
| [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin) | Block | Event Trigger: Applies nested statuses to each turn begin. | 12 |
| [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus) | Block | Applies the 'CritsApplyStatus' effect. | 10 |
| [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold) | Block | Applies the 'PassiveAtStatThreshold' effect. | 10 |
| [`RevengeDamage`](./Passives_and_Statuses.md#context-revengedamage) | Block | Reaction trigger: Deals damage to the attacker when hit. | 9 |
| [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage) | Block | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. | 8 |
| [`StatusAlliesOnDeath`](./Passives_and_Statuses.md#context-statusalliesondeath) | Block | Event Trigger: Applies nested statuses to allies on death. | 7 |
| [`AddStatusToWeapons`](./Passives_and_Statuses.md#context-addstatustoweapons) | Block | Applies the 'AddStatusToWeapons' effect. | 6 |
| [`AddStatusToAllDamage`](./Passives_and_Statuses.md#context-addstatustoalldamage) | Block | Applies the 'AddStatusToAllDamage' effect. | 5 |
| [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack) | Block | Applies the 'AddStatusToBasicMeleeAttack' effect. | 5 |
| [`StatusOnCastSpell`](./Passives_and_Statuses.md#context-statusoncastspell) | Block | Event Trigger: Applies nested statuses when cast spell. | 5 |
| [`AddPassivesToCharmed`](./Passives_and_Statuses.md#context-addpassivestocharmed) | Block | Applies the 'AddPassivesToCharmed' effect. | 4 |
| [`AddStatusToElementDamage`](./Passives_and_Statuses.md#context-addstatustoelementdamage) | Block | Applies the 'AddStatusToElementDamage' effect. | 4 |
| [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#context-passiveathealththreshold) | Block | Applies the 'PassiveAtHealthThreshold' effect. | 4 |
| [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#context-passivewhenatfullmana) | Block | State Trigger: Grants nested passives when at full mana. | 4 |
| [`StatusIfUnusedMovePoints`](./Passives_and_Statuses.md#context-statusifunusedmovepoints) | Block | Event Trigger: Applies nested statuses to if unused move points. | 4 |
| [`AddSelfStatusToBasicAttack`](./Passives_and_Statuses.md#context-addselfstatustobasicattack) | Block | Applies the 'AddSelfStatusToBasicAttack' effect. | 3 |
| [`StatusEveryXSpellCasts`](./Passives_and_Statuses.md#context-statuseveryxspellcasts) | Block | Event Trigger: Applies nested statuses to every x spell casts. | 3 |
| [`StatusKilledCharacters`](./Passives_and_Statuses.md#context-statuskilledcharacters) | Block | Event Trigger: Applies nested statuses to killed characters. | 3 |
| [`StatusOnAllyCatDeath`](./Passives_and_Statuses.md#context-statusonallycatdeath) | Block | Event Trigger: Applies nested statuses when ally cat death. | 3 |
| [`StatusOnBattleStart`](./Passives_and_Statuses.md#context-statusonbattlestart) | Block | Event Trigger: Applies nested statuses when battle start. | 3 |
| [`StatusOnEatFood`](./Passives_and_Statuses.md#context-statusoneatfood) | Block | Event Trigger: Applies nested statuses when eat food. | 3 |
| [`StatusOnGainCoins`](./Passives_and_Statuses.md#context-statusongaincoins) | Block | Event Trigger: Applies nested statuses when gain coins. | 3 |
| [`StatusOnHealed`](./Passives_and_Statuses.md#context-statusonhealed) | Block | Event Trigger: Applies nested statuses when healed. | 3 |
| [`StatusOnKillEnemy`](./Passives_and_Statuses.md#context-statusonkillenemy) | Block | Event Trigger: Applies nested statuses when kill enemy. | 3 |
| [`StatusOnTookDamageFromAbility`](./Passives_and_Statuses.md#context-statusontookdamagefromability) | Block | Event Trigger: Applies nested statuses when took damage from ability. | 3 |
| [`AddSelfStatusToWeapons`](./Passives_and_Statuses.md#context-addselfstatustoweapons) | Block | Applies the 'AddSelfStatusToWeapons' effect. | 2 |
| [`AddStatusToTrampleDamage`](./Passives_and_Statuses.md#context-addstatustotrampledamage) | Block | Applies the 'AddStatusToTrampleDamage' effect. | 2 |
| [`ApplyStatusesToRandomEnemiesEachTurn`](./Passives_and_Statuses.md#context-applystatusestorandomenemieseachturn) | Block | Applies the 'ApplyStatusesToRandomEnemiesEachTurn' effect. | 2 |
| [`CatchProjectiles`](./Passives_and_Statuses.md#context-catchprojectiles) | Block | Applies the 'CatchProjectiles' effect. | 2 |
| [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#context-extrastatuswhendealingdamage) | Block | Applies the 'ExtraStatusWhenDealingDamage' effect. | 2 |
| [`PassiveAfterXKills`](./Passives_and_Statuses.md#context-passiveafterxkills) | Block | Applies the 'PassiveAfterXKills' effect. | 2 |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement) | Block | State Trigger: Grants nested passives when affected by element. | 2 |
| [`PassiveWhileInMonkMeleeStance`](./Passives_and_Statuses.md#context-passivewhileinmonkmeleestance) | Block | Applies the 'PassiveWhileInMonkMeleeStance' effect. | 2 |
| [`StatusAfterCastSpell`](./Passives_and_Statuses.md#context-statusaftercastspell) | Block | Event Trigger: Applies nested statuses to after cast spell. | 2 |
| [`StatusAlliesOnBattleStart`](./Passives_and_Statuses.md#context-statusalliesonbattlestart) | Block | Event Trigger: Applies nested statuses to allies on battle start. | 2 |
| [`StatusEachTurnEndForEachTurn`](./Passives_and_Statuses.md#context-statuseachturnendforeachturn) | Block | Event Trigger: Applies nested statuses to each turn end for each turn. | 2 |
| [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers) | Block | Instantly kills the target if they possess the specified status effects. | 2 |
| [`StatusOnBreakItem`](./Passives_and_Statuses.md#context-statusonbreakitem) | Block | Event Trigger: Applies nested statuses when break item. | 2 |
| [`StatusOnCollectPickup`](./Passives_and_Statuses.md#context-statusoncollectpickup) | Block | Event Trigger: Applies nested statuses when collect pickup. | 2 |
| [`StatusOnEndMove`](./Passives_and_Statuses.md#context-statusonendmove) | Block | Event Trigger: Applies nested statuses when end move. | 2 |
| [`StatusOnPickupCoins`](./Passives_and_Statuses.md#context-statusonpickupcoins) | Block | Event Trigger: Applies nested statuses when pickup coins. | 2 |
| [`StatusOnPopCorpse`](./Passives_and_Statuses.md#context-statusonpopcorpse) | Block | Event Trigger: Applies nested statuses when pop corpse. | 2 |
| [`StatusOnUseBasicAttack`](./Passives_and_Statuses.md#context-statusonusebasicattack) | Block | Event Trigger: Applies nested statuses when use basic attack. | 2 |
| [`StatusWhenAllySpendsMana`](./Passives_and_Statuses.md#context-statuswhenallyspendsmana) | Block | Event Trigger: Applies nested statuses to when ally spends mana. | 2 |
| [`AddStatusToKnockbackDamage`](./Passives_and_Statuses.md#context-addstatustoknockbackdamage) | Block | Applies the 'AddStatusToKnockbackDamage' effect. | 1 |
| [`AddStatusToSpells`](./Passives_and_Statuses.md#context-addstatustospells) | Block | Applies the 'AddStatusToSpells' effect. | 1 |
| [`RandomPassivePool`](./Passives_and_Statuses.md#context-randompassivepool) | Block | Applies the 'RandomPassivePool' effect. | 1 |
| [`StatusOnEatPill`](./Passives_and_Statuses.md#context-statusoneatpill) | Block | Event Trigger: Applies nested statuses when eat pill. | 1 |

</details>

---

### Context: `stats` (97 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Passives_and_Statuses.md#context-1), [`2`](./Passives_and_Statuses.md#context-2), [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
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

### Context: `AddStatusToBasicAttack` (92 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToCharmed`](./Passives_and_Statuses.md#context-addpassivestocharmed), [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#context-passivewhenatfullmana), [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`ApplyStatusIfCrit`](./Passives_and_Statuses.md#context-applystatusifcrit) | Block | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. | 2 |
| [`ApplyToSource`](./Passives_and_Statuses.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`Else`](./Passives_and_Statuses.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |

</details>

---

### Context: `effects` (30 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#context-damageneighborsaftermove), [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#context-damageneighborsonendmove), [`GravityWell`](./Passives_and_Statuses.md#context-gravitywell), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`RevengeDamage`](./Passives_and_Statuses.md#context-revengedamage), [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#context-smiteenemieswhokill), [`fire`](./Passives_and_Statuses.md#context-fire), [`ice`](./Passives_and_Statuses.md#context-ice), [`lightning`](./Passives_and_Statuses.md#context-lightning), [`triattack`](./Passives_and_Statuses.md#context-triattack)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `AddPassivesToMinions` (29 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 5 |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement) | Block | State Trigger: Grants nested passives when affected by element. | 2 |
| [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill) | Block | Event Trigger: Applies nested statuses when kill. | 2 |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum |  | 2 |

</details>

---

### Context: `StatusOnTookDamage` (21 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`Else`](./Passives_and_Statuses.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `StatusEachTurnEnd` (20 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnBattleEnd` (16 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 10 |

</details>

---

### Context: `StatusOnKill` (16 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`TakeBonusTurnWithStatus`](./Passives_and_Statuses.md#context-takebonusturnwithstatus) | Block | Grants the character an immediate extra turn while afflicted with specific statuses. | 1 |

</details>

---

### Context: `lock_item_slot` (16 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum |  | 16 |
| `frame` | Number |  | 3 |

</details>

---

### Context: `SpawnOnBattleStart` (14 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array |  | 14 |
| [`number`](./Arrays.md#array-number) | Array |  | 13 |

</details>

---

### Context: `StatusOnStanceSwitch` (14 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#context-passiveifemptyface), [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#context-passiveifemptyhead), [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#context-passiveifemptyneck), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. | 6 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | Applies the 'ForceUseAbility' effect. | 2 |
| `NextBasicAttackCritsThisTurn` | Number | Guarantees the next basic attack executed this turn will be a critical hit. | 2 |
| `RandomStatUp` | Number | Applies the 'RandomStatUp' effect. | 2 |
| `Shield` | Number | Applies the 'Shield' effect. | 2 |
| `PartialCleanse` | Number | Applies the 'PartialCleanse' effect. | 1 |

</details>

---

### Context: `SpreadDisease` (12 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`effects`](./Passives_and_Statuses.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`disease`](./Enums.md#enum-disease) | Enum | The specific status effect ID representing the disease. | 12 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of transmitting. | 11 |
| `can_apply_to_anything` | Boolean |  | 6 |

</details>

---

### Context: `StatusEachTurnBegin` (12 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |

</details>

---

### Context: `Conditional_Ally` (11 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#context-conditional_sourcehastag), [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#context-extrastatuswhendealingdamage), [`StatusKilledCharacters`](./Passives_and_Statuses.md#context-statuskilledcharacters)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 2 |
| [`ApplyToSource`](./Passives_and_Statuses.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |

</details>

---

### Context: `CritsApplyStatus` (11 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`Else`](./Passives_and_Statuses.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 2 |

</details>

---

### Context: `Temporary` (11 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_BadRoll`](./Passives_and_Statuses.md#context-conditional_badroll), [`StatusOnGainShield`](./Passives_and_Statuses.md#context-statusongainshield), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage), [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#context-statusonturnendifmanaorhealthexact)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 11 |
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 11 |
| `turns` | Number | Duration in turns. | 8 |
| `expires_on_end_turn` | Boolean |  | 6 |
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 5 |

</details>

---

### Context: `PassiveAtStatThreshold` (10 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 10 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 10 |
| [`threshold`](./Passives_and_Statuses.md#context-threshold) | Block |  | 10 |

</details>

---

### Context: `threshold` (10 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 6 |
| `cha` | Number |  | 2 |
| `spd` | Number |  | 2 |

</details>

---

### Context: `RevengeDamage` (9 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 8 |
| `knockback` | Number |  | 2 |

</details>

---

### Context: `MeleeRevengeDamage` (8 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 7 |
| `damage` | Number | The base damage properties of an attack. | 4 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 4 |

</details>

---

### Context: `PassiveIfAllArmorEmpty` (8 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddSpellDamage` | Number | Applies the 'AddSpellDamage' effect. | 2 |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum | Applies the 'CounterAttack' effect. | 2 |
| `ExtraMovePoints` | Number | Applies the 'ExtraMovePoints' effect. | 2 |
| `ManaCostReduction` | Number | Applies the 'ManaCostReduction' effect. | 2 |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch) | Block | Event Trigger: Applies nested statuses when stance switch. | 2 |
| [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus) | Block | Applies the 'CritsApplyStatus' effect. | 1 |
| `Flying` | Number | Applies the 'Flying' effect. | 1 |

</details>

---

### Context: `RandomStatusFromPool` (8 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`StatusOnGainCoins`](./Passives_and_Statuses.md#context-statusongaincoins), [`StatusOnHealed`](./Passives_and_Statuses.md#context-statusonhealed), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`StatusGroup`](./Passives_and_Statuses.md#context-statusgroup) | Block | Groups multiple status effects together for batch application. | 3 |

</details>

---

### Context: `StatusOnCrit` (8 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | Applies the 'LuckUp' effect. | 3 |
| `DamageUp` | Number | Combat Trigger: Deals damage to up. | 2 |
| `Shield` | Number | Applies the 'Shield' effect. | 2 |
| `CritChanceUp` | Number | Applies the 'CritChanceUp' effect. | 1 |
| `RandomStatUp` | Number | Applies the 'RandomStatUp' effect. | 1 |

</details>

---

### Context: `Conditional_Enemy` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_NotBoss`](./Passives_and_Statuses.md#context-conditional_notboss)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`Else`](./Passives_and_Statuses.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 2 |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 2 |

</details>

---

### Context: `DamageNeighborsOnEndMove` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 7 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 7 |
| `cant_miss` | Boolean |  | 6 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 6 |
| `knockback` | Number |  | 1 |

</details>

---

### Context: `PassiveIfEmptyFace` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | Applies the 'AddCritMultiplier' effect. | 2 |
| `CritChanceUp` | Number | Applies the 'CritChanceUp' effect. | 2 |
| `DodgeChance` | Number | Applies the 'DodgeChance' effect. | 2 |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch) | Block | Event Trigger: Applies nested statuses when stance switch. | 2 |
| `KineticSpikes` | Number | Applies the 'KineticSpikes' effect. | 1 |

</details>

---

### Context: `PassiveIfEmptyHead` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | Applies the 'AddCritMultiplier' effect. | 2 |
| `CritChanceUp` | Number | Applies the 'CritChanceUp' effect. | 2 |
| `DodgeChance` | Number | Applies the 'DodgeChance' effect. | 2 |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch) | Block | Event Trigger: Applies nested statuses when stance switch. | 2 |
| `KineticSpikes` | Number | Applies the 'KineticSpikes' effect. | 1 |

</details>

---

### Context: `PassiveIfEmptyNeck` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | Applies the 'AddCritMultiplier' effect. | 2 |
| `CritChanceUp` | Number | Applies the 'CritChanceUp' effect. | 2 |
| `DodgeChance` | Number | Applies the 'DodgeChance' effect. | 2 |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch) | Block | Event Trigger: Applies nested statuses when stance switch. | 2 |
| `KineticSpikes` | Number | Applies the 'KineticSpikes' effect. | 1 |

</details>

---

### Context: `StatusAlliesOnDeath` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| `triggers_limit` | Number |  | 2 |

</details>

---

### Context: `StatusOnUseAbilityWithTag` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 7 |
| `RefreshActPoints` | Number | Applies the 'RefreshActPoints' effect. | 3 |
| [`Conditional_FirstApplicationThisTurn`](./Passives_and_Statuses.md#context-conditional_firstapplicationthisturn) | Block | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 2 |
| `DamageUp` | Number | Combat Trigger: Deals damage to up. | 2 |
| `exclude_basicattack` | Boolean |  | 2 |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 1 |
| `RandomStatUp` | Number | Applies the 'RandomStatUp' effect. | 1 |

</details>

---

### Context: `AddStatusToElementAbilities` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 6 |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum | Transforms the terrain tile under the target. | 2 |
| [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally) | Block | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 2 |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy) | Block | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 2 |
| `Bleed` | Number | Applies the 'Bleed' effect. | 1 |

</details>

---

### Context: `AddStatusToWeapons` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `CureDisease` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 6 |
| [`disease`](./Enums.md#enum-disease) | Enum |  | 6 |
| `can_apply_to_anything` | Boolean |  | 1 |

</details>

---

### Context: `Else` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `ManaCostReductionTagged` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reduction` | Number |  | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 6 |

</details>

---

### Context: `SpawnEachTurn` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array |  | 6 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 5 |
| `number` | Number |  | 2 |
| `good` | Boolean |  | 1 |

</details>

---

### Context: `SpawnThingOnDamage` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 6 |
| `good` | Boolean |  | 3 |
| `spawn_on_death_hit` | Boolean |  | 2 |
| `consider_all_layers` | Boolean |  | 1 |

</details>

---

### Context: `keyword_tooltips` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Passives_and_Statuses.md#context-1), [`2`](./Passives_and_Statuses.md#context-2)

> **Engine Schema:** This block is a `[keyword_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[keyword_id]`](./Engine_Statuses.md#all-confirmed-keyword-id-values) | String | A Status or Keyword ID whose tooltip text is defined here. See Engine_Statuses.md for all IDs. |

</details>

---

### Context: `AddStatusToAllDamage` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |

</details>

---

### Context: `AddStatusToBasicMeleeAttack` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnCastSpell` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnOverHealed` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility_NonStack`](./Enums.md#enum-forceuseability_nonstack) | Enum | Applies the 'ForceUseAbility_NonStack' effect. | 2 |
| `StrengthUp` | Number | Applies the 'StrengthUp' effect. | 2 |
| `CurrentWeaponDamageUp` | Number | Applies the 'CurrentWeaponDamageUp' effect. | 1 |
| `SpawnScaledRotFly` | Number | Applies the 'SpawnScaledRotFly' effect. | 1 |

</details>

---

### Context: `AddDamageToElementDamage` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 4 |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 4 |

</details>

---

### Context: `AddPassivesToCharmed` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 5 |

</details>

---

### Context: `AddStatusToElementDamage` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 4 |

</details>

---

### Context: `AddStatusToExplosions` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddElement`](./Enums.md#enum-addelement) | Enum | Applies the 'AddElement' effect. | 8 |
| `Burn` | Number | Applies the 'Burn' effect. | 4 |

</details>

---

### Context: `AllyManaRegenAura` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 4 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 4 |

</details>

---

### Context: `AutocastEachRound` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 4 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 2 |
| `force_display_name` | Boolean |  | 2 |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill), [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#context-statusonuseabilitywithtag)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `DistanceBonusDamage` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `min_range` | Number |  | 4 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 4 |

</details>

---

### Context: `EMP` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`spell_graphics_override`](./Passives_and_Statuses.md#context-spell_graphics_override) | Block |  | 4 |
| [`status_explosion_override`](./Enums.md#enum-status_explosion_override) | Enum |  | 4 |

</details>

---

### Context: `PassiveAtHealthThreshold` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 4 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 4 |
| `threshold` | Number |  | 4 |

</details>

---

### Context: `PassiveWhenAffectedByElement` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 4 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 4 |

</details>

---

### Context: `PassiveWhenAtFullMana` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 2 |

</details>

---

### Context: `StatusAlliesOnKill` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `DamageUp` | Number | Combat Trigger: Deals damage to up. | 2 |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 1 |

</details>

---

### Context: `StatusIfUnusedMovePoints` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnTurnEndIfCastNSpells` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spells` | Number |  | 4 |
| `DoubleCastSpell` | Number | Applies the 'DoubleCastSpell' effect. | 2 |
| `Quivered` | Number | Applies the 'Quivered' effect. | 2 |
| `MoveQuivered` | Number | Applies the 'MoveQuivered' effect. | 1 |

</details>

---

### Context: `StatusOnTurnEndIfManaExact` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `mana` | Number |  | 4 |
| `FreeSpell` | Number | Applies the 'FreeSpell' effect. | 2 |
| `Quivered` | Number | Applies the 'Quivered' effect. | 2 |
| `MoveQuivered` | Number | Applies the 'MoveQuivered' effect. | 1 |
| `SpellDamageUp` | Number | Applies the 'SpellDamageUp' effect. | 1 |

</details>

---

### Context: `StatusOnTurnEndIfManaOrHealthExact` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
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

### Context: `empty_armor_scaled_stats` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Passives_and_Statuses.md#context-1), [`2`](./Passives_and_Statuses.md#context-2)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 2 |
| `int` | Number |  | 2 |
| `spd` | Number |  | 2 |

</details>

---

### Context: `spell_graphics_override` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`EMP`](./Passives_and_Statuses.md#context-emp)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum |  | 4 |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum |  | 4 |
| `palette` | Number |  | 4 |
| [`particle`](./Enums.md#enum-particle) | Enum |  | 4 |

</details>

---

### Context: `AddSelfStatusToBasicAttack` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | Applies the 'CastAgain' effect. | 2 |
| `Fury` | Number | Applies the 'Fury' effect. | 1 |

</details>

---

### Context: `AmplifyStatus` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `addstacks` | Number |  | 3 |
| [`status`](./Enums.md#enum-status) | Enum | The ID of the status effect to check or apply. | 3 |

</details>

---

### Context: `Conditional_BadRoll` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`odds`](./Enums.md#enum-odds) | Enum | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 3 |

</details>

---

### Context: `Conditional_HasStatus` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 3 |

</details>

---

### Context: `DeathRattle` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `pop_corpse` | Boolean |  | 2 |

</details>

---

### Context: `ElementalManaCostReduction` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array | The specific element type required or applied. | 3 |
| `reduction` | Number |  | 3 |

</details>

---

### Context: `MoveTowardsDamageSource` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 3 |
| `move_far` | Boolean |  | 3 |

</details>

---

### Context: `ObjectOnHitCharacter` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend), [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#context-statuseachturnendperenemykill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the character to spawn (e.g., CharmedFlea). | 3 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 3 |

</details>

---

### Context: `SpawnCatCopyOnBattleStart` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 3 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum |  | 3 |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 3 |
| [`object`](./Enums.md#enum-object) | Enum |  | 3 |

</details>

---

### Context: `StatusEveryXSpellCasts` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 3 |

</details>

---

### Context: `StatusGroup` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusKilledCharacters` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |

</details>

---

### Context: `StatusOnAllyCatDeath` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnBattleStart` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnEatFood` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnGainCoins` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 2 |

</details>

---

### Context: `StatusOnHealed` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `StatusOnKillEnemy` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnTookDamageFromAbility` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `statuses` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChanceToRevive`](./Passives_and_Statuses.md#context-chancetorevive), [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#context-statusonbattleendifkillthresholdmet)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `range` | Number | Distance or area of effect in tiles. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 2 |

</details>

---

### Context: `AddPassiveToSpawnedRocks` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddFilledMaxHealth` | Number | Applies the 'AddFilledMaxHealth' effect. | 2 |
| `JoinSpawnerFaction` | Number | Applies the 'JoinSpawnerFaction' effect. | 2 |

</details>

---

### Context: `AddPassivesToSummonAbilityMinions` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | Combat Trigger: Deals damage to up. | 2 |
| `Doomed` | Number | Applies the 'Doomed' effect. | 2 |
| `MovementUp` | Number | Applies the 'MovementUp' effect. | 2 |

</details>

---

### Context: `AddSelfStatusToWeapons` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `AddStatusToAllDamageAbilities` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | Applies the 'Bleed' effect. | 1 |
| `Piercing` | Number | Applies the 'Piercing' effect. | 1 |
| `Weakness` | Number | Applies the 'Weakness' effect. | 1 |

</details>

---

### Context: `AddStatusToBasicAttackWithCooldown` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CharmedForceAttack` | Number | Applies the 'CharmedForceAttack' effect. | 2 |

</details>

---

### Context: `AddStatusToFirstBasicAttack` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | Applies the 'Charmed' effect. | 2 |

</details>

---

### Context: `AddStatusToMeleeDamage` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DelayedWind`](./Passives_and_Statuses.md#context-delayedwind) | Block | Applies the 'DelayedWind' effect. | 1 |
| [`DelayedWindCone`](./Passives_and_Statuses.md#context-delayedwindcone) | Block | Creates a delayed Area of Effect cone. | 1 |

</details>

---

### Context: `AddStatusToTrampleDamage` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `AllyBonusAbilityAura` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `square` | Boolean |  | 2 |

</details>

---

### Context: `AllyHealthRegenAura` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `AlternateCraftingPools` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tinkerer_0`](./Enums.md#enum-tinkerer_0) | Enum |  | 2 |
| [`tinkerer_1`](./Enums.md#enum-tinkerer_1) | Enum |  | 2 |

</details>

---

### Context: `ApplyStatusIfCrit` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `ApplyStatusesToRandomEnemiesEachTurn` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| `count` | Number | The numerical quantity. | 1 |

</details>

---

### Context: `ApplyToSource` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `BoobyTrapItems` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`on_break`](./Passives_and_Statuses.md#context-on_break) | Block |  | 2 |
| [`on_throw`](./Passives_and_Statuses.md#context-on_throw) | Block |  | 2 |

</details>

---

### Context: `BoostWeaponDamage` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`crit_chance`](./Enums.md#enum-crit_chance) | Enum |  | 2 |
| `damage` | Number | The base damage properties of an attack. | 2 |

</details>

---

### Context: `BouncyProjectiles` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number |  | 2 |
| `max_range` | Number |  | 2 |

</details>

---

### Context: `CatAPultAnimation` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |

</details>

---

### Context: `CatchProjectiles` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| `ally_chance` | Number |  | 2 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |

</details>

---

### Context: `ChanceToBackflip` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |

</details>

---

### Context: `ClassManaCostReduction` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 2 |
| `reduction` | Number |  | 2 |

</details>

---

### Context: `Conditional_Adjacent` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_Boss` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_Corpse` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToElementDamage`](./Passives_and_Statuses.md#context-addstatustoelementdamage)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_HasTag` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Passives_and_Statuses.md#context-addstatustoalldamage), [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. | 2 |

</details>

---

### Context: `Conditional_NotBoss` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |

</details>

---

### Context: `Conditional_PartyMember` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_Shielded` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Craft` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 2 |
| [`slot`](./Enums.md#enum-slot) | Enum |  | 2 |

</details>

---

### Context: `DamageNeighborTilesWhenCastSpell` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`fire`](./Passives_and_Statuses.md#context-fire) | Block |  | 1 |
| [`ice`](./Passives_and_Statuses.md#context-ice) | Block |  | 1 |
| [`lightning`](./Passives_and_Statuses.md#context-lightning) | Block |  | 1 |
| [`triattack`](./Passives_and_Statuses.md#context-triattack) | Block |  | 1 |

</details>

---

### Context: `DamageNeighborsAfterMove` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Equation | The base damage properties of an attack. | 2 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |

</details>

---

### Context: `DamageReductionAura` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 2 |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `Earth` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Equation | The base damage properties of an attack. | 2 |

</details>

---

### Context: `Electric` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Stun`](./Arrays.md#array-stun) | Array | Applies the 'Stun' effect. | 2 |

</details>

---

### Context: `ElementalAttunement` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
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

### Context: `EscapeSequence` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomDistanceDisplace` | Number | Displaces the target by a randomized distance. | 2 |
| `SafeExplosionIfHitSomething` | Number | Applies the 'SafeExplosionIfHitSomething' effect. | 2 |

</details>

---

### Context: `Eternal` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health_percent` | Number |  | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 1 |
| `TakeExtraTurn` | Number | Applies the 'TakeExtraTurn' effect. | 1 |

</details>

---

### Context: `ExtraStatusWhenDealingDamage` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |

</details>

---

### Context: `Fire` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Burn`](./Math_Equations.md) | Equation | Applies the 'Burn' effect. | 2 |

</details>

---

### Context: `Grass` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Poison`](./Math_Equations.md) | Equation | Applies the 'Poison' effect. | 2 |

</details>

---

### Context: `Gravity` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Weakness`](./Math_Equations.md) | Equation | Applies the 'Weakness' effect. | 2 |

</details>

---

### Context: `GravityWell` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean |  | 2 |
| `damage` | Number | The base damage properties of an attack. | 2 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |

</details>

---

### Context: `HealAlliesEachTurn` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean |  | 2 |
| `mana` | Number |  | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `Holy` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`FlatLeech`](./Math_Equations.md) | Equation | Applies the 'FlatLeech' effect. | 2 |

</details>

---

### Context: `HolyDamageBlessing` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilGetKill`](./Passives_and_Statuses.md#context-passiveuntilgetkill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | Applies the 'Burn' effect. | 2 |
| `damage_multiplier` | Number |  | 2 |

</details>

---

### Context: `Ice` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Slow`](./Math_Equations.md) | Equation | Applies the 'Slow' effect. | 2 |

</details>

---

### Context: `InfiniteRebirth` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempSpeedUp` | Number | Applies the 'TempSpeedUp' effect. | 2 |
| `health` | Number |  | 2 |
| `playercat_health` | Number |  | 2 |

</details>

---

### Context: `LateBloomer` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `LightningRod` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | Applies the 'Tech' effect. | 2 |

</details>

---

### Context: `LowHealthAllyDodgeChanceAura` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |
| `theshold` | Number |  | 2 |

</details>

---

### Context: `MovementReaction` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `enemies_only` | Boolean |  | 2 |

</details>

---

### Context: `NextBattleStatus` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `FullHeal` | Number | Applies the 'FullHeal' effect. | 2 |

</details>

---

### Context: `PassiveAfterXKills` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `PassiveAtFullHealth` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ManaCostReduction` | Number | Applies the 'ManaCostReduction' effect. | 2 |
| `TakeExtraDamage` | Number | Applies the 'TakeExtraDamage' effect. | 2 |

</details>

---

### Context: `PassiveAtInjuryThreshold` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`injury`](./Math_Equations.md) | Equation |  | 2 |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 2 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 2 |
| `threshold` | Number |  | 2 |

</details>

---

### Context: `PassiveGroup` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Passives_and_Statuses.md#context-randompassivepool)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |

</details>

---

### Context: `PassiveUntilCastSpell` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`HealAlliesEachTurn`](./Passives_and_Statuses.md#context-healallieseachturn) | Block | Applies the 'HealAlliesEachTurn' effect. | 2 |
| [`StatusAlliesEachTurn`](./Passives_and_Statuses.md#context-statusallieseachturn) | Block | Event Trigger: Applies nested statuses to allies each turn. | 1 |

</details>

---

### Context: `PassiveUntilGetKill` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`HolyDamageBlessing`](./Passives_and_Statuses.md#context-holydamageblessing) | Block | Applies the 'HolyDamageBlessing' effect. | 2 |

</details>

---

### Context: `PassiveWhenTheAlpha` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TogglableRoundEndExtraTurn` | Number | Applies the 'TogglableRoundEndExtraTurn' effect. | 2 |

</details>

---

### Context: `PassiveWhileInMonkMeleeStance` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |

</details>

---

### Context: `PassiveWhileInMonkRangedStance` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddBonusRange` | Number | Applies the 'AddBonusRange' effect. | 2 |
| `AddSpellDamage` | Number | Applies the 'AddSpellDamage' effect. | 2 |
| `KineticSpikes` | Number | Applies the 'KineticSpikes' effect. | 1 |

</details>

---

### Context: `PassiveWhilePreviewingMonkRangedStance` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddBonusRange` | Number | Applies the 'AddBonusRange' effect. | 2 |

</details>

---

### Context: `PassiveWhileWearingMetal` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddElementsToWeapon`](./Enums.md#enum-addelementstoweapon) | Enum | Applies the 'AddElementsToWeapon' effect. | 2 |

</details>

---

### Context: `RepressedMemoriesMetronome` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#context-scaledstatusonspendmana)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Context: `ScaledStatusOnOverMana` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. | 2 |
| `Cleanse` | Number | Applies the 'Cleanse' effect. | 1 |

</details>

---

### Context: `ScaledStatusOnSpendMana` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RepressedMemoriesMetronome`](./Passives_and_Statuses.md#context-repressedmemoriesmetronome) | Block | Applies the 'RepressedMemoriesMetronome' effect. | 2 |

</details>

---

### Context: `SecurityBotProtect` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |

</details>

---

### Context: `Shadow` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`crit_chance`](./Math_Equations.md) | Equation |  | 2 |

</details>

---

### Context: `SmiteEnemiesWhoKill` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |

</details>

---

### Context: `SpecialFriends` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 2 |

</details>

---

### Context: `StatsAtLowHealth` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `threshold` | Number |  | 2 |
| `speed` | Number |  | 1 |
| `strength` | Number |  | 1 |

</details>

---

### Context: `StatusAfterCastSpell` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusAlliesOnBattleStart` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusAlliesOnGainCoins` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | Applies the 'HealthGain' effect. | 2 |
| `LuckUp` | Number | Applies the 'LuckUp' effect. | 2 |
| `scaled` | Boolean |  | 1 |

</details>

---

### Context: `StatusAllyWhenAllySpendsMana` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `threshold` | Number |  | 2 |

</details>

---

### Context: `StatusAnyCatAllyWhoKills` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AlphaCat` | Number | Applies the 'AlphaCat' effect. | 2 |

</details>

---

### Context: `StatusDamagers` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | Applies the 'LuckUp' effect. | 2 |
| [`Fear`](./Arrays.md#array-fear) | Array | Applies the 'Fear' effect. | 1 |

</details>

---

### Context: `StatusEachTurnEndForEachTurn` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusEachTurnEndPerEnemyKill` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#context-objectonhitcharacter) | Block | Spawns a specific character or entity upon impact. | 2 |

</details>

---

### Context: `StatusEnemiesOnDeath` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 2 |
| `Freeze` | Number | Applies the 'Freeze' effect. | 2 |

</details>

---

### Context: `StatusEveryXTurnBegins` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | Applies the 'DivineShield' effect. | 2 |
| `turns` | Number | The duration of the effect in turns. | 2 |

</details>

---

### Context: `StatusKillers` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |

</details>

---

### Context: `StatusOnAnyDeath` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | Applies the 'LuckUp' effect. | 2 |

</details>

---

### Context: `StatusOnBattleEndIfKillThresholdMet` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `kills` | Number |  | 2 |
| [`statuses`](./Passives_and_Statuses.md#context-statuses) | Block |  | 2 |

</details>

---

### Context: `StatusOnBreakItem` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnCollectPickup` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnDealtDamage` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempDexterityUp` | Number | Applies the 'TempDexterityUp' effect. | 2 |
| `TempStrengthUp` | Number | Applies the 'TempStrengthUp' effect. | 2 |
| `TempLuckUp` | Number | Applies the 'TempLuckUp' effect. | 1 |

</details>

---

### Context: `StatusOnDealtDamageThreshold` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RefreshMovePoints` | Number | Applies the 'RefreshMovePoints' effect. | 2 |
| `Shield` | Number | Applies the 'Shield' effect. | 2 |
| `count_overkill` | Boolean |  | 2 |
| `ignore_during_movement` | Boolean |  | 2 |
| `threshold` | Number |  | 2 |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 1 |

</details>

---

### Context: `StatusOnEndMove` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnGainShield` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Temporary`](./Passives_and_Statuses.md#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 2 |

</details>

---

### Context: `StatusOnHeal` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | Applies the 'SpeedUp' effect. | 2 |
| `RandomStatUp` | Number | Applies the 'RandomStatUp' effect. | 1 |

</details>

---

### Context: `StatusOnOverMana` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `IntelligenceUp` | Number | Applies the 'IntelligenceUp' effect. | 2 |
| `SpellDamageUp` | Number | Applies the 'SpellDamageUp' effect. | 2 |
| `DivineShield` | Number | Applies the 'DivineShield' effect. | 1 |

</details>

---

### Context: `StatusOnPickupCoins` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnPopCorpse` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnTookDamageFromEnemyAbility` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | Applies the 'Quivered' effect. | 2 |
| `MoveQuivered` | Number | Applies the 'MoveQuivered' effect. | 1 |

</details>

---

### Context: `StatusOnTriggerTrap` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DexterityUp` | Number | Applies the 'DexterityUp' effect. | 2 |
| `Quivered` | Number | Applies the 'Quivered' effect. | 1 |

</details>

---

### Context: `StatusOnUseBasicAttack` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnUseElementAbility` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | Applies the 'SpeedUp' effect. | 2 |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 2 |

</details>

---

### Context: `StatusPerInjury` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | Applies the 'Shield' effect. | 2 |
| `cap` | Number |  | 2 |
| [`injury`](./Math_Equations.md) | Equation |  | 2 |
| `StrengthUp` | Number | Applies the 'StrengthUp' effect. | 1 |

</details>

---

### Context: `StatusThingsKnockedBack` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Drag` | Number | Applies the 'Drag' effect. | 2 |

</details>

---

### Context: `StatusWhenAllySpendsMana` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `TaggedPickupEffectReplacement` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`HealthGain`](./Math_Equations.md) | Equation | Applies the 'HealthGain' effect. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 2 |

</details>

---

### Context: `TowerDefense` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 2 |
| `range` | Number | Distance or area of effect in tiles. | 2 |

</details>

---

### Context: `Water` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AOEPuddle`](./Math_Equations.md) | Equation | Applies the 'AOEPuddle' effect. | 2 |

</details>

---

### Context: `Wind` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`knockback`](./Math_Equations.md) | Equation |  | 2 |

</details>

---

### Context: `on_break` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SafeExplosionIfHitSomething` | Number | Applies the 'SafeExplosionIfHitSomething' effect. | 2 |

</details>

---

### Context: `on_throw` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HitExplosion` | Number | Applies the 'HitExplosion' effect. | 2 |

</details>

---

### Context: `schadenfreude_scaled_stats` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Passives_and_Statuses.md#context-1), [`2`](./Passives_and_Statuses.md#context-2)

| Property Key | Type | Definition | Count |
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

### Context: `AbilityChargeRefundChance` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `advantage_softcap` | Number |  | 1 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 1 |

</details>

---

### Context: `AbilityReaction` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 1 |
| `ability_damage_only` | Boolean |  | 1 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 1 |

</details>

---

### Context: `AddStatusToKnockbackDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `AddStatusToReceivedDamage_ExcludeStatuses` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_DoesDamage`](./Passives_and_Statuses.md#context-conditional_doesdamage) | Block | Conditional block: Executes nested logic only if the target is/has DoesDamage. | 1 |

</details>

---

### Context: `AddStatusToSpells` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `AddStatusesIfPersistentWeatherElement` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | Applies the 'Burn' effect. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |

</details>

---

### Context: `AddStatusesToReceivedElementalDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | Applies the 'Burn' effect. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |

</details>

---

### Context: `AddTemporaryEffectsToEquipment` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | Applies the 'CastAgain' effect. | 1 |

</details>

---

### Context: `Autism` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `innate` | Number |  | 1 |
| `learned` | Number |  | 1 |

</details>

---

### Context: `AutocastEachTurnBegin` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 1 |
| `advantage_polarity` | Number |  | 1 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 1 |

</details>

---

### Context: `ChanceToRevive` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 1 |
| [`statuses`](./Passives_and_Statuses.md#context-statuses) | Block |  | 1 |

</details>

---

### Context: `ChangeTile` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `aoe` | Number | The area of effect or distance in tiles. | 1 |
| [`tile`](./Enums.md#enum-tile) | Enum | The specific tile type to change into (e.g., GlassTile). | 1 |

</details>

---

### Context: `CollectPickupsOnBattleEnd` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `pop_corpses` | Boolean |  | 1 |

</details>

---

### Context: `Conditional_DoesDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage_ExcludeStatuses`](./Passives_and_Statuses.md#context-addstatustoreceiveddamage_excludestatuses)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Bleed`](./Arrays.md#array-bleed) | Array | Applies the 'Bleed' effect. | 1 |

</details>

---

### Context: `Conditional_GoodRoll` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 1 |

</details>

---

### Context: `Conditional_SourceHasTag` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 1 |

</details>

---

### Context: `DamageIfDidntUseSpecificAbility` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 1 |
| `damage` | Number | The base damage properties of an attack. | 1 |

</details>

---

### Context: `DelayedWind` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | The area of effect or distance in tiles. | 1 |

</details>

---

### Context: `DelayedWindCone` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | The area of effect or distance in tiles. | 1 |

</details>

---

### Context: `Diabetes` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies the 'AllStatsUp' effect. | 1 |
| `Confusion` | Number | Applies the 'Confusion' effect. | 1 |

</details>

---

### Context: `EnergyStorm` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number |  | 1 |
| `period` | Number |  | 1 |

</details>

---

### Context: `FindItemFromPool` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability of finding the item. | 1 |
| [`pool`](./Enums.md#enum-pool) | Enum | The item pool to draw from. | 1 |

</details>

---

### Context: `ForceMoveAway` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusAdjacentOnTheirTurnBegin`](./Passives_and_Statuses.md#context-statusadjacentontheirturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `free` | Boolean |  | 1 |

</details>

---

### Context: `ForceUseAbility` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 3 |
| [`chance`](./Enums.md#enum-chance) | Enum | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 3 |

</details>

---

### Context: `FurnitureStats` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Appeal` | Number | Applies the 'Appeal' effect. | 1 |
| `Comfort` | Number | Applies the 'Comfort' effect. | 1 |
| `Stimulation` | Number | Applies the 'Stimulation' effect. | 1 |

</details>

---

### Context: `MegaMinions` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number |  | 1 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 1 |

</details>

---

### Context: `MoveWhenDamaged` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 1 |

</details>

---

### Context: `PassiveLevelScaledStatus` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Shield`](./Math_Equations.md) | Equation | Applies the 'Shield' effect. | 1 |
| [`SizeScalePercent`](./Math_Equations.md) | Equation | Applies the 'SizeScalePercent' effect. | 1 |
| [`Trample`](./Arrays.md#array-trample) | Array | Applies the 'Trample' effect. | 1 |

</details>

---

### Context: `RandomPassivePool` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`PassiveGroup`](./Passives_and_Statuses.md#context-passivegroup) | Block | Applies the 'PassiveGroup' effect. | 2 |

</details>

---

### Context: `ReplaceBrain` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `Robot` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean |  | 1 |

</details>

---

### Context: `ScaledStatusOnBleedDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | Applies the 'Charge' effect. | 1 |

</details>

---

### Context: `ScaledStatusOnLoseShield` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | Applies the 'Thorns' effect. | 1 |

</details>

---

### Context: `ScaledStatusOnOverHealed` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnScaledRotFly` | Number | Applies the 'SpawnScaledRotFly' effect. | 1 |

</details>

---

### Context: `SelfDamageWhenDealDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Context: `StackingDodgeChanceOnTookDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `amount` | Number | The numerical quantity. | 1 |
| `cap` | Number |  | 1 |

</details>

---

### Context: `StatusAdjacentOnTheirTurnBegin` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceMoveAway`](./Passives_and_Statuses.md#context-forcemoveaway) | Block | Applies the 'ForceMoveAway' effect. | 1 |

</details>

---

### Context: `StatusAlliesEachTurn` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| `exclude_self` | Boolean |  | 1 |

</details>

---

### Context: `StatusAlliesOnSpendMana` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | Applies the 'ManaGain' effect. | 1 |

</details>

---

### Context: `StatusAlliesScaledByCursedOnDeath` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | Applies the 'LuckUp' effect. | 1 |

</details>

---

### Context: `StatusIfBattleAlreadyBegan` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PermanentMadness` | Number | Applies the 'PermanentMadness' effect. | 1 |

</details>

---

### Context: `StatusOnEatPill` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnLoseShield` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | Applies the 'Thorns' effect. | 1 |

</details>

---

### Context: `StatusOnTakeHealthDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PermanentConstitution` | Number | Applies the 'PermanentConstitution' effect. | 1 |

</details>

---

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | Applies the 'ManaGain' effect. | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Context: `StrengthInNumbersAura` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count_self` | Boolean |  | 1 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 1 |

</details>

---

### Context: `Study` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `marked` | Number |  | 1 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 1 |

</details>

---

### Context: `TakeBonusTurnWithStatus` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `TheHunger` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | Applies the Madness debuff/status effect. | 1 |

</details>

---

### Context: `TileDamageMultiplier` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ally_multiplier` | Number |  | 1 |
| `multiplier` | Number | Multiplicative modifier to a base value. | 1 |

</details>

---

### Context: `TourettesMeows` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cooldown`](./Arrays.md#array-cooldown) | Array |  | 1 |
| [`pool`](./Arrays.md#array-pool) | Array |  | 1 |

</details>

---

### Context: `fire` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Context: `ice` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Context: `lightning` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Context: `triattack` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Passives_and_Statuses.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Numerical Contexts

> The following contexts are numeric keys or array indices.


### Context: `2` (372 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the passive's display description. | 372 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 369 |
| [`stats`](./Passives_and_Statuses.md#context-stats) | Block |  | 36 |
| [`desc_multiclass`](./Strings.md#string-desc_multiclass) | String |  | 5 |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum |  | 4 |
| `shield` | Number |  | 4 |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | Flat addition to a base value. | 3 |
| `divine_shield` | Number |  | 3 |
| [`keyword_tooltips`](./Passives_and_Statuses.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear when hovering over the ability. | 3 |
| [`empty_armor_scaled_stats`](./Passives_and_Statuses.md#context-empty_armor_scaled_stats) | Block |  | 2 |
| [`icon`](./Enums.md#enum-icon) | Enum |  | 1 |
| [`schadenfreude_scaled_stats`](./Passives_and_Statuses.md#context-schadenfreude_scaled_stats) | Block |  | 1 |

</details>

---

### Context: `1` (368 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 368 |
| [`stats`](./Passives_and_Statuses.md#context-stats) | Block |  | 26 |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | Flat addition to a base value. | 4 |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum |  | 4 |
| `divine_shield` | Number |  | 3 |
| [`keyword_tooltips`](./Passives_and_Statuses.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear when hovering over the ability. | 3 |
| `shield` | Number |  | 3 |
| [`empty_armor_scaled_stats`](./Passives_and_Statuses.md#context-empty_armor_scaled_stats) | Block |  | 2 |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the passive's display description. | 1 |
| [`schadenfreude_scaled_stats`](./Passives_and_Statuses.md#context-schadenfreude_scaled_stats) | Block |  | 1 |

</details>

---

### Context: `3` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 2 |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the passive's display description. | 1 |
| [`icon`](./Enums.md#enum-icon) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the passive's display name. | 1 |

</details>

---

### Context: `10` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the passive's display description. | 1 |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `4` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `5` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `6` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `7` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `8` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 1 |

</details>

---

### Context: `9` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#context-passives) | Block |  | 1 |

</details>

---

