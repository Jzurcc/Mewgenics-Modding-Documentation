# Mewgenics Mod Developer Documentation: Engine: Global Modifier IDs

## Engine: Global Modifier IDs

This document lists every confirmed Global Modifier ID. These are game-state flags that affect the entire battle or run (e.g. `BloodRain`, `NoCorpses`, `LowerAmbientLight`). Used as keys in `CreateGlobalModifiers {}`.

> **Referenced by:** [`CreateGlobalModifiers` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-createglobalmodifiers), [`CreateGlobalModifiers` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-createglobalmodifiers), [`global_passives` (Items_and_Equipment)](./Items_and_Equipment.md#context-global_passives), [`CreateGlobalModifiers` (Items_and_Equipment)](./Items_and_Equipment.md#context-createglobalmodifiers)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BloodRain` | Integer | Applies or references the 'BloodRain' effect/state. | 3 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| `NextPlayerCatTakesExtraTurn` | Integer | Applies or references the 'NextPlayerCatTakesExtraTurn' effect/state. | 1 |
| `NoCorpses` | Integer | Applies or references the 'NoCorpses' effect/state. | 1 |

</details>

### Valid Nested Blocks

The following blocks all behave as `{Global Modifier Keys}` containers. Each has its own unique parameters listed below its entry.

---

#### `CreateGlobalModifiers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`LowerAmbientLight`](#lowerambientlight) | Block | A visual effect that dims the map's lighting. | 3 |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

