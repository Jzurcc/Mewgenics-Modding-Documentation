# GON Format Comparison

> **Purpose:** A quick mapping for modders familiar with standard data formats.

GON was designed as a streamlined alternative to JSON, optimizing exclusively for human readability and writability at the expense of strict typing and machine interchangeability.

## Feature Comparison

| Feature | GON | JSON | TOML | YAML |
|---------|-----|------|------|------|
| **Comments** | ✓ `//` | ✗ | ✓ `#` | ✓ `#` |
| **Unquoted Strings** | ✓ (single words) | ✗ | ✗ | ✓ |
| **Optional Commas** | ✓ (ignored) | ✗ | ✗ | ✓ |
| **Optional Colons/Equals** | ✓ (whitespace used) | ✗ (`:`) | ✗ (`=`) | ✗ (`:`) |
| **Root Wrapper Required** | ✗ (Implicit root) | ✓ `{}` | ✗ | ✗ |
| **Trailing Commas** | N/A (commas ignored) | ✗ | ✓ | N/A |
| **Strict Typing** | ✗ (All parsed as strings) | ✓ | ✓ | ✓ |
| **Multi-line Strings** | ✗ | ✗ | ✓ `"""` | ✓ `>` or `\|` |
| **Nested Objects** | ✓ `{ }` | ✓ `{ }` | ✓ `[table]` | ✓ (indentation) |
| **Numeric Keys** | ✓ | ✗ | ✗ | ✓ |

## Transitioning from JSON

**Standard JSON syntax is natively supported.**

Because the GON parser treats commas `,` and colons `:` as ignorable whitespace, a perfectly formatted JSON file is completely valid GON. 

```json
{
    "name": "Water",
    "paint": "true"
}
```
*The GON parser reads the above JSON perfectly fine, stripping the quotes from the keys and ignoring the colons/commas.*

However, **the reverse is not true**. You cannot feed a `.gon` file into a JSON parser.
