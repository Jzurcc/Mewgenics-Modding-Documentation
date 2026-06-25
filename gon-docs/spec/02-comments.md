# 02. Comments

> **Purpose:** How to annotate code without it being parsed.

GON supports C-style single-line comments.

## Syntax

Everything from the `//` sequence to the end of the line is ignored by the parser.

### ✅ Valid: Full-Line Comments
*(Source evidence: `data/difficulties.gon`)*
```gon
// default difficulty
0 {
    boss_health_multiplier 1
}
```

### ✅ Valid: Inline Comments
*(Source evidence: `data/difficulties.gon`)*
```gon
0 {
    champ_chance_mini .25 // chance for maggots, fleas, etc to become champs
}
```

## Unsupported Comment Styles

Mewgenics GON does **not** support block comments or alternative comment characters.

### ❌ Invalid: Hash/Pound
```gon
# This is invalid
key value # Invalid inline comment
```

### ❌ Invalid: Block Comments
```gon
/*
This will cause a parser error.
*/
```
