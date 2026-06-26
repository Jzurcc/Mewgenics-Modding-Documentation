# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


## Status Effect Keywords

> **Associated Files:** `data/keyword_tooltips.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 236

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 206 |  |
| `icon_frame` | Integer |  | 128 |  |
| [`tooltip_stackless`](./Strings.md#string-tooltip_stackless) | String |  | 76 |  |
| [`tooltip_stacks`](./Strings.md#string-tooltip_stacks) | String |  | 69 |  |
| [`alias`](./Enums.md#enum-alias) | Enum |  | 57 |  |
| [`tooltip_stacks_singular`](./Strings.md#string-tooltip_stacks_singular) | String |  | 15 |  |
| [`tooltip_stacks_neg`](./Strings.md#string-tooltip_stacks_neg) | String |  | 13 |  |
| [`name_stacks_neg`](./Strings.md#string-name_stacks_neg) | String |  | 11 |  |
| [`tooltip_stacks_pos`](./Strings.md#string-tooltip_stacks_pos) | String |  | 10 |  |
| [`name_reference_applier`](./Strings.md#string-name_reference_applier) | String |  | 3 |  |
| [`tooltip_reference_applier`](./Strings.md#string-tooltip_reference_applier) | String |  | 3 |  |
| [`tooltip_stackless_neg`](./Strings.md#string-tooltip_stackless_neg) | String |  | 3 |  |
| [`tooltip_stackless_pos`](./Strings.md#string-tooltip_stackless_pos) | String |  | 2 |  |

</details>

---

