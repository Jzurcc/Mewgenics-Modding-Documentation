# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


## Damage Text Styles

> **Associated Files:** `data/damage_text_styles.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 26

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 206 |
| [`color`](./Arrays.md#array-color) | Array |  | 10 |
| [`right_icon`](./Enums.md#enum-right_icon) | String |  | 10 |
| [`back_icon`](./Enums.md#enum-back_icon) | String |  | 8 |
| [`outline_color`](./Enums.md#enum-outline_color) | Enum |  | 2 |
| [`suffix`](./Strings.md#string-suffix) | String |  | 1 |

</details>

---

