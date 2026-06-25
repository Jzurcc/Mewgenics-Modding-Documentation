# Annotated Example: Item (`GlassShard`)

> **Source:** `data/items/weapons.gon`

This is a complete annotation of the `GlassShard` weapon, along with its `TinkererGlassShard` variant. This demonstrates how standard item definitions work and how to use inheritance (`variant_of`) to save time.

```gon
GlassShard {                    // ← The Entity ID (PascalCase)
    name "ITEM_SHARDOFGLASS_NAME" // ← Localization key
    desc "ITEM_SHARDOFGLASS_DESC" // ← Localization key
    rarity common               // ← Enum determining drop weight/pool
    kind weapon                 // ← Enum determining equipment slot
    frame 2                     // ← Integer referencing the sprite index in the item spritesheet
    durability [7, 12]          // ← Array representing a min/max roll for starting durability
    
    ability wp_GlassShard       // ← Identifier linking the weapon to the spell/attack it grants
}

TinkererGlassShard {            // ← A new, separate Entity ID
    variant_of GlassShard       // ← INHERITS all properties from the GlassShard block above
    durability [4 9]            // ← OVERRIDES the durability array with a worse roll
}
```

## Key Takeaways
1. **Arrays vs Commas:** Notice that the `GlassShard` uses `[7, 12]` while the `Tinkerer` uses `[4 9]`. Both are perfectly valid because GON ignores commas.
2. **Abilities:** The weapon itself does not deal damage. It grants the character the `wp_GlassShard` ability. The actual damage, range, and graphics of the attack are defined inside that ability's `.gon` block.
3. **Variant Inheritance:** When the engine loads `TinkererGlassShard`, it essentially copies the `name`, `desc`, `rarity`, `kind`, `frame`, and `ability` from the `GlassShard`, and only overwrites the `durability`. This is an incredibly powerful tool for modders making "Upgraded" versions of weapons.
