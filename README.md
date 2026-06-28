---
title: "Mewgenics Modding Documentation"
description: "Root index for all Mewgenics modding guides, schemas, and specifications"
---

# Mewgenics Modding Documentation

This repository serves as an **unofficial** documentation and reference index for Mewgenics modding. It was originally compiled as a personal study resource, but has been shared to assist others in the modding community. It contains the structural schemas, syntax specifications, and practical guides required to implement custom classes, enemies, items, and abilities.

> [!WARNING]
> **Disclaimer:** This documentation is an individual, fan-made resource and is not foolproof. While heavily cross-referenced against the base game files, it may contain incorrect information, outdated assumptions, or incomplete schemas.

Mewgenics utilizes a proprietary engine architecture and data serialization format known as Glaiel Object Notation (GON). To accommodate this, the documentation is divided into four functional areas: **Theory**, **Syntax**, **Practice**, and **Reference**. Of these, the [**`Schema/`**](./Schema/) directory serves as your primary technical reference and is where you will likely spend the majority of your time during mod development.

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

Mod development in Mewgenics generally follows a strict four-step pipeline:

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
| [**`old-docs (deprecated)/`**](./old-docs%20%28deprecated%29/) | Legacy documentation files that I initially started with. Superseded by the `Schema/` directory. Retained solely for historical reference. |
