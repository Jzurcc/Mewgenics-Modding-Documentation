# Common Pitfalls & Silent Failures

> **Purpose:** Common parsing mistakes in GON and how to fix them.

Because GON is incredibly permissive (ignoring commas and equals signs), the parser rarely "crashes". Instead, it will silently misinterpret your data if you break structural rules, resulting in logic bugs or objects failing to load in-game.

---

## 1. The Missing Brace Pitfall
**Cause:** Missing a closing brace `}` on a nested object.
**Symptom:** The parser assumes all subsequent objects in the file are children of the unclosed object. This usually results in a silent failure where your game objects simply do not appear.

**Fix:** Count your braces. Every `{` needs a matching `}`.
```gon
✗  parent {
        child value
    // missing }

✓  parent {
        child value
    }
```

---

## 2. The String Merging Pitfall
**Cause:** Forgetting quotes around a string that contains spaces.
**Symptom:** Because whitespace is the primary delimiter in GON, the parser interprets the second word as a completely new key instead of as part of the string value.

**Fix:** Wrap multi-word text in double quotes `""`.
```gon
✗  name Tall Grass

✓  name "Tall Grass"
```

---

## 3. The Capitalized Boolean Pitfall
**Cause:** Capitalizing `True` or `False`.
**Symptom:** The game's engine expects the exact string `"true"` or `"false"` to trigger boolean logic. Because GON is strictly case-sensitive, `"True"` does not match the expected value, often defaulting the internal boolean to false silently.

**Fix:** Use strict lowercase for booleans.
```gon
✗  paint True

✓  paint true
```

---

## 4. The Array/Object Mismatch Pitfall
**Cause:** Putting objects `{ }` inside arrays `[ ]`.
**Symptom:** While syntactically valid in GON, the Mewgenics engine code is often strictly typed on the backend. Many array properties are designed only to read scalar values (strings, numbers) and will silently fail to parse complex nested objects.

**Fix:** Always check the Schema for your specific property. If you need multiple objects, the standard convention is to assign them sequential numeric keys inside a parent object rather than using an array.
```gon
✗  levels [
        { name "1" }
        { name "2" }
    ]

✓  levels {
        0 { name "1" }
        1 { name "2" }
    }
```
