# Mewgenics Modding Guide

> **Purpose:** A comprehensive technical guide for constructing game-ready modifications. This documentation covers the core systems of Mewgenics modding: Classes, Abilities, and Passives.

## Prerequisites
Before you begin, you must unpack the base game files to use as reference material. You can use [Mewtator](https://www.nexusmods.com/mewgenics/mods/1) to manage your mods and unpack the game's `.gpack` file (simply open Mewtator and click `File > Unpack Base Resources`). This will create an `_unpacked/data/` folder containing the base game's scripts. **This is your reference material.** Do not edit the unpacked files directly; modifying these files will compromise your reference baseline.

---

## Core Requirement: Directory Mirroring
Your modification's directory structure must perfectly mirror the base game's structure. If the base game defines abilities in `data/abilities/`, your custom abilities must also be placed in a `data/abilities/` folder inside your mod. If files are placed outside of their expected hierarchy, the engine will fail to load them.

```text
MyMod/
└── data/
    ├── classes/
    │   └── my_custom_class.gon.patch
    ├── abilities/
    │   └── my_custom_abilities.gon
    └── passives/
        └── my_custom_passives.gon
```

---

## The Patch System (`.patch`, `.merge`, `.append`)
Mewgenics utilizes a proprietary data format (`.gon`), and the Mewtator mod loader relies on a specific syntax to patch these files without destructively overwriting the base game data.

To modify a base game file (e.g., `classes.gon`), you must create a patch file with the exact same name, appended with `.patch` (e.g., `classes.gon.patch`). Inside this file, utilize specific keywords for data injection:

- **`.merge` (Objects):** Used to insert or override a dictionary/object.
  ```gon
  // Inserts a new class object into the main classes dictionary
  HaunterClass.merge { 
      // Class data here
  }
  ```
- **`.append` (Arrays):** Used to push a new element into an existing array.
  ```gon
  // Pushes "HaunterClass" into a list of unlockable classes
  available_classes.append [ 
      HaunterClass 
  ]
  ```

---

## Phase 1: Class Implementation

To implement a new class, begin by modifying a `classes.gon.patch` file within your mod's `data/classes/` directory. Rather than wrapping all data in a single block, declare your class ID at the root level utilizing the `.merge` syntax.

```gon
// data/classes/classes.gon.patch

HaunterClass.merge {
    meta {
        name "CLASS_HAUNTER_NAME"
        description "CLASS_HAUNTER_DESC"
    }

    graphics {
        palette 12
        alt_animations [
            [idle, GhostIdle]
            [StartTurn, GhostStartTurn]
        ]
    }

    innate_items {
        weapon SpookyClaws
    }
    
    innate_passives {
        HaunterPassives [GhostlyForm]
    }

    attack_pool [
        BasicGhostStrike
    ]

    ability_pool [
        Spook
        Poltergeist
        EtherealPhase
    ]

    starter_abilities [
        Spook
    ]
}

// Append the new class to the available classes array
available_classes.append [ 
    HaunterClass 
]
```

**Crucial Note:** A class requires specific arrays to dictate which abilities it can execute. **If these arrays are omitted or left undefined, the engine will crash when attempting to load the class.**

---

## Phase 2: Ability Implementation

Abilities referenced in your class arrays must be defined within the `data/abilities/` directory. Create a new file (e.g., `my_abilities.gon`) to define them.

Every ability must declare a `template` definition (e.g., `template melee_attack`, `template spell`). Within the `meta` block, specify the `ability_icon` (base game icon IDs can be reused) and the string identifier for the `name`.

```gon
// data/abilities/my_abilities.gon

Spook {
    template spell
    
    meta {
        name "ABILITY_SPOOK_NAME"
        description "ABILITY_SPOOK_DESC"
        ability_icon ScaryFace
        class HaunterClass
    }

    cost {
        mana 2
    }

    target {
        range 3
        type enemy
    }

    damage_instance {
        damage 5
        statuses [
            Fear { duration 2 }
        ]
    }
}
```
*Note:* When creating an upgraded or modified iteration of an existing ability, utilize `variant_of BaseAbilityName` rather than duplicating the entire ability block from scratch.

---

## Phase 3: Passive Implementation

Passives adhere to the same structural syntax as abilities but must be situated in the `data/passives/` directory. Note that passives use the `icon` property rather than `ability_icon`.

Passives operate reactively and depend on Engine Keys (e.g., `CounterAttack`, `StatusOnTookDamage`, or `AddStatusToBasicAttack`) to function.

```gon
// data/passives/my_passives.gon

GhostlyForm {
    template passive
    
    meta {
        name "PASSIVE_GHOSTLYFORM_NAME"
        description "PASSIVE_GHOSTLYFORM_DESC"
        icon GhostSilhouette
    }

    StatusOnTookDamage {
        statuses [
            Invisibilty { duration 1 }
        ]
    }
    
    MeleeRevengeDamage {
        damage 2
    }
}
```

---

## Phase 4: Localization & Strings

The game engine maps localization keys to display text. String identifiers like `CLASS_HAUNTER_NAME` are used instead of hardcoded English words.

These string keys must be mapped in a CSV file. It is not necessary to inject these strings into the base game's `combined.csv`; you may provide a custom `.csv` file within your mod's localization directory (e.g., `data/localization/`) to map your text.

```csv
Key,English,French,Spanish
CLASS_HAUNTER_NAME,"Haunter","Hanteur","Cazador"
CLASS_HAUNTER_DESC,"A spooky phantom that terrifies enemies.","Un fantôme effrayant...","Un fantasma espeluznante..."
ABILITY_SPOOK_NAME,"Spook","Effrayer","Asustar"
```

---

## Phase 5: Audio & Music

To implement custom audio, supply `.ogg` files and place them in the appropriate directory hierarchy. You may overwrite an existing sound by utilizing the identical filename, or introduce an entirely new track.

When adding a new track to the in-game radio, you must register it in `data/audio/music_info.gon` and append the song name to the radio pool located in `data/audio/radio.gon`.

---

## Phase 6: Art Assets & Animations (`.swf`)

Art assets in Mewgenics are driven by compiled Flash files (`.swf`). This process represents the most complex aspect of modifying the game.

- **Viewing Assets:** Unpacked `.swf` files can be viewed using utilities such as [Ruffle](https://ruffle.rs/).
- **Editing Assets:** `.swf` files cannot be edited natively. You must employ a flash decompiler, such as [JPEXS Free Flash Decompiler (FFDec)](https://github.com/jindrapetrik/jpexs-decompiler), to convert the `.swf` back into an editable `.fla` file.
- **Creating Assets:** The `.fla` file can then be opened in Adobe Animate to implement new art and animations. Upon exporting back to `.swf`, ensure the new `.swf` file is registered within the game's `swflist.gon`.

*(Note: Action scripts are often broken during decompilation. A standard workaround is to export the `.fla` without scripts from JPEXS, and subsequently re-inject the original scripts.)*

---

## ⚠️ Common Pitfalls

If your mod fails to load or causes the engine to crash, verify the files against these common syntax errors:

1. **Missing Quotes:** If a string contains spaces, it must be enclosed in double quotes.
   - ❌ `name My Cool Sword`
   - ✅ `name "My Cool Sword"`
2. **Capitalized Booleans:** The engine strictly enforces lowercase booleans.
   - ❌ `paint True`
   - ✅ `paint true`
3. **Unmatched Braces:** Every `{` requires a terminating `}`. A missing brace will cause the parser to fail for the remainder of the file.
