# 06. Booleans

> **Purpose:** True / False toggles.

Booleans must be strictly **lowercase**.

### ✅ Valid: Booleans
*(Source evidence: `data/tiles.gon`, `data/abilities/basic_attacks.gon`)*
```gon
paint true
animate_name false
```

### ❌ Invalid: Alternative Casings
Mewgenics requires strict lowercasing.
```gon
paint True     // ❌ Invalid
paint TRUE     // ❌ Invalid
paint yes      // ❌ Invalid
paint 1        // ❌ Will parse as Integer 1, not Boolean true
```

> **Note on "Types" in GON:**
> Because GON treats all values as strings internally during parsing, `true` and `"true"` would technically result in the same internal string. However, conventions dictate that boolean keywords should be written as unquoted bare words.
