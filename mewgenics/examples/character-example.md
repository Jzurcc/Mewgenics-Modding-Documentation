# Annotated Example: Character (`Rat`)

> **Source:** `data/characters/enemies.gon`

This is a complete, line-by-line annotation of the `Rat` enemy from the base game. It demonstrates how graphics, stats, physics, and abilities are bound to a single character entity.

```gon
Rat {                           // ← The Entity ID (PascalCase). This is how the engine spawns it.
    graphics {                  // ← Visual representation block
        movieclip Rat           // ← Enum referencing a Flash SWF animation export
        name "ENEMY_LILRAT_NAME"// ← Localization string key (Requires quotes due to engine convention, even without spaces)
        shadow_size .70         // ← Float controlling the drop shadow (leading dot is valid)
        
        tooltip "ENEMY_LILRAT_DESC" // ← Localization key for the hover text
    }

    stats {                     // ← Core RPG attributes block
        strength 4              // ← Integers
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {                // ← Physics and engine categorization block
        tag rat                 // ← Enum identifier used by AI/events to identify "rat-like" things
        faction enemies         // ← Enum assigning team alignment
        
        movement 1              // ← Grid squares per turn
        health 5                // ← Base max HP
        base_mana_regen 999     // ← Mana gained per turn (effectively infinite here)
    }

    abilities {                 // ← Bound combat actions block
        move DefaultMove        // ← Identifier linking to an ability in `abilities/`
        attack Dash_Enemy       // ← Identifier linking to the rat's default attack ability
        
        spells [                // ← Empty array. Rats have no spells.

        ]
    }

    passives {                  // ← Status effects and mutations block
        // An array of identifiers. The `CanMutateTo` passive specifically 
        // hooks into the elite generation system.
        CanMutateTo [Lumpy, Leaper] 
    }
}
```

## Key Takeaways
1. **Nesting:** The `Rat` object contains 5 child objects (`graphics`, `stats`, `properties`, `abilities`, `passives`).
2. **References:** The `Rat` does not define what `Dash_Enemy` does. It simply references the identifier `Dash_Enemy`, which is defined in a completely separate file (likely `data/abilities/basic_attacks.gon`).
3. **Implicit Structure:** You do not have to define every single possible property. If the `Rat` lacked the `passives` block entirely, the engine would simply assume it has no passives.
