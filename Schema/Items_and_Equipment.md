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
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4118 |
| `frame` | Number | {'type': '`Number`', 'df': ''} | 1106 |
| [`kind`](./Enums.md#enum-kind) | Enum | {'type': '`Enum/String`', 'df': ''} | 1106 |
| [`rarity`](./Enums.md#enum-rarity) | Enum | {'type': '`Enum/String`', 'df': ''} | 967 |
| [`set`](./Enums.md#enum-set) | Enum | {'type': '`Enum/String`', 'df': ''} | 765 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1549 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2609 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 65

> **Referenced by:** [`AddPassivesToMinions`](./Items_and_Equipment.md#context-addpassivestominions), [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 119 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

> **Referenced by:** [`DoDamage`](./Items_and_Equipment.md#context-dodamage), [`MeleeRevengeDamage`](./Items_and_Equipment.md#context-meleerevengedamage), [`RevengeDamage`](./Items_and_Equipment.md#context-revengedamage), [`damage_instance`](./Items_and_Equipment.md#context-damage_instance)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 552 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1886 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 32

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 36 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 56 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 42 |

</details>

---

### Context: `StatusOnBreak`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 11 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 14 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 40 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 20 |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 30 |

</details>

---

### Context: `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 10 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 9 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 10 |

</details>

---

### Context: `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 12 |
| `must_do_damage` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus), [`Else`](./Items_and_Equipment.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 22 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 41 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 22 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 23 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 15 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |

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
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | All valid keys from the specified engine key are applicable to this context/block. | 1 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |
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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 20 |

</details>

---

### Context: `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `PassiveWhenDead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 9 |

</details>

---

### Context: `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

</details>

---

### Context: `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
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
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |

</details>

---

### Context: `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_HealthThreshold`](./Items_and_Equipment.md#context-conditional_healththreshold), [`StatusOnFullMana`](./Items_and_Equipment.md#context-statusonfullmana)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |
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
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | All valid keys from the specified engine key are applicable to this context/block. | 5 |

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
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 7 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 31 |

</details>

---

### Context: `PassiveIfWeaponIsUsable`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |

</details>

---

### Context: `StatusOnBackstab`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |

</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `bonus_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`str_aux_is_copy_ability`](./Items_and_Equipment.md#context-str_aux_is_copy_ability)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 125 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 10 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 12 |

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
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 9 |

</details>

---

### Context: `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `AddStatusToBackstabs`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 13 |

</details>

---

### Context: `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 16 |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToSpells`](./Items_and_Equipment.md#context-addstatustospells)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 49 |
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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 9 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `ConvertDamageToScaledStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 30 |

</details>

---

### Context: `PassiveWhileHasDurability`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `PassiveWhileShielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 31 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `ScaledStatusAlliesOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `ScaledStatusOnHolyShieldBlock`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `ScaledStatusOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusAdjacentOnTheirTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusAfterXTurns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |

</details>

---

### Context: `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`PassiveWhenDead`](./Items_and_Equipment.md#context-passivewhendead)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |

</details>

---

### Context: `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusOnDodge`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `StatusOnEnemyDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusOnFallAsleep`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusOnFullMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `TempPassiveUntilSettled`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnEatFood`](./Items_and_Equipment.md#context-statusoneatfood)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

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
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

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
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1731 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'Classification type.'} | 1 |

</details>

---

