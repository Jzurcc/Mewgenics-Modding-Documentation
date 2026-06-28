# 00. Formal Grammar

> **Purpose:** The definitive syntactic specification for GON, expressed in Extended Backus-Naur Form (EBNF).

This grammar defines the precise rules of the permissive parser used in Mewgenics `.gon` files.

```ebnf
<document>      ::= <node>*
<node>          ::= <key> <value> 
                 |  <key> <object> 
                 |  <key> <array> 
                 |  <comment>

<key>           ::= <bare-word> | <quoted-string>
<bare-word>     ::= ( letter | digit | "_" | "-" | "." )+

<value>         ::= <quoted-string> 
                 |  <number> 
                 |  <boolean> 
                 |  <identifier>

<quoted-string> ::= '"' <char>* '"'
<identifier>    ::= <bare-word>

<number>        ::= ["-"] ( "." digit+ | digit+ ["." digit*] )
<boolean>       ::= "true" | "false"

<object>        ::= "{" <node>* "}"
<array>         ::= "[" ( <value> | <array> )* "]"

<comment>       ::= "//" <any-char-except-newline>*
```

> **Note on Syntactic Sugar (JSON Compatibility):** 
> The GON parser explicitly treats commas (`,`), colons (`:`), and equals signs (`=`) as optional syntactic whitespace. They are completely ignored. Therefore, standard JSON files will parse perfectly, even if they aren't represented in the strict grammar above.

## Component Breakdown

| Rule | Explanation & Prose Spec |
|------|-------------------------|
| `<document>` | A GON file is simply a list of 0 or more nodes. There is no root wrapper required. See [01. Overview](01-overview.md). |
| `<comment>` | `//` comments ignoring the rest of the line. See [02. Comments](02-comments.md). |
| `<node>` | Every node is a key mapping to a scalar value, an object, an array, or a comment. |
| `<key>` | Keys are typically unquoted, but standard JSON quoted strings are fully supported. See [03. Keys](03-keys.md). |
| `<quoted-string>` | Required when spaces or slashes are present. See [04. Strings](04-strings.md). |
| `<number>` | Integers and floats. Leading dots are permitted. See [05. Numbers](05-numbers.md). |
| `<boolean>` | Strictly lowercase. See [06. Booleans](06-booleans.md). |
| `<identifier>` | Unquoted strings (Enums/labels). See [07. Identifiers](07-identifiers.md). |
| `<object>` | Brace-wrapped blocks. Colons/equals are ignored. See [08. Objects](08-objects.md). |
| `<array>` | Bracket-wrapped, space-separated lists. See [09. Arrays](09-arrays.md). |


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
