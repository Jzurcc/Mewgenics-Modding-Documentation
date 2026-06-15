# Mewgenics Mod Developer Documentation: Getting Started

This documentation serves as the technical API reference for engineering Mewgenics mods. It assumes a basic understanding of software development and focuses on the underlying schema, syntax, and architecture of the engine.

## 1. The `.gon` File Format
Mewgenics uses a proprietary data format called **`.gon`** (Game Object Notation). It behaves similarly to JSON or YAML but with specific syntactic rules defined by the engine's creator, Tyler Glaiel.

### Syntax Rules
1. **Whitespace is King**: `.gon` files do not use commas to separate elements. Elements in an array or properties in an object are separated entirely by spaces or newlines.
2. **Hierarchical Blocks**: Objects are defined using curly braces `{}` and arrays are defined using square brackets `[]`.
3. **No Quotes Needed for Keys**: Keys do not require strings. Values only require strings `""` if they contain spaces.

**Example Schema:**
```gon
ClassName {
    meta {
        name "CAT_CLASS_NAME"
        description "CAT_CLASS_DESC"
    }
    
    // Arrays use brackets and are whitespace separated
    starter_abilities [
        AbilityOne
        AbilityTwo
    ]
}
```

## 2. Mod Project Architecture
A standard Mewgenics class mod should follow a strict directory structure mirroring the base game's architecture.

```text
MyMod/
├── description.json                 // Mod metadata for the mod manager
└── data/
    ├── classes/
    │   └── classes.gon.patch        // Patches the base game class list
    ├── abilities/
    │   └── custom_abilities.gon     // Defines new abilities
    └── text/
        └── custom_text.csv          // Localization strings
```

## 3. The `_unpacked` API Reference
The most powerful tool in a mod developer's arsenal is the `_unpacked` directory (usually found in your Mewtator mods folder). This contains the raw, uncompiled `.gon` files of the entire base game. 

Whenever you need to understand how the engine handles a specific edge case or how a specific spell is built, **do not guess**. Open the `_unpacked/data` folder and read the official implementation.
* `_unpacked/data/classes/classes.gon`
* `_unpacked/data/ability_templates/ability_templates.gon`

## 4. File Overwriting vs. Patching
When modifying base game data (such as adding a new class to the game's master list), you must use `.patch` files rather than overwriting the core files. Overwriting `classes.gon` will break the game or cause massive incompatibilities with other mods.

### Patching Operations
When you append `.patch` to a filename (e.g., `classes.gon.patch`), the engine uses specific operators to merge your data safely.

* **`.merge`**: Used to add or replace keys within an object `{}`.
* **`.append`**: Used to add elements to the end of an array `[]`.

**Example Patching (Adding a new class to the class list):**
```gon
// classes.gon.patch
// This appends your custom class to the master class list
class_list .append [
    MyCustomClass
]

// This merges your custom class definition into the root object
.merge {
    MyCustomClass {
        meta { ... }
        graphics { ... }
        // ... class definition ...
    }
}
```
