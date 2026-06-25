# GON Quick Reference Cheat Sheet

A dense, visual reminder of how to format `.gon` files for Mewgenics.

## Core Rules
1. **No colons `:` or equals signs `=`**. Space is the only separator.
2. **No root wrapper needed**. Multiple top-level objects can coexist.
3. **Typeless parser**. `true` is a boolean, `1` is an integer, `WaterTile` is an enum, but to the GON parser, they are all just strings.

## Comments
```gon
// This is a full line comment
key value    // This is an inline comment

/* 
  ❌ Block comments are NOT supported 
*/
```

## Key-Value Pairs
```gon
// Unquoted string (enum/identifier)
tile WaterTile

// Quoted string (required for spaces or slashes)
name "Tall Grass"
image "textures/grass.png"

// Numbers
boss_health_multiplier 1.25     // Float
elite_budget 0                  // Integer
champ_chance .25                // Leading dots are valid
offset -5                       // Negative numbers are valid

// Booleans (MUST be lowercase)
paint true
animate_name false
```

## Objects (Blocks)
Objects use curly braces `{ }`. Do not put a separator before the brace.

```gon
// Standard Object
editor {
    name "Empty"
    image "empty.png"
}

// Deep Nesting is valid
graphics {
    animation Default
    damage_threshold_altanimations {
        heavyMelee 10
    }
}

// Numeric Keys are valid
0 {
    difficulty normal
}
```

## Arrays (Lists)
Arrays use square brackets `[ ]`. Values are separated by spaces.

```gon
// Array of strings
image ["ground.png" "ground_spots.png"]

// Array of enums
tags [ weapon_throw spell ]

// Multi-line arrays are valid
Fighter [
    CAT_VS_BOSS_QUOTES_FIGHTER_1
    CAT_VS_BOSS_QUOTES_FIGHTER_2
]

// Nested arrays
image_tint [[0 .5 0] [0 .5 0]]
```

## What NOT to do
```gon
key: value            // ❌ No colons
key = value           // ❌ No equals signs
"my key" { }          // ❌ No quoted keys
boolean True          // ❌ Must be lowercase 'true'
desc "Multi
line"                 // ❌ No multi-line strings
```
