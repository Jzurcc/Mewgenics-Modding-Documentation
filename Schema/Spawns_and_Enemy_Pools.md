# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


## Spawns & Enemy Pools

> **Associated Files:** `data/spawns.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 550

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`image`](./Strings.md#string-image) | String |  | 578 |  |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 291 |  |
| `value` | Float | The magnitude or stat reference for this elite buff (e.g., numeric, 'spd', 'con'). | 54 |  |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 3 |  |
| [`element`](./Engine_LogicKeys.md#valid-property-keys) | Array / Enum | Specific element type required or applied. | 1 |  |

</details>

---

### Object: `editor`


**Definition:** No definition provided.  
**Total Count:** 578


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |  |

</details>

---

### Object: `weather_element_alt`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

