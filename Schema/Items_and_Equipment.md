# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Items & Equipment

> **Associated Files:** `data/items/, data/item_setbonuses.gon`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1116

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 898 |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the item's desc. | 5441 |
| `frame` | Number |  | 2212 |
| [`kind`](./Enums.md#enum-kind) | Enum |  | 2212 |
| [`name`](./Strings.md#string-name) | String | Localization key for the item's name. | 5027 |
| [`rarity`](./Enums.md#enum-rarity) | Enum |  | 1934 |
| [`set`](./Enums.md#enum-set) | Enum |  | 1504 |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 730 |
| `shield` | Number |  | 422 |
| `durability` | Number | Maximum uses before breaking. | 264 |
| `cursed` | Boolean |  | 154 |
| `cha` | Number |  | 468 |
| `consumable` | Boolean |  | 140 |
| `spd` | Number |  | 424 |
| `con` | Number |  | 416 |
| `int` | Number |  | 401 |
| `lck` | Number |  | 351 |
| `quest_item` | Boolean |  | 80 |
| `parasite` | Boolean |  | 102 |
| `aux` | Number |  | 82 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum |  | 2364 |
| [`str`](./Engine_DamagingKeys.md#valid-property-keys) | Mixed |  | 337 |
| `dex` | Number |  | 301 |
| [`quest_reward_item`](./Enums.md#enum-quest_reward_item) | Enum |  | 44 |
| `indestructible` | Boolean |  | 40 |
| `legacy_quest` | Boolean |  | 34 |
| [`hint_destination`](./Enums.md#enum-hint_destination) | Enum |  | 32 |
| `divine_shield` | Number |  | 54 |
| [`str_aux_initialize`](./Enums.md#enum-str_aux_initialize) | Enum |  | 30 |
| `dont_destroy_on_0` | Boolean |  | 26 |
| [`global_tags`](./Arrays.md#array-global_tags) | Array |  | 12 |
| `max_durability` | Number |  | 22 |
| [`on_store`](./Enums.md#enum-on_store) | Enum |  | 16 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 26 |
| [`hint_prerequisite_flag`](./Enums.md#enum-hint_prerequisite_flag) | Enum |  | 10 |
| `failable` | Boolean |  | 8 |
| [`global_passives`](./Items_and_Equipment.md#context-global_passives) | Object |  | 8 |
| `randomize_piece_frames` | Boolean |  | 8 |
| `str_aux_is_copy_passive` | Boolean |  | 8 |
| `fragile` | Boolean |  | 6 |
| [`icon_hint`](./Enums.md#enum-icon_hint) | Enum |  | 6 |
| `max_health` | Number |  | 6 |
| `reset_aux_on_store` | Number |  | 6 |
| `sticky` | Boolean |  | 6 |
| `weightless` | Boolean |  | 6 |
| [`keyword_tooltips`](./Items_and_Equipment.md#context-keyword_tooltips) | Object | Forces specific UI tooltips to appear when hovering over the ability. | 62 |
| [`passive`](./Items_and_Equipment.md#context-passive) | Object |  | 4 |
| `prevent_level_up` | Boolean |  | 4 |
| [`quest_item_alias`](./Enums.md#enum-quest_item_alias) | Enum |  | 4 |
| `speed` | Number |  | 6 |
| [`str_aux_is_copy_ability`](./Items_and_Equipment.md#context-str_aux_is_copy_ability) | Object |  | 4 |
| `str_aux_is_copy_item_passive` | Boolean |  | 4 |
| `aux_is_catid` | Boolean |  | 2 |
| `cant_equip_to_colorless` | Boolean |  | 2 |
| `degrade_after_adventure` | Boolean |  | 2 |
| [`equip_sound`](./Enums.md#enum-equip_sound) | Enum |  | 2 |
| `force_sticky` | Boolean |  | 2 |
| [`reset_str_aux_on_store`](./Enums.md#enum-reset_str_aux_on_store) | Enum |  | 2 |
| [`Set`](./Enums.md#enum-set) | Enum | Applies or references the 'Set' effect/state. | 1504 |
| [`str_aux`](./Enums.md#enum-str_aux) | Enum |  | 2 |
| `str_aux_is_copy_item_active` | Boolean |  | 2 |
| `str_aux_is_copy_item_icon` | Boolean |  | 2 |

</details>

---

### Object: `passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 748

> **Referenced by:** [`PassiveAfterXKills`](./Items_and_Equipment.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Items_and_Equipment.md#context-passiveathealththreshold), [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold), [`PassiveIfStrAuxEquals`](./Items_and_Equipment.md#context-passiveifstrauxequals), [`PassiveWhenAffectedByElement`](./Items_and_Equipment.md#context-passivewhenaffectedbyelement), [`PassiveWhenOnTile`](./Items_and_Equipment.md#context-passivewhenontile), [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2609 |

</details>

---

### Object: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 65

> **Referenced by:** [`AddPassivesToMinions`](./Items_and_Equipment.md#context-addpassivestominions), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 119 |

</details>

---

### Object: `effects`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

> **Referenced by:** [`DoDamage`](./Items_and_Equipment.md#context-dodamage), [`MeleeRevengeDamage`](./Items_and_Equipment.md#context-meleerevengedamage), [`RevengeDamage`](./Items_and_Equipment.md#context-revengedamage), [`damage_instance`](./Items_and_Equipment.md#context-damage_instance)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 205 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 37 |
| [`BounceObject`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Spawns a physics object that visually bounces off the target. | 70 |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#object-conditional-goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 28 |
| `DestroyTrinket` | Number | Applies or references the 'DestroyTrinket' effect/state. | 6 |
| [`ForceUseAbility_NonStack`](./Engine_LogicKeys.md#valid-property-keys) | Enum/String | Applies or references the 'ForceUseAbility_NonStack' effect/state. | 0 |
| [`VisualFX`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'VisualFX' effect/state. | 20 |
| [`VisualFXTile`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'VisualFXTile' effect/state. | 72 |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 0 |

</details>

---

### Object: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 32

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 186 |
| `knockback` | Number |  | 48 |
| `damage` | Number | The base damage properties of an attack. | 44 |
  | [`AddDamageToElementDamage`](#adddamagetoelementdamage) | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 0 |
  | [`AddStatusToElementDamage`](#addstatustoelementdamage) | Object | Applies the 'AddStatusToElementDamage' effect. | 0 |
  | [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. | 0 |
  | [`StatusImmunity`](./Enums.md#enum-statusimmunity) | Enum | Applies or references the 'StatusImmunity' effect/state. | 0 |
| [`effects`](./Items_and_Equipment.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 94 |

</details>

---

### Object: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 25

> **Referenced by:** [`ApplyPassives`](./Items_and_Equipment.md#context-applypassives), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 50 |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 50 |

</details>

---

### Object: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 42 |

</details>

---

### Object: `StatusOnBreak`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |

</details>

---

### Object: `SpawnOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 72 |
| [`number`](./Arrays.md#array-number) | Array |  | 48 |

</details>

---

### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>



> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend), [`StatusOnKill`](./Items_and_Equipment.md#context-statusonkill), [`StatusOnTakeHealthOrShieldDamage`](./Items_and_Equipment.md#context-statusontakehealthorshielddamage), [`effects`](./Items_and_Equipment.md#context-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 82 |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 72 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 |
| `DestroyTrinket` | `Number` | Applies or references the 'DestroyTrinket' effect/state. | 2 |
| [`ForceUseAbility_NonStack`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'ForceUseAbility_NonStack' effect/state. | 8 |

</details>

---

### Object: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

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

### Object: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 30 |

</details>

---

### Object: `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |

</details>

---

### Object: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 76 |
| `good` | Boolean |  | 40 |
| `spawn_on_death_hit` | Boolean |  | 20 |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0 or percentage) of this occurring. | 24 |
| `number` | Number |  | 2 |

</details>

---

### Object: `SpawnEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array |  | 34 |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Probability (0.0 to 1.0 or percentage) of this occurring. | 40 |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum |  | 10 |

</details>

---

### Object: `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |

</details>

---

### Object: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 76 |
| `damage` | Number | The base damage properties of an attack. | 16 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
  | [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. | 0 |
| [`effects`](./Items_and_Equipment.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 58 |

</details>

---

### Object: `AddSelfStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |

</details>

---

### Object: `DurabilityTransform`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eq`](./Arrays.md#array-eq) | Array |  | 11 |
| [`ge`](./Arrays.md#array-ge) | Array |  | 4 |

</details>

---

### Object: `PassiveIfStrAuxEquals`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`value`](./Math_Equations.md) | Equation |  | 14 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusOnKillEnemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |

</details>

---

### Object: `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
| `must_do_damage` | Boolean |  | 6 |
  | [`Conditional_HasTag`](#conditionalhastag) | Object | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 0 |
  | [`KnockbackIfCrit`](#knockbackifcrit) | Object | Applies or references the 'KnockbackIfCrit' effect/state. | 0 |
  | `LeaveBehindRockOnKnockback` | Number | Applies or references the 'LeaveBehindRockOnKnockback' effect/state. | 0 |
  | [`Blind`](./Arrays.md#array-blind) | Array | Applies or references the 'Blind' effect/state. | 0 |
  | `NonLethal` | Integer | Applies the 'NonLethal' effect. | 0 |
  | [`Rot`](./Arrays.md#array-rot) | Array | Applies or references the 'Rot' effect/state. | 0 |
  | [`Conditional_HasStatus`](#conditionalhasstatus) | Object | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 0 |
  | `BonusKnockbackDamage` | Number | Applies or references the 'BonusKnockbackDamage' effect/state. | 0 |

</details>

---

### Object: `ApplyToSource`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus), [`Else`](./Items_and_Equipment.md#context-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 22 |

</details>

---

### Object: `GainCoinsRange`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak), [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number | Maximum coins granted. | 22 |
| `min` | Number | Minimum coins granted. | 22 |

</details>

---

### Object: `ItemAuxTransform`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`le`](./Arrays.md#array-le) | Array |  | 6 |
| [`ge`](./Arrays.md#array-ge) | Array |  | 2 |
| [`lt`](./Arrays.md#array-lt) | Array |  | 1 |

</details>

---

### Object: `PassiveWhenOnTile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |
| [`tile`](./Arrays.md#array-tile) | Array |  | 6 |

</details>

---

### Object: `StatusAlliesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |

</details>

---

### Object: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

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

### Object: `Temporary`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`Conditional_BadRoll`](./Items_and_Equipment.md#context-conditional_badroll), [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin), [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 112 |
| `stacks` | Number | Number of stacks or intensity to apply. | 114 |
| `expires_on_end_turn` | Boolean |  | 42 |
| `turns` | Number | Duration in turns. | 104 |
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 50 |

</details>

---

### Object: `TransformItemOnElementInfluence`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 10 |
| [`item`](./Enums.md#enum-item) | Enum | Item ID to reference. | 10 |
| `full_repair` | Boolean |  | 10 |

</details>

---

### Object: `AddDamageToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 18 |
| `damage` | Number | The base damage properties of an attack. | 18 |

</details>

---

### Object: `AddPassivesToMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 41 |

</details>

---

### Object: `ChanceToRevive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 8 |
| `stacks` | Number | Number of stacks or intensity to apply. | 10 |

</details>

---

### Object: `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage), [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 50 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 40 |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 40 |
  | [`ImmediateUseAbility_Instant`](./Enums.md#enum-immediateuseability_instant) | Enum | Applies or references the 'ImmediateUseAbility_Instant' effect/state. | 0 |
| [`ApplyToSource`](./Items_and_Equipment.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 6 |
| `FlatLeechIfDamaged` | `Number` | Applies or references the 'FlatLeechIfDamaged' effect/state. | 2 |
| [`RemoveStatusStacks`](./Items_and_Equipment.md#object-removestatusstacks) | Object | Removes a specific number of stacks of a status effect. | 2 |

</details>

---

### Object: `Craft`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`StatusIfUnusedActPoints`](./Items_and_Equipment.md#context-statusifunusedactpoints), [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 30 |
| [`slot`](./Enums.md#enum-slot) | Enum | Equipment slot (weapon, hat, face, chest, etc.). | 28 |
| `works_with_tech` | Boolean |  | 8 |

</details>

---

### Object: `DelayedAutoRevive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 12 |
| `rounds` | Number |  | 12 |

</details>

---

### Object: `PassiveAtHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 18 |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 18 |

</details>

---

### Object: `SpawnObjectOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |
| `count` | Number | Quantity. | 2 |
| `except_tiny` | Boolean |  | 2 |

</details>

---

### Object: `StatusOnTakeHealthOrShieldDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 39 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 37 |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#object-conditional-goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 2 |
| `DestroyTrinket` | Number | Applies or references the 'DestroyTrinket' effect/state. | 0 |
| [`ForceUseAbility_NonStack`](./Engine_LogicKeys.md#valid-property-keys) | Enum/String | Applies or references the 'ForceUseAbility_NonStack' effect/state. | 0 |
| `Metronome` | `Number` | Executes a random musical or metronome ability. | 2 |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 0 |

</details>

---

### Object: `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 |
| `count` | Number | Quantity. | 11 |

</details>

---

### Object: `global_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GlobalEnemyAutoRevive` | Number | Applies or references the 'GlobalEnemyAutoRevive' effect/state. | 4 |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `RealTimePressure` | Number | Applies or references the 'RealTimePressure' effect/state. | 2 |
| `NoCorpses` | `Number` | Applies or references the 'NoCorpses' effect/state. | 2 |

</details>

---

### Object: `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 20 |
| `ally_chance` | Number |  | 10 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 10 |

</details>

---

### Object: `ClassManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reduction` | Number |  | 14 |
| [`class`](./Enums.md#enum-class) | Enum | Character class identifier. | 12 |

</details>

---

### Object: `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ExtraStatusWhenDealingDamage`](./Items_and_Equipment.md#context-extrastatuswhendealingdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Else`](#else) | Object | Fallback object that executes if the preceding `Conditional_` block evaluated to false. | 0 |
  | [`Charmed`](./Arrays.md#array-charmed) | Array | Applies or references the 'Charmed' effect/state. | 0 |
  | [`ApplyPassives`](#applypassives) | Object | Grants the nested passive abilities dynamically. | 0 |
  | [`Conditional_IsSelf`](#conditional_isself) | Object | Conditional trigger: Executes nested logic if the target is the caster themselves. | 0 |

</details>

---

### Object: `CounterAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 10 |
| `melee_only` | Boolean |  | 2 |
| `ranged_only` | Boolean |  | 2 |

</details>

---

### Object: `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`Conditional_PartyMember`](./Items_and_Equipment.md#context-conditional_partymember)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 20 |

</details>

---

### Object: `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Conditional_PartyMember`](#conditional_partymember) | Object | Conditional constraint. Nested properties only trigger if this is true. | 0 |
  | [`Conditional_Ally`](#conditionalally) | Object | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 0 |

</details>

---

### Object: `PassiveWhenDead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`StatusEachRoundEnd`](#statuseachroundend) | Object | Applies or references the 'StatusEachRoundEnd' effect/state. | 0 |
  | [`StatusEachTurnBegin`](#statuseachturnbegin) | Object | Event Trigger: Applies nested statuses to each turn begin. | 0 |
  | [`AddStatusToTrampleDamage`](#addstatustotrampledamage) | Object | Applies the 'AddStatusToTrampleDamage' effect. | 0 |
  | [`AutocastEachRound`](#autocasteachround) | Object | Forces the character to automatically cast a specific ability at the start of each combat round. | 0 |

</details>

---

### Object: `SetItemAux`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`Conditional_Shielded`](./Items_and_Equipment.md#context-conditional_shielded), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum | Equipment slot (weapon, hat, face, chest, etc.). | 6 |
| [`value`](./Math_Equations.md) | Equation |  | 6 |

</details>

---

### Object: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 3 |
| [`object`](./Enums.md#enum-object) | Enum |  | 19 |

</details>

---

### Object: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array |  | 6 |
| [`object`](./Enums.md#enum-object) | Enum |  | 22 |

</details>

---

### Object: `StackingFlowerTrail`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum |  | 6 |
| `stacks` | Number | Number of stacks or intensity to apply. | 6 |

</details>

---

### Object: `StatusAllCharactersOnSpawn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 |
| `stacks` | Number | Number of stacks or intensity to apply. | 16 |

</details>

---

### Object: `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `StatusOnTurnEndIfDidntCastAbilityTypes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 8 |

</details>

---

### Object: `AddStatusToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 12 |
  | [`AddDamageToElementDamage`](#adddamagetoelementdamage) | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 0 |

</details>

---

### Object: `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Stun`](./Arrays.md#array-stun) | Array | Applies or references the 'Stun' effect/state. | 0 |
  | `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 0 |

</details>

---

### Object: `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `Leech` | Number | Applies or references the 'Leech' effect/state. | 0 |
  | `LeechPercent` | Integer | Applies the 'LeechPercent' effect. | 0 |
  | [`Conditional_Enemy`](#conditionalenemy) | Object | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 0 |

</details>

---

### Object: `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| `count` | Number | Quantity. | 4 |

</details>

---

### Object: `ArmorBreakOnHit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance_to_break` | Number |  | 4 |
| `durability_loss` | Number |  | 4 |

</details>

---

### Object: `BoostWeaponDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 |
| `damage` | Number | The base damage properties of an attack. | 8 |
| `crit_chance` | `Number` |  | 8 |

</details>

---

### Object: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 12 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 12 |

</details>

---

### Object: `ChanceToBlockAndCounter`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean |  | 2 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |

</details>

---

### Object: `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ScaledStatusAlliesOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusalliesonspendmana), [`StatusAlliesEachTurn`](./Items_and_Equipment.md#context-statusallieseachturn)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
  | [`Conditional_PlayerCat`](#conditional_playercat) | Object | Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 0 |
  | `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 0 |
  | [`Bleed`](./Arrays.md#array-bleed) | Number | Applies or references the 'Bleed' effect/state. | 0 |
  | [`Conditional_Ally`](#conditionalally) | Object | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 0 |
  | `BonusCritChance` | Integer | Applies the 'BonusCritChance' effect. | 0 |
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 0 |

</details>

---

### Object: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
| [`odds`](./Enums.md#enum-odds) | Enum | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 16 |

</details>

---

### Object: `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusAllCharactersOnSpawn`](./Items_and_Equipment.md#context-statusallcharactersonspawn)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |
  | `ExplodeCharacter_PartyBoss` | Integer | Applies or references the 'ExplodeCharacter_PartyBoss' effect/state. | 0 |
  | `ExplodeCharacter_RockCrusher_PetrifyBreak` | Integer | Applies or references the 'ExplodeCharacter_RockCrusher_PetrifyBreak' effect/state. | 0 |

</details>

---

### Object: `Conditional_OncePerBattle`


**Definition:** Conditional trigger: Executes nested logic only once per encounter/battle.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>



> **Referenced by:** [`Conditional_HealthThreshold`](./Items_and_Equipment.md#context-conditional_healththreshold), [`StatusOnFullMana`](./Items_and_Equipment.md#context-statusonfullmana)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |
| [`key`](./Enums.md#enum-key) | Enum |  | 6 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`ShowText`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ShowText' effect/state. | 2 |

</details>

---

### Object: `CreateGlobalModifiers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| `NextPlayerCatTakesExtraTurn` | `Number` | Applies or references the 'NextPlayerCatTakesExtraTurn' effect/state. | 2 |
| `NoCorpses` | `Number` | Applies or references the 'NoCorpses' effect/state. | 2 |

</details>

---

### Object: `DoDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusEachRoundEnd`](./Items_and_Equipment.md#context-statuseachroundend), [`StatusOnBreakItem`](./Items_and_Equipment.md#context-statusonbreakitem)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 36 |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum |  | 8 |
| [`type`](./Enums.md#enum-type) | Enum | The classification of the damage (e.g., spell, melee). | 14 |
| `damage` | Number | The flat damage amount. | 14 |
| [`effects`](./Items_and_Equipment.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 8 |

</details>

---

### Object: `ElementalManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array | Specific element type required or applied. | 4 |
| `reduction` | Number |  | 10 |

</details>

---

### Object: `ImmediateUseAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 2 |
| `even_if_stunned` | Boolean |  | 2 |

</details>

---

### Object: `ModifyAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bonus_passives`](./Items_and_Equipment.md#context-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cost`](./Items_and_Equipment.md#context-cost) | Object | Currency value in shops/merchants. | 4 |
| [`meta`](./Items_and_Equipment.md#context-meta) | Object |  | 4 |

</details>

---

### Object: `MovementReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`PassiveWhileHasDurability`](./Items_and_Equipment.md#context-passivewhilehasdurability), [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 22 |
| `create_temp_ability` | Boolean |  | 4 |
| `enemies_only` | Boolean |  | 14 |
| `on_self_move_too` | Boolean |  | 6 |

</details>

---

### Object: `ObjectOnHitCharacter`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusEveryXSpellCasts`](./Items_and_Equipment.md#context-statuseveryxspellcasts), [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the character to spawn (e.g., CharmedFlea). | 14 |
| [`stacks`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Number of stacks or intensity to apply. | 10 |

</details>

---

### Object: `PassiveAtStatThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 26 |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 26 |

</details>

---

### Object: `PassiveIfWeaponIsUsable`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `RefreshEquipmentAbilityOnElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 4 |
| [`text`](./Strings.md#string-text) | String |  | 4 |

</details>

---

### Object: `SpawnItemLinkedFamiliar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 4 |
| `break_on_pop_only` | Boolean |  | 4 |

</details>

---

### Object: `StatusAfterCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusAfterXStacks`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusonspendmana), [`StatusOnCollectPickup`](./Items_and_Equipment.md#context-statusoncollectpickup)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum |  | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `expires_on_end_turn` | Boolean |  | 2 |

</details>

---

### Object: `StatusIfUnusedActPoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `Craft` | Object | Synthesizes or spawns a new item from a specific pool. | 0 |
  | `BackflipWhenTargeted` | Object | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. | 0 |

</details>

---

### Object: `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |

</details>

---

### Object: `StatusOnBackstab`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `SerratedClaws` | Number | Applies or references the 'SerratedClaws' effect/state. | 2 |

</details>

---

### Object: `StatusOnBreakItem`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |

</details>

---

### Object: `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `bonus_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`str_aux_is_copy_ability`](./Items_and_Equipment.md#context-str_aux_is_copy_ability)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 125 |

</details>

---

### Object: `cost`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ModifyAbility`](./Items_and_Equipment.md#context-modifyability)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `charge` | Number |  | 36 |
| `mana` | Number |  | 3210 |

</details>

---

### Object: `keyword_tooltips`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |

</details>

---

### Object: `meta`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ModifyAbility`](./Items_and_Equipment.md#context-modifyability)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `is_basic_attack` | Boolean |  | 12 |
| `is_weapon` | Boolean |  | 8 |

</details>

---

### Object: `passive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `str_aux_is_copy_ability`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`bonus_passives`](./Items_and_Equipment.md#context-bonus_passives) | Object | Passives granted to the character while this ability is equipped. | 4 |

</details>

---

### Object: `threshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 2 |
| `int` | Number |  | 16 |

</details>

---

### Object: `AIControlNextTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean |  | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Object: `AbilityHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 26 |
| `aux` | Number |  | 2 |
| `even_if_stunned` | Boolean |  | 14 |
| `immediate` | Boolean |  | 12 |

</details>

---

### Object: `AbilityOnRoundEndOnce`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 2 |
| `even_of_stunned` | Boolean |  | 2 |

</details>

---

### Object: `AddAdvantageToEvent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 2 |
| `add` | Number |  | 2 |
  | `treasure_box` | Any | Explicit empirical property. | 0 |

</details>

---

### Object: `AddPassivesToCharmed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |

</details>

---

### Object: `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `ChanceToBreak` | Number | Applies or references the 'ChanceToBreak' effect/state. | 0 |
  | [`RepairWeapon`](./Arrays.md#array-repairweapon) | Number | Applies or references the 'RepairWeapon' effect/state. | 0 |

</details>

---

### Object: `AddStatusToBackstabs`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CastAgainWithStatus`](./Items_and_Equipment.md#context-castagainwithstatus) | Object | Applies or references the 'CastAgainWithStatus' effect/state. | 2 |

</details>

---

### Object: `AlluringDoodieEater`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage_instance`](./Items_and_Equipment.md#context-damage_instance) | Object |  | 2 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |

</details>

---

### Object: `AllyDodgeChanceAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |
| `range` | Number | Distance or area of effect in tiles. | 2 |

</details>

---

### Object: `ApplyPassives`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_RandomChance`](./Items_and_Equipment.md#context-conditional_randomchance)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 13 |

</details>

---

### Object: `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`GainDisorderFromPool_PostCast`](./Enums.md#enum-gaindisorderfrompool_postcast) | Enum | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 0 |
  | [`GainDisorderFromPool`](./Enums.md#enum-gaindisorderfrompool) | Object | Logic: Applies a negative mutation/disorder from a specific pool. | 0 |

</details>

---

### Object: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 18 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 12 |

</details>

---

### Object: `BackflipWhenTargeted`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific dodge ability to trigger (e.g., DestroyerDodge). | 14 |
| `stacks` | Number | Number of stacks or intensity to apply. | 14 |

</details>

---

### Object: `BouncyProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number |  | 6 |
| `max_range` | Number |  | 6 |

</details>

---

### Object: `BuffImmunity`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exclude`](./Enums.md#enum-exclude) | Enum |  | 2 |

</details>

---

### Object: `CastAgainWithStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddTemporaryEffectsToBasicAttack`](./Items_and_Equipment.md#context-addtemporaryeffectstobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 2 |

</details>

---

### Object: `CatPartsSizeScale`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `head` | Number |  | 2 |

</details>

---

### Object: `ChanceToForceEvent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`event`](./Enums.md#enum-event) | Enum |  | 2 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |

</details>

---

### Object: `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 |

</details>

---

### Object: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToSpells`](./Items_and_Equipment.md#context-addstatustospells)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
  | [`Conditional_FinishedSpawning`](#conditional_finishedspawning) | Object | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. | 0 |
  | `DisplaceToAbilityTarget` | Integer | Applies or references the 'DisplaceToAbilityTarget' effect/state. | 0 |
  | `DontHealEnemies` | Integer | Applies or references the 'DontHealEnemies' effect/state. | 0 |

</details>

---

### Object: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 91 |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. | 91 |
  | `EventBounty` | Integer | Applies or references the 'EventBounty' effect/state. | 0 |
  | [`MergeDamageInstance`](#mergedamageinstance) | Object | Combines damage numbers or visual hit effects. | 0 |
  | [`SetAnimationAlts`](#setanimationalts) | Object | Overrides specific animation states with alternative animations. | 0 |

</details>

---

### Object: `Conditional_HealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 |
| `threshold_flat` | Number | A flat numerical health value threshold. | 10 |
| [`Conditional_OncePerBattle`](./Items_and_Equipment.md#object-conditional-onceperbattle) | Object | Conditional trigger: Executes nested logic only once per encounter/battle. | 2 |
| [`ShowText`](./Engine_LogicKeys.md#valid-property-keys) | String | Applies or references the 'ShowText' effect/state. | 0 |
| `key` | Enum/String |  | 0 |

</details>

---

### Object: `Conditional_ManaThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `threshold_flat` | Number |  | 2 |

</details>

---

### Object: `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 |
| `odds` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 8 |
| [`ApplyPassives`](./Items_and_Equipment.md#object-applypassives) | Object | Grants the nested passive abilities dynamically. | 4 |

</details>

---

### Object: `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `SetItemAux` | Object | Applies or references the 'SetItemAux' effect/state. | 0 |
  | `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 0 |
  | `Cleave` | Object | Causes the attack to hit adjacent enemies alongside the primary target. | 0 |
  | [`Stun`](./Arrays.md#array-stun) | Array | Applies or references the 'Stun' effect/state. | 0 |
  | `BonusCritChance` | Integer | Applies the 'BonusCritChance' effect. | 0 |

</details>

---

### Object: `ConvertDamageToScaledStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Object: `CritsApplyStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `DestroyEquipmentAndAttachParasite`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0 or percentage) of this occurring. | 8 |
| [`pool`](./Arrays.md#array-pool) | Array | The item pool to draw the parasite from. | 4 |

</details>

---

### Object: `Eternal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health_percent` | Number |  | 6 |
| `stacks` | Number | Number of stacks or intensity to apply. | 6 |

</details>

---

### Object: `FlyDamageIncrease`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Object: `ForceUseAbilityOnTarget`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 2 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |

</details>

---

### Object: `GlobalMeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `knockback` | Number |  | 2 |

</details>

---

### Object: `KnockUpAndAway`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | The distance in tiles to knock the target away. | 48 |
| `stacks` | Number | Number of stacks or intensity to apply. | 44 |

</details>

---

### Object: `KnockbackIfCrit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `knockback` | Number |  | 2 |
| `override_chain_knockback` | Number |  | 2 |

</details>

---

### Object: `ManaGainRange`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number |  | 2 |
| `min` | Number |  | 2 |

</details>

---

### Object: `ObjectDetector`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |

</details>

---

### Object: `PassiveAfterXKills`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |
| `stacks` | Number | Number of stacks or intensity to apply. | 8 |

</details>

---

### Object: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 36 |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 36 |

</details>

---

### Object: `PassiveWhileHasDurability`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`MovementReaction`](#movementreaction) | Object | Reaction: Triggers an effect or ability when forced to move. | 0 |

</details>

---

### Object: `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `PassiveWhileShielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `PoopWhenHit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |

</details>

---

### Object: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 31 |

</details>

---

### Object: `RemoveStatusStacks`



<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 8 |
| `stacks` | Number | The number of stacks to remove. | 8 |

</details>

---

### Object: `ReviveNextRound`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `revive_health` | Number | The flat amount of health to revive with. | 8 |

</details>

---

### Object: `ScaldingOrbMoonBossOneShot`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`CompleteItemQuest`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'CompleteItemQuest' effect/state. | 2 |
| [`RemoveItem`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'RemoveItem' effect/state. | 2 |

</details>

---

### Object: `ScaledStatusAlliesOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Conditional_Adjacent`](#conditional_adjacent) | Object | Conditional constraint. Nested properties only trigger if this is true. | 0 |

</details>

---

### Object: `ScaledStatusOnHolyShieldBlock`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `ScaledStatusOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `SpawnOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 8 |
| [`obj`](./Enums.md#enum-obj) | Enum |  | 4 |

</details>

---

### Object: `SpawnRandomPickupsOnTaggedUnitKilled`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array | Quantity. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 2 |

</details>

---

### Object: `StatDependentPassive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusAdjacentOnTheirTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `ForceMoveAway` | `Number` | Applies or references the 'ForceMoveAway' effect/state. | 2 |

</details>

---

### Object: `StatusAfterXTurns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| `stacks` | Number | Number of stacks or intensity to apply. | 4 |

</details>

---

### Object: `StatusAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. | 0 |
  | `exclude_self` | Boolean | `false` | 0 |
  | [`Conditional_Adjacent`](#conditional_adjacent) | Object | Conditional constraint. Nested properties only trigger if this is true. | 0 |

</details>

---

### Object: `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |

</details>

---

### Object: `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |

</details>

---

### Object: `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnDodge`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `StatusOnEnemyDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnFallAsleep`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
  | [`AllStatsUp`](./Arrays.md#array-allstatsup) | Number | Applies or references the 'AllStatsUp' effect/state. | 0 |
  | [`FillMana`](./Arrays.md#array-fillmana) | Number | Applies or references the 'FillMana' effect/state. | 0 |
  | `HealRandomInjury` | Integer | Applies or references the 'HealRandomInjury' effect/state. | 0 |

</details>

---

### Object: `StatusOnFullMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`Conditional_OncePerBattle`](./Items_and_Equipment.md#object-conditional-onceperbattle) | Object | Conditional trigger: Executes nested logic only once per encounter/battle. | 2 |
| [`ShowText`](./Engine_LogicKeys.md#valid-property-keys) | String | Applies or references the 'ShowText' effect/state. | 0 |
| `key` | Enum/String |  | 0 |

</details>

---

### Object: `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `TempPassiveUntilSettled`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnEatFood`](./Items_and_Equipment.md#context-statusoneatfood)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `TintItem`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`add`](./Arrays.md#array-add) | Array |  | 1 |
| [`ignore_if_str_aux_equals`](./Enums.md#enum-ignore_if_str_aux_equals) | Enum |  | 2 |
| [`mul`](./Arrays.md#array-mul) | Array |  | 1 |

</details>

---

### Object: `TransformWeapon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | The original weapon ID. | 4 |
| [`to`](./Enums.md#enum-to) | Enum | The transformed weapon ID. | 4 |

</details>

---

### Object: `TunnelVision`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `crit_chance` | `Number` |  | 2 |

</details>

---

### Object: `damage_instance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AlluringDoodieEater`](./Items_and_Equipment.md#context-alluringdoodieeater)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7186 |
| [`type`](./Enums.md#enum-type) | Enum | Classification type. | 718 |
| `damage` | Number | The base damage properties of an attack. | 2894 |
| [`effects`](./Items_and_Equipment.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 3574 |

</details>

---

