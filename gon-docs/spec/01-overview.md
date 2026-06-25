# 01. Overview & File Structure

> **Purpose:** Baseline rules for GON file encoding, whitespace, and structural layout.

## Encoding & Line Endings

- **Encoding:** `UTF-8` is the standard encoding for Mewgenics data files.
- **Line Endings:** Windows CRLF (`\r\n`) is commonly observed, but standard LF (`\n`) is widely supported. 

## Whitespace is Delimitation

In GON, **whitespace separates tokens**. 
Both spaces (` `) and tabs (`\t`) are treated as valid separators. 

- **Indentation:** Entirely aesthetic. It does not affect parsing (unlike Python or YAML). The base game files predominantly use **tabs** for indentation.
- **Newlines:** A newline generally signifies the end of a node or entry, but arrays and objects can span multiple lines natively without escape characters.

## File Structure: The Implicit Root

A `.gon` file is fundamentally an **implicit list of nodes**. 

Unlike JSON, which requires exactly one root element (usually `{ }` or `[ ]`), a GON file can contain multiple top-level scalars, objects, or arrays sitting side-by-side.

### ✅ Valid: Multiple Top-Level Objects
*(Source evidence: `data/tiles.gon`)*

```gon
// Object 1
0 {
    editor {
        name "Empty"
    }
}

// Object 2
1 {
    tile WaterTile
    paint true
}
```

### ✅ Valid: Top-Level Scalars
*(Source evidence: `data/catgen.gon`)*

```gon
num_textures 250
num_bodies 250

voice_sets {
    male1 1
}
```

There is no need to wrap the entire file in an outer `root { }` block.
