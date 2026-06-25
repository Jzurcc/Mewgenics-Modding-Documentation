# 05. Numbers

> **Purpose:** Representing mathematical values.

GON natively supports standard numerical formats. 

## Integers
Plain decimal digits. Negative values are supported natively.

### ✅ Valid: Integers
*(Source evidence: `data/abilities/basic_attacks.gon`, `data/difficulties.gon`)*
```gon
bonus_itemroll_luck 200
elite_budget 0
offset -5
```

## Floats
Decimals use a standard period (`.`).
**Leading dots** are fully supported (you do not need a leading `0`).

### ✅ Valid: Floats
*(Source evidence: `data/difficulties.gon`)*
```gon
boss_health_multiplier 1.25
champ_chance_mini .25          // Valid leading dot
```

## Equations (Math Expressions)

Some values in Mewgenics look like math equations (`1+bonus_melee_range`). 
**To the GON parser, these are strings.**

GON does not evaluate math. It parses the entire expression as a raw text string, and passes it to the Mewgenics engine. The engine then runs its own internal math parser on that string.

### ✅ Valid: Equations
*(Source evidence: `data/abilities/basic_attacks.gon`)*
```gon
max_aoe 1+bonus_melee_range
```

## Unsupported Number Formats
GON does **not** support:
- Hexadecimal (`0x1A`)
- Binary (`0b10`)
- Exponential notation (`1e5`)
- Explicit positive prefixes (`+5`)
- `NaN` or `Infinity`
