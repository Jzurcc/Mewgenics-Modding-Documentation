---
title: "Spawns & Enemy Pools Schema"
description: "Tables determining which enemies spawn per biome."
---

# Spawns & Enemy Pools Schema

## Overview
> [!NOTE]
> This schema dictates which enemies are allowed to appear in specific environments, ensuring you don't fight a lava boss in an ice biome.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
editor {
        image "empty.png"
        name "Empty"
    }
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Spawns_and_Enemy_Pools.md`](../../Directory/Enemies_and_Combat/Spawns_and_Enemy_Pools.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Spawns & Enemy Pools

> **Associated Files:** `data/spawns.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 550

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 543 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `value` | Float | The numeric value or formula associated with the buff. | 377 | `.5`<br>`0`<br>`1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 19 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 3 | Default<br>FormChange<br>Druid |
| [`image`](../Assets_and_Localization/Strings.md#string-image) | String | Array of image filenames used for the related editor object. | 0 | `"empty.png"`<br>`["1.png" "pyrophina.png"]`<br>`["1.png" "zaratana.png"]` |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 0 | `Electric`<br>`Fire`<br>`Gravity` |

</details>


---


### Object: `editor`


**Definition:** An object containing metadata for the level editor, such as category, image, and name.  
**Total Count:** 578

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Spawns_and_Enemy_Pools.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 3 | `damage_instance`<br>`spell`<br>`false` |
`damage_instance`<br>`spell`<br>`self_damage`

</details>


---


### Object: `weather_element_alt`


**Definition:** Defines an alternative weather element, specifying its element type and associated object.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Spawns_and_Enemy_Pools.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---