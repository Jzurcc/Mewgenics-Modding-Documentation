# Step-by-Step Modding Guide

> **Purpose:** A walkthrough for taking your first idea from concept to injected mod.

## Prerequisites
Before you begin, you must use a tool to unpack the base game files. You should have a directory (often called `_unpacked`) that contains the base `data/` folder. **This is your reference material.**

---

## Step 1: Find the Original
Do not write code from scratch. Find something in the base game that is close to what you want.

If you want to make a new sword, use your text editor to search the `_unpacked/data/items` folder for an existing sword (e.g., search for `"kind weapon"`). You will likely end up in `weapons.gon`. Look at how the `GlassShard` or `RailSpikes` are built.

## Step 2: Set Up Your Mod Directory
**Never edit the `_unpacked` files directly.** If you break them, you lose your reference.

Create a new folder for your mod (e.g., `HauntersMod/`). 
Inside your mod folder, recreate the directory structure for the file you want to inject.
```text
HauntersMod/
└── data/
    └── items/
        └── haunters_weapons.gon
```

## Step 3: Write the GON
Open your new `haunters_weapons.gon` file.

### Goal A: Overwrite an existing item
If you want to change the `GlassShard` to have infinite durability, use the exact same Entity ID as the base game. When injected, the engine will overwrite the base `GlassShard` with yours.
```gon
GlassShard {
    name "ITEM_SHARDOFGLASS_NAME"
    rarity common
    kind weapon
    // Remove durability entirely, or set to an absurd number
}
```

### Goal B: Create a new item
If you are adding a completely new weapon, use a **namespace** so it doesn't collide with other mods.
```gon
Haunters_GhostBlade {
    name "ITEM_HAUNTERS_GHOSTBLADE_NAME"
    rarity legendary
    kind weapon
    durability 99
}
```
*(Remember: The game relies on localization keys for text. You will also need to add `ITEM_HAUNTERS_GHOSTBLADE_NAME` to your mod's localization string file!)*

## Step 4: Inject the Mod
Once your `.gon` file is ready, you must use the community modding toolchain (e.g., Mewtator) to inject your `HauntersMod/` folder into the live game. 

The toolchain will zip your files and merge them with the game's `data/` directory at runtime.

---

## ⚠️ Common Pitfalls

If your mod crashes the game or fails to load, check for these three common syntax errors:

1. **Forgetting Quotes:** If your string has a space, it MUST have double quotes.
   - ❌ `name My Cool Sword`
   - ✅ `name "My Cool Sword"`
2. **Capitalized Booleans:** Mewgenics strictly enforces lowercase booleans.
   - ❌ `paint True`
   - ✅ `paint true`
3. **Unmatched Braces:** Every `{` needs a matching `}`. If you miss one, the parser will swallow the rest of the file.
