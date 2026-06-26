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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 291 |  |
| [`frame_label`](./Enums.md#enum-frame_label) | Enum | Specifies the label for a boss cutscene frame, identifying which character or scene is shown. | 67 |  |
| [`quotes`](./Arrays.md#array-quotes) | Array | List of dialogue quotes or lines for a boss cutscene. | 36 |  |

</details>

---

