# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Passives & Statuses

> **Associated Files:** `data/passives/, data/passive_pools.gon`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 885

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 531 |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the passive's display description. | 885 |
| [`name`](./Strings.md#string-name) | String | Localization key for the passive's display name. | 512 |
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 510 |
| [`stats`](./Passives_and_Statuses.md#context-stats) | Object |  | 97 |
| `con` | Number |  | 18 |
| `spd` | Number |  | 17 |
| [`lock_item_slot`](./Passives_and_Statuses.md#context-lock_item_slot) | Object |  | 16 |
| `cha` | Number |  | 13 |
| `int` | Number |  | 12 |
| `str` | Number |  | 12 |
| [`desc_multiclass`](./Strings.md#string-desc_multiclass) | String |  | 10 |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum |  | 10 |
| `lck` | Number |  | 9 |
| `shield` | Number |  | 9 |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | Flat addition to a base value. | 8 |
| `dex` | Number |  | 8 |
| `divine_shield` | Number | Examples: `3, 1` | 6 |
| [`keyword_tooltips`](./Passives_and_Statuses.md#context-keyword_tooltips) | Object | Examples: `{ ... }` | 6 |
| `auto_plus_signs_on_name` | Boolean |  | 4 |
| [`empty_armor_scaled_stats`](./Passives_and_Statuses.md#context-empty_armor_scaled_stats) | Object | Examples: `{ ... }` | 4 |
| [`name_mod`](./Strings.md#string-name_mod) | String |  | 4 |
| [`tags`](./Arrays.md#array-tags) | Array |  | 3 |
| [`icon`](./Enums.md#enum-icon) | Enum | Examples: `DejaVu3, DejaVu2` | 2 |
| [`schadenfreude_scaled_stats`](./Passives_and_Statuses.md#context-schadenfreude_scaled_stats) | Object | Examples: `{ ... }` | 2 |
| [`grant_ability`](./Enums.md#enum-grant_ability) | Enum |  | 1 |

</details>

---

### Object: `passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 884

> **Referenced by:** [`PassiveAfterXKills`](./Passives_and_Statuses.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#context-passiveathealththreshold), [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#context-passiveatinjurythreshold), [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold), [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement), [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2609 |

</details>

---

### Object: `stats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 97

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 31 |
| `spd` | Number |  | 26 |
| `cha` | Number |  | 22 |
| `int` | Number |  | 22 |
| `str` | Number |  | 20 |
| `dex` | Number |  | 16 |
| `lck` | Number |  | 13 |

</details>

---

### Object: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 92

> **Referenced by:** [`AddPassivesToCharmed`](./Passives_and_Statuses.md#context-addpassivestocharmed), [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#context-passivewhenatfullmana), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 119 |

</details>

---

### Object: `effects`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 30

> **Referenced by:** [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#context-damageneighborsaftermove), [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#context-damageneighborsonendmove), [`GravityWell`](./Passives_and_Statuses.md#context-gravitywell), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`RevengeDamage`](./Passives_and_Statuses.md#context-revengedamage), [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#context-smiteenemieswhokill), [`fire`](./Passives_and_Statuses.md#context-fire), [`ice`](./Passives_and_Statuses.md#context-ice), [`lightning`](./Passives_and_Statuses.md#context-lightning), [`triattack`](./Passives_and_Statuses.md#context-triattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 552 |

</details>

---

### Object: `AddPassivesToMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 29

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 41 |

</details>

---

### Object: `SpawnOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array |  | 14 |
| [`number`](./Arrays.md#array-number) | Array |  | 13 |

</details>

---

### Object: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 30 |

</details>

---

### Object: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 42 |

</details>

---

### Object: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 10 |

</details>

---

### Object: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 20 |
  | `BrittleCharismaUp` | Integer | Applies or references the 'BrittleCharismaUp' effect/state. | 0 |
  | `BrittleConstitutionUp` | Integer | Applies or references the 'BrittleConstitutionUp' effect/state. | 0 |
  | `BrittleDexterityUp` | Integer | Applies or references the 'BrittleDexterityUp' effect/state. | 0 |
  | `BrittleIntelligenceUp` | Integer | Applies or references the 'BrittleIntelligenceUp' effect/state. | 0 |
  | `BrittleLuckUp` | Integer | Applies or references the 'BrittleLuckUp' effect/state. | 0 |
  | `BrittleSpeedUp` | Integer | Applies or references the 'BrittleSpeedUp' effect/state. | 0 |
  | `BrittleStrengthUp` | Integer | Applies or references the 'BrittleStrengthUp' effect/state. | 0 |
  | [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum | Applies or references the 'UseAbility_NonStack' effect/state. | 0 |

</details>

---

### Object: `lock_item_slot`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum |  | 16 |
| `frame` | Number |  | 3 |

</details>

---

### Object: `StatusOnStanceSwitch`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#context-passiveifemptyface), [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#context-passiveifemptyhead), [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#context-passiveifemptyneck), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| `NextBasicAttackCritsThisTurn` | `Number` | Guarantees the next basic attack executed this turn will be a critical hit. | 0 |

</details>

---

### Object: `SpreadDisease`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`effects`](./Passives_and_Statuses.md#context-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`disease`](./Enums.md#enum-disease) | Enum | The specific status effect ID representing the disease. | 12 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of transmitting. | 11 |
| `can_apply_to_anything` | Boolean |  | 6 |

</details>

---

### Object: `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |

</details>

---

### Object: `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#context-conditional_sourcehastag), [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#context-extrastatuswhendealingdamage), [`StatusKilledCharacters`](./Passives_and_Statuses.md#context-statuskilledcharacters)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 29 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 |
| [`ApplyToSource`](./Passives_and_Statuses.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `Cleanse` | `Number` | Applies the 'Cleanse' effect. | 0 |
| `ClearNegativeEffects` | `Number` | Applies the 'ClearNegativeEffects' effect. | 0 |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object | Selects and applies a random status effect from the provided nested block. | 0 |

</details>

---

### Object: `CritsApplyStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `Temporary`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`Conditional_BadRoll`](./Passives_and_Statuses.md#context-conditional_badroll), [`StatusOnGainShield`](./Passives_and_Statuses.md#context-statusongainshield), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage), [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#context-statusonturnendifmanaorhealthexact)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 11 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 11 |
| `turns` | Number | Duration in turns. | 8 |
| `expires_on_end_turn` | Boolean |  | 6 |
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 5 |

</details>

---

### Object: `PassiveAtStatThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 10 |

</details>

---

### Object: `threshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number |  | 6 |
| `cha` | Number |  | 2 |
| `spd` | Number |  | 2 |

</details>

---

### Object: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `knockback` | Number |  | 2 |
  | [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. | 0 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 0 |

</details>

---

### Object: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 4 |
| `damage` | Number | The base damage properties of an attack. | 4 |
  | [`AddDamageToElementDamage`](#adddamagetoelementdamage) | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 0 |
  | [`AddStatusToElementDamage`](#addstatustoelementdamage) | Object | Applies the 'AddStatusToElementDamage' effect. | 0 |
  | [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. | 0 |
  | [`StatusImmunity`](./Enums.md#enum-statusimmunity) | Enum | Applies or references the 'StatusImmunity' effect/state. | 0 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 0 |

</details>

---

### Object: `PassiveIfAllArmorEmpty`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |

</details>

---

### Object: `RandomStatusFromPool`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`StatusOnGainCoins`](./Passives_and_Statuses.md#context-statusongaincoins), [`StatusOnHealed`](./Passives_and_Statuses.md#context-statusonhealed), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 31 |

</details>

---

### Object: `StatusOnCrit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_NotBoss`](./Passives_and_Statuses.md#context-conditional_notboss)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
  | [`Conditional_FinishedSpawning`](#conditional_finishedspawning) | Object | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. | 0 |
  | `DisplaceToAbilityTarget` | Integer | Applies or references the 'DisplaceToAbilityTarget' effect/state. | 0 |
  | `DontHealEnemies` | Integer | Applies or references the 'DontHealEnemies' effect/state. | 0 |

</details>

---

### Object: `DamageNeighborsOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 7 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 15 |
| `damage` | Number | The base damage properties of an attack. | 7 |
| `knockback` | Number |  | 1 |
| `cant_miss` | `Boolean` |  | 0 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 0 |

</details>

---

### Object: `ForceUseAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin), [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 3 |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 3 |

</details>

---

### Object: `PassiveIfEmptyFace`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |

</details>

---

### Object: `PassiveIfEmptyHead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |

</details>

---

### Object: `PassiveIfEmptyNeck`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |

</details>

---

### Object: `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `triggers_limit` | Number |  | 2 |

</details>

---

### Object: `StatusOnUseAbilityWithTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 7 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |
| `exclude_basicattack` | Boolean |  | 2 |

</details>

---

### Object: `AddStatusToElementAbilities`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 6 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `CureDisease`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`disease`](./Enums.md#enum-disease) | Enum |  | 6 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 6 |
| `can_apply_to_anything` | Boolean |  | 1 |

</details>

---

### Object: `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 71 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 20 |
| `CaptureFamiliar` | `Number` | Applies the 'CaptureFamiliar' effect. | 0 |
| `FactionConversion` | `Number` | Applies the 'FactionConversion' effect. | 0 |

</details>

---

### Object: `ManaCostReductionTagged`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 6 |
| `reduction` | Number |  | 6 |

</details>

---

### Object: `SpawnEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array |  | 6 |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 5 |
| `number` | Number |  | 2 |
| `good` | Boolean |  | 1 |

</details>

---

### Object: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 6 |
| `good` | Boolean |  | 3 |
| `spawn_on_death_hit` | Boolean |  | 2 |
| `consider_all_layers` | Boolean |  | 1 |

</details>

---

### Object: `keyword_tooltips`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |

</details>

---

### Object: `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Conditional_HasTag`](#conditionalhastag) | Object | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 0 |
  | [`KnockbackIfCrit`](#knockbackifcrit) | Object | Applies or references the 'KnockbackIfCrit' effect/state. | 0 |
  | `LeaveBehindRockOnKnockback` | Number | Applies or references the 'LeaveBehindRockOnKnockback' effect/state. | 0 |
  | [`Blind`](./Arrays.md#array-blind) | Array | Applies or references the 'Blind' effect/state. | 0 |
  | `NonLethal` | Integer | Applies the 'NonLethal' effect. | 0 |
  | [`Rot`](./Arrays.md#array-rot) | Array | Applies or references the 'Rot' effect/state. | 0 |
  | `must_do_damage` | Boolean | `true` | 0 |
  | [`Conditional_HasStatus`](#conditionalhasstatus) | Object | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 0 |
  | `BonusKnockbackDamage` | Number | Applies or references the 'BonusKnockbackDamage' effect/state. | 0 |

</details>

---

### Object: `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |

</details>

---

### Object: `StatusOnOverHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| `SpawnScaledRotFly` | Number | Applies the 'SpawnScaledRotFly' effect. | 1 |
  | `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. | 0 |
  | [`ForceUseAbility_NonStack`](./Enums.md#enum-forceuseability_nonstack) | Enum | Applies or references the 'ForceUseAbility_NonStack' effect/state. | 0 |
  | `CurrentWeaponDamageUp` | Number | Applies or references the 'CurrentWeaponDamageUp' effect/state. | 0 |

</details>

---

### Object: `AddDamageToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 4 |
| `damage` | Number | The base damage properties of an attack. | 4 |

</details>

---

### Object: `AddPassivesToCharmed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |

</details>

---

### Object: `AddStatusToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 4 |
  | [`AddDamageToElementDamage`](#adddamagetoelementdamage) | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 0 |

</details>

---

### Object: `AddStatusToExplosions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddElement`](./Enums.md#enum-addelement) | Enum | Applies the 'AddElement' effect. | 8 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `AllyBonusAbilityAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `square` | Boolean |  | 2 |

</details>

---

### Object: `AllyManaRegenAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 4 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 4 |

</details>

---

### Object: `AmplifyStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The ID of the status effect to check or apply. | 3 |
| `addstacks` | Number |  | 3 |

</details>

---

### Object: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 4 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 2 |
| `force_display_name` | Boolean |  | 2 |

</details>

---

### Object: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill), [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#context-statusonuseabilitywithtag)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `DistanceBonusDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `min_range` | Number |  | 4 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 4 |

</details>

---

### Object: `EMP`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`spell_graphics_override`](./Passives_and_Statuses.md#context-spell_graphics_override) | Object |  | 4 |
| [`status_explosion_override`](./Enums.md#enum-status_explosion_override) | Enum |  | 4 |

</details>

---

### Object: `PassiveAtHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 4 |

</details>

---

### Object: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 4 |

</details>

---

### Object: `PassiveWhenAtFullMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `StatusAlliesOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |

</details>

---

### Object: `StatusOnTurnEndIfCastNSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spells` | Number |  | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnTurnEndIfManaExact`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `mana` | Number |  | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnTurnEndIfManaOrHealthExact`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
| `mana` | Number |  | 4 |

</details>

---

### Object: `empty_armor_scaled_stats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 1 |
| `int` | Number |  | 1 |
| `spd` | Number |  | 1 |

</details>

---

### Object: `spell_graphics_override`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`EMP`](./Passives_and_Statuses.md#context-emp)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum |  | 4 |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum |  | 4 |
| `palette` | Number |  | 4 |
| [`particle`](./Enums.md#enum-particle) | Enum |  | 4 |

</details>

---

### Object: `AbilityReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 1 |
| `ability_damage_only` | Boolean |  | 1 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 1 |

</details>

---

### Object: `AddSelfStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |

</details>

---

### Object: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | Applies the 'CastAgain' effect. | 2 |
| `Fury` | Number | Applies the 'Fury' effect. | 1 |

</details>

---

### Object: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
| [`odds`](./Enums.md#enum-odds) | Enum | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 3 |

</details>

---

### Object: `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 3 |

</details>

---

### Object: `DeathRattle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `pop_corpse` | Boolean |  | 2 |

</details>

---

### Object: `ElementalManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array | The specific element type required or applied. | 3 |
| `reduction` | Number |  | 3 |

</details>

---

### Object: `FindItemFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability of finding the item. | 1 |
| [`pool`](./Enums.md#enum-pool) | Enum | The item pool to draw from. | 1 |

</details>

---

### Object: `MoveTowardsDamageSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 3 |
| `move_far` | Boolean |  | 3 |

</details>

---

### Object: `ObjectOnHitCharacter`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend), [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#context-statuseachturnendperenemykill)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the character to spawn (e.g., CharmedFlea). | 3 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 3 |

</details>

---

### Object: `SpawnCatCopyOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 3 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum |  | 3 |

</details>

---

### Object: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 3 |
| [`object`](./Enums.md#enum-object) | Enum |  | 3 |

</details>

---

### Object: `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 3 |

</details>

---

### Object: `StatusGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `AutoReanimate` | Number | Examples: `50` | 0 |
  | [`Conditional_Ally`](#conditionalally) | Object | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 0 |
  | [`Conditional_RandomChance`](#conditional_randomchance) | Object | Conditional trigger: Executes nested logic based on a flat percentage random roll. | 0 |

</details>

---

### Object: `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |

</details>

---

### Object: `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |

</details>

---

### Object: `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `StatusOnKillEnemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |

</details>

---

### Object: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `statuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ChanceToRevive`](./Passives_and_Statuses.md#context-chancetorevive), [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#context-statusonbattleendifkillthresholdmet)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |

</details>

---

### Object: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 2 |
| [`range`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Mixed | Distance or area of effect in tiles. | 2 |

</details>

---

### Object: `AddPassiveToSpawnedRocks`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddFilledMaxHealth` | Number | Applies the 'AddFilledMaxHealth' effect. | 2 |
| `JoinSpawnerFaction` | Number | Applies the 'JoinSpawnerFaction' effect. | 2 |

</details>

---

### Object: `AddPassivesToSummonAbilityMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `ChanceToBreak` | Number | Applies or references the 'ChanceToBreak' effect/state. | 0 |
  | [`RepairWeapon`](./Arrays.md#array-repairweapon) | Number | Applies or references the 'RepairWeapon' effect/state. | 0 |

</details>

---

### Object: `AddStatusToAllDamageAbilities`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `AddStatusToBasicAttackWithCooldown`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `CharmedForceAttack` | `Number` | Applies the 'CharmedForceAttack' effect. | 0 |

</details>

---

### Object: `AddStatusToFirstBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Charmed`](./Arrays.md#array-charmed) | Array | Applies or references the 'Charmed' effect/state. | 0 |

</details>

---

### Object: `AddStatusToMeleeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`DelayedWind`](./Passives_and_Statuses.md#context-delayedwind) | Object | Applies the 'DelayedWind' effect. | 1 |
  | [`DelayedWindCone`](#delayedwindcone) | Object | Creates a delayed Area of Effect cone. | 0 |

</details>

---

### Object: `AddStatusToTrampleDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `Cleave` | Object | Causes the attack to hit adjacent enemies alongside the primary target. | 0 |
  | `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 0 |

</details>

---

### Object: `AllyHealthRegenAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Object: `AlternateCraftingPools`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tinkerer_0`](./Enums.md#enum-tinkerer_0) | Enum |  | 2 |
| [`tinkerer_1`](./Enums.md#enum-tinkerer_1) | Enum |  | 2 |

</details>

---

### Object: `ApplyStatusIfCrit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `count` | Number | The numerical quantity. | 1 |

</details>

---

### Object: `ApplyToSource`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 22 |

</details>

---

### Object: `AutocastEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 1 |
| `advantage_polarity` | Number |  | 1 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 1 |

</details>

---

### Object: `BoobyTrapItems`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`on_break`](./Passives_and_Statuses.md#context-on_break) | Object |  | 2 |
| [`on_throw`](./Passives_and_Statuses.md#context-on_throw) | Object |  | 2 |

</details>

---

### Object: `BoostWeaponDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `damage` | Number | The base damage properties of an attack. | 2 |
| [`crit_chance`](./Engine_DamagingKeys.md#valid-property-keys) | `Enum/String` |  | 0 |

</details>

---

### Object: `BouncyProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number |  | 2 |
| `max_range` | Number |  | 2 |

</details>

---

### Object: `CatAPultAnimation`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |

</details>

---

### Object: `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| `ally_chance` | Number |  | 2 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |

</details>

---

### Object: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |

</details>

---

### Object: `ChangeTile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tile`](./Enums.md#enum-tile) | Enum | The specific tile type to change into (e.g., GlassTile). | 1 |
| `aoe` | Number | The area of effect or distance in tiles. | 1 |

</details>

---

### Object: `ClassManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 2 |
| `reduction` | Number |  | 2 |

</details>

---

### Object: `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
  | [`Conditional_PlayerCat`](#conditional_playercat) | Object | Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 0 |
  | `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 0 |
  | [`Bleed`](./Arrays.md#array-bleed) | Number | Applies or references the 'Bleed' effect/state. | 0 |
  | [`Conditional_Ally`](#conditionalally) | Object | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 0 |
  | `BonusCritChance` | Integer | Applies the 'BonusCritChance' effect. | 0 |

</details>

---

### Object: `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |
  | `ExplodeCharacter_PartyBoss` | Integer | Applies or references the 'ExplodeCharacter_PartyBoss' effect/state. | 0 |
  | `ExplodeCharacter_RockCrusher_PetrifyBreak` | Integer | Applies or references the 'ExplodeCharacter_RockCrusher_PetrifyBreak' effect/state. | 0 |

</details>

---

### Object: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToElementDamage`](./Passives_and_Statuses.md#context-addstatustoelementdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| `OverrideDamage` | `Number` | Applies the 'OverrideDamage' effect. | 0 |
| `Revive` | `Number` | Applies the 'Revive' effect. | 0 |
| `TakeExtraTurn` | `Number` | Applies the 'TakeExtraTurn' effect. | 0 |

</details>

---

### Object: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToAllDamage`](./Passives_and_Statuses.md#context-addstatustoalldamage), [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. | 2 |
  | `EventBounty` | Integer | Applies or references the 'EventBounty' effect/state. | 0 |
  | [`MergeDamageInstance`](#mergedamageinstance) | Object | Combines damage numbers or visual hit effects. | 0 |
  | [`SetAnimationAlts`](#setanimationalts) | Object | Overrides specific animation states with alternative animations. | 0 |
| `FlatLeechIfDamaged` | `Number` | Applies the 'FlatLeechIfDamaged' effect. | 0 |

</details>

---

### Object: `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Conditional_HasTag`](#conditionalhastag) | Object | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 0 |
  | `FactionConversion` | Integer | Applies or references the 'FactionConversion' effect/state. | 0 |
  | `PermanentCharm` | Integer | Applies the 'PermanentCharm' effect. | 0 |
  | [`Conditional_Enemy`](#conditionalenemy) | Object | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 0 |
  | `ExplodeCharacter_RockCrusher` | Integer | Applies or references the 'ExplodeCharacter_RockCrusher' effect/state. | 0 |
  | [`CanApplyToInanimate`](#canapplytoinanimate) | Object | Modifier object that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 0 |
  | `Vaporize` | Integer | Applies or references the 'Vaporize' effect/state. | 0 |
  | `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 0 |
  | `VaporizeInanimate` | Number | Applies or references the 'VaporizeInanimate' effect/state. | 0 |
  | [`Fear`](./Arrays.md#array-fear) | Array | Applies or references the 'Fear' effect/state. | 0 |
  | `Doomed` | Number | Applies or references the 'Doomed' effect/state. | 0 |
  | [`Conditional_HealthThreshold`](#conditionalhealththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 0 |

</details>

---

### Object: `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Else`](#else) | Object | Fallback object that executes if the preceding `Conditional_` block evaluated to false. | 0 |
  | [`Charmed`](./Arrays.md#array-charmed) | Array | Applies or references the 'Charmed' effect/state. | 0 |
  | [`ApplyPassives`](#applypassives) | Object | Grants the nested passive abilities dynamically. | 0 |
  | [`Conditional_IsSelf`](#conditional_isself) | Object | Conditional trigger: Executes nested logic if the target is the caster themselves. | 0 |

</details>

---

### Object: `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| `BonusCritChance` | `Number` | Applies the 'BonusCritChance' effect. | 0 |

</details>

---

### Object: `Craft`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 2 |
| [`slot`](./Enums.md#enum-slot) | Enum |  | 2 |

</details>

---

### Object: `DamageNeighborTilesWhenCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`fire`](./Passives_and_Statuses.md#context-fire) | Object |  | 1 |
| [`ice`](./Passives_and_Statuses.md#context-ice) | Object |  | 1 |
| [`lightning`](./Passives_and_Statuses.md#context-lightning) | Object |  | 1 |
| [`triattack`](./Passives_and_Statuses.md#context-triattack) | Object |  | 1 |

</details>

---

### Object: `DamageNeighborsAfterMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
| [`damage`](./Math_Equations.md) | Equation | The base damage properties of an attack. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 0 |

</details>

---

### Object: `DamageReductionAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 2 |
| `allies_only` | Boolean |  | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Object: `Earth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Equation | The base damage properties of an attack. | 2 |

</details>

---

### Object: `Electric`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
  | `X` | Variable |  | 0 |
  | [`Stun`](./Arrays.md#array-stun) | Array | Applies or references the 'Stun' effect/state. | 0 |

</details>

---

### Object: `ElementalAttunement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Earth`](./Passives_and_Statuses.md#context-earth) | Object | Applies the 'Earth' effect. | 2 |
| [`Electric`](./Passives_and_Statuses.md#context-electric) | Object | Applies the 'Electric' effect. | 2 |
| [`Fire`](./Passives_and_Statuses.md#context-fire) | Object | Applies the 'Fire' effect. | 2 |
| [`Grass`](./Passives_and_Statuses.md#context-grass) | Object | Applies the 'Grass' effect. | 2 |
| [`Gravity`](./Passives_and_Statuses.md#context-gravity) | Object | Applies the 'Gravity' effect. | 2 |
| [`Holy`](./Passives_and_Statuses.md#context-holy) | Object | Applies the 'Holy' effect. | 2 |
| [`Ice`](./Passives_and_Statuses.md#context-ice) | Object | Applies the 'Ice' effect. | 2 |
| [`Shadow`](./Passives_and_Statuses.md#context-shadow) | Object | Applies the 'Shadow' effect. | 2 |
| [`Water`](./Passives_and_Statuses.md#context-water) | Object | Applies the 'Water' effect. | 2 |
| [`Wind`](./Passives_and_Statuses.md#context-wind) | Object | Applies the 'Wind' effect. | 2 |

</details>

---

### Object: `EscapeSequence`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `SafeExplosionIfHitSomething` | Number | Applies the 'SafeExplosionIfHitSomething' effect. | 2 |
| `RandomDistanceDisplace` | `Number` | Displaces the target by a randomized distance. | 0 |

</details>

---

### Object: `Eternal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `health_percent` | Number |  | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Object: `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Conditional_PartyMember`](#conditional_partymember) | Object | Conditional constraint. Nested properties only trigger if this is true. | 0 |
  | [`Conditional_Ally`](#conditionalally) | Object | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 0 |

</details>

---

### Object: `Fire`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `Grass`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `Gravity`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
  | [`Weakness`](./Arrays.md#array-weakness) | Array | Applies or references the 'Weakness' effect/state. | 0 |

</details>

---

### Object: `GravityWell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |
| `damage` | Number | The base damage properties of an attack. | 2 |
  | `desc` | Any | Explicit empirical property. | 0 |
  | [`class`](./Enums.md#enum-class) | Enum | Categorizes the ability for specific UI filters. | 0 |
  | `name` | Any | Explicit empirical property. | 0 |

</details>

---

### Object: `HealAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean |  | 2 |
| `mana` | Number |  | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Object: `Holy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `HolyDamageBlessing`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`PassiveUntilGetKill`](./Passives_and_Statuses.md#context-passiveuntilgetkill)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage_multiplier` | Number |  | 2 |
  | `Burn` | Number | Applies or references the 'Burn' effect/state. | 0 |

</details>

---

### Object: `Ice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
  | [`Slow`](./Arrays.md#array-slow) | Array | Applies or references the 'Slow' effect/state. | 0 |

</details>

---

### Object: `InfiniteRebirth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `health` | Number |  | 2 |
| `playercat_health` | Number |  | 2 |

</details>

---

### Object: `LateBloomer`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Object: `LightningRod`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `LowHealthAllyDodgeChanceAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 2 |
| `theshold` | Number |  | 2 |

</details>

---

### Object: `MovementReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| `enemies_only` | Boolean |  | 2 |

</details>

---

### Object: `NextBattleStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`AllStatsUp`](./Arrays.md#array-allstatsup) | Number | Applies or references the 'AllStatsUp' effect/state. | 0 |
  | `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 0 |

</details>

---

### Object: `PassiveAfterXKills`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Object: `PassiveAtFullHealth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `TakeExtraDamage` | Number | Applies the 'TakeExtraDamage' effect. | 2 |

</details>

---

### Object: `PassiveAtInjuryThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 2 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |

</details>

---

### Object: `PassiveGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`RandomPassivePool`](./Passives_and_Statuses.md#context-randompassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 |

</details>

---

### Object: `PassiveUntilCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`HealAlliesEachTurn`](./Passives_and_Statuses.md#context-healallieseachturn) | Object | Applies the 'HealAlliesEachTurn' effect. | 2 |

</details>

---

### Object: `PassiveUntilGetKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`HolyDamageBlessing`](./Passives_and_Statuses.md#context-holydamageblessing) | Object | Applies the 'HolyDamageBlessing' effect. | 2 |

</details>

---

### Object: `PassiveWhenTheAlpha`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TogglableRoundEndExtraTurn` | Number | Applies the 'TogglableRoundEndExtraTurn' effect. | 2 |

</details>

---

### Object: `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `PassiveWhileInMonkRangedStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `PassiveWhilePreviewingMonkRangedStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `PassiveWhileWearingMetal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddElementsToWeapon`](./Enums.md#enum-addelementstoweapon) | Enum | Applies the 'AddElementsToWeapon' effect. | 2 |

</details>

---

### Object: `RepressedMemoriesMetronome`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#context-scaledstatusonspendmana)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 2 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 2 |

</details>

---

### Object: `ScaledStatusOnOverMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `ScaledStatusOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RepressedMemoriesMetronome`](./Passives_and_Statuses.md#context-repressedmemoriesmetronome) | Object | Applies the 'RepressedMemoriesMetronome' effect. | 2 |

</details>

---

### Object: `SecurityBotProtect`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |

</details>

---

### Object: `Shadow`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`crit_chance`](./Engine_DamagingKeys.md#valid-property-keys) | `Enum/String` |  | 0 |

</details>

---

### Object: `SmiteEnemiesWhoKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 2 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
| `damage` | Number | The base damage properties of an attack. | 2 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 0 |

</details>

---

### Object: `SpecialFriends`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `StatsAtLowHealth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `speed` | Number |  | 1 |
| `strength` | Number |  | 1 |

</details>

---

### Object: `StatusAfterCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusAlliesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |

</details>

---

### Object: `StatusAlliesOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `scaled` | Boolean |  | 1 |

</details>

---

### Object: `StatusAllyWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusAnyCatAllyWhoKills`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `AlphaCat` | Number | Applies or references the 'AlphaCat' effect/state. | 0 |

</details>

---

### Object: `StatusDamagers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `StatusEachTurnEndPerEnemyKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusEnemiesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StatusEveryXTurnBegins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `turns` | Number | The duration of the effect in turns. | 2 |

</details>

---

### Object: `StatusKillers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Conditional_Boss`](#conditionalboss) | Object | Conditional trigger: Executes nested logic if the target is a Boss. | 0 |
  | [`Conditional_NotBoss`](#conditionalnotboss) | Object | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 0 |
  | [`Confusion`](./Arrays.md#array-confusion) | Number | Applies or references the 'Confusion' effect/state. | 0 |

</details>

---

### Object: `StatusOnAnyDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnBattleEndIfKillThresholdMet`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`statuses`](./Passives_and_Statuses.md#context-statuses) | Object |  | 2 |
| `kills` | Number |  | 2 |

</details>

---

### Object: `StatusOnBreakItem`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnDealtDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
  | [`TempDexterityUp`](./Enums.md#enum-tempdexterityup) | Enum | Applies or references the 'TempDexterityUp' effect/state. | 0 |
  | `TempLuckUp` | Integer | Applies or references the 'TempLuckUp' effect/state. | 0 |
  | `TempStrengthUp` | Equation | Applies or references the 'TempStrengthUp' effect/state. | 0 |

</details>

---

### Object: `StatusOnDealtDamageThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `count_overkill` | Boolean |  | 2 |
| `ignore_during_movement` | Boolean |  | 2 |

</details>

---

### Object: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `RemoveStatusStacks` | Object | Removes a specific number of stacks of a status effect. | 0 |
  | [`Conditional_FirstApplicationThisTurn`](#conditionalfirstapplicationthisturn) | Object | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 0 |
  | [`DivineShield`](./Arrays.md#array-divineshield) | Number | Applies or references the 'DivineShield' effect/state. | 0 |
  | [`Conditional_GoodRoll`](#conditional_goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 0 |
  | [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | Applies or references the 'ImmediateUseAbility' effect/state. | 0 |
  | `Charge` | Number | Applies or references the 'Charge' effect/state. | 0 |
  | `SpeedUp_WithoutInitiative` | Integer | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. | 0 |
  | `ForceAttack` | Object | Forces the character to execute an immediate attack. | 0 |
  | `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 0 |

</details>

---

### Object: `StatusOnGainShield`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnHeal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnOverMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `StatusOnTookDamageFromEnemyAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnTriggerTrap`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `StatusOnUseElementAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusPerInjury`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `cap` | Number |  | 2 |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |

</details>

---

### Object: `StatusThingsKnockedBack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Drag` | Number | Applies the 'Drag' effect. | 2 |

</details>

---

### Object: `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `TaggedPickupEffectReplacement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `TowerDefense`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 2 |
| `range` | Number | Distance or area of effect in tiles. | 2 |

</details>

---

### Object: `Water`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AOEPuddle`](./Math_Equations.md) | Equation | Applies the 'AOEPuddle' effect. | 2 |

</details>

---

### Object: `Wind`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`knockback`](./Math_Equations.md) | Equation |  | 2 |

</details>

---

### Object: `on_break`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SafeExplosionIfHitSomething` | Number | Applies the 'SafeExplosionIfHitSomething' effect. | 2 |

</details>

---

### Object: `on_throw`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `HitExplosion` | `Number` | Applies the 'HitExplosion' effect. | 0 |

</details>

---

### Object: `schadenfreude_scaled_stats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 1 |
| `str` | Number |  | 1 |

</details>

---

### Object: `AbilityChargeRefundChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `advantage_softcap` | Number |  | 1 |
| `chance` | Number | The probability (0.0 to 1.0 or percentage) of this effect triggering. | 1 |

</details>

---

### Object: `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Stun`](./Arrays.md#array-stun) | Array | Applies or references the 'Stun' effect/state. | 0 |
  | `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 0 |

</details>

---

### Object: `AddStatusToReceivedDamage_ExcludeStatuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `Leech` | Number | Applies or references the 'Leech' effect/state. | 0 |
  | `LeechPercent` | Integer | Applies the 'LeechPercent' effect. | 0 |
  | [`Conditional_Enemy`](#conditionalenemy) | Object | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 0 |

</details>

---

### Object: `AddStatusesIfPersistentWeatherElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `AddStatusesToReceivedElementalDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
  | [`AddStatusesIfPersistentWeatherElement`](#addstatusesifpersistentweatherelement) | Object | Applies the 'AddStatusesIfPersistentWeatherElement' effect. | 0 |

</details>

---

### Object: `AddTemporaryEffectsToEquipment`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | Applies the 'CastAgain' effect. | 1 |

</details>

---

### Object: `Autism`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `innate` | Number |  | 1 |
| `learned` | Number |  | 1 |

</details>

---

### Object: `ChanceToRevive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`statuses`](./Passives_and_Statuses.md#context-statuses) | Object |  | 1 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 1 |

</details>

---

### Object: `CollectPickupsOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `pop_corpses` | Boolean |  | 1 |

</details>

---

### Object: `Conditional_DoesDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToReceivedDamage_ExcludeStatuses`](./Passives_and_Statuses.md#context-addstatustoreceiveddamage_excludestatuses)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Bleed`](./Arrays.md#array-bleed) | Number | Applies or references the 'Bleed' effect/state. | 0 |

</details>

---

### Object: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 1 |
| `UseRandomSpell_Madness` | `Number` | Applies the 'UseRandomSpell_Madness' effect. | 0 |

</details>

---

### Object: `Conditional_SourceHasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific entity tag required or applied. | 1 |
  | [`Conditional_Ally`](#conditionalally) | Object | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 0 |

</details>

---

### Object: `DamageIfDidntUseSpecificAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger or reference. | 1 |
| `damage` | Number | The base damage properties of an attack. | 1 |

</details>

---

### Object: `DelayedWind`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | The area of effect or distance in tiles. | 1 |

</details>

---

### Object: `DelayedWindCone`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | The area of effect or distance in tiles. | 1 |

</details>

---

### Object: `Diabetes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `EnergyStorm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number |  | 1 |
| `period` | Number |  | 1 |

</details>

---

### Object: `ForceMoveAway`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusAdjacentOnTheirTurnBegin`](./Passives_and_Statuses.md#context-statusadjacentontheirturnbegin)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `free` | Boolean |  | 1 |

</details>

---

### Object: `FurnitureStats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Appeal` | Number | Applies the 'Appeal' effect. | 1 |
| `Comfort` | Number | Applies the 'Comfort' effect. | 1 |
| `Stimulation` | Number | Applies the 'Stimulation' effect. | 1 |

</details>

---

### Object: `MegaMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number |  | 1 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 1 |

</details>

---

### Object: `MoveWhenDamaged`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 1 |

</details>

---

### Object: `PassiveLevelScaledStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`SizeScalePercent`](./Math_Equations.md) | Equation | Applies the 'SizeScalePercent' effect. | 1 |
  | `Shield` | Number | Applies or references the 'Shield' effect/state. | 0 |
  | [`Trample`](./Arrays.md#array-trample) | Number | Applies or references the 'Trample' effect/state. | 0 |

</details>

---

### Object: `RandomPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 22 |

</details>

---

### Object: `ReplaceBrain`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `Robot`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean |  | 1 |

</details>

---

### Object: `ScaledStatusOnBleedDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `ScaledStatusOnLoseShield`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `ScaledStatusOnOverHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnScaledRotFly` | Number | Applies the 'SpawnScaledRotFly' effect. | 1 |

</details>

---

### Object: `SelfDamageWhenDealDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |
| `damage` | Number | The base damage properties of an attack. | 1 |

</details>

---

### Object: `StackingDodgeChanceOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `amount` | Number | The numerical quantity. | 1 |
| `cap` | Number |  | 1 |

</details>

---

### Object: `StatusAdjacentOnTheirTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `ForceMoveAway` | Integer | Applies or references the 'ForceMoveAway' effect/state. | 0 |

</details>

---

### Object: `StatusAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `exclude_self` | Boolean |  | 1 |
  | `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. | 0 |
  | [`Conditional_Adjacent`](#conditional_adjacent) | Object | Conditional constraint. Nested properties only trigger if this is true. | 0 |

</details>

---

### Object: `StatusAlliesOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 0 |

</details>

---

### Object: `StatusAlliesScaledByCursedOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusIfBattleAlreadyBegan`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnEatPill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`AllStatsUp`](./Arrays.md#array-allstatsup) | Number | Applies or references the 'AllStatsUp' effect/state. | 0 |
  | [`RandomPermanentStatsDistinct`](#randompermanentstatsdistinct) | Object | Examples: `{ ... }` | 0 |

</details>

---

### Object: `StatusOnLoseShield`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnTakeHealthDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnTurnEndIfDidntCastAbilityTypes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |

</details>

---

### Object: `StrengthInNumbersAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count_self` | Boolean |  | 1 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 1 |

</details>

---

### Object: `Study`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `marked` | Number |  | 1 |
| `stacks` | Number | The number of stacks, duration, or intensity to apply. | 1 |

</details>

---

### Object: `TakeBonusTurnWithStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `TheHunger`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `TileDamageMultiplier`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ally_multiplier` | Number |  | 1 |
| `multiplier` | Number | Multiplicative modifier to a base value. | 1 |

</details>

---

### Object: `TourettesMeows`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cooldown`](./Arrays.md#array-cooldown) | Array |  | 1 |
| [`pool`](./Arrays.md#array-pool) | Array |  | 1 |

</details>

---

### Object: `fire`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 0 |

</details>

---

### Object: `ice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 0 |

</details>

---

### Object: `lightning`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 0 |

</details>

---

### Object: `triattack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | The classification type (e.g., damage type or element). | 1 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 0 |

</details>

---

