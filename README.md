---
title: "Mewgenics Modding Documentation"
description: "Root index for all Mewgenics modding guides, schemas, and specifications"
---

# Mewgenics Modding Documentation

Welcome to the Mewgenics modding documentation root. This directory contains all the resources, tutorials, and schemas you need to create custom classes, enemies, items, and abilities for Mewgenics.

Because the game uses a highly custom data format and engine architecture, the documentation is split into three main pillars: **Theory**, **Syntax**, and **Practice**.

---

## Directory Overview

Here is a breakdown of where to find what you need:

| Directory | Focus Area | Description |
|-----------|------------|-------------|
| [**`Schema/`**](./Schema/) | **Theory (What to write)** | The comprehensive semantic index of the engine. Look here if you want to know what properties (keys) are valid for an Item, Character, or Ability, and how the C++ engine uses them. |
| [**`gon-docs/`**](./gon-docs/) | **Syntax (How to format)** | The formal specification for the `.gon` (Glaiel Object Notation) text format. Look here if your file is failing to parse or if you need to know the rules for arrays, strings, and objects. |
| [**`mewgenics/`**](./mewgenics/) | **Practice (How to build)** | Practical modding tutorials. Look here for step-by-step guides on making your first mod, understanding file architecture, and heavily annotated examples of real base-game objects. |

### Deprecated Documentation

| Directory | Description |
|-----------|-------------|
| [**`old-docs (deprecated)/`**](./old-docs%20%28deprecated%29/) | The original, legacy documentation files (01-18). These have been superseded by the `Schema/` directory, but are kept here for historical reference. The information within these files may be outdated or inaccurate. |

---

## Where should I start?

- **If you are completely new to Mewgenics modding:**  
  Start with the [**Step-by-Step Modding Guide**](./mewgenics/modding-guide.md).

- **If you want to know what a specific status effect or engine property does:**  
  Head into the [**Schema Index**](./Schema/README.md) and click on the relevant subsystem.

- **If your game is crashing when reading your mod:**  
  Check the [**GON Error Reference**](./gon-docs/reference/error-reference.md).
