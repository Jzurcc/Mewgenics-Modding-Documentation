# 03. Keys

> **Purpose:** Defining the labels for values and blocks.

A key is the identifier on the left side of a node mapping.

## Syntax

- Keys are **bare words** consisting of alphanumeric characters, underscores (`_`), and sometimes hyphens (`-`).
- Keys are **case-sensitive** (`Meta` is not the same as `meta`).
- While colons `:` and equals signs `=` are conventionally omitted, they are explicitly ignored by the parser. A key can be separated from its value by whitespace, colons, or equals signs interchangeably.

### ✓ Valid: Standard Keys
*(Source evidence: `data/abilities/basic_attacks.gon`)*
```gon
template melee_attack
meta {
    name "ABILITY_NAME"
}
```

### ✓ Valid: Numeric Keys
*(Source evidence: `data/tiles.gon`)*
Keys do not need to start with a letter. Pure numbers are fully valid as keys.
```gon
0 {
    name "Water"
}
```

### ✓ Valid: Quoted Keys (JSON Compatibility)
*(Source evidence: Standard JSON structure)*
While rarely seen in the game's actual data files, keys **can** be quoted to support standard JSON format or to include whitespace within the key name itself.
```gon
"my key": {      
    "value": 1
}
```

## Duplicate Keys

If you define the same key multiple times within the same block, the parser accepts it. The engine will read them sequentially. Depending on the specific property's logic, the engine may **override** the previous value or **accumulate/add** them together.

### ✓ Valid: Duplicate Keys
*(Source evidence: `data/difficulties.gon`)*
```gon
0 {
    boss_health_multiplier 1
    boss_health_multiplier 1.2    // Engine will process both
}
```

---

## The Specification (spec/)
The strict rules of the language, confirmed directly against the Mewgenics codebase.

- [00. Formal Grammar](00-formal-grammar.md)
- [01. Overview & File Structure](01-overview.md)
- [02. Comments](02-comments.md)
- [03. Keys](03-keys.md)
- [04. Strings](04-strings.md)
- [05. Numbers](05-numbers.md)
- [06. Booleans](06-booleans.md)
- [07. Identifiers](07-identifiers.md)
- [08. Objects](08-objects.md)
- [09. Arrays](09-arrays.md)
