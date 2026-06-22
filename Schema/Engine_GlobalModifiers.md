# Mewgenics Mod Developer Documentation: Engine: Global Modifier IDs

## Engine: Global Modifier IDs

This document lists every confirmed Global Modifier ID. These are game-state flags that affect the entire battle or run (e.g. `BloodRain`, `NoCorpses`, `LowerAmbientLight`). Used as keys in `CreateGlobalModifiers {}`.

> **Referenced by:** [`effects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-effects), [`CreateGlobalModifiers` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-createglobalmodifiers), [`effects` (Cat_Mutations)](./Cat_Mutations.md#context-effects), [`effects` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-effects), [`CreateGlobalModifiers` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-createglobalmodifiers), [`effects` (Elite_Buffs)](./Elite_Buffs.md#context-effects), [`effects` (House_and_Environment)](./House_and_Environment.md#context-effects), [`effects` (Items_and_Equipment)](./Items_and_Equipment.md#context-effects), [`global_passives` (Items_and_Equipment)](./Items_and_Equipment.md#context-global_passives), [`CreateGlobalModifiers` (Items_and_Equipment)](./Items_and_Equipment.md#context-createglobalmodifiers), [`effects` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-effects)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| `BloodRain` | Integer | Applies or references the 'BloodRain' effect/state. |
| [`LowerAmbientLight`](#lowerambientlight) | Block | A visual effect that dims the map's lighting. |
| `NextPlayerCatTakesExtraTurn` | Integer | Applies or references the 'NextPlayerCatTakesExtraTurn' effect/state. |
| `NoCorpses` | Integer | Applies or references the 'NoCorpses' effect/state. |
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

