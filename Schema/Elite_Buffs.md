# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Elite Buffs

> **Associated Files:** `data/elite_buffs.gon, data/boss_elite_buffs.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 54

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1549 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 206 |
| `icon_frame` | Integer |  | 128 |
| `value` | Float |  | 485 |
| `unique` | Boolean |  | 72 |
| `specific_chapter` | Integer |  | 16 |
| [`minion_alt`](./Enums.md#enum-minion_alt) | Enum |  | 10 |
| `rollable` | Boolean |  | 10 |
| `only_at_battle_start` | Boolean |  | 4 |
| `requires_corpse` | Boolean |  | 4 |
| `roll_limit` | Integer |  | 4 |

</details>

---

### Object: `passives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2805

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 2609 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 173 |

</details>

---

### Object: `StatusEachRoundBegin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 8 |

</details>

---

### Object: `effects`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2166

> **Referenced by:** [`DamageNeighborsAfterMove`](#object-damageneighborsaftermove), [`MeleeRevengeDamage`](#object-meleerevengedamage), [`RevengeDamage`](#object-revengedamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1886 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 59 |
</details>

---

### Object: `DepressionAura`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `aura_effects_allies` | Boolean |  | 8 |
| `range` | Integer |  | 8 |
| `stacks` | Integer |  | 8 |

</details>

---

### Object: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 73

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 49 |
| `knockback` | Integer |  | 48 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |
  | [`AddDamageToElementDamage`](#adddamagetoelementdamage) | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 0 |
  | [`AddStatusToElementDamage`](#addstatustoelementdamage) | Object | Applies the 'AddStatusToElementDamage' effect. | 0 |
  | [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. | 0 |
  | [`StatusImmunity`](./Enums.md#enum-statusimmunity) | Enum | Applies or references the 'StatusImmunity' effect/state. | 0 |

</details>

---

### Object: `ChanceToRevive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`statuses`](#object-statuses) | Object |  | 6 |
| `health` | Integer |  | 8 |
| `stacks` | Integer |  | 10 |

</details>

---

### Object: `DamageNeighborsAfterMove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 18 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum |  | 8 |
| `damage` | Integer |  | 8 |

</details>

---

### Object: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 31

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 10 |
  | [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. | 0 |

</details>

---

### Object: `SpawnOnBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 38

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 72 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum |  | 4 |

</details>

---

### Object: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 57

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
  | [`Conditional_ManaThreshold`](#conditional_manathreshold) | Object | Conditional constraint. Nested properties only trigger if this is true. | 0 |
  | `EmptyMana` | Integer | Applies the 'EmptyMana' effect. | 0 |
  | `PreEmptiveCounterNextAttacks` | Integer | Applies or references the 'PreEmptiveCounterNextAttacks' effect/state. | 0 |
  | [`UseAbility_Madness`](./Enums.md#enum-useability_madness) | Enum | Applies the 'UseAbility_Madness' effect. | 0 |
</details>

---

### Object: `statuses`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 14

> **Referenced by:** [`ChanceToRevive`](#object-chancetorevive)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
 | `Zombie` | Number |  | 2 | 
  | `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
  | `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 0 |
  | `PermanentDexterity` | Number | Applies or references the 'PermanentDexterity' effect/state. | 0 |
  | [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Object | Generates an item drop from the specified loot pool. | 0 |
  | [`AllStatsUp`](./Arrays.md#array-allstatsup) | Number | Applies or references the 'AllStatsUp' effect/state. | 0 |
  | [`Consumed`](#consumed) | Object | State object triggered when this object or entity is eaten/consumed by another character. | 0 |
</details> 

---

### Object: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 248

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
  | [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum | Examples: `Ice, Electric, Water` | 0 |
  | [`AddStatusesToReceivedElementalDamage`](#addstatusestoreceivedelementaldamage) | Object | Applies the 'AddStatusesToReceivedElementalDamage' effect. | 0 |
  | `BigSplashDamage` | Integer | Applies the 'BigSplashDamage' effect. | 0 |
  | [`Conditional_SourceHasTag`](#conditional_sourcehastag) | Object | Examples: `{ ... }` | 0 |
  | [`DistanceBonusDamage`](#distancebonusdamage) | Object | Applies the 'DistanceBonusDamage' effect. | 0 |
  | [`ForceUseAbilityOnTarget`](#forceuseabilityontarget) | Object | Applies or references the 'ForceUseAbilityOnTarget' effect/state. | 0 |
  | `RemoteFlatLeech` | Integer | Applies or references the 'RemoteFlatLeech' effect/state. | 0 |
  | `RemoteLeech` | Integer | Applies or references the 'RemoteLeech' effect/state. | 0 |
  | `SleepParalysis` | Variable |  | 0 |
  | `SpawnBearTrapOnMiss` | Integer | Applies the 'SpawnBearTrapOnMiss' effect. | 0 |
  | [`StatusDamagers`](#statusdamagers) | Object | Event Trigger: Applies nested statuses to damagers. | 0 |
</details>

---

### Object: `ReflectProjectiles`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
  | [`self_damage`](./Arrays.md#array-self_damage) | Object | Recoil or self-inflicted damage/effects applied to the caster. | 0 |

</details>

---

### Object: `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1 |
</details>

---

### Object: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
  | [`RemoveGlobalModifiers`](./Arrays.md#array-removeglobalmodifiers) | Array | Applies or references the 'RemoveGlobalModifiers' effect/state. | 0 |
  | [`ScatterCoins`](./Arrays.md#array-scattercoins) | Object | Throws coins out into the level randomly. | 0 |
  | `GainCoinsRange` | Object | Grants the player a randomized amount of coins within a min/max range. | 0 |
  | [`RemoveAmbientLightEffects`](./Enums.md#enum-removeambientlighteffects) | Float | Applies or references the 'RemoveAmbientLightEffects' effect/state. | 0 |
  | `BloodRain` | Integer | Applies or references the 'BloodRain' effect/state. | 0 |
  | `StackingSandstorm` | Number | Applies or references the 'StackingSandstorm' effect/state. | 0 |
  | [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Object | Generates an item drop from the specified loot pool. | 0 |
  | `RandomStatusFromPool` | Object | Selects and applies a random status effect from the provided nested object. | 0 |
  | [`Conditional_RandomChance`](#conditional_randomchance) | Object | Conditional trigger: Executes nested logic based on a flat percentage random roll. | 0 |
  | [`CreateGlobalModifiers`](#createglobalmodifiers) | Object | Generates global map or encounter rules/modifiers. | 0 |
  | `RandomMagicMissile` | Object | Fires a randomized number of magic missiles. | 0 |
</details>

---

### Object: `StatusOnEnemyCastSpell`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1 |

</details>

---

### Object: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 40

> **Referenced by:** [`passives`](#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
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

