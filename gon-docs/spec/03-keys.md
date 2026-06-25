# 03. Keys

> **Purpose:** Defining the labels for values and blocks.

A key is the identifier on the left side of a node mapping.

## Syntax

- Keys are **bare words** consisting of alphanumeric characters, underscores (`_`), and sometimes hyphens (`-`).
- Keys are **case-sensitive** (`Meta` is not the same as `meta`).
- No colons `:` or equals signs `=` are used to separate a key from its value. The separator is simply **whitespace**.

### ✅ Valid: Standard Keys
*(Source evidence: `data/abilities/basic_attacks.gon`)*
```gon
template melee_attack
meta {
    name "ABILITY_NAME"
}
```

### ✅ Valid: Numeric Keys
*(Source evidence: `data/tiles.gon`)*
Keys do not need to start with a letter. Pure numbers are fully valid as keys.
```gon
0 {
    name "Water"
}
```

### ❌ Invalid: Quoted Keys
*(Source evidence: No instances observed in `data/`)*
You cannot use spaces in keys by quoting them.
```gon
"my key" {      // ❌ Invalid
    value 1
}
```

## Duplicate Keys

If you define the same key multiple times within the same block, the parser accepts it. The engine will read them sequentially. Depending on the specific property's logic, the engine may **override** the previous value or **accumulate/add** them together.

### ✅ Valid: Duplicate Keys
*(Source evidence: `data/difficulties.gon`)*
```gon
0 {
    boss_health_multiplier 1
    boss_health_multiplier 1.2    // Engine will process both
}
```
