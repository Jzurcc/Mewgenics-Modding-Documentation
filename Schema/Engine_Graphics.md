# Mewgenics Mod Developer Documentation: Engine: Graphics Block

## Engine: Graphics Block

This document defines the `graphics {}` schema. This block configures all visual and animation properties for an ability, character, or class. It is shared across Abilities & Spells, Characters & Bosses, and Cat Classes.

> **Referenced by:** [`graphics` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-graphics), [`graphics` (Cat_Classes)](./Cat_Classes.md#context-graphics), [`graphics` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-graphics)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`affected_animation`](./Enums.md#enum-affected_animation) | Enum | Visuals applied to the target receiving the effect. |
| [`affected_particle`](./Enums.md#enum-affected_particle) | Enum | Visuals applied to the target receiving the effect. |
| [`air_animation`](./Enums.md#enum-air_animation) | Enum | Animation played while entity is airborne. |
| [`ally_animation`](./Enums.md#enum-ally_animation) | Enum | Distinct animation used when targeting a friendly unit. |
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array |  |
| `always_huge_mask` | Boolean |  |
| `always_play_animations` | Boolean | Bypasses speed-up/skip logic. |
| `animate_name` | String | Animates the ability name text on cast. |
| [`animation`](./Enums.md#enum-animation) | Enum | The primary flash animation label triggered. |
| [`animation_in`](./Enums.md#enum-animation_in) | Enum | Used for transition states (like burrowing). |
| [`animation_out`](./Enums.md#enum-animation_out) | Enum | Used for transition states (like burrowing). |
| `aoe_spell_on_land` | Boolean | Visual trigger when a jump lands. |
| `apex_distance` | Float | Calculations for the peak of a jump/lob arc. |
| `apex_time` | Float | Calculations for the peak of a jump/lob arc. |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum | Specific spawn points for particles. |
| `art_flip` | Integer |  |
| [`beam_cap`](./Enums.md#enum-beam_cap) | Enum | Flash movieclips used to render continuous laser beams. |
| [`beam_clip`](./Enums.md#enum-beam_clip) | Enum | Flash movieclips used to render continuous laser beams. |
| `bounce_on_hit` | Boolean | Visual hop when striking a target. |
| `bypass_combatspeed` | Boolean |  |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum | Specific spawn points for particles. |
| `chain_distance` | Float | Creates a tethered repeating graphic (like a hook). |
| [`chain_movieclip`](./Enums.md#enum-chain_movieclip) | Enum | Creates a tethered repeating graphic (like a hook). |
| [`custom_cat_data`](./Enums.md#enum-custom_cat_data) | Enum |  |
| [`custom_priming_animation`](./Enums.md#enum-custom_priming_animation) | Enum | Animation used while charging an ability. |
| [`damage_threshold_altanimations`](#damage_threshold_altanimations) | Block | Triggers different hit animations based on the amount of damage dealt. |
| `darken_screen` | Boolean | Dims the background during the ability cast. |
| `darken_screen_exclude_characters_on_tile` | Boolean |  |
| `darken_screen_exclude_self` | Boolean |  |
| `darken_screen_start_early` | Boolean |  |
| [`dash_animation`](./Enums.md#enum-dash_animation) | Enum | State-specific animations for trample/dash abilities. |
| [`dash_attack_animation`](./Enums.md#enum-dash_attack_animation) | Enum |  |
| [`dash_bonk_animation`](./Enums.md#enum-dash_bonk_animation) | Enum |  |
| [`dash_decelerating_animation`](./Enums.md#enum-dash_decelerating_animation) | Enum |  |
| [`dash_end_animation`](./Enums.md#enum-dash_end_animation) | Enum |  |
| [`dash_start_animation`](./Enums.md#enum-dash_start_animation) | Enum |  |
| [`dead`](./Enums.md#enum-dead) | Enum |  |
| [`deadhit`](./Enums.md#enum-deadhit) | Enum |  |
| `decelerate` | Integer | Visual slowdown at the end of a movement. |
| [`default_attack_animation`](./Enums.md#enum-default_attack_animation) | Enum |  |
| [`default_face`](./Enums.md#enum-default_face) | Enum |  |
| `delay` | Float | Frame delay before firing projectile/effect. |
| `delay_from_map_center` | Boolean | Positional based timing delays. |
| `delay_from_map_edge` | Boolean | Delays effect based on distance from the screen edge. |
| `delay_from_reverse_map_edge` | Boolean |  |
| `depth_offset` | Float |  |
| `desc` | String | Localization key for the character's desc. |
| [`detatched_animation`](./Enums.md#enum-detatched_animation) | Enum | Plays an animation separated from the character body. |
| `detatched_animation_cutoff` | Boolean |  |
| `detatched_animation_reach` | Integer |  |
| `do_animation_offscreen` | Boolean |  |
| `do_damage_immediately` | Boolean | Applies math before the animation actually hits. |
| `do_not_clear_placeholder` | Boolean |  |
| [`dodge`](./Enums.md#enum-dodge) | Enum |  |
| `dont_orient` | Boolean | Prevents the character from turning to face the target. |
| `dont_sink` | Boolean |  |
| `dont_visualize_ai` | Boolean |  |
| [`dying`](./Enums.md#enum-dying) | Enum |  |
| `easing` | Integer | Smoothing function for movement animations. |
| [`empty_animation`](./Enums.md#enum-empty_animation) | Enum |  |
| [`end`](./Enums.md#enum-end) | Enum | Segments for continuous channeled animations. |
| `face_targets` | Boolean | Forces the sprite to look at the target tile. |
| `face_toss_target` | Boolean |  |
| `fall_from_sky` | Boolean | Spawns the projectile from the top of the screen. |
| `fall_randomize_timing` | Float |  |
| `first_castpoint_is_self_damage_only` | Boolean |  |
| `fixed_jump_height` | Float |  |
| `fixed_jump_speed` | Float |  |
| `four_way_animations` | Boolean |  |
| [`full_jump_animation`](./Enums.md#enum-full_jump_animation) | Enum |  |
| `full_jump_sync_frames` | Integer |  |
| `full_jump_windup_frames` | Integer |  |
| `fx_is_placeholder_animation` | Boolean |  |
| `fx_random_flip` | Boolean |  |
| [`grab_animation`](./Enums.md#enum-grab_animation) | Enum |  |
| `hang_time` | Float |  |
| [`hit`](./Enums.md#enum-hit) | Enum |  |
| `hud_palette` | Integer |  |
| `ignore_slowtiles` | Boolean |  |
| [`jump_attack_animation`](./Enums.md#enum-jump_attack_animation) | Enum | Overrides for jump physics. |
| `jump_height_multiplier` | Float | Overrides for jump physics. |
| `jump_speed_multiplier` | Float |  |
| [`jump_start_animation`](./Enums.md#enum-jump_start_animation) | Enum |  |
| [`land_animation`](./Enums.md#enum-land_animation) | Enum |  |
| `lob` | Boolean |  |
| `lob_height` | Integer | Adjustments for arcing projectiles. |
| `lob_speed` | Float | Adjustments for arcing projectiles. |
| `lob_yoff` | Float | Adjustments for arcing projectiles. |
| `lock_orientation_during_dash` | Boolean | Prevents the sprite from flipping mid-dash. |
| [`loop`](./Enums.md#enum-loop) | Enum | Segments for continuous channeled animations. |
| [`mask_center`](./Enums.md#enum-mask_center) | Enum |  |
| [`mask_extent`](./Enums.md#enum-mask_extent) | Enum |  |
| `max_range` | Integer | The maximum and minimum distance required to cast. |
| `max_throw_height` | Float |  |
| `max_tiles_single_loop` | Integer |  |
| `min_range` | Integer | The maximum and minimum distance required to cast. |
| `min_throw_height` | Float |  |
| [`miss_particle`](./Enums.md#enum-miss_particle) | Enum | Specific spawn points for particles. |
| [`miss_random_delay`](./Arrays.md#array-miss_random_delay) | Array |  |
| [`mode`](./Enums.md#enum-mode) | Enum |  |
| [`move_end_animation`](./Enums.md#enum-move_end_animation) | Enum |  |
| `move_speed_multiplier` | Float |  |
| `move_speed_sync_frames` | Float |  |
| [`move_start_animation`](./Enums.md#enum-move_start_animation) | Enum |  |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  |
| `name` | String | Localization key for the character's name. |
| `no_horizontal_flip` | Boolean |  |
| `no_splatter` | Boolean |  |
| [`non_blocking_animations`](./Arrays.md#array-non_blocking_animations) | Array |  |
| `othercat_placeholder_available` | Boolean |  |
| [`override_portrait`](./Enums.md#enum-override_portrait) | Enum |  |
| `palette` | Integer | Swaps the color palette ID. |
| [`particle`](./Enums.md#enum-particle) | Enum | References an impact or cast particle effect. |
| [`particle_mat`](./Enums.md#enum-particle_mat) | Enum |  |
| `piece_alt_frame` | Integer |  |
| [`portrait_face`](./Enums.md#enum-portrait_face) | Enum |  |
| `precast_delay` | Float |  |
| [`preturn_animation`](./Enums.md#enum-preturn_animation) | Enum |  |
| [`prime_animation`](./Enums.md#enum-prime_animation) | Enum |  |
| `primed_alt_animation` | String |  |
| [`projectile`](./Enums.md#enum-projectile) | Enum | References a projectile entity. |
| [`projectile_spawn_offset`](./Arrays.md#array-projectile_spawn_offset) | Array |  |
| [`pseudoprojectile`](./Enums.md#enum-pseudoprojectile) | Enum |  |
| [`random_delay`](./Arrays.md#array-random_delay) | Array | Adds chaotic timing to multi-projectile casts. |
| `randomize_starting_frame` | Boolean |  |
| `reverse_orientation` | Boolean |  |
| [`rocket_swirl`](#rocket_swirl) | Block | Visual parameters for swirling projectile paths. |
| `scale` | Float |  |
| `self_damage_mid_port` | Boolean |  |
| `shade_occluded_objects` | Boolean |  |
| [`shadow`](./Enums.md#enum-shadow) | Enum |  |
| `shadow_size` | Float |  |
| `show_infinity_damage_warning` | Boolean |  |
| `single_projectile` | Boolean |  |
| [`spawn_offset`](./Arrays.md#array-spawn_offset) | Array |  |
| `spawnin_animation` | String |  |
| `speed` | Float | Rotations per second. |
| [`start`](./Enums.md#enum-start) | Enum | Segments for continuous channeled animations. |
| `status_display_count_max` | Integer |  |
| [`stunned`](./Enums.md#enum-stunned) | Enum |  |
| `sync_frames` | Integer |  |
| `sync_speed` | Integer |  |
| `throw_speed` | Integer |  |
| [`tint`](./Arrays.md#array-tint) | Array |  |
| `tooltip` | String |  |
| `uifloaters_offset` | Float |  |
| `uncatchable` | Boolean |  |
| `use_directional_animations` | Boolean |  |
| `use_hit_alts` | Boolean |  |
| `use_origin_offsets` | Boolean |  |
| `use_placeholder` | Boolean |  |
| `use_projectile` | Boolean |  |
| `use_projectile_spawn_offset` | Boolean |  |
| `use_rotation` | Boolean |  |
| `use_rotation_once` | Boolean |  |
| `use_super_armor` | Boolean | Prevents flinch animations from interrupting this cast. |
| `visual_delay_but_simultaneous_damage` | Integer |  |
| [`walk`](./Enums.md#enum-walk) | Enum |  |
| [`water_mask`](./Enums.md#enum-water_mask) | Enum |  |
| [`weak`](./Enums.md#enum-weak) | Enum |  |

</details>

### Valid Nested Blocks

The following blocks all behave as `[graphic_block]` containers. Each has its own unique parameters listed below its entry.

---

#### `graphics`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[graphic_block]`](./Engine_Graphics.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`affected_animation`](./Enums.md#enum-affected_animation) | Enum | Visuals applied to the target receiving the effect. |
| [`affected_particle`](./Enums.md#enum-affected_particle) | Enum | Visuals applied to the target receiving the effect. |
| [`air_animation`](./Enums.md#enum-air_animation) | Enum | Animation played while entity is airborne. |
| [`ally_animation`](./Enums.md#enum-ally_animation) | Enum | Distinct animation used when targeting a friendly unit. |
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array |  |
| `always_huge_mask` | Boolean |  |
| `always_play_animations` | Boolean | Bypasses speed-up/skip logic. |
| `animate_name` | String | Animates the ability name text on cast. |
| [`animation`](./Enums.md#enum-animation) | Enum | The primary flash animation label triggered. |
| [`animation_in`](./Enums.md#enum-animation_in) | Enum | Used for transition states (like burrowing). |
| [`animation_out`](./Enums.md#enum-animation_out) | Enum | Used for transition states (like burrowing). |
| `aoe_spell_on_land` | Boolean | Visual trigger when a jump lands. |
| `apex_distance` | Float | Calculations for the peak of a jump/lob arc. |
| `apex_time` | Float | Calculations for the peak of a jump/lob arc. |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum | Specific spawn points for particles. |
| `art_flip` | Integer |  |
| [`beam_cap`](./Enums.md#enum-beam_cap) | Enum | Flash movieclips used to render continuous laser beams. |
| [`beam_clip`](./Enums.md#enum-beam_clip) | Enum | Flash movieclips used to render continuous laser beams. |
| `bounce_on_hit` | Boolean | Visual hop when striking a target. |
| `bypass_combatspeed` | Boolean |  |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum | Specific spawn points for particles. |
| `chain_distance` | Float | Creates a tethered repeating graphic (like a hook). |
| [`chain_movieclip`](./Enums.md#enum-chain_movieclip) | Enum | Creates a tethered repeating graphic (like a hook). |
| [`custom_cat_data`](./Enums.md#enum-custom_cat_data) | Enum |  |
| [`custom_priming_animation`](./Enums.md#enum-custom_priming_animation) | Enum | Animation used while charging an ability. |
| [`damage_threshold_altanimations`](#damage_threshold_altanimations) | Block | Triggers different hit animations based on the amount of damage dealt. |
| `darken_screen` | Boolean | Dims the background during the ability cast. |
| `darken_screen_exclude_characters_on_tile` | Boolean |  |
| `darken_screen_exclude_self` | Boolean |  |
| `darken_screen_start_early` | Boolean |  |
| [`dash_animation`](./Enums.md#enum-dash_animation) | Enum | State-specific animations for trample/dash abilities. |
| [`dash_attack_animation`](./Enums.md#enum-dash_attack_animation) | Enum |  |
| [`dash_bonk_animation`](./Enums.md#enum-dash_bonk_animation) | Enum |  |
| [`dash_decelerating_animation`](./Enums.md#enum-dash_decelerating_animation) | Enum |  |
| [`dash_end_animation`](./Enums.md#enum-dash_end_animation) | Enum |  |
| [`dash_start_animation`](./Enums.md#enum-dash_start_animation) | Enum |  |
| [`dead`](./Enums.md#enum-dead) | Enum |  |
| [`deadhit`](./Enums.md#enum-deadhit) | Enum |  |
| `decelerate` | Integer | Visual slowdown at the end of a movement. |
| [`default_attack_animation`](./Enums.md#enum-default_attack_animation) | Enum |  |
| [`default_face`](./Enums.md#enum-default_face) | Enum |  |
| `delay` | Float | Frame delay before firing projectile/effect. |
| `delay_from_map_center` | Boolean | Positional based timing delays. |
| `delay_from_map_edge` | Boolean | Delays effect based on distance from the screen edge. |
| `delay_from_reverse_map_edge` | Boolean |  |
| `depth_offset` | Float |  |
| `desc` | String | Localization key for the character's desc. |
| [`detatched_animation`](./Enums.md#enum-detatched_animation) | Enum | Plays an animation separated from the character body. |
| `detatched_animation_cutoff` | Boolean |  |
| `detatched_animation_reach` | Integer |  |
| `do_animation_offscreen` | Boolean |  |
| `do_damage_immediately` | Boolean | Applies math before the animation actually hits. |
| `do_not_clear_placeholder` | Boolean |  |
| [`dodge`](./Enums.md#enum-dodge) | Enum |  |
| `dont_orient` | Boolean | Prevents the character from turning to face the target. |
| `dont_sink` | Boolean |  |
| `dont_visualize_ai` | Boolean |  |
| [`dying`](./Enums.md#enum-dying) | Enum |  |
| `easing` | Integer | Smoothing function for movement animations. |
| [`empty_animation`](./Enums.md#enum-empty_animation) | Enum |  |
| [`end`](./Enums.md#enum-end) | Enum | Segments for continuous channeled animations. |
| `face_targets` | Boolean | Forces the sprite to look at the target tile. |
| `face_toss_target` | Boolean |  |
| `fall_from_sky` | Boolean | Spawns the projectile from the top of the screen. |
| `fall_randomize_timing` | Float |  |
| `first_castpoint_is_self_damage_only` | Boolean |  |
| `fixed_jump_height` | Float |  |
| `fixed_jump_speed` | Float |  |
| `four_way_animations` | Boolean |  |
| [`full_jump_animation`](./Enums.md#enum-full_jump_animation) | Enum |  |
| `full_jump_sync_frames` | Integer |  |
| `full_jump_windup_frames` | Integer |  |
| `fx_is_placeholder_animation` | Boolean |  |
| `fx_random_flip` | Boolean |  |
| [`grab_animation`](./Enums.md#enum-grab_animation) | Enum |  |
| `hang_time` | Float |  |
| [`hit`](./Enums.md#enum-hit) | Enum |  |
| `hud_palette` | Integer |  |
| `ignore_slowtiles` | Boolean |  |
| [`jump_attack_animation`](./Enums.md#enum-jump_attack_animation) | Enum | Overrides for jump physics. |
| `jump_height_multiplier` | Float | Overrides for jump physics. |
| `jump_speed_multiplier` | Float |  |
| [`jump_start_animation`](./Enums.md#enum-jump_start_animation) | Enum |  |
| [`land_animation`](./Enums.md#enum-land_animation) | Enum |  |
| `lob` | Boolean |  |
| `lob_height` | Integer | Adjustments for arcing projectiles. |
| `lob_speed` | Float | Adjustments for arcing projectiles. |
| `lob_yoff` | Float | Adjustments for arcing projectiles. |
| `lock_orientation_during_dash` | Boolean | Prevents the sprite from flipping mid-dash. |
| [`loop`](./Enums.md#enum-loop) | Enum | Segments for continuous channeled animations. |
| [`mask_center`](./Enums.md#enum-mask_center) | Enum |  |
| [`mask_extent`](./Enums.md#enum-mask_extent) | Enum |  |
| `max_range` | Integer | The maximum and minimum distance required to cast. |
| `max_throw_height` | Float |  |
| `max_tiles_single_loop` | Integer |  |
| `min_range` | Integer | The maximum and minimum distance required to cast. |
| `min_throw_height` | Float |  |
| [`miss_particle`](./Enums.md#enum-miss_particle) | Enum | Specific spawn points for particles. |
| [`miss_random_delay`](./Arrays.md#array-miss_random_delay) | Array |  |
| [`mode`](./Enums.md#enum-mode) | Enum |  |
| [`move_end_animation`](./Enums.md#enum-move_end_animation) | Enum |  |
| `move_speed_multiplier` | Float |  |
| `move_speed_sync_frames` | Float |  |
| [`move_start_animation`](./Enums.md#enum-move_start_animation) | Enum |  |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  |
| `name` | String | Localization key for the character's name. |
| `no_horizontal_flip` | Boolean |  |
| `no_splatter` | Boolean |  |
| [`non_blocking_animations`](./Arrays.md#array-non_blocking_animations) | Array |  |
| `othercat_placeholder_available` | Boolean |  |
| [`override_portrait`](./Enums.md#enum-override_portrait) | Enum |  |
| `palette` | Integer | Swaps the color palette ID. |
| [`particle`](./Enums.md#enum-particle) | Enum | References an impact or cast particle effect. |
| [`particle_mat`](./Enums.md#enum-particle_mat) | Enum |  |
| `piece_alt_frame` | Integer |  |
| [`portrait_face`](./Enums.md#enum-portrait_face) | Enum |  |
| `precast_delay` | Float |  |
| [`preturn_animation`](./Enums.md#enum-preturn_animation) | Enum |  |
| [`prime_animation`](./Enums.md#enum-prime_animation) | Enum |  |
| `primed_alt_animation` | String |  |
| [`projectile`](./Enums.md#enum-projectile) | Enum | References a projectile entity. |
| [`projectile_spawn_offset`](./Arrays.md#array-projectile_spawn_offset) | Array |  |
| [`pseudoprojectile`](./Enums.md#enum-pseudoprojectile) | Enum |  |
| [`random_delay`](./Arrays.md#array-random_delay) | Array | Adds chaotic timing to multi-projectile casts. |
| `randomize_starting_frame` | Boolean |  |
| `reverse_orientation` | Boolean |  |
| [`rocket_swirl`](#rocket_swirl) | Block | Visual parameters for swirling projectile paths. |
| `scale` | Float |  |
| `self_damage_mid_port` | Boolean |  |
| `shade_occluded_objects` | Boolean |  |
| [`shadow`](./Enums.md#enum-shadow) | Enum |  |
| `shadow_size` | Float |  |
| `show_infinity_damage_warning` | Boolean |  |
| `single_projectile` | Boolean |  |
| [`spawn_offset`](./Arrays.md#array-spawn_offset) | Array |  |
| `spawnin_animation` | String |  |
| `speed` | Float | Rotations per second. |
| [`start`](./Enums.md#enum-start) | Enum | Segments for continuous channeled animations. |
| `status_display_count_max` | Integer |  |
| [`stunned`](./Enums.md#enum-stunned) | Enum |  |
| `sync_frames` | Integer |  |
| `sync_speed` | Integer |  |
| `throw_speed` | Integer |  |
| [`tint`](./Arrays.md#array-tint) | Array |  |
| `tooltip` | String |  |
| `uifloaters_offset` | Float |  |
| `uncatchable` | Boolean |  |
| `use_directional_animations` | Boolean |  |
| `use_hit_alts` | Boolean |  |
| `use_origin_offsets` | Boolean |  |
| `use_placeholder` | Boolean |  |
| `use_projectile` | Boolean |  |
| `use_projectile_spawn_offset` | Boolean |  |
| `use_rotation` | Boolean |  |
| `use_rotation_once` | Boolean |  |
| `use_super_armor` | Boolean | Prevents flinch animations from interrupting this cast. |
| `visual_delay_but_simultaneous_damage` | Integer |  |
| [`walk`](./Enums.md#enum-walk) | Enum |  |
| [`water_mask`](./Enums.md#enum-water_mask) | Enum |  |
| [`weak`](./Enums.md#enum-weak) | Enum |  |

</details>

