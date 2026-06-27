# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


## Boss Cutscene Info

> **Associated Files:** `data/boss_cutscene_info.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 67

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 291 | `Default`<br>`FormChange`<br>`Druid` |
| [`frame_label`](./Enums.md#enum-frame_label) | Enum | Specifies the frame or cutscene animation label for the boss encounter. | 67 | `AlienBeast`<br>`ColorlessCat_Tutorial`<br>`DrMangler` |
| [`quotes`](./Arrays.md#array-quotes) | Array | An array of dialogue quotes for the boss cutscene. | 36 | `[` |

</details>

---

