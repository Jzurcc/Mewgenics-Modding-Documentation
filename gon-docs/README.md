# GON Syntax Documentation

> **One-liner:** Formal syntactic specification and syntax reference for GON (Glaiel Object Notation) files in Mewgenics.

## What is GON?
GON is a custom data serialization format created by Tyler Glaiel, designed specifically for human-to-computer configuration and data entry. It is used extensively in Mewgenics to define everything from characters and abilities to map generation rules.

## First Principles: "JSON without the crap"
GON was designed with a core philosophy: **make it as easy as possible for a human to type.**
- **Typeless:** GON has no native type system. Everything parses as a string, and the game engine determines how to interpret it.
- **Permissive:** It ignores commas `,`, equals signs `=`, and colons `:`.
- **Low Noise:** Quotes are only required if a string contains spaces or special characters.
- **Implicit Root:** A single file can contain multiple standalone objects without needing a wrapper.

## Where to Go

| Goal | Destination |
|------|-------------|
| **I need to know what properties are valid for an Ability/Item/etc.** | Go to `../Schema/README.md` |
| **I need a quick reminder of how to format arrays or objects.** | [Cheat Sheet](reference/cheat-sheet.md) |
| **My file won't parse and I don't know why.** | [Error Reference](reference/error-reference.md) |
| **I know JSON/TOML/YAML. How is GON different?** | [Format Comparison](reference/comparison.md) |
| **I need the exact rule for how strings are parsed.** | `spec/` (See below) |

---

## The Specification (`spec/`)

The strict rules of the language, confirmed directly against the Mewgenics codebase.

- [00. Formal Grammar](spec/00-formal-grammar.md)
- [01. Overview & File Structure](spec/01-overview.md)
- [02. Comments](spec/02-comments.md)
- [03. Keys](spec/03-keys.md)
- [04. Strings](spec/04-strings.md)
- [05. Numbers](spec/05-numbers.md)
- [06. Booleans](spec/06-booleans.md)
- [07. Identifiers](spec/07-identifiers.md)
- [08. Objects](spec/08-objects.md)
- [09. Arrays](spec/09-arrays.md)
