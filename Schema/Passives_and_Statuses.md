# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Passives & Statuses

> **Associated Files:** `data/passives/, data/passive_pools.gon`


### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 885

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4118 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1549 |
| [`class`](./Enums.md#enum-class) | Enum | {'type': '`Enum/String`', 'df': 'Character class identifier.'} | 510 |
| [`stats`](./Passives_and_Statuses.md#context-stats) | Block | {'type': '`Block`', 'df': ' | 97 |
| `con` | Number | {'type': 'Number', 'df': ''} | 18 |
| `spd` | Number | {'type': 'Number', 'df': ''} | 17 |
| [`lock_item_slot`](./Passives_and_Statuses.md#context-lock_item_slot) | Block | {'type': '`Block`', 'df': ' | 16 |
| `cha` | Number | {'type': 'Number', 'df': ''} | 13 |
| `int` | Number | {'type': 'Number', 'df': ''} | 12 |
| `str` | Number | {'type': 'Number', 'df': ''} | 12 |
| [`desc_multiclass`](./Strings.md#string-desc_multiclass) | String | {'type': '`String`', 'df': ''} | 10 |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 10 |
| `lck` | Number | {'type': 'Number', 'df': ''} | 9 |
| `shield` | Number | {'type': '`Number`', 'df': ''} | 9 |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | {'type': '`Array`', 'df': 'Flat addition to a base value.'} | 8 |
| `dex` | Number | {'type': 'Number', 'df': ''} | 8 |
| `divine_shield` | Number | Examples: `3, 1` | 6 |
| [`keyword_tooltips`](./Passives_and_Statuses.md#context-keyword_tooltips) | Block | Examples: `{ ... }` | 6 |
| `auto_plus_signs_on_name` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| [`empty_armor_scaled_stats`](./Passives_and_Statuses.md#context-empty_armor_scaled_stats) | Block | Examples: `{ ... }` | 4 |
| [`name_mod`](./Strings.md#string-name_mod) | String | {'type': '`String`', 'df': ''} | 4 |
| [`tags`](./Arrays.md#array-tags) | Array | {'type': '`Array`', 'df': ''} | 3 |
| [`icon`](./Enums.md#enum-icon) | Enum | Examples: `DejaVu3, DejaVu2` | 2 |
| [`schadenfreude_scaled_stats`](./Passives_and_Statuses.md#context-schadenfreude_scaled_stats) | Block | Examples: `{ ... }` | 2 |
| [`grant_ability`](./Enums.md#enum-grant_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 884

> **Referenced by:** [`PassiveAfterXKills`](./Passives_and_Statuses.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#context-passiveathealththreshold), [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#context-passiveatinjurythreshold), [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold), [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement), [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2609 |

</details>

---

### Context: `stats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 97

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number | {'type': '`Number`', 'df': ''} | 31 |
| `spd` | Number | {'type': '`Number`', 'df': ''} | 26 |
| `cha` | Number | {'type': '`Number`', 'df': ''} | 22 |
| `int` | Number | {'type': '`Number`', 'df': ''} | 22 |
| `str` | Number | {'type': '`Number`', 'df': ''} | 20 |
| `dex` | Number | {'type': '`Number`', 'df': ''} | 16 |
| `lck` | Number | {'type': '`Number`', 'df': ''} | 13 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 92

> **Referenced by:** [`AddPassivesToCharmed`](./Passives_and_Statuses.md#context-addpassivestocharmed), [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#context-passivewhenatfullmana), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 119 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 30

> **Referenced by:** [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#context-damageneighborsaftermove), [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#context-damageneighborsonendmove), [`GravityWell`](./Passives_and_Statuses.md#context-gravitywell), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`RevengeDamage`](./Passives_and_Statuses.md#context-revengedamage), [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#context-smiteenemieswhokill), [`fire`](./Passives_and_Statuses.md#context-fire), [`ice`](./Passives_and_Statuses.md#context-ice), [`lightning`](./Passives_and_Statuses.md#context-lightning), [`triattack`](./Passives_and_Statuses.md#context-triattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 552 |

</details>

---

### Context: `AddPassivesToMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 29

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 41 |

</details>

---

### Context: `SpawnOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array | {'type': '`Enum/String`', 'df': ''} | 14 |
| [`number`](./Arrays.md#array-number) | Array | {'type': '`Number`', 'df': ''} | 13 |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 30 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 42 |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | {'type': '`Boolean`', 'df': 'If true, triggers the effect even if the character died during the battle.'} | 10 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 56 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 20 |

</details>

---

### Context: `lock_item_slot`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum | {'type': '`Enum/String`', 'df': ''} | 16 |
| `frame` | Number | {'type': '`Number`', 'df': ''} | 3 |

</details>

---

### Context: `StatusOnStanceSwitch`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#context-passiveifemptyface), [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#context-passiveifemptyhead), [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#context-passiveifemptyneck), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 11 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `SpreadDisease`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`effects`](./Passives_and_Statuses.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`disease`](./Enums.md#enum-disease) | Enum | {'type': '`Enum/String`', 'df': 'The specific status effect ID representing the disease.'} | 12 |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of transmitting.'} | 11 |
| `can_apply_to_anything` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

</details>

---

### Context: `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#context-conditional_sourcehastag), [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#context-extrastatuswhendealingdamage), [`StatusKilledCharacters`](./Passives_and_Statuses.md#context-statuskilledcharacters)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 16 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 29 |

</details>

---

### Context: `CritsApplyStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `Temporary`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`Conditional_BadRoll`](./Passives_and_Statuses.md#context-conditional_badroll), [`StatusOnGainShield`](./Passives_and_Statuses.md#context-statusongainshield), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage), [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#context-statusonturnendifmanaorhealthexact)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 11 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The status effect to apply.'} | 11 |
| `turns` | Number | {'type': '`Number`', 'df': 'Duration in turns.'} | 8 |
| `expires_on_end_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| `expires_on_begin_turn` | Boolean | {'type': '`Boolean`', 'df': 'If true, ticks down at the start of the turn rather than the end.'} | 5 |

</details>

---

### Context: `PassiveAtStatThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum | {'type': '`Enum/String`', 'df': ''} | 10 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 31 |

</details>

---

### Context: `threshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `int` | Number | {'type': '`Number`', 'df': ''} | 6 |
| `cha` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `spd` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 10 |
| `knockback` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 36 |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 4 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 45 |

</details>

---

### Context: `PassiveIfAllArmorEmpty`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 9 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`StatusOnGainCoins`](./Passives_and_Statuses.md#context-statusongaincoins), [`StatusOnHealed`](./Passives_and_Statuses.md#context-statusonhealed), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 31 |

</details>

---

### Context: `StatusOnCrit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_NotBoss`](./Passives_and_Statuses.md#context-conditional_notboss)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `DamageNeighborsOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 7 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 7 |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 7 |
| `knockback` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `ForceUseAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin), [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 3 |
| `chance` | Mixed | {'type': '`Enum/String`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 3 |

</details>

---

### Context: `PassiveIfEmptyFace`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |

</details>

---

### Context: `PassiveIfEmptyHead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |

</details>

---

### Context: `PassiveIfEmptyNeck`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |

</details>

---

### Context: `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |
| `triggers_limit` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `StatusOnUseAbilityWithTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The specific entity tag required or applied.'} | 7 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |
| `exclude_basicattack` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `AddStatusToElementAbilities`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'The specific element type required or applied.'} | 6 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `CureDisease`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 6 |
| [`disease`](./Enums.md#enum-disease) | Enum | {'type': '`Enum/String`', 'df': ''} | 6 |
| `can_apply_to_anything` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 20 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 71 |

</details>

---

### Context: `ManaCostReductionTagged`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reduction` | Number | {'type': '`Number`', 'df': ''} | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The specific entity tag required or applied.'} | 6 |

</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array | {'type': '`Enum/String`', 'df': ''} | 6 |
| `chance` | Mixed | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 5 |
| `number` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `good` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 6 |
| `good` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| `spawn_on_death_hit` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `consider_all_layers` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 10 |

</details>

---

### Context: `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 12 |

</details>

---

### Context: `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |

</details>

---

### Context: `StatusOnOverHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| `SpawnScaledRotFly` | Number | {'type': '`Number`', 'df': "Applies the 'SpawnScaledRotFly' effect."} | 1 |

</details>

---

### Context: `AddDamageToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 4 |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'The specific element type required or applied.'} | 4 |

</details>

---

### Context: `AddPassivesToCharmed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 9 |

</details>

---

### Context: `AddStatusToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'The specific element type required or applied.'} | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

</details>

---

### Context: `AddStatusToExplosions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddElement`](./Enums.md#enum-addelement) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'AddElement' effect."} | 8 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `AllyBonusAbilityAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 2 |
| `square` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `AllyManaRegenAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum | {'type': '`Enum/String`', 'df': 'Distance or area of effect in tiles.'} | 4 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 4 |

</details>

---

### Context: `AmplifyStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `addstacks` | Number | {'type': '`Number`', 'df': ''} | 3 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the status effect to check or apply.'} | 3 |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to autocast.'} | 4 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': 'If true, bypasses stun and hard-CC restrictions to cast anyway.'} | 2 |
| `force_display_name` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill), [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#context-statusonuseabilitywithtag)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `DistanceBonusDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 4 |

</details>

---

### Context: `EMP`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`spell_graphics_override`](./Passives_and_Statuses.md#context-spell_graphics_override) | Block | {'type': '`Block`', 'df': ' | 4 |
| [`status_explosion_override`](./Enums.md#enum-status_explosion_override) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |

</details>

---

### Context: `PassiveAtHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 15 |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'The specific element type required or applied.'} | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 30 |

</details>

---

### Context: `PassiveWhenAtFullMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `StatusAlliesOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |

</details>

---

### Context: `StatusOnTurnEndIfCastNSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `spells` | Number | {'type': '`Number`', 'df': ''} | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `StatusOnTurnEndIfManaExact`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `mana` | Number | {'type': '`Number`', 'df': ''} | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `StatusOnTurnEndIfManaOrHealthExact`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `mana` | Number | {'type': '`Number`', 'df': ''} | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `empty_armor_scaled_stats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `int` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `spd` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `spell_graphics_override`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`EMP`](./Passives_and_Statuses.md#context-emp)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `AbilityReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 1 |
| `ability_damage_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `chance` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 1 |

</details>

---

### Context: `AddSelfStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 9 |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | {'type': '`Number`', 'df': "Applies the 'CastAgain' effect."} | 2 |
| `Fury` | Number | {'type': '`Number`', 'df': "Applies the 'Fury' effect."} | 1 |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |
| [`odds`](./Enums.md#enum-odds) | Enum | {'type': '`Enum/String`', 'df': "The probability (0.0 to 1.0) of triggering the 'bad roll' failure state."} | 3 |

</details>

---

### Context: `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The specific status ID to check for.'} | 3 |

</details>

---

### Context: `DeathRattle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 2 |
| `pop_corpse` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `ElementalManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array | {'type': '`Enum/String`', 'df': 'The specific element type required or applied.'} | 3 |
| `reduction` | Number | {'type': '`Number`', 'df': ''} | 3 |

</details>

---

### Context: `FindItemFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | {'type': '`Enum/String`', 'df': 'Probability of finding the item.'} | 1 |
| [`pool`](./Enums.md#enum-pool) | Enum | {'type': '`Enum/String`', 'df': 'The item pool to draw from.'} | 1 |

</details>

---

### Context: `MoveTowardsDamageSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| `move_far` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |

</details>

---

### Context: `ObjectOnHitCharacter`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend), [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#context-statuseachturnendperenemykill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': 'The entity ID of the character to spawn (e.g., CharmedFlea).'} | 3 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 3 |

</details>

---

### Context: `SpawnCatCopyOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array | {'type': '`Array`', 'df': ''} | 3 |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |

</details>

---

### Context: `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 9 |

</details>

---

### Context: `StatusGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |

</details>

---

### Context: `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `StatusOnKillEnemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 10 |

</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `statuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ChanceToRevive`](./Passives_and_Statuses.md#context-chancetorevive), [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#context-statusonbattleendifkillthresholdmet)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 2 |
| `range` | Mixed | {'type': '`Enum/String`', 'df': 'Distance or area of effect in tiles.'} | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The specific entity tag required or applied.'} | 2 |

</details>

---

### Context: `AddPassiveToSpawnedRocks`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddFilledMaxHealth` | Number | {'type': '`Number`', 'df': "Applies the 'AddFilledMaxHealth' effect."} | 2 |
| `JoinSpawnerFaction` | Number | {'type': '`Number`', 'df': "Applies the 'JoinSpawnerFaction' effect."} | 2 |

</details>

---

### Context: `AddPassivesToSummonAbilityMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `AddStatusToAllDamageAbilities`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `AddStatusToBasicAttackWithCooldown`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `AddStatusToFirstBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `AddStatusToMeleeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DelayedWind`](./Passives_and_Statuses.md#context-delayedwind) | Block | {'type': '`Block`', 'df': "Applies the 'DelayedWind' effect. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `AddStatusToTrampleDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `AllyHealthRegenAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum | {'type': '`Enum/String`', 'df': 'Distance or area of effect in tiles.'} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 2 |

</details>

---

### Context: `AlternateCraftingPools`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tinkerer_0`](./Enums.md#enum-tinkerer_0) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`tinkerer_1`](./Enums.md#enum-tinkerer_1) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `ApplyStatusIfCrit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| `count` | Number | {'type': '`Number`', 'df': 'The numerical quantity.'} | 1 |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 22 |

</details>

---

### Context: `AutocastEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 1 |
| `advantage_polarity` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `chance` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 1 |

</details>

---

### Context: `BoobyTrapItems`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`on_break`](./Passives_and_Statuses.md#context-on_break) | Block | {'type': '`Block`', 'df': " | 2 |
| [`on_throw`](./Passives_and_Statuses.md#context-on_throw) | Block | {'type': '`Block`', 'df': " | 2 |

</details>

---

### Context: `BoostWeaponDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 2 |

</details>

---

### Context: `BouncyProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `max_range` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `CatAPultAnimation`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 2 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |
| `ally_chance` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `chance` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 2 |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 2 |
| `chance` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 2 |

</details>

---

### Context: `ChangeTile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `aoe` | Number | {'type': '`Number`', 'df': 'The area of effect or distance in tiles.'} | 1 |
| [`tile`](./Enums.md#enum-tile) | Enum | {'type': '`Enum/String`', 'df': 'The specific tile type to change into (e.g., GlassTile).'} | 1 |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`class`](./Enums.md#enum-class) | Enum | {'type': '`Enum/String`', 'df': 'Character class identifier.'} | 2 |
| `reduction` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `Conditional_Adjacent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToElementDamage`](./Passives_and_Statuses.md#context-addstatustoelementdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 10 |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToAllDamage`](./Passives_and_Statuses.md#context-addstatustoalldamage), [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The specific string tag to check for.'} | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 49 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 63 |

</details>

---

### Context: `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `Conditional_PartyMember`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `Craft`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`slot`](./Enums.md#enum-slot) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `DamageNeighborTilesWhenCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`fire`](./Passives_and_Statuses.md#context-fire) | Block | {'type': '`Block`', 'df': ' | 1 |
| [`ice`](./Passives_and_Statuses.md#context-ice) | Block | {'type': '`Block`', 'df': ' | 1 |
| [`lightning`](./Passives_and_Statuses.md#context-lightning) | Block | {'type': '`Block`', 'df': ' | 1 |
| [`triattack`](./Passives_and_Statuses.md#context-triattack) | Block | {'type': '`Block`', 'df': ' | 1 |

</details>

---

### Context: `DamageNeighborsAfterMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': 'The base damage properties of an attack.'} | 2 |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 2 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 2 |

</details>

---

### Context: `DamageReductionAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| [`range`](./Enums.md#enum-range) | Enum | {'type': '`Enum/String`', 'df': 'Distance or area of effect in tiles.'} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 2 |

</details>

---

### Context: `Earth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': 'The base damage properties of an attack.'} | 2 |

</details>

---

### Context: `Electric`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `ElementalAttunement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Earth`](./Passives_and_Statuses.md#context-earth) | Block | {'type': '`Block`', 'df': "Applies the 'Earth' effect. | 2 |
| [`Electric`](./Passives_and_Statuses.md#context-electric) | Block | {'type': '`Block`', 'df': "Applies the 'Electric' effect. | 2 |
| [`Fire`](./Passives_and_Statuses.md#context-fire) | Block | {'type': '`Block`', 'df': "Applies the 'Fire' effect. | 2 |
| [`Grass`](./Passives_and_Statuses.md#context-grass) | Block | {'type': '`Block`', 'df': "Applies the 'Grass' effect. | 2 |
| [`Gravity`](./Passives_and_Statuses.md#context-gravity) | Block | {'type': '`Block`', 'df': "Applies the 'Gravity' effect. | 2 |
| [`Holy`](./Passives_and_Statuses.md#context-holy) | Block | {'type': '`Block`', 'df': "Applies the 'Holy' effect. | 2 |
| [`Ice`](./Passives_and_Statuses.md#context-ice) | Block | {'type': '`Block`', 'df': "Applies the 'Ice' effect. | 2 |
| [`Shadow`](./Passives_and_Statuses.md#context-shadow) | Block | {'type': '`Block`', 'df': "Applies the 'Shadow' effect. | 2 |
| [`Water`](./Passives_and_Statuses.md#context-water) | Block | {'type': '`Block`', 'df': "Applies the 'Water' effect. | 2 |
| [`Wind`](./Passives_and_Statuses.md#context-wind) | Block | {'type': '`Block`', 'df': "Applies the 'Wind' effect. | 2 |

</details>

---

### Context: `EscapeSequence`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `SafeExplosionIfHitSomething` | Number | {'type': '`Number`', 'df': "Applies the 'SafeExplosionIfHitSomething' effect."} | 2 |

</details>

---

### Context: `Eternal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health_percent` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `Fire`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `Grass`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `Gravity`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `GravityWell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 2 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 2 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 2 |

</details>

---

### Context: `HealAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `mana` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 2 |

</details>

---

### Context: `Holy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `HolyDamageBlessing`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`PassiveUntilGetKill`](./Passives_and_Statuses.md#context-passiveuntilgetkill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| `damage_multiplier` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `Ice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `InfiniteRebirth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `health` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `playercat_health` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `LateBloomer`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 2 |

</details>

---

### Context: `LightningRod`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `LowHealthAllyDodgeChanceAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 2 |
| `theshold` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 2 |
| `enemies_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `NextBattleStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `PassiveAfterXKills`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 2 |

</details>

---

### Context: `PassiveAtFullHealth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `TakeExtraDamage` | Number | {'type': '`Number`', 'df': "Applies the 'TakeExtraDamage' effect."} | 2 |

</details>

---

### Context: `PassiveAtInjuryThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`mode`](./Enums.md#enum-mode) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `PassiveGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`RandomPassivePool`](./Passives_and_Statuses.md#context-randompassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 14 |

</details>

---

### Context: `PassiveUntilCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`HealAlliesEachTurn`](./Passives_and_Statuses.md#context-healallieseachturn) | Block | {'type': '`Block`', 'df': "Applies the 'HealAlliesEachTurn' effect. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `PassiveUntilGetKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`HolyDamageBlessing`](./Passives_and_Statuses.md#context-holydamageblessing) | Block | {'type': '`Block`', 'df': "Applies the 'HolyDamageBlessing' effect. | 2 |

</details>

---

### Context: `PassiveWhenTheAlpha`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TogglableRoundEndExtraTurn` | Number | {'type': '`Number`', 'df': "Applies the 'TogglableRoundEndExtraTurn' effect."} | 2 |

</details>

---

### Context: `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `PassiveWhileInMonkRangedStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `PassiveWhilePreviewingMonkRangedStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `PassiveWhileWearingMetal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddElementsToWeapon`](./Enums.md#enum-addelementstoweapon) | Enum | {'type': '`Enum/String`', 'df': "Applies the 'AddElementsToWeapon' effect."} | 2 |

</details>

---

### Context: `RepressedMemoriesMetronome`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#context-scaledstatusonspendmana)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 2 |

</details>

---

### Context: `ScaledStatusOnOverMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `ScaledStatusOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RepressedMemoriesMetronome`](./Passives_and_Statuses.md#context-repressedmemoriesmetronome) | Block | {'type': '`Block`', 'df': "Applies the 'RepressedMemoriesMetronome' effect. | 2 |

</details>

---

### Context: `SecurityBotProtect`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 2 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `Shadow`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `SmiteEnemiesWhoKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 2 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 2 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 2 |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `SpecialFriends`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `StatsAtLowHealth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `speed` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `strength` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `StatusAfterCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusAlliesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |

</details>

---

### Context: `StatusAlliesOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `scaled` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `StatusAllyWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `StatusAnyCatAllyWhoKills`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `StatusDamagers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `StatusEachTurnEndPerEnemyKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `StatusEnemiesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `StatusEveryXTurnBegins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `turns` | Number | {'type': '`Number`', 'df': 'The duration of the effect in turns.'} | 2 |

</details>

---

### Context: `StatusKillers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `StatusOnAnyDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `StatusOnBattleEndIfKillThresholdMet`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `kills` | Number | {'type': '`Number`', 'df': ''} | 2 |
| [`statuses`](./Passives_and_Statuses.md#context-statuses) | Block | {'type': '`Block`', 'df': " | 2 |

</details>

---

### Context: `StatusOnBreakItem`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusOnDealtDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `StatusOnDealtDamageThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `count_overkill` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `ignore_during_movement` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

</details>

---

### Context: `StatusOnGainShield`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `StatusOnHeal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusOnOverMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `StatusOnTookDamageFromEnemyAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `StatusOnTriggerTrap`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `StatusOnUseElementAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'The specific element type required or applied.'} | 2 |

</details>

---

### Context: `StatusPerInjury`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `cap` | Number | {'type': '`Number`', 'df': ''} | 2 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `StatusThingsKnockedBack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Drag` | Number | {'type': '`Number`', 'df': "Applies the 'Drag' effect."} | 2 |

</details>

---

### Context: `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `TaggedPickupEffectReplacement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The specific entity tag required or applied.'} | 2 |

</details>

---

### Context: `TowerDefense`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 2 |
| `range` | Number | {'type': '`Number`', 'df': 'Distance or area of effect in tiles.'} | 2 |

</details>

---

### Context: `Water`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AOEPuddle`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies the 'AOEPuddle' effect."} | 2 |

</details>

---

### Context: `Wind`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`knockback`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `on_break`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SafeExplosionIfHitSomething` | Number | {'type': '`Number`', 'df': "Applies the 'SafeExplosionIfHitSomething' effect."} | 2 |

</details>

---

### Context: `on_throw`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `schadenfreude_scaled_stats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `str` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `AbilityChargeRefundChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `advantage_softcap` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `chance` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0 or percentage) of this effect triggering.'} | 1 |

</details>

---

### Context: `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `AddStatusToReceivedDamage_ExcludeStatuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_DoesDamage`](./Passives_and_Statuses.md#context-conditional_doesdamage) | Block | {'type': '`Block`', 'df': "Conditional block: Executes nested logic only if the target is/has DoesDamage. | 1 |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `AddStatusesIfPersistentWeatherElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `AddStatusesToReceivedElementalDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `AddTemporaryEffectsToEquipment`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | {'type': '`Number`', 'df': "Applies the 'CastAgain' effect."} | 1 |

</details>

---

### Context: `Autism`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `innate` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `learned` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `ChanceToRevive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 1 |
| [`statuses`](./Passives_and_Statuses.md#context-statuses) | Block | {'type': '`Block`', 'df': " | 1 |

</details>

---

### Context: `CollectPickupsOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `pop_corpses` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `Conditional_DoesDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToReceivedDamage_ExcludeStatuses`](./Passives_and_Statuses.md#context-addstatustoreceiveddamage_excludestatuses)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 40 |
| `odds` | Number | {'type': '`Number`', 'df': "The probability (0.0 to 1.0) of triggering the 'good roll' success state."} | 1 |

</details>

---

### Context: `Conditional_SourceHasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The specific entity tag required or applied.'} | 1 |

</details>

---

### Context: `DamageIfDidntUseSpecificAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger or reference.'} | 1 |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |

</details>

---

### Context: `DelayedWind`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | {'type': '`Number`', 'df': 'The area of effect or distance in tiles.'} | 1 |

</details>

---

### Context: `DelayedWindCone`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | {'type': '`Number`', 'df': 'The area of effect or distance in tiles.'} | 1 |

</details>

---

### Context: `Diabetes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `EnergyStorm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `period` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `ForceMoveAway`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusAdjacentOnTheirTurnBegin`](./Passives_and_Statuses.md#context-statusadjacentontheirturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `free` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `FurnitureStats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Appeal` | Number | {'type': '`Number`', 'df': "Applies the 'Appeal' effect."} | 1 |
| `Comfort` | Number | {'type': '`Number`', 'df': "Applies the 'Comfort' effect."} | 1 |
| `Stimulation` | Number | {'type': '`Number`', 'df': "Applies the 'Stimulation' effect."} | 1 |

</details>

---

### Context: `MegaMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 1 |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `PassiveLevelScaledStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [`SizeScalePercent`](./Math_Equations.md) | Equation | {'type': '`String`', 'df': "Applies the 'SizeScalePercent' effect."} | 1 |

</details>

---

### Context: `RandomPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 22 |

</details>

---

### Context: `ReplaceBrain`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Robot`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `ScaledStatusOnBleedDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `ScaledStatusOnLoseShield`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `ScaledStatusOnOverHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnScaledRotFly` | Number | {'type': '`Number`', 'df': "Applies the 'SpawnScaledRotFly' effect."} | 1 |

</details>

---

### Context: `SelfDamageWhenDealDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 1 |

</details>

---

### Context: `StackingDodgeChanceOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `amount` | Number | {'type': '`Number`', 'df': 'The numerical quantity.'} | 1 |
| `cap` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `StatusAdjacentOnTheirTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `StatusAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `exclude_self` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `StatusAlliesOnSpendMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `StatusAlliesScaledByCursedOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusIfBattleAlreadyBegan`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusOnEatPill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `StatusOnLoseShield`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusOnTakeHealthDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 1 |

</details>

---

### Context: `StrengthInNumbersAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count_self` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 1 |

</details>

---

### Context: `Study`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `marked` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks, duration, or intensity to apply.'} | 1 |

</details>

---

### Context: `TakeBonusTurnWithStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `TheHunger`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `TileDamageMultiplier`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ally_multiplier` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `multiplier` | Number | {'type': '`Number`', 'df': 'Multiplicative modifier to a base value.'} | 1 |

</details>

---

### Context: `TourettesMeows`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cooldown`](./Arrays.md#array-cooldown) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`pool`](./Arrays.md#array-pool) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `fire`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 1 |

</details>

---

### Context: `ice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 1 |

</details>

---

### Context: `lightning`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 1 |

</details>

---

### Context: `triattack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification type (e.g., damage type or element).'} | 1 |

</details>

---

