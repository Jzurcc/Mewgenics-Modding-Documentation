# Mewgenics Mod Developer Documentation: Engine: Global Modifier IDs

## Engine: Global Modifier IDs

This document lists every confirmed Global Modifier ID. These are game-state flags that affect the entire battle or run (e.g. `BloodRain`, `NoCorpses`, `LowerAmbientLight`). Used as keys in `CreateGlobalModifiers {}`.

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| `BloodRain` | Number | Applies or references the 'BloodRain' effect/state. |
| [`LowerAmbientLight`](#lowerambientlight) | Block | A visual effect that dims the map's lighting. |
| `NextPlayerCatTakesExtraTurn` | Number | Applies or references the 'NextPlayerCatTakesExtraTurn' effect/state. |
| `NoCorpses` | Number | Applies or references the 'NoCorpses' effect/state. |
| `{Global Modifiers}` | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |

</details>

### Valid Nested Blocks

The following blocks all behave as `[global_modifier_id]` containers. Each has its own unique parameters listed below its entry.

---

#### `CreateGlobalModifiers`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[global_modifier_id]`](./Engine_GlobalModifiers.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

