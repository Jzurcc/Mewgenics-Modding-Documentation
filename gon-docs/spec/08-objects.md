# 08. Objects

> **Purpose:** Grouping key-value pairs into nested structures.

Objects (sometimes called blocks) map string keys to values, arrays, or other objects.

## Syntax
An object is defined by a key, followed by a set of curly braces `{ }`. 

- **No Separators:** There is no colon `:` or equals sign `=` between the key and the opening brace.
- **Closing Braces:** You must provide exactly one closing brace `}` for every opening brace `{`.

### ✅ Valid: Object Definition
*(Source evidence: `data/abilities/basic_attacks.gon`)*
```gon
meta {
    name "ABILITY_NAME"
    desc "ABILITY_DESC"
}
```

## Nesting
Objects can be nested infinitely deep.

### ✅ Valid: Deep Nesting
*(Source evidence: `data/abilities/basic_attacks.gon`)*
```gon
graphics {
    animation Default

    damage_threshold_altanimations {
        heavyMelee 10
        heaviestMelee 20
    }
}
```

## Anonymous Objects
GON does **not** support anonymous objects (objects without a key). Every opening brace must be preceded by a key. 

Because GON does not strictly enforce types, it also does not natively support objects inside arrays (unless parsed via custom engine code), as arrays expect space-separated scalars or nested arrays.

### ❌ Invalid: Anonymous Object
```gon
{
    key value     // ❌ Invalid: Missing parent key
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
