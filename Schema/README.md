---
title: "Mewgenics Object Schema"
description: "Semantic documentation index for Mewgenics .gon data files"
---

# Mewgenics Object Schema

> **What is this folder?**
> This directory serves as the **semantic reference index** for the `.gon` files used in Mewgenics. It describes exactly what properties (keys) are valid inside specific game objects (e.g., Abilities, Characters, Items) and how the C++ game engine interprets them at runtime.

For rules regarding string parsing, arrays, and structural syntax, refer to the [GON Syntax Documentation](../gon-docs/README.md).  
For practical step-by-step tutorials on creating and injecting mods, refer to the [Practical Modding Guides](../mewgenics/README.md).

---

## 1. Type Reference Guidelines

Throughout the schema markdown files, you will encounter a standard table format detailing the properties of an object:

| Property Key | Inferred Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `base_health` | Integer | The base HP of the unit. | 45 |

> [!IMPORTANT]
> The **Inferred Type** listed in these tables describes the C++ engine's internal cast target, **not** a rigid GON syntax rule.

| Inferred Type | Engine Cast Behavior | Example |
|---------------|----------------------|---------|
| **Boolean** | Evaluates explicitly for `true` or `false` string literals. | `true`, `false` |
| **Integer** | Casts the string to a whole number (e.g., `atoi`). Decimals are truncated. | `5`, `100`, `-3` |
| **Float** | Casts the string to a floating-point decimal (e.g., `atof`). | `1.25`, `.5` |
| **Number** | Used when it is empirically unknown if the engine utilizes an int or float cast internally. | `42` |
| **Enum** | Maps the string against a hardcoded C++ `enum`. Unrecognized strings are typically ignored. | `melee_attack`, `north` |
| **String** | Read raw. Used for file paths or localization keys. | `"ABILITY_NAME"`, `"cats/tabby.png"` |
| **Equation** | Passed to the engine's internal math parser. Evaluated dynamically at runtime, allowing state variables. | `1+bonus_melee_range` |
| **Array** | Expects a bracketed list. The engine iterates over the elements and casts each individually. | `[ Fire Holy ]` |
| **Object** | Expects a nested dictionary of keys and values. | `{ value 5 }` |

---

## 2. Comprehensive File Index

The schema documentation is divided logically by subsystem. Click on any file to view the comprehensive list of properties and behaviors accepted by the engine for those objects.

### Core Entities & Combat
| File | Description |
|------|-------------|
| [Characters_and_Bosses.md](./Characters_and_Bosses.md) | Cat classes, enemies, bosses, and summons. |
| [Abilities_and_Spells.md](./Abilities_and_Spells.md) | Spells, attacks, and combat abilities. |
| [Items_and_Equipment.md](./Items_and_Equipment.md) | Consumables, weapons, and trinkets. |
| [Passives_and_Statuses.md](./Passives_and_Statuses.md) | Status effects and permanent passive buffs. |
| [Elite_Buffs.md](./Elite_Buffs.md) | Modifiers applied to elite enemies. |
| [Enemy_AI.md](./Enemy_AI.md) | AI decision nodes and behavioral weighting. |
| [Status_Effect_Keywords.md](./Status_Effect_Keywords.md) | Dictionary of valid status effect keywords. |

### Player Progression & Cats
| File | Description |
|------|-------------|
| [Cat_Classes.md](./Cat_Classes.md) | Definitions for cat classes and stat scaling. |
| [Cat_Mutations.md](./Cat_Mutations.md) | Visual body mutations and their stat impacts. |
| [Custom_Cats.md](./Custom_Cats.md) | Properties for generating specific, bespoke cats. |
| [Injuries.md](./Injuries.md) | Post-combat injury definitions and penalties. |
| [Progression_Unlocks.md](./Progression_Unlocks.md) | Conditions and flags for unlocking content. |
| [Combat_Rewards.md](./Combat_Rewards.md) | Loot tables and combat reward generation. |

### World, Maps & Events
| File | Description |
|------|-------------|
| [Events_and_Encounters.md](./Events_and_Encounters.md) | Dialogue encounters and choice nodes. |
| [House_and_Environment.md](./House_and_Environment.md) | Overworld tiles and intractable house objects. |
| [Map_Generation_and_Routing.md](./Map_Generation_and_Routing.md) | Biome layout rules and node generation logic. |
| [Furniture_and_Metaprogression.md](./Furniture_and_Metaprogression.md) | Placeable furniture and permanent upgrades. |
| [Shops.md](./Shops.md) | Vendor inventories and pricing multipliers. |
| [Spawns_and_Enemy_Pools.md](./Spawns_and_Enemy_Pools.md) | Tables determining which enemies spawn per biome. |
| [Boss_Cutscene_Info.md](./Boss_Cutscene_Info.md) | Camera and timing configuration for boss intros. |
| [NPC_Scripts.md](./NPC_Scripts.md) | Behavior logic for non-combat interactive NPCs. |

### Engine Scripts & Logic
| File | Description |
|------|-------------|
| [Engine_LogicKeys.md](./Engine_LogicKeys.md) | Core conditionals, loops, and execution flow. |
| [Engine_EventKeys.md](./Engine_EventKeys.md) | Scripting keys for narrative and map events. |
| [Engine_DamagingKeys.md](./Engine_DamagingKeys.md) | Hooks for calculating and modifying damage. |
| [Engine_StatusAndPassiveKeys.md](./Engine_StatusAndPassiveKeys.md) | Hooks for triggering logic when statuses are applied. |
| [Engine_GlobalModifierKeys.md](./Engine_GlobalModifierKeys.md) | Global state flags affecting the entire run. |
| [Math_Equations.md](./Math_Equations.md) | Valid syntax and variables for Equation strings. |

### Assets & Localization
| File | Description |
|------|-------------|
| [Audio_SFX_Dictionary.md](./Audio_SFX_Dictionary.md) | Triggers for playing sound effects. |
| [Particles_and_VFX_Dictionary.md](./Particles_and_VFX_Dictionary.md) | Identifiers for spawning visual effects. |
| [Damage_Text_Styles.md](./Damage_Text_Styles.md) | Configuration for floating combat text. |
| [Localization_Guide.md](./Localization_Guide.md) | Best practices for translating and keying strings. |
| [Strings.md](./Strings.md) | Internal engine string references. |

### Reference & Meta
| File | Description |
|------|-------------|
| [Enums.md](./Enums.md) | Valid string identifiers for all enum-backed properties. |
| [Arrays.md](./Arrays.md) | Specialized array formats. |
| [Item_Pools.md](./Item_Pools.md) | Identifiers for categorizing item drops. |
| [Difficulties.md](./Difficulties.md) | Scaling multipliers across game difficulty settings. |
| [Engine_Hidden_Passives_and_Statuses.md](./Engine_Hidden_Passives_and_Statuses.md) | Passives that exist but are hidden from the UI. |
| [Passive_Identifiers_Audit.md](./Passive_Identifiers_Audit.md) | Deep-dive tracking of passive effect implementations. |
| [Engine_Uncategorized_Resources.md](./Engine_Uncategorized_Resources.md) | Keys that have not yet been fully categorized. |
| [Miscellaneous.md](./Miscellaneous.md) | Assorted properties lacking clear subsystem alignment. |

> [!TIP]
> The exact boundaries between these schema files often blur (e.g., an Ability might trigger an Event). If you cannot find a property in the expected file, try checking the **Reference & Meta** subsystem, specifically `Miscellaneous.md` or `Engine_Uncategorized_Resources.md`.