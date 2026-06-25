# 09. Arrays

> **Purpose:** Defining lists of values.

Arrays in GON are lists of space-separated values enclosed in square brackets `[ ]`.

## Syntax
- **Separators:** Values are separated by whitespace (spaces or tabs).
- **Commas:** While you can technically include commas `,`, the parser treats them as whitespace/syntactic noise. It is standard convention to simply use spaces.

### ✅ Valid: Arrays
*(Source evidence: `data/tiles.gon`, `data/catquotes.gon`)*
```gon
image ["ground.png" "ground_spots.png"]
image_tint [blue blue]
```

## Multi-Line Arrays
Arrays can natively span multiple lines.

### ✅ Valid: Multi-Line Array
*(Source evidence: `data/catquotes.gon`)*
```gon
Fighter [
    CAT_VS_BOSS_QUOTES_FIGHTER_1
    CAT_VS_BOSS_QUOTES_FIGHTER_2
    CAT_VS_BOSS_QUOTES_FIGHTER_3
]
```

## Nested Arrays
Arrays can contain other arrays.

### ✅ Valid: Nested Arrays
*(Source evidence: `data/tiles.gon`)*
```gon
image_tint [[0,.5,0], [0,.5,0]]
```
*(Notice the commas here are permitted, but they are functionally ignored by the parser; `[[0 .5 0] [0 .5 0]]` is identical).*

## Heterogeneous Arrays
Because GON has no native type constraints, arrays can mix numbers, strings, and identifiers freely.

```gon
mixed_array [ 1 "two" true ]
```
