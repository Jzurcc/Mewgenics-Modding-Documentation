# 07. Identifiers (Enums)

> **Purpose:** Representing fixed engine constants and entity references.

In most programming languages, `WaterTile` or `melee_attack` would be considered variables or constants. In GON, they are simply **unquoted strings** acting as identifiers or Enums.

## Parsing Context
The GON parser is contextual. It assumes that the **first token** on a line is the key, and the subsequent tokens form the value.

### ✅ Valid: Identifiers
*(Source evidence: `data/tiles.gon`, `data/abilities/basic_attacks.gon`)*
```gon
tile WaterTile
template melee_attack
```
- `tile` is parsed as the key.
- `WaterTile` is parsed as an unquoted string value.
- The engine then takes `"WaterTile"`, looks it up in its internal Enum list, and binds the appropriate logic.

## Casing Conventions
Identifiers use whatever casing the underlying Mewgenics C++ code expects. You must match the casing exactly.

- **PascalCase:** Often used for entity IDs and major systems (`WaterTile`, `BasicMelee`).
- **snake_case:** Used for most templates and logic hooks (`melee_attack`, `must_have_line_of_sight_unpurgable`).
- **lowercase:** Used for simple enums (`north`, `south`).
