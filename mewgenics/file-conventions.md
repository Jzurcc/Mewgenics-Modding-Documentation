# File & Engine Conventions

> **Purpose:** Understanding how the Mewgenics engine structures, loads, and manages `.gon` data files.

To construct modifications that seamlessly integrate with the engine and maintain compatibility, you must understand the engine's architectural assumptions.

---

## 1. Directory Layout
The base game data is stored in the `data/` folder, organized by semantic purpose:
- `/abilities/` & `/ability_templates/` - Spells, attacks, passives
- `/characters/` - Cats, bosses, enemies
- `/items/` - Consumables, weapons, trinkets
- `/maps/` - Overworld generation and level nodes
- `/events/` - Map events and dialogue encounters

When you create a mod, you should mirror this directory structure. If you are adding a new weapon, put your `.gon` file inside `data/items/`.

## 2. File Architecture and Object Grouping
A `.gon` file acts as an unstructured container for objects.
**The engine does not evaluate the filename when loading data.** 

If you put a character definition inside `data/items/my_weapon.gon`, the engine will likely load it successfully (though this violates standard architectural conventions). 

You can define 100 items in a single file (`my_big_mod.gon`), or you can create 100 separate files with one item each. The base game usually groups related objects (e.g., all weapons in `weapons.gon`).

## 3. Naming Conventions

By examining the base game, we can see clear casing conventions established by the developers:

- **Entity IDs (Object Keys):** `PascalCase`
  - Examples: `Rat`, `GlassShard`, `WaterTile`
- **Properties:** `snake_case`
  - Examples: `boss_health_multiplier`, `shadow_size`, `base_mana_regen`
- **Enums/Values:** Usually `lowercase` or `snake_case`
  - Examples: `common`, `weapon`, `melee_attack`

## 4. Mod Namespacing (Critical Requirement)

The Mewgenics engine loads all objects into a global pool, indexed by their Entity ID (the key).

**If two mods define an object with the exact same key, they will collide.**

To prevent this, you **must namespace your additions**. If your mod is called "Haunters", prepend your Entity IDs with `Haunters_`.

### ✓ Correct Namespacing
```gon
Haunters_GhostBlade {
    name "ITEM_HAUNTERS_GHOSTBLADE_NAME"
    kind weapon
}
```

### ✗ Incorrect (High Collision Risk)
```gon
GhostBlade {
    name "ITEM_GHOSTBLADE_NAME"
    kind weapon
}
```

*Note: If your explicit goal is to OVERWRITE a base game item, you should intentionally use the exact base game key (e.g., `GlassShard`).*

## 5. Inheritance (`variant_of`)

If you want to create a slightly modified version of an existing item or enemy, you do not need to copy/paste the entire block. Use the `variant_of` key to inherit the parent's properties.

```gon
TinkererGlassShard {
    variant_of GlassShard       // Inherit everything from GlassShard
    durability [4 9]            // Override the durability array
}
```
*The engine resolves this during load time, automatically cloning the properties of `GlassShard` into `TinkererGlassShard` before applying the new durability.*
