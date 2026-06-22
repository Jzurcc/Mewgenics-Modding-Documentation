# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Abilities & Spells

> **Associated Files:** `data/abilities/, data/ability_templates/`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2343

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`damage_instance`](#context-damage_instance) | Block | Block defining the combat math and status effects applied upon successful hit. | 2343 |
| [`meta`](#context-meta) | Block | Block defining UI display data (Name, Description, Icon). | 2333 |
| [`template`](./Enums.md#enum-template) | Enum | Inherits baseline internal logic from a hardcoded engine template. | 2174 |
| [`graphics`](#context-graphics) | Block | Block defining visual animations and sequence timings. | 2037 |
| [`target`](#context-target) | Block | Block defining the shape, range, and restrictions of the ability's aiming phase. | 1862 |
| [`cost`](#context-cost) | Block | Block defining resource requirements (Mana, Act Points, Moves) needed to cast. | 1851 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum | Inherits properties from a previously defined ability (used for upgrading tiers). | 900 |
| [`tags`](./Arrays.md#array-tags) | Array | Array of string categories used by the engine for filtering (e.g. [weapon_throw, spell]). | 238 |
| [`self_damage`](#context-self_damage) | Block | Recoil or self-inflicted damage/effects applied to the caster. | 218 |
| [`spawn`](#context-spawn) | Block | Parameters for summoning new characters, objects, or entities. | 192 |
| [`bonus_passives`](#context-bonus_passives) | Block | Passives granted to the character while this ability is equipped. | 136 |
| [`class`](./Enums.md#enum-class) | Enum | Categorizes the ability for specific UI filters. | 90 |
| [`temporary_effects`](#context-temporary_effects) | Block | Status applications that wear off automatically or at the end of the turn. | 88 |
| [`sounds`](#context-sounds) | Block | Audio cues triggered by the ability. | 39 |
| [`splash_damage`](#context-splash_damage) | Block | Secondary Area of Effect blast parameters. | 34 |
| [`ai_ability`](./Enums.md#enum-ai_ability) | Enum | Overrides the ability used when triggered by AI. | 29 |
| [`keyword_tooltips`](#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear when hovering over the ability. | 23 |
| [`chain_ability`](./Enums.md#enum-chain_ability) | Enum | An ability that automatically executes sequentially after this one. | 15 |
| [`sub_ability`](./Enums.md#enum-sub_ability) | Enum | A secondary ability component referenced by complex templates. | 8 |
| [`cloned_ability`](./Enums.md#enum-cloned_ability) | Enum | Copies the properties of another ability dynamically. | 2 |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`empty_self_damage`](#context-empty_self_damage) | Block | Recoil damage specifically applied when the attack misses all targets. | 2 |
| [`bonk_damage`](#context-bonk_damage) | Block | Damage dealt when knocked into a wall or obstacle. | 1 |
| [`damage`](#context-damage) | Block | The base damage properties of an attack. | 1 |

</details>

---

### Context: `damage_instance`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2344

> **Referenced by:** [`NukeQuestFinalBossModifications`](#context-nukequestfinalbossmodifications), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damage Blocks}`](./Engine_Damage.md#all-confirmed-damage-instance-values) | Block | A damage hit definition. See Engine_Damage.md for the full schema. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1785 |
| `damage` | Integer | The base damage properties of an attack. | 1446 |
| [`type`](./Enums.md#enum-type) | Enum | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). | 358 |
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 352 |
| [`knockback`](./Math_Equations.md) | Integer | The base physics pushing power (in tiles). | 254 |
| `ai_base_score` | Integer | How highly the AI values using this ability. | 223 |
| `heal` | Integer | Restores health instead of dealing damage. | 122 |
| `cant_miss` | Boolean | Guarantees the hit, bypassing dodge mechanics. | 110 |
| `incidentally_collects_pickups` | Boolean | Automatically grabs items in the AoE. | 103 |
| [`custom_additional_ai_weight`](./Enums.md#enum-custom_additional_ai_weight) | Enum | Granular AI preference adjustments (e.g., `prefer_dont_move`). | 82 |
| `piercing` | Boolean | Ignores a percentage of target defense/armor. | 52 |
| `makes_contact` | Boolean | If false, explicitly avoids triggering contact-based passives. | 40 |
| [`layer`](./Enums.md#enum-layer) | Enum | Z-index targeting (e.g., `characters`, `self`). | 26 |
| [`blocked_damage`](./Math_Equations.md) | Equation | Base damage dealt if the attack is blocked. | 24 |
| [`raw_damage`](./Math_Equations.md) | Equation | Unmitigated, unscaled base numbers. | 22 |
| `crit_chance` | Float | Override for base critical hit probability. | 16 |
| `override_trample_damage` | Boolean | Custom damage value for trample moves. | 15 |
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. | 14 |
| `can_revive` | Boolean | Healing instance that can bring dead allies back to life. | 8 |
| `show_damage_on_0` | Boolean | Forces the "-0" floater text to appear. | 6 |
| `force_play_hit_animation` | Boolean | Forces the flinch animation even on 0 damage. | 5 |
| `blocked_multiplier` | Integer | Multiplier applied when hitting a blocking target. | 4 |
| `accuracy` | Float | Hit chance modifier. | 3 |
| `can_collect_pickups` | Boolean | The damage instance can grab items on the ground. | 3 |
| `can_instapop` | Boolean | Allows the attack to instantly destroy specific weak entities. | 2 |
| `disallow_modifications` | Boolean | Prevents passives from altering this damage instance. | 2 |
| `force_no_contact` | Boolean | Bypasses all contact-based retaliation (Thorns, etc). | 2 |
| `non_lethal` | Boolean | Reduces target to 1 HP but will never kill. | 2 |
| [`raw_heal`](./Math_Equations.md) | String | Unmitigated, unscaled base numbers. | 2 |
| `two_way_contact` | Boolean | Both caster and target trigger contact effects on each other. | 2 |
| `damage_shield_only` | Boolean | Depletes shields but cannot harm base health. | 1 |
| [`faction`](./Enums.md#enum-faction) | Enum | Determines alignment (`enemies`, `cats`, `neutral`). | 1 |
| [`final_hit_bonus_damage`](./Math_Equations.md) | Equation | Extra damage applied on the last hit of a multihit. | 1 |
| `force_adjacent_and_diagonal_contact` | Boolean | Treats diagonal hits as physical contact. | 1 |
| `force_no_knockback` | Boolean | Prevents the target from being pushed. | 1 |
| `hint_dont_lowgravboost` | Boolean | AI hint to ignore wind physics. | 1 |
| [`hit_animation_alt`](./Enums.md#enum-hit_animation_alt) | Enum | Custom flinch animation for the target. | 1 |
| `ranged` | Boolean | Boolean flagging the damage as explicitly ranged. | 1 |

</details>

---

### Context: `meta`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2333

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String | The localization key for the ability's display description. | 1641 |
| [`name`](./Strings.md#string-name) | String | The localization key for the ability's display name. | 1597 |
| [`class`](./Enums.md#enum-class) | Enum | Categorizes the ability for specific UI filters. | 876 |
| [`type_icon`](./Strings.md#string-type_icon) | String |  | 283 |
| `animate_name` | Boolean | If true, adds a visual pop/animation to the name text when cast. | 177 |
| [`icon_shell_frame`](./Strings.md#string-icon_shell_frame) | String |  | 28 |
| [`is_move`](./Enums.md#enum-is_move) | Boolean |  | 20 |
| [`ability_icon`](./Enums.md#enum-ability_icon) | String | The UI icon to display in the action bar. | 14 |
| [`tooltip_values`](./Arrays.md#array-tooltip_values) | Array |  | 9 |
| [`icon_damage_display`](./Strings.md#string-icon_damage_display) | String |  | 8 |
| [`icon_damage_display_eq`](./Math_Equations.md) | String |  | 7 |
| `is_basic_attack` | Boolean |  | 4 |
| [`icon_damage_type`](./Enums.md#enum-icon_damage_type) | String |  | 3 |
| `is_trinket` | Boolean |  | 3 |
| `dont_visualize_ai` | Boolean |  | 2 |
| [`icon_damage_display_suffix`](./Strings.md#string-icon_damage_display_suffix) | String |  | 2 |
| `is_weapon` | Boolean |  | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |

</details>

---

### Context: `graphics`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2037

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Graphics Blocks}`](./Engine_Graphics.md#all-confirmed-graphic-block-values) | Block | A visual/animation configuration. See Engine_Graphics.md for the full schema. |  |
| [`animation`](./Enums.md#enum-animation) | Enum | The primary flash animation label triggered. | 1559 |
| [`particle`](./Enums.md#enum-particle) | Enum | References an impact or cast particle effect. | 488 |
| [`projectile`](./Enums.md#enum-projectile) | Enum | References a projectile entity. | 228 |
| `lob` | Boolean |  | 130 |
| `delay` | Float | Frame delay before firing projectile/effect. | 93 |
| `dont_visualize_ai` | Boolean |  | 86 |
| `dont_orient` | Boolean | Prevents the character from turning to face the target. | 83 |
| [`dash_animation`](./Enums.md#enum-dash_animation) | Enum | State-specific animations for trample/dash abilities. | 65 |
| [`dash_start_animation`](./Enums.md#enum-dash_start_animation) | Enum |  | 63 |
| `speed` | Float | Rotations per second. | 61 |
| [`affected_particle`](./Enums.md#enum-affected_particle) | Enum | Visuals applied to the target receiving the effect. | 51 |
| [`dash_attack_animation`](./Enums.md#enum-dash_attack_animation) | Enum |  | 45 |
| `lob_height` | Integer | Adjustments for arcing projectiles. | 45 |
| [`animation_in`](./Enums.md#enum-animation_in) | Enum | Used for transition states (like burrowing). | 43 |
| [`animation_out`](./Enums.md#enum-animation_out) | Enum | Used for transition states (like burrowing). | 43 |
| [`jump_attack_animation`](./Enums.md#enum-jump_attack_animation) | Enum | Overrides for jump physics. | 39 |
| `use_projectile` | Boolean |  | 35 |
| [`full_jump_animation`](./Enums.md#enum-full_jump_animation) | Enum |  | 24 |
| `full_jump_sync_frames` | Integer |  | 24 |
| `use_rotation` | Boolean |  | 24 |
| [`dash_end_animation`](./Enums.md#enum-dash_end_animation) | Enum |  | 22 |
| `palette` | Integer | Swaps the color palette ID. | 21 |
| `full_jump_windup_frames` | Integer |  | 20 |
| `visual_delay_but_simultaneous_damage` | Integer |  | 18 |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum | Specific spawn points for particles. | 17 |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum | Specific spawn points for particles. | 16 |
| `fall_from_sky` | Boolean | Spawns the projectile from the top of the screen. | 16 |
| [`move_start_animation`](./Enums.md#enum-move_start_animation) | Enum |  | 14 |
| `use_placeholder` | Boolean |  | 14 |
| [`move_end_animation`](./Enums.md#enum-move_end_animation) | Enum |  | 13 |
| `face_toss_target` | Boolean |  | 12 |
| `ignore_slowtiles` | Boolean |  | 12 |
| `chain_distance` | Float | Creates a tethered repeating graphic (like a hook). | 11 |
| [`chain_movieclip`](./Enums.md#enum-chain_movieclip) | Enum | Creates a tethered repeating graphic (like a hook). | 11 |
| `darken_screen` | Boolean | Dims the background during the ability cast. | 11 |
| [`beam_cap`](./Enums.md#enum-beam_cap) | Enum | Flash movieclips used to render continuous laser beams. | 10 |
| [`beam_clip`](./Enums.md#enum-beam_clip) | Enum | Flash movieclips used to render continuous laser beams. | 10 |
| `bounce_on_hit` | Boolean | Visual hop when striking a target. | 10 |
| `darken_screen_exclude_characters_on_tile` | Boolean |  | 10 |
| [`end`](./Enums.md#enum-end) | Enum | Segments for continuous channeled animations. | 10 |
| [`jump_start_animation`](./Enums.md#enum-jump_start_animation) | Enum |  | 10 |
| [`loop`](./Enums.md#enum-loop) | Enum | Segments for continuous channeled animations. | 10 |
| [`prime_animation`](./Enums.md#enum-prime_animation) | Enum |  | 10 |
| [`start`](./Enums.md#enum-start) | Enum | Segments for continuous channeled animations. | 10 |
| `max_tiles_single_loop` | Integer |  | 9 |
| [`random_delay`](./Arrays.md#array-random_delay) | Array | Adds chaotic timing to multi-projectile casts. | 9 |
| `sync_speed` | Integer |  | 9 |
| `fx_is_placeholder_animation` | Boolean |  | 8 |
| `aoe_spell_on_land` | Boolean | Visual trigger when a jump lands. | 7 |
| `fx_random_flip` | Boolean |  | 7 |
| [`land_animation`](./Enums.md#enum-land_animation) | Enum |  | 7 |
| [`miss_particle`](./Enums.md#enum-miss_particle) | Enum | Specific spawn points for particles. | 7 |
| `use_super_armor` | Boolean | Prevents flinch animations from interrupting this cast. | 7 |
| [`air_animation`](./Enums.md#enum-air_animation) | Enum | Animation played while entity is airborne. | 6 |
| [`custom_priming_animation`](./Enums.md#enum-custom_priming_animation) | Enum | Animation used while charging an ability. | 6 |
| `darken_screen_exclude_self` | Boolean |  | 6 |
| `darken_screen_start_early` | Boolean |  | 6 |
| `fall_randomize_timing` | Float |  | 6 |
| `min_throw_height` | Float |  | 6 |
| [`miss_random_delay`](./Arrays.md#array-miss_random_delay) | Array |  | 6 |
| `single_projectile` | Boolean |  | 6 |
| [`detatched_animation`](./Enums.md#enum-detatched_animation) | Enum | Plays an animation separated from the character body. | 5 |
| `detatched_animation_reach` | Integer |  | 5 |
| [`empty_animation`](./Enums.md#enum-empty_animation) | Enum |  | 5 |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 5 |
| `fixed_jump_height` | Float |  | 4 |
| [`rocket_swirl`](#context-rocket_swirl) | Block | Visual parameters for swirling projectile paths. | 4 |
| `sync_frames` | Integer |  | 4 |
| [`dash_decelerating_animation`](./Enums.md#enum-dash_decelerating_animation) | Enum |  | 3 |
| `decelerate` | Integer | Visual slowdown at the end of a movement. | 3 |
| `delay_from_map_edge` | Boolean | Delays effect based on distance from the screen edge. | 3 |
| `easing` | Integer | Smoothing function for movement animations. | 3 |
| [`fixed_jump_speed`](./Enums.md#enum-fixed_jump_speed) | Float |  | 3 |
| [`grab_animation`](./Enums.md#enum-grab_animation) | Enum |  | 3 |
| `lob_yoff` | Float | Adjustments for arcing projectiles. | 3 |
| `lock_orientation_during_dash` | Boolean | Prevents the sprite from flipping mid-dash. | 3 |
| `use_projectile_spawn_offset` | Boolean |  | 3 |
| `use_rotation_once` | Boolean |  | 3 |
| `always_play_animations` | Boolean | Bypasses speed-up/skip logic. | 2 |
| `detatched_animation_cutoff` | Boolean |  | 2 |
| `do_damage_immediately` | Boolean | Applies math before the animation actually hits. | 2 |
| `jump_height_multiplier` | Float | Overrides for jump physics. | 2 |
| [`mask_center`](./Enums.md#enum-mask_center) | Enum |  | 2 |
| [`mask_extent`](./Enums.md#enum-mask_extent) | Enum |  | 2 |
| `max_throw_height` | Float |  | 2 |
| [`particle_mat`](./Enums.md#enum-particle_mat) | Enum |  | 2 |
| [`preturn_animation`](./Enums.md#enum-preturn_animation) | Enum |  | 2 |
| [`primed_alt_animation`](./Strings.md#string-primed_alt_animation) | String |  | 2 |
| [`pseudoprojectile`](./Enums.md#enum-pseudoprojectile) | Enum |  | 2 |
| `reverse_orientation` | Boolean |  | 2 |
| `self_damage_mid_port` | Boolean |  | 2 |
| `throw_speed` | Integer |  | 2 |
| `use_hit_alts` | Boolean |  | 2 |
| [`affected_animation`](./Enums.md#enum-affected_animation) | Enum | Visuals applied to the target receiving the effect. | 1 |
| [`ally_animation`](./Enums.md#enum-ally_animation) | Enum | Distinct animation used when targeting a friendly unit. | 1 |
| [`animate_name`](./Enums.md#enum-animate_name) | String | Animates the ability name text on cast. | 1 |
| `apex_distance` | Float | Calculations for the peak of a jump/lob arc. | 1 |
| `apex_time` | Float | Calculations for the peak of a jump/lob arc. | 1 |
| `bypass_combatspeed` | Boolean |  | 1 |
| [`damage_threshold_altanimations`](#context-damage_threshold_altanimations) | Block | Triggers different hit animations based on the amount of damage dealt. | 1 |
| [`dash_bonk_animation`](./Enums.md#enum-dash_bonk_animation) | Enum |  | 1 |
| `delay_from_map_center` | Boolean | Positional based timing delays. | 1 |
| `delay_from_reverse_map_edge` | Boolean |  | 1 |
| `do_animation_offscreen` | Boolean |  | 1 |
| `do_not_clear_placeholder` | Boolean |  | 1 |
| `face_targets` | Boolean | Forces the sprite to look at the target tile. | 1 |
| `first_castpoint_is_self_damage_only` | Boolean |  | 1 |
| `hang_time` | Float |  | 1 |
| `jump_speed_multiplier` | Float |  | 1 |
| `lob_speed` | Float | Adjustments for arcing projectiles. | 1 |
| `max_range` | Integer | The maximum and minimum distance required to cast. | 1 |
| `min_range` | Integer | The maximum and minimum distance required to cast. | 1 |
| `othercat_placeholder_available` | Boolean |  | 1 |
| `precast_delay` | Float |  | 1 |
| [`spawn_offset`](./Arrays.md#array-spawn_offset) | Array |  | 1 |
| `uncatchable` | Boolean |  | 1 |
| `use_directional_animations` | Boolean |  | 1 |
| `use_origin_offsets` | Boolean |  | 1 |

</details>

---

### Context: `effects`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2012

> **Referenced by:** [`DoDamage`](#context-dodamage), [`MeleeRevengeDamage`](#context-meleerevengedamage), [`ROOT`](#context-root), [`RevengeDamage`](#context-revengedamage), [`bonk_damage`](#context-bonk_damage), [`damage_instance`](#context-damage_instance), [`empty_self_damage`](#context-empty_self_damage), [`self_damage`](#context-self_damage), [`splash_damage`](#context-splash_damage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`LowerAmbientLight`](#context-lowerambientlight) | Block | A visual effect that dims the map's lighting. | 2 |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Else`](#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 59 |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 27 |
| [`Consumed`](#context-consumed) | Block | State block triggered when this object or entity is eaten/consumed by another character. | 15 |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 13 |
| [`ApplyToSourceOnKill`](#context-applytosourceonkill) | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 11 |
| [`ApplyPassives`](#context-applypassives) | Block | Grants the nested passive abilities dynamically. | 9 |
| [`ApplyStatusIfCrit`](#context-applystatusifcrit) | Block | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. | 7 |
| [`TakeBonusTurnWithStatus`](#context-takebonusturnwithstatus) | Block | Grants the character an immediate extra turn while afflicted with specific statuses. | 4 |
| [`TakeBonusTurnWithAIControl`](#context-takebonusturnwithaicontrol) | Block | Grants the character an immediate extra turn, but forces the AI to control them during it. | 2 |
| [`Conditional_HasCleansableDebuffs`](#context-conditional_hascleansabledebuffs) | Block | Conditional trigger: Executes nested logic if the target currently has negative status effects that can be cleansed. | 1 |
| [`CreateGlobalModifiers`](#context-createglobalmodifiers) | Block | Generates global map or encounter rules/modifiers. | 1 |
| [`StatusGroup`](#context-statusgroup) | Block | Groups multiple status effects together for batch application. | 1 |

</details>

---

### Context: `target`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1862

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_range` | Integer | The maximum and minimum distance required to cast. | 1088 |
| `max_aoe` | Integer | The maximum and minimum radius/length of the AoE. | 795 |
| `min_range` | Integer | The maximum and minimum distance required to cast. | 583 |
| [`target_mode`](./Enums.md#enum-target_mode) | Enum | How the cursor operates (`tile`, `direction`, `none`). | 503 |
| [`restrictions`](./Arrays.md#array-restrictions) | Enum | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). | 463 |
| [`aoe_mode`](./Enums.md#enum-aoe_mode) | Enum | The shape of the area (`standard`, `line`, `cross`, `square`, `custom`). | 432 |
| [`knockback_mode`](./Enums.md#enum-knockback_mode) | Enum | How physics vectors apply (`character_to_tile`, `pull_to_character`, `zero`, `orientation`). | 265 |
| `min_aoe` | Integer | The maximum and minimum radius/length of the AoE. | 253 |
| `aoe_excludes_self` | Boolean | Prevents the AoE from hitting the caster. | 241 |
| [`aoe_restrictions`](./Arrays.md#array-aoe_restrictions) | Array | Array of conditions the AoE tiles must meet (e.g., `must_have_line_of_sight_unpurgable`). | 197 |
| `aoe_considers_character_size` | Boolean | Scales the AoE based on the caster's tile size (e.g., 2x2). | 170 |
| [`range_mode`](./Enums.md#enum-range_mode) | Enum | How range is counted (`standard`, `ground_move`). | 114 |
| [`X_is`](./Enums.md#enum-x_is) | Enum | Applies or references the 'X_is' effect/state. | 86 |
| [`custom_aoe`](./Arrays.md#array-custom_aoe) | Array | Array of exact coordinates for a custom shape (e.g., `[[1, -1] [1, 0]]`). | 83 |
| `multihit` | Integer | Hardcoded number of times the ability hits the target. | 62 |
| `max_targets` | Integer | Limits on how many distinct entities can be targeted. | 56 |
| `range_excludes_blocking` | Boolean | Cannot target through walls/obstacles. | 53 |
| `prioritize_dont_change_direction` | Integer | AI preference to maintain current facing angle. | 52 |
| [`target_requires_tag`](./Enums.md#enum-target_requires_tag) | Enum | Target must possess this exact character tag. | 40 |
| [`aoe_symmetry`](./Enums.md#enum-aoe_symmetry) | Enum | Determines if the AoE mirrors on axes. | 28 |
| `prioritize_face_camera` | Integer | AI preference to face South. | 26 |
| `straight_shot` | Boolean | Ensures projectiles do not arc. | 24 |
| `can_multihit` | Boolean | If true, overlapping AoEs can hit the same target multiple times. | 17 |
| `allow_any_orientation` | Boolean | Allows casting regardless of the character's facing direction. | 16 |
| `range_considers_character_size` | Boolean | Range calculation accounts for large entities. | 16 |
| `throw_consumed_character` | Boolean | Throws the entity currently held/eaten. | 15 |
| `min_targets` | Integer | Limits on how many distinct entities can be targeted. | 14 |
| `aoe_leading_edge_only` | Boolean | Only the outermost edge of the AoE shape applies effects. | 13 |
| `allow_diagonals` | Boolean | Allows targeting on diagonal grid axes. | 12 |
| `range_display_include_character_size` | Boolean | Visual: offsets the range indicator for 2x2 units. | 12 |
| `stagger_multihit_targets` | Boolean | Delays hits slightly between multiple targets. | 12 |
| `upgrade_straight_shot_to_piercing` | Boolean | Allows the projectile to pass through multiple targets. | 11 |
| `delayed_trigger` | Boolean | Delays the actual execution of the target effect. | 10 |
| `consider_trample` | Boolean | AI consideration for moving through units. | 9 |
| `N` | Integer | Variable modifier parameter. | 7 |
| [`custom_range`](./Arrays.md#array-custom_range) | Array | Overrides standard range scaling. | 7 |
| `always_bounce` | Boolean | Forces the attack/projectile to bounce regardless of hit. | 6 |
| [`custom_aoe_util`](./Arrays.md#array-custom_aoe_util) | Array | Utility variants of custom AoE definitions. | 6 |
| `multihit_max` | Integer | Variable limits for random multihit abilities. | 6 |
| `multihit_min` | Integer | Variable limits for random multihit abilities. | 6 |
| `reorient_thrown_character` | Boolean | Forces a thrown entity to face a certain way. | 6 |
| [`toss_direction_restriction`](./Enums.md#enum-toss_direction_restriction) | Enum | Limits which ways an entity can be tossed. | 6 |
| `aoe_hint_teamcast` | Boolean | Visual hint for cooperative casting abilities. | 5 |
| [`aoe_tile_requires_element`](./Enums.md#enum-aoe_tile_requires_element) | Enum | Only affects tiles painted with a specific element. | 5 |
| `distance_sort_targets` | Integer | Prioritizes targets based on proximity. | 5 |
| `dont_orient_aoe` | Boolean | Prevents the AoE shape from rotating with the character. | 5 |
| `hint_can_target_pickups` | Boolean | UI hint that the player can target items on the ground. | 5 |
| `max_bounces` | Integer | Hard cap on how many times a bouncing effect can trigger. | 5 |
| `splash_damage_aoe_begin` | Integer | At what radius splash damage starts applying. | 5 |
| [`aoe_chance`](./Math_Equations.md) | Equation | Percentage chance for the AoE to trigger. (Must be float values) | 4 |
| `as_the_crow_flies` | Boolean | Calculates range ignoring all pathing terrain obstacles. | 4 |
| `force_ai_target_as_spell` | Boolean | Forces the AI to treat a physical move like a spell for targeting logic. | 4 |
| [`mouse_offset`](./Arrays.md#array-mouse_offset) | Array | Visual offset for the targeting cursor. | 4 |
| `range_display_include_aoe` | Boolean | Visual: shows the full AoE potential when previewing range. | 4 |
| `shotgun_mode` | Boolean | Deals more damage/hits if targets are closer. | 4 |
| `shuffle_tile_order` | Boolean | Randomizes the execution order of AoE tiles. | 4 |
| `upgrade_straight_shot_to_boomerang` | Boolean | Makes the projectile return to caster. | 4 |
| `dont_orient` | Boolean | Prevents the character from turning to face the target. | 3 |
| `low_health_character_threshold` | Enum | AI targeting threshold for seeking weak targets. | 3 |
| `randomize_target_within_range` | Integer | Picks a random valid tile instead of the user's click. | 3 |
| [`special_tile_tag`](./Enums.md#enum-special_tile_tag) | Enum | Targets only tiles with this specific tag. | 3 |
| `track_target` | Boolean | Projectile/Effect follows moving targets. | 3 |
| `corpse_priority` | Integer | AI preference for targeting dead bodies. | 2 |
| `hint_can_target_empty` | Boolean | UI hint that the player can click an empty tile. | 2 |
| `low_gravity_boostable` | Boolean | Can be affected by low gravity wind/effects. | 2 |
| `prioritize_change_direction` | Boolean | AI preference to attack from different angles. | 2 |
| [`range_bonuses`](./Enums.md#enum-range_bonuses) | Enum | How much extra range is added by stats/passives. | 2 |
| `range_display_include_direction` | Boolean | Visual: shows directional arrows. | 2 |
| `recalc_target_on_castpoint` | Boolean | Re-checks if target is valid at the exact frame of cast. | 2 |
| `redirect_location_if_blocked` | Boolean | Shifts target to adjacent tile if original is invalid. | 2 |
| [`target_requires_element`](./Arrays.md#array-target_requires_element) | Array | Target must be afflicted with this element. | 2 |
| `trample_allies_too` | Boolean | Trample movement damages allies in the path. | 2 |
| [`adjust_target`](./Enums.md#enum-adjust_target) | Enum | Tweaks target selection post-cast. | 1 |
| `allow_diagonal_passthrough` | Boolean | Permits diagonal targeting through tight corners. | 1 |
| `ally_priority` | Integer | AI preference for targeting allies. | 1 |
| `aoe_display_exclude_restrictions` | Boolean | Visual only: Hides invalid tiles from the AoE preview. | 1 |
| `aoe_rotate_around_character_center` | Boolean | Anchors the AoE rotation to the character rather than the tile. | 1 |
| `aoe_spell_on_land` | Boolean | Visual trigger when a jump lands. | 1 |
| `bonus_pathing_leniency` | Integer | Gives the AI leeway when calculating complex paths. | 1 |
| [`custom_aoe_mirror`](./Arrays.md#array-custom_aoe_mirror) | Array | How the custom shape mirrors when facing left vs right. | 1 |
| [`custom_aoe_util_mirror`](./Arrays.md#array-custom_aoe_util_mirror) | Array |  | 1 |
| `damage_collided_only` | Boolean | Only damages the first entity the projectile/dash hits. | 1 |
| `enemy_priority` | Integer | AI preference for targeting enemies. | 1 |
| `force_no_contact` | Boolean | Bypasses all contact-based retaliation (Thorns, etc). | 1 |
| `hint_can_target_static` | Boolean | UI hint that the player can target inanimate objects. | 1 |
| [`knockback_modifier`](./Enums.md#enum-knockback_modifier) | Enum | Multiplier for the knockback physics force. | 1 |
| `lingering` | Boolean | Target zone remains active across multiple turns. | 1 |
| `mirror_custom_aoe` | Boolean | Flips the custom AoE array. | 1 |
| [`prioritize_throw_target_with_passive`](./Enums.md#enum-prioritize_throw_target_with_passive) | Enum | AI prefers throwing targets that have specific passives. | 1 |
| `randomize_knockback_direction_except_for_finisher` | Boolean | Chaotic knockback unless it kills the target. | 1 |
| `range_excludes_self` | Boolean | Cannot click on the caster's tile. | 1 |
| `range_max` | Integer | Alternate syntax for `max_range`/`min_range`. | 1 |
| `range_min` | Integer | Alternate syntax for `max_range`/`min_range`. | 1 |
| [`range_symmetry`](./Enums.md#enum-range_symmetry) | Enum | Mirrors the range grid. | 1 |
| `remain_off_map` | Boolean | Keeps entity removed from the grid. | 1 |
| [`restructions`](./Enums.md#enum-restructions) | Enum | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). | 1 |
| `reverse_target_direction` | Boolean | Inverts the targeting vector. | 1 |
| `spin_steps` | Integer | Number of rotational increments for spin targeting. | 1 |
| `uncounterable` | Boolean | Bypasses counter-attack passives. | 1 |

</details>

---

### Context: `cost`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1851

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `mana` | Integer | MP pool and how much it restores per turn. | 1603 |
| `infcantrip` | Boolean | Can be cast infinitely as long as costs are met. | 810 |
| `cantrip` | Boolean | Does not end the turn when cast. | 560 |
| `once_per_fight` | Boolean | Exhausts for the remainder of combat after one use. | 98 |
| `act_points` | Integer | Consumes primary action points (default 1). | 86 |
| `move_points` | Integer | Consumes movement points. | 59 |
| `prime` | Integer | Requires a "priming" turn before it fires. | 30 |
| `allow_offmap_casts` | Boolean | Can be used while the character is hidden/removed from grid. | 22 |
| `cant_cast` | Enum | Explicitly disables casting (used for passive-triggered only abilities). | 18 |
| `must_be_consuming` | Boolean | Requires the character to be eating/holding something. | 17 |
| `charge` | Integer | Cooldown timers measured in turns. | 16 |
| `must_not_be_consuming` | Boolean | Cannot be holding/eating an entity. | 14 |
| `requires_reload` | Boolean | Must spend an action to reload before casting again. | 14 |
| `can_cast_while_dead` | Boolean | Usable by corpses (e.g., DeathRattle triggers). | 12 |
| [`cantrip_group`](./Enums.md#enum-cantrip_group) | Enum | Groups cantrips so using one exhausts the others. | 12 |
| `must_be_offmap` | Boolean | Requires the character to be hidden/dug underground. | 12 |
| `X_cant_be_zero` | Boolean | Applies or references the 'X_cant_be_zero' effect/state. | 11 |
| `disallow_cost_modification` | Boolean | Prevents passives from making this cheaper. | 9 |
| `coins` | Integer | Consumes currency to cast. | 8 |
| `durability` | Integer | Consumes item durability. | 8 |
| `main_turn_only` | Boolean | Cannot be cast during bonus or dispersed turns. | 8 |
| `requires_destructible_weapon` | Boolean | The equipped weapon must be breakable. | 8 |
| `requires_exact_character_aux` | Integer | Hardcoded character specific lock. | 8 |
| `must_not_be_a_summon` | Boolean | Summons/Familiars cannot cast this. | 7 |
| `start_reloaded` | Boolean | Spawns with the ability pre-loaded. | 7 |
| `must_be_first_action` | Boolean | Can only be used at the very start of the turn. | 4 |
| [`enabled_formula`](./Math_Equations.md) | Integer | Mathematical string required to be >0 to cast. | 3 |
| `must_be_first_nonmove_action` | Boolean | Can move first, but cannot use other abilities first. | 3 |
| `must_have_weapon` | Boolean | Requires a weapon equipped in the item slot. | 2 |
| `can_be_refreshed` | Boolean | Passives/Effects can reset this ability's cooldown. | 1 |
| `can_pay_over_multiple_turns` | Boolean | Allows channeling costs over time. | 1 |
| `can_self_refresh` | Boolean | The ability has mechanics to reset its own cooldown. | 1 |
| `damage_cant_be_zero` | Boolean | Requires the ability to have >0 calculated damage to cast. | 1 |
| `initial_charge` | Integer | How many turns it starts on cooldown at battle start. | 1 |
| `manacost_cant_be_zero` | Boolean | Fails to cast if mana cost is reduced to 0. | 1 |
| `minimum_con` | Integer | Stat thresholds required to cast. | 1 |
| `minimum_spd` | Integer | Stat thresholds required to cast. | 1 |
| `require_default_size` | Boolean | 2x2 or altered characters cannot cast this. | 1 |
| `requires_attack_damage_threshold` | Integer | Needs a certain amount of innate damage. | 1 |
| `requires_consumed_trinket` | Boolean | Must have eaten a specific item type. | 1 |
| `requires_empty_trinket` | Boolean | Must not have an accessory equipped. | 1 |
| `requires_hp_threshold` | Integer | Must be below/above a certain health percentage. | 1 |
| `requires_weapon` | Boolean | Prerequisite: Must meet this condition. | 1 |

</details>

---

### Context: `self_damage`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 220

> **Referenced by:** [`NukeQuestFinalBossModifications`](#context-nukequestfinalbossmodifications), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damage Blocks}`](./Engine_Damage.md#all-confirmed-damage-instance-values) | Block | A damage hit definition. See Engine_Damage.md for the full schema. |  |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 200 |
| `damage` | Equation | The base damage properties of an attack. | 47 |
| `piercing` | Boolean |  | 12 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 11 |
| `cant_miss` | Boolean |  | 10 |
| `knockback` | Integer |  | 10 |
| `heal` | Integer |  | 6 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 4 |
| `ai_base_score` | Integer |  | 2 |
| `non_lethal` | Boolean |  | 1 |

</details>

---

### Context: `spawn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 192

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 184 |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 59 |
| `ai_base_score` | Integer |  | 31 |
| [`additional_passives`](#context-additional_passives) | Block | Passives granted intrinsically to a spawned entity. | 20 |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum |  | 17 |
| [`layer`](./Enums.md#enum-layer) | Enum |  | 14 |
| [`catdata`](./Enums.md#enum-catdata) | Enum | Defines genetic/clone data cloning. | 13 |
| `clone_items` | Boolean | If true, transfers inventory to the clone. | 12 |
| `lob` | Boolean |  | 4 |
| [`post_spawn_statuses`](#context-post_spawn_statuses) | Block | Status effects applied immediately after an entity spawns. | 4 |
| `size` | Integer |  | 4 |
| `face_camera` | Boolean |  | 2 |
| `inherit_elite_buffs` | Boolean |  | 2 |
| `start_dead` | Boolean |  | 2 |
| [`appearance`](./Enums.md#enum-appearance) | Enum |  | 1 |
| [`auto_cast_on_spawn`](./Enums.md#enum-auto_cast_on_spawn) | Enum |  | 1 |
| [`chapter`](./Enums.md#enum-chapter) | Enum |  | 1 |
| [`custom_additional_ai_weight`](./Enums.md#enum-custom_additional_ai_weight) | Enum |  | 1 |
| `include_passives` | Boolean |  | 1 |
| `redirect_location_if_blocked` | Boolean |  | 1 |
| [`spawnin_animation`](./Enums.md#enum-spawnin_animation) | Enum |  | 1 |
| `trigger_battle_start` | Boolean |  | 1 |

</details>

---

### Context: `bonus_passives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 136

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`AddStatusToBasicAttack`](#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 1 |
| [`RevengeDamage`](#context-revengedamage) | Block | Reaction trigger: Deals damage to the attacker when hit. | 1 |
| [`StatusKillers`](#context-statuskillers) | Block | Instantly kills the target if they possess the specified status effects. | 1 |

</details>

---

### Context: `temporary_effects`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 88

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Trample` | Integer | Applies or references the 'Trample' effect/state. | 26 |
| `CastAgain` | Integer | Applies or references the 'CastAgain' effect/state. | 20 |
| `DisableTrample` | Integer | Applies or references the 'DisableTrample' effect/state. | 10 |
| `Fury` | Integer | Applies or references the 'Fury' effect/state. | 7 |
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum | Applies or references the 'TileTrail' effect/state. | 6 |
| `JustInCaseTrample` | Integer | Applies or references the 'JustInCaseTrample' effect/state. | 5 |
| [`LeaveBehind`](./Enums.md#enum-leavebehind) | Enum | Spawns a specific object at the character's previous location when they move. | 5 |
| `DashFury` | Integer | Applies or references the 'DashFury' effect/state. | 3 |
| [`AfterImage`](#context-afterimage) | Block | Spawns a visual decoy or shade at the caster's previous location. | 2 |
| `BearTrapTrail` | Integer | Applies or references the 'BearTrapTrail' effect/state. | 2 |
| `DelayedWindTrail` | Integer | Applies or references the 'DelayedWindTrail' effect/state. | 1 |
| `DoubleLoot` | Integer | Applies or references the 'DoubleLoot' effect/state. | 1 |
| [`JumpAttackLeaveBehind`](./Enums.md#enum-jumpattackleavebehind) | Enum | Applies or references the 'JumpAttackLeaveBehind' effect/state. | 1 |
| `KnockbackImmunity` | Integer | Applies or references the 'KnockbackImmunity' effect/state. | 1 |
| [`TileTrail_Ahead`](./Enums.md#enum-tiletrail_ahead) | Enum | Applies or references the 'TileTrail_Ahead' effect/state. | 1 |

</details>

---

### Context: `Else`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 71

> **Referenced by:** [`Conditional_Boss`](#context-conditional_boss), [`Conditional_Buddy`](#context-conditional_buddy), [`Conditional_HasTag`](#context-conditional_hastag), [`Conditional_Object`](#context-conditional_object), [`Conditional_Speculative`](#context-conditional_speculative), [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 |
| [`ApplyToRandomPartyMemberIfPossible`](#context-applytorandompartymemberifpossible) | Block | Redirects the nested effects to apply to a random living member of the player's party. | 1 |
| [`Consumed`](#context-consumed) | Block | State block triggered when this object or entity is eaten/consumed by another character. | 1 |
| [`Else`](#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 51

> **Referenced by:** [`ApplyStatusIfCrit`](#context-applystatusifcrit), [`CanApplyToInanimate`](#context-canapplytoinanimate), [`Conditional_Ally`](#context-conditional_ally), [`Conditional_Enemy`](#context-conditional_enemy), [`Conditional_GoodRoll`](#context-conditional_goodroll), [`Conditional_HasStatus`](#context-conditional_hasstatus), [`Conditional_HasTag`](#context-conditional_hastag), [`Conditional_HealthThreshold`](#context-conditional_healththreshold), [`Conditional_LivingPlayerCat`](#context-conditional_livingplayercat), [`Conditional_PlayerCat`](#context-conditional_playercat), [`Conditional_SourceAbilityHasTag`](#context-conditional_sourceabilityhastag), [`Else`](#context-else), [`Math`](#context-math), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 42

> **Referenced by:** [`Conditional_Object`](#context-conditional_object), [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. | 41 |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 |
| [`ApplyToSourceOnKill`](#context-applytosourceonkill) | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 2 |
| [`Else`](#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 2 |

</details>

---

### Context: `Temporary`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 41

> **Referenced by:** [`CanApplyToInanimate`](#context-canapplytoinanimate), [`Conditional_Ally`](#context-conditional_ally), [`Conditional_Enemy`](#context-conditional_enemy), [`Conditional_NotAlly`](#context-conditional_notally), [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Integer | Number of stacks or intensity to apply. | 41 |
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 40 |
| `turns` | Integer | Duration in turns. | 40 |
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 19 |
| `expires_on_end_turn` | Boolean |  | 11 |
| `data` | Integer |  | 2 |
| `expires_on_appliers_turn` | Boolean |  | 2 |
| `expires_on_move` | Boolean |  | 1 |

</details>

---

### Context: `sounds`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 39

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ontrigger`](./Enums.md#enum-ontrigger) | Enum |  | 32 |
| [`oncast`](./Enums.md#enum-oncast) | Enum |  | 3 |
| [`oncastpoint`](./Enums.md#enum-oncastpoint) | Enum |  | 3 |
| [`ontrigger_intentional`](./Enums.md#enum-ontrigger_intentional) | Enum |  | 1 |

</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 36

> **Referenced by:** [`Conditional_Corpse`](#context-conditional_corpse), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`ApplyToSourceOnKill`](#context-applytosourceonkill) | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 1 |
| [`Conditional_FinishedSpawning`](#context-conditional_finishedspawning) | Block | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. | 1 |

</details>

---

### Context: `splash_damage`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 35

> **Referenced by:** [`NukeQuestFinalBossModifications`](#context-nukequestfinalbossmodifications), [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damage Blocks}`](./Engine_Damage.md#all-confirmed-damage-instance-values) | Block | A damage hit definition. See Engine_Damage.md for the full schema. |  |
| `damage` | Integer | The base damage properties of an attack. | 32 |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 17 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 13 |
| `knockback` | Integer | Knockback force of the splash blast. | 13 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 12 |
| `makes_contact` | Boolean |  | 6 |
| `override_trample_damage` | Boolean |  | 2 |
| `ai_base_score` | Integer |  | 1 |
| `crit_chance` | Float |  | 1 |
| `force_no_knockback` | Boolean |  | 1 |
| `force_play_hit_animation` | Boolean |  | 1 |
| [`layer`](./Enums.md#enum-layer) | Enum |  | 1 |

</details>

---

### Context: `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 25

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`ApplyToSourceOnKill`](#context-applytosourceonkill) | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 1 |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 23

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`[keyword_id]`](./Engine_Statuses.md#all-confirmed-keyword_id-values) | String | A Status or Keyword ID whose tooltip text is defined here. See Engine_Statuses.md for all IDs. |  |
</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 21

> **Referenced by:** [`ApplyToSource`](#context-applytosource), [`Conditional_LastHit`](#context-conditional_lasthit), [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Integer | The distance in tiles to knock the target away. | 20 |
| [`stacks`](./Math_Equations.md) | Integer | Number of stacks or intensity to apply. | 18 |
| `height` | Integer |  | 2 |
| `circular_variance` | Integer |  | 1 |

</details>

---

### Context: `additional_passives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 20

> **Referenced by:** [`spawn`](#context-spawn)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 19

> **Referenced by:** [`ApplyMultipleTimes`](#context-applymultipletimes), [`Conditional_CanBeHealed`](#context-conditional_canbehealed), [`Conditional_HasCleansableDebuffs`](#context-conditional_hascleansabledebuffs), [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Consumed`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 18

> **Referenced by:** [`Conditional_Buddy`](#context-conditional_buddy), [`Conditional_LivingPlayerCat`](#context-conditional_livingplayercat), [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Ability triggered by the consumed entity while inside the consumer. | 13 |
| `force_contact` | Boolean | If true, enforces physical overlap. | 11 |
| `instant` | Boolean |  | 8 |
| [`mount_mode`](./Enums.md#enum-mount_mode) | Boolean | If true, treats the consumption as riding/mounting instead of eating. | 8 |
| `wet` | Boolean |  | 8 |
| `do_not_pop_corpse` | Boolean |  | 7 |
| `drop_on_death` | Boolean |  | 7 |
| `drop_on_self_death` | Boolean |  | 3 |
| [`extra_statuses`](#context-extra_statuses) | Block | Additional generic status applications. | 3 |
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum |  | 1 |
| `kill_on_consume` | Boolean |  | 1 |
| `use_placeholder` | Boolean |  | 1 |

</details>

---

### Context: `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 17

> **Referenced by:** [`Conditional_HasTag`](#context-conditional_hastag), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Else`](#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 4 |

</details>

---

### Context: `ApplyToSourceOnKill`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 15

> **Referenced by:** [`Conditional_Ally`](#context-conditional_ally), [`Conditional_Enemy`](#context-conditional_enemy), [`Conditional_HasTag`](#context-conditional_hastag), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `CanApplyToInanimate`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 15

> **Referenced by:** [`Conditional_HasTag`](#context-conditional_hastag), [`Conditional_NotBoss`](#context-conditional_notboss), [`Conditional_Object`](#context-conditional_object), [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum | Spawns a specific character or entity upon impact. | 10 |
| [`BreakIntoRocks`](./Enums.md#enum-breakintorocks) | Enum | Applies or references the 'BreakIntoRocks' effect/state. | 4 |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 |
| `Vaporize` | Integer | Applies or references the 'Vaporize' effect/state. | 3 |
| `GetAggroTarget` | Integer | Applies or references the 'GetAggroTarget' effect/state. | 2 |
| `PreventDeathTransforms` | Integer | Applies or references the 'PreventDeathTransforms' effect/state. | 1 |
| [`Temporary`](#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 1 |

</details>

---

### Context: `CatPartsTransform`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 14

> **Referenced by:** [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ear1` | Integer | Sprite variant ID for the front ear. | 10 |
| `tail` | Integer | Sprite variant ID for the tail. | 10 |
| `ear2` | Integer |  | 9 |
| `arm2` | Float |  | 8 |
| `mouth` | Float |  | 8 |
| `arm1` | Float | Sprite variant ID for the front arm. | 7 |
| `leg1` | Integer | Sprite variant ID for the front leg. | 5 |
| `leg2` | Integer |  | 5 |
| `head` | Float | Sprite variant ID for the head. | 3 |
| `texture` | Integer |  | 3 |
| `body` | Float | Sprite variant ID for the body. | 2 |
| `eye1` | Integer |  | 1 |
| `eye2` | Integer |  | 1 |
| `eyebrow1` | Integer |  | 1 |
| `eyebrow2` | Integer |  | 1 |
| `palette` | Integer |  | 1 |

</details>

---

### Context: `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 14

> **Referenced by:** [`Conditional_Enemy`](#context-conditional_enemy), [`Conditional_HasTag`](#context-conditional_hastag), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `FormChange`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 14

> **Referenced by:** [`Else`](#context-else), [`RandomStatusFromPool`](#context-randomstatusfrompool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form`](./Strings.md#string-form) | String |  | 75 |
| `chance` | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Context: `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 13

> **Referenced by:** [`Conditional_Boss`](#context-conditional_boss), [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 13 |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |

</details>

---

### Context: `EvolveAbilityFromPool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 13

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 13 |
| `upgraded` | Boolean |  | 13 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `odds` | Float | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 12 |
| [`ApplyToRandomPartyMemberIfPossible`](#context-applytorandompartymemberifpossible) | Block | Redirects the nested effects to apply to a random living member of the player's party. | 1 |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |

</details>

---

### Context: `Conditional_Speculative`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`Conditional_AffectedByElement`](#context-conditional_affectedbyelement), [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Else`](#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |

</details>

---

### Context: `DoScreenShake`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`TimeDelayStatusApplication`](#context-timedelaystatusapplication), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `intensity` | Integer |  | 10 |
| `time` | Float |  | 10 |

</details>

---

### Context: `ChanceToBreakFree`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 11

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ability triggered upon successfully breaking free. | 11 |
| [`fail_ability`](./Enums.md#enum-fail_ability) | Enum | The ability triggered if the break free attempt fails. | 3 |
| `stacks` | Integer | Percentage base chance to break free. | 3 |

</details>

---

### Context: `ChangeTile`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 11

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tile`](./Enums.md#enum-tile) | Enum | The specific tile type to change into (e.g., GlassTile). | 11 |
| [`chance`](./Math_Equations.md) | Equation | Probability (0.0 to 1.0 or percentage) of this occurring. (Must be float values) | 2 |
| `aoe` | Integer |  | 1 |

</details>

---

### Context: `ApplyPassives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 10

> **Referenced by:** [`Conditional_RandomChance`](#context-conditional_randomchance), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`StatusOnBattleEnd`](#context-statusonbattleend) | Block | Applies the nested status effects when the encounter finishes. | 3 |

</details>

---

### Context: `Conditional_FormulaIsPositive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 10

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`formula`](./Math_Equations.md) | Enum | The math expression to evaluate. | 8 |

</details>

---

### Context: `Craft`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

> **Referenced by:** [`ApplyToSource`](#context-applytosource), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 9 |
| [`slot`](./Enums.md#enum-slot) | Enum |  | 8 |
| `temporary` | Boolean |  | 4 |
| `works_with_tech` | Boolean |  | 1 |

</details>

---

### Context: `ApplyStatusIfCrit`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 6 |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`Conditional_Ally`](#context-conditional_ally), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_InForm`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`Conditional_Buddy`](#context-conditional_buddy), [`Conditional_HasTag`](#context-conditional_hastag), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`form`](./Enums.md#enum-form) | Enum | The specific form ID to check for. | 7 |

</details>

---

### Context: `Conditional_HealthThreshold`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`Conditional_NotBoss`](#context-conditional_notboss), [`Conditional_Speculative`](#context-conditional_speculative), [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `threshold_flat` | Integer | A flat numerical health value threshold. | 4 |
| `threshold_percent` | Integer | A percentage-based health threshold (e.g. 50%). | 2 |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`threshold_expr`](./Math_Equations.md) | Enum |  | 1 |

</details>

---

### Context: `Conditional_Object`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Else`](#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 3 |

</details>

---

### Context: `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`Conditional_Ally`](#context-conditional_ally), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |

</details>

---

### Context: `DoDistortionRing`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `intensity` | Integer |  | 6 |
| `radius` | Integer | Distance or area of effect in tiles. | 6 |
| `speed` | Float |  | 6 |

</details>

---

### Context: `SwitchMusic`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`TimeDelayStatusApplication`](#context-timedelaystatusapplication), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | The specific audio layer to transition to (e.g., map, battle). | 6 |
| [`new_song`](./Enums.md#enum-new_song) | Enum | The ID of the new music track. | 5 |
| `crossfade_speed` | Integer |  | 1 |

</details>

---

### Context: `TwisterDisplaceWithDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer | The damage formula or inherit flag. | 6 |
| `max_dist` | Integer | Maximum displacement distance. | 6 |
| `min_dist` | Integer | Minimum displacement distance. | 2 |
| [`exclude_prefix`](./Enums.md#enum-exclude_prefix) | Enum |  | 1 |

</details>

---

### Context: `CollectsPickupsWithAltEffects`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Tech` | Integer | Applies or references the 'Tech' effect/state. | 2 |
| `CurrentWeaponAddPoison` | Integer | Applies or references the 'CurrentWeaponAddPoison' effect/state. | 1 |
| `LuckUp` | Integer | Applies or references the 'LuckUp' effect/state. | 1 |
| `Quivered` | Integer | Applies or references the 'Quivered' effect/state. | 1 |
| `RandomStatUp` | Integer | Applies or references the 'RandomStatUp' effect/state. | 1 |
| `Shield` | Integer | Applies or references the 'Shield' effect/state. | 1 |

</details>

---

### Context: `DestroyEquipmentAndAttachParasite`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`Conditional_ActiveWeather_Any`](#context-conditional_activeweather_any), [`Conditional_DebuffRoll`](#context-conditional_debuffroll), [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Enum | The item pool to draw the parasite from. | 5 |
| `chance` | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 3 |

</details>

---

### Context: `DoDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`ApplyToSource`](#context-applytosource), [`Else`](#context-else), [`post_spawn_statuses`](#context-post_spawn_statuses)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer | The flat damage amount. | 5 |
| [`type`](./Enums.md#enum-type) | Enum | The classification of the damage (e.g., spell, melee). | 5 |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum |  | 2 |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |

</details>

---

### Context: `ApplyToConsumed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| `DeleteObject` | Integer | Applies or references the 'DeleteObject' effect/state. | 3 |
| `Die` | Integer | Applies or references the 'Die' effect/state. | 1 |

</details>

---

### Context: `ArcLightning`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, the arc will not bounce to friendly targets. | 4 |
| `max_distance` | Integer | The maximum tile range the lightning can jump between bounces. | 4 |
| `stacks` | Integer | The maximum number of targets the lightning can bounce to. | 4 |
| [`chance`](./Math_Equations.md) | Equation | Probability (0.0 to 1.0 or percentage) of this occurring. (Must be float values) | 1 |
| `ignore_self` | Boolean | If true, prevents the arc from bouncing back to the caster. | 1 |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific dodge ability to trigger (e.g., DestroyerDodge). | 4 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 4 |

</details>

---

### Context: `Conditional_Familiar`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `GainCoinsRange`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`ApplyToSource`](#context-applytosource), [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Integer | Maximum coins granted. | 4 |
| `min` | Integer | Minimum coins granted. | 4 |

</details>

---

### Context: `LateStatusApplication`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `CurrentWeaponDamageUp` | Integer | Applies or references the 'CurrentWeaponDamageUp' effect/state. | 3 |
| `AddWeaponAux` | Integer | Applies or references the 'AddWeaponAux' effect/state. | 1 |

</details>

---

### Context: `LeaveBehind`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID to spawn. | 4 |

</details>

---

### Context: `ReplaceSpell`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`TempPassiveWhileHasStatus`](#context-temppassivewhilehasstatus)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The new ability ID to insert. | 4 |
| `slot` | Integer | The spell slot index to replace. | 4 |

</details>

---

### Context: `TakeBonusTurnWithStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `TempPassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`Conditional_FirstApplicationThisTurn`](#context-conditional_firstapplicationthisturn), [`Conditional_LivingPlayerCat`](#context-conditional_livingplayercat)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ReplaceSpell`](#context-replacespell) | Block | Replaces a spell in the character's hand/deck with a different one. | 4 |
| [`status`](./Enums.md#enum-status) | Enum | The required status effect. | 3 |
| [`MeleeRevengeDamage`](#context-meleerevengedamage) | Block | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. | 2 |
| `AddManaRegen` | Integer | Applies or references the 'AddManaRegen' effect/state. | 1 |
| `HealthRegenUp` | Integer | Applies or references the 'HealthRegenUp' effect/state. | 1 |

</details>

---

### Context: `TimeDelayStatusApplication`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `delay` | Float | The float time delay in seconds. | 4 |
| [`SwitchMusic`](#context-switchmusic) | Block | Changes the background music track or layer during combat. | 2 |
| `Cleanse` | Integer | Applies or references the 'Cleanse' effect/state. | 1 |
| [`CreateGlobalModifiers`](#context-createglobalmodifiers) | Block | Generates global map or encounter rules/modifiers. | 1 |
| [`DoScreenShake`](#context-doscreenshake) | Block | Triggers a camera screen shake effect. | 1 |
| [`FormChange`](./Enums.md#enum-formchange) | Enum | Transforms the character into a different state or form (e.g., Rage, HasCat). | 1 |
| `FullHeal` | Integer | Applies or references the 'FullHeal' effect/state. | 1 |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | Applies or references the 'GlobalSpawnCharacter' effect/state. | 1 |
| `PlayBackground` | Integer | Applies or references the 'PlayBackground' effect/state. | 1 |
| `RemoveAmbientLightEffects` | Float | Applies or references the 'RemoveAmbientLightEffects' effect/state. | 1 |
| `Vaporize` | Integer | Applies or references the 'Vaporize' effect/state. | 1 |

</details>

---

### Context: `post_spawn_statuses`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`spawn`](#context-spawn)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`DoDamage`](#context-dodamage) | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 2 |
| [`EnterMount`](./Enums.md#enum-entermount) | Enum | Applies or references the 'EnterMount' effect/state. | 1 |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum | Applies or references the 'VisualFXTile' effect/state. | 1 |

</details>

---

### Context: `rocket_swirl`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`graphics`](#context-graphics)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`radius`](./Arrays.md#array-radius) | Array | Swirl radius. | 4 |
| [`speed`](./Arrays.md#array-speed) | Array | Rotations per second. | 4 |

</details>

---

### Context: `ApplyMultipleTimes`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 3 |
| [`stacks`](./Math_Equations.md) | Enum | The number of times the nested effects block should be repeatedly executed. | 3 |

</details>

---

### Context: `BounceObject`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`obj`](./Enums.md#enum-obj) | Enum | The entity ID of the object to spawn (e.g., chapter_corpse_medium). | 3 |
| [`chance`](./Math_Equations.md) | Equation | Probability (0.0 to 1.0) of spawning the object. (Must be float values) | 2 |
| `slide` | Integer |  | 1 |

</details>

---

### Context: `CatPartsSizeScaleStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `arm1` | Float | Scale multiplier for the front arm. | 1 |
| `arm2` | Float | Scale multiplier for the back arm. | 1 |
| `body` | Float |  | 1 |
| `mouth` | Float |  | 1 |

</details>

---

### Context: `Conditional_AffectedByElement`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type to check for. | 3 |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. | 3 |

</details>

---

### Context: `Conditional_LastHit`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `DustOnHit`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The ID of the object/particle to spawn. | 3 |

</details>

---

### Context: `IncAuxCounterClamped`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`RandomStatusFromPool`](#context-randomstatusfrompool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `change` | Integer |  | 3 |
| `max` | Integer |  | 3 |

</details>

---

### Context: `SetCrazyEyeBackgroundWeights`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Arrays.md#array-weights) | Array |  | 3 |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`ApplyPassives`](#context-applypassives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 3 |

</details>

---

### Context: `extra_statuses`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`Consumed`](#context-consumed)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>
 | `Burn` | Number | Applies or references the 'Burn' effect/state. | 1 | 
 | `Poison` | Number | Applies or references the 'Poison' effect/state. | 1 | 
 | `Tarred` | Number | Applies or references the 'Tarred' effect/state. | 1 | 

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`PassiveWhileNotTakingTurn`](#context-passivewhilenottakingturn), [`bonus_passives`](#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `AfterImage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`temporary_effects`](#context-temporary_effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the visual decoy to spawn (e.g., PlayerCat_ThiefShade). | 2 |
| `skilltemp` | Boolean | If true, the decoy is automatically destroyed once the skill finishes executing. | 2 |

</details>

---

### Context: `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`Conditional_GoodRoll`](#context-conditional_goodroll), [`Else`](#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `ApplyToTile`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`Conditional_DestructibleCorpse`](#context-conditional_destructiblecorpse)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`ObjectOnHit`](./Enums.md#enum-objectonhit) | Enum | Spawns a specific physics/item object upon impact. | 2 |
| `SpawnBearTrap` | Integer | Applies or references the 'SpawnBearTrap' effect/state. | 2 |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`bonus_passives`](#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 2 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 1 |

</details>

---

### Context: `BodyGuard`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to use when intercepting (e.g., BodyGuardSwap). | 2 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`odds`](./Math_Equations.md) | Equation | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. (Must be float values) | 2 |

</details>

---

### Context: `Conditional_BossOrBig`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_Buddy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`Consumed`](#context-consumed) | Block | State block triggered when this object or entity is eaten/consumed by another character. | 1 |
| [`Else`](#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |

</details>

---

### Context: `Conditional_DestructibleCorpse`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
</details>

---

### Context: `Conditional_Displaceable`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`Else`](#context-else), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_IsSelf`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
</details>

---

### Context: `Conditional_NotAlly`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_NotBossOrBig`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_NotShielded`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`key`](./Enums.md#enum-key) | Enum |  | 2 |

</details>

---

### Context: `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `ConjureBonusAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to conjure. | 2 |
| `upgraded` | Boolean | If true, conjures the upgraded version of the ability. | 2 |

</details>

---

### Context: `CreateGlobalModifiers`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`TimeDelayStatusApplication`](#context-timedelaystatusapplication), [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Global Modifiers}`](./Engine_GlobalModifiers.md#all-confirmed-global-modifier-id-values) | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |  |
</details>

---

### Context: `FindItemFromPool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ApplyToSource`](#context-applytosource)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Math_Equations.md) | Equation | Probability of finding the item. (Must be float values) | 2 |
| [`pool`](./Enums.md#enum-pool) | Enum | The item pool to draw from. | 1 |

</details>

---

### Context: `ForceAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `immediate` | Boolean |  | 2 |

</details>

---

### Context: `ForceMoveTowardsTaggedObject`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The movement ability to use. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | The entity tag to seek out. | 1 |

</details>

---

### Context: `LowerAmbientLight`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`CreateGlobalModifiers`](#context-createglobalmodifiers)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array | The target opacity/dimness level. | 2 |
| `speed` | Float | The transition speed. | 2 |

</details>

---

### Context: `Math`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Stun` | Integer | Applies or references the 'Stun' effect/state. | 2 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 2 |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`TempPassiveWhileHasStatus`](#context-temppassivewhilehasstatus)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |

</details>

---

### Context: `NukeQuestFinalBossModifications`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`bonus_passives`](#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`self_damage`](#context-self_damage) | Block | Recoil or self-inflicted damage/effects applied to the caster. | 2 |
| [`damage_instance`](#context-damage_instance) | Block |  | 1 |
| [`splash_damage`](#context-splash_damage) | Block | Secondary Area of Effect blast parameters. | 1 |

</details>

---

### Context: `ObjectOnHit`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the object to spawn (e.g., Poop). | 2 |

</details>

---

### Context: `ObjectOnHitCharacter`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Float | Probability (0.0 to 1.0) of spawning. | 2 |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the character to spawn (e.g., CharmedFlea). | 2 |

</details>

---

### Context: `OverHealToStatuses`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `RandomStatUp` | Integer | Applies or references the 'RandomStatUp' effect/state. | 1 |
| `TakeExtraTurn` | Integer | Applies or references the 'TakeExtraTurn' effect/state. | 1 |
| `stack_scale` | Integer |  | 1 |

</details>

---

### Context: `QuakeAreaChance`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Float | Probability of triggering the quake. | 2 |
| `radius` | Integer | The tile radius of the quake. | 2 |

</details>

---

### Context: `RandomKnockback`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Integer | Maximum knockback distance. | 2 |
| `min` | Integer | Minimum knockback distance. | 2 |

</details>

---

### Context: `RandomMagicMissile`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `full_size` | Boolean | If true, fires normal sized missiles instead of mini ones. | 2 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `ScatterCoins`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`Conditional_SourceAbilityHasTag`](#context-conditional_sourceabilityhastag), [`Else`](#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stackable` | Boolean | If true, multiple instances of this trigger can stack. | 2 |
| [`stacks`](./Math_Equations.md) | Enum | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `TakeBonusTurnWithAIControl`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | If true, allows the AI to cast spells during this bonus turn. | 2 |

</details>

---

### Context: `TeamCastAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The underlying logic ability executed by the team. | 2 |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum | Requires participants to share this tag. | 2 |
| `same_orientation` | Boolean |  | 1 |

</details>

---

### Context: `XIsTargetHealth`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`Conditional_Boss`](#context-conditional_boss), [`Else`](#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`BonusDamage`](./Math_Equations.md) | Equation | Applies or references the 'BonusDamage' effect/state. | 2 |

</details>

---

### Context: `empty_self_damage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |

</details>

---

### Context: `AlphaStatusOnTurnBegin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`bonus_passives`](#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `DoubleCastSpellThisTurn` | Integer | Applies or references the 'DoubleCastSpellThisTurn' effect/state. | 1 |

</details>

---

### Context: `ApplyPassivesToSpawnerWhileAlive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`additional_passives`](#context-additional_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum | Applies or references the 'HideEquipment' effect/state. | 1 |

</details>

---

### Context: `ApplyStatusesNextTurnBegin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Quivered` | Integer | Applies or references the 'Quivered' effect/state. | 1 |

</details>

---

### Context: `ApplyToOthersWithSharedTagAndFaction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Marked` | Integer | Applies or references the 'Marked' effect/state. | 1 |

</details>

---

### Context: `ApplyToRandomClosestAlly`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| `ForceMoveTowards` | Integer | Applies or references the 'ForceMoveTowards' effect/state. | 1 |

</details>

---

### Context: `Cleave`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Math_Equations.md) | Equation | Probability (0.0 to 1.0) that the cleave effect triggers. (Must be float values) | 1 |

</details>

---

### Context: `Conditional_ActiveWeather_Any`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. | 1 |

</details>

---

### Context: `Conditional_Backstab`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `Conditional_CanBeHealed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `Conditional_DebuffRoll`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `odds` | Float | The probability (0.0 to 1.0) of applying the debuff. | 1 |

</details>

---

### Context: `Conditional_FinishedSpawning`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`Conditional_Enemy`](#context-conditional_enemy)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`Imprison`](./Enums.md#enum-imprison) | Enum | Applies or references the 'Imprison' effect/state. | 1 |

</details>

---

### Context: `Conditional_HasCleansableDebuffs`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `GenericBuff` | Integer | Applies or references the 'GenericBuff' effect/state. | 1 |
| `PartialCleanse` | Integer | Applies or references the 'PartialCleanse' effect/state. | 1 |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `Conditional_IsTrample`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
</details>

---

### Context: `Conditional_LivingPlayerCat`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`Consumed`](#context-consumed) | Block | State block triggered when this object or entity is eaten/consumed by another character. | 1 |

</details>

---

### Context: `Conditional_NotBig`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
</details>

---

### Context: `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ApplyPassives`](#context-applypassives) | Block | Grants the nested passive abilities dynamically. | 1 |
| `odds` | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Context: `Conditional_SourceAbilityHasTag`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ApplyToSource`](#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 1 |

</details>

---

### Context: `Conditional_SourceHasStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |

</details>

---

### Context: `CopySpells`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |
| `upgraded` | Boolean |  | 1 |

</details>

---

### Context: `DelayCastAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to cast later. | 1 |
| `lingering` | Boolean |  | 1 |
| `relative` | Boolean |  | 1 |

</details>

---

### Context: `DelayedWindCone`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer | The base damage properties of an attack. | 1 |
| `distance` | Integer | Distance or area of effect in tiles. | 1 |

</details>

---

### Context: `DybbukPossessed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`Else`](#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum |  | 1 |
| [`punch_self_ability`](./Enums.md#enum-punch_self_ability) | Enum |  | 1 |

</details>

---

### Context: `ForceImmediateMoveAndAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`Conditional_InForm`](#context-conditional_inform)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ability to execute after moving. | 1 |
| `even_if_cant_reach` | Boolean | If true, executes the attack even if the move fails to reach the target. | 1 |

</details>

---

### Context: `IncAuxCounterCycle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `change` | Integer |  | 1 |
| `max` | Integer |  | 1 |

</details>

---

### Context: `KnockOutCoin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Math_Equations.md) | Equation | Probability (0.0 to 1.0 or percentage) of this occurring. (Must be float values) | 1 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `Madness`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |
| `tickdown_this_turn` | Boolean |  | 1 |

</details>

---

### Context: `MergeDamageInstance`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`Conditional_HasTag`](#context-conditional_hastag)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `can_instapop` | Boolean | If false, prevents the damage from instantly popping the target. | 1 |
| `force_no_hit_animation` | Boolean | If true, suppresses the flinch/hit animation. | 1 |

</details>

---

### Context: `Metronome`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`banned_abilities`](./Arrays.md#array-banned_abilities) | Array |  | 1 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `NextAttackSpecialCrit`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Integer | Flat addition to the critical damage multiplier. | 1 |
| `extra_coins_per_stack` | Integer | Grants bonus coins based on stacks. | 1 |
| `luck_increase` | Integer | Increases luck stat for the attack. | 1 |

</details>

---

### Context: `NextBasicAttackCritsThisTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | If true, ensures the attack cannot be dodged. | 1 |
| `piercing` | Boolean | If true, the attack ignores armor. | 1 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `NextBattleStatusStacks`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| `MadnessChanceOnTurnBegin` | Integer | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. | 1 |
| `fights` | Integer | The number of encounters this buff/debuff persists for. | 1 |

</details>

---

### Context: `PassiveWhileNotTakingTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`bonus_passives`](#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`AddStatusToBasicAttack`](#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 1 |

</details>

---

### Context: `PoolMetronome`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | An array of ability IDs to randomly choose from. | 1 |

</details>

---

### Context: `PopAndSpawn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`Conditional_HasTag`](#context-conditional_hastag)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID to spawn in place. | 2 |
| `clone_items` | Boolean | If true, transfers inventory to the new entity. | 1 |
| `clone_referenced_catdata` | Boolean | If true, copies the genetic data of the popped cat. | 1 |
| `no_splatter` | Boolean |  | 1 |

</details>

---

### Context: `RandomDistanceDisplace`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `min_dist` | Integer | The minimum tile distance they will be moved. | 1 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `RemoveStatusStacks`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Integer | The number of stacks to remove. | 1 |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 1 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`bonus_passives`](#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |

</details>

---

### Context: `ReviveNextRound`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`additional_passives`](#context-additional_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `revive_health` | Integer | The flat amount of health to revive with. | 3 |
| `AllStatsUp` | Integer | Applies or references the 'AllStatsUp' effect/state. | 2 |
| `Shield` | Integer | Applies or references the 'Shield' effect/state. | 2 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 2 |
| `DivineShield` | Integer | Applies or references the 'DivineShield' effect/state. | 1 |

</details>

---

### Context: `ScrambleLastUsedSpell`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `permanent` | Boolean | If true, the scramble persists for the rest of the run. | 1 |

</details>

---

### Context: `SetAnimationAlts`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`Conditional_HasTag`](#context-conditional_hastag)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dead`](./Enums.md#enum-dead) | Enum |  | 1 |
| [`dying`](./Enums.md#enum-dying) | Enum |  | 1 |

</details>

---

### Context: `ShowFakeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`Else`](#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |
| [`style`](./Arrays.md#array-style) | Array | The visual font style for the text (e.g., [crit]). | 1 |

</details>

---

### Context: `SmartMetronome`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |
| `upgraded` | Boolean |  | 1 |

</details>

---

### Context: `SpreadDisease`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Float | Probability (0.0 to 1.0 or percentage) of transmitting. | 1 |
| [`disease`](./Enums.md#enum-disease) | Enum | The specific status effect ID representing the disease. | 1 |

</details>

---

### Context: `StatusGroup`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>

---

### Context: `StatusKillers`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`bonus_passives`](#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
</details>
 | `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 1 | 

---

### Context: `SwapWeapon`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | An array of weapon item IDs to draw from. | 1 |

</details>

---

### Context: `Tangled`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_art`](./Enums.md#enum-alt_art) | Enum | The alternative sprite art to use while tangled. | 1 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `TransformEquipment`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | The original item ID. | 1 |
| [`to`](./Enums.md#enum-to) | Enum | The new item ID. | 1 |

</details>

---

### Context: `TransformWeapon`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ApplyToSourceOnKill`](#context-applytosourceonkill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | The original weapon ID. | 1 |
| [`to`](./Enums.md#enum-to) | Enum | The transformed weapon ID. | 1 |

</details>

---

### Context: `UseAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger. | 1 |
| `respect_prime` | Boolean | If true, respects the ability's prime/cooldown state. | 1 |

</details>

---

### Context: `UseMoveAbilityWithAI`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | The AI positioning logic profile to use. | 1 |

</details>

---

### Context: `VisualCountDownThenApplyStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | Applies or references the 'ForceUseAbility' effect/state. | 1 |

</details>

---

### Context: `WaggleClone`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`effects`](#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`1x1_object`](./Enums.md#enum-1x1_object) | Enum | The 1x1 variant of the object. | 1 |
| [`2x2_object`](./Enums.md#enum-2x2_object) | Enum | The 2x2 variant of the object. | 1 |
| [`3x3_object`](./Enums.md#enum-3x3_object) | Enum | The 3x3 variant of the object. | 1 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `XIsSpellStormRampAndReset`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reset_percent` | Integer | The percentage of stacks to keep after resetting. | 1 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `bonk_damage`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damage Blocks}`](./Engine_Damage.md#all-confirmed-damage-instance-values) | Block | A damage hit definition. See Engine_Damage.md for the full schema. |  |
| `damage` | Integer | The base damage properties of an attack. | 1 |
| [`effects`](#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |

</details>

---

### Context: `damage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Integer | The base damage properties of an attack. | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 1 |

</details>

---

### Context: `damage_threshold_altanimations`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`graphics`](#context-graphics)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `heaviestMelee` | Integer | Animation trigger for massive damage. | 1 |
| `heavyMelee` | Integer | Animation trigger if damage exceeds this threshold. | 1 |

</details>

---

