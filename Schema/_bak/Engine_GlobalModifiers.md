# Mewgenics Mod Developer Documentation: Engine: Global Modifier IDs

> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Engine: Global Modifier IDs

This document lists every confirmed Global Modifier ID. These are game-state flags that affect the entire battle or run (e.g. `BloodRain`, `NoCorpses`, `LowerAmbientLight`). Used as keys in `CreateGlobalModifiers {}`.

### All Confirmed `[global_modifier_id]` Values

<details>
<summary><b>Expand</b></summary>

| ID | Type | Notes |
| :--- | :--- | :--- |
| `BloodRain` | Number | Applies or references the 'BloodRain' effect/state. |
| `LowerAmbientLight` | Block | A visual effect that dims the map's lighting. |
| `NextPlayerCatTakesExtraTurn` | Number | Applies or references the 'NextPlayerCatTakesExtraTurn' effect/state. |
| `NoCorpses` | Number | Applies or references the 'NoCorpses' effect/state. |
| `{Global Modifiers}` | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |

</details>

