# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Passives & Statuses

> **Associated Files:** `data/passives/, data/passive_pools.gon`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 885

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the passive's display description. | 5441 |
| [`name`](./Strings.md#string-name) | String | Localization key for the passive's display name. | 5027 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1570 |
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 1200 |
| [`stats`](./Passives_and_Statuses.md#context-stats) | Object |  | 982 |
| `cha` | Number |  | 468 |
| `spd` | Number |  | 424 |
| `shield` | Number |  | 422 |
| `con` | Number |  | 416 |
| `int` | Number |  | 401 |
| `lck` | Number |  | 351 |
| `str` | Number |  | 337 |
| `dex` | Number |  | 301 |
| [`keyword_tooltips`](./Passives_and_Statuses.md#context-keyword_tooltips) | Object | Examples: `{ ... }` | 62 |
| `divine_shield` | Number | Examples: `3, 1` | 54 |
| [`lock_item_slot`](./Passives_and_Statuses.md#context-lock_item_slot) | Object |  | 32 |
| [`name_mod`](./Strings.md#string-name_mod) | String |  | 22 |
| [`desc_multiclass`](./Strings.md#string-desc_multiclass) | String |  | 20 |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum |  | 20 |
| `auto_plus_signs_on_name` | Boolean |  | 8 |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | Flat addition to a base value. | 8 |
| [`empty_armor_scaled_stats`](./Passives_and_Statuses.md#context-empty_armor_scaled_stats) | Object | Examples: `{ ... }` | 8 |
| [`tags`](./Arrays.md#array-tags) | Array |  | 8 |
| [`icon`](./Enums.md#enum-icon) | Enum | Examples: `DejaVu3, DejaVu2` | 4 |
| [`schadenfreude_scaled_stats`](./Passives_and_Statuses.md#context-schadenfreude_scaled_stats) | Object | Examples: `{ ... }` | 4 |
| [`grant_ability`](./Enums.md#enum-grant_ability) | Enum |  | 2 |

</details>

---

### Object: `passives`


**Definition:** Object listing intrinsic passive modifiers.  
**Total Count:** 884


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAfterXKills`](./Passives_and_Statuses.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#context-passiveathealththreshold), [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#context-passiveatinjurythreshold), [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold), [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement), [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2827 |

</details>

---

### Object: `stats`


**Definition:** Core character metrics (Health, Strength, etc.).  
**Total Count:** 97


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 65 |
| `spd` | Number |  | 53 |
| `cha` | Number |  | 46 |
| `int` | Number |  | 46 |
| `str` | Number |  | 42 |
| `dex` | Number |  | 34 |
| `lck` | Number |  | 29 |

</details>

---

### Object: `AddStatusToBasicAttack`


**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 92


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToCharmed`](./Passives_and_Statuses.md#context-addpassivestocharmed), [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#context-passivewhenatfullmana), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 187 |

</details>

---

### Object: `effects`


**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 30


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#context-damageneighborsaftermove), [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#context-damageneighborsonendmove), [`GravityWell`](./Passives_and_Statuses.md#context-gravitywell), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`RevengeDamage`](./Passives_and_Statuses.md#context-revengedamage), [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#context-smiteenemieswhokill), [`fire`](./Passives_and_Statuses.md#context-fire), [`ice`](./Passives_and_Statuses.md#context-ice), [`lightning`](./Passives_and_Statuses.md#context-lightning), [`triattack`](./Passives_and_Statuses.md#context-triattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1390 |

</details>

---

### Object: `AddPassivesToMinions`


**Definition:** Applies the 'AddPassivesToMinions' effect.  
**Total Count:** 29


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 44 |

</details>

---

### Object: `SpawnOnBattleStart`


**Definition:** No definition provided.  
**Total Count:** 21


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array |  | 72 |
| [`number`](./Arrays.md#array-number) | Array |  | 48 |

</details>

---

### Object: `StatusOnTookDamage`


**Definition:** Event Trigger: Applies nested statuses when took damage.  
**Total Count:** 21


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 40 |

</details>

---

### Object: `StatusEachTurnEnd`


**Definition:** Applies or references the 'StatusEachTurnEnd' effect/state.  
**Total Count:** 20


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 55 |

</details>

---

### Object: `lock_item_slot`


**Definition:** No definition provided.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum |  | 20 |
| `frame` | Number |  | 6 |

</details>

---

### Object: `StatusOnBattleEnd`


**Definition:** Applies the nested status effects when the encounter finishes.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 58 |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 50 |

</details>

---

### Object: `StatusOnKill`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 36 |

</details>

---

### Object: `StatusOnStanceSwitch`


**Definition:** Event Trigger: Applies nested statuses when stance switch.  
**Total Count:** 14


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#context-passiveifemptyface), [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#context-passiveifemptyhead), [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#context-passiveifemptyneck), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 |
| `NextBasicAttackCritsThisTurn` | `Number` | Guarantees the next basic attack executed this turn will be a critical hit. | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `SpreadDisease`


**Definition:** Provides a chance to transmit a disease status to adjacent targets.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`effects`](./Passives_and_Statuses.md#context-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`disease`](./Enums.md#enum-disease) | Enum | The specific status effect ID representing the disease. | 26 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of transmitting. | 24 |
| `can_apply_to_anything` | Boolean |  | 12 |

</details>

---

### Object: `StatusEachTurnBegin`


**Definition:** Event Trigger: Applies nested statuses to each turn begin.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |

</details>

---

### Object: `Conditional_Ally`


**Definition:** Conditional trigger: Executes nested logic if the target is friendly to the caster.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#context-conditional_sourcehastag), [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#context-extrastatuswhendealingdamage), [`StatusKilledCharacters`](./Passives_and_Statuses.md#context-statuskilledcharacters)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 30 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 29 |
| `Cleanse` | `Number` | Applies the 'Cleanse' effect. | 6 |
| [`ApplyToSource`](./Passives_and_Statuses.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 4 |
| `ClearNegativeEffects` | `Number` | Applies the 'ClearNegativeEffects' effect. | 4 |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object | Selects and applies a random status effect from the provided nested block. | 4 |

</details>

---

### Object: `CritsApplyStatus`


**Definition:** Applies the 'CritsApplyStatus' effect.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 |

</details>

---

### Object: `Temporary`


**Definition:** A wrapper object for applying status effects that automatically expire.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_BadRoll`](./Passives_and_Statuses.md#context-conditional_badroll), [`StatusOnGainShield`](./Passives_and_Statuses.md#context-statusongainshield), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage), [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#context-statusonturnendifmanaorhealthexact)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 114 |
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 112 |
| `turns` | Number | Duration in turns. | 104 |
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 50 |
| `expires_on_end_turn` | Boolean |  | 42 |

</details>

---

### Object: `PassiveAtStatThreshold`


**Definition:** Applies the 'PassiveAtStatThreshold' effect.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 33 |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 26 |

</details>

---

### Object: `threshold`


**Definition:** Examples: `4*champion_multiplier, 3*champion_multiplier, 1`  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 16 |
| `cha` | Number |  | 4 |
| `spd` | Number |  | 4 |

</details>

---

### Object: `RevengeDamage`


**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 58 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |
| `knockback` | Number |  | 6 |

</details>

---

### Object: `MeleeRevengeDamage`


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 94 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 75 |
| `damage` | Number | The base damage properties of an attack. | 44 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 36 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 4 |

</details>

---

### Object: `PassiveIfAllArmorEmpty`


**Definition:** Applies the 'PassiveIfAllArmorEmpty' effect.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |

</details>

---

### Object: `RandomStatusFromPool`


**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`StatusOnGainCoins`](./Passives_and_Statuses.md#context-statusongaincoins), [`StatusOnHealed`](./Passives_and_Statuses.md#context-statusonhealed), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 35 |

</details>

---

### Object: `StatusOnCrit`


**Definition:** Event Trigger: Applies nested statuses when crit.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |

</details>

---

### Object: `Conditional_Enemy`


**Definition:** Conditional trigger: Executes nested logic if the target is hostile to the caster.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_NotBoss`](./Passives_and_Statuses.md#context-conditional_notboss)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 37 |

</details>

---

### Object: `DamageNeighborsOnEndMove`


**Definition:** Combat Trigger: Deals damage to neighbors on end move.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 14 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 14 |
| `cant_miss` | `Boolean` |  | 12 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 12 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |
| `knockback` | Number |  | 2 |

</details>

---

### Object: `ForceUseAbility`


**Definition:** No definition provided.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin), [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 10 |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 6 |

</details>

---

### Object: `PassiveIfEmptyFace`


**Definition:** Applies the 'PassiveIfEmptyFace' effect.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |

</details>

---

### Object: `PassiveIfEmptyHead`


**Definition:** Applies the 'PassiveIfEmptyHead' effect.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |

</details>

---

### Object: `PassiveIfEmptyNeck`


**Definition:** Applies the 'PassiveIfEmptyNeck' effect.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |

</details>

---

### Object: `StatusAlliesOnDeath`


**Definition:** Event Trigger: Applies nested statuses to allies on death.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |
| `triggers_limit` | Number |  | 4 |

</details>

---

### Object: `StatusOnUseAbilityWithTag`


**Definition:** Event Trigger: Applies nested statuses when use ability with tag.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 14 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |
| `exclude_basicattack` | Boolean |  | 4 |

</details>

---

### Object: `AddStatusToElementAbilities`


**Definition:** Applies the 'AddStatusToElementAbilities' effect.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 12 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `AddStatusToWeapons`


**Definition:** Applies the 'AddStatusToWeapons' effect.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |

</details>

---

### Object: `CureDisease`


**Definition:** Applies the 'CureDisease' effect.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 12 |
| [`disease`](./Enums.md#enum-disease) | Enum |  | 12 |
| `can_apply_to_anything` | Boolean |  | 2 |

</details>

---

### Object: `Else`


**Definition:** Fallback object that executes if the preceding `Conditional_` block evaluated to false.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 76 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 72 |
| `CaptureFamiliar` | `Number` | Applies the 'CaptureFamiliar' effect. | 4 |
| `FactionConversion` | `Number` | Applies the 'FactionConversion' effect. | 4 |

</details>

---

### Object: `keyword_tooltips`


**Definition:** Forces specific UI tooltips to appear when hovering over the ability.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 18 |

</details>

---

### Object: `ManaCostReductionTagged`


**Definition:** Applies the 'ManaCostReductionTagged' effect.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reduction` | Number |  | 12 |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 12 |

</details>

---

### Object: `SpawnEachTurn`


**Definition:** Applies or references the 'SpawnEachTurn' effect/state.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 40 |
| [`object`](./Arrays.md#array-object) | Array |  | 34 |
| `good` | Boolean |  | 4 |
| `number` | Number |  | 4 |

</details>

---

### Object: `SpawnThingOnDamage`


**Definition:** Applies or references the 'SpawnThingOnDamage' effect/state.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 76 |
| `good` | Boolean |  | 40 |
| `spawn_on_death_hit` | Boolean |  | 20 |
| `consider_all_layers` | Boolean |  | 4 |

</details>

---

### Object: `AddStatusToAllDamage`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToBasicMeleeAttack`


**Definition:** Examples: `{ ... }`  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |

</details>

---

### Object: `StatusOnCastSpell`


**Definition:** Event Trigger: Applies nested statuses when cast spell.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |

</details>

---

### Object: `StatusOnOverHealed`


**Definition:** Event Trigger: Applies nested statuses when over healed.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| `SpawnScaledRotFly` | Number | Applies the 'SpawnScaledRotFly' effect. | 2 |

</details>

---

### Object: `AddDamageToElementDamage`


**Definition:** Applies or references the 'AddDamageToElementDamage' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 18 |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 18 |

</details>

---

### Object: `AddPassivesToCharmed`


**Definition:** Applies the 'AddPassivesToCharmed' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |

</details>

---

### Object: `AddStatusToElementDamage`


**Definition:** Applies the 'AddStatusToElementDamage' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 12 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |

</details>

---

### Object: `AddStatusToExplosions`


**Definition:** Applies the 'AddStatusToExplosions' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddElement`](./Enums.md#enum-addelement) | Enum | Applies the 'AddElement' effect. | 16 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `AllyBonusAbilityAura`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 4 |
| `square` | Boolean |  | 4 |

</details>

---

### Object: `AllyManaRegenAura`


**Definition:** Applies the 'AllyManaRegenAura' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 8 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 8 |

</details>

---

### Object: `AmplifyStatus`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `addstacks` | Number |  | 6 |
| [`status`](./Enums.md#enum-status) | Enum | The ID of the status effect to check or apply. | 6 |

</details>

---

### Object: `AutocastEachRound`


**Definition:** Forces the character to automatically cast a specific ability at the start of each combat round.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 18 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 12 |
| `force_display_name` | Boolean |  | 4 |

</details>

---

### Object: `Conditional_FirstApplicationThisTurn`


**Definition:** Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill), [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#context-statusonuseabilitywithtag)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |

</details>

---

### Object: `DistanceBonusDamage`


**Definition:** Applies the 'DistanceBonusDamage' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `min_range` | Number |  | 8 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 8 |

</details>

---

### Object: `EMP`


**Definition:** Applies the 'EMP' effect.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`spell_graphics_override`](./Passives_and_Statuses.md#context-spell_graphics_override) | Object |  | 8 |
| [`status_explosion_override`](./Enums.md#enum-status_explosion_override) | Enum |  | 8 |

</details>

---

### Object: `empty_armor_scaled_stats`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 2 |
| `int` | Number |  | 2 |
| `spd` | Number |  | 2 |

</details>

---

### Object: `PassiveAtHealthThreshold`


**Definition:** Applies or references the 'PassiveAtHealthThreshold' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 18 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 |

</details>

---

### Object: `PassiveWhenAffectedByElement`


**Definition:** Examples: `{ ... }`  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 36 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 33 |

</details>

---

### Object: `PassiveWhenAtFullMana`


**Definition:** State Trigger: Grants nested passives when at full mana.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |

</details>

---

### Object: `spell_graphics_override`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`EMP`](./Passives_and_Statuses.md#context-emp)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum |  | 8 |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum |  | 8 |
| `palette` | Number |  | 8 |
| [`particle`](./Enums.md#enum-particle) | Enum |  | 8 |

</details>

---

### Object: `StatusAlliesOnKill`


**Definition:** Event Trigger: Applies nested statuses to allies on kill.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `StatusIfUnusedMovePoints`


**Definition:** Event Trigger: Applies nested statuses to if unused move points.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |

</details>

---

### Object: `StatusOnTurnEndIfCastNSpells`


**Definition:** Event Trigger: Applies nested statuses when turn end if cast n spells.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spells` | Number |  | 10 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnTurnEndIfManaExact`


**Definition:** Event Trigger: Applies nested statuses when turn end if mana exact.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `mana` | Number |  | 8 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnTurnEndIfManaOrHealthExact`


**Definition:** Event Trigger: Applies nested statuses when turn end if mana or health exact.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `mana` | Number |  | 8 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |

</details>

---

### Object: `AbilityReaction`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 20 |
| `ability_damage_only` | Boolean |  | 14 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |

</details>

---

### Object: `AddSelfStatusToBasicAttack`


**Definition:** Applies or references the 'AddSelfStatusToBasicAttack' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |

</details>

---

### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** Applies the 'AddTemporaryEffectsToBasicAttack' effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fury` | Number | Applies the 'Fury' effect. | 8 |
| `CastAgain` | Number | Applies the 'CastAgain' effect. | 4 |

</details>

---

### Object: `Conditional_BadRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized bad outcome probability.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Enum | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 16 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |

</details>

---

### Object: `Conditional_HasStatus`


**Definition:** Conditional trigger: Executes nested logic if the target currently has the specified status effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 40 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 24 |

</details>

---

### Object: `DeathRattle`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 26 |
| `pop_corpse` | Boolean |  | 22 |

</details>

---

### Object: `ElementalManaCostReduction`


**Definition:** Applies the 'ElementalManaCostReduction' effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reduction` | Number |  | 10 |
| [`element`](./Arrays.md#array-element) | Array | The specific element type required or applied. | 4 |

</details>

---

### Object: `FindItemFromPool`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability of finding the item. | 6 |
| [`pool`](./Enums.md#enum-pool) | Enum | The item pool to draw from. | 4 |

</details>

---

### Object: `MoveTowardsDamageSource`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 10 |
| `move_far` | Boolean |  | 8 |

</details>

---

### Object: `ObjectOnHitCharacter`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend), [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#context-statuseachturnendperenemykill)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the character to spawn (e.g., CharmedFlea). | 14 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 10 |

</details>

---

### Object: `SpawnCatCopyOnBattleStart`


**Definition:** Applies the 'SpawnCatCopyOnBattleStart' effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 8 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum |  | 8 |

</details>

---

### Object: `SpawnOnBattleStartRandomEmptyTile`


**Definition:** Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 22 |
| [`number`](./Arrays.md#array-number) | Array |  | 6 |

</details>

---

### Object: `statuses`


**Definition:** Status effects possessed by the character.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChanceToRevive`](./Passives_and_Statuses.md#context-chancetorevive), [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#context-statusonbattleendifkillthresholdmet)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |

</details>

---

### Object: `StatusEveryXSpellCasts`


**Definition:** Applies or references the 'StatusEveryXSpellCasts' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 16 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |

</details>

---

### Object: `StatusGroup`


**Definition:** Groups multiple status effects together for batch application.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `StatusKilledCharacters`


**Definition:** Event Trigger: Applies nested statuses to killed characters.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnAllyCatDeath`


**Definition:** Event Trigger: Applies nested statuses when ally cat death.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `StatusOnBattleStart`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |

</details>

---

### Object: `StatusOnEatFood`


**Definition:** Event Trigger: Applies nested statuses when eat food.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `StatusOnGainCoins`


**Definition:** Event Trigger: Applies nested statuses when gain coins.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |

</details>

---

### Object: `StatusOnHealed`


**Definition:** Event Trigger: Applies nested statuses when healed.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `StatusOnKillEnemy`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |

</details>

---

### Object: `StatusOnTookDamageFromAbility`


**Definition:** Event Trigger: Applies statuses when taking damage from an ability.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |

</details>

---

### Object: `AbilityWhenTaggedCharacterMovesNear`


**Definition:** AI Trigger: Executes an ability when a character with a specific tag moves adjacent.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 10 |
| [`range`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Mixed | Distance or area of effect in tiles. | 10 |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 10 |

</details>

---

### Object: `AddPassivesToSummonAbilityMinions`


**Definition:** Applies the 'AddPassivesToSummonAbilityMinions' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `AddPassiveToSpawnedRocks`


**Definition:** Applies the 'AddPassiveToSpawnedRocks' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddFilledMaxHealth` | Number | Applies the 'AddFilledMaxHealth' effect. | 4 |
| `JoinSpawnerFaction` | Number | Applies the 'JoinSpawnerFaction' effect. | 4 |

</details>

---

### Object: `AddSelfStatusToWeapons`


**Definition:** Applies the 'AddSelfStatusToWeapons' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToAllDamageAbilities`


**Definition:** Applies the 'AddStatusToAllDamageAbilities' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `AddStatusToBasicAttackWithCooldown`


**Definition:** Applies the 'AddStatusToBasicAttackWithCooldown' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CharmedForceAttack` | `Number` | Applies the 'CharmedForceAttack' effect. | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `AddStatusToFirstBasicAttack`


**Definition:** Applies the 'AddStatusToFirstBasicAttack' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToMeleeDamage`


**Definition:** Applies the 'AddStatusToMeleeDamage' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DelayedWind`](./Passives_and_Statuses.md#context-delayedwind) | Object | Applies the 'DelayedWind' effect. | 2 |

</details>

---

### Object: `AddStatusToTrampleDamage`


**Definition:** Applies the 'AddStatusToTrampleDamage' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `AllyHealthRegenAura`


**Definition:** Applies the 'AllyHealthRegenAura' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 4 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 4 |

</details>

---

### Object: `AlternateCraftingPools`


**Definition:** Applies the 'AlternateCraftingPools' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tinkerer_0`](./Enums.md#enum-tinkerer_0) | Enum |  | 4 |
| [`tinkerer_1`](./Enums.md#enum-tinkerer_1) | Enum |  | 4 |

</details>

---

### Object: `ApplyStatusesToRandomEnemiesEachTurn`


**Definition:** Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Number | The numerical quantity. | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `ApplyStatusIfCrit`


**Definition:** Conditional trigger: Executes the nested logic only if the triggering action was a critical hit.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |

</details>

---

### Object: `ApplyToSource`


**Definition:** Redirects the nested effects to apply to the caster/source of the ability instead of the target.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 46 |

</details>

---

### Object: `AutocastEachTurnBegin`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `advantage_polarity` | Number |  | 2 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |

</details>

---

### Object: `BoobyTrapItems`


**Definition:** Applies the 'BoobyTrapItems' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`on_break`](./Passives_and_Statuses.md#context-on_break) | Object |  | 4 |
| [`on_throw`](./Passives_and_Statuses.md#context-on_throw) | Object |  | 4 |

</details>

---

### Object: `BoostWeaponDamage`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`crit_chance`](./Engine_DamagingKeys.md#valid-property-keys) | `String` |  | 8 |
| `damage` | Number | The base damage properties of an attack. | 8 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `BouncyProjectiles`


**Definition:** Applies the 'BouncyProjectiles' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number |  | 6 |
| `max_range` | Number |  | 6 |

</details>

---

### Object: `CatAPultAnimation`


**Definition:** Applies the 'CatAPultAnimation' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 4 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 4 |

</details>

---

### Object: `CatchProjectiles`


**Definition:** Applies or references the 'CatchProjectiles' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ally_chance` | Number |  | 10 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 10 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `ChanceToBackflip`


**Definition:** Applies or references the 'ChanceToBackflip' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 12 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 12 |

</details>

---

### Object: `ChangeTile`


**Definition:** Transforms the terrain tile under the target.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tile`](./Enums.md#enum-tile) | Enum | The specific tile type to change into (e.g., GlassTile). | 22 |
| `aoe` | Number | The area of effect or distance in tiles. | 4 |

</details>

---

### Object: `ClassManaCostReduction`


**Definition:** Applies or references the 'ClassManaCostReduction' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reduction` | Number |  | 14 |
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 12 |

</details>

---

### Object: `Conditional_Adjacent`


**Definition:** Conditional object: Executes nested logic only if the target is/has Adjacent.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `Conditional_Boss`


**Definition:** Conditional trigger: Executes nested logic if the target is a Boss.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 27 |

</details>

---

### Object: `Conditional_Corpse`


**Definition:** Conditional trigger: Executes nested logic if the target is a dead body/corpse.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToElementDamage`](./Passives_and_Statuses.md#context-addstatustoelementdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Revive` | `Number` | Applies the 'Revive' effect. | 13 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |
| `OverrideDamage` | `Number` | Applies the 'OverrideDamage' effect. | 4 |
| `TakeExtraTurn` | `Number` | Applies the 'TakeExtraTurn' effect. | 4 |

</details>

---

### Object: `Conditional_HasTag`


**Definition:** Conditional trigger: Executes nested logic if the target possesses the specified entity tag.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Passives_and_Statuses.md#context-addstatustoalldamage), [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. | 91 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 63 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 63 |
| `FlatLeechIfDamaged` | `Number` | Applies the 'FlatLeechIfDamaged' effect. | 2 |

</details>

---

### Object: `Conditional_NotBoss`


**Definition:** Conditional trigger: Executes nested logic if the target is NOT a Boss.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `Conditional_PartyMember`


**Definition:** Conditional constraint. Nested properties only trigger if this is true.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `Conditional_Shielded`


**Definition:** Conditional trigger: Executes nested logic if the target currently has a Shield status.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BonusCritChance` | `Number` | Applies the 'BonusCritChance' effect. | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `Craft`


**Definition:** Synthesizes or spawns a new item from a specific pool.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 30 |
| [`slot`](./Enums.md#enum-slot) | Enum |  | 28 |

</details>

---

### Object: `DamageNeighborsAfterMove`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Equation | The base damage properties of an attack. | 8 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 8 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 8 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |

</details>

---

### Object: `DamageNeighborTilesWhenCastSpell`


**Definition:** Combat Trigger: Deals damage to neighbor tiles when cast spell.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`fire`](./Passives_and_Statuses.md#context-fire) | Object |  | 2 |
| [`ice`](./Passives_and_Statuses.md#context-ice) | Object |  | 2 |
| [`lightning`](./Passives_and_Statuses.md#context-lightning) | Object |  | 2 |
| [`triattack`](./Passives_and_Statuses.md#context-triattack) | Object |  | 2 |

</details>

---

### Object: `DamageReductionAura`


**Definition:** Combat Trigger: Deals damage to reduction aura.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 4 |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 4 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 4 |

</details>

---

### Object: `Earth`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Equation | The base damage properties of an attack. | 4 |

</details>

---

### Object: `Electric`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `ElementalAttunement`


**Definition:** Applies the 'ElementalAttunement' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Earth`](./Passives_and_Statuses.md#context-earth) | Object | Applies the 'Earth' effect. | 4 |
| [`Electric`](./Passives_and_Statuses.md#context-electric) | Object | Applies the 'Electric' effect. | 4 |
| [`Fire`](./Passives_and_Statuses.md#context-fire) | Object | Applies the 'Fire' effect. | 4 |
| [`Grass`](./Passives_and_Statuses.md#context-grass) | Object | Applies the 'Grass' effect. | 4 |
| [`Gravity`](./Passives_and_Statuses.md#context-gravity) | Object | Applies the 'Gravity' effect. | 4 |
| [`Holy`](./Passives_and_Statuses.md#context-holy) | Object | Applies the 'Holy' effect. | 4 |
| [`Ice`](./Passives_and_Statuses.md#context-ice) | Object | Applies the 'Ice' effect. | 4 |
| [`Shadow`](./Passives_and_Statuses.md#context-shadow) | Object | Applies the 'Shadow' effect. | 4 |
| [`Water`](./Passives_and_Statuses.md#context-water) | Object | Applies the 'Water' effect. | 4 |
| [`Wind`](./Passives_and_Statuses.md#context-wind) | Object | Applies the 'Wind' effect. | 4 |

</details>

---

### Object: `EscapeSequence`


**Definition:** Applies the 'EscapeSequence' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomDistanceDisplace` | `Number` | Displaces the target by a randomized distance. | 4 |
| `SafeExplosionIfHitSomething` | Number | Applies the 'SafeExplosionIfHitSomething' effect. | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `Eternal`


**Definition:** Applies the 'Eternal' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health_percent` | Number |  | 6 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 6 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `ExtraStatusWhenDealingDamage`


**Definition:** Applies or references the 'ExtraStatusWhenDealingDamage' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `Fire`


**Definition:** Character Form: Behavior and stats for the 'Fire' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `Grass`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `Gravity`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `GravityWell`


**Definition:** Applies the 'GravityWell' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 4 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 4 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |

</details>

---

### Object: `HealAlliesEachTurn`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean |  | 4 |
| `mana` | Number |  | 4 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 4 |

</details>

---

### Object: `Holy`


**Definition:** Character Form: Behavior and stats for the \'Holy\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `HolyDamageBlessing`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilGetKill`](./Passives_and_Statuses.md#context-passiveuntilgetkill)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage_multiplier` | Number |  | 4 |

</details>

---

### Object: `Ice`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `InfiniteRebirth`


**Definition:** Applies the 'InfiniteRebirth' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 6 |
| `playercat_health` | Number |  | 6 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `LateBloomer`


**Definition:** Applies the 'LateBloomer' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `LightningRod`


**Definition:** Applies the 'LightningRod' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `LowHealthAllyDodgeChanceAura`


**Definition:** Applies the 'LowHealthAllyDodgeChanceAura' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 4 |
| `theshold` | Number |  | 4 |

</details>

---

### Object: `MovementReaction`


**Definition:** Reaction: Triggers an effect or ability when forced to move.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 22 |
| `enemies_only` | Boolean |  | 14 |

</details>

---

### Object: `NextBattleStatus`


**Definition:** Applies the 'NextBattleStatus' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `on_break`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SafeExplosionIfHitSomething` | Number | Applies the 'SafeExplosionIfHitSomething' effect. | 4 |

</details>

---

### Object: `on_throw`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HitExplosion` | `Number` | Applies the 'HitExplosion' effect. | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `PassiveAfterXKills`


**Definition:** Applies or references the 'PassiveAfterXKills' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 8 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |

</details>

---

### Object: `PassiveAtFullHealth`


**Definition:** Applies the 'PassiveAtFullHealth' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TakeExtraDamage` | Number | Applies the 'TakeExtraDamage' effect. | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `PassiveAtInjuryThreshold`


**Definition:** Applies the 'PassiveAtInjuryThreshold' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `String` |  | 4 |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `PassiveGroup`


**Definition:** Passive: A collection of passives grouped together for easier management.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Passives_and_Statuses.md#context-randompassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 |

</details>

---

### Object: `PassiveUntilCastSpell`


**Definition:** Applies the 'PassiveUntilCastSpell' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`HealAlliesEachTurn`](./Passives_and_Statuses.md#context-healallieseachturn) | Object | Applies the 'HealAlliesEachTurn' effect. | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `PassiveUntilGetKill`


**Definition:** Applies the 'PassiveUntilGetKill' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`HolyDamageBlessing`](./Passives_and_Statuses.md#context-holydamageblessing) | Object | Applies the 'HolyDamageBlessing' effect. | 4 |

</details>

---

### Object: `PassiveWhenTheAlpha`


**Definition:** State Trigger: Grants nested passives when the alpha.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TogglableRoundEndExtraTurn` | Number | Applies the 'TogglableRoundEndExtraTurn' effect. | 4 |

</details>

---

### Object: `PassiveWhileInMonkMeleeStance`


**Definition:** Applies the 'PassiveWhileInMonkMeleeStance' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `PassiveWhileInMonkRangedStance`


**Definition:** Applies the 'PassiveWhileInMonkRangedStance' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `PassiveWhilePreviewingMonkRangedStance`


**Definition:** Applies the 'PassiveWhilePreviewingMonkRangedStance' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `PassiveWhileWearingMetal`


**Definition:** Applies the 'PassiveWhileWearingMetal' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddElementsToWeapon`](./Enums.md#enum-addelementstoweapon) | Enum | Applies the 'AddElementsToWeapon' effect. | 4 |

</details>

---

### Object: `RepressedMemoriesMetronome`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#context-scaledstatusonspendmana)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 4 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 4 |

</details>

---

### Object: `ScaledStatusOnOverMana`


**Definition:** Applies the 'ScaledStatusOnOverMana' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `ScaledStatusOnSpendMana`


**Definition:** Applies the 'ScaledStatusOnSpendMana' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RepressedMemoriesMetronome`](./Passives_and_Statuses.md#context-repressedmemoriesmetronome) | Object | Applies the 'RepressedMemoriesMetronome' effect. | 4 |

</details>

---

### Object: `schadenfreude_scaled_stats`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 2 |
| `str` | Number |  | 2 |

</details>

---

### Object: `SecurityBotProtect`


**Definition:** AI Logic: Guarding behavior for Security Bot units.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 14 |
| [`move`](./Enums.md#enum-move) | Enum |  | 10 |

</details>

---

### Object: `Shadow`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`crit_chance`](./Engine_DamagingKeys.md#valid-property-keys) | `String` |  | 4 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `SmiteEnemiesWhoKill`


**Definition:** Applies the 'SmiteEnemiesWhoKill' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 4 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 4 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `SpecialFriends`


**Definition:** Applies the 'SpecialFriends' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `StatsAtLowHealth`


**Definition:** Applies the 'StatsAtLowHealth' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `speed` | Number |  | 2 |
| `strength` | Number |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusAfterCastSpell`


**Definition:** Applies or references the 'StatusAfterCastSpell' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusAlliesOnBattleStart`


**Definition:** Applies or references the 'StatusAlliesOnBattleStart' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |

</details>

---

### Object: `StatusAlliesOnGainCoins`


**Definition:** Event Trigger: Applies nested statuses to allies on gain coins.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `scaled` | Boolean |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusAllyWhenAllySpendsMana`


**Definition:** Event Trigger: Applies nested statuses to ally when ally spends mana.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusAnyCatAllyWhoKills`


**Definition:** Event Trigger: Applies nested statuses to any cat ally who kills.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusDamagers`


**Definition:** Event Trigger: Applies nested statuses to damagers.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusEachTurnEndForEachTurn`


**Definition:** Event Trigger: Applies nested statuses to each turn end for each turn.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `StatusEachTurnEndPerEnemyKill`


**Definition:** Event Trigger: Applies nested statuses to each turn end per enemy kill.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusEnemiesOnDeath`


**Definition:** Event Trigger: Applies nested statuses to enemies on death.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusEveryXTurnBegins`


**Definition:** Event Trigger: Applies nested statuses to every x turn begins.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `turns` | Number | The duration of the effect in turns. | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusKillers`


**Definition:** Instantly kills the target if they possess the specified status effects.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnAnyDeath`


**Definition:** Event Trigger: Applies nested statuses when any death.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnBattleEndIfKillThresholdMet`


**Definition:** Event Trigger: Applies nested statuses when battle end if kill threshold met.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `kills` | Number |  | 4 |
| [`statuses`](./Passives_and_Statuses.md#context-statuses) | Object |  | 4 |

</details>

---

### Object: `StatusOnBreakItem`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `StatusOnCollectPickup`


**Definition:** Event Trigger: Applies nested statuses when collect pickup.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnDealtDamage`


**Definition:** Event Trigger: Applies nested statuses when dealt damage.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnDealtDamageThreshold`


**Definition:** Event Trigger: Applies nested statuses when dealt damage threshold.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count_overkill` | Boolean |  | 4 |
| `ignore_during_movement` | Boolean |  | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnEndMove`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnGainShield`


**Definition:** Event Trigger: Applies nested statuses when gain shield.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnHeal`


**Definition:** Event Trigger: Applies nested statuses when heal.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnOverMana`


**Definition:** Event Trigger: Applies nested statuses when over mana.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnPickupCoins`


**Definition:** Event Trigger: Applies nested statuses when pickup coins.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `StatusOnPopCorpse`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |

</details>

---

### Object: `StatusOnTookDamageFromEnemyAbility`


**Definition:** Event Trigger: Applies nested statuses when took damage from enemy ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnTriggerTrap`


**Definition:** Event Trigger: Applies nested statuses when trigger trap.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnUseBasicAttack`


**Definition:** Event Trigger: Applies nested statuses when use basic attack.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `StatusOnUseElementAbility`


**Definition:** Event Trigger: Applies nested statuses when use element ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusPerInjury`


**Definition:** Event Trigger: Applies nested statuses to per injury.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cap` | Number |  | 4 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `String` |  | 4 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusThingsKnockedBack`


**Definition:** Event Trigger: Applies nested statuses to things knocked back.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Drag` | Number | Applies the 'Drag' effect. | 4 |

</details>

---

### Object: `StatusWhenAllySpendsMana`


**Definition:** Event Trigger: Applies nested statuses to when ally spends mana.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `TaggedPickupEffectReplacement`


**Definition:** Applies the 'TaggedPickupEffectReplacement' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `TowerDefense`


**Definition:** Applies the 'TowerDefense' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 4 |
| `range` | Number | Distance or area of effect in tiles. | 4 |

</details>

---

### Object: `Water`


**Definition:** Character Form: Behavior and stats for the \'Water\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AOEPuddle`](./Math_Equations.md) | Equation | Applies the 'AOEPuddle' effect. | 4 |

</details>

---

### Object: `Wind`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`knockback`](./Math_Equations.md) | Equation |  | 4 |

</details>

---

### Object: `AbilityChargeRefundChance`


**Definition:** Applies the 'AbilityChargeRefundChance' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `advantage_softcap` | Number |  | 2 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |

</details>

---

### Object: `AddStatusesIfPersistentWeatherElement`


**Definition:** Applies the 'AddStatusesIfPersistentWeatherElement' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `AddStatusesToReceivedElementalDamage`


**Definition:** Applies the 'AddStatusesToReceivedElementalDamage' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `AddStatusToKnockbackDamage`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToReceivedDamage_ExcludeStatuses`


**Definition:** Applies the 'AddStatusToReceivedDamage_ExcludeStatuses' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToSpells`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddTemporaryEffectsToEquipment`


**Definition:** Applies the 'AddTemporaryEffectsToEquipment' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | Applies the 'CastAgain' effect. | 2 |

</details>

---

### Object: `Autism`


**Definition:** Applies the 'Autism' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `innate` | Number |  | 2 |
| `learned` | Number |  | 2 |

</details>

---

### Object: `ChanceToRevive`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 10 |
| [`statuses`](./Passives_and_Statuses.md#context-statuses) | Object |  | 6 |

</details>

---

### Object: `CollectPickupsOnBattleEnd`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `pop_corpses` | Boolean |  | 2 |

</details>

---

### Object: `Conditional_DoesDamage`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage_ExcludeStatuses`](./Passives_and_Statuses.md#context-addstatustoreceiveddamage_excludestatuses)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 72 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 40 |
| `UseRandomSpell_Madness` | `Number` | Applies the 'UseRandomSpell_Madness' effect. | 2 |

</details>

---

### Object: `Conditional_SourceHasTag`


**Definition:** Conditional object: Executes nested logic only if the target is/has SourceHasTag.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `DamageIfDidntUseSpecificAbility`


**Definition:** Combat Trigger: Deals damage to if didnt use specific ability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `damage` | Number | The base damage properties of an attack. | 2 |

</details>

---

### Object: `DelayedWind`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | The area of effect or distance in tiles. | 2 |

</details>

---

### Object: `DelayedWindCone`


**Definition:** Creates a delayed Area of Effect cone.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | The area of effect or distance in tiles. | 4 |

</details>

---

### Object: `Diabetes`


**Definition:** Applies the 'Diabetes' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `EnergyStorm`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number |  | 2 |
| `period` | Number |  | 2 |

</details>

---

### Object: `fire`


**Definition:** Character Form: Behavior and stats for the 'Fire' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 2 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `ForceMoveAway`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusAdjacentOnTheirTurnBegin`](./Passives_and_Statuses.md#context-statusadjacentontheirturnbegin)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `free` | Boolean |  | 2 |

</details>

---

### Object: `FurnitureStats`


**Definition:** Applies the 'FurnitureStats' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Appeal` | Number | Applies the 'Appeal' effect. | 2 |
| `Comfort` | Number | Applies the 'Comfort' effect. | 2 |
| `Stimulation` | Number | Applies the 'Stimulation' effect. | 2 |

</details>

---

### Object: `ice`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 2 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `lightning`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 2 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `MegaMinions`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number |  | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Object: `MoveWhenDamaged`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 18 |

</details>

---

### Object: `PassiveLevelScaledStatus`


**Definition:** Applies the 'PassiveLevelScaledStatus' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`SizeScalePercent`](./Math_Equations.md) | Equation | Applies the 'SizeScalePercent' effect. | 2 |

</details>

---

### Object: `RandomPassivePool`


**Definition:** Logic: Grants a random passive from the specified pool upon spawning.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 26 |

</details>

---

### Object: `ReplaceBrain`


**Definition:** Applies the 'ReplaceBrain' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 8 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 8 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 8 |

</details>

---

### Object: `Robot`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean |  | 4 |

</details>

---

### Object: `ScaledStatusOnBleedDamage`


**Definition:** Applies the 'ScaledStatusOnBleedDamage' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `ScaledStatusOnLoseShield`


**Definition:** Applies the 'ScaledStatusOnLoseShield' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `ScaledStatusOnOverHealed`


**Definition:** Applies the 'ScaledStatusOnOverHealed' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnScaledRotFly` | Number | Applies the 'SpawnScaledRotFly' effect. | 2 |

</details>

---

### Object: `SelfDamageWhenDealDamage`


**Definition:** Applies the 'SelfDamageWhenDealDamage' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |

</details>

---

### Object: `StackingDodgeChanceOnTookDamage`


**Definition:** Applies the 'StackingDodgeChanceOnTookDamage' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `amount` | Number | The numerical quantity. | 2 |
| `cap` | Number |  | 2 |

</details>

---

### Object: `StatusAdjacentOnTheirTurnBegin`


**Definition:** Event Trigger: Applies nested statuses to adjacent on their turn begin.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusAlliesEachTurn`


**Definition:** Applies or references the 'StatusAlliesEachTurn' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusAlliesOnSpendMana`


**Definition:** Event Trigger: Applies nested statuses to allies on spend mana.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusAlliesScaledByCursedOnDeath`


**Definition:** Event Trigger: Applies nested statuses to allies scaled by cursed on death.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusIfBattleAlreadyBegan`


**Definition:** Event Trigger: Applies nested statuses to if battle already began.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnEatPill`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnLoseShield`


**Definition:** Event Trigger: Applies nested statuses when lose shield.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnTakeHealthDamage`


**Definition:** Event Trigger: Applies nested statuses when take health damage.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnTurnEndIfDidntCastAbilityTypes`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 8 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |

</details>

---

### Object: `StrengthInNumbersAura`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count_self` | Boolean |  | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Object: `Study`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `marked` | Number |  | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Object: `TakeBonusTurnWithStatus`


**Definition:** Grants the character an immediate extra turn while afflicted with specific statuses.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |

</details>

---

### Object: `TheHunger`


**Definition:** Applies the 'TheHunger' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `TileDamageMultiplier`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ally_multiplier` | Number |  | 2 |
| `multiplier` | Number | Multiplicative modifier to a base value. | 2 |

</details>

---

### Object: `TourettesMeows`


**Definition:** Applies the 'TourettesMeows' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cooldown`](./Arrays.md#array-cooldown) | Array |  | 1 |
| [`pool`](./Arrays.md#array-pool) | Array |  | 1 |

</details>

---

### Object: `triattack`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 2 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---


<details>
<summary><b>AddSelfStatusToWeapons</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

<details>
<summary><b>AddStatusToAllDamage</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 |

</details>

<details>
<summary><b>AddStatusToBasicAttackWithCooldown</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>AddStatusToFirstBasicAttack</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

<details>
<summary><b>AddStatusToKnockbackDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

<details>
<summary><b>AddStatusToMeleeDamage</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>AddStatusToReceivedDamage_ExcludeStatuses</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>AddStatusToSpells</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

<details>
<summary><b>AddStatusToTrampleDamage</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

<details>
<summary><b>Conditional_Adjacent</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

<details>
<summary><b>Conditional_DoesDamage</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>Conditional_GoodRoll</b></summary>

> **Total Count:** 30

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 30 |

</details>

<details>
<summary><b>Conditional_NotBoss</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 13 |

</details>

<details>
<summary><b>Conditional_PartyMember</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

<details>
<summary><b>Conditional_Shielded</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

<details>
<summary><b>ExtraStatusWhenDealingDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

<details>
<summary><b>NextBattleStatus</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

<details>
<summary><b>PassiveLevelScaledStatus</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

<details>
<summary><b>StatusAdjacentOnTheirTurnBegin</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>StatusAlliesOnSpendMana</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

<details>
<summary><b>StatusAnyCatAllyWhoKills</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

<details>
<summary><b>StatusEnemiesOnDeath</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

<details>
<summary><b>StatusKilledCharacters</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>StatusKillers</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

<details>
<summary><b>StatusOnDealtDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

<details>
<summary><b>StatusOnEatPill</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |

</details>

<details>
<summary><b>StatusOnOverHealed</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>
