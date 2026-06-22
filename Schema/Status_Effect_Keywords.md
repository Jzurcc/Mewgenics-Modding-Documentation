# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Status Effect Keywords

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `name` | String | `"KEYWORD_ALLSTATSUP_NAME", "KEYWORD_ALPHA_NAME", "KEYWORD_ADRENALINE_NAME"` |  |
| `tooltip` | String | `"KEYWORD_ADRENALINE_DESC", "KEYWORD_BACKFLIP_DESC", "KEYWORD_ALPHA_DESC"` |  |
| `tooltip_stackless` | String | `"KEYWORD_ALPHA_DESC_STACKLESS", "KEYWORD_ATTRACTION_DESC_STACKLESS", none` |  |
| `tooltip_stacks` | String | `"KEYWORD_BLASTRESISTANCE_DESC", "KEYWORD_AMMO_DESC", "KEYWORD_ATTRACTION_DESC"` |  |
| `alias` | [`Enum/String`](./Enums.md#enum-alias) | `Infested, AllStatsUp, DodgeChance_Status` |  |
| `icon_frame` | Number | `152, 141, 17` |  |
| `tooltip_stacks_singular` | String | `"KEYWORD_CHARGEFISTS_DESC_SINGULAR", "KEYWORD_COUNTER_DESC", "KEYWORD_BLIND_DESC_STACKLESS"` |  |
| `tooltip_stacks_neg` | String | `"KEYWORD_ALLSTATSDOWN_DESC", "KEYWORD_CHADOWN_DESC", "KEYWORD_PERMABLIND_DESC"` |  |
| `name_stacks_neg` | String | `"KEYWORD_ALLSTATSDOWN_NAME", "KEYWORD_CHADOWN_NAME", "KEYWORD_CONDOWN_NAME"` |  |
| `tooltip_stacks_pos` | String | `"KEYWORD_CONUP_DESC", "KEYWORD_CHAUP_DESC", "KEYWORD_ALLSTATSUP_DESC"` |  |
| `name_reference_applier` | String | `"KEYWORD_LEECHES_NAME_APPLIER", "KEYWORD_MANALEECHES_NAME_APPLIER", "KEYWORD_ATTRACTION_REF"` |  |
| `tooltip_reference_applier` | String | `"KEYWORD_MANALEECHES_DESC_APPLIER", "KEYWORD_ATTRACTION_DESC_REF", "KEYWORD_LEECHES_DESC_APPLIER"` |  |
| `tooltip_stackless_neg` | String | `"KEYWORD_DAMAGEDOWN_DESC_STACKLESS", "KEYWORD_MOVEMENTDOWN_DESC_STACKLESS", "KEYWORD_TEMPINITDOWN_DESC"` |  |
| `tooltip_stackless_pos` | String | `"KEYWORD_MOVEMENTUP_DESC_STACKLESS", "KEYWORD_DAMAGEUP_DESC_STACKLESS"` |  |

</details>

---
