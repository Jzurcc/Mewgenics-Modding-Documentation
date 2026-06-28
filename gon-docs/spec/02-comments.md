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
