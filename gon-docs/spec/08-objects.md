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
