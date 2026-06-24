# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Abilities & Spells

> **Associated Files:** `data/abilities/, data/ability_templates/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2343

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage_instance`](./Abilities_and_Spells.md#object-damage_instance) | Object | Block defining the combat math and status effects applied upon successful hit. | 2343 |
| [`meta`](./Abilities_and_Spells.md#object-meta) | Object | Block defining UI display data (Name, Description, Icon). | 2333 |
| [`template`](./Enums.md#enum-template) | Enum | Inherits baseline internal logic from a hardcoded engine template. | 2174 |
| [`graphics`](./Abilities_and_Spells.md#object-graphics) | Object | Block defining visual animations and sequence timings. | 2037 |
| [`target`](./Abilities_and_Spells.md#object-target) | Object | Block defining the shape, range, and restrictions of the ability's aiming phase. | 1862 |
| [`cost`](./Abilities_and_Spells.md#object-cost) | Object | Block defining resource requirements (Mana, Act Points, Moves) needed to cast. | 1851 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1274 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum | Inherits properties from a previously defined ability (used for upgrading tiers). | 900 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 890 |
| [`tags`](./Arrays.md#array-tags) | Array | Array of string categories used by the engine for filtering (e.g. [weapon_throw, spell]). | 238 |
| [`spawn`](./Abilities_and_Spells.md#object-spawn) | Object | Parameters for summoning new characters, objects, or entities. | 192 |
| [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives) | Object | Passives granted to the character while this ability is equipped. | 136 |
| [`class`](./Enums.md#enum-class) | Enum | Categorizes the ability for specific UI filters. | 90 |
| [`temporary_effects`](./Abilities_and_Spells.md#object-temporary_effects) | Object | Status applications that wear off automatically or at the end of the turn. | 88 |
| [`sounds`](./Abilities_and_Spells.md#object-sounds) | Object | Audio cues triggered by the ability. | 39 |
| [`splash_damage`](./Abilities_and_Spells.md#object-splash_damage) | Object | Secondary Area of Effect blast parameters. | 34 |
| [`ai_ability`](./Enums.md#enum-ai_ability) | Enum | Overrides the ability used when triggered by AI. | 29 |
| [`keyword_tooltips`](./Abilities_and_Spells.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear when hovering over the ability. | 23 |
| [`chain_ability`](./Enums.md#enum-chain_ability) | Enum | An ability that automatically executes sequentially after this one. | 15 |
| [`sub_ability`](./Enums.md#enum-sub_ability) | Enum | A secondary ability component referenced by complex templates. | 8 |
| [`cloned_ability`](./Enums.md#enum-cloned_ability) | Enum | Copies the properties of another ability dynamically. | 2 |
| [`empty_self_damage`](./Abilities_and_Spells.md#object-empty_self_damage) | Object | Recoil damage specifically applied when the attack misses all targets. | 2 |
| [`bonk_damage`](./Abilities_and_Spells.md#object-bonk_damage) | Object | Damage dealt when knocked into a wall or obstacle. | 1 |
| [`damage`](./Abilities_and_Spells.md#object-damage) | Object | The base damage properties of an attack. | 1 |
| `accuracy` | Enum/String | Hit chance modifier. | 0 |
| `ai_base_score` | Number |  | 0 |
| `blocked_damage` | Enum/String | Base damage dealt if the attack is blocked. | 0 |
| `blocked_multiplier` | Number | Multiplier applied when hitting a blocking target. | 0 |
| `can_collect_pickups` | Boolean | The damage instance can grab items on the ground. | 0 |
| `can_instapop` | Boolean | Allows the attack to instantly destroy specific weak entities. | 0 |
| `can_revive` | Boolean | Healing instance that can bring dead allies back to life. | 0 |
| `cant_miss` | Boolean |  | 0 |
| `chapter` | Enum/String |  | 0 |
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. | 0 |
| `crit_chance` | Number |  | 0 |
| `custom_additional_ai_weight` | Enum/String |  | 0 |
| `damage_shield_only` | Boolean | Depletes shields but cannot harm base health. | 0 |
| `disallow_modifications` | Boolean | Prevents passives from altering this damage instance. | 0 |
| `durability` | Number | Consumes item durability. | 0 |
| `effects` | Block | Non-damaging status applications and logic triggers executed on impact. | 0 |
| `elements` | Array |  | 0 |
| `faction` | Enum/String |  | 0 |
| `final_hit_bonus_damage` | Enum/String | Extra damage applied on the last hit of a multihit. | 0 |
| `force_adjacent_and_diagonal_contact` | Boolean | Treats diagonal hits as physical contact. | 0 |
| `force_no_contact` | Boolean | Bypasses all contact-based retaliation (Thorns, etc). | 0 |
| `force_no_knockback` | Boolean |  | 0 |
| `force_play_hit_animation` | Boolean |  | 0 |
| `heal` | Number |  | 0 |
| `hint_dont_lowgravboost` | Boolean | AI hint to ignore wind physics. | 0 |
| `hit_animation_alt` | Enum/String | Custom flinch animation for the target. | 0 |
| `incidentally_collects_pickups` | Boolean | Automatically grabs items in the AoE. | 0 |
| `knockback` | Number | Knockback force of the splash blast. | 0 |
| `layer` | Enum/String |  | 0 |
| `makes_contact` | Boolean |  | 0 |
| `non_lethal` | Boolean |  | 0 |
| `override_trample_damage` | Boolean |  | 0 |
| `piercing` | Boolean |  | 0 |
| `ranged` | Boolean | Boolean flagging the damage as explicitly ranged. | 0 |
| `raw_damage` | Enum/String | Unmitigated, unscaled base numbers. | 0 |
| `raw_heal` | String | Unmitigated, unscaled base numbers. | 0 |
| `self_damage` | `Block` | Recoil or self-inflicted damage/effects applied to the caster. | 0 |
| `show_damage_on_0` | Boolean | Forces the "-0" floater text to appear. | 0 |
| `two_way_contact` | Boolean | Both caster and target trigger contact effects on each other. | 0 |
| `damage` | Number | The base damage properties of an attack. | 0 |

</details>

---

### Object: `damage_instance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2344

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#object-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1789 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1731 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1448 |
| `damage` | Number | The base damage properties of an attack. | 1446 |
| [`type`](./Enums.md#enum-type) | Enum | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). | 358 |
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 352 |
| `knockback` | Mixed | The base physics pushing power (in tiles). | 254 |
| `ai_base_score` | Number | How highly the AI values using this ability. | 223 |
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. | 14 |
| [`faction`](./Enums.md#enum-faction) | Enum | Determines alignment (`enemies`, `cats`, `neutral`). | 1 |
| `accuracy` | `Enum/String` | Hit chance modifier. | 0 |
| `blocked_damage` | `Enum/String` | Base damage dealt if the attack is blocked. | 0 |
| `blocked_multiplier` | `Number` | Multiplier applied when hitting a blocking target. | 0 |
| `can_collect_pickups` | `Boolean` | The damage instance can grab items on the ground. | 0 |
| `can_instapop` | `Boolean` | Allows the attack to instantly destroy specific weak entities. | 0 |
| `can_revive` | `Boolean` | Healing instance that can bring dead allies back to life. | 0 |
| `cant_miss` | `Boolean` | Guarantees the hit, bypassing dodge mechanics. | 0 |
| `crit_chance` | `Number` | Override for base critical hit probability. | 0 |
| `custom_additional_ai_weight` | `Enum/String` | Granular AI preference adjustments (e.g., `prefer_dont_move`). | 0 |
| `damage_shield_only` | `Boolean` | Depletes shields but cannot harm base health. | 0 |
| `disallow_modifications` | `Boolean` | Prevents passives from altering this damage instance. | 0 |
| `effects` | `Block` | Non-damaging status applications and logic triggers executed on impact. | 0 |
| `final_hit_bonus_damage` | `Enum/String` | Extra damage applied on the last hit of a multihit. | 0 |
| `force_adjacent_and_diagonal_contact` | `Boolean` | Treats diagonal hits as physical contact. | 0 |
| `force_no_contact` | `Boolean` | Bypasses all contact-based retaliation (Thorns, etc). | 0 |
| `force_no_knockback` | `Boolean` | Prevents the target from being pushed. | 0 |
| `force_play_hit_animation` | `Boolean` | Forces the flinch animation even on 0 damage. | 0 |
| `heal` | `Number` | Restores health instead of dealing damage. | 0 |
| `hint_dont_lowgravboost` | `Boolean` | AI hint to ignore wind physics. | 0 |
| `hit_animation_alt` | `Enum/String` | Custom flinch animation for the target. | 0 |
| `incidentally_collects_pickups` | `Boolean` | Automatically grabs items in the AoE. | 0 |
| `layer` | `Enum/String` | Z-index targeting (e.g., `characters`, `self`). | 0 |
| `makes_contact` | `Boolean` | If false, explicitly avoids triggering contact-based passives. | 0 |
| `non_lethal` | `Boolean` | Reduces target to 1 HP but will never kill. | 0 |
| `override_trample_damage` | `Boolean` | Custom damage value for trample moves. | 0 |
| `piercing` | `Boolean` | Ignores a percentage of target defense/armor. | 0 |
| `raw_damage` | `Enum/String` | Unmitigated, unscaled base numbers. | 0 |
| `raw_heal` | `String` | Unmitigated, unscaled base numbers. | 0 |
| `show_damage_on_0` | `Boolean` | Forces the "-0" floater text to appear. | 0 |
| `two_way_contact` | `Boolean` | Both caster and target trigger contact effects on each other. | 0 |

</details>

---

### Object: `meta`
### Object: `meta`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2333

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String | The localization key for the ability's display description. | 1641 |
| [`name`](./Strings.md#string-name) | String | The localization key for the ability's display name. | 1597 |
| [`class`](./Enums.md#enum-class) | Enum | Categorizes the ability for specific UI filters. | 876 |
| [`type_icon`](./Strings.md#string-type_icon) | String |  | 283 |
| `animate_name` | Boolean | If true, adds a visual pop/animation to the name text when cast. | 177 |
| `icon_shell_frame` | Mixed |  | 28 |
| `is_move` | Mixed |  | 20 |
| [`ability_icon`](./Enums.md#enum-ability_icon) | Enum | The UI icon to display in the action bar. | 14 |
| [`tooltip_values`](./Arrays.md#array-tooltip_values) | Array |  | 9 |
| [`icon_damage_display`](./Strings.md#string-icon_damage_display) | String |  | 8 |
| [`icon_damage_display_eq`](./Math_Equations.md) | Equation |  | 7 |
| `is_basic_attack` | Boolean |  | 4 |
| [`icon_damage_type`](./Enums.md#enum-icon_damage_type) | Enum |  | 3 |
| `is_trinket` | Boolean |  | 3 |
| `dont_visualize_ai` | Boolean |  | 2 |
| [`icon_damage_display_suffix`](./Strings.md#string-icon_damage_display_suffix) | String |  | 2 |
| `is_weapon` | Boolean |  | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |

</details>

---

### Object: `graphics`
### Object: `graphics`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2037

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | The primary flash animation label triggered. | 1559 |
| [`particle`](./Enums.md#enum-particle) | Enum | References an impact or cast particle effect. | 488 |
| [`projectile`](./Enums.md#enum-projectile) | Enum | References a projectile entity. | 228 |
| `lob` | Boolean |  | 130 |
| `delay` | Number | Frame delay before firing projectile/effect. | 93 |
| `dont_visualize_ai` | Boolean |  | 86 |
| `dont_orient` | Boolean | Prevents the character from turning to face the target. | 83 |
| [`dash_animation`](./Enums.md#enum-dash_animation) | Enum | State-specific animations for trample/dash abilities. | 65 |
| [`dash_start_animation`](./Enums.md#enum-dash_start_animation) | Enum |  | 63 |
| `speed` | Number | Rotations per second. | 61 |
| [`affected_particle`](./Enums.md#enum-affected_particle) | Enum | Visuals applied to the target receiving the effect. | 51 |
| [`dash_attack_animation`](./Enums.md#enum-dash_attack_animation) | Enum |  | 45 |
| `lob_height` | Number | Adjustments for arcing projectiles. | 45 |
| [`animation_in`](./Enums.md#enum-animation_in) | Enum | Used for transition states (like burrowing). | 43 |
| [`animation_out`](./Enums.md#enum-animation_out) | Enum | Used for transition states (like burrowing). | 43 |
| [`jump_attack_animation`](./Enums.md#enum-jump_attack_animation) | Enum | Overrides for jump physics. | 39 |
| `use_projectile` | Boolean |  | 35 |
| [`full_jump_animation`](./Enums.md#enum-full_jump_animation) | Enum |  | 24 |
| `full_jump_sync_frames` | Number |  | 24 |
| `use_rotation` | Boolean |  | 24 |
| [`dash_end_animation`](./Enums.md#enum-dash_end_animation) | Enum |  | 22 |
| `palette` | Number | Swaps the color palette ID. | 21 |
| `full_jump_windup_frames` | Number |  | 20 |
| `visual_delay_but_simultaneous_damage` | Number |  | 18 |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum | Specific spawn points for particles. | 17 |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum | Specific spawn points for particles. | 16 |
| `fall_from_sky` | Boolean | Spawns the projectile from the top of the screen. | 16 |
| [`move_start_animation`](./Enums.md#enum-move_start_animation) | Enum |  | 14 |
| `use_placeholder` | Boolean |  | 14 |
| [`move_end_animation`](./Enums.md#enum-move_end_animation) | Enum |  | 13 |
| `face_toss_target` | Boolean |  | 12 |
| `ignore_slowtiles` | Boolean |  | 12 |
| [`chain_distance`](./Enums.md#enum-chain_distance) | Enum | Creates a tethered repeating graphic (like a hook). | 11 |
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
| `max_tiles_single_loop` | Number |  | 9 |
| [`random_delay`](./Arrays.md#array-random_delay) | Array | Adds chaotic timing to multi-projectile casts. | 9 |
| `sync_speed` | Number |  | 9 |
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
| [`fall_randomize_timing`](./Enums.md#enum-fall_randomize_timing) | Enum |  | 6 |
| `min_throw_height` | Number |  | 6 |
| [`miss_random_delay`](./Arrays.md#array-miss_random_delay) | Array |  | 6 |
| `single_projectile` | Boolean |  | 6 |
| [`detatched_animation`](./Enums.md#enum-detatched_animation) | Enum | Plays an animation separated from the character body. | 5 |
| `detatched_animation_reach` | Number |  | 5 |
| [`empty_animation`](./Enums.md#enum-empty_animation) | Enum |  | 5 |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 5 |
| `fixed_jump_height` | Number |  | 4 |
| [`rocket_swirl`](#object-rocket_swirl) | Object | Visual parameters for swirling projectile paths. | 4 |
| `sync_frames` | Number |  | 4 |
| [`dash_decelerating_animation`](./Enums.md#enum-dash_decelerating_animation) | Enum |  | 3 |
| `decelerate` | Number | Visual slowdown at the end of a movement. | 3 |
| `delay_from_map_edge` | Boolean | Delays effect based on distance from the screen edge. | 3 |
| `easing` | Number | Smoothing function for movement animations. | 3 |
| [`fixed_jump_speed`](./Enums.md#enum-fixed_jump_speed) | Number |  | 3 |
| [`grab_animation`](./Enums.md#enum-grab_animation) | Enum |  | 3 |
| [`lob_yoff`](./Enums.md#enum-lob_yoff) | Enum | Adjustments for arcing projectiles. | 3 |
| `lock_orientation_during_dash` | Boolean | Prevents the sprite from flipping mid-dash. | 3 |
| `use_projectile_spawn_offset` | Boolean |  | 3 |
| `use_rotation_once` | Boolean |  | 3 |
| `always_play_animations` | Boolean | Bypasses speed-up/skip logic. | 2 |
| `detatched_animation_cutoff` | Boolean |  | 2 |
| `do_damage_immediately` | Boolean | Applies math before the animation actually hits. | 2 |
| `jump_height_multiplier` | Enum | Overrides for jump physics. | 2 |
| [`mask_center`](./Enums.md#enum-mask_center) | Enum |  | 2 |
| [`mask_extent`](./Enums.md#enum-mask_extent) | Enum |  | 2 |
| `max_throw_height` | Number |  | 2 |
| [`particle_mat`](./Enums.md#enum-particle_mat) | Enum |  | 2 |
| [`preturn_animation`](./Enums.md#enum-preturn_animation) | Enum |  | 2 |
| [`primed_alt_animation`](./Strings.md#string-primed_alt_animation) | String |  | 2 |
| [`pseudoprojectile`](./Enums.md#enum-pseudoprojectile) | Enum |  | 2 |
| `reverse_orientation` | Boolean |  | 2 |
| `self_damage_mid_port` | Boolean |  | 2 |
| `throw_speed` | Number |  | 2 |
| `use_hit_alts` | Boolean |  | 2 |
| [`affected_animation`](./Enums.md#enum-affected_animation) | Enum | Visuals applied to the target receiving the effect. | 1 |
| [`ally_animation`](./Enums.md#enum-ally_animation) | Enum | Distinct animation used when targeting a friendly unit. | 1 |
| [`animate_name`](./Enums.md#enum-animate_name) | String | Animates the ability name text on cast. | 1 |
| `apex_distance` | Number | Calculations for the peak of a jump/lob arc. | 1 |
| [`apex_time`](./Enums.md#enum-apex_time) | Enum | Calculations for the peak of a jump/lob arc. | 1 |
| `bypass_combatspeed` | Boolean |  | 1 |
| [`damage_threshold_altanimations`](#object-damage_threshold_altanimations) | Object | Triggers different hit animations based on the amount of damage dealt. | 1 |
| [`dash_bonk_animation`](./Enums.md#enum-dash_bonk_animation) | Enum |  | 1 |
| `delay_from_map_center` | Boolean | Positional based timing delays. | 1 |
| `delay_from_reverse_map_edge` | Boolean |  | 1 |
| `do_animation_offscreen` | Boolean |  | 1 |
| `do_not_clear_placeholder` | Boolean |  | 1 |
| `face_targets` | Boolean | Forces the sprite to look at the target tile. | 1 |
| `first_castpoint_is_self_damage_only` | Boolean |  | 1 |
| [`hang_time`](./Enums.md#enum-hang_time) | Enum |  | 1 |
| `jump_speed_multiplier` | Number |  | 1 |
| [`lob_speed`](./Enums.md#enum-lob_speed) | Enum | Adjustments for arcing projectiles. | 1 |
| `max_range` | Number | The maximum and minimum distance required to cast. | 1 |
| `min_range` | Number | The maximum and minimum distance required to cast. | 1 |
| `othercat_placeholder_available` | Boolean |  | 1 |
| [`precast_delay`](./Enums.md#enum-precast_delay) | Enum |  | 1 |
| [`spawn_offset`](./Arrays.md#array-spawn_offset) | Array |  | 1 |
| `uncatchable` | Boolean |  | 1 |
| `use_directional_animations` | Boolean |  | 1 |
| `use_origin_offsets` | Boolean |  | 1 |

</details>

---

### Object: `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2012

> **Referenced by:** [`DoDamage`](./Abilities_and_Spells.md#object-dodamage), [`MeleeRevengeDamage`](./Abilities_and_Spells.md#object-meleerevengedamage), [`ROOT`](./Abilities_and_Spells.md#object-root), [`RevengeDamage`](./Abilities_and_Spells.md#object-revengedamage), [`bonk_damage`](./Abilities_and_Spells.md#object-bonk_damage), [`damage_instance`](./Abilities_and_Spells.md#object-damage_instance), [`empty_self_damage`](./Abilities_and_Spells.md#object-empty_self_damage), [`self_damage`](./Abilities_and_Spells.md#object-self_damage), [`splash_damage`](./Abilities_and_Spells.md#object-splash_damage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1886 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 552 |
| `AIFavorLowHealth` | `Number` | Applies or references the 'AIFavorLowHealth' effect/state. | 0 |
| `AddLeechesStatus` | Number | Applies or references the 'AddLeechesStatus' effect/state. | 0 |
| `AddSpiritBombCharges` | `Number` | Applies or references the 'AddSpiritBombCharges' effect/state. | 0 |
| `AddWeaponAux` | Number | Applies or references the 'AddWeaponAux' effect/state. | 0 |
| `AlliesTakeExtraTurn` | `Number` | Applies or references the 'AlliesTakeExtraTurn' effect/state. | 0 |
| `AlternateIdleAnimation` | `Enum/String` | Applies or references the 'AlternateIdleAnimation' effect/state. | 0 |
| `ApplyMultipleTimes` | `Block` | A loop block that executes its nested logic multiple times. | 0 |
| `ApplyPassives` | Block | Grants the nested passive abilities dynamically. | 0 |
| `ApplyShieldToApplierBasedOnMaxHealth` | `Number` | Applies or references the 'ApplyShieldToApplierBasedOnMaxHealth' effect/state. | 0 |
| `ApplyStatusIfCrit` | `Block` | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. | 0 |
| `ApplyStatusesNextTurnBegin` | `Block` | Delays the application of the nested status effects until the start of the target's next turn. | 0 |
| `ApplyToConsumed` | `Block` | Redirects the nested effects to apply to the entity that just consumed this object. | 0 |
| `ApplyToOthersWithSharedTagAndFaction` | `Block` | Redirects the nested effects to apply to all other entities on the map that share the target's faction and specified tags. | 0 |
| `ApplyToRandomClosestAlly` | `Block` | Redirects the nested effects to apply to the nearest friendly unit. If tied, chooses randomly among them. | 0 |
| `ApplyToRandomPartyMemberIfPossible` | Block | Redirects the nested effects to apply to a random living member of the player's party. | 0 |
| `ApplyToSource` | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `ApplyToSourceOnKill` | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 0 |
| `ApplyToTile` | Block | Redirects the nested effects to apply to the terrain/tile underneath the target rather than the target itself. | 0 |
| `ArcLightning` | `Block` | Executes a chain-lightning logic block that bounces between targets. | 0 |
| `BombRatTurtle` | `Number` | Applies or references the 'BombRatTurtle' effect/state. | 0 |
| `BonusCritChance` | Number | Applies or references the 'BonusCritChance' effect/state. | 0 |
| `BonusDamage` | String | Applies or references the 'BonusDamage' effect/state. | 0 |
| `BonusDamageBasedOnDistance` | Number | Applies or references the 'BonusDamageBasedOnDistance' effect/state. | 0 |
| `BonusDamageBasedOnMana` | `Number` | Applies or references the 'BonusDamageBasedOnMana' effect/state. | 0 |
| `BonusKnockbackDamage` | `Number` | Applies or references the 'BonusKnockbackDamage' effect/state. | 0 |
| `BounceObject` | `Enum/String` | Spawns a physics object that visually bounces off the target. | 0 |
| `BounceRock` | `Enum/String` | Applies or references the 'BounceRock' effect/state. | 0 |
| `Bound` | `Number` | Applies or references the 'Bound' effect/state. | 0 |
| `BramblesOnHit` | `Number` | Applies or references the 'BramblesOnHit' effect/state. | 0 |
| `BurgleCoin` | `Number` | Applies or references the 'BurgleCoin' effect/state. | 0 |
| `BypassRockKnockback` | `Number` | Applies or references the 'BypassRockKnockback' effect/state. | 0 |
| `CanApplyToInanimate` | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 0 |
| `CancelPrimedAbilities` | `Number` | Applies or references the 'CancelPrimedAbilities' effect/state. | 0 |
| `CanceledQueuedInput` | `Number` | Applies or references the 'CanceledQueuedInput' effect/state. | 0 |
| `CapDamage` | Number | Applies or references the 'CapDamage' effect/state. | 0 |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 0 |
| `CatPartsSizeScaleStatus` | `Block` | Visually scales specific body parts of a character. | 0 |
| `CatPartsTransform` | Block | Transforms specific body parts into different visual variants. | 0 |
| `ChanceToBreak` | Number | Applies or references the 'ChanceToBreak' effect/state. | 0 |
| `ChanceToBreakFree` | `Block` | Provides a probability to escape a grapple or restraining effect. | 0 |
| `ChangeCatClass` | `Enum/String` | Applies or references the 'ChangeCatClass' effect/state. | 0 |
| `ChangeFaction` | `Enum/String` | Applies or references the 'ChangeFaction' effect/state. | 0 |
| `ChangeTile` | `Enum/String` | Transforms the terrain tile under the target. | 0 |
| `ChaosBossFlipMidTeleport` | `Number` | Applies or references the 'ChaosBossFlipMidTeleport' effect/state. | 0 |
| `ChaosBossFormChange` | `Number` | Applies or references the 'ChaosBossFormChange' effect/state. | 0 |
| `CharmedFacingForceAttack` | `Number` | Applies or references the 'CharmedFacingForceAttack' effect/state. | 0 |
| `CharmedForceAttack` | `Number` | Applies or references the 'CharmedForceAttack' effect/state. | 0 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 0 |
| `ClearFinalBossBattlefield` | `Number` | Applies or references the 'ClearFinalBossBattlefield' effect/state. | 0 |
| `ClearStarving` | `Number` | Applies or references the 'ClearStarving' effect/state. | 0 |
| `CloneWeaponTemp` | `Number` | Applies or references the 'CloneWeaponTemp' effect/state. | 0 |
| `CoinTossBounce` | `Enum/String` | Applies or references the 'CoinTossBounce' effect/state. | 0 |
| `CollectsPickups` | `Number` | Applies or references the 'CollectsPickups' effect/state. | 0 |
| `CollectsPickupsWithAltEffects` | `Block` | Triggers alternative nested effects when collecting items or pickups. | 0 |
| `CollideWithConsumed` | `Enum/String` | Applies or references the 'CollideWithConsumed' effect/state. | 0 |
| `CollideWithThrowTarget` | `Number` | Applies or references the 'CollideWithThrowTarget' effect/state. | 0 |
| `CompleteItemQuest` | Enum/String | Applies or references the 'CompleteItemQuest' effect/state. | 0 |
| `Conditional_AbilityTargetIsSelf` | `Block` | Conditional constraint. Nested properties only trigger if this is true. | 0 |
| `Conditional_ActiveWeather_Any` | `Block` | Conditional trigger: Executes nested logic if the current map weather matches any in the list. | 0 |
| `Conditional_AffectedByElement` | `Block` | Conditional trigger: Executes nested logic if the target is currently afflicted by the specified element. | 0 |
| `Conditional_Ally` | `Block` | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 0 |
| `Conditional_Backstab` | `Block` | Conditional trigger: Executes nested logic if the attacker is positioned behind the target. | 0 |
| `Conditional_BadRoll` | `Block` | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. | 0 |
| `Conditional_Boss` | Block | Conditional trigger: Executes nested logic if the target is a Boss. | 0 |
| `Conditional_BossOrBig` | `Block` | Conditional trigger: Executes nested logic if the target is a Boss or has a large size classification. | 0 |
| `Conditional_Buddy` | `Block` | Conditional trigger: Executes nested logic if the target is the caster's summoned buddy/familiar. | 0 |
| `Conditional_CanBeHealed` | `Block` | Conditional trigger: Executes nested logic if the target's health is below maximum and they are capable of receiving healing. | 0 |
| `Conditional_Corpse` | `Block` | Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 0 |
| `Conditional_DebuffRoll` | `Block` | Conditional trigger: Executes nested logic based on a randomized debuff probability. | 0 |
| `Conditional_DestructibleCorpse` | `Block` | Conditional trigger: Executes nested logic if the target is a corpse that can be destroyed or vaporized. | 0 |
| `Conditional_Displaceable` | Block | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 0 |
| `Conditional_Enemy` | `Block` | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 0 |
| `Conditional_Familiar` | `Block` | Conditional trigger: Executes nested logic if the target is a familiar. | 0 |
| `Conditional_FinishedSpawning` | Block | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. | 0 |
| `Conditional_FirstApplicationThisTurn` | `Block` | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 0 |
| `Conditional_FormulaIsPositive` | `Block` | Conditional trigger: Executes nested logic if the evaluated mathematical formula returns a value greater than 0. | 0 |
| `Conditional_GoodRoll` | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 0 |
| `Conditional_HasCleansableDebuffs` | `Block` | Conditional trigger: Executes nested logic if the target currently has negative status effects that can be cleansed. | 0 |
| `Conditional_HasStatus` | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 0 |
| `Conditional_HasTag` | Block | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 0 |
| `Conditional_HealthThreshold` | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 0 |
| `Conditional_InForm` | `Block` | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 0 |
| `Conditional_IsSelf` | `Block` | Conditional trigger: Executes nested logic if the target is the caster themselves. | 0 |
| `Conditional_IsTrample` | `Block` | Conditional trigger: Executes nested logic if the current movement/attack is classified as a trample. | 0 |
| `Conditional_LastHit` | `Block` | Conditional trigger: Executes nested logic if this attack is the final hit of a multi-hit sequence. | 0 |
| `Conditional_LivingPlayerCat` | `Block` | Conditional trigger: Executes nested logic if the target is an alive player-controlled cat. | 0 |
| `Conditional_NotAlly` | `Block` | Conditional trigger: Executes nested logic if the target is NOT friendly to the caster. | 0 |
| `Conditional_NotBig` | `Block` | Conditional trigger: Executes nested logic if the target is NOT classified as large. | 0 |
| `Conditional_NotBoss` | `Block` | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 0 |
| `Conditional_NotBossOrBig` | `Block` | Conditional trigger: Executes nested logic if the target is NEITHER a Boss nor large. | 0 |
| `Conditional_NotShielded` | `Block` | Conditional trigger: Executes nested logic if the target does NOT currently have a Shield status. | 0 |
| `Conditional_Object` | Block | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 0 |
| `Conditional_OncePerBattle` | `Block` | Conditional trigger: Executes nested logic only once per encounter/battle. | 0 |
| `Conditional_PlayerCat` | `Block` | Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 0 |
| `Conditional_RandomChance` | `Block` | Conditional trigger: Executes nested logic based on a flat percentage random roll. | 0 |
| `Conditional_Shielded` | `Block` | Conditional trigger: Executes nested logic if the target currently has a Shield status. | 0 |
| `Conditional_SourceAbilityHasTag` | `Block` | Conditional trigger: Executes nested logic if the ability that triggered this effect has the specified tag. | 0 |
| `Conditional_SourceHasStatus` | `Block` | Conditional trigger: Executes nested logic if the caster currently has the specified status. | 0 |
| `Conditional_Speculative` | Block | A simulation block used by the AI to test hypothetical outcomes before committing to an action. | 0 |
| `ConjureBonusAbility` | `Enum/String` | Adds a temporary bonus ability to the character's hand/deck. | 0 |
| `ConjureRandomAbilityFromCat` | Number | Applies or references the 'ConjureRandomAbilityFromCat' effect/state. | 0 |
| `ConjureSingleUseBonusAbility` | `Enum/String` | Applies or references the 'ConjureSingleUseBonusAbility' effect/state. | 0 |
| `Consumed` | Block | State block triggered when this object or entity is eaten/consumed by another character. | 0 |
| `ContextualHeal` | `Number` | Applies or references the 'ContextualHeal' effect/state. | 0 |
| `CopySpells` | `Number` | Duplicates existing spells currently in the character's hand. | 0 |
| `CorpseVaporizer` | `Number` | Applies or references the 'CorpseVaporizer' effect/state. | 0 |
| `Counterspell` | `Number` | Applies or references the 'Counterspell' effect/state. | 0 |
| `CrackMoonHead` | Number | Applies or references the 'CrackMoonHead' effect/state. | 0 |
| `Craft` | `Block` | Synthesizes or spawns a new item from a specific pool. | 0 |
| `CurrentWeaponAddElectricElement` | `Number` | Applies or references the 'CurrentWeaponAddElectricElement' effect/state. | 0 |
| `CurrentWeaponDamageUp` | Number | Applies or references the 'CurrentWeaponDamageUp' effect/state. | 0 |
| `DamageBasedOnMissingHealth` | `Number` | Applies or references the 'DamageBasedOnMissingHealth' effect/state. | 0 |
| `DamageDistanceAOEFalloff` | `Number` | Applies or references the 'DamageDistanceAOEFalloff' effect/state. | 0 |
| `DamageTrinket` | `Number` | Applies or references the 'DamageTrinket' effect/state. | 0 |
| `DamageWeapon` | `Number` | Applies or references the 'DamageWeapon' effect/state. | 0 |
| `DeathwormUnderground` | `Enum/String` | Applies or references the 'DeathwormUnderground' effect/state. | 0 |
| `DecoySwapper` | `Number` | Applies or references the 'DecoySwapper' effect/state. | 0 |
| `DeferVaporize` | `Number` | Applies or references the 'DeferVaporize' effect/state. | 0 |
| `DelayCastAbility` | `Block` | Queues an ability to be cast automatically after a certain delay or trigger. | 0 |
| `DelayedFury` | `Number` | Applies or references the 'DelayedFury' effect/state. | 0 |
| `DelayedWindCone` | `Block` | Creates a delayed Area of Effect cone. | 0 |
| `DeleteObject` | `Number` | Applies or references the 'DeleteObject' effect/state. | 0 |
| `DeleteTraps` | `Number` | Applies or references the 'DeleteTraps' effect/state. | 0 |
| `DestroyEquipmentAndAttachParasite` | Block | Removes an equipped item and replaces it with a parasite from a specified pool. | 0 |
| `DestroyNeckArmor` | `Number` | Applies or references the 'DestroyNeckArmor' effect/state. | 0 |
| `DestroyTrinket` | `Number` | Applies or references the 'DestroyTrinket' effect/state. | 0 |
| `DestroyWeapon` | `Number` | Applies or references the 'DestroyWeapon' effect/state. | 0 |
| `DestroyWeaponThrow` | `Number` | Applies or references the 'DestroyWeaponThrow' effect/state. | 0 |
| `Die` | `Number` | Applies or references the 'Die' effect/state. | 0 |
| `DieViaAbilityInternally` | `Number` | Applies or references the 'DieViaAbilityInternally' effect/state. | 0 |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. | 0 |
| `DinoLegAnimation` | `Enum/String` | Applies or references the 'DinoLegAnimation' effect/state. | 0 |
| `DisableWeapon` | Number | Applies or references the 'DisableWeapon' effect/state. | 0 |
| `Disguised` | `Number` | Applies or references the 'Disguised' effect/state. | 0 |
| `Displace` | `Number` | Applies or references the 'Displace' effect/state. | 0 |
| `DisplaceToAbilityTarget` | Number | Applies or references the 'DisplaceToAbilityTarget' effect/state. | 0 |
| `DisplaceToOriginalPosition` | `Number` | Applies or references the 'DisplaceToOriginalPosition' effect/state. | 0 |
| `DisplaceTowardsSource` | `Number` | Applies or references the 'DisplaceTowardsSource' effect/state. | 0 |
| `DissolveRandomArmorPiece` | `Number` | Applies or references the 'DissolveRandomArmorPiece' effect/state. | 0 |
| `DoDistortionRing` | `Block` | Creates a visual distortion ring effect on the screen. | 0 |
| `DoScreenShake` | Block | Triggers a camera screen shake effect. | 0 |
| `DontHealEnemies` | `Number` | Applies or references the 'DontHealEnemies' effect/state. | 0 |
| `DoubleCastSpellsEachTurn_Status` | `Number` | Applies or references the 'DoubleCastSpellsEachTurn_Status' effect/state. | 0 |
| `DoubleStatus` | `Enum/String` | Applies or references the 'DoubleStatus' effect/state. | 0 |
| `DrainAllyCatsForFleshGolem` | `Number` | Applies or references the 'DrainAllyCatsForFleshGolem' effect/state. | 0 |
| `DuplicateRandomEquippedItem` | `Number` | Applies or references the 'DuplicateRandomEquippedItem' effect/state. | 0 |
| `DustOnHit` | `Block` | Spawns a specific particle or cloud object upon impact. | 0 |
| `Else` | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 0 |
| `EnableWeather` | `Enum/String` | Applies or references the 'EnableWeather' effect/state. | 0 |
| `EndTurn` | `Number` | Applies or references the 'EndTurn' effect/state. | 0 |
| `Enlarge` | `Number` | Applies or references the 'Enlarge' effect/state. | 0 |
| `EnterMount` | `Enum/String` | Applies or references the 'EnterMount' effect/state. | 0 |
| `EvolveAbilityFromPool` | `Enum/String` | Upgrades or transforms an existing ability into a new one from the specified pool. | 0 |
| `ExistUntilIdleUpkeep` | `Number` | Applies or references the 'ExistUntilIdleUpkeep' effect/state. | 0 |
| `ExplodeCharacter` | `Number` | Applies or references the 'ExplodeCharacter' effect/state. | 0 |
| `ExplodeCharacter_DeathBloom` | `Number` | Applies or references the 'ExplodeCharacter_DeathBloom' effect/state. | 0 |
| `ExplodeCharacter_DeathBloom2` | `Number` | Applies or references the 'ExplodeCharacter_DeathBloom2' effect/state. | 0 |
| `ExplodeCharacter_NoDie` | `Number` | Applies or references the 'ExplodeCharacter_NoDie' effect/state. | 0 |
| `ExplodeCharacter_Party` | Number | Applies or references the 'ExplodeCharacter_Party' effect/state. | 0 |
| `ExplodeCharacter_PartyBoss` | Number | Applies or references the 'ExplodeCharacter_PartyBoss' effect/state. | 0 |
| `ExplodeCharacter_RockCrusher` | Number | Applies or references the 'ExplodeCharacter_RockCrusher' effect/state. | 0 |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Number | Applies or references the 'ExplodeCharacter_RockCrusher_PetrifyBreak' effect/state. | 0 |
| `ExplosionIfHitSomething` | `Number` | Applies or references the 'ExplosionIfHitSomething' effect/state. | 0 |
| `FaceAway` | `Number` | Applies or references the 'FaceAway' effect/state. | 0 |
| `FaceCamera` | `Number` | Applies or references the 'FaceCamera' effect/state. | 0 |
| `FactionConversion` | `Number` | Applies or references the 'FactionConversion' effect/state. | 0 |
| `FactionDisguiseSource` | `Number` | Applies or references the 'FactionDisguiseSource' effect/state. | 0 |
| `FastKnockback` | `Number` | Applies or references the 'FastKnockback' effect/state. | 0 |
| `FillMana` | `Number` | Applies or references the 'FillMana' effect/state. | 0 |
| `FinalBossQueueBeam` | `Number` | Applies or references the 'FinalBossQueueBeam' effect/state. | 0 |
| `FlatAIBonus` | `Number` | Applies or references the 'FlatAIBonus' effect/state. | 0 |
| `FlatLeech` | `Number` | Applies or references the 'FlatLeech' effect/state. | 0 |
| `FloatingRockTrap` | Number | Applies or references the 'FloatingRockTrap' effect/state. | 0 |
| `FlowersOnHit` | `Number` | Applies or references the 'FlowersOnHit' effect/state. | 0 |
| `ForceAttack` | `Number` | Forces the character to execute an immediate attack. | 0 |
| `ForceCollectsPickups` | `Number` | Applies or references the 'ForceCollectsPickups' effect/state. | 0 |
| `ForceDisplace` | `Number` | Applies or references the 'ForceDisplace' effect/state. | 0 |
| `ForceImmediateMove` | Number | Applies or references the 'ForceImmediateMove' effect/state. | 0 |
| `ForceImmediateMoveAndAttack` | Block | Forces the character to immediately move to a target and use a specified ability. | 0 |
| `ForceMoveAndAttack` | `Number` | Applies or references the 'ForceMoveAndAttack' effect/state. | 0 |
| `ForceMoveAway` | `Number` | Applies or references the 'ForceMoveAway' effect/state. | 0 |
| `ForceMoveNonAlliesInRangeTowardsTile` | `Number` | Applies or references the 'ForceMoveNonAlliesInRangeTowardsTile' effect/state. | 0 |
| `ForceMoveTowards` | `Number` | Applies or references the 'ForceMoveTowards' effect/state. | 0 |
| `ForceMoveTowardsEnemies` | `Number` | Applies or references the 'ForceMoveTowardsEnemies' effect/state. | 0 |
| `ForceMoveTowardsTaggedObject` | `Block` | Forces the character to move towards the nearest object with a specific tag. | 0 |
| `ForceTransferWeapon` | `Number` | Applies or references the 'ForceTransferWeapon' effect/state. | 0 |
| `FormChange` | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 0 |
| `GainDisorder` | Enum/String | Applies or references the 'GainDisorder' effect/state. | 0 |
| `GainDisorderFromPool_PostCast` | Enum/String | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 0 |
| `GenericBuff` | `Number` | Applies or references the 'GenericBuff' effect/state. | 0 |
| `GenericDebuff` | `Number` | Applies or references the 'GenericDebuff' effect/state. | 0 |
| `GiveBoundItemToTarget` | `Number` | Applies or references the 'GiveBoundItemToTarget' effect/state. | 0 |
| `GlobalSpawnCharacter` | Enum/String | Applies or references the 'GlobalSpawnCharacter' effect/state. | 0 |
| `HealPercentMaxHP` | `Number` | Applies or references the 'HealPercentMaxHP' effect/state. | 0 |
| `HealTo` | `Number` | Applies or references the 'HealTo' effect/state. | 0 |
| `HitExplosion` | `Number` | Applies or references the 'HitExplosion' effect/state. | 0 |
| `IgnoreDamage` | `Number` | Applies or references the 'IgnoreDamage' effect/state. | 0 |
| `IgnoreDebuffs` | `Number` | Applies or references the 'IgnoreDebuffs' effect/state. | 0 |
| `IgnoreSelf` | `Number` | Applies or references the 'IgnoreSelf' effect/state. | 0 |
| `ImmediateUseAbility` | `Enum/String` | Applies or references the 'ImmediateUseAbility' effect/state. | 0 |
| `ImmediateUseDirectionalAbility` | `Enum/String` | Applies or references the 'ImmediateUseDirectionalAbility' effect/state. | 0 |
| `Imprison` | `Enum/String` | Applies or references the 'Imprison' effect/state. | 0 |
| `IncAuxCounterCycle` | `Block` | Increments a generic auxiliary counter, looping back to 0 when it exceeds the maximum. | 0 |
| `IncreaseCumulativeBlastDamage` | `Number` | Applies or references the 'IncreaseCumulativeBlastDamage' effect/state. | 0 |
| `IncreaseItemAuxOnKill` | `Number` | Applies or references the 'IncreaseItemAuxOnKill' effect/state. | 0 |
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 0 |
| `InstantMaxHealthUp` | `Number` | Applies or references the 'InstantMaxHealthUp' effect/state. | 0 |
| `InterchangeMoveActPoints` | `Number` | Applies or references the 'InterchangeMoveActPoints' effect/state. | 0 |
| `JohnnyCriesForWashers` | `Number` | Applies or references the 'JohnnyCriesForWashers' effect/state. | 0 |
| `KnockOutClone` | Enum/String | Applies or references the 'KnockOutClone' effect/state. | 0 |
| `KnockUpAndAway` | `Block` | Displaces the target vertically and horizontally away from the source. | 0 |
| `KnockbackDamageImmuneUntilSettled` | `Number` | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. | 0 |
| `KnockbackDirectionIsFacingDirection` | `Enum/String` | Applies or references the 'KnockbackDirectionIsFacingDirection' effect/state. | 0 |
| `LateStatusApplication` | `Block` | Applies a status effect after all primary damage and effects have fully resolved. | 0 |
| `LaunchOffScreen` | Enum/String | Applies or references the 'LaunchOffScreen' effect/state. | 0 |
| `LaunchOffScreenInstakill` | Number | Applies or references the 'LaunchOffScreenInstakill' effect/state. | 0 |
| `LeaveBehindRockOnKnockback` | `Number` | Applies or references the 'LeaveBehindRockOnKnockback' effect/state. | 0 |
| `LowerAmbientLight` | Block | A visual effect that dims the map's lighting. | 0 |
| `MadnessChanceOnTurnBegin` | Number | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. | 0 |
| `MakeWeaponUnbreakable` | `Number` | Applies or references the 'MakeWeaponUnbreakable' effect/state. | 0 |
| `ManaGain` | String | Applies or references the 'ManaGain' effect/state. | 0 |
| `ManaSteal` | `Number` | Applies or references the 'ManaSteal' effect/state. | 0 |
| `ManaStealToHealth` | `Number` | Applies or references the 'ManaStealToHealth' effect/state. | 0 |
| `ManglerAttack` | `Number` | Applies or references the 'ManglerAttack' effect/state. | 0 |
| `ManglerShuffle` | `Boolean` | Applies or references the 'ManglerShuffle' effect/state. | 0 |
| `MassAttackThis` | `Number` | Applies or references the 'MassAttackThis' effect/state. | 0 |
| `Math` | `Block` | Triggers the Tinkerer's Math ability sequence. | 0 |
| `MaxHPUp` | `Number` | Applies or references the 'MaxHPUp' effect/state. | 0 |
| `MergeDamageInstance` | Block | Combines damage numbers or visual hit effects. | 0 |
| `Metronome` | `Number` | Executes a random musical or metronome ability. | 0 |
| `MimicMetronome` | `Number` | Applies or references the 'MimicMetronome' effect/state. | 0 |
| `MonkStanceSwitch` | `Number` | Applies or references the 'MonkStanceSwitch' effect/state. | 0 |
| `MotherTumorDebugForcePass` | `Number` | Applies or references the 'MotherTumorDebugForcePass' effect/state. | 0 |
| `NextAttackSpecialCrit` | `Number` | Modifies the character's next attack to have special critical properties. | 0 |
| `NextBasicAttackCritsThisTurn` | `Block` | Guarantees the next basic attack executed this turn will be a critical hit. | 0 |
| `NextBattleStatusStacks` | `Block` | Carries over the specified status effects into the next encounter/battle. | 0 |
| `ObjectOnHit` | `Enum/String` | Spawns a specific physics/item object upon impact. | 0 |
| `ObjectOnHitEmpty` | `Enum/String` | Applies or references the 'ObjectOnHitEmpty' effect/state. | 0 |
| `ObjectOnHitFullyEmpty` | `Enum/String` | Applies or references the 'ObjectOnHitFullyEmpty' effect/state. | 0 |
| `OverHealToShield` | `Number` | Applies or references the 'OverHealToShield' effect/state. | 0 |
| `OverHealToStatuses` | `Block` | Converts excessive healing beyond maximum health into specific status effects. | 0 |
| `OverrideChainKnockback` | `Number` | Applies or references the 'OverrideChainKnockback' effect/state. | 0 |
| `OverrideChainKnockbackDamage` | `Enum/String` | Applies or references the 'OverrideChainKnockbackDamage' effect/state. | 0 |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 0 |
| `OverrideKnockbackDamage` | `Number` | Applies or references the 'OverrideKnockbackDamage' effect/state. | 0 |
| `PartialPurge` | `Number` | Applies or references the 'PartialPurge' effect/state. | 0 |
| `PermanentCharisma` | `Number` | Applies or references the 'PermanentCharisma' effect/state. | 0 |
| `PermanentLuck` | `Number` | Applies or references the 'PermanentLuck' effect/state. | 0 |
| `PermanentStrength` | `Number` | Applies or references the 'PermanentStrength' effect/state. | 0 |
| `PermanentUpgradeRandomActive` | `Number` | Applies or references the 'PermanentUpgradeRandomActive' effect/state. | 0 |
| `PermanentUpgradeRandomActiveOrPassive` | `Number` | Applies or references the 'PermanentUpgradeRandomActiveOrPassive' effect/state. | 0 |
| `PlayBackground` | Number | Applies or references the 'PlayBackground' effect/state. | 0 |
| `PoolMetronome` | `Block` | Executes a random ability drawn from a specific pool. | 0 |
| `PopAndSpawn` | `Enum/String` | Destroys the target and replaces it with a new spawned entity. | 0 |
| `PullSourceToKnockbackImmuneTarget` | `Number` | Applies or references the 'PullSourceToKnockbackImmuneTarget' effect/state. | 0 |
| `PullSourceToTarget` | `Number` | Applies or references the 'PullSourceToTarget' effect/state. | 0 |
| `Purge` | `Number` | Applies or references the 'Purge' effect/state. | 0 |
| `PurgeAll` | `Number` | Applies or references the 'PurgeAll' effect/state. | 0 |
| `QuakeAreaChance` | `Block` | Provides a probability to trigger an earthquake Area of Effect. | 0 |
| `QueueUseAbility` | `Enum/String` | Applies or references the 'QueueUseAbility' effect/state. | 0 |
| `RNGCannonRandomDamage` | `Number` | Applies or references the 'RNGCannonRandomDamage' effect/state. | 0 |
| `RandomBonusDamage` | Number | Applies or references the 'RandomBonusDamage' effect/state. | 0 |
| `RandomDistanceDisplace` | `Number` | Displaces the target by a randomized distance. | 0 |
| `RandomKnockback` | `Block` | Applies a randomized amount of knockback force. | 0 |
| `RandomKnockbackDirection` | `Number` | Applies or references the 'RandomKnockbackDirection' effect/state. | 0 |
| `RandomStatDown` | Number | Applies or references the 'RandomStatDown' effect/state. | 0 |
| `RandomStatusFromPool` | `Block` | Selects and applies a random status effect from the provided nested block. | 0 |
| `Reanimate` | `Number` | Applies or references the 'Reanimate' effect/state. | 0 |
| `RebukeDamage` | `Number` | Applies or references the 'RebukeDamage' effect/state. | 0 |
| `ReformMoonHead` | `Number` | Applies or references the 'ReformMoonHead' effect/state. | 0 |
| `RefreshActPoints` | `Number` | Applies or references the 'RefreshActPoints' effect/state. | 0 |
| `RefreshItemAbilities` | `Number` | Applies or references the 'RefreshItemAbilities' effect/state. | 0 |
| `RefreshMovePoints` | `Number` | Applies or references the 'RefreshMovePoints' effect/state. | 0 |
| `RefreshMovePointsIfHit` | `Number` | Applies or references the 'RefreshMovePointsIfHit' effect/state. | 0 |
| `RefreshNonManaItemAbilities` | `Number` | Applies or references the 'RefreshNonManaItemAbilities' effect/state. | 0 |
| `RefreshOncePerFightAbilities` | `Number` | Applies or references the 'RefreshOncePerFightAbilities' effect/state. | 0 |
| `RefreshWeaponAbility` | `Number` | Applies or references the 'RefreshWeaponAbility' effect/state. | 0 |
| `Regurge` | `Number` | Applies or references the 'Regurge' effect/state. | 0 |
| `RemoveActPoints` | `Number` | Applies or references the 'RemoveActPoints' effect/state. | 0 |
| `RemoveItem` | Enum/String | Applies or references the 'RemoveItem' effect/state. | 0 |
| `RemoveMovePoints` | `Number` | Applies or references the 'RemoveMovePoints' effect/state. | 0 |
| `RemoveStatus` | `Enum/String` | Applies or references the 'RemoveStatus' effect/state. | 0 |
| `RemoveStatusStacks` | `Block` | Removes a specific number of stacks of a status effect. | 0 |
| `RemoveTurnsThisRound` | Number | Applies or references the 'RemoveTurnsThisRound' effect/state. | 0 |
| `RepairAll` | `Number` | Applies or references the 'RepairAll' effect/state. | 0 |
| `RepairAllCondition` | `Number` | Applies or references the 'RepairAllCondition' effect/state. | 0 |
| `RepairArmorCondition` | `Number` | Applies or references the 'RepairArmorCondition' effect/state. | 0 |
| `RepairOnKill` | `Number` | Applies or references the 'RepairOnKill' effect/state. | 0 |
| `RepairWeaponCondition` | `Number` | Applies or references the 'RepairWeaponCondition' effect/state. | 0 |
| `RerollEnemy` | `Number` | Applies or references the 'RerollEnemy' effect/state. | 0 |
| `ResetArmorShield` | `Number` | Applies or references the 'ResetArmorShield' effect/state. | 0 |
| `ReturnDinoLegs` | `Number` | Applies or references the 'ReturnDinoLegs' effect/state. | 0 |
| `Revive` | `Number` | Applies or references the 'Revive' effect/state. | 0 |
| `SafeDie` | `Number` | Applies or references the 'SafeDie' effect/state. | 0 |
| `ScatterHeldCoin` | `Number` | Applies or references the 'ScatterHeldCoin' effect/state. | 0 |
| `ScatterRandomPickups` | `Number` | Applies or references the 'ScatterRandomPickups' effect/state. | 0 |
| `ScrambleEverything` | `Number` | Applies or references the 'ScrambleEverything' effect/state. | 0 |
| `ScrambleLastUsedSpell` | `Block` | Randomizes or scrambles the properties of the last spell cast. | 0 |
| `SelfStun` | `Number` | Applies or references the 'SelfStun' effect/state. | 0 |
| `SendRock` | `Number` | Applies or references the 'SendRock' effect/state. | 0 |
| `SetAnimationAlts` | Block | Overrides specific animation states with alternative animations. | 0 |
| `SetCrazyEyeBackgroundWeights` | `Block` | Adjusts visual rendering weights for the 'Crazy Eye' background effect. | 0 |
| `SetDistanceDisplace` | `Number` | Applies or references the 'SetDistanceDisplace' effect/state. | 0 |
| `SetHealth` | `Number` | Applies or references the 'SetHealth' effect/state. | 0 |
| `SetKnockback` | Number | Applies or references the 'SetKnockback' effect/state. | 0 |
| `SetShield` | `Number` | Applies or references the 'SetShield' effect/state. | 0 |
| `ShadowCrit` | `Number` | Applies or references the 'ShadowCrit' effect/state. | 0 |
| `Shatter` | `Number` | Applies or references the 'Shatter' effect/state. | 0 |
| `ShootHereCommand` | `Number` | Applies or references the 'ShootHereCommand' effect/state. | 0 |
| `ShootHereReceiver` | `Number` | Applies or references the 'ShootHereReceiver' effect/state. | 0 |
| `ShowFakeDamage` | Block | Displays a visual damage number without actually modifying health. | 0 |
| `ShowText` | String | Applies or references the 'ShowText' effect/state. | 0 |
| `SignalFinalBossShieldBroke` | `Number` | Applies or references the 'SignalFinalBossShieldBroke' effect/state. | 0 |
| `SmallHitExplosion` | `Number` | Applies or references the 'SmallHitExplosion' effect/state. | 0 |
| `SmartMetronome` | `Number` | Executes a 'smart' random ability that aims to be beneficial based on context. | 0 |
| `SmellBlood` | `Number` | Applies or references the 'SmellBlood' effect/state. | 0 |
| `SoundEventOnHit` | `Enum/String` | Applies or references the 'SoundEventOnHit' effect/state. | 0 |
| `SourceSwapsBackEndOfTurn` | `Enum/String` | Applies or references the 'SourceSwapsBackEndOfTurn' effect/state. | 0 |
| `SpawnBearTrap` | `Number` | Applies or references the 'SpawnBearTrap' effect/state. | 0 |
| `SpawnBearTrapIfHitKills` | Number | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. | 0 |
| `SpawnCreep` | `Number` | Applies or references the 'SpawnCreep' effect/state. | 0 |
| `SpawnCustomTrap` | `Enum/String` | Applies or references the 'SpawnCustomTrap' effect/state. | 0 |
| `SpawnFlames` | `Array` | Applies or references the 'SpawnFlames' effect/state. | 0 |
| `SpawnNeutralWebTrapOnMiss` | `Number` | Applies or references the 'SpawnNeutralWebTrapOnMiss' effect/state. | 0 |
| `SpawnRock` | `Number` | Applies or references the 'SpawnRock' effect/state. | 0 |
| `SpawnThingIfHitKills` | `Enum/String` | Applies or references the 'SpawnThingIfHitKills' effect/state. | 0 |
| `SpawnWebTrap` | `Number` | Applies or references the 'SpawnWebTrap' effect/state. | 0 |
| `SpecialBossMultipartInstakill` | `Enum/String` | Applies or references the 'SpecialBossMultipartInstakill' effect/state. | 0 |
| `SpecificInjury` | `Enum/String` | Applies or references the 'SpecificInjury' effect/state. | 0 |
| `SpeculativeMoveSelfCorpseOffMap` | `Number` | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 0 |
| `SpitConsumed` | `Number` | Applies or references the 'SpitConsumed' effect/state. | 0 |
| `SplashDamage` | `Number` | Applies or references the 'SplashDamage' effect/state. | 0 |
| `SpreadDisease` | `Block` | Provides a chance to transmit a disease status to adjacent targets. | 0 |
| `StackingSandstorm` | `Number` | Applies or references the 'StackingSandstorm' effect/state. | 0 |
| `StanceSwitchToMelee` | `Number` | Applies or references the 'StanceSwitchToMelee' effect/state. | 0 |
| `StanceSwitchToRanged` | Number | Applies or references the 'StanceSwitchToRanged' effect/state. | 0 |
| `StealDemonicGlyph` | `Number` | Applies or references the 'StealDemonicGlyph' effect/state. | 0 |
| `StealEquipment` | `Enum/String` | Applies or references the 'StealEquipment' effect/state. | 0 |
| `StealTurn` | `Number` | Applies or references the 'StealTurn' effect/state. | 0 |
| `StealthCritChance` | `Number` | Applies or references the 'StealthCritChance' effect/state. | 0 |
| `SwallowSmallCharacter` | `Number` | Applies or references the 'SwallowSmallCharacter' effect/state. | 0 |
| `SwapHighestAndLowestStat` | `Number` | Applies or references the 'SwapHighestAndLowestStat' effect/state. | 0 |
| `SwapWeapon` | `Block` | Replaces the character's currently equipped weapon with one from a specified pool. | 0 |
| `SwitchMusic` | Block | Changes the background music track or layer during combat. | 0 |
| `T2CopyCat` | Number | Applies or references the 'T2CopyCat' effect/state. | 0 |
| `T3HitlerTriggerInitialSpawns` | `Number` | Applies or references the 'T3HitlerTriggerInitialSpawns' effect/state. | 0 |
| `TagMetronome` | `Enum/String` | Applies or references the 'TagMetronome' effect/state. | 0 |
| `TakeBonusTurnWithAIControl` | `Block` | Grants the character an immediate extra turn, but forces the AI to control them during it. | 0 |
| `TakeBonusTurnWithStatus` | `Block` | Grants the character an immediate extra turn while afflicted with specific statuses. | 0 |
| `TakeExtraTurn` | `Number` | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
| `TakeExtraTurnEndOfRound` | `Number` | Applies or references the 'TakeExtraTurnEndOfRound' effect/state. | 0 |
| `TargetedMetronome` | `Number` | Applies or references the 'TargetedMetronome' effect/state. | 0 |
| `TeamBonusAbility` | `Enum/String` | Applies or references the 'TeamBonusAbility' effect/state. | 0 |
| `TeamCastAbility` | `Enum/String` | Requires or involves multiple characters to execute the ability. | 0 |
| `TeleportBackAtTurnEnd` | `Enum/String` | Applies or references the 'TeleportBackAtTurnEnd' effect/state. | 0 |
| `TempBackstabBleed` | `Number` | Applies or references the 'TempBackstabBleed' effect/state. | 0 |
| `TempBackstabPiercing` | `Number` | Applies or references the 'TempBackstabPiercing' effect/state. | 0 |
| `TempBackstabPoison` | `Number` | Applies or references the 'TempBackstabPoison' effect/state. | 0 |
| `TempBasicAttackBonusAOE` | `Number` | Applies or references the 'TempBasicAttackBonusAOE' effect/state. | 0 |
| `TempLuckUp` | `Number` | Applies or references the 'TempLuckUp' effect/state. | 0 |
| `TempPassiveWhileHasStatus` | Block | Grants nested passives only while the character possesses the specified status. | 0 |
| `TempPenetrate` | `Number` | Applies or references the 'TempPenetrate' effect/state. | 0 |
| `TempTrampleUntilSettled` | `Number` | Applies or references the 'TempTrampleUntilSettled' effect/state. | 0 |
| `Temporary` | `Block` | A wrapper block for applying status effects that automatically expire. | 0 |
| `ThornsDamageImmuneUntilSettled` | `Number` | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. | 0 |
| `TickDownStatus` | `Enum/String` | Applies or references the 'TickDownStatus' effect/state. | 0 |
| `TileDamageImmuneUntilSettled` | `Number` | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. | 0 |
| `TimeDelayStatusApplication` | `Block` | Delays the nested effects by a specified amount of real-time seconds. | 0 |
| `TradeLife` | `Number` | Applies or references the 'TradeLife' effect/state. | 0 |
| `TransformAbility` | `Enum/String` | Applies or references the 'TransformAbility' effect/state. | 0 |
| `TransformBasicAttack` | `Enum/String` | Applies or references the 'TransformBasicAttack' effect/state. | 0 |
| `TransformBasicMove` | `Enum/String` | Applies or references the 'TransformBasicMove' effect/state. | 0 |
| `TransformEquipment` | `Block` | Upgrades or transforms a specific equipped item into another. | 0 |
| `TransformNow` | `Enum/String` | Applies or references the 'TransformNow' effect/state. | 0 |
| `TransformWeapon` | Block | Transforms the equipped weapon into another specific weapon state. | 0 |
| `Trapper_Status` | `Number` | Applies or references the 'Trapper_Status' effect/state. | 0 |
| `TriggerDOTStatuses` | `Number` | Applies or references the 'TriggerDOTStatuses' effect/state. | 0 |
| `TriggerGameEnding` | `Number` | Applies or references the 'TriggerGameEnding' effect/state. | 0 |
| `TriggerMotherConsume` | `Number` | Applies or references the 'TriggerMotherConsume' effect/state. | 0 |
| `TriggerMotherGrow` | `Number` | Applies or references the 'TriggerMotherGrow' effect/state. | 0 |
| `TriggerWerewolfTransform` | `Array` | Applies or references the 'TriggerWerewolfTransform' effect/state. | 0 |
| `TurnAround` | `Number` | Applies or references the 'TurnAround' effect/state. | 0 |
| `TurnControlDelay` | `Enum/String` | Applies or references the 'TurnControlDelay' effect/state. | 0 |
| `TurnRight` | `Number` | Applies or references the 'TurnRight' effect/state. | 0 |
| `TwisterDisplaceWithDamage` | `Block` | A whirlwind effect that randomly displaces targets and deals damage. | 0 |
| `UndoDamage` | `Number` | Applies or references the 'UndoDamage' effect/state. | 0 |
| `UpgradeRandomAbility` | `Number` | Applies or references the 'UpgradeRandomAbility' effect/state. | 0 |
| `UseAbility` | `Enum/String` | Forces the character or target to instantly use a specified ability. | 0 |
| `UseMoveAbilityWithAI` | `Block` | Forces the character to execute a movement ability using specific AI weights. | 0 |
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 0 |
| `VaporizeCorpse` | `Number` | Applies or references the 'VaporizeCorpse' effect/state. | 0 |
| `VaporizeCorpseFlipAdvantage` | `Array` | Applies or references the 'VaporizeCorpseFlipAdvantage' effect/state. | 0 |
| `VaporizeDice` | `Number` | Applies or references the 'VaporizeDice' effect/state. | 0 |
| `VaporizeInanimate` | `Number` | Applies or references the 'VaporizeInanimate' effect/state. | 0 |
| `VaporizeTarget` | `Number` | Applies or references the 'VaporizeTarget' effect/state. | 0 |
| `VisualCountDownThenApplyStatus` | `Block` | Displays a visual countdown above the target before applying the nested effects. | 0 |
| `VisualFX` | `Enum/String` | Applies or references the 'VisualFX' effect/state. | 0 |
| `VisualFXTile` | `Enum/String` | Applies or references the 'VisualFXTile' effect/state. | 0 |
| `WaggleClone` | `Block` | Spawns visual clones or alternative hitbox variants of the projectile. | 0 |
| `WeaponAuxMultiplier` | Enum/String | Applies or references the 'WeaponAuxMultiplier' effect/state. | 0 |
| `XIsTargetHealth` | Block | Math variable assignment: Evaluates X as the target's current health. | 0 |
| `do_not_pop_corpse` | Boolean |  | 0 |
| `drop_body_ability` | Enum/String |  | 0 |
| `drop_on_death` | Enum/String |  | 0 |
| `drop_on_self_death` | Boolean |  | 0 |
| `element` | Enum/String | The specific element type to check for. | 0 |
| `extra_statuses` | Block | Additional generic status applications. | 0 |
| `force_contact` | Boolean | If true, enforces physical overlap. | 0 |
| `form` | Enum/String | The specific form ID to check for. | 0 |
| `formula` | Enum/String | The math expression to evaluate. | 0 |
| `instant` | Boolean |  | 0 |
| `key` | Enum/String |  | 0 |
| `kill_on_consume` | Boolean |  | 0 |
| `mount_mode` | Enum/String | If true, treats the consumption as riding/mounting instead of eating. | 0 |
| `odds` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 0 |
| `status` | Enum/String | The status effect to apply. | 0 |
| `struggle_ability` | Enum/String | Ability triggered by the consumed entity while inside the consumer. | 0 |
| `tag` | Enum/String | The entity tag to seek out. | 0 |
| `threshold_expr` | Enum/String |  | 0 |
| `threshold_flat` | Number | A flat numerical health value threshold. | 0 |
| `threshold_percent` | Number | A percentage-based health threshold (e.g. 50%). | 0 |
| `use_placeholder` | Boolean |  | 0 |
| `weather` | Array | An array of weather states to check against. | 0 |
| `wet` | Boolean |  | 0 |

</details>

---

### Object: `target`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1862

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_range` | Number | The maximum and minimum distance required to cast. | 1088 |
| `max_aoe` | Number | The maximum and minimum radius/length of the AoE. | 795 |
| `min_range` | Number | The maximum and minimum distance required to cast. | 583 |
| [`target_mode`](./Enums.md#enum-target_mode) | Enum | How the cursor operates (`tile`, `direction`, `none`). | 503 |
| [`restrictions`](./Arrays.md#array-restrictions) | Array | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). | 463 |
| [`aoe_mode`](./Enums.md#enum-aoe_mode) | Enum | The shape of the area (`standard`, `line`, `cross`, `square`, `custom`). | 432 |
| [`knockback_mode`](./Enums.md#enum-knockback_mode) | Enum | How physics vectors apply (`character_to_tile`, `pull_to_character`, `zero`, `orientation`). | 265 |
| `min_aoe` | Mixed | The maximum and minimum radius/length of the AoE. | 253 |
| `aoe_excludes_self` | Boolean | Prevents the AoE from hitting the caster. | 241 |
| [`aoe_restrictions`](./Arrays.md#array-aoe_restrictions) | Array | Array of conditions the AoE tiles must meet (e.g., `must_have_line_of_sight_unpurgable`). | 197 |
| `aoe_considers_character_size` | Boolean | Scales the AoE based on the caster's tile size (e.g., 2x2). | 170 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 162 |
| [`range_mode`](./Enums.md#enum-range_mode) | Enum | How range is counted (`standard`, `ground_move`). | 114 |
| [`X_is`](./Enums.md#enum-x_is) | Enum | Applies or references the 'X_is' effect/state. | 86 |
| [`custom_aoe`](./Arrays.md#array-custom_aoe) | Array | Array of exact coordinates for a custom shape (e.g., `[[1, -1] [1, 0]]`). | 83 |
| `multihit` | Number | Hardcoded number of times the ability hits the target. | 62 |
| `max_targets` | Number | Limits on how many distinct entities can be targeted. | 56 |
| `range_excludes_blocking` | Boolean | Cannot target through walls/obstacles. | 53 |
| `prioritize_dont_change_direction` | Mixed | AI preference to maintain current facing angle. | 52 |
| [`target_requires_tag`](./Enums.md#enum-target_requires_tag) | Enum | Target must possess this exact character tag. | 40 |
| [`aoe_symmetry`](./Enums.md#enum-aoe_symmetry) | Enum | Determines if the AoE mirrors on axes. | 28 |
| `prioritize_face_camera` | Mixed | AI preference to face South. | 26 |
| `straight_shot` | Boolean | Ensures projectiles do not arc. | 24 |
| `can_multihit` | Boolean | If true, overlapping AoEs can hit the same target multiple times. | 17 |
| `allow_any_orientation` | Boolean | Allows casting regardless of the character's facing direction. | 16 |
| `range_considers_character_size` | Boolean | Range calculation accounts for large entities. | 16 |
| `throw_consumed_character` | Boolean | Throws the entity currently held/eaten. | 15 |
| `min_targets` | Number | Limits on how many distinct entities can be targeted. | 14 |
| `aoe_leading_edge_only` | Boolean | Only the outermost edge of the AoE shape applies effects. | 13 |
| `allow_diagonals` | Boolean | Allows targeting on diagonal grid axes. | 12 |
| `range_display_include_character_size` | Boolean | Visual: offsets the range indicator for 2x2 units. | 12 |
| `stagger_multihit_targets` | Boolean | Delays hits slightly between multiple targets. | 12 |
| `upgrade_straight_shot_to_piercing` | Boolean | Allows the projectile to pass through multiple targets. | 11 |
| `delayed_trigger` | Boolean | Delays the actual execution of the target effect. | 10 |
| `consider_trample` | Boolean | AI consideration for moving through units. | 9 |
| [`custom_range`](./Arrays.md#array-custom_range) | Array | Overrides standard range scaling. | 7 |
| `N` | Number | Variable modifier parameter. | 7 |
| `always_bounce` | Boolean | Forces the attack/projectile to bounce regardless of hit. | 6 |
| [`custom_aoe_util`](./Arrays.md#array-custom_aoe_util) | Array | Utility variants of custom AoE definitions. | 6 |
| `multihit_max` | Number | Variable limits for random multihit abilities. | 6 |
| `multihit_min` | Number | Variable limits for random multihit abilities. | 6 |
| `reorient_thrown_character` | Boolean | Forces a thrown entity to face a certain way. | 6 |
| [`toss_direction_restriction`](./Enums.md#enum-toss_direction_restriction) | Enum | Limits which ways an entity can be tossed. | 6 |
| `aoe_hint_teamcast` | Boolean | Visual hint for cooperative casting abilities. | 5 |
| [`aoe_tile_requires_element`](./Enums.md#enum-aoe_tile_requires_element) | Enum | Only affects tiles painted with a specific element. | 5 |
| `distance_sort_targets` | Mixed | Prioritizes targets based on proximity. | 5 |
| `dont_orient_aoe` | Boolean | Prevents the AoE shape from rotating with the character. | 5 |
| `hint_can_target_pickups` | Boolean | UI hint that the player can target items on the ground. | 5 |
| `max_bounces` | Number | Hard cap on how many times a bouncing effect can trigger. | 5 |
| `splash_damage_aoe_begin` | Number | At what radius splash damage starts applying. | 5 |
| [`aoe_chance`](./Enums.md#enum-aoe_chance) | Enum | Percentage chance for the AoE to trigger. | 4 |
| `as_the_crow_flies` | Boolean | Calculates range ignoring all pathing terrain obstacles. | 4 |
| `force_ai_target_as_spell` | Boolean | Forces the AI to treat a physical move like a spell for targeting logic. | 4 |
| [`mouse_offset`](./Arrays.md#array-mouse_offset) | Array | Visual offset for the targeting cursor. | 4 |
| `range_display_include_aoe` | Boolean | Visual: shows the full AoE potential when previewing range. | 4 |
| `shotgun_mode` | Boolean | Deals more damage/hits if targets are closer. | 4 |
| `shuffle_tile_order` | Boolean | Randomizes the execution order of AoE tiles. | 4 |
| `upgrade_straight_shot_to_boomerang` | Boolean | Makes the projectile return to caster. | 4 |
| `dont_orient` | Boolean | Prevents the character from turning to face the target. | 3 |
| `low_health_character_threshold` | Mixed | AI targeting threshold for seeking weak targets. | 3 |
| `randomize_target_within_range` | Number | Picks a random valid tile instead of the user's click. | 3 |
| [`special_tile_tag`](./Enums.md#enum-special_tile_tag) | Enum | Targets only tiles with this specific tag. | 3 |
| `track_target` | Boolean | Projectile/Effect follows moving targets. | 3 |
| `corpse_priority` | Number | AI preference for targeting dead bodies. | 2 |
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
| `ally_priority` | Number | AI preference for targeting allies. | 1 |
| `aoe_display_exclude_restrictions` | Boolean | Visual only: Hides invalid tiles from the AoE preview. | 1 |
| `aoe_rotate_around_character_center` | Boolean | Anchors the AoE rotation to the character rather than the tile. | 1 |
| `aoe_spell_on_land` | Boolean | Visual trigger when a jump lands. | 1 |
| `bonus_pathing_leniency` | Number | Gives the AI leeway when calculating complex paths. | 1 |
| [`custom_aoe_mirror`](./Arrays.md#array-custom_aoe_mirror) | Array | How the custom shape mirrors when facing left vs right. | 1 |
| [`custom_aoe_util_mirror`](./Arrays.md#array-custom_aoe_util_mirror) | Array |  | 1 |
| `damage_collided_only` | Boolean | Only damages the first entity the projectile/dash hits. | 1 |
| `enemy_priority` | Number | AI preference for targeting enemies. | 1 |
| `hint_can_target_static` | Boolean | UI hint that the player can target inanimate objects. | 1 |
| [`knockback_modifier`](./Enums.md#enum-knockback_modifier) | Enum | Multiplier for the knockback physics force. | 1 |
| `lingering` | Boolean | Target zone remains active across multiple turns. | 1 |
| `mirror_custom_aoe` | Boolean | Flips the custom AoE array. | 1 |
| [`prioritize_throw_target_with_passive`](./Enums.md#enum-prioritize_throw_target_with_passive) | Enum | AI prefers throwing targets that have specific passives. | 1 |
| `randomize_knockback_direction_except_for_finisher` | Boolean | Chaotic knockback unless it kills the target. | 1 |
| `range_excludes_self` | Boolean | Cannot click on the caster's tile. | 1 |
| `range_max` | Number | Alternate syntax for `max_range`/`min_range`. | 1 |
| `range_min` | Number | Alternate syntax for `max_range`/`min_range`. | 1 |
| [`range_symmetry`](./Enums.md#enum-range_symmetry) | Enum | Mirrors the range grid. | 1 |
| `remain_off_map` | Boolean | Keeps entity removed from the grid. | 1 |
| [`restructions`](./Enums.md#enum-restructions) | Enum | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). | 1 |
| `reverse_target_direction` | Boolean | Inverts the targeting vector. | 1 |
| `spin_steps` | Number | Number of rotational increments for spin targeting. | 1 |
| `uncounterable` | Boolean | Bypasses counter-attack passives. | 1 |
| `force_no_contact` | `Boolean` | Bypasses all contact-based retaliation (Thorns, etc). | 0 |

</details>

---

### Object: `cost`
### Object: `cost`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1851

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `mana` | Number | MP pool and how much it restores per turn. | 1603 |
| `infcantrip` | Boolean | Can be cast infinitely as long as costs are met. | 810 |
| `cantrip` | Boolean | Does not end the turn when cast. | 560 |
| `once_per_fight` | Mixed | Exhausts for the remainder of combat after one use. | 98 |
| `act_points` | Number | Consumes primary action points (default 1). | 86 |
| `move_points` | Number | Consumes movement points. | 59 |
| `prime` | Number | Requires a "priming" turn before it fires. | 30 |
| `allow_offmap_casts` | Boolean | Can be used while the character is hidden/removed from grid. | 22 |
| `cant_cast` | Mixed | Explicitly disables casting (used for passive-triggered only abilities). | 18 |
| `must_be_consuming` | Boolean | Requires the character to be eating/holding something. | 17 |
| `charge` | Mixed | Cooldown timers measured in turns. | 16 |
| `must_not_be_consuming` | Boolean | Cannot be holding/eating an entity. | 14 |
| `requires_reload` | Boolean | Must spend an action to reload before casting again. | 14 |
| [`cantrip_group`](./Enums.md#enum-cantrip_group) | Enum | Groups cantrips so using one exhausts the others. | 12 |
| `can_cast_while_dead` | Boolean | Usable by corpses (e.g., DeathRattle triggers). | 12 |
| `must_be_offmap` | Boolean | Requires the character to be hidden/dug underground. | 12 |
| `X_cant_be_zero` | Boolean | Applies or references the 'X_cant_be_zero' effect/state. | 11 |
| `disallow_cost_modification` | Boolean | Prevents passives from making this cheaper. | 9 |
| `coins` | Number | Consumes currency to cast. | 8 |
| `durability` | Number | Consumes item durability. | 8 |
| `main_turn_only` | Boolean | Cannot be cast during bonus or dispersed turns. | 8 |
| `requires_destructible_weapon` | Boolean | The equipped weapon must be breakable. | 8 |
| `requires_exact_character_aux` | Number | Hardcoded character specific lock. | 8 |
| `must_not_be_a_summon` | Boolean | Summons/Familiars cannot cast this. | 7 |
| `start_reloaded` | Boolean | Spawns with the ability pre-loaded. | 7 |
| `must_be_first_action` | Boolean | Can only be used at the very start of the turn. | 4 |
| `enabled_formula` | Mixed | Mathematical string required to be >0 to cast. | 3 |
| `must_be_first_nonmove_action` | Boolean | Can move first, but cannot use other abilities first. | 3 |
| `must_have_weapon` | Boolean | Requires a weapon equipped in the item slot. | 2 |
| `can_be_refreshed` | Boolean | Passives/Effects can reset this ability's cooldown. | 1 |
| `can_pay_over_multiple_turns` | Boolean | Allows channeling costs over time. | 1 |
| `can_self_refresh` | Boolean | The ability has mechanics to reset its own cooldown. | 1 |
| `damage_cant_be_zero` | Boolean | Requires the ability to have >0 calculated damage to cast. | 1 |
| `initial_charge` | Number | How many turns it starts on cooldown at battle start. | 1 |
| `manacost_cant_be_zero` | Boolean | Fails to cast if mana cost is reduced to 0. | 1 |
| `minimum_con` | Number | Stat thresholds required to cast. | 1 |
| `minimum_spd` | Number | Stat thresholds required to cast. | 1 |
| `require_default_size` | Boolean | 2x2 or altered characters cannot cast this. | 1 |
| `requires_attack_damage_threshold` | Number | Needs a certain amount of innate damage. | 1 |
| `requires_consumed_trinket` | Boolean | Must have eaten a specific item type. | 1 |
| `requires_empty_trinket` | Boolean | Must not have an accessory equipped. | 1 |
| `requires_hp_threshold` | Number | Must be below/above a certain health percentage. | 1 |
| `requires_weapon` | Boolean | Prerequisite: Must meet this condition. | 1 |

</details>

---

### Object: `self_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 220

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#object-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 65 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 47 |
| `damage` | Mixed | The base damage properties of an attack. | 47 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 11 |
| `knockback` | Number |  | 10 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 4 |
| `ai_base_score` | Number |  | 2 |
  | `bonus_melee_damage` | Any | Native property. | 0 |
  | `melee` | Variable |  | 0 |
  | `spawn` | Any | Native property. | 0 |
  | `true` | Any | Native property. | 0 |
| `cant_miss` | `Boolean` |  | 0 |
| `effects` | `Block` | Non-damaging status applications and logic triggers executed on impact. | 0 |
| `heal` | `Number` |  | 0 |
| `non_lethal` | `Boolean` |  | 0 |
| `piercing` | `Boolean` |  | 0 |

</details>

---

### Object: `spawn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 192

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 184 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 86 |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 59 |
| `ai_base_score` | Number |  | 31 |
| [`additional_passives`](./Abilities_and_Spells.md#object-additional_passives) | Object | Passives granted intrinsically to a spawned entity. | 20 |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum |  | 17 |
| [`catdata`](./Enums.md#enum-catdata) | Enum | Defines genetic/clone data cloning. | 13 |
| `clone_items` | Boolean | If true, transfers inventory to the clone. | 12 |
| `lob` | Boolean |  | 4 |
| [`post_spawn_statuses`](./Abilities_and_Spells.md#object-post_spawn_statuses) | Object | Status effects applied immediately after an entity spawns. | 4 |
| `size` | Number |  | 4 |
| `face_camera` | Boolean |  | 2 |
| `inherit_elite_buffs` | Boolean |  | 2 |
| `start_dead` | Boolean |  | 2 |
| [`appearance`](./Enums.md#enum-appearance) | Enum |  | 1 |
| [`auto_cast_on_spawn`](./Enums.md#enum-auto_cast_on_spawn) | Enum |  | 1 |
| [`chapter`](./Enums.md#enum-chapter) | Enum |  | 1 |
| `include_passives` | Boolean |  | 1 |
| `redirect_location_if_blocked` | Boolean |  | 1 |
| [`spawnin_animation`](./Enums.md#enum-spawnin_animation) | Enum |  | 1 |
| `trigger_battle_start` | Boolean |  | 1 |
| `custom_additional_ai_weight` | `Enum/String` |  | 0 |
| `layer` | `Enum/String` |  | 0 |

</details>

---

### Object: `bonus_passives`
### Object: `bonus_passives`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 136

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 125 |

</details>

---

### Object: `temporary_effects`
### Object: `temporary_effects`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 88

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 34 |
| `CastAgain` | Number | Applies or references the 'CastAgain' effect/state. | 20 |
| `DisableTrample` | Number | Applies or references the 'DisableTrample' effect/state. | 10 |
| `Fury` | Number | Applies or references the 'Fury' effect/state. | 7 |
| [`LeaveBehind`](./Abilities_and_Spells.md#object-leavebehind) | Object | Spawns a specific object at the character's previous location when they move. | 5 |
| `JustInCaseTrample` | Number | Applies or references the 'JustInCaseTrample' effect/state. | 5 |
| `DashFury` | Number | Applies or references the 'DashFury' effect/state. | 3 |
| `BearTrapTrail` | Number | Applies or references the 'BearTrapTrail' effect/state. | 2 |
| [`JumpAttackLeaveBehind`](./Enums.md#enum-jumpattackleavebehind) | Enum | Applies or references the 'JumpAttackLeaveBehind' effect/state. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `DelayedWindTrail` | Number | Applies or references the 'DelayedWindTrail' effect/state. | 1 |

</details>

---

### Object: `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 71

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional_boss), [`Conditional_Buddy`](./Abilities_and_Spells.md#object-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional_object), [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional_speculative), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 71 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 20 |
| `AddLeechesStatus` | Number | Applies or references the 'AddLeechesStatus' effect/state. | 0 |
| `AddWeaponAux` | String | Applies or references the 'AddWeaponAux' effect/state. | 0 |
| `ApplyToRandomPartyMemberIfPossible` | Block | Redirects the nested effects to apply to a random living member of the player's party. | 0 |
| `ApplyToSource` | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `ApplyToSourceOnKill` | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 0 |
| `BonusDamage` | String | Applies or references the 'BonusDamage' effect/state. | 0 |
| `BonusDamageBasedOnDistance` | Number | Applies or references the 'BonusDamageBasedOnDistance' effect/state. | 0 |
| `CanApplyToInanimate` | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 0 |
| `CapDamage` | Number | Applies or references the 'CapDamage' effect/state. | 0 |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 0 |
| `CatPartsTransform` | Block | Transforms specific body parts into different visual variants. | 0 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 0 |
| `Conditional_Displaceable` | Block | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 0 |
| `Conditional_GoodRoll` | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 0 |
| `Conditional_HasStatus` | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 0 |
| `Conditional_HealthThreshold` | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 0 |
| `Conditional_InForm` | Block | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 0 |
| `Conditional_NotBoss` | Block | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 0 |
| `Consumed` | Block | State block triggered when this object or entity is eaten/consumed by another character. | 0 |
| `CrackMoonHead` | Number | Applies or references the 'CrackMoonHead' effect/state. | 0 |
| `Craft` | Block | Synthesizes or spawns a new item from a specific pool. | 0 |
| `DeleteObject` | Number | Applies or references the 'DeleteObject' effect/state. | 0 |
| `DestroyEquipmentAndAttachParasite` | Block | Removes an equipped item and replaces it with a parasite from a specified pool. | 0 |
| `Die` | Number | Applies or references the 'Die' effect/state. | 0 |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. | 0 |
| `DisableWeapon` | Number | Applies or references the 'DisableWeapon' effect/state. | 0 |
| `DisplaceTowardsSource` | Number | Applies or references the 'DisplaceTowardsSource' effect/state. | 0 |
| `DoDamage` | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 0 |
| `EvolveAbilityFromPool` | Enum/String | Upgrades or transforms an existing ability into a new one from the specified pool. | 0 |
| `ExplodeCharacter` | `Number` | Applies or references the 'ExplodeCharacter' effect/state. | 0 |
| `ExplodeCharacter_Party` | `Number` | Applies or references the 'ExplodeCharacter_Party' effect/state. | 0 |
| `FaceAway` | Number | Applies or references the 'FaceAway' effect/state. | 0 |
| `FaceCamera` | `Number` | Applies or references the 'FaceCamera' effect/state. | 0 |
| `FactionConversion` | Number | Applies or references the 'FactionConversion' effect/state. | 0 |
| `FlatAIBonus` | `Number` | Applies or references the 'FlatAIBonus' effect/state. | 0 |
| `FlatLeech` | Number | Applies or references the 'FlatLeech' effect/state. | 0 |
| `FloatingRockTrap` | Number | Applies or references the 'FloatingRockTrap' effect/state. | 0 |
| `ForceImmediateMove` | `Number` | Applies or references the 'ForceImmediateMove' effect/state. | 0 |
| `FormChange` | Block | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 0 |
| `GainDisorder` | Enum/String | Applies or references the 'GainDisorder' effect/state. | 0 |
| `GainDisorderFromPool_PostCast` | `Enum/String` | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 0 |
| `GenericDebuff` | `Number` | Applies or references the 'GenericDebuff' effect/state. | 0 |
| `IgnoreDamage` | Number | Applies or references the 'IgnoreDamage' effect/state. | 0 |
| `ImmediateUseAbility` | `Enum/String` | Applies or references the 'ImmediateUseAbility' effect/state. | 0 |
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 0 |
| `KnockUpAndAway` | `Block` | Displaces the target vertically and horizontally away from the source. | 0 |
| `LaunchOffScreen` | Enum/String | Applies or references the 'LaunchOffScreen' effect/state. | 0 |
| `LaunchOffScreenInstakill` | Number | Applies or references the 'LaunchOffScreenInstakill' effect/state. | 0 |
| `ManaGain` | String | Applies or references the 'ManaGain' effect/state. | 0 |
| `MergeDamageInstance` | Block | Combines damage numbers or visual hit effects. | 0 |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 0 |
| `PopAndSpawn` | Block | Destroys the target and replaces it with a new spawned entity. | 0 |
| `PurgeAll` | `Number` | Applies or references the 'PurgeAll' effect/state. | 0 |
| `RandomBonusDamage` | Number | Applies or references the 'RandomBonusDamage' effect/state. | 0 |
| `RandomStatDown` | Number | Applies or references the 'RandomStatDown' effect/state. | 0 |
| `RandomStatusFromPool` | `Block` | Selects and applies a random status effect from the provided nested block. | 0 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 0 |
| `RefreshMovePoints` | Number | Applies or references the 'RefreshMovePoints' effect/state. | 0 |
| `RefreshWeaponAbility` | Number | Applies or references the 'RefreshWeaponAbility' effect/state. | 0 |
| `RemoveMovePoints` | `Number` | Applies or references the 'RemoveMovePoints' effect/state. | 0 |
| `RemoveStatus` | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 0 |
| `RemoveTurnsThisRound` | `Number` | Applies or references the 'RemoveTurnsThisRound' effect/state. | 0 |
| `Revive` | `Number` | Applies or references the 'Revive' effect/state. | 0 |
| `ScatterRandomPickups` | Number | Applies or references the 'ScatterRandomPickups' effect/state. | 0 |
| `SetAnimationAlts` | Block | Overrides specific animation states with alternative animations. | 0 |
| `SetHealth` | `Number` | Applies or references the 'SetHealth' effect/state. | 0 |
| `SetKnockback` | Number | Applies or references the 'SetKnockback' effect/state. | 0 |
| `SetShield` | `Number` | Applies or references the 'SetShield' effect/state. | 0 |
| `ShowFakeDamage` | `Block` | Displays a visual damage number without actually modifying health. | 0 |
| `ShowText` | String | Applies or references the 'ShowText' effect/state. | 0 |
| `SpawnBearTrapIfHitKills` | `Number` | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. | 0 |
| `SpawnThingIfHitKills` | `Enum/String` | Applies or references the 'SpawnThingIfHitKills' effect/state. | 0 |
| `SpecificInjury` | Enum/String | Applies or references the 'SpecificInjury' effect/state. | 0 |
| `SpeculativeMoveSelfCorpseOffMap` | `Number` | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 0 |
| `StanceSwitchToMelee` | Number | Applies or references the 'StanceSwitchToMelee' effect/state. | 0 |
| `StanceSwitchToRanged` | Number | Applies or references the 'StanceSwitchToRanged' effect/state. | 0 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
| `TempTrampleUntilSettled` | Number | Applies or references the 'TempTrampleUntilSettled' effect/state. | 0 |
| `Temporary` | `Block` | A wrapper block for applying status effects that automatically expire. | 0 |
| `UseAbility` | Enum/String | Forces the character or target to instantly use a specified ability. | 0 |
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 0 |
| `VaporizeCorpse` | Number | Applies or references the 'VaporizeCorpse' effect/state. | 0 |
| `VaporizeInanimate` | `Number` | Applies or references the 'VaporizeInanimate' effect/state. | 0 |
| `XIsTargetHealth` | `Block` | Math variable assignment: Evaluates X as the target's current health. | 0 |
| `do_not_pop_corpse` | Boolean |  | 0 |
| `drop_body_ability` | Enum/String |  | 0 |
| `drop_on_death` | Enum/String |  | 0 |
| `drop_on_self_death` | Boolean |  | 0 |
| `extra_statuses` | Block | Additional generic status applications. | 0 |
| `force_contact` | Boolean | If true, enforces physical overlap. | 0 |
| `instant` | Boolean |  | 0 |
| `kill_on_consume` | Boolean |  | 0 |
| `mount_mode` | Enum/String | If true, treats the consumption as riding/mounting instead of eating. | 0 |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 0 |
| `status` | Enum/String | The status effect to apply. | 0 |
| `struggle_ability` | Enum/String | Ability triggered by the consumed entity while inside the consumer. | 0 |
| `tag` | Enum/String | The specific string tag to check for. | 0 |
| `threshold_expr` | Enum/String |  | 0 |
| `threshold_flat` | Number | A flat numerical health value threshold. | 0 |
| `threshold_percent` | Number | A percentage-based health threshold (e.g. 50%). | 0 |
| `use_placeholder` | Boolean |  | 0 |
| `wet` | Boolean |  | 0 |

</details>

---

### Object: `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 51

> **Referenced by:** [`ApplyStatusIfCrit`](./Abilities_and_Spells.md#object-applystatusifcrit), [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate), [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional_goodroll), [`Conditional_HasStatus`](./Abilities_and_Spells.md#object-conditional_hasstatus), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional_healththreshold), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#object-conditional_livingplayercat), [`Conditional_PlayerCat`](./Abilities_and_Spells.md#object-conditional_playercat), [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#object-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#object-else), [`Math`](./Abilities_and_Spells.md#object-math), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 43 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 22 |
| `AddLeechesStatus` | `Number` | Applies or references the 'AddLeechesStatus' effect/state. | 0 |
| `AddWeaponAux` | `String` | Applies or references the 'AddWeaponAux' effect/state. | 0 |
| `Cleanse` | `Number` | Applies or references the 'Cleanse' effect/state. | 0 |
| `Craft` | `Block` | Synthesizes or spawns a new item from a specific pool. | 0 |
| `DisableWeapon` | `Number` | Applies or references the 'DisableWeapon' effect/state. | 0 |
| `DoDamage` | `Block` | Explicitly triggers a secondary damage instance independent of the main attack. | 0 |
| `EvolveAbilityFromPool` | `Enum/String` | Upgrades or transforms an existing ability into a new one from the specified pool. | 0 |
| `FormChange` | `Enum/String` | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 0 |
| `KnockUpAndAway` | `Block` | Displaces the target vertically and horizontally away from the source. | 0 |
| `ManaGain` | `Number` | Applies or references the 'ManaGain' effect/state. | 0 |
| `RefreshActPoints` | `Number` | Applies or references the 'RefreshActPoints' effect/state. | 0 |
| `RefreshMovePoints` | `Number` | Applies or references the 'RefreshMovePoints' effect/state. | 0 |
| `RemoveStatus` | `Enum/String` | Applies or references the 'RemoveStatus' effect/state. | 0 |
| `SpecificInjury` | `Enum/String` | Applies or references the 'SpecificInjury' effect/state. | 0 |
| `StanceSwitchToMelee` | `Number` | Applies or references the 'StanceSwitchToMelee' effect/state. | 0 |
| `StanceSwitchToRanged` | `Number` | Applies or references the 'StanceSwitchToRanged' effect/state. | 0 |
| `TakeExtraTurn` | `Number` | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
| `TempTrampleUntilSettled` | `Number` | Applies or references the 'TempTrampleUntilSettled' effect/state. | 0 |

</details>

---

### Object: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 42

> **Referenced by:** [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional_object), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 63 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 49 |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. | 41 |
  | `EventBounty` | Integer | Applies or references the 'EventBounty' effect/state. | 0 |
  | [`MergeDamageInstance`](#mergedamageinstance) | Object | Combines damage numbers or visual hit effects. | 0 |
  | [`SetAnimationAlts`](#setanimationalts) | Object | Overrides specific animation states with alternative animations. | 0 |
| `AddLeechesStatus` | Number | Applies or references the 'AddLeechesStatus' effect/state. | 0 |
| `AddWeaponAux` | String | Applies or references the 'AddWeaponAux' effect/state. | 0 |
| `ApplyToRandomPartyMemberIfPossible` | Block | Redirects the nested effects to apply to a random living member of the player's party. | 0 |
| `ApplyToSource` | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `ApplyToSourceOnKill` | `Block` | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 0 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 0 |
| `CanApplyToInanimate` | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 0 |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 0 |
| `CatPartsTransform` | Block | Transforms specific body parts into different visual variants. | 0 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 0 |
| `CompleteItemQuest` | Enum/String | Applies or references the 'CompleteItemQuest' effect/state. | 0 |
| `Conditional_Boss` | `Block` | Conditional trigger: Executes nested logic if the target is a Boss. | 0 |
| `Conditional_Displaceable` | Block | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 0 |
| `Conditional_GoodRoll` | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 0 |
| `Conditional_HasStatus` | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 0 |
| `Conditional_HasTag` | Block | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 0 |
| `Conditional_HealthThreshold` | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 0 |
| `Conditional_InForm` | `Block` | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 0 |
| `Conditional_NotBoss` | `Block` | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 0 |
| `Conditional_Speculative` | Block | A simulation block used by the AI to test hypothetical outcomes before committing to an action. | 0 |
| `Consumed` | Block | State block triggered when this object or entity is eaten/consumed by another character. | 0 |
| `CrackMoonHead` | `Number` | Applies or references the 'CrackMoonHead' effect/state. | 0 |
| `Craft` | Block | Synthesizes or spawns a new item from a specific pool. | 0 |
| `DeleteObject` | `Number` | Applies or references the 'DeleteObject' effect/state. | 0 |
| `DestroyEquipmentAndAttachParasite` | Block | Removes an equipped item and replaces it with a parasite from a specified pool. | 0 |
| `Die` | `Number` | Applies or references the 'Die' effect/state. | 0 |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. | 0 |
| `DisableWeapon` | Number | Applies or references the 'DisableWeapon' effect/state. | 0 |
| `DisplaceTowardsSource` | `Number` | Applies or references the 'DisplaceTowardsSource' effect/state. | 0 |
| `DoDamage` | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 0 |
| `EvolveAbilityFromPool` | Enum/String | Upgrades or transforms an existing ability into a new one from the specified pool. | 0 |
| `ExplodeCharacter` | Number | Applies or references the 'ExplodeCharacter' effect/state. | 0 |
| `ExplodeCharacter_NoDie` | Number | Applies or references the 'ExplodeCharacter_NoDie' effect/state. | 0 |
| `ExplodeCharacter_Party` | Number | Applies or references the 'ExplodeCharacter_Party' effect/state. | 0 |
| `ExplodeCharacter_PartyBoss` | Number | Applies or references the 'ExplodeCharacter_PartyBoss' effect/state. | 0 |
| `ExplodeCharacter_RockCrusher` | Number | Applies or references the 'ExplodeCharacter_RockCrusher' effect/state. | 0 |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Number | Applies or references the 'ExplodeCharacter_RockCrusher_PetrifyBreak' effect/state. | 0 |
| `FaceAway` | `Number` | Applies or references the 'FaceAway' effect/state. | 0 |
| `FaceCamera` | Number | Applies or references the 'FaceCamera' effect/state. | 0 |
| `FactionConversion` | Number | Applies or references the 'FactionConversion' effect/state. | 0 |
| `FlatAIBonus` | Number | Applies or references the 'FlatAIBonus' effect/state. | 0 |
| `FloatingRockTrap` | `Number` | Applies or references the 'FloatingRockTrap' effect/state. | 0 |
| `ForceImmediateMove` | Number | Applies or references the 'ForceImmediateMove' effect/state. | 0 |
| `ForceImmediateMoveAndAttack` | Block | Forces the character to immediately move to a target and use a specified ability. | 0 |
| `FormChange` | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 0 |
| `GainDisorderFromPool_PostCast` | Enum/String | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 0 |
| `GenericDebuff` | Number | Applies or references the 'GenericDebuff' effect/state. | 0 |
| `IgnoreDamage` | `Number` | Applies or references the 'IgnoreDamage' effect/state. | 0 |
| `ImmediateUseAbility` | `Enum/String` | Applies or references the 'ImmediateUseAbility' effect/state. | 0 |
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 0 |
| `KnockUpAndAway` | Block | Displaces the target vertically and horizontally away from the source. | 0 |
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 0 |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 0 |
| `PopAndSpawn` | `Block` | Destroys the target and replaces it with a new spawned entity. | 0 |
| `PurgeAll` | Number | Applies or references the 'PurgeAll' effect/state. | 0 |
| `RandomStatDown` | String | Applies or references the 'RandomStatDown' effect/state. | 0 |
| `RandomStatusFromPool` | Block | Selects and applies a random status effect from the provided nested block. | 0 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 0 |
| `RefreshMovePoints` | Number | Applies or references the 'RefreshMovePoints' effect/state. | 0 |
| `RemoveItem` | Enum/String | Applies or references the 'RemoveItem' effect/state. | 0 |
| `RemoveMovePoints` | Number | Applies or references the 'RemoveMovePoints' effect/state. | 0 |
| `RemoveStatus` | `Enum/String` | Applies or references the 'RemoveStatus' effect/state. | 0 |
| `RemoveTurnsThisRound` | Number | Applies or references the 'RemoveTurnsThisRound' effect/state. | 0 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 0 |
| `ScatterRandomPickups` | `Number` | Applies or references the 'ScatterRandomPickups' effect/state. | 0 |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. | 0 |
| `SetKnockback` | `Number` | Applies or references the 'SetKnockback' effect/state. | 0 |
| `SetShield` | Number | Applies or references the 'SetShield' effect/state. | 0 |
| `ShowFakeDamage` | Block | Displays a visual damage number without actually modifying health. | 0 |
| `SpawnBearTrapIfHitKills` | Number | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. | 0 |
| `SpawnThingIfHitKills` | Enum/String | Applies or references the 'SpawnThingIfHitKills' effect/state. | 0 |
| `SpecificInjury` | Enum/String | Applies or references the 'SpecificInjury' effect/state. | 0 |
| `SpeculativeMoveSelfCorpseOffMap` | Number | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 0 |
| `StanceSwitchToMelee` | Number | Applies or references the 'StanceSwitchToMelee' effect/state. | 0 |
| `StanceSwitchToRanged` | Number | Applies or references the 'StanceSwitchToRanged' effect/state. | 0 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
| `TempTrampleUntilSettled` | Number | Applies or references the 'TempTrampleUntilSettled' effect/state. | 0 |
| `Temporary` | Block | A wrapper block for applying status effects that automatically expire. | 0 |
| `TransformWeapon` | Block | Transforms the equipped weapon into another specific weapon state. | 0 |
| `UseAbility` | `Enum/String` | Forces the character or target to instantly use a specified ability. | 0 |
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 0 |
| `VaporizeCorpse` | `Number` | Applies or references the 'VaporizeCorpse' effect/state. | 0 |
| `VaporizeInanimate` | Number | Applies or references the 'VaporizeInanimate' effect/state. | 0 |
| `VisualFX` | Enum/String | Applies or references the 'VisualFX' effect/state. | 0 |
| `WeaponAuxMultiplier` | Enum/String | Applies or references the 'WeaponAuxMultiplier' effect/state. | 0 |
| `XIsTargetHealth` | Block | Math variable assignment: Evaluates X as the target's current health. | 0 |
| `form` | Enum/String | The specific form ID to check for. | 0 |

</details>

---

### Object: `Temporary`
### Object: `Temporary`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 41

> **Referenced by:** [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate), [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_NotAlly`](./Abilities_and_Spells.md#object-conditional_notally), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 41 |
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 40 |
| `turns` | Number | Duration in turns. | 40 |
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 19 |
| `expires_on_end_turn` | Boolean |  | 11 |
| `data` | Number |  | 2 |
| `expires_on_appliers_turn` | Boolean |  | 2 |
| `expires_on_move` | Boolean |  | 1 |

</details>

---

### Object: `sounds`
### Object: `sounds`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 39

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ontrigger`](./Enums.md#enum-ontrigger) | Enum |  | 32 |
| [`oncast`](./Enums.md#enum-oncast) | Enum |  | 3 |
| [`oncastpoint`](./Enums.md#enum-oncastpoint) | Enum |  | 3 |
| [`ontrigger_intentional`](./Enums.md#enum-ontrigger_intentional) | Enum |  | 1 |

</details>

---

### Object: `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 36

> **Referenced by:** [`Conditional_Corpse`](./Abilities_and_Spells.md#object-conditional_corpse), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 40 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
  | [`Conditional_FinishedSpawning`](#conditional_finishedspawning) | Object | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. | 0 |
  | `DisplaceToAbilityTarget` | Integer | Applies or references the 'DisplaceToAbilityTarget' effect/state. | 0 |
  | `DontHealEnemies` | Integer | Applies or references the 'DontHealEnemies' effect/state. | 0 |
| `AddLeechesStatus` | Number | Applies or references the 'AddLeechesStatus' effect/state. | 0 |
| `AddWeaponAux` | String | Applies or references the 'AddWeaponAux' effect/state. | 0 |
| `ApplyToSource` | `Block` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `ApplyToSourceOnKill` | `Block` | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 0 |
| `BonusDamage` | `Number` | Applies or references the 'BonusDamage' effect/state. | 0 |
| `CanApplyToInanimate` | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 0 |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 0 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 0 |
| `CompleteItemQuest` | Enum/String | Applies or references the 'CompleteItemQuest' effect/state. | 0 |
| `Conditional_HealthThreshold` | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 0 |
| `Conditional_NotBoss` | `Block` | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 0 |
| `Craft` | Block | Synthesizes or spawns a new item from a specific pool. | 0 |
| `DisableWeapon` | Number | Applies or references the 'DisableWeapon' effect/state. | 0 |
| `DoDamage` | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 0 |
| `EvolveAbilityFromPool` | Enum/String | Upgrades or transforms an existing ability into a new one from the specified pool. | 0 |
| `ExplodeCharacter_RockCrusher` | Number | Applies or references the 'ExplodeCharacter_RockCrusher' effect/state. | 0 |
| `FactionConversion` | Number | Applies or references the 'FactionConversion' effect/state. | 0 |
| `ForceMoveTowards` | `Number` | Applies or references the 'ForceMoveTowards' effect/state. | 0 |
| `FormChange` | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 0 |
| `Imprison` | Enum/String | Applies or references the 'Imprison' effect/state. | 0 |
| `KnockUpAndAway` | Block | Displaces the target vertically and horizontally away from the source. | 0 |
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 0 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 0 |
| `RefreshMovePoints` | Number | Applies or references the 'RefreshMovePoints' effect/state. | 0 |
| `RemoveItem` | Enum/String | Applies or references the 'RemoveItem' effect/state. | 0 |
| `RemoveStatus` | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 0 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 0 |
| `SpecificInjury` | Enum/String | Applies or references the 'SpecificInjury' effect/state. | 0 |
| `StanceSwitchToMelee` | Number | Applies or references the 'StanceSwitchToMelee' effect/state. | 0 |
| `StanceSwitchToRanged` | Number | Applies or references the 'StanceSwitchToRanged' effect/state. | 0 |
| `TakeExtraTurn` | `Number` | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
| `TempTrampleUntilSettled` | Number | Applies or references the 'TempTrampleUntilSettled' effect/state. | 0 |
| `Temporary` | `Block` | A wrapper block for applying status effects that automatically expire. | 0 |
| `TransformWeapon` | Block | Transforms the equipped weapon into another specific weapon state. | 0 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 0 |
| `VaporizeInanimate` | Number | Applies or references the 'VaporizeInanimate' effect/state. | 0 |
| `WeaponAuxMultiplier` | Enum/String | Applies or references the 'WeaponAuxMultiplier' effect/state. | 0 |
| `status` | Enum/String | The status effect to apply. | 0 |

</details>

---

### Object: `splash_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#object-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 33 |
| `damage` | Number | The base damage properties of an attack. | 32 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 13 |
| `knockback` | Number | Knockback force of the splash blast. | 13 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 12 |
| `ai_base_score` | Number |  | 1 |
| `crit_chance` | `Number` |  | 0 |
| `effects` | `Block` | Non-damaging status applications and logic triggers executed on impact. | 0 |
| `force_no_knockback` | `Boolean` |  | 0 |
| `force_play_hit_animation` | `Boolean` |  | 0 |
| `layer` | `Enum/String` |  | 0 |
| `makes_contact` | `Boolean` |  | 0 |
| `override_trample_damage` | `Boolean` |  | 0 |

</details>

---

### Object: `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 25

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 29 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 |
| `AddLeechesStatus` | Number | Applies or references the 'AddLeechesStatus' effect/state. | 0 |
| `AddWeaponAux` | String | Applies or references the 'AddWeaponAux' effect/state. | 0 |
| `ApplyToSource` | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `ApplyToSourceOnKill` | `Block` | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 0 |
| `ChanceToBreak` | `Number` | Applies or references the 'ChanceToBreak' effect/state. | 0 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 0 |
| `CompleteItemQuest` | Enum/String | Applies or references the 'CompleteItemQuest' effect/state. | 0 |
| `Conditional_Corpse` | `Block` | Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 0 |
| `Conditional_Enemy` | Block | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 0 |
| `Conditional_PlayerCat` | `Block` | Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 0 |
| `ConjureRandomAbilityFromCat` | Number | Applies or references the 'ConjureRandomAbilityFromCat' effect/state. | 0 |
| `Craft` | Block | Synthesizes or spawns a new item from a specific pool. | 0 |
| `DisableWeapon` | Number | Applies or references the 'DisableWeapon' effect/state. | 0 |
| `DoDamage` | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 0 |
| `EvolveAbilityFromPool` | Enum/String | Upgrades or transforms an existing ability into a new one from the specified pool. | 0 |
| `FlatAIBonus` | Number | Applies or references the 'FlatAIBonus' effect/state. | 0 |
| `FormChange` | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 0 |
| `GenericDebuff` | Number | Applies or references the 'GenericDebuff' effect/state. | 0 |
| `KnockOutClone` | Enum/String | Applies or references the 'KnockOutClone' effect/state. | 0 |
| `KnockUpAndAway` | Block | Displaces the target vertically and horizontally away from the source. | 0 |
| `KnockbackDamageImmuneUntilSettled` | `Number` | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. | 0 |
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 0 |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 0 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 0 |
| `RefreshMovePoints` | Number | Applies or references the 'RefreshMovePoints' effect/state. | 0 |
| `RemoveItem` | Enum/String | Applies or references the 'RemoveItem' effect/state. | 0 |
| `RemoveStatus` | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 0 |
| `RepairAll` | `Number` | Applies or references the 'RepairAll' effect/state. | 0 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 0 |
| `ShowText` | `String` | Applies or references the 'ShowText' effect/state. | 0 |
| `SpecificInjury` | Enum/String | Applies or references the 'SpecificInjury' effect/state. | 0 |
| `StanceSwitchToMelee` | Number | Applies or references the 'StanceSwitchToMelee' effect/state. | 0 |
| `StanceSwitchToRanged` | Number | Applies or references the 'StanceSwitchToRanged' effect/state. | 0 |
| `T2CopyCat` | Number | Applies or references the 'T2CopyCat' effect/state. | 0 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
| `TempTrampleUntilSettled` | Number | Applies or references the 'TempTrampleUntilSettled' effect/state. | 0 |
| `Temporary` | `Block` | A wrapper block for applying status effects that automatically expire. | 0 |
| `ThornsDamageImmuneUntilSettled` | `Number` | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. | 0 |
| `TileDamageImmuneUntilSettled` | `Number` | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. | 0 |
| `TransformWeapon` | Block | Transforms the equipped weapon into another specific weapon state. | 0 |
| `WeaponAuxMultiplier` | Enum/String | Applies or references the 'WeaponAuxMultiplier' effect/state. | 0 |
| `status` | Enum/String | The status effect to apply. | 0 |

</details>

---

### Object: `keyword_tooltips`
### Object: `keyword_tooltips`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |
| `TemporaryItem` | Number | Applies or references the 'TemporaryItem' effect/state. | 1 |

</details>

---

### Object: `EvolveAbilityFromPool`
### Object: `EvolveAbilityFromPool`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 13 |
| `upgraded` | Boolean |  | 13 |

</details>

---

### Object: `KnockUpAndAway`
### Object: `KnockUpAndAway`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`Conditional_LastHit`](./Abilities_and_Spells.md#object-conditional_lasthit), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | The distance in tiles to knock the target away. | 20 |
| `stacks` | Mixed | Number of stacks or intensity to apply. | 18 |
| `height` | Number |  | 2 |
| `circular_variance` | Number |  | 1 |

</details>

---

### Object: `additional_passives`
### Object: `additional_passives`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#object-spawn)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 17 |

</details>

---

### Object: `RandomStatusFromPool`
### Object: `RandomStatusFromPool`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 19

> **Referenced by:** [`ApplyMultipleTimes`](./Abilities_and_Spells.md#object-applymultipletimes), [`Conditional_CanBeHealed`](./Abilities_and_Spells.md#object-conditional_canbehealed), [`Conditional_HasCleansableDebuffs`](./Abilities_and_Spells.md#object-conditional_hascleansabledebuffs), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 31 |

</details>

---

### Object: `Consumed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#object-conditional_buddy), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#object-conditional_livingplayercat), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 23 |
| `use_placeholder` | Boolean |  | 1 |
| `do_not_pop_corpse` | `Boolean` |  | 0 |
| `drop_body_ability` | `Enum/String` |  | 0 |
| `drop_on_death` | `Enum/String` |  | 0 |
| `drop_on_self_death` | `Boolean` |  | 0 |
| `extra_statuses` | `Block` | Additional generic status applications. | 0 |
| `force_contact` | `Boolean` | If true, enforces physical overlap. | 0 |
| `instant` | `Boolean` |  | 0 |
| `kill_on_consume` | `Boolean` |  | 0 |
| `mount_mode` | `Enum/String` | If true, treats the consumption as riding/mounting instead of eating. | 0 |
| `struggle_ability` | `Enum/String` | Ability triggered by the consumed entity while inside the consumer. | 0 |
| `wet` | `Boolean` |  | 0 |

</details>

---

### Object: `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 17

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 29 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |
  | `ExplodeCharacter_PartyBoss` | Integer | Applies or references the 'ExplodeCharacter_PartyBoss' effect/state. | 0 |
  | `ExplodeCharacter_RockCrusher_PetrifyBreak` | Integer | Applies or references the 'ExplodeCharacter_RockCrusher_PetrifyBreak' effect/state. | 0 |
| `ApplyToRandomPartyMemberIfPossible` | Block | Redirects the nested effects to apply to a random living member of the player's party. | 0 |
| `ApplyToSource` | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `BonusDamage` | String | Applies or references the 'BonusDamage' effect/state. | 0 |
| `CanApplyToInanimate` | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 0 |
| `CatPartsTransform` | Block | Transforms specific body parts into different visual variants. | 0 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 0 |
| `Conditional_Displaceable` | Block | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 0 |
| `Conditional_GoodRoll` | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 0 |
| `Conditional_HasStatus` | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 0 |
| `Conditional_HealthThreshold` | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 0 |
| `Conditional_Object` | Block | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 0 |
| `Conditional_Speculative` | Block | A simulation block used by the AI to test hypothetical outcomes before committing to an action. | 0 |
| `Consumed` | Block | State block triggered when this object or entity is eaten/consumed by another character. | 0 |
| `DestroyEquipmentAndAttachParasite` | Block | Removes an equipped item and replaces it with a parasite from a specified pool. | 0 |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. | 0 |
| `DoDamage` | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 0 |
| `Else` | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 0 |
| `ExplodeCharacter` | Number | Applies or references the 'ExplodeCharacter' effect/state. | 0 |
| `ExplodeCharacter_NoDie` | `Number` | Applies or references the 'ExplodeCharacter_NoDie' effect/state. | 0 |
| `ExplodeCharacter_Party` | Number | Applies or references the 'ExplodeCharacter_Party' effect/state. | 0 |
| `FaceCamera` | Number | Applies or references the 'FaceCamera' effect/state. | 0 |
| `FlatAIBonus` | Number | Applies or references the 'FlatAIBonus' effect/state. | 0 |
| `ForceImmediateMove` | Number | Applies or references the 'ForceImmediateMove' effect/state. | 0 |
| `FormChange` | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 0 |
| `GainDisorderFromPool_PostCast` | Enum/String | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 0 |
| `GenericDebuff` | Number | Applies or references the 'GenericDebuff' effect/state. | 0 |
| `ImmediateUseAbility` | Enum/String | Applies or references the 'ImmediateUseAbility' effect/state. | 0 |
| `Instakill` | Number | Applies or references the 'Instakill' effect/state. | 0 |
| `KnockUpAndAway` | Block | Displaces the target vertically and horizontally away from the source. | 0 |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 0 |
| `PurgeAll` | Number | Applies or references the 'PurgeAll' effect/state. | 0 |
| `RandomStatDown` | String | Applies or references the 'RandomStatDown' effect/state. | 0 |
| `RandomStatusFromPool` | Block | Selects and applies a random status effect from the provided nested block. | 0 |
| `RemoveMovePoints` | Number | Applies or references the 'RemoveMovePoints' effect/state. | 0 |
| `RemoveStatus` | `Enum/String` | Applies or references the 'RemoveStatus' effect/state. | 0 |
| `RemoveTurnsThisRound` | Number | Applies or references the 'RemoveTurnsThisRound' effect/state. | 0 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 0 |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. | 0 |
| `SetShield` | Number | Applies or references the 'SetShield' effect/state. | 0 |
| `ShowFakeDamage` | Block | Displays a visual damage number without actually modifying health. | 0 |
| `SpawnBearTrapIfHitKills` | Number | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. | 0 |
| `SpawnThingIfHitKills` | Enum/String | Applies or references the 'SpawnThingIfHitKills' effect/state. | 0 |
| `SpeculativeMoveSelfCorpseOffMap` | Number | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 0 |
| `Temporary` | Block | A wrapper block for applying status effects that automatically expire. | 0 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 0 |
| `VaporizeInanimate` | Number | Applies or references the 'VaporizeInanimate' effect/state. | 0 |
| `VisualFX` | `Enum/String` | Applies or references the 'VisualFX' effect/state. | 0 |
| `XIsTargetHealth` | `Block` | Math variable assignment: Evaluates X as the target's current health. | 0 |
| `status` | Enum/String | The specific status ID to check for. | 0 |

</details>

---

### Object: `FormChange`
### Object: `FormChange`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `form` | Mixed |  | 75 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Object: `ApplyToSourceOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| `CompleteItemQuest` | `Enum/String` | Applies or references the 'CompleteItemQuest' effect/state. | 0 |
| `EvolveAbilityFromPool` | `Enum/String` | Upgrades or transforms an existing ability into a new one from the specified pool. | 0 |
| `ManaGain` | `Number` | Applies or references the 'ManaGain' effect/state. | 0 |
| `RefreshActPoints` | `Number` | Applies or references the 'RefreshActPoints' effect/state. | 0 |
| `RemoveItem` | `Enum/String` | Applies or references the 'RemoveItem' effect/state. | 0 |
| `Revive` | `Number` | Applies or references the 'Revive' effect/state. | 0 |
| `TakeExtraTurn` | `Number` | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
| `TransformWeapon` | `Block` | Transforms the equipped weapon into another specific weapon state. | 0 |
| `WeaponAuxMultiplier` | `Enum/String` | Applies or references the 'WeaponAuxMultiplier' effect/state. | 0 |

</details>

---

### Object: `CanApplyToInanimate`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional_notboss), [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional_object), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |
| [`BreakIntoRocks`](./Enums.md#enum-breakintorocks) | Enum | Applies or references the 'BreakIntoRocks' effect/state. | 4 |
| `GetAggroTarget` | Number | Applies or references the 'GetAggroTarget' effect/state. | 2 |
| `PreventDeathTransforms` | Number | Applies or references the 'PreventDeathTransforms' effect/state. | 1 |
| `AddLeechesStatus` | Number | Applies or references the 'AddLeechesStatus' effect/state. | 0 |
| `AddWeaponAux` | String | Applies or references the 'AddWeaponAux' effect/state. | 0 |
| `ApplyToSource` | `Block` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 0 |
| `Craft` | Block | Synthesizes or spawns a new item from a specific pool. | 0 |
| `DisableWeapon` | Number | Applies or references the 'DisableWeapon' effect/state. | 0 |
| `DoDamage` | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 0 |
| `EvolveAbilityFromPool` | Enum/String | Upgrades or transforms an existing ability into a new one from the specified pool. | 0 |
| `FormChange` | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 0 |
| `KnockUpAndAway` | Block | Displaces the target vertically and horizontally away from the source. | 0 |
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 0 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 0 |
| `RefreshMovePoints` | Number | Applies or references the 'RefreshMovePoints' effect/state. | 0 |
| `RemoveStatus` | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 0 |
| `SpecificInjury` | Enum/String | Applies or references the 'SpecificInjury' effect/state. | 0 |
| `StanceSwitchToMelee` | Number | Applies or references the 'StanceSwitchToMelee' effect/state. | 0 |
| `StanceSwitchToRanged` | Number | Applies or references the 'StanceSwitchToRanged' effect/state. | 0 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
| `TempTrampleUntilSettled` | Number | Applies or references the 'TempTrampleUntilSettled' effect/state. | 0 |
| `Temporary` | `Block` | A wrapper block for applying status effects that automatically expire. | 0 |
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 0 |
| `status` | Enum/String | The status effect to apply. | 0 |

</details>

---

### Object: `CatPartsTransform`
### Object: `CatPartsTransform`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ear1` | Number | Sprite variant ID for the front ear. | 10 |
| `tail` | Number | Sprite variant ID for the tail. | 10 |
| `ear2` | Number |  | 9 |
| `arm2` | Number |  | 8 |
| `mouth` | Number |  | 8 |
| `arm1` | Number | Sprite variant ID for the front arm. | 7 |
| `leg1` | Number | Sprite variant ID for the front leg. | 5 |
| `leg2` | Number |  | 5 |
| `head` | Number | Sprite variant ID for the head. | 3 |
| `texture` | Number |  | 3 |
| `body` | Number | Sprite variant ID for the body. | 2 |
| `eye1` | Number |  | 1 |
| `eye2` | Number |  | 1 |
| `eyebrow1` | Number |  | 1 |
| `eyebrow2` | Number |  | 1 |
| `palette` | Number |  | 1 |

</details>

---

### Object: `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 13 |
  | `FactionConversion` | Integer | Applies or references the 'FactionConversion' effect/state. | 0 |
  | `PermanentCharm` | Integer | Applies the 'PermanentCharm' effect. | 0 |
  | `ExplodeCharacter_RockCrusher` | Integer | Applies or references the 'ExplodeCharacter_RockCrusher' effect/state. | 0 |
  | [`CanApplyToInanimate`](#canapplytoinanimate) | Object | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 0 |
  | `Vaporize` | Integer | Applies or references the 'Vaporize' effect/state. | 0 |
  | `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 0 |
  | `VaporizeInanimate` | Number | Applies or references the 'VaporizeInanimate' effect/state. | 0 |
  | [`Fear`](./Arrays.md#array-fear) | Array | Applies or references the 'Fear' effect/state. | 0 |
  | `Doomed` | Number | Applies or references the 'Doomed' effect/state. | 0 |
  | [`Conditional_HealthThreshold`](#conditionalhealththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 0 |
| `ApplyToSource` | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `BonusDamage` | Enum/String | Applies or references the 'BonusDamage' effect/state. | 0 |
| `Die` | Number | Applies or references the 'Die' effect/state. | 0 |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. | 0 |
| `FlatLeech` | Number | Applies or references the 'FlatLeech' effect/state. | 0 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 0 |
| `Instakill` | Number | Applies or references the 'Instakill' effect/state. | 0 |
| `SpawnThingIfHitKills` | Enum/String | Applies or references the 'SpawnThingIfHitKills' effect/state. | 0 |
| `Temporary` | Block | A wrapper block for applying status effects that automatically expire. | 0 |
| `threshold_expr` | Enum/String |  | 0 |
| `threshold_flat` | Number | A flat numerical health value threshold. | 0 |
| `threshold_percent` | Number | A percentage-based health threshold (e.g. 50%). | 0 |

</details>

---

### Object: `Conditional_HasStatus`
### Object: `Conditional_HasStatus`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional_boss), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 22 |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 13 |
  | [`ImmediateUseAbility_Instant`](./Enums.md#enum-immediateuseability_instant) | Enum | Applies or references the 'ImmediateUseAbility_Instant' effect/state. | 0 |

</details>

---

### Object: `RandomMagicMissile`
### Object: `RandomMagicMissile`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `full_size` | Boolean | If true, fires normal sized missiles instead of mini ones. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Object: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 40 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 12 |
| `AddLeechesStatus` | Number | Applies or references the 'AddLeechesStatus' effect/state. | 0 |
| `AddWeaponAux` | String | Applies or references the 'AddWeaponAux' effect/state. | 0 |
| `ApplyToRandomPartyMemberIfPossible` | `Block` | Redirects the nested effects to apply to a random living member of the player's party. | 0 |
| `ApplyToSource` | `Block` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 0 |
| `Craft` | Block | Synthesizes or spawns a new item from a specific pool. | 0 |
| `DisableWeapon` | Number | Applies or references the 'DisableWeapon' effect/state. | 0 |
| `DoDamage` | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 0 |
| `EvolveAbilityFromPool` | Enum/String | Upgrades or transforms an existing ability into a new one from the specified pool. | 0 |
| `FormChange` | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 0 |
| `GainDisorder` | `Enum/String` | Applies or references the 'GainDisorder' effect/state. | 0 |
| `GainDisorderFromPool_PostCast` | `Enum/String` | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 0 |
| `ImmediateUseAbility` | `Enum/String` | Applies or references the 'ImmediateUseAbility' effect/state. | 0 |
| `KnockUpAndAway` | Block | Displaces the target vertically and horizontally away from the source. | 0 |
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 0 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 0 |
| `RefreshMovePoints` | Number | Applies or references the 'RefreshMovePoints' effect/state. | 0 |
| `RefreshWeaponAbility` | `Number` | Applies or references the 'RefreshWeaponAbility' effect/state. | 0 |
| `RemoveStatus` | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 0 |
| `ShowText` | `String` | Applies or references the 'ShowText' effect/state. | 0 |
| `SpecificInjury` | Enum/String | Applies or references the 'SpecificInjury' effect/state. | 0 |
| `StanceSwitchToMelee` | Number | Applies or references the 'StanceSwitchToMelee' effect/state. | 0 |
| `StanceSwitchToRanged` | Number | Applies or references the 'StanceSwitchToRanged' effect/state. | 0 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
| `TempTrampleUntilSettled` | Number | Applies or references the 'TempTrampleUntilSettled' effect/state. | 0 |

</details>

---

### Object: `Conditional_Speculative`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`Conditional_AffectedByElement`](./Abilities_and_Spells.md#object-conditional_affectedbyelement), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `ApplyToRandomPartyMemberIfPossible` | Block | Redirects the nested effects to apply to a random living member of the player's party. | 0 |
| `ApplyToSource` | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 0 |
| `BonusDamageBasedOnDistance` | `Number` | Applies or references the 'BonusDamageBasedOnDistance' effect/state. | 0 |
| `CanApplyToInanimate` | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 0 |
| `CapDamage` | `Number` | Applies or references the 'CapDamage' effect/state. | 0 |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 0 |
| `CatPartsTransform` | Block | Transforms specific body parts into different visual variants. | 0 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 0 |
| `Conditional_Displaceable` | Block | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 0 |
| `Conditional_GoodRoll` | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 0 |
| `Conditional_HasStatus` | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 0 |
| `Conditional_HasTag` | Block | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 0 |
| `Conditional_HealthThreshold` | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 0 |
| `Conditional_Object` | Block | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 0 |
| `Conditional_Speculative` | Block | A simulation block used by the AI to test hypothetical outcomes before committing to an action. | 0 |
| `Consumed` | Block | State block triggered when this object or entity is eaten/consumed by another character. | 0 |
| `DestroyEquipmentAndAttachParasite` | Block | Removes an equipped item and replaces it with a parasite from a specified pool. | 0 |
| `Die` | Number | Applies or references the 'Die' effect/state. | 0 |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. | 0 |
| `DoDamage` | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 0 |
| `ExplodeCharacter` | Number | Applies or references the 'ExplodeCharacter' effect/state. | 0 |
| `ExplodeCharacter_Party` | Number | Applies or references the 'ExplodeCharacter_Party' effect/state. | 0 |
| `FaceCamera` | Number | Applies or references the 'FaceCamera' effect/state. | 0 |
| `FactionConversion` | Number | Applies or references the 'FactionConversion' effect/state. | 0 |
| `FlatAIBonus` | Number | Applies or references the 'FlatAIBonus' effect/state. | 0 |
| `FlatLeech` | Number | Applies or references the 'FlatLeech' effect/state. | 0 |
| `ForceImmediateMove` | Number | Applies or references the 'ForceImmediateMove' effect/state. | 0 |
| `FormChange` | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 0 |
| `GainDisorderFromPool_PostCast` | Enum/String | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 0 |
| `GenericDebuff` | Number | Applies or references the 'GenericDebuff' effect/state. | 0 |
| `IgnoreDamage` | `Number` | Applies or references the 'IgnoreDamage' effect/state. | 0 |
| `ImmediateUseAbility` | Enum/String | Applies or references the 'ImmediateUseAbility' effect/state. | 0 |
| `Instakill` | Number | Applies or references the 'Instakill' effect/state. | 0 |
| `KnockUpAndAway` | Block | Displaces the target vertically and horizontally away from the source. | 0 |
| `OverrideDamage` | Number | Applies or references the 'OverrideDamage' effect/state. | 0 |
| `PurgeAll` | Number | Applies or references the 'PurgeAll' effect/state. | 0 |
| `RandomBonusDamage` | `Number` | Applies or references the 'RandomBonusDamage' effect/state. | 0 |
| `RandomStatDown` | String | Applies or references the 'RandomStatDown' effect/state. | 0 |
| `RandomStatusFromPool` | Block | Selects and applies a random status effect from the provided nested block. | 0 |
| `RemoveMovePoints` | Number | Applies or references the 'RemoveMovePoints' effect/state. | 0 |
| `RemoveTurnsThisRound` | Number | Applies or references the 'RemoveTurnsThisRound' effect/state. | 0 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 0 |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. | 0 |
| `SetShield` | Number | Applies or references the 'SetShield' effect/state. | 0 |
| `ShowFakeDamage` | Block | Displays a visual damage number without actually modifying health. | 0 |
| `SpawnBearTrapIfHitKills` | Number | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. | 0 |
| `SpawnThingIfHitKills` | Enum/String | Applies or references the 'SpawnThingIfHitKills' effect/state. | 0 |
| `SpeculativeMoveSelfCorpseOffMap` | Number | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 0 |
| `Temporary` | Block | A wrapper block for applying status effects that automatically expire. | 0 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 0 |
| `VaporizeInanimate` | Number | Applies or references the 'VaporizeInanimate' effect/state. | 0 |
| `XIsTargetHealth` | Block | Math variable assignment: Evaluates X as the target's current health. | 0 |
| `threshold_expr` | Enum/String |  | 0 |
| `threshold_flat` | Number | A flat numerical health value threshold. | 0 |
| `threshold_percent` | Number | A percentage-based health threshold (e.g. 50%). | 0 |

</details>

---

### Object: `DoScreenShake`
### Object: `DoScreenShake`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#object-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `intensity` | Number |  | 10 |
| `time` | Mixed |  | 10 |

</details>

---

### Object: `ChanceToBreakFree`
### Object: `ChanceToBreakFree`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ability triggered upon successfully breaking free. | 11 |
| [`fail_ability`](./Enums.md#enum-fail_ability) | Enum | The ability triggered if the break free attempt fails. | 3 |
| `stacks` | Number | Percentage base chance to break free. | 3 |

</details>

---

### Object: `ChangeTile`
### Object: `ChangeTile`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tile`](./Arrays.md#array-tile) | Array | The specific tile type to change into (e.g., GlassTile). | 11 |
| `chance` | Mixed | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |
| `aoe` | Number |  | 1 |

</details>

---

### Object: `Cleave`
### Object: `Cleave`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0) that the cleave effect triggers. | 1 |

</details>

---

### Object: `ApplyPassives`
### Object: `ApplyPassives`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`Conditional_RandomChance`](./Abilities_and_Spells.md#object-conditional_randomchance), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 13 |

</details>

---

### Object: `Conditional_FormulaIsPositive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |
| [`formula`](./Math_Equations.md) | Equation | The math expression to evaluate. | 8 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `X` | Variable |  | 0 |
| `OverrideKnockbackDamage` | `Enum/String` | Applies or references the 'OverrideKnockbackDamage' effect/state. | 0 |

</details>

---

### Object: `Craft`
### Object: `Craft`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 9 |
| [`slot`](./Enums.md#enum-slot) | Enum |  | 8 |
| `temporary` | Boolean |  | 4 |
| `works_with_tech` | Boolean |  | 1 |

</details>

---

### Object: `ApplyStatusIfCrit`
### Object: `ApplyStatusIfCrit`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| `ApplyToSource` | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `ApplyToSourceOnKill` | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 0 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 0 |
| `Conditional_Enemy` | `Block` | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 0 |
| `Conditional_FinishedSpawning` | Block | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. | 0 |
| `Conditional_NotBoss` | Block | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 0 |
| `DisplaceToAbilityTarget` | Number | Applies or references the 'DisplaceToAbilityTarget' effect/state. | 0 |
| `FlatAIBonus` | `Number` | Applies or references the 'FlatAIBonus' effect/state. | 0 |
| `ForceMoveTowards` | Number | Applies or references the 'ForceMoveTowards' effect/state. | 0 |
| `Revive` | `Number` | Applies or references the 'Revive' effect/state. | 0 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
| `Temporary` | Block | A wrapper block for applying status effects that automatically expire. | 0 |

</details>

---

### Object: `Conditional_InForm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#object-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum | The specific form ID to check for. | 7 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `ForceImmediateMoveAndAttack` | `Block` | Forces the character to immediately move to a target and use a specified ability. | 0 |
| `FormChange` | `Enum/String` | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `UseAbility` | `Enum/String` | Forces the character or target to instantly use a specified ability. | 0 |

</details>

---

### Object: `ForceAttack`
### Object: `ForceAttack`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `immediate` | Boolean |  | 2 |

</details>

---

### Object: `BackflipWhenTargeted`
### Object: `BackflipWhenTargeted`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific dodge ability to trigger (e.g., DestroyerDodge). | 4 |
| `stacks` | Number | Number of stacks or intensity to apply. | 4 |

</details>

---

### Object: `Conditional_HealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional_notboss), [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional_speculative), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |
| `threshold_flat` | Number | A flat numerical health value threshold. | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `threshold_percent` | Number | A percentage-based health threshold (e.g. 50%). | 2 |
| [`threshold_expr`](./Math_Equations.md) | Equation |  | 1 |
| `AddLeechesStatus` | Number | Applies or references the 'AddLeechesStatus' effect/state. | 0 |
| `AddWeaponAux` | String | Applies or references the 'AddWeaponAux' effect/state. | 0 |
| `ApplyToSource` | `Block` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `BonusDamage` | `Enum/String` | Applies or references the 'BonusDamage' effect/state. | 0 |
| `CaptureFamiliar` | `Number` | Applies or references the 'CaptureFamiliar' effect/state. | 0 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 0 |
| `Craft` | Block | Synthesizes or spawns a new item from a specific pool. | 0 |
| `Die` | `Number` | Applies or references the 'Die' effect/state. | 0 |
| `DieViolently` | `Number` | Applies or references the 'DieViolently' effect/state. | 0 |
| `DisableWeapon` | Number | Applies or references the 'DisableWeapon' effect/state. | 0 |
| `DoDamage` | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 0 |
| `EvolveAbilityFromPool` | Enum/String | Upgrades or transforms an existing ability into a new one from the specified pool. | 0 |
| `FactionConversion` | `Number` | Applies or references the 'FactionConversion' effect/state. | 0 |
| `FlatLeech` | `Number` | Applies or references the 'FlatLeech' effect/state. | 0 |
| `FormChange` | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 0 |
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 0 |
| `KnockUpAndAway` | Block | Displaces the target vertically and horizontally away from the source. | 0 |
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 0 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 0 |
| `RefreshMovePoints` | Number | Applies or references the 'RefreshMovePoints' effect/state. | 0 |
| `RemoveStatus` | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 0 |
| `SpawnThingIfHitKills` | `Enum/String` | Applies or references the 'SpawnThingIfHitKills' effect/state. | 0 |
| `SpecificInjury` | Enum/String | Applies or references the 'SpecificInjury' effect/state. | 0 |
| `StanceSwitchToMelee` | Number | Applies or references the 'StanceSwitchToMelee' effect/state. | 0 |
| `StanceSwitchToRanged` | Number | Applies or references the 'StanceSwitchToRanged' effect/state. | 0 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
| `TempTrampleUntilSettled` | Number | Applies or references the 'TempTrampleUntilSettled' effect/state. | 0 |
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 0 |

</details>

---

### Object: `Conditional_Object`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| `ApplyToRandomPartyMemberIfPossible` | Block | Redirects the nested effects to apply to a random living member of the player's party. | 0 |
| `ApplyToSource` | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `ApplyToSourceOnKill` | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 0 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 0 |
| `CanApplyToInanimate` | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 0 |
| `CatPartsTransform` | Block | Transforms specific body parts into different visual variants. | 0 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 0 |
| `Conditional_Boss` | Block | Conditional trigger: Executes nested logic if the target is a Boss. | 0 |
| `Conditional_Displaceable` | Block | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 0 |
| `Conditional_GoodRoll` | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 0 |
| `Conditional_HasStatus` | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 0 |
| `Conditional_HasTag` | Block | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 0 |
| `Conditional_HealthThreshold` | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 0 |
| `Conditional_InForm` | Block | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 0 |
| `Conditional_NotBoss` | Block | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 0 |
| `Conditional_Object` | Block | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 0 |
| `Conditional_Speculative` | Block | A simulation block used by the AI to test hypothetical outcomes before committing to an action. | 0 |
| `Consumed` | Block | State block triggered when this object or entity is eaten/consumed by another character. | 0 |
| `CrackMoonHead` | Number | Applies or references the 'CrackMoonHead' effect/state. | 0 |
| `DeleteObject` | Number | Applies or references the 'DeleteObject' effect/state. | 0 |
| `DestroyEquipmentAndAttachParasite` | Block | Removes an equipped item and replaces it with a parasite from a specified pool. | 0 |
| `Die` | Number | Applies or references the 'Die' effect/state. | 0 |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. | 0 |
| `DisplaceTowardsSource` | Number | Applies or references the 'DisplaceTowardsSource' effect/state. | 0 |
| `DoDamage` | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 0 |
| `ExplodeCharacter` | Number | Applies or references the 'ExplodeCharacter' effect/state. | 0 |
| `ExplodeCharacter_Party` | Number | Applies or references the 'ExplodeCharacter_Party' effect/state. | 0 |
| `FaceAway` | Number | Applies or references the 'FaceAway' effect/state. | 0 |
| `FaceCamera` | Number | Applies or references the 'FaceCamera' effect/state. | 0 |
| `FlatAIBonus` | Number | Applies or references the 'FlatAIBonus' effect/state. | 0 |
| `FloatingRockTrap` | Number | Applies or references the 'FloatingRockTrap' effect/state. | 0 |
| `ForceImmediateMove` | Number | Applies or references the 'ForceImmediateMove' effect/state. | 0 |
| `FormChange` | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 0 |
| `GainDisorderFromPool_PostCast` | Enum/String | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 0 |
| `GenericDebuff` | Number | Applies or references the 'GenericDebuff' effect/state. | 0 |
| `IgnoreDamage` | Number | Applies or references the 'IgnoreDamage' effect/state. | 0 |
| `ImmediateUseAbility` | Enum/String | Applies or references the 'ImmediateUseAbility' effect/state. | 0 |
| `Instakill` | Number | Applies or references the 'Instakill' effect/state. | 0 |
| `KnockUpAndAway` | Block | Displaces the target vertically and horizontally away from the source. | 0 |
| `MergeDamageInstance` | Block | Combines damage numbers or visual hit effects. | 0 |
| `OverrideDamage` | Number | Applies or references the 'OverrideDamage' effect/state. | 0 |
| `PopAndSpawn` | Block | Destroys the target and replaces it with a new spawned entity. | 0 |
| `PurgeAll` | Number | Applies or references the 'PurgeAll' effect/state. | 0 |
| `RandomStatDown` | String | Applies or references the 'RandomStatDown' effect/state. | 0 |
| `RandomStatusFromPool` | Block | Selects and applies a random status effect from the provided nested block. | 0 |
| `RemoveMovePoints` | Number | Applies or references the 'RemoveMovePoints' effect/state. | 0 |
| `RemoveStatus` | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 0 |
| `RemoveTurnsThisRound` | Number | Applies or references the 'RemoveTurnsThisRound' effect/state. | 0 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 0 |
| `ScatterRandomPickups` | Number | Applies or references the 'ScatterRandomPickups' effect/state. | 0 |
| `SetAnimationAlts` | Block | Overrides specific animation states with alternative animations. | 0 |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. | 0 |
| `SetKnockback` | Number | Applies or references the 'SetKnockback' effect/state. | 0 |
| `SetShield` | Number | Applies or references the 'SetShield' effect/state. | 0 |
| `ShowFakeDamage` | Block | Displays a visual damage number without actually modifying health. | 0 |
| `SpawnBearTrapIfHitKills` | Number | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. | 0 |
| `SpawnThingIfHitKills` | Enum/String | Applies or references the 'SpawnThingIfHitKills' effect/state. | 0 |
| `SpeculativeMoveSelfCorpseOffMap` | Number | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 0 |
| `Temporary` | Block | A wrapper block for applying status effects that automatically expire. | 0 |
| `UseAbility` | Enum/String | Forces the character or target to instantly use a specified ability. | 0 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 0 |
| `VaporizeCorpse` | Number | Applies or references the 'VaporizeCorpse' effect/state. | 0 |
| `VaporizeInanimate` | Number | Applies or references the 'VaporizeInanimate' effect/state. | 0 |
| `XIsTargetHealth` | Block | Math variable assignment: Evaluates X as the target's current health. | 0 |
| `tag` | Enum/String | The specific string tag to check for. | 0 |

</details>

---

### Object: `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `AddLeechesStatus` | Number | Applies or references the 'AddLeechesStatus' effect/state. | 0 |
| `AddWeaponAux` | String | Applies or references the 'AddWeaponAux' effect/state. | 0 |
| `ApplyToSource` | `Block` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `Cleanse` | `Number` | Applies or references the 'Cleanse' effect/state. | 0 |
| `ConjureRandomAbilityFromCat` | `Number` | Applies or references the 'ConjureRandomAbilityFromCat' effect/state. | 0 |
| `Craft` | Block | Synthesizes or spawns a new item from a specific pool. | 0 |
| `DisableWeapon` | Number | Applies or references the 'DisableWeapon' effect/state. | 0 |
| `DoDamage` | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 0 |
| `EvolveAbilityFromPool` | Enum/String | Upgrades or transforms an existing ability into a new one from the specified pool. | 0 |
| `FormChange` | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 0 |
| `GenericDebuff` | `Number` | Applies or references the 'GenericDebuff' effect/state. | 0 |
| `KnockOutClone` | `Enum/String` | Applies or references the 'KnockOutClone' effect/state. | 0 |
| `KnockUpAndAway` | Block | Displaces the target vertically and horizontally away from the source. | 0 |
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 0 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 0 |
| `RefreshMovePoints` | Number | Applies or references the 'RefreshMovePoints' effect/state. | 0 |
| `RemoveStatus` | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 0 |
| `SpecificInjury` | Enum/String | Applies or references the 'SpecificInjury' effect/state. | 0 |
| `StanceSwitchToMelee` | Number | Applies or references the 'StanceSwitchToMelee' effect/state. | 0 |
| `StanceSwitchToRanged` | Number | Applies or references the 'StanceSwitchToRanged' effect/state. | 0 |
| `T2CopyCat` | `Number` | Applies or references the 'T2CopyCat' effect/state. | 0 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
| `TempTrampleUntilSettled` | Number | Applies or references the 'TempTrampleUntilSettled' effect/state. | 0 |

</details>

---

### Object: `ConjureBonusAbility`
### Object: `ConjureBonusAbility`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to conjure. | 2 |
| `upgraded` | Boolean | If true, conjures the upgraded version of the ability. | 2 |

</details>

---

### Object: `DoDistortionRing`
### Object: `DoDistortionRing`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `intensity` | Number |  | 6 |
| `radius` | Number | Distance or area of effect in tiles. | 6 |
| `speed` | Number |  | 6 |

</details>

---

### Object: `Metronome`
### Object: `Metronome`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`banned_abilities`](./Arrays.md#array-banned_abilities) | Array |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Object: `ObjectOnHitCharacter`
### Object: `ObjectOnHitCharacter`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the character to spawn (e.g., CharmedFlea). | 2 |
| `chance` | Mixed | Probability (0.0 to 1.0) of spawning. | 2 |

</details>

---

### Object: `SwitchMusic`
### Object: `SwitchMusic`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#object-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | The specific audio layer to transition to (e.g., map, battle). | 6 |
| [`new_song`](./Enums.md#enum-new_song) | Enum | The ID of the new music track. | 5 |
| `crossfade_speed` | Number |  | 1 |

</details>

---

### Object: `TwisterDisplaceWithDamage`
### Object: `TwisterDisplaceWithDamage`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Mixed | The damage formula or inherit flag. | 6 |
| `max_dist` | Number | Maximum displacement distance. | 6 |
| `min_dist` | Number | Minimum displacement distance. | 2 |
| [`exclude_prefix`](./Enums.md#enum-exclude_prefix) | Enum |  | 1 |

</details>

---

### Object: `CollectsPickupsWithAltEffects`
### Object: `CollectsPickupsWithAltEffects`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| `CurrentWeaponAddPoison` | Number | Applies or references the 'CurrentWeaponAddPoison' effect/state. | 1 |

</details>

---

### Object: `DestroyEquipmentAndAttachParasite`
### Object: `DestroyEquipmentAndAttachParasite`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`Conditional_ActiveWeather_Any`](./Abilities_and_Spells.md#object-conditional_activeweather_any), [`Conditional_DebuffRoll`](./Abilities_and_Spells.md#object-conditional_debuffroll), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | The item pool to draw the parasite from. | 5 |
| `chance` | Mixed | Probability (0.0 to 1.0 or percentage) of this occurring. | 3 |

</details>

---

### Object: `DoDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`Else`](./Abilities_and_Spells.md#object-else), [`post_spawn_statuses`](./Abilities_and_Spells.md#object-post_spawn_statuses)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |
| [`type`](./Enums.md#enum-type) | Enum | The classification of the damage (e.g., spell, melee). | 5 |
| `damage` | Number | The flat damage amount. | 5 |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum |  | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| `effects` | `Block` | Non-damaging status applications and logic triggers executed on impact. | 0 |

</details>

---

### Object: `LeaveBehind`
### Object: `LeaveBehind`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#object-temporary_effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID to spawn. | 4 |

</details>

---

### Object: `ObjectOnHit`
### Object: `ObjectOnHit`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the object to spawn (e.g., Poop). | 2 |

</details>

---

### Object: `ApplyToConsumed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| `DeleteObject` | `Number` | Applies or references the 'DeleteObject' effect/state. | 0 |
| `Die` | `Number` | Applies or references the 'Die' effect/state. | 0 |

</details>

---

### Object: `ArcLightning`
### Object: `ArcLightning`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, the arc will not bounce to friendly targets. | 4 |
| `max_distance` | Number | The maximum tile range the lightning can jump between bounces. | 4 |
| `stacks` | Number | The maximum number of targets the lightning can bounce to. | 4 |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| `ignore_self` | Boolean | If true, prevents the arc from bouncing back to the caster. | 1 |

</details>

---

### Object: `Conditional_Familiar`
### Object: `Conditional_Familiar`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `GainCoinsRange`
### Object: `GainCoinsRange`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number | Maximum coins granted. | 4 |
| `min` | Number | Minimum coins granted. | 4 |

</details>

---

### Object: `LateStatusApplication`
### Object: `LateStatusApplication`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `AddWeaponAux` | Number | Applies or references the 'AddWeaponAux' effect/state. | 0 |
  | `CurrentWeaponDamageUp` | Number | Applies or references the 'CurrentWeaponDamageUp' effect/state. | 0 |

</details>

---

### Object: `ReplaceSpell`
### Object: `ReplaceSpell`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#object-temppassivewhilehasstatus)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The new ability ID to insert. | 4 |
| `slot` | Number | The spell slot index to replace. | 4 |

</details>

---

### Object: `ReviveNextRound`
### Object: `ReviveNextRound`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#object-additional_passives), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `revive_health` | Number | The flat amount of health to revive with. | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Object: `TakeBonusTurnWithStatus`
### Object: `TakeBonusTurnWithStatus`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `TempPassiveWhileHasStatus`
### Object: `TempPassiveWhileHasStatus`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`Conditional_FirstApplicationThisTurn`](./Abilities_and_Spells.md#object-conditional_firstapplicationthisturn), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#object-conditional_livingplayercat)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The required status effect. | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `TimeDelayStatusApplication`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `delay` | Mixed | The float time delay in seconds. | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `Cleanse` | `Number` | Applies or references the 'Cleanse' effect/state. | 0 |
| `DoScreenShake` | `Block` | Triggers a camera screen shake effect. | 0 |
| `FormChange` | `Enum/String` | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 0 |
| `GlobalSpawnCharacter` | `Enum/String` | Applies or references the 'GlobalSpawnCharacter' effect/state. | 0 |
| `LowerAmbientLight` | Block | A visual effect that dims the map's lighting. | 0 |
| `PlayBackground` | `Number` | Applies or references the 'PlayBackground' effect/state. | 0 |
| `SwitchMusic` | `Block` | Changes the background music track or layer during combat. | 0 |
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 0 |

</details>

---

### Object: `post_spawn_statuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#object-spawn)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `DoDamage` | `Block` | Explicitly triggers a secondary damage instance independent of the main attack. | 0 |
| `EnterMount` | `Enum/String` | Applies or references the 'EnterMount' effect/state. | 0 |
| `VisualFXTile` | `Enum/String` | Applies or references the 'VisualFXTile' effect/state. | 0 |
| `effects` | Block | Non-damaging status applications and logic triggers executed on impact. | 0 |

</details>

---

### Object: `rocket_swirl`
### Object: `rocket_swirl`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#object-graphics)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`radius`](./Arrays.md#array-radius) | Array | Swirl radius. | 4 |
| [`speed`](./Arrays.md#array-speed) | Array | Rotations per second. | 4 |

</details>

---

### Object: `ApplyMultipleTimes`
### Object: `ApplyMultipleTimes`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
| `stacks` | Mixed | The number of times the nested effects block should be repeatedly executed. | 3 |

</details>

---

### Object: `BounceObject`
### Object: `BounceObject`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`obj`](./Enums.md#enum-obj) | Enum | The entity ID of the object to spawn (e.g., chapter_corpse_medium). | 3 |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0) of spawning the object. | 2 |
| `slide` | Number |  | 1 |

</details>

---

### Object: `CatPartsSizeScaleStatus`
### Object: `CatPartsSizeScaleStatus`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `arm1` | Number | Scale multiplier for the front arm. | 1 |
| `arm2` | Number | Scale multiplier for the back arm. | 1 |
| `body` | Number |  | 1 |
| `mouth` | Number |  | 1 |

</details>

---

### Object: `Conditional_AffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type to check for. | 3 |
  | [`Conditional_Speculative`](#conditional_speculative) | Object | A simulation block used by the AI to test hypothetical outcomes before committing to an action. | 0 |
  | `BonusCritChance` | Integer | Applies the 'BonusCritChance' effect. | 0 |
  | `Burn` | Number | Applies or references the 'Burn' effect/state. | 0 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 0 |
| `BonusDamageBasedOnDistance` | Number | Applies or references the 'BonusDamageBasedOnDistance' effect/state. | 0 |
| `CapDamage` | Number | Applies or references the 'CapDamage' effect/state. | 0 |
| `Conditional_HealthThreshold` | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 0 |
| `Else` | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 0 |
| `IgnoreDamage` | Number | Applies or references the 'IgnoreDamage' effect/state. | 0 |
| `RandomBonusDamage` | Number | Applies or references the 'RandomBonusDamage' effect/state. | 0 |

</details>

---

### Object: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. | 3 |
| `TempPassiveWhileHasStatus` | `Block` | Grants nested passives only while the character possesses the specified status. | 0 |
| `status` | Enum/String | The required status effect. | 0 |

</details>

---

### Object: `Conditional_LastHit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `BonusDamage` | `Number` | Applies or references the 'BonusDamage' effect/state. | 0 |
| `DelayCastAbility` | `Enum/String` | Queues an ability to be cast automatically after a certain delay or trigger. | 0 |
| `KnockUpAndAway` | `Block` | Displaces the target vertically and horizontally away from the source. | 0 |

</details>

---

### Object: `DustOnHit`
### Object: `DustOnHit`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The ID of the object/particle to spawn. | 3 |

</details>

---

### Object: `IncAuxCounterClamped`
### Object: `IncAuxCounterClamped`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `change` | Number |  | 3 |
| `max` | Number |  | 3 |

</details>

---

### Object: `SetCrazyEyeBackgroundWeights`
### Object: `SetCrazyEyeBackgroundWeights`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Arrays.md#array-weights) | Array |  | 3 |

</details>

---

### Object: `StatusOnBattleEnd`
### Object: `StatusOnBattleEnd`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ApplyPassives`](./Abilities_and_Spells.md#object-applypassives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 56 |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 3 |

</details>

---

### Object: `Tangled`
### Object: `Tangled`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_art`](./Enums.md#enum-alt_art) | Enum | The alternative sprite art to use while tangled. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Object: `extra_statuses`
### Object: `extra_statuses`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`Consumed`](./Abilities_and_Spells.md#object-consumed)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `AddStatusToBasicAttack`
### Object: `AddStatusToBasicAttack`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`PassiveWhileNotTakingTurn`](./Abilities_and_Spells.md#object-passivewhilenottakingturn), [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 119 |

</details>

---

### Object: `AfterImage`
### Object: `AfterImage`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#object-temporary_effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the visual decoy to spawn (e.g., PlayerCat_ThiefShade). | 2 |
| `skilltemp` | Boolean | If true, the decoy is automatically destroyed once the skill finishes executing. | 2 |

</details>

---

### Object: `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional_goodroll), [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| `GainDisorderFromPool_PostCast` | `Enum/String` | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 0 |

</details>

---

### Object: `ApplyToTile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_DestructibleCorpse`](./Abilities_and_Spells.md#object-conditional_destructiblecorpse)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `ObjectOnHit` | `Enum/String` | Spawns a specific physics/item object upon impact. | 0 |
| `SpawnBearTrap` | `Number` | Applies or references the 'SpawnBearTrap' effect/state. | 0 |

</details>

---

### Object: `AutocastEachRound`
### Object: `AutocastEachRound`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 2 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 1 |

</details>

---

### Object: `BodyGuard`
### Object: `BodyGuard`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to use when intercepting (e.g., BodyGuardSwap). | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Object: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
| [`odds`](./Enums.md#enum-odds) | Enum | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 2 |
| `DieViolently` | `Number` | Applies or references the 'DieViolently' effect/state. | 0 |
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 0 |

</details>

---

### Object: `Conditional_BossOrBig`
### Object: `Conditional_BossOrBig`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Conditional_NotBossOrBig`](#conditional_notbossorbig) | Object | Conditional trigger: Executes nested logic if the target is NEITHER a Boss nor large. | 0 |
  | [`Immobile`](./Arrays.md#array-immobile) | Number | Applies or references the 'Immobile' effect/state. | 0 |

</details>

---

### Object: `Conditional_Buddy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
  | [`Conditional_InForm`](#conditional_inform) | Object | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 0 |
  | [`Else`](#else) | Object | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 0 |
  | [`Consumed`](#consumed) | Object | State block triggered when this object or entity is eaten/consumed by another character. | 0 |
| `ApplyToRandomPartyMemberIfPossible` | Block | Redirects the nested effects to apply to a random living member of the player's party. | 0 |
| `ApplyToSource` | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 0 |
| `CanApplyToInanimate` | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 0 |
| `CatPartsTransform` | Block | Transforms specific body parts into different visual variants. | 0 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 0 |
| `Conditional_Displaceable` | Block | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 0 |
| `Conditional_GoodRoll` | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 0 |
| `Conditional_HasStatus` | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 0 |
| `Conditional_HasTag` | Block | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 0 |
| `Conditional_HealthThreshold` | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 0 |
| `Conditional_Object` | Block | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 0 |
| `Conditional_Speculative` | Block | A simulation block used by the AI to test hypothetical outcomes before committing to an action. | 0 |
| `DestroyEquipmentAndAttachParasite` | Block | Removes an equipped item and replaces it with a parasite from a specified pool. | 0 |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. | 0 |
| `DoDamage` | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 0 |
| `ExplodeCharacter` | Number | Applies or references the 'ExplodeCharacter' effect/state. | 0 |
| `ExplodeCharacter_Party` | Number | Applies or references the 'ExplodeCharacter_Party' effect/state. | 0 |
| `FaceCamera` | Number | Applies or references the 'FaceCamera' effect/state. | 0 |
| `FlatAIBonus` | Number | Applies or references the 'FlatAIBonus' effect/state. | 0 |
| `ForceImmediateMove` | Number | Applies or references the 'ForceImmediateMove' effect/state. | 0 |
| `ForceImmediateMoveAndAttack` | Block | Forces the character to immediately move to a target and use a specified ability. | 0 |
| `FormChange` | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 0 |
| `GainDisorderFromPool_PostCast` | Enum/String | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 0 |
| `GenericDebuff` | Number | Applies or references the 'GenericDebuff' effect/state. | 0 |
| `ImmediateUseAbility` | Enum/String | Applies or references the 'ImmediateUseAbility' effect/state. | 0 |
| `Instakill` | Number | Applies or references the 'Instakill' effect/state. | 0 |
| `KnockUpAndAway` | Block | Displaces the target vertically and horizontally away from the source. | 0 |
| `OverrideDamage` | Number | Applies or references the 'OverrideDamage' effect/state. | 0 |
| `PurgeAll` | Number | Applies or references the 'PurgeAll' effect/state. | 0 |
| `RandomStatDown` | String | Applies or references the 'RandomStatDown' effect/state. | 0 |
| `RandomStatusFromPool` | Block | Selects and applies a random status effect from the provided nested block. | 0 |
| `RemoveMovePoints` | Number | Applies or references the 'RemoveMovePoints' effect/state. | 0 |
| `RemoveTurnsThisRound` | Number | Applies or references the 'RemoveTurnsThisRound' effect/state. | 0 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 0 |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. | 0 |
| `SetShield` | Number | Applies or references the 'SetShield' effect/state. | 0 |
| `ShowFakeDamage` | Block | Displays a visual damage number without actually modifying health. | 0 |
| `SpawnBearTrapIfHitKills` | Number | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. | 0 |
| `SpawnThingIfHitKills` | Enum/String | Applies or references the 'SpawnThingIfHitKills' effect/state. | 0 |
| `SpeculativeMoveSelfCorpseOffMap` | Number | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 0 |
| `Temporary` | Block | A wrapper block for applying status effects that automatically expire. | 0 |
| `UseAbility` | Enum/String | Forces the character or target to instantly use a specified ability. | 0 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 0 |
| `VaporizeInanimate` | Number | Applies or references the 'VaporizeInanimate' effect/state. | 0 |
| `XIsTargetHealth` | Block | Math variable assignment: Evaluates X as the target's current health. | 0 |
| `do_not_pop_corpse` | Boolean |  | 0 |
| `drop_body_ability` | Enum/String |  | 0 |
| `drop_on_death` | Enum/String |  | 0 |
| `drop_on_self_death` | Boolean |  | 0 |
| `extra_statuses` | Block | Additional generic status applications. | 0 |
| `force_contact` | Boolean | If true, enforces physical overlap. | 0 |
| `form` | Enum/String | The specific form ID to check for. | 0 |
| `instant` | Boolean |  | 0 |
| `kill_on_consume` | Boolean |  | 0 |
| `mount_mode` | Enum/String | If true, treats the consumption as riding/mounting instead of eating. | 0 |
| `struggle_ability` | Enum/String | Ability triggered by the consumed entity while inside the consumer. | 0 |
| `use_placeholder` | Boolean |  | 0 |
| `wet` | Boolean |  | 0 |

</details>

---

### Object: `Conditional_DestructibleCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| `ApplyToTile` | `Block` | Redirects the nested effects to apply to the terrain/tile underneath the target rather than the target itself. | 0 |
| `ObjectOnHit` | Enum/String | Spawns a specific physics/item object upon impact. | 0 |
| `SpawnBearTrap` | Number | Applies or references the 'SpawnBearTrap' effect/state. | 0 |
| `VaporizeCorpse` | `Number` | Applies or references the 'VaporizeCorpse' effect/state. | 0 |

</details>

---

### Object: `Conditional_Displaceable`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
  | [`LaunchOffScreen`](./Math_Equations.md) | Equation | Applies or references the 'LaunchOffScreen' effect/state. | 0 |
  | `bonus_melee_ability_damage` | Any | Explicit empirical property. | 0 |
  | `LaunchOffScreenInstakill` | Integer | Applies or references the 'LaunchOffScreenInstakill' effect/state. | 0 |

</details>

---

### Object: `Conditional_IsSelf`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 0 |

</details>

---

### Object: `Conditional_NotAlly`
### Object: `Conditional_NotAlly`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `Conditional_NotBossOrBig`
### Object: `Conditional_NotBossOrBig`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Immobile`](./Arrays.md#array-immobile) | Number | Applies or references the 'Immobile' effect/state. | 0 |

</details>

---

### Object: `Conditional_NotShielded`
### Object: `Conditional_NotShielded`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`key`](./Enums.md#enum-key) | Enum |  | 2 |
| `CompleteItemQuest` | `Enum/String` | Applies or references the 'CompleteItemQuest' effect/state. | 0 |
| `TriggerGameEnding` | `Number` | Applies or references the 'TriggerGameEnding' effect/state. | 0 |

</details>

---

### Object: `Conditional_Shielded`
### Object: `Conditional_Shielded`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `SetItemAux` | Object | Applies or references the 'SetItemAux' effect/state. | 0 |
  | `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 0 |
  | `Cleave` | Object | Causes the attack to hit adjacent enemies alongside the primary target. | 0 |
  | [`Stun`](./Arrays.md#array-stun) | Array | Applies or references the 'Stun' effect/state. | 0 |
  | `BonusCritChance` | Integer | Applies the 'BonusCritChance' effect. | 0 |

</details>

---

### Object: `CopySpells`
### Object: `CopySpells`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |
| `upgraded` | Boolean |  | 1 |

</details>

---

### Object: `CreateGlobalModifiers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#object-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |
| `BloodRain` | `Number` | Applies or references the 'BloodRain' effect/state. | 0 |
| `LowerAmbientLight` | `Block` | A visual effect that dims the map's lighting. | 0 |

</details>

---

### Object: `FindItemFromPool`
### Object: `FindItemFromPool`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability of finding the item. | 2 |
| [`pool`](./Enums.md#enum-pool) | Enum | The item pool to draw from. | 1 |

</details>

---

### Object: `ForceMoveTowardsTaggedObject`
### Object: `ForceMoveTowardsTaggedObject`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The movement ability to use. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | The entity tag to seek out. | 1 |

</details>

---

### Object: `KnockOutCoin`
### Object: `KnockOutCoin`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Object: `LowerAmbientLight`
### Object: `LowerAmbientLight`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`CreateGlobalModifiers`](./Abilities_and_Spells.md#object-createglobalmodifiers)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array | The target opacity/dimness level. | 2 |
| `speed` | Number | The transition speed. | 2 |

</details>

---

### Object: `Math`
### Object: `Math`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Object: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#object-temppassivewhilehasstatus)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 36 |
  | [`AddDamageToElementDamage`](#adddamagetoelementdamage) | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 0 |
  | [`AddStatusToElementDamage`](#addstatustoelementdamage) | Object | Applies the 'AddStatusToElementDamage' effect. | 0 |
  | [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. | 0 |
  | [`StatusImmunity`](./Enums.md#enum-statusimmunity) | Enum | Applies or references the 'StatusImmunity' effect/state. | 0 |
| `effects` | `Block` | Non-damaging status applications and logic triggers executed on impact. | 0 |

</details>

---

### Object: `NextAttackSpecialCrit`
### Object: `NextAttackSpecialCrit`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Number | Flat addition to the critical damage multiplier. | 1 |
| `extra_coins_per_stack` | Number | Grants bonus coins based on stacks. | 1 |
| `luck_increase` | Number | Increases luck stat for the attack. | 1 |

</details>

---

### Object: `NukeQuestFinalBossModifications`
### Object: `NukeQuestFinalBossModifications`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage_instance`](./Abilities_and_Spells.md#object-damage_instance) | Object |  | 1 |
| [`splash_damage`](./Abilities_and_Spells.md#object-splash_damage) | Object | Secondary Area of Effect blast parameters. | 1 |
  | [`self_damage`](./Arrays.md#array-self_damage) | Object | Recoil or self-inflicted damage/effects applied to the caster. | 0 |

</details>

---

### Object: `OverHealToStatuses`
### Object: `OverHealToStatuses`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `stack_scale` | Number |  | 1 |

</details>

---

### Object: `QuakeAreaChance`
### Object: `QuakeAreaChance`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability of triggering the quake. | 2 |
| `radius` | Number | The tile radius of the quake. | 2 |

</details>

---

### Object: `RandomDistanceDisplace`
### Object: `RandomDistanceDisplace`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `min_dist` | Number | The minimum tile distance they will be moved. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Object: `RandomKnockback`
### Object: `RandomKnockback`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number | Maximum knockback distance. | 2 |
| `min` | Number | Minimum knockback distance. | 2 |

</details>

---

### Object: `ScatterCoins`
### Object: `ScatterCoins`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#object-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`stacks`](./Math_Equations.md) | Equation | Number of stacks or intensity to apply. | 2 |
| `stackable` | Boolean | If true, multiple instances of this trigger can stack. | 2 |

</details>

---

### Object: `SmartMetronome`
### Object: `SmartMetronome`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |
| `upgraded` | Boolean |  | 1 |

</details>

---

### Object: `TakeBonusTurnWithAIControl`
### Object: `TakeBonusTurnWithAIControl`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | If true, allows the AI to cast spells during this bonus turn. | 2 |

</details>

---

### Object: `TeamCastAbility`
### Object: `TeamCastAbility`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The underlying logic ability executed by the team. | 2 |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum | Requires participants to share this tag. | 2 |
| `same_orientation` | Boolean |  | 1 |

</details>

---

### Object: `XIsSpellStormRampAndReset`
### Object: `XIsSpellStormRampAndReset`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reset_percent` | Number | The percentage of stacks to keep after resetting. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Object: `XIsTargetHealth`
### Object: `XIsTargetHealth`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional_boss), [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 0 |

</details>

---

### Object: `empty_self_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `effects` | `Block` | Non-damaging status applications and logic triggers executed on impact. | 0 |

</details>

---

### Object: `AlphaStatusOnTurnBegin`
### Object: `AlphaStatusOnTurnBegin`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `ApplyPassivesToSpawnerWhileAlive`
### Object: `ApplyPassivesToSpawnerWhileAlive`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#object-additional_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `ApplyStatusesNextTurnBegin`
### Object: `ApplyStatusesNextTurnBegin`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `ApplyToOthersWithSharedTagAndFaction`
### Object: `ApplyToOthersWithSharedTagAndFaction`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Marked`](./Arrays.md#array-marked) | Array | Applies or references the 'Marked' effect/state. | 0 |

</details>

---

### Object: `ApplyToRandomClosestAlly`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `ForceMoveTowards` | `Number` | Applies or references the 'ForceMoveTowards' effect/state. | 0 |

</details>

---

### Object: `Conditional_ActiveWeather_Any`
### Object: `Conditional_ActiveWeather_Any`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `Conditional_Backstab`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `BonusCritChance` | `Number` | Applies or references the 'BonusCritChance' effect/state. | 0 |

</details>

---

### Object: `Conditional_CanBeHealed`
### Object: `Conditional_CanBeHealed`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `RandomStatusFromPool` | Object | Selects and applies a random status effect from the provided nested object. | 0 |

</details>

---

### Object: `Conditional_DebuffRoll`
### Object: `Conditional_DebuffRoll`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `odds` | Number | The probability (0.0 to 1.0) of applying the debuff. | 1 |
  | `DestroyEquipmentAndAttachParasite` | Object | Removes an equipped item and replaces it with a parasite from a specified pool. | 0 |

</details>

---

### Object: `Conditional_FinishedSpawning`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `Imprison` | `Enum/String` | Applies or references the 'Imprison' effect/state. | 0 |

</details>

---

### Object: `Conditional_HasCleansableDebuffs`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `BonusDamage` | String | Applies or references the 'BonusDamage' effect/state. | 0 |
| `FormChange` | Block | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `GenericBuff` | `Number` | Applies or references the 'GenericBuff' effect/state. | 0 |
| `ManaGain` | String | Applies or references the 'ManaGain' effect/state. | 0 |
| `RandomStatDown` | Number | Applies or references the 'RandomStatDown' effect/state. | 0 |
| `RandomStatusFromPool` | `Block` | Selects and applies a random status effect from the provided nested block. | 0 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 0 |
| `RefreshMovePoints` | Number | Applies or references the 'RefreshMovePoints' effect/state. | 0 |

</details>

---

### Object: `Conditional_IsTrample`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `SetKnockback` | `Number` | Applies or references the 'SetKnockback' effect/state. | 0 |

</details>

---

### Object: `Conditional_LivingPlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
  | [`Else`](#else) | Object | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 0 |
  | [`ApplyToSource`](#applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 0 |
  | [`Consumed`](#consumed) | Object | State block triggered when this object or entity is eaten/consumed by another character. | 0 |
  | `GenericDebuff` | Integer | Applies or references the 'GenericDebuff' effect/state. | 0 |
| `AddLeechesStatus` | Number | Applies or references the 'AddLeechesStatus' effect/state. | 0 |
| `AddWeaponAux` | String | Applies or references the 'AddWeaponAux' effect/state. | 0 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 0 |
| `Craft` | Block | Synthesizes or spawns a new item from a specific pool. | 0 |
| `DisableWeapon` | Number | Applies or references the 'DisableWeapon' effect/state. | 0 |
| `DoDamage` | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 0 |
| `EvolveAbilityFromPool` | Enum/String | Upgrades or transforms an existing ability into a new one from the specified pool. | 0 |
| `FormChange` | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 0 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 0 |
| `KnockUpAndAway` | Block | Displaces the target vertically and horizontally away from the source. | 0 |
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 0 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 0 |
| `RefreshMovePoints` | Number | Applies or references the 'RefreshMovePoints' effect/state. | 0 |
| `RemoveStatus` | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 0 |
| `SpecificInjury` | Enum/String | Applies or references the 'SpecificInjury' effect/state. | 0 |
| `StanceSwitchToMelee` | Number | Applies or references the 'StanceSwitchToMelee' effect/state. | 0 |
| `StanceSwitchToRanged` | Number | Applies or references the 'StanceSwitchToRanged' effect/state. | 0 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
| `TempPassiveWhileHasStatus` | `Block` | Grants nested passives only while the character possesses the specified status. | 0 |
| `TempTrampleUntilSettled` | Number | Applies or references the 'TempTrampleUntilSettled' effect/state. | 0 |
| `do_not_pop_corpse` | Boolean |  | 0 |
| `drop_body_ability` | Enum/String |  | 0 |
| `drop_on_death` | Enum/String |  | 0 |
| `drop_on_self_death` | Boolean |  | 0 |
| `extra_statuses` | Block | Additional generic status applications. | 0 |
| `force_contact` | Boolean | If true, enforces physical overlap. | 0 |
| `instant` | Boolean |  | 0 |
| `kill_on_consume` | Boolean |  | 0 |
| `mount_mode` | Enum/String | If true, treats the consumption as riding/mounting instead of eating. | 0 |
| `status` | Enum/String | The required status effect. | 0 |
| `struggle_ability` | Enum/String | Ability triggered by the consumed entity while inside the consumer. | 0 |
| `use_placeholder` | Boolean |  | 0 |
| `wet` | Boolean |  | 0 |

</details>

---

### Object: `Conditional_NotBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `DisplaceTowardsSource` | `Number` | Applies or references the 'DisplaceTowardsSource' effect/state. | 0 |

</details>

---

### Object: `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| `odds` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| `ApplyPassives` | `Block` | Grants the nested passive abilities dynamically. | 0 |

</details>

---

### Object: `Conditional_SourceAbilityHasTag`
### Object: `Conditional_SourceAbilityHasTag`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 1 |

</details>

---

### Object: `Conditional_SourceHasStatus`
### Object: `Conditional_SourceHasStatus`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |
  | `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 0 |

</details>

---

### Object: `DelayCastAbility`
### Object: `DelayCastAbility`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to cast later. | 1 |
| `lingering` | Boolean |  | 1 |
| `relative` | Boolean |  | 1 |

</details>

---

### Object: `DelayedWindCone`
### Object: `DelayedWindCone`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| `distance` | Number | Distance or area of effect in tiles. | 1 |

</details>

---

### Object: `DybbukPossessed`
### Object: `DybbukPossessed`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum |  | 1 |
| [`punch_self_ability`](./Enums.md#enum-punch_self_ability) | Enum |  | 1 |

</details>

---

### Object: `ForceImmediateMoveAndAttack`
### Object: `ForceImmediateMoveAndAttack`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_InForm`](./Abilities_and_Spells.md#object-conditional_inform)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ability to execute after moving. | 1 |
| `even_if_cant_reach` | Boolean | If true, executes the attack even if the move fails to reach the target. | 1 |

</details>

---

### Object: `IncAuxCounterCycle`
### Object: `IncAuxCounterCycle`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `change` | Number |  | 1 |
| `max` | Number |  | 1 |

</details>

---

### Object: `Madness`
### Object: `Madness`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |
| `tickdown_this_turn` | Boolean |  | 1 |

</details>

---

### Object: `MergeDamageInstance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `force_no_hit_animation` | Boolean | If true, suppresses the flinch/hit animation. | 1 |
| `can_instapop` | `Boolean` | If false, prevents the damage from instantly popping the target. | 0 |

</details>

---

### Object: `NextBasicAttackCritsThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |
| `cant_miss` | `Boolean` | If true, ensures the attack cannot be dodged. | 0 |
| `piercing` | `Boolean` | If true, the attack ignores armor. | 0 |

</details>

---

### Object: `NextBattleStatusStacks`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `fights` | Number | The number of encounters this buff/debuff persists for. | 1 |
| `MadnessChanceOnTurnBegin` | `Number` | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. | 0 |

</details>

---

### Object: `PassiveWhileNotTakingTurn`
### Object: `PassiveWhileNotTakingTurn`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`AddStatusToBasicAttack`](#addstatustobasicattack) | Object | Injects a status effect payload that applies whenever the character performs a basic attack. | 0 |

</details>

---

### Object: `PoolMetronome`
### Object: `PoolMetronome`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | An array of ability IDs to randomly choose from. | 1 |

</details>

---

### Object: `PopAndSpawn`
### Object: `PopAndSpawn`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID to spawn in place. | 2 |
| `clone_items` | Boolean | If true, transfers inventory to the new entity. | 1 |
| `clone_referenced_catdata` | Boolean | If true, copies the genetic data of the popped cat. | 1 |
| `no_splatter` | Boolean |  | 1 |

</details>

---

### Object: `RemoveStatusStacks`
### Object: `RemoveStatusStacks`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 1 |
| `stacks` | Number | The number of stacks to remove. | 1 |

</details>

---

### Object: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |
  | [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. | 0 |
| `effects` | `Block` | Non-damaging status applications and logic triggers executed on impact. | 0 |

</details>

---

### Object: `ScrambleLastUsedSpell`
### Object: `ScrambleLastUsedSpell`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `permanent` | Boolean | If true, the scramble persists for the rest of the run. | 1 |

</details>

---

### Object: `SetAnimationAlts`
### Object: `SetAnimationAlts`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dead`](./Enums.md#enum-dead) | Enum |  | 1 |
| [`dying`](./Enums.md#enum-dying) | Enum |  | 1 |

</details>

---

### Object: `ShowFakeDamage`
### Object: `ShowFakeDamage`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`style`](./Arrays.md#array-style) | Array | The visual font style for the text (e.g., [crit]). | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Object: `SpreadDisease`
### Object: `SpreadDisease`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`disease`](./Enums.md#enum-disease) | Enum | The specific status effect ID representing the disease. | 1 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of transmitting. | 1 |

</details>

---

### Object: `StatusGroup`
### Object: `StatusGroup`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `StatusKillers`
### Object: `StatusKillers`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Conditional_Boss`](#conditionalboss) | Object | Conditional trigger: Executes nested logic if the target is a Boss. | 0 |
  | [`Conditional_NotBoss`](#conditionalnotboss) | Object | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 0 |
  | [`Confusion`](./Arrays.md#array-confusion) | Number | Applies or references the 'Confusion' effect/state. | 0 |

</details>

---

### Object: `SwapWeapon`
### Object: `SwapWeapon`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | An array of weapon item IDs to draw from. | 1 |

</details>

---

### Object: `TransformEquipment`
### Object: `TransformEquipment`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | The original item ID. | 1 |
| [`to`](./Enums.md#enum-to) | Enum | The new item ID. | 1 |

</details>

---

### Object: `TransformWeapon`
### Object: `TransformWeapon`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#object-applytosourceonkill)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | The original weapon ID. | 1 |
| [`to`](./Enums.md#enum-to) | Enum | The transformed weapon ID. | 1 |

</details>

---

### Object: `UseAbility`
### Object: `UseAbility`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger. | 1 |
| `respect_prime` | Boolean | If true, respects the ability's prime/cooldown state. | 1 |

</details>

---

### Object: `UseMoveAbilityWithAI`
### Object: `UseMoveAbilityWithAI`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | The AI positioning logic profile to use. | 1 |

</details>

---

### Object: `VisualCountDownThenApplyStatus`
### Object: `VisualCountDownThenApplyStatus`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `WaggleClone`
### Object: `WaggleClone`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cWaggle2x2` | Flag |  | 1 |
| `cWaggle3x3` | Flag |  | 1 |
| `cWaggle` | Flag |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Object: `bonk_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `damage` | Number | The base damage properties of an attack. | 1 |
| `effects` | `Block` | Non-damaging status applications and logic triggers executed on impact. | 0 |

</details>

---

### Object: `damage`
### Object: `damage`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 1 |
| `damage` | Number | The base damage properties of an attack. | 1 |

</details>

---

### Object: `damage_threshold_altanimations`
### Object: `damage_threshold_altanimations`
<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#object-graphics)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `heaviestMelee` | Number | Animation trigger for massive damage. | 1 |
| `heavyMelee` | Number | Animation trigger if damage exceeds this threshold. | 1 |

</details>

---

