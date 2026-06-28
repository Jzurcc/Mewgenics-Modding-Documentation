# 04. Strings

> **Purpose:** Representing text data.

GON supports both quoted and unquoted strings.

## Unquoted Strings (Bare Words)
If a string consists of a single contiguous word without spaces, special characters, or slashes, quotes are **optional** (and usually omitted by convention).

### ✓ Valid: Unquoted
*(Source evidence: `data/tiles.gon`)*
```gon
tile WaterTile
orientation north
```

## Quoted Strings
Double quotes (`"`) are required when a string contains:
1. Spaces.
2. Slashes (like file paths).
3. Certain special characters that might confuse the parser.

### ✓ Valid: Quoted
*(Source evidence: `data/tiles.gon`)*
```gon
name "Tall Grass"               // Contains a space
image "ground.png"              // Contains a dot (though sometimes bare words allow dots)
path "textures/grass.png"       // Contains a slash
```

## Escape Sequences and Multi-Line

Mewgenics GON **does not utilize** escape sequences (`\n`, `\t`, `\"`) or multi-line strings in its configuration files. 

For long dialogue or localized text, the engine relies on **localization keys** (which are bare words) that point to a separate translation database.

### ✓ Valid: Localization Key Paradigm
*(Source evidence: `data/catquotes.gon`)*
```gon
Fighter [
    CAT_VS_BOSS_QUOTES_FIGHTER_1
    CAT_VS_BOSS_QUOTES_FIGHTER_2
]
```

### ✗ Invalid: Multi-Line
```gon
desc "This is a 
multi-line string"  // ✗ Invalid
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
