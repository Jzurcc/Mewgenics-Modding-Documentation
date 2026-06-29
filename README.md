# Mewgenics Modding Documentation

After a gruesome struggling with the Mewgenics base resources, I welcome you to my personal compilation of references for Mewgenics modding! What simply started as a simple list for my studies now became an exhaustive compilation of what is found in the game files.

> [!WARNING]
> **Disclaimer:** There are thousands of keys and objects in Mewgenics, and I've decided to use AI to help define them. While provided with deep contextual data, they are not guaranteed to be perfectly accurate. Furthermore, I will most likely not actively maintain this documentation for long, so treat it as a quick library of sort rather than the sole source of truth. You WILL have to study the base files on your own and verify these implementations within the game yourself.

For a more continuously updated resource on engine scripting, please refer to **[Ombrellus' GON Scripting Resources](https://github.com/ombrellus/MewgenicsScriptResources)**. They actively test out engine resources, but because they are human-tested before adding, they might not have a complete list of syntax and possible keys as of yet (This has all 3,436 keys while they have about 1.3k verified as of June).

To start, Mewgenics uses a proprietary engine architecture and data serialization format known as Glaiel Object Notation (GON). To accommodate this, the documentation is divided into four functional areas: **Theory**, **Syntax**, **Practice**, and **Reference**. Of these, most developers will probably be most interested in the [**`Schema/`**](./Schema/) directory, and is where you will spend the majority of your time during mod development.

Also, be sure to open the outline in Github for easier navigation!
<img width="1882" height="136" alt="image" src="https://github.com/user-attachments/assets/d0052a13-da26-45d1-a5fd-e72b44b277bf" />


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

<details open>
<summary><strong>Schema Quick Navigation</strong></summary>

<table>
  <tr>
    <td width="22%"><strong>Core Entities & Combat</strong></td>
    <td><a href="./Schema/Core_Entities_and_Combat/Abilities_and_Spells.md">Abilities & Spells</a> • <a href="./Schema/Core_Entities_and_Combat/Characters_and_Bosses.md">Characters & Bosses</a> • <a href="./Schema/Core_Entities_and_Combat/Items_and_Equipment.md">Items & Equipment</a> • <a href="./Schema/Core_Entities_and_Combat/Passives_and_Statuses.md">Passives & Statuses</a> • <a href="./Schema/Core_Entities_and_Combat/Elite_Buffs.md">Elite Buffs</a> • <a href="./Schema/Core_Entities_and_Combat/Enemy_AI.md">Enemy AI</a> • <a href="./Schema/Core_Entities_and_Combat/Status_Effect_Keywords.md">Status Keywords</a></td>
  </tr>
  <tr>
    <td><strong>Engine Scripts & Logic</strong></td>
    <td><a href="./Schema/Engine_Scripts_and_Logic/Engine_LogicKeys.md">Logic Keys</a> • <a href="./Schema/Engine_Scripts_and_Logic/Engine_EventKeys.md">Event Keys</a> • <a href="./Schema/Engine_Scripts_and_Logic/Engine_DamagingKeys.md">Damaging Keys</a> • <a href="./Schema/Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md">Status & Passive Keys</a> • <a href="./Schema/Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md">Global Modifiers</a> • <a href="./Schema/Engine_Scripts_and_Logic/Math_Equations.md">Math Equations</a></td>
  </tr>
  <tr>
    <td><strong>Player Progression & Cats</strong></td>
    <td><a href="./Schema/Player_Progression_and_Cats/Cat_Classes.md">Cat Classes</a> • <a href="./Schema/Player_Progression_and_Cats/Cat_Mutations.md">Cat Mutations</a> • <a href="./Schema/Player_Progression_and_Cats/Custom_Cats.md">Custom Cats</a> • <a href="./Schema/Player_Progression_and_Cats/Injuries.md">Injuries</a> • <a href="./Schema/Player_Progression_and_Cats/Progression_Unlocks.md">Progression Unlocks</a> • <a href="./Schema/Player_Progression_and_Cats/Combat_Rewards.md">Combat Rewards</a></td>
  </tr>
  <tr>
    <td><strong>World, Maps & Events</strong></td>
    <td><a href="./Schema/World_Maps_and_Events/Events_and_Encounters.md">Events & Encounters</a> • <a href="./Schema/World_Maps_and_Events/House_and_Environment.md">House & Environment</a> • <a href="./Schema/World_Maps_and_Events/Map_Generation_and_Routing.md">Map Gen & Routing</a> • <a href="./Schema/World_Maps_and_Events/Furniture_and_Metaprogression.md">Furniture & Meta</a> • <a href="./Schema/World_Maps_and_Events/Shops.md">Shops</a> • <a href="./Schema/World_Maps_and_Events/Spawns_and_Enemy_Pools.md">Spawns & Enemy Pools</a> • <a href="./Schema/World_Maps_and_Events/Boss_Cutscene_Info.md">Boss Cutscenes</a> • <a href="./Schema/World_Maps_and_Events/NPC_Scripts.md">NPC Scripts</a></td>
  </tr>
  <tr>
    <td><strong>Assets & Localization</strong></td>
    <td><a href="./Schema/Assets_and_Localization/Audio_SFX_Dictionary.md">Audio SFX</a> • <a href="./Schema/Assets_and_Localization/Particles_and_VFX_Dictionary.md">Particles & VFX</a> • <a href="./Schema/Assets_and_Localization/Damage_Text_Styles.md">Damage Text</a> • <a href="./Schema/Assets_and_Localization/Localization_Guide.md">Localization Guide</a> • <a href="./Schema/Assets_and_Localization/Text_Formatting_and_Effects.md">Text Formatting</a> • <a href="./Schema/Assets_and_Localization/Strings.md">Strings</a></td>
  </tr>
  <tr>
    <td><strong>Reference & Meta</strong></td>
    <td><a href="./Schema/Reference_and_Meta/Enums.md">Enums</a> • <a href="./Schema/Reference_and_Meta/Arrays.md">Arrays</a> • <a href="./Schema/Reference_and_Meta/Item_Pools.md">Item Pools</a> • <a href="./Schema/Reference_and_Meta/Difficulties.md">Difficulties</a> • <a href="./Schema/Reference_and_Meta/Engine_Hidden_Passives_and_Statuses.md">Hidden Passives</a> • <a href="./Schema/Reference_and_Meta/Passive_Identifiers_Audit.md">Passive Audit</a> • <a href="./Schema/Reference_and_Meta/Engine_Uncategorized_Resources.md">Uncategorized Keys</a> • <a href="./Schema/Reference_and_Meta/Miscellaneous.md">Miscellaneous</a></td>
  </tr>
</table>

</details>

<details open>
<summary><strong>Directory Quick Navigation</strong></summary>

<table>
  <tr>
    <td width="22%"><strong>Abilities</strong></td>
    <td><a href="./Directory/Abilities/Ability_Pools.md">Ability Pools</a> • <a href="./Directory/Abilities/Cat_Abilities.md">Cat Abilities</a> • <a href="./Directory/Abilities/Enemy_and_Boss_Abilities.md">Enemy & Boss Abilities</a> • <a href="./Directory/Abilities/System_and_Item_Abilities.md">System & Item Abilities</a></td>
  </tr>
  <tr>
    <td><strong>Cats and Classes</strong></td>
    <td><a href="./Directory/Cats_and_Classes/Cat_Quotes.md">Cat Quotes</a> • <a href="./Directory/Cats_and_Classes/Classes.md">Classes</a> • <a href="./Directory/Cats_and_Classes/Custom_Cats.md">Custom Cats</a> • <a href="./Directory/Cats_and_Classes/Mutations.md">Mutations</a> • <a href="./Directory/Cats_and_Classes/Special_Strays.md">Special Strays</a> • <a href="./Directory/Cats_and_Classes/Tutorial_Cats.md">Tutorial Cats</a></td>
  </tr>
  <tr>
    <td><strong>Enemies and Combat</strong></td>
    <td><a href="./Directory/Enemies_and_Combat/Boss_Cutscene_Info.md">Boss Cutscene Info</a> • <a href="./Directory/Enemies_and_Combat/Combat_Rewards.md">Combat Rewards</a> • <a href="./Directory/Enemies_and_Combat/Elite_Buffs.md">Elite Buffs</a> • <a href="./Directory/Enemies_and_Combat/Enemies_and_Characters.md">Enemies & Characters</a> • <a href="./Directory/Enemies_and_Combat/Enemy_AI.md">Enemy AI</a> • <a href="./Directory/Enemies_and_Combat/Spawns_and_Enemy_Pools.md">Spawns & Enemy Pools</a> • <a href="./Directory/Enemies_and_Combat/Team_Names.md">Team Names</a></td>
  </tr>
  <tr>
    <td><strong>Items and Passives</strong></td>
    <td><a href="./Directory/Items_and_Passives/Item_Pools.md">Item Pools</a> • <a href="./Directory/Items_and_Passives/Item_Set_Bonuses.md">Item Set Bonuses</a> • <a href="./Directory/Items_and_Passives/Items_and_Equipment.md">Items & Equipment</a> • <a href="./Directory/Items_and_Passives/Passive_Pools.md">Passive Pools</a> • <a href="./Directory/Items_and_Passives/Passives.md">Passives</a></td>
  </tr>
  <tr>
    <td><strong>Statuses and Injuries</strong></td>
    <td><a href="./Directory/Statuses_and_Injuries/Injuries.md">Injuries</a> • <a href="./Directory/Statuses_and_Injuries/Status_Effect_Keywords.md">Status Effect Keywords</a></td>
  </tr>
  <tr>
    <td><strong>System and Engine</strong></td>
    <td><a href="./Directory/System_and_Engine/Damage_Text_Styles.md">Damage Text Styles</a> • <a href="./Directory/System_and_Engine/Difficulties.md">Difficulties</a> • <a href="./Directory/System_and_Engine/Particles_and_VFX_Dictionary.md">Particles & VFX Dictionary</a> • <a href="./Directory/System_and_Engine/Progression_Unlocks.md">Progression Unlocks</a></td>
  </tr>
  <tr>
    <td><strong>World and Events</strong></td>
    <td><a href="./Directory/World_and_Events/Events_and_Encounters.md">Events & Encounters</a> • <a href="./Directory/World_and_Events/Furniture_and_Metaprogression.md">Furniture & Metaprogression</a> • <a href="./Directory/World_and_Events/House_and_Environment.md">House & Environment</a> • <a href="./Directory/World_and_Events/Map_Generation_and_Routing.md">Map Generation & Routing</a> • <a href="./Directory/World_and_Events/NPC_Scripts.md">NPC Scripts</a> • <a href="./Directory/World_and_Events/Shops.md">Shops</a></td>
  </tr>
</table>

</details>
