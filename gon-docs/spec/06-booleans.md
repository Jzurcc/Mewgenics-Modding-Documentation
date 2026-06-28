# 06. Booleans

> **Purpose:** True / False toggles.

Booleans must be strictly **lowercase**.

### ✓ Valid: Booleans
*(Source evidence: `data/tiles.gon`, `data/abilities/basic_attacks.gon`)*
```gon
paint true
animate_name false
```

### ✗ Invalid: Alternative Casings
Mewgenics requires strict lowercasing.
```gon
paint True     // ✗ Invalid
paint TRUE     // ✗ Invalid
paint yes      // ✗ Invalid
paint 1        // ✗ Will parse as Integer 1, not Boolean true
```

> **Note on "Types" in GON:**
> Because GON treats all values as strings internally during parsing, `true` and `"true"` would technically result in the same internal string. However, conventions dictate that boolean keywords should be written as unquoted bare words.

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
