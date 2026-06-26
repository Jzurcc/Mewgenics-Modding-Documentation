# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Abilities & Spells

> **Associated Files:** `data/abilities/, data/ability_templates/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2343

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2731 ||
| [`graphics`](#object-graphics) | Object | Object defining visual animations and sequence timings. | 2609 ||
| [`meta`](#object-meta) | Object | Object defining UI display data (Name, Description, Icon). | 2372 ||
| [`damage_instance`](#object-damage_instance) | Object | Object defining the combat math and status effects applied upon successful hit. | 2344 ||
| [`template`](./Enums.md#enum-template) | Enum | Inherits baseline internal logic from a hardcoded engine template. | 2174 ||
| [`target`](#object-target) | Object | Object defining the shape, range, and restrictions of the ability's aiming phase. | 1861 ||
| [`cost`](#object-cost) | Object | Object defining resource requirements (Mana, Act Points, Moves) needed to cast. | 1851 ||
| [`variant_of`](./Enums.md#enum-variant_of) | Enum | Inherits properties from a previously defined ability (used for upgrading tiers). | 1195 ||
| [`class`](./Enums.md#enum-class) | Enum | Categorizes the ability for specific UI filters. | 600 ||
| [`tags`](./Arrays.md#array-tags) | Array / Enum | Array of string categories used by the engine for filtering (e.g. [weapon_throw, spell]). | 241 ||
| [`self_damage`](#object-self_damage) | Boolean / Integer / Object | Recoil or self-inflicted damage/effects applied to the caster. | 218 ||
| [`spawn`](#object-spawn) | Object | Parameters for summoning new characters, objects, or entities. | 192 ||
| [`bonus_passives`](#object-bonus_passives) | Object | Passives granted to the character while this ability is equipped. | 136 ||
| [`temporary_effects`](#object-temporary_effects) | Object | Status applications that wear off automatically or at the end of the turn. | 88 ||
| [`effects`](#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 60 ||
| [`sounds`](#object-sounds) | Object | Audio cues triggered by the ability. | 39 ||
| [`splash_damage`](#object-splash_damage) | Object | Secondary Area of Effect blast parameters. | 34 ||
| [`ai_ability`](./Enums.md#enum-ai_ability) | Enum | Overrides the ability used when triggered by AI. | 29 ||
| [`keyword_tooltips`](#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear when hovering over the ability. | 28 ||
| [`chain_ability`](./Enums.md#enum-chain_ability) | Enum | An ability that automatically executes sequentially after this one. | 15 ||
| [`sub_ability`](./Enums.md#enum-sub_ability) | Enum | A secondary ability component referenced by complex templates. | 8 ||
| [`chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum || 3 ||
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | Enum || 3 ||
| [`cloned_ability`](./Enums.md#enum-cloned_ability) | Enum | Copies the properties of another ability dynamically. | 2 ||
| [`empty_self_damage`](#object-empty_self_damage) | Object | Recoil damage specifically applied when the attack misses all targets. | 2 ||
| [`bonk_damage`](#object-bonk_damage) | Object | Damage dealt when knocked into a wall or obstacle. | 1 ||
| [`damage`](#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1 ||

</details>

---

### Object: `graphics`


**Definition:** Object defining visual animations and sequence timings.  
**Total Count:** 2609


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | The primary flash animation label triggered. | 1557 ||
| [`particle`](./Enums.md#enum-particle) | Enum | References an impact or cast particle effect. | 486 ||
| [`projectile`](./Enums.md#enum-projectile) | Enum | References a projectile entity. | 227 ||
| `lob` | Boolean || 130 ||
| `delay` | Number | Frame delay before firing projectile/effect. | 93 ||
| `dont_visualize_ai` | Boolean || 86 ||
| `dont_orient` | Boolean | Prevents the character from turning to face the target. | 83 ||
| [`dash_animation`](./Enums.md#enum-dash_animation) | Enum | State-specific animations for trample/dash abilities. | 65 ||
| [`dash_start_animation`](./Enums.md#enum-dash_start_animation) | Enum || 63 ||
| [`speed`](./Enums.md) | Array / Number || 61 | [1.0] |
| [`affected_particle`](./Enums.md#enum-affected_particle) | Enum | Visuals applied to the target receiving the effect. | 51 ||
| [`dash_attack_animation`](./Enums.md#enum-dash_attack_animation) | Enum || 45 ||
| `lob_height` | Integer | Adjustments for arcing projectiles. | 45 ||
| [`animation_in`](./Enums.md#enum-animation_in) | Enum | Used for transition states (like burrowing). | 43 ||
| [`animation_out`](./Enums.md#enum-animation_out) | Enum | Used for transition states (like burrowing). | 43 ||
| [`jump_attack_animation`](./Enums.md#enum-jump_attack_animation) | Enum | Overrides for jump physics. | 39 ||
| `use_projectile` | Boolean || 35 ||
| [`palette`](./Enums.md) | Integer || 34 | 6 |
| [`full_jump_animation`](./Enums.md#enum-full_jump_animation) | Enum || 24 ||
| `full_jump_sync_frames` | Integer || 24 ||
| `use_rotation` | Boolean || 24 ||
| [`dash_end_animation`](./Enums.md#enum-dash_end_animation) | Enum || 22 ||
| `full_jump_windup_frames` | Integer || 20 ||
| `visual_delay_but_simultaneous_damage` | Integer || 18 ||
| [`center_particle`](./Enums.md#enum-center_particle) | Enum | Specific spawn points for particles. | 17 ||
| [`area_particle`](./Enums.md#enum-area_particle) | Enum | Specific spawn points for particles. | 16 ||
| `fall_from_sky` | Boolean | Spawns the projectile from the top of the screen. | 16 ||
| [`move_start_animation`](./Enums.md#enum-move_start_animation) | Enum || 14 ||
| `use_placeholder` | Boolean || 14 ||
| [`move_end_animation`](./Enums.md#enum-move_end_animation) | Enum || 13 ||
| `face_toss_target` | Boolean || 12 ||
| `ignore_slowtiles` | Boolean || 12 ||
| [`chain_distance`](./Enums.md#enum-chain_distance) | Number | Creates a tethered repeating graphic (like a hook). | 11 ||
| [`chain_movieclip`](./Enums.md#enum-chain_movieclip) | Enum | Creates a tethered repeating graphic (like a hook). | 11 ||
| `darken_screen` | Boolean | Dims the background during the ability cast. | 11 ||
| [`beam_cap`](./Enums.md#enum-beam_cap) | Enum | Flash movieclips used to render continuous laser beams. | 10 ||
| [`beam_clip`](./Enums.md#enum-beam_clip) | Enum | Flash movieclips used to render continuous laser beams. | 10 ||
| `bounce_on_hit` | Boolean | Visual hop when striking a target. | 10 ||
| `darken_screen_exclude_characters_on_tile` | Boolean || 10 ||
| [`end`](./Enums.md#enum-end) | Enum | Segments for continuous channeled animations. | 10 ||
| [`jump_start_animation`](./Enums.md#enum-jump_start_animation) | Enum || 10 ||
| [`loop`](./Enums.md#enum-loop) | Enum | Segments for continuous channeled animations. | 10 ||
| [`prime_animation`](./Enums.md#enum-prime_animation) | Enum || 10 ||
| [`start`](./Enums.md#enum-start) | Enum | Segments for continuous channeled animations. | 10 ||
| `max_tiles_single_loop` | Integer || 9 ||
| `sync_speed` | Integer || 9 ||
| [`random_delay`](./Arrays.md#array-random_delay) | Array | Adds chaotic timing to multi-projectile casts. | 9 ||
| `fx_is_placeholder_animation` | Boolean || 8 ||
| `aoe_spell_on_land` | Boolean | Visual trigger when a jump lands. | 7 ||
| `fx_random_flip` | Boolean || 7 ||
| [`land_animation`](./Enums.md#enum-land_animation) | Enum || 7 ||
| [`miss_particle`](./Enums.md#enum-miss_particle) | Enum | Specific spawn points for particles. | 7 ||
| `use_super_armor` | Boolean | Prevents flinch animations from interrupting this cast. | 7 ||
| [`air_animation`](./Enums.md#enum-air_animation) | Enum | Animation played while entity is airborne. | 6 ||
| [`custom_priming_animation`](./Enums.md#enum-custom_priming_animation) | Enum | Animation used while charging an ability. | 6 ||
| `darken_screen_exclude_self` | Boolean || 6 ||
| `darken_screen_start_early` | Boolean || 6 ||
| [`fall_randomize_timing`](./Enums.md#enum-fall_randomize_timing) | Number || 6 ||
| `min_throw_height` | Number || 6 ||
| `single_projectile` | Boolean || 6 ||
| [`miss_random_delay`](./Arrays.md#array-miss_random_delay) | Array || 6 ||
| [`detatched_animation`](./Enums.md#enum-detatched_animation) | Enum | Plays an animation separated from the character body. | 5 ||
| `detatched_animation_reach` | Integer || 5 ||
| [`empty_animation`](./Enums.md#enum-empty_animation) | Enum || 5 ||
| [`mode`](./Enums.md#enum-mode) | Enum || 5 ||
| `fixed_jump_height` | Number || 4 ||
| [`rocket_swirl`](#object-rocket_swirl) | Object | Visual parameters for swirling projectile paths. | 4 ||
| `sync_frames` | Integer || 4 ||
| [`dash_decelerating_animation`](./Enums.md#enum-dash_decelerating_animation) | Enum || 3 ||
| `decelerate` | Integer | Visual slowdown at the end of a movement. | 3 ||
| `delay_from_map_edge` | Boolean | Delays effect based on distance from the screen edge. | 3 ||
| `easing` | Integer | Smoothing function for movement animations. | 3 ||
| [`fixed_jump_speed`](./Enums.md#enum-fixed_jump_speed) | Number || 3 ||
| [`grab_animation`](./Enums.md#enum-grab_animation) | Enum || 3 ||
| [`lob_yoff`](./Enums.md#enum-lob_yoff) | Number | Adjustments for arcing projectiles. | 3 ||
| `lock_orientation_during_dash` | Boolean | Prevents the sprite from flipping mid-dash. | 3 ||
| `use_projectile_spawn_offset` | Boolean || 3 ||
| `use_rotation_once` | Boolean || 3 ||
| `always_play_animations` | Boolean | Bypasses speed-up/skip logic. | 2 ||
| `detatched_animation_cutoff` | Boolean || 2 ||
| `do_damage_immediately` | Boolean | Applies math before the animation actually hits. | 2 ||
| `jump_height_multiplier` | Number | Overrides for jump physics. | 2 ||
| [`mask_center`](./Enums.md#enum-mask_center) | Enum || 2 ||
| [`mask_extent`](./Enums.md#enum-mask_extent) | Enum || 2 ||
| `max_throw_height` | Number || 2 ||
| [`particle_mat`](./Enums.md#enum-particle_mat) | Enum || 2 ||
| [`preturn_animation`](./Enums.md#enum-preturn_animation) | Enum || 2 ||
| [`primed_alt_animation`](./Strings.md#string-primed_alt_animation) | String || 2 ||
| [`pseudoprojectile`](./Enums.md#enum-pseudoprojectile) | Enum || 2 ||
| `reverse_orientation` | Boolean || 2 ||
| `self_damage_mid_port` | Boolean || 2 ||
| `throw_speed` | Integer || 2 ||
| `use_hit_alts` | Boolean || 2 ||
| [`affected_animation`](./Enums.md#enum-affected_animation) | Enum | Visuals applied to the target receiving the effect. | 1 ||
| [`ally_animation`](./Enums.md#enum-ally_animation) | Enum | Distinct animation used when targeting a friendly unit. | 1 ||
| [`animate_name`](./Enums.md#enum-animate_name) | Boolean / Enum | Animates the ability name text on cast. | 1 ||
| `apex_distance` | Number | Calculations for the peak of a jump/lob arc. | 1 ||
| [`apex_time`](./Enums.md#enum-apex_time) | Number | Calculations for the peak of a jump/lob arc. | 1 ||
| `bypass_combatspeed` | Boolean || 1 ||
| [`damage_threshold_altanimations`](#object-damage_threshold_altanimations) | Object | Triggers different hit animations based on the amount of damage dealt. | 1 ||
| [`dash_bonk_animation`](./Enums.md#enum-dash_bonk_animation) | Enum || 1 ||
| `delay_from_map_center` | Boolean | Positional based timing delays. | 1 ||
| `delay_from_reverse_map_edge` | Boolean || 1 ||
| `do_animation_offscreen` | Boolean || 1 ||
| `do_not_clear_placeholder` | Boolean || 1 ||
| `face_targets` | Boolean | Forces the sprite to look at the target tile. | 1 ||
| `first_castpoint_is_self_damage_only` | Boolean || 1 ||
| [`hang_time`](./Enums.md#enum-hang_time) | Number || 1 ||
| `jump_speed_multiplier` | Number || 1 ||
| [`lob_speed`](./Enums.md#enum-lob_speed) | Number | Adjustments for arcing projectiles. | 1 ||
| `max_range` | Enum / Integer | The maximum and minimum distance required to cast. | 1 ||
| `min_range` | Integer | The maximum and minimum distance required to cast. | 1 ||
| `othercat_placeholder_available` | Boolean || 1 ||
| [`precast_delay`](./Enums.md#enum-precast_delay) | Number || 1 ||
| `uncatchable` | Boolean || 1 ||
| `use_directional_animations` | Boolean || 1 ||
| `use_origin_offsets` | Boolean || 1 ||
| [`spawn_offset`](./Arrays.md#array-spawn_offset) | Array || 1 ||

</details>

---

### Object: `meta`


**Definition:** Object defining UI display data (Name, Description, Icon).  
**Total Count:** 2374


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md) | Enum || 1641 | ABILITY_FORMOFTHEWOLF2_DESC |
| [`name`](./Enums.md) | Enum || 1611 | ABILITY_HAILOFNAILS_NAME |
| [`class`](./Enums.md#enum-class) | Enum | Categorizes the ability for specific UI filters. | 876 ||
| [`type_icon`](./Strings.md#string-type_icon) | Enum || 283 ||
| `animate_name` | Boolean / Enum | If true, adds a visual pop/animation to the name text when cast. | 177 ||
| [`icon_shell_frame`](./Strings.md#string-icon_shell_frame) | Mixed || 28 ||
| [`is_move`](./Enums.md#enum-is_move) | Mixed || 20 ||
| [`ability_icon`](./Enums.md#enum-ability_icon) | Enum | The UI icon to display in the action bar. | 14 ||
| [`tooltip_values`](./Arrays.md#array-tooltip_values) | Array || 9 ||
| [`icon_damage_display`](./Strings.md#string-icon_damage_display) | String || 8 ||
| [`icon_damage_display_eq`](./Math_Equations.md) | Equation || 7 ||
| `is_basic_attack` | Boolean || 6 ||
| `is_weapon` | Boolean || 4 ||
| [`icon_damage_type`](./Enums.md#enum-icon_damage_type) | Enum || 3 ||
| `is_trinket` | Boolean || 3 ||
| `dont_visualize_ai` | Boolean || 2 ||
| [`icon_damage_display_suffix`](./Strings.md#string-icon_damage_display_suffix) | String || 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||

</details>

---

### Object: `damage_instance`


**Definition:** Object defining the combat math and status effects applied upon successful hit.  
**Total Count:** 2346


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#object-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2344 ||
| [`effects`](#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 1787 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1554 ||
| [`damage`](#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1447 ||
| [`type`](./Enums.md#enum-type) | Enum | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). | 359 ||
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 352 ||
| [`knockback`](./Engine_DamagingKeys.md#valid-property-keys) | Mixed | The base physics pushing power (in tiles). | 254 ||
| `ai_base_score` | Integer | How highly the AI values using this ability. | 222 ||
| `heal` | `Number` | Restores health instead of dealing damage. | 122 ||
| `cant_miss` | `Boolean` | Guarantees the hit, bypassing dodge mechanics. | 110 ||
| `incidentally_collects_pickups` | `Boolean` | Automatically grabs items in the AoE. | 103 ||
| [`custom_additional_ai_weight`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Granular AI preference adjustments (e.g., `prefer_dont_move`). | 82 ||
| `piercing` | `Boolean` | Ignores a percentage of target defense/armor. | 52 ||
| `makes_contact` | `Boolean` | If false, explicitly avoids triggering contact-based passives. | 40 ||
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Z-index targeting (e.g., `characters`, `self`). | 26 ||
| [`blocked_damage`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Base damage dealt if the attack is blocked. | 24 ||
| [`raw_damage`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Unmitigated, unscaled base numbers. | 22 ||
| `crit_chance` | `Number` | Override for base critical hit probability. | 16 ||
| `override_trample_damage` | `Boolean` | Custom damage value for trample moves. | 15 ||
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. | 14 ||
| `can_revive` | `Boolean` | Healing instance that can bring dead allies back to life. | 8 ||
| `show_damage_on_0` | `Boolean` | Forces the "-0" floater text to appear. | 6 ||
| `force_play_hit_animation` | `Boolean` | Forces the flinch animation even on 0 damage. | 5 ||
| `blocked_multiplier` | `Number` | Multiplier applied when hitting a blocking target. | 4 ||
| [`accuracy`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Hit chance modifier. | 3 ||
| `can_collect_pickups` | `Boolean` | The damage instance can grab items on the ground. | 3 ||
| `can_instapop` | `Boolean` | Allows the attack to instantly destroy specific weak entities. | 2 ||
| `disallow_modifications` | `Boolean` | Prevents passives from altering this damage instance. | 2 ||
| `force_no_contact` | `Boolean` | Bypasses all contact-based retaliation (Thorns, etc). | 2 ||
| `non_lethal` | `Boolean` | Reduces target to 1 HP but will never kill. | 2 ||
| [`raw_heal`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Unmitigated, unscaled base numbers. | 2 ||
| `two_way_contact` | `Boolean` | Both caster and target trigger contact effects on each other. | 2 ||
| `damage_shield_only` | `Boolean` | Depletes shields but cannot harm base health. | 1 ||
| [`faction`](./Enums.md#enum-faction) | Enum | Determines alignment (`enemies`, `cats`, `neutral`). | 1 ||
| [`final_hit_bonus_damage`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Extra damage applied on the last hit of a multihit. | 1 ||
| `force_adjacent_and_diagonal_contact` | `Boolean` | Treats diagonal hits as physical contact. | 1 ||
| `force_no_knockback` | `Boolean` | Prevents the target from being pushed. | 1 ||
| `hint_dont_lowgravboost` | `Boolean` | AI hint to ignore wind physics. | 1 ||
| [`hit_animation_alt`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Custom flinch animation for the target. | 1 ||
| [`HealthRegenUp`](./Enums.md) | Integer || 1 | 2 |
| [`ranged`](./Enums.md) | Boolean || 1 | true |

</details>

---

### Object: `target`


**Definition:** Object defining the shape, range, and restrictions of the ability's aiming phase.  
**Total Count:** 1862


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max_range` | Enum / Integer | The maximum and minimum distance required to cast. | 1088 ||
| `max_aoe` | Enum / Integer | The maximum and minimum radius/length of the AoE. | 792 ||
| `min_range` | Integer | The maximum and minimum distance required to cast. | 583 ||
| [`target_mode`](./Enums.md#enum-target_mode) | Enum | How the cursor operates (`tile`, `direction`, `none`). | 503 ||
| [`restrictions`](./Arrays.md#array-restrictions) | Array / Enum | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). | 462 ||
| [`aoe_mode`](./Enums.md#enum-aoe_mode) | Enum | The shape of the area (`standard`, `line`, `cross`, `square`, `custom`). | 429 ||
| [`knockback_mode`](./Enums.md#enum-knockback_mode) | Enum / Integer | How physics vectors apply (`character_to_tile`, `pull_to_character`, `zero`, `orientation`). | 264 ||
| [`min_aoe`](./Enums.md#enum-min_aoe) | Mixed | The maximum and minimum radius/length of the AoE. | 253 ||
| `aoe_excludes_self` | Boolean | Prevents the AoE from hitting the caster. | 241 ||
| [`aoe_restrictions`](./Arrays.md#array-aoe_restrictions) | Array / Enum | Array of conditions the AoE tiles must meet (e.g., `must_have_line_of_sight_unpurgable`). | 197 ||
| `aoe_considers_character_size` | Boolean | Scales the AoE based on the caster's tile size (e.g., 2x2). | 170 ||
| [`range_mode`](./Enums.md#enum-range_mode) | Enum | How range is counted (`standard`, `ground_move`). | 114 ||
| [`X_is`](./Enums.md#enum-x_is) | Enum | Applies or references the 'X_is' effect/state. | 86 ||
| [`custom_aoe`](./Arrays.md#array-custom_aoe) | Array | Array of exact coordinates for a custom shape (e.g., `[[1, -1] [1, 0]]`). | 83 ||
| `multihit` | Enum / Integer | Hardcoded number of times the ability hits the target. | 62 ||
| `max_targets` | Integer / String | Limits on how many distinct entities can be targeted. | 56 ||
| `range_excludes_blocking` | Boolean | Cannot target through walls/obstacles. | 53 ||
| `prioritize_dont_change_direction` | Mixed | AI preference to maintain current facing angle. | 52 ||
| [`target_requires_tag`](./Enums.md#enum-target_requires_tag) | Enum | Target must possess this exact character tag. | 40 ||
| [`aoe_symmetry`](./Enums.md#enum-aoe_symmetry) | Enum | Determines if the AoE mirrors on axes. | 28 ||
| `prioritize_face_camera` | Mixed | AI preference to face South. | 26 ||
| `straight_shot` | Boolean | Ensures projectiles do not arc. | 24 ||
| `can_multihit` | Boolean | If true, overlapping AoEs can hit the same target multiple times. | 17 ||
| `allow_any_orientation` | Boolean | Allows casting regardless of the character's facing direction. | 16 ||
| `range_considers_character_size` | Boolean | Range calculation accounts for large entities. | 16 ||
| `throw_consumed_character` | Boolean | Throws the entity currently held/eaten. | 15 ||
| `min_targets` | Integer | Limits on how many distinct entities can be targeted. | 14 ||
| `aoe_leading_edge_only` | Boolean | Only the outermost edge of the AoE shape applies effects. | 13 ||
| `allow_diagonals` | Boolean | Allows targeting on diagonal grid axes. | 12 ||
| `range_display_include_character_size` | Boolean | Visual: offsets the range indicator for 2x2 units. | 12 ||
| `stagger_multihit_targets` | Boolean | Delays hits slightly between multiple targets. | 12 ||
| `upgrade_straight_shot_to_piercing` | Boolean | Allows the projectile to pass through multiple targets. | 11 ||
| `delayed_trigger` | Boolean | Delays the actual execution of the target effect. | 10 ||
| `consider_trample` | Boolean | AI consideration for moving through units. | 9 ||
| `N` | Integer | Variable modifier parameter. | 7 ||
| [`custom_range`](./Arrays.md#array-custom_range) | Array | Overrides standard range scaling. | 7 ||
| `always_bounce` | Boolean | Forces the attack/projectile to bounce regardless of hit. | 6 ||
| `multihit_max` | Integer | Variable limits for random multihit abilities. | 6 ||
| `multihit_min` | Integer | Variable limits for random multihit abilities. | 6 ||
| `reorient_thrown_character` | Boolean | Forces a thrown entity to face a certain way. | 6 ||
| [`toss_direction_restriction`](./Enums.md#enum-toss_direction_restriction) | Enum | Limits which ways an entity can be tossed. | 6 ||
| [`custom_aoe_util`](./Arrays.md#array-custom_aoe_util) | Array | Utility variants of custom AoE definitions. | 6 ||
| `aoe_hint_teamcast` | Boolean | Visual hint for cooperative casting abilities. | 5 ||
| [`aoe_tile_requires_element`](./Enums.md#enum-aoe_tile_requires_element) | Enum | Only affects tiles painted with a specific element. | 5 ||
| `distance_sort_targets` | Mixed | Prioritizes targets based on proximity. | 5 ||
| `dont_orient_aoe` | Boolean | Prevents the AoE shape from rotating with the character. | 5 ||
| `hint_can_target_pickups` | Boolean | UI hint that the player can target items on the ground. | 5 ||
| `max_bounces` | Integer | Hard cap on how many times a bouncing effect can trigger. | 5 ||
| `splash_damage_aoe_begin` | Integer | At what radius splash damage starts applying. | 5 ||
| [`aoe_chance`](./Enums.md#enum-aoe_chance) | Number / String | Percentage chance for the AoE to trigger. | 4 ||
| `as_the_crow_flies` | Boolean | Calculates range ignoring all pathing terrain obstacles. | 4 ||
| `force_ai_target_as_spell` | Boolean | Forces the AI to treat a physical move like a spell for targeting logic. | 4 ||
| `range_display_include_aoe` | Boolean | Visual: shows the full AoE potential when previewing range. | 4 ||
| `shotgun_mode` | Boolean | Deals more damage/hits if targets are closer. | 4 ||
| `shuffle_tile_order` | Boolean | Randomizes the execution order of AoE tiles. | 4 ||
| `upgrade_straight_shot_to_boomerang` | Boolean | Makes the projectile return to caster. | 4 ||
| [`mouse_offset`](./Arrays.md#array-mouse_offset) | Array | Visual offset for the targeting cursor. | 4 ||
| `dont_orient` | Boolean | Prevents the character from turning to face the target. | 3 ||
| `low_health_character_threshold` | Mixed | AI targeting threshold for seeking weak targets. | 3 ||
| `randomize_target_within_range` | Integer | Picks a random valid tile instead of the user's click. | 3 ||
| [`special_tile_tag`](./Enums.md#enum-special_tile_tag) | Enum | Targets only tiles with this specific tag. | 3 ||
| `track_target` | Boolean | Projectile/Effect follows moving targets. | 3 ||
| `corpse_priority` | Integer | AI preference for targeting dead bodies. | 2 ||
| `hint_can_target_empty` | Boolean | UI hint that the player can click an empty tile. | 2 ||
| `low_gravity_boostable` | Boolean | Can be affected by low gravity wind/effects. | 2 ||
| `prioritize_change_direction` | Boolean | AI preference to attack from different angles. | 2 ||
| [`range_bonuses`](./Enums.md#enum-range_bonuses) | Enum | How much extra range is added by stats/passives. | 2 ||
| `range_display_include_direction` | Boolean | Visual: shows directional arrows. | 2 ||
| `recalc_target_on_castpoint` | Boolean | Re-checks if target is valid at the exact frame of cast. | 2 ||
| `redirect_location_if_blocked` | Boolean | Shifts target to adjacent tile if original is invalid. | 2 ||
| `trample_allies_too` | Boolean | Trample movement damages allies in the path. | 2 ||
| [`target_requires_element`](./Arrays.md#array-target_requires_element) | Array | Target must be afflicted with this element. | 2 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`adjust_target`](./Enums.md#enum-adjust_target) | Enum | Tweaks target selection post-cast. | 1 ||
| `allow_diagonal_passthrough` | Boolean | Permits diagonal targeting through tight corners. | 1 ||
| `ally_priority` | Integer | AI preference for targeting allies. | 1 ||
| `aoe_display_exclude_restrictions` | Boolean | Visual only: Hides invalid tiles from the AoE preview. | 1 ||
| `aoe_rotate_around_character_center` | Boolean | Anchors the AoE rotation to the character rather than the tile. | 1 ||
| `aoe_spell_on_land` | Boolean | Visual trigger when a jump lands. | 1 ||
| `bonus_pathing_leniency` | Integer | Gives the AI leeway when calculating complex paths. | 1 ||
| `damage_collided_only` | Boolean | Only damages the first entity the projectile/dash hits. | 1 ||
| `enemy_priority` | Integer | AI preference for targeting enemies. | 1 ||
| `force_no_contact` | `Boolean` | Bypasses all contact-based retaliation (Thorns, etc). | 1 ||
| `hint_can_target_static` | Boolean | UI hint that the player can target inanimate objects. | 1 ||
| [`knockback_modifier`](./Enums.md#enum-knockback_modifier) | Enum | Multiplier for the knockback physics force. | 1 ||
| `lingering` | Boolean | Target zone remains active across multiple turns. | 1 ||
| `mirror_custom_aoe` | Boolean | Flips the custom AoE array. | 1 ||
| [`prioritize_throw_target_with_passive`](./Enums.md#enum-prioritize_throw_target_with_passive) | Enum | AI prefers throwing targets that have specific passives. | 1 ||
| `randomize_knockback_direction_except_for_finisher` | Boolean | Chaotic knockback unless it kills the target. | 1 ||
| `range_excludes_self` | Boolean | Cannot click on the caster's tile. | 1 ||
| `range_max` | Integer | Alternate syntax for `max_range`/`min_range`. | 1 ||
| `range_min` | Integer | Alternate syntax for `max_range`/`min_range`. | 1 ||
| [`range_symmetry`](./Enums.md#enum-range_symmetry) | Enum | Mirrors the range grid. | 1 ||
| `remain_off_map` | Boolean | Keeps entity removed from the grid. | 1 ||
| [`restructions`](./Enums.md#enum-restructions) | Enum | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). | 1 ||
| `reverse_target_direction` | Boolean | Inverts the targeting vector. | 1 ||
| `spin_steps` | Integer | Number of rotational increments for spin targeting. | 1 ||
| `uncounterable` | Boolean | Bypasses counter-attack passives. | 1 ||
| [`custom_aoe_mirror`](./Arrays.md#array-custom_aoe_mirror) | Array | How the custom shape mirrors when facing left vs right. | 1 ||
| [`custom_aoe_util_mirror`](./Arrays.md#array-custom_aoe_util_mirror) | Array || 1 ||

</details>

---

### Object: `cost`


**Definition:** Object defining resource requirements (Mana, Act Points, Moves) needed to cast.  
**Total Count:** 1853


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Enum / Integer | MP pool and how much it restores per turn. | 1605 ||
| `infcantrip` | Boolean | Can be cast infinitely as long as costs are met. | 810 ||
| `cantrip` | Boolean | Does not end the turn when cast. | 560 ||
| `once_per_fight` | Mixed | Exhausts for the remainder of combat after one use. | 98 ||
| `act_points` | Integer | Consumes primary action points (default 1). | 86 ||
| `move_points` | Integer | Consumes movement points. | 59 ||
| `prime` | Integer | Requires a "priming" turn before it fires. | 30 ||
| `allow_offmap_casts` | Boolean | Can be used while the character is hidden/removed from grid. | 22 ||
| `cant_cast` | Mixed | Explicitly disables casting (used for passive-triggered only abilities). | 18 ||
| [`charge`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Cooldown timers measured in turns. | 18 ||
| `must_be_consuming` | Boolean | Requires the character to be eating/holding something. | 17 ||
| `must_not_be_consuming` | Boolean | Cannot be holding/eating an entity. | 14 ||
| `requires_reload` | Boolean | Must spend an action to reload before casting again. | 14 ||
| `can_cast_while_dead` | Boolean | Usable by corpses (e.g., DeathRattle triggers). | 12 ||
| [`cantrip_group`](./Enums.md#enum-cantrip_group) | Enum | Groups cantrips so using one exhausts the others. | 12 ||
| `must_be_offmap` | Boolean | Requires the character to be hidden/dug underground. | 12 ||
| `X_cant_be_zero` | Boolean | Applies or references the 'X_cant_be_zero' effect/state. | 11 ||
| `disallow_cost_modification` | Boolean | Prevents passives from making this cheaper. | 9 ||
| `coins` | Integer | Consumes currency to cast. | 8 ||
| `main_turn_only` | Boolean | Cannot be cast during bonus or dispersed turns. | 8 ||
| `requires_destructible_weapon` | Boolean | The equipped weapon must be breakable. | 8 ||
| `requires_exact_character_aux` | Integer | Hardcoded character specific lock. | 8 ||
| [`durability`](./Enums.md) | Integer || 8 | 0 |
| `must_not_be_a_summon` | Boolean | Summons/Familiars cannot cast this. | 7 ||
| `start_reloaded` | Boolean | Spawns with the ability pre-loaded. | 7 ||
| `must_be_first_action` | Boolean | Can only be used at the very start of the turn. | 4 ||
| `enabled_formula` | Mixed | Mathematical string required to be >0 to cast. | 3 ||
| `must_be_first_nonmove_action` | Boolean | Can move first, but cannot use other abilities first. | 3 ||
| `must_have_weapon` | Boolean | Requires a weapon equipped in the item slot. | 2 ||
| `can_be_refreshed` | Boolean | Passives/Effects can reset this ability's cooldown. | 1 ||
| `can_pay_over_multiple_turns` | Boolean | Allows channeling costs over time. | 1 ||
| `can_self_refresh` | Boolean | The ability has mechanics to reset its own cooldown. | 1 ||
| `damage_cant_be_zero` | Boolean | Requires the ability to have >0 calculated damage to cast. | 1 ||
| `initial_charge` | Integer | How many turns it starts on cooldown at battle start. | 1 ||
| `manacost_cant_be_zero` | Boolean | Fails to cast if mana cost is reduced to 0. | 1 ||
| `minimum_con` | Integer | Stat thresholds required to cast. | 1 ||
| `minimum_spd` | Integer | Stat thresholds required to cast. | 1 ||
| `require_default_size` | Boolean | 2x2 or altered characters cannot cast this. | 1 ||
| `requires_attack_damage_threshold` | Integer | Needs a certain amount of innate damage. | 1 ||
| `requires_consumed_trinket` | Boolean | Must have eaten a specific item type. | 1 ||
| `requires_empty_trinket` | Boolean | Must not have an accessory equipped. | 1 ||
| `requires_hp_threshold` | Integer | Must be below/above a certain health percentage. | 1 ||
| `requires_weapon` | Boolean | Prerequisite: Must meet this condition. | 1 ||

</details>

---

### Object: `self_damage`


**Definition:** Recoil or self-inflicted damage/effects applied to the caster.  
**Total Count:** 220


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#object-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 220 ||
| [`effects`](#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 200 ||
| [`damage`](./Abilities_and_Spells.md#object-damage) | Mixed | The base damage properties of an attack. | 47 ||
| `piercing` | `Boolean` || 12 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 11 ||
| `cant_miss` | `Boolean` || 10 ||
| `knockback` | Enum / Integer || 10 ||
| `heal` | `Number` || 6 ||
| [`elements`](./Arrays.md#array-elements) | Array || 4 ||
| `ai_base_score` | Integer || 2 ||
| `non_lethal` | `Boolean` || 1 ||

</details>

---

### Object: `spawn`


**Definition:** Parameters for summoning new characters, objects, or entities.  
**Total Count:** 192


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md) | Array / Enum || 184 | [TallSkeletonCat] |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 83 ||
| [`faction`](./Enums.md#enum-faction) | Enum || 59 ||
| `ai_base_score` | Integer || 31 ||
| [`additional_passives`](#object-additional_passives) | Object | Passives granted intrinsically to a spawned entity. | 20 ||
| [`first_turn`](./Enums.md#enum-first_turn) | Enum || 17 ||
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `String` || 14 ||
| [`catdata`](./Enums.md) | Enum || 13 | fleshgolem |
| `clone_items` | Boolean | If true, transfers inventory to the clone. | 12 ||
| `lob` | Boolean || 4 ||
| [`post_spawn_statuses`](#object-post_spawn_statuses) | Object | Status effects applied immediately after an entity spawns. | 4 ||
| [`size`](./Enums.md) | Integer || 4 | 2 |
| `face_camera` | Boolean || 2 ||
| `inherit_elite_buffs` | Boolean || 2 ||
| `start_dead` | Boolean || 2 ||
| [`appearance`](./Enums.md#enum-appearance) | Enum || 1 ||
| [`auto_cast_on_spawn`](./Enums.md#enum-auto_cast_on_spawn) | Enum || 1 ||
| [`chapter`](./Enums.md#enum-chapter) | Enum || 1 ||
| [`custom_additional_ai_weight`](./Engine_DamagingKeys.md#valid-property-keys) | `String` || 1 ||
| `include_passives` | Boolean || 1 ||
| `redirect_location_if_blocked` | Boolean || 1 ||
| [`spawnin_animation`](./Enums.md#enum-spawnin_animation) | Enum || 1 ||
| `trigger_battle_start` | Boolean || 1 ||

</details>

---

### Object: `bonus_passives`


**Definition:** Passives granted to the character while this ability is equipped.  
**Total Count:** 138


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 137 ||
| [`DeadAltAbility`](./Enums.md) | Enum || 12 | DonateBlood_Afterlife |
| [`AbilityEnabledOncePerFightAtHealthThreshold`](./Enums.md) | Integer || 7 | 50 |
| [`XIsFreeArmorSlots`](./Enums.md) | Integer || 7 | 1 |
| [`AbilityEnabledPercentEachTurn`](./Enums.md) | Integer || 6 | 50 |
| [`FreeFirstCast`](./Enums.md) | Integer || 6 | 4 |
| [`XIsLivingAlliesWithTag`](./Enums.md) | Enum || 5 | hitler_clone_fetus |
| [`CatchBoomerang`](./Enums.md) | Integer || 4 | 1 |
| [`CopyBasicAttackEffects`](./Enums.md) | Integer || 4 | 1 |
| [`DownRankAIIfWeaponUsable`](./Enums.md) | Number || 4 | .001 |
| [`AbilityEnableIfConsumedCharacterHasTag`](./Enums.md) | Enum || 3 | sp_pill_normal |
| [`AbilityEnabledOncePerRound`](./Enums.md) | Integer || 3 | 1 |
| [`AbilityInheritsWeaponEffects`](./Enums.md) | Integer || 3 | 2 |
| [`MoonHeadFinisherEnabler`](./Enums.md) | Integer || 3 | 0 |
| [`XIsMultipliedPercentHealth`](./Enums.md) | Array || 3 | [2] |
| [`AbilityEnabledIfHasStatus`](./Enums.md) | Enum || 2 | DemonicGlyph_Summon |
| [`AutocastEachRound`](#object-autocasteachround) | Object || 2 ||
| [`ChargeSpiritBombAura`](./Enums.md) | Enum || 2 | DonateEnergy |
| [`CopyCatPassive_Initializer`](./Enums.md) | Integer || 2 | 2 |
| [`NukeQuestFinalBossModifications`](#object-nukequestfinalbossmodifications) | Object || 2 ||
| [`ReloadOnKill`](./Enums.md) | Integer || 2 | 1 |
| [`ReloadOnKillEnemy`](./Enums.md) | Integer || 2 | 1 |
| [`ReloadOnTotalDamageReceived`](./Enums.md) | Integer || 2 | 15 |
| [`XIsLivingCharactersWithTag`](./Enums.md) | Enum || 2 | husk |
| [`XIsOtherHealsThisTurn`](./Enums.md) | Integer || 2 | 1 |
| [`XIsSpellStormRampAndReset`](#object-xisspellstormrampandreset) | Integer / Object || 2 | 0 |
| [`XIsTimesDamageTaken`](./Enums.md) | Integer || 2 | 1 |
| [`AbilityDisableIfLivingCrow`](./Enums.md) | Integer || 1 | 1 |
| [`AbilityEnabledAtHealthThreshold`](./Enums.md) | Integer || 1 | 50 |
| [`AbilityEnabledIfBasicAttackUsedThisTurn`](./Enums.md) | Integer || 1 | 1 |
| [`AbilityEnabledIfMovementTrapped`](./Enums.md) | Integer || 1 | 1 |
| [`AbilityEnabledIfNoAggroTarget`](./Enums.md) | Integer || 1 | 1 |
| [`AbilityEnabledIfNotHasStatus`](./Enums.md) | Enum || 1 | BackflipWhenTargeted |
| [`AbilityEnabledIfSpecificItemEquipped`](./Enums.md) | Enum || 1 | Neverstone |
| [`AbsorbManaFromOtherSpells`](./Enums.md) | Integer || 1 | 1 |
| [`AddElementsToSpells`](./Enums.md) | Enum || 1 | Earth |
| [`AddStatusToBasicAttack`](#object-addstatustobasicattack) | Object || 1 ||
| [`AlphaDodgeChance`](./Enums.md) | Integer || 1 | 50 |
| [`AlphaStatusOnTurnBegin`](#object-alphastatusonturnbegin) | Object || 1 ||
| [`BonusAbility_DelayedApplication`](./Enums.md) | Enum || 1 | Slap |
| [`CapTechSpent`](./Enums.md) | Integer || 1 | 1 |
| [`CaveWomanBirthControl`](./Enums.md) | Integer || 1 | 1 |
| [`CritChanceUp`](./Enums.md) | Integer || 1 | 2 |
| [`FistOfFateUniqueEnemyTracker`](./Enums.md) | Integer || 1 | 1 |
| [`FreeFirstCastAndAfterSpendMana`](./Enums.md) | Integer || 1 | 1 |
| [`FreeFirstCastEachMatch`](./Enums.md) | Integer || 1 | 1 |
| [`HealthRegenUp`](./Enums.md) | Integer || 1 | 2 |
| [`IgnoreTiles`](./Enums.md) | Integer || 1 | 1 |
| [`IntelligenceUp`](./Enums.md) | Enum / Integer || 1 | item_aux |
| [`InterchangeDisabler`](./Enums.md) | Integer || 1 | 1 |
| [`KnockbackImmunity`](./Enums.md) | Integer || 1 | 1 |
| [`PassiveWhileNotTakingTurn`](#object-passivewhilenottakingturn) | Object || 1 ||
| [`ReloadOnAllyCatDies`](./Enums.md) | Integer || 1 | 1 |
| [`ReloadOnAllyDies`](./Enums.md) | Integer || 1 | 1 |
| [`ReloadOnAnyDamage`](./Enums.md) | Integer || 1 | 1 |
| [`ReloadOnBackstab`](./Enums.md) | Integer || 1 | 1 |
| [`ReloadOnElementalDamageReceived`](./Enums.md) | Enum || 1 | Holy |
| [`ReloadOnGainCoins`](./Enums.md) | Integer || 1 | 1 |
| [`ReloadOnGainDivineShield`](./Enums.md) | Integer || 1 | 1 |
| [`ReloadOnKillTagged`](./Enums.md) | Enum || 1 | rock |
| [`ReloadOnSpendMana`](./Enums.md) | Integer || 1 | 1 |
| [`ReloadOnUseAbilityWithManaCost`](./Enums.md) | Integer || 1 | 6 |
| [`RevengeDamage`](#object-revengedamage) | Object || 1 ||
| [`StatusKillers`](#object-statuskillers) | Object || 1 ||
| [`TossTargetIsAggroTarget`](./Enums.md) | Integer || 1 | 1 |
| [`TossTargetIsBuddy`](./Enums.md) | Integer || 1 | 1 |
| [`TossTargetIsNotInWater`](./Enums.md) | Integer || 1 | 1 |
| [`Trample`](./Enums.md) | Integer || 1 | 3 |
| [`XIsConsumedCharacterMaxHP`](./Enums.md) | Integer || 1 | 3 |
| [`XIsCountDeaths`](./Enums.md) | Integer || 1 | 1 |
| [`XIsCountStatusStacks`](./Enums.md) | Enum || 1 | DodgeChance_Status |
| [`XIsFormulaLockedUntilComplete`](./Enums.md) | Enum || 1 | dex |
| [`XIsIncreaseEachTurn`](./Enums.md) | Integer || 1 | 1 |
| [`XIsRampAndReset`](./Enums.md) | Integer || 1 | 0 |
| [`XIsRecycleCostReduction`](./Enums.md) | Integer || 1 | 5 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `temporary_effects`


**Definition:** Status applications that wear off automatically or at the end of the turn.  
**Total Count:** 88


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 37 ||
| [`Trample`](./Enums.md) | Integer || 26 | 3 |
| `CastAgain` | Integer / String | Applies or references the 'CastAgain' effect/state. | 20 ||
| `DisableTrample` | Integer | Applies or references the 'DisableTrample' effect/state. | 10 ||
| `Fury` | Integer | Applies or references the 'Fury' effect/state. | 7 ||
| [`TileTrail`](./Enums.md) | Enum || 6 | FloatingGlassTile |
| `JustInCaseTrample` | Integer | Applies or references the 'JustInCaseTrample' effect/state. | 5 ||
| [`LeaveBehind`](#object-leavebehind) | Enum / Object | Spawns a specific object at the character's previous location when they move. | 5 ||
| `DashFury` | Integer | Applies or references the 'DashFury' effect/state. | 3 ||
| `BearTrapTrail` | Integer | Applies or references the 'BearTrapTrail' effect/state. | 2 ||
| [`AfterImage`](#object-afterimage) | Object || 2 ||
| `DelayedWindTrail` | Integer | Applies or references the 'DelayedWindTrail' effect/state. | 1 ||
| [`JumpAttackLeaveBehind`](./Enums.md#enum-jumpattackleavebehind) | Enum | Applies or references the 'JumpAttackLeaveBehind' effect/state. | 1 ||
| [`DoubleLoot`](./Enums.md) | Integer || 1 | 2 |
| [`KnockbackImmunity`](./Enums.md) | Integer || 1 | 1 |
| [`TileTrail_Ahead`](./Enums.md) | Enum || 1 | FlowerTile |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `Else`


**Definition:** Fallback object that executes if the preceding `Conditional_` block evaluated to false.  
**Total Count:** 71


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional_boss), [`Conditional_Buddy`](./Abilities_and_Spells.md#object-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional_object), [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional_speculative), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 66 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 23 ||
| [`GainDisorderFromPool_PostCast`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 7 ||
| [`ApplyToSource`](#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 6 ||
| [`BonusDamage`](./Engine_LogicKeys.md#valid-property-keys) | Enum / Integer | Applies or references the 'BonusDamage' effect/state. | 6 ||
| [`CanApplyToInanimate`](#object-canapplytoinanimate) | Object | Modifier object that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 3 ||
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 3 ||
| `CaptureFamiliar` | Integer | Applies or references the 'CaptureFamiliar' effect/state. | 2 ||
| [`Conditional_HasStatus`](#object-conditional_hasstatus) | Object | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 2 ||
| `FactionConversion` | Integer | Applies or references the 'FactionConversion' effect/state. | 2 ||
| [`FormChange`](#object-formchange) | Enum / Object | Transforms the character into a different state or form (e.g., Rage, HasCat). | 2 ||
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 2 ||
| `RandomStatDown` | Array / Integer / String | Applies or references the 'RandomStatDown' effect/state. | 2 ||
| `SpawnBearTrapIfHitKills` | `Number` | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. | 2 ||
| [`SpawnThingIfHitKills`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'SpawnThingIfHitKills' effect/state. | 2 ||
| [`RandomStatusFromPool`](#object-randomstatusfrompool) | Object | Selects and applies a random status effect from the provided nested block. | 2 ||
| [`Cleanse`](./Enums.md) | Integer || 2 | 0 |
| [`Confusion`](./Enums.md) | Array / Integer || 2 | [.1] |
| [`GainCoinsRange`](#object-gaincoinsrange) | Object || 2 ||
| [`RandomStatUp`](./Enums.md) | Enum / Integer || 2 | ceil(X/3) |
| [`Revive`](./Enums.md) | Integer || 2 | 50 |
| [`ApplyToRandomPartyMemberIfPossible`](#object-applytorandompartymemberifpossible) | Object | Redirects the nested effects to apply to a random living member of the player's party. | 1 ||
| [`CatPartsTransform`](#object-catpartstransform) | Object | Transforms specific body parts into different visual variants. | 1 ||
| [`Conditional_Displaceable`](#object-conditional_displaceable) | Object | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 1 ||
| [`Conditional_GoodRoll`](#object-conditional_goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 1 ||
| [`Conditional_HealthThreshold`](#object-conditional_healththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 1 ||
| [`Consumed`](#object-consumed) | Object | State object triggered when this object or entity is eaten/consumed by another character. | 1 ||
| [`DestroyEquipmentAndAttachParasite`](#object-destroyequipmentandattachparasite) | Object | Removes an equipped item and replaces it with a parasite from a specified pool. | 1 ||
| `DieViolently` | Integer | Applies or references the 'DieViolently' effect/state. | 1 ||
| [`DoDamage`](#object-dodamage) | Object | Explicitly triggers a secondary damage instance independent of the main attack. | 1 ||
| `ExplodeCharacter` | `Number` | Applies or references the 'ExplodeCharacter' effect/state. | 1 ||
| `ExplodeCharacter_Party` | `Number` | Applies or references the 'ExplodeCharacter_Party' effect/state. | 1 ||
| `FaceCamera` | `Number` | Applies or references the 'FaceCamera' effect/state. | 1 ||
| `FlatAIBonus` | `Number` | Applies or references the 'FlatAIBonus' effect/state. | 1 ||
| `ForceImmediateMove` | `Number` | Applies or references the 'ForceImmediateMove' effect/state. | 1 ||
| `GenericDebuff` | `Number` | Applies or references the 'GenericDebuff' effect/state. | 1 ||
| [`ImmediateUseAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ImmediateUseAbility' effect/state. | 1 ||
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 1 ||
| [`KnockUpAndAway`](#object-knockupandaway) | Object | Displaces the target vertically and horizontally away from the source. | 1 ||
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 1 ||
| `PurgeAll` | `Number` | Applies or references the 'PurgeAll' effect/state. | 1 ||
| `RemoveMovePoints` | `Number` | Applies or references the 'RemoveMovePoints' effect/state. | 1 ||
| `RemoveTurnsThisRound` | `Number` | Applies or references the 'RemoveTurnsThisRound' effect/state. | 1 ||
| `SetHealth` | `Number` | Applies or references the 'SetHealth' effect/state. | 1 ||
| `SetShield` | `Number` | Applies or references the 'SetShield' effect/state. | 1 ||
| [`ShowFakeDamage`](#object-showfakedamage) | Object | Displays a visual damage number without actually modifying health. | 1 ||
| `SpeculativeMoveSelfCorpseOffMap` | `Number` | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 1 ||
| [`Temporary`](#object-temporary) | Object | A wrapper object for applying status effects that automatically expire. | 1 ||
| `VaporizeInanimate` | `Number` | Applies or references the 'VaporizeInanimate' effect/state. | 1 ||
| [`XIsTargetHealth`](#object-xistargethealth) | Object | Math variable assignment: Evaluates X as the target's current health. | 1 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer || 1 | 2 |
| [`Bruise`](./Enums.md) | Array / Integer || 1 | [.1] |
| [`Charmed`](./Enums.md) | Array / Enum / Integer || 1 | [.1] |
| [`Cleave`](#object-cleave) | Integer / Object || 1 | 1 |
| [`Conditional_HasTag`](#object-conditional_hastag) | Object || 1 ||
| [`Conditional_Object`](#object-conditional_object) | Object || 1 ||
| [`Conditional_Speculative`](#object-conditional_speculative) | Object || 1 ||
| [`ConstitutionUp`](./Enums.md) | Array / Enum / Integer || 1 | [.5] |
| [`CritChanceUp`](./Enums.md) | Integer || 1 | 2 |
| [`DamageUp`](./Enums.md) | Integer / String || 1 | 3 |
| [`DodgeChance_Status`](./Enums.md) | Integer || 1 | 50 |
| [`DybbukPossessed`](#object-dybbukpossessed) | Object || 1 ||
| [`Else`](#object-else) | Object || 1 ||
| [`Immobile`](./Enums.md) | Array / Integer || 1 | [.1] |
| [`Leeches`](./Enums.md) | Integer || 1 | 2 |
| [`ObjectOnHitCharacter`](#object-objectonhitcharacter) | Enum / Object || 1 | SkeletonCatFamiliar |
| [`PartialCleanse`](./Enums.md) | Integer || 1 | 9999 |
| [`ScatterCoins`](#object-scattercoins) | Object || 1 ||
| [`Slow`](./Enums.md) | Array / Enum / Integer || 1 | [.1] |
| [`SpeedUp`](./Enums.md) | Enum / Integer || 1 | 4 |

</details>

---

### Object: `ApplyToSource`


**Definition:** Redirects the nested effects to apply to the caster/source of the ability instead of the target.  
**Total Count:** 51


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyStatusIfCrit`](./Abilities_and_Spells.md#object-applystatusifcrit), [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate), [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional_goodroll), [`Conditional_HasStatus`](./Abilities_and_Spells.md#object-conditional_hasstatus), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional_healththreshold), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#object-conditional_livingplayercat), [`Conditional_PlayerCat`](./Abilities_and_Spells.md#object-conditional_playercat), [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#object-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#object-else), [`Math`](./Abilities_and_Spells.md#object-math), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 43 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 20 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer || 6 | 2 |
| [`HealthGain`](./Enums.md) | Integer || 6 | 5 |
| [`StrengthUp`](./Enums.md) | Enum / Integer || 6 | max(int, 0) |
| [`Shield`](./Enums.md) | Enum / Integer || 5 | 2*X |
| [`EvolveAbilityFromPool`](./Abilities_and_Spells.md#object-evolveabilityfrompool) | `String` | Upgrades or transforms an existing ability into a new one from the specified pool. | 4 ||
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | `String` | Transforms the character into a different state or form (e.g., Rage, HasCat). | 4 ||
| [`AddWeaponAux`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'AddWeaponAux' effect/state. | 3 ||
| [`Craft`](#object-craft) | Object | Synthesizes or spawns a new item from a specific pool. | 3 ||
| `RefreshActPoints` | `Number` | Applies or references the 'RefreshActPoints' effect/state. | 3 ||
| [`ConstitutionUp`](./Enums.md) | Array / Enum / Integer || 3 | [.5] |
| `AddLeechesStatus` | `Number` | Applies or references the 'AddLeechesStatus' effect/state. | 2 ||
| [`DoDamage`](#object-dodamage) | Object | Explicitly triggers a secondary damage instance independent of the main attack. | 2 ||
| [`Cleanse`](./Enums.md) | Integer || 2 | 0 |
| [`EquipPermanentItem`](./Enums.md) | Enum || 2 | BoneClub |
| [`FindItemFromPool`](#object-finditemfrompool) | Object || 2 ||
| [`FreeSpell`](./Enums.md) | Integer || 2 | 2 |
| [`LuckUp`](./Enums.md) | Enum / Integer || 2 | 2 |
| [`RemoveStatus`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'RemoveStatus' effect/state. | 1 ||
| `DisableWeapon` | `Number` | Applies or references the 'DisableWeapon' effect/state. | 1 ||
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 1 ||
| [`KnockUpAndAway`](#object-knockupandaway) | Object | Displaces the target vertically and horizontally away from the source. | 1 ||
| `ManaGain` | `Number` | Applies or references the 'ManaGain' effect/state. | 1 ||
| `RefreshMovePoints` | `Number` | Applies or references the 'RefreshMovePoints' effect/state. | 1 ||
| [`SpecificInjury`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'SpecificInjury' effect/state. | 1 ||
| `StanceSwitchToMelee` | `Number` | Applies or references the 'StanceSwitchToMelee' effect/state. | 1 ||
| `StanceSwitchToRanged` | `Number` | Applies or references the 'StanceSwitchToRanged' effect/state. | 1 ||
| `TakeExtraTurn` | `Number` | Applies or references the 'TakeExtraTurn' effect/state. | 1 ||
| `TempTrampleUntilSettled` | `Number` | Applies or references the 'TempTrampleUntilSettled' effect/state. | 1 ||
| [`Brace`](./Enums.md) | Integer || 1 | 2 |
| [`Bruise`](./Enums.md) | Array / Integer || 1 | [.1] |
| [`DivineShield`](./Enums.md) | Integer || 1 | 2 |
| [`FindItem`](./Enums.md) | Enum || 1 | Molars |
| [`ForceUseAbility`](./Enums.md) | Enum || 1 | MotherTumorGrow |
| [`GainCoinsRange`](#object-gaincoinsrange) | Object || 1 ||
| [`KineticSpikes`](./Enums.md) | Integer || 1 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer || 1 | 1 |
| [`Tech`](./Enums.md) | Integer || 1 | 3 |

</details>

---

### Object: `Conditional_HasTag`


**Definition:** Conditional trigger: Executes nested logic if the target possesses the specified entity tag.  
**Total Count:** 47


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional_object), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 46 ||
| [`tag`](./Enums.md) | Enum || 46 | megadino |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 11 ||
| [`Conditional_NotBoss`](#object-conditional_notboss) | Object | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 6 ||
| `FloatingRockTrap` | `Number` | Applies or references the 'FloatingRockTrap' effect/state. | 6 ||
| [`Conditional_Boss`](#object-conditional_boss) | Object | Conditional trigger: Executes nested logic if the target is a Boss. | 4 ||
| `IgnoreDamage` | `Number` | Applies or references the 'IgnoreDamage' effect/state. | 4 ||
| [`ApplyToSource`](#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 ||
| [`ImmediateUseAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ImmediateUseAbility' effect/state. | 3 ||
| [`ApplyToSourceOnKill`](#object-applytosourceonkill) | Object | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 2 ||
| [`CanApplyToInanimate`](#object-canapplytoinanimate) | Object | Modifier object that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 2 ||
| `Die` | `Number` | Applies or references the 'Die' effect/state. | 2 ||
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 2 ||
| [`ChangeTilesUnder`](./Enums.md) | Enum || 2 | LavaTile |
| [`DamageUp`](./Enums.md) | Integer / String || 2 | 3 |
| [`Else`](#object-else) | Object || 2 ||
| `BonusDamage` | Enum / Integer | Applies or references the 'BonusDamage' effect/state. | 1 ||
| [`Conditional_InForm`](#object-conditional_inform) | Object | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 1 ||
| `CrackMoonHead` | `Number` | Applies or references the 'CrackMoonHead' effect/state. | 1 ||
| `DeleteObject` | `Number` | Applies or references the 'DeleteObject' effect/state. | 1 ||
| `DisplaceTowardsSource` | `Number` | Applies or references the 'DisplaceTowardsSource' effect/state. | 1 ||
| `FaceAway` | `Number` | Applies or references the 'FaceAway' effect/state. | 1 ||
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 1 ||
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 1 ||
| [`PopAndSpawn`](#object-popandspawn) | Enum / Object | Destroys the target and replaces it with a new spawned entity. | 1 ||
| [`RemoveStatus`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'RemoveStatus' effect/state. | 1 ||
| `ScatterRandomPickups` | `Number` | Applies or references the 'ScatterRandomPickups' effect/state. | 1 ||
| `SetKnockback` | `Number` | Applies or references the 'SetKnockback' effect/state. | 1 ||
| [`UseAbility`](./Abilities_and_Spells.md#object-useability) | `String` | Forces the character or target to instantly use a specified ability. | 1 ||
| `VaporizeCorpse` | `Number` | Applies or references the 'VaporizeCorpse' effect/state. | 1 ||
| [`EventBounty`](./Enums.md) | Integer || 1 | 5 |
| [`MergeDamageInstance`](#object-mergedamageinstance) | Object || 1 ||
| [`SetAnimationAlts`](#object-setanimationalts) | Object || 1 ||

</details>

---

### Object: `Conditional_Enemy`


**Definition:** Conditional trigger: Executes nested logic if the target is hostile to the caster.  
**Total Count:** 44


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Corpse`](./Abilities_and_Spells.md#object-conditional_corpse), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 34 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 ||
| [`Confusion`](./Enums.md) | Array / Integer || 9 | [.1] |
| [`Conditional_NotBoss`](#object-conditional_notboss) | Object | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 3 ||
| [`DisplaceToAbilityTarget`](./Enums.md) | Integer || 3 | 1 |
| `TakeExtraTurn` | `Number` | Applies or references the 'TakeExtraTurn' effect/state. | 2 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer || 2 | 2 |
| [`Attraction`](./Enums.md) | Integer || 2 | 1 |
| [`Fear`](./Enums.md) | Array / Integer || 2 | [.3] |
| [`Madness`](#object-madness) | Array / Enum / Integer / Object || 2 | [.1] |
| [`Stun`](./Enums.md) | Array / Integer || 2 | [0] |
| [`Weakness`](./Enums.md) | Array / Integer || 2 | [.1] |
| [`ApplyToSource`](#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 ||
| [`ApplyToSourceOnKill`](#object-applytosourceonkill) | Object | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 1 ||
| `BonusDamage` | `Number` | Applies or references the 'BonusDamage' effect/state. | 1 ||
| `ForceMoveTowards` | `Number` | Applies or references the 'ForceMoveTowards' effect/state. | 1 ||
| [`Temporary`](#object-temporary) | Object | A wrapper object for applying status effects that automatically expire. | 1 ||
| [`Burn`](./Enums.md) | Array / Enum / Integer || 1 | [.1] |
| [`Charmed`](./Enums.md) | Array / Enum / Integer || 1 | [.1] |
| [`Conditional_FinishedSpawning`](#object-conditional_finishedspawning) | Object || 1 ||
| [`Doomed`](./Enums.md) | Integer || 1 | 3 |
| [`Hex`](./Enums.md) | Integer || 1 | 1 |
| [`Marked`](./Enums.md) | Array / Integer || 1 | [.1] |
| [`PermanentCharm`](./Enums.md) | Integer || 1 | 1 |
| [`Poison`](./Enums.md) | Array / Integer || 1 | [.1] |
| [`TempDamageUp`](./Enums.md) | Integer || 1 | 2 |

</details>

---

### Object: `Temporary`


**Definition:** A wrapper object for applying status effects that automatically expire.  
**Total Count:** 41


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate), [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_NotAlly`](./Abilities_and_Spells.md#object-conditional_notally), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 57 ||
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 56 ||
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Duration in turns. | 52 ||
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 25 ||
| `expires_on_end_turn` | Boolean || 21 ||
| `data` | Integer || 2 ||
| `expires_on_appliers_turn` | Boolean || 2 ||
| `expires_on_move` | Boolean || 1 ||

</details>

---

### Object: `sounds`


**Definition:** Audio cues triggered by the ability.  
**Total Count:** 39


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ontrigger`](./Enums.md#enum-ontrigger) | Enum || 32 ||
| [`oncast`](./Enums.md#enum-oncast) | Enum || 3 ||
| [`oncastpoint`](./Enums.md#enum-oncastpoint) | Enum || 3 ||
| [`ontrigger_intentional`](./Enums.md#enum-ontrigger_intentional) | Enum || 1 ||

</details>

---

### Object: `Conditional_Ally`


**Definition:** Conditional trigger: Executes nested logic if the target is friendly to the caster.  
**Total Count:** 37


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 28 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`DamageUp`](./Enums.md) | Integer / String || 5 | 3 |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 4 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer || 4 | 2 |
| `KnockbackDamageImmuneUntilSettled` | `Number` | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. | 3 ||
| [`Temporary`](#object-temporary) | Object | A wrapper object for applying status effects that automatically expire. | 3 ||
| [`Cleanse`](./Enums.md) | Integer || 3 | 0 |
| [`ApplyToSource`](#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 2 ||
| [`HealthGain`](./Enums.md) | Integer || 2 | 5 |
| [`RandomStatUp`](./Enums.md) | Enum / Integer || 2 | ceil(X/3) |
| [`ApplyToSourceOnKill`](#object-applytosourceonkill) | Object | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 1 ||
| `ChanceToBreak` | `Number` | Applies or references the 'ChanceToBreak' effect/state. | 1 ||
| [`Conditional_Corpse`](#object-conditional_corpse) | Object | Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 1 ||
| [`Conditional_PlayerCat`](#object-conditional_playercat) | Object | Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 1 ||
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 1 ||
| `ManaGain` | Enum / Integer | Applies or references the 'ManaGain' effect/state. | 1 ||
| `RepairAll` | `Number` | Applies or references the 'RepairAll' effect/state. | 1 ||
| [`ShowText`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ShowText' effect/state. | 1 ||
| `ThornsDamageImmuneUntilSettled` | `Number` | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. | 1 ||
| `TileDamageImmuneUntilSettled` | `Number` | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. | 1 ||
| [`BleedThorns`](./Enums.md) | Integer || 1 | 3 |
| [`Charmed`](./Enums.md) | Array / Enum / Integer || 1 | [.1] |
| [`TempDamageUp`](./Enums.md) | Integer || 1 | 2 |
| [`Thorns`](./Enums.md) | Integer || 1 | 2 |

</details>

---

### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 37


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 37 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 37 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 28 ||
| [`GainDisorderFromPool_PostCast`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 7 ||
| [`ApplyToRandomPartyMemberIfPossible`](#object-applytorandompartymemberifpossible) | Object | Redirects the nested effects to apply to a random living member of the player's party. | 1 ||
| [`ApplyToSource`](#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 ||
| [`GainDisorder`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'GainDisorder' effect/state. | 1 ||
| [`ImmediateUseAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ImmediateUseAbility' effect/state. | 1 ||
| `RefreshWeaponAbility` | `Number` | Applies or references the 'RefreshWeaponAbility' effect/state. | 1 ||
| [`ShowText`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ShowText' effect/state. | 1 ||

</details>

---

### Object: `keyword_tooltips`


**Definition:** Forces specific UI tooltips to appear when hovering over the ability.  
**Total Count:** 35


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 ||
| [`BonusAbility`](./Enums.md) | Enum || 2 | DonateEnergy |
| [`DamageUp`](./Enums.md) | Integer / String || 2 | 3 |
| [`Shield`](./Enums.md) | Enum / Integer || 2 | 2*X |
| `TemporaryItem` | Integer | Applies or references the 'TemporaryItem' effect/state. | 1 ||
| [`Bleed`](./Enums.md) | Array / Integer || 1 | [.1] |
| [`Brace`](./Enums.md) | Integer || 1 | 2 |
| [`Charmed`](./Enums.md) | Array / Enum / Integer || 1 | [.1] |
| [`Madness`](#object-madness) | Array / Enum / Integer / Object || 1 | [.1] |
| [`PermanentMadness`](./Enums.md) | Integer || 1 | 1 |
| [`RandomMagicMissile`](#object-randommagicmissile) | Integer / Object || 1 | 5 |
| [`Webbed`](./Enums.md) | Integer || 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `splash_damage`


**Definition:** Secondary Area of Effect blast parameters.  
**Total Count:** 35


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#object-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 35 ||
| [`damage`](#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 32 ||
| [`effects`](#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 17 ||
| `knockback` | Enum / Integer | Knockback force of the splash blast. | 13 ||
| [`elements`](./Arrays.md#array-elements) | Array || 13 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 12 ||
| `makes_contact` | `Boolean` || 6 ||
| `override_trample_damage` | `Boolean` || 2 ||
| `ai_base_score` | Integer || 1 ||
| `crit_chance` | `Number` || 1 ||
| `force_no_knockback` | `Boolean` || 1 ||
| `force_play_hit_animation` | `Boolean` || 1 ||
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `String` || 1 ||

</details>

---

### Object: `Conditional_Boss`


**Definition:** Conditional trigger: Executes nested logic if the target is a Boss.  
**Total Count:** 21


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 19 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [`Conditional_HasStatus`](#object-conditional_hasstatus) | Object | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 6 ||
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 4 ||
| [`RemoveStatus`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'RemoveStatus' effect/state. | 4 ||
| [`Else`](#object-else) | Object || 4 ||
| [`VisualFX`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'VisualFX' effect/state. | 3 ||
| [`Stun`](./Enums.md) | Array / Integer || 3 | [0] |
| [`BonusDamage`](./Engine_LogicKeys.md#valid-property-keys) | Enum / Integer | Applies or references the 'BonusDamage' effect/state. | 2 ||
| [`Charmed`](./Enums.md) | Array / Enum / Integer || 2 | [.1] |
| [`Drowsy`](./Enums.md) | Integer || 2 | 8 |
| [`ExplodeCharacter_PartyBoss`](./Enums.md) | Integer || 2 | 5 |
| [`ExplodeCharacter_RockCrusher_PetrifyBreak`](./Enums.md) | Integer || 2 | 5 |
| `ExplodeCharacter_NoDie` | `Number` | Applies or references the 'ExplodeCharacter_NoDie' effect/state. | 1 ||
| [`XIsTargetHealth`](#object-xistargethealth) | Object | Math variable assignment: Evaluates X as the target's current health. | 1 ||
| [`Fear`](./Enums.md) | Array / Integer || 1 | [.3] |

</details>

---

### Object: `EvolveAbilityFromPool`


**Definition:** Upgrades or transforms an existing ability into a new one from the specified pool.  
**Total Count:** 21


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `upgraded` | Boolean || 13 ||
| [`pool`](./Enums.md) | Array / Enum || 13 | [Ping] |

</details>

---

### Object: `KnockUpAndAway`


**Definition:** Displaces the target vertically and horizontally away from the source.  
**Total Count:** 21


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`Conditional_LastHit`](./Abilities_and_Spells.md#object-conditional_lasthit), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The distance in tiles to knock the target away. | 24 ||
| [`stacks`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Number of stacks or intensity to apply. | 22 ||
| `height` | Integer || 2 ||
| `circular_variance` | Integer || 1 ||

</details>

---

### Object: `additional_passives`


**Definition:** Passives granted intrinsically to a spawned entity.  
**Total Count:** 20


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#object-spawn)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 19 ||
| [`SafeDoomed`](./Enums.md) | Enum / Integer || 11 | 2 |
| [`InjuryImmunity`](./Enums.md) | Integer || 7 | 1 |
| [`AllStatsUp`](./Enums.md) | Enum / Integer || 2 | 2 |
| [`FadeInsteadOfDie`](./Enums.md) | Integer || 2 | 1 |
| [`IllusionTint`](./Enums.md) | Integer || 2 | 1 |
| [`PermanentMadness`](./Enums.md) | Integer || 2 | 1 |
| [`ApplyPassivesToSpawnerWhileAlive`](#object-applypassivestospawnerwhilealive) | Object || 1 ||
| [`CaptureFamiliar`](./Enums.md) | Integer || 1 | 1 |
| [`DamageUp`](./Enums.md) | Integer / String || 1 | 3 |
| [`FillMana`](./Enums.md) | Integer || 1 | 1 |
| [`HealthGain`](./Enums.md) | Integer || 1 | 5 |
| [`HideEquipment`](./Enums.md) | Enum || 1 | neck |
| [`ReviveNextRound`](#object-revivenextround) | Integer / Object || 1 | 2 |
| [`SchizoIllusionAIModifier`](./Enums.md) | Integer || 1 | 1 |
| [`SpeedUp`](./Enums.md) | Enum / Integer || 1 | 4 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `Conditional_HasStatus`


**Definition:** Conditional trigger: Executes nested logic if the target currently has the specified status effect.  
**Total Count:** 20


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional_boss), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 20 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 20 ||
| [`BonusDamage`](./Enums.md) | Enum / Integer || 6 | -4 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`ApplyToSource`](#object-applytosource) | Object || 3 ||
| [`Burn`](./Enums.md) | Array / Enum / Integer || 2 | [.1] |
| [`RemoveStatus`](./Enums.md) | Enum || 2 | Sleep |
| [`Slow`](./Enums.md) | Array / Enum / Integer || 2 | [.1] |
| [`Confusion`](./Enums.md) | Array / Integer || 1 | [.1] |
| [`Fear`](./Enums.md) | Array / Integer || 1 | [.3] |
| [`FormChange`](#object-formchange) | Enum / Object || 1 | Open |
| [`Quivered`](./Enums.md) | Integer || 1 | 1 |

</details>

---

### Object: `RandomStatusFromPool`


**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 19


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyMultipleTimes`](./Abilities_and_Spells.md#object-applymultipletimes), [`Conditional_CanBeHealed`](./Abilities_and_Spells.md#object-conditional_canbehealed), [`Conditional_HasCleansableDebuffs`](./Abilities_and_Spells.md#object-conditional_hascleansabledebuffs), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 33 ||
| [`Shield`](./Enums.md) | Enum / Integer || 12 | 2*X |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 12 |
| [`Thorns`](./Enums.md) | Integer || 10 | 2 |
| [`DivineShield`](./Enums.md) | Integer || 9 | 2 |
| [`KineticSpikes`](./Enums.md) | Integer || 9 | 2 |
| [`Poison`](./Enums.md) | Array / Integer || 9 | [.1] |
| [`Bleed`](./Enums.md) | Array / Integer || 8 | [.1] |
| [`Charge`](./Enums.md) | Integer || 8 | 2 |
| [`Weakness`](./Enums.md) | Array / Integer || 8 | [.1] |
| [`Slow`](./Enums.md) | Array / Enum / Integer || 7 | [.1] |
| [`Blind`](./Enums.md) | Array / Integer || 6 | [2] |
| [`Brace`](./Enums.md) | Integer || 6 | 2 |
| [`Bruise`](./Enums.md) | Array / Integer || 6 | [.1] |
| [`DiminishingHealthRegen`](./Enums.md) | Integer || 6 | 3 |
| [`GainCoins`](./Enums.md) | Integer || 6 | 2 |
| [`AllStatsUp`](./Enums.md) | Enum / Integer || 5 | 2 |
| [`Burn`](./Enums.md) | Array / Enum / Integer || 5 | [.1] |
| [`MoveQuivered`](./Enums.md) | Integer || 5 | 1 |
| [`Quivered`](./Enums.md) | Integer || 5 | 1 |
| [`RandomStatUp`](./Enums.md) | Enum / Integer || 5 | ceil(X/3) |
| [`BleedThorns`](./Enums.md) | Integer || 4 | 3 |
| [`ConstitutionUp`](./Enums.md) | Array / Enum / Integer || 4 | [.5] |
| [`Madness`](#object-madness) | Array / Enum / Integer / Object || 4 | [.1] |
| [`MagicWeakness`](./Enums.md) | Array / Integer || 4 | [.1] |
| [`Marked`](./Enums.md) | Array / Integer || 4 | [.1] |
| [`Reflect`](./Enums.md) | Integer || 4 | 5 |
| [`SpeedUp`](./Enums.md) | Enum / Integer || 4 | 4 |
| [`Stun`](./Enums.md) | Array / Integer || 4 | [0] |
| [`Tarred`](./Enums.md) | Array / Integer || 4 | [.1] |
| [`Charmed`](./Enums.md) | Array / Enum / Integer || 3 | [.1] |
| [`Confusion`](./Enums.md) | Array / Integer || 3 | [.1] |
| [`DamageUp`](./Enums.md) | Integer / String || 3 | 3 |
| [`Fear`](./Enums.md) | Array / Integer || 3 | [.3] |
| [`Freeze`](./Enums.md) | Array / Integer || 3 | [.1] |
| [`Immobile`](./Enums.md) | Array / Integer || 3 | [.1] |
| [`Petrify`](./Enums.md) | Array / Integer || 3 | [.15] |
| [`Sleep`](./Enums.md) | Array / Integer || 3 | [.1] |
| [`StrengthUp`](./Enums.md) | Enum / Integer || 3 | max(int, 0) |
| [`BackflipWhenTargeted`](#object-backflipwhentargeted) | Integer / Object || 2 | 2 |
| [`BonusDamage`](./Enums.md) | Enum / Integer || 2 | -4 |
| [`CharismaUp`](./Enums.md) | Enum / Integer || 2 | -2 |
| [`CritChanceUp`](./Enums.md) | Integer || 2 | 2 |
| [`DexterityUp`](./Enums.md) | Enum / Integer || 2 | 2 |
| [`DodgeChance_Status`](./Enums.md) | Integer || 2 | 50 |
| [`FormChange`](#object-formchange) | Enum / Object || 2 | Open |
| [`HealthRegenUp`](./Enums.md) | Integer || 2 | 2 |
| [`IntelligenceUp`](./Enums.md) | Enum / Integer || 2 | item_aux |
| [`Lifesteal`](./Enums.md) | Integer || 2 | 3 |
| [`LuckUp`](./Enums.md) | Enum / Integer || 2 | 2 |
| [`PoisonLace`](./Enums.md) | Enum / Integer || 2 | X/3 |
| [`RandomStatDown`](./Enums.md) | Array / Enum / Integer || 2 | [.25] |
| [`Rot`](./Enums.md) | Array / Integer || 2 | [.1] |
| [`SpellDamageUp`](./Enums.md) | Integer || 2 | 3 |
| [`TempCounterAttack`](./Enums.md) | Integer || 2 | 1 |
| [`DelayedPain`](./Enums.md) | Integer || 1 | 1 |
| [`Hex`](./Enums.md) | Integer || 1 | 1 |
| [`IncAuxCounterClamped`](#object-incauxcounterclamped) | Object || 1 ||
| [`Infested`](./Enums.md) | Integer || 1 | 1 |
| [`ManaGain`](./Enums.md) | Enum / Integer || 1 | 0 |
| [`Ostracized`](./Enums.md) | Integer || 1 | 2 |
| [`RefreshActPoints`](./Enums.md) | Integer || 1 | 1 |
| [`RefreshMovePoints`](./Enums.md) | Integer || 1 | 1 |
| [`Scrambled`](./Enums.md) | Integer || 1 | 2 |

</details>

---

### Object: `Consumed`


**Definition:** State object triggered when this object or entity is eaten/consumed by another character.  
**Total Count:** 18


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#object-conditional_buddy), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#object-conditional_livingplayercat), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 22 ||
| [`struggle_ability`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Ability triggered by the consumed entity while inside the consumer. | 17 ||
| `force_contact` | `Boolean` | If true, enforces physical overlap. | 15 ||
| `instant` | `Boolean` || 12 ||
| [`mount_mode`](./Engine_LogicKeys.md#valid-property-keys) | `String` | If true, treats the consumption as riding/mounting instead of eating. | 12 ||
| `do_not_pop_corpse` | `Boolean` || 11 ||
| [`drop_on_death`](./Engine_LogicKeys.md#valid-property-keys) | `String` || 11 ||
| `wet` | `Boolean` || 8 ||
| `drop_on_self_death` | `Boolean` || 3 ||
| [`extra_statuses`](#object-extra_statuses) | Object | Additional generic status applications. | 3 ||
| `use_placeholder` | Boolean || 3 ||
| [`drop_body_ability`](./Engine_LogicKeys.md#valid-property-keys) | `String` || 1 ||
| `kill_on_consume` | `Boolean` || 1 ||

</details>

---

### Object: `Conditional_NotBoss`


**Definition:** Conditional trigger: Executes nested logic if the target is NOT a Boss.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 13 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`CaptureFamiliar`](./Enums.md) | Integer || 2 | 1 |
| [`Doomed`](./Enums.md) | Integer || 2 | 3 |
| [`ExplodeCharacter_RockCrusher`](./Enums.md) | Integer || 2 | 5 |
| [`FactionConversion`](./Enums.md) | Integer || 2 | 1 |
| [`Vaporize`](./Enums.md) | Integer || 2 | 20 |
| [`VaporizeInanimate`](./Enums.md) | Integer || 2 | 1 |
| [`CanApplyToInanimate`](#object-canapplytoinanimate) | Object || 1 ||
| [`Conditional_HealthThreshold`](#object-conditional_healththreshold) | Object || 1 ||
| [`Fear`](./Enums.md) | Array / Integer || 1 | [.3] |
| [`PermanentCharm`](./Enums.md) | Integer || 1 | 1 |

</details>

---

### Object: `FormChange`


**Definition:** Transforms the character into a different state or form (e.g., Rage, HasCat).  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form`](./Engine_LogicKeys.md#valid-property-keys) | Mixed || 75 ||
| [`chance`](./Enums.md) | Number || 1 | .02 |

</details>

---

### Object: `ApplyToSourceOnKill`


**Definition:** Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action.  
**Total Count:** 15


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 13 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`RemoveItem`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'RemoveItem' effect/state. | 2 ||
| [`CompleteItemQuest`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'CompleteItemQuest' effect/state. | 2 ||
| `ManaGain` | `Number` | Applies or references the 'ManaGain' effect/state. | 2 ||
| [`AlphaCat`](./Enums.md) | Integer || 2 | 1 |
| [`HealthGain`](./Enums.md) | Integer || 2 | 5 |
| [`Revive`](./Enums.md) | Integer || 2 | 50 |
| [`EvolveAbilityFromPool`](./Abilities_and_Spells.md#object-evolveabilityfrompool) | `String` | Upgrades or transforms an existing ability into a new one from the specified pool. | 1 ||
| `RefreshActPoints` | `Number` | Applies or references the 'RefreshActPoints' effect/state. | 1 ||
| `TakeExtraTurn` | `Number` | Applies or references the 'TakeExtraTurn' effect/state. | 1 ||
| [`TransformWeapon`](#object-transformweapon) | Object | Transforms the equipped weapon into another specific weapon state. | 1 ||
| [`WeaponAuxMultiplier`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'WeaponAuxMultiplier' effect/state. | 1 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer || 1 | 2 |
| [`StrengthUp`](./Enums.md) | Enum / Integer || 1 | max(int, 0) |

</details>

---

### Object: `CanApplyToInanimate`


**Definition:** Modifier object that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters.  
**Total Count:** 15


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional_notboss), [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional_object), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [`BreakIntoRocks`](./Enums.md#enum-breakintorocks) | Enum | Applies or references the 'BreakIntoRocks' effect/state. | 4 ||
| [`ObjectOnHitCharacter`](#object-objectonhitcharacter) | Enum / Object || 4 | SkeletonCatFamiliar |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`ApplyToSource`](#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 ||
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 3 ||
| `GetAggroTarget` | Integer | Applies or references the 'GetAggroTarget' effect/state. | 2 ||
| `PreventDeathTransforms` | Integer | Applies or references the 'PreventDeathTransforms' effect/state. | 1 ||
| [`Temporary`](#object-temporary) | Object | A wrapper object for applying status effects that automatically expire. | 1 ||

</details>

---

### Object: `CatPartsTransform`


**Definition:** Transforms specific body parts into different visual variants.  
**Total Count:** 14


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`palette`](./Enums.md) | Integer || 17 | 6 |
| `ear1` | Integer | Sprite variant ID for the front ear. | 13 ||
| [`tail`](./Enums.md) | Integer || 13 | 1042 |
| [`arm2`](./Enums.md) | Number || 11 | 1013 |
| `ear2` | Integer || 10 ||
| [`arm1`](./Enums.md) | Number || 10 | 1013 |
| [`leg1`](./Enums.md) | Integer || 8 | 338 |
| [`leg2`](./Enums.md) | Integer || 8 | 338 |
| [`mouth`](./Enums.md) | Number || 8 | 1005 |
| [`head`](./Enums.md) | Integer || 6 | 12 |
| [`texture`](./Enums.md) | Integer || 6 | 1008 |
| [`body`](./Enums.md) | Number || 5 | 1029 |
| `eye1` | Integer || 3 ||
| `eye2` | Integer || 3 ||
| `eyebrow1` | Integer || 1 ||
| `eyebrow2` | Integer || 1 ||

</details>

---

### Object: `RandomMagicMissile`


**Definition:** No definition provided.  
**Total Count:** 13


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `full_size` | Boolean | If true, fires normal sized missiles instead of mini ones. | 2 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 2 ||

</details>

---

### Object: `ChangeTile`


**Definition:** Transforms the terrain tile under the target.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tile`](./Enums.md) | Array / Enum || 12 | [BrambleTile] |
| `aoe` | Integer || 2 ||
| [`chance`](./Enums.md) | Number || 2 | .02 |

</details>

---

### Object: `Conditional_Speculative`


**Definition:** A simulation object used by the AI to test hypothetical outcomes before committing to an action.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_AffectedByElement`](./Abilities_and_Spells.md#object-conditional_affectedbyelement), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| `IgnoreDamage` | `Number` | Applies or references the 'IgnoreDamage' effect/state. | 3 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| `BonusDamageBasedOnDistance` | `Number` | Applies or references the 'BonusDamageBasedOnDistance' effect/state. | 2 ||
| [`Conditional_HealthThreshold`](#object-conditional_healththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 2 ||
| `BonusDamage` | Enum / Integer | Applies or references the 'BonusDamage' effect/state. | 1 ||
| `CapDamage` | `Number` | Applies or references the 'CapDamage' effect/state. | 1 ||
| `RandomBonusDamage` | `Number` | Applies or references the 'RandomBonusDamage' effect/state. | 1 ||
| [`Else`](#object-else) | Object || 1 ||
| [`Knockback`](./Enums.md) | Integer || 1 | 5 |

</details>

---

### Object: `DoScreenShake`


**Definition:** Triggers a camera screen shake effect.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#object-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intensity` | Integer || 10 ||
| [`time`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Mixed || 10 ||

</details>

---

### Object: `ChanceToBreakFree`


**Definition:** Provides a probability to escape a grapple or restraining effect.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md) | Enum || 11 | MoonHandDrop |
| [`fail_ability`](./Enums.md#enum-fail_ability) | Enum | The ability triggered if the break free attempt fails. | 3 ||
| `stacks` | Enum / Integer | Percentage base chance to break free. | 3 ||

</details>

---

### Object: `Cleave`


**Definition:** No definition provided.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `Conditional_Corpse`


**Definition:** Conditional trigger: Executes nested logic if the target is a dead body/corpse.  
**Total Count:** 11


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 ||
| [`Revive`](./Enums.md) | Integer || 7 | 50 |
| `TakeExtraTurn` | Integer | Applies or references the 'TakeExtraTurn' effect/state. | 2 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer || 2 | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Conditional_Enemy`](#object-conditional_enemy) | Object | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 1 ||
| `FlatAIBonus` | `Number` | Applies or references the 'FlatAIBonus' effect/state. | 1 ||
| [`HealRandomInjury`](./Enums.md) | Integer || 1 | 1 |
| [`PermanentCharm`](./Enums.md) | Integer || 1 | 1 |

</details>

---

### Object: `ApplyPassives`


**Definition:** Grants the nested passive abilities dynamically.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_RandomChance`](./Abilities_and_Spells.md#object-conditional_randomchance), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 13 ||
| [`StatusOnBattleEnd`](#object-statusonbattleend) | Object || 5 ||
| [`AddTag`](./Enums.md) | Enum || 2 | squirrel |
| [`Flying`](./Enums.md) | Integer || 2 | 1 |
| [`IgnoreTiles`](./Enums.md) | Integer || 2 | 1 |
| [`YOffset`](./Enums.md) | Number || 2 | .25 |
| [`ElementImmune`](./Enums.md) | Enum || 1 | Creep |
| [`KnockbackImmunity`](./Enums.md) | Integer || 1 | 1 |
| [`Plant`](./Enums.md) | Integer || 1 | 1 |
| [`ReplaceBasicAttack`](./Enums.md) | Enum || 1 | BasicPuke |

</details>

---

### Object: `Conditional_FormulaIsPositive`


**Definition:** Conditional trigger: Executes nested logic if the evaluated mathematical formula returns a value greater than 0.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 9 |
| [`formula`](./Math_Equations.md) | Equation | The math expression to evaluate. | 8 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`Burn`](./Enums.md) | Array / Enum / Integer || 2 | [.1] |
| [`Immobile`](./Enums.md) | Array / Integer || 2 | [.1] |
| [`Shield`](./Enums.md) | Enum / Integer || 2 | 2*X |
| [`OverrideKnockbackDamage`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'OverrideKnockbackDamage' effect/state. | 1 ||
| [`Freeze`](./Enums.md) | Array / Integer || 1 | [.1] |
| [`Slow`](./Enums.md) | Array / Enum / Integer || 1 | [.1] |
| [`SpeedUp`](./Enums.md) | Enum / Integer || 1 | 4 |
| [`Stun`](./Enums.md) | Array / Integer || 1 | [0] |

</details>

---

### Object: `Craft`


**Definition:** Synthesizes or spawns a new item from a specific pool.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md) | Array / Enum || 15 | [Ping] |
| [`slot`](./Enums.md#enum-slot) | Enum / Integer || 14 ||
| `temporary` | Boolean || 4 ||
| `works_with_tech` | Boolean || 4 ||

</details>

---

### Object: `Conditional_BadRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized bad outcome probability.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Number | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 8 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| `DieViolently` | `Number` | Applies or references the 'DieViolently' effect/state. | 1 ||
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 1 ||

</details>

---

### Object: `Conditional_FirstApplicationThisTurn`


**Definition:** Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. | 3 ||
| [`TempPassiveWhileHasStatus`](#object-temppassivewhilehasstatus) | Object | Grants nested passives only while the character possesses the specified status. | 3 ||

</details>

---

### Object: `ApplyStatusIfCrit`


**Definition:** Conditional trigger: Executes the nested logic only if the triggering action was a critical hit.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |
| [`ApplyToSource`](#object-applytosource) | Object || 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`Bleed`](./Enums.md) | Array / Integer || 3 | [.1] |
| [`LuckUp`](./Enums.md) | Enum / Integer || 1 | 2 |

</details>

---

### Object: `Conditional_HealthThreshold`


**Definition:** Conditional trigger: Executes nested logic if the target's health falls below the specified threshold.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional_notboss), [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional_speculative), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| `threshold_flat` | Integer | A flat numerical health value threshold. | 5 ||
| [`SpawnThingIfHitKills`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'SpawnThingIfHitKills' effect/state. | 2 ||
| `threshold_percent` | Integer | A percentage-based health threshold (e.g. 50%). | 2 ||
| [`ApplyToSource`](#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 ||
| [`BonusDamage`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'BonusDamage' effect/state. | 1 ||
| `CaptureFamiliar` | `Number` | Applies or references the 'CaptureFamiliar' effect/state. | 1 ||
| `Die` | `Number` | Applies or references the 'Die' effect/state. | 1 ||
| `DieViolently` | `Number` | Applies or references the 'DieViolently' effect/state. | 1 ||
| `FactionConversion` | `Number` | Applies or references the 'FactionConversion' effect/state. | 1 ||
| `FlatLeech` | `Number` | Applies or references the 'FlatLeech' effect/state. | 1 ||
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 1 ||
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 1 ||
| [`threshold_expr`](./Math_Equations.md) | Equation || 1 ||
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 1 ||

</details>

---

### Object: `Conditional_InForm`


**Definition:** Conditional trigger: Executes nested logic if the target is currently in the specified transformation form.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#object-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum / Integer | The specific form ID to check for. | 7 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | `String` | Transforms the character into a different state or form (e.g., Rage, HasCat). | 5 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`ForceImmediateMoveAndAttack`](#object-forceimmediatemoveandattack) | Object | Forces the character to immediately move to a target and use a specified ability. | 1 ||
| [`UseAbility`](./Abilities_and_Spells.md#object-useability) | `String` | Forces the character or target to instantly use a specified ability. | 1 ||
| [`CritChanceUp`](./Enums.md) | Integer || 1 | 2 |
| [`DamageUp`](./Enums.md) | Integer / String || 1 | 3 |
| [`DodgeChance_Status`](./Enums.md) | Integer || 1 | 50 |
| [`SpeedUp`](./Enums.md) | Enum / Integer || 1 | 4 |

</details>

---

### Object: `Conditional_PlayerCat`


**Definition:** Conditional trigger: Executes nested logic if the target is a player-controlled cat.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| `ConjureRandomAbilityFromCat` | `Number` | Applies or references the 'ConjureRandomAbilityFromCat' effect/state. | 2 ||
| [`ApplyToSource`](#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 ||
| `GenericDebuff` | `Number` | Applies or references the 'GenericDebuff' effect/state. | 1 ||
| [`KnockOutClone`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'KnockOutClone' effect/state. | 1 ||
| `T2CopyCat` | `Number` | Applies or references the 'T2CopyCat' effect/state. | 1 ||
| [`Adrenaline`](./Enums.md) | Integer || 1 | 10 |
| [`Cleanse`](./Enums.md) | Integer || 1 | 0 |
| [`Scrambled`](./Enums.md) | Integer || 1 | 2 |

</details>

---

### Object: `ForceAttack`


**Definition:** No definition provided.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `immediate` | Boolean || 2 ||

</details>

---

### Object: `BackflipWhenTargeted`


**Definition:** No definition provided.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 7 ||
| [`ability`](./Enums.md) | Enum || 7 | MoonHandDrop |

</details>

---

### Object: `Conditional_IsSelf`


**Definition:** Conditional trigger: Executes nested logic if the target is the caster themselves.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `Conditional_Object`


**Definition:** Conditional trigger: Executes nested logic if the target is an inanimate object or furniture.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_HasTag`](#object-conditional_hastag) | Object | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 3 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`Else`](#object-else) | Object || 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`CanApplyToInanimate`](#object-canapplytoinanimate) | Object | Modifier object that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 1 ||
| [`RepairWeapon`](./Enums.md) | Integer || 1 | 99 |

</details>

---

### Object: `DoDistortionRing`


**Definition:** Creates a visual distortion ring effect on the screen.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intensity` | Integer || 6 ||
| `radius` | Array / Integer | Distance or area of effect in tiles. | 6 ||
| [`speed`](./Enums.md) | Array / Number || 6 | [1.0] |

</details>

---

### Object: `Metronome`


**Definition:** No definition provided.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||
| [`banned_abilities`](./Arrays.md#array-banned_abilities) | Array || 1 ||

</details>

---

### Object: `ObjectOnHitCharacter`


**Definition:** No definition provided.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `SwitchMusic`


**Definition:** Changes the background music track or layer during combat.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#object-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | The specific audio layer to transition to (e.g., map, battle). | 7 ||
| [`new_song`](./Enums.md#enum-new_song) | Enum | The ID of the new music track. | 6 ||
| `crossfade_speed` | Integer || 1 ||

</details>

---

### Object: `TwisterDisplaceWithDamage`


**Definition:** A whirlwind effect that randomly displaces targets and deals damage.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Abilities_and_Spells.md#object-damage) | Mixed | The damage formula or inherit flag. | 6 ||
| `max_dist` | Integer | Maximum displacement distance. | 6 ||
| `min_dist` | Integer | Minimum displacement distance. | 2 ||
| [`exclude_prefix`](./Enums.md#enum-exclude_prefix) | Enum || 1 ||

</details>

---

### Object: `CollectsPickupsWithAltEffects`


**Definition:** Triggers alternative nested effects when collecting items or pickups.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`Tech`](./Enums.md) | Integer || 2 | 3 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `CurrentWeaponAddPoison` | Integer | Applies or references the 'CurrentWeaponAddPoison' effect/state. | 1 ||
| [`LuckUp`](./Enums.md) | Enum / Integer || 1 | 2 |
| [`Quivered`](./Enums.md) | Integer || 1 | 1 |
| [`RandomStatUp`](./Enums.md) | Enum / Integer || 1 | ceil(X/3) |
| [`Shield`](./Enums.md) | Enum / Integer || 1 | 2*X |

</details>

---

### Object: `Conditional_Shielded`


**Definition:** Conditional trigger: Executes nested logic if the target currently has a Shield status.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 2 | |

</details>

---

### Object: `damage`


**Definition:** The base damage properties of an attack.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 1 ||

</details>

---

### Object: `DestroyEquipmentAndAttachParasite`


**Definition:** Removes an equipped item and replaces it with a parasite from a specified pool.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_ActiveWeather_Any`](./Abilities_and_Spells.md#object-conditional_activeweather_any), [`Conditional_DebuffRoll`](./Abilities_and_Spells.md#object-conditional_debuffroll), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `DoDamage`


**Definition:** Explicitly triggers a secondary damage instance independent of the main attack.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`Else`](./Abilities_and_Spells.md#object-else), [`post_spawn_statuses`](./Abilities_and_Spells.md#object-post_spawn_statuses)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](#object-damage) | Enum / Integer / Object | The flat damage amount. | 7 ||
| [`type`](./Enums.md#enum-type) | Enum | The classification of the damage (e.g., spell, melee). | 7 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 ||
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum || 4 ||
| [`effects`](#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 4 ||
| [`elements`](./Arrays.md#array-elements) | Array || 2 ||

</details>

---

### Object: `ObjectOnHit`


**Definition:** Spawns a specific physics/item object upon impact.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `ApplyToConsumed`


**Definition:** Redirects the nested effects to apply to the entity that just consumed this object.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DeleteObject` | `Number` | Applies or references the 'DeleteObject' effect/state. | 3 ||
| `Die` | `Number` | Applies or references the 'Die' effect/state. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `ArcLightning`


**Definition:** Executes a chain-lightning logic block that bounces between targets.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, the arc will not bounce to friendly targets. | 4 ||
| `max_distance` | Integer | The maximum tile range the lightning can jump between bounces. | 4 ||
| `stacks` | Enum / Integer | The maximum number of targets the lightning can bounce to. | 4 ||
| `ignore_self` | Boolean | If true, prevents the arc from bouncing back to the caster. | 1 ||
| [`chance`](./Enums.md) | Number || 1 | .02 |

</details>

---

### Object: `Conditional_Familiar`


**Definition:** Conditional trigger: Executes nested logic if the target is a familiar.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`DamageUp`](./Enums.md) | Integer / String || 2 | 3 |
| [`AllStatsUp`](./Enums.md) | Enum / Integer || 1 | 2 |
| [`BonusDamage`](./Enums.md) | Enum / Integer || 1 | -4 |
| [`DivineShield`](./Enums.md) | Integer || 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `Conditional_OncePerBattle`


**Definition:** Conditional trigger: Executes nested logic only once per encounter/battle.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`key`](./Enums.md#enum-key) | Enum || 3 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`CompleteItemQuest`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'CompleteItemQuest' effect/state. | 2 ||
| `TriggerGameEnding` | `Number` | Applies or references the 'TriggerGameEnding' effect/state. | 2 ||

</details>

---

### Object: `Conditional_RandomChance`


**Definition:** Conditional trigger: Executes nested logic based on a flat percentage random roll.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 4 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`ApplyPassives`](#object-applypassives) | Object | Grants the nested passive abilities dynamically. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||

</details>

---

### Object: `extra_statuses`


**Definition:** Additional generic status applications.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Consumed`](./Abilities_and_Spells.md#object-consumed)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`Burn`](./Enums.md) | Array / Enum / Integer || 1 | [.1] |
| [`Poison`](./Enums.md) | Array / Integer || 1 | [.1] |
| [`Tarred`](./Enums.md) | Array / Integer || 1 | [.1] |

</details>

---

### Object: `GainCoinsRange`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | Maximum coins granted. | 11 ||
| `min` | Integer | Minimum coins granted. | 11 ||

</details>

---

### Object: `LateStatusApplication`


**Definition:** Applies a status effect after all primary damage and effects have fully resolved.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `LeaveBehind`


**Definition:** Spawns a specific object at the character's previous location when they move.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#object-temporary_effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `post_spawn_statuses`


**Definition:** Status effects applied immediately after an entity spawns.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#object-spawn)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`DoDamage`](#object-dodamage) | Object | Explicitly triggers a secondary damage instance independent of the main attack. | 2 ||
| [`EnterMount`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'EnterMount' effect/state. | 1 ||
| [`VisualFXTile`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'VisualFXTile' effect/state. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---

### Object: `ReplaceSpell`


**Definition:** Replaces a spell in the character's hand/deck with a different one.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#object-temppassivewhilehasstatus)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `slot` | Enum / Integer | The spell slot index to replace. | 4 ||
| [`ability`](./Enums.md) | Enum || 4 | MoonHandDrop |

</details>

---

### Object: `ReviveNextRound`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#object-additional_passives), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `revive_health` | Integer | The flat amount of health to revive with. | 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`Shield`](./Enums.md) | Enum / Integer || 3 | 2*X |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 2 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer || 2 | 2 |
| [`DivineShield`](./Enums.md) | Integer || 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `rocket_swirl`


**Definition:** Visual parameters for swirling projectile paths.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#object-graphics)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`radius`](./Arrays.md#array-radius) | Array / Integer | Swirl radius. | 4 ||
| [`speed`](./Enums.md) | Array / Number || 4 | [1.0] |

</details>

---

### Object: `TakeBonusTurnWithStatus`


**Definition:** Grants the character an immediate extra turn while afflicted with specific statuses.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`Madness`](#object-madness) | Array / Enum / Integer / Object || 3 | [.1] |
| [`Stun`](./Enums.md) | Array / Integer || 2 | [0] |
| [`TempNoManaRegen`](./Enums.md) | Integer || 2 | 1 |
| [`Confusion`](./Enums.md) | Array / Integer || 1 | [.1] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `TempPassiveWhileHasStatus`


**Definition:** Grants nested passives only while the character possesses the specified status.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_FirstApplicationThisTurn`](./Abilities_and_Spells.md#object-conditional_firstapplicationthisturn), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#object-conditional_livingplayercat)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`status`](./Enums.md#enum-status) | Enum | The required status effect. | 3 ||
| [`MeleeRevengeDamage`](#object-meleerevengedamage) | Object || 2 ||
| [`AddManaRegen`](./Enums.md) | Integer || 1 | 5 |
| [`HealthRegenUp`](./Enums.md) | Integer || 1 | 2 |
| [`ReplaceSpell`](#object-replacespell) | Object || 1 ||

</details>

---

### Object: `TimeDelayStatusApplication`


**Definition:** Delays the nested effects by a specified amount of real-time seconds.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`delay`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Mixed | The float time delay in seconds. | 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`SwitchMusic`](#object-switchmusic) | Object | Changes the background music track or layer during combat. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`DoScreenShake`](#object-doscreenshake) | Integer / Object | Triggers a camera screen shake effect. | 1 ||
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | `String` | Transforms the character into a different state or form (e.g., Rage, HasCat). | 1 ||
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 1 ||
| [`GlobalSpawnCharacter`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'GlobalSpawnCharacter' effect/state. | 1 ||
| `PlayBackground` | `Number` | Applies or references the 'PlayBackground' effect/state. | 1 ||
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 1 ||
| [`Cleanse`](./Enums.md) | Integer || 1 | 0 |
| [`CreateGlobalModifiers`](#object-createglobalmodifiers) | Object || 1 ||
| [`RemoveAmbientLightEffects`](./Enums.md) | Number || 1 | .5 |

</details>

---

### Object: `ApplyMultipleTimes`


**Definition:** A loop object that executes its nested logic multiple times.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stacks`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | The number of times the nested effects block should be repeatedly executed. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`RandomStatusFromPool`](#object-randomstatusfrompool) | Object || 3 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `BounceObject`


**Definition:** Spawns a physics object that visually bounces off the target.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`obj`](./Enums.md#enum-obj) | Array / Enum | The entity ID of the object to spawn (e.g., chapter_corpse_medium). | 3 ||
| [`chance`](./Enums.md) | Number || 2 | .02 |
| `slide` | Integer || 1 ||

</details>

---

### Object: `CatPartsSizeScaleStatus`


**Definition:** Visually scales specific body parts of a character.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `Conditional_AffectedByElement`


**Definition:** Conditional trigger: Executes nested logic if the target is currently afflicted by the specified element.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type to check for. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`BonusCritChance`](./Enums.md) | Integer || 2 | 100 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Burn`](./Enums.md) | Array / Enum / Integer || 1 | [.1] |
| [`Conditional_Speculative`](#object-conditional_speculative) | Object || 1 ||

</details>

---

### Object: `Conditional_LastHit`


**Definition:** Conditional trigger: Executes nested logic if this attack is the final hit of a multi-hit sequence.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](#object-knockupandaway) | Object | Displaces the target vertically and horizontally away from the source. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| `BonusDamage` | `Number` | Applies or references the 'BonusDamage' effect/state. | 1 ||
| [`DelayCastAbility`](./Abilities_and_Spells.md#object-delaycastability) | `String` | Queues an ability to be cast automatically after a certain delay or trigger. | 1 ||
| [`Bruise`](./Enums.md) | Array / Integer || 1 | [.1] |

</details>

---

### Object: `DustOnHit`


**Definition:** Spawns a specific particle or cloud object upon impact.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `IncAuxCounterClamped`


**Definition:** Increments a generic auxiliary counter on the character, capped by a maximum value.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `change` | Integer || 3 ||
| `max` | Integer || 3 ||

</details>

---

### Object: `SetCrazyEyeBackgroundWeights`


**Definition:** Adjusts visual rendering weights for the 'Crazy Eye' background effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Arrays.md#array-weights) | Array / Enum || 3 ||

</details>

---

### Object: `StatusOnBattleEnd`


**Definition:** Applies the nested status effects when the encounter finishes.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./Abilities_and_Spells.md#object-applypassives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 52 ||
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 25 ||
| [`RandomMutation`](./Enums.md) | Integer || 9 | 3 |
| [`RandomTaggedMutation`](./Enums.md) | Enum || 2 | bird |

</details>

---

### Object: `Tangled`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_art`](./Enums.md#enum-alt_art) | Enum | The alternative sprite art to use while tangled. | 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||

</details>

---

### Object: `AddStatusToBasicAttack`


**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhileNotTakingTurn`](./Abilities_and_Spells.md#object-passivewhilenottakingturn), [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 205 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 56 |
| [`Bleed`](./Enums.md) | Array / Integer || 30 | [.1] |
| [`Bruise`](./Enums.md) | Array / Integer || 12 | [.1] |

</details>

---

### Object: `AfterImage`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#object-temporary_effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `skilltemp` | Boolean | If true, the decoy is automatically destroyed once the skill finishes executing. | 2 ||
| [`object`](./Enums.md) | Array / Enum || 2 | [TallSkeletonCat] |

</details>

---

### Object: `ApplyToRandomPartyMemberIfPossible`


**Definition:** Redirects the nested effects to apply to a random living member of the player's party.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional_goodroll), [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GainDisorderFromPool_PostCast`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---

### Object: `ApplyToTile`


**Definition:** Redirects the nested effects to apply to the terrain/tile underneath the target rather than the target itself.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_DestructibleCorpse`](./Abilities_and_Spells.md#object-conditional_destructiblecorpse)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ObjectOnHit`](./Abilities_and_Spells.md#object-objectonhit) | `String` | Spawns a specific physics/item object upon impact. | 2 ||
| `SpawnBearTrap` | `Number` | Applies or references the 'SpawnBearTrap' effect/state. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `AutocastEachRound`


**Definition:** Forces the character to automatically cast a specific ability at the start of each combat round.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md) | Enum || 9 | MoonHandDrop |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 6 ||

</details>

---

### Object: `BodyGuard`


**Definition:** Protects an ally by intercepting attacks directed at them.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 2 ||
| [`ability`](./Enums.md) | Enum || 2 | MoonHandDrop |

</details>

---

### Object: `Conditional_BossOrBig`


**Definition:** Conditional trigger: Executes nested logic if the target is a Boss or has a large size classification.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 0 | |

</details>

---

### Object: `Conditional_Buddy`


**Definition:** Conditional trigger: Executes nested logic if the target is the caster's summoned buddy/familiar.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Conditional_InForm`](#object-conditional_inform) | Object || 1 ||
| [`Consumed`](#object-consumed) | Object || 1 ||
| [`Else`](#object-else) | Object || 1 ||

</details>

---

### Object: `Conditional_DestructibleCorpse`


**Definition:** Conditional trigger: Executes nested logic if the target is a corpse that can be destroyed or vaporized.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ApplyToTile`](#object-applytotile) | Object | Redirects the nested effects to apply to the terrain/tile underneath the target rather than the target itself. | 2 ||
| `VaporizeCorpse` | `Number` | Applies or references the 'VaporizeCorpse' effect/state. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `Conditional_Displaceable`


**Definition:** Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`LaunchOffScreen`](./Enums.md) | String || 1 | 10+bonus_melee_ability_damage |
| [`LaunchOffScreenInstakill`](./Enums.md) | Integer || 1 | 1 |
| [`TempInitiativeChange`](./Enums.md) | Integer || 1 | -100 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `Conditional_HasCleansableDebuffs`


**Definition:** Conditional trigger: Executes nested logic if the target currently has negative status effects that can be cleansed.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| `GenericBuff` | `Number` | Applies or references the 'GenericBuff' effect/state. | 1 ||
| [`RandomStatusFromPool`](#object-randomstatusfrompool) | Object | Selects and applies a random status effect from the provided nested block. | 1 ||
| [`PartialCleanse`](./Enums.md) | Integer || 1 | 9999 |

</details>

---

### Object: `Conditional_NotAlly`


**Definition:** Conditional trigger: Executes nested logic if the target is NOT friendly to the caster.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`Confusion`](./Enums.md) | Array / Integer || 1 | [.1] |
| [`Temporary`](#object-temporary) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `Conditional_NotBossOrBig`


**Definition:** Conditional trigger: Executes nested logic if the target is NEITHER a Boss nor large.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 0 | |

</details>

---

### Object: `Conditional_NotShielded`


**Definition:** Conditional trigger: Executes nested logic if the target does NOT currently have a Shield status.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`Knockback`](./Enums.md) | Integer || 2 | 5 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 0 | |

</details>

---

### Object: `ConjureBonusAbility`


**Definition:** Adds a temporary bonus ability to the character's hand/deck.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `upgraded` | Boolean | If true, conjures the upgraded version of the ability. | 2 ||
| [`ability`](./Enums.md) | Enum || 2 | MoonHandDrop |

</details>

---

### Object: `CopySpells`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||
| `upgraded` | Boolean || 1 ||

</details>

---

### Object: `CreateGlobalModifiers`


**Definition:** Generates global map or encounter rules/modifiers.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#object-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`LowerAmbientLight`](#object-lowerambientlight) | Object | A visual effect that dims the map's lighting. | 3 ||
| [`BloodRain`](./Enums.md) | Integer || 3 | 1 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Object: `empty_self_damage`


**Definition:** Recoil damage specifically applied when the attack misses all targets.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 2 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||

</details>

---

### Object: `FindItemFromPool`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `ForceMoveTowardsTaggedObject`


**Definition:** Forces the character to move towards the nearest object with a specific tag.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `KnockOutCoin`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||
| [`chance`](./Enums.md) | Number || 1 | .02 |

</details>

---

### Object: `LowerAmbientLight`


**Definition:** A visual effect that dims the map's lighting.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CreateGlobalModifiers`](./Abilities_and_Spells.md#object-createglobalmodifiers)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array | The target opacity/dimness level. | 3 ||
| [`speed`](./Enums.md) | Array / Number || 3 | [1.0] |

</details>

---

### Object: `Math`


**Definition:** Triggers the Tinkerer's Math ability sequence.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`Stun`](./Enums.md) | Array / Integer || 2 | [0] |
| [`ApplyToSource`](#object-applytosource) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `MeleeRevengeDamage`


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#object-temppassivewhilehasstatus)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 70 ||
| [`effects`](#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 47 ||

</details>

---

### Object: `NextAttackSpecialCrit`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Integer | Flat addition to the critical damage multiplier. | 1 ||
| `extra_coins_per_stack` | Integer | Grants bonus coins based on stacks. | 1 ||
| `luck_increase` | Integer | Increases luck stat for the attack. | 1 ||

</details>

---

### Object: `NukeQuestFinalBossModifications`


**Definition:** Special encounter trigger for the Nuke Quest ending.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](#object-self_damage) | Object || 2 ||
| [`damage_instance`](#object-damage_instance) | Object || 1 ||
| [`splash_damage`](#object-splash_damage) | Object | Secondary Area of Effect blast parameters. | 1 ||

</details>

---

### Object: `OverHealToStatuses`


**Definition:** Converts excessive healing beyond maximum health into specific status effects.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| `stack_scale` | Integer || 1 ||
| [`RandomStatUp`](./Enums.md) | Enum / Integer || 1 | ceil(X/3) |
| [`TakeExtraTurn`](./Enums.md) | Integer || 1 | 1 |

</details>

---

### Object: `QuakeAreaChance`


**Definition:** Provides a probability to trigger an earthquake Area of Effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `radius` | Array / Integer | The tile radius of the quake. | 2 ||
| [`chance`](./Enums.md) | Number || 2 | .02 |

</details>

---

### Object: `RandomDistanceDisplace`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `min_dist` | Integer | The minimum tile distance they will be moved. | 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||

</details>

---

### Object: `RandomKnockback`


**Definition:** Applies a randomized amount of knockback force.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | Maximum knockback distance. | 2 ||
| `min` | Integer | Minimum knockback distance. | 2 ||

</details>

---

### Object: `ScatterCoins`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#object-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stackable` | Boolean | If true, multiple instances of this trigger can stack. | 2 ||
| [`stacks`](./Math_Equations.md) | Equation | Number of stacks or intensity to apply. | 2 ||

</details>

---

### Object: `SmartMetronome`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||
| `upgraded` | Boolean || 1 ||

</details>

---

### Object: `TakeBonusTurnWithAIControl`


**Definition:** Grants the character an immediate extra turn, but forces the AI to control them during it.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | If true, allows the AI to cast spells during this bonus turn. | 3 ||

</details>

---

### Object: `TeamCastAbility`


**Definition:** Requires or involves multiple characters to execute the ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum | Requires participants to share this tag. | 2 ||
| [`ability`](./Enums.md) | Enum || 2 | MoonHandDrop |
| `same_orientation` | Boolean || 1 ||

</details>

---

### Object: `XIsSpellStormRampAndReset`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reset_percent` | Integer | The percentage of stacks to keep after resetting. | 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||

</details>

---

### Object: `XIsTargetHealth`


**Definition:** Math variable assignment: Evaluates X as the target's current health.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional_boss), [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AlphaStatusOnTurnBegin`


**Definition:** Grants a specific status effect to the 'Alpha' (the party leader) at the start of their turn.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`DoubleCastSpellThisTurn`](./Enums.md) | Integer || 1 | 1 |

</details>

---

### Object: `ApplyPassivesToSpawnerWhileAlive`


**Definition:** Grants nested passives to the entity that spawned this object, lasting only as long as this object remains alive.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#object-additional_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`HideEquipment`](./Enums.md) | Enum || 1 | neck |

</details>

---

### Object: `ApplyStatusesNextTurnBegin`


**Definition:** Delays the application of the nested status effects until the start of the target's next turn.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Quivered`](./Enums.md) | Integer || 1 | 1 |

</details>

---

### Object: `ApplyToOthersWithSharedTagAndFaction`


**Definition:** Redirects the nested effects to apply to all other entities on the map that share the target's faction and specified tags.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `ApplyToRandomClosestAlly`


**Definition:** Redirects the nested effects to apply to the nearest friendly unit. If tied, chooses randomly among them.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | `Number` | Applies or references the 'ForceMoveTowards' effect/state. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `bonk_damage`


**Definition:** Damage dealt when knocked into a wall or obstacle.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1 ||
| [`effects`](#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---

### Object: `Conditional_ActiveWeather_Any`


**Definition:** Conditional trigger: Executes nested logic if the current map weather matches any in the list.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. | 1 ||
| [`DestroyEquipmentAndAttachParasite`](#object-destroyequipmentandattachparasite) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `Conditional_Backstab`


**Definition:** Conditional trigger: Executes nested logic if the attacker is positioned behind the target.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusCritChance` | `Number` | Applies or references the 'BonusCritChance' effect/state. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Fear`](./Enums.md) | Array / Integer || 1 | [.3] |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `Conditional_CanBeHealed`


**Definition:** Conditional trigger: Executes nested logic if the target's health is below maximum and they are capable of receiving healing.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 0 | |

</details>

---

### Object: `Conditional_DebuffRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized debuff probability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | The probability (0.0 to 1.0) of applying the debuff. | 1 ||
| [`DestroyEquipmentAndAttachParasite`](#object-destroyequipmentandattachparasite) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `Conditional_FinishedSpawning`


**Definition:** Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Imprison`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'Imprison' effect/state. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `Conditional_IsTrample`


**Definition:** Conditional trigger: Executes nested logic if the current movement/attack is classified as a trample.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SetKnockback` | `Number` | Applies or references the 'SetKnockback' effect/state. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `Conditional_LivingPlayerCat`


**Definition:** Conditional trigger: Executes nested logic if the target is an alive player-controlled cat.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`TempPassiveWhileHasStatus`](#object-temppassivewhilehasstatus) | Object | Grants nested passives only while the character possesses the specified status. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`ApplyToSource`](#object-applytosource) | Object || 1 ||
| [`Consumed`](#object-consumed) | Object || 1 ||

</details>

---

### Object: `Conditional_NotBig`


**Definition:** Conditional trigger: Executes nested logic if the target is NOT classified as large.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DisplaceTowardsSource` | `Number` | Applies or references the 'DisplaceTowardsSource' effect/state. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `Conditional_SourceAbilityHasTag`


**Definition:** Conditional trigger: Executes nested logic if the ability that triggered this effect has the specified tag.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`ApplyToSource`](#object-applytosource) | Object || 1 ||
| [`ScatterCoins`](#object-scattercoins) | Object || 1 ||
| [`tag`](./Enums.md) | Enum || 1 | megadino |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `Conditional_SourceHasStatus`


**Definition:** Conditional trigger: Executes nested logic if the caster currently has the specified status.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Bruise`](./Enums.md) | Array / Integer || 1 | [.1] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `damage_threshold_altanimations`


**Definition:** Triggers different hit animations based on the amount of damage dealt.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#object-graphics)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `heaviestMelee` | Integer | Animation trigger for massive damage. | 1 ||
| `heavyMelee` | Integer | Animation trigger if damage exceeds this threshold. | 1 ||

</details>

---


<details>
<summary><b>ApplyToOthersWithSharedTagAndFaction</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>ApplyToRandomPartyMemberIfPossible</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_BossOrBig</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_CanBeHealed</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_DebuffRoll</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_DestructibleCorpse</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_Displaceable</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_FinishedSpawning</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_FormulaIsPositive</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_IsSelf</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_IsTrample</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_NotBig</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_NotBoss</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_NotBossOrBig</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_OncePerBattle</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>Conditional_Shielded</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>LateStatusApplication</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>PassiveWhileNotTakingTurn</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>StatusKillers</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>XIsTargetHealth</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

### Object: `DelayCastAbility`


**Definition:** Queues an ability to be cast automatically after a certain delay or trigger.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `lingering` | Boolean || 1 ||
| `relative` | Boolean || 1 ||
| [`ability`](./Enums.md) | Enum || 1 | MoonHandDrop |

</details>

---

### Object: `DelayedWindCone`


**Definition:** Creates a delayed Area of Effect cone.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | Distance or area of effect in tiles. | 2 ||
| [`damage`](#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1 ||

</details>

---

### Object: `DybbukPossessed`


**Definition:** Defines the abilities and behaviors available when possessing another entity.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum || 1 ||
| [`punch_self_ability`](./Enums.md#enum-punch_self_ability) | Enum || 1 ||

</details>

---

### Object: `ForceImmediateMoveAndAttack`


**Definition:** Forces the character to immediately move to a target and use a specified ability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_InForm`](./Abilities_and_Spells.md#object-conditional_inform)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `even_if_cant_reach` | Boolean | If true, executes the attack even if the move fails to reach the target. | 1 ||
| [`ability`](./Enums.md) | Enum || 1 | MoonHandDrop |

</details>

---

### Object: `IncAuxCounterCycle`


**Definition:** Increments a generic auxiliary counter, looping back to 0 when it exceeds the maximum.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `change` | Integer || 1 ||
| `max` | Integer || 1 ||

</details>

---

### Object: `Madness`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||
| `tickdown_this_turn` | Boolean || 1 ||

</details>

---

### Object: `MergeDamageInstance`


**Definition:** Combines damage numbers or visual hit effects.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `can_instapop` | `Boolean` | If false, prevents the damage from instantly popping the target. | 1 ||
| `force_no_hit_animation` | Boolean | If true, suppresses the flinch/hit animation. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---

### Object: `NextBasicAttackCritsThisTurn`


**Definition:** Guarantees the next basic attack executed this turn will be a critical hit.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cant_miss` | `Boolean` | If true, ensures the attack cannot be dodged. | 1 ||
| `piercing` | `Boolean` | If true, the attack ignores armor. | 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---

### Object: `NextBattleStatusStacks`


**Definition:** Carries over the specified status effects into the next encounter/battle.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | `Number` | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. | 1 ||
| [`fights`](./Enums.md) | Integer || 1 | 9999 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `PassiveWhileNotTakingTurn`


**Definition:** Grants nested passives that are only active while it is NOT the character's turn.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `PoolMetronome`


**Definition:** Executes a random ability drawn from a specific pool.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `PopAndSpawn`


**Definition:** Destroys the target and replaces it with a new spawned entity.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md) | Array / Enum || 2 | [TallSkeletonCat] |
| `clone_items` | Boolean | If true, transfers inventory to the new entity. | 1 ||
| `clone_referenced_catdata` | Boolean | If true, copies the genetic data of the popped cat. | 1 ||
| `no_splatter` | Boolean || 1 ||

</details>

---

### Object: `RemoveStatusStacks`


**Definition:** Removes a specific number of stacks of a status effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks to remove. | 4 ||
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 4 ||

</details>

---

### Object: `RevengeDamage`


**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 31 ||
| [`effects`](#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 29 ||

</details>

---

### Object: `ScrambleLastUsedSpell`


**Definition:** Randomizes or scrambles the properties of the last spell cast.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `permanent` | Boolean | If true, the scramble persists for the rest of the run. | 1 ||

</details>

---

### Object: `SetAnimationAlts`


**Definition:** Overrides specific animation states with alternative animations.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dying`](./Enums.md#enum-dying) | Enum || 1 ||
| [`dead`](./Enums.md) | Enum || 1 | deadShot |

</details>

---

### Object: `ShowFakeDamage`


**Definition:** Displays a visual damage number without actually modifying health.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||
| [`style`](./Arrays.md#array-style) | Array | The visual font style for the text (e.g., [crit]). | 1 ||

</details>

---

### Object: `SpreadDisease`


**Definition:** Provides a chance to transmit a disease status to adjacent targets.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`disease`](./Enums.md#enum-disease) | Enum | The specific status effect ID representing the disease. | 13 ||
| [`chance`](./Enums.md) | Number || 12 | .02 |

</details>

---

### Object: `StatusGroup`


**Definition:** Groups multiple status effects together for batch application.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`DamageOrHealConditionally`](./Enums.md) | Integer || 1 | 1 |
| [`Freeze`](./Enums.md) | Array / Integer || 1 | [.1] |

</details>

---

### Object: `StatusKillers`


**Definition:** Instantly kills the target if they possess the specified status effects.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `SwapWeapon`


**Definition:** Replaces the character's currently equipped weapon with one from a specified pool.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `TransformEquipment`


**Definition:** Upgrades or transforms a specific equipped item into another.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | The original item ID. | 1 ||
| [`to`](./Enums.md#enum-to) | Enum | The new item ID. | 1 ||

</details>

---

### Object: `TransformWeapon`


**Definition:** Transforms the equipped weapon into another specific weapon state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#object-applytosourceonkill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | The original weapon ID. | 2 ||
| [`to`](./Enums.md#enum-to) | Enum | The transformed weapon ID. | 2 ||

</details>

---

### Object: `UseAbility`


**Definition:** Forces the character or target to instantly use a specified ability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `respect_prime` | Boolean | If true, respects the ability's prime/cooldown state. | 2 ||
| [`ability`](./Enums.md) | Enum || 2 | MoonHandDrop |

</details>

---

### Object: `UseMoveAbilityWithAI`


**Definition:** Forces the character to execute a movement ability using specific AI weights.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | The AI positioning logic profile to use. | 1 ||
| [`ability`](./Enums.md) | Enum || 1 | MoonHandDrop |

</details>

---

### Object: `VisualCountDownThenApplyStatus`


**Definition:** Displays a visual countdown above the target before applying the nested effects.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`ForceUseAbility`](./Enums.md) | Enum || 1 | MotherTumorGrow |

</details>

---

### Object: `WaggleClone`


**Definition:** Spawns visual clones or alternative hitbox variants of the projectile.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cWaggle`](#object-cwaggle) | Object || 1 ||
| [`cWaggle2x2`](#object-cwaggle2x2) | Object || 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||
| [`cWaggle3x3`](#object-cwaggle3x3) | Object || 1 ||

</details>

---

### Object: `effects`
### Object: `effects`

**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 0


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](./Abilities_and_Spells.md#object-dodamage), [`MeleeRevengeDamage`](./Abilities_and_Spells.md#object-meleerevengedamage), [`ROOT`](./Abilities_and_Spells.md#object-root), [`RevengeDamage`](./Abilities_and_Spells.md#object-revengedamage), [`bonk_damage`](./Abilities_and_Spells.md#object-bonk_damage), [`damage_instance`](./Abilities_and_Spells.md#object-damage_instance), [`empty_self_damage`](./Abilities_and_Spells.md#object-empty_self_damage), [`self_damage`](./Abilities_and_Spells.md#object-self_damage), [`splash_damage`](./Abilities_and_Spells.md#object-splash_damage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1695 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 750 ||
| [`FormChange`](#object-formchange) | Enum / Object | Transforms the character into a different state or form (e.g., Rage, HasCat). | 102 ||
| [`Stun`](./Enums.md) | Array / Integer || 98 | [0] |
| [`Burn`](./Enums.md) | Array / Enum / Integer || 85 | [.1] |
| [`Bruise`](./Enums.md) | Array / Integer || 79 | [.1] |
| `IgnoreSelf` | `Number` | Applies or references the 'IgnoreSelf' effect/state. | 75 ||
| [`Poison`](./Enums.md) | Array / Integer || 67 | [.1] |
| [`ChangeTile`](./Abilities_and_Spells.md#object-changetile) | `String` | Transforms the terrain tile under the target. | 62 ||
| [`Else`](#object-else) | Object || 59 ||
| [`Bleed`](./Enums.md) | Array / Integer || 54 | [.1] |
| [`Shield`](./Enums.md) | Enum / Integer || 49 | 2*X |
| [`Cleanse`](./Enums.md) | Integer || 44 | 0 |
| [`Confusion`](./Enums.md) | Array / Integer || 37 | [.1] |
| [`Conditional_HasTag`](#object-conditional_hastag) | Object | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 36 ||
| [`Conditional_Enemy`](#object-conditional_enemy) | Object | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 35 ||
| [`VisualFXTile`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'VisualFXTile' effect/state. | 34 ||
| [`SpeedUp`](./Enums.md) | Enum / Integer || 34 | 4 |
| [`Fear`](./Enums.md) | Array / Integer || 31 | [.3] |
| [`AllStatsUp`](./Enums.md) | Enum / Integer || 29 | 2 |
| [`Slow`](./Enums.md) | Array / Enum / Integer || 29 | [.1] |
| [`TransformAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'TransformAbility' effect/state. | 28 ||
| [`DamageUp`](./Enums.md) | Integer / String || 28 | 3 |
| [`ApplyToSource`](#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 27 ||
| [`BounceObject`](./Abilities_and_Spells.md#object-bounceobject) | `String` | Spawns a physics object that visually bounces off the target. | 26 ||
| [`Temporary`](#object-temporary) | Object | A wrapper object for applying status effects that automatically expire. | 26 ||
| [`ManaGain`](./Engine_LogicKeys.md#valid-property-keys) | Enum / Integer | Applies or references the 'ManaGain' effect/state. | 26 ||
| [`Conditional_Ally`](#object-conditional_ally) | Object | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 25 ||
| [`Blind`](./Enums.md) | Array / Integer || 24 | [2] |
| [`Immobile`](./Enums.md) | Array / Integer || 24 | [.1] |
| [`Weakness`](./Enums.md) | Array / Integer || 23 | [.1] |
| [`Charmed`](./Enums.md) | Array / Enum / Integer || 22 | [.1] |
| [`ConstitutionUp`](./Enums.md) | Array / Enum / Integer || 22 | [.5] |
| [`Leech`](./Enums.md) | Integer || 22 | 1 |
| [`StrengthUp`](./Enums.md) | Enum / Integer || 22 | max(int, 0) |
| [`EvolveAbilityFromPool`](./Abilities_and_Spells.md#object-evolveabilityfrompool) | `String` | Upgrades or transforms an existing ability into a new one from the specified pool. | 21 ||
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 21 ||
| [`IntelligenceUp`](./Enums.md) | Enum / Integer || 21 | item_aux |
| [`Freeze`](./Enums.md) | Array / Integer || 19 | [.1] |
| [`Madness`](#object-madness) | Array / Enum / Integer / Object || 19 | [.1] |
| [`Sleep`](./Enums.md) | Array / Integer || 19 | [.1] |
| `CollectsPickups` | `Number` | Applies or references the 'CollectsPickups' effect/state. | 17 ||
| [`KnockUpAndAway`](#object-knockupandaway) | Object | Displaces the target vertically and horizontally away from the source. | 17 ||
| [`Brace`](./Enums.md) | Integer || 17 | 2 |
| `OverrideKnockbackDamage` | `Number` | Applies or references the 'OverrideKnockbackDamage' effect/state. | 16 ||
| [`Consumed`](#object-consumed) | Object | State object triggered when this object or entity is eaten/consumed by another character. | 15 ||
| `VaporizeCorpse` | `Number` | Applies or references the 'VaporizeCorpse' effect/state. | 15 ||
| [`Petrify`](./Enums.md) | Array / Integer || 15 | [.15] |
| [`RandomStatUp`](./Enums.md) | Enum / Integer || 15 | ceil(X/3) |
| [`ChangeCatClass`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ChangeCatClass' effect/state. | 14 ||
| [`Conditional_GoodRoll`](#object-conditional_goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 14 ||
| `EndTurn` | `Number` | Applies or references the 'EndTurn' effect/state. | 14 ||
| `FaceAway` | `Number` | Applies or references the 'FaceAway' effect/state. | 14 ||
| [`RandomStatusFromPool`](#object-randomstatusfrompool) | Object | Selects and applies a random status effect from the provided nested block. | 14 ||
| `RefreshMovePoints` | `Number` | Applies or references the 'RefreshMovePoints' effect/state. | 14 ||
| `TakeExtraTurn` | `Number` | Applies or references the 'TakeExtraTurn' effect/state. | 14 ||
| [`TransformBasicAttack`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'TransformBasicAttack' effect/state. | 14 ||
| [`DivineShield`](./Enums.md) | Integer || 14 | 2 |
| [`Leeches`](./Enums.md) | Integer || 14 | 2 |
| [`CatPartsTransform`](#object-catpartstransform) | Object | Transforms specific body parts into different visual variants. | 13 ||
| [`Conditional_Boss`](#object-conditional_boss) | Object | Conditional trigger: Executes nested logic if the target is a Boss. | 13 ||
| `GenericDebuff` | `Number` | Applies or references the 'GenericDebuff' effect/state. | 13 ||
| `Displace` | `Number` | Applies or references the 'Displace' effect/state. | 12 ||
| [`Cleave`](#object-cleave) | Integer / Object || 12 | 1 |
| [`LuckUp`](./Enums.md) | Enum / Integer || 12 | 2 |
| [`Thorns`](./Enums.md) | Integer || 12 | 2 |
| [`ApplyToSourceOnKill`](#object-applytosourceonkill) | Object | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 11 ||
| [`ChanceToBreakFree`](#object-chancetobreakfree) | Object | Provides a probability to escape a grapple or restraining effect. | 11 ||
| [`DoScreenShake`](#object-doscreenshake) | Integer / Object | Triggers a camera screen shake effect. | 11 ||
| `FullHeal` | Integer | Applies or references the 'FullHeal' effect/state. | 11 ||
| [`Conditional_Speculative`](#object-conditional_speculative) | Object | A simulation object used by the AI to test hypothetical outcomes before committing to an action. | 10 ||
| `RefreshActPoints` | `Number` | Applies or references the 'RefreshActPoints' effect/state. | 10 ||
| [`VisualFX`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'VisualFX' effect/state. | 10 ||
| [`DexterityUp`](./Enums.md) | Enum / Integer || 10 | 2 |
| `PurgeAll` | `Number` | Applies or references the 'PurgeAll' effect/state. | 9 ||
| [`ApplyPassives`](#object-applypassives) | Object | Grants the nested passive abilities dynamically. | 9 ||
| `DeferVaporize` | `Number` | Applies or references the 'DeferVaporize' effect/state. | 9 ||
| `SpawnCreep` | `Number` | Applies or references the 'SpawnCreep' effect/state. | 9 ||
| [`MagicWeakness`](./Enums.md) | Array / Integer || 9 | [.1] |
| [`Marked`](./Enums.md) | Array / Integer || 9 | [.1] |
| [`RandomMagicMissile`](#object-randommagicmissile) | Integer / Object || 9 | 5 |
| [`Conditional_FormulaIsPositive`](#object-conditional_formulaispositive) | Object | Conditional trigger: Executes nested logic if the evaluated mathematical formula returns a value greater than 0. | 8 ||
| [`CanApplyToInanimate`](#object-canapplytoinanimate) | Object | Modifier object that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 8 ||
| `ChanceToBreak` | Integer | Applies or references the 'ChanceToBreak' effect/state. | 8 ||
| `OverrideChainKnockback` | `Number` | Applies or references the 'OverrideChainKnockback' effect/state. | 8 ||
| [`SpreadDisease`](#object-spreaddisease) | Object | Provides a chance to transmit a disease status to adjacent targets. | 8 ||
| [`Ammo`](./Enums.md) | Integer || 8 | -1 |
| [`Grappled`](./Enums.md) | Integer || 8 | 1 |
| [`HealthRegenUp`](./Enums.md) | Integer || 8 | 2 |
| [`ApplyStatusIfCrit`](#object-applystatusifcrit) | Object | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. | 7 ||
| `BramblesOnHit` | `Number` | Applies or references the 'BramblesOnHit' effect/state. | 7 ||
| `ContextualHeal` | `Number` | Applies or references the 'ContextualHeal' effect/state. | 7 ||
| `ForceAttack` | `Number` | Forces the character to execute an immediate attack. | 7 ||
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 7 ||
| `KnockbackDamageImmuneUntilSettled` | `Number` | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. | 7 ||
| `ManaSteal` | `Number` | Applies or references the 'ManaSteal' effect/state. | 7 ||
| [`TriggerWerewolfTransform`](./Engine_LogicKeys.md#valid-property-keys) | `Array` | Applies or references the 'TriggerWerewolfTransform' effect/state. | 7 ||
| [`AlphaCat`](./Enums.md) | Integer || 7 | 1 |
| [`Rot`](./Enums.md) | Array / Integer || 7 | [.1] |
| [`Tarred`](./Enums.md) | Array / Integer || 7 | [.1] |
| [`Tech`](./Enums.md) | Integer || 7 | 3 |
| [`TempRangeUp`](./Enums.md) | Integer || 7 | 2 |
| `ClearStarving` | `Number` | Applies or references the 'ClearStarving' effect/state. | 6 ||
| [`Conditional_Corpse`](#object-conditional_corpse) | Object | Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 6 ||
| [`ConjureBonusAbility`](./Abilities_and_Spells.md#object-conjurebonusability) | `String` | Adds a temporary bonus ability to the character's hand/deck. | 6 ||
| [`Craft`](#object-craft) | Object | Synthesizes or spawns a new item from a specific pool. | 6 ||
| [`DoDistortionRing`](#object-dodistortionring) | Object | Creates a visual distortion ring effect on the screen. | 6 ||
| `Metronome` | `Number` | Executes a random musical or metronome ability. | 6 ||
| `SetDistanceDisplace` | `Number` | Applies or references the 'SetDistanceDisplace' effect/state. | 6 ||
| `SetHealth` | `Number` | Applies or references the 'SetHealth' effect/state. | 6 ||
| [`TeamCastAbility`](./Abilities_and_Spells.md#object-teamcastability) | `String` | Requires or involves multiple characters to execute the ability. | 6 ||
| [`TwisterDisplaceWithDamage`](#object-twisterdisplacewithdamage) | Object | A whirlwind effect that randomly displaces targets and deals damage. | 6 ||
| [`BounceRock`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'BounceRock' effect/state. | 6 ||
| [`BackflipWhenTargeted`](#object-backflipwhentargeted) | Integer / Object || 6 | 2 |
| [`CharismaUp`](./Enums.md) | Enum / Integer || 6 | -2 |
| [`ObjectOnHitCharacter`](#object-objectonhitcharacter) | Enum / Object || 6 | SkeletonCatFamiliar |
| [`RandomInjury`](./Enums.md) | Integer || 6 | 1 |
| [`SpiderInfested`](./Enums.md) | Integer || 6 | 2 |
| [`CollectsPickupsWithAltEffects`](#object-collectspickupswithalteffects) | Object | Triggers alternative nested effects when collecting items or pickups. | 5 ||
| [`Conditional_HasStatus`](#object-conditional_hasstatus) | Object | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 5 ||
| [`Conditional_NotBoss`](#object-conditional_notboss) | Object | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 5 ||
| [`Conditional_Object`](#object-conditional_object) | Object | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 5 ||
| [`Conditional_PlayerCat`](#object-conditional_playercat) | Object | Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 5 ||
| `FillMana` | `Number` | Applies or references the 'FillMana' effect/state. | 5 ||
| `FlatLeech` | `Number` | Applies or references the 'FlatLeech' effect/state. | 5 ||
| `ForceMoveAway` | `Number` | Applies or references the 'ForceMoveAway' effect/state. | 5 ||
| `ForceMoveTowards` | `Number` | Applies or references the 'ForceMoveTowards' effect/state. | 5 ||
| `HitExplosion` | `Number` | Applies or references the 'HitExplosion' effect/state. | 5 ||
| [`Imprison`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'Imprison' effect/state. | 5 ||
| [`KnockbackDirectionIsFacingDirection`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'KnockbackDirectionIsFacingDirection' effect/state. | 5 ||
| `MonkStanceSwitch` | `Number` | Applies or references the 'MonkStanceSwitch' effect/state. | 5 ||
| [`ObjectOnHit`](./Abilities_and_Spells.md#object-objectonhit) | `String` | Spawns a specific physics/item object upon impact. | 5 ||
| [`ObjectOnHitEmpty`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ObjectOnHitEmpty' effect/state. | 5 ||
| [`PopAndSpawn`](./Abilities_and_Spells.md#object-popandspawn) | `String` | Destroys the target and replaces it with a new spawned entity. | 5 ||
| `Purge` | `Number` | Applies or references the 'Purge' effect/state. | 5 ||
| `RefreshMovePointsIfHit` | `Number` | Applies or references the 'RefreshMovePointsIfHit' effect/state. | 5 ||
| `SafeDie` | `Number` | Applies or references the 'SafeDie' effect/state. | 5 ||
| `SpawnBearTrap` | `Number` | Applies or references the 'SpawnBearTrap' effect/state. | 5 ||
| `SpawnRock` | `Number` | Applies or references the 'SpawnRock' effect/state. | 5 ||
| [`DodgeChance_Status`](./Enums.md) | Integer || 5 | 50 |
| [`Drowsy`](./Enums.md) | Integer || 5 | 8 |
| [`MovementUp`](./Enums.md) | Integer || 5 | -2 |
| [`Revive`](./Enums.md) | Integer || 5 | 50 |
| [`SoulLink`](./Enums.md) | Integer || 5 | 1 |
| [`Stealth`](./Enums.md) | Integer || 5 | 2 |
| [`TempDamageUp`](./Enums.md) | Integer || 5 | 2 |
| [`Webbed`](./Enums.md) | Integer || 5 | 1 |
| [`RemoveStatus`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'RemoveStatus' effect/state. | 4 ||
| [`SpawnThingIfHitKills`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'SpawnThingIfHitKills' effect/state. | 4 ||
| [`ApplyToConsumed`](#object-applytoconsumed) | Object | Redirects the nested effects to apply to the entity that just consumed this object. | 4 ||
| [`ArcLightning`](#object-arclightning) | Object | Executes a chain-lightning logic block that bounces between targets. | 4 ||
| [`Conditional_Familiar`](#object-conditional_familiar) | Object | Conditional trigger: Executes nested logic if the target is a familiar. | 4 ||
| [`EnableWeather`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'EnableWeather' effect/state. | 4 ||
| `ExplosionIfHitSomething` | `Number` | Applies or references the 'ExplosionIfHitSomething' effect/state. | 4 ||
| `FaceCamera` | `Number` | Applies or references the 'FaceCamera' effect/state. | 4 ||
| [`LateStatusApplication`](#object-latestatusapplication) | Object | Applies a status effect after all primary damage and effects have fully resolved. | 4 ||
| `RemoveActPoints` | `Number` | Applies or references the 'RemoveActPoints' effect/state. | 4 ||
| `SendRock` | `Number` | Applies or references the 'SendRock' effect/state. | 4 ||
| [`SpecificInjury`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'SpecificInjury' effect/state. | 4 ||
| [`SwitchMusic`](#object-switchmusic) | Object | Changes the background music track or layer during combat. | 4 ||
| [`TakeBonusTurnWithStatus`](#object-takebonusturnwithstatus) | Object | Grants the character an immediate extra turn while afflicted with specific statuses. | 4 ||
| [`TimeDelayStatusApplication`](#object-timedelaystatusapplication) | Object | Delays the nested effects by a specified amount of real-time seconds. | 4 ||
| [`UseAbility`](./Abilities_and_Spells.md#object-useability) | `String` | Forces the character or target to instantly use a specified ability. | 4 ||
| `VaporizeInanimate` | `Number` | Applies or references the 'VaporizeInanimate' effect/state. | 4 ||
| [`LowerAmbientLight`](#object-lowerambientlight) | Object | A visual effect that dims the map's lighting. | 4 ||
| [`Charge`](./Enums.md) | Integer || 4 | 2 |
| [`HealthGain`](./Enums.md) | Integer || 4 | 5 |
| [`Reanimate`](./Enums.md) | Integer || 4 | 50 |
| [`Conditional_InForm`](#object-conditional_inform) | Object | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 3 ||
| [`CatPartsSizeScaleStatus`](#object-catpartssizescalestatus) | Object | Visually scales specific body parts of a character. | 3 ||
| [`CollideWithConsumed`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'CollideWithConsumed' effect/state. | 3 ||
| [`Conditional_AffectedByElement`](#object-conditional_affectedbyelement) | Object | Conditional trigger: Executes nested logic if the target is currently afflicted by the specified element. | 3 ||
| [`Conditional_FirstApplicationThisTurn`](#object-conditional_firstapplicationthisturn) | Object | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 3 ||
| [`Conditional_LastHit`](#object-conditional_lasthit) | Object | Conditional trigger: Executes nested logic if this attack is the final hit of a multi-hit sequence. | 3 ||
| `CorpseVaporizer` | `Number` | Applies or references the 'CorpseVaporizer' effect/state. | 3 ||
| `CurrentWeaponDamageUp` | Integer | Applies or references the 'CurrentWeaponDamageUp' effect/state. | 3 ||
| `DeleteObject` | `Number` | Applies or references the 'DeleteObject' effect/state. | 3 ||
| `DestroyTrinket` | `Number` | Applies or references the 'DestroyTrinket' effect/state. | 3 ||
| `DestroyWeapon` | `Number` | Applies or references the 'DestroyWeapon' effect/state. | 3 ||
| `DestroyWeaponThrow` | `Number` | Applies or references the 'DestroyWeaponThrow' effect/state. | 3 ||
| `Die` | `Number` | Applies or references the 'Die' effect/state. | 3 ||
| `DisplaceTowardsSource` | `Number` | Applies or references the 'DisplaceTowardsSource' effect/state. | 3 ||
| [`DustOnHit`](#object-dustonhit) | Object | Spawns a specific particle or cloud object upon impact. | 3 ||
| `ForceDisplace` | `Number` | Applies or references the 'ForceDisplace' effect/state. | 3 ||
| `ForceMoveTowardsEnemies` | `Number` | Applies or references the 'ForceMoveTowardsEnemies' effect/state. | 3 ||
| `InstantMaxHealthUp` | `Number` | Applies or references the 'InstantMaxHealthUp' effect/state. | 3 ||
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 3 ||
| `PlayBackground` | Integer | Applies or references the 'PlayBackground' effect/state. | 3 ||
| `PullSourceToTarget` | `Number` | Applies or references the 'PullSourceToTarget' effect/state. | 3 ||
| `RefreshWeaponAbility` | `Number` | Applies or references the 'RefreshWeaponAbility' effect/state. | 3 ||
| `RepairAll` | `Number` | Applies or references the 'RepairAll' effect/state. | 3 ||
| `RepairOnKill` | `Number` | Applies or references the 'RepairOnKill' effect/state. | 3 ||
| [`SetCrazyEyeBackgroundWeights`](#object-setcrazyeyebackgroundweights) | Object | Adjusts visual rendering weights for the 'Crazy Eye' background effect. | 3 ||
| [`SpawnCustomTrap`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'SpawnCustomTrap' effect/state. | 3 ||
| `SpawnNeutralWebTrapOnMiss` | `Number` | Applies or references the 'SpawnNeutralWebTrapOnMiss' effect/state. | 3 ||
| `VaporizeTarget` | `Number` | Applies or references the 'VaporizeTarget' effect/state. | 3 ||
| [`DamageOrHealConditionally`](./Enums.md) | Integer || 3 | 1 |
| [`Doomed`](./Enums.md) | Integer || 3 | 3 |
| [`ExtraBasicAttacks_Status`](./Enums.md) | Integer || 3 | 1 |
| [`KineticSpikes`](./Enums.md) | Integer || 3 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer || 3 | 1 |
| [`NextAttackBonusRange`](./Enums.md) | Integer || 3 | 3 |
| [`PermanentConstitution`](./Enums.md) | Integer || 3 | 2 |
| [`PoisonLace`](./Enums.md) | Enum / Integer || 3 | X/3 |
| [`Reflect`](./Enums.md) | Integer || 3 | 5 |
| [`ReviveNextRound`](#object-revivenextround) | Integer / Object || 3 | 2 |
| [`SpellDamageUp`](./Enums.md) | Integer || 3 | 3 |
| [`Tangled`](#object-tangled) | Integer / Object || 3 | 1 |
| [`TempSpeedUp`](./Enums.md) | Enum / Integer || 3 | 4 |
| [`TempStrengthUp`](./Enums.md) | Enum || 3 | X |
| `PartialPurge` | `Number` | Applies or references the 'PartialPurge' effect/state. | 2 ||
| `UpgradeRandomAbility` | `Number` | Applies or references the 'UpgradeRandomAbility' effect/state. | 2 ||
| [`ApplyMultipleTimes`](#object-applymultipletimes) | Object | A loop object that executes its nested logic multiple times. | 2 ||
| `AddSpiritBombCharges` | `Number` | Applies or references the 'AddSpiritBombCharges' effect/state. | 2 ||
| `BonusKnockbackDamage` | `Number` | Applies or references the 'BonusKnockbackDamage' effect/state. | 2 ||
| `Bound` | `Number` | Applies or references the 'Bound' effect/state. | 2 ||
| `BurgleCoin` | `Number` | Applies or references the 'BurgleCoin' effect/state. | 2 ||
| `CancelPrimedAbilities` | `Number` | Applies or references the 'CancelPrimedAbilities' effect/state. | 2 ||
| [`ChangeFaction`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ChangeFaction' effect/state. | 2 ||
| `CharmedForceAttack` | `Number` | Applies or references the 'CharmedForceAttack' effect/state. | 2 ||
| `CollideWithThrowTarget` | `Number` | Applies or references the 'CollideWithThrowTarget' effect/state. | 2 ||
| [`Conditional_BadRoll`](#object-conditional_badroll) | Object | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. | 2 ||
| [`Conditional_BossOrBig`](#object-conditional_bossorbig) | Object | Conditional trigger: Executes nested logic if the target is a Boss or has a large size classification. | 2 ||
| [`Conditional_Buddy`](#object-conditional_buddy) | Object | Conditional trigger: Executes nested logic if the target is the caster's summoned buddy/familiar. | 2 ||
| [`Conditional_DestructibleCorpse`](#object-conditional_destructiblecorpse) | Object | Conditional trigger: Executes nested logic if the target is a corpse that can be destroyed or vaporized. | 2 ||
| [`Conditional_HealthThreshold`](#object-conditional_healththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 2 ||
| [`Conditional_IsSelf`](#object-conditional_isself) | Object | Conditional trigger: Executes nested logic if the target is the caster themselves. | 2 ||
| [`Conditional_NotAlly`](#object-conditional_notally) | Object | Conditional trigger: Executes nested logic if the target is NOT friendly to the caster. | 2 ||
| [`Conditional_NotBossOrBig`](#object-conditional_notbossorbig) | Object | Conditional trigger: Executes nested logic if the target is NEITHER a Boss nor large. | 2 ||
| [`Conditional_NotShielded`](#object-conditional_notshielded) | Object | Conditional trigger: Executes nested logic if the target does NOT currently have a Shield status. | 2 ||
| [`Conditional_OncePerBattle`](#object-conditional_onceperbattle) | Object | Conditional trigger: Executes nested logic only once per encounter/battle. | 2 ||
| [`Conditional_Shielded`](#object-conditional_shielded) | Object | Conditional trigger: Executes nested logic if the target currently has a Shield status. | 2 ||
| `CopySpells` | `Number` | Duplicates existing spells currently in the character's hand. | 2 ||
| `Counterspell` | `Number` | Applies or references the 'Counterspell' effect/state. | 2 ||
| `DamageBasedOnMissingHealth` | `Number` | Applies or references the 'DamageBasedOnMissingHealth' effect/state. | 2 ||
| `DamageDistanceAOEFalloff` | `Number` | Applies or references the 'DamageDistanceAOEFalloff' effect/state. | 2 ||
| `DamageTrinket` | `Number` | Applies or references the 'DamageTrinket' effect/state. | 2 ||
| `DelayedFury` | `Number` | Applies or references the 'DelayedFury' effect/state. | 2 ||
| [`DestroyEquipmentAndAttachParasite`](#object-destroyequipmentandattachparasite) | Object | Removes an equipped item and replaces it with a parasite from a specified pool. | 2 ||
| `DieViaAbilityInternally` | `Number` | Applies or references the 'DieViaAbilityInternally' effect/state. | 2 ||
| `DisplaceToOriginalPosition` | `Number` | Applies or references the 'DisplaceToOriginalPosition' effect/state. | 2 ||
| `FlowersOnHit` | `Number` | Applies or references the 'FlowersOnHit' effect/state. | 2 ||
| `ForceMoveNonAlliesInRangeTowardsTile` | `Number` | Applies or references the 'ForceMoveNonAlliesInRangeTowardsTile' effect/state. | 2 ||
| [`ForceMoveTowardsTaggedObject`](#object-forcemovetowardstaggedobject) | Object | Forces the character to move towards the nearest object with a specific tag. | 2 ||
| `IgnoreDamage` | `Number` | Applies or references the 'IgnoreDamage' effect/state. | 2 ||
| [`ImmediateUseAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ImmediateUseAbility' effect/state. | 2 ||
| [`ImmediateUseDirectionalAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ImmediateUseDirectionalAbility' effect/state. | 2 ||
| `JohnnyCriesForWashers` | `Number` | Applies or references the 'JohnnyCriesForWashers' effect/state. | 2 ||
| `LeaveBehindRockOnKnockback` | `Number` | Applies or references the 'LeaveBehindRockOnKnockback' effect/state. | 2 ||
| [`Math`](#object-math) | Object | Triggers the Tinkerer's Math ability sequence. | 2 ||
| `MaxHPUp` | `Number` | Applies or references the 'MaxHPUp' effect/state. | 2 ||
| `NextAttackSpecialCrit` | `Number` | Modifies the character's next attack to have special critical properties. | 2 ||
| [`OverHealToStatuses`](#object-overhealtostatuses) | Object | Converts excessive healing beyond maximum health into specific status effects. | 2 ||
| `PermanentStrength` | `Number` | Applies or references the 'PermanentStrength' effect/state. | 2 ||
| `PermanentUpgradeRandomActive` | `Number` | Applies or references the 'PermanentUpgradeRandomActive' effect/state. | 2 ||
| `PullSourceToKnockbackImmuneTarget` | `Number` | Applies or references the 'PullSourceToKnockbackImmuneTarget' effect/state. | 2 ||
| [`QuakeAreaChance`](#object-quakeareachance) | Object | Provides a probability to trigger an earthquake Area of Effect. | 2 ||
| `RandomDistanceDisplace` | `Number` | Displaces the target by a randomized distance. | 2 ||
| [`RandomKnockback`](#object-randomknockback) | Object | Applies a randomized amount of knockback force. | 2 ||
| `RebukeDamage` | `Number` | Applies or references the 'RebukeDamage' effect/state. | 2 ||
| `RemoveMovePoints` | `Number` | Applies or references the 'RemoveMovePoints' effect/state. | 2 ||
| `RepairArmorCondition` | `Number` | Applies or references the 'RepairArmorCondition' effect/state. | 2 ||
| `RepairWeaponCondition` | `Number` | Applies or references the 'RepairWeaponCondition' effect/state. | 2 ||
| `ResetArmorShield` | `Number` | Applies or references the 'ResetArmorShield' effect/state. | 2 ||
| `ScatterHeldCoin` | `Number` | Applies or references the 'ScatterHeldCoin' effect/state. | 2 ||
| `ScrambleEverything` | `Number` | Applies or references the 'ScrambleEverything' effect/state. | 2 ||
| `SetShield` | `Number` | Applies or references the 'SetShield' effect/state. | 2 ||
| `Shatter` | `Number` | Applies or references the 'Shatter' effect/state. | 2 ||
| `SignalFinalBossShieldBroke` | `Number` | Applies or references the 'SignalFinalBossShieldBroke' effect/state. | 2 ||
| `SmartMetronome` | `Number` | Executes a 'smart' random ability that aims to be beneficial based on context. | 2 ||
| `SpeculativeMoveSelfCorpseOffMap` | `Number` | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 2 ||
| `StanceSwitchToMelee` | `Number` | Applies or references the 'StanceSwitchToMelee' effect/state. | 2 ||
| `SwallowSmallCharacter` | `Number` | Applies or references the 'SwallowSmallCharacter' effect/state. | 2 ||
| [`TakeBonusTurnWithAIControl`](#object-takebonusturnwithaicontrol) | Object | Grants the character an immediate extra turn, but forces the AI to control them during it. | 2 ||
| `TempTrampleUntilSettled` | `Number` | Applies or references the 'TempTrampleUntilSettled' effect/state. | 2 ||
| `TradeLife` | `Number` | Applies or references the 'TradeLife' effect/state. | 2 ||
| `TriggerDOTStatuses` | `Number` | Applies or references the 'TriggerDOTStatuses' effect/state. | 2 ||
| `RandomStatDown` | Array / Integer / String | Applies or references the 'RandomStatDown' effect/state. | 2 ||
| `SelfStun` | `Number` | Applies or references the 'SelfStun' effect/state. | 2 ||
| [`BodyGuard`](#object-bodyguard) | Object || 2 ||
| [`CritChanceUp`](./Enums.md) | Integer || 2 | 2 |
| [`DiminishingHealthRegen`](./Enums.md) | Integer || 2 | 3 |
| [`DoubleCastSpell`](./Enums.md) | Integer || 2 | 1 |
| [`DoubleLoot`](./Enums.md) | Integer || 2 | 2 |
| [`FreeSpell`](./Enums.md) | Integer || 2 | 2 |
| [`Hex`](./Enums.md) | Integer || 2 | 1 |
| [`KnockOutCoin`](#object-knockoutcoin) | Integer / Object || 2 | 1 |
| [`Knockback`](./Enums.md) | Integer || 2 | 5 |
| [`Lifesteal`](./Enums.md) | Integer || 2 | 3 |
| [`ManaLeeches`](./Enums.md) | Integer || 2 | 2 |
| [`Ostracized`](./Enums.md) | Integer || 2 | 2 |
| [`PartialCleanse`](./Enums.md) | Integer || 2 | 9999 |
| [`Possessed`](./Enums.md) | Integer || 2 | 1 |
| [`RangeUp`](./Enums.md) | Integer || 2 | 1 |
| [`RepairWeapon`](./Enums.md) | Integer || 2 | 99 |
| [`SizeScale`](./Enums.md) | Number || 2 | .6 |
| [`SpawnFlames`](./Enums.md) | Array || 2 | [.20+.1*level] |
| [`TempCritChanceUp`](./Enums.md) | Integer || 2 | 30 |
| [`TempDexterityUp`](./Enums.md) | Enum || 2 | X |
| [`TempInitiativeChange`](./Enums.md) | Integer || 2 | -100 |
| [`TempMovement`](./Enums.md) | Enum / Integer || 2 | 20 |
| [`TempSpellDamageUp`](./Enums.md) | Integer || 2 | 1 |
| [`TrailBlazer`](./Enums.md) | Enum / Integer || 2 | mov |
| [`Trample`](./Enums.md) | Integer || 2 | 3 |
| [`DoubleStatus`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'DoubleStatus' effect/state. | 1 ||
| `AIFavorLowHealth` | `Number` | Applies or references the 'AIFavorLowHealth' effect/state. | 1 ||
| `AlliesTakeExtraTurn` | `Number` | Applies or references the 'AlliesTakeExtraTurn' effect/state. | 1 ||
| [`AlternateIdleAnimation`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'AlternateIdleAnimation' effect/state. | 1 ||
| `ApplyShieldToApplierBasedOnMaxHealth` | `Number` | Applies or references the 'ApplyShieldToApplierBasedOnMaxHealth' effect/state. | 1 ||
| [`ApplyStatusesNextTurnBegin`](#object-applystatusesnextturnbegin) | Object | Delays the application of the nested status effects until the start of the target's next turn. | 1 ||
| [`ApplyToOthersWithSharedTagAndFaction`](#object-applytootherswithsharedtagandfaction) | Object | Redirects the nested effects to apply to all other entities on the map that share the target's faction and specified tags. | 1 ||
| [`ApplyToRandomClosestAlly`](#object-applytorandomclosestally) | Object | Redirects the nested effects to apply to the nearest friendly unit. If tied, chooses randomly among them. | 1 ||
| `BombRatTurtle` | `Number` | Applies or references the 'BombRatTurtle' effect/state. | 1 ||
| `BonusDamageBasedOnMana` | `Number` | Applies or references the 'BonusDamageBasedOnMana' effect/state. | 1 ||
| `BypassRockKnockback` | `Number` | Applies or references the 'BypassRockKnockback' effect/state. | 1 ||
| `CanceledQueuedInput` | `Number` | Applies or references the 'CanceledQueuedInput' effect/state. | 1 ||
| `CaptureFamiliar` | Integer | Applies or references the 'CaptureFamiliar' effect/state. | 1 ||
| `ChaosBossFlipMidTeleport` | `Number` | Applies or references the 'ChaosBossFlipMidTeleport' effect/state. | 1 ||
| `ChaosBossFormChange` | `Number` | Applies or references the 'ChaosBossFormChange' effect/state. | 1 ||
| `CharmedFacingForceAttack` | `Number` | Applies or references the 'CharmedFacingForceAttack' effect/state. | 1 ||
| `ClearFinalBossBattlefield` | `Number` | Applies or references the 'ClearFinalBossBattlefield' effect/state. | 1 ||
| `CloneWeaponTemp` | `Number` | Applies or references the 'CloneWeaponTemp' effect/state. | 1 ||
| [`CoinTossBounce`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'CoinTossBounce' effect/state. | 1 ||
| [`Conditional_AbilityTargetIsSelf`](Engine_Uncategorized_Resources.md#conditional_abilitytargetisself) | Object | Conditional constraint. Nested properties only trigger if this is true. | 1 ||
| [`Conditional_ActiveWeather_Any`](#object-conditional_activeweather_any) | Object | Conditional trigger: Executes nested logic if the current map weather matches any in the list. | 1 ||
| [`Conditional_Backstab`](#object-conditional_backstab) | Object | Conditional trigger: Executes nested logic if the attacker is positioned behind the target. | 1 ||
| [`Conditional_CanBeHealed`](#object-conditional_canbehealed) | Object | Conditional trigger: Executes nested logic if the target's health is below maximum and they are capable of receiving healing. | 1 ||
| [`Conditional_DebuffRoll`](#object-conditional_debuffroll) | Object | Conditional trigger: Executes nested logic based on a randomized debuff probability. | 1 ||
| [`Conditional_Displaceable`](#object-conditional_displaceable) | Object | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 1 ||
| [`Conditional_HasCleansableDebuffs`](#object-conditional_hascleansabledebuffs) | Object | Conditional trigger: Executes nested logic if the target currently has negative status effects that can be cleansed. | 1 ||
| [`Conditional_IsTrample`](#object-conditional_istrample) | Object | Conditional trigger: Executes nested logic if the current movement/attack is classified as a trample. | 1 ||
| [`Conditional_LivingPlayerCat`](#object-conditional_livingplayercat) | Object | Conditional trigger: Executes nested logic if the target is an alive player-controlled cat. | 1 ||
| [`Conditional_NotBig`](#object-conditional_notbig) | Object | Conditional trigger: Executes nested logic if the target is NOT classified as large. | 1 ||
| [`Conditional_RandomChance`](#object-conditional_randomchance) | Object | Conditional trigger: Executes nested logic based on a flat percentage random roll. | 1 ||
| [`Conditional_SourceAbilityHasTag`](#object-conditional_sourceabilityhastag) | Object | Conditional trigger: Executes nested logic if the ability that triggered this effect has the specified tag. | 1 ||
| [`Conditional_SourceHasStatus`](#object-conditional_sourcehasstatus) | Object | Conditional trigger: Executes nested logic if the caster currently has the specified status. | 1 ||
| [`ConjureSingleUseBonusAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ConjureSingleUseBonusAbility' effect/state. | 1 ||
| `CurrentWeaponAddElectricElement` | `Number` | Applies or references the 'CurrentWeaponAddElectricElement' effect/state. | 1 ||
| `DamageWeapon` | `Number` | Applies or references the 'DamageWeapon' effect/state. | 1 ||
| [`DeathwormUnderground`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'DeathwormUnderground' effect/state. | 1 ||
| `DecoySwapper` | `Number` | Applies or references the 'DecoySwapper' effect/state. | 1 ||
| [`DelayCastAbility`](#object-delaycastability) | Enum / Object | Queues an ability to be cast automatically after a certain delay or trigger. | 1 ||
| [`DelayedWindCone`](#object-delayedwindcone) | Object | Creates a delayed Area of Effect cone. | 1 ||
| `DeleteTraps` | `Number` | Applies or references the 'DeleteTraps' effect/state. | 1 ||
| `DestroyNeckArmor` | `Number` | Applies or references the 'DestroyNeckArmor' effect/state. | 1 ||
| `DieViolently` | Integer | Applies or references the 'DieViolently' effect/state. | 1 ||
| [`DinoLegAnimation`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'DinoLegAnimation' effect/state. | 1 ||
| `Disguised` | `Number` | Applies or references the 'Disguised' effect/state. | 1 ||
| `DissolveRandomArmorPiece` | `Number` | Applies or references the 'DissolveRandomArmorPiece' effect/state. | 1 ||
| `DontHealEnemies` | `Number` | Applies or references the 'DontHealEnemies' effect/state. | 1 ||
| `DoubleCastSpellsEachTurn_Status` | `Number` | Applies or references the 'DoubleCastSpellsEachTurn_Status' effect/state. | 1 ||
| `DrainAllyCatsForFleshGolem` | `Number` | Applies or references the 'DrainAllyCatsForFleshGolem' effect/state. | 1 ||
| `DuplicateRandomEquippedItem` | `Number` | Applies or references the 'DuplicateRandomEquippedItem' effect/state. | 1 ||
| `Enlarge` | `Number` | Applies or references the 'Enlarge' effect/state. | 1 ||
| [`EnterMount`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'EnterMount' effect/state. | 1 ||
| `ExistUntilIdleUpkeep` | `Number` | Applies or references the 'ExistUntilIdleUpkeep' effect/state. | 1 ||
| `ExplodeCharacter` | `Number` | Applies or references the 'ExplodeCharacter' effect/state. | 1 ||
| `ExplodeCharacter_DeathBloom` | `Number` | Applies or references the 'ExplodeCharacter_DeathBloom' effect/state. | 1 ||
| `ExplodeCharacter_DeathBloom2` | `Number` | Applies or references the 'ExplodeCharacter_DeathBloom2' effect/state. | 1 ||
| `ExplodeCharacter_NoDie` | `Number` | Applies or references the 'ExplodeCharacter_NoDie' effect/state. | 1 ||
| `FactionConversion` | `Number` | Applies or references the 'FactionConversion' effect/state. | 1 ||
| `FactionDisguiseSource` | `Number` | Applies or references the 'FactionDisguiseSource' effect/state. | 1 ||
| `FastKnockback` | `Number` | Applies or references the 'FastKnockback' effect/state. | 1 ||
| `FinalBossQueueBeam` | `Number` | Applies or references the 'FinalBossQueueBeam' effect/state. | 1 ||
| `FlatAIBonus` | `Number` | Applies or references the 'FlatAIBonus' effect/state. | 1 ||
| `ForceCollectsPickups` | `Number` | Applies or references the 'ForceCollectsPickups' effect/state. | 1 ||
| `ForceMoveAndAttack` | `Number` | Applies or references the 'ForceMoveAndAttack' effect/state. | 1 ||
| `ForceTransferWeapon` | `Number` | Applies or references the 'ForceTransferWeapon' effect/state. | 1 ||
| `GenericBuff` | `Number` | Applies or references the 'GenericBuff' effect/state. | 1 ||
| `GiveBoundItemToTarget` | `Number` | Applies or references the 'GiveBoundItemToTarget' effect/state. | 1 ||
| [`GlobalSpawnCharacter`](./Engine_LogicKeys.md#valid-property-keys) | Enum | Applies or references the 'GlobalSpawnCharacter' effect/state. | 1 ||
| `HealPercentMaxHP` | `Number` | Applies or references the 'HealPercentMaxHP' effect/state. | 1 ||
| `HealTo` | `Number` | Applies or references the 'HealTo' effect/state. | 1 ||
| `IgnoreDebuffs` | `Number` | Applies or references the 'IgnoreDebuffs' effect/state. | 1 ||
| [`IncAuxCounterCycle`](#object-incauxcountercycle) | Object | Increments a generic auxiliary counter, looping back to 0 when it exceeds the maximum. | 1 ||
| `IncreaseCumulativeBlastDamage` | `Number` | Applies or references the 'IncreaseCumulativeBlastDamage' effect/state. | 1 ||
| `IncreaseItemAuxOnKill` | `Number` | Applies or references the 'IncreaseItemAuxOnKill' effect/state. | 1 ||
| `InterchangeMoveActPoints` | `Number` | Applies or references the 'InterchangeMoveActPoints' effect/state. | 1 ||
| `MadnessChanceOnTurnBegin` | Integer | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. | 1 ||
| `MakeWeaponUnbreakable` | `Number` | Applies or references the 'MakeWeaponUnbreakable' effect/state. | 1 ||
| `ManaStealToHealth` | `Number` | Applies or references the 'ManaStealToHealth' effect/state. | 1 ||
| `ManglerAttack` | `Number` | Applies or references the 'ManglerAttack' effect/state. | 1 ||
| `ManglerShuffle` | `Boolean` | Applies or references the 'ManglerShuffle' effect/state. | 1 ||
| `MassAttackThis` | `Number` | Applies or references the 'MassAttackThis' effect/state. | 1 ||
| `MimicMetronome` | `Number` | Applies or references the 'MimicMetronome' effect/state. | 1 ||
| `MotherTumorDebugForcePass` | `Number` | Applies or references the 'MotherTumorDebugForcePass' effect/state. | 1 ||
| [`NextBasicAttackCritsThisTurn`](#object-nextbasicattackcritsthisturn) | Object | Guarantees the next basic attack executed this turn will be a critical hit. | 1 ||
| [`NextBattleStatusStacks`](#object-nextbattlestatusstacks) | Object | Carries over the specified status effects into the next encounter/battle. | 1 ||
| [`ObjectOnHitFullyEmpty`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ObjectOnHitFullyEmpty' effect/state. | 1 ||
| `OverHealToShield` | `Number` | Applies or references the 'OverHealToShield' effect/state. | 1 ||
| [`OverrideChainKnockbackDamage`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'OverrideChainKnockbackDamage' effect/state. | 1 ||
| `PermanentCharisma` | `Number` | Applies or references the 'PermanentCharisma' effect/state. | 1 ||
| `PermanentLuck` | `Number` | Applies or references the 'PermanentLuck' effect/state. | 1 ||
| `PermanentUpgradeRandomActiveOrPassive` | `Number` | Applies or references the 'PermanentUpgradeRandomActiveOrPassive' effect/state. | 1 ||
| [`PoolMetronome`](#object-poolmetronome) | Object | Executes a random ability drawn from a specific pool. | 1 ||
| [`QueueUseAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'QueueUseAbility' effect/state. | 1 ||
| `RandomKnockbackDirection` | `Number` | Applies or references the 'RandomKnockbackDirection' effect/state. | 1 ||
| `ReformMoonHead` | `Number` | Applies or references the 'ReformMoonHead' effect/state. | 1 ||
| `RefreshItemAbilities` | `Number` | Applies or references the 'RefreshItemAbilities' effect/state. | 1 ||
| `RefreshNonManaItemAbilities` | `Number` | Applies or references the 'RefreshNonManaItemAbilities' effect/state. | 1 ||
| `RefreshOncePerFightAbilities` | `Number` | Applies or references the 'RefreshOncePerFightAbilities' effect/state. | 1 ||
| [`RemoveStatusStacks`](#object-removestatusstacks) | Object | Removes a specific number of stacks of a status effect. | 1 ||
| `RepairAllCondition` | `Number` | Applies or references the 'RepairAllCondition' effect/state. | 1 ||
| `RerollEnemy` | `Number` | Applies or references the 'RerollEnemy' effect/state. | 1 ||
| `ReturnDinoLegs` | `Number` | Applies or references the 'ReturnDinoLegs' effect/state. | 1 ||
| `RNGCannonRandomDamage` | `Number` | Applies or references the 'RNGCannonRandomDamage' effect/state. | 1 ||
| `ScatterRandomPickups` | `Number` | Applies or references the 'ScatterRandomPickups' effect/state. | 1 ||
| [`ScrambleLastUsedSpell`](#object-scramblelastusedspell) | Object | Randomizes or scrambles the properties of the last spell cast. | 1 ||
| `ShadowCrit` | `Number` | Applies or references the 'ShadowCrit' effect/state. | 1 ||
| `ShootHereCommand` | `Number` | Applies or references the 'ShootHereCommand' effect/state. | 1 ||
| `ShootHereReceiver` | `Number` | Applies or references the 'ShootHereReceiver' effect/state. | 1 ||
| `SmallHitExplosion` | `Number` | Applies or references the 'SmallHitExplosion' effect/state. | 1 ||
| `SmellBlood` | `Number` | Applies or references the 'SmellBlood' effect/state. | 1 ||
| [`SoundEventOnHit`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'SoundEventOnHit' effect/state. | 1 ||
| [`SourceSwapsBackEndOfTurn`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'SourceSwapsBackEndOfTurn' effect/state. | 1 ||
| `SpawnWebTrap` | `Number` | Applies or references the 'SpawnWebTrap' effect/state. | 1 ||
| [`SpecialBossMultipartInstakill`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'SpecialBossMultipartInstakill' effect/state. | 1 ||
| `SpitConsumed` | `Number` | Applies or references the 'SpitConsumed' effect/state. | 1 ||
| `SplashDamage` | `Number` | Applies or references the 'SplashDamage' effect/state. | 1 ||
| `StackingSandstorm` | `Number` | Applies or references the 'StackingSandstorm' effect/state. | 1 ||
| `StealDemonicGlyph` | `Number` | Applies or references the 'StealDemonicGlyph' effect/state. | 1 ||
| [`StealEquipment`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'StealEquipment' effect/state. | 1 ||
| `StealthCritChance` | `Number` | Applies or references the 'StealthCritChance' effect/state. | 1 ||
| `StealTurn` | `Number` | Applies or references the 'StealTurn' effect/state. | 1 ||
| `SwapHighestAndLowestStat` | `Number` | Applies or references the 'SwapHighestAndLowestStat' effect/state. | 1 ||
| [`SwapWeapon`](#object-swapweapon) | Object | Replaces the character's currently equipped weapon with one from a specified pool. | 1 ||
| `T3HitlerTriggerInitialSpawns` | `Number` | Applies or references the 'T3HitlerTriggerInitialSpawns' effect/state. | 1 ||
| [`TagMetronome`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'TagMetronome' effect/state. | 1 ||
| `TakeExtraTurnEndOfRound` | `Number` | Applies or references the 'TakeExtraTurnEndOfRound' effect/state. | 1 ||
| `TargetedMetronome` | `Number` | Applies or references the 'TargetedMetronome' effect/state. | 1 ||
| [`TeamBonusAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'TeamBonusAbility' effect/state. | 1 ||
| [`TeleportBackAtTurnEnd`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'TeleportBackAtTurnEnd' effect/state. | 1 ||
| `TempBackstabBleed` | `Number` | Applies or references the 'TempBackstabBleed' effect/state. | 1 ||
| `TempBackstabPiercing` | `Number` | Applies or references the 'TempBackstabPiercing' effect/state. | 1 ||
| `TempBackstabPoison` | `Number` | Applies or references the 'TempBackstabPoison' effect/state. | 1 ||
| `TempBasicAttackBonusAOE` | `Number` | Applies or references the 'TempBasicAttackBonusAOE' effect/state. | 1 ||
| `TempLuckUp` | `Number` | Applies or references the 'TempLuckUp' effect/state. | 1 ||
| `TempPenetrate` | `Number` | Applies or references the 'TempPenetrate' effect/state. | 1 ||
| `ThornsDamageImmuneUntilSettled` | `Number` | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. | 1 ||
| [`TickDownStatus`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'TickDownStatus' effect/state. | 1 ||
| `TileDamageImmuneUntilSettled` | `Number` | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. | 1 ||
| [`TransformBasicMove`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'TransformBasicMove' effect/state. | 1 ||
| [`TransformEquipment`](#object-transformequipment) | Object | Upgrades or transforms a specific equipped item into another. | 1 ||
| [`TransformNow`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'TransformNow' effect/state. | 1 ||
| `Trapper_Status` | `Number` | Applies or references the 'Trapper_Status' effect/state. | 1 ||
| `TriggerGameEnding` | `Number` | Applies or references the 'TriggerGameEnding' effect/state. | 1 ||
| `TriggerMotherConsume` | `Number` | Applies or references the 'TriggerMotherConsume' effect/state. | 1 ||
| `TriggerMotherGrow` | `Number` | Applies or references the 'TriggerMotherGrow' effect/state. | 1 ||
| `TurnAround` | `Number` | Applies or references the 'TurnAround' effect/state. | 1 ||
| [`TurnControlDelay`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'TurnControlDelay' effect/state. | 1 ||
| `TurnRight` | `Number` | Applies or references the 'TurnRight' effect/state. | 1 ||
| `UndoDamage` | `Number` | Applies or references the 'UndoDamage' effect/state. | 1 ||
| [`UseMoveAbilityWithAI`](#object-usemoveabilitywithai) | Object | Forces the character to execute a movement ability using specific AI weights. | 1 ||
| `VaporizeDice` | `Number` | Applies or references the 'VaporizeDice' effect/state. | 1 ||
| [`VisualCountDownThenApplyStatus`](#object-visualcountdownthenapplystatus) | Object | Displays a visual countdown above the target before applying the nested effects. | 1 ||
| [`WaggleClone`](#object-waggleclone) | Object | Spawns visual clones or alternative hitbox variants of the projectile. | 1 ||
| [`Attraction`](./Enums.md) | Integer || 1 | 1 |
| [`Bloodzerked`](./Enums.md) | Integer || 1 | 1 |
| [`ChampionUpgradeNextMinion`](./Enums.md) | Integer || 1 | 1 |
| [`ChangeTilesUnder`](./Enums.md) | Enum || 1 | LavaTile |
| [`ChargeFists`](./Enums.md) | Integer || 1 | 1 |
| [`CreateGlobalModifiers`](#object-createglobalmodifiers) | Object || 1 ||
| [`DoubleCast`](./Enums.md) | Integer || 1 | 1 |
| [`DrinkWater`](./Enums.md) | Integer || 1 | 1 |
| [`EliteUpgradeNextMinion`](./Enums.md) | Integer || 1 | 1 |
| [`EmptyMind`](./Enums.md) | Integer || 1 | 1 |
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer || 1 | 1 |
| [`FireArmor`](./Enums.md) | Integer || 1 | 1 |
| [`FireArmor2`](./Enums.md) | Integer || 1 | 1 |
| [`ForceUseAbility`](./Enums.md) | Enum || 1 | MotherTumorGrow |
| [`GainCoinsRange`](#object-gaincoinsrange) | Object || 1 ||
| [`HealRandomInjury`](./Enums.md) | Integer || 1 | 1 |
| [`HeavyHits`](./Enums.md) | Integer || 1 | 1 |
| [`IceArmor`](./Enums.md) | Integer || 1 | 1 |
| [`Infested`](./Enums.md) | Integer || 1 | 1 |
| [`Invulnerable`](./Enums.md) | Integer || 1 | 1 |
| [`Meaty`](./Enums.md) | Integer || 1 | 1 |
| [`Muted`](./Enums.md) | Integer || 1 | 1 |
| [`NextAbilityHeals`](./Enums.md) | Integer || 1 | 1 |
| [`NextActionLuckUp`](./Enums.md) | Integer || 1 | 99 |
| [`NextDamageReduceAndHealAllies`](./Enums.md) | Integer || 1 | 1 |
| [`NextTurnDoubleRangedDamage`](./Enums.md) | Integer || 1 | 1 |
| [`NonStackingDivineShield`](./Enums.md) | Integer || 1 | 1 |
| [`PermanentDexterity`](./Enums.md) | Integer || 1 | 2 |
| [`PermanentImmobile`](./Enums.md) | Integer || 1 | 1 |
| [`PermanentIntelligence`](./Enums.md) | Integer || 1 | 2 |
| [`PermanentSpeed`](./Enums.md) | Integer || 1 | 2 |
| [`ProbeCharmed`](./Enums.md) | Integer || 1 | 1 |
| [`RandomPermanentStat`](./Enums.md) | Integer || 1 | 1 |
| [`ReduceManaCost`](./Enums.md) | Integer || 1 | 1 |
| [`ReduceManaCostExcludeBrainstorm`](./Enums.md) | Integer || 1 | 1 |
| [`Regurge`](./Enums.md) | Integer || 1 | 1 |
| [`SetDefaultFace`](./Enums.md) | Enum || 1 | insane |
| [`ShortCircuit`](./Enums.md) | Integer || 1 | 1 |
| [`SpawnCoinAnywhere`](./Enums.md) | Array / Integer || 1 | [.5] |
| [`SpellShield`](./Enums.md) | Integer || 1 | 1 |
| [`StatBounty`](./Enums.md) | Integer || 1 | 1 |
| [`StatusGroup`](#object-statusgroup) | Object || 1 ||
| [`Switcheroo`](./Enums.md) | Integer || 1 | 1 |
| [`Taunting`](./Enums.md) | Integer || 1 | 1 |
| [`TempBackstab`](./Enums.md) | Integer || 1 | 75 |
| [`TempBonusKnockback`](./Enums.md) | Integer || 1 | 1 |
| [`TempBonusKnockbackDamage`](./Enums.md) | Integer || 1 | 1 |
| [`TempCounterAttack`](./Enums.md) | Integer || 1 | 1 |
| [`TempInjuryImmunity`](./Enums.md) | Integer || 1 | 1 |
| [`TempManaCostReduction`](./Enums.md) | Integer || 1 | 1 |
| [`TempPreEmptiveCounterAttack`](./Enums.md) | Integer || 1 | 1 |
| [`TilesMovedToCritChance`](./Enums.md) | Integer || 1 | 1 |
| [`TilesMovedToMana`](./Enums.md) | Integer || 1 | 1 |
| [`TilesMovedToNeighborHeal`](./Enums.md) | Enum || 1 | level |
| [`TilesMovedToStrength`](./Enums.md) | Integer || 1 | 1 |
| [`TowerDefenseStatus`](./Enums.md) | Integer || 1 | 1 |
| [`TowerDefenseStatus2`](./Enums.md) | Integer || 1 | 1 |
| [`VaporizeCorpseFlipAdvantage`](./Enums.md) | Array || 1 | [.33] |

</details>

---


---

## Auto-Discovered Objects


### Object: `cWaggle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

### Object: `cWaggle2x2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

### Object: `cWaggle3x3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>
