# Mewgenics Practical Modding Guides

> **What is this folder?**
> If the [`Schema/`](../Schema/) folder explains **what** the game expects, and [`gon-docs/`](../gon-docs/) explains **how to format** the text, this folder **details the practical implementation of modifications**.

This directory serves as the practical guide to Mewgenics modding. It contains comprehensive tutorials, architectural conventions, and detailed analyses of production game objects.

## Directory Index

| File | Purpose |
|------|---------|
| [File Conventions](file-conventions.md) | How the engine loads files, naming conventions, and mod namespacing. |
| [Modding Guide](modding-guide.md) | A step-by-step tutorial on creating and injecting your first mod. |

## Real-World Examples

Sometimes the easiest way to learn is by looking at code. Analyzing production code is a highly effective method for understanding engine conventions. We have taken real entities from the base game and annotated every single line to explain exactly what it does.

- [Annotated Character: `Rat`](examples/character-example.md)
- [Annotated Item: `GlassShard`](examples/item-example.md)
