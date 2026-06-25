# Troubleshooting & Error Reference

> **Purpose:** Common parsing mistakes in GON and how to fix them.

Because GON is incredibly permissive (ignoring commas and equals signs), the parser rarely "crashes", but it will misinterpret your data if you break structural rules.

---

## 1. The "Everything after this is broken" Error
**Cause:** Missing a closing brace `}` on a nested object.
**Symptom:** The parser thinks all subsequent objects in the file are children of the unclosed object. The game either crashes on load or the objects fail to spawn.

**Fix:** Count your braces. Every `{` needs a matching `}`.
```gon
❌  parent {
        child value
    // missing }

✅  parent {
        child value
    }
```

---

## 2. The "String merging" Error
**Cause:** Forgetting quotes around a string that contains spaces.
**Symptom:** Because space is the separator in GON, the parser thinks the second word is a new key-value node instead of part of the string.

**Fix:** Wrap multi-word text in double quotes `""`.
```gon
❌  name Tall Grass

✅  name "Tall Grass"
```

---

## 3. The "Invalid Boolean" Error
**Cause:** Capitalizing `True` or `False`.
**Symptom:** The game's engine expects the literal string `"true"` to trigger boolean logic. `"True"` does not match, so the boolean evaluates to false.

**Fix:** Use strict lowercase.
```gon
❌  paint True

✅  paint true
```

---

## 4. The "Unexpected Colon" Error
**Cause:** Muscle memory from JSON or YAML causing you to write `key: value`.
**Symptom:** The parser may see `key:` as the identifier, and fail to map it to the engine's expected `key`.

**Fix:** Use only whitespace to separate keys and values.
```gon
❌  health: 10
❌  health = 10

✅  health 10
```

---

## 5. The "Array Syntax" Error
**Cause:** Putting objects `{ }` inside arrays `[ ]`.
**Symptom:** GON arrays are intended for scalar values (strings, numbers, enums) or nested arrays. Mewgenics engine code rarely supports reading complex objects out of an array.

**Fix:** If you need multiple objects, assign them sequential numeric keys inside a parent object, or check the Schema for that specific property.
```gon
❌  levels [
        { name "1" }
        { name "2" }
    ]

✅  levels {
        0 { name "1" }
        1 { name "2" }
    }
```
