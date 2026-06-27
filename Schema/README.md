# Mewgenics Object Schema

> **What is this folder?**
> This folder contains **semantic documentation** for the `.gon` files used in Mewgenics. It describes what keys are valid inside specific game objects (like Abilities, Characters, Items) and what the engine expects those keys to mean.

If you are looking for how to format a `.gon` file (the *syntax* rules like comments, braces, and arrays), see the `gon-docs/spec/` folder.


---


## How to Read These Files

The documentation in this folder is divided into three main types of files:

### 1. Schema Files
Files like `Abilities_and_Spells.md`, `Characters_and_Bosses.md`, and `Events_and_Encounters.md` map out the specific properties allowed for different objects.

They use tables structured like this:
| Property Key | Inferred Type | Definition | Count |
| :--- | :--- | :--- | :--- |

- **Property Key:** The exact string used as the key in the `.gon` file.
- **Inferred Type:** How the *Mewgenics engine* interprets the value. (See the Type Reference Table below).
- **Definition:** Explanation of what the key does in the engine.
- **Count:** How many `.gon` files in the base game use this key.

### 2. Enums (`Enums.md`)
Some keys expect a specific identifier from a fixed list (an Enum). `Enums.md` lists the confirmed valid string values for every enum-type key.
- Values marked as "Confirmed" mean they appear in the base game files.
- The engine may support additional values that aren't used in the vanilla game; you'll need to test these to discover them.

### 3. Gap Audits (`AUDIT_GAPS.md`)
Because the game updates and new keys are discovered, `AUDIT_GAPS.md` lists keys that have been found in the game's source files but haven't yet been fully documented in the Schema files. Always check this file if you're looking for an undocumented feature!

> **Note:** `Master_Schema_Dictionary.md` and `MASTER_SYNC_AUDIT.md` are legacy/abandoned files and may contain outdated information. Stick to the specific markdown files.


---


## Type Reference Table

> ⚠️ **Important:** GON has **no native type system**. All values are parsed as raw strings. The "Type" listed in these documentation tables describes the Mewgenics engine's *expected interpretation*, not a rigid GON syntax rule.

| Type Label | Meaning | Example |
|-----------|---------|---------|
| **Boolean** | Engine interprets as true/false | `true`, `false` |
| **Integer** | Engine interprets as a whole number | `5`, `100`, `-3` |
| **Float** | Engine interprets as a decimal number | `1.25`, `.5` |
| **Number** | Used when it is unknown if the engine strictly requires an Integer or a Float | `42` |
| **Enum** | Engine matches against a fixed set of identifiers | `melee_attack`, `north` |
| **String** | Engine uses as text (usually a localization key or file path) | `"ABILITY_NAME"`, `"cats/tabby.png"` |
| **Array** | Engine reads as a list of values | `[ Fire Holy ]`, `[ 1 2 3 ]` |
| **Object** | A nested key-value structure | `{ key value }` |
| **Equation** | Engine evaluates as a mathematical formula (may reference stat variables) | `1+bonus_melee_range`, `"ceil(X*.25)"` |


---


## File Index

| File | Covers |
|------|--------|
| `Abilities_and_Spells.md` | `abilities/` — spells, attacks, passives |
| `Characters_and_Bosses.md` | `characters/` — cats, enemies, bosses |
| `Events_and_Encounters.md` | `events/` — map events, choice nodes |
| `Passives_and_Statuses.md` | `passives/` — status effects, buffs |
| `Items_and_Equipment.md` | `items/` — weapons, armor, trinkets |
| `House_and_Environment.md` | `house/`, `tiles/` — furniture, tiles |
| `Cat_Classes.md` | `classes/` — cat classes and progression |
| `Cat_Mutations.md` | `mutations/` — visual and stat mutations |
| `Elite_Buffs.md` | Elite enemy modifiers |
| `Engine_LogicKeys.md` | Engine scripting keys (conditionals, loops) |
| `Engine_StatusAndPassiveKeys.md` | Status/passive engine hooks |
| `Engine_EventKeys.md` | Event scripting engine keys |
| `Engine_DamagingKeys.md` | Damage calculation engine keys |
| `Enums.md` | Valid values for every enum-type property |
| `AUDIT_GAPS.md` | Undocumented keys found in source files |