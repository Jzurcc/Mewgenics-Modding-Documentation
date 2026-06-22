# Mewgenics Mod Developer Documentation: Engine: Graphics Block

> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Engine: Graphics Block

This document defines the `graphics {}` schema. This block configures all visual and animation properties for an ability, character, or class. It is shared across Abilities & Spells, Characters & Bosses, and Cat Classes.

### Known Explicit Parameters

These are hardcoded configuration keys found within these blocks (not dynamic IDs).

<details>
<summary><b>Expand</b></summary>

| Parameter | Type | Notes |
| :--- | :--- | :--- |
| `affected_animation` | Enum | Visuals applied to the target receiving the effect. |
| `affected_particle` | Enum | Visuals applied to the target receiving the effect. |
| `air_animation` | Enum | Animation played while entity is airborne. |
| `ally_animation` | Enum | Distinct animation used when targeting a friendly unit. |
| `alt_animations` | Array |  |
| `always_huge_mask` | Boolean |  |
| `always_play_animations` | Boolean | Bypasses speed-up/skip logic. |
| `animate_name` | String | Animates the ability name text on cast. |
| `animation` | Enum | The primary flash animation label triggered. |
| `animation_in` | Enum | Used for transition states (like burrowing). |
| `animation_out` | Enum | Used for transition states (like burrowing). |
| `aoe_spell_on_land` | Boolean | Visual trigger when a jump lands. |
| `apex_distance` | Number | Calculations for the peak of a jump/lob arc. |
| `apex_time` | Enum | Calculations for the peak of a jump/lob arc. |
| `area_particle` | Enum | Specific spawn points for particles. |
| `art_flip` | Number |  |
| `beam_cap` | Enum | Flash movieclips used to render continuous laser beams. |
| `beam_clip` | Enum | Flash movieclips used to render continuous laser beams. |
| `bounce_on_hit` | Boolean | Visual hop when striking a target. |
| `bypass_combatspeed` | Boolean |  |
| `center_particle` | Enum | Specific spawn points for particles. |
| `chain_distance` | Enum | Creates a tethered repeating graphic (like a hook). |
| `chain_movieclip` | Enum | Creates a tethered repeating graphic (like a hook). |
| `custom_cat_data` | Enum |  |
| `custom_priming_animation` | Enum | Animation used while charging an ability. |
| `damage_threshold_altanimations` | Block | Triggers different hit animations based on the amount of damage dealt. |
| `darken_screen` | Boolean | Dims the background during the ability cast. |
| `darken_screen_exclude_characters_on_tile` | Boolean |  |
| `darken_screen_exclude_self` | Boolean |  |
| `darken_screen_start_early` | Boolean |  |
| `dash_animation` | Enum | State-specific animations for trample/dash abilities. |
| `dash_attack_animation` | Enum |  |
| `dash_bonk_animation` | Enum |  |
| `dash_decelerating_animation` | Enum |  |
| `dash_end_animation` | Enum |  |
| `dash_start_animation` | Enum |  |
| `dead` | Enum |  |
| `deadhit` | Enum |  |
| `decelerate` | Number | Visual slowdown at the end of a movement. |
| `default_attack_animation` | Enum |  |
| `default_face` | Enum |  |
| `delay` | Number | Frame delay before firing projectile/effect. |
| `delay_from_map_center` | Boolean | Positional based timing delays. |
| `delay_from_map_edge` | Boolean | Delays effect based on distance from the screen edge. |
| `delay_from_reverse_map_edge` | Boolean |  |
| `depth_offset` | Enum |  |
| `desc` | String | Localization key for the character's desc. |
| `detatched_animation` | Enum | Plays an animation separated from the character body. |
| `detatched_animation_cutoff` | Boolean |  |
| `detatched_animation_reach` | Number |  |
| `do_animation_offscreen` | Boolean |  |
| `do_damage_immediately` | Boolean | Applies math before the animation actually hits. |
| `do_not_clear_placeholder` | Boolean |  |
| `dodge` | Enum |  |
| `dont_orient` | Boolean | Prevents the character from turning to face the target. |
| `dont_sink` | Boolean |  |
| `dont_visualize_ai` | Boolean |  |
| `dying` | Enum |  |
| `easing` | Number | Smoothing function for movement animations. |
| `empty_animation` | Enum |  |
| `end` | Enum | Segments for continuous channeled animations. |
| `face_targets` | Boolean | Forces the sprite to look at the target tile. |
| `face_toss_target` | Boolean |  |
| `fall_from_sky` | Boolean | Spawns the projectile from the top of the screen. |
| `fall_randomize_timing` | Enum |  |
| `first_castpoint_is_self_damage_only` | Boolean |  |
| `fixed_jump_height` | Number |  |
| `fixed_jump_speed` | Number |  |
| `four_way_animations` | Boolean |  |
| `full_jump_animation` | Enum |  |
| `full_jump_sync_frames` | Number |  |
| `full_jump_windup_frames` | Number |  |
| `fx_is_placeholder_animation` | Boolean |  |
| `fx_random_flip` | Boolean |  |
| `grab_animation` | Enum |  |
| `hang_time` | Enum |  |
| `hit` | Enum |  |
| `hud_palette` | Number |  |
| `ignore_slowtiles` | Boolean |  |
| `jump_attack_animation` | Enum | Overrides for jump physics. |
| `jump_height_multiplier` | Enum | Overrides for jump physics. |
| `jump_speed_multiplier` | Number |  |
| `jump_start_animation` | Enum |  |
| `land_animation` | Enum |  |
| `lob` | Boolean |  |
| `lob_height` | Number | Adjustments for arcing projectiles. |
| `lob_speed` | Enum | Adjustments for arcing projectiles. |
| `lob_yoff` | Enum | Adjustments for arcing projectiles. |
| `lock_orientation_during_dash` | Boolean | Prevents the sprite from flipping mid-dash. |
| `loop` | Enum | Segments for continuous channeled animations. |
| `mask_center` | Enum |  |
| `mask_extent` | Enum |  |
| `max_range` | Number | The maximum and minimum distance required to cast. |
| `max_throw_height` | Number |  |
| `max_tiles_single_loop` | Number |  |
| `min_range` | Number | The maximum and minimum distance required to cast. |
| `min_throw_height` | Number |  |
| `miss_particle` | Enum | Specific spawn points for particles. |
| `miss_random_delay` | Array |  |
| `mode` | Enum |  |
| `move_end_animation` | Enum |  |
| `move_speed_multiplier` | Enum |  |
| `move_speed_sync_frames` | Number |  |
| `move_start_animation` | Enum |  |
| `movieclip` | Enum |  |
| `name` | String | Localization key for the character's name. |
| `no_horizontal_flip` | Boolean |  |
| `no_splatter` | Boolean |  |
| `non_blocking_animations` | Array |  |
| `othercat_placeholder_available` | Boolean |  |
| `override_portrait` | Enum |  |
| `palette` | Number | Swaps the color palette ID. |
| `particle` | Enum | References an impact or cast particle effect. |
| `particle_mat` | Enum |  |
| `piece_alt_frame` | Number |  |
| `portrait_face` | Enum |  |
| `precast_delay` | Enum |  |
| `preturn_animation` | Enum |  |
| `prime_animation` | Enum |  |
| `primed_alt_animation` | String |  |
| `projectile` | Enum | References a projectile entity. |
| `projectile_spawn_offset` | Array |  |
| `pseudoprojectile` | Enum |  |
| `random_delay` | Array | Adds chaotic timing to multi-projectile casts. |
| `randomize_starting_frame` | Boolean |  |
| `reverse_orientation` | Boolean |  |
| `rocket_swirl` | Block | Visual parameters for swirling projectile paths. |
| `scale` | Enum |  |
| `self_damage_mid_port` | Boolean |  |
| `shade_occluded_objects` | Boolean |  |
| `shadow` | Enum |  |
| `shadow_size` | Number |  |
| `show_infinity_damage_warning` | Boolean |  |
| `single_projectile` | Boolean |  |
| `spawn_offset` | Array |  |
| `spawnin_animation` | String |  |
| `speed` | Number | Rotations per second. |
| `start` | Enum | Segments for continuous channeled animations. |
| `status_display_count_max` | Number |  |
| `stunned` | Enum |  |
| `sync_frames` | Number |  |
| `sync_speed` | Number |  |
| `throw_speed` | Number |  |
| `tint` | Array |  |
| `tooltip` | String |  |
| `uifloaters_offset` | Number |  |
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
| `visual_delay_but_simultaneous_damage` | Number |  |
| `walk` | Enum |  |
| `water_mask` | Enum |  |
| `weak` | Enum |  |

</details>

