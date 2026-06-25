# Mewgenics Mod Developer Documentation: Engine: Global Modifier IDs

## Engine: Global Modifier IDs

This document lists every confirmed Global Modifier ID. These are game-state flags that affect the entire battle or run (e.g. `BloodRain`, `NoCorpses`, `LowerAmbientLight`). Used as keys in `CreateGlobalModifiers {}`.

> **Referenced by:** [`CreateGlobalModifiers` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-createglobalmodifiers), [`CreateGlobalModifiers` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-createglobalmodifiers), [`global_passives` (Items_and_Equipment)](./Items_and_Equipment.md#context-global_passives), [`CreateGlobalModifiers` (Items_and_Equipment)](./Items_and_Equipment.md#context-createglobalmodifiers)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CreateGlobalModifiers`](#createglobalmodifiers) | Object | Generates global map or encounter rules/modifiers. | 5 |
| `BloodRain` | Integer | Applies or references the 'BloodRain' effect/state. | 3 |
| `NextPlayerCatTakesExtraTurn` | Integer | Applies or references the 'NextPlayerCatTakesExtraTurn' effect/state. | 1 |
| `NoCorpses` | Integer | Applies or references the 'NoCorpses' effect/state. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |

</details>


### Valid Nested Objects

The following objects all behave as `{Global Modifier Keys}` containers. Each has its own unique parameters listed below its entry.


#### `CreateGlobalModifiers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Object | Game-state flag identifiers for tracking world progression and event states. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 5 |
| [`LowerAmbientLight`](#lowerambientlight) | Object | A visual effect that dims the map's lighting. | 3 |

</details>


---
