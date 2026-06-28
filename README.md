---
title: "Mewgenics Modding Documentation"
description: "Root index for all Mewgenics modding guides, schemas, and specifications"
---

# Mewgenics Modding Documentation

Welcome to my personal compilation of references for Mewgenics modding! What simply started as a simple list for my studies now became an exhaustive compilation of what is found in the game files.

> [!WARNING]
> **Disclaimer:** There are thousands of keys and objects in Mewgenics, and I've decided to use AI to help define them. While provided with deep contextual data, they are not guaranteed to be perfectly accurate. Furthermore, I will most likely not actively maintain this documentation for long, so treat it as a library of sort. You WILL have to study the base files on your own and verify these implementations within the game yourself.

For a more continuously updated resource on engine scripting, please refer to **[Ombrellus' GON Scripting Resources](https://github.com/ombrellus/MewgenicsScriptResources)**. They actively test out engine resources, but because they are human-tested before adding, they might not have a complete list of syntax and possible keys as of yet.

To start, Mewgenics uses a proprietary engine architecture and data serialization format known as Glaiel Object Notation (GON). To accommodate this, the documentation is divided into four functional areas: **Theory**, **Syntax**, **Practice**, and **Reference**. Of these, most developers will probably be most interested in the [**`Schema/`**](./Schema/) directory, and is where you will spend the majority of your time during mod development.

---

## Suggested Entry Points

### For New Developers
- Read the [**Step-by-Step Modding Guide**](./mewgenics/modding-guide.md) to understand project structure and how to load a mod into the runtime.
- Review the [**GON Format Overview**](./gon-docs/spec/01-overview.md) for a primer on how the engine parses data files.

### Implementing Items and Equipment
- Consult the [**Items & Equipment Schema**](./Schema/Core_Entities_and_Combat/Items_and_Equipment.md) for the complete list of valid object properties.
- Reference the [**Items Directory**](./Directory/Items_and_Passives/Items_and_Equipment.md) to analyze how base-game weapons are constructed.

### Implementing Classes and Mutations
- Consult the [**Cat Classes Schema**](./Schema/Player_Progression_and_Cats/Cat_Classes.md) to understand base stat initialization and level-up pools.
- Reference the [**Cat Abilities Directory**](./Directory/Abilities/Cat_Abilities.md) to analyze ability balance and targeting logic.

### Troubleshooting and Debugging
- Refer to the [**GON Error Reference**](./gon-docs/reference/error-reference.md) to diagnose common parsing failures.
- Review the [**Syntax Cheat Sheet**](./gon-docs/reference/cheat-sheet.md) to verify your file formatting.

---

## The Core Modding Workflow

If you want a modding workflow, you can follow this:

1. **Identify:** Locate a base-game object within the [**`Directory/`**](./Directory/) that most closely approximates your intended functionality.
2. **Define:** Cross-reference that object type in the [**`Schema/`**](./Schema/) to discover which engine properties and hooks are available for modification.
3. **Format:** Construct your object in a `.gon` file. Ensure compliance with the parser rules outlined in the [**`gon-docs/`**](./gon-docs/).
4. **Test:** Execute the game, monitor the developer console for parsing errors, and validate the logic in combat.

---

## Directory Overview

> [!TIP]
> **Navigation:** When browsing the directories below, refer to the `README.md` index file rendered at the bottom of each folder for context and cross-linking.

| Directory | Scope | Description |
|-----------|------------|-------------|
| [**`Schema/`**](./Schema/) | **Theory (Engine Semantics)** | The exhaustive dictionary of the engine. Defines valid properties, keys, and values for all objects (Items, Characters, Abilities, etc). |
| [**`gon-docs/`**](./gon-docs/) | **Syntax (File Formatting)** | The formal language specification for Glaiel Object Notation (`.gon`). Contains syntax rules, format comparisons, and troubleshooting. |
| [**`mewgenics/`**](./mewgenics/) | **Practice (Implementation)** | Practical implementation guides. Includes step-by-step tutorials and annotated case studies of base-game objects. |
| [**`Directory/`**](./Directory/) | **Reference (Base Game Data)** | A comprehensive reference index containing raw `.gon` extracts of base-game content. Essential for referencing existing architectural structures and utilizing the `variant_of` inheritance key. |

---

## Tooling & Architecture Principles

Ensure your development environment is properly configured before writing code:

1. **Text Editor:** Use a modern code editor (e.g., [VSCode](https://code.visualstudio.com/), [Notepad++](https://notepad-plus-plus.org/), or [Sublime Text](https://www.sublimetext.com/)). Avoid basic text editors like Windows Notepad.
2. **Syntax Highlighting:** Install the [Mewgenics GON Extension for VSCode](https://github.com/henriquel1997/gon_vs_syntax_highlighting) to improve readability and catch formatting errors early.

> [!IMPORTANT]
> **Core Architectural Rules**
> 1. **GON is JSON-compatible.** Commas, colons, and equals signs are ignored by the parser as syntactic whitespace. Standard JSON syntax is fully valid.
> 2. **Strict Case Sensitivity.** The engine parses all values as strings. If a schema defines an enum as `Fire`, writing `fire` will result in a silent failure. Always match the casing found in the Reference Directories.

---

### Deprecated Documentation

| Directory | Description |
|-----------|-------------|
| [**`old-docs (deprecated)/`**](./old-docs%20%28deprecated%29/) | Legacy documentation files that I initially started with. Superseded by the `Schema/` directory. |

<details>
<summary><strong>Quick Navigation</strong></summary>  

- **Core Entities & Combat**: [Abilities & Spells](../Core_Entities_and_Combat/Abilities_and_Spells.md) | [Characters & Bosses](../Core_Entities_and_Combat/Characters_and_Bosses.md) | [Items & Equipment](../Core_Entities_and_Combat/Items_and_Equipment.md) | [Passives & Statuses](../Core_Entities_and_Combat/Passives_and_Statuses.md) | [Elite Buffs](../Core_Entities_and_Combat/Elite_Buffs.md) | [Enemy AI](../Core_Entities_and_Combat/Enemy_AI.md) | [Status Keywords](../Core_Entities_and_Combat/Status_Effect_Keywords.md)
- **Engine Scripts & Logic**: [Logic Keys](../Engine_Scripts_and_Logic/Engine_LogicKeys.md) | [Event Keys](../Engine_Scripts_and_Logic/Engine_EventKeys.md) | [Damaging Keys](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md) | [Status & Passive Keys](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | [Global Modifiers](../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md) | [Math Equations](../Engine_Scripts_and_Logic/Math_Equations.md)
- **Player Progression & Cats**: [Cat Classes](../Player_Progression_and_Cats/Cat_Classes.md) | [Cat Mutations](../Player_Progression_and_Cats/Cat_Mutations.md) | [Custom Cats](../Player_Progression_and_Cats/Custom_Cats.md) | [Injuries](../Player_Progression_and_Cats/Injuries.md) | [Progression Unlocks](../Player_Progression_and_Cats/Progression_Unlocks.md) | [Combat Rewards](../Player_Progression_and_Cats/Combat_Rewards.md)
- **World, Maps & Events**: [Events & Encounters](../World_Maps_and_Events/Events_and_Encounters.md) | [House & Environment](../World_Maps_and_Events/House_and_Environment.md) | [Map Gen & Routing](../World_Maps_and_Events/Map_Generation_and_Routing.md) | [Furniture & Meta](../World_Maps_and_Events/Furniture_and_Metaprogression.md) | [Shops](../World_Maps_and_Events/Shops.md) | [Spawns & Enemy Pools](../World_Maps_and_Events/Spawns_and_Enemy_Pools.md) | [Boss Cutscenes](../World_Maps_and_Events/Boss_Cutscene_Info.md) | [NPC Scripts](../World_Maps_and_Events/NPC_Scripts.md)
- **Assets & Localization**: [Audio SFX](../Assets_and_Localization/Audio_SFX_Dictionary.md) | [Particles & VFX](../Assets_and_Localization/Particles_and_VFX_Dictionary.md) | [Damage Text](../Assets_and_Localization/Damage_Text_Styles.md) | [Localization Guide](../Assets_and_Localization/Localization_Guide.md) | [Text Formatting](../Assets_and_Localization/Text_Formatting_and_Effects.md) | [Strings](../Assets_and_Localization/Strings.md)
- **Reference & Meta**: [Enums](../Reference_and_Meta/Enums.md) | [Arrays](../Reference_and_Meta/Arrays.md) | [Item Pools](../Reference_and_Meta/Item_Pools.md) | [Difficulties](../Reference_and_Meta/Difficulties.md) | [Hidden Passives](../Reference_and_Meta/Engine_Hidden_Passives_and_Statuses.md) | [Passive Audit](../Reference_and_Meta/Passive_Identifiers_Audit.md) | [Uncategorized Keys](../Reference_and_Meta/Engine_Uncategorized_Resources.md) | [Miscellaneous](../Reference_and_Meta/Miscellaneous.md)
</details>
<br>