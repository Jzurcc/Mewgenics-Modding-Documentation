# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Abilities & Spells

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `template` | [`Enum/String`](./Enums.md#enum-template) | `spell, targeted_status, melee_attack` | Inherits baseline internal logic from a hardcoded engine template. |
| `variant_of` | [`Enum/String`](./Enums.md#enum-variant_of) | `Asteroid, BasicMelee, BasicJump` | Inherits properties from a previously defined ability (used for upgrading tiers). |
| `tags` | [`Array`](./Arrays.md#array-tags) | `[ musical ], [ weapon_throw ], [ summon ]` | Array of string categories used by the engine for filtering (e.g. [weapon_throw, spell]). |
| `class` | [`Enum/String`](./Enums.md#enum-class) | `PlaceholderMeleeAttackAbility, MultiHitMeleeAttackAbility, SuplexAbility` | Categorizes the ability for specific UI filters. |
| `ai_ability` | [`Enum/String`](./Enums.md#enum-ai_ability) | `SpawnBomb_AI, NubsJump_AI, Magnetize_AI` | Overrides the ability used when triggered by AI. |
| `chain_ability` | [`Enum/String`](./Enums.md#enum-chain_ability) | `Dump, ControlPlantsPartTwo, ControlPlantsPartTwo2` | An ability that automatically executes sequentially after this one. |
| `sub_ability` | [`Enum/String`](./Enums.md#enum-sub_ability) | `Huddle_Impl, Spin, TeamFlex_Impl` | A secondary ability component referenced by complex templates. |
| `cloned_ability` | [`Enum/String`](./Enums.md#enum-cloned_ability) | `attack` | Copies the properties of another ability dynamically. |
| `effects` | [`Block`](./Abilities_and_Spells.md#context-effects) | `{ ... }` | Non-damaging status applications and logic triggers executed on impact. |
| `damage` | [`Block`](./Abilities_and_Spells.md#context-damage) | `{ ... }` | The base damage properties of an attack. |

</details>

---

### Context: `target`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `max_range` | Number | `5, 1, 20` | The maximum and minimum distance required to cast. |
| `max_aoe` | Number | `1, 2, 0` | The maximum and minimum radius/length of the AoE. |
| `min_range` | Number | `2, 1, 3` | The maximum and minimum distance required to cast. |
| `target_mode` | [`Enum/String`](./Enums.md#enum-target_mode) | `direction8, random_tile, none` | How the cursor operates (`tile`, `direction`, `none`). |
| `restrictions` | [`Array`](./Arrays.md#array-restrictions) | `[ must_have_buddy must_have_living_character ], aoe_must_exist, none` | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). |
| `aoe_mode` | [`Enum/String`](./Enums.md#enum-aoe_mode) | `custom, standard, all` | The shape of the area (`standard`, `line`, `cross`, `square`, `custom`). |
| `knockback_mode` | [`Enum/String`](./Enums.md#enum-knockback_mode) | `tile_to_target, tile_to_character, zero` | How physics vectors apply (`character_to_tile`, `pull_to_character`, `zero`, `orientation`). |
| `min_aoe` | Number | `0, 1, 2+size` | The maximum and minimum radius/length of the AoE. |
| `aoe_excludes_self` | Boolean | `false, true` | Prevents the AoE from hitting the caster. |
| `aoe_restrictions` | [`Array`](./Arrays.md#array-aoe_restrictions) | `must_have_tag, [ exclude_blocking ], enemies_only` | Array of conditions the AoE tiles must meet (e.g., `must_have_line_of_sight_unpurgable`). |
| `aoe_considers_character_size` | Boolean | `false, true` | Scales the AoE based on the caster's tile size (e.g., 2x2). |
| `range_mode` | [`Enum/String`](./Enums.md#enum-range_mode) | `water_move, cross, standard` | How range is counted (`standard`, `ground_move`). |
| `X_is` | [`Enum/String`](./Enums.md#enum-x_is) | `current_health, turn_count, custom` | Applies or references the 'X_is' effect/state. |
| `custom_aoe` | [`Array`](./Arrays.md#array-custom_aoe) | `[ [ -1, 0 ], [ [ 1, 1 ], [ [ 1, -1 ]` | Array of exact coordinates for a custom shape (e.g., `[[1, -1] [1, 0]]`). |
| `multihit` | Number | `2, 5, 3` | Hardcoded number of times the ability hits the target. |
| `max_targets` | Number | `7, 1, 15` | Limits on how many distinct entities can be targeted. |
| `range_excludes_blocking` | Boolean | `false, true` | Cannot target through walls/obstacles. |
| `prioritize_dont_change_direction` | Number | `1, true` | AI preference to maintain current facing angle. |
| `target_requires_tag` | [`Enum/String`](./Enums.md#enum-target_requires_tag) | `pickup, bowling_ball, food` | Target must possess this exact character tag. |
| `aoe_symmetry` | [`Enum/String`](./Enums.md#enum-aoe_symmetry) | `eight_way, four_way, none` | Determines if the AoE mirrors on axes. |
| `prioritize_face_camera` | Number | `1, true` | AI preference to face South. |
| `straight_shot` | Boolean | `false, true` | Ensures projectiles do not arc. |
| `can_multihit` | Boolean | `false, true` | If true, overlapping AoEs can hit the same target multiple times. |
| `allow_any_orientation` | Boolean | `true` | Allows casting regardless of the character's facing direction. |
| `range_considers_character_size` | Boolean | `false` | Range calculation accounts for large entities. |
| `throw_consumed_character` | Boolean | `true` | Throws the entity currently held/eaten. |
| `min_targets` | Number | `2, 1, 5` | Limits on how many distinct entities can be targeted. |
| `aoe_leading_edge_only` | Boolean | `true` | Only the outermost edge of the AoE shape applies effects. |
| `allow_diagonals` | Boolean | `true` | Allows targeting on diagonal grid axes. |
| `range_display_include_character_size` | Boolean | `true` | Visual: offsets the range indicator for 2x2 units. |
| `stagger_multihit_targets` | Boolean | `true` | Delays hits slightly between multiple targets. |
| `upgrade_straight_shot_to_piercing` | Boolean | `true` | Allows the projectile to pass through multiple targets. |
| `delayed_trigger` | Boolean | `false, true` | Delays the actual execution of the target effect. |
| `consider_trample` | Boolean | `false, true` | AI consideration for moving through units. |
| `N` | Number | `2, 5, 3` | Variable modifier parameter. |
| `custom_range` | [`Array`](./Arrays.md#array-custom_range) | `[ [ 1, 1 ], [ [ 1 2 ], [ [ -2 0 ]` | Overrides standard range scaling. |
| `always_bounce` | Boolean | `true` | Forces the attack/projectile to bounce regardless of hit. |
| `custom_aoe_util` | [`Array`](./Arrays.md#array-custom_aoe_util) | `[ [ -1, 1 ], [ [ 0, 1 ], [ [ 1, 1 ]` | Utility variants of custom AoE definitions. |
| `multihit_max` | Number | `10, 5, 3` | Variable limits for random multihit abilities. |
| `multihit_min` | Number | `1, 5, 3` | Variable limits for random multihit abilities. |
| `reorient_thrown_character` | Boolean | `true` | Forces a thrown entity to face a certain way. |
| `toss_direction_restriction` | [`Enum/String`](./Enums.md#enum-toss_direction_restriction) | `backwards, forwards` | Limits which ways an entity can be tossed. |
| `aoe_hint_teamcast` | Boolean | `true` | Visual hint for cooperative casting abilities. |
| `aoe_tile_requires_element` | [`Enum/String`](./Enums.md#enum-aoe_tile_requires_element) | `Grass, Water, Earth` | Only affects tiles painted with a specific element. |
| `distance_sort_targets` | Number | `1, true` | Prioritizes targets based on proximity. |
| `dont_orient_aoe` | Boolean | `true` | Prevents the AoE shape from rotating with the character. |
| `hint_can_target_pickups` | Boolean | `true` | UI hint that the player can target items on the ground. |
| `max_bounces` | Number | `10, 3, -1` | Hard cap on how many times a bouncing effect can trigger. |
| `splash_damage_aoe_begin` | Number | `1, 999` | At what radius splash damage starts applying. |
| `aoe_chance` | [`Enum/String`](./Enums.md#enum-aoe_chance) | `.33, .5, .4+.2*level` | Percentage chance for the AoE to trigger. |
| `as_the_crow_flies` | Boolean | `true` | Calculates range ignoring all pathing terrain obstacles. |
| `force_ai_target_as_spell` | Boolean | `true` | Forces the AI to treat a physical move like a spell for targeting logic. |
| `mouse_offset` | [`Array`](./Arrays.md#array-mouse_offset) | `[ .5 .5 ]` | Visual offset for the targeting cursor. |
| `range_display_include_aoe` | Boolean | `true` | Visual: shows the full AoE potential when previewing range. |
| `shotgun_mode` | Boolean | `true` | Deals more damage/hits if targets are closer. |
| `shuffle_tile_order` | Boolean | `true` | Randomizes the execution order of AoE tiles. |
| `upgrade_straight_shot_to_boomerang` | Boolean | `true` | Makes the projectile return to caster. |
| `dont_orient` | Boolean | `true` | Prevents the character from turning to face the target. |
| `low_health_character_threshold` | [`Enum/String`](./Enums.md#enum-low_health_character_threshold) | `item_aux, 10, 5` | AI targeting threshold for seeking weak targets. |
| `randomize_target_within_range` | Number | `2, 0, 3` | Picks a random valid tile instead of the user's click. |
| `special_tile_tag` | [`Enum/String`](./Enums.md#enum-special_tile_tag) | `FinalBossTheChildLocation, FinalBossCloneSpot, ChaosValidPosition` | Targets only tiles with this specific tag. |
| `track_target` | Boolean | `true` | Projectile/Effect follows moving targets. |
| `corpse_priority` | Number | `10, 5` | AI preference for targeting dead bodies. |
| `hint_can_target_empty` | Boolean | `false, true` | UI hint that the player can click an empty tile. |
| `low_gravity_boostable` | Boolean | `false, true` | Can be affected by low gravity wind/effects. |
| `prioritize_change_direction` | Boolean | `true` | AI preference to attack from different angles. |
| `range_bonuses` | [`Enum/String`](./Enums.md#enum-range_bonuses) | `include_alpha` | How much extra range is added by stats/passives. |
| `range_display_include_direction` | Boolean | `true` | Visual: shows directional arrows. |
| `recalc_target_on_castpoint` | Boolean | `true` | Re-checks if target is valid at the exact frame of cast. |
| `redirect_location_if_blocked` | Boolean | `true` | Shifts target to adjacent tile if original is invalid. |
| `target_requires_element` | [`Array`](./Arrays.md#array-target_requires_element) | `[ grass ], [ grass water ]` | Target must be afflicted with this element. |
| `trample_allies_too` | Boolean | `true` | Trample movement damages allies in the path. |
| `adjust_target` | [`Enum/String`](./Enums.md#enum-adjust_target) | `stalk` | Tweaks target selection post-cast. |
| `allow_diagonal_passthrough` | Boolean | `true` | Permits diagonal targeting through tight corners. |
| `ally_priority` | Number | `1` | AI preference for targeting allies. |
| `aoe_display_exclude_restrictions` | Boolean | `true` | Visual only: Hides invalid tiles from the AoE preview. |
| `aoe_rotate_around_character_center` | Boolean | `true` | Anchors the AoE rotation to the character rather than the tile. |
| `aoe_spell_on_land` | Boolean | `true` | Visual trigger when a jump lands. |
| `bonus_pathing_leniency` | Number | `4` | Gives the AI leeway when calculating complex paths. |
| `custom_aoe_mirror` | [`Array`](./Arrays.md#array-custom_aoe_mirror) | `[ [ 1 0 ]` | How the custom shape mirrors when facing left vs right. |
| `custom_aoe_util_mirror` | [`Array`](./Arrays.md#array-custom_aoe_util_mirror) | `[ [ 1, 1 ]` |  |
| `damage_collided_only` | Boolean | `true` | Only damages the first entity the projectile/dash hits. |
| `enemy_priority` | Number | `10` | AI preference for targeting enemies. |
| `force_no_contact` | Boolean | `true` | Bypasses all contact-based retaliation (Thorns, etc). |
| `hint_can_target_static` | Boolean | `true` | UI hint that the player can target inanimate objects. |
| `knockback_modifier` | [`Enum/String`](./Enums.md#enum-knockback_modifier) | `rotate_cw` | Multiplier for the knockback physics force. |
| `lingering` | Boolean | `true` | Target zone remains active across multiple turns. |
| `mirror_custom_aoe` | Boolean | `true` | Flips the custom AoE array. |
| `prioritize_throw_target_with_passive` | [`Enum/String`](./Enums.md#enum-prioritize_throw_target_with_passive) | `NubbyTossPriority` | AI prefers throwing targets that have specific passives. |
| `randomize_knockback_direction_except_for_finisher` | Boolean | `true` | Chaotic knockback unless it kills the target. |
| `range_excludes_self` | Boolean | `false` | Cannot click on the caster's tile. |
| `range_max` | Number | `4` | Alternate syntax for `max_range`/`min_range`. |
| `range_min` | Number | `1` | Alternate syntax for `max_range`/`min_range`. |
| `range_symmetry` | [`Enum/String`](./Enums.md#enum-range_symmetry) | `eight_way` | Mirrors the range grid. |
| `remain_off_map` | Boolean | `true` | Keeps entity removed from the grid. |
| `restructions` | [`Enum/String`](./Enums.md#enum-restructions) | `aoe_must_exist` | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). |
| `reverse_target_direction` | Boolean | `true` | Inverts the targeting vector. |
| `spin_steps` | Number | `-16` | Number of rotational increments for spin targeting. |
| `uncounterable` | Boolean | `true` | Bypasses counter-attack passives. |

</details>

---

### Context: `meta`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"nothing", "ABILITY_MELEEATTACK_DESC", "ABILITY_CROWNOFPESTILENCE_DESC"` | The localization key for the ability's display description. |
| `name` | String | `"ABILITY_MELEEATTACK_NAME", "ABILITY_CROWNOFPESTILENCE_NAME", "None"` | The localization key for the ability's display name. |
| `class` | [`Enum/String`](./Enums.md#enum-class) | `Mage, Fighter, Hunter` | Categorizes the ability for specific UI filters. |
| `type_icon` | String | `"defense", "misc", "unknown"` |  |
| `animate_name` | Boolean | `false, true` | If true, adds a visual pop/animation to the name text when cast. |
| `icon_shell_frame` | [`Enum/String`](./Enums.md#enum-icon_shell_frame) | `multihit_attack, attack, "attack"` |  |
| `is_move` | [`Enum/String`](./Enums.md#enum-is_move) | `auto, true` |  |
| `ability_icon` | [`Enum/String`](./Enums.md#enum-ability_icon) | `BasicMelee, Pestilence, BasicRanged` | The UI icon to display in the action bar. |
| `tooltip_values` | [`Array`](./Arrays.md#array-tooltip_values) | `[ "max((X-1)*2, 0)" ], [ "X" ], [ "max(X*3, 0)" ]` |  |
| `icon_damage_display` | String | `"0-25", "?", "1-6"` |  |
| `icon_damage_display_eq` | [`Enum/String`](./Enums.md#enum-icon_damage_display_eq) | `item_aux, "10+bonus_melee_ability_damage", "3+bonus_melee_ability_damage"` |  |
| `is_basic_attack` | Boolean | `true` |  |
| `icon_damage_type` | [`Enum/String`](./Enums.md#enum-icon_damage_type) | `magic, physical` |  |
| `is_trinket` | Boolean | `true` |  |
| `dont_visualize_ai` | Boolean | `true` |  |
| `icon_damage_display_suffix` | String | `"x2", "x10"` |  |
| `is_weapon` | Boolean | `true` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `portin` |  |

</details>

---

### Context: `graphics`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `sing3, attack, none` | The primary flash animation label triggered. |
| `particle` | [`Enum/String`](./Enums.md#enum-particle) | `PoisonPoof, None, none` | References an impact or cast particle effect. |
| `projectile` | [`Enum/String`](./Enums.md#enum-projectile) | `LeechProjectile, NeedleProjectile, MagicSpikeProjectile` | References a projectile entity. |
| `lob` | Boolean | `false, true` |  |
| `delay` | Number | `2, 5, 4` | Frame delay before firing projectile/effect. |
| `dont_visualize_ai` | Boolean | `true` |  |
| `dont_orient` | Boolean | `true` | Prevents the character from turning to face the target. |
| `dash_animation` | [`Enum/String`](./Enums.md#enum-dash_animation) | `spinattackloop, roll, headbuttdash` | State-specific animations for trample/dash abilities. |
| `dash_start_animation` | [`Enum/String`](./Enums.md#enum-dash_start_animation) | `dashstart, headbuttdashStart, none` |  |
| `speed` | Number | `2, 20, .5` | Rotations per second. |
| `affected_particle` | [`Enum/String`](./Enums.md#enum-affected_particle) | `HealBig, HealMed, fx_tentaclestrangle` | Visuals applied to the target receiving the effect. |
| `dash_attack_animation` | [`Enum/String`](./Enums.md#enum-dash_attack_animation) | `headbuttdashEnd, spinattackloop, none` |  |
| `lob_height` | Number | `0, 1, 4` | Adjustments for arcing projectiles. |
| `animation_in` | [`Enum/String`](./Enums.md#enum-animation_in) | `teleportIn, shadowStepIn, digUp` | Used for transition states (like burrowing). |
| `animation_out` | [`Enum/String`](./Enums.md#enum-animation_out) | `shadowStepOut, teleportOut, digDown` | Used for transition states (like burrowing). |
| `jump_attack_animation` | [`Enum/String`](./Enums.md#enum-jump_attack_animation) | `gravitySlamEnd, block, land` | Overrides for jump physics. |
| `use_projectile` | Boolean | `true` |  |
| `full_jump_animation` | [`Enum/String`](./Enums.md#enum-full_jump_animation) | `jumpmove, attack, jumpattack` |  |
| `full_jump_sync_frames` | Number | `38, 46, 49` |  |
| `use_rotation` | Boolean | `false` |  |
| `dash_end_animation` | [`Enum/String`](./Enums.md#enum-dash_end_animation) | `timberEnd, dashend, launchStop` |  |
| `palette` | Number | `6` | Swaps the color palette ID. |
| `full_jump_windup_frames` | Number | `13, 20, 22` |  |
| `visual_delay_but_simultaneous_damage` | Number | `8, 0, 3` |  |
| `center_particle` | [`Enum/String`](./Enums.md#enum-center_particle) | `FireBlastMushroom, Explosion, none` | Specific spawn points for particles. |
| `area_particle` | [`Enum/String`](./Enums.md#enum-area_particle) | `FireBlastSmall, BurnTrigger, none` | Specific spawn points for particles. |
| `fall_from_sky` | Boolean | `true` | Spawns the projectile from the top of the screen. |
| `move_start_animation` | [`Enum/String`](./Enums.md#enum-move_start_animation) | `startroll, buttScootStart, none` |  |
| `use_placeholder` | Boolean | `true` |  |
| `move_end_animation` | [`Enum/String`](./Enums.md#enum-move_end_animation) | `buttScootEnd, endroll, none` |  |
| `face_toss_target` | Boolean | `true` |  |
| `ignore_slowtiles` | Boolean | `true` |  |
| `chain_distance` | [`Enum/String`](./Enums.md#enum-chain_distance) | `.25, .38` | Creates a tethered repeating graphic (like a hook). |
| `chain_movieclip` | [`Enum/String`](./Enums.md#enum-chain_movieclip) | `ChainLink, Bramblechain, Frogchain` | Creates a tethered repeating graphic (like a hook). |
| `darken_screen` | Boolean | `false, true` | Dims the background during the ability cast. |
| `beam_cap` | [`Enum/String`](./Enums.md#enum-beam_cap) | `greenlasercap, greenmegalasercap, thinlasercap` | Flash movieclips used to render continuous laser beams. |
| `beam_clip` | [`Enum/String`](./Enums.md#enum-beam_clip) | `greenmegalaser, greenlaser, thinlaser` | Flash movieclips used to render continuous laser beams. |
| `bounce_on_hit` | Boolean | `false, true` | Visual hop when striking a target. |
| `darken_screen_exclude_characters_on_tile` | Boolean | `false, true` |  |
| `end` | [`Enum/String`](./Enums.md#enum-end) | `spinattackend, attack, lickAttack` | Segments for continuous channeled animations. |
| `jump_start_animation` | [`Enum/String`](./Enums.md#enum-jump_start_animation) | `gravitySlamStart, leapattackwindup, none` |  |
| `loop` | [`Enum/String`](./Enums.md#enum-loop) | `spinattackloop, attack, lickAttack` | Segments for continuous channeled animations. |
| `prime_animation` | [`Enum/String`](./Enums.md#enum-prime_animation) | `pointout, prouder, chargeholy` |  |
| `start` | [`Enum/String`](./Enums.md#enum-start) | `spinattackstart, attack, lickAttack` | Segments for continuous channeled animations. |
| `max_tiles_single_loop` | Number | `6, 1, 5` |  |
| `random_delay` | [`Array`](./Arrays.md#array-random_delay) | `[ 70 100 ], [ 30 50 ], [ 0, 120 ]` | Adds chaotic timing to multi-projectile casts. |
| `sync_speed` | Number | `28, 30, 22` |  |
| `fx_is_placeholder_animation` | Boolean | `true` |  |
| `aoe_spell_on_land` | Boolean | `true` | Visual trigger when a jump lands. |
| `fx_random_flip` | Boolean | `true` |  |
| `land_animation` | [`Enum/String`](./Enums.md#enum-land_animation) | `none` |  |
| `miss_particle` | [`Enum/String`](./Enums.md#enum-miss_particle) | `fx_tentaclestrangleMiss` | Specific spawn points for particles. |
| `use_super_armor` | Boolean | `false, true` | Prevents flinch animations from interrupting this cast. |
| `air_animation` | [`Enum/String`](./Enums.md#enum-air_animation) | `entrance, gravitySlam_air, bellyflop_air` | Animation played while entity is airborne. |
| `custom_priming_animation` | [`Enum/String`](./Enums.md#enum-custom_priming_animation) | `priming, idleCommand3, idleCommand2` | Animation used while charging an ability. |
| `darken_screen_exclude_self` | Boolean | `true` |  |
| `darken_screen_start_early` | Boolean | `true` |  |
| `fall_randomize_timing` | [`Enum/String`](./Enums.md#enum-fall_randomize_timing) | `.3` |  |
| `min_throw_height` | Number | `0, 4, 1.75` |  |
| `miss_random_delay` | [`Array`](./Arrays.md#array-miss_random_delay) | `[ 0, 60 ], [ 0, 20 ]` |  |
| `single_projectile` | Boolean | `true` |  |
| `detatched_animation` | [`Enum/String`](./Enums.md#enum-detatched_animation) | `LiquidMetalSpear, TinaSpear, WaterGush` | Plays an animation separated from the character body. |
| `detatched_animation_reach` | Number | `3, 20, 4` |  |
| `empty_animation` | [`Enum/String`](./Enums.md#enum-empty_animation) | `empty` |  |
| `mode` | [`Enum/String`](./Enums.md#enum-mode) | `yeet` |  |
| `fixed_jump_height` | Number | `1, 3.5` |  |
| `sync_frames` | Number | `26, 34` |  |
| `dash_decelerating_animation` | [`Enum/String`](./Enums.md#enum-dash_decelerating_animation) | `dashslow` |  |
| `decelerate` | Number | `5` | Visual slowdown at the end of a movement. |
| `delay_from_map_edge` | Boolean | `false, true` | Delays effect based on distance from the screen edge. |
| `easing` | Number | `1` | Smoothing function for movement animations. |
| `fixed_jump_speed` | Number | `2, 1, .8` |  |
| `grab_animation` | [`Enum/String`](./Enums.md#enum-grab_animation) | `grab` |  |
| `lob_yoff` | [`Enum/String`](./Enums.md#enum-lob_yoff) | `-.5` | Adjustments for arcing projectiles. |
| `lock_orientation_during_dash` | Boolean | `true` | Prevents the sprite from flipping mid-dash. |
| `use_projectile_spawn_offset` | Boolean | `true` |  |
| `use_rotation_once` | Boolean | `true` |  |
| `always_play_animations` | Boolean | `true` | Bypasses speed-up/skip logic. |
| `detatched_animation_cutoff` | Boolean | `true` |  |
| `do_damage_immediately` | Boolean | `true` | Applies math before the animation actually hits. |
| `jump_height_multiplier` | Number | `2, .25` | Overrides for jump physics. |
| `mask_center` | [`Enum/String`](./Enums.md#enum-mask_center) | `SpearMaskCenter` |  |
| `mask_extent` | [`Enum/String`](./Enums.md#enum-mask_extent) | `SpearMaskExtent` |  |
| `max_throw_height` | Number | `1.75` |  |
| `particle_mat` | [`Enum/String`](./Enums.md#enum-particle_mat) | `shadow_occluded_spelldissolve` |  |
| `preturn_animation` | [`Enum/String`](./Enums.md#enum-preturn_animation) | `alertstart` |  |
| `primed_alt_animation` | String | `"shootPrimed"` |  |
| `pseudoprojectile` | [`Enum/String`](./Enums.md#enum-pseudoprojectile) | `RocketFromAbove` |  |
| `reverse_orientation` | Boolean | `true` |  |
| `self_damage_mid_port` | Boolean | `true` |  |
| `throw_speed` | Number | `3` |  |
| `use_hit_alts` | Boolean | `false` |  |
| `affected_animation` | [`Enum/String`](./Enums.md#enum-affected_animation) | `statDown` | Visuals applied to the target receiving the effect. |
| `ally_animation` | [`Enum/String`](./Enums.md#enum-ally_animation) | `lickAttack` | Distinct animation used when targeting a friendly unit. |
| `animate_name` | [`Enum/String`](./Enums.md#enum-animate_name) | `pointout` | Animates the ability name text on cast. |
| `apex_distance` | Number | `0.875` | Calculations for the peak of a jump/lob arc. |
| `apex_time` | [`Enum/String`](./Enums.md#enum-apex_time) | `.35` | Calculations for the peak of a jump/lob arc. |
| `bypass_combatspeed` | Boolean | `true` |  |
| `dash_bonk_animation` | [`Enum/String`](./Enums.md#enum-dash_bonk_animation) | `bonk` |  |
| `delay_from_map_center` | Boolean | `true` | Positional based timing delays. |
| `delay_from_reverse_map_edge` | Boolean | `true` |  |
| `do_animation_offscreen` | Boolean | `true` |  |
| `do_not_clear_placeholder` | Boolean | `true` |  |
| `face_targets` | Boolean | `true` | Forces the sprite to look at the target tile. |
| `first_castpoint_is_self_damage_only` | Boolean | `true` |  |
| `hang_time` | [`Enum/String`](./Enums.md#enum-hang_time) | `.6` |  |
| `jump_speed_multiplier` | Number | `1.5` |  |
| `lob_speed` | [`Enum/String`](./Enums.md#enum-lob_speed) | `.5` | Adjustments for arcing projectiles. |
| `max_range` | Number | `3` | The maximum and minimum distance required to cast. |
| `min_range` | Number | `1` | The maximum and minimum distance required to cast. |
| `othercat_placeholder_available` | Boolean | `true` |  |
| `precast_delay` | [`Enum/String`](./Enums.md#enum-precast_delay) | `.25` |  |
| `spawn_offset` | [`Array`](./Arrays.md#array-spawn_offset) | `[ 0, .5, 0 ]` |  |
| `uncatchable` | Boolean | `true` |  |
| `use_directional_animations` | Boolean | `true` |  |
| `use_origin_offsets` | Boolean | `false` |  |

</details>

---

### Context: `cost`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `mana` | Number | `7, 0, 5` | MP pool and how much it restores per turn. |
| `infcantrip` | Boolean | `false, true` | Can be cast infinitely as long as costs are met. |
| `cantrip` | Boolean | `false, true` | Does not end the turn when cast. |
| `once_per_fight` | Boolean | `false, 3-X, true` | Exhausts for the remainder of combat after one use. |
| `act_points` | Number | `0, 1, 3` | Consumes primary action points (default 1). |
| `move_points` | Number | `1, 0` | Consumes movement points. |
| `prime` | Number | `1` | Requires a "priming" turn before it fires. |
| `allow_offmap_casts` | Boolean | `true` | Can be used while the character is hidden/removed from grid. |
| `cant_cast` | Boolean | `false, true, X-5` | Explicitly disables casting (used for passive-triggered only abilities). |
| `must_be_consuming` | Boolean | `true` | Requires the character to be eating/holding something. |
| `charge` | String | `"1-clamp(spd,0,1)", 0, 1` | Cooldown timers measured in turns. |
| `must_not_be_consuming` | Boolean | `true` | Cannot be holding/eating an entity. |
| `requires_reload` | Boolean | `true` | Must spend an action to reload before casting again. |
| `can_cast_while_dead` | Boolean | `true` | Usable by corpses (e.g., DeathRattle triggers). |
| `cantrip_group` | [`Enum/String`](./Enums.md#enum-cantrip_group) | `THC_CoinRoll, kaiju_roar, spewer_suck` | Groups cantrips so using one exhausts the others. |
| `must_be_offmap` | Boolean | `true` | Requires the character to be hidden/dug underground. |
| `X_cant_be_zero` | Boolean | `true` | Applies or references the 'X_cant_be_zero' effect/state. |
| `disallow_cost_modification` | Boolean | `true` | Prevents passives from making this cheaper. |
| `coins` | Number | `7, 1, 5` | Consumes currency to cast. |
| `durability` | Number | `0` | Consumes item durability. |
| `main_turn_only` | Boolean | `true` | Cannot be cast during bonus or dispersed turns. |
| `requires_destructible_weapon` | Boolean | `true` | The equipped weapon must be breakable. |
| `requires_exact_character_aux` | Number | `1, 2, 0` | Hardcoded character specific lock. |
| `must_not_be_a_summon` | Boolean | `true` | Summons/Familiars cannot cast this. |
| `start_reloaded` | Boolean | `true` | Spawns with the ability pre-loaded. |
| `must_be_first_action` | Boolean | `false, true` | Can only be used at the very start of the turn. |
| `enabled_formula` | [`Enum/String`](./Enums.md#enum-enabled_formula) | `1-X, 1, X` | Mathematical string required to be >0 to cast. |
| `must_be_first_nonmove_action` | Boolean | `true` | Can move first, but cannot use other abilities first. |
| `must_have_weapon` | Boolean | `true` | Requires a weapon equipped in the item slot. |
| `can_be_refreshed` | Boolean | `false` | Passives/Effects can reset this ability's cooldown. |
| `can_pay_over_multiple_turns` | Boolean | `true` | Allows channeling costs over time. |
| `can_self_refresh` | Boolean | `false` | The ability has mechanics to reset its own cooldown. |
| `damage_cant_be_zero` | Boolean | `true` | Requires the ability to have >0 calculated damage to cast. |
| `initial_charge` | Number | `1` | How many turns it starts on cooldown at battle start. |
| `manacost_cant_be_zero` | Boolean | `true` | Fails to cast if mana cost is reduced to 0. |
| `minimum_con` | Number | `1` | Stat thresholds required to cast. |
| `minimum_spd` | Number | `1` | Stat thresholds required to cast. |
| `require_default_size` | Boolean | `true` | 2x2 or altered characters cannot cast this. |
| `requires_attack_damage_threshold` | Number | `2` | Needs a certain amount of innate damage. |
| `requires_consumed_trinket` | Boolean | `true` | Must have eaten a specific item type. |
| `requires_empty_trinket` | Boolean | `true` | Must not have an accessory equipped. |
| `requires_hp_threshold` | Number | `200` | Must be below/above a certain health percentage. |
| `requires_weapon` | Boolean | `true` | Prerequisite: Must meet this condition. |

</details>

---

### Context: `damage_instance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `2, 0, 4` | The base damage properties of an attack. |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `physical_spell, status_spell, melee` | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Gravity ], [ Water ], [ Holy ]` | Array of elemental tags to apply (e.g., `[Fire Holy]`). |
| `knockback` | [`Equation`](./Enums.md#enum-mathequation) | `"ceil(X*.25/5)", 1, 5` | The base physics pushing power (in tiles). |
| `ai_base_score` | Number | `1000, 9999, 999999` | How highly the AI values using this ability. |
| `heal` | Number | `10, 1, 4` | Restores health instead of dealing damage. |
| `cant_miss` | Boolean | `true` | Guarantees the hit, bypassing dodge mechanics. |
| `incidentally_collects_pickups` | Boolean | `false, true` | Automatically grabs items in the AoE. |
| `custom_additional_ai_weight` | [`Enum/String`](./Enums.md#enum-custom_additional_ai_weight) | `toss_towards_buddy, tile_close_to_enemy, prefer_dont_move` | Granular AI preference adjustments (e.g., `prefer_dont_move`). |
| `piercing` | Boolean | `true` | Ignores a percentage of target defense/armor. |
| `makes_contact` | Boolean | `false, true` | If false, explicitly avoids triggering contact-based passives. |
| `layer` | [`Enum/String`](./Enums.md#enum-layer) | `characters, tiles, all` | Z-index targeting (e.g., `characters`, `self`). |
| `blocked_damage` | [`Equation`](./Enums.md#enum-mathequation) | `7+bonus_melee_ability_damage, 5+bonus_melee_damage, 3+bonus_melee_ability_damage` | Base damage dealt if the attack is blocked. |
| `raw_damage` | [`Enum/String`](./Enums.md#enum-raw_damage) | `int, "(con+1)/2", "max((X-1)*2, 0)"` | Unmitigated, unscaled base numbers. |
| `crit_chance` | Number | `-999999, .5, 100%` | Override for base critical hit probability. |
| `override_trample_damage` | Boolean | `true` | Custom damage value for trample moves. |
| `contact_requires_adjacency` | Boolean | `false` | Contact effects only trigger if standing next to the target. |
| `can_revive` | Boolean | `true` | Healing instance that can bring dead allies back to life. |
| `show_damage_on_0` | Boolean | `true` | Forces the "-0" floater text to appear. |
| `force_play_hit_animation` | Boolean | `true` | Forces the flinch animation even on 0 damage. |
| `blocked_multiplier` | Number | `2` | Multiplier applied when hitting a blocking target. |
| `accuracy` | [`Enum/String`](./Enums.md#enum-accuracy) | `.5` | Hit chance modifier. |
| `can_collect_pickups` | Boolean | `true` | The damage instance can grab items on the ground. |
| `can_instapop` | Boolean | `false` | Allows the attack to instantly destroy specific weak entities. |
| `disallow_modifications` | Boolean | `true` | Prevents passives from altering this damage instance. |
| `force_no_contact` | Boolean | `true` | Bypasses all contact-based retaliation (Thorns, etc). |
| `non_lethal` | Boolean | `true` | Reduces target to 1 HP but will never kill. |
| `raw_heal` | [`Equation`](./Enums.md#enum-mathequation) | `"(str+1)/2", "100-X"` | Unmitigated, unscaled base numbers. |
| `two_way_contact` | Boolean | `true` | Both caster and target trigger contact effects on each other. |
| `HealthRegenUp` | Number | `2` | Applies or references the 'HealthRegenUp' effect/state. |
| `damage_shield_only` | Boolean | `true` | Depletes shields but cannot harm base health. |
| `faction` | [`Enum/String`](./Enums.md#enum-faction) | `auto` | Determines alignment (`enemies`, `cats`, `neutral`). |
| `final_hit_bonus_damage` | [`Equation`](./Enums.md#enum-mathequation) | `5+bonus_melee_ability_damage` | Extra damage applied on the last hit of a multihit. |
| `force_adjacent_and_diagonal_contact` | Boolean | `true` | Treats diagonal hits as physical contact. |
| `force_no_knockback` | Boolean | `true` | Prevents the target from being pushed. |
| `hint_dont_lowgravboost` | Boolean | `true` | AI hint to ignore wind physics. |
| `hit_animation_alt` | [`Enum/String`](./Enums.md#enum-hit_animation_alt) | `catch` | Custom flinch animation for the target. |
| `ranged` | Boolean | `true` | Boolean flagging the damage as explicitly ranged. |

</details>

---

### Context: `effects`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FormChange` | [`Enum/String`](./Enums.md#enum-formchange) | `DualSword, Explosive, Holy` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `Stun` | Number | `1, [ 1 .5 ], [ 1, .25 ]` | Applies or references the 'Stun' effect/state. |
| `Burn` | Number | `2, 1, 3` | Applies or references the 'Burn' effect/state. |
| `IgnoreSelf` | Number | `1, true` | Applies or references the 'IgnoreSelf' effect/state. |
| `Bruise` | Number | `2, 1, 5` | Applies or references the 'Bruise' effect/state. |
| `Poison` | Number | `2, 3, 4` | Applies or references the 'Poison' effect/state. |
| `ChangeTile` | [`Enum/String`](./Enums.md#enum-changetile) | `WaterTile, LavaTile, FireTile` | Transforms the terrain tile under the target. |
| `Else` | [`Block`](./Abilities_and_Spells.md#context-else) | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `Bleed` | Number | `2, 1, 10` | Applies or references the 'Bleed' effect/state. |
| `Shield` | [`Equation`](./Enums.md#enum-mathequation) | `"max((X-1)*2, 0)", 2, 5` | Applies or references the 'Shield' effect/state. |
| `Cleanse` | Number | `1, 0` | Applies or references the 'Cleanse' effect/state. |
| `Conditional_HasTag` | [`Block`](./Abilities_and_Spells.md#context-conditional_hastag) | `{ ... }` | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. |
| `Conditional_Enemy` | [`Block`](./Abilities_and_Spells.md#context-conditional_enemy) | `{ ... }` | Conditional trigger: Executes nested logic if the target is hostile to the caster. |
| `Confusion` | Number | `2, 1, 4` | Applies or references the 'Confusion' effect/state. |
| `SpeedUp` | Number | `2, 1, -1` | Applies or references the 'SpeedUp' effect/state. |
| `Temporary` | [`Block`](./Abilities_and_Spells.md#context-temporary) | `{ ... }` | A wrapper block for applying status effects that automatically expire. |
| `BounceObject` | [`Enum/String`](./Enums.md#enum-bounceobject) | `CharmedDip, SmallRock, CharmedFlea` | Spawns a physics object that visually bounces off the target. |
| `AllStatsUp` | [`Enum/String`](./Enums.md#enum-allstatsup) | `item_aux, 1, -1` | Applies or references the 'AllStatsUp' effect/state. |
| `DamageUp` | Number | `-2, 1, -1` | Applies or references the 'DamageUp' effect/state. |
| `TransformAbility` | [`Enum/String`](./Enums.md#enum-transformability) | `MonkeyThrow, Pounce, Pounce2` | Applies or references the 'TransformAbility' effect/state. |
| `ApplyToSource` | [`Block`](./Abilities_and_Spells.md#context-applytosource) | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `ManaGain` | [`Equation`](./Enums.md#enum-mathequation) | `"max((X-1)*2, 0)", 10, 5` | Applies or references the 'ManaGain' effect/state. |
| `Slow` | [`Array`](./Arrays.md#array-slow) | `[ 1 .1 ], [ 1 .25 ], 1` | Applies or references the 'Slow' effect/state. |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1 .25 ], 2, 1` | Applies or references the 'Fear' effect/state. |
| `Weakness` | [`Array`](./Arrays.md#array-weakness) | `[ 1 .25 ], 2, 1` | Applies or references the 'Weakness' effect/state. |
| `Blind` | [`Array`](./Arrays.md#array-blind) | `[ 1 .25 ], 1, [ 2 .33 ]` | Applies or references the 'Blind' effect/state. |
| `Leech` | Number | `1` | Applies or references the 'Leech' effect/state. |
| `StrengthUp` | [`Enum/String`](./Enums.md#enum-strengthup) | `item_aux, 2, 1` | Applies or references the 'StrengthUp' effect/state. |
| `ConstitutionUp` | Number | `1, [ 1 .5 ], -1` | Applies or references the 'ConstitutionUp' effect/state. |
| `EvolveAbilityFromPool` | [`Block`](./Abilities_and_Spells.md#context-evolveabilityfrompool) | `{ ... }, Mage, Fighter` | Upgrades or transforms an existing ability into a new one from the specified pool. |
| `Immobile` | Number | `0, 2, 1` | Applies or references the 'Immobile' effect/state. |
| `IntelligenceUp` | [`Equation`](./Enums.md#enum-mathequation) | `-int, item_aux, 1` | Applies or references the 'IntelligenceUp' effect/state. |
| `VisualFXTile` | [`Enum/String`](./Enums.md#enum-visualfxtile) | `PoisonPoof, WaterConduct, FireBlastSmall` | Applies or references the 'VisualFXTile' effect/state. |
| `Charmed` | [`Enum/String`](./Enums.md#enum-charmed) | `level, [ 1, .1+.02*cha ], 1` | Applies or references the 'Charmed' effect/state. |
| `Sleep` | [`Array`](./Arrays.md#array-sleep) | `[ 1 .1 ], 1, 3` | Applies or references the 'Sleep' effect/state. |
| `Vaporize` | Number | `1, 20` | Applies or references the 'Vaporize' effect/state. |
| `Madness` | Number | `999, 1, 3` | Applies the Madness debuff/status effect. |
| `Brace` | Number | `2, 1, 4` | Applies or references the 'Brace' effect/state. |
| `CollectsPickups` | Number | `2, 1` | Applies or references the 'CollectsPickups' effect/state. |
| `KnockUpAndAway` | [`Block`](./Abilities_and_Spells.md#context-knockupandaway) | `{ ... }` | Displaces the target vertically and horizontally away from the source. |
| `RandomStatUp` | Number | `-5, 10, 1` | Applies or references the 'RandomStatUp' effect/state. |
| `Freeze` | [`Array`](./Arrays.md#array-freeze) | `[ 1 .1 ], [ 1 .25 ], 1` | Applies or references the 'Freeze' effect/state. |
| `OverrideKnockbackDamage` | Number | `0, str, 3` | Applies or references the 'OverrideKnockbackDamage' effect/state. |
| `Consumed` | [`Block`](./Abilities_and_Spells.md#context-consumed) | `{ ... }` | State block triggered when this object or entity is eaten/consumed by another character. |
| `VaporizeCorpse` | Number | `1` | Applies or references the 'VaporizeCorpse' effect/state. |
| `ChangeCatClass` | [`Enum/String`](./Enums.md#enum-changecatclass) | `Mage, Fighter, Hunter` | Applies or references the 'ChangeCatClass' effect/state. |
| `DivineShield` | Number | `2, 1, 4` | Applies or references the 'DivineShield' effect/state. |
| `EndTurn` | Number | `1` | Applies or references the 'EndTurn' effect/state. |
| `FaceAway` | Number | `1` | Applies or references the 'FaceAway' effect/state. |
| `RefreshMovePoints` | Number | `1` | Applies or references the 'RefreshMovePoints' effect/state. |
| `TakeExtraTurn` | Number | `1` | Applies or references the 'TakeExtraTurn' effect/state. |
| `TransformBasicAttack` | [`Enum/String`](./Enums.md#enum-transformbasicattack) | `ThrowPoop, TigerSwipes2, TigerSwipes` | Applies or references the 'TransformBasicAttack' effect/state. |
| `CatPartsTransform` | [`Block`](./Abilities_and_Spells.md#context-catpartstransform) | `{ ... }` | Transforms specific body parts into different visual variants. |
| `Conditional_Boss` | [`Block`](./Abilities_and_Spells.md#context-conditional_boss) | `{ ... }` | Conditional trigger: Executes nested logic if the target is a Boss. |
| `GenericDebuff` | Number | `100, 1, 999` | Applies or references the 'GenericDebuff' effect/state. |
| `Leeches` | Number | `2, 1, 3` | Applies or references the 'Leeches' effect/state. |
| `Petrify` | [`Array`](./Arrays.md#array-petrify) | `[ 1 .1 ], 1, [ 1, .1 ]` | Applies or references the 'Petrify' effect/state. |
| `RandomMagicMissile` | [`Block`](./Abilities_and_Spells.md#context-randommagicmissile) | `{ ... }, 1, 5` | Fires a randomized number of magic missiles. |
| `RandomStatusFromPool` | [`Block`](./Abilities_and_Spells.md#context-randomstatusfrompool) | `{ ... }` | Selects and applies a random status effect from the provided nested block. |
| `Displace` | Number | `1` | Applies or references the 'Displace' effect/state. |
| `LuckUp` | [`Enum/String`](./Enums.md#enum-luckup) | `item_aux, -2, 1` | Applies or references the 'LuckUp' effect/state. |
| `ApplyToSourceOnKill` | [`Block`](./Abilities_and_Spells.md#context-applytosourceonkill) | `{ ... }` | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. |
| `Cleave` | [`Block`](./Abilities_and_Spells.md#context-cleave) | `{ ... }, 1` | Causes the attack to hit adjacent enemies alongside the primary target. |
| `Conditional_GoodRoll` | [`Block`](./Abilities_and_Spells.md#context-conditional_goodroll) | `{ ... }` | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. |
| `DoScreenShake` | [`Block`](./Abilities_and_Spells.md#context-doscreenshake) | `{ ... }, 1` | Triggers a camera screen shake effect. |
| `FullHeal` | Number | `1` | Applies or references the 'FullHeal' effect/state. |
| `Conditional_Speculative` | [`Block`](./Abilities_and_Spells.md#context-conditional_speculative) | `{ ... }` | A simulation block used by the AI to test hypothetical outcomes before committing to an action. |
| `DexterityUp` | [`Enum/String`](./Enums.md#enum-dexterityup) | `item_aux, 2, 1` | Applies or references the 'DexterityUp' effect/state. |
| `MagicWeakness` | [`Array`](./Arrays.md#array-magicweakness) | `[ 1 .1 ], 1, 4` | Applies or references the 'MagicWeakness' effect/state. |
| `PartialPurge` | Number | `1` | Applies or references the 'PartialPurge' effect/state. |
| `PurgeAll` | Number | `1` | Applies or references the 'PurgeAll' effect/state. |
| `RefreshActPoints` | Number | `1` | Applies or references the 'RefreshActPoints' effect/state. |
| `Thorns` | Number | `6, 2, 1` | Applies or references the 'Thorns' effect/state. |
| `Ammo` | Number | `6, -99999, -1` | Applies or references the 'Ammo' effect/state. |
| `ApplyPassives` | [`Block`](./Abilities_and_Spells.md#context-applypassives) | `{ ... }` | Grants the nested passive abilities dynamically. |
| `DeferVaporize` | Number | `1` | Applies or references the 'DeferVaporize' effect/state. |
| `Marked` | [`Array`](./Arrays.md#array-marked) | `[ 1 .1 ], 1, 5` | Applies or references the 'Marked' effect/state. |
| `SpawnCreep` | Number | `1` | Applies or references the 'SpawnCreep' effect/state. |
| `VisualFX` | [`Enum/String`](./Enums.md#enum-visualfx) | `WaterConduct, Holyatk, MagicMissleBlast` | Applies or references the 'VisualFX' effect/state. |
| `CanApplyToInanimate` | [`Block`](./Abilities_and_Spells.md#context-canapplytoinanimate) | `{ ... }` | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. |
| `ChanceToBreak` | Number | `20, 5, 15` | Applies or references the 'ChanceToBreak' effect/state. |
| `HealthRegenUp` | Number | `2, 1, 3` | Applies or references the 'HealthRegenUp' effect/state. |
| `OverrideChainKnockback` | Number | `10, 1, 3` | Applies or references the 'OverrideChainKnockback' effect/state. |
| `Rot` | [`Array`](./Arrays.md#array-rot) | `[ 1 .1 ], 2, 1` | Applies or references the 'Rot' effect/state. |
| `AlphaCat` | Number | `1` | Applies or references the 'AlphaCat' effect/state. |
| `BramblesOnHit` | Number | `1` | Applies or references the 'BramblesOnHit' effect/state. |
| `ContextualHeal` | Number | `1` | Applies or references the 'ContextualHeal' effect/state. |
| `ForceAttack` | [`Block`](./Abilities_and_Spells.md#context-forceattack) | `{ ... }, 1` | Forces the character to execute an immediate attack. |
| `Instakill` | Number | `50, 25` | Applies or references the 'Instakill' effect/state. |
| `KnockbackDamageImmuneUntilSettled` | Number | `1` | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. |
| `ManaSteal` | Number | `5, -1` | Applies or references the 'ManaSteal' effect/state. |
| `Tech` | Number | `1, 3` | Applies or references the 'Tech' effect/state. |
| `TempRangeUp` | Number | `1, 20, 3` | Applies or references the 'TempRangeUp' effect/state. |
| `TriggerWerewolfTransform` | [`Array`](./Arrays.md#array-triggerwerewolftransform) | `[ 1 .15 ], .5, [ 1 .5 ]` | Applies or references the 'TriggerWerewolfTransform' effect/state. |
| `BackflipWhenTargeted` | [`Block`](./Abilities_and_Spells.md#context-backflipwhentargeted) | `{ ... }, 2, 1` | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |
| `BounceRock` | [`Enum/String`](./Enums.md#enum-bouncerock) | `SmallRock, SmallLavaRock, [ 1 .2 ]` | Applies or references the 'BounceRock' effect/state. |
| `CharismaUp` | [`Enum/String`](./Enums.md#enum-charismaup) | `item_aux, -2, 1` | Applies or references the 'CharismaUp' effect/state. |
| `ClearStarving` | Number | `1` | Applies or references the 'ClearStarving' effect/state. |
| `Conditional_Corpse` | [`Block`](./Abilities_and_Spells.md#context-conditional_corpse) | `{ ... }` | Conditional trigger: Executes nested logic if the target is a dead body/corpse. |
| `ConjureBonusAbility` | [`Block`](./Abilities_and_Spells.md#context-conjurebonusability) | `{ ... }, Colorless, random` | Adds a temporary bonus ability to the character's hand/deck. |
| `Craft` | [`Block`](./Abilities_and_Spells.md#context-craft) | `{ ... }` | Synthesizes or spawns a new item from a specific pool. |
| `Metronome` | [`Block`](./Abilities_and_Spells.md#context-metronome) | `{ ... }, 2, 1` | Executes a random musical or metronome ability. |
| `ObjectOnHitCharacter` | [`Block`](./Abilities_and_Spells.md#context-objectonhitcharacter) | `{ ... }, SmallRock, SkeletonCatFamiliar` | Spawns a specific character or entity upon impact. |
| `RandomInjury` | Number | `1` | Applies or references the 'RandomInjury' effect/state. |
| `RemoveStatus` | [`Enum/String`](./Enums.md#enum-removestatus) | `Drowsy, SleepParalysis, Sleep` | Applies or references the 'RemoveStatus' effect/state. |
| `ScatterHeldCoin` | Number | `1, [ 1 .5 ], [ 1 .3 ]` | Applies or references the 'ScatterHeldCoin' effect/state. |
| `SetDistanceDisplace` | Number | `5` | Applies or references the 'SetDistanceDisplace' effect/state. |
| `SetHealth` | Number | `100%, 1` | Applies or references the 'SetHealth' effect/state. |
| `SpawnThingIfHitKills` | [`Enum/String`](./Enums.md#enum-spawnthingifhitkills) | `BiggestFood, Food, BigFood` | Applies or references the 'SpawnThingIfHitKills' effect/state. |
| `SpiderInfested` | Number | `2, 1, 4` | Applies or references the 'SpiderInfested' effect/state. |
| `Tarred` | [`Array`](./Arrays.md#array-tarred) | `[ 1 .1 ], 2` | Applies or references the 'Tarred' effect/state. |
| `TeamCastAbility` | [`Enum/String`](./Enums.md#enum-teamcastability) | `TeamFlex_Impl2, Spin, TeamFlex_Impl` | Requires or involves multiple characters to execute the ability. |
| `Conditional_HasStatus` | [`Block`](./Abilities_and_Spells.md#context-conditional_hasstatus) | `{ ... }` | Conditional trigger: Executes nested logic if the target currently has the specified status effect. |
| `Conditional_InForm` | [`Block`](./Abilities_and_Spells.md#context-conditional_inform) | `{ ... }` | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. |
| `Conditional_NotBoss` | [`Block`](./Abilities_and_Spells.md#context-conditional_notboss) | `{ ... }` | Conditional trigger: Executes nested logic if the target is NOT a Boss. |
| `Conditional_Object` | [`Block`](./Abilities_and_Spells.md#context-conditional_object) | `{ ... }` | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. |
| `Conditional_PlayerCat` | [`Block`](./Abilities_and_Spells.md#context-conditional_playercat) | `{ ... }` | Conditional trigger: Executes nested logic if the target is a player-controlled cat. |
| `DodgeChance_Status` | Number | `50, 10, 20` | Applies or references the 'DodgeChance_Status' effect/state. |
| `Drowsy` | Number | `8, 1` | Applies or references the 'Drowsy' effect/state. |
| `FillMana` | Number | `1` | Applies or references the 'FillMana' effect/state. |
| `FlatLeech` | Number | `2, 10` | Applies or references the 'FlatLeech' effect/state. |
| `ForceMoveAway` | Number | `1` | Applies or references the 'ForceMoveAway' effect/state. |
| `ForceMoveTowards` | Number | `1` | Applies or references the 'ForceMoveTowards' effect/state. |
| `HitExplosion` | Number | `5` | Applies or references the 'HitExplosion' effect/state. |
| `Imprison` | [`Enum/String`](./Enums.md#enum-imprison) | `CharmedLeech, BeefyCharmedLeech, Tumor` | Applies or references the 'Imprison' effect/state. |
| `KnockbackDirectionIsFacingDirection` | [`Enum/String`](./Enums.md#enum-knockbackdirectionisfacingdirection) | `rotate_right, 1, flip` | Applies or references the 'KnockbackDirectionIsFacingDirection' effect/state. |
| `MonkStanceSwitch` | Number | `1` | Applies or references the 'MonkStanceSwitch' effect/state. |
| `MovementUp` | Number | `2, -2, 1` | Applies or references the 'MovementUp' effect/state. |
| `ObjectOnHit` | [`Block`](./Abilities_and_Spells.md#context-objectonhit) | `{ ... }, BiggestFood, FetusNoJar` | Spawns a specific physics/item object upon impact. |
| `ObjectOnHitEmpty` | [`Enum/String`](./Enums.md#enum-objectonhitempty) | `AnimalEgg, AnimalEgg2, SmallRock` | Applies or references the 'ObjectOnHitEmpty' effect/state. |
| `PopAndSpawn` | [`Enum/String`](./Enums.md#enum-popandspawn) | `TheDestroyer, StemCat_HalfHealth, Tormentor` | Destroys the target and replaces it with a new spawned entity. |
| `Purge` | Number | `0, 3` | Applies or references the 'Purge' effect/state. |
| `RefreshMovePointsIfHit` | Number | `1` | Applies or references the 'RefreshMovePointsIfHit' effect/state. |
| `Revive` | Number | `1, 50%, 100%` | Applies or references the 'Revive' effect/state. |
| `SafeDie` | Number | `1` | Applies or references the 'SafeDie' effect/state. |
| `SoulLink` | Number | `1` | Applies or references the 'SoulLink' effect/state. |
| `SpawnBearTrap` | Number | `1` | Applies or references the 'SpawnBearTrap' effect/state. |
| `SpawnRock` | [`Array`](./Arrays.md#array-spawnrock) | `[ 1, .20 ], 1` | Applies or references the 'SpawnRock' effect/state. |
| `Stealth` | Number | `2, 1` | Applies or references the 'Stealth' effect/state. |
| `TempDamageUp` | Number | `2, 1` | Applies or references the 'TempDamageUp' effect/state. |
| `UpgradeRandomAbility` | Number | `1` | Applies or references the 'UpgradeRandomAbility' effect/state. |
| `Webbed` | Number | `1` | Applies or references the 'Webbed' effect/state. |
| `BurgleCoin` | Number | `1, [ 1 .5 ], 3` | Applies or references the 'BurgleCoin' effect/state. |
| `Charge` | Number | `2, 1` | Applies or references the 'Charge' effect/state. |
| `EnableWeather` | [`Enum/String`](./Enums.md#enum-enableweather) | `KaijuFirestorm, KaijuMeteornado, KaijuMeteornadoSolo` | Applies or references the 'EnableWeather' effect/state. |
| `ExplosionIfHitSomething` | Number | `5` | Applies or references the 'ExplosionIfHitSomething' effect/state. |
| `FaceCamera` | Number | `1` | Applies or references the 'FaceCamera' effect/state. |
| `Grappled` | Number | `1` | Applies or references the 'Grappled' effect/state. |
| `HealthGain` | Number | `5, 4` | Applies or references the 'HealthGain' effect/state. |
| `RandomStatDown` | [`Array`](./Arrays.md#array-randomstatdown) | `[ 1 .25 ], 1` | Applies or references the 'RandomStatDown' effect/state. |
| `Reanimate` | Number | `50%, 100%` | Applies or references the 'Reanimate' effect/state. |
| `RemoveActPoints` | Number | `1` | Applies or references the 'RemoveActPoints' effect/state. |
| `SendRock` | Number | `1` | Applies or references the 'SendRock' effect/state. |
| `SpecificInjury` | [`Enum/String`](./Enums.md#enum-specificinjury) | `spd, int, str` | Applies or references the 'SpecificInjury' effect/state. |
| `SwitchMusic` | [`Block`](./Abilities_and_Spells.md#context-switchmusic) | `{ ... }` | Changes the background music track or layer during combat. |
| `UseAbility` | [`Enum/String`](./Enums.md#enum-useability) | `GirlDinoPoop, MD_PoopChain, ManglerThrowRemote` | Forces the character or target to instantly use a specified ability. |
| `VaporizeInanimate` | Number | `1` | Applies or references the 'VaporizeInanimate' effect/state. |
| `CollideWithConsumed` | [`Equation`](./Enums.md#enum-mathequation) | `1+bonus_melee_damage, 5+bonus_melee_damage, 4+bonus_melee_damage` | Applies or references the 'CollideWithConsumed' effect/state. |
| `CorpseVaporizer` | Number | `1` | Applies or references the 'CorpseVaporizer' effect/state. |
| `CurrentWeaponDamageUp` | Number | `1, 3` | Applies or references the 'CurrentWeaponDamageUp' effect/state. |
| `DamageOrHealConditionally` | Number | `1` | Applies or references the 'DamageOrHealConditionally' effect/state. |
| `DeleteObject` | Number | `1` | Applies or references the 'DeleteObject' effect/state. |
| `DestroyTrinket` | Number | `1` | Applies or references the 'DestroyTrinket' effect/state. |
| `DestroyWeapon` | Number | `1` | Applies or references the 'DestroyWeapon' effect/state. |
| `DestroyWeaponThrow` | Number | `1` | Applies or references the 'DestroyWeaponThrow' effect/state. |
| `Die` | Number | `1` | Applies or references the 'Die' effect/state. |
| `DisplaceTowardsSource` | Number | `1` | Applies or references the 'DisplaceTowardsSource' effect/state. |
| `Doomed` | Number | `2, 1, 3` | Applies or references the 'Doomed' effect/state. |
| `DoubleStatus` | [`Enum/String`](./Enums.md#enum-doublestatus) | `Bleed, Poison, Burn` | Applies or references the 'DoubleStatus' effect/state. |
| `ExtraBasicAttacks_Status` | Number | `1` | Applies or references the 'ExtraBasicAttacks_Status' effect/state. |
| `ForceDisplace` | Number | `1` | Applies or references the 'ForceDisplace' effect/state. |
| `ForceMoveTowardsEnemies` | Number | `1, MoveOne, DumbMove_Impl` | Applies or references the 'ForceMoveTowardsEnemies' effect/state. |
| `InstantMaxHealthUp` | Number | `20, 4` | Applies or references the 'InstantMaxHealthUp' effect/state. |
| `KineticSpikes` | Number | `2, 1` | Applies or references the 'KineticSpikes' effect/state. |
| `MoveQuivered` | Number | `1` | Applies or references the 'MoveQuivered' effect/state. |
| `NextAttackBonusRange` | Number | `1, 5, 3` | Applies or references the 'NextAttackBonusRange' effect/state. |
| `OverrideDamage` | Number | `0` | Applies or references the 'OverrideDamage' effect/state. |
| `PermanentConstitution` | Number | `-2, 2, -1` | Applies or references the 'PermanentConstitution' effect/state. |
| `PlayBackground` | Number | `1, 0` | Applies or references the 'PlayBackground' effect/state. |
| `PoisonLace` | String | `"X/5", 1, "X/3"` | Applies or references the 'PoisonLace' effect/state. |
| `PullSourceToTarget` | Number | `1` | Applies or references the 'PullSourceToTarget' effect/state. |
| `Reflect` | Number | `1, 5` | Applies or references the 'Reflect' effect/state. |
| `RefreshWeaponAbility` | Number | `1` | Applies or references the 'RefreshWeaponAbility' effect/state. |
| `RepairAll` | Number | `10, 1` | Applies or references the 'RepairAll' effect/state. |
| `RepairOnKill` | Number | `2, 1` | Applies or references the 'RepairOnKill' effect/state. |
| `ReviveNextRound` | [`Block`](./Abilities_and_Spells.md#context-revivenextround) | `{ ... }, 2` | Queues the character to be resurrected at the start of the next combat round. |
| `SpawnCustomTrap` | [`Enum/String`](./Enums.md#enum-spawncustomtrap) | `SpikeTrap, EggSackTrap, CharmTrap` | Applies or references the 'SpawnCustomTrap' effect/state. |
| `SpawnNeutralWebTrapOnMiss` | Number | `1` | Applies or references the 'SpawnNeutralWebTrapOnMiss' effect/state. |
| `SpellDamageUp` | Number | `1, 3` | Applies or references the 'SpellDamageUp' effect/state. |
| `Tangled` | [`Block`](./Abilities_and_Spells.md#context-tangled) | `{ ... }, 1` | Applies a tangled/ensnared status effect, often modifying visual sprites. |
| `TempSpeedUp` | Number | `10, 4, X` | Applies or references the 'TempSpeedUp' effect/state. |
| `TempStrengthUp` | [`Enum/String`](./Enums.md#enum-tempstrengthup) | `X` | Applies or references the 'TempStrengthUp' effect/state. |
| `VaporizeTarget` | Number | `1` | Applies or references the 'VaporizeTarget' effect/state. |
| `AddSpiritBombCharges` | Number | `2, 1` | Applies or references the 'AddSpiritBombCharges' effect/state. |
| `BonusKnockbackDamage` | Number | `2` | Applies or references the 'BonusKnockbackDamage' effect/state. |
| `Bound` | Number | `3` | Applies or references the 'Bound' effect/state. |
| `CancelPrimedAbilities` | Number | `1` | Applies or references the 'CancelPrimedAbilities' effect/state. |
| `ChangeFaction` | [`Enum/String`](./Enums.md#enum-changefaction) | `sabertooths` | Applies or references the 'ChangeFaction' effect/state. |
| `CharmedForceAttack` | Number | `1` | Applies or references the 'CharmedForceAttack' effect/state. |
| `CollideWithThrowTarget` | Number | `0` | Applies or references the 'CollideWithThrowTarget' effect/state. |
| `Conditional_HealthThreshold` | [`Block`](./Abilities_and_Spells.md#context-conditional_healththreshold) | `{ ... }` | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. |
| `CopySpells` | [`Block`](./Abilities_and_Spells.md#context-copyspells) | `{ ... }, 1` | Duplicates existing spells currently in the character's hand. |
| `Counterspell` | Number | `1` | Applies or references the 'Counterspell' effect/state. |
| `CritChanceUp` | Number | `2` | Applies or references the 'CritChanceUp' effect/state. |
| `DamageBasedOnMissingHealth` | Number | `50, 25` | Applies or references the 'DamageBasedOnMissingHealth' effect/state. |
| `DamageDistanceAOEFalloff` | Number | `2, 1` | Applies or references the 'DamageDistanceAOEFalloff' effect/state. |
| `DamageTrinket` | Number | `1` | Applies or references the 'DamageTrinket' effect/state. |
| `DelayedFury` | Number | `75, 0` | Applies or references the 'DelayedFury' effect/state. |
| `DestroyEquipmentAndAttachParasite` | [`Block`](./Abilities_and_Spells.md#context-destroyequipmentandattachparasite) | `{ ... }` | Removes an equipped item and replaces it with a parasite from a specified pool. |
| `DieViaAbilityInternally` | Number | `1` | Applies or references the 'DieViaAbilityInternally' effect/state. |
| `DiminishingHealthRegen` | Number | `2, 3` | Applies or references the 'DiminishingHealthRegen' effect/state. |
| `DisplaceToOriginalPosition` | Number | `1` | Applies or references the 'DisplaceToOriginalPosition' effect/state. |
| `DoubleCastSpell` | Number | `1` | Applies or references the 'DoubleCastSpell' effect/state. |
| `DoubleLoot` | Number | `2, 1` | Applies or references the 'DoubleLoot' effect/state. |
| `FlowersOnHit` | Number | `1` | Applies or references the 'FlowersOnHit' effect/state. |
| `ForceMoveNonAlliesInRangeTowardsTile` | Number | `4, 3` | Applies or references the 'ForceMoveNonAlliesInRangeTowardsTile' effect/state. |
| `FreeSpell` | Number | `1` | Applies or references the 'FreeSpell' effect/state. |
| `Hex` | Number | `1` | Applies or references the 'Hex' effect/state. |
| `IgnoreDamage` | Number | `1` | Applies or references the 'IgnoreDamage' effect/state. |
| `ImmediateUseAbility` | [`Enum/String`](./Enums.md#enum-immediateuseability) | `cm_Lard_Impl, HitlerCloneTransform` | Applies or references the 'ImmediateUseAbility' effect/state. |
| `ImmediateUseDirectionalAbility` | [`Enum/String`](./Enums.md#enum-immediateusedirectionalability) | `BowlDash2, BowlDash` | Applies or references the 'ImmediateUseDirectionalAbility' effect/state. |
| `JohnnyCriesForWashers` | Number | `2, 1` | Applies or references the 'JohnnyCriesForWashers' effect/state. |
| `KnockOutCoin` | [`Block`](./Abilities_and_Spells.md#context-knockoutcoin) | `{ ... }, 1` | Forces the target to drop coins. |
| `Knockback` | Number | `1, 5` | Applies or references the 'Knockback' effect/state. |
| `LeaveBehindRockOnKnockback` | Number | `1` | Applies or references the 'LeaveBehindRockOnKnockback' effect/state. |
| `Lifesteal` | Number | `1, 3` | Applies or references the 'Lifesteal' effect/state. |
| `ManaLeeches` | Number | `2, 1` | Applies or references the 'ManaLeeches' effect/state. |
| `MaxHPUp` | Number | `100` | Applies or references the 'MaxHPUp' effect/state. |
| `NextAttackSpecialCrit` | [`Block`](./Abilities_and_Spells.md#context-nextattackspecialcrit) | `{ ... }, 1` | Modifies the character's next attack to have special critical properties. |
| `Ostracized` | Number | `2, 4` | Applies or references the 'Ostracized' effect/state. |
| `PartialCleanse` | Number | `9999, 1` | Applies or references the 'PartialCleanse' effect/state. |
| `PermanentStrength` | Number | `2, 1` | Applies or references the 'PermanentStrength' effect/state. |
| `PermanentUpgradeRandomActive` | Number | `1, 4` | Applies or references the 'PermanentUpgradeRandomActive' effect/state. |
| `Possessed` | Number | `1` | Applies or references the 'Possessed' effect/state. |
| `PullSourceToKnockbackImmuneTarget` | Number | `1` | Applies or references the 'PullSourceToKnockbackImmuneTarget' effect/state. |
| `RandomDistanceDisplace` | [`Block`](./Abilities_and_Spells.md#context-randomdistancedisplace) | `{ ... }, 20` | Displaces the target by a randomized distance. |
| `RangeUp` | Number | `1` | Applies or references the 'RangeUp' effect/state. |
| `RebukeDamage` | Number | `2, 1` | Applies or references the 'RebukeDamage' effect/state. |
| `RemoveMovePoints` | Number | `1` | Applies or references the 'RemoveMovePoints' effect/state. |
| `RepairArmorCondition` | Number | `1` | Applies or references the 'RepairArmorCondition' effect/state. |
| `RepairWeapon` | Number | `99, 1` | Applies or references the 'RepairWeapon' effect/state. |
| `RepairWeaponCondition` | Number | `1` | Applies or references the 'RepairWeaponCondition' effect/state. |
| `ResetArmorShield` | Number | `1` | Applies or references the 'ResetArmorShield' effect/state. |
| `ScrambleEverything` | Number | `0, 10%` | Applies or references the 'ScrambleEverything' effect/state. |
| `SelfStun` | Number | `1, [ 1 .5 ]` | Applies or references the 'SelfStun' effect/state. |
| `SetShield` | Number | `0` | Applies or references the 'SetShield' effect/state. |
| `Shatter` | Number | `15` | Applies or references the 'Shatter' effect/state. |
| `SignalFinalBossShieldBroke` | Number | `1` | Applies or references the 'SignalFinalBossShieldBroke' effect/state. |
| `SizeScale` | [`Enum/String`](./Enums.md#enum-sizescale) | `.6` | Applies or references the 'SizeScale' effect/state. |
| `SmartMetronome` | [`Block`](./Abilities_and_Spells.md#context-smartmetronome) | `{ ... }, 20` | Executes a 'smart' random ability that aims to be beneficial based on context. |
| `SpawnCoinAnywhere` | Number | `1, [ 1 .5 ]` | Applies or references the 'SpawnCoinAnywhere' effect/state. |
| `SpawnFlames` | [`Array`](./Arrays.md#array-spawnflames) | `[ 1, .20+.1*level ], [ 1, .20 ]` | Applies or references the 'SpawnFlames' effect/state. |
| `SpeculativeMoveSelfCorpseOffMap` | Number | `1` | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. |
| `StanceSwitchToMelee` | Number | `1` | Applies or references the 'StanceSwitchToMelee' effect/state. |
| `SwallowSmallCharacter` | Number | `50%, 100%` | Applies or references the 'SwallowSmallCharacter' effect/state. |
| `TempCritChanceUp` | Number | `100, 30` | Applies or references the 'TempCritChanceUp' effect/state. |
| `TempDexterityUp` | [`Enum/String`](./Enums.md#enum-tempdexterityup) | `X` | Applies or references the 'TempDexterityUp' effect/state. |
| `TempInitiativeChange` | Number | `9999, 100` | Applies or references the 'TempInitiativeChange' effect/state. |
| `TempMovement` | Number | `20, mov` | Applies or references the 'TempMovement' effect/state. |
| `TempSpellDamageUp` | Number | `1` | Applies or references the 'TempSpellDamageUp' effect/state. |
| `TempTrampleUntilSettled` | Number | `3` | Applies or references the 'TempTrampleUntilSettled' effect/state. |
| `TradeLife` | Number | `1` | Applies or references the 'TradeLife' effect/state. |
| `TrailBlazer` | Number | `1, mov` | Applies or references the 'TrailBlazer' effect/state. |
| `Trample` | Number | `3` | Applies or references the 'Trample' effect/state. |
| `TriggerDOTStatuses` | Number | `1, 0` | Applies or references the 'TriggerDOTStatuses' effect/state. |
| `AIFavorLowHealth` | Number | `100` | Applies or references the 'AIFavorLowHealth' effect/state. |
| `AlliesTakeExtraTurn` | Number | `1` | Applies or references the 'AlliesTakeExtraTurn' effect/state. |
| `AlternateIdleAnimation` | [`Enum/String`](./Enums.md#enum-alternateidleanimation) | `berserkIdle` | Applies or references the 'AlternateIdleAnimation' effect/state. |
| `ApplyShieldToApplierBasedOnMaxHealth` | Number | `1` | Applies or references the 'ApplyShieldToApplierBasedOnMaxHealth' effect/state. |
| `Attraction` | Number | `1` | Applies or references the 'Attraction' effect/state. |
| `Bloodzerked` | Number | `1` | Applies or references the 'Bloodzerked' effect/state. |
| `BombRatTurtle` | Number | `1` | Applies or references the 'BombRatTurtle' effect/state. |
| `BonusDamageBasedOnMana` | Number | `1` | Applies or references the 'BonusDamageBasedOnMana' effect/state. |
| `BypassRockKnockback` | Number | `1` | Applies or references the 'BypassRockKnockback' effect/state. |
| `CanceledQueuedInput` | Number | `1` | Applies or references the 'CanceledQueuedInput' effect/state. |
| `CaptureFamiliar` | Number | `1` | Applies or references the 'CaptureFamiliar' effect/state. |
| `ChampionUpgradeNextMinion` | Number | `1` | Applies or references the 'ChampionUpgradeNextMinion' effect/state. |
| `ChangeTilesUnder` | [`Enum/String`](./Enums.md#enum-changetilesunder) | `DirtTile` | Applies or references the 'ChangeTilesUnder' effect/state. |
| `ChaosBossFlipMidTeleport` | Number | `1` | Applies or references the 'ChaosBossFlipMidTeleport' effect/state. |
| `ChaosBossFormChange` | Number | `1` | Applies or references the 'ChaosBossFormChange' effect/state. |
| `ChargeFists` | Number | `1` | Applies or references the 'ChargeFists' effect/state. |
| `CharmedFacingForceAttack` | Number | `1` | Applies or references the 'CharmedFacingForceAttack' effect/state. |
| `ClearFinalBossBattlefield` | Number | `1` | Applies or references the 'ClearFinalBossBattlefield' effect/state. |
| `CloneWeaponTemp` | Number | `1` | Applies or references the 'CloneWeaponTemp' effect/state. |
| `CoinTossBounce` | [`Enum/String`](./Enums.md#enum-cointossbounce) | `X` | Applies or references the 'CoinTossBounce' effect/state. |
| `Conditional_AbilityTargetIsSelf` | Block | `{ ... }` | Conditional constraint. Nested properties only trigger if this is true. |
| `Conditional_Displaceable` | [`Block`](./Abilities_and_Spells.md#context-conditional_displaceable) | `{ ... }` | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. |
| `ConjureSingleUseBonusAbility` | [`Enum/String`](./Enums.md#enum-conjuresingleusebonusability) | `random` | Applies or references the 'ConjureSingleUseBonusAbility' effect/state. |
| `CreateGlobalModifiers` | [`Block`](./Abilities_and_Spells.md#context-createglobalmodifiers) | `{ ... }` | Generates global map or encounter rules/modifiers. |
| `CurrentWeaponAddElectricElement` | Number | `1` | Applies or references the 'CurrentWeaponAddElectricElement' effect/state. |
| `DamageWeapon` | Number | `1` | Applies or references the 'DamageWeapon' effect/state. |
| `DeathwormUnderground` | [`Enum/String`](./Enums.md#enum-deathwormunderground) | `DeathWormEat` | Applies or references the 'DeathwormUnderground' effect/state. |
| `DecoySwapper` | Number | `1` | Applies or references the 'DecoySwapper' effect/state. |
| `DelayCastAbility` | [`Block`](./Abilities_and_Spells.md#context-delaycastability) | `{ ... }` | Queues an ability to be cast automatically after a certain delay or trigger. |
| `DeleteTraps` | Number | `1` | Applies or references the 'DeleteTraps' effect/state. |
| `DestroyNeckArmor` | Number | `1` | Applies or references the 'DestroyNeckArmor' effect/state. |
| `DieViolently` | Number | `1` | Applies or references the 'DieViolently' effect/state. |
| `DinoLegAnimation` | [`Enum/String`](./Enums.md#enum-dinoleganimation) | `poop` | Applies or references the 'DinoLegAnimation' effect/state. |
| `Disguised` | Number | `1` | Applies or references the 'Disguised' effect/state. |
| `DissolveRandomArmorPiece` | Number | `1` | Applies or references the 'DissolveRandomArmorPiece' effect/state. |
| `DontHealEnemies` | Number | `1` | Applies or references the 'DontHealEnemies' effect/state. |
| `DoubleCast` | Number | `1` | Applies or references the 'DoubleCast' effect/state. |
| `DoubleCastSpellsEachTurn_Status` | Number | `1` | Applies or references the 'DoubleCastSpellsEachTurn_Status' effect/state. |
| `DrainAllyCatsForFleshGolem` | Number | `7` | Applies or references the 'DrainAllyCatsForFleshGolem' effect/state. |
| `DrinkWater` | Number | `1` | Applies or references the 'DrinkWater' effect/state. |
| `DuplicateRandomEquippedItem` | Number | `1` | Applies or references the 'DuplicateRandomEquippedItem' effect/state. |
| `EliteUpgradeNextMinion` | Number | `1` | Applies or references the 'EliteUpgradeNextMinion' effect/state. |
| `EmptyMind` | Number | `1` | Applies or references the 'EmptyMind' effect/state. |
| `Enlarge` | Number | `3` | Applies or references the 'Enlarge' effect/state. |
| `EnterMount` | [`Enum/String`](./Enums.md#enum-entermount) | `enter` | Applies or references the 'EnterMount' effect/state. |
| `ExistUntilIdleUpkeep` | Number | `1` | Applies or references the 'ExistUntilIdleUpkeep' effect/state. |
| `ExplodeCharacter` | Number | `5` | Applies or references the 'ExplodeCharacter' effect/state. |
| `ExplodeCharacter_DeathBloom` | Number | `5` | Applies or references the 'ExplodeCharacter_DeathBloom' effect/state. |
| `ExplodeCharacter_DeathBloom2` | Number | `5` | Applies or references the 'ExplodeCharacter_DeathBloom2' effect/state. |
| `ExplodeCharacter_NoDie` | Number | `1` | Applies or references the 'ExplodeCharacter_NoDie' effect/state. |
| `ExtraBasicMoves_Status` | Number | `1` | Applies or references the 'ExtraBasicMoves_Status' effect/state. |
| `FactionConversion` | Number | `1` | Applies or references the 'FactionConversion' effect/state. |
| `FactionDisguiseSource` | Number | `1` | Applies or references the 'FactionDisguiseSource' effect/state. |
| `FastKnockback` | Number | `4` | Applies or references the 'FastKnockback' effect/state. |
| `FinalBossQueueBeam` | Number | `1` | Applies or references the 'FinalBossQueueBeam' effect/state. |
| `FireArmor` | Number | `1` | Applies or references the 'FireArmor' effect/state. |
| `FireArmor2` | Number | `1` | Applies or references the 'FireArmor2' effect/state. |
| `FlatAIBonus` | Number | `999999` | Applies or references the 'FlatAIBonus' effect/state. |
| `ForceCollectsPickups` | Number | `1` | Applies or references the 'ForceCollectsPickups' effect/state. |
| `ForceMoveAndAttack` | Number | `1` | Applies or references the 'ForceMoveAndAttack' effect/state. |
| `ForceTransferWeapon` | Number | `1` | Applies or references the 'ForceTransferWeapon' effect/state. |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `MotherTumorGrow` | Applies or references the 'ForceUseAbility' effect/state. |
| `GainCoinsRange` | [`Block`](./Abilities_and_Spells.md#context-gaincoinsrange) | `{ ... }` | Grants the player a randomized amount of coins within a min/max range. |
| `GenericBuff` | Number | `100` | Applies or references the 'GenericBuff' effect/state. |
| `GiveBoundItemToTarget` | Number | `1` | Applies or references the 'GiveBoundItemToTarget' effect/state. |
| `GlobalSpawnCharacter` | [`Enum/String`](./Enums.md#enum-globalspawncharacter) | `MegaGuppy` | Applies or references the 'GlobalSpawnCharacter' effect/state. |
| `HealPercentMaxHP` | Number | `100` | Applies or references the 'HealPercentMaxHP' effect/state. |
| `HealRandomInjury` | Number | `1` | Applies or references the 'HealRandomInjury' effect/state. |
| `HealTo` | Number | `50%` | Applies or references the 'HealTo' effect/state. |
| `HeavyHits` | Number | `1` | Applies or references the 'HeavyHits' effect/state. |
| `IceArmor` | Number | `1` | Applies or references the 'IceArmor' effect/state. |
| `IgnoreDebuffs` | Number | `1` | Applies or references the 'IgnoreDebuffs' effect/state. |
| `IncreaseCumulativeBlastDamage` | Number | `1` | Applies or references the 'IncreaseCumulativeBlastDamage' effect/state. |
| `IncreaseItemAuxOnKill` | Number | `1` | Applies or references the 'IncreaseItemAuxOnKill' effect/state. |
| `Infested` | Number | `1` | Applies or references the 'Infested' effect/state. |
| `InterchangeMoveActPoints` | Number | `1` | Applies or references the 'InterchangeMoveActPoints' effect/state. |
| `Invulnerable` | Number | `1` | Applies or references the 'Invulnerable' effect/state. |
| `MadnessChanceOnTurnBegin` | Number | `2` | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. |
| `MakeWeaponUnbreakable` | Number | `1` | Applies or references the 'MakeWeaponUnbreakable' effect/state. |
| `ManaStealToHealth` | Number | `-1` | Applies or references the 'ManaStealToHealth' effect/state. |
| `ManglerAttack` | Number | `1` | Applies or references the 'ManglerAttack' effect/state. |
| `ManglerShuffle` | Boolean | `false` | Applies or references the 'ManglerShuffle' effect/state. |
| `MassAttackThis` | Number | `1` | Applies or references the 'MassAttackThis' effect/state. |
| `Meaty` | Number | `1` | Applies or references the 'Meaty' effect/state. |
| `MimicMetronome` | Number | `1` | Applies or references the 'MimicMetronome' effect/state. |
| `MotherTumorDebugForcePass` | Number | `1` | Applies or references the 'MotherTumorDebugForcePass' effect/state. |
| `Muted` | Number | `1` | Applies or references the 'Muted' effect/state. |
| `NextAbilityHeals` | Number | `1` | Applies or references the 'NextAbilityHeals' effect/state. |
| `NextActionLuckUp` | Number | `99` | Applies or references the 'NextActionLuckUp' effect/state. |
| `NextDamageReduceAndHealAllies` | Number | `1` | Applies or references the 'NextDamageReduceAndHealAllies' effect/state. |
| `NextTurnDoubleRangedDamage` | Number | `1` | Applies or references the 'NextTurnDoubleRangedDamage' effect/state. |
| `NonStackingDivineShield` | Number | `1` | Applies or references the 'NonStackingDivineShield' effect/state. |
| `ObjectOnHitFullyEmpty` | [`Enum/String`](./Enums.md#enum-objectonhitfullyempty) | `RandomArmorPickup` | Applies or references the 'ObjectOnHitFullyEmpty' effect/state. |
| `OverHealToShield` | Number | `1` | Applies or references the 'OverHealToShield' effect/state. |
| `OverrideChainKnockbackDamage` | [`Equation`](./Enums.md#enum-mathequation) | `3+bonus_melee_ability_damage` | Applies or references the 'OverrideChainKnockbackDamage' effect/state. |
| `PermanentCharisma` | Number | `2` | Applies or references the 'PermanentCharisma' effect/state. |
| `PermanentDexterity` | Number | `2` | Applies or references the 'PermanentDexterity' effect/state. |
| `PermanentImmobile` | Number | `1` | Applies or references the 'PermanentImmobile' effect/state. |
| `PermanentIntelligence` | Number | `2` | Applies or references the 'PermanentIntelligence' effect/state. |
| `PermanentLuck` | Number | `2` | Applies or references the 'PermanentLuck' effect/state. |
| `PermanentSpeed` | Number | `2` | Applies or references the 'PermanentSpeed' effect/state. |
| `PermanentUpgradeRandomActiveOrPassive` | Number | `1` | Applies or references the 'PermanentUpgradeRandomActiveOrPassive' effect/state. |
| `ProbeCharmed` | Number | `1` | Applies or references the 'ProbeCharmed' effect/state. |
| `QueueUseAbility` | [`Enum/String`](./Enums.md#enum-queueuseability) | `Spider_GoInsane` | Applies or references the 'QueueUseAbility' effect/state. |
| `RNGCannonRandomDamage` | Number | `100` | Applies or references the 'RNGCannonRandomDamage' effect/state. |
| `RandomKnockbackDirection` | Number | `4` | Applies or references the 'RandomKnockbackDirection' effect/state. |
| `RandomPermanentStat` | Number | `1` | Applies or references the 'RandomPermanentStat' effect/state. |
| `ReduceManaCost` | Number | `1` | Applies or references the 'ReduceManaCost' effect/state. |
| `ReduceManaCostExcludeBrainstorm` | Number | `1` | Applies or references the 'ReduceManaCostExcludeBrainstorm' effect/state. |
| `ReformMoonHead` | Number | `1` | Applies or references the 'ReformMoonHead' effect/state. |
| `RefreshItemAbilities` | Number | `1` | Applies or references the 'RefreshItemAbilities' effect/state. |
| `RefreshNonManaItemAbilities` | Number | `1` | Applies or references the 'RefreshNonManaItemAbilities' effect/state. |
| `RefreshOncePerFightAbilities` | Number | `1` | Applies or references the 'RefreshOncePerFightAbilities' effect/state. |
| `Regurge` | Number | `1` | Applies or references the 'Regurge' effect/state. |
| `RepairAllCondition` | Number | `1` | Applies or references the 'RepairAllCondition' effect/state. |
| `RerollEnemy` | Number | `1` | Applies or references the 'RerollEnemy' effect/state. |
| `ReturnDinoLegs` | Number | `1` | Applies or references the 'ReturnDinoLegs' effect/state. |
| `ScatterRandomPickups` | Number | `2` | Applies or references the 'ScatterRandomPickups' effect/state. |
| `SetDefaultFace` | [`Enum/String`](./Enums.md#enum-setdefaultface) | `insane` | Applies or references the 'SetDefaultFace' effect/state. |
| `ShadowCrit` | Number | `1` | Applies or references the 'ShadowCrit' effect/state. |
| `ShootHereCommand` | Number | `1` | Applies or references the 'ShootHereCommand' effect/state. |
| `ShootHereReceiver` | Number | `1` | Applies or references the 'ShootHereReceiver' effect/state. |
| `ShortCircuit` | Number | `1` | Applies or references the 'ShortCircuit' effect/state. |
| `SmallHitExplosion` | Number | `1` | Applies or references the 'SmallHitExplosion' effect/state. |
| `SmellBlood` | Number | `1` | Applies or references the 'SmellBlood' effect/state. |
| `SoundEventOnHit` | [`Enum/String`](./Enums.md#enum-soundeventonhit) | `Batterup_Connect` | Applies or references the 'SoundEventOnHit' effect/state. |
| `SourceSwapsBackEndOfTurn` | [`Enum/String`](./Enums.md#enum-sourceswapsbackendofturn) | `ThiefSwapBack` | Applies or references the 'SourceSwapsBackEndOfTurn' effect/state. |
| `SpawnWebTrap` | Number | `1` | Applies or references the 'SpawnWebTrap' effect/state. |
| `SpecialBossMultipartInstakill` | [`Enum/String`](./Enums.md#enum-specialbossmultipartinstakill) | `moonboss` | Applies or references the 'SpecialBossMultipartInstakill' effect/state. |
| `SpellShield` | Number | `1` | Applies or references the 'SpellShield' effect/state. |
| `SpitConsumed` | Number | `1` | Applies or references the 'SpitConsumed' effect/state. |
| `SplashDamage` | Number | `1` | Applies or references the 'SplashDamage' effect/state. |
| `StackingSandstorm` | Number | `1` | Applies or references the 'StackingSandstorm' effect/state. |
| `StatBounty` | Number | `1` | Applies or references the 'StatBounty' effect/state. |
| `StealDemonicGlyph` | Number | `1` | Applies or references the 'StealDemonicGlyph' effect/state. |
| `StealEquipment` | [`Enum/String`](./Enums.md#enum-stealequipment) | `any` | Applies or references the 'StealEquipment' effect/state. |
| `StealTurn` | Number | `1` | Applies or references the 'StealTurn' effect/state. |
| `StealthCritChance` | Number | `100` | Applies or references the 'StealthCritChance' effect/state. |
| `SwapHighestAndLowestStat` | Number | `1` | Applies or references the 'SwapHighestAndLowestStat' effect/state. |
| `Switcheroo` | Number | `1` | Applies or references the 'Switcheroo' effect/state. |
| `T3HitlerTriggerInitialSpawns` | Number | `1` | Applies or references the 'T3HitlerTriggerInitialSpawns' effect/state. |
| `TagMetronome` | [`Enum/String`](./Enums.md#enum-tagmetronome) | `musical` | Applies or references the 'TagMetronome' effect/state. |
| `TakeExtraTurnEndOfRound` | Number | `1` | Applies or references the 'TakeExtraTurnEndOfRound' effect/state. |
| `TargetedMetronome` | Number | `20` | Applies or references the 'TargetedMetronome' effect/state. |
| `Taunting` | Number | `1` | Applies or references the 'Taunting' effect/state. |
| `TeamBonusAbility` | [`Enum/String`](./Enums.md#enum-teambonusability) | `ShootHere` | Applies or references the 'TeamBonusAbility' effect/state. |
| `TeleportBackAtTurnEnd` | [`Enum/String`](./Enums.md#enum-teleportbackatturnend) | `FlashBack` | Applies or references the 'TeleportBackAtTurnEnd' effect/state. |
| `TempBackstab` | Number | `75` | Applies or references the 'TempBackstab' effect/state. |
| `TempBackstabBleed` | Number | `1` | Applies or references the 'TempBackstabBleed' effect/state. |
| `TempBackstabPiercing` | Number | `1` | Applies or references the 'TempBackstabPiercing' effect/state. |
| `TempBackstabPoison` | Number | `1` | Applies or references the 'TempBackstabPoison' effect/state. |
| `TempBasicAttackBonusAOE` | Number | `1` | Applies or references the 'TempBasicAttackBonusAOE' effect/state. |
| `TempBonusKnockback` | Number | `1` | Applies or references the 'TempBonusKnockback' effect/state. |
| `TempBonusKnockbackDamage` | Number | `1` | Applies or references the 'TempBonusKnockbackDamage' effect/state. |
| `TempCounterAttack` | Number | `1` | Applies or references the 'TempCounterAttack' effect/state. |
| `TempInjuryImmunity` | Number | `1` | Applies or references the 'TempInjuryImmunity' effect/state. |
| `TempLuckUp` | Number | `99` | Applies or references the 'TempLuckUp' effect/state. |
| `TempManaCostReduction` | Number | `1` | Applies or references the 'TempManaCostReduction' effect/state. |
| `TempPenetrate` | Number | `1` | Applies or references the 'TempPenetrate' effect/state. |
| `TempPreEmptiveCounterAttack` | Number | `1` | Applies or references the 'TempPreEmptiveCounterAttack' effect/state. |
| `ThornsDamageImmuneUntilSettled` | Number | `1` | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. |
| `TickDownStatus` | [`Enum/String`](./Enums.md#enum-tickdownstatus) | `ShortCircuit` | Applies or references the 'TickDownStatus' effect/state. |
| `TileDamageImmuneUntilSettled` | Number | `1` | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. |
| `TilesMovedToCritChance` | Number | `1` | Applies or references the 'TilesMovedToCritChance' effect/state. |
| `TilesMovedToMana` | Number | `1` | Applies or references the 'TilesMovedToMana' effect/state. |
| `TilesMovedToNeighborHeal` | [`Enum/String`](./Enums.md#enum-tilesmovedtoneighborheal) | `level` | Applies or references the 'TilesMovedToNeighborHeal' effect/state. |
| `TilesMovedToStrength` | Number | `1` | Applies or references the 'TilesMovedToStrength' effect/state. |
| `TowerDefenseStatus` | Number | `1` | Applies or references the 'TowerDefenseStatus' effect/state. |
| `TowerDefenseStatus2` | Number | `1` | Applies or references the 'TowerDefenseStatus2' effect/state. |
| `TransformBasicMove` | [`Enum/String`](./Enums.md#enum-transformbasicmove) | `BasicDashAttackMove_NoKnockback` | Applies or references the 'TransformBasicMove' effect/state. |
| `TransformNow` | [`Enum/String`](./Enums.md#enum-transformnow) | `Hitler` | Applies or references the 'TransformNow' effect/state. |
| `Trapper_Status` | Number | `1` | Applies or references the 'Trapper_Status' effect/state. |
| `TriggerGameEnding` | Number | `1` | Applies or references the 'TriggerGameEnding' effect/state. |
| `TriggerMotherConsume` | Number | `1` | Applies or references the 'TriggerMotherConsume' effect/state. |
| `TriggerMotherGrow` | Number | `4` | Applies or references the 'TriggerMotherGrow' effect/state. |
| `TurnAround` | Number | `1` | Applies or references the 'TurnAround' effect/state. |
| `TurnControlDelay` | [`Enum/String`](./Enums.md#enum-turncontroldelay) | `.25` | Applies or references the 'TurnControlDelay' effect/state. |
| `TurnRight` | Number | `1` | Applies or references the 'TurnRight' effect/state. |
| `UndoDamage` | Number | `1` | Applies or references the 'UndoDamage' effect/state. |
| `VaporizeCorpseFlipAdvantage` | [`Array`](./Arrays.md#array-vaporizecorpseflipadvantage) | `[ 1 .33 ]` | Applies or references the 'VaporizeCorpseFlipAdvantage' effect/state. |
| `VaporizeDice` | Number | `1` | Applies or references the 'VaporizeDice' effect/state. |

</details>

---

### Context: `spawn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `RANDOM_1X1_ENEMY, Food, PlayerCat_ThiefShade` |  |
| `faction` | [`Enum/String`](./Enums.md#enum-faction) | `solitary_enemies, self, default` |  |
| `ai_base_score` | Number | `99999, 9999, 999999` |  |
| `first_turn` | [`Enum/String`](./Enums.md#enum-first_turn) | `next_turn, end_of_round, initiative` |  |
| `layer` | [`Enum/String`](./Enums.md#enum-layer) | `pickups, characters, gas` |  |
| `catdata` | [`Enum/String`](./Enums.md#enum-catdata) | `item_aux_catid, clone, teamclone` | Defines genetic/clone data cloning. |
| `clone_items` | Boolean | `true` | If true, transfers inventory to the clone. |
| `lob` | Boolean | `false` |  |
| `size` | Number | `2` |  |
| `face_camera` | Boolean | `true` |  |
| `inherit_elite_buffs` | Boolean | `false` |  |
| `start_dead` | Boolean | `true` |  |
| `appearance` | [`Enum/String`](./Enums.md#enum-appearance) | `GolemCat` |  |
| `auto_cast_on_spawn` | [`Enum/String`](./Enums.md#enum-auto_cast_on_spawn) | `Dash_Enemy` |  |
| `chapter` | [`Enum/String`](./Enums.md#enum-chapter) | `alley` |  |
| `custom_additional_ai_weight` | [`Enum/String`](./Enums.md#enum-custom_additional_ai_weight) | `tile_exists` |  |
| `include_passives` | Boolean | `true` |  |
| `redirect_location_if_blocked` | Boolean | `true` |  |
| `spawnin_animation` | [`Enum/String`](./Enums.md#enum-spawnin_animation) | `summonspawnin` |  |
| `trigger_battle_start` | Boolean | `true` |  |

</details>

---

### Context: `Temporary`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `10, 1, 5` | Number of stacks or intensity to apply. |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Brace, Thorns, AllDamageImmune` | The status effect to apply. |
| `turns` | Number | `1, 3` | Duration in turns. |
| `expires_on_begin_turn` | Boolean | `true` | If true, ticks down at the start of the turn rather than the end. |
| `expires_on_end_turn` | Boolean | `true` |  |
| `data` | Number | `2` |  |
| `expires_on_appliers_turn` | Boolean | `true` |  |
| `expires_on_move` | Boolean | `true` |  |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `GainCoins` | Number | `-5, 1, 5` | Applies or references the 'GainCoins' effect/state. |
| `Shield` | Number | `2, 1, 4` | Applies or references the 'Shield' effect/state. |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |
| `Slow` | Number | `2, 1` | Applies or references the 'Slow' effect/state. |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `Thorns` | Number | `2, 1` | Applies or references the 'Thorns' effect/state. |
| `BonusDamage` | Number | `-5, -4, "ceil(X/2)"` | Applies or references the 'BonusDamage' effect/state. |
| `Charge` | Number | `8, 1, 4` | Applies or references the 'Charge' effect/state. |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `KineticSpikes` | Number | `1` | Applies or references the 'KineticSpikes' effect/state. |
| `RandomStatUp` | Number | `1` | Applies or references the 'RandomStatUp' effect/state. |
| `SpeedUp` | Number | `1` | Applies or references the 'SpeedUp' effect/state. |
| `Brace` | Number | `1` | Applies or references the 'Brace' effect/state. |
| `Bruise` | Number | `2, 1` | Applies or references the 'Bruise' effect/state. |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `MoveQuivered` | Number | `1` | Applies or references the 'MoveQuivered' effect/state. |
| `Quivered` | Number | `1` | Applies or references the 'Quivered' effect/state. |
| `Weakness` | Number | `2, 1` | Applies or references the 'Weakness' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `BackflipWhenTargeted` | Number | `1` | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |
| `BleedThorns` | Number | `1` | Applies or references the 'BleedThorns' effect/state. |
| `CharismaUp` | Number | `1` | Applies or references the 'CharismaUp' effect/state. |
| `CritChanceUp` | Number | `1` | Applies or references the 'CritChanceUp' effect/state. |
| `DexterityUp` | Number | `1` | Applies or references the 'DexterityUp' effect/state. |
| `DiminishingHealthRegen` | Number | `1` | Applies or references the 'DiminishingHealthRegen' effect/state. |
| `DodgeChance_Status` | Number | `1` | Applies or references the 'DodgeChance_Status' effect/state. |
| `HealthRegenUp` | Number | `1` | Applies or references the 'HealthRegenUp' effect/state. |
| `IntelligenceUp` | Number | `1` | Applies or references the 'IntelligenceUp' effect/state. |
| `Lifesteal` | Number | `1` | Applies or references the 'Lifesteal' effect/state. |
| `LuckUp` | Number | `1` | Applies or references the 'LuckUp' effect/state. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `MagicWeakness` | Number | `2, 1` | Applies or references the 'MagicWeakness' effect/state. |
| `ManaGain` | [`Equation`](./Enums.md#enum-mathequation) | `"-ceil(X/2)", X` | Applies or references the 'ManaGain' effect/state. |
| `Marked` | Number | `1` | Applies or references the 'Marked' effect/state. |
| `PoisonLace` | Number | `1` | Applies or references the 'PoisonLace' effect/state. |
| `Reflect` | Number | `1` | Applies or references the 'Reflect' effect/state. |
| `Rot` | Number | `1` | Applies or references the 'Rot' effect/state. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `Tarred` | Number | `1` | Applies or references the 'Tarred' effect/state. |
| `TempCounterAttack` | Number | `1` | Applies or references the 'TempCounterAttack' effect/state. |
| `Blind` | Number | `1` | Applies or references the 'Blind' effect/state. |
| `Burn` | Number | `1` | Applies or references the 'Burn' effect/state. |
| `Charmed` | Number | `1` | Applies or references the 'Charmed' effect/state. |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |
| `DelayedPain` | Number | `1` | Applies or references the 'DelayedPain' effect/state. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `Freeze` | Number | `1` | Applies or references the 'Freeze' effect/state. |
| `Hex` | Number | `1` | Applies or references the 'Hex' effect/state. |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |
| `Infested` | Number | `1` | Applies or references the 'Infested' effect/state. |
| `Ostracized` | Number | `1` | Applies or references the 'Ostracized' effect/state. |
| `Petrify` | Number | `1` | Applies or references the 'Petrify' effect/state. |
| `RandomStatDown` | Number | `1` | Applies or references the 'RandomStatDown' effect/state. |
| `RefreshActPoints` | Number | `1` | Applies or references the 'RefreshActPoints' effect/state. |
| `RefreshMovePoints` | Number | `1` | Applies or references the 'RefreshMovePoints' effect/state. |
| `Scrambled` | Number | `2` | Applies or references the 'Scrambled' effect/state. |
| `Sleep` | Number | `1` | Applies or references the 'Sleep' effect/state. |
| `SpellDamageUp` | Number | `1` | Applies or references the 'SpellDamageUp' effect/state. |

</details>

---

### Context: `bonus_passives`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DeadAltAbility` | [`Enum/String`](./Enums.md#enum-deadaltability) | `LifeDrain_Afterlife, CarrionShot_Afterlife2, CarrionShot_Afterlife` | Applies or references the 'DeadAltAbility' effect/state. |
| `AbilityEnabledOncePerFightAtHealthThreshold` | Number | `16, 25%, 50%` | Applies or references the 'AbilityEnabledOncePerFightAtHealthThreshold' effect/state. |
| `XIsFreeArmorSlots` | Number | `1` | Applies or references the 'XIsFreeArmorSlots' effect/state. |
| `AbilityEnabledPercentEachTurn` | Number | `25%, 50%, 35%` | Applies or references the 'AbilityEnabledPercentEachTurn' effect/state. |
| `FreeFirstCast` | Number | `1, 4` | Applies or references the 'FreeFirstCast' effect/state. |
| `XIsLivingAlliesWithTag` | [`Enum/String`](./Enums.md#enum-xislivingallieswithtag) | `dc_crow, hitler_clone_fetus, terminator_mini` | Applies or references the 'XIsLivingAlliesWithTag' effect/state. |
| `CatchBoomerang` | Number | `1` | Applies or references the 'CatchBoomerang' effect/state. |
| `CopyBasicAttackEffects` | Number | `1` | Applies or references the 'CopyBasicAttackEffects' effect/state. |
| `DownRankAIIfWeaponUsable` | [`Enum/String`](./Enums.md#enum-downrankaiifweaponusable) | `.001` | Applies or references the 'DownRankAIIfWeaponUsable' effect/state. |
| `AbilityEnableIfConsumedCharacterHasTag` | [`Enum/String`](./Enums.md#enum-abilityenableifconsumedcharacterhastag) | `sp_pill_fire, sp_pill_tar, sp_pill_normal` | Applies or references the 'AbilityEnableIfConsumedCharacterHasTag' effect/state. |
| `AbilityEnabledOncePerRound` | Number | `1` | Applies or references the 'AbilityEnabledOncePerRound' effect/state. |
| `AbilityInheritsWeaponEffects` | Number | `2, 1` | Applies or references the 'AbilityInheritsWeaponEffects' effect/state. |
| `MoonHeadFinisherEnabler` | Number | `1, 0, -1` | Applies or references the 'MoonHeadFinisherEnabler' effect/state. |
| `XIsMultipliedPercentHealth` | [`Array`](./Arrays.md#array-xismultipliedpercenthealth) | `[ 6 2 ], [ 1 12 ], [ 14 1 ]` | Applies or references the 'XIsMultipliedPercentHealth' effect/state. |
| `AbilityEnabledIfHasStatus` | [`Enum/String`](./Enums.md#enum-abilityenabledifhasstatus) | `DemonicGlyph_Summon, DemonicGlyph_Bite` | Applies or references the 'AbilityEnabledIfHasStatus' effect/state. |
| `ChargeSpiritBombAura` | [`Enum/String`](./Enums.md#enum-chargespiritbombaura) | `DonateEnergy, DonateEnergy2` | Applies or references the 'ChargeSpiritBombAura' effect/state. |
| `CopyCatPassive_Initializer` | Number | `2, 1` | Applies or references the 'CopyCatPassive_Initializer' effect/state. |
| `ReloadOnKill` | Number | `1` | Applies or references the 'ReloadOnKill' effect/state. |
| `ReloadOnKillEnemy` | Number | `1` | Applies or references the 'ReloadOnKillEnemy' effect/state. |
| `ReloadOnTotalDamageReceived` | Number | `25, 15` | Applies or references the 'ReloadOnTotalDamageReceived' effect/state. |
| `XIsLivingCharactersWithTag` | [`Enum/String`](./Enums.md#enum-xislivingcharacterswithtag) | `rock, husk` | Applies or references the 'XIsLivingCharactersWithTag' effect/state. |
| `XIsOtherHealsThisTurn` | Number | `1` | Applies or references the 'XIsOtherHealsThisTurn' effect/state. |
| `XIsSpellStormRampAndReset` | [`Block`](./Abilities_and_Spells.md#context-xisspellstormrampandreset) | `{ ... }, 0` | Math variable assignment: Evaluates X based on Spell Storm stacks, then resets them. |
| `XIsTimesDamageTaken` | Number | `1` | Applies or references the 'XIsTimesDamageTaken' effect/state. |
| `AbilityDisableIfLivingCrow` | Number | `1` | Applies or references the 'AbilityDisableIfLivingCrow' effect/state. |
| `AbilityEnabledAtHealthThreshold` | Number | `50%` | Applies or references the 'AbilityEnabledAtHealthThreshold' effect/state. |
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Number | `1` | Applies or references the 'AbilityEnabledIfBasicAttackUsedThisTurn' effect/state. |
| `AbilityEnabledIfMovementTrapped` | Number | `1` | Applies or references the 'AbilityEnabledIfMovementTrapped' effect/state. |
| `AbilityEnabledIfNoAggroTarget` | Number | `1` | Applies or references the 'AbilityEnabledIfNoAggroTarget' effect/state. |
| `AbilityEnabledIfNotHasStatus` | [`Enum/String`](./Enums.md#enum-abilityenabledifnothasstatus) | `BackflipWhenTargeted` | Applies or references the 'AbilityEnabledIfNotHasStatus' effect/state. |
| `AbilityEnabledIfSpecificItemEquipped` | [`Enum/String`](./Enums.md#enum-abilityenabledifspecificitemequipped) | `Neverstone` | Applies or references the 'AbilityEnabledIfSpecificItemEquipped' effect/state. |
| `AbsorbManaFromOtherSpells` | Number | `1` | Applies or references the 'AbsorbManaFromOtherSpells' effect/state. |
| `AddElementsToSpells` | [`Enum/String`](./Enums.md#enum-addelementstospells) | `Earth` | Applies or references the 'AddElementsToSpells' effect/state. |
| `AddStatusToBasicAttack` | [`Block`](./Abilities_and_Spells.md#context-addstatustobasicattack) | `{ ... }` | Injects a status effect payload that applies whenever the character performs a basic attack. |
| `AlphaDodgeChance` | Number | `50%` | Applies or references the 'AlphaDodgeChance' effect/state. |
| `BonusAbility_DelayedApplication` | [`Enum/String`](./Enums.md#enum-bonusability_delayedapplication) | `Slap` | Applies or references the 'BonusAbility_DelayedApplication' effect/state. |
| `CapTechSpent` | Number | `1` | Applies or references the 'CapTechSpent' effect/state. |
| `CaveWomanBirthControl` | Number | `1` | Applies or references the 'CaveWomanBirthControl' effect/state. |
| `CritChanceUp` | Number | `25` | Applies or references the 'CritChanceUp' effect/state. |
| `FistOfFateUniqueEnemyTracker` | Number | `1` | Applies or references the 'FistOfFateUniqueEnemyTracker' effect/state. |
| `FreeFirstCastAndAfterSpendMana` | Number | `1` | Applies or references the 'FreeFirstCastAndAfterSpendMana' effect/state. |
| `FreeFirstCastEachMatch` | Number | `1` | Applies or references the 'FreeFirstCastEachMatch' effect/state. |
| `HealthRegenUp` | Number | `3` | Applies or references the 'HealthRegenUp' effect/state. |
| `IgnoreTiles` | Number | `1` | Applies or references the 'IgnoreTiles' effect/state. |
| `IntelligenceUp` | Number | `2` | Applies or references the 'IntelligenceUp' effect/state. |
| `InterchangeDisabler` | Number | `1` | Applies or references the 'InterchangeDisabler' effect/state. |
| `KnockbackImmunity` | Number | `1` | Applies or references the 'KnockbackImmunity' effect/state. |
| `ReloadOnAllyCatDies` | Number | `1` | Applies or references the 'ReloadOnAllyCatDies' effect/state. |
| `ReloadOnAllyDies` | Number | `1` | Applies or references the 'ReloadOnAllyDies' effect/state. |
| `ReloadOnAnyDamage` | Number | `1` | Applies or references the 'ReloadOnAnyDamage' effect/state. |
| `ReloadOnBackstab` | Number | `1` | Applies or references the 'ReloadOnBackstab' effect/state. |
| `ReloadOnElementalDamageReceived` | [`Enum/String`](./Enums.md#enum-reloadonelementaldamagereceived) | `Holy` | Applies or references the 'ReloadOnElementalDamageReceived' effect/state. |
| `ReloadOnGainCoins` | Number | `1` | Applies or references the 'ReloadOnGainCoins' effect/state. |
| `ReloadOnGainDivineShield` | Number | `1` | Applies or references the 'ReloadOnGainDivineShield' effect/state. |
| `ReloadOnKillTagged` | [`Enum/String`](./Enums.md#enum-reloadonkilltagged) | `rock` | Applies or references the 'ReloadOnKillTagged' effect/state. |
| `ReloadOnSpendMana` | Number | `1` | Applies or references the 'ReloadOnSpendMana' effect/state. |
| `ReloadOnUseAbilityWithManaCost` | Number | `6` | Applies or references the 'ReloadOnUseAbilityWithManaCost' effect/state. |
| `TossTargetIsAggroTarget` | Number | `1` | Applies or references the 'TossTargetIsAggroTarget' effect/state. |
| `TossTargetIsBuddy` | Number | `1` | Applies or references the 'TossTargetIsBuddy' effect/state. |
| `TossTargetIsNotInWater` | Number | `1` | Applies or references the 'TossTargetIsNotInWater' effect/state. |
| `Trample` | Number | `3` | Applies or references the 'Trample' effect/state. |
| `XIsConsumedCharacterMaxHP` | Number | `3` | Applies or references the 'XIsConsumedCharacterMaxHP' effect/state. |
| `XIsCountDeaths` | Number | `1` | Applies or references the 'XIsCountDeaths' effect/state. |
| `XIsCountStatusStacks` | [`Enum/String`](./Enums.md#enum-xiscountstatusstacks) | `DodgeChance_Status` | Applies or references the 'XIsCountStatusStacks' effect/state. |
| `XIsFormulaLockedUntilComplete` | [`Enum/String`](./Enums.md#enum-xisformulalockeduntilcomplete) | `dex` | Applies or references the 'XIsFormulaLockedUntilComplete' effect/state. |
| `XIsIncreaseEachTurn` | Number | `1` | Applies or references the 'XIsIncreaseEachTurn' effect/state. |
| `XIsRampAndReset` | Number | `0` | Applies or references the 'XIsRampAndReset' effect/state. |
| `XIsRecycleCostReduction` | Number | `5` | Applies or references the 'XIsRecycleCostReduction' effect/state. |

</details>

---

### Context: `self_damage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `2, 0, "floor(X*.25)"` | The base damage properties of an attack. |
| `piercing` | Boolean | `true` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell, melee, none` | Classification/category type. |
| `cant_miss` | Boolean | `true` |  |
| `knockback` | Number | `-10, 1, -3` |  |
| `heal` | Number | `8, 25, 4` |  |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Explosion ], [ Water ], [ Fire ]` |  |
| `ai_base_score` | Number | `9999` |  |
| `non_lethal` | Boolean | `true` |  |

</details>

---

### Context: `Else`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object), [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `GainDisorderFromPool_PostCast` | [`Enum/String`](./Enums.md#enum-gaindisorderfrompool_postcast) | `forbidden_spell_consequences_crippling` | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. |
| `BonusDamage` | [`Equation`](./Enums.md#enum-mathequation) | `20+bonus_melee_damage, 1, 5` | Applies or references the 'BonusDamage' effect/state. |
| `ApplyToSource` | [`Block`](./Abilities_and_Spells.md#context-applytosource) | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `CanApplyToInanimate` | [`Block`](./Abilities_and_Spells.md#context-canapplytoinanimate) | `{ ... }` | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. |
| `Vaporize` | Number | `1, 20` | Applies or references the 'Vaporize' effect/state. |
| `Cleanse` | Number | `0` | Applies or references the 'Cleanse' effect/state. |
| `Conditional_HasStatus` | [`Block`](./Abilities_and_Spells.md#context-conditional_hasstatus) | `{ ... }` | Conditional trigger: Executes nested logic if the target currently has the specified status effect. |
| `Confusion` | Number | `2, 1` | Applies or references the 'Confusion' effect/state. |
| `FormChange` | [`Block`](./Abilities_and_Spells.md#context-formchange) | `Nuke, LastHit` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `FullHeal` | Number | `0, 1` | Applies or references the 'FullHeal' effect/state. |
| `GainCoinsRange` | [`Block`](./Abilities_and_Spells.md#context-gaincoinsrange) | `{ ... }` | Grants the player a randomized amount of coins within a min/max range. |
| `RandomStatDown` | [`Equation`](./Enums.md#enum-mathequation) | `"ceil(X/3)", "ceil(X/2)"` | Applies or references the 'RandomStatDown' effect/state. |
| `RandomStatUp` | Number | `2, 1` | Applies or references the 'RandomStatUp' effect/state. |
| `Revive` | Number | `1, 100%` | Applies or references the 'Revive' effect/state. |
| `SpawnBearTrapIfHitKills` | Number | `1` | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. |
| `SpawnThingIfHitKills` | [`Enum/String`](./Enums.md#enum-spawnthingifhitkills) | `Bait` | Applies or references the 'SpawnThingIfHitKills' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `ApplyToRandomPartyMemberIfPossible` | [`Block`](./Abilities_and_Spells.md#context-applytorandompartymemberifpossible) | `{ ... }` | Redirects the nested effects to apply to a random living member of the player's party. |
| `Bruise` | Number | `4` | Applies or references the 'Bruise' effect/state. |
| `CatPartsTransform` | [`Block`](./Abilities_and_Spells.md#context-catpartstransform) | `{ ... }` | Transforms specific body parts into different visual variants. |
| `Charmed` | Number | `2` | Applies or references the 'Charmed' effect/state. |
| `Cleave` | Number | `1` | Causes the attack to hit adjacent enemies alongside the primary target. |
| `Conditional_Displaceable` | [`Block`](./Abilities_and_Spells.md#context-conditional_displaceable) | `{ ... }` | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. |
| `Conditional_GoodRoll` | [`Block`](./Abilities_and_Spells.md#context-conditional_goodroll) | `{ ... }` | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. |
| `Conditional_HasTag` | [`Block`](./Abilities_and_Spells.md#context-conditional_hastag) | `{ ... }` | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. |
| `Conditional_HealthThreshold` | [`Block`](./Abilities_and_Spells.md#context-conditional_healththreshold) | `{ ... }` | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. |
| `Conditional_Object` | [`Block`](./Abilities_and_Spells.md#context-conditional_object) | `{ ... }` | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. |
| `Conditional_Speculative` | [`Block`](./Abilities_and_Spells.md#context-conditional_speculative) | `{ ... }` | A simulation block used by the AI to test hypothetical outcomes before committing to an action. |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `Consumed` | [`Block`](./Abilities_and_Spells.md#context-consumed) | `{ ... }` | State block triggered when this object or entity is eaten/consumed by another character. |
| `CritChanceUp` | Number | `5` | Applies or references the 'CritChanceUp' effect/state. |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `DestroyEquipmentAndAttachParasite` | [`Block`](./Abilities_and_Spells.md#context-destroyequipmentandattachparasite) | `{ ... }` | Removes an equipped item and replaces it with a parasite from a specified pool. |
| `DieViolently` | Number | `1` | Applies or references the 'DieViolently' effect/state. |
| `DoDamage` | [`Block`](./Abilities_and_Spells.md#context-dodamage) | `{ ... }` | Explicitly triggers a secondary damage instance independent of the main attack. |
| `DodgeChance_Status` | Number | `5` | Applies or references the 'DodgeChance_Status' effect/state. |
| `DybbukPossessed` | [`Block`](./Abilities_and_Spells.md#context-dybbukpossessed) | `{ ... }` | Defines the abilities and behaviors available when possessing another entity. |
| `Else` | [`Block`](./Abilities_and_Spells.md#context-else) | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `ExplodeCharacter` | Number | `5` | Applies or references the 'ExplodeCharacter' effect/state. |
| `ExplodeCharacter_Party` | Number | `5` | Applies or references the 'ExplodeCharacter_Party' effect/state. |
| `FaceCamera` | Number | `1` | Applies or references the 'FaceCamera' effect/state. |
| `FlatAIBonus` | Number | `-999999` | Applies or references the 'FlatAIBonus' effect/state. |
| `ForceImmediateMove` | Number | `1` | Applies or references the 'ForceImmediateMove' effect/state. |
| `GenericDebuff` | Number | `100` | Applies or references the 'GenericDebuff' effect/state. |
| `ImmediateUseAbility` | [`Enum/String`](./Enums.md#enum-immediateuseability) | `tk_ButterBean_Normal` | Applies or references the 'ImmediateUseAbility' effect/state. |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |
| `Instakill` | Number | `25` | Applies or references the 'Instakill' effect/state. |
| `KnockUpAndAway` | [`Block`](./Abilities_and_Spells.md#context-knockupandaway) | `{ ... }` | Displaces the target vertically and horizontally away from the source. |
| `Leeches` | Number | `2` | Applies or references the 'Leeches' effect/state. |
| `ObjectOnHitCharacter` | [`Enum/String`](./Enums.md#enum-objectonhitcharacter) | `Maggot` | Spawns a specific character or entity upon impact. |
| `OverrideDamage` | Number | `0` | Applies or references the 'OverrideDamage' effect/state. |
| `PartialCleanse` | Number | `1` | Applies or references the 'PartialCleanse' effect/state. |
| `PurgeAll` | Number | `1` | Applies or references the 'PurgeAll' effect/state. |
| `RandomStatusFromPool` | [`Block`](./Abilities_and_Spells.md#context-randomstatusfrompool) | `{ ... }` | Selects and applies a random status effect from the provided nested block. |
| `RemoveMovePoints` | Number | `1` | Applies or references the 'RemoveMovePoints' effect/state. |
| `RemoveTurnsThisRound` | Number | `1` | Applies or references the 'RemoveTurnsThisRound' effect/state. |
| `ScatterCoins` | [`Block`](./Abilities_and_Spells.md#context-scattercoins) | `{ ... }` | Throws coins out into the level randomly. |
| `SetHealth` | Number | `1` | Applies or references the 'SetHealth' effect/state. |
| `SetShield` | Number | `88` | Applies or references the 'SetShield' effect/state. |
| `ShowFakeDamage` | [`Block`](./Abilities_and_Spells.md#context-showfakedamage) | `{ ... }` | Displays a visual damage number without actually modifying health. |
| `Slow` | Number | `1` | Applies or references the 'Slow' effect/state. |
| `SpeculativeMoveSelfCorpseOffMap` | Number | `1` | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. |
| `SpeedUp` | Number | `1` | Applies or references the 'SpeedUp' effect/state. |
| `Temporary` | [`Block`](./Abilities_and_Spells.md#context-temporary) | `{ ... }` | A wrapper block for applying status effects that automatically expire. |
| `VaporizeInanimate` | Number | `1` | Applies or references the 'VaporizeInanimate' effect/state. |
| `XIsTargetHealth` | [`Block`](./Abilities_and_Spells.md#context-xistargethealth) | `{ ... }` | Math variable assignment: Evaluates X as the target's current health. |

</details>

---

### Context: `temporary_effects`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Trample` | Number | `4, 1, 3` | Applies or references the 'Trample' effect/state. |
| `CastAgain` | Number | `2, 1, 4` | Applies or references the 'CastAgain' effect/state. |
| `DisableTrample` | Number | `1` | Applies or references the 'DisableTrample' effect/state. |
| `Fury` | Number | `55, 75` | Applies or references the 'Fury' effect/state. |
| `TileTrail` | [`Enum/String`](./Enums.md#enum-tiletrail) | `FloatingGlassTile, FlowerTile, BrambleTile` | Applies or references the 'TileTrail' effect/state. |
| `JustInCaseTrample` | Number | `0` | Applies or references the 'JustInCaseTrample' effect/state. |
| `LeaveBehind` | [`Block`](./Abilities_and_Spells.md#context-leavebehind) | `{ ... }, Bait` | Spawns a specific object at the character's previous location when they move. |
| `DashFury` | Number | `4` | Applies or references the 'DashFury' effect/state. |
| `BearTrapTrail` | Number | `1` | Applies or references the 'BearTrapTrail' effect/state. |
| `DelayedWindTrail` | Number | `1` | Applies or references the 'DelayedWindTrail' effect/state. |
| `DoubleLoot` | Number | `1` | Applies or references the 'DoubleLoot' effect/state. |
| `JumpAttackLeaveBehind` | [`Enum/String`](./Enums.md#enum-jumpattackleavebehind) | `BungaThrone` | Applies or references the 'JumpAttackLeaveBehind' effect/state. |
| `KnockbackImmunity` | Number | `1` | Applies or references the 'KnockbackImmunity' effect/state. |
| `TileTrail_Ahead` | [`Enum/String`](./Enums.md#enum-tiletrail_ahead) | `FlowerTile` | Applies or references the 'TileTrail_Ahead' effect/state. |

</details>

---

### Context: `splash_damage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `8, 0, 4` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Fire Napalm Explosion ], [ Fire Explosion ], [ Water ]` |  |
| `knockback` | Number | `0, 2, 1` | Knockback force of the splash blast. |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `knockblock, status_spell, spell` | Classification/category type. |
| `makes_contact` | Boolean | `false, true` |  |
| `override_trample_damage` | Boolean | `true` |  |
| `ai_base_score` | Number | `9999` |  |
| `crit_chance` | Number | `100` |  |
| `force_no_knockback` | Boolean | `true` |  |
| `force_play_hit_animation` | Boolean | `true` |  |
| `layer` | [`Enum/String`](./Enums.md#enum-layer) | `tiles` |  |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `poop, moonhead, food` | The specific string tag to check for. |
| `FloatingRockTrap` | Number | `1` | Applies or references the 'FloatingRockTrap' effect/state. |
| `IgnoreDamage` | Number | `1` | Applies or references the 'IgnoreDamage' effect/state. |
| `ApplyToSource` | [`Block`](./Abilities_and_Spells.md#context-applytosource) | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `ImmediateUseAbility` | [`Enum/String`](./Enums.md#enum-immediateuseability) | `HitlerCloneTransform, HitlerCloneHeil, MoonHandMegaSqueeze` | Applies or references the 'ImmediateUseAbility' effect/state. |
| `CanApplyToInanimate` | [`Block`](./Abilities_and_Spells.md#context-canapplytoinanimate) | `{ ... }` | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. |
| `ChangeTilesUnder` | [`Enum/String`](./Enums.md#enum-changetilesunder) | `LavaTile` | Applies or references the 'ChangeTilesUnder' effect/state. |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `Die` | Number | `1` | Applies or references the 'Die' effect/state. |
| `Else` | [`Block`](./Abilities_and_Spells.md#context-else) | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `Vaporize` | Number | `1` | Applies or references the 'Vaporize' effect/state. |
| `BonusDamage` | Number | `10` | Applies or references the 'BonusDamage' effect/state. |
| `CrackMoonHead` | Number | `1` | Applies or references the 'CrackMoonHead' effect/state. |
| `DeleteObject` | Number | `1` | Applies or references the 'DeleteObject' effect/state. |
| `DisplaceTowardsSource` | Number | `1` | Applies or references the 'DisplaceTowardsSource' effect/state. |
| `EventBounty` | Number | `5` | Applies or references the 'EventBounty' effect/state. |
| `FaceAway` | Number | `1` | Applies or references the 'FaceAway' effect/state. |
| `Instakill` | Number | `25` | Applies or references the 'Instakill' effect/state. |
| `OverrideDamage` | Number | `1` | Applies or references the 'OverrideDamage' effect/state. |
| `RemoveStatus` | [`Enum/String`](./Enums.md#enum-removestatus) | `Brace` | Applies or references the 'RemoveStatus' effect/state. |
| `ScatterRandomPickups` | Number | `5` | Applies or references the 'ScatterRandomPickups' effect/state. |
| `SetKnockback` | Number | `0` | Applies or references the 'SetKnockback' effect/state. |
| `UseAbility` | [`Enum/String`](./Enums.md#enum-useability) | `MoonHead_CommandHeadPunch` | Forces the character or target to instantly use a specified ability. |
| `VaporizeCorpse` | Number | `1` | Applies or references the 'VaporizeCorpse' effect/state. |

</details>

---

### Context: `FormChange`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `form` | String | `"Rage", "Turtled", Rage` |  |
| `chance` | Number | `30%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

### Context: `CatPartsTransform`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ear1` | Number | `1501, 23, 325` | Sprite variant ID for the front ear. |
| `tail` | Number | `1503, 1502, 4` | Sprite variant ID for the tail. |
| `ear2` | Number | `1501, 23, 1036` |  |
| `arm2` | Number | `1501, 1013, 324` |  |
| `mouth` | Number | `1501, 1005, 1071` |  |
| `arm1` | Number | `1501, 1013, 338` | Sprite variant ID for the front arm. |
| `leg1` | Number | `1501, 41, 338` | Sprite variant ID for the front leg. |
| `leg2` | Number | `1501, 41, 338` |  |
| `head` | Number | `12, 1504` | Sprite variant ID for the head. |
| `texture` | Number | `1008, 322` |  |
| `body` | Number | `31, 1029` | Sprite variant ID for the body. |
| `eye1` | Number | `1069` |  |
| `eye2` | Number | `1069` |  |
| `eyebrow1` | Number | `1069` |  |
| `eyebrow2` | Number | `1070` |  |
| `palette` | Number | `86` |  |

</details>

---

### Context: `Consumed`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `struggle_ability` | [`Enum/String`](./Enums.md#enum-struggle_ability) | `TinaFlailRage, Thrash, TinaFlail` | Ability triggered by the consumed entity while inside the consumer. |
| `force_contact` | Boolean | `true` | If true, enforces physical overlap. |
| `instant` | Boolean | `true` |  |
| `mount_mode` | [`Enum/String`](./Enums.md#enum-mount_mode) | `auto, true` | If true, treats the consumption as riding/mounting instead of eating. |
| `wet` | Boolean | `false, true` |  |
| `do_not_pop_corpse` | Boolean | `true` |  |
| `drop_on_death` | Boolean | `false, deferred, true` |  |
| `drop_on_self_death` | Boolean | `true` |  |
| `drop_body_ability` | [`Enum/String`](./Enums.md#enum-drop_body_ability) | `MoonHandDrop` |  |
| `kill_on_consume` | Boolean | `true` |  |
| `use_placeholder` | Boolean | `true` |  |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `8, 1, 4` | Applies or references the 'HealthGain' effect/state. |
| `StrengthUp` | Number | `1, 3` | Applies or references the 'StrengthUp' effect/state. |
| `EvolveAbilityFromPool` | [`Enum/String`](./Enums.md#enum-evolveabilityfrompool) | `Medic, Butcher, Thief` | Upgrades or transforms an existing ability into a new one from the specified pool. |
| `FormChange` | [`Block`](./Abilities_and_Spells.md#context-formchange) | `{ ... }, HasCat, Default` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `Shield` | Number | `2, 1, 5` | Applies or references the 'Shield' effect/state. |
| `AddWeaponAux` | Number | `1, "-max(min(X+1, item_aux), 0)", -item_aux` | Applies or references the 'AddWeaponAux' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `ConstitutionUp` | Number | `2, 1` | Applies or references the 'ConstitutionUp' effect/state. |
| `RefreshActPoints` | Number | `1` | Applies or references the 'RefreshActPoints' effect/state. |
| `AddLeechesStatus` | Number | `1` | Applies or references the 'AddLeechesStatus' effect/state. |
| `Cleanse` | Number | `0` | Applies or references the 'Cleanse' effect/state. |
| `EquipPermanentItem` | [`Enum/String`](./Enums.md#enum-equippermanentitem) | `BoneClub, Kidney` | Applies or references the 'EquipPermanentItem' effect/state. |
| `FreeSpell` | Number | `2, 1` | Applies or references the 'FreeSpell' effect/state. |
| `LuckUp` | Number | `1` | Applies or references the 'LuckUp' effect/state. |
| `RemoveStatus` | [`Enum/String`](./Enums.md#enum-removestatus) | `SpeedUp_WithoutInitiative, DodgeChance_Status` | Applies or references the 'RemoveStatus' effect/state. |
| `Brace` | Number | `1` | Applies or references the 'Brace' effect/state. |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `DisableWeapon` | Number | `1` | Applies or references the 'DisableWeapon' effect/state. |
| `DivineShield` | Number | `2` | Applies or references the 'DivineShield' effect/state. |
| `FindItem` | [`Enum/String`](./Enums.md#enum-finditem) | `Molars` | Applies or references the 'FindItem' effect/state. |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `Ram_chained` | Applies or references the 'ForceUseAbility' effect/state. |
| `FullHeal` | Number | `1` | Applies or references the 'FullHeal' effect/state. |
| `KineticSpikes` | Number | `1` | Applies or references the 'KineticSpikes' effect/state. |
| `ManaGain` | Number | `2` | Applies or references the 'ManaGain' effect/state. |
| `MoveQuivered` | Number | `1` | Applies or references the 'MoveQuivered' effect/state. |
| `RefreshMovePoints` | Number | `1` | Applies or references the 'RefreshMovePoints' effect/state. |
| `SpecificInjury` | [`Enum/String`](./Enums.md#enum-specificinjury) | `str` | Applies or references the 'SpecificInjury' effect/state. |
| `StanceSwitchToMelee` | Number | `1` | Applies or references the 'StanceSwitchToMelee' effect/state. |
| `StanceSwitchToRanged` | Number | `1` | Applies or references the 'StanceSwitchToRanged' effect/state. |
| `TakeExtraTurn` | Number | `1` | Applies or references the 'TakeExtraTurn' effect/state. |
| `Tech` | Number | `1` | Applies or references the 'Tech' effect/state. |
| `TempTrampleUntilSettled` | Number | `3` | Applies or references the 'TempTrampleUntilSettled' effect/state. |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `distance` | Number | `2, 3, -3` | The distance in tiles to knock the target away. |
| `stacks` | Number | `1, 5, 5+bonus_melee_ability_damage` | Number of stacks or intensity to apply. |
| `height` | Number | `2, 0` |  |
| `circular_variance` | Number | `2` |  |

</details>

---

### Context: `sounds`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ontrigger` | [`Enum/String`](./Enums.md#enum-ontrigger) | `Spawn_Donate, Spiderweb_Break, SE_BullRushDash` |  |
| `oncast` | [`Enum/String`](./Enums.md#enum-oncast) | `AbilitySnd_BoulderDrop, AbilitySnd_Assassinate` |  |
| `oncastpoint` | [`Enum/String`](./Enums.md#enum-oncastpoint) | `Batterup_Swing_Castpoint, AirHorn` |  |
| `ontrigger_intentional` | [`Enum/String`](./Enums.md#enum-ontrigger_intentional) | `Lenny_HereKitty` |  |

</details>

---

### Context: `Conditional_Boss`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_HasStatus` | [`Block`](./Abilities_and_Spells.md#context-conditional_hasstatus) | `{ ... }` | Conditional trigger: Executes nested logic if the target currently has the specified status effect. |
| `Else` | [`Block`](./Abilities_and_Spells.md#context-else) | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `OverrideDamage` | Number | `10, 25` | Applies or references the 'OverrideDamage' effect/state. |
| `RemoveStatus` | [`Enum/String`](./Enums.md#enum-removestatus) | `Petrify` | Applies or references the 'RemoveStatus' effect/state. |
| `VisualFX` | [`Enum/String`](./Enums.md#enum-visualfx) | `PartyExplosion, Explosion` | Applies or references the 'VisualFX' effect/state. |
| `BonusDamage` | Number | `25` | Applies or references the 'BonusDamage' effect/state. |
| `Drowsy` | Number | `1` | Applies or references the 'Drowsy' effect/state. |
| `ExplodeCharacter_PartyBoss` | Number | `5` | Applies or references the 'ExplodeCharacter_PartyBoss' effect/state. |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Number | `9, 5` | Applies or references the 'ExplodeCharacter_RockCrusher_PetrifyBreak' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `Charmed` | Number | `1` | Applies or references the 'Charmed' effect/state. |
| `ExplodeCharacter_NoDie` | Number | `5` | Applies or references the 'ExplodeCharacter_NoDie' effect/state. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `XIsTargetHealth` | [`Block`](./Abilities_and_Spells.md#context-xistargethealth) | `{ ... }` | Math variable assignment: Evaluates X as the target's current health. |

</details>

---

### Context: `additional_passives`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SafeDoomed` | [`Enum/String`](./Enums.md#enum-safedoomed) | `level, 2, 1` | Applies or references the 'SafeDoomed' effect/state. |
| `InjuryImmunity` | Number | `1` | Applies or references the 'InjuryImmunity' effect/state. |
| `AllStatsUp` | Number | `2` | Applies or references the 'AllStatsUp' effect/state. |
| `FadeInsteadOfDie` | Number | `1` | Applies or references the 'FadeInsteadOfDie' effect/state. |
| `IllusionTint` | Number | `1` | Applies or references the 'IllusionTint' effect/state. |
| `PermanentMadness` | Number | `1` | Applies or references the 'PermanentMadness' effect/state. |
| `CaptureFamiliar` | Number | `1` | Applies or references the 'CaptureFamiliar' effect/state. |
| `DamageUp` | Number | `2` | Applies or references the 'DamageUp' effect/state. |
| `FillMana` | Number | `1` | Applies or references the 'FillMana' effect/state. |
| `HealthGain` | Number | `8` | Applies or references the 'HealthGain' effect/state. |
| `HideEquipment` | [`Enum/String`](./Enums.md#enum-hideequipment) | `neck` | Applies or references the 'HideEquipment' effect/state. |
| `SchizoIllusionAIModifier` | Number | `1` | Applies or references the 'SchizoIllusionAIModifier' effect/state. |
| `SpeedUp` | Number | `4` | Applies or references the 'SpeedUp' effect/state. |

</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | `1, [ 1 .2 ], 3` | Applies or references the 'Confusion' effect/state. |
| `DisplaceToAbilityTarget` | Number | `1` | Applies or references the 'DisplaceToAbilityTarget' effect/state. |
| `AllStatsUp` | Number | `1, -1` | Applies or references the 'AllStatsUp' effect/state. |
| `Attraction` | Number | `1` | Applies or references the 'Attraction' effect/state. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `TakeExtraTurn` | Number | `1` | Applies or references the 'TakeExtraTurn' effect/state. |
| `Weakness` | Number | `2, 1` | Applies or references the 'Weakness' effect/state. |
| `BonusDamage` | Number | `1` | Applies or references the 'BonusDamage' effect/state. |
| `Burn` | Number | `3` | Applies or references the 'Burn' effect/state. |
| `Charmed` | Number | `1` | Applies or references the 'Charmed' effect/state. |
| `Doomed` | Number | `1` | Applies or references the 'Doomed' effect/state. |
| `ForceMoveTowards` | Number | `1` | Applies or references the 'ForceMoveTowards' effect/state. |
| `Hex` | Number | `1` | Applies or references the 'Hex' effect/state. |
| `Marked` | Number | `1` | Applies or references the 'Marked' effect/state. |
| `PermanentCharm` | Number | `1` | Applies or references the 'PermanentCharm' effect/state. |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1, .25 ]` | Applies or references the 'Stun' effect/state. |
| `TempDamageUp` | Number | `-1` | Applies or references the 'TempDamageUp' effect/state. |

</details>

---

### Context: `Conditional_HasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Petrify, Undead, Freeze` | The specific status ID to check for. |
| `BonusDamage` | Number | `10, 20` | Applies or references the 'BonusDamage' effect/state. |
| `Burn` | Number | `3` | Applies or references the 'Burn' effect/state. |
| `RemoveStatus` | [`Enum/String`](./Enums.md#enum-removestatus) | `Petrify` | Applies or references the 'RemoveStatus' effect/state. |
| `Slow` | Number | `2` | Applies or references the 'Slow' effect/state. |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `FormChange` | [`Enum/String`](./Enums.md#enum-formchange) | `Bully` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `Quivered` | Number | `1` | Applies or references the 'Quivered' effect/state. |

</details>

---

### Context: `Conditional_Ally`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | Number | `-10, 0` | Applies or references the 'OverrideDamage' effect/state. |
| `DamageUp` | Number | `2, 1` | Applies or references the 'DamageUp' effect/state. |
| `KnockbackDamageImmuneUntilSettled` | Number | `1` | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `HealthGain` | Number | `4` | Applies or references the 'HealthGain' effect/state. |
| `RandomStatUp` | [`Equation`](./Enums.md#enum-mathequation) | `"ceil(X/3)", "ceil(X/2)"` | Applies or references the 'RandomStatUp' effect/state. |
| `ApplyToSource` | [`Block`](./Abilities_and_Spells.md#context-applytosource) | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `BleedThorns` | Number | `3` | Applies or references the 'BleedThorns' effect/state. |
| `ChanceToBreak` | Number | `5%` | Applies or references the 'ChanceToBreak' effect/state. |
| `Charmed` | Number | `1` | Applies or references the 'Charmed' effect/state. |
| `Cleanse` | Number | `0` | Applies or references the 'Cleanse' effect/state. |
| `FullHeal` | Number | `1` | Applies or references the 'FullHeal' effect/state. |
| `RepairAll` | Number | `1` | Applies or references the 'RepairAll' effect/state. |
| `ShowText` | String | `"COMBAT_POPUP_REPAIRED"` | Applies or references the 'ShowText' effect/state. |
| `TempDamageUp` | Number | `1` | Applies or references the 'TempDamageUp' effect/state. |
| `Thorns` | Number | `1` | Applies or references the 'Thorns' effect/state. |
| `ThornsDamageImmuneUntilSettled` | Number | `1` | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. |
| `TileDamageImmuneUntilSettled` | Number | `1` | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. |

</details>

---

### Context: `EvolveAbilityFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `Mage, Hunter, Thief` |  |
| `upgraded` | Boolean | `true` |  |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `odds` | Number | `50%, 90%, 10%` | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |
| `GainDisorderFromPool_PostCast` | [`Enum/String`](./Enums.md#enum-gaindisorderfrompool_postcast) | `forbidden_spell_consequences` | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. |
| `GainDisorder` | [`Enum/String`](./Enums.md#enum-gaindisorder) | `Chungus` | Applies or references the 'GainDisorder' effect/state. |
| `ImmediateUseAbility` | [`Enum/String`](./Enums.md#enum-immediateuseability) | `tk_ButterBean_Mega` | Applies or references the 'ImmediateUseAbility' effect/state. |
| `RefreshWeaponAbility` | Number | `1` | Applies or references the 'RefreshWeaponAbility' effect/state. |
| `ShowText` | String | `"COMBAT_POPUP_RELOAD"` | Applies or references the 'ShowText' effect/state. |

</details>

---

### Context: `Craft`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `allsticks, tinkerer_default, stick` |  |
| `slot` | [`Enum/String`](./Enums.md#enum-slot) | `trinket, random_empty_armor, weapon` |  |
| `temporary` | Boolean | `false` |  |
| `works_with_tech` | Boolean | `true` |  |

</details>

---

### Context: `CanApplyToInanimate`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ObjectOnHitCharacter` | [`Enum/String`](./Enums.md#enum-objectonhitcharacter) | `CharmedLeech, Fly, AllyRotFly` | Spawns a specific character or entity upon impact. |
| `BreakIntoRocks` | [`Enum/String`](./Enums.md#enum-breakintorocks) | `SmallRock, Coin` | Applies or references the 'BreakIntoRocks' effect/state. |
| `Vaporize` | Number | `1` | Applies or references the 'Vaporize' effect/state. |
| `GetAggroTarget` | Number | `1` | Applies or references the 'GetAggroTarget' effect/state. |
| `PreventDeathTransforms` | Number | `1` | Applies or references the 'PreventDeathTransforms' effect/state. |

</details>

---

### Context: `DoScreenShake`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `intensity` | Number | `10, 20, 3` |  |
| `time` | Number | `2, .5, .75` |  |

</details>

---

### Context: `ApplyToSourceOnKill`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RemoveItem` | [`Enum/String`](./Enums.md#enum-removeitem) | `BlackShard, BlackShard_Glowing` | Applies or references the 'RemoveItem' effect/state. |
| `AlphaCat` | Number | `1` | Applies or references the 'AlphaCat' effect/state. |
| `CompleteItemQuest` | [`Enum/String`](./Enums.md#enum-completeitemquest) | `BlackShard` | Applies or references the 'CompleteItemQuest' effect/state. |
| `HealthGain` | Number | `10, 5` | Applies or references the 'HealthGain' effect/state. |
| `ManaGain` | Number | `5` | Applies or references the 'ManaGain' effect/state. |
| `Revive` | Number | `50%, 100%` | Applies or references the 'Revive' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `EvolveAbilityFromPool` | [`Enum/String`](./Enums.md#enum-evolveabilityfrompool) | `Hunter` | Upgrades or transforms an existing ability into a new one from the specified pool. |
| `RefreshActPoints` | Number | `1` | Applies or references the 'RefreshActPoints' effect/state. |
| `StrengthUp` | Number | `2` | Applies or references the 'StrengthUp' effect/state. |
| `TakeExtraTurn` | Number | `1` | Applies or references the 'TakeExtraTurn' effect/state. |
| `WeaponAuxMultiplier` | [`Enum/String`](./Enums.md#enum-weaponauxmultiplier) | `.5` | Applies or references the 'WeaponAuxMultiplier' effect/state. |

</details>

---

### Context: `Conditional_FormulaIsPositive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `formula` | [`Enum/String`](./Enums.md#enum-formula) | `X+1, X-1, X` | The math expression to evaluate. |
| `Burn` | [`Enum/String`](./Enums.md#enum-burn) | `X+1, X` | Applies or references the 'Burn' effect/state. |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |
| `Shield` | Number | `6, 5` | Applies or references the 'Shield' effect/state. |
| `Freeze` | Number | `1` | Applies or references the 'Freeze' effect/state. |
| `OverrideKnockbackDamage` | [`Enum/String`](./Enums.md#enum-overrideknockbackdamage) | `X*10` | Applies or references the 'OverrideKnockbackDamage' effect/state. |
| `Slow` | [`Enum/String`](./Enums.md#enum-slow) | `X` | Applies or references the 'Slow' effect/state. |
| `SpeedUp` | Number | `-1` | Applies or references the 'SpeedUp' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |

</details>

---

### Context: `Conditional_HealthThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `threshold_flat` | Number | `10, 5, 3` | A flat numerical health value threshold. |
| `SpawnThingIfHitKills` | [`Enum/String`](./Enums.md#enum-spawnthingifhitkills) | `Food` | Applies or references the 'SpawnThingIfHitKills' effect/state. |
| `threshold_percent` | Number | `25%, 50%` | A percentage-based health threshold (e.g. 50%). |
| `BonusDamage` | [`Equation`](./Enums.md#enum-mathequation) | `20+bonus_melee_damage` | Applies or references the 'BonusDamage' effect/state. |
| `CaptureFamiliar` | Number | `1` | Applies or references the 'CaptureFamiliar' effect/state. |
| `Die` | Number | `1` | Applies or references the 'Die' effect/state. |
| `DieViolently` | Number | `1` | Applies or references the 'DieViolently' effect/state. |
| `FactionConversion` | Number | `1` | Applies or references the 'FactionConversion' effect/state. |
| `FlatLeech` | Number | `5` | Applies or references the 'FlatLeech' effect/state. |
| `FullHeal` | Number | `1` | Applies or references the 'FullHeal' effect/state. |
| `Instakill` | Number | `999` | Applies or references the 'Instakill' effect/state. |
| `Vaporize` | Number | `1` | Applies or references the 'Vaporize' effect/state. |
| `threshold_expr` | [`Enum/String`](./Enums.md#enum-threshold_expr) | `item_aux` |  |

</details>

---

### Context: `DoDistortionRing`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `intensity` | Number | `2, 1, -1` |  |
| `radius` | Number | `5, 4` | Distance or area of effect in tiles. |
| `speed` | Number | `30, -30, 20` |  |

</details>

---

### Context: `ChanceToBreakFree`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `CHuskDrop, XXX, LennyDrop` | The ability triggered upon successfully breaking free. |
| `fail_ability` | [`Enum/String`](./Enums.md#enum-fail_ability) | `LennyStruggleFail, XXX, CHuskDropFail` | The ability triggered if the break free attempt fails. |
| `stacks` | Number | `25` | Percentage base chance to break free. |

</details>

---

### Context: `Conditional_InForm`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `form` | [`Enum/String`](./Enums.md#enum-form) | `Normal, Small, Default` | The specific form ID to check for. |
| `FormChange` | [`Enum/String`](./Enums.md#enum-formchange) | `Big, Lifted, Drunker` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `CritChanceUp` | Number | `20` | Applies or references the 'CritChanceUp' effect/state. |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `DodgeChance_Status` | Number | `20` | Applies or references the 'DodgeChance_Status' effect/state. |
| `SpeedUp` | Number | `1` | Applies or references the 'SpeedUp' effect/state. |
| `UseAbility` | [`Enum/String`](./Enums.md#enum-useability) | `MoonHandPunchHead` | Forces the character or target to instantly use a specified ability. |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `BonusAbility` | [`Enum/String`](./Enums.md#enum-bonusability) | `ThrowSpiritBomb, TinkererThrow, DonateEnergy` | Applies or references the 'BonusAbility' effect/state. |
| `DamageUp` | Number | `-1` | Applies or references the 'DamageUp' effect/state. |
| `Shield` | Number | `5` | Applies or references the 'Shield' effect/state. |
| `Bleed` | Number | `3` | Applies or references the 'Bleed' effect/state. |
| `Brace` | Number | `1` | Applies or references the 'Brace' effect/state. |
| `Charmed` | Number | `1` | Applies or references the 'Charmed' effect/state. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `PermanentMadness` | Number | `1` | Applies or references the 'PermanentMadness' effect/state. |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |
| `TemporaryItem` | Number | `1` | Applies or references the 'TemporaryItem' effect/state. |
| `Webbed` | Number | `1` | Applies or references the 'Webbed' effect/state. |

</details>

---

### Context: `TwisterDisplaceWithDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | [`Enum/String`](./Enums.md#enum-damage) | `inherit, 1` | The damage formula or inherit flag. |
| `max_dist` | Number | `2, 20, 3` | Maximum displacement distance. |
| `min_dist` | Number | `2, 3` | Minimum displacement distance. |
| `exclude_prefix` | [`Enum/String`](./Enums.md#enum-exclude_prefix) | `Twister` |  |

</details>

---

### Context: `ArcLightning`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | `false, true` | If true, the arc will not bounce to friendly targets. |
| `max_distance` | Number | `2, 1, 3` | The maximum tile range the lightning can jump between bounces. |
| `stacks` | Number | `100` | The maximum number of targets the lightning can bounce to. |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.5` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `ignore_self` | Boolean | `true` | If true, prevents the arc from bouncing back to the caster. |

</details>

---

### Context: `ChangeTile`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tile` | [`Array`](./Arrays.md#array-tile) | `[ TallGrassTile TallFlowerTile BrambleTile ], ToxicTile, GlassTile` | The specific tile type to change into (e.g., GlassTile). |
| `chance` | Number | `25%, .25` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `aoe` | Number | `1` |  |

</details>

---

### Context: `Conditional_NotBoss`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Number | `1` | Applies or references the 'CaptureFamiliar' effect/state. |
| `Doomed` | Number | `1` | Applies or references the 'Doomed' effect/state. |
| `ExplodeCharacter_RockCrusher` | Number | `9, 5` | Applies or references the 'ExplodeCharacter_RockCrusher' effect/state. |
| `FactionConversion` | Number | `1` | Applies or references the 'FactionConversion' effect/state. |
| `Vaporize` | Number | `1` | Applies or references the 'Vaporize' effect/state. |
| `VaporizeInanimate` | Number | `1` | Applies or references the 'VaporizeInanimate' effect/state. |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1 .3 ]` | Applies or references the 'Fear' effect/state. |
| `PermanentCharm` | Number | `1` | Applies or references the 'PermanentCharm' effect/state. |

</details>

---

### Context: `DoDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `8, 0, 5` | The flat damage amount. |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell, generic_physical, melee` | The classification of the damage (e.g., spell, melee). |
| `damage_tiles` | [`Enum/String`](./Enums.md#enum-damage_tiles) | `all` |  |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Water ], [ Fire ]` |  |

</details>

---

### Context: `ApplyPassives`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddTag` | [`Enum/String`](./Enums.md#enum-addtag) | `plant, squirrel` | Applies or references the 'AddTag' effect/state. |
| `Flying` | Number | `1` | Applies or references the 'Flying' effect/state. |
| `IgnoreTiles` | Number | `1` | Applies or references the 'IgnoreTiles' effect/state. |
| `YOffset` | [`Enum/String`](./Enums.md#enum-yoffset) | `.25` | Applies or references the 'YOffset' effect/state. |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Creep` | Applies or references the 'ElementImmune' effect/state. |
| `KnockbackImmunity` | Number | `1` | Applies or references the 'KnockbackImmunity' effect/state. |
| `Plant` | Number | `1` | Applies or references the 'Plant' effect/state. |
| `ReplaceBasicAttack` | [`Enum/String`](./Enums.md#enum-replacebasicattack) | `BasicPuke` | Applies or references the 'ReplaceBasicAttack' effect/state. |

</details>

---

### Context: `Conditional_Speculative`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `IgnoreDamage` | Number | `1` | Applies or references the 'IgnoreDamage' effect/state. |
| `BonusDamageBasedOnDistance` | Number | `1` | Applies or references the 'BonusDamageBasedOnDistance' effect/state. |
| `Conditional_HealthThreshold` | [`Block`](./Abilities_and_Spells.md#context-conditional_healththreshold) | `{ ... }` | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. |
| `BonusDamage` | Number | `-1` | Applies or references the 'BonusDamage' effect/state. |
| `CapDamage` | Number | `1` | Applies or references the 'CapDamage' effect/state. |
| `Else` | [`Block`](./Abilities_and_Spells.md#context-else) | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `Knockback` | Number | `10` | Applies or references the 'Knockback' effect/state. |
| `RandomBonusDamage` | Number | `25` | Applies or references the 'RandomBonusDamage' effect/state. |

</details>

---

### Context: `SwitchMusic`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `new_layer` | [`Enum/String`](./Enums.md#enum-new_layer) | `map, battle, event` | The specific audio layer to transition to (e.g., map, battle). |
| `new_song` | [`Enum/String`](./Enums.md#enum-new_song) | `same` | The ID of the new music track. |
| `crossfade_speed` | Number | `1` |  |

</details>

---

### Context: `TimeDelayStatusApplication`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `delay` | [`Enum/String`](./Enums.md#enum-delay) | `.25, 3, 1.13333` | The float time delay in seconds. |
| `Cleanse` | Number | `0` | Applies or references the 'Cleanse' effect/state. |
| `FormChange` | [`Enum/String`](./Enums.md#enum-formchange) | `DualSword` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `FullHeal` | Number | `1` | Applies or references the 'FullHeal' effect/state. |
| `GlobalSpawnCharacter` | [`Enum/String`](./Enums.md#enum-globalspawncharacter) | `MegaGuppy` | Applies or references the 'GlobalSpawnCharacter' effect/state. |
| `PlayBackground` | Number | `1` | Applies or references the 'PlayBackground' effect/state. |
| `RemoveAmbientLightEffects` | [`Enum/String`](./Enums.md#enum-removeambientlighteffects) | `.5` | Applies or references the 'RemoveAmbientLightEffects' effect/state. |
| `Vaporize` | Number | `1` | Applies or references the 'Vaporize' effect/state. |

</details>

---

### Context: `ReviveNextRound`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `revive_health` | Number | `100%, 50%, 1` | The flat amount of health to revive with. |
| `AllStatsUp` | Number | `2, 1` | Applies or references the 'AllStatsUp' effect/state. |
| `Shield` | Number | `20, 15` | Applies or references the 'Shield' effect/state. |
| `stacks` | Number | `2` | Number of stacks or intensity to apply. |
| `DivineShield` | Number | `2` | Applies or references the 'DivineShield' effect/state. |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Revive` | Number | `50%, 100%` | Applies or references the 'Revive' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `FlatAIBonus` | Number | `100` | Applies or references the 'FlatAIBonus' effect/state. |
| `HealRandomInjury` | Number | `1` | Applies or references the 'HealRandomInjury' effect/state. |
| `PermanentCharm` | Number | `1` | Applies or references the 'PermanentCharm' effect/state. |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `Teleport, DestroyerDodge, SZBBackflipDodge` | The specific dodge ability to trigger (e.g., DestroyerDodge). |
| `stacks` | Number | `1, 4` | Number of stacks or intensity to apply. |

</details>

---

### Context: `Conditional_Object`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_HasTag` | [`Block`](./Abilities_and_Spells.md#context-conditional_hastag) | `{ ... }` | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. |
| `Else` | [`Block`](./Abilities_and_Spells.md#context-else) | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `CanApplyToInanimate` | [`Block`](./Abilities_and_Spells.md#context-canapplytoinanimate) | `{ ... }` | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. |
| `RepairWeapon` | Number | `1` | Applies or references the 'RepairWeapon' effect/state. |

</details>

---

### Context: `Conditional_PlayerCat`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ConjureRandomAbilityFromCat` | Number | `1` | Applies or references the 'ConjureRandomAbilityFromCat' effect/state. |
| `Adrenaline` | Number | `10` | Applies or references the 'Adrenaline' effect/state. |
| `Cleanse` | Number | `0` | Applies or references the 'Cleanse' effect/state. |
| `GenericDebuff` | Number | `999999` | Applies or references the 'GenericDebuff' effect/state. |
| `KnockOutClone` | [`Enum/String`](./Enums.md#enum-knockoutclone) | `PlayerCat_MiniMiniMe` | Applies or references the 'KnockOutClone' effect/state. |
| `Scrambled` | Number | `1` | Applies or references the 'Scrambled' effect/state. |
| `T2CopyCat` | Number | `1` | Applies or references the 'T2CopyCat' effect/state. |

</details>

---

### Context: `DestroyEquipmentAndAttachParasite`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `parasites, [ FlyHat FlyMask FlyNeck ], [ AmoebaHat AmoebaNeck AmoebaFace ]` | The item pool to draw the parasite from. |
| `chance` | Number | `1, .15` | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

### Context: `GainCoinsRange`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `max` | Number | `2, 30, 4` | Maximum coins granted. |
| `min` | Number | `2, 1, 10` | Minimum coins granted. |

</details>

---

### Context: `ReplaceSpell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MoonHeadCommandStopHittingYourself, None` | The new ability ID to insert. |
| `slot` | Number | `1, 2, 0` | The spell slot index to replace. |

</details>

---

### Context: `rocket_swirl`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `radius` | [`Array`](./Arrays.md#array-radius) | `[ .25 .5 ], [ .5 1 ]` | Swirl radius. |
| `speed` | [`Array`](./Arrays.md#array-speed) | `[ 1.5, 2.5 ], [ .25, 1.0 ]` | Rotations per second. |

</details>

---

### Context: `CollectsPickupsWithAltEffects`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | `1` | Applies or references the 'Tech' effect/state. |
| `CurrentWeaponAddPoison` | Number | `1` | Applies or references the 'CurrentWeaponAddPoison' effect/state. |
| `LuckUp` | Number | `2` | Applies or references the 'LuckUp' effect/state. |
| `Quivered` | Number | `1` | Applies or references the 'Quivered' effect/state. |
| `RandomStatUp` | Number | `1` | Applies or references the 'RandomStatUp' effect/state. |
| `Shield` | Number | `1` | Applies or references the 'Shield' effect/state. |

</details>

---

### Context: `TakeBonusTurnWithStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `Stun` | Number | `1, [ 1 .75 ]` | Applies or references the 'Stun' effect/state. |
| `TempNoManaRegen` | Number | `1` | Applies or references the 'TempNoManaRegen' effect/state. |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |

</details>

---

### Context: `BounceObject`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `obj` | [`Enum/String`](./Enums.md#enum-obj) | `chapter_corpse_medium, SmallLavaRock` | The entity ID of the object to spawn (e.g., chapter_corpse_medium). |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.5, .25` | Probability (0.0 to 1.0) of spawning the object. |
| `slide` | Number | `10` |  |

</details>

---

### Context: `Conditional_AffectedByElement`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Water, Fire` | The specific element type to check for. |
| `BonusCritChance` | Number | `100` | Applies or references the 'BonusCritChance' effect/state. |
| `Burn` | Number | `2` | Applies or references the 'Burn' effect/state. |

</details>

---

### Context: `Conditional_OncePerBattle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CompleteItemQuest` | [`Enum/String`](./Enums.md#enum-completeitemquest) | `Nuke` | Applies or references the 'CompleteItemQuest' effect/state. |
| `TriggerGameEnding` | Number | `0, 1` | Applies or references the 'TriggerGameEnding' effect/state. |
| `key` | [`Enum/String`](./Enums.md#enum-key) | `gamewin` |  |

</details>

---

### Context: `IncAuxCounterClamped`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `change` | Number | `-3, -2, -1` |  |
| `max` | Number | `3` |  |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | `true` | If true, triggers the effect even if the character died during the battle. |
| `RandomTaggedMutation` | [`Enum/String`](./Enums.md#enum-randomtaggedmutation) | `melted, bird` | Applies or references the 'RandomTaggedMutation' effect/state. |
| `RandomMutation` | Number | `3` | Applies or references the 'RandomMutation' effect/state. |

</details>

---

### Context: `Conditional_Familiar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `2, 3` | Applies or references the 'DamageUp' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `BonusDamage` | Number | `-2` | Applies or references the 'BonusDamage' effect/state. |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |

</details>

---

### Context: `PopAndSpawn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `PlayerCat_ClotClone, BoyShade` | The entity ID to spawn in place. |
| `clone_items` | Boolean | `false` | If true, transfers inventory to the new entity. |
| `clone_referenced_catdata` | Boolean | `true` | If true, copies the genetic data of the popped cat. |
| `no_splatter` | Boolean | `false` |  |

</details>

---

### Context: `TeamCastAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `CollectiveSpinImpl, CollectiveCounterImpl` | The underlying logic ability executed by the team. |
| `tag_restriction` | [`Enum/String`](./Enums.md#enum-tag_restriction) | `collective` | Requires participants to share this tag. |
| `same_orientation` | Boolean | `true` |  |

</details>

---

### Context: `TempPassiveWhileHasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Consumed, Sleep` | The required status effect. |
| `AddManaRegen` | Number | `5` | Applies or references the 'AddManaRegen' effect/state. |
| `HealthRegenUp` | Number | `5` | Applies or references the 'HealthRegenUp' effect/state. |

</details>

---

### Context: `AfterImage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `PlayerCat_ThiefShade` | The entity ID of the visual decoy to spawn (e.g., PlayerCat_ThiefShade). |
| `skilltemp` | Boolean | `true` | If true, the decoy is automatically destroyed once the skill finishes executing. |

</details>

---

### Context: `ApplyStatusIfCrit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1, 5` | Applies or references the 'Bleed' effect/state. |
| `LuckUp` | Number | `-1` | Applies or references the 'LuckUp' effect/state. |

</details>

---

### Context: `ApplyToConsumed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DeleteObject` | Number | `1` | Applies or references the 'DeleteObject' effect/state. |
| `Die` | Number | `1` | Applies or references the 'Die' effect/state. |

</details>

---

### Context: `ApplyToTile`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ObjectOnHit` | [`Enum/String`](./Enums.md#enum-objectonhit) | `Bait` | Spawns a specific physics/item object upon impact. |
| `SpawnBearTrap` | Number | `1` | Applies or references the 'SpawnBearTrap' effect/state. |

</details>

---

### Context: `BodyGuard`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `BodyGuardSwap, BodyGuardSwap2` | The specific ability ID to use when intercepting (e.g., BodyGuardSwap). |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `CatPartsSizeScaleStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `arm1` | Number | `1.1` | Scale multiplier for the front arm. |
| `arm2` | Number | `1.1` | Scale multiplier for the back arm. |
| `body` | Number | `1.1` |  |
| `mouth` | Number | `1.1` |  |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `odds` | [`Enum/String`](./Enums.md#enum-odds) | `.16666666` | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. |
| `DieViolently` | Number | `1` | Applies or references the 'DieViolently' effect/state. |
| `Instakill` | Number | `25` | Applies or references the 'Instakill' effect/state. |

</details>

---

### Context: `Conditional_Shielded`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Cleave` | Number | `1` | Causes the attack to hit adjacent enemies alongside the primary target. |
| `BonusDamage` | [`Enum/String`](./Enums.md#enum-bonusdamage) | `str` | Applies or references the 'BonusDamage' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |

</details>

---

### Context: `ConjureBonusAbility`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `Class, Colorless` | The ID of the ability to conjure. |
| `upgraded` | Boolean | `true` | If true, conjures the upgraded version of the ability. |

</details>

---

### Context: `LateStatusApplication`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CurrentWeaponDamageUp` | Number | `1, 5` | Applies or references the 'CurrentWeaponDamageUp' effect/state. |
| `AddWeaponAux` | Number | `2` | Applies or references the 'AddWeaponAux' effect/state. |

</details>

---

### Context: `LeaveBehind`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#context-temporary_effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Fly, Twister, CharmedMaggot` | The entity ID to spawn. |

</details>

---

### Context: `LowerAmbientLight`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `amount` | [`Array`](./Arrays.md#array-amount) | `[ 50% 60% 60% ]` | The target opacity/dimness level. |
| `speed` | Number | `4` | The transition speed. |

</details>

---

### Context: `Math`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `ObjectOnHitCharacter`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.5, 1` | Probability (0.0 to 1.0) of spawning. |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CharmedFlea` | The entity ID of the character to spawn (e.g., CharmedFlea). |

</details>

---

### Context: `QuakeAreaChance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `50%` | Probability of triggering the quake. |
| `radius` | Number | `1, 0` | The tile radius of the quake. |

</details>

---

### Context: `RandomKnockback`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `max` | Number | `10, 3` | Maximum knockback distance. |
| `min` | Number | `1` | Minimum knockback distance. |

</details>

---

### Context: `RandomMagicMissile`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `full_size` | Boolean | `true` | If true, fires normal sized missiles instead of mini ones. |
| `stacks` | Number | `4, 3` | Number of stacks or intensity to apply. |

</details>

---

### Context: `ScatterCoins`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stackable` | Boolean | `true` | If true, multiple instances of this trigger can stack. |
| `stacks` | [`Enum/String`](./Enums.md#enum-stacks) | `item_aux, "max(min(X+1, item_aux), 0)"` | Number of stacks or intensity to apply. |

</details>

---

### Context: `WaggleClone`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `1x1_object` | [`Enum/String`](./Enums.md#enum-1x1_object) | `cWaggle` | The 1x1 variant of the object. |
| `2x2_object` | [`Enum/String`](./Enums.md#enum-2x2_object) | `cWaggle2x2` | The 2x2 variant of the object. |
| `3x3_object` | [`Enum/String`](./Enums.md#enum-3x3_object) | `cWaggle3x3` | The 3x3 variant of the object. |
| `stacks` | Number | `5` | Number of stacks or intensity to apply. |

</details>

---

### Context: `ApplyMultipleTimes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `8, 4, X` | The number of times the nested effects block should be repeatedly executed. |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `Transcend2, SharpenNail2` | The ID of the ability to autocast. |
| `even_if_stunned` | Boolean | `true` | If true, bypasses stun and hard-CC restrictions to cast anyway. |

</details>

---

### Context: `Conditional_Displaceable`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LaunchOffScreen` | [`Equation`](./Enums.md#enum-mathequation) | `10+bonus_melee_ability_damage` | Applies or references the 'LaunchOffScreen' effect/state. |
| `LaunchOffScreenInstakill` | Number | `1` | Applies or references the 'LaunchOffScreenInstakill' effect/state. |
| `TempInitiativeChange` | Number | `-100` | Applies or references the 'TempInitiativeChange' effect/state. |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `key` | [`Enum/String`](./Enums.md#enum-key) | `EtherSoakedRag, TaintedOffering2, TaintedOffering` | A unique string identifier to track this specific application. |

</details>

---

### Context: `Conditional_LastHit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `BonusDamage` | Number | `3` | Applies or references the 'BonusDamage' effect/state. |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `DelayCastAbility` | [`Enum/String`](./Enums.md#enum-delaycastability) | `HitlerNuke` | Queues an ability to be cast automatically after a certain delay or trigger. |

</details>

---

### Context: `DelayCastAbility`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `FetusAirstrike` | The ID of the ability to cast later. |
| `lingering` | Boolean | `true` |  |
| `relative` | Boolean | `false` |  |

</details>

---

### Context: `DustOnHit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `GasCloud` | The ID of the object/particle to spawn. |

</details>

---

### Context: `FindItemFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.02, .15` | Probability of finding the item. |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `chapter` | The item pool to draw from. |

</details>

---

### Context: `ForceMoveTowardsTaggedObject`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MoveTwoTrample, MoveOneTrample` | The movement ability to use. |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `food` | The entity tag to seek out. |

</details>

---

### Context: `NextAttackSpecialCrit`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Number | `2` | Flat addition to the critical damage multiplier. |
| `extra_coins_per_stack` | Number | `2` | Grants bonus coins based on stacks. |
| `luck_increase` | Number | `1` | Increases luck stat for the attack. |

</details>

---

### Context: `NextBasicAttackCritsThisTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | `true` | If true, ensures the attack cannot be dodged. |
| `piercing` | Boolean | `true` | If true, the attack ignores armor. |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `OverHealToStatuses`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomStatUp` | Number | `1` | Applies or references the 'RandomStatUp' effect/state. |
| `TakeExtraTurn` | Number | `1` | Applies or references the 'TakeExtraTurn' effect/state. |
| `stack_scale` | Number | `0` |  |

</details>

---

### Context: `SetCrazyEyeBackgroundWeights`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `weights` | [`Array`](./Arrays.md#array-weights) | `[ 0 1 0 ], [ 1 0 0 ], [ 0 0 1 ]` |  |

</details>

---

### Context: `extra_statuses`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | `4` | Applies or references the 'Burn' effect/state. |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |
| `Tarred` | Number | `2` | Applies or references the 'Tarred' effect/state. |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `Bruise` | Number | `2` | Applies or references the 'Bruise' effect/state. |

</details>

---

### Context: `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `GainDisorderFromPool_PostCast` | [`Enum/String`](./Enums.md#enum-gaindisorderfrompool_postcast) | `forbidden_spell_consequences, forbidden_spell_consequences_crippling` | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. |

</details>

---

### Context: `Conditional_Backstab`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `BonusCritChance` | Number | `100` | Applies or references the 'BonusCritChance' effect/state. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |

</details>

---

### Context: `Conditional_BossOrBig`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Immobile` | [`Array`](./Arrays.md#array-immobile) | `[ 1 .25 ]` | Applies or references the 'Immobile' effect/state. |

</details>

---

### Context: `Conditional_Buddy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Consumed` | [`Block`](./Abilities_and_Spells.md#context-consumed) | `{ ... }` | State block triggered when this object or entity is eaten/consumed by another character. |
| `Else` | [`Block`](./Abilities_and_Spells.md#context-else) | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |

</details>

---

### Context: `Conditional_DestructibleCorpse`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `VaporizeCorpse` | Number | `1` | Applies or references the 'VaporizeCorpse' effect/state. |

</details>

---

### Context: `Conditional_HasCleansableDebuffs`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `GenericBuff` | Number | `5` | Applies or references the 'GenericBuff' effect/state. |
| `PartialCleanse` | Number | `1` | Applies or references the 'PartialCleanse' effect/state. |

</details>

---

### Context: `Conditional_NotBossOrBig`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |

</details>

---

### Context: `Conditional_NotShielded`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Knockback` | Number | `10, 3` | Applies or references the 'Knockback' effect/state. |

</details>

---

### Context: `Conditional_SourceHasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `AlphaCat` | ID of the status effect to apply or check. |

</details>

---

### Context: `CopySpells`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |
| `upgraded` | Boolean | `true` |  |

</details>

---

### Context: `CreateGlobalModifiers`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `BloodRain` | Number | `1` | Applies or references the 'BloodRain' effect/state. |

</details>

---

### Context: `DelayedWindCone`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `5` | The base damage properties of an attack. |
| `distance` | Number | `10` | Distance or area of effect in tiles. |

</details>

---

### Context: `DybbukPossessed`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `exit_ability` | [`Enum/String`](./Enums.md#enum-exit_ability) | `DybbukReturn` |  |
| `punch_self_ability` | [`Enum/String`](./Enums.md#enum-punch_self_ability) | `Dybbuk_StopHittingYourself` |  |

</details>

---

### Context: `ForceAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `immediate` | Boolean | `true` |  |

</details>

---

### Context: `ForceImmediateMoveAndAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `G3GrabHead` | The ability to execute after moving. |
| `even_if_cant_reach` | Boolean | `true` | If true, executes the attack even if the move fails to reach the target. |

</details>

---

### Context: `IncAuxCounterCycle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `change` | Number | `1` |  |
| `max` | Number | `3` |  |

</details>

---

### Context: `KnockOutCoin`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.5` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `Madness`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |
| `tickdown_this_turn` | Boolean | `true` |  |

</details>

---

### Context: `MergeDamageInstance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `can_instapop` | Boolean | `false` | If false, prevents the damage from instantly popping the target. |
| `force_no_hit_animation` | Boolean | `true` | If true, suppresses the flinch/hit animation. |

</details>

---

### Context: `Metronome`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `banned_abilities` | [`Array`](./Arrays.md#array-banned_abilities) | `[ BatteryNuke WeAreOne Metronome SmartMetronome BecomeEnt...` |  |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `NextBattleStatusStacks`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | Number | `2` | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. |
| `fights` | Number | `9999` | The number of encounters this buff/debuff persists for. |

</details>

---

### Context: `ObjectOnHit`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Poop` | The entity ID of the object to spawn (e.g., Poop). |

</details>

---

### Context: `RandomDistanceDisplace`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `min_dist` | Number | `4` | The minimum tile distance they will be moved. |
| `stacks` | Number | `20` | Number of stacks or intensity to apply. |

</details>

---

### Context: `RemoveStatusStacks`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `1` | The number of stacks to remove. |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Brace` | The specific status effect ID to remove. |

</details>

---

### Context: `SetAnimationAlts`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dead` | [`Enum/String`](./Enums.md#enum-dead) | `deadShot` |  |
| `dying` | [`Enum/String`](./Enums.md#enum-dying) | `shot` |  |

</details>

---

### Context: `ShowFakeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `999` | Number of stacks or intensity to apply. |
| `style` | [`Array`](./Arrays.md#array-style) | `[ crit ]` | The visual font style for the text (e.g., [crit]). |

</details>

---

### Context: `SmartMetronome`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `20` | Number of stacks or intensity to apply. |
| `upgraded` | Boolean | `true` |  |

</details>

---

### Context: `SpreadDisease`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `30%` | Probability (0.0 to 1.0 or percentage) of transmitting. |
| `disease` | [`Enum/String`](./Enums.md#enum-disease) | `Cancer` | The specific status effect ID representing the disease. |

</details>

---

### Context: `StatusGroup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageOrHealConditionally` | Number | `1` | Applies or references the 'DamageOrHealConditionally' effect/state. |
| `Freeze` | Number | `2` | Applies or references the 'Freeze' effect/state. |

</details>

---

### Context: `TakeBonusTurnWithAIControl`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | `true` | If true, allows the AI to cast spells during this bonus turn. |

</details>

---

### Context: `Tangled`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `alt_art` | [`Enum/String`](./Enums.md#enum-alt_art) | `TangledMeat` | The alternative sprite art to use while tangled. |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `TransformEquipment`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `from` | [`Enum/String`](./Enums.md#enum-from) | `JarOfChaos` | The original item ID. |
| `to` | [`Enum/String`](./Enums.md#enum-to) | `JarOfNothing` | The new item ID. |

</details>

---

### Context: `TransformWeapon`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `from` | [`Enum/String`](./Enums.md#enum-from) | `Necro_SoulDagger_Uncharged` | The original weapon ID. |
| `to` | [`Enum/String`](./Enums.md#enum-to) | `Necro_SoulDagger_Charged` | The transformed weapon ID. |

</details>

---

### Context: `UseAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `T3Pebbles_BoulderDrop` | The ID of the ability to trigger. |
| `respect_prime` | Boolean | `true` | If true, respects the ability's prime/cooldown state. |

</details>

---

### Context: `UseMoveAbilityWithAI`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `LEPortFar` | ID of the ability to trigger or reference. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_far_move_far` | The AI positioning logic profile to use. |

</details>

---

### Context: `XIsSpellStormRampAndReset`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `reset_percent` | Number | `50%` | The percentage of stacks to keep after resetting. |
| `stacks` | Number | `0` | Number of stacks or intensity to apply. |

</details>

---

### Context: `XIsTargetHealth`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `BonusDamage` | [`Equation`](./Enums.md#enum-mathequation) | `"max(0, floor(X/2)-1)", "max(0, floor(X/6)-1)"` | Applies or references the 'BonusDamage' effect/state. |

</details>

---

### Context: `damage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `none` | Classification/category type. |

</details>

---

### Context: `damage_threshold_altanimations`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `heaviestMelee` | Number | `20` | Animation trigger for massive damage. |
| `heavyMelee` | Number | `10` | Animation trigger if damage exceeds this threshold. |

</details>

---

### Context: `post_spawn_statuses`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `EnterMount` | [`Enum/String`](./Enums.md#enum-entermount) | `enter` | Applies or references the 'EnterMount' effect/state. |
| `VisualFXTile` | [`Enum/String`](./Enums.md#enum-visualfxtile) | `PoisonPoof` | Applies or references the 'VisualFXTile' effect/state. |

</details>

---

### Context: `AlphaStatusOnTurnBegin`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DoubleCastSpellThisTurn` | Number | `1` | Applies or references the 'DoubleCastSpellThisTurn' effect/state. |

</details>

---

### Context: `ApplyPassivesToSpawnerWhileAlive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HideEquipment` | [`Enum/String`](./Enums.md#enum-hideequipment) | `neck` | Applies or references the 'HideEquipment' effect/state. |

</details>

---

### Context: `ApplyStatusesNextTurnBegin`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | `1` | Applies or references the 'Quivered' effect/state. |

</details>

---

### Context: `ApplyToOthersWithSharedTagAndFaction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Marked` | Number | `1` | Applies or references the 'Marked' effect/state. |

</details>

---

### Context: `ApplyToRandomClosestAlly`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | Number | `1` | Applies or references the 'ForceMoveTowards' effect/state. |

</details>

---

### Context: `Cleave`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.25` | Probability (0.0 to 1.0) that the cleave effect triggers. |

</details>

---

### Context: `Conditional_ActiveWeather_Any`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `weather` | [`Array`](./Arrays.md#array-weather) | `[ FlySwarm FireflySwarm ButterflySwarm ]` | An array of weather states to check against. |

</details>

---

### Context: `Conditional_DebuffRoll`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `odds` | Number | `15%` | The probability (0.0 to 1.0) of applying the debuff. |

</details>

---

### Context: `Conditional_FinishedSpawning`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Imprison` | [`Enum/String`](./Enums.md#enum-imprison) | `Fly` | Applies or references the 'Imprison' effect/state. |

</details>

---

### Context: `Conditional_IsSelf`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | Number | `0` | Applies or references the 'OverrideDamage' effect/state. |

</details>

---

### Context: `Conditional_IsTrample`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SetKnockback` | Number | `0` | Applies or references the 'SetKnockback' effect/state. |

</details>

---

### Context: `Conditional_NotAlly`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |

</details>

---

### Context: `Conditional_NotBig`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DisplaceTowardsSource` | Number | `1` | Applies or references the 'DisplaceTowardsSource' effect/state. |

</details>

---

### Context: `Conditional_RandomChance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `odds` | Number | `10%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

### Context: `Conditional_SourceAbilityHasTag`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `weapon_throw` | Specific entity tag required. |

</details>

---

### Context: `PoolMetronome`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | [`Array`](./Arrays.md#array-pool) | `[ Shockwave Ping Telefrag Stasis Reduce Zealot ]` | An array of ability IDs to randomly choose from. |

</details>

---

### Context: `ScrambleLastUsedSpell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `permanent` | Boolean | `true` | If true, the scramble persists for the rest of the run. |

</details>

---

### Context: `StatusKillers`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | `10` | Applies or references the 'Confusion' effect/state. |

</details>

---

### Context: `SwapWeapon`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | [`Array`](./Arrays.md#array-pool) | `[ TerminatorShotgun TerminatorSniper TerminatorUzi ]` | An array of weapon item IDs to draw from. |

</details>

---

### Context: `VisualCountDownThenApplyStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `neck_NukeExplode` | Applies or references the 'ForceUseAbility' effect/state. |

</details>

---

### Context: `bonk_damage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0` | The base damage properties of an attack. |

</details>

---

### Context: `Conditional_CanBeHealed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Conditional_LivingPlayerCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `NukeQuestFinalBossModifications`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `PassiveWhileNotTakingTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `empty_self_damage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

## Cat Classes

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability_pool` | [`Array`](./Arrays.md#array-ability_pool) | `[ ManaBomb SongOfSpring GrantLife SquirrelSquad SummonSqu..., [ HogRush Burp SelfMutilate ForceFeed Fartoom Mutilate Sk..., [ Propell Hadouken Cartwheel StoneFists Transcend HipToss...` |  |
| `attack_pool` | [`Array`](./Arrays.md#array-attack_pool) | `[ BasicDruidAbility ], [ BasicButcherMelee ], [ BasicMonkMelee ]` |  |
| `graphics` | [`Block`](./Cat_Classes.md#context-graphics) | `{ ... }` |  |
| `levelup_stats` | [`Array`](./Arrays.md#array-levelup_stats) | `[ int str lck ], [ cha int str ], [ con str lck ]` |  |
| `meta` | [`Block`](./Cat_Classes.md#context-meta) | `{ ... }` |  |
| `passive_pool` | [`Array`](./Arrays.md#array-passive_pool) | `[ Putrefy NeverFull MainCourse FreshMeat Masochist Glutto..., [ SuperCrow NaturesGuidance PoisonIvy Pathfinder EmptyVes..., [ SafeSwitching Mixup Turnabout MonkeyStyle BrickSkin Jag...` |  |
| `stat_mods` | [`Block`](./Cat_Classes.md#context-stat_mods) | `{ ... }` |  |
| `ability_groups` | [`Block`](./Cat_Classes.md#context-ability_groups) | `{ ... }` |  |
| `starter_abilities` | [`Array`](./Arrays.md#array-starter_abilities) | `[ Propell Pogo ComboThrow ComboPull Bruise Anneal Hadouke..., [ Succ HogRush Chomp BodySlam Vurp Tromp Spoil Grill Shar..., [ SummonSquirrel SummonToad Encourage Protection SongOfSp...` |  |
| `complicated_abilities` | [`Array`](./Arrays.md#array-complicated_abilities) | `[ DealWithTheDevil ForbiddenFlame ForbiddenFlood Forbidde..., [ Extend LastHit StakeOut Diversion ScoutMe CraftArrow Bo..., [ FalconPunch Exert Challenge Stoopzerk Grapple ThinkTooH...` |  |
| `complicated_passives` | [`Array`](./Arrays.md#array-complicated_passives) | `[ ElementalAttunement LatentEnergy MagicGuru One Two Four..., [ Hazardous Traps CatchProjectiles Host SleepDarts Surviv..., [ ShoulderCheck DumbMuscle ThickSkull MostValuableCat Hit...` |  |
| `innate_passives` | [`Block`](./Cat_Classes.md#context-innate_passives) | `{ ... }` |  |
| `innate_items` | [`Block`](./Cat_Classes.md#context-innate_items) | `{ ... }` |  |
| `move_pool` | [`Array`](./Arrays.md#array-move_pool) | `[ DefaultMove ]` |  |
| `tutorial_levelup_active_pool` | [`Array`](./Arrays.md#array-tutorial_levelup_active_pool) | `[ Block LickHeal Dump ]` |  |
| `tutorial_levelup_active_pool_2` | [`Array`](./Arrays.md#array-tutorial_levelup_active_pool_2) | `[ GainThorns ButtScoot Burst HireHitman ]` |  |
| `tutorial_levelup_passive_pool` | [`Array`](./Arrays.md#array-tutorial_levelup_passive_pool) | `[ Furious PressurePoints LateBloomer ZenkaiBoost ]` |  |

</details>

---

### Context: `ability_groups`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Array`](./Arrays.md#array-attack) | `[ SquirrelSquad SummonSquirrel SummonSnake SummonToad Bra..., [ Propell Hadouken HipToss Slapback Finisher ComboThrow C..., [ Fartoom Mutilate SkullBash Shred Chomp BodySlam SliceAn...` |  |
| `misc` | [`Array`](./Arrays.md#array-misc) | `[ SelfMutilate Succ Consume BloodMagic SmellBlood Vurp Li..., [ ManaBomb BattleCry Encourage GrantLife Promote MonkeyFo..., [ StoneFists Bruise TrainArms TrainMind DetectWeakness Ai...` |  |
| `move` | [`Array`](./Arrays.md#array-move) | `[ Cartwheel OneWithTheWind Pogo HopAndBlock TrainLegs Rea..., [ HogRush Trudge LunchTime Tromp CannonBall BadGas Butche..., [ DruidSwap FlowerFeet ThornyFeet RaccoonForm HydroPump C...` |  |
| `defense` | [`Array`](./Arrays.md#array-defense) | `[ Transcend Reverberate Porcupine Anneal DeepDive Meditat..., [ Burp ForceFeed Binge Gib DeliciousScent Tryptophan Regu..., [ SongOfSpring SummonTurtle PullToSafety Protection Safet...` |  |

</details>

---

### Context: `graphics`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `alt_animations` | [`Array`](./Arrays.md#array-alt_animations) | `[ [ idle, ButcherIdle ], [ [ idle, DruidIdle ], [ [ idle, MonkIdle ]` |  |
| `palette` | Number | `66, 64, 65` |  |
| `portrait_face` | [`Enum/String`](./Enums.md#enum-portrait_face) | `butcher_portrait, druid_portrait, monk_portrait` |  |
| `default_face` | [`Enum/String`](./Enums.md#enum-default_face) | `happy` |  |
| `hud_palette` | Number | `11` |  |

</details>

---

### Context: `stat_mods`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2, -2, 3` |  |
| `cha` | Number | `2, 3, -1` |  |
| `int` | Number | `2, 1, 4` |  |
| `spd` | Number | `-2, 1, -1` |  |
| `str` | Number | `-2, 2, -1` |  |
| `dex` | Number | `3, -1` |  |
| `lck` | Number | `2, 1, -1` |  |

</details>

---

### Context: `meta`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `description` | String | `"CAT_CLASS_BUTCHER_DESC", "CAT_CLASS_MONK_DESC", "CAT_CLASS_DRUID_DESC"` |  |
| `name` | String | `"CAT_CLASS_DRUID_NAME", "CAT_CLASS_BUTCHER_NAME", "CAT_CLASS_MONK_NAME"` |  |

</details>

---

### Context: `innate_passives`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddStartingMana` | Number | `5` |  |
| `MonkStances` | [`Array`](./Arrays.md#array-monkstances) | `[ BasicMonkMelee BasicMonkRanged ]` |  |
| `SpawnOnBattleStart` | [`Enum/String`](./Enums.md#enum-spawnonbattlestart) | `Crow` |  |
| `TinkererBasicAttackSwitching` | [`Block`](./Cat_Classes.md#context-tinkererbasicattackswitching) | `{ ... }` |  |

</details>

---

### Context: `innate_items`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Classes.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `weapon` | [`Enum/String`](./Enums.md#enum-weapon) | `ButcherHook, MonkFist` |  |
| `trinket` | [`Enum/String`](./Enums.md#enum-trinket) | `MonkStyleChanger` |  |

</details>

---

### Context: `TinkererBasicAttackSwitching`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`innate_passives`](./Cat_Classes.md#context-innate_passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `craft_ability` | [`Enum/String`](./Enums.md#enum-craft_ability) | `TinkererCraft` |  |
| `throw_ability` | [`Enum/String`](./Enums.md#enum-throw_ability) | `TinkererThrow` |  |

</details>

---

## Cat Mutations

### Context: `passives`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`-2`](./Cat_Mutations.md#context--2), [`1026`](./Cat_Mutations.md#context-1026), [`1029`](./Cat_Mutations.md#context-1029), [`1500`](./Cat_Mutations.md#context-1500), [`300`](./Cat_Mutations.md#context-300), [`301`](./Cat_Mutations.md#context-301), [`302`](./Cat_Mutations.md#context-302), [`303`](./Cat_Mutations.md#context-303), [`304`](./Cat_Mutations.md#context-304), [`305`](./Cat_Mutations.md#context-305), [`306`](./Cat_Mutations.md#context-306), [`307`](./Cat_Mutations.md#context-307), [`308`](./Cat_Mutations.md#context-308), [`309`](./Cat_Mutations.md#context-309), [`310`](./Cat_Mutations.md#context-310), [`311`](./Cat_Mutations.md#context-311), [`312`](./Cat_Mutations.md#context-312), [`313`](./Cat_Mutations.md#context-313), [`314`](./Cat_Mutations.md#context-314), [`315`](./Cat_Mutations.md#context-315), [`316`](./Cat_Mutations.md#context-316), [`317`](./Cat_Mutations.md#context-317), [`318`](./Cat_Mutations.md#context-318), [`319`](./Cat_Mutations.md#context-319), [`320`](./Cat_Mutations.md#context-320), [`321`](./Cat_Mutations.md#context-321), [`322`](./Cat_Mutations.md#context-322), [`323`](./Cat_Mutations.md#context-323), [`324`](./Cat_Mutations.md#context-324), [`325`](./Cat_Mutations.md#context-325), [`326`](./Cat_Mutations.md#context-326), [`327`](./Cat_Mutations.md#context-327), [`328`](./Cat_Mutations.md#context-328), [`329`](./Cat_Mutations.md#context-329), [`330`](./Cat_Mutations.md#context-330), [`331`](./Cat_Mutations.md#context-331), [`332`](./Cat_Mutations.md#context-332), [`333`](./Cat_Mutations.md#context-333), [`334`](./Cat_Mutations.md#context-334), [`335`](./Cat_Mutations.md#context-335), [`336`](./Cat_Mutations.md#context-336), [`337`](./Cat_Mutations.md#context-337), [`338`](./Cat_Mutations.md#context-338), [`339`](./Cat_Mutations.md#context-339), [`340`](./Cat_Mutations.md#context-340), [`341`](./Cat_Mutations.md#context-341), [`342`](./Cat_Mutations.md#context-342), [`343`](./Cat_Mutations.md#context-343), [`344`](./Cat_Mutations.md#context-344), [`345`](./Cat_Mutations.md#context-345), [`346`](./Cat_Mutations.md#context-346), [`347`](./Cat_Mutations.md#context-347), [`348`](./Cat_Mutations.md#context-348), [`349`](./Cat_Mutations.md#context-349), [`351`](./Cat_Mutations.md#context-351), [`352`](./Cat_Mutations.md#context-352), [`353`](./Cat_Mutations.md#context-353), [`442`](./Cat_Mutations.md#context-442), [`702`](./Cat_Mutations.md#context-702), [`703`](./Cat_Mutations.md#context-703), [`704`](./Cat_Mutations.md#context-704), [`705`](./Cat_Mutations.md#context-705), [`706`](./Cat_Mutations.md#context-706), [`707`](./Cat_Mutations.md#context-707), [`750`](./Cat_Mutations.md#context-750), [`751`](./Cat_Mutations.md#context-751), [`752`](./Cat_Mutations.md#context-752), [`753`](./Cat_Mutations.md#context-753), [`754`](./Cat_Mutations.md#context-754), [`755`](./Cat_Mutations.md#context-755), [`756`](./Cat_Mutations.md#context-756), [`757`](./Cat_Mutations.md#context-757), [`758`](./Cat_Mutations.md#context-758), [`759`](./Cat_Mutations.md#context-759), [`760`](./Cat_Mutations.md#context-760), [`761`](./Cat_Mutations.md#context-761), [`762`](./Cat_Mutations.md#context-762), [`763`](./Cat_Mutations.md#context-763), [`900`](./Cat_Mutations.md#context-900), [`PassiveWhenAffectedByElement`](./Cat_Mutations.md#context-passivewhenaffectedbyelement), [`PassiveWhileHasStatus`](./Cat_Mutations.md#context-passivewhilehasstatus)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddStatusToBasicAttack` | [`Block`](./Cat_Mutations.md#context-addstatustobasicattack) | `{ ... }` |  |
| `Thorns` | Number | `2, 1` |  |
| `AddElementsToBasicAttack` | [`Enum/String`](./Enums.md#enum-addelementstobasicattack) | `Electric, Water, Ice` |  |
| `HealthRegenUp` | Number | `2, 1` |  |
| `DodgeChance` | Number | `5%, 10%, 2%` |  |
| `PassiveWhenAffectedByElement` | [`Block`](./Cat_Mutations.md#context-passivewhenaffectedbyelement) | `{ ... }` |  |
| `RevengeDamage` | [`Block`](./Cat_Mutations.md#context-revengedamage) | `{ ... }` |  |
| `MeleeRevengeDamage` | [`Block`](./Cat_Mutations.md#context-meleerevengedamage) | `{ ... }` |  |
| `SpawnOnDowned` | [`Enum/String`](./Enums.md#enum-spawnondowned) | `CharmedFly, CharmedKitten` |  |
| `SpawnThingOnDamage` | [`Block`](./Cat_Mutations.md#context-spawnthingondamage) | `{ ... }` |  |
| `AddBonusRange` | Number | `1` |  |
| `AddStatusToBasicMeleeAttack` | [`Block`](./Cat_Mutations.md#context-addstatustobasicmeleeattack) | `{ ... }` |  |
| `Brace` | Number | `1` |  |
| `StatusOnTookDamage` | [`Block`](./Cat_Mutations.md#context-statusontookdamage) | `{ ... }` |  |
| `StatusEachTurnBegin` | [`Block`](./Cat_Mutations.md#context-statuseachturnbegin) | `{ ... }` |  |
| `WaterWalk` | Number | `1` |  |
| `BlacklistPickupType` | [`Enum/String`](./Enums.md#enum-blacklistpickuptype) | `catnip, food` |  |
| `Bleed` | Number | `1` |  |
| `BleedThorns` | Number | `2, 1` |  |
| `DisableAbilitiesWithTag` | [`Enum/String`](./Enums.md#enum-disableabilitieswithtag) | `musical, consumable` |  |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Electric, Ice` |  |
| `IgnoreTiles` | Number | `1` |  |
| `MulticlassLevelUp` | [`Enum/String`](./Enums.md#enum-multiclasslevelup) | `Fighter, Mage, Hunter` |  |
| `SpawnEachTurn` | [`Block`](./Cat_Mutations.md#context-spawneachturn) | `{ ... }` |  |
| `StatusEachTurnEnd` | [`Block`](./Cat_Mutations.md#context-statuseachturnend) | `{ ... }` |  |
| `AddBonusMeleeRange` | Number | `1` |  |
| `AddCorpseHealth` | Number | `2, 100` |  |
| `AddLevelUpRerolls` | Number | `1` |  |
| `AddManaRegen` | Number | `1` |  |
| `AddMovement` | Number | `1` |  |
| `AllStatsUp` | Number | `1` |  |
| `Blind` | Number | `-1` |  |
| `Bruise` | Number | `2, 1` |  |
| `KineticSpikes` | Number | `1` |  |
| `Quivered` | Number | `1` |  |
| `ReplaceBasicMove` | [`Enum/String`](./Enums.md#enum-replacebasicmove) | `ToadJump_BasicMove, Shadowstep` |  |
| `ReplaceBasicMove_Mutation` | [`Enum/String`](./Enums.md#enum-replacebasicmove_mutation) | `BasicDig, BasicJump` |  |
| `SpawnOnBattleStartRandomEmptyTile` | [`Block`](./Cat_Mutations.md#context-spawnonbattlestartrandomemptytile) | `{ ... }` |  |
| `Trample` | Number | `3` |  |
| `YOffset` | [`Enum/String`](./Enums.md#enum-yoffset) | `.25` |  |
| `AddKnockbackDamage` | Number | `1` |  |
| `BackstabImmunity` | Number | `1` |  |
| `Confusion` | Number | `2` |  |
| `CritChanceUp` | Number | `10, 5` |  |
| `DamageUp` | Number | `2, 1` |  |
| `EquipTemporaryItem` | [`Enum/String`](./Enums.md#enum-equiptemporaryitem) | `Bottles, WaterBottle_Full` |  |
| `HouseFoodRequirementMultiplier` | Number | `0` |  |
| `Immobile` | Number | `1` |  |
| `MissChance` | Number | `10, 20` |  |
| `Poison` | Number | `1` |  |
| `PoisonThorns` | Number | `2, 1` |  |
| `PoopWhenHit` | [`Enum/String`](./Enums.md#enum-poopwhenhit) | `Poop` |  |
| `ReflectProjectiles` | Number | `25%, 10%` |  |
| `ShowHiddenThings` | Number | `1` |  |
| `StatusEveryXSpellCasts` | [`Block`](./Cat_Mutations.md#context-statuseveryxspellcasts) | `{ ... }` |  |
| `StatusKilledCharacters` | [`Block`](./Cat_Mutations.md#context-statuskilledcharacters) | `{ ... }` |  |
| `StatusOnBattleEnd` | [`Block`](./Cat_Mutations.md#context-statusonbattleend) | `{ ... }` |  |
| `StatusOnEndMove` | [`Block`](./Cat_Mutations.md#context-statusonendmove) | `{ ... }` |  |
| `StatusOnTookDamageFromAbility` | [`Block`](./Cat_Mutations.md#context-statusontookdamagefromability) | `{ ... }` |  |
| `Vegan` | Number | `1` |  |
| `AbilityReaction` | [`Enum/String`](./Enums.md#enum-abilityreaction) | `SkunkTail` |  |
| `AbilityWhenTaggedCharacterMovesNear` | [`Block`](./Cat_Mutations.md#context-abilitywhentaggedcharactermovesnear) | `{ ... }` |  |
| `AddDamageToElementDamage` | [`Block`](./Cat_Mutations.md#context-adddamagetoelementdamage) | `{ ... }` |  |
| `AddInitiative` | Number | `-20` |  |
| `AddLootMultiplier` | Number | `1` |  |
| `AddTemporaryEffectsToBasicAttack` | [`Block`](./Cat_Mutations.md#context-addtemporaryeffectstobasicattack) | `{ ... }` |  |
| `AlphaTurns` | Number | `1` |  |
| `BackflipWhenTargeted` | [`Block`](./Cat_Mutations.md#context-backflipwhentargeted) | `{ ... }` |  |
| `BackstabFront` | Number | `1` |  |
| `BasicAttackCantMiss` | Number | `1` |  |
| `BoostWeaponDamage` | Number | `1` |  |
| `CanRemoveCursedItems` | Number | `1` |  |
| `ChanceToBackflip` | [`Block`](./Cat_Mutations.md#context-chancetobackflip) | `{ ... }` |  |
| `ClassManaCostReduction` | [`Block`](./Cat_Mutations.md#context-classmanacostreduction) | `{ ... }` |  |
| `ConjureBonusAbility` | [`Enum/String`](./Enums.md#enum-conjurebonusability) | `random` |  |
| `CounterAttack` | [`Block`](./Cat_Mutations.md#context-counterattack) | `{ ... }` |  |
| `DepressionAura` | Number | `1` |  |
| `DodgeChance_Status` | Number | `10` |  |
| `DrinkWater` | Number | `1` |  |
| `EquipRandomTemporaryItemFromPool` | [`Enum/String`](./Enums.md#enum-equiprandomtemporaryitemfrompool) | `pills` |  |
| `ExtraBasicAttacks` | Number | `2` |  |
| `FlatHealWhenDealDamage` | Number | `1` |  |
| `FreePathfindElement` | [`Enum/String`](./Enums.md#enum-freepathfindelement) | `Water` |  |
| `GainManaWhenAnythingDies` | Number | `1` |  |
| `KnockbackImmunity` | Number | `1` |  |
| `MakeBasicAttackPull` | Number | `1` |  |
| `ManaCostReduction` | Number | `1` |  |
| `MoveAwayFromDamageSource` | [`Enum/String`](./Enums.md#enum-moveawayfromdamagesource) | `BasicJump` |  |
| `MoveWhenDamaged` | [`Block`](./Cat_Mutations.md#context-movewhendamaged) | `{ ... }` |  |
| `PassiveWhenAtFullMana` | [`Block`](./Cat_Mutations.md#context-passivewhenatfullmana) | `{ ... }` |  |
| `PassiveWhileHasStatus` | [`Block`](./Cat_Mutations.md#context-passivewhilehasstatus) | `{ ... }` |  |
| `RandomStatUp` | Number | `1` |  |
| `ReplaceBasicAttack_Mutation` | [`Enum/String`](./Enums.md#enum-replacebasicattack_mutation) | `FetusSpit` |  |
| `Slow` | Number | `-1` |  |
| `SpawnExtraThingsOnBattleStart` | [`Block`](./Cat_Mutations.md#context-spawnextrathingsonbattlestart) | `{ ... }` |  |
| `StatusEachRoundEnd` | [`Block`](./Cat_Mutations.md#context-statuseachroundend) | `{ ... }` |  |
| `StatusEveryXSpellCastsEachTurn` | [`Block`](./Cat_Mutations.md#context-statuseveryxspellcastseachturn) | `{ ... }` |  |
| `StatusIfDidntMove` | [`Block`](./Cat_Mutations.md#context-statusifdidntmove) | `{ ... }` |  |
| `StatusIfUnusedMovePoints` | [`Block`](./Cat_Mutations.md#context-statusifunusedmovepoints) | `{ ... }` |  |
| `StatusImmunity` | [`Array`](./Arrays.md#array-statusimmunity) | `[ Freeze, Slow ]` |  |
| `StatusOnAllyCatDeath` | [`Block`](./Cat_Mutations.md#context-statusonallycatdeath) | `{ ... }` |  |
| `StatusOnCastSpell` | [`Block`](./Cat_Mutations.md#context-statusoncastspell) | `{ ... }` |  |
| `StatusOnDie` | [`Block`](./Cat_Mutations.md#context-statusondie) | `{ ... }` |  |
| `StatusOnEatFood` | [`Block`](./Cat_Mutations.md#context-statusoneatfood) | `{ ... }` |  |
| `StatusOnKill` | [`Block`](./Cat_Mutations.md#context-statusonkill) | `{ ... }` |  |
| `SwapHighestAndLowestStat` | Number | `1` |  |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Knockback` | Number | `2, 1` |  |
| `Bleed` | [`Array`](./Arrays.md#array-bleed) | `[ 3, .1 ], 1` |  |
| `ChangeTile` | [`Enum/String`](./Enums.md#enum-changetile) | `WaterTile, DirtTile` |  |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1 .1 ], [ 1 .15 ], [ 1, .05 ]` |  |
| `Poison` | Number | `1` |  |
| `Burn` | Number | `1` |  |
| `Confusion` | [`Array`](./Arrays.md#array-confusion) | `[ 3, .1 ], [ 2, .15 ], [ 1, .15 ]` |  |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .05 ], [ 1, .05 ]` |  |
| `Bruise` | Number | `1` |  |
| `Leeches` | Number | `1` |  |
| `Slow` | [`Array`](./Arrays.md#array-slow) | `[ 1 .1 ], 1` |  |
| `VisualFXTile` | [`Enum/String`](./Enums.md#enum-visualfxtile) | `fx_windSpell` |  |
| `Charmed` | [`Array`](./Arrays.md#array-charmed) | `[ 1, .10 ]` |  |
| `FaceAway` | Number | `1` |  |
| `FlatLeech` | Number | `1` |  |
| `Freeze` | [`Array`](./Arrays.md#array-freeze) | `[ 1 .01 ]` |  |
| `Immobile` | [`Array`](./Arrays.md#array-immobile) | `[ 1, .05 ]` |  |
| `Instakill` | [`Array`](./Arrays.md#array-instakill) | `[ 25, .01 ]` |  |
| `Petrify` | [`Array`](./Arrays.md#array-petrify) | `[ 1, .05 ]` |  |
| `RandomStatusFromPool` | [`Block`](./Cat_Mutations.md#context-randomstatusfrompool) | `{ ... }` |  |
| `SoulLink` | Number | `1` |  |
| `VaporizeInanimate` | Number | `1` |  |
| `Webbed` | [`Array`](./Arrays.md#array-webbed) | `[ 1 .1 ]` |  |

</details>

---

### Context: `400`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `-1` |  |
| `str` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `401`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `-1` |  |
| `str` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `402`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `-1` |  |
| `str` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `403`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `-1` |  |
| `str` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `404`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spd` | Number | `-1` |  |
| `str` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `405`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `lck` | Number | `-1` |  |
| `str` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `406`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2` |  |
| `str` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `407`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2` |  |
| `dex` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `408`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `-1` |  |
| `con` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `409`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2` |  |
| `int` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `410`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2` |  |
| `spd` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `411`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2` |  |
| `lck` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `412`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `-1` |  |
| `dex` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `413`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `2` |  |
| `str` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `414`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `-1` |  |
| `dex` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `415`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `2` |  |
| `int` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `416`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `2` |  |
| `spd` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `417`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `2` |  |
| `lck` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `418`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `-1` |  |
| `int` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `419`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `-1` |  |
| `int` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `420`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `-1` |  |
| `int` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `421`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `2` |  |
| `str` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `422`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `2` |  |
| `spd` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `423`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `2` |  |
| `lck` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `424`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2` |  |
| `con` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `425`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2` |  |
| `dex` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `426`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2` |  |
| `str` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `427`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2` |  |
| `int` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `428`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2` |  |
| `spd` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `429`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2` |  |
| `lck` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `430`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `-1` |  |
| `lck` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `431`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `-1` |  |
| `lck` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `432`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `-1` |  |
| `lck` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `433`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `-1` |  |
| `lck` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `434`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `lck` | Number | `2` |  |
| `spd` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `435`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `lck` | Number | `2` |  |
| `str` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `436`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `-1` |  |
| `spd` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `437`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spd` | Number | `2` |  |
| `str` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `438`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `-1` |  |
| `spd` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `439`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `-1` |  |
| `spd` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `440`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dex` | Number | `-1` |  |
| `spd` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `441`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `lck` | Number | `-1` |  |
| `spd` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `common` |  |

</details>

---

### Context: `704`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `desc` | String | `"MUTATION_HEAD_704_DESC", "MUTATION_EYES_704_DESC", "MUTATION_EARS_704_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `-2` |  |
| `str` | Number | `1, -1` |  |
| `con` | Number | `2` |  |
| `lck` | Number | `-2` |  |
| `spd` | Number | `-3` |  |

</details>

---

### Context: `703`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `desc` | String | `"MUTATION_EARS_703_DESC", "MUTATION_HEAD_703_DESC", "MUTATION_BODY_703_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `1` |  |
| `cha` | Number | `-2` |  |
| `int` | Number | `-2` |  |
| `spd` | Number | `-2` |  |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `water` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `301`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_BODY_301_DESC", "MUTATION_LEGS_301_DESC", MUTATION_EYEBROWS_301_DESC` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |
| `int` | Number | `1, -1` |  |
| `con` | Number | `1` |  |
| `dex` | Number | `1` |  |
| `spd` | Number | `1` |  |
| `str` | Number | `1` |  |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack), [`StatusOnTookDamageFromAbility`](./Cat_Mutations.md#context-statusontookdamagefromability), [`effects`](./Cat_Mutations.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` |  |
| `Blind` | Number | `1` |  |
| `Burn` | Number | `1` |  |
| `Charge` | Number | `1` |  |
| `DiminishingHealthRegen` | Number | `1` |  |
| `KineticSpikes` | Number | `1` |  |
| `Poison` | Number | `1` |  |
| `RandomStatUp` | Number | `1` |  |
| `Shield` | Number | `1` |  |
| `Thorns` | Number | `1` |  |
| `Weakness` | Number | `1` |  |

</details>

---

### Context: `303`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_303_DESC", "MUTATION_HEAD_303_DESC", "MUTATION_LEGS_303_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `melted, animal` |  |
| `cha` | Number | `1` |  |
| `int` | Number | `1` |  |
| `shield` | Number | `10` |  |
| `spd` | Number | `-2` |  |
| `str` | Number | `1` |  |

</details>

---

### Context: `701`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `cha` | Number | `-2, -1` |  |
| `dex` | Number | `-2, -1` |  |
| `int` | Number | `-2` |  |
| `spd` | Number | `-2, -1` |  |
| `lck` | Number | `-2` |  |
| `shield` | Number | `1` |  |
| `str` | Number | `-1` |  |

</details>

---

### Context: `302`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_302_DESC", "MUTATION_LEGS_302_DESC", "MUTATION_EYES_302_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |
| `shield` | Number | `2, 5` |  |
| `con` | Number | `-1` |  |
| `int` | Number | `2` |  |
| `lck` | Number | `1` |  |
| `spd` | Number | `-1` |  |

</details>

---

### Context: `304`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_HEAD_304_DESC", "MUTATION_EYES_304_DESC", "MUTATION_MOUTH_304_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `melted, animal` |  |
| `cha` | Number | `-2, 1` |  |
| `dex` | Number | `1` |  |
| `int` | Number | `1` |  |
| `spd` | Number | `1` |  |
| `str` | Number | `1` |  |

</details>

---

### Context: `308`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_308_DESC", "MUTATION_MOUTH_308_DESC", "MUTATION_HEAD_308_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `1, -1` |  |
| `lck` | Number | `1` |  |
| `str` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |
| `con` | Number | `1` |  |
| `int` | Number | `-1` |  |

</details>

---

### Context: `313`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | [`Enum/String`](./Enums.md#enum-desc) | `MUTATION_EYEBROWS_313_DESC, "MUTATION_EARS_313_DESC", "MUTATION_BODY_313_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `divine_shield` | Number | `1` |  |
| `shield` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `20%, 100%, 10%` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `SmallRock, CharmedFlea, Coin` |  |
| `good` | Boolean | `false` |  |

</details>

---

### Context: `309`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_BODY_309_DESC", "MUTATION_EARS_309_DESC", MUTATION_EYEBROWS_309_DESC` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |
| `cha` | Number | `1` |  |
| `lck` | Number | `2` |  |

</details>

---

### Context: `314`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_314_DESC", MUTATION_EYEBROWS_314_DESC, "MUTATION_BODY_314_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `-1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `700`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `cha` | Number | `-2` |  |
| `lck` | Number | `-2, -1` |  |
| `con` | Number | `-2` |  |
| `int` | Number | `-2` |  |
| `str` | Number | `-2` |  |

</details>

---

### Context: `300`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal, extra` |  |
| `desc` | String | `"MUTATION_EYES_300_DESC", "MUTATION_TEXTURE_300_DESC", "MUTATION_LEGS_300_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `str` | Number | `1` |  |
| `con` | Number | `1` |  |
| `cha` | Number | `-1` |  |
| `spd` | Number | `1` |  |

</details>

---

### Context: `315`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_BODY_315_DESC", "MUTATION_EARS_315_DESC", MUTATION_EYEBROWS_315_DESC` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `705`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_MOUTH_705_DESC", "MUTATION_EYES_705_DESC", "MUTATION_LEGS_705_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `cha` | Number | `-2, -3` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `FetusSpit` |  |
| `int` | Number | `2` |  |
| `speed` | Number | `-4` |  |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `effects` | [`Block`](./Cat_Mutations.md#context-effects) | `{ ... }` |  |
| `damage` | Number | `0` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status` |  |

</details>

---

### Context: `307`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | [`Enum/String`](./Enums.md#enum-desc) | `MUTATION_EYEBROWS_307_DESC, "MUTATION_EYES_307_DESC", "MUTATION_HEAD_307_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `1` |  |
| `cha` | Number | `1` |  |
| `int` | Number | `1` |  |
| `shield` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `310`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_310_DESC", MUTATION_EYEBROWS_310_DESC, "MUTATION_EYES_310_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal, extra` |  |
| `int` | Number | `1` |  |
| `override_move` | [`Enum/String`](./Enums.md#enum-override_move) | `BasicJump` |  |
| `shield` | Number | `2` |  |

</details>

---

### Context: `702`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `int` | Number | `1, -1` |  |
| `cha` | Number | `1, -1` |  |
| `con` | Number | `-2, -1` |  |
| `desc` | String | `"MUTATION_TEXTURE_702_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `-2` |  |

</details>

---

### Context: `900`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | [`Enum/String`](./Enums.md#enum-desc) | `MUTATION_EYEBROWS_900_DESC, "MUTATION_EYES_900_DESC", "MUTATION_EARS_900_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `1` |  |
| `cha` | Number | `-1` |  |
| `con` | Number | `-2` |  |

</details>

---

### Context: `306`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_MOUTH_306_DESC", "MUTATION_EYES_306_DESC", MUTATION_EYEBROWS_306_DESC` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `1, -3` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |
| `dex` | Number | `1` |  |
| `int` | Number | `1` |  |
| `shield` | Number | `12` |  |
| `spd` | Number | `1` |  |
| `str` | Number | `1` |  |

</details>

---

### Context: `317`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_317_DESC", "MUTATION_BODY_317_DESC", "MUTATION_EARS_317_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `1` |  |

</details>

---

### Context: `318`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_BODY_318_DESC", "MUTATION_EYES_318_DESC", "MUTATION_EARS_318_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |
| `divine_shield` | Number | `1` |  |

</details>

---

### Context: `319`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_BODY_319_DESC", "MUTATION_EARS_319_DESC", "MUTATION_EYES_319_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `305`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_MOUTH_305_DESC", "MUTATION_LEGS_305_DESC", "MUTATION_TAIL_305_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `int` | Number | `1, 3` |  |
| `lck` | Number | `1` |  |
| `cha` | Number | `1` |  |
| `dex` | Number | `-1` |  |
| `shield` | Number | `1` |  |
| `str` | Number | `-1` |  |

</details>

---

### Context: `311`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | [`Enum/String`](./Enums.md#enum-desc) | `MUTATION_EYEBROWS_311_DESC, "MUTATION_HEAD_311_DESC", "MUTATION_EYES_311_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `312`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_312_DESC", "MUTATION_HEAD_312_DESC", "MUTATION_BODY_312_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `divine_shield` | Number | `1` |  |
| `shield` | Number | `1` |  |
| `str` | Number | `1` |  |

</details>

---

### Context: `316`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_316_DESC", "MUTATION_EARS_316_DESC", "MUTATION_HEAD_316_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `-1` |  |
| `shield` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `706`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `desc` | String | `"MUTATION_TEXTURE_706_DESC", "MUTATION_EYES_706_DESC", "MUTATION_HEAD_706_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `-1, -3` |  |
| `spd` | Number | `-1` |  |

</details>

---

### Context: `750`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_HEAD_750_DESC", "MUTATION_EARS_750_DESC", "MUTATION_BODY_750_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `1` |  |
| `int` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `-2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |
| `desc` | String | `"MUTATION_EYES_M2_DESC", "MUTATION_MOUTH_M2_DESC"` |  |
| `dex` | Number | `-2, -1` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `-2` |  |

</details>

---

### Context: `321`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_HEAD_321_DESC", "MUTATION_EARS_321_DESC", "MUTATION_BODY_321_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `int` | Number | `1` |  |
| `shield` | Number | `3` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `extra` |  |

</details>

---

### Context: `754`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_754_DESC", "MUTATION_EARS_754_DESC", "MUTATION_EYES_754_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `1` |  |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | `2, 1` |  |
| `damage` | Number | `0` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status` |  |
| `Freeze` | [`Array`](./Arrays.md#array-freeze) | `[ 1 0.15 ]` |  |
| `Immobile` | Number | `10%` |  |
| `effects` | [`Block`](./Cat_Mutations.md#context-effects) | `{ ... }` |  |

</details>

---

### Context: `322`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_TAIL_322_DESC", "MUTATION_BODY_322_DESC", "MUTATION_MOUTH_322_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `1` |  |
| `con` | Number | `1` |  |
| `str` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `323`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_MOUTH_323_DESC", "MUTATION_BODY_323_DESC", "MUTATION_EARS_323_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `2, -3` |  |

</details>

---

### Context: `325`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_325_DESC", "MUTATION_EARS_325_DESC", "MUTATION_LEGS_325_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `-2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `extra` |  |

</details>

---

### Context: `326`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_326_DESC", "MUTATION_EYES_326_DESC", "MUTATION_LEGS_326_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `327`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_327_DESC", "MUTATION_LEGS_327_DESC", "MUTATION_MOUTH_327_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `cha` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `328`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_328_DESC", "MUTATION_EYES_328_DESC", "MUTATION_EARS_328_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `339`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_339_DESC", "MUTATION_LEGS_339_DESC", "MUTATION_EYES_339_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `bird` |  |

</details>

---

### Context: `effects`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Cat_Mutations.md#context-meleerevengedamage), [`RevengeDamage`](./Cat_Mutations.md#context-revengedamage)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1, .05 ]` |  |
| `Confusion` | [`Array`](./Arrays.md#array-confusion) | `[ 1, .1 ]` |  |
| `Blind` | [`Array`](./Arrays.md#array-blind) | `[ 1, .10 ]` |  |
| `Charmed` | [`Array`](./Arrays.md#array-charmed) | `[ 1, .15 ]` |  |
| `Petrify` | [`Array`](./Arrays.md#array-petrify) | `[ 1, .05 ]` |  |
| `RandomStatusFromPool` | [`Block`](./Cat_Mutations.md#context-randomstatusfrompool) | `{ ... }` |  |

</details>

---

### Context: `320`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_320_DESC", "MUTATION_EARS_320_DESC", "MUTATION_HEAD_320_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `shield` | Number | `1` |  |

</details>

---

### Context: `329`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_329_DESC", "MUTATION_EARS_329_DESC", "MUTATION_LEGS_329_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `331`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_331_DESC", "MUTATION_LEGS_331_DESC", "MUTATION_EYES_331_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `override_move` | [`Enum/String`](./Enums.md#enum-override_move) | `BasicJump` |  |

</details>

---

### Context: `332`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_332_DESC", "MUTATION_LEGS_332_DESC", "MUTATION_EARS_332_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `-1` |  |

</details>

---

### Context: `334`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_334_DESC", "MUTATION_EYES_334_DESC", "MUTATION_EARS_334_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `str` | Number | `1` |  |

</details>

---

### Context: `336`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_336_DESC", "MUTATION_LEGS_336_DESC", "MUTATION_EARS_336_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `bird` |  |

</details>

---

### Context: `337`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_337_DESC", "MUTATION_EARS_337_DESC", "MUTATION_LEGS_337_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `bird` |  |

</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `5%, 25%, 50%` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `RandomPickup, CharmedFly, CharmedMaggot` |  |
| `good` | Boolean | `false` |  |

</details>

---

### Context: `1500`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |
| `desc` | String | `"MUTATION_EARS_1500_DESC", "MUTATION_MOUTH_1500_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `dex` | Number | `1` |  |

</details>

---

### Context: `324`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_MOUTH_324_DESC", "MUTATION_BODY_324_DESC", "MUTATION_EYES_324_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `1` |  |
| `spd` | Number | `2` |  |

</details>

---

### Context: `341`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_341_DESC", "MUTATION_EARS_341_DESC", "MUTATION_LEGS_341_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `755`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_755_DESC", "MUTATION_EARS_755_DESC", "MUTATION_MOUTH_755_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `342`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_TAIL_342_DESC", "MUTATION_EARS_342_DESC", "MUTATION_EYES_342_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `-1` |  |

</details>

---

### Context: `343`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_343_DESC", "MUTATION_EYES_343_DESC", "MUTATION_EARS_343_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `757`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_TAIL_757_DESC", "MUTATION_MOUTH_757_DESC", "MUTATION_LEGS_757_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `int` | Number | `2` |  |

</details>

---

### Context: `759`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_HEAD_759_DESC", "MUTATION_TAIL_759_DESC", "MUTATION_LEGS_759_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `-2` |  |

</details>

---

### Context: `335`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_335_DESC", "MUTATION_EARS_335_DESC", "MUTATION_EYES_335_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `338`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_338_DESC", "MUTATION_EYES_338_DESC", "MUTATION_TAIL_338_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `752`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_MOUTH_752_DESC", "MUTATION_EARS_752_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `753`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_753_DESC", "MUTATION_HEAD_753_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `shield` | Number | `5` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` |  |
| `Knockback` | Number | `1` |  |
| `Immobile` | [`Array`](./Arrays.md#array-immobile) | `[ 1, .1 ]` |  |
| `KnockUpAndAway` | [`Block`](./Cat_Mutations.md#context-knockupandaway) | `{ ... }` |  |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomStatUp` | Number | `2, 1` |  |
| `Charge` | Number | `1` |  |
| `IntelligenceUp` | Number | `1` |  |
| `RandomStatDown` | Number | `1` |  |
| `Shield` | Number | `1` |  |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ScatterCoins` | [`Array`](./Arrays.md#array-scattercoins) | `[ 1 .5 ], 5` |  |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` |  |
| `ChangeTilesUnder` | [`Enum/String`](./Enums.md#enum-changetilesunder) | `GlassTile` |  |
| `LuckUp` | Number | `1` |  |

</details>

---

### Context: `333`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_333_DESC", "MUTATION_LEGS_333_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `shield` | Number | `3` |  |

</details>

---

### Context: `340`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_340_DESC", "MUTATION_LEGS_340_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `divine_shield` | Number | `1` |  |

</details>

---

### Context: `345`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_345_DESC", "MUTATION_EYES_345_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `751`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_751_DESC", "MUTATION_TAIL_751_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `2` |  |

</details>

---

### Context: `758`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_BODY_758_DESC", "MUTATION_LEGS_758_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `con` | Number | `1` |  |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Coin, RandomFoodPickup` |  |
| `number` | Number | `2, [ 1 3 ]` |  |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Quivered` | [`Array`](./Arrays.md#array-quivered) | `[ 1, 0.1 ]` |  |
| `MissChance` | Number | `5` |  |
| `MoveQuivered` | [`Array`](./Arrays.md#array-movequivered) | `[ 1, 0.1 ]` |  |
| `SpeedUp` | Number | `1` |  |

</details>

---

### Context: `330`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EARS_330_DESC", "MUTATION_LEGS_330_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `344`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_344_DESC", "MUTATION_EARS_344_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `442`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `-1` |  |
| `desc` | String | `"MUTATION_EYES_442_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `melted` |  |

</details>

---

### Context: `707`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_707_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `str` | Number | `1` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `birth_defect` |  |

</details>

---

### Context: `756`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_TAIL_756_DESC"` |  |
| `int` | Number | `1` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `spd` | Number | `2` |  |

</details>

---

### Context: `760`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_TAIL_760_DESC", "MUTATION_MOUTH_760_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `Conditional_RandomChance`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusKilledCharacters`](./Cat_Mutations.md#context-statuskilledcharacters)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AutoReanimate` | Number | `50%` |  |
| `odds` | Number | `10%` |  |

</details>

---

### Context: `StatusEveryXSpellCasts`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `8, 4` |  |
| `Charge` | Number | `2` |  |
| `RandomMagicMissile` | Number | `4` |  |

</details>

---

### Context: `1026`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_MOUTH_1026_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `346`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_346_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `shield` | Number | `1` |  |

</details>

---

### Context: `353`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_353_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `animal` |  |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` |  |
| `range` | Number | `2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `food` |  |

</details>

---

### Context: `1029`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_1029_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `347`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_347_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `348`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_348_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `349`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_349_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `351`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_351_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `352`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_EYES_352_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `761`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_761_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `762`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_762_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `763`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"MUTATION_LEGS_763_DESC"` |  |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |

</details>

---

### Context: `AddDamageToElementDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `1` |  |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Electric` |  |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `BackflipDodge` |  |
| `stacks` | Number | `2` |  |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `BackflipDodge` |  |
| `chance` | Number | `10%` |  |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `class` | [`Enum/String`](./Enums.md#enum-class) | `Colorless` |  |
| `reduction` | Number | `1` |  |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ChangeTilesUnder` | [`Enum/String`](./Enums.md#enum-changetilesunder) | `TallGrassTile` |  |
| `odds` | Number | `25%` |  |

</details>

---

### Context: `CounterAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `ChainLightning` |  |
| `chance` | Number | `15%` |  |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddStatusToBasicMeleeAttack`](./Cat_Mutations.md#context-addstatustobasicmeleeattack)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `distance` | Number | `3` |  |
| `stacks` | Number | `3` |  |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `MoveOne` |  |
| `weights` | [`Enum/String`](./Enums.md#enum-weights) | `chaotic` |  |

</details>

---

### Context: `PassiveWhileHasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `passives` | [`Block`](./Cat_Mutations.md#context-passives) | `{ ... }` |  |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Bleed` |  |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `number` | [`Array`](./Arrays.md#array-number) | `[ 1 2 ]` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `RandomPickup` |  |

</details>

---

### Context: `StatusEveryXSpellCastsEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `2` |  |
| `stacks` | Number | `3` |  |

</details>

---

### Context: `StatusKilledCharacters`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_RandomChance` | [`Block`](./Cat_Mutations.md#context-conditional_randomchance) | `{ ... }` |  |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `consumables` |  |
| `PermanentIntelligence` | Number | `1` |  |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_FirstApplicationThisTurn` | [`Block`](./Cat_Mutations.md#context-conditional_firstapplicationthisturn) | `{ ... }` |  |
| `Conditional_GoodRoll` | [`Block`](./Cat_Mutations.md#context-conditional_goodroll) | `{ ... }` |  |

</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomStatusFromPool` | [`Block`](./Cat_Mutations.md#context-randomstatusfrompool) | `{ ... }` |  |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fury` | Number | `10` |  |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` |  |

</details>

---

### Context: `PassiveWhenAtFullMana`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `2` |  |

</details>

---

### Context: `StatusEachRoundEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `UseAbility` | [`Enum/String`](./Enums.md#enum-useability) | `Spit` |  |

</details>

---

### Context: `StatusIfDidntMove`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `3` |  |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | `3` |  |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `2` |  |

</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` |  |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Number | `1` |  |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RangeUp` | Number | `1` |  |

</details>

---

## Characters & Bosses

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `variant_of` | [`Enum/String`](./Enums.md#enum-variant_of) | `BirdSmall, BirdBase, Cherub` |  |
| `scale` | [`Enum/String`](./Enums.md#enum-scale) | `.5` |  |

</details>

---

### Context: `properties`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `faction` | [`Enum/String`](./Enums.md#enum-faction) | `enemies, birds, none` |  |
| `health` | Number | `7, 16, 2` |  |
| `tag` | [`Array`](./Arrays.md#array-tag) | `rat, animal, [ cat blob ]` | Specific entity tag required. |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `boss, object, cat` | Classification/category type. |
| `movement` | Number | `4, 5, 3` |  |
| `corpse_health` | [`Enum/String`](./Enums.md#enum-corpse_health) | `indestructible, 0, 3` |  |
| `inherit_faction` | Boolean | `false, true` |  |
| `dispersed_bonus_turns` | Number | `2, 0, 3` |  |
| `base_mana_regen` | Number | `3, 0, 999` |  |
| `size` | [`Enum/String`](./Enums.md#enum-size) | `gemini, 2x2, 3x3` |  |
| `shield` | Number | `100, 50, 65` |  |
| `move_block` | [`Enum/String`](./Enums.md#enum-move_block) | `everything_even_when_dead, nothing` |  |
| `kill_required` | Boolean | `false, true` |  |
| `can_be_backstabbed` | Boolean | `false` |  |
| `initiative` | Number | `-100, -999, 999` |  |
| `takes_turns` | Boolean | `false, true` |  |
| `mana_regen` | Number | `999` |  |
| `mana` | Number | `100` | Base maximum mana pool. |
| `flying` | Boolean | `true` |  |
| `banned_elite_buffs` | [`Array`](./Arrays.md#array-banned_elite_buffs) | `[ Twin ], [ Mad ], [ Protected ]` |  |
| `hidden_tag` | [`Enum/String`](./Enums.md#enum-hidden_tag) | `the_coven, [ bird bonusbird ], angeljunk` |  |
| `weak_threshold` | Number | `1, 0, 5` |  |
| `knockback_immune` | Boolean | `true` |  |
| `can_be_champion` | Boolean | `false, true` |  |
| `lock_orientation` | [`Array`](./Arrays.md#array-lock_orientation) | `[ -1 0 ], [ 0, -1 ], [ -1, 0 ]` |  |
| `ai_scale` | [`Enum/String`](./Enums.md#enum-ai_scale) | `.5, .25, .01` |  |
| `layer` | [`Enum/String`](./Enums.md#enum-layer) | `pickups, gas, all` |  |
| `auto_run_priority` | [`Enum/String`](./Enums.md#enum-auto_run_priority) | `stationary, support, default` |  |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Rock ], [ Earth ], [ Dust ]` |  |
| `inanimate` | Boolean | `true` |  |
| `disperse_main_turns` | Boolean | `false, true` |  |
| `hidden_tags` | [`Enum/String`](./Enums.md#enum-hidden_tags) | `terminator_mini, [ terminator_mini dc_cat ]` |  |
| `tags` | [`Array`](./Arrays.md#array-tags) | `[ cat robot ]` |  |
| `evenly_dispersed_bonus_turns` | Number | `2, 1, 3` |  |
| `exclude_from_hallucinate` | Boolean | `true` |  |
| `round_end_bonus_turns` | Number | `1` |  |
| `can_be_overkilled` | Boolean | `false, true` |  |
| `can_collect_coins` | Boolean | `false, true` |  |
| `deathpoof_size` | Number | `1` |  |
| `dispersed_bonus_turns_consider_initiative` | Boolean | `false` |  |
| `held_coins` | [`Array`](./Arrays.md#array-held_coins) | `[ 5 10 ], 0, 5` |  |
| `initial_health` | Number | `4, 10, 14` |  |
| `can_eat_food` | Boolean | `false, true` |  |
| `can_grant_extra_turns` | Boolean | `false` |  |
| `tall` | Boolean | `true` |  |
| `dispersed_bonus_turns_before_cats` | Boolean | `false, true` |  |
| `divine_shield` | Number | `2, 1, 3` |  |
| `is_player_cat` | Boolean | `false, true` |  |
| `boss_minions_runaway` | Boolean | `false` |  |
| `mana_matters` | Boolean | `false, true` |  |
| `access_to_player_inventory` | Boolean | `false, true` |  |
| `act_points` | Number | `2, 0, 4` |  |
| `takes_main_turn` | Boolean | `false` |  |
| `visually_spiky` | Boolean | `true` |  |
| `allow_passive_spelltransforming` | Boolean | `true` |  |
| `base_crit_chance` | Number | `0` |  |
| `last_turn_is_main_turn` | Boolean | `true` |  |
| `round_start_bonus_turns` | Number | `1` |  |
| `view_bleeding_characters_as_enemies` | Boolean | `true` |  |
| `aoe_pierce_mode` | [`Enum/String`](./Enums.md#enum-aoe_pierce_mode) | `block` |  |
| `base_initiative` | Number | `0, -1` |  |
| `base_movement` | Number | `4` |  |
| `catdata_ignore_skills` | Boolean | `true` |  |
| `disallow_items` | [`Enum/String`](./Enums.md#enum-disallow_items) | `Nuke, all` |  |
| `always_triggers_traps` | Boolean | `true` |  |
| `base_health` | Number | `0` |  |
| `base_health_regen` | Number | `0` |  |
| `base_initial_mana` | Number | `0` |  |
| `base_mana` | Number | `0` |  |
| `blocking` | Boolean | `false` |  |
| `can_be_elite` | Boolean | `false` |  |
| `can_run` | Boolean | `false` |  |
| `champion` | Boolean | `true` |  |
| `force_not_familiar` | Boolean | `true` |  |
| `hint_no_corpse` | Boolean | `true` |  |
| `must_start_facing_camera` | Boolean | `false` |  |
| `tile_desire_cost` | Number | `200, 100` |  |
| `uncapturable` | Boolean | `false, true` |  |
| `aggro_target_is_enemy` | Boolean | `true` |  |
| `allow_flying_effect` | Boolean | `true` |  |
| `allow_offmap_corpse` | Boolean | `true` |  |
| `allow_replacebrain` | Boolean | `false` |  |
| `always_face_forward` | Boolean | `true` |  |
| `capture_as_cat` | Boolean | `true` |  |
| `elite` | Boolean | `true` |  |
| `first_turn_is_main_turn` | Boolean | `true` |  |
| `ignore_mouseover` | Boolean | `true` |  |
| `ignore_tiles` | Boolean | `true` |  |
| `inanimate_can_receive_specific_statuses` | [`Array`](./Arrays.md#array-inanimate_can_receive_specific_statuses) | `[ Burn ]` |  |
| `mouseover_priority` | Number | `10` |  |
| `move_points` | Number | `2` |  |
| `pickup_type` | Number | `1` |  |
| `scale` | Number | `1.3` |  |
| `speculative_inanimate` | Boolean | `false` |  |
| `static` | Boolean | `true` |  |
| `two_fronts` | Boolean | `true` |  |
| `two_fronts_switch` | Boolean | `true` |  |
| `view_bugs_as_enemies` | Boolean | `true` |  |

</details>

---

### Context: `stats`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `strength` | Number | `8, 5, 4` |  |
| `constitution` | Number | `8, 9, 5` |  |
| `dexterity` | Number | `8, 9, 5` |  |
| `charisma` | Number | `8, 9, 5` |  |
| `intelligence` | Number | `10, 9, 5` |  |
| `speed` | Number | `7, 2, 5` | Base speed/initiative stat. |
| `luck` | Number | `8, 5, 3` |  |

</details>

---

### Context: `graphics`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `name` | String | `"ENEMY_MEDBIRD_NAME", "ENEMY_BIRD_NAME", "ENEMY_LITTLEBIRD_NAME"` | Localization key for the character's name. |
| `movieclip` | [`Enum/String`](./Enums.md#enum-movieclip) | `BirdMed, BirdSmall, BirdLarge` |  |
| `tooltip` | String | `"ENEMY_RADICALRAT_DESC", "ENEMY_BIRD_DESC", "ENEMY_CHERUB_FINALBOSS_DESC"` |  |
| `shadow_size` | Number | `2, .5, 3` |  |
| `scale` | [`Enum/String`](./Enums.md#enum-scale) | `.9, .5, .8` |  |
| `uifloaters_offset` | Number | `2.5, 2, 1.5` |  |
| `custom_cat_data` | [`Enum/String`](./Enums.md#enum-custom_cat_data) | `Kitten, Mangy, TomTom` |  |
| `water_mask` | [`Enum/String`](./Enums.md#enum-water_mask) | `square, medium, medmed` |  |
| `spawnin_animation` | String | `"digUp", digUp, "howl"` |  |
| `alt_animations` | [`Array`](./Arrays.md#array-alt_animations) | `[ [ idle girlyIdle ], [ [ idle twitchyIdle ], [ [ idle cuteIdle ]` |  |
| `piece_alt_frame` | Number | `7, 5, 3` |  |
| `shadow` | [`Enum/String`](./Enums.md#enum-shadow) | `MedSlimeShadow, TormentorShadow, none` |  |
| `move_speed_sync_frames` | Number | `7, 22.5, 40` |  |
| `no_splatter` | Boolean | `true` |  |
| `projectile_spawn_offset` | [`Array`](./Arrays.md#array-projectile_spawn_offset) | `[ 0 1.5 ], [ 0 1 ], [ .25 1 ]` |  |
| `tint` | [`Array`](./Arrays.md#array-tint) | `[ .7 1 .7 1 ], [ 0 0 0 1 ], green` |  |
| `move_speed_multiplier` | [`Enum/String`](./Enums.md#enum-move_speed_multiplier) | `.5, .66, 1.75` |  |
| `dont_sink` | Boolean | `true` |  |
| `art_flip` | Number | `-1` |  |
| `depth_offset` | [`Enum/String`](./Enums.md#enum-depth_offset) | `-.1, 5, .01` |  |
| `walk` | [`Enum/String`](./Enums.md#enum-walk) | `raptorWalk, stompwalk, zombieWalk` |  |
| `dead` | [`Enum/String`](./Enums.md#enum-dead) | `skeletonDead, empty` |  |
| `dying` | [`Enum/String`](./Enums.md#enum-dying) | `dead, dyingDisassembled` |  |
| `four_way_animations` | Boolean | `true` |  |
| `hit` | [`Enum/String`](./Enums.md#enum-hit) | `hitDisassembled, skeletonCorpseHit` |  |
| `stunned` | [`Enum/String`](./Enums.md#enum-stunned) | `dead, idleDisassembled` |  |
| `weak` | [`Enum/String`](./Enums.md#enum-weak) | `dead, idleDisassembled` |  |
| `deadhit` | [`Enum/String`](./Enums.md#enum-deadhit) | `skeletonCorpseHit` |  |
| `show_infinity_damage_warning` | Boolean | `true` |  |
| `always_huge_mask` | Boolean | `true` |  |
| `default_attack_animation` | [`Enum/String`](./Enums.md#enum-default_attack_animation) | `bite1, attack2` |  |
| `desc` | [`Enum/String`](./Enums.md#enum-desc) | `ENEMY_FATWOMAN_DESC, "OBJECT_DECOY_DESC"` | Localization key for the character's desc. |
| `shade_occluded_objects` | Boolean | `true` |  |
| `dodge` | [`Enum/String`](./Enums.md#enum-dodge) | `liquidmetaldodge` |  |
| `no_horizontal_flip` | Boolean | `true` |  |
| `non_blocking_animations` | [`Array`](./Arrays.md#array-non_blocking_animations) | `[ "hit" , "critical" ]` |  |
| `override_portrait` | [`Enum/String`](./Enums.md#enum-override_portrait) | `Cherub` |  |
| `randomize_starting_frame` | Boolean | `false` |  |
| `status_display_count_max` | Number | `5` |  |

</details>

---

### Context: `ai`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `brain` | [`Enum/String`](./Enums.md#enum-brain) | `PatternBrain, PlayerBrain, GenericBrain` |  |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `extra_careless, simple, default` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance_always_move, chaotic_runaway, bird` |  |
| `end_turn_on_formswitch` | Boolean | `false, true` |  |
| `auto_orient` | Boolean | `false` |  |
| `reset_pattern_on_formswitch` | Boolean | `false, true` |  |
| `stun_advances_pattern` | Boolean | `false, true` |  |
| `fallback_advances_pattern` | Boolean | `false, true` |  |
| `consider_spells` | Boolean | `false` |  |
| `animate_choice` | Boolean | `false, true` |  |
| `clamp_pattern` | Boolean | `true` |  |
| `randomize_pattern_start` | Boolean | `true` |  |
| `random_orient` | Boolean | `true` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `JohnnyBlast` |  |
| `dice_abilities` | [`Array`](./Arrays.md#array-dice_abilities) | `[ D6Fizzle D6Confused D6Poop D6Laser D6Quake D6Storm D6Wr...` |  |
| `never_hit_ally_corpses` | Boolean | `true` |  |
| `post_absorb_move_weights` | [`Enum/String`](./Enums.md#enum-post_absorb_move_weights) | `minimum_move` |  |
| `reset_pattern_on_round_begin` | Boolean | `true` |  |
| `roll_ability` | [`Enum/String`](./Enums.md#enum-roll_ability) | `RollDice` |  |

</details>

---

### Context: `abilities`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee, None, DustMelee` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `DustMove, DefaultMove, None` |  |
| `spells` | [`Array`](./Arrays.md#array-spells) | `[ BirdFly ], [ TrampleDash MoveOne ], [ SpawnBomb BombRatTurtle RockToss_BomberRat ]` |  |
| `can_get_bonus` | Boolean | `true` |  |

</details>

---

### Context: `passives`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpawnOnDeath` | [`Block`](./Characters_and_Bosses.md#context-spawnondeath) | `{ ... }, BiggestFood, FrankPinky` | Event Trigger: Spawns a specific entity when killed. |
| `Trample` | Number | `6, 5, 3` | Applies or references the 'Trample' effect/state. |
| `Robot` | [`Block`](./Items_and_Equipment.md#context-robot) | `{ ... }, 1` | Character Form: Behavior and stats for the 'Robot' state. |
| `Brace` | Number | `10, 1, 4` | Applies or references the 'Brace' effect/state. |
| `CounterAttack` | [`Enum/String`](./Enums.md#enum-counterattack) | `YeticatSnowball_Counter, BungaSwipe, attack` | Reaction: Executes a counter-attack ability when hit. |
| `DeathRattle` | [`Block`](./Characters_and_Bosses.md#context-deathrattle) | `{ ... }, BoomerCatExplode, MoonHead_KillHands` | Event Trigger: Executes logic or abilities exactly when the character dies. |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Creep, Fire, Ice` | Applies or references the 'ElementImmune' effect/state. |
| `ImmediateAbilityReaction` | [`Enum/String`](./Enums.md#enum-immediateabilityreaction) | `NubsGoop, ChubsGoop, BumbleButt` | Reaction: Executes an ability instantly, interrupting the current sequence. |
| `Undead` | Number | `1` | Applies or references the 'Undead' effect/state. |
| `AddStatusToBasicAttack` | [`Block`](./Characters_and_Bosses.md#context-addstatustobasicattack) | `{ ... }` | Modifier: Injects a status effect payload into the character's basic attacks. |
| `AbilityReaction` | [`Block`](./Characters_and_Bosses.md#context-abilityreaction) | `{ ... }, TC_DashReaction, attack` | AI Trigger: Executes an ability in reaction to a specific event (e.g., taking damage). |
| `StatusImmunity` | [`Enum/String`](./Enums.md#enum-statusimmunity) | `Webbed, Poison, [ Poison, Bleed ]` | Applies or references the 'StatusImmunity' effect/state. |
| `Buddy` | [`Enum/String`](./Enums.md#enum-buddy) | `Nubs, Ornstein, Smough` | Character Form / AI State: Behavior and stats for the 'Buddy' familiar state. |
| `AddMovement` | Number | `-2, 2, 1` | Applies or references the 'AddMovement' effect/state. |
| `Thorns` | Number | `2, 5, 3` | Applies or references the 'Thorns' effect/state. |
| `TransformOnDeath` | [`Enum/String`](./Enums.md#enum-transformondeath) | `RatKing, SimonFlopper, Carcus` | Applies or references the 'TransformOnDeath' effect/state. |
| `NoHealthOnlyShield` | Number | `1` | Applies or references the 'NoHealthOnlyShield' effect/state. |
| `WaterWalk` | Number | `1` | Applies or references the 'WaterWalk' effect/state. |
| `CoinPickup` | Number | `2, 1, 3` | Applies or references the 'CoinPickup' effect/state. |
| `LimitDamage` | Number | `1` | Applies or references the 'LimitDamage' effect/state. |
| `MoveWhenDamaged` | [`Block`](./Characters_and_Bosses.md#context-movewhendamaged) | `{ ... }, move, TKNG_Hop` | AI Movement: Forces a reposition when taking damage. |
| `StripStatuses` | Number | `1` | Applies or references the 'StripStatuses' effect/state. |
| `LimitHeal` | Number | `1, 0` | Applies or references the 'LimitHeal' effect/state. |
| `ReflectProjectiles` | [`Block`](./Characters_and_Bosses.md#context-reflectprojectiles) | `{ ... }, 100%, 1` | Passive: Reflects incoming projectiles back at the attacker. |
| `BackstabImmunity` | Number | `1` | Applies or references the 'BackstabImmunity' effect/state. |
| `FadeInsteadOfDie` | Number | `1` | Applies or references the 'FadeInsteadOfDie' effect/state. |
| `Plant` | Number | `1` | Applies or references the 'Plant' effect/state. |
| `RandomizeAIWeightsEachTurn` | [`Array`](./Arrays.md#array-randomizeaiweightseachturn) | `[ { decision_weights default move_weights keep_distance }..., [ { decision_weights blind move_weights chubs_and_nubs_bl..., [ { decision_weights default move_weights stay_close } { ...` | Applies or references the 'RandomizeAIWeightsEachTurn' effect/state. |
| `SmallRockBehavior` | [`Block`](./Characters_and_Bosses.md#context-smallrockbehavior) | `{ ... }, 0, 5` | AI Logic: Movement/interaction profile for small rocks. |
| `AbilityWhenBuddyDies` | [`Enum/String`](./Enums.md#enum-abilitywhenbuddydies) | `GirlDinoCry, ChubsRage, Guillotina2Rage` | Applies or references the 'AbilityWhenBuddyDies' effect/state. |
| `TransformInXTurns` | [`Block`](./Characters_and_Bosses.md#context-transforminxturns) | `{ ... }` | Logic: Forces a form change after X turns. |
| `AddDamage` | Number | `2, 1, 4` | Applies or references the 'AddDamage' effect/state. |
| `Divide4OnDeath` | [`Enum/String`](./Enums.md#enum-divide4ondeath) | `BiggestFood, MedSlime, Clot` | Applies or references the 'Divide4OnDeath' effect/state. |
| `HealthGain` | Number | `8, 1, 5` | Applies or references the 'HealthGain' effect/state. |
| `InnateElement` | [`Enum/String`](./Enums.md#enum-innateelement) | `Water, Fire` | Applies or references the 'InnateElement' effect/state. |
| `KaijuKnockbackImmune` | Number | `1` | Applies or references the 'KaijuKnockbackImmune' effect/state. |
| `MoveTowardsDamageSource` | [`Block`](./Characters_and_Bosses.md#context-movetowardsdamagesource) | `{ ... }, MoveOne` | AI Movement: Closes distance on the last source of damage. |
| `OverrideMaxHealth` | Number | `1, 25` | Applies or references the 'OverrideMaxHealth' effect/state. |
| `TagGreed` | [`Enum/String`](./Enums.md#enum-taggreed) | `pickup, bishop_hat, food` | Applies or references the 'TagGreed' effect/state. |
| `YOffset` | [`Enum/String`](./Enums.md#enum-yoffset) | `.35, -.18` | Applies or references the 'YOffset' effect/state. |
| `Angel` | Number | `1` | Applies or references the 'Angel' effect/state. |
| `DebuffImmunity` | Number | `1` | Applies or references the 'DebuffImmunity' effect/state. |
| `KineticSpikes` | Number | `1, 5` | Applies or references the 'KineticSpikes' effect/state. |
| `MinimumKnockbackFromAllDamage` | Number | `1` | Applies or references the 'MinimumKnockbackFromAllDamage' effect/state. |
| `MoveTowardsKillers` | [`Block`](./Characters_and_Bosses.md#context-movetowardskillers) | `{ ... }, ReaperRevenge` | AI Movement: Seeks out entities that have recently killed an ally. |
| `StartOffMap` | Number | `1` | Applies or references the 'StartOffMap' effect/state. |
| `TransformOnDeathImmediately` | [`Block`](./Characters_and_Bosses.md#context-transformondeathimmediately) | `{ ... }, NoHead` | Logic: Bypasses death sequence to instantly assume a new form. |
| `AbilityAfterEnemyCastSpell_Stackable` | [`Enum/String`](./Enums.md#enum-abilityafterenemycastspell_stackable) | `ThornUpX, ThornUp` | Applies or references the 'AbilityAfterEnemyCastSpell_Stackable' effect/state. |
| `AddMaxHealth` | Number | `5` | Applies or references the 'AddMaxHealth' effect/state. |
| `AddMeleeKnockback` | Number | `2, 1, 10` | Applies or references the 'AddMeleeKnockback' effect/state. |
| `Ammo` | Number | `6, 1, 3` | Applies or references the 'Ammo' effect/state. |
| `BackstabAllDirections` | Number | `1` | Applies or references the 'BackstabAllDirections' effect/state. |
| `Bird` | [`Enum/String`](./Enums.md#enum-bird) | `CookedChickenLeg` | Applies or references the 'Bird' effect/state. |
| `ChangeTileOnPop` | [`Enum/String`](./Enums.md#enum-changetileonpop) | `GlitchTile, OilTile, CreepTile` | Applies or references the 'ChangeTileOnPop' effect/state. |
| `CountAsCorpse` | Number | `1` | Applies or references the 'CountAsCorpse' effect/state. |
| `DisplayDangerAOE` | [`Enum/String`](./Enums.md#enum-displaydangeraoe) | `TheChild_Wrath, MoonHead_Blow, attack` | Applies or references the 'DisplayDangerAOE' effect/state. |
| `GroundFlopper` | [`Enum/String`](./Enums.md#enum-groundflopper) | `MoveOne, DefaultMove` | Applies or references the 'GroundFlopper' effect/state. |
| `IgnoreTiles` | Number | `1` | Applies or references the 'IgnoreTiles' effect/state. |
| `LoopingSoundWhileAlive` | [`Enum/String`](./Enums.md#enum-loopingsoundwhilealive) | `Twister_loop, BigUFO_ambient_looping, Bomb_FuseLoop` | Applies or references the 'LoopingSoundWhileAlive' effect/state. |
| `PrioritizeFarAwayTargets` | Number | `10, 1` | Applies or references the 'PrioritizeFarAwayTargets' effect/state. |
| `SharkySmellsBlood` | Number | `1` | Applies or references the 'SharkySmellsBlood' effect/state. |
| `StunImmunity` | [`Block`](./Characters_and_Bosses.md#context-stunimmunity) | `{ ... }, 1` | Passive: Prevents Stun from being applied. |
| `WeremanTransformationReceiver` | [`Enum/String`](./Enums.md#enum-weremantransformationreceiver) | `CaveWomanDropTransform, CaveManTransform` | Applies or references the 'WeremanTransformationReceiver' effect/state. |
| `AddHiddenTag` | [`Enum/String`](./Enums.md#enum-addhiddentag) | `unlit_candle, grown_hitler_clone, hitler_clone_fetus` | Applies or references the 'AddHiddenTag' effect/state. |
| `AddInitiative` | Number | `-10, -9999, 999999` | Applies or references the 'AddInitiative' effect/state. |
| `AddTag` | [`Enum/String`](./Enums.md#enum-addtag) | `tumor, fetus, cat` | Applies or references the 'AddTag' effect/state. |
| `AggroTargetIsCurrentTurn` | Number | `1` | Applies or references the 'AggroTargetIsCurrentTurn' effect/state. |
| `BaseStatMultiply` | [`Enum/String`](./Enums.md#enum-basestatmultiply) | `.666, .5, .25` | Applies or references the 'BaseStatMultiply' effect/state. |
| `BonusTurnPattern` | [`Array`](./Arrays.md#array-bonusturnpattern) | `[ { dispersed_bonus_turns 2 round_end_bonus_turns 1 } { r..., [ { evenly_dispersed_bonus_turns 0 round_end_bonus_turns ..., [ { evenly_dispersed_bonus_turns 1 round_end_bonus_turns ...` | Applies or references the 'BonusTurnPattern' effect/state. |
| `CanMutateTo` | [`Array`](./Arrays.md#array-canmutateto) | `[ TumorousMaggot, ChargeyMaggot, SwappyMaggot ], Hyde, [ Lumpy, Leaper ]` | Applies or references the 'CanMutateTo' effect/state. |
| `DigestDeadBodies` | [`Enum/String`](./Enums.md#enum-digestdeadbodies) | `MoonHead_Digest, Digest, LennyCatDies` | Applies or references the 'DigestDeadBodies' effect/state. |
| `FaceShield` | Number | `0` | Applies or references the 'FaceShield' effect/state. |
| `InjuryImmunity` | Number | `1` | Applies or references the 'InjuryImmunity' effect/state. |
| `MimicSpawnerAttacks` | Number | `1, -1` | Applies or references the 'MimicSpawnerAttacks' effect/state. |
| `MinimumKnockbackFromPhysicalAttacks` | Number | `1` | Applies or references the 'MinimumKnockbackFromPhysicalAttacks' effect/state. |
| `MutateViaAbility` | [`Enum/String`](./Enums.md#enum-mutateviaability) | `BBTransformMutant` | Applies or references the 'MutateViaAbility' effect/state. |
| `PrioritizeHitDifferentTargets` | Number | `1` | Applies or references the 'PrioritizeHitDifferentTargets' effect/state. |
| `RunInXTurns` | Number | `2, 1, 3` | Applies or references the 'RunInXTurns' effect/state. |
| `SharePickupsWithSpawner` | Number | `0, 1` | Applies or references the 'SharePickupsWithSpawner' effect/state. |
| `SpawnThingOnDeath` | [`Enum/String`](./Enums.md#enum-spawnthingondeath) | `Boulder, Food, Gamete` | Applies or references the 'SpawnThingOnDeath' effect/state. |
| `SpeedUp` | Number | `6, 2` | Applies or references the 'SpeedUp' effect/state. |
| `SupportFormChangeInsteadOfRun` | [`Block`](./Characters_and_Bosses.md#context-supportformchangeinsteadofrun) | `{ ... }, Attacker` | AI Logic: Forces a support unit to transform rather than flee. |
| `TileTrail_Ahead` | [`Enum/String`](./Enums.md#enum-tiletrail_ahead) | `WaterTile, FireTile, OilTile` | Applies or references the 'TileTrail_Ahead' effect/state. |
| `WeaponsDontLoseDurability` | Number | `1` | Applies or references the 'WeaponsDontLoseDurability' effect/state. |
| `AddCorpseHealth` | Number | `-999` | Applies or references the 'AddCorpseHealth' effect/state. |
| `AggroTargetIsBuddy` | Number | `1` | Applies or references the 'AggroTargetIsBuddy' effect/state. |
| `AllDamageImmune_IncludingSpeculative` | Number | `1` | Applies or references the 'AllDamageImmune_IncludingSpeculative' effect/state. |
| `AlphaTurns` | Number | `1` | Applies or references the 'AlphaTurns' effect/state. |
| `AlwaysHitDifferentTargets` | Number | `1` | Applies or references the 'AlwaysHitDifferentTargets' effect/state. |
| `BuffImmunity` | Number | `1` | Applies or references the 'BuffImmunity' effect/state. |
| `CanShield` | Number | `1` | Applies or references the 'CanShield' effect/state. |
| `ChanceToDisableActionsIfNotCharmed` | Number | `75%` | Applies or references the 'ChanceToDisableActionsIfNotCharmed' effect/state. |
| `ChangeTileOnDeath` | [`Enum/String`](./Enums.md#enum-changetileondeath) | `WaterTile` | Applies or references the 'ChangeTileOnDeath' effect/state. |
| `DemonicGlyphFrames` | Number | `1` | Applies or references the 'DemonicGlyphFrames' effect/state. |
| `DiesToElement` | [`Block`](./Characters_and_Bosses.md#context-diestoelement) | `{ ... }, Wind` | Vulnerability: Character dies instantly if hit by this element. |
| `DissuadeInstakills` | Number | `1` | Applies or references the 'DissuadeInstakills' effect/state. |
| `DodgeChance_Status` | Number | `66, 100` | Applies or references the 'DodgeChance_Status' effect/state. |
| `ExpireOnSpawnerTurnEnd` | Number | `1` | Applies or references the 'ExpireOnSpawnerTurnEnd' effect/state. |
| `ExtraDispersedTurns` | Number | `1` | Applies or references the 'ExtraDispersedTurns' effect/state. |
| `FaceLastDamage` | [`Block`](./Characters_and_Bosses.md#context-facelastdamage) | `{ ... }, 1` | Reaction: Forces the character to face towards the last damage source. |
| `FinalBossShield` | [`Enum/String`](./Enums.md#enum-finalbossshield) | `DestroyerShieldBash, None` | Applies or references the 'FinalBossShield' effect/state. |
| `Flying` | Number | `1` | Applies or references the 'Flying' effect/state. |
| `GoopWalk` | Number | `1` | Applies or references the 'GoopWalk' effect/state. |
| `HealthRegenUp` | Number | `2, 4` | Applies or references the 'HealthRegenUp' effect/state. |
| `ImmobilePassive` | Number | `1` | Applies or references the 'ImmobilePassive' effect/state. |
| `KaijuWinCon` | [`Enum/String`](./Enums.md#enum-kaijuwincon) | `zaratana, pyrophina` | Applies or references the 'KaijuWinCon' effect/state. |
| `MagicDamageImmune` | Number | `1` | Applies or references the 'MagicDamageImmune' effect/state. |
| `MamaCatAnimations` | Number | `1` | Applies or references the 'MamaCatAnimations' effect/state. |
| `MiniVolcanoReaction` | [`Enum/String`](./Enums.md#enum-minivolcanoreaction) | `MiniVolcano_Spurt, ThrobShot_Reaction` | Applies or references the 'MiniVolcanoReaction' effect/state. |
| `PermanentMadness` | Number | `1` | Applies or references the 'PermanentMadness' effect/state. |
| `PrioritizeAggroTarget` | Number | `1` | Applies or references the 'PrioritizeAggroTarget' effect/state. |
| `PrioritizePlayerCats` | Number | `1` | Applies or references the 'PrioritizePlayerCats' effect/state. |
| `PrioritizeWeakestEnemy` | Number | `1` | Applies or references the 'PrioritizeWeakestEnemy' effect/state. |
| `SafeDoomed` | Number | `1` | Applies or references the 'SafeDoomed' effect/state. |
| `SpawnCreepOnHit` | Number | `1` | Applies or references the 'SpawnCreepOnHit' effect/state. |
| `SurviveAt1HP` | Number | `1` | Applies or references the 'SurviveAt1HP' effect/state. |
| `TileTrail` | [`Enum/String`](./Enums.md#enum-tiletrail) | `ShadowTile, CreepTile` | Applies or references the 'TileTrail' effect/state. |
| `TransformWhenBuddyDies` | [`Enum/String`](./Enums.md#enum-transformwhenbuddydies) | `UltraOrnstein, UltraSmough` | Applies or references the 'TransformWhenBuddyDies' effect/state. |
| `UnlockOrientation` | Number | `1` | Applies or references the 'UnlockOrientation' effect/state. |
| `UseAbility` | [`Enum/String`](./Enums.md#enum-useability) | `TormentorRuneAbsorb, MegaGuppy_SummonTheChild` | Logic: Forces execution of an ability. |
| `AbilityOnBattleStart_UseAI` | [`Enum/String`](./Enums.md#enum-abilityonbattlestart_useai) | `TheCreator_SpawnCloneTeam` | Applies or references the 'AbilityOnBattleStart_UseAI' effect/state. |
| `AddElementsToBasicAttack` | [`Enum/String`](./Enums.md#enum-addelementstobasicattack) | `Fire` | Applies or references the 'AddElementsToBasicAttack' effect/state. |
| `AdvancedTint` | [`Array`](./Arrays.md#array-advancedtint) | `[ .6, .6, .6, 1 .5, .5, .5, 0 ]` | Applies or references the 'AdvancedTint' effect/state. |
| `AggroTargetIsLastEnemyThatDealtDamage` | Number | `1` | Applies or references the 'AggroTargetIsLastEnemyThatDealtDamage' effect/state. |
| `AggroTargetIsLowestHealthEnemyTillItDies` | Number | `1` | Applies or references the 'AggroTargetIsLowestHealthEnemyTillItDies' effect/state. |
| `AggroTargetIsLowestMaxHealthCat` | Number | `1` | Applies or references the 'AggroTargetIsLowestMaxHealthCat' effect/state. |
| `AlienBeastDangerZones` | [`Array`](./Arrays.md#array-alienbeastdangerzones) | `[ AlienBeastScream AlienBeastEat AlienBeastPuke AlienBeas...` | Applies or references the 'AlienBeastDangerZones' effect/state. |
| `AlienBeastEyeStalks` | Number | `3` | Applies or references the 'AlienBeastEyeStalks' effect/state. |
| `AllSpellsCostActPoints` | Number | `1` | Applies or references the 'AllSpellsCostActPoints' effect/state. |
| `AllStatsUp` | Number | `2` | Applies or references the 'AllStatsUp' effect/state. |
| `AvoidDamagingCharmedEnemies` | Number | `1` | Applies or references the 'AvoidDamagingCharmedEnemies' effect/state. |
| `AwardCoinsOnDeath` | Number | `10` | Applies or references the 'AwardCoinsOnDeath' effect/state. |
| `BasicAIDangerZone` | Number | `2` | Applies or references the 'BasicAIDangerZone' effect/state. |
| `BlackHolePassive` | Number | `1` | Applies or references the 'BlackHolePassive' effect/state. |
| `BloatEyePassive2` | [`Enum/String`](./Enums.md#enum-bloateyepassive2) | `BloatEyeMovement2` | Applies or references the 'BloatEyePassive2' effect/state. |
| `BlockAllDamage` | Number | `1` | Applies or references the 'BlockAllDamage' effect/state. |
| `BombBehavior` | Number | `1` | Applies or references the 'BombBehavior' effect/state. |
| `Burn` | Number | `3` | Applies or references the 'Burn' effect/state. |
| `CCImmunity` | Number | `1` | Applies or references the 'CCImmunity' effect/state. |
| `CapReceivedDamage` | Number | `1` | Applies or references the 'CapReceivedDamage' effect/state. |
| `ConjureBonusAbility` | [`Enum/String`](./Enums.md#enum-conjurebonusability) | `random` | Adds a temporary bonus ability to the character's hand/deck. |
| `CounterAttackAfterEnemyCastSpell` | [`Enum/String`](./Enums.md#enum-counterattackafterenemycastspell) | `Telekinesis` | Applies or references the 'CounterAttackAfterEnemyCastSpell' effect/state. |
| `CrowAttackLink` | Number | `1` | Applies or references the 'CrowAttackLink' effect/state. |
| `DamageFromBehindOnly` | Number | `1` | Applies or references the 'DamageFromBehindOnly' effect/state. |
| `DemonicGlyphStealer` | Number | `1` | Applies or references the 'DemonicGlyphStealer' effect/state. |
| `DicerArt` | [`Array`](./Arrays.md#array-dicerart) | `[ 59 52 65 50 54 63 64 ]` | Applies or references the 'DicerArt' effect/state. |
| `DieWhenOnlyGolemsLeft` | Number | `1` | Applies or references the 'DieWhenOnlyGolemsLeft' effect/state. |
| `DieWhenSpawnerDies` | Number | `1` | Applies or references the 'DieWhenSpawnerDies' effect/state. |
| `DisableSpells` | Number | `1` | Applies or references the 'DisableSpells' effect/state. |
| `Disguised` | Number | `1` | Applies or references the 'Disguised' effect/state. |
| `DisguisedTrapper` | [`Enum/String`](./Enums.md#enum-disguisedtrapper) | `FearMelee` | Applies or references the 'DisguisedTrapper' effect/state. |
| `DisplayBuddyCatOnSpawn` | Number | `3` | Applies or references the 'DisplayBuddyCatOnSpawn' effect/state. |
| `DivineShield` | Number | `2` | Applies or references the 'DivineShield' effect/state. |
| `DivineShieldPickup` | Number | `1` | Applies or references the 'DivineShieldPickup' effect/state. |
| `DodgeChance` | Number | `50%` | Applies or references the 'DodgeChance' effect/state. |
| `DodgeChanceWithBlindSpot` | Number | `25%` | Applies or references the 'DodgeChanceWithBlindSpot' effect/state. |
| `DustCloudBehavior` | Number | `1` | Applies or references the 'DustCloudBehavior' effect/state. |
| `Dybbuk1HPTracker` | Number | `1` | Applies or references the 'Dybbuk1HPTracker' effect/state. |
| `ElectricArcs` | Number | `1` | Applies or references the 'ElectricArcs' effect/state. |
| `ElementWeakness` | [`Enum/String`](./Enums.md#enum-elementweakness) | `Fire` | Applies or references the 'ElementWeakness' effect/state. |
| `EnrageOnDamage` | Number | `1` | Applies or references the 'EnrageOnDamage' effect/state. |
| `EraseSpawnCoins` | Number | `1` | Applies or references the 'EraseSpawnCoins' effect/state. |
| `EventBounterHunterPassive` | Number | `1` | Applies or references the 'EventBounterHunterPassive' effect/state. |
| `ExtraMovePoints` | Number | `1` | Applies or references the 'ExtraMovePoints' effect/state. |
| `ExtraTurnsPerTaggedUnit` | [`Enum/String`](./Enums.md#enum-extraturnspertaggedunit) | `sprout` | Applies or references the 'ExtraTurnsPerTaggedUnit' effect/state. |
| `FlingObjectsOnTop` | Number | `8` | Applies or references the 'FlingObjectsOnTop' effect/state. |
| `FlushmasterCelebration` | [`Enum/String`](./Enums.md#enum-flushmastercelebration) | `celebrate` | Applies or references the 'FlushmasterCelebration' effect/state. |
| `ForceDodgeEverything` | Number | `1` | Applies or references the 'ForceDodgeEverything' effect/state. |
| `FormChangeWhenBuddyDies` | [`Enum/String`](./Enums.md#enum-formchangewhenbuddydies) | `Rage` | Applies or references the 'FormChangeWhenBuddyDies' effect/state. |
| `FreePathfindElement` | [`Enum/String`](./Enums.md#enum-freepathfindelement) | `Water` | Applies or references the 'FreePathfindElement' effect/state. |
| `FullBlockEverything` | Number | `1` | Applies or references the 'FullBlockEverything' effect/state. |
| `FullBlockEverythingTo0Damage` | Number | `1` | Applies or references the 'FullBlockEverythingTo0Damage' effect/state. |
| `GasCanBehavior` | Number | `1` | Applies or references the 'GasCanBehavior' effect/state. |
| `GasCloudBehavior2` | Number | `2` | Applies or references the 'GasCloudBehavior2' effect/state. |
| `GeminiTwin` | Number | `1` | Applies or references the 'GeminiTwin' effect/state. |
| `GlobalManaDrainAura` | Number | `-1` | Applies or references the 'GlobalManaDrainAura' effect/state. |
| `GoopImmunity` | Number | `1` | Applies or references the 'GoopImmunity' effect/state. |
| `GuillotinaDeathHead` | Number | `1` | Applies or references the 'GuillotinaDeathHead' effect/state. |
| `HarpoonTrapPassive` | [`Enum/String`](./Enums.md#enum-harpoontrappassive) | `HarpoonTrapPull` | Applies or references the 'HarpoonTrapPassive' effect/state. |
| `HiddenDoomed` | Number | `2` | Applies or references the 'HiddenDoomed' effect/state. |
| `IceBlockBehavior` | Number | `1` | Applies or references the 'IceBlockBehavior' effect/state. |
| `IllusionTint` | Number | `1` | Applies or references the 'IllusionTint' effect/state. |
| `InheritSpawnerStats` | Number | `1` | Applies or references the 'InheritSpawnerStats' effect/state. |
| `InsertIntoBackgroundPlaceholder` | Number | `1` | Applies or references the 'InsertIntoBackgroundPlaceholder' effect/state. |
| `JohnnyWasher` | [`Enum/String`](./Enums.md#enum-johnnywasher) | `BBTransformZealot` | Applies or references the 'JohnnyWasher' effect/state. |
| `KnockbackImmunity` | Number | `1` | Applies or references the 'KnockbackImmunity' effect/state. |
| `LegacySpawnSavedCatIfExists` | [`Enum/String`](./Enums.md#enum-legacyspawnsavedcatifexists) | `Legacy_Marshmallow_StolenCatID` | Applies or references the 'LegacySpawnSavedCatIfExists' effect/state. |
| `LockOrientationFaceTile` | [`Array`](./Arrays.md#array-lockorientationfacetile) | `[ 0 0 ]` | Applies or references the 'LockOrientationFaceTile' effect/state. |
| `ManglerMonsterPassive` | [`Enum/String`](./Enums.md#enum-manglermonsterpassive) | `ManglerMonsterDashAttack` | Applies or references the 'ManglerMonsterPassive' effect/state. |
| `MissChance` | Number | `20` | Applies or references the 'MissChance' effect/state. |
| `MoonHeadCrackedVisual` | [`Enum/String`](./Enums.md#enum-moonheadcrackedvisual) | `Cracked` | Applies or references the 'MoonHeadCrackedVisual' effect/state. |
| `MulticatHeads` | Number | `0` | Applies or references the 'MulticatHeads' effect/state. |
| `MutateAfterXTurns` | Number | `3` | Applies or references the 'MutateAfterXTurns' effect/state. |
| `MuteDemonicGlyphDisplay` | Number | `1` | Applies or references the 'MuteDemonicGlyphDisplay' effect/state. |
| `OrthogonalAIDangerZone` | Number | `10` | Applies or references the 'OrthogonalAIDangerZone' effect/state. |
| `PackHunting` | Number | `1` | Applies or references the 'PackHunting' effect/state. |
| `Phasing` | Number | `1` | Applies or references the 'Phasing' effect/state. |
| `PoisonThorns` | Number | `3` | Applies or references the 'PoisonThorns' effect/state. |
| `ReturnBoundItemOnBattleEnd` | Number | `1` | Applies or references the 'ReturnBoundItemOnBattleEnd' effect/state. |
| `RunWhenKittensDead` | Number | `1` | Applies or references the 'RunWhenKittensDead' effect/state. |
| `SetSpellCosts` | Number | `0` | Applies or references the 'SetSpellCosts' effect/state. |
| `SpawnCreepOnHitKnockback` | Number | `1` | Applies or references the 'SpawnCreepOnHitKnockback' effect/state. |
| `SpawnerCatDataReference` | Number | `1` | Applies or references the 'SpawnerCatDataReference' effect/state. |
| `SpreadWater` | Number | `1` | Applies or references the 'SpreadWater' effect/state. |
| `SproutsGrantMovement` | Number | `1` | Applies or references the 'SproutsGrantMovement' effect/state. |
| `StartDead` | Number | `100%` | Applies or references the 'StartDead' effect/state. |
| `StrengthUp` | Number | `2` | Applies or references the 'StrengthUp' effect/state. |
| `TVBotDisableAttack` | Number | `1` | Applies or references the 'TVBotDisableAttack' effect/state. |
| `TVBotDisableMove` | Number | `1` | Applies or references the 'TVBotDisableMove' effect/state. |
| `TVBotDisableSpells` | Number | `1` | Applies or references the 'TVBotDisableSpells' effect/state. |
| `TakeWeaponFromSpawner` | Number | `1` | Applies or references the 'TakeWeaponFromSpawner' effect/state. |
| `Tall` | Number | `1` | Applies or references the 'Tall' effect/state. |
| `TallTumorManaBurn` | [`Enum/String`](./Enums.md#enum-talltumormanaburn) | `TT_ManaBurn` | Applies or references the 'TallTumorManaBurn' effect/state. |
| `Terminator2Chase` | [`Enum/String`](./Enums.md#enum-terminator2chase) | `move` | Applies or references the 'Terminator2Chase' effect/state. |
| `TileElementDamageImmunity` | [`Enum/String`](./Enums.md#enum-tileelementdamageimmunity) | `Ice` | Applies or references the 'TileElementDamageImmunity' effect/state. |
| `TireBehavior` | Number | `1` | Applies or references the 'TireBehavior' effect/state. |
| `TormentorHeal` | Number | `1` | Applies or references the 'TormentorHeal' effect/state. |
| `TowerDefenseReflex` | [`Enum/String`](./Enums.md#enum-towerdefensereflex) | `attack` | Applies or references the 'TowerDefenseReflex' effect/state. |
| `TrackAmountKilledByPlayer` | [`Enum/String`](./Enums.md#enum-trackamountkilledbyplayer) | `BonusBirdsKilled` | Applies or references the 'TrackAmountKilledByPlayer' effect/state. |
| `TutorialBossRiggedFight` | Number | `16` | Applies or references the 'TutorialBossRiggedFight' effect/state. |
| `UncappedHP` | Number | `1` | Applies or references the 'UncappedHP' effect/state. |
| `UpTireBehavior` | Number | `5` | Applies or references the 'UpTireBehavior' effect/state. |
| `UseAbilityWhenShieldDepleted` | [`Enum/String`](./Enums.md#enum-useabilitywhenshielddepleted) | `T3Pebbles_PrimeBoulderDrop` | Applies or references the 'UseAbilityWhenShieldDepleted' effect/state. |
| `Wall` | Number | `1` | Applies or references the 'Wall' effect/state. |
| `WhitelistPickupType` | [`Enum/String`](./Enums.md#enum-whitelistpickuptype) | `food` | Applies or references the 'WhitelistPickupType' effect/state. |
| `WideBackstab` | Number | `1` | Applies or references the 'WideBackstab' effect/state. |
| `WispDodge` | Number | `1` | Applies or references the 'WispDodge' effect/state. |
| `ZeroKnockbackDamage` | Number | `1` | Applies or references the 'ZeroKnockbackDamage' effect/state. |

</details>

---

### Context: `pattern`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do` | [`Enum/String`](./Enums.md#enum-do) | `**SimonFlopper_WiggleChance, **SimonFlopper_WiggleGuaranteed, **SimonFlopper_WiggleFake` |  |
| `do_priority` | [`Array`](./Arrays.md#array-do_priority) | `[ *RockToss_BomberRat, RockToss_BomberRat ], [ BumblefootEatCorpse, BumblefootEatCat, BumblefootBoneSh..., [ *QueenWeb, attack, QueenMinis ]` |  |
| `do_all` | [`Array`](./Arrays.md#array-do_all) | `[ CovenFamine CovenRise3 ], [ CovenPestilence CovenRise2 ], [ CovenWar CovenRise4 ]` |  |
| `move_then_do` | [`Enum/String`](./Enums.md#enum-move_then_do) | `attack, NubsJump, SimonFlopper_SpawnMinion` |  |
| `do_random` | [`Array`](./Arrays.md#array-do_random) | `[ ScaryHaunt ScaryFear ], [ Escape attack DybbukReanimate ], [ Escape attack DybbukReanimate DybbukWisps ]` |  |
| `do_strict` | [`Array`](./Arrays.md#array-do_strict) | `[ MCFlamethrower ], [ MCStorm ], [ MCBlizzard ]` |  |
| `do_nothing` | [`Array`](./Arrays.md#array-do_nothing) | `[ ]` |  |
| `move_then_do_priority` | [`Array`](./Arrays.md#array-move_then_do_priority) | `[ BBPickupCrown, *attack, *BBToss ], [ BBPickupCrown, *BBToss, *attack ], [ DrinkUp attack ]` |  |
| `move_then_do_random` | [`Array`](./Arrays.md#array-move_then_do_random) | `[ CerberubsJumpBlind CerberubsJumpNormal ], [ ClotEvolve ClotFailEvolve ], [ ClotEvolveCatCopy ClotFailEvolve ]` |  |
| `do_all_shuffle` | [`Array`](./Arrays.md#array-do_all_shuffle) | `[ attack DybbukWisps DybbukRePossess ], [ YetiSlam YetiSlam YetiSlam YetiBite YetiBite YetiBite Y...` |  |
| `do_best` | [`Array`](./Arrays.md#array-do_best) | `[ JohnnyPush JohnnyPull ]` |  |
| `do_best_multiple` | [`Array`](./Arrays.md#array-do_best_multiple) | `[ attack spell0 spell1 spell2 spell3 spell4 weapon trinket ]` |  |
| `do_priority_alternating` | [`Array`](./Arrays.md#array-do_priority_alternating) | `[ *BadBone, *GoodBone, BadBone_copy, GoodBone_copy, BadBo...` |  |
| `move_then_do_all` | [`Array`](./Arrays.md#array-move_then_do_all) | `[ LennyShove, LennyGrabDead, LennyGrab ]` |  |

</details>

---

### Context: `FormChangeWhileHasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Counterspell, Consuming, Grappling` | ID of the status effect to apply or check. |
| `form_hasnot` | [`Enum/String`](./Enums.md#enum-form_hasnot) | `Big, Small, Default` |  |
| `form_has` | [`Enum/String`](./Enums.md#enum-form_has) | `HasCat, HasRock, Full` |  |

</details>

---

### Context: `FormChanger`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `initial_form` | [`Enum/String`](./Enums.md#enum-initial_form) | `Up, Flop, Default` |  |
| `Butcher` | Block | `{ ... }` | Applies or references the 'Butcher' effect/state. |
| `Colorless` | Block | `{ ... }` | Applies or references the 'Colorless' effect/state. |
| `Druid` | Block | `{ ... }` | Applies or references the 'Druid' effect/state. |
| `Fighter` | Block | `{ ... }` | Applies or references the 'Fighter' effect/state. |
| `Hunter` | Block | `{ ... }` | Applies or references the 'Hunter' effect/state. |
| `Mage` | Block | `{ ... }` | Applies or references the 'Mage' effect/state. |
| `Medic` | Block | `{ ... }` | Applies or references the 'Medic' effect/state. |
| `Monk` | Block | `{ ... }` | Applies or references the 'Monk' effect/state. |
| `Necromancer` | Block | `{ ... }` | Applies or references the 'Necromancer' effect/state. |
| `NoDeathRattle` | Block | `{ ... }` | Applies or references the 'NoDeathRattle' effect/state. |
| `Psychic` | Block | `{ ... }` | Applies or references the 'Psychic' effect/state. |
| `Tank` | Block | `{ ... }` | Applies or references the 'Tank' effect/state. |
| `Thief` | Block | `{ ... }` | Applies or references the 'Thief' effect/state. |
| `Tinkerer` | Block | `{ ... }` | Applies or references the 'Tinkerer' effect/state. |
| `Unmounted` | Block | `{ ... }` | Applies or references the 'Unmounted' effect/state. |
| `sync_brain_patterns` | Boolean | `true` |  |

</details>

---

### Context: `alt_spawn_pool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Antidote` | [`Enum/String`](./Enums.md#enum-antidote) | `.5, 1` | Applies or references the 'Antidote' effect/state. |
| `Blessing` | [`Enum/String`](./Enums.md#enum-blessing) | `.5, 1` | Applies or references the 'Blessing' effect/state. |
| `BigCatnip` | Number | `6, 10, 1` | Applies or references the 'BigCatnip' effect/state. |
| `BigScrap` | Number | `6, 4.5, 1` | Applies or references the 'BigScrap' effect/state. |
| `BiggestFood` | Number | `6, 1, 15` | Applies or references the 'BiggestFood' effect/state. |
| `Coin` | Number | `1, 70` | Applies or references the 'Coin' effect/state. |
| `BigFood` | Number | `20, 5` | Applies or references the 'BigFood' effect/state. |
| `Coin10` | Number | `1, .1` | Applies or references the 'Coin10' effect/state. |
| `Coin3` | Number | `1` | Applies or references the 'Coin3' effect/state. |
| `Coin4` | Number | `1` | Applies or references the 'Coin4' effect/state. |
| `MedCatnip` | Number | `20, 5` | Applies or references the 'MedCatnip' effect/state. |
| `MedScrap` | Number | `20, 5` | Applies or references the 'MedScrap' effect/state. |
| `RandomArmorPickup` | Number | `4.5, 40` | Applies or references the 'RandomArmorPickup' effect/state. |
| `RandomCatnipPickup` | Number | `10, 30` | Applies or references the 'RandomCatnipPickup' effect/state. |
| `RandomFoodPickup` | Number | `40, 15` | Applies or references the 'RandomFoodPickup' effect/state. |
| `Bear` | Number | `1` | Applies or references the 'Bear' effect/state. |
| `BlackBird` | Number | `3000` | Applies or references the 'BlackBird' effect/state. |
| `Catepillar` | Number | `10` | Applies or references the 'Catepillar' effect/state. |
| `Catnip` | Number | `20` | Applies or references the 'Catnip' effect/state. |
| `CharmedDip` | Number | `1` | Applies or references the 'CharmedDip' effect/state. |
| `CharmedFloater` | Number | `1` | Applies or references the 'CharmedFloater' effect/state. |
| `CharmedPile` | Number | `1` | Applies or references the 'CharmedPile' effect/state. |
| `Cherub` | Number | `1` | Applies or references the 'Cherub' effect/state. |
| `Chicken` | Number | `3000` | Applies or references the 'Chicken' effect/state. |
| `Coin2` | Number | `1` | Applies or references the 'Coin2' effect/state. |
| `Dove` | Number | `1000` | Applies or references the 'Dove' effect/state. |
| `Eagle` | Number | `300` | Applies or references the 'Eagle' effect/state. |
| `Food` | Number | `20` | Applies or references the 'Food' effect/state. |
| `Harpy` | Number | `1` | Applies or references the 'Harpy' effect/state. |
| `HummingBird` | Number | `300` | Applies or references the 'HummingBird' effect/state. |
| `LargeBirdPool` | Number | `1` | Applies or references the 'LargeBirdPool' effect/state. |
| `MedBirdPool` | Number | `1` | Applies or references the 'MedBirdPool' effect/state. |
| `Mutant` | Number | `1` | Character Form: Behavior and stats for the 'Mutant' state. |
| `Pigeon` | Number | `3000` | Applies or references the 'Pigeon' effect/state. |
| `RandomBiggerArmorPickup` | Number | `4.5` | Applies or references the 'RandomBiggerArmorPickup' effect/state. |
| `RandomBiggerCatnipPickup` | Number | `10` | Applies or references the 'RandomBiggerCatnipPickup' effect/state. |
| `RandomBiggerFoodPickup` | Number | `15` | Applies or references the 'RandomBiggerFoodPickup' effect/state. |
| `Raven` | Number | `300` | Applies or references the 'Raven' effect/state. |
| `Scrap` | Number | `20` | Applies or references the 'Scrap' effect/state. |
| `Seagull` | Number | `1000` | Applies or references the 'Seagull' effect/state. |
| `SmallBirdPool` | Number | `1` | Applies or references the 'SmallBirdPool' effect/state. |
| `Snake` | Number | `10` | Applies or references the 'Snake' effect/state. |
| `Squirrel` | Number | `10` | Applies or references the 'Squirrel' effect/state. |
| `Toad` | Number | `10` | Applies or references the 'Toad' effect/state. |
| `Turkey` | Number | `1000` | Applies or references the 'Turkey' effect/state. |
| `Turtle` | Number | `10` | Applies or references the 'Turtle' effect/state. |

</details>

---

### Context: `sound`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `alt_sounds` | [`Array`](./Arrays.md#array-alt_sounds) | `[ [ SE_BirdSmall_DyingCall SE_BirdDying_Hummingbird ], [ [ SE_BirdSmall_DyingCall SE_BirdDying_Blackbird ], [ [ SE_BirdSmall_DyingCall SE_BirdDying_Dove ]` |  |
| `SE_Cat_StompLegMove` | [`Enum/String`](./Enums.md#enum-se_cat_stomplegmove) | `SE_Terminator1_WalkLeg, SE_Terminator2_WalkLeg` | Applies or references the 'SE_Cat_StompLegMove' effect/state. |
| `SE_CatSwishThrow` | [`Enum/String`](./Enums.md#enum-se_catswishthrow) | `SE_ThrowGrenade` | Applies or references the 'SE_CatSwishThrow' effect/state. |
| `SE_Cat_ShadowStepIn` | [`Enum/String`](./Enums.md#enum-se_cat_shadowstepin) | `SE_Terminator_ShadowStepIn` | Applies or references the 'SE_Cat_ShadowStepIn' effect/state. |
| `SE_Cat_ShadowStepOut` | [`Enum/String`](./Enums.md#enum-se_cat_shadowstepout) | `SE_Terminator_ShadowStepOut` | Applies or references the 'SE_Cat_ShadowStepOut' effect/state. |
| `SE_Cat_WeaponLower` | [`Enum/String`](./Enums.md#enum-se_cat_weaponlower) | `SE_Terminator_WeaponLower` | Applies or references the 'SE_Cat_WeaponLower' effect/state. |
| `SE_Cat_WeaponRaise` | [`Enum/String`](./Enums.md#enum-se_cat_weaponraise) | `SE_Terminator_WeaponRaise` | Applies or references the 'SE_Cat_WeaponRaise' effect/state. |
| `SE_Cat_bearHug` | [`Enum/String`](./Enums.md#enum-se_cat_bearhug) | `SE_Terminator_bearHug` | Applies or references the 'SE_Cat_bearHug' effect/state. |
| `SE_Cat_equipWeapon` | [`Enum/String`](./Enums.md#enum-se_cat_equipweapon) | `SE_TerminatorSwapWeapon` | Applies or references the 'SE_Cat_equipWeapon' effect/state. |
| `SE_PetRock_Dash` | [`Enum/String`](./Enums.md#enum-se_petrock_dash) | `SE_PetBoulder_Dash` | Applies or references the 'SE_PetRock_Dash' effect/state. |
| `animation_prefix` | [`Enum/String`](./Enums.md#enum-animation_prefix) | `RattleSnake` |  |

</details>

---

### Context: `turns`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `takes_turns` | Boolean | `false, true` |  |
| `dispersed_bonus_turns` | Number | `1, 2, 0` |  |
| `takes_main_turn` | Boolean | `false, true` |  |
| `evenly_dispersed_bonus_turns` | Number | `2, 1` |  |
| `round_end_bonus_turns` | Number | `1` |  |
| `wait_till_next_round_to_update_turns` | Boolean | `true` |  |
| `round_start_bonus_turns` | Number | `1` |  |

</details>

---

### Context: `HealthPickup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `frame_range` | [`Array`](./Arrays.md#array-frame_range) | `[ 5 5 ], [ 3 4 ], [ 1 2 ]` |  |
| `stacks` | Number | `7, 10, 4` | Number of stacks or intensity to apply. |
| `stored_food_value` | Number | `2, 1, 3` |  |
| `anything_eats` | Boolean | `true` |  |
| `force_frame` | Number | `12` |  |

</details>

---

### Context: `CatPartsTransform`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `palette` | [`Enum/String`](./Enums.md#enum-palette) | `Mage, Fighter, Hunter` |  |
| `arm1` | Number | `1045, 1044, 1043` | Sprite variant ID for the front arm. |
| `arm2` | Number | `1045, 1044, 1043` |  |
| `body` | Number | `1024, 1013, 1012` | Sprite variant ID for the body. |
| `ear1` | Number | `1013, 1028, 1029` | Sprite variant ID for the front ear. |
| `head` | Number | `1019, 1027, 1020` | Sprite variant ID for the head. |
| `leg1` | Number | `1045, 1044, 1043` | Sprite variant ID for the front leg. |
| `leg2` | Number | `1045, 1044, 1043` |  |
| `tail` | Number | `1034, 1036, 1035` | Sprite variant ID for the tail. |
| `texture` | Number | `29, 60, 19` |  |
| `eye1` | Number | `1057, 1013` |  |
| `eye2` | Number | `1057, 1013` |  |
| `ear2` | Number | `1013` |  |

</details>

---

### Context: `equipment`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `face` | [`Enum/String`](./Enums.md#enum-face) | `AtomicMark, WesternHat, MetalPlate` |  |
| `head` | [`Enum/String`](./Enums.md#enum-head) | `Banana, LoansharksFedora, CoinBag` |  |
| `neck` | [`Enum/String`](./Enums.md#enum-neck) | `MageCollar, Poncho, Slime` |  |
| `weapon` | [`Enum/String`](./Enums.md#enum-weapon) | `ButcherHook, GunslingerPistol, AstroTaser` | Weapon item constraint. |

</details>

---

### Context: `mainturn_pattern`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do` | [`Enum/String`](./Enums.md#enum-do) | `**BombRatTurtle, **TrampleDash, HealSelf` |  |
| `do_all` | [`Array`](./Arrays.md#array-do_all) | `[ *AlienBeastScream *AlienBeastEat *AlienBeastPuke *Alien..., [ *MarshmallowZealot, CloseConvert, attack ], [ attack DustTeleport ]` |  |
| `do_priority` | [`Array`](./Arrays.md#array-do_priority) | `[ ChumShot_Damage, ChumShot_Maggot ], [ attack Simon_Shot ], [ *HitlerHeil attack move ]` |  |
| `do_strict` | [`Array`](./Arrays.md#array-do_strict) | `[ BasicMelee, RageUp ], [ *WizSpellShield, WizBlizzard ]` |  |
| `move_then_do` | [`Enum/String`](./Enums.md#enum-move_then_do) | `RockSong, attack` |  |

</details>

---

### Context: `CharacterLightSource`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `color` | [`Array`](./Arrays.md#array-color) | `[ .7, .8, .9 ], [ .3, .7, 1 ], [ .8, .9, 1 ]` |  |
| `size` | Number | `2, 1.5, 4` |  |
| `glow` | [`Array`](./Arrays.md#array-glow) | `[ 1, 1, 1, .5 ], [ .7, .8, .9, .5 ], [ .3, .7, 1, .5 ]` |  |

</details>

---

### Context: `bonusturn_pattern`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do` | [`Enum/String`](./Enums.md#enum-do) | `move, *SpawnBomb, DustDash` |  |
| `do_priority` | [`Array`](./Arrays.md#array-do_priority) | `[ TormentorBite TormentorSpawn attack ], [ TormentorSpawn TormentorBite attack ], [ G3GrabHead move *G3GrabHead ]` |  |
| `do_strict` | [`Array`](./Arrays.md#array-do_strict) | `[ WizStorm ], [ WizFlamethrower ], [ ]` |  |
| `do_all` | [`Array`](./Arrays.md#array-do_all) | `[ attack AlienBeastOpenEyes ], [ TrembloSuck *TrembloEat TrembloEat ], [ CloseConvert, attack ]` |  |
| `move_then_do` | [`Enum/String`](./Enums.md#enum-move_then_do) | `RatKingSpawn` |  |

</details>

---

### Context: `AbilityHealthThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `DybbukPossess, FormShrinkFour, FormShrinkThree` | The specific ability ID to cast. |
| `threshold` | [`Enum/String`](./Enums.md#enum-threshold) | `4*champion_multiplier, 3*champion_multiplier, 1` |  |
| `even_if_stunned` | Boolean | `true` |  |
| `immediate` | Boolean | `true` |  |
| `use_ai` | Boolean | `true` |  |
| `also_use_if_buddy_is_dead` | Boolean | `true` |  |
| `threshold_min` | [`Enum/String`](./Enums.md#enum-threshold_min) | `X` |  |

</details>

---

### Context: `BossRewards`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `common` | [`Enum/String`](./Enums.md#enum-common) | `RatBomb, ChubsCollar, Blubber` |  |
| `rare` | [`Enum/String`](./Enums.md#enum-rare) | `SpiderBaby, RadGlasses, BorisBrain` |  |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `TinySpider, Rat, Maggot` |  |
| `good` | Boolean | `false, true` |  |
| `spawn_on_death_hit` | Boolean | `false` |  |
| `chance` | Number | `50%, .25, 33%` | Probability (0.0 to 1.0) of executing this action. |
| `coins` | Number | `1` |  |
| `auto_cast` | [`Enum/String`](./Enums.md#enum-auto_cast) | `Dash_Enemy` |  |
| `consider_all_layers` | Boolean | `true` |  |
| `melee_ability_only` | Boolean | `true` |  |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0, 5` | The base damage properties of an attack. |
| `knockback` | Number | `4, 2, 3` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status, none` | Classification/category type. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Fire ]` |  |
| `cant_miss` | Boolean | `true` |  |

</details>

---

### Context: `FormChangeOnElementInfluence`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `water, very_hot, wind` | Specific element type required or applied. |
| `form` | [`Enum/String`](./Enums.md#enum-form) | `hot, default, Unlit` |  |
| `exclude` | [`Enum/String`](./Enums.md#enum-exclude) | `water, fire` |  |
| `particle` | [`Enum/String`](./Enums.md#enum-particle) | `FireExtinguish` |  |
| `sfx` | [`Enum/String`](./Enums.md#enum-sfx) | `FireExtinguish` |  |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `2, 1` | Applies or references the 'Bleed' effect/state. |
| `Burn` | Number | `2, 1, 4` | Applies or references the 'Burn' effect/state. |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `RemoteLeech` | Number | `1` | Applies or references the 'RemoteLeech' effect/state. |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |
| `DamageUp` | Number | `-1` | Applies or references the 'DamageUp' effect/state. |
| `Knockback` | Number | `3` | Applies or references the 'Knockback' effect/state. |
| `Leech` | Number | `2` | Applies or references the 'Leech' effect/state. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `Possessed` | Number | `1` | Applies or references the 'Possessed' effect/state. |
| `RandomStatUp` | Number | `-1` | Applies or references the 'RandomStatUp' effect/state. |
| `RemoteFlatLeech` | Number | `1` | Applies or references the 'RemoteFlatLeech' effect/state. |
| `Rot` | Number | `1` | Applies or references the 'Rot' effect/state. |
| `Slow` | Number | `1` | Applies or references the 'Slow' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `Weakness` | Number | `1` | Applies or references the 'Weakness' effect/state. |

</details>

---

### Context: `ImmediateAbilityReaction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `ButtWeb, AlienBeastGoop, ButtWeb_AlreadyEnraged` | The specific ability ID to cast. |
| `ability_damage_only` | Boolean | `true` |  |
| `backstabs_only` | Boolean | `true` |  |
| `damage_threshold` | Number | `10` |  |
| `even_if_blocked` | Boolean | `true` |  |
| `even_if_stunned` | Boolean | `true` |  |
| `health_threshold` | Number | `50, 70` |  |
| `buddy_damage_only` | Boolean | `true` |  |
| `target_furthest_valid` | Boolean | `true` |  |

</details>

---

### Context: `AbilityReaction`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MoonHandDash, attack, ButtFlip` | The specific ability ID to cast. |
| `ability_damage_only` | Boolean | `true` |  |
| `backstabs_only` | Boolean | `true` |  |
| `only_when_not_your_turn` | Boolean | `true` |  |
| `cancel_knockback` | Boolean | `true` |  |
| `enemies_only` | Boolean | `true` |  |
| `even_on_0_damage` | Boolean | `true` |  |
| `even_on_0_damage_if_knockback` | Boolean | `true` |  |
| `match_knockback_direction` | Boolean | `true` |  |
| `ranged_only` | Boolean | `true` |  |
| `verify_target` | Boolean | `true` |  |

</details>

---

### Context: `PassiveGroup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FormChange` | [`Enum/String`](./Enums.md#enum-formchange) | `Mage, Fighter, Hunter` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `ReplaceBasicAttack` | [`Enum/String`](./Enums.md#enum-replacebasicattack) | `BasicMelee, BasicRanged, BasicMagicShortRanged` | Applies or references the 'ReplaceBasicAttack' effect/state. |
| `SelfStatusCarefulness` | Number | `1` | Applies or references the 'SelfStatusCarefulness' effect/state. |
| `StatusCarefulness` | Number | `1` | Applies or references the 'StatusCarefulness' effect/state. |
| `ExtraBasicAttacks` | Number | `1` | Applies or references the 'ExtraBasicAttacks' effect/state. |

</details>

---

### Context: `Consumed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do_not_pop_corpse` | Boolean | `true` |  |
| `drop_on_death` | [`Enum/String`](./Enums.md#enum-drop_on_death) | `deferred` |  |
| `force_contact` | Boolean | `true` | If true, enforces physical overlap. |
| `instant` | Boolean | `true` |  |
| `mount_mode` | [`Enum/String`](./Enums.md#enum-mount_mode) | `auto` | If true, treats the consumption as riding/mounting instead of eating. |
| `struggle_ability` | [`Enum/String`](./Enums.md#enum-struggle_ability) | `Thrash` | Ability triggered by the consumed entity while inside the consumer. |
| `use_placeholder` | Boolean | `true` |  |

</details>

---

### Context: `DeathRattle`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MoonHandDrop_Deathrattle, UFO_SpelunkyDeath, JarHeadDeath` | The specific ability ID to cast. |
| `is_dying_animation` | Boolean | `true` |  |
| `pop_corpse` | Boolean | `false` |  |
| `cancel_knockback` | Boolean | `true` |  |
| `immediate` | Boolean | `true` |  |
| `must_target_killer` | Boolean | `true` |  |
| `target_killer` | Boolean | `true` |  |

</details>

---

### Context: `TransformInXTurns`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Array`](./Arrays.md#array-object) | `SkeletonCatRevived, TallSkeletonCatRevived, [ Squirrel Crow Snake Turtle Toad Catepillar ]` |  |
| `stacks` | Number | `2, 1, 3` | Number of stacks or intensity to apply. |
| `initiative` | [`Enum/String`](./Enums.md#enum-initiative) | `keep_turns_end_turn` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `hatch` |  |
| `turns` | [`Array`](./Arrays.md#array-turns) | `[ 1 4 ]` | Turn counter tracking. |

</details>

---

### Context: `fallback`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do` | [`Enum/String`](./Enums.md#enum-do) | `RockToss_ColorlessCat_AsCloseAsPossible, JohnnyBlast, attack` |  |
| `do_priority` | [`Array`](./Arrays.md#array-do_priority) | `[ *attack RunFar ], [ attack TrembloEat ], [ attack, Magnetize, YeetTowardsBuddy ]` |  |
| `do_all` | [`Array`](./Arrays.md#array-do_all) | `[ move, *CoreFreakFury ]` |  |
| `do_best` | [`Array`](./Arrays.md#array-do_best) | `[ Magnetize, attack, GuillotinaTossCollide, YeetTowardsBu...` |  |
| `do_nothing` | [`Array`](./Arrays.md#array-do_nothing) | `[ ]` |  |
| `do_random` | [`Array`](./Arrays.md#array-do_random) | `[ CHSpawn CHCry ]` |  |
| `move_then_do` | [`Enum/String`](./Enums.md#enum-move_then_do) | `CerberubsCalm` |  |

</details>

---

### Context: `CaveFamilyEnrage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `CaveCatEnrageTwo, CaveCatEnrageOne` | The specific ability ID to cast. |
| `count` | Number | `0, 1` | The numerical quantity. |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `cavefamily` | Specific entity tag required. |

</details>

---

### Context: `TransformOnElementInfluence`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Holy, Fire` | Specific element type required or applied. |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CookedFood, CookedBiggestFood, CookedBigFood` |  |

</details>

---

### Context: `ChanceToSpitOnDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `TinaSpit, PteroEscape, MoonHandDrop` | The specific ability ID to cast. |
| `flat_chance` | Number | `50%, 100%` |  |
| `chance_per_damage` | Number | `0%, 2%` |  |
| `backstabs_only` | Boolean | `true` |  |
| `even_on_0_damage_if_knockback` | Boolean | `true` |  |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MoonHandGrab, MoonHead_EatCat, weapon` | The specific ability ID to cast. |
| `enemies_only` | Boolean | `false, true` |  |
| `objects_too` | Boolean | `true` |  |
| `on_self_move_too` | Boolean | `true` |  |
| `blind_spot` | Boolean | `true` |  |
| `forward_only` | Boolean | `true` |  |
| `self_move_exclude_self_abilities` | Boolean | `true` |  |

</details>

---

### Context: `DeathRattleRevive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `AZ_LoseHead, HitlerPulp1, HitlerPulp2` | The specific ability ID to cast. |
| `even_if_stunned` | Boolean | `true` |  |

</details>

---

### Context: `FormChangeOffMap`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `form_offmap` | [`Enum/String`](./Enums.md#enum-form_offmap) | `Start_Ceiling, Default_Ceiling, Insane_Ceiling` |  |
| `form_onmap` | [`Enum/String`](./Enums.md#enum-form_onmap) | `Insane_Ground, Default, Default_Ground` |  |

</details>

---

### Context: `SecurityBotProtect`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `SZBShoot, CBShoot_ZodiacStyle, attack` | The specific ability ID to cast. |
| `enemies_only` | Boolean | `true` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None, SBotAngryMove` |  |
| `tag_restriction` | [`Enum/String`](./Enums.md#enum-tag_restriction) | `dinofamily, dc_cat` |  |
| `not_on_kill` | Boolean | `true` |  |

</details>

---

### Context: `ally_rewards`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `blackbird_pool, chapter, dove_pool` | Generates an item drop from the specified loot pool. |

</details>

---

### Context: `StatusCollector`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |
| `Poison` | Number | `2` | Applies or references the 'Poison' effect/state. |
| `Slow` | Number | `2` | Applies or references the 'Slow' effect/state. |

</details>

---

### Context: `round_end_bonusturn_pattern`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do_all` | [`Array`](./Arrays.md#array-do_all) | `[ MoonHead_CallForHelp MoonHead_RefreshBrace ], [ MoonHead_ChewCat MoonHead_CallForHelp MoonHead_RefreshB..., [ *QueenHippoUppercut QueenHippoAttack move QueenHippoTire ]` |  |
| `do` | [`Enum/String`](./Enums.md#enum-do) | `RallyMaggots, CutterCut, SuckMF` |  |
| `do_one` | [`Array`](./Arrays.md#array-do_one) | `[ **ZaratanaVSWeatherRoar **ZaratanaVSRoar ], [ **PyrophinaVSWeatherRoar **PyrophinaVSRoar ]` |  |
| `do_random` | [`Array`](./Arrays.md#array-do_random) | `[ TKNG_Spread TKNG_Kneel TKNG_Roulette TKNG_GoAway ], [ SimonSays_Scatter, SimonSays_ComeHere, SimonSays_GoAway ]` |  |
| `do_nothing` | [`Array`](./Arrays.md#array-do_nothing) | `[ ]` |  |
| `do_priority` | [`Array`](./Arrays.md#array-do_priority) | `[ NCReanimate NCGravecrawlFAR ]` |  |

</details>

---

### Context: `effects`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | `2, 5` | Applies or references the 'Burn' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `Thorns` | Number | `1` | Applies or references the 'Thorns' effect/state. |
| `BlackHoleSuck` | Number | `1` | Applies or references the 'BlackHoleSuck' effect/state. |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |
| `ConstitutionUp` | Number | `-1` | Applies or references the 'ConstitutionUp' effect/state. |
| `Vaporize` | Number | `20` | Applies or references the 'Vaporize' effect/state. |

</details>

---

### Context: `FormChangeWhilePrimingAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `not_priming` | [`Enum/String`](./Enums.md#enum-not_priming) | `DualSword, SwordAndShield, NotPriming` |  |
| `priming` | [`Enum/String`](./Enums.md#enum-priming) | `Priming, SwordAndShield_Primed, DualSword_Primed` |  |

</details>

---

### Context: `MoveTowardsDamageSource`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `check_in_form` | [`Enum/String`](./Enums.md#enum-check_in_form) | `Boris, Default` |  |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `MoveOne, MD_WalkOne` |  |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `can_move_zero` | Boolean | `true` |  |
| `check_has_status` | [`Enum/String`](./Enums.md#enum-check_has_status) | `FinalBossHitCountdownBoris` |  |
| `do_not_move_on_top` | Boolean | `true` |  |
| `face_towards_after` | Boolean | `true` |  |
| `ignore_tagged_sources` | [`Enum/String`](./Enums.md#enum-ignore_tagged_sources) | `megadino` |  |
| `move_far` | Boolean | `false` |  |
| `move_short` | Boolean | `true` |  |

</details>

---

### Context: `HasCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `PteroPeck, MoonHandSqueeze, MoonHead_ChewCat` |  |
| `animation_suffix` | String | `"Grabbing", "Cat"` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |
| `partial_animation_suffix` | String | `"Swallowed"` |  |

</details>

---

### Context: `MoveClose`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_close, stay_close_always_move, stay_close_avoid_allies` |  |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `attack, Spin_Enemy` |  |

</details>

---

### Context: `FormChangeHealthThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `form_above` | [`Enum/String`](./Enums.md#enum-form_above) | `Full, Standing, Default` |  |
| `form_below` | [`Enum/String`](./Enums.md#enum-form_below) | `Damaged, Standing2, DesireMech` |  |
| `threshold` | [`Enum/String`](./Enums.md#enum-threshold) | `X-4, 50, 25` |  |
| `count_shield` | Boolean | `true` |  |

</details>

---

### Context: `SmallRockBehavior`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `9, 5` | The base damage properties of an attack. |
| `knockback` | Number | `2, 1, 5` |  |
| `chain` | Boolean | `true` |  |

</details>

---

### Context: `Trapper`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `YA_Laser, HellHandGrab, BloatSideLaser` | The specific ability ID to cast. |
| `cancel_movement` | Boolean | `false` |  |
| `pathfinding_avoidance` | Number | `250` |  |
| `range` | Number | `10` | Distance or area of effect in tiles. |

</details>

---

### Context: `ReplaceBrain`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `brain` | [`Enum/String`](./Enums.md#enum-brain) | `PatternBrain` |  |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `default` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance, stay_close` |  |

</details>

---

### Context: `BungaEntrance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `BecomeTheDestroyer, BungaEntrance` | The specific ability ID to cast. |
| `even_if_stunned` | Boolean | `true` |  |
| `health_threshold` | Number | `150, -1` |  |
| `warrior_tag` | [`Enum/String`](./Enums.md#enum-warrior_tag) | `bungawarrior, finalboss_clonecat` |  |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `displace` | Boolean | `true` |  |
| `distance` | Number | `3` | The distance in tiles to knock the target away. |
| `self_damage` | Boolean | `false` | Recoil or self-inflicted damage/effects applied to the caster. |
| `stacks` | Number | `5` | Number of stacks or intensity to apply. |

</details>

---

### Context: `MoveAway`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MoveTwoCantrip, DoubleDistanceMove, ExtraMove` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_far, blind_move_far, keep_distance_always_move` |  |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `weights` | [`Enum/String`](./Enums.md#enum-weights) | `stay_far_always_move, chaotic, stay_near_allies_always_move` |  |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `WaterTrailMove` |  |

</details>

---

### Context: `Rage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"Rage"` |  |
| `animation_suffix` | String | `"Rage"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `ChubsSpinRage` |  |
| `move_speed_multiplier` | Number | `2` |  |

</details>

---

### Context: `TransformOnDeathImmediately`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `first_turn` | [`Enum/String`](./Enums.md#enum-first_turn) | `keep_turns` |  |
| `obj` | [`Enum/String`](./Enums.md#enum-obj) | `TallSkeletonCatCorpse, SkeletonCatCorpse, SkeletonShamblerCorpse` |  |

</details>

---

### Context: `hot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Hot"` |  |
| `name` | String | `"OBJECT_HOTPETROCK_NAME", "OBJECT_HOTROCK_NAME", "OBJECT_HOTBOULDER_NAME"` | Localization key for the character's name. |

</details>

---

### Context: `Buddy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | `false` |  |
| `obj` | [`Enum/String`](./Enums.md#enum-obj) | `PyrophinaVS, Dice, ZaratanaVS` |  |
| `reclaim_if_lost` | Boolean | `true` |  |

</details>

---

### Context: `FinalBossPupils`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `look_at_offset` | [`Array`](./Arrays.md#array-look_at_offset) | `[ 0 2.5 0 ]` |  |
| `radius` | Number | `13` | Distance or area of effect in tiles. |
| `reset_center_because_no_target_halflife` | [`Enum/String`](./Enums.md#enum-reset_center_because_no_target_halflife) | `.1` |  |
| `reset_center_because_of_animation_halflife` | [`Enum/String`](./Enums.md#enum-reset_center_because_of_animation_halflife) | `.05` |  |
| `teleport_tracking_halflife` | [`Enum/String`](./Enums.md#enum-teleport_tracking_halflife) | `.01` |  |
| `tracking_acquisition_halflife` | [`Enum/String`](./Enums.md#enum-tracking_acquisition_halflife) | `.1` |  |
| `virtual_head_position` | [`Array`](./Arrays.md#array-virtual_head_position) | `[ 11 2 11 ]` |  |

</details>

---

### Context: `ReflectProjectiles`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `self_damage` | Number | `2` | Recoil or self-inflicted damage/effects applied to the caster. |

</details>

---

### Context: `2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee_2Hits, BoneWormShotMed` |  |
| `partial_animation_suffix` | Number | `2` |  |
| `animation_suffix` | Number | `2` |  |
| `uifloaters_offset` | Number | `2.2` |  |

</details>

---

### Context: `3`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee_3Hits, BoneWormShotTall` |  |
| `partial_animation_suffix` | Number | `3` |  |
| `animation_suffix` | Number | `3` |  |
| `uifloaters_offset` | Number | `3` |  |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MoveTwo` | The specific ability ID to cast. |
| `range` | Number | `2, 4` | Distance or area of effect in tiles. |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `food` | Specific entity tag required. |

</details>

---

### Context: `ArmorPickup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `frame_range` | [`Array`](./Arrays.md#array-frame_range) | `[ 3 5 ], [ 6 6 ], [ 1 2 ]` |  |
| `stacks` | Number | `6, 2, 4` | Number of stacks or intensity to apply. |

</details>

---

### Context: `CaveMan`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"CaveMan"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `CaveMan3HitCombo` |  |
| `name` | String | `"ENEMY_CAVEMANMAN_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CAVEMANMAN_DESC"` |  |

</details>

---

### Context: `CaveManSpear`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"SpearCaveMan"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `CaveManThrowSpear` |  |
| `name` | String | `"ENEMY_SPEARCAVEMAN_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_SPEARCAVEMAN_DESC"` |  |

</details>

---

### Context: `ManaPickup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `frame_range` | [`Array`](./Arrays.md#array-frame_range) | `[ 3 5 ], [ 6 6 ], [ 1 2 ]` |  |
| `stacks` | Number | `6, 2, 4` | Number of stacks or intensity to apply. |

</details>

---

### Context: `MoveForThrow`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `PyrophinaVSCatThrow, PyrophinaSoloCatThrow` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `util_minmove` |  |

</details>

---

### Context: `MoveTowardsKillers`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `character_filter` | [`Array`](./Arrays.md#array-character_filter) | `[ SpiderCat, TallSpiderCat ]` |  |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `SpiderReturn` |  |

</details>

---

### Context: `SpawnOnDeath`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `faction` | [`Enum/String`](./Enums.md#enum-faction) | `enemies, allies` |  |
| `obj` | [`Array`](./Arrays.md#array-obj) | `RiftKitten, [ Kitten Kitten TomTom TomTom Mangy Mangy CatCaller CatCa..., [ Spookie Spookie Scary Coin2 Coin3 Coin4 ]` |  |

</details>

---

### Context: `SpearRun`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `CaveManSpearRun` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `CaveManPickupSpear` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `util_minmove` |  |

</details>

---

### Context: `SpewerAltGraphics`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fire` | Number | `1` | Character Form: Behavior and stats for the 'Fire' state. |
| `FireFull` | Number | `1` | Character Form: Behavior and stats for the 'FireFull' state. |
| `Normal` | Number | `0` | Character Form: Behavior and stats for the 'Normal' state. |
| `NormalFull` | Number | `0` | Character Form: Behavior and stats for the 'NormalFull' state. |
| `Tar` | Number | `2` | Character Form: Behavior and stats for the 'Tar' state. |
| `TarFull` | Number | `2` | Character Form: Behavior and stats for the 'TarFull' state. |

</details>

---

### Context: `StatusEachTurnBeginIfHasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` | Applies or references the 'AllStatsUp' effect/state. |
| `DamageUp` | Number | `2` | Applies or references the 'DamageUp' effect/state. |
| `HealthGain` | Number | `8` | Applies or references the 'HealthGain' effect/state. |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `pulse3` |  |
| `consume` | Boolean | `true` |  |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Counterspell` | ID of the status effect to apply or check. |

</details>

---

### Context: `TVBotScreen`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Die` | Number | `6` | Character Form / Logic: Forces the character to die. |
| `Dumb` | Number | `3` | AI Profile: A simplified, less optimal decision-making profile. |
| `Fuck` | Number | `5` | Applies or references the 'Fuck' effect/state. |
| `Obey` | Number | `1` | AI State: Enforced compliance logic (e.g., when Charmed). |
| `Shit` | Number | `4` | Applies or references the 'Shit' effect/state. |
| `Stop` | Number | `2` | AI Movement: Forces the character to cease movement. |

</details>

---

### Context: `Turtled`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Turtle` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |

</details>

---

### Context: `BattlefieldUniqueRandomPassive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Number | `1` | Applies or references the 'DemonicGlyph_Bite' effect/state. |
| `DemonicGlyph_Bounce` | Number | `1` | Applies or references the 'DemonicGlyph_Bounce' effect/state. |
| `DemonicGlyph_Fire` | Number | `1` | Applies or references the 'DemonicGlyph_Fire' effect/state. |
| `DemonicGlyph_Movement` | Number | `1` | Applies or references the 'DemonicGlyph_Movement' effect/state. |
| `DemonicGlyph_Summon` | Number | `1` | Applies or references the 'DemonicGlyph_Summon' effect/state. |

</details>

---

### Context: `Bishop`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Bishop"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BBXLightning` |  |
| `name` | String | `"ENEMY_CULTISTBISHOP_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CULTISTBISHOP_DESC"` |  |
| `uifloaters_offset` | Number | `2.5` |  |

</details>

---

### Context: `BungaCheers`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ally_damage` | [`Enum/String`](./Enums.md#enum-ally_damage) | `littleboo` |  |
| `ally_dead` | [`Enum/String`](./Enums.md#enum-ally_dead) | `bigboo` |  |
| `enemy_damage` | [`Enum/String`](./Enums.md#enum-enemy_damage) | `littlecheer` |  |
| `enemy_dead` | [`Enum/String`](./Enums.md#enum-enemy_dead) | `bigcheer` |  |
| `warrior_tag` | [`Enum/String`](./Enums.md#enum-warrior_tag) | `bungawarrior` |  |

</details>

---

### Context: `FinalBossHitCountdownBoris`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Block`](./Characters_and_Bosses.md#context-forceuseability) | `{ ... }, TheChild_TransformExplosive` | Logic: Forces the execution of a specific ability. |
| `icon` | Number | `802` |  |
| `icon_ready` | Number | `803` |  |
| `stacks` | Number | `7` | Number of stacks or intensity to apply. |

</details>

---

### Context: `FinalBossHitCountdownExplosive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Block`](./Characters_and_Bosses.md#context-forceuseability) | `{ ... }, TheChild_TransformHoly` | Logic: Forces the execution of a specific ability. |
| `icon` | Number | `800` |  |
| `icon_ready` | Number | `801` |  |
| `stacks` | Number | `7` | Number of stacks or intensity to apply. |

</details>

---

### Context: `Grown`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Grown` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `HitlerCloneSwipes` |  |
| `name` | String | `"ENEMY_HITLERCLONE_NAME"` | Localization key for the character's name. |
| `uifloaters_offset` | Number | `1.5` |  |
| `weak_threshold` | Number | `15` |  |

</details>

---

### Context: `MonkCatReactionAbilities`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `attack` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `move` |  |
| `spell` | [`Enum/String`](./Enums.md#enum-spell) | `MCHadouken` |  |
| `trinket` | [`Enum/String`](./Enums.md#enum-trinket) | `MCHadouken` |  |
| `weapon` | [`Enum/String`](./Enums.md#enum-weapon) | `attack` | Weapon item constraint. |

</details>

---

### Context: `Mutant`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Mutant"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BBMutantSwipe` |  |
| `move_speed_multiplier` | [`Enum/String`](./Enums.md#enum-move_speed_multiplier) | `.5` |  |
| `name` | String | `"ENEMY_CULTISTMUTANT_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CULTISTMUTANT_DESC"` |  |

</details>

---

### Context: `PassiveWhileHasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `DemonicGlyph_Summon, DemonicGlyph_Fire, DemonicGlyph_Bite` | ID of the status effect to apply or check. |

</details>

---

### Context: `Pulp2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `2` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |
| `tooltip` | [`Enum/String`](./Enums.md#enum-tooltip) | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `uifloaters_offset` | Number | `1` |  |

</details>

---

### Context: `Pulp3`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `3` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |
| `tooltip` | [`Enum/String`](./Enums.md#enum-tooltip) | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `uifloaters_offset` | Number | `1` |  |

</details>

---

### Context: `Pulp4`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `4` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |
| `tooltip` | [`Enum/String`](./Enums.md#enum-tooltip) | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `uifloaters_offset` | Number | `1` |  |

</details>

---

### Context: `Pulp5`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `5` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |
| `tooltip` | [`Enum/String`](./Enums.md#enum-tooltip) | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `uifloaters_offset` | Number | `1` |  |

</details>

---

### Context: `Pulp6`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `6` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |
| `tooltip` | [`Enum/String`](./Enums.md#enum-tooltip) | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `uifloaters_offset` | Number | `1` |  |

</details>

---

### Context: `Pulp7`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `7` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |
| `tooltip` | [`Enum/String`](./Enums.md#enum-tooltip) | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `uifloaters_offset` | Number | `1` |  |

</details>

---

### Context: `SlotMachineRollPool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SlotResult_Jackpot_Coins` | Number | `1` | Applies or references the 'SlotResult_Jackpot_Coins' effect/state. |
| `SlotResult_Explode` | Number | `1` | Applies or references the 'SlotResult_Explode' effect/state. |
| `SlotResult_Nothing` | Number | `7` | Applies or references the 'SlotResult_Nothing' effect/state. |
| `SlotResult_RandomPickup` | Number | `11` | Applies or references the 'SlotResult_RandomPickup' effect/state. |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `UseAbility_NonStack` | [`Enum/String`](./Enums.md#enum-useability_nonstack) | `BBTransformZealot, GenericRage` | Applies or references the 'UseAbility_NonStack' effect/state. |
| `HealthGain` | Number | `5` | Applies or references the 'HealthGain' effect/state. |

</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ExtraBasicAttacks_Status` | Number | `1` | Applies or references the 'ExtraBasicAttacks_Status' effect/state. |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `HealthRegenUp` | Number | `1` | Applies or references the 'HealthRegenUp' effect/state. |
| `TakeExtraTurn` | Number | `1` | Applies or references the 'TakeExtraTurn' effect/state. |

</details>

---

### Context: `eat_damage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | `true` |  |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `makes_contact` | Boolean | `true` |  |
| `piercing` | Boolean | `true` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `melee` | Classification/category type. |

</details>

---

### Context: `AbilityOnRoundEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `DestroyerRaise` | The specific ability ID to cast. |
| `force_display_name` | Boolean | `true` |  |

</details>

---

### Context: `BaitAura`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `range` | Number | `3` | Distance or area of effect in tiles. |

</details>

---

### Context: `Cat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `formchange` | [`Enum/String`](./Enums.md#enum-formchange) | `BigHoldingCat, SmallHoldingCat` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `spawnHoldingCat` |  |

</details>

---

### Context: `CaveBaby`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"CaveBaby"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `CaveBabyMelee` |  |
| `name` | String | `"ENEMY_CAVEBABY_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CAVEBABY_DESC"` |  |

</details>

---

### Context: `CaveWoman`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"CaveWoman"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `CaveWomanKick` |  |
| `name` | String | `"ENEMY_CAVEMANWOMAN_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CAVEMANWOMAN_DESC"` |  |

</details>

---

### Context: `CaveWomanHasCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"CatCaveWoman"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `CaveWomanCatSlap` |  |
| `name` | String | `"ENEMY_CAVEMANWOMAN2_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CAVEMANWOMAN2_DESC"` |  |

</details>

---

### Context: `CherubimReaction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Leave` | [`Enum/String`](./Enums.md#enum-leave) | `LELeave, CherubimLeave` | Applies or references the 'Leave' effect/state. |
| `Return` | [`Enum/String`](./Enums.md#enum-return) | `CherubimReturn, LEReturn` | Applies or references the 'Return' effect/state. |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `chapter` | Generates an item drop from the specified loot pool. |
| `odds` | Number | `5%, 33%` | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |

</details>

---

### Context: `Cultist`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Cultist"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee` |  |
| `name` | String | `"ENEMY_CULTISTLACKEY_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CULTISTLACKEY_DESC"` |  |

</details>

---

### Context: `DashRandomly`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `ShamblerDash` | The specific ability ID to cast. |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `blind` |  |

</details>

---

### Context: `Down`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Down"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `ButtFart` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `TeleportFlipUp` |  |

</details>

---

### Context: `DualSword`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"2"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `DestroyerAttack2` |  |
| `move_speed_multiplier` | Number | `1.5` |  |
| `tooltip` | String | `"ENEMY_DESTROYER2_DESC"` |  |

</details>

---

### Context: `DualSword_Primed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Holy2"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `DestroyerAttack2` |  |
| `move_speed_multiplier` | Number | `1.5` |  |
| `tooltip` | String | `"ENEMY_DESTROYER2_DESC"` |  |

</details>

---

### Context: `Escape`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `DybbukEscape` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance_always_move` |  |

</details>

---

### Context: `ForceUseAbility`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`FinalBossHitCountdownBoris`](./Characters_and_Bosses.md#context-finalbosshitcountdownboris), [`FinalBossHitCountdownExplosive`](./Characters_and_Bosses.md#context-finalbosshitcountdownexplosive)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `TheChild_Wrath, TheChild_Pulse` | The specific ability ID to cast. |
| `show_name` | Boolean | `true` |  |

</details>

---

### Context: `FormChangeDuringWeatherElement`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Water` | Specific element type required or applied. |
| `form` | [`Enum/String`](./Enums.md#enum-form) | `Rain` |  |

</details>

---

### Context: `Full`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Full"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `KirbySpit` |  |

</details>

---

### Context: `MegaDinoDropController`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `head_drop` | [`Enum/String`](./Enums.md#enum-head_drop) | `MD_HeadDrop` |  |
| `leg_leave` | [`Enum/String`](./Enums.md#enum-leg_leave) | `MD_LegLeave` |  |
| `leg_return` | [`Enum/String`](./Enums.md#enum-leg_return) | `MD_LegReturn` |  |
| `stable_legs` | Number | `3` |  |

</details>

---

### Context: `MotherTumorPassive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `considered_forms` | [`Array`](./Arrays.md#array-considered_forms) | `[ Big BigHolding BigHoldingCat ]` |  |
| `grow_ability` | [`Enum/String`](./Enums.md#enum-grow_ability) | `MotherTumorGrow` |  |
| `pass_ani` | [`Enum/String`](./Enums.md#enum-pass_ani) | `pass` |  |
| `receive_ani` | [`Enum/String`](./Enums.md#enum-receive_ani) | `receive` |  |

</details>

---

### Context: `MoveCenter`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_near_map_center` |  |

</details>

---

### Context: `NonCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `formchange` | [`Enum/String`](./Enums.md#enum-formchange) | `BigHolding, SmallHolding` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `spawnHolding` |  |

</details>

---

### Context: `ProtectTargetedAllies`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `SwapPositions_TankCat` | The specific ability ID to cast. |
| `target_filter` | [`Enum/String`](./Enums.md#enum-target_filter) | `any, Kitten` |  |

</details>

---

### Context: `RemoveStatusStacks`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `10, 1` | The number of stacks to remove. |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Brace, DodgeChance_Status` | The specific status effect ID to remove. |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `HealthGain` | Number | `4` | Applies or references the 'HealthGain' effect/state. |
| `SpeedUp` | Number | `2` | Applies or references the 'SpeedUp' effect/state. |

</details>

---

### Context: `StatusGroup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `mutant_pool, parasites` | Generates an item drop from the specified loot pool. |

</details>

---

### Context: `TinkererBasicAttackSwitching`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `craft_ability` | [`Enum/String`](./Enums.md#enum-craft_ability) | `TinkererCraft` |  |
| `throw_ability` | [`Enum/String`](./Enums.md#enum-throw_ability) | `TinkererThrow` |  |

</details>

---

### Context: `TransformOnElementInfluencex`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Holy` | Specific element type required or applied. |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Bait, PurifiedPoisonFood` |  |

</details>

---

### Context: `Washer`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee` |  |
| `name` | String | `"ENEMY_CULTISTWASHER_NAME"` | Localization key for the character's name. |
| `partial_animation_suffix` | String | `"Cultist"` |  |
| `tooltip` | String | `"ENEMY_CULTISTWASHER_DESC"` |  |

</details>

---

### Context: `WereMan`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"WereMan"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `WereManFurySwipes` |  |
| `name` | String | `"ENEMY_WEREMAN_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_WEREMAN_DESC"` |  |

</details>

---

### Context: `Zealot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Zealot"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BBStabby` |  |
| `name` | String | `"ENEMY_CULTISTZEALOT_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CULTISTZEALOT_DESC"` |  |

</details>

---

### Context: `ZealotBomb`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"BombZealot"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BBExplode` |  |
| `name` | String | `"ENEMY_BOMBZEALOT_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_BOMBZEALOT_DESC"` |  |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TVBotDie` | Number | `1` | Applies or references the 'TVBotDie' effect/state. |
| `TVBotDumb` | Number | `1` | Applies or references the 'TVBotDumb' effect/state. |
| `TVBotObey` | Number | `1` | Applies or references the 'TVBotObey' effect/state. |
| `TVBotStop` | Number | `1` | Applies or references the 'TVBotStop' effect/state. |

</details>

---

### Context: `1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `1` |  |
| `partial_animation_suffix` | Number | `1` |  |
| `uifloaters_offset` | Number | `1.4` |  |

</details>

---

### Context: `4`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `4` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee_4Hits` |  |
| `partial_animation_suffix` | Number | `4` |  |

</details>

---

### Context: `AllStatsAura`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `aura_requires_tag` | [`Enum/String`](./Enums.md#enum-aura_requires_tag) | `humanoid` |  |
| `range` | [`Enum/String`](./Enums.md#enum-range) | `global` | Distance or area of effect in tiles. |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `Big`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Big, "Big"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `GameteSpawn` |  |

</details>

---

### Context: `BlackHole`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"BlackHole"` |  |
| `name` | String | `"OBJECT_BLACKHOLE_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"OBJECT_BLACKHOLE_DESC"` |  |

</details>

---

### Context: `ChaosBossFormChangeGuide`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `active_pieces` | [`Array`](./Arrays.md#array-active_pieces) | `[ Johnny Throb Flush ]` |  |
| `passive_pieces` | [`Array`](./Arrays.md#array-passive_pieces) | `[ Host Nettle Bubs ]` |  |
| `passives_health_threshold` | Number | `50%` |  |

</details>

---

### Context: `ChaosHeadDropIn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `ChaosSpawnIn` | The specific ability ID to cast. |
| `new_music` | [`Enum/String`](./Enums.md#enum-new_music) | `chaos_boss_part2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `riftheadguardian` | Specific entity tag required. |

</details>

---

### Context: `Default`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `LennyShove` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `LennyTrampleMove` |  |
| `partial_animation_suffix` | String | `""` |  |

</details>

---

### Context: `Explody`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Expl` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `ToxExplode` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |

</details>

---

### Context: `FaceAwayLastDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean | `true` |  |
| `override_hit_animation` | Boolean | `true` |  |
| `use_turn_animations` | Boolean | `true` |  |

</details>

---

### Context: `FinalBossBeamQueue`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `queue` | [`Enum/String`](./Enums.md#enum-queue) | `TheChild_TargetBeam` |  |
| `release` | [`Enum/String`](./Enums.md#enum-release) | `TheChild_ReleaseBeams` |  |
| `transform` | [`Enum/String`](./Enums.md#enum-transform) | `TheChild_TransformBoris` |  |

</details>

---

### Context: `FinalBossHitCountdownHoly`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `icon` | Number | `804` |  |
| `icon_ready` | Number | `805` |  |
| `stacks` | Number | `7` | Number of stacks or intensity to apply. |

</details>

---

### Context: `HitlerExecute`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `HitlerShoot` | The specific ability ID to cast. |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `grown_hitler_clone` | Specific entity tag required. |
| `threshold` | Number | `15` |  |

</details>

---

### Context: `HumanDead`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `DH` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `HCSpin` |  |
| `tooltip` | String | `"ENEMY_HUMANCAT2_DESC"` |  |

</details>

---

### Context: `InfiniteRebirth`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `health` | Number | `25%` |  |
| `immediate` | Boolean | `true` |  |
| `playercat_health` | Number | `25%` |  |

</details>

---

### Context: `Lifted`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Lift"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |

</details>

---

### Context: `MoveAwayWhenEnemyAdjacent`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `YA_Jetpack` |  |
| `once_per_turn` | Boolean | `true` |  |
| `weights` | [`Enum/String`](./Enums.md#enum-weights) | `stay_far_always_move` |  |

</details>

---

### Context: `MoveForBarrage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `ZaratanaVSBombardment` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_far` |  |

</details>

---

### Context: `MoveForDash`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `attack` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance` |  |

</details>

---

### Context: `MoveForGrass`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `StegoGrassStomp` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `StegoEatGrass` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `minimum_move` |  |

</details>

---

### Context: `MoveForPounce`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `attack` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance` |  |

</details>

---

### Context: `MoveForSpin`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `PyrophinaVSRun` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `PyrophinaVSSpinThrow` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_close` |  |

</details>

---

### Context: `MoveOneForPuke`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `AlienBeastMoveOne` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `AlienBeastPuke` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance` |  |

</details>

---

### Context: `MoveToHead`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `G3RunToHead` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `G3GrabHead` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `minimum_move` |  |

</details>

---

### Context: `MoveTowards`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `attack` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_close` |  |

</details>

---

### Context: `Normal`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `TinaBasicBigMeleeA, SpewerLobbed_Normal` |  |
| `animation_suffix` | String | `"Up"` |  |

</details>

---

### Context: `Nuke`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Nuke` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `knockback` | Number | `5` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status` | Classification/category type. |

</details>

---

### Context: `Sitting`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Chair` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `DoNothing` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `DoNothing` |  |

</details>

---

### Context: `SquirrelForm`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee` |  |
| `tooltip` | [`Enum/String`](./Enums.md#enum-tooltip) | `ENEMY_DRAVENSQUIRRELFORM_DESC` |  |

</details>

---

### Context: `StacyMutant_Health`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddMaxHealth` | Number | `25` | Applies or references the 'AddMaxHealth' effect/state. |
| `AddSpeed` | Number | `-3` | Applies or references the 'AddSpeed' effect/state. |
| `SizeScale` | Number | `1.2` | Applies or references the 'SizeScale' effect/state. |

</details>

---

### Context: `StacyMutant_Ice`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddMovement` | Number | `-1` | Applies or references the 'AddMovement' effect/state. |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Ice` | Applies or references the 'ElementImmune' effect/state. |
| `ReplaceBasicAttack` | [`Enum/String`](./Enums.md#enum-replacebasicattack) | `SM_IceBreath` | Applies or references the 'ReplaceBasicAttack' effect/state. |

</details>

---

### Context: `StacyMutant_Speed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddDamage` | Number | `-1` | Applies or references the 'AddDamage' effect/state. |
| `AddSpeed` | Number | `6` | Applies or references the 'AddSpeed' effect/state. |
| `SizeScale` | [`Enum/String`](./Enums.md#enum-sizescale) | `.8` | Applies or references the 'SizeScale' effect/state. |

</details>

---

### Context: `SuckMF`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `TormentorSuck` | The specific ability ID to cast. |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `careless` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance` |  |

</details>

---

### Context: `SupportFormChangeInsteadOfRun`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `SBotAnger, TVChangeDie` | The specific ability ID to cast. |
| `wait_till_turn` | Boolean | `true` |  |

</details>

---

### Context: `T3HitlerSpawningPhase`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `T3JoinFight` | Flag |  | Applies or references the 'T3JoinFight' effect/state. |
| `T3Spawn_Colorless` | Flag |  | Applies or references the 'T3Spawn_Colorless' effect/state. |
| `spell_use_groups` | [`Array`](./Arrays.md#array-spell_use_groups) | `[ [ T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T...` |  |

</details>

---

### Context: `TransformOnStatusThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Moth` |  |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `AllStatsUp` | ID of the status effect to apply or check. |
| `threshold` | Number | `5` |  |

</details>

---

### Context: `TwisterFling`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `5` | The base damage properties of an attack. |
| `max_dist` | Number | `5` |  |
| `min_dist` | Number | `3` |  |

</details>

---

### Context: `Unflip`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `TeleportFlipUp` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `Spin_Enemy` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_close_always_move` |  |

</details>

---

### Context: `Up`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Up"` |  |
| `tooltip` | String | `"OBJECT_TIREUP_DESC"` |  |

</details>

---

### Context: `ai_if_spawned_as_enemy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `brain` | [`Enum/String`](./Enums.md#enum-brain) | `PatternBrain` |  |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `default` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance` |  |

</details>

---

### Context: `dispersed_bonusturn_pattern`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do` | [`Enum/String`](./Enums.md#enum-do) | `Simon_Trash, attack, Simon_Tentacle` |  |

</details>

---

### Context: `other_form_change_abilities`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Boris` | [`Enum/String`](./Enums.md#enum-boris) | `MegaGuppy_TransformBoris` | Character Form / AI State: Behavior and stats for the 'Boris' state. |
| `Explosive` | [`Enum/String`](./Enums.md#enum-explosive) | `MegaGuppy_TransformExplosive` | Character Form: Behavior and stats for the 'Explosive' state. |
| `Holy` | [`Enum/String`](./Enums.md#enum-holy) | `MegaGuppy_TransformHoly` | Character Form: Behavior and stats for the 'Holy' state. |

</details>

---

### Context: `statuses`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |

</details>

---

### Context: `5`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee_5Hits` |  |
| `partial_animation_suffix` | Number | `5` |  |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fury` | Number | `75` | Applies or references the 'Fury' effect/state. |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `ZombieTombstone` | The ID of the ability to autocast. |
| `even_if_stunned` | Boolean | `true` | If true, bypasses stun and hard-CC restrictions to cast anyway. |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `BackflipDodge` | The specific dodge ability to trigger (e.g., DestroyerDodge). |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `Boris`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"2"` |  |

</details>

---

### Context: `CerberubsAggroTargetBehavior`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `alert_form` | [`Enum/String`](./Enums.md#enum-alert_form) | `Alert` |  |
| `default_form` | [`Enum/String`](./Enums.md#enum-default_form) | `Normal` |  |

</details>

---

### Context: `CerberubsJumpBlind`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `CerberubsJump` | The specific ability ID to cast. |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `nubs_fakeblind` |  |

</details>

---

### Context: `CerberubsJumpNormal`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `CerberubsJump` | The specific ability ID to cast. |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `default` |  |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `DybbukBackflipDodge` | The specific ability ID to cast. |
| `chance` | Number | `100%` | Probability (0.0 to 1.0) of executing this action. |

</details>

---

### Context: `ChanceToFormChangeOnAbilityDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `15%` | Probability (0.0 to 1.0) of executing this action. |
| `form` | [`Enum/String`](./Enums.md#enum-form) | `Flop2` |  |

</details>

---

### Context: `ChaosBossPieces`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `active_pieces` | [`Array`](./Arrays.md#array-active_pieces) | `[ Johnny Throb Flush ]` |  |
| `passive_pieces` | [`Array`](./Arrays.md#array-passive_pieces) | `[ Host Nettle Bubs ]` |  |

</details>

---

### Context: `Charging`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `MoonHead_Blow` |  |
| `partial_animation_suffix` | String | `"Charging"` |  |

</details>

---

### Context: `CloseConvert`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MarshmallowConvert` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_close` |  |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `odds` | Number | `0.5` | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. |

</details>

---

### Context: `CounterAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `StegoTailSwipe` | The specific ability ID to cast. |
| `without_orienting` | Boolean | `true` |  |

</details>

---

### Context: `DelayedAutoRevive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `health` | Number | `50%` |  |
| `rounds` | Number | `1` |  |

</details>

---

### Context: `DiceBehavior`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dice_size` | Number | `6` |  |
| `knockback_damage` | Number | `5` |  |

</details>

---

### Context: `DiesToElement`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Fire` | Specific element type required or applied. |
| `instant` | Boolean | `true` |  |

</details>

---

### Context: `DybbukPossessionFallback`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `exit_ability` | [`Enum/String`](./Enums.md#enum-exit_ability) | `DybbukReturn` |  |
| `form` | [`Enum/String`](./Enums.md#enum-form) | `Possessing` |  |

</details>

---

### Context: `Empty`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `""` |  |

</details>

---

### Context: `Explosive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"3"` |  |

</details>

---

### Context: `FightPhase`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `T3Shoot` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `FloatMove` |  |

</details>

---

### Context: `FinalBossBecomeTheChild`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `GlobalSpawnCharacter` | [`Enum/String`](./Enums.md#enum-globalspawncharacter) | `MegaGuppy` | Applies or references the 'GlobalSpawnCharacter' effect/state. |
| `PlayBackground` | Number | `1` | Applies or references the 'PlayBackground' effect/state. |

</details>

---

### Context: `FinalBossShieldHealth`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `break_ability` | [`Enum/String`](./Enums.md#enum-break_ability) | `DestroyerBreakShield` |  |
| `state_health` | [`Array`](./Arrays.md#array-state_health) | `[ 0 35 35 35 35 0 ]` |  |

</details>

---

### Context: `FireFull`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Full` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `SpewerSpit` |  |

</details>

---

### Context: `FoodMove`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `CaveBabyFoodMove` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_close_move_if_possible` |  |

</details>

---

### Context: `ForceTrample`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `BirthwortTrample` | The specific ability ID to cast. |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `always_cast_careless` |  |

</details>

---

### Context: `GainDisorderFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.1` | Probability (0.0 to 1.0) of executing this action. |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `diseases` |  |

</details>

---

### Context: `HPAltStates`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `clipname` | [`Enum/String`](./Enums.md#enum-clipname) | `poopmain` |  |
| `thresholds` | [`Array`](./Arrays.md#array-thresholds) | `[ [ 1 0 ]` |  |

</details>

---

### Context: `HalfDead`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"2"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `RatKingDash` |  |

</details>

---

### Context: `HasDeadCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"CatDead"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `LennyCatSlap` |  |

</details>

---

### Context: `HasRock`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"rock"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `AmoebaRockBash` |  |

</details>

---

### Context: `HealNeighborsEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | `true` |  |
| `stacks` | Number | `3` | Number of stacks or intensity to apply. |

</details>

---

### Context: `Holy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"1"` |  |

</details>

---

### Context: `InitialPhase`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `T3Shoot` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `FloatMove` |  |

</details>

---

### Context: `JohnnyNeedsWashing`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `form_unwashed` | [`Enum/String`](./Enums.md#enum-form_unwashed) | `Unwashed` |  |
| `form_washed` | [`Enum/String`](./Enums.md#enum-form_washed) | `Washed` |  |

</details>

---

### Context: `LeapClose`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `GKLeap` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `towards_aggro` |  |

</details>

---

### Context: `LowerAmbientLight`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `amount` | [`Array`](./Arrays.md#array-amount) | `[ 50% 60% 60% ]` | The target opacity/dimness level. |
| `speed` | Number | `4` | The transition speed. |

</details>

---

### Context: `ModularPickup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Cleanse` | Number | `0` | Applies or references the 'Cleanse' effect/state. |
| `sound_event` | [`Enum/String`](./Enums.md#enum-sound_event) | `EatAntidote` |  |

</details>

---

### Context: `Mount`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `eject_ability` | [`Enum/String`](./Enums.md#enum-eject_ability) | `MechSuitEject` |  |
| `enter_ability` | [`Enum/String`](./Enums.md#enum-enter_ability) | `EnterMech` |  |

</details>

---

### Context: `MoveSpaced`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `terminator_keep_distance_always_move` |  |

</details>

---

### Context: `MultiSpawnOnDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | [`Array`](./Arrays.md#array-count) | `[ 0, 2 ]` | The numerical quantity. |
| `obj` | [`Enum/String`](./Enums.md#enum-obj) | `Maggot` |  |

</details>

---

### Context: `NCGravecrawlFAR`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `NCGravecrawl` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_far` |  |

</details>

---

### Context: `NormalFull`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Full` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `SpewerSpit` |  |

</details>

---

### Context: `Open`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Open` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `GSOpenAttack` |  |

</details>

---

### Context: `PassiveWhileNotHasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `ExistUntilIdleUpkeep, DemonicGlyph_Movement` | ID of the status effect to apply or check. |

</details>

---

### Context: `Primed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `GA_Telekinesis_Big` |  |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `primed` |  |

</details>

---

### Context: `ReturnA`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `HangerBotReturn` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_close` |  |

</details>

---

### Context: `RunFar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `PyrophinaVSRun` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `run_far` |  |

</details>

---

### Context: `RunWhenLastPlayerCatIsCharmed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean | `true` |  |
| `legacy_savekey` | [`Enum/String`](./Enums.md#enum-legacy_savekey) | `Legacy_Marshmallow_StolenCatID` |  |

</details>

---

### Context: `ScalingAttackAnimation`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `default` | [`Enum/String`](./Enums.md#enum-default) | `bite1` | Baseline configuration. |
| `thresholds` | [`Array`](./Arrays.md#array-thresholds) | `[ [ 5, bite2 ]` |  |

</details>

---

### Context: `SkipFirstRounds`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pop_chance` | Number | `50%` |  |
| `stacks` | Number | `2` | Number of stacks or intensity to apply. |

</details>

---

### Context: `Small`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `""` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `GameteInflate` |  |

</details>

---

### Context: `StacyMutant_Damage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddDamage` | Number | `2` | Applies or references the 'AddDamage' effect/state. |
| `AddMaxHealth` | Number | `-25` | Applies or references the 'AddMaxHealth' effect/state. |

</details>

---

### Context: `StacyMutant_Fire`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Fire` | Applies or references the 'ElementImmune' effect/state. |
| `ReplaceBasicAttack` | [`Enum/String`](./Enums.md#enum-replacebasicattack) | `SM_Lavashot` | Applies or references the 'ReplaceBasicAttack' effect/state. |

</details>

---

### Context: `StacyMutant_Lightning`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Electric` | Applies or references the 'ElementImmune' effect/state. |
| `ReplaceBasicAttack` | [`Enum/String`](./Enums.md#enum-replacebasicattack) | `SM_LightningDash` | Applies or references the 'ReplaceBasicAttack' effect/state. |

</details>

---

### Context: `Standing`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BungaSmash` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `DefaultMove` |  |

</details>

---

### Context: `Standing2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BungaSmash` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `BungaJumpMove` |  |

</details>

---

### Context: `StatusAfterXTurns`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `CancerExplode` | Logic: Forces the execution of a specific ability. |
| `stacks` | Number | `3` | Number of stacks or intensity to apply. |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RemoveAmbientLightEffects` | Number | `4` | Applies or references the 'RemoveAmbientLightEffects' effect/state. |
| `RemoveGlobalModifiers` | [`Array`](./Arrays.md#array-removeglobalmodifiers) | `[ BloodRain ]` | Applies or references the 'RemoveGlobalModifiers' effect/state. |

</details>

---

### Context: `StatusOnSpawnIn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Number | `1` | Applies or references the 'CaptureFamiliar' effect/state. |
| `SetHealth` | Number | `50%` | Applies or references the 'SetHealth' effect/state. |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ConstitutionUp` | Number | `-1` | Applies or references the 'ConstitutionUp' effect/state. |
| `StrengthUp` | Number | `-1` | Applies or references the 'StrengthUp' effect/state. |

</details>

---

### Context: `SupportDieInsteadOfRun`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `alt_dead_ani` | [`Enum/String`](./Enums.md#enum-alt_dead_ani) | `off` |  |
| `alt_dying_ani` | [`Enum/String`](./Enums.md#enum-alt_dying_ani) | `shutdown` |  |

</details>

---

### Context: `SwimmingFormChange`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `form_in` | [`Enum/String`](./Enums.md#enum-form_in) | `Water` |  |
| `form_out` | [`Enum/String`](./Enums.md#enum-form_out) | `Out` |  |

</details>

---

### Context: `SwitchMusic`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `new_layer` | [`Enum/String`](./Enums.md#enum-new_layer) | `event` | The specific audio layer to transition to (e.g., map, battle). |
| `new_song` | [`Enum/String`](./Enums.md#enum-new_song) | `same` | The ID of the new music track. |

</details>

---

### Context: `SwordAndShield_Primed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Holy"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `DestroyerAttack` |  |

</details>

---

### Context: `TF_TargetAllies`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `TwistingFlames` | The specific ability ID to cast. |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `util_target_allies` |  |

</details>

---

### Context: `TF_TargetEnemies`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `TwistingFlames` | The specific ability ID to cast. |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `util_target_enemies` |  |

</details>

---

### Context: `TarFull`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Full` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `SpewerSpit` |  |

</details>

---

### Context: `Terminator2Run`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `T2GoopRun` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_far_always_move` |  |

</details>

---

### Context: `TerminatorChase`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `T1ChokeReaction` | The specific ability ID to cast. |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `MoveOne` |  |

</details>

---

### Context: `TerminatorSkin`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `groups` | [`Array`](./Arrays.md#array-groups) | `[ { stacks 48 ParticleBurst Gibs_terminatorskin CatPartsT...` |  |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Brace` | ID of the status effect to apply or check. |

</details>

---

### Context: `UnlimitedDeathRattleRevive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MD_Lift` | The specific ability ID to cast. |
| `even_if_stunned` | Boolean | `true` |  |

</details>

---

### Context: `UseAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `Destroyer2HolyAttack` | The ID of the ability to trigger. |
| `respect_prime` | Boolean | `true` | If true, respects the ability's prime/cooldown state. |

</details>

---

### Context: `UseAbilityWhenOutOfStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `QueenHippoHeartAttack` | The specific ability ID to cast. |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Brace` | ID of the status effect to apply or check. |

</details>

---

### Context: `alternate_energized_effect`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FormChange` | [`Enum/String`](./Enums.md#enum-formchange) | `GuaranteedJackpot` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `SpellDamageUp` | Number | `1` | Applies or references the 'SpellDamageUp' effect/state. |

</details>

---

### Context: `passive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `DoNothing` |  |

</details>

---

### Context: `statuses_on_enter_form`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `UseAbility` | [`Enum/String`](./Enums.md#enum-useability) | `KirbySpit` | Logic: Forces execution of an ability. |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Leech` | Number | `2` | Applies or references the 'Leech' effect/state. |

</details>

---

### Context: `AddStatusToTrampleDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |

</details>

---

### Context: `AggroTargetIsGovernedByHitEffect`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | `false` |  |

</details>

---

### Context: `Alert`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Alert` |  |

</details>

---

### Context: `Angry`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"Angry"` |  |

</details>

---

### Context: `BellyFull`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"Belly"` |  |

</details>

---

### Context: `BigHolding`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"BigHolding"` |  |

</details>

---

### Context: `BigHoldingCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"BigHoldingCat"` |  |

</details>

---

### Context: `Bomb`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Button` |  |

</details>

---

### Context: `Conditional_HasKnockback`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RemoveKnockback` | Number | `1` | Applies or references the 'RemoveKnockback' effect/state. |

</details>

---

### Context: `Conditional_IsPhysicalAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RemoveKnockback` | Number | `1` | Applies or references the 'RemoveKnockback' effect/state. |

</details>

---

### Context: `CreateGlobalModifiers`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `BloodRain` | Number | `1` | Applies or references the 'BloodRain' effect/state. |

</details>

---

### Context: `DiesToPiercingAndSpikes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `deferred` | Boolean | `true` |  |

</details>

---

### Context: `DodgeWhenTargeted`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `ShadowstepDodge` | The specific ability ID to cast. |

</details>

---

### Context: `Drunker`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Drunk` |  |

</details>

---

### Context: `FaceLastDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean | `true` |  |

</details>

---

### Context: `FinalBossSyncAnimations`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `other_character` | [`Enum/String`](./Enums.md#enum-other_character) | `MegaGuppy` |  |

</details>

---

### Context: `Fire`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `SpewerLobbed_Lava` |  |

</details>

---

### Context: `Flop`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Down"` |  |

</details>

---

### Context: `Flop2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Down"` |  |

</details>

---

### Context: `FlushHost`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Host` |  |

</details>

---

### Context: `Grappling`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Grapple` |  |

</details>

---

### Context: `Guarding`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"Guarding"` |  |

</details>

---

### Context: `Headless`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Headless"` |  |

</details>

---

### Context: `Hint_CrackedVisuals`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Cracked"` |  |

</details>

---

### Context: `Hint_CrackedVisuals2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"ChargingCracked"` |  |

</details>

---

### Context: `Hint_CrackedVisuals3`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"SwallowedCracked"` |  |

</details>

---

### Context: `Holding`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"Holding"` |  |

</details>

---

### Context: `Insane_Ceiling`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Insane"` |  |

</details>

---

### Context: `Insane_Ground`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Insane"` |  |

</details>

---

### Context: `JohnnyHost`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Host` |  |

</details>

---

### Context: `Joystick`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Joystick"` |  |

</details>

---

### Context: `Lit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Lit` |  |

</details>

---

### Context: `MotherGrowController`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tumor_object` | [`Enum/String`](./Enums.md#enum-tumor_object) | `MotherTumor` |  |

</details>

---

### Context: `Mounted`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Cat"` |  |

</details>

---

### Context: `MouthFull`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"MouthFull"` |  |

</details>

---

### Context: `MoveAfterAnyAttemptedAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `weights` | [`Enum/String`](./Enums.md#enum-weights) | `bat_chaos_runaway` |  |

</details>

---

### Context: `MoveAwayFromDamageSource`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `BirdFly` |  |

</details>

---

### Context: `NoEyes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"0"` |  |

</details>

---

### Context: `NoStick`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `ManglerJab` |  |

</details>

---

### Context: `Nothing`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `spawn` |  |

</details>

---

### Context: `Off`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Off` |  |

</details>

---

### Context: `OneEye`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"1"` |  |

</details>

---

### Context: `OpenCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `OpenCat` |  |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Fire` | Specific element type required or applied. |

</details>

---

### Context: `Possessing`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Possessing"` |  |

</details>

---

### Context: `SharePickups`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `include_coins` | Boolean | `true` |  |

</details>

---

### Context: `SmallHolding`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Holding"` |  |

</details>

---

### Context: `SmallHoldingCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"HoldingCat"` |  |

</details>

---

### Context: `StacyMutant_Brace`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `3` | Applies or references the 'Brace' effect/state. |

</details>

---

### Context: `StacyMutant_Counter`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CounterAttack` | [`Enum/String`](./Enums.md#enum-counterattack) | `SM_BleedCounter` | Reaction: Executes a counter-attack ability when hit. |

</details>

---

### Context: `StacyMutant_DoubleHead`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ExtraDispersedTurns` | Number | `1` | Applies or references the 'ExtraDispersedTurns' effect/state. |

</details>

---

### Context: `StacyMutant_Holy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `7` | Applies or references the 'DivineShield' effect/state. |

</details>

---

### Context: `StacyMutant_Mirror`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ReflectProjectiles` | Number | `100%` | Passive: Reflects incoming projectiles back at the attacker. |

</details>

---

### Context: `StacyMutant_Thorns`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | `3` | Applies or references the 'Thorns' effect/state. |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |

</details>

---

### Context: `StatusEachTurnEndIfEnabledAtStartOfTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `T2UnClone` | Logic: Forces the execution of a specific ability. |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpeedUp_WithoutInitiative` | Number | `1` | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. |

</details>

---

### Context: `StatusOnEnemyConfused`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ImmediateUseAbility` | [`Enum/String`](./Enums.md#enum-immediateuseability) | `FuzzerReact` | Applies or references the 'ImmediateUseAbility' effect/state. |

</details>

---

### Context: `StatusOverlappingCharactersAndDie`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |

</details>

---

### Context: `StatusWhenStatusCompletelyRemoved`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `BackflipWhenTargeted` | ID of the status effect to apply or check. |

</details>

---

### Context: `StunImmunity`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean | `false` |  |

</details>

---

### Context: `SwordAndShield`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `DestroyerAttack` |  |

</details>

---

### Context: `SyncFormsWithBuddy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `no_buddy` | [`Enum/String`](./Enums.md#enum-no_buddy) | `Rage` |  |

</details>

---

### Context: `Tar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `SpewerLobbed_Tar` |  |

</details>

---

### Context: `ThrobHost`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Host` |  |

</details>

---

### Context: `Unlit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Unlit` |  |

</details>

---

### Context: `Unwashed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Unwashed` |  |

</details>

---

### Context: `Water`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"Water"` |  |

</details>

---

### Context: `additional_statuses`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `PermanentMadness` | Number | `1` | Applies or references the 'PermanentMadness' effect/state. |

</details>

---

### Context: `exit_animations`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Default` | [`Enum/String`](./Enums.md#enum-default) | `release` | Character Form: The baseline default behavior state. |

</details>

---

### Context: `round_start_bonusturn_pattern`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do_priority` | [`Array`](./Arrays.md#array-do_priority) | `[ MutateAOE SpawnMaggots ]` |  |

</details>

---

### Context: `0`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `AddStatusToReceivedDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `AdventureTokenPassivePool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `AllAlive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Attacker`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `BirdRewards`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Bully`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Close`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Damaged`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Default_Ceiling`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Default_Ground`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `DesireMech`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Die`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Dumb`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Else`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Flush`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `FlushBubs`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `FlushNettle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `GuaranteedJackpot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Johnny`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `JohnnyBubs`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `JohnnyNettle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `LastHit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `MotherTumorSpawnInCapture`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `NeutronStar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `NotPriming`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Obey`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `OffMap`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `OffScreen`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `OneAlive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Out`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `PassiveWhenDead`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Priming`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Rain`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `RandomPassivePool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Robot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `SpawningPhase`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Start_Ceiling`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Stop`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `TempPassiveUntilSettled`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Throb`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ThrobBubs`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ThrobNettle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Transformed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `TwoAlive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `TwoEyes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Washed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `active`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `damage_instance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `default`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `virtual_abilities`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

## Combat Rewards

### Context: `boss`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`1`](./Combat_Rewards.md#context-1), [`2`](./Combat_Rewards.md#context-2), [`3`](./Combat_Rewards.md#context-3), [`4`](./Combat_Rewards.md#context-4)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins` | [`Array`](./Arrays.md#array-coins) | `[ 10 20 ]` |  |
| `consumable_chance` | [`Enum/String`](./Enums.md#enum-consumable_chance) | `.5` |  |
| `food` | [`Array`](./Arrays.md#array-food) | `[ 5 8 ], [ 6 12 ], [ 10 15 ]` |  |
| `item_chance` | Number | `1` |  |

</details>

---

### Context: `hard`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`1`](./Combat_Rewards.md#context-1), [`2`](./Combat_Rewards.md#context-2), [`3`](./Combat_Rewards.md#context-3), [`4`](./Combat_Rewards.md#context-4)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins` | [`Array`](./Arrays.md#array-coins) | `[ 1 6 ]` |  |
| `consumable_chance` | [`Enum/String`](./Enums.md#enum-consumable_chance) | `.25` |  |
| `food` | [`Array`](./Arrays.md#array-food) | `[ 4 7 ]` |  |
| `item_chance` | [`Enum/String`](./Enums.md#enum-item_chance) | `.25` |  |

</details>

---

### Context: `miniboss`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`1`](./Combat_Rewards.md#context-1), [`2`](./Combat_Rewards.md#context-2), [`3`](./Combat_Rewards.md#context-3), [`4`](./Combat_Rewards.md#context-4)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins` | [`Array`](./Arrays.md#array-coins) | `[ 10 20 ]` |  |
| `consumable_chance` | [`Enum/String`](./Enums.md#enum-consumable_chance) | `.3` |  |
| `food` | [`Array`](./Arrays.md#array-food) | `[ 5 10 ], [ 2 5 ], [ 4 8 ]` |  |
| `item_chance` | [`Enum/String`](./Enums.md#enum-item_chance) | `.5` |  |

</details>

---

### Context: `normal`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`1`](./Combat_Rewards.md#context-1), [`2`](./Combat_Rewards.md#context-2), [`3`](./Combat_Rewards.md#context-3), [`4`](./Combat_Rewards.md#context-4)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins` | [`Array`](./Arrays.md#array-coins) | `[ 1 6 ]` |  |
| `consumable_chance` | [`Enum/String`](./Enums.md#enum-consumable_chance) | `.25` |  |
| `food` | [`Array`](./Arrays.md#array-food) | `[ 1 3 ]` |  |
| `item_chance` | [`Enum/String`](./Enums.md#enum-item_chance) | `.25` |  |

</details>

---

### Context: `1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins_bonus` | [`Enum/String`](./Enums.md#enum-coins_bonus) | `.5, 1` |  |
| `food_bonus` | Number | `1` |  |
| `boss` | [`Block`](./Combat_Rewards.md#context-boss) | `{ ... }` |  |
| `hard` | [`Block`](./Combat_Rewards.md#context-hard) | `{ ... }` |  |
| `miniboss` | [`Block`](./Combat_Rewards.md#context-miniboss) | `{ ... }` |  |
| `normal` | [`Block`](./Combat_Rewards.md#context-normal) | `{ ... }` |  |
| `chapters` | Block | `{ ... }` |  |

</details>

---

### Context: `2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins_bonus` | Number | `1, .75` |  |
| `food_bonus` | Number | `1, 1.75` |  |
| `boss` | [`Block`](./Combat_Rewards.md#context-boss) | `{ ... }` |  |
| `hard` | [`Block`](./Combat_Rewards.md#context-hard) | `{ ... }` |  |
| `miniboss` | [`Block`](./Combat_Rewards.md#context-miniboss) | `{ ... }` |  |
| `normal` | [`Block`](./Combat_Rewards.md#context-normal) | `{ ... }` |  |
| `chapters` | Block | `{ ... }` |  |

</details>

---

### Context: `3`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins_bonus` | Number | `1` |  |
| `food_bonus` | Number | `2.5, 1` |  |
| `boss` | [`Block`](./Combat_Rewards.md#context-boss) | `{ ... }` |  |
| `hard` | [`Block`](./Combat_Rewards.md#context-hard) | `{ ... }` |  |
| `miniboss` | [`Block`](./Combat_Rewards.md#context-miniboss) | `{ ... }` |  |
| `normal` | [`Block`](./Combat_Rewards.md#context-normal) | `{ ... }` |  |
| `chapters` | Block | `{ ... }` |  |

</details>

---

### Context: `4`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `boss` | [`Block`](./Combat_Rewards.md#context-boss) | `{ ... }` |  |
| `coins_bonus` | Number | `1` |  |
| `food_bonus` | Number | `1` |  |
| `hard` | [`Block`](./Combat_Rewards.md#context-hard) | `{ ... }` |  |
| `miniboss` | [`Block`](./Combat_Rewards.md#context-miniboss) | `{ ... }` |  |
| `normal` | [`Block`](./Combat_Rewards.md#context-normal) | `{ ... }` |  |

</details>

---

## Custom Cats

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `texture` | Number | `1000, 1002, 1050` |  |
| `default_frame` | Number | `1000, 1001, 1002` |  |
| `palette` | Number | `137, 9, 16` |  |
| `righteye` | Number | `1001, 1, 1006` |  |
| `voice` | [`Enum/String`](./Enums.md#enum-voice) | `male1, male4, female2` |  |
| `lefteye` | Number | `1001, 1033, 1006` |  |
| `claws` | Number | `2, 1032, 1` |  |
| `mouth` | Number | `2, 1001, 1005` |  |
| `rightear` | Number | `1001, 1004, 3` |  |
| `leftear` | Number | `1005, 1, 1004` |  |
| `head` | Number | `1001, 1080, 1028` |  |
| `tail` | Number | `1001, 1010, 26` |  |
| `arm2` | Number | `1001, 42, 3` |  |
| `arm1` | Number | `2, 1018, 3` |  |
| `righteyebrow` | Number | `1001, 1005, 1006` |  |
| `lefteyebrow` | Number | `1001, 1005, 1006` |  |
| `leg1` | Number | `1001, 1, 3` |  |
| `body` | Number | `1000, 1001, 1028` |  |
| `leg2` | Number | `1019, 1001, 3` |  |
| `pitch` | Number | `2, .7, .5` |  |
| `class_anis` | [`Enum/String`](./Enums.md#enum-class_anis) | `Tank, Mage, Hunter` |  |
| `default_face` | [`Enum/String`](./Enums.md#enum-default_face) | `mad, worried, happy` |  |
| `face` | Number | `1019, 1004` |  |

</details>

---

### Context: `arm1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `frame` | Number | `1040` |  |
| `texture` | Number | `1` |  |

</details>

---

### Context: `arm2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `frame` | Number | `1040` |  |
| `texture` | Number | `1` |  |

</details>

---

## Difficulties

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `bonus_itemroll_luck` | Number | `8, 0, 16` |  |
| `boss_health_multiplier` | Number | `1.4, 1, 1.2` |  |
| `coins_multiplier` | Number | `1, 1.5, 1.25` |  |
| `easy` | [`Block`](./Difficulties.md#context-easy) | `{ ... }` |  |
| `event_difficulty` | Number | `1, 2, 0` |  |
| `food_multiplier` | Number | `1, 1.5, 1.25` |  |
| `hard` | [`Block`](./Difficulties.md#context-hard) | `{ ... }` |  |
| `wallet_size` | Number | `99` |  |
| `boss_elite_buffs` | Number | `2, 1, 3` |  |

</details>

---

### Context: `hard`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Difficulties.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `champ_budget` | Number | `2, 1, 1.5` |  |
| `champ_chance_mini` | Number | `1, .5, .25` |  |
| `elite_buffs` | Number | `2, 1, 3` |  |
| `rare_elite_buffs` | Number | `2, 1, 3` |  |
| `elite_budget` | Number | `2, 1, 3` |  |
| `elite_chance_mini` | Number | `1, .5, .25` |  |

</details>

---

### Context: `easy`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Difficulties.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `champ_budget` | Number | `1, 0, 999` |  |
| `elite_budget` | Number | `1, 2, 0` |  |
| `elite_buffs` | Number | `2, 1, 3` |  |
| `rare_elite_buffs` | Number | `2, 1, 3` |  |
| `champ_chance_mini` | Number | `1, .5, .25` |  |
| `elite_chance_mini` | Number | `1, .5, .25` |  |

</details>

---

## Elite Buffs

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `icon_frame` | Number | `500, 501, 502` |  |
| `passives` | [`Block`](./Elite_Buffs.md#context-passives) | `{ ... }` |  |
| `value` | Number | `1` |  |
| `unique` | Boolean | `true` |  |
| `specific_chapter` | Number | `2, 1, 3` |  |
| `minion_alt` | [`Enum/String`](./Enums.md#enum-minion_alt) | `SlightlyDepressing, SubUndying, SubTwin` |  |
| `rollable` | Boolean | `false` |  |
| `only_at_battle_start` | Boolean | `true` |  |
| `requires_corpse` | Boolean | `true` |  |
| `roll_limit` | Number | `2` |  |

</details>

---

### Context: `passives`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Elite_Buffs.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `EliteTint` | [`Array`](./Arrays.md#array-elitetint) | `[ .4 .4 .4 ], [ .6 .6 .6 .50 ], red` |  |
| `EliteParticle` | [`Enum/String`](./Enums.md#enum-eliteparticle) | `SparkleBuff, Lava_Distortion, SpikeBuff` |  |
| `HealthMultiplier` | [`Enum/String`](./Enums.md#enum-healthmultiplier) | `.5, 1.5, .8` |  |
| `EliteFlatTint` | [`Array`](./Arrays.md#array-eliteflattint) | `[ 1.1 1.1 1.3 ], [ 1.1 1.1 1.1 ], [ 1.1 1.1 1 ]` |  |
| `NonStackingShield` | Number | `7, 5, 3` |  |
| `SizeScale` | Number | `1.2, .8, .75` |  |
| `StatusEachRoundBegin` | [`Block`](./Elite_Buffs.md#context-statuseachroundbegin) | `{ ... }` |  |
| `DepressionAura` | [`Block`](./Elite_Buffs.md#context-depressionaura) | `{ ... }` |  |
| `DodgeChance` | Number | `10%` |  |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Creep, Fire` |  |
| `MeleeRevengeDamage` | [`Block`](./Elite_Buffs.md#context-meleerevengedamage) | `{ ... }` |  |
| `TileTrail` | [`Enum/String`](./Enums.md#enum-tiletrail) | `FireTile, CreepTile` |  |
| `AddCorpseHealth` | Number | `-999999, 2` |  |
| `Brace` | Number | `2, 1` |  |
| `ChanceToRevive` | [`Block`](./Elite_Buffs.md#context-chancetorevive) | `{ ... }` |  |
| `CritChanceUp` | Number | `10` |  |
| `DamageNeighborsAfterMove` | [`Block`](./Elite_Buffs.md#context-damageneighborsaftermove) | `{ ... }` |  |
| `DamageUp` | Number | `2` |  |
| `ExtraDispersedTurns` | Number | `1, -1` |  |
| `GlobalManaBurnAura` | Number | `-1` |  |
| `InnateElement` | [`Enum/String`](./Enums.md#enum-innateelement) | `Fire` |  |
| `KineticSpikes` | Number | `1` |  |
| `LuckUp` | Number | `3` |  |
| `MinimumKnockbackFromAllDamage` | Number | `1` |  |
| `NonStackingDivineShield` | Number | `1` |  |
| `RevengeDamage` | [`Block`](./Elite_Buffs.md#context-revengedamage) | `{ ... }` |  |
| `SpawnOnBattleStart` | [`Block`](./Elite_Buffs.md#context-spawnonbattlestart) | `{ ... }` |  |
| `SpeedUp` | Number | `4` |  |
| `StatusEachTurnEnd` | [`Block`](./Elite_Buffs.md#context-statuseachturnend) | `{ ... }` |  |
| `StunImmunity` | Number | `1` |  |
| `Thorns` | Number | `2, 1` |  |
| `AbilityDamageMultiplier` | Number | `1.5` |  |
| `AddStatusToBasicAttack` | [`Block`](./Elite_Buffs.md#context-addstatustobasicattack) | `{ ... }` |  |
| `AddUnfilledMaxHealth` | Number | `20` |  |
| `HealthRegenUp` | Number | `3` |  |
| `MoveTowardsDamageSource` | [`Enum/String`](./Enums.md#enum-movetowardsdamagesource) | `MoveOne` |  |
| `PermanentMadness` | Number | `1` |  |
| `ReflectProjectiles` | [`Block`](./Elite_Buffs.md#context-reflectprojectiles) | `{ ... }` |  |
| `RemoveExtraDispersedTurn` | Number | `1` |  |
| `SpawnOnDeath` | [`Enum/String`](./Enums.md#enum-spawnondeath) | `NonChampionFlySwarm` |  |
| `StatusEachRoundEnd` | [`Block`](./Elite_Buffs.md#context-statuseachroundend) | `{ ... }` |  |
| `StatusOnDie` | [`Block`](./Elite_Buffs.md#context-statusondie) | `{ ... }` |  |
| `StatusOnEnemyCastSpell` | [`Block`](./Elite_Buffs.md#context-statusonenemycastspell) | `{ ... }` |  |
| `StatusOnKill` | [`Block`](./Elite_Buffs.md#context-statusonkill) | `{ ... }` |  |
| `Trample` | Number | `3` |  |

</details>

---

### Context: `DepressionAura`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `aura_effects_allies` | Boolean | `false` |  |
| `range` | Number | `1, global` |  |
| `stacks` | Number | `1` |  |

</details>

---

### Context: `DamageNeighborsAfterMove`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `1` |  |
| `effects` | [`Block`](./Elite_Buffs.md#context-effects) | `{ ... }` |  |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Electric ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` |  |

</details>

---

### Context: `StatusEachRoundBegin`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `NonStackingShield` | Number | `7, 5, 3` |  |

</details>

---

### Context: `ChanceToRevive`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `health` | Number | `50%` |  |
| `stacks` | Number | `100` |  |
| `statuses` | [`Block`](./Elite_Buffs.md#context-statuses) | `{ ... }` |  |

</details>

---

### Context: `effects`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`DamageNeighborsAfterMove`](./Elite_Buffs.md#context-damageneighborsaftermove), [`MeleeRevengeDamage`](./Elite_Buffs.md#context-meleerevengedamage), [`RevengeDamage`](./Elite_Buffs.md#context-revengedamage)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Tarred` | Number | `1` |  |
| `VisualFXTile` | [`Enum/String`](./Enums.md#enum-visualfxtile) | `WaterConduct` |  |
| `Burn` | Number | `1` |  |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | `1` |  |
| `effects` | [`Block`](./Elite_Buffs.md#context-effects) | `{ ... }` |  |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Fire ]` |  |

</details>

---

### Context: `SpawnOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `twin` |  |
| `prevent_chain_tag` | [`Enum/String`](./Enums.md#enum-prevent_chain_tag) | `eb_twin` |  |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `effects` | [`Block`](./Elite_Buffs.md#context-effects) | `{ ... }` |  |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `NonStackingDivineShield` | Number | `1` |  |

</details>

---

### Context: `StatusOnEnemyCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |  |
| `HealthGain` | Number | `1` |  |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |  |
| `HealthGain` | Number | `4` |  |

</details>

---

### Context: `statuses`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ChanceToRevive`](./Elite_Buffs.md#context-chancetorevive)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Zombie` | Number | `1` |  |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Poison` | Number | `1` |  |

</details>

---

### Context: `ReflectProjectiles`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `self_damage` | Number | `2` |  |

</details>

---

### Context: `StatusEachRoundEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddRandomEliteBuff` | Number | `1` |  |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `StackingSandstorm` | Number | `1` |  |

</details>

---

## Enemy AI

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `distance_to_ally` | Number | `1, 0, -1` |  |
| `distance_to_character` | Number | `1, 0, -1` |  |
| `distance_to_enemy` | Number | `1, 0, -1` |  |
| `face_closest_enemy` | Number | `0, 1` |  |
| `preferred_distance` | Number | `0, mov, mov+5` |  |
| `total_distance_moved` | Number | `-0.01, 0.01, -1` |  |
| `accurate_knockback` | Boolean | `false` |  |
| `buff_ally` | Number | `0, 1, 10` |  |
| `buff_enemy` | Number | `1, 0, -1` |  |
| `buff_self` | Number | `0, -1` |  |
| `consider_overkill` | Boolean | `false, true` |  |
| `consider_secondary_damage` | Boolean | `false, true` |  |
| `consider_total_damage` | Boolean | `false, true` |  |
| `damage_ally` | Number | `1, 0, -1` |  |
| `damage_ally_corpse` | Number | `1, 100, 0` |  |
| `damage_enemy` | Number | `0, 1, 100` |  |
| `damage_enemy_corpse` | Number | `1, 100, 0` |  |
| `damage_self` | Number | `-0.1, 0, -1` |  |
| `debuff_ally` | Number | `1, 0, -1` |  |
| `debuff_enemy` | Number | `0, 1, 100` |  |
| `debuff_self` | Number | `-0.1, 0, -1` |  |
| `heal_ally` | Number | `0, 1, 100` |  |
| `heal_enemy` | Number | `1, 0, -1` |  |
| `heal_self` | Number | `-100, 0, -1` |  |
| `kill_ally` | Number | `40, 0` |  |
| `kill_enemy` | [`Enum/String`](./Enums.md#enum-kill_enemy) | `.2, 50, 0` |  |
| `negative_weight_scale` | [`Enum/String`](./Enums.md#enum-negative_weight_scale) | `.99` |  |
| `revive_ally_corpse` | Number | `0, 1, 100` |  |
| `revive_enemy_corpse` | Number | `1, 0, -1` |  |
| `spawn_object` | Number | `0, 1` |  |
| `spawn_object_distance_to_ally` | [`Enum/String`](./Enums.md#enum-spawn_object_distance_to_ally) | `.0001, 0, -.01` |  |
| `spawn_object_distance_to_enemy` | Number | `1, 0, -.01` |  |
| `spend_mana_scale` | [`Enum/String`](./Enums.md#enum-spend_mana_scale) | `.99` |  |
| `flat_cast_bonus` | Number | `99999` |  |
| `randomness` | Number | `6, 50, 4` |  |
| `cap_distance_to_ally` | Number | `7, 2, 4` |  |
| `consider_aoe` | Boolean | `false, true` |  |
| `danger_avoidance` | Number | `1000, 20, .1` |  |
| `distance_to_aggro_target` | Number | `-10, -1` |  |
| `distance_to_corpse` | Number | `0, -100, -.1` |  |
| `simple` | Boolean | `true` |  |
| `cap_distance_to_enemy` | Number | `2, 5` |  |
| `distance_to_water` | [`Enum/String`](./Enums.md#enum-distance_to_water) | `-.0001, -1` |  |
| `face_aggro_target` | Number | `10, 1` |  |
| `spawn_object_preferred_distance` | Number | `5, 4` |  |
| `cap_distance_to_character` | Number | `2` |  |
| `cap_total_distance_moved` | Number | `1` |  |
| `consider_aggro_target_enemy` | Boolean | `true` |  |
| `count_nomove_in_eval` | Boolean | `false` |  |
| `distance_to_center` | Number | `-1` |  |
| `exclude_characters_tagged` | [`Enum/String`](./Enums.md#enum-exclude_characters_tagged) | `siren` |  |
| `face_camera` | Number | `1000` |  |
| `lava` | Number | `5` |  |
| `tall_grass` | Number | `5` |  |

</details>

---

## Events & Encounters

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_OPEN_ANSW", "EVENT_LEAVE_ANSW", "EVENT_PICK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex, none, lck` |  |
| `requirements` | [`Block`](./Events_and_Encounters.md#context-requirements) | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_twentyfive, choice_dex_alt, choice_leave` |  |
| `prompt` | String | `"EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2", "EVENT_BEGGAR_NOTENOUGHMONEY"` |  |
| `set_frame` | Number | `2, 5, 4` |  |
| `copy_results` | [`Enum/String`](./Enums.md#enum-copy_results) | `smash, examine` |  |
| `good` | [`Block`](./Events_and_Encounters.md#context-good) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `get_item_from_pool` | [`Enum/String`](./Enums.md#enum-get_item_from_pool) | `food, chapter_rare` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `bad` | [`Block`](./Events_and_Encounters.md#context-bad) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `reward` | [`Block`](./Events_and_Encounters.md#context-reward) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Reward' action. |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `stat_max` | Number | `10, 25, 15` |  |
| `stat_min` | Number | `10, 25, 15` |  |
| `weight` | [`Enum/String`](./Enums.md#enum-weight) | `.5, .25, 15` | Probability weight for this outcome. |
| `cha` | Number | `1` |  |
| `con` | Number | `1` |  |
| `int` | Number | `1` |  |
| `lck` | Number | `1` |  |
| `spd` | Number | `1` |  |
| `str` | Number | `1` |  |
| `add_weather` | [`Enum/String`](./Enums.md#enum-add_weather) | `SolarFlare` |  |
| `dex` | Number | `1` |  |
| `gain_familiar` | [`Enum/String`](./Enums.md#enum-gain_familiar) | `Toad` | Event Action: Adds a specific familiar to the party. |
| `next_event_bonus` | Number | `2` |  |
| `requires_flag` | [`Enum/String`](./Enums.md#enum-requires_flag) | `SolarFlareUnlocked` | Prerequisite: Must meet this condition. |
| `self_status_next_fight` | [`Block`](./Events_and_Encounters.md#context-self_status_next_fight) | `{ ... }` | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |

</details>

---

### Context: `rare`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`attack`](./Events_and_Encounters.md#context-attack), [`good`](./Events_and_Encounters.md#context-good), [`loot`](./Events_and_Encounters.md#context-loot), [`main`](./Events_and_Encounters.md#context-main), [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prompt` | String | `"EVENT_CLOSEDWINDOW_REW2", "EVENT_CLOSEDWINDOW_REW6", "EVENT_CLOSEDWINDOW_REW4"` |  |
| `set_frame` | Number | `4, 6, 3` |  |
| `get_item_from_pool` | [`Block`](./Events_and_Encounters.md#context-get_item_from_pool) | `{ ... }, treasure_easy, bone_equipment` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `gain_disorder` | [`Enum/String`](./Enums.md#enum-gain_disorder) | `Dyslexia, BorrowedTime, Brave` |  |
| `gain_disorder_from_pool` | [`Enum/String`](./Enums.md#enum-gain_disorder_from_pool) | `diseases, all_disorders, physical_disorders` |  |
| `injury` | [`Enum/String`](./Enums.md#enum-injury) | `radiated, str, cursed` |  |
| `get_item` | [`Enum/String`](./Enums.md#enum-get_item) | `MomsKnife, BigToe, MomsToeNail` |  |
| `random_mutation` | [`Block`](./Events_and_Encounters.md#context-random_mutation) | `{ ... }, 2, 1` | Event Reward: Applies a completely random mutation to a character. |
| `event_now_same_cat` | [`Enum/String`](./Enums.md#enum-event_now_same_cat) | `BigToe, CatHole, SpookieApparation` |  |
| `get_parasite` | [`Enum/String`](./Enums.md#enum-get_parasite) | `FaceShards, BigToeCursed, MetalRod` |  |
| `gain_familiar` | [`Enum/String`](./Enums.md#enum-gain_familiar) | `CharmedLeaper, CharmedFetus2, CharmedHeadTumor` | Event Action: Adds a specific familiar to the party. |
| `random_pool` | [`Array`](./Arrays.md#array-random_pool) | `[ { event_now_same_cat Crate } { event_now_same_cat Safe ..., [ { permanent_stats { str -1 } } { permanent_stats { dex ..., [ { party_heal 100% gain_food [ 10 25 ]` |  |
| `get_parasite_from_pool` | [`Enum/String`](./Enums.md#enum-get_parasite_from_pool) | `sludge_armor, parasites, good_parasites` |  |
| `set_adventure_token` | [`Enum/String`](./Enums.md#enum-set_adventure_token) | `AdventureToken_TrippedOnBigToe, MysteriousStranger_HasLostFinger, HasPlayedMysteriousStranger` |  |
| `damage` | Number | `6, 10, 99%` | Event Node: Story branch or dialog option representing the 'Damage' action. |
| `gain_coins` | [`Array`](./Arrays.md#array-gain_coins) | `[ 20 100 ], [ 10 15 ], [ 10 30 ]` |  |
| `next_event_bonus` | Number | `-2, 1, -1` |  |
| `self_damage` | Number | `50%, 1, 99%` | Recoil or self-inflicted damage/effects applied to the caster. |
| `play_animation` | [`Array`](./Arrays.md#array-play_animation) | `resultHole, [ resultLeave 0 ]` |  |
| `learn_passive` | [`Enum/String`](./Enums.md#enum-learn_passive) | `DeathProof, PoisonTips, CobraStyle` |  |
| `party_damage` | [`Array`](./Arrays.md#array-party_damage) | `[ 5 10 ], 2, 5` |  |
| `party_heal` | Number | `6, 100%, 5` |  |
| `battle` | [`Equation`](./Enums.md#enum-mathequation) | `"events/chupacabra.lvl", "events/bigtoe.lvl", "events/crackinthewall.lvl"` |  |
| `increment_legacy_counter` | [`Enum/String`](./Enums.md#enum-increment_legacy_counter) | `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_ToiletFlushes, WorldEventLegacyCounter_CrackInTheWall` |  |
| `override_end_option_prompt` | String | `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_LOCKEDDOOR_PROMPT2", "EVENT_MYSTERIOUSTENT_PROMPT"` |  |
| `party_random_mutation` | Number | `1` |  |
| `ambush_next_basic_fights` | Number | `1` |  |
| `lose_item` | [`Enum/String`](./Enums.md#enum-lose_item) | `inventory, equipped` |  |
| `set_legacy_token` | [`Enum/String`](./Enums.md#enum-set_legacy_token) | `WorldEventLegacyToken_HeadInTireCompleted, WorldEventLegacyToken_MomsKnife, WorldEventLegacyToken_MonkeyPaw1` |  |
| `gain_food` | [`Array`](./Arrays.md#array-gain_food) | `[ 2 5 ], [ 1 5 ], [ 8 10 ]` |  |
| `hide_appearance_changes` | Number | `1` |  |
| `shop_now` | [`Enum/String`](./Enums.md#enum-shop_now) | `Event_SmallShop, Event_RareShop, TreasureHard` |  |
| `ally_ambush_next_fights` | Number | `2, 1` |  |
| `decrement_legacy_counter` | [`Enum/String`](./Enums.md#enum-decrement_legacy_counter) | `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall` |  |
| `add_weather` | [`Enum/String`](./Enums.md#enum-add_weather) | `HauntedNight, RestlessDead` |  |
| `full_heal` | Number | `1` |  |
| `learn_ability` | [`Enum/String`](./Enums.md#enum-learn_ability) | `FutureSight, BarfBall` |  |
| `gain_cat_familiar` | Number | `1` |  |
| `kill` | [`Enum/String`](./Enums.md#enum-kill) | `cat` |  |
| `level_up` | [`Enum/String`](./Enums.md#enum-level_up) | `self` |  |
| `lose_item_from_inventory` | [`Enum/String`](./Enums.md#enum-lose_item_from_inventory) | `cat` |  |
| `make_old` | [`Enum/String`](./Enums.md#enum-make_old) | `self` |  |
| `next_event_from_set` | [`Block`](./Events_and_Encounters.md#context-next_event_from_set) | `{ ... }, WatchingHead2` | Event Action: Chains immediately into a randomly selected subsequent story event. |
| `spawn_reflection_next_fight` | Block | `{ ... }, 1` | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. |
| `event_now` | [`Enum/String`](./Enums.md#enum-event_now) | `MysteriousMachine_Good, MysteriousMachine_Bad` |  |
| `lose_specific_item` | [`Enum/String`](./Enums.md#enum-lose_specific_item) | `SlagTight` |  |
| `party_heal_disorder` | Number | `2` |  |
| `party_heal_injury` | Number | `99` |  |
| `set_age` | Number | `1` |  |
| `upgrade_ability` | [`Enum/String`](./Enums.md#enum-upgrade_ability) | `random` |  |
| `upgrade_passive` | [`Enum/String`](./Enums.md#enum-upgrade_passive) | `random` |  |
| `ambush` | [`Equation`](./Enums.md#enum-mathequation) | `"events/chupacabra.lvl"` |  |
| `clear_result_animation` | Number | `1` |  |
| `gain_immortal_familiar` | [`Enum/String`](./Enums.md#enum-gain_immortal_familiar) | `CharmedFleaSpecial` |  |
| `get_and_equip_item` | [`Enum/String`](./Enums.md#enum-get_and_equip_item) | `FlyLarva` |  |
| `heal_disorder` | Number | `2` |  |
| `learn_ability_from_pool` | [`Enum/String`](./Enums.md#enum-learn_ability_from_pool) | `Necromancer` |  |
| `learn_passive_from_pool` | [`Enum/String`](./Enums.md#enum-learn_passive_from_pool) | `AnyUnlocked` |  |
| `lose_all_equipped_items` | [`Enum/String`](./Enums.md#enum-lose_all_equipped_items) | `cat` |  |
| `party_injury` | [`Enum/String`](./Enums.md#enum-party_injury) | `random` |  |
| `play_result_animation` | [`Enum/String`](./Enums.md#enum-play_result_animation) | `resultVeryGood` |  |
| `scramble_abilities` | [`Enum/String`](./Enums.md#enum-scramble_abilities) | `all` |  |
| `scramble_basic_attack` | [`Enum/String`](./Enums.md#enum-scramble_basic_attack) | `all` |  |
| `trigger_adventure_unlock` | [`Enum/String`](./Enums.md#enum-trigger_adventure_unlock) | `legacy_event_unlock_momsknife` |  |

</details>

---

### Context: `common`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prompt` | String | `"EVENT_CLOSEDWINDOW_REW5", "EVENT_CLOSEDWINDOW_REW1", "EVENT_CLOSEDWINDOW_REW3"` |  |
| `set_frame` | Number | `2, 5, 3` |  |
| `get_item_from_pool` | [`Enum/String`](./Enums.md#enum-get_item_from_pool) | `consumables, { ... }, [ CarvingKnife RazorBlade ButterflyKnife ]` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `random_pool` | [`Array`](./Arrays.md#array-random_pool) | `[ { prompt "EVENT_KNIFEINTHEWALL_REW1" } { prompt "EVENT_..., [ { permanent_stats { str -1 } } { permanent_stats { dex ..., [ { party_heal 5 gain_food [ 2 4 ]` |  |
| `damage` | [`Array`](./Arrays.md#array-damage) | `[ 5 10 ], 5, [ 3 6 ]` | Event Node: Story branch or dialog option representing the 'Damage' action. |
| `gain_coins` | [`Array`](./Arrays.md#array-gain_coins) | `[ 5 15 ], 5, [ 4 8 ]` |  |
| `injury` | [`Enum/String`](./Enums.md#enum-injury) | `spd, radiated, str` |  |
| `self_damage` | Number | `50%, 1, 99%` | Recoil or self-inflicted damage/effects applied to the caster. |
| `random_mutation` | [`Block`](./Events_and_Encounters.md#context-random_mutation) | `{ ... }, 2, 1` | Event Reward: Applies a completely random mutation to a character. |
| `clear_adventure_token` | [`Enum/String`](./Enums.md#enum-clear_adventure_token) | `AdventureToken_RedNeedle, AdventureToken_HasTakenNeedle, AdventureToken_BlueNeedle` |  |
| `gain_disorder_from_pool` | [`Enum/String`](./Enums.md#enum-gain_disorder_from_pool) | `mental_disorders, all_disorders, physical_disorders` |  |
| `play_animation` | [`Enum/String`](./Enums.md#enum-play_animation) | `resultLeave, resultConfused, [ resultLeave 0 ]` |  |
| `event_now_same_cat` | [`Enum/String`](./Enums.md#enum-event_now_same_cat) | `UnmarkedGrave, ElephantsFootCloser, random` |  |
| `gain_food` | Number | `-5, [ 1 4 ], [ 5 10 ]` |  |
| `gain_familiar` | [`Enum/String`](./Enums.md#enum-gain_familiar) | `CharmedFetus, CharmedPinky, Snake` | Event Action: Adds a specific familiar to the party. |
| `party_damage` | [`Array`](./Arrays.md#array-party_damage) | `[ 1 6 ], 5, 3` |  |
| `party_heal` | Number | `1, 100%, 3` |  |
| `get_item` | [`Enum/String`](./Enums.md#enum-get_item) | `EnchantingPoop, SeedBombs, CatnipBig` |  |
| `heal` | Number | `10, 1, 3` |  |
| `gain_disorder` | [`Enum/String`](./Enums.md#enum-gain_disorder) | `IntestinalProlapse, Scatological, Stinky` |  |
| `get_parasite_from_pool` | [`Enum/String`](./Enums.md#enum-get_parasite_from_pool) | `parasites, [ AmoebaHat AmoebaNeck AmoebaFace ], [ CrimsonMask_Cursed RedCap_Cursed PoundOfFlesh_Cursed ]` |  |
| `override_end_option_prompt` | String | `"EVENT_MYSTERIOUSTENT_PROMPT", "EVENT_MYSTERIOUSSTRANGER_END_AGAIN", "EVENT_LOCKEDDOOR_PROMPT1"` |  |
| `ally_ambush_next_fights` | Number | `2, 1` |  |
| `full_heal` | Number | `1` |  |
| `ambush_next_basic_fights` | Number | `1` |  |
| `set_adventure_token` | [`Enum/String`](./Enums.md#enum-set_adventure_token) | `MysteriousStranger_HasLostFinger, AdventureToken_UnmarkedGraveForced, HasPlayedMysteriousStranger` |  |
| `get_parasite` | [`Enum/String`](./Enums.md#enum-get_parasite) | `CursedHairball, PawShards, EnchantingPoop_Cursed` |  |
| `next_event_bonus` | Number | `2, 1, -1` |  |
| `increment_legacy_counter` | [`Enum/String`](./Enums.md#enum-increment_legacy_counter) | `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall, WorldEventLegacyCounter_VolcanoSacrifices` |  |
| `kill` | [`Enum/String`](./Enums.md#enum-kill) | `cat` |  |
| `lose_item` | [`Enum/String`](./Enums.md#enum-lose_item) | `inventory, weapon, equipped` |  |
| `shop_now` | [`Enum/String`](./Enums.md#enum-shop_now) | `Event_SmallShop, TreasureEasy` |  |
| `add_weather` | [`Enum/String`](./Enums.md#enum-add_weather) | `RestlessDead, Sandstorm` |  |
| `event_now` | [`Enum/String`](./Enums.md#enum-event_now) | `random` |  |
| `lose_specific_item` | [`Enum/String`](./Enums.md#enum-lose_specific_item) | `SlagTight` |  |
| `party_heal_disorder` | Number | `2` |  |
| `spin` | [`Enum/String`](./Enums.md#enum-spin) | `again` |  |
| `clear_result_animation` | Number | `1` |  |
| `decrement_legacy_counter` | [`Enum/String`](./Enums.md#enum-decrement_legacy_counter) | `WorldEventLegacyCounter_CrackInTheWall` |  |
| `get_and_equip_item` | [`Enum/String`](./Enums.md#enum-get_and_equip_item) | `Catnip` |  |
| `heal_disorder` | Number | `1` |  |
| `heal_injury` | Number | `1` |  |
| `learn_ability_from_pool` | [`Enum/String`](./Enums.md#enum-learn_ability_from_pool) | `AnyUnlocked` |  |
| `self_heal` | Number | `10` |  |
| `set_legacy_token` | [`Enum/String`](./Enums.md#enum-set_legacy_token) | `WorldEventLegacyToken_HasRunFromDeath` |  |
| `upgrade_ability` | [`Enum/String`](./Enums.md#enum-upgrade_ability) | `random` |  |

</details>

---

### Context: `good`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `reward` | [`Block`](./Events_and_Encounters.md#context-reward) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Reward' action. |
| `set_frame` | Number | `4, 2, 3` |  |
| `prompt` | String | `"EVENT_CLOSEDWINDOW_REW8", "EVENT_TRASHBIN_REW1", "EVENT_SEALEDCRYPT_LEAVE"` |  |
| `play_animation` | [`Enum/String`](./Enums.md#enum-play_animation) | `resultHole, resultVeryGood, [ resultLeave 0 ]` |  |
| `increment_legacy_counter` | [`Enum/String`](./Enums.md#enum-increment_legacy_counter) | `WorldEventLegacyCounter_TestLegacyFoo, WorldEventLegacyCounter_SealedCrypt, WorldEventLegacyCounter_Jack` |  |
| `conditional_reward` | [`Block`](./Events_and_Encounters.md#context-conditional_reward) | `{ ... }` | Event Action: Provides a reward only if a specific condition is met. |
| `set_legacy_token` | [`Enum/String`](./Enums.md#enum-set_legacy_token) | `WorldEventLegacyToken_StacyMutant, mapflag_ThrobbingArteryDone, MeatWorldQuest_Leech` |  |
| `cutscene` | [`Block`](./Events_and_Encounters.md#context-cutscene) | `{ ... }, "chapterintros/bunker"` | Event Node: Triggers a narrative cutscene. |
| `begin_chapter` | [`Enum/String`](./Enums.md#enum-begin_chapter) | `iceage.gon, future.gon, dimensionx.gon` |  |
| `complete_item_quest` | [`Enum/String`](./Enums.md#enum-complete_item_quest) | `PutridLeech, GuillotinasHead, ThrobbingGristle` |  |
| `random_mutation` | Number | `10, 1, 5` | Event Reward: Applies a completely random mutation to a character. |
| `set_adventure_token` | [`Enum/String`](./Enums.md#enum-set_adventure_token) | `StacyMutant_Thorns, StacyMutant_Holy, StacyMutant_Brace` |  |
| `event_now` | [`Enum/String`](./Enums.md#enum-event_now) | `StacyMutant3, StacyMutant4, StacyMutant2` |  |
| `event_now_same_cat` | [`Enum/String`](./Enums.md#enum-event_now_same_cat) | `MysteriousTomb1, BodyOfGlorg_Gift, random` |  |
| `gain_disorder` | [`Enum/String`](./Enums.md#enum-gain_disorder) | `Gargantuan, Anxiety, Depression` |  |
| `lose_specific_item` | [`Enum/String`](./Enums.md#enum-lose_specific_item) | `PutridLeech, PyrophinasCollar, ThrobbingGristle` |  |
| `trigger_adventure_unlock` | [`Enum/String`](./Enums.md#enum-trigger_adventure_unlock) | `legacy_event_unlock_momsknife, time_machine_quest_finalstep, meat_world_open` |  |
| `add_weather` | [`Enum/String`](./Enums.md#enum-add_weather) | `MeteorShower, SolarFlare, GeomagneticStorm` |  |
| `random_pool` | [`Array`](./Arrays.md#array-random_pool) | `[ { prompt "EVENT_TRAVERSETHENECROPOLIS_REW1" play_animat..., [ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 95 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran...` |  |
| `get_item` | [`Enum/String`](./Enums.md#enum-get_item) | `MomsKnife, HumanBrain, CryogenicTimeChamber_Full` |  |
| `get_item_from_pool` | [`Enum/String`](./Enums.md#enum-get_item_from_pool) | `godly_items, glitched_items, bloody_items` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `heal_disorder` | [`Enum/String`](./Enums.md#enum-heal_disorder) | `mental_disorders, 1, Anxiety` |  |
| `injury` | [`Enum/String`](./Enums.md#enum-injury) | `random` |  |
| `level_up` | [`Enum/String`](./Enums.md#enum-level_up) | `self, all` |  |
| `mutation` | [`Block`](./Events_and_Encounters.md#context-mutation) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Mutation' action. |
| `random_pool_consider_luck` | [`Array`](./Arrays.md#array-random_pool_consider_luck) | `[ { prompt "EVENT_VENDINGMACHINE_REW4" set_frame 5 gain_d..., [ { prompt "EVENT_TRACY_REW11" weight 1 get_item_from_poo..., [ { prompt "EVENT_TRACY_REW1" weight 1 get_parasite_from_...` |  |
| `rare` | [`Block`](./Events_and_Encounters.md#context-rare) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |
| `get_parasite` | [`Enum/String`](./Enums.md#enum-get_parasite) | `Beepis, Cunch, Feebis` |  |
| `heal_injury` | Number | `1, 5` |  |
| `kill` | [`Enum/String`](./Enums.md#enum-kill) | `cat` |  |
| `transform_item` | [`Array`](./Arrays.md#array-transform_item) | `[ JarOfRadiation JarOfRadiatedBlood ], [ JarOfRadiatedBlood JarOfChaos ], [ CryogenicTimeChamber_Empty CryogenicTimeChamber_Full ]` |  |
| `unlock_item_quest` | [`Enum/String`](./Enums.md#enum-unlock_item_quest) | `JarOfRadiatedBlood, JarOfChaos, CryogenicTimeChamber_Full` |  |
| `clear_surviving_kaiju` | [`Enum/String`](./Enums.md#enum-clear_surviving_kaiju) | `zaratana, pyrophina` |  |
| `cutscene_on_exit` | [`Enum/String`](./Enums.md#enum-cutscene_on_exit) | `king_intro` |  |
| `full_heal` | Number | `1` |  |
| `gain_disorder_from_pool` | [`Enum/String`](./Enums.md#enum-gain_disorder_from_pool) | `all_disorders` |  |
| `learn_ability_from_pool` | [`Enum/String`](./Enums.md#enum-learn_ability_from_pool) | `Necromancer, [ Smack Meow Hiss ]` |  |
| `learn_passive_from_pool` | [`Enum/String`](./Enums.md#enum-learn_passive_from_pool) | `Necromancer, [ MiniMe SkillShare ]` |  |
| `override_end_option_prompt` | String | `"EVENT_MYSTERIOUSTOMB_END", "EVENT_MYSTERIOUSTOMB1_END"` |  |
| `party_gain_disorder_from_pool` | [`Array`](./Arrays.md#array-party_gain_disorder_from_pool) | `[ Gigantism ], [ Dwarfism ]` |  |
| `ally_ambush_next_fights` | Number | `1` |  |
| `clone_self_to_party` | Number | `1` |  |
| `copy_items_to_party` | Number | `1` |  |
| `copy_party_items` | Number | `1` |  |
| `gain_food` | [`Array`](./Arrays.md#array-gain_food) | `[ 10 20 ]` |  |
| `get_full_item_set_from_pool` | [`Enum/String`](./Enums.md#enum-get_full_item_set_from_pool) | `common` |  |
| `global_effect_next_fight` | [`Block`](./Events_and_Encounters.md#context-global_effect_next_fight) | `{ ... }` | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. |
| `heal` | Number | `50%` |  |
| `lose_item` | [`Enum/String`](./Enums.md#enum-lose_item) | `parasite` |  |
| `next_event_bonus` | Number | `1` |  |
| `next_event_from_set` | [`Block`](./Events_and_Encounters.md#context-next_event_from_set) | `{ ... }` | Event Action: Chains immediately into a randomly selected subsequent story event. |
| `scramble_abilities` | [`Enum/String`](./Enums.md#enum-scramble_abilities) | `all` |  |
| `scramble_passives` | [`Enum/String`](./Enums.md#enum-scramble_passives) | `all` |  |
| `shop_now` | [`Enum/String`](./Enums.md#enum-shop_now) | `Event_SmallShop` |  |
| `trigger_butterfly_effect` | Number | `1` |  |
| `upgrade_ability` | [`Enum/String`](./Enums.md#enum-upgrade_ability) | `random` |  |
| `upgrade_passive` | [`Enum/String`](./Enums.md#enum-upgrade_passive) | `random` |  |

</details>

---

### Context: `intro`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cat_choice` | [`Enum/String`](./Enums.md#enum-cat_choice) | `random` |  |
| `event_clip` | [`Enum/String`](./Enums.md#enum-event_clip) | `NonWheelEvent` |  |
| `subject_clip` | [`Enum/String`](./Enums.md#enum-subject_clip) | `EventSubject` |  |
| `subject_frame` | [`Enum/String`](./Enums.md#enum-subject_frame) | `trashcan, brokenwindow, mouse_nest` |  |
| `title` | String | `"EVENT_MOUSENEST_NAME", "EVENT_TRASHBIN_NAME", "EVENT_CLOSEDWINDOW_NAME"` |  |
| `choose_cat_with_item` | [`Enum/String`](./Enums.md#enum-choose_cat_with_item) | `PutridLeech, GuillotinasHead, ThrobbingGristle` |  |
| `different_from_last_x_cats` | Number | `2, 1, 3` |  |
| `subject_frame_inner` | Number | `2, 4` |  |
| `choose_cat_with_highest_stat` | [`Enum/String`](./Enums.md#enum-choose_cat_with_highest_stat) | `int` |  |
| `choose_cat_with_item_slot_equipped` | [`Enum/String`](./Enums.md#enum-choose_cat_with_item_slot_equipped) | `weapon` |  |
| `choose_cat_with_min_health` | Number | `75%` |  |
| `choose_cat_with_most_injuries` | Boolean | `true` |  |
| `choose_cat_with_parasite` | Boolean | `true` |  |
| `set_frame` | Number | `1` |  |

</details>

---

### Context: `bad`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`main`](./Events_and_Encounters.md#context-main), [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `reward` | [`Block`](./Events_and_Encounters.md#context-reward) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Reward' action. |
| `set_frame` | Number | `2, 3, 4` |  |
| `prompt` | String | `"QEVENT_STACYMUTANT1_REW4_B", "EVENT_CLOSEDWINDOW_REW7", "QEVENT_STACYMUTANT1_REW4"` |  |
| `play_animation` | [`Enum/String`](./Enums.md#enum-play_animation) | `resultHole, resultVeryBad, [ resultLeave 0 ]` |  |
| `injury` | [`Enum/String`](./Enums.md#enum-injury) | `dex, str, con` |  |
| `battle` | [`Equation`](./Enums.md#enum-mathequation) | `"events/Death.lvl"` |  |
| `gain_disorder_from_pool` | [`Enum/String`](./Enums.md#enum-gain_disorder_from_pool) | `diseases, all_disorders` |  |
| `kill` | [`Enum/String`](./Enums.md#enum-kill) | `cat` |  |
| `cutscene` | [`Block`](./Events_and_Encounters.md#context-cutscene) | `{ ... }` | Event Node: Triggers a narrative cutscene. |
| `event_now` | [`Enum/String`](./Enums.md#enum-event_now) | `StacyMutant3, StacyMutant4, StacyMutant2` |  |
| `event_now_same_cat` | [`Enum/String`](./Enums.md#enum-event_now_same_cat) | `StevenFetus, random` |  |
| `get_parasite_from_pool` | [`Enum/String`](./Enums.md#enum-get_parasite_from_pool) | `parasites` |  |
| `next_event_bonus` | Number | `-1` |  |
| `gain_immortal_familiar` | [`Enum/String`](./Enums.md#enum-gain_immortal_familiar) | `CharmedFlea` |  |
| `get_parasite` | [`Enum/String`](./Enums.md#enum-get_parasite) | `CursedRock` |  |
| `lose_item` | [`Enum/String`](./Enums.md#enum-lose_item) | `parasite` |  |
| `select_item_from_pool_for_cutscene_only` | [`Enum/String`](./Enums.md#enum-select_item_from_pool_for_cutscene_only) | `glitched_items` |  |
| `set_legacy_token` | [`Enum/String`](./Enums.md#enum-set_legacy_token) | `WorldEventLegacyToken_StacyMutant` |  |

</details>

---

### Context: `requirements`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `has_token` | [`Enum/String`](./Enums.md#enum-has_token) | `WorldEventLegacyToken_StacyMutant, AdventureToken_TrippedOnBigToe, HasPlayedMysteriousStranger` |  |
| `counter_range` | [`Array`](./Arrays.md#array-counter_range) | `[ WorldEventLegacyCounter_SealedCrypt 1 1 ], [ WorldEventLegacyCounter_SealedCrypt 2 2 ], [ WorldEventLegacyCounter_SealedCrypt 0 0 ]` |  |
| `not_has_token` | [`Enum/String`](./Enums.md#enum-not_has_token) | `AdventureToken_UnmarkedGraveForced, WorldEventLegacyToken_MomsKnife, WorldEventLegacyToken_CryptOpened` |  |
| `counter_minimum` | [`Array`](./Arrays.md#array-counter_minimum) | `[ WorldEventLegacyCounter_CrackInTheWall 4 ], [ WorldEventLegacyCounter_TestLegacyFoo 3 ], [ WorldEventLegacyToken_StartDigging 4 ]` |  |
| `cat_has_item_equipped` | [`Enum/String`](./Enums.md#enum-cat_has_item_equipped) | `PutridLeech, GuillotinasHead, ThrobbingGristle` |  |
| `counter_maximum` | [`Array`](./Arrays.md#array-counter_maximum) | `[ WorldEventLegacyCounter_SealedCrypt 4 ], [ WorldEventLegacyCounter_CrackInTheWall 0 ], [ WorldEventLegacyCounter_CrackInTheWall 3 ]` |  |
| `is_not_chapter` | [`Array`](./Arrays.md#array-is_not_chapter) | `[ future theend ], [ jurassic iceage ], [ iceage jurassic ]` |  |
| `is_chapter` | [`Array`](./Arrays.md#array-is_chapter) | `[ future theend ], [ future ], [ theend ]` |  |
| `minimum_party_size` | Number | `2` |  |
| `not_cat_has_item_equipped` | [`Enum/String`](./Enums.md#enum-not_cat_has_item_equipped) | `GuillotinasHead, CryogenicTimeChamber_Full` |  |
| `not_on_quest` | Number | `1` |  |
| `cat_has_injury_count_min` | Number | `2` |  |
| `cat_has_item_slot_equipped` | [`Enum/String`](./Enums.md#enum-cat_has_item_slot_equipped) | `weapon` |  |
| `cat_has_parasite` | Boolean | `true` |  |

</details>

---

### Context: `main`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prompt` | String | `"EVENT_MOUSENEST_QUES", "EVENT_CLOSEDWINDOW_QUES", "EVENT_TRASHBIN_QUES"` |  |
| `bad` | [`Block`](./Events_and_Encounters.md#context-bad) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `goto` | [`Enum/String`](./Enums.md#enum-goto) | `end` |  |
| `max_options` | Number | `2, 3` |  |
| `set_frame` | Number | `16, 3, 15` |  |
| `shuffle_options` | Boolean | `true` |  |
| `weight` | [`Enum/String`](./Enums.md#enum-weight) | `.5, .25` | Probability weight for this outcome. |
| `add_weather` | [`Enum/String`](./Enums.md#enum-add_weather) | `MeteorShower` |  |
| `gain_familiar` | [`Enum/String`](./Enums.md#enum-gain_familiar) | `Snake` | Event Action: Adds a specific familiar to the party. |
| `leave` | [`Block`](./Events_and_Encounters.md#context-leave) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Leave' action. |
| `next_event_from_set` | [`Enum/String`](./Enums.md#enum-next_event_from_set) | `Tragedy` | Event Action: Chains immediately into a randomly selected subsequent story event. |
| `party_heal` | Number | `3` |  |
| `party_permanent_stats` | [`Block`](./Events_and_Encounters.md#context-party_permanent_stats) | `{ ... }` | Event Reward: Permanently increases (or decreases) the core stats of all party members. |
| `play_animation` | [`Array`](./Arrays.md#array-play_animation) | `resultVeryGood` |  |
| `rare` | [`Block`](./Events_and_Encounters.md#context-rare) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |
| `requires_flag` | [`Enum/String`](./Enums.md#enum-requires_flag) | `MeteorShowerUnlocked` | Prerequisite: Must meet this condition. |
| `self_damage` | [`Array`](./Arrays.md#array-self_damage) | `[ 4 8 ]` | Recoil or self-inflicted damage/effects applied to the caster. |
| `self_status_next_fight` | [`Block`](./Events_and_Encounters.md#context-self_status_next_fight) | `{ ... }` | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |
| `shop_now` | [`Enum/String`](./Enums.md#enum-shop_now) | `Event_RareShop` |  |

</details>

---

### Context: `reward`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`bad`](./Events_and_Encounters.md#context-bad), [`good`](./Events_and_Encounters.md#context-good)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prompt` | String | `"EVENT_SEALEDCRYPT_QUES2", "EVENT_SEALEDCRYPT_QUES1", "EVENT_TRASHBIN_REW2"` |  |
| `set_frame` | Number | `2, 1, 3` |  |
| `clear_adventure_token` | [`Enum/String`](./Enums.md#enum-clear_adventure_token) | `AdventureToken_RedNeedle, AdventureToken_HasTakenNeedle, AdventureToken_BlueNeedle` |  |
| `get_item_from_pool` | [`Block`](./Events_and_Encounters.md#context-get_item_from_pool) | `{ ... }, consumables, food` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `set_adventure_token` | [`Enum/String`](./Enums.md#enum-set_adventure_token) | `AdventureToken_StevenTryAgain3, AdventureToken_Mirage2, HasPlayedMysteriousStranger` |  |
| `set_subject` | [`Enum/String`](./Enums.md#enum-set_subject) | `throbbing_artery_noflesh, wall_of_flesh_noartery, dimensionx_head2` |  |
| `random_pool` | [`Array`](./Arrays.md#array-random_pool) | `[ { weight 10 gain_disorder_from_pool diseases } { weight..., [ { get_item_from_pool rare get_item_from_pool rare } { g..., [ { get_item_from_pool uncommon get_item_from_pool uncomm...` |  |
| `next_event_bonus` | Number | `-2, 1, -1` |  |
| `trigger_adventure_unlock` | [`Enum/String`](./Enums.md#enum-trigger_adventure_unlock) | `meat_world_unlock, end_of_time_unlock` |  |
| `play_animation` | [`Array`](./Arrays.md#array-play_animation) | `resultVeryGood, resultBad` |  |
| `cutscene_on_exit` | [`Enum/String`](./Enums.md#enum-cutscene_on_exit) | `infinite_intro` |  |
| `gain_disorder_from_pool` | [`Enum/String`](./Enums.md#enum-gain_disorder_from_pool) | `diseases, Steven_disorders` |  |
| `injury` | [`Enum/String`](./Enums.md#enum-injury) | `con, random` |  |
| `spawn_unit_next_fight` | [`Block`](./Events_and_Encounters.md#context-spawn_unit_next_fight) | `{ ... }` | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. |
| `event_now` | [`Enum/String`](./Enums.md#enum-event_now) | `MeatGolem` |  |
| `gain_coins` | [`Array`](./Arrays.md#array-gain_coins) | `[ 4 15 ]` |  |
| `get_item` | [`Enum/String`](./Enums.md#enum-get_item) | `BrokenWindow` |  |
| `get_parasite_from_pool` | [`Enum/String`](./Enums.md#enum-get_parasite_from_pool) | `parasites` |  |
| `party_damage` | [`Array`](./Arrays.md#array-party_damage) | `[ 5 10 ]` |  |
| `set_legacy_token` | [`Enum/String`](./Enums.md#enum-set_legacy_token) | `WorldEventLegacyToken_CryptOpened` |  |
| `weight` | Number | `3` | Probability weight for this outcome. |

</details>

---

### Context: `ignore`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_IGNORE_ANSW, "EVENT_LEAVE_ANSW", "EVENT_IGNORE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con, none` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |
| `hint_chapter_exit` | [`Enum/String`](./Enums.md#enum-hint_chapter_exit) | `home` |  |

</details>

---

### Context: `self_status_next_fight`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`main`](./Events_and_Encounters.md#context-main)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fear` | Number | `2, 1, 5` | Applies or references the 'Fear' effect/state. |
| `Poison` | Number | `10, 2, 3` | Applies or references the 'Poison' effect/state. |
| `Bleed` | Number | `2, 1, 3` | Applies or references the 'Bleed' effect/state. |
| `AbilityOnBattleStart_Immediate` | [`Enum/String`](./Enums.md#enum-abilityonbattlestart_immediate) | `SummonBrambles2, FlowerEventSleep, BrambleRandomTileEvent` | Applies or references the 'AbilityOnBattleStart_Immediate' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `SpeedUp` | Number | `2, -4, -2` | Applies or references the 'SpeedUp' effect/state. |
| `StrengthUp` | Number | `-2, 2, -1` | Applies or references the 'StrengthUp' effect/state. |
| `ConstitutionUp` | Number | `1, -1` | Applies or references the 'ConstitutionUp' effect/state. |
| `AddStartingMana` | Number | `5` | Applies or references the 'AddStartingMana' effect/state. |
| `Burn` | Number | `6, 5, 4` | Applies or references the 'Burn' effect/state. |
| `CharismaUp` | Number | `2, -2, -1` | Applies or references the 'CharismaUp' effect/state. |
| `Confusion` | Number | `2, 4` | Applies or references the 'Confusion' effect/state. |
| `HealthRegenUp` | Number | `2, 1` | Applies or references the 'HealthRegenUp' effect/state. |
| `Webbed` | Number | `2, 1` | Applies or references the 'Webbed' effect/state. |
| `Blind` | Number | `6, 4` | Applies or references the 'Blind' effect/state. |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `DexterityUp` | Number | `2, -1` | Applies or references the 'DexterityUp' effect/state. |
| `IntelligenceUp` | Number | `3, -3` | Applies or references the 'IntelligenceUp' effect/state. |
| `NoHealthRegen` | Number | `1` | Applies or references the 'NoHealthRegen' effect/state. |
| `Sleep` | Number | `2, 1` | Applies or references the 'Sleep' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `AbilityOnBattleStart` | [`Enum/String`](./Enums.md#enum-abilityonbattlestart) | `Flush` | Applies or references the 'AbilityOnBattleStart' effect/state. |
| `AddInitiative` | Number | `-99` | Applies or references the 'AddInitiative' effect/state. |
| `AlphaTurns` | Number | `1` | Applies or references the 'AlphaTurns' effect/state. |
| `ChangeTileUnderCharacterAtStart` | [`Enum/String`](./Enums.md#enum-changetileundercharacteratstart) | `GlassTile` | Applies or references the 'ChangeTileUnderCharacterAtStart' effect/state. |
| `DivineShield` | Number | `2` | Applies or references the 'DivineShield' effect/state. |
| `Fights` | Number | `99` | Applies or references the 'Fights' effect/state. |
| `LuckUp` | Number | `1` | Applies or references the 'LuckUp' effect/state. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `MissChance` | Number | `10` | Applies or references the 'MissChance' effect/state. |
| `NoManaRegen` | Number | `1` | Applies or references the 'NoManaRegen' effect/state. |
| `PermanentConfusion` | Number | `1` | Applies or references the 'PermanentConfusion' effect/state. |
| `ProbeCharmed` | Number | `1` | Applies or references the 'ProbeCharmed' effect/state. |
| `RandomStatUp` | Number | `1` | Applies or references the 'RandomStatUp' effect/state. |
| `Rot` | Number | `2` | Applies or references the 'Rot' effect/state. |
| `Slow` | Number | `3` | Applies or references the 'Slow' effect/state. |
| `SpiderInfested` | Number | `1` | Applies or references the 'SpiderInfested' effect/state. |
| `Tarred` | Number | `1` | Applies or references the 'Tarred' effect/state. |
| `TempStrengthUp` | Number | `1` | Applies or references the 'TempStrengthUp' effect/state. |

</details>

---

### Context: `permanent_stats`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2, 1, -1` |  |
| `random` | Number | `2, 1, -1` |  |
| `int` | Number | `-4, 1, -1` |  |
| `lck` | Number | `-2, 1, -1` |  |
| `spd` | Number | `-2, 1, -1` |  |
| `str` | Number | `2, 1, -1` |  |
| `cha` | [`Enum/String`](./Enums.md#enum-cha) | `+1, 1, -1` |  |
| `dex` | Number | `2, 1, -1` |  |

</details>

---

### Context: `spawn_unit_next_fight`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`reward`](./Events_and_Encounters.md#context-reward)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `RandomNonCoinPickup, DeadPinky, [ Junk Junk TrashBag ]` |  |
| `count` | Number | `8, 3, [ 3 6 ]` | Quantity. |
| `spawn_side` | [`Enum/String`](./Enums.md#enum-spawn_side) | `anywhere, cats, enemies` |  |
| `side` | [`Enum/String`](./Enums.md#enum-side) | `enemies` |  |

</details>

---

### Context: `examine`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_EXAMINE_ANSW", EVENT_EXAMINE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int, lck` |  |
| `copy_results` | [`Enum/String`](./Enums.md#enum-copy_results) | `smash, open` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `gain_coins` | [`Array`](./Arrays.md#array-gain_coins) | `[ 5 15 ]` |  |

</details>

---

### Context: `leave`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LEAVE_ANSW", "EVENT_WALKAWAY_ANSW", "EVENT_IGNORE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd, lck, none` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |

</details>

---

### Context: `mutation`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `eyes` | Number | `900, -2, 702` |  |
| `mouth` | Number | `900, -2, 705` |  |
| `ears` | Number | `310, -2, 328` |  |
| `eyebrows` | Number | `900, 440, -2` |  |
| `head` | Number | `900, 305` | Event Node: Story branch or dialog option representing the 'Head' action. |
| `legs` | Number | `900, 322` |  |
| `arms` | Number | `900` |  |
| `body` | Number | `900` | Event Node: Story branch or dialog option representing the 'Body' action. |
| `tail` | Number | `900` | Event Node: Story branch or dialog option representing the 'Tail' action. |
| `eye1` | Number | `-2, -1` |  |
| `arm1` | Number | `-2` |  |
| `ear1` | Number | `-2` |  |
| `eyebrow1` | Number | `-2` |  |
| `leg1` | Number | `-2` |  |
| `eye2` | Number | `-1` |  |

</details>

---

### Context: `loot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_dex_alt, choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_LOOT_ANSW, QEVENT_DEADKING_LOOTCORPSE_ANSW, "EVENT_LOOT_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex, lck` |  |
| `rare` | [`Block`](./Events_and_Encounters.md#context-rare) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |

</details>

---

### Context: `get_item_from_pool`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `chapter_common, chapter, chapter_rare` |  |
| `restrict` | [`Array`](./Arrays.md#array-restrict) | `consumables, [ weapon, trinket, armor ], trinket` |  |
| `prompt` | String | `"EVENT_FRANK2_REW4"` |  |

</details>

---

### Context: `random_mutation_from_set`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `mouth` | Number | `1500, 1026, -1` |  |
| `count` | Number | `1, 3` | Quantity. |
| `tail` | Number | `1500, 760, -1` | Event Node: Story branch or dialog option representing the 'Tail' action. |
| `ears` | Number | `1500, -2, -1` |  |
| `eyes` | Number | `-1, -2, 1029` |  |
| `legs` | Number | `306, -1` |  |
| `body` | Number | `758, -1` | Event Node: Story branch or dialog option representing the 'Body' action. |
| `eyebrows` | Number | `-2, -1` |  |
| `head` | Number | `759, -1` | Event Node: Story branch or dialog option representing the 'Head' action. |
| `arm1` | Number | `-2, -1` |  |
| `arm2` | Number | `-2, -1` |  |
| `leg1` | Number | `-1` |  |
| `leg2` | Number | `-1` |  |
| `texture` | Number | `-1` |  |

</details>

---

### Context: `else`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prompt` | String | `"EVENT_MIRAGE_REW4", "QEVENT_STACYMUTANT1_QUES1", "EVENT_MIRAGE_REW3"` |  |
| `event_now_same_cat` | [`Enum/String`](./Enums.md#enum-event_now_same_cat) | `Needles` |  |
| `set_adventure_token` | [`Enum/String`](./Enums.md#enum-set_adventure_token) | `AdventureToken_Mirage1` |  |
| `party_damage` | [`Array`](./Arrays.md#array-party_damage) | `[ 10 15 ], 1, 5` |  |
| `set_frame` | Number | `4, 3` |  |
| `event_now` | [`Enum/String`](./Enums.md#enum-event_now) | `Mirage` |  |
| `random_pool` | [`Array`](./Arrays.md#array-random_pool) | `[ { get_item FrozenHat get_item FrozenMask get_item Froze..., [ { get_item Catnip } { gain_food [ 2 5 ]` |  |
| `gain_disorder` | [`Enum/String`](./Enums.md#enum-gain_disorder) | `Soulless, AcidReflux` |  |
| `get_item_from_pool` | [`Array`](./Arrays.md#array-get_item_from_pool) | `[ LeafyMask LeafyHat LeafyNecklace DinoHat DinoMask DinoN...` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `damage` | Number | `50%` | Event Node: Story branch or dialog option representing the 'Damage' action. |
| `next_event_bonus` | Number | `1` |  |
| `set_legacy_token` | [`Enum/String`](./Enums.md#enum-set_legacy_token) | `WorldEventLegacyToken_HasRunFromDeath` |  |

</details>

---

### Context: `eat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_EAT_ANSW", "EVENT_DRINK_ANSW", EVENT_EAT_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `cutscene`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`good`](./Events_and_Encounters.md#context-good)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cutscene` | String | `"time_machine", "desert_intro", "chaos_ending_good"` | Event Node: Triggers a narrative cutscene. |
| `skip_result_screen` | Boolean | `true` |  |

</details>

---

### Context: `random_mutation`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `2, 1, 15` | Quantity. |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `melted, animal, birth_defect` | Specific entity tag required. |
| `asymmetric` | Boolean | `false, true` |  |

</details>

---

### Context: `smash`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_SMASH_ANSW", "EVENT_MYSTERIOUSTOMB_ANSW", "EVENT_GOLEMSMASH_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex, str, none` |  |
| `copy_results` | [`Enum/String`](./Enums.md#enum-copy_results) | `open` |  |

</details>

---

### Context: `destroy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DESTROY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `party_permanent_stats_exclude_self`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2, 1` |  |
| `con` | Number | `2, 1` |  |
| `dex` | Number | `2, 1` |  |
| `int` | Number | `2, 1` |  |
| `lck` | Number | `2, 1` |  |
| `spd` | Number | `2, 1` |  |
| `str` | Number | `2, 1` |  |

</details>

---

### Context: `bash`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BASH_ANSW", "EVENT_BASHOPEN_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `party_status_next_fight`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `Poison` | Number | `2, 1, 3` | Applies or references the 'Poison' effect/state. |
| `AbilityOnBattleStart_Immediate` | [`Enum/String`](./Enums.md#enum-abilityonbattlestart_immediate) | `RocksFallEvent, SummonBrambles2, GrassEvent` | Applies or references the 'AbilityOnBattleStart_Immediate' effect/state. |
| `NoHealthRegen` | Number | `1` | Applies or references the 'NoHealthRegen' effect/state. |
| `Bleed` | Number | `3` | Applies or references the 'Bleed' effect/state. |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `HealthRegenUp` | Number | `2` | Applies or references the 'HealthRegenUp' effect/state. |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |
| `Tangled` | Number | `2` | Applies a tangled/ensnared status effect, often modifying visual sprites. |
| `Tarred` | Number | `1` | Applies or references the 'Tarred' effect/state. |
| `Webbed` | Number | `1` | Applies or references the 'Webbed' effect/state. |

</details>

---

### Context: `sneak`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_SNEAKBY_ANSW, EVENT_RUN_ANSW, "EVENT_SNEAKBY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd, dex` |  |

</details>

---

### Context: `touch`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_OBELISK_MOON_TOUCH_ANSW, QEVENT_OBELISK_CORE_TOUCH_ANSW, "EVENT_MYSTERIOUSOBELISK_TOUCH_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha, none, lck` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |

</details>

---

### Context: `a`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"1", "class ability pool", "1 injury"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |

</details>

---

### Context: `b`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"5", "set ability pool", "many injuries"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |

</details>

---

### Context: `c`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"all (symmetric)", "class passive pool", "specific disorder"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |

</details>

---

### Context: `activate_p`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_OBELISK_MOON_ACTIVATE_ANSW, QEVENT_OBELISK_CORE_ACTIVATE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest, none` |  |

</details>

---

### Context: `activate_z`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_OBELISK_MOON_ACTIVATE_ANSW, QEVENT_OBELISK_CORE_ACTIVATE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest, none` |  |

</details>

---

### Context: `options`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | [`Block`](./Events_and_Encounters.md#context-bad) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `damage` | [`Block`](./Events_and_Encounters.md#context-damage) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Damage' action. |
| `rare` | [`Block`](./Events_and_Encounters.md#context-rare) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |
| `get_item_from_pool` | [`Enum/String`](./Enums.md#enum-get_item_from_pool) | `any_chapter, flesh_items` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `prompt` | String | `"EVENT_TRAVERSETHENECROPOLIS_REW6", "EVENT_TRACY_REW5"` |  |
| `gain_familiar` | [`Enum/String`](./Enums.md#enum-gain_familiar) | `Squirrel` | Event Action: Adds a specific familiar to the party. |
| `play_animation` | [`Enum/String`](./Enums.md#enum-play_animation) | `resultGood` |  |
| `weight` | [`Enum/String`](./Enums.md#enum-weight) | `.5` | Probability weight for this outcome. |

</details>

---

### Context: `d`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"all (asymmetric)", "pool disorder", "set passive pool"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |

</details>

---

### Context: `open`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_OPEN_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |
| `copy_results` | [`Enum/String`](./Enums.md#enum-copy_results) | `smash` |  |

</details>

---

### Context: `take`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_TAKE_ANSW", "EVENT_GOAROUND_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd, con, lck` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_dex_alt` |  |

</details>

---

### Context: `home`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `hint_chapter_exit` | [`Enum/String`](./Enums.md#enum-hint_chapter_exit) | `home` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_TIMEMACHINE_HOME_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `past`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `hint_chapter_exit` | [`Enum/String`](./Enums.md#enum-hint_chapter_exit) | `jurassic, iceage, endoftime` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_TIMEMACHINE_ICEAGE_PAST_ANSW, QEVENT_TIMEMACHINE_JURASSIC_INFINITE_ANSW, QEVENT_TIMEMACHINE_PAST_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `attack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BREAK_ANSW", "EVENT_BASH_ANSW", "EVENT_ATTACK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |
| `rare` | [`Block`](./Events_and_Encounters.md#context-rare) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |

</details>

---

### Context: `charm`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_CHARM_ANSW, "EVENT_CHARM_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `fight`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_FIGHT_ANSW, "EVENT_FIGHT_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `next_event_from_set`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `event` | [`Enum/String`](./Enums.md#enum-event) | `Tragedy, Death` |  |
| `same_cat` | Boolean | `true` |  |
| `count` | Number | `4, 1, 3` | Quantity. |

</details>

---

### Context: `enter`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_HOLEINTHEEARTH_ENTER_ANSW", QEVENT_DIMENSIONXPORTAL_ENTER_ANSW, "EVENT_ENTER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none, con, lck` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `hint_chapter_exit` | [`Enum/String`](./Enums.md#enum-hint_chapter_exit) | `dimensionx` |  |

</details>

---

### Context: `leave_party_temporarily`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `fights_skipped` | Number | `0, 1` |  |
| `return_as` | [`Enum/String`](./Enums.md#enum-return_as) | `enemy` |  |
| `return_during` | [`Enum/String`](./Enums.md#enum-return_during) | `boss` |  |

</details>

---

### Context: `lick`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LICK_ANSW", QEVENT_GLOWINGORB_LICK_ANSW, "EVENT_GOLEMLICK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha, con, none` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |

</details>

---

### Context: `bite`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_con` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_WALLOFFLESH_BITE2_ANSW, QEVENT_THROBBINGARTERY_BITE_ANSW, QEVENT_WALLOFFLESH_BITE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str, con` |  |

</details>

---

### Context: `inspect`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_INSPECT_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `skip`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW4", "QEVENT_STACYMUTANT1_ANSW4", "QEVENT_STACYMUTANT3_ANSW4"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `run`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_RUN_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |

</details>

---

### Context: `10coins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_ten` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `get_item_from_pool` | [`Enum/String`](./Enums.md#enum-get_item_from_pool) | `chapter_rare` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `label` | String | `"EVENT_BEGGAR_5_ANSW"` |  |
| `prompt` | String | `"EVENT_ABEGGAR_REW2"` |  |
| `set_frame` | Number | `2` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `10` |  |
| `stat_min` | Number | `10` |  |
| `weight` | Number | `10` | Probability weight for this outcome. |

</details>

---

### Context: `5coins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_one` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `get_item_from_pool` | [`Enum/String`](./Enums.md#enum-get_item_from_pool) | `chapter_rare` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `label` | String | `"EVENT_BEGGAR_5_ANSW"` |  |
| `prompt` | String | `"EVENT_ABEGGAR_REW2"` |  |
| `set_frame` | Number | `2` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `5` |  |
| `stat_min` | Number | `5` |  |
| `weight` | Number | `5` | Probability weight for this outcome. |

</details>

---

### Context: `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `robot, rat` | Specific entity tag required. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |

</details>

---

### Context: `damage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BAHPHOMET_HEALTH_ANSW", "EVENT_DAMAGE_ANSW", "QEVENT_STACYMUTANT3_ANSW2"` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `drink`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_DRINK_ANSW, "EVENT_DRINK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con, lck` |  |

</details>

---

### Context: `kiss`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_KISS_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `party_random_mutation_from_set`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `1` | Quantity. |
| `ears` | Number | `-2` |  |
| `eyebrows` | Number | `-2` |  |
| `eyes` | Number | `-2` |  |
| `mouth` | Number | `-2` |  |

</details>

---

### Context: `go_around`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GOAROUND_ANSW", "EVENT_TAKELONGWAY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd, none, lck` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |

</details>

---

### Context: `outcome`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `play_animation` | [`Array`](./Arrays.md#array-play_animation) | `[ resultTragedy .5 ], [ resultBlessing .5 ], [ resultWeather .5 ]` |  |
| `random_pool` | [`Array`](./Arrays.md#array-random_pool) | `[ { set_frame 12 prompt "EVENT_ACAT_REW1" gain_cat_famili..., [ { set_frame 1 prompt "EVENT_BLESSING_REW1" heal 5 } { s..., [ { set_frame 1 prompt "EVENT_TRAGEDY_REW1" } { set_frame...` |  |
| `add_weather` | [`Enum/String`](./Enums.md#enum-add_weather) | `Birdemic` |  |
| `weather_roll` | [`Array`](./Arrays.md#array-weather_roll) | `[ { weight 1 set_frame 2 prompt "EVENT_HAPPENING_FOG_REW"...` |  |

</details>

---

### Context: `buy1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_one` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `label` | String | `"EVENT_BUY_ANSW"` |  |
| `prompt` | String | `"EVENT_TRACY_REW4"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `1` |  |
| `stat_min` | Number | `1` |  |
| `weight` | Number | `1` | Probability weight for this outcome. |

</details>

---

### Context: `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `99, 2, 1` | Quantity. |
| `Fear` | Number | `2, 3` | Applies or references the 'Fear' effect/state. |
| `Bleed` | Number | `2` | Applies or references the 'Bleed' effect/state. |

</details>

---

### Context: `attach_antenna`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_GLOWINGORB_ANTENNA_ANSW, QEVENT_VOLCANO_ANTENNA_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `boogers`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_BEEPIS_ANSW", "EVENT_BOOGERS_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `donate_10`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_ten` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `label` | String | `"EVENT_DONATE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `10` |  |
| `stat_min` | Number | `10` |  |

</details>

---

### Context: `donate_15`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_ten` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `label` | String | `"EVENT_DONATE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `15` |  |
| `stat_min` | Number | `15` |  |

</details>

---

### Context: `donate_20`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_twentyfive` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `label` | String | `"EVENT_DONATE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `20` |  |
| `stat_min` | Number | `20` |  |

</details>

---

### Context: `donate_5`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_one` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `label` | String | `"EVENT_DONATE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `5` |  |
| `stat_min` | Number | `5` |  |

</details>

---

### Context: `global_effect_next_fight`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fights` | Number | `1, 3` | Applies or references the 'Fights' effect/state. |

</details>

---

### Context: `investigate`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_INVESTIGATE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `poop`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_FEEBIS_ANSW", "EVENT_POOP_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `protection`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_CUTS_ANSW", "EVENT_PROTECTION_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `put_in_coins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_ten` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `label` | String | `"EVENT_VENDINGMACHINE_COINS_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `10` |  |
| `stat_min` | Number | `10` |  |

</details>

---

### Context: `repell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSCAVE1_RAPPEL_ANSW", "EVENT_MYSTERIOUSCAVE1_TALKTO_ANSW", "EVENT_MYSTERIOUSCAVE3_CLIMB_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex, str, cha` |  |

</details>

---

### Context: `blue`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `copy_results` | [`Enum/String`](./Enums.md#enum-copy_results) | `red` |  |
| `fixed_chance` | Number | `50%` |  |
| `label` | String | `"EVENT_BLUE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `button`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `copy_results` | [`Enum/String`](./Enums.md#enum-copy_results) | `lever` |  |
| `fixed_chance` | Number | `50%` |  |
| `label` | String | `"EVENT_PUSHBUTTON_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `find_another_way`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_JAGEDPATHWAY_ANSW_AROUND", "EVENT_FINDANOTHERWAY_ANSW"` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `future`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `hint_chapter_exit` | [`Enum/String`](./Enums.md#enum-hint_chapter_exit) | `future` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_TIMEMACHINE_FUTURE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `infinite`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `hint_chapter_exit` | [`Enum/String`](./Enums.md#enum-hint_chapter_exit) | `endoftime` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_TIMEMACHINE_THEEND_INFINITE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `lever`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `fixed_chance` | Number | `50%` |  |
| `label` | String | `"EVENT_PULLLEVER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `move_closer`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_ELEPHANTSFOOTCLOSER_ANSW", "EVENT_ELEPHANTSFOOT_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `play`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSSTRANGER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |

</details>

---

### Context: `red`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `fixed_chance` | Number | `50%` |  |
| `label` | String | `"EVENT_RED_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `repair`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_REPAIR_ANSW", EVENT_REPAIR_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none, lck` |  |

</details>

---

### Context: `sacrifice`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BAHPHOMET_SACRIFICE_ANSW", "QEVENT_VOLCANO_SACRIFICE_ANSW"` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `traverse`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_TRAVERSETHENECROPOLIS_ANSW"` |  |
| `play_animation` | [`Enum/String`](./Enums.md#enum-play_animation) | `resultGood` |  |
| `prompt` | String | `"EVENT_TRAVERSETHENECROPOLIS_REW5"` |  |
| `shop_now` | [`Enum/String`](./Enums.md#enum-shop_now) | `TreasureHard` |  |

</details>

---

### Context: `turnon`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSMACHINE_TURNITON_ANSW", "EVENT_TURNONTV_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int, lck` |  |

</details>

---

### Context: `KillEnemyOfTypeAtBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `enemy_type` | [`Enum/String`](./Enums.md#enum-enemy_type) | `any, cat` |  |
| `fallback_spawn` | [`Array`](./Arrays.md#array-fallback_spawn) | `[ TomTom Kitten CatCaller Mangy ]` |  |

</details>

---

### Context: `attach_amplifier`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_THEHEAD_AMPLIFIER_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `attach_leech`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_THROBBINGARTERY_ATTACH_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `book`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_SOMEOLDBOOK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `brace`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT1_ANSW2"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `counter`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT4_ANSW2"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `donate`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"Donate"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `double`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT4_ANSW1"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `fill_jar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_THEHEAD_FILLJAR_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `fire`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW1"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `holy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT1_ANSW3"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `hp`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT3_ANSW1"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `ice`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW2"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `intimidation`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_INTIMIDATION_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `itchies`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_ITCHIES_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `knife`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"Get a knife"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `leave_it_in`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |
| `label` | String | `"EVENT_JAGGEDPATHWAY_STALACTITE_ANSW2"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `lightning`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW3"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `loot_heart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_DEADKING_TAKEHEART_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `makeup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_MAKEUP_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `nothanks`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |
| `label` | String | `"EVENT_NOTHANKS_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `pirouette`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_PIROUETTE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `place_gristle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_WALLOFFLESH_PLACE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `receive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"Receive"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `reflect`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT4_ANSW3"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `run_again`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |
| `label` | String | `"EVENT_RUN_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |

</details>

---

### Context: `sacrifice_full_favor`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_VOLCANO_SACRIFICE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `sacrifice_normal`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_MEATALTAR_SACRIFICE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `sacrifice_partial_favor`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_VOLCANO_SACRIFICE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `sacrifice_quest`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_MEATALTAR_SACRIFICE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `setup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `set_frame` | Number | `4` |  |

</details>

---

### Context: `speed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT3_ANSW3"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `surprise`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_SURPRISE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `take_blood`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_DEADKING_DRAINBLOOD_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `tappytoes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_TAPPYTOES_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `thorns`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT1_ANSW1"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `w1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW1"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `w2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW2"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `w3`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW3"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `w4`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW4"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `w5`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW5"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `w6`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW6"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `wheezies`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_WHEEZIES_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `altar_sacrifice`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"king intro"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `arm`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_ARMINSIDE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `bash_past_alt`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BASH_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `bite_it_off`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BIGTOE_BITE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `blue_needle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_NEEDLES_BLUE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `body`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_GENIE_CHOICE_CURSEBODY` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `break_lock`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LOCKEDCRATE_BREAK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `bribe`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_BRIBE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `catch`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_CATCH_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |

</details>

---

### Context: `challenge_to_game`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DEATH_CHALLENGE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `chaos_ending`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"chaos ending"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `chapter_cutscene`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"chap"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `charm_past_alt`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_CHARM_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `climb`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_CLIMB_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `comfort`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_COMFORT_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `communicate`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_COMMUNICATE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `concheck`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GETINTHEHOLE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `conditional_reward`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prompt` | String | `"EVENT_CATSINHEAT_REW6", "EVENT_CATSINHEAT_REW8"` |  |

</details>

---

### Context: `copy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSMACHINE_COPY_ANSW"` |  |

</details>

---

### Context: `crack_open`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_CRACKOPEN_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `cut_wires`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_CUTWIRES_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `damage_1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DEMONICIDOL_1DAMAGE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `damage_full`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DEMONICIDOL_FULLDAMAGE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `damage_half`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DEMONICIDOL_HALFDAMAGE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `desert_cutscene`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"desert"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `dexcheck`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GETINTHEHOLE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `dig`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DIG_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `disarm`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DISARM_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `dive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DIVE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `eat_meat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LEAKINGMEAT_EAT_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `enter_crater`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSCRATER_ENTER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `fiddle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_EXAMINE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `find`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GOLEMFIND_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `follow`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_FOLLOW_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |

</details>

---

### Context: `free`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_FREE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `gain_familiar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `initial_health` | Number | `10` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CharmedCaveBaby` |  |

</details>

---

### Context: `hack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_HACK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `intcheck`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GETINTHEHOLE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `join`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_JOININ_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `jump`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_JUMPOVER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |

</details>

---

### Context: `jump_over`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_JUMPOVER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `kiss_meat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LEAKINGMEAT_KISS_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `leg`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LEGINSIDE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `lick_alt`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LICK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `listen`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LISTEN_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `looks`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_GENIE_CHOICE_LOOKS` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `mind`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_GENIE_CHOICE_CURSEMIND` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `outsmart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BUTCHTUTORIAL_OUTSMART_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `party_permanent_stats`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `1` |  |

</details>

---

### Context: `patch_up`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_PATCHUP_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `pick_lock`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LOCKEDCRATE_PICK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `pilfer`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_PILFER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `power`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_GENIE_CHOICE_POWER` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `print`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSMACHINE_PRINT_ANSW"` |  |

</details>

---

### Context: `pull`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_PULLKNIFE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `pull_it_out`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_JAGGEDPATHWAY_STALACTITE_ANSW1"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `purify`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSCHAMBER_PURIFY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `push_through`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_JAGEDPATHWAY_ANSW_PUSH"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `put_out_of_misery`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_PUTOUTOFMISERY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `random_chance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `50%` | Probability weight for this outcome. |
| `get_item_from_pool` | [`Enum/String`](./Enums.md#enum-get_item_from_pool) | `chapter` | Event Action: Rewards the player with an item drawn from a specific loot pool. |

</details>

---

### Context: `reach_inside`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_SMALLBLACKHOLE_REACHINSIDE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |

</details>

---

### Context: `read`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_READ_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `red_needle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_NEEDLES_RED_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `remove`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_REMOVE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `remove_the_nail`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BIGTOE_NAIL_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `repair_quest`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_REPAIR_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `rest`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_REST_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `revive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_REVIVE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `rub`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_RUB_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `run_away`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_RUNAWAY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |

</details>

---

### Context: `scale`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSMACHINE_SCALE_ANSW"` |  |

</details>

---

### Context: `scream`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GOLEMSCREAM_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `shake`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_VENDINGMACHINE_SHAKE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `slip_through`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_SLIPTHROUGH_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `sneak_by`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_SNEAKBY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `sneak_past_alt`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_SNEAKBY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `soul`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_GENIE_CHOICE_CURSESOUL` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `sweet_talk`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DEATH_SWEETTALK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `swim`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_SWIM_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `tail`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_TAILINSIDE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `talk`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_TALKTO_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `talk_to`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_TALKTO_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `teleport`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSCHAMBER_TELEPORT_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `throw`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_HOLEINTHEEARTH_THROW_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `timemachine`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"Go to The Past"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `upgrade_yourself`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSCHAMBER_UPGRADE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `use_item`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_USE_ITEM_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `use_toilet_con`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_USETOILET_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `use_toilet_str`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_USETOILET_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `wealth`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_GENIE_CHOICE_WEALTH` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `wish_genes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MONKEYPAW_WISH2"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `wish_items`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MONKEYPAW_WISH3"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `wish_levelups`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MONKEYPAW_WISH4"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `wish_strength`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MONKEYPAW_WISH1"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `withstand`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_ELEPHANTSFOOTEVENCLOSER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `yank_it_out`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BIGTOE_YANK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `yellow_needle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_NEEDLES_YELLOW_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `break_ice`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_FROZENHUMANOID_BREAKICE_ANSW"` |  |

</details>

---

### Context: `cross`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_CROSS_ANSW"` |  |

</details>

---

### Context: `face`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GIFTOFGLORG_FACE_ANSW"` |  |

</details>

---

### Context: `flush_yourself`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_FLUSHYOURSELF_ANSW"` |  |

</details>

---

### Context: `gain_clone_familiar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `PlayerCat_MachineClone` |  |

</details>

---

### Context: `give_parasite`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BODYOFGLORG_PARASITE_ANSW"` |  |

</details>

---

### Context: `head`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GIFTOFGLORG_HEAD_ANSW"` |  |

</details>

---

### Context: `keep_going`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_KEEPGOING_ANSW"` |  |

</details>

---

### Context: `neck`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GIFTOFGLORG_NECK_ANSW"` |  |

</details>

---

### Context: `pull_lever`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_ODDDEVICE_PULLLEVER_ANSW"` |  |

</details>

---

### Context: `push_buttons`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_ODDDEVICE_PUSHBUTTONS_ANSW"` |  |

</details>

---

### Context: `use_weapon`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_USE_WEAPON_ANSW"` |  |

</details>

---

### Context: `spawn_reflection_next_fight`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

## Furniture & Metaprogression

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | [`Enum/String`](./Enums.md#enum-desc) | `FURNITURE_DESC_AUTOFEEDER, FURNITURE_DESC_SPECIAL_FOODBOX, FURNITURE_DESC_POOP` |  |
| `name` | [`Enum/String`](./Enums.md#enum-name) | `FURNITURE_NAME_SPECIAL_FOODBOX, FURNITURE_NAME_AUTOFEEDER, FURNITURE_NAME_POOP` |  |
| `Comfort` | Number | `-5, -2, 5` | Applies or references the 'Comfort' effect/state. |
| `Appeal` | Number | `2, 1, 5` | Applies or references the 'Appeal' effect/state. |
| `Stimulation` | Number | `2, 1, 5` | Applies or references the 'Stimulation' effect/state. |
| `set` | [`Enum/String`](./Enums.md#enum-set) | `spider, sewn, junk` |  |
| `Health` | Number | `-2, 5, -1` | Applies or references the 'Health' effect/state. |
| `Evolution` | Number | `2, 1, 5` | Applies or references the 'Evolution' effect/state. |
| `can_be_rare` | Boolean | `false` |  |
| `special` | Boolean | `true` |  |
| `BreedSuppression` | Number | `1` | Applies or references the 'BreedSuppression' effect/state. |
| `FightBonusRewards` | Number | `1` | Applies or references the 'FightBonusRewards' effect/state. |
| `FightRisk` | Number | `2` | Applies or references the 'FightRisk' effect/state. |
| `FoodStorage` | Number | `40` | Applies or references the 'FoodStorage' effect/state. |
| `removed` | Boolean | `true` |  |

</details>

---

## House & Environment

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"WEATHER_RAIN_DESC", "WEATHER_NONE_DESC", "WEATHER_FOG_DESC"` |  |
| `name` | String | `"WEATHER_RAIN_NAME", "WEATHER_NONE_NAME", "WEATHER_FOG_NAME"` |  |
| `effects` | [`Block`](./House_and_Environment.md#context-effects) | `{ ... }` |  |
| `ambient_sound` | [`Enum/String`](./Enums.md#enum-ambient_sound) | `amb_rain.ogg, amb_heavyrain.ogg, amb_windy.ogg` |  |
| `hint_persistent_elements` | [`Array`](./Arrays.md#array-hint_persistent_elements) | `[ Wind ], [ Heat ], [ Water ]` |  |
| `height` | Number | `7, 9, 5` |  |
| `movieclip` | [`Enum/String`](./Enums.md#enum-movieclip) | `RoomBackgroundSmallF2, RoomBackgroundAttic, RoomBackgroundLargeF2` |  |
| `width` | Number | `16, 35, 33` |  |
| `reverb_empty` | [`Block`](./House_and_Environment.md#context-reverb_empty) | `{ ... }` |  |
| `reverb_full` | [`Block`](./House_and_Environment.md#context-reverb_full) | `{ ... }` |  |
| `amount` | [`Enum/String`](./Enums.md#enum-amount) | `.25, .65` |  |
| `preset` | [`Enum/String`](./Enums.md#enum-preset) | `AUDITORIUM, LIVINGROOM` |  |
| `interstitial_bg_frame` | [`Enum/String`](./Enums.md#enum-interstitial_bg_frame) | `attic, room3, room4` |  |
| `n` | [`Array`](./Arrays.md#array-n) | `[ 1 -2 ], [ -1 -2 ]` |  |
| `volume_adjustment` | Number | `1.50` |  |
| `BasementUpgrade` | [`Block`](./House_and_Environment.md#context-basementupgrade) | `{ ... }` |  |
| `BasementUpgrade2` | [`Block`](./House_and_Environment.md#context-basementupgrade2) | `{ ... }` |  |
| `BasementUpgrade3` | [`Block`](./House_and_Environment.md#context-basementupgrade3) | `{ ... }` |  |
| `BasementUpgrade4` | [`Block`](./House_and_Environment.md#context-basementupgrade4) | `{ ... }` |  |
| `BasementUpgrade5` | [`Block`](./House_and_Environment.md#context-basementupgrade5) | `{ ... }` |  |
| `Default` | [`Block`](./House_and_Environment.md#context-default) | `{ ... }` |  |
| `Floor1_Large` | [`Block`](./House_and_Environment.md#context-floor1_large) | `{ ... }` |  |
| `Floor1_Small` | [`Block`](./House_and_Environment.md#context-floor1_small) | `{ ... }` |  |
| `House1` | [`Block`](./House_and_Environment.md#context-house1) | `{ ... }` |  |
| `House2` | [`Block`](./House_and_Environment.md#context-house2) | `{ ... }` |  |
| `House3` | [`Block`](./House_and_Environment.md#context-house3) | `{ ... }` |  |
| `LargeHouse` | [`Block`](./House_and_Environment.md#context-largehouse) | `{ ... }` |  |
| `LargeHouse_Floor2Large` | [`Block`](./House_and_Environment.md#context-largehouse_floor2large) | `{ ... }` |  |
| `LargeHouse_Floor2Small` | [`Block`](./House_and_Environment.md#context-largehouse_floor2small) | `{ ... }` |  |
| `MediumHouse` | [`Block`](./House_and_Environment.md#context-mediumhouse) | `{ ... }` |  |
| `MediumHouse_SmallRoom` | [`Block`](./House_and_Environment.md#context-mediumhouse_smallroom) | `{ ... }` |  |
| `Rain` | [`Block`](./House_and_Environment.md#context-rain) | `{ ... }` |  |
| `SmallAttic` | [`Block`](./House_and_Environment.md#context-smallattic) | `{ ... }` |  |
| `SmallHouse_Attic` | [`Block`](./House_and_Environment.md#context-smallhouse_attic) | `{ ... }` |  |
| `Snow` | [`Block`](./House_and_Environment.md#context-snow) | `{ ... }` |  |
| `Thunderstorm` | [`Block`](./House_and_Environment.md#context-thunderstorm) | `{ ... }` |  |
| `Windy` | [`Block`](./House_and_Environment.md#context-windy) | `{ ... }` |  |
| `extra_bound_planes` | [`Array`](./Arrays.md#array-extra_bound_planes) | `[ { p [ 0 0 ]` |  |
| `id` | [`Enum/String`](./Enums.md#enum-id) | `Attic` |  |
| `p` | [`Array`](./Arrays.md#array-p) | `[ 18 0 ]` |  |

</details>

---

### Context: `effects`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root), [`SolarFlare`](./House_and_Environment.md#context-solarflare)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpawnExtraThingsOnBattleStart` | [`Block`](./House_and_Environment.md#context-spawnextrathingsonbattlestart) | `{ ... }` |  |
| `FactionUprising` | [`Enum/String`](./Enums.md#enum-factionuprising) | `alien, robot, ghost` |  |
| `LowerAmbientLight` | Number | `50%, 33%` |  |
| `Rain` | Number | `2, 1, 4` |  |
| `Windy` | Number | `10, 1` |  |
| `Meteornado` | Number | `1` |  |
| `SpawnVolcanoOnBattleStart` | [`Block`](./House_and_Environment.md#context-spawnvolcanoonbattlestart) | `{ ... }` |  |
| `StatusCharactersOnRoundEnd` | [`Block`](./House_and_Environment.md#context-statuscharactersonroundend) | `{ ... }` |  |
| `CharacterTypeGainsStatusAtBattleStart` | [`Block`](./House_and_Environment.md#context-charactertypegainsstatusatbattlestart) | `{ ... }` |  |
| `FireStorm` | Number | `0%, 33%` |  |
| `GlobalSpawnOnRoundEnd` | [`Block`](./House_and_Environment.md#context-globalspawnonroundend) | `{ ... }` |  |
| `RandomLightning` | Number | `50%` |  |
| `Snow` | Number | `1` |  |
| `SpecialGodRays` | [`Block`](./House_and_Environment.md#context-specialgodrays) | `{ ... }` |  |
| `StatusAllCharactersOnSpawn` | [`Block`](./House_and_Environment.md#context-statusallcharactersonspawn) | `{ ... }` |  |
| `StatusCharactersOnRoundStart` | [`Block`](./House_and_Environment.md#context-statuscharactersonroundstart) | `{ ... }` |  |
| `AcidRain` | Number | `2` |  |
| `AddPostProcessEffect` | [`Block`](./House_and_Environment.md#context-addpostprocesseffect) | `{ ... }` |  |
| `AddTilesetObjects` | [`Block`](./House_and_Environment.md#context-addtilesetobjects) | `{ ... }` |  |
| `Blind` | Number | `3` |  |
| `Burn` | Number | `3` |  |
| `ButterflySwarm` | Number | `2` |  |
| `ClearDefaultDebris` | Number | `1` |  |
| `CockroachSwarm` | Number | `1` |  |
| `DeleteInanimateObjectsChance` | Number | `25%` |  |
| `FindExtraItemFromPoolOnBattleEnd` | [`Enum/String`](./Enums.md#enum-findextraitemfrompoolonbattleend) | `pills` |  |
| `FireflySwarm` | Number | `2` |  |
| `FlySwarm` | Number | `50%` |  |
| `Fog` | Number | `1` |  |
| `GlobalHealthRegenAura` | Number | `3` |  |
| `HeatWave` | Number | `1` |  |
| `JudgementDay` | Number | `25` |  |
| `LowGravityKnockbackBoost` | Number | `1` |  |
| `LowGravityRangeBoost` | Number | `2` |  |
| `MeteorShower` | Number | `25%` |  |
| `PersistentElement` | [`Enum/String`](./Enums.md#enum-persistentelement) | `Holy` |  |
| `RandomWeatherEachFight` | [`Array`](./Arrays.md#array-randomweathereachfight) | `[ Fog Rain Windy Sandstorm HeatWave Snow Thunderstorm Bli...` |  |
| `Sandstorm` | Number | `1` |  |
| `SolarFlare` | [`Block`](./House_and_Environment.md#context-solarflare) | `{ ... }` |  |
| `SpawnTilePuddleOnBattleStart` | [`Block`](./House_and_Environment.md#context-spawntilepuddleonbattlestart) | `{ ... }` |  |
| `VisualFlySwarm` | Number | `1` |  |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `number` | [`Array`](./Arrays.md#array-number) | `[ 3 5 ], [ 2 5 ], [ 12 20 ]` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Boulder, SmallRock, [ Junk Junk TrashBag ]` |  |
| `tile` | [`Enum/String`](./Enums.md#enum-tile) | `WaterTile, TallGrassTile, BrambleTile` |  |
| `trap` | [`Enum/String`](./Enums.md#enum-trap) | `LandMine, BearTrap` |  |

</details>

---

### Context: `reverb_empty`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Floor1_Large`](./House_and_Environment.md#context-floor1_large), [`Floor1_Small`](./House_and_Environment.md#context-floor1_small), [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `amount` | [`Enum/String`](./Enums.md#enum-amount) | `.65` |  |
| `preset` | [`Enum/String`](./Enums.md#enum-preset) | `AUDITORIUM, STONEROOM` |  |
| `volume_adjustment` | Number | `1.50, 2` |  |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./House_and_Environment.md#context-conditional_goodroll), [`Else`](./House_and_Environment.md#context-else)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomStatDown` | Number | `1` |  |
| `RandomStatUp` | Number | `1` |  |
| `Bleed` | Number | `1` |  |
| `Blind` | Number | `1` |  |
| `Brace` | Number | `1` |  |
| `Bruise` | Number | `1` |  |
| `DamageUp` | Number | `1` |  |
| `DivineShield` | Number | `1` |  |
| `Drowsy` | Number | `1` |  |
| `KineticSpikes` | Number | `1` |  |
| `Poison` | Number | `1` |  |
| `Shield` | Number | `1` |  |
| `Slow` | Number | `1` |  |
| `SpellDamageUp` | Number | `1` |  |
| `Thorns` | Number | `1` |  |
| `Weakness` | Number | `1` |  |

</details>

---

### Context: `room_positions`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`House1`](./House_and_Environment.md#context-house1), [`House2`](./House_and_Environment.md#context-house2), [`House3`](./House_and_Environment.md#context-house3)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Floor1_Large` | [`Array`](./Arrays.md#array-floor1_large) | `[ 1, 1 ]` |  |
| `Basement0` | [`Array`](./Arrays.md#array-basement0) | `[ 1 -6 ]` |  |
| `Basement1` | [`Array`](./Arrays.md#array-basement1) | `[ 1 -12 ]` |  |
| `Basement2` | [`Array`](./Arrays.md#array-basement2) | `[ 1 -18 ]` |  |
| `Basement3` | [`Array`](./Arrays.md#array-basement3) | `[ 1 -24 ]` |  |
| `Basement4` | [`Array`](./Arrays.md#array-basement4) | `[ 1 -30 ]` |  |
| `Floor1_Small` | [`Array`](./Arrays.md#array-floor1_small) | `[ 18, 1 ]` |  |
| `LargeAttic` | [`Array`](./Arrays.md#array-largeattic) | `[ 0, 9 ], [ 0, 17 ]` |  |
| `Floor2_Large` | [`Array`](./Arrays.md#array-floor2_large) | `[ 18, 9 ]` |  |
| `Floor2_Small` | [`Array`](./Arrays.md#array-floor2_small) | `[ 1, 9 ]` |  |
| `SmallAttic` | [`Array`](./Arrays.md#array-smallattic) | `[ 0, 9 ]` |  |

</details>

---

### Context: `aux_positions`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`House1`](./House_and_Environment.md#context-house1), [`House2`](./House_and_Environment.md#context-house2), [`House3`](./House_and_Environment.md#context-house3)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ButchBox` | [`Array`](./Arrays.md#array-butchbox) | `[ 21, 0 ], [ 38, 0 ]` |  |
| `HousePipe` | [`Array`](./Arrays.md#array-housepipe) | `[ -2 0 ]` |  |
| `Roof_LeftEdge` | [`Array`](./Arrays.md#array-roof_leftedge) | `[ -3.482 16.11 ], [ -3.617 8.112 ], [ -3.388 8.138 ]` |  |
| `Roof_RightEdge` | [`Array`](./Arrays.md#array-roof_rightedge) | `[ 21.548 8.175 ], [ 38.518 8.207 ], [ 38.408 16.185 ]` |  |
| `Roof_Top` | [`Array`](./Arrays.md#array-roof_top) | `[ 17.563 18.677 ], [ 8.983 14.4 ], [ 17.562 26.715 ]` |  |
| `StraySpawn` | [`Array`](./Arrays.md#array-strayspawn) | `[ -3 0 ]` |  |

</details>

---

### Context: `reverb_full`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Floor1_Large`](./House_and_Environment.md#context-floor1_large), [`Floor1_Small`](./House_and_Environment.md#context-floor1_small), [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `amount` | [`Enum/String`](./Enums.md#enum-amount) | `.25` |  |
| `preset` | [`Enum/String`](./Enums.md#enum-preset) | `LIVINGROOM` |  |

</details>

---

### Context: `SpawnVolcanoOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Sprout, PunchingBag, MiniVolcano` |  |
| `max_radius` | Number | `2.2` |  |
| `min_radius` | Number | `1, .2` |  |
| `puddle_tile` | [`Enum/String`](./Enums.md#enum-puddle_tile) | `LavaTile, [ BrambleTile TallBrambleTile ]` |  |
| `number` | [`Array`](./Arrays.md#array-number) | `[ 3 5 ]` |  |

</details>

---

### Context: `SmallAttic`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `extra_bound_planes` | [`Array`](./Arrays.md#array-extra_bound_planes) | `[ { p [ 0 0 ]` |  |
| `height` | Number | `5` |  |
| `id` | [`Enum/String`](./Enums.md#enum-id) | `Attic` |  |
| `interstitial_bg_frame` | [`Enum/String`](./Enums.md#enum-interstitial_bg_frame) | `attic` |  |
| `movieclip` | [`Enum/String`](./Enums.md#enum-movieclip) | `RoomBackgroundSmallAttic` |  |
| `n` | [`Array`](./Arrays.md#array-n) | `[ 1 -2 ]` |  |
| `width` | Number | `18` |  |

</details>

---

### Context: `Floor1_Large`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `height` | Number | `7` |  |
| `interstitial_bg_frame` | [`Enum/String`](./Enums.md#enum-interstitial_bg_frame) | `room1` |  |
| `movieclip` | [`Enum/String`](./Enums.md#enum-movieclip) | `RoomBackgroundLargeF1` |  |
| `reverb_empty` | [`Block`](./House_and_Environment.md#context-reverb_empty) | `{ ... }` |  |
| `reverb_full` | [`Block`](./House_and_Environment.md#context-reverb_full) | `{ ... }` |  |
| `width` | Number | `16` |  |

</details>

---

### Context: `Floor1_Small`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `height` | Number | `7` |  |
| `interstitial_bg_frame` | [`Enum/String`](./Enums.md#enum-interstitial_bg_frame) | `room2` |  |
| `movieclip` | [`Enum/String`](./Enums.md#enum-movieclip) | `RoomBackgroundSmallF1` |  |
| `reverb_empty` | [`Block`](./House_and_Environment.md#context-reverb_empty) | `{ ... }` |  |
| `reverb_full` | [`Block`](./House_and_Environment.md#context-reverb_full) | `{ ... }` |  |
| `width` | Number | `16` |  |

</details>

---

### Context: `House1`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `aux_positions` | [`Block`](./House_and_Environment.md#context-aux_positions) | `{ ... }` |  |
| `bg_placements_frame` | [`Enum/String`](./Enums.md#enum-bg_placements_frame) | `small` |  |
| `movieclip_bg` | [`Enum/String`](./Enums.md#enum-movieclip_bg) | `HouseBackground1` |  |
| `movieclip_fg` | [`Enum/String`](./Enums.md#enum-movieclip_fg) | `HouseForeground1` |  |
| `room_positions` | [`Block`](./House_and_Environment.md#context-room_positions) | `{ ... }` |  |
| `zoomout_catvolume` | [`Enum/String`](./Enums.md#enum-zoomout_catvolume) | `.8` |  |

</details>

---

### Context: `House2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `aux_positions` | [`Block`](./House_and_Environment.md#context-aux_positions) | `{ ... }` |  |
| `bg_placements_frame` | [`Enum/String`](./Enums.md#enum-bg_placements_frame) | `large` |  |
| `movieclip_bg` | [`Enum/String`](./Enums.md#enum-movieclip_bg) | `HouseBackground2` |  |
| `movieclip_fg` | [`Enum/String`](./Enums.md#enum-movieclip_fg) | `HouseForeground2` |  |
| `room_positions` | [`Block`](./House_and_Environment.md#context-room_positions) | `{ ... }` |  |
| `zoomout_catvolume` | [`Enum/String`](./Enums.md#enum-zoomout_catvolume) | `.7` |  |

</details>

---

### Context: `House3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `aux_positions` | [`Block`](./House_and_Environment.md#context-aux_positions) | `{ ... }` |  |
| `bg_placements_frame` | [`Enum/String`](./Enums.md#enum-bg_placements_frame) | `large` |  |
| `movieclip_bg` | [`Enum/String`](./Enums.md#enum-movieclip_bg) | `HouseBackground3` |  |
| `movieclip_fg` | [`Enum/String`](./Enums.md#enum-movieclip_fg) | `HouseForeground3` |  |
| `room_positions` | [`Block`](./House_and_Environment.md#context-room_positions) | `{ ... }` |  |
| `zoomout_catvolume` | [`Enum/String`](./Enums.md#enum-zoomout_catvolume) | `.6` |  |

</details>

---

### Context: `Thunderstorm`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `adventure_weather` | [`Enum/String`](./Enums.md#enum-adventure_weather) | `Thunderstorm` |  |
| `ambient_sound` | [`Enum/String`](./Enums.md#enum-ambient_sound) | `amb_heavyrain.ogg` |  |
| `lightning_fx` | Boolean | `true` |  |
| `particles` | [`Array`](./Arrays.md#array-particles) | `[ Thunderstorm ]` |  |
| `prewarm` | Number | `5` |  |
| `skybox_frame` | [`Enum/String`](./Enums.md#enum-skybox_frame) | `day_thunderstorm` |  |

</details>

---

### Context: `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `any` |  |
| `Conditional_Flying` | Block | `{ ... }` |  |
| `Else` | [`Block`](./House_and_Environment.md#context-else) | `{ ... }` |  |
| `Stealth` | Number | `1` |  |

</details>

---

### Context: `Rain`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `adventure_weather` | [`Enum/String`](./Enums.md#enum-adventure_weather) | `Rain` |  |
| `ambient_sound` | [`Enum/String`](./Enums.md#enum-ambient_sound) | `amb_rain.ogg` |  |
| `particles` | [`Array`](./Arrays.md#array-particles) | `[ Rain ]` |  |
| `prewarm` | Number | `5` |  |
| `skybox_frame` | [`Enum/String`](./Enums.md#enum-skybox_frame) | `day_rain` |  |

</details>

---

### Context: `Snow`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `adventure_weather` | [`Enum/String`](./Enums.md#enum-adventure_weather) | `Snow` |  |
| `ambient_sound` | [`Enum/String`](./Enums.md#enum-ambient_sound) | `amb_snow.ogg` |  |
| `particles` | [`Array`](./Arrays.md#array-particles) | `[ Snow ]` |  |
| `prewarm` | Number | `20` |  |
| `skybox_frame` | [`Enum/String`](./Enums.md#enum-skybox_frame) | `day_snow` |  |

</details>

---

### Context: `Windy`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `adventure_weather` | [`Enum/String`](./Enums.md#enum-adventure_weather) | `Windy` |  |
| `ambient_sound` | [`Enum/String`](./Enums.md#enum-ambient_sound) | `amb_windy.ogg` |  |
| `particles` | [`Array`](./Arrays.md#array-particles) | `[ WindFull ]` |  |
| `prewarm` | Number | `5` |  |
| `skybox_frame` | [`Enum/String`](./Enums.md#enum-skybox_frame) | `day_windy` |  |

</details>

---

### Context: `Big`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`SpecialGodRays`](./House_and_Environment.md#context-specialgodrays)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `follow_character_tag` | [`Enum/String`](./Enums.md#enum-follow_character_tag) | `zaratana` |  |
| `position` | [`Array`](./Arrays.md#array-position) | `[ 4.5 4.5 ]` |  |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusCharactersOnRoundEnd`](./House_and_Environment.md#context-statuscharactersonroundend), [`StatusCharactersOnRoundStart`](./House_and_Environment.md#context-statuscharactersonroundstart)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `odds` | Number | `25%, .5` |  |
| `Conditional_Corpse` | [`Block`](./House_and_Environment.md#context-conditional_corpse) | `{ ... }` |  |
| `RandomStatusFromPool` | [`Block`](./House_and_Environment.md#context-randomstatusfrompool) | `{ ... }` |  |

</details>

---

### Context: `Else`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`CharacterTypeGainsStatusAtBattleStart`](./House_and_Environment.md#context-charactertypegainsstatusatbattlestart), [`StatusAllCharactersOnSpawn`](./House_and_Environment.md#context-statusallcharactersonspawn), [`StatusCharactersOnRoundStart`](./House_and_Environment.md#context-statuscharactersonroundstart)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllyInfested` | [`Block`](./House_and_Environment.md#context-allyinfested) | `{ ... }` |  |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1 .25 ]` |  |
| `Poison` | [`Array`](./Arrays.md#array-poison) | `[ 1 .25 ]` |  |
| `RandomStatusFromPool` | [`Block`](./House_and_Environment.md#context-randomstatusfrompool) | `{ ... }` |  |

</details>

---

### Context: `StatusCharactersOnRoundEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_GoodRoll` | [`Block`](./House_and_Environment.md#context-conditional_goodroll) | `{ ... }` |  |
| `FloatingRockTrap` | Number | `1` |  |
| `Thorns` | Number | `1` |  |
| `tag_filter` | [`Enum/String`](./Enums.md#enum-tag_filter) | `rock` |  |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`extra_statuses`](./House_and_Environment.md#context-extra_statuses)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddExtraTurnsBeforeRun` | Number | `2` |  |
| `ApplyPassives` | [`Block`](./House_and_Environment.md#context-applypassives) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `bonusbird` |  |

</details>

---

### Context: `GlobalSpawnOnRoundEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `NeutralTwister, NeutralZombieKitten` |  |
| `number` | [`Array`](./Arrays.md#array-number) | `[ 1 2 ]` |  |

</details>

---

### Context: `SolarFlare`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `5` |  |
| `effects` | [`Block`](./House_and_Environment.md#context-effects) | `{ ... }` |  |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Fire ]` |  |

</details>

---

### Context: `SpawnTilePuddleOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `max_radius` | Number | `3.5` |  |
| `min_radius` | Number | `1.5` |  |
| `tile` | [`Enum/String`](./Enums.md#enum-tile) | `OilTile` |  |

</details>

---

### Context: `StatusAllCharactersOnSpawn`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_PartyMember` | [`Block`](./House_and_Environment.md#context-conditional_partymember) | `{ ... }` |  |
| `Conditional_Tiny` | Block | `{ ... }` |  |
| `Else` | [`Block`](./House_and_Environment.md#context-else) | `{ ... }` |  |

</details>

---

### Context: `StatusCharactersOnRoundStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_GoodRoll` | [`Block`](./House_and_Environment.md#context-conditional_goodroll) | `{ ... }` |  |
| `Else` | [`Block`](./House_and_Environment.md#context-else) | `{ ... }` |  |
| `Madness` | [`Array`](./Arrays.md#array-madness) | `[ 1 .25 ]` |  |

</details>

---

### Context: `extra_statuses`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`FactionUprising`](./House_and_Environment.md#context-factionuprising)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` |  |
| `Conditional_HasTag` | [`Block`](./House_and_Environment.md#context-conditional_hastag) | `{ ... }` |  |
| `HealthGain` | Number | `8` |  |

</details>

---

### Context: `AddPostProcessEffect`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `requires_framebuffer` | Boolean | `false` |  |
| `shader` | [`Enum/String`](./Enums.md#enum-shader) | `shimmervignette` |  |

</details>

---

### Context: `AllyInfested`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Else`](./House_and_Environment.md#context-else)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `faction` | [`Enum/String`](./Enums.md#enum-faction) | `allies` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CharmedMaggot` |  |

</details>

---

### Context: `ApplyPassives`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./House_and_Environment.md#context-conditional_hastag), [`Conditional_PartyMember`](./House_and_Environment.md#context-conditional_partymember)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddInitiative` | Number | `999` |  |
| `StatusOnBattleEnd` | [`Block`](./House_and_Environment.md#context-statusonbattleend) | `{ ... }` |  |

</details>

---

### Context: `BasementUpgrade`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `MediumHouse` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Basement0` |  |

</details>

---

### Context: `BasementUpgrade2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `BasementUpgrade` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Basement1` |  |

</details>

---

### Context: `BasementUpgrade3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `BasementUpgrade2` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Basement2` |  |

</details>

---

### Context: `BasementUpgrade4`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `BasementUpgrade3` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Basement3` |  |

</details>

---

### Context: `BasementUpgrade5`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `BasementUpgrade4` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Basement4` |  |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./House_and_Environment.md#context-conditional_goodroll)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | `5` |  |
| `Revive` | Number | `50%` |  |

</details>

---

### Context: `Default`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `set_house` | [`Enum/String`](./Enums.md#enum-set_house) | `House1` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Floor1_Large` |  |

</details>

---

### Context: `FactionUprising`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `extra_statuses` | [`Block`](./House_and_Environment.md#context-extra_statuses) | `{ ... }` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `bird` |  |

</details>

---

### Context: `LargeHouse`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `MediumHouse` |  |
| `set_house` | [`Enum/String`](./Enums.md#enum-set_house) | `House3` |  |

</details>

---

### Context: `LargeHouse_Floor2Large`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `LargeHouse` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Floor2_Large` |  |

</details>

---

### Context: `LargeHouse_Floor2Small`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `LargeHouse` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Floor2_Small` |  |

</details>

---

### Context: `MediumHouse`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `Default` |  |
| `set_house` | [`Enum/String`](./Enums.md#enum-set_house) | `House2` |  |

</details>

---

### Context: `MediumHouse_SmallRoom`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `MediumHouse` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Floor1_Small` |  |

</details>

---

### Context: `SmallHouse_Attic`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prereq` | [`Enum/String`](./Enums.md#enum-prereq) | `Default` |  |
| `unlock_room` | [`Enum/String`](./Enums.md#enum-unlock_room) | `Attic` |  |

</details>

---

### Context: `SpecialGodRays`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Big` | [`Block`](./House_and_Environment.md#context-big) | `{ ... }` |  |

</details>

---

### Context: `AddTilesetObjects`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FloatingDebris` | [`Block`](./House_and_Environment.md#context-floatingdebris) | `{ ... }` |  |

</details>

---

### Context: `Conditional_PartyMember`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusAllCharactersOnSpawn`](./House_and_Environment.md#context-statusallcharactersonspawn)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ApplyPassives` | [`Block`](./House_and_Environment.md#context-applypassives) | `{ ... }` |  |

</details>

---

### Context: `FloatingDebris`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddTilesetObjects`](./House_and_Environment.md#context-addtilesetobjects)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `20` |  |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ApplyPassives`](./House_and_Environment.md#context-applypassives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMutation` | Number | `1` |  |

</details>

---

## Injuries

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `deathsound` | [`Enum/String`](./Enums.md#enum-deathsound) | `Injury_BrokenPaw, Injury_BrokenRib, Injury_TornTendon` |  |
| `id` | Number | `1, 2, 0` |  |
| `text` | String | `"INJURY_NAME_TORNTENDON", "INJURY_NAME_BROKENPAW", "INJURY_NAME_BROKENRIB"` |  |
| `stats` | [`Block`](./Injuries.md#context-stats) | `{ ... }` |  |
| `scars` | [`Block`](./Injuries.md#context-scars) | `{ ... }` |  |
| `alt_animations` | [`Array`](./Arrays.md#array-alt_animations) | `[ [ dying, brokenPaw ], [ [ dying, dislocatedShoulder ], [ [ dying, intestinalProlapse ]` |  |

</details>

---

### Context: `stats`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Injuries.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `-1` |  |
| `lck` | Number | `-2, -1` |  |
| `cha` | Number | `-1` |  |
| `dex` | Number | `-1` |  |
| `int` | Number | `-1` |  |
| `str` | Number | `-1` |  |
| `spd` | Number | `-1` |  |

</details>

---

### Context: `scars`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Injuries.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `head` | [`Array`](./Arrays.md#array-head) | `[ 34 41 ], [ 15 22 ], [ 23 33 ]` |  |
| `body` | [`Array`](./Arrays.md#array-body) | `[ 2 9 ], [ 16 25 ], [ 26 30 ]` |  |
| `arms` | [`Array`](./Arrays.md#array-arms) | `[ 10 20 ]` |  |
| `legs` | [`Array`](./Arrays.md#array-legs) | `[ 2 9 ]` |  |
| `limbs` | [`Array`](./Arrays.md#array-limbs) | `[ 21 31 ]` |  |

</details>

---

## Item Pools

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `rare` | Number | `10, 40, 15` |  |
| `uncommon` | Number | `75, 35, 60` |  |
| `very_rare` | Number | `2, 1, .01` |  |
| `common` | Number | `55, 50, 60` |  |
| `current_chapter_common` | [`Enum/String`](./Enums.md#enum-current_chapter_common) | `auto, 55` |  |
| `current_chapter_rare` | [`Enum/String`](./Enums.md#enum-current_chapter_rare) | `auto, 10` |  |
| `current_chapter_uncommon` | [`Enum/String`](./Enums.md#enum-current_chapter_uncommon) | `auto, 35` |  |
| `current_chapter_very_rare` | [`Enum/String`](./Enums.md#enum-current_chapter_very_rare) | `auto, 1` |  |
| `chapter_rare` | Number | `1` |  |
| `Chicken` | Number | `2, .01, .1` |  |
| `chapter` | Number | `1` |  |
| `chapter_common` | Number | `1` |  |
| `consumables` | Number | `10, 60` |  |
| `FoodBig` | Number | `2, 1` |  |
| `FoodMedium` | Number | `1, 5` |  |
| `basic_consumables` | Number | `90, 100` |  |
| `shop_common` | Number | `1` |  |
| `Antidote` | Number | `1` |  |
| `BagOfSeeds` | [`Enum/String`](./Enums.md#enum-bagofseeds) | `.3` |  |
| `BirdFeed` | [`Enum/String`](./Enums.md#enum-birdfeed) | `.3` |  |
| `BirdPoopHat` | [`Enum/String`](./Enums.md#enum-birdpoophat) | `.3` |  |
| `Catnip` | Number | `3` |  |
| `CatnipBig` | Number | `2` |  |
| `DeadHummingbird` | [`Enum/String`](./Enums.md#enum-deadhummingbird) | `.3` |  |
| `GlowingSeed` | [`Enum/String`](./Enums.md#enum-glowingseed) | `.3` |  |
| `GoldenEgg` | [`Enum/String`](./Enums.md#enum-goldenegg) | `.3` |  |
| `HarpysClaw` | [`Enum/String`](./Enums.md#enum-harpysclaw) | `.5` |  |
| `LostSoul` | [`Enum/String`](./Enums.md#enum-lostsoul) | `.5` |  |
| `MagicSeed` | [`Enum/String`](./Enums.md#enum-magicseed) | `.3` |  |
| `Parousworm` | [`Enum/String`](./Enums.md#enum-parousworm) | `.5` |  |
| `PeaceSymbol` | [`Enum/String`](./Enums.md#enum-peacesymbol) | `.3` |  |
| `PeaceSymbolFacePaint` | [`Enum/String`](./Enums.md#enum-peacesymbolfacepaint) | `.3` |  |
| `RaptorEgg` | [`Enum/String`](./Enums.md#enum-raptoregg) | `.1` |  |
| `RavenFeather` | [`Enum/String`](./Enums.md#enum-ravenfeather) | `.3` |  |
| `TieDyeBandana` | [`Enum/String`](./Enums.md#enum-tiedyebandana) | `.3` |  |
| `Turkey` | Number | `2` |  |
| `WeirdEgg` | [`Enum/String`](./Enums.md#enum-weirdegg) | `.3` |  |
| `WishBone` | [`Enum/String`](./Enums.md#enum-wishbone) | `.3` |  |
| `consumables_consumable_common` | Number | `50` |  |
| `consumables_consumable_rare` | Number | `15` |  |
| `consumables_consumable_uncommon` | Number | `35` |  |
| `consumables_consumable_very_rare` | Number | `1` |  |
| `general_common` | [`Enum/String`](./Enums.md#enum-general_common) | `auto` |  |
| `general_rare` | [`Enum/String`](./Enums.md#enum-general_rare) | `auto` |  |
| `general_uncommon` | [`Enum/String`](./Enums.md#enum-general_uncommon) | `auto` |  |
| `general_very_rare` | [`Enum/String`](./Enums.md#enum-general_very_rare) | `auto` |  |
| `pills` | Number | `7` |  |

</details>

---

## Items & Equipment

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"ARMOR_SCRAPMETALARMOR_DESC", "ARMOR_SCRAPMETALHAT_DESC", "ARMOR_SCRAPMETALMASK_DESC"` | Localization key for the item's desc. |
| `name` | String | `"ARMOR_SCRAPMETALARMOR_NAME", "ARMOR_SCRAPMETALMASK_NAME", "ARMOR_SCRAPMETALHAT_NAME"` | Localization key for the item's name. |
| `frame` | Number | `2, 23, 12` |  |
| `kind` | [`Enum/String`](./Enums.md#enum-kind) | `neck, face, head` |  |
| `rarity` | [`Enum/String`](./Enums.md#enum-rarity) | `common, uncommon, rare` |  |
| `set` | [`Enum/String`](./Enums.md#enum-set) | `Scrap, Leather, Rag` |  |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `wp_PartyDetonatorFixed, wp_PersuasionDevice, wp_PartyDetonator` | ID of the ability to trigger or reference. |
| `shield` | Number | `2, 1, 4` |  |
| `durability` | Number | `2, 1, 3` | Maximum uses before breaking. |
| `pieces_required` | Number | `3` |  |
| `cursed` | Boolean | `true` |  |
| `cha` | Number | `2, 1, -1` |  |
| `consumable` | Boolean | `true` |  |
| `spd` | Number | `-4, 3, -1` |  |
| `con` | Number | `2, 1, 3` |  |
| `int` | Number | `7, 1, -1` |  |
| `lck` | Number | `2, 1, -3` |  |
| `quest_item` | Boolean | `false, true` |  |
| `parasite` | Boolean | `true` |  |
| `aux` | Number | `24, 10, 12` |  |
| `variant_of` | [`Enum/String`](./Enums.md#enum-variant_of) | `RedCap, PoundOfFlesh, CrimsonMask` |  |
| `str` | [`Enum/String`](./Enums.md#enum-str) | `aux, 2, 1` |  |
| `dex` | Number | `1, 3, -1` |  |
| `quest_reward_item` | [`Enum/String`](./Enums.md#enum-quest_reward_item) | `PersuasionDevice_Fixed, MagicMirror_Fixed, ChaosDevice_Fixed` |  |
| `indestructible` | Boolean | `true` |  |
| `divine_shield` | Number | `2, 1, 3` |  |
| `legacy_quest` | Boolean | `true` |  |
| `hint_destination` | [`Enum/String`](./Enums.md#enum-hint_destination) | `caves, boneyard, meatworld` |  |
| `str_aux_initialize` | [`Enum/String`](./Enums.md#enum-str_aux_initialize) | `random_seed, random_stat, random_class_passive` |  |
| `dont_destroy_on_0` | Boolean | `true` |  |
| `global_tags` | [`Array`](./Arrays.md#array-global_tags) | `[ all_cats_are_jester ], [ fail_all_events ], [ always_ambushed ]` |  |
| `max_durability` | Number | `2, 9, 3` |  |
| `on_store` | [`Enum/String`](./Enums.md#enum-on_store) | `become_rare_furniture, become_furniture, become_aux_coins` |  |
| `name_mod` | String | `"CAT_NAME_MOD_AMOEBA", "CAT_NAME_MOD_MAN", "CAT_NAME_MOD_COOL"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicTankMelee, BasicSpin, IsaacBasicAttack` |  |
| `hint_prerequisite_flag` | [`Enum/String`](./Enums.md#enum-hint_prerequisite_flag) | `mapflag_MeatWorldUnlocked, mapflag_BothObelisksUnlocked, mapflag_MeatWorldUnlockedFull` |  |
| `failable` | Boolean | `true` |  |
| `randomize_piece_frames` | Boolean | `true` |  |
| `str_aux_is_copy_passive` | Boolean | `true` |  |
| `fragile` | Boolean | `true` |  |
| `icon_hint` | [`Enum/String`](./Enums.md#enum-icon_hint) | `passive_syringe, ability_syringe` |  |
| `max_health` | Number | `-1` |  |
| `reset_aux_on_store` | Number | `1` |  |
| `sticky` | Boolean | `true` |  |
| `weightless` | Boolean | `true` |  |
| `prevent_level_up` | Boolean | `true` |  |
| `quest_item_alias` | [`Enum/String`](./Enums.md#enum-quest_item_alias) | `BlackShard, NuclearKnife` |  |
| `speed` | Number | `1` |  |
| `str_aux_is_copy_item_passive` | Boolean | `true` |  |
| `Set` | [`Enum/String`](./Enums.md#enum-set) | `Monk` | Applies or references the 'Set' effect/state. |
| `aux_is_catid` | Boolean | `true` |  |
| `cant_equip_to_colorless` | Boolean | `true` |  |
| `degrade_after_adventure` | Boolean | `false` |  |
| `equip_sound` | [`Enum/String`](./Enums.md#enum-equip_sound) | `SE_CatWeaponPoke_Chainsaw` |  |
| `force_sticky` | Boolean | `true` |  |
| `reset_str_aux_on_store` | [`Enum/String`](./Enums.md#enum-reset_str_aux_on_store) | `ModelingClay_Default` |  |
| `str_aux` | [`Enum/String`](./Enums.md#enum-str_aux) | `ModelingClay_Default` |  |
| `str_aux_is_copy_item_active` | Boolean | `true` |  |
| `str_aux_is_copy_item_icon` | Boolean | `true` |  |

</details>

---

### Context: `passives`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Metal` | Number | `1` | Applies or references the 'Metal' effect/state. |
| `AddStatusToBasicAttack` | [`Block`](./Items_and_Equipment.md#context-addstatustobasicattack) | `{ ... }` | Injects a status effect payload that applies whenever the character performs a basic attack. |
| `Brace` | Number | `2, 1, 3` | Applies or references the 'Brace' effect/state. |
| `Thorns` | Number | `2, 1, 3` | Applies or references the 'Thorns' effect/state. |
| `HealthRegenUp` | Number | `2, 1, 3` | Applies or references the 'HealthRegenUp' effect/state. |
| `SpawnOnBattleStart` | [`Block`](./Items_and_Equipment.md#context-spawnonbattlestart) | `{ ... }, CharmedCultist, CharmedGamete` | Applies or references the 'SpawnOnBattleStart' effect/state. |
| `Brittle` | Number | `1` | Applies or references the 'Brittle' effect/state. |
| `Fragile` | Number | `1` | Applies or references the 'Fragile' effect/state. |
| `ArmorDodgeChance` | Number | `10%, 5%, 15%` | Applies or references the 'ArmorDodgeChance' effect/state. |
| `DamageUp` | Number | `6, -2, 1` | Applies or references the 'DamageUp' effect/state. |
| `Flammable` | Number | `2, 1` | Applies or references the 'Flammable' effect/state. |
| `AddBonusRange` | Number | `2, 1, 10` | Applies or references the 'AddBonusRange' effect/state. |
| `BleedThorns` | Number | `6, 1, 3` | Applies or references the 'BleedThorns' effect/state. |
| `StatusImmunity` | [`Array`](./Arrays.md#array-statusimmunity) | `[ Fear Confusion PermanentConfusion ], [ Freeze, Slow ], Poison` | Applies or references the 'StatusImmunity' effect/state. |
| `SpawnThingOnDeath` | [`Enum/String`](./Enums.md#enum-spawnthingondeath) | `CharmedPooter, CharmedTinyTumor, TheIntruder` | Applies or references the 'SpawnThingOnDeath' effect/state. |
| `StatusEachTurnBegin` | [`Block`](./Items_and_Equipment.md#context-statuseachturnbegin) | `{ ... }` | Applies or references the 'StatusEachTurnBegin' effect/state. |
| `CritChanceUp` | Number | `10, 100, 5` | Applies or references the 'CritChanceUp' effect/state. |
| `KineticSpikes` | Number | `1, 3` | Applies or references the 'KineticSpikes' effect/state. |
| `ReplaceBasicMove` | [`Enum/String`](./Enums.md#enum-replacebasicmove) | `BellyFlop_BasicMove, head_HeadBrandJump, BasicJump` | Applies or references the 'ReplaceBasicMove' effect/state. |
| `AbilityOnBattleStart` | [`Enum/String`](./Enums.md#enum-abilityonbattlestart) | `face_FartFace, head_SpiderInjector, face_FartFaceFixed` | Applies or references the 'AbilityOnBattleStart' effect/state. |
| `AddLevelUpRerolls` | Number | `2, 1, 3` | Applies or references the 'AddLevelUpRerolls' effect/state. |
| `AddManaRegen` | Number | `2, 1, 3` | Applies or references the 'AddManaRegen' effect/state. |
| `BrittleDuringElement` | [`Enum/String`](./Enums.md#enum-brittleduringelement) | `water` | Applies or references the 'BrittleDuringElement' effect/state. |
| `ManaCostReduction` | Number | `2, -2, 1` | Applies or references the 'ManaCostReduction' effect/state. |
| `PoisonThorns` | Number | `2, 1` | Applies or references the 'PoisonThorns' effect/state. |
| `SetFragileImmune` | [`Enum/String`](./Enums.md#enum-setfragileimmune) | `Paper, Cool, ""` | Applies or references the 'SetFragileImmune' effect/state. |
| `TrinketPassiveMultiplierBonus` | Number | `2, 1` | Applies or references the 'TrinketPassiveMultiplierBonus' effect/state. |
| `AddCorpseHealth` | Number | `6, -999999` | Applies or references the 'AddCorpseHealth' effect/state. |
| `Bruise` | Number | `2, 1` | Applies or references the 'Bruise' effect/state. |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Fire, Ice` | Applies or references the 'ElementImmune' effect/state. |
| `Flying` | Number | `1` | Applies or references the 'Flying' effect/state. |
| `SetBrittleImmune` | [`Enum/String`](./Enums.md#enum-setbrittleimmune) | `Paper, JankAlloy, ""` | Applies or references the 'SetBrittleImmune' effect/state. |
| `Trample` | Number | `9, 3` | Applies or references the 'Trample' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `Bleed` | Number | `6, 1, 3` | Applies or references the 'Bleed' effect/state. |
| `BoostHeals` | Number | `2, 1` | Applies or references the 'BoostHeals' effect/state. |
| `ChanceToRevive` | [`Block`](./Items_and_Equipment.md#context-chancetorevive) | `{ ... }, 100, 25` | Applies or references the 'ChanceToRevive' effect/state. |
| `OverrideBasicAttack` | [`Enum/String`](./Enums.md#enum-overridebasicattack) | `BasicTankMelee, BasicSpin, IsaacBasicAttack` | Applies or references the 'OverrideBasicAttack' effect/state. |
| `Poison` | Number | `2, 1, 3` | Applies or references the 'Poison' effect/state. |
| `Quivered` | Number | `2, 1` | Applies or references the 'Quivered' effect/state. |
| `SpellDamageUp` | Number | `1, 3` | Applies or references the 'SpellDamageUp' effect/state. |
| `AddTag` | [`Enum/String`](./Enums.md#enum-addtag) | `rock, bug` | Applies or references the 'AddTag' effect/state. |
| `AmplifyStatus` | [`Enum/String`](./Enums.md#enum-amplifystatus) | `Bleed, Poison` | Applies or references the 'AmplifyStatus' effect/state. |
| `BreakAtAux` | Number | `0` | Applies or references the 'BreakAtAux' effect/state. |
| `DeathRattle` | [`Block`](./Items_and_Equipment.md#context-deathrattle) | `{ ... }, neck_NukeExplode` | Applies or references the 'DeathRattle' effect/state. |
| `DepressionAura` | Number | `2, 1` | Applies or references the 'DepressionAura' effect/state. |
| `DodgeChance_Status` | Number | `10, 40, 15` | Applies or references the 'DodgeChance_Status' effect/state. |
| `ExtraBasicAttacks` | Number | `2, 1` | Applies or references the 'ExtraBasicAttacks' effect/state. |
| `ExtraWeaponAttacks` | Number | `2, 1` | Applies or references the 'ExtraWeaponAttacks' effect/state. |
| `FragileDuringElement` | [`Enum/String`](./Enums.md#enum-fragileduringelement) | `water` | Applies or references the 'FragileDuringElement' effect/state. |
| `MissChance` | Number | `10` | Applies or references the 'MissChance' effect/state. |
| `PermanentMadness` | Number | `1` | Applies or references the 'PermanentMadness' effect/state. |
| `RandomSeededStatModifier` | [`Array`](./Arrays.md#array-randomseededstatmodifier) | `[ 2 -1 ]` | Applies or references the 'RandomSeededStatModifier' effect/state. |
| `SpawnObjectOnPopCorpse` | [`Block`](./Items_and_Equipment.md#context-spawnobjectonpopcorpse) | `{ ... }, Food, Coin` | Applies or references the 'SpawnObjectOnPopCorpse' effect/state. |
| `AddBonusMeleeRange` | Number | `1` | Applies or references the 'AddBonusMeleeRange' effect/state. |
| `AddElementsToBasicAttack` | [`Enum/String`](./Enums.md#enum-addelementstobasicattack) | `Holy, Electric` | Applies or references the 'AddElementsToBasicAttack' effect/state. |
| `AddEndOfCombatRegen` | Number | `12, 999999` | Applies or references the 'AddEndOfCombatRegen' effect/state. |
| `AddKnockbackDamage` | Number | `1` | Applies or references the 'AddKnockbackDamage' effect/state. |
| `AllStatsUpPerDisorder` | Number | `1` | Applies or references the 'AllStatsUpPerDisorder' effect/state. |
| `AlphaTurns` | Number | `1, -1` | Applies or references the 'AlphaTurns' effect/state. |
| `BoneArmorPassive` | Number | `1` | Applies or references the 'BoneArmorPassive' effect/state. |
| `BreakOnElement` | [`Enum/String`](./Enums.md#enum-breakonelement) | `water` | Applies or references the 'BreakOnElement' effect/state. |
| `Burn` | Number | `2` | Applies or references the 'Burn' effect/state. |
| `CantCatchDiseases` | Number | `1` | Applies or references the 'CantCatchDiseases' effect/state. |
| `CantSpreadDiseases` | Number | `1` | Applies or references the 'CantSpreadDiseases' effect/state. |
| `ChanceToBlock` | Number | `10%` | Applies or references the 'ChanceToBlock' effect/state. |
| `Confusion` | Number | `99, 2, 3` | Applies or references the 'Confusion' effect/state. |
| `CopyPassiveSlot` | Number | `1, 0` | Applies or references the 'CopyPassiveSlot' effect/state. |
| `DeathRattleRevive` | [`Enum/String`](./Enums.md#enum-deathrattlerevive) | `DoNothing, tk_PetrifiedPinky` | Applies or references the 'DeathRattleRevive' effect/state. |
| `DisableAbilities` | [`Enum/String`](./Enums.md#enum-disableabilities) | `all_items, basic_attack, all_spells` | Applies or references the 'DisableAbilities' effect/state. |
| `DropAsFamiliarOnArmorBreak` | [`Enum/String`](./Enums.md#enum-dropasfamiliaronarmorbreak) | `FaceGrubFamiliar, HeadGrubFamiliar, NeckGrubFamiliar` | Applies or references the 'DropAsFamiliarOnArmorBreak' effect/state. |
| `FaceArmorPassiveMultiplierBonus` | Number | `2, 1` | Applies or references the 'FaceArmorPassiveMultiplierBonus' effect/state. |
| `HeadArmorPassiveMultiplierBonus` | Number | `2, 1` | Applies or references the 'HeadArmorPassiveMultiplierBonus' effect/state. |
| `IncreaseExplosionSize` | Number | `7, 1` | Applies or references the 'IncreaseExplosionSize' effect/state. |
| `RockyArmorPassive` | Number | `1` | Applies or references the 'RockyArmorPassive' effect/state. |
| `TrinketActiveEffectsMultiplierBonus` | Number | `2, 1` | Applies or references the 'TrinketActiveEffectsMultiplierBonus' effect/state. |
| `TrueShot` | Number | `1` | Applies or references the 'TrueShot' effect/state. |
| `AddInitiative` | Number | `100, -20` | Applies or references the 'AddInitiative' effect/state. |
| `AmplifyKnockback` | Number | `2, 10` | Applies or references the 'AmplifyKnockback' effect/state. |
| `AutoEquipConsumables` | Number | `1` | Applies or references the 'AutoEquipConsumables' effect/state. |
| `BackstabCritChance` | Number | `1, .25` | Applies or references the 'BackstabCritChance' effect/state. |
| `BonusAbility` | [`Enum/String`](./Enums.md#enum-bonusability) | `WasteTime, neck_NukeBonus` | Applies or references the 'BonusAbility' effect/state. |
| `BreakWhenNoShield` | Number | `1` | Applies or references the 'BreakWhenNoShield' effect/state. |
| `CanLevelUpWhenDead` | Number | `1` | Applies or references the 'CanLevelUpWhenDead' effect/state. |
| `ChanceToBlockAndCounter` | [`Block`](./Items_and_Equipment.md#context-chancetoblockandcounter) | `{ ... }, 25%` | Applies or references the 'ChanceToBlockAndCounter' effect/state. |
| `DisablePassiveSlot` | Number | `1, 0` | Applies or references the 'DisablePassiveSlot' effect/state. |
| `DodgeChance` | Number | `25%, 15%` | Applies or references the 'DodgeChance' effect/state. |
| `ExtraBasicMoves_Status` | Number | `1` | Applies or references the 'ExtraBasicMoves_Status' effect/state. |
| `FindExtraItemFromPoolOnBattleEnd` | [`Enum/String`](./Enums.md#enum-findextraitemfrompoolonbattleend) | `pills, combat_reward_easy` | Applies or references the 'FindExtraItemFromPoolOnBattleEnd' effect/state. |
| `FlowersOnEndTurn` | Number | `1` | Applies or references the 'FlowersOnEndTurn' effect/state. |
| `FreezePiercing` | Number | `1` | Applies or references the 'FreezePiercing' effect/state. |
| `IncreaseExplosionDamage` | Number | `2, 1` | Applies or references the 'IncreaseExplosionDamage' effect/state. |
| `IncreaseSpellRange` | Number | `2, 20` | Applies or references the 'IncreaseSpellRange' effect/state. |
| `InjuryImmunity` | Number | `1` | Applies or references the 'InjuryImmunity' effect/state. |
| `InnateElement` | [`Enum/String`](./Enums.md#enum-innateelement) | `Fire, Ice` | Applies or references the 'InnateElement' effect/state. |
| `KillsToMeat` | [`Enum/String`](./Enums.md#enum-killstomeat) | `Food` | Applies or references the 'KillsToMeat' effect/state. |
| `KnockbackImmunity` | Number | `1` | Applies or references the 'KnockbackImmunity' effect/state. |
| `LeaveBehindOnceEachMove` | [`Enum/String`](./Enums.md#enum-leavebehindonceeachmove) | `Scrap, Poop` | Applies or references the 'LeaveBehindOnceEachMove' effect/state. |
| `LevelUpClassOverride` | [`Enum/String`](./Enums.md#enum-levelupclassoverride) | `Jester` | Applies or references the 'LevelUpClassOverride' effect/state. |
| `MoveQuivered` | Number | `2, 1` | Applies or references the 'MoveQuivered' effect/state. |
| `NeckArmorPassiveMultiplierBonus` | Number | `1` | Applies or references the 'NeckArmorPassiveMultiplierBonus' effect/state. |
| `RangedTrueShot` | Number | `1` | Applies or references the 'RangedTrueShot' effect/state. |
| `ReflectProjectiles` | Number | `20%, 25%` | Applies or references the 'ReflectProjectiles' effect/state. |
| `ReplaceBasicAttack` | [`Enum/String`](./Enums.md#enum-replacebasicattack) | `BasicPoke, head_Pestilence` | Applies or references the 'ReplaceBasicAttack' effect/state. |
| `ReplaceSpawnedObjects` | [`Array`](./Arrays.md#array-replacespawnedobjects) | `[ FlamingPoop RandomLivingPoop ], [ Poop RandomLivingPoop ]` | Applies or references the 'ReplaceSpawnedObjects' effect/state. |
| `SetDefaultFacePassive` | [`Enum/String`](./Enums.md#enum-setdefaultfacepassive) | `euphoric` | Applies or references the 'SetDefaultFacePassive' effect/state. |
| `SpawnCatCopyWhenDowned` | [`Block`](./Items_and_Equipment.md#context-spawncatcopywhendowned) | `{ ... }` |  |
| `SpawnNearEnemies` | Number | `1` | Applies or references the 'SpawnNearEnemies' effect/state. |
| `StatusOnSetPieceBreak` | [`Block`](./Items_and_Equipment.md#context-statusonsetpiecebreak) | `{ ... }` |  |
| `Uncontrollable` | Number | `1` | Applies or references the 'Uncontrollable' effect/state. |
| `UpgradeTaggedSpawnsToChampions` | [`Enum/String`](./Enums.md#enum-upgradetaggedspawnstochampions) | `worm, bug` |  |
| `AOEBonus` | Number | `1` | Applies or references the 'AOEBonus' effect/state. |
| `AbilityReaction` | [`Enum/String`](./Enums.md#enum-abilityreaction) | `head_EmoSong` | Applies or references the 'AbilityReaction' effect/state. |
| `AddConstitution` | Number | `2` |  |
| `AddCritMultiplier` | Number | `33%` | Applies or references the 'AddCritMultiplier' effect/state. |
| `AddHiddenTag` | [`Enum/String`](./Enums.md#enum-addhiddentag) | `the_nuke_bearer` | Applies or references the 'AddHiddenTag' effect/state. |
| `AddStartingMana` | Number | `5` |  |
| `AddStatusToFirstSpellEachTurn` | [`Block`](./Items_and_Equipment.md#context-addstatustofirstspelleachturn) | `{ ... }` |  |
| `AllSpellsCostCharge` | Number | `1` | Applies or references the 'AllSpellsCostCharge' effect/state. |
| `AllUnitsExplodeOnDeath` | Number | `5` | Applies or references the 'AllUnitsExplodeOnDeath' effect/state. |
| `AlliesScrambleSpellAfterCast` | Number | `1` | Applies or references the 'AlliesScrambleSpellAfterCast' effect/state. |
| `AllyDamageReduction` | Number | `0` | Applies or references the 'AllyDamageReduction' effect/state. |
| `AlphaAllStatsUp` | Number | `1` | Applies or references the 'AlphaAllStatsUp' effect/state. |
| `AlphaCat` | Number | `1` | Applies or references the 'AlphaCat' effect/state. |
| `AlwaysChosenForLevelUp` | Number | `1` | Applies or references the 'AlwaysChosenForLevelUp' effect/state. |
| `AutocastEachRound` | [`Block`](./Items_and_Equipment.md#context-autocasteachround) | `{ ... }` | Forces the character to automatically cast a specific ability at the start of each combat round. |
| `BackflipWhenTargeted` | [`Block`](./Items_and_Equipment.md#context-backflipwhentargeted) | `{ ... }` | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |
| `BackstabImmunity` | Number | `1` |  |
| `BalanceStats` | Number | `1` | Applies or references the 'BalanceStats' effect/state. |
| `BasicAttackCantMiss` | Number | `1` | Applies or references the 'BasicAttackCantMiss' effect/state. |
| `BasicAttackCritChance` | [`Enum/String`](./Enums.md#enum-basicattackcritchance) | `.1` | Applies or references the 'BasicAttackCritChance' effect/state. |
| `Blind` | Number | `-1` | Applies or references the 'Blind' effect/state. |
| `BlockDamageUnderThreshold` | Number | `1` | Applies or references the 'BlockDamageUnderThreshold' effect/state. |
| `BlockNegativeStatus` | Number | `30%` | Applies or references the 'BlockNegativeStatus' effect/state. |
| `BonusHealthRegenPerDisorder` | Number | `1` |  |
| `BoostReceivedHealing` | Number | `2` | Applies or references the 'BoostReceivedHealing' effect/state. |
| `CanRemoveCursedItems` | Number | `1` | Applies or references the 'CanRemoveCursedItems' effect/state. |
| `CapBasicAttackDamage` | Number | `1` | Applies or references the 'CapBasicAttackDamage' effect/state. |
| `CapMovementAbilityRange` | Number | `1` | Applies or references the 'CapMovementAbilityRange' effect/state. |
| `ChanceToAmbush` | Number | `25%` | Applies or references the 'ChanceToAmbush' effect/state. |
| `Charge` | Number | `5` | Applies or references the 'Charge' effect/state. |
| `CharismaIsMaxStat` | Number | `1` | Applies or references the 'CharismaIsMaxStat' effect/state. |
| `CharmImmunity` | Number | `1` | Applies or references the 'CharmImmunity' effect/state. |
| `ConsumableEffectsMultiplierBonus` | Number | `1` | Applies or references the 'ConsumableEffectsMultiplierBonus' effect/state. |
| `CounterNextAttacks` | Number | `2` | Applies or references the 'CounterNextAttacks' effect/state. |
| `CreateGlobalModifiers` | [`Block`](./Items_and_Equipment.md#context-createglobalmodifiers) | `{ ... }` | Generates global map or encounter rules/modifiers. |
| `CyborgTurns` | [`Block`](./Items_and_Equipment.md#context-cyborgturns) | `{ ... }` |  |
| `DebuffImmunity` | Number | `1` | Applies or references the 'DebuffImmunity' effect/state. |
| `DoubleCastSpellIfManaCostUnderThreshold` | Number | `3` | Applies or references the 'DoubleCastSpellIfManaCostUnderThreshold' effect/state. |
| `DoubleCastSpellsEachTurn_Status` | Number | `1` |  |
| `DoubleCastTaggedSpells` | [`Enum/String`](./Enums.md#enum-doublecasttaggedspells) | `musical` | Applies or references the 'DoubleCastTaggedSpells' effect/state. |
| `DoubleCastWeapons` | Number | `1` | Applies or references the 'DoubleCastWeapons' effect/state. |
| `DoubleReceivedNegativeStatus` | Number | `1` | Applies or references the 'DoubleReceivedNegativeStatus' effect/state. |
| `DoubleReceivedPositiveStatus` | Number | `1` | Applies or references the 'DoubleReceivedPositiveStatus' effect/state. |
| `DropAsFamiliarOnTookDamage` | [`Enum/String`](./Enums.md#enum-dropasfamiliarontookdamage) | `PhantomMaskRock` | Applies or references the 'DropAsFamiliarOnTookDamage' effect/state. |
| `DropSoulJarOnDeath` | [`Enum/String`](./Enums.md#enum-dropsouljarondeath) | `SoulJar_Full` | Applies or references the 'DropSoulJarOnDeath' effect/state. |
| `ExcludeFromEvents` | [`Enum/String`](./Enums.md#enum-excludefromevents) | `Tragedy` | Applies or references the 'ExcludeFromEvents' effect/state. |
| `ExplosionImmunity` | Number | `1` | Applies or references the 'ExplosionImmunity' effect/state. |
| `ExtraBasicAttacks_Status` | Number | `1` | Applies or references the 'ExtraBasicAttacks_Status' effect/state. |
| `ExtraMovePoints` | Number | `1` | Applies or references the 'ExtraMovePoints' effect/state. |
| `ExtraTrinketUses` | Number | `10` | Applies or references the 'ExtraTrinketUses' effect/state. |
| `FaceShield` | Number | `1` | Applies or references the 'FaceShield' effect/state. |
| `FrankBolts` | Number | `1` | Applies or references the 'FrankBolts' effect/state. |
| `GainExtraShield` | Number | `4` | Applies or references the 'GainExtraShield' effect/state. |
| `GlobalFamiliarDamageBoost` | Number | `1` |  |
| `GlobalFamiliarMoveBoost` | Number | `1` |  |
| `GlobalFlowerTrapperAura` | [`Block`](./Items_and_Equipment.md#context-globalflowertrapperaura) | `{ ... }` |  |
| `HPGainBlock` | Number | `1` | Applies or references the 'HPGainBlock' effect/state. |
| `HideSomeHudStuff` | Number | `1` | Applies or references the 'HideSomeHudStuff' effect/state. |
| `IgnoreTiles` | Number | `1` | Applies or references the 'IgnoreTiles' effect/state. |
| `JesterLevelUpRerolls` | Number | `1` | Applies or references the 'JesterLevelUpRerolls' effect/state. |
| `Lifesteal` | Number | `1` | Applies or references the 'Lifesteal' effect/state. |
| `LuckUp` | Number | `222` | Applies or references the 'LuckUp' effect/state. |
| `MakeBasicAttackPull` | Number | `1` | Applies or references the 'MakeBasicAttackPull' effect/state. |
| `MakeSpellsRequireCharge` | Number | `1` | Applies or references the 'MakeSpellsRequireCharge' effect/state. |
| `ModelingClayPassive` | Number | `1` | Applies or references the 'ModelingClayPassive' effect/state. |
| `MoveAndUseAbilityEachTurnBeginIfPossible` | [`Enum/String`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | `face_EatNeverstone` | Applies or references the 'MoveAndUseAbilityEachTurnBeginIfPossible' effect/state. |
| `MoveSpeedMultiplier` | [`Enum/String`](./Enums.md#enum-movespeedmultiplier) | `.5` | Applies or references the 'MoveSpeedMultiplier' effect/state. |
| `MoveTowardsDamageSource` | [`Enum/String`](./Enums.md#enum-movetowardsdamagesource) | `MoveOne` | Applies or references the 'MoveTowardsDamageSource' effect/state. |
| `MovementReaction` | [`Block`](./Items_and_Equipment.md#context-movementreaction) | `{ ... }` | Applies or references the 'MovementReaction' effect/state. |
| `MultiplyCoinsOnBattleStart` | Number | `2` | Applies or references the 'MultiplyCoinsOnBattleStart' effect/state. |
| `MultiplyReceivedHealing` | Number | `2` | Applies or references the 'MultiplyReceivedHealing' effect/state. |
| `OverManaReducesManaCosts` | Number | `1` |  |
| `PhysicalAttacksMiss` | Number | `1` | Applies or references the 'PhysicalAttacksMiss' effect/state. |
| `PreventSpecificInjury` | [`Enum/String`](./Enums.md#enum-preventspecificinjury) | `int` | Applies or references the 'PreventSpecificInjury' effect/state. |
| `ReclaimItemOnBreak` | Number | `1` | Applies or references the 'ReclaimItemOnBreak' effect/state. |
| `ReduceManaCost` | Number | `2` | Applies or references the 'ReduceManaCost' effect/state. |
| `ReduceSpellCostsPerDisorder` | Number | `1` | Applies or references the 'ReduceSpellCostsPerDisorder' effect/state. |
| `ReduceSpellCostsPerParasite` | Number | `1` | Applies or references the 'ReduceSpellCostsPerParasite' effect/state. |
| `RemoveLineOfSightRestrictions` | Number | `1` | Applies or references the 'RemoveLineOfSightRestrictions' effect/state. |
| `ReplaceBlankTilesOnBattleStart` | [`Enum/String`](./Enums.md#enum-replaceblanktilesonbattlestart) | `GlassTile` | Applies or references the 'ReplaceBlankTilesOnBattleStart' effect/state. |
| `RerollItemsOnBattleEnd` | Number | `1` | Applies or references the 'RerollItemsOnBattleEnd' effect/state. |
| `Robot` | [`Block`](./Items_and_Equipment.md#context-robot) | `{ ... }` |  |
| `RockyArmorSalvage` | [`Enum/String`](./Enums.md#enum-rockyarmorsalvage) | `.75` |  |
| `SetFaction` | [`Enum/String`](./Enums.md#enum-setfaction) | `enemies` | Applies or references the 'SetFaction' effect/state. |
| `SetSpellCosts` | Number | `0` | Applies or references the 'SetSpellCosts' effect/state. |
| `SharkySmellsBlood` | Number | `1` | Applies or references the 'SharkySmellsBlood' effect/state. |
| `SpawnCatCloneOnCorpsePopped` | Number | `1` | Applies or references the 'SpawnCatCloneOnCorpsePopped' effect/state. |
| `SpawnCatCopyOnBattleStart` | [`Block`](./Items_and_Equipment.md#context-spawncatcopyonbattlestart) | `{ ... }` |  |
| `SpawnOnDowned` | [`Enum/String`](./Enums.md#enum-spawnondowned) | `CharmedSpookie` | Applies or references the 'SpawnOnDowned' effect/state. |
| `StatusOnEatPill` | [`Block`](./Items_and_Equipment.md#context-statusoneatpill) | `{ ... }` |  |
| `StatusOnTurnEndIfCastNSpells` | [`Block`](./Items_and_Equipment.md#context-statusonturnendifcastnspells) | `{ ... }` |  |
| `StevenBolts` | Number | `1` | Applies or references the 'StevenBolts' effect/state. |
| `StripKnockback` | Number | `1` | Applies or references the 'StripKnockback' effect/state. |
| `TauntAlways` | Number | `1` | Applies or references the 'TauntAlways' effect/state. |
| `TriggerBleedOnBleed` | Number | `1` |  |
| `Undead` | Number | `1` | Applies or references the 'Undead' effect/state. |
| `UpgradeSpawnedPickups` | Number | `1` |  |
| `WeaponActiveEffectsMultiplierBonus` | Number | `2` |  |
| `WeaponDamageMultiplierBonus` | Number | `1` | Applies or references the 'WeaponDamageMultiplierBonus' effect/state. |
| `WeaponPassiveMultiplierBonus` | Number | `2` |  |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `Knockback` | Number | `2, 1` | Applies or references the 'Knockback' effect/state. |
| `Poison` | Number | `2, 1` | Applies or references the 'Poison' effect/state. |
| `Burn` | Number | `1` | Applies or references the 'Burn' effect/state. |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1 .1 ], [ 1 .15 ], [ 1, .25 ]` | Applies or references the 'Fear' effect/state. |
| `Slow` | Number | `1` | Applies or references the 'Slow' effect/state. |
| `Tangled` | [`Array`](./Arrays.md#array-tangled) | `[ 1, .05 ], [ 1, .33 ]` | Applies a tangled/ensnared status effect, often modifying visual sprites. |
| `ChangeTile` | [`Enum/String`](./Enums.md#enum-changetile) | `TallGrassTile, GlassTile, BrambleTile` | Transforms the terrain tile under the target. |
| `DamageOrHealConditionally` | Number | `1` | Applies or references the 'DamageOrHealConditionally' effect/state. |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |
| `Rot` | Number | `1` | Applies or references the 'Rot' effect/state. |
| `SpiderInfested` | Number | `1` | Applies or references the 'SpiderInfested' effect/state. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .1 ], [ 1, .1 ]` | Applies or references the 'Stun' effect/state. |
| `Weakness` | Number | `1, 3` | Applies or references the 'Weakness' effect/state. |
| `Blind` | Number | `1` | Applies or references the 'Blind' effect/state. |
| `Freeze` | [`Array`](./Arrays.md#array-freeze) | `[ 1 .1 ]` | Applies or references the 'Freeze' effect/state. |
| `KnockOutCoin` | Number | `1` | Forces the target to drop coins. |
| `Leech` | Number | `1` | Applies or references the 'Leech' effect/state. |
| `Leeches` | Number | `1` | Applies or references the 'Leeches' effect/state. |
| `MagicWeakness` | Number | `1` | Applies or references the 'MagicWeakness' effect/state. |
| `ManaLeeches` | Number | `1` | Applies or references the 'ManaLeeches' effect/state. |
| `Marked` | Number | `1` | Applies or references the 'Marked' effect/state. |
| `OverrideChainKnockback` | Number | `1` | Applies or references the 'OverrideChainKnockback' effect/state. |
| `PullSourceToTarget` | Number | `1` | Applies or references the 'PullSourceToTarget' effect/state. |
| `SoulLink` | Number | `1` | Applies or references the 'SoulLink' effect/state. |

</details>

---

### Context: `effects`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `BounceObject` | [`Enum/String`](./Enums.md#enum-bounceobject) | `RandomPickup, CharmedDip` | Spawns a physics object that visually bounces off the target. |
| `Burn` | Number | `1` | Applies or references the 'Burn' effect/state. |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1, .5 ], [ 1, .25 ], [ 1, .15 ]` | Applies or references the 'Fear' effect/state. |
| `Grappled` | [`Array`](./Arrays.md#array-grappled) | `[ 1, .50 ], [ 1, .75 ]` | Applies or references the 'Grappled' effect/state. |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |
| `Slow` | Number | `1` | Applies or references the 'Slow' effect/state. |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1, .1 ], [ 1, .25 ]` | Applies or references the 'Stun' effect/state. |
| `Blind` | Number | `1` | Applies or references the 'Blind' effect/state. |
| `Cleave` | Number | `1` | Causes the attack to hit adjacent enemies alongside the primary target. |
| `Confusion` | Number | `2` | Applies or references the 'Confusion' effect/state. |
| `Freeze` | [`Array`](./Arrays.md#array-freeze) | `[ 1, .25 ]` | Applies or references the 'Freeze' effect/state. |
| `VisualFX` | [`Enum/String`](./Enums.md#enum-visualfx) | `Bolt` | Applies or references the 'VisualFX' effect/state. |
| `VisualFXTile` | [`Enum/String`](./Enums.md#enum-visualfxtile) | `WaterConduct` | Applies or references the 'VisualFXTile' effect/state. |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | `true` | If true, triggers the effect even if the character died during the battle. |
| `RandomPermanentStat` | Number | `-1, 1, -3` | Applies or references the 'RandomPermanentStat' effect/state. |
| `RandomMutation` | Number | `1` | Applies or references the 'RandomMutation' effect/state. |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `pills, chapter_specific_item, common_bones` | Generates an item drop from the specified loot pool. |
| `GainCoins` | Number | `1, [ 3 5 ]` | Applies or references the 'GainCoins' effect/state. |
| `RepairTrinket` | Number | `99` | Applies or references the 'RepairTrinket' effect/state. |
| `SetItemAux` | [`Block`](./Items_and_Equipment.md#context-setitemaux) | `{ ... }` | Applies or references the 'SetItemAux' effect/state. |
| `FindItem` | [`Enum/String`](./Enums.md#enum-finditem) | `BoneClub` |  |
| `GainCoinsRange` | [`Block`](./Items_and_Equipment.md#context-gaincoinsrange) | `{ ... }` |  |
| `PermanentConstitution` | Number | `-1` | Applies or references the 'PermanentConstitution' effect/state. |
| `PermanentIntelligence` | Number | `-1` | Applies or references the 'PermanentIntelligence' effect/state. |
| `RepairAll` | Number | `1` | Applies or references the 'RepairAll' effect/state. |
| `RepairWeapon` | Number | `6` | Applies or references the 'RepairWeapon' effect/state. |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `odds` | Number | `1%, 10%, 15%` | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |
| `Freeze` | Number | `1` | Applies or references the 'Freeze' effect/state. |
| `ForceUseAbility_NonStack` | [`Enum/String`](./Enums.md#enum-forceuseability_nonstack) | `Endeavor_Auto` | Applies or references the 'ForceUseAbility_NonStack' effect/state. |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `consumables, parasites` | Generates an item drop from the specified loot pool. |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `tk_WeirdEgg_Spawn, tk_Asteroid, cm_RaptorEggSpawn` | Applies or references the 'ForceUseAbility' effect/state. |
| `RandomMutation` | Number | `1` | Applies or references the 'RandomMutation' effect/state. |
| `DestroyTrinket` | Number | `1` | Applies or references the 'DestroyTrinket' effect/state. |

</details>

---

### Context: `SpawnOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Food, CharmedPinky, CharmedTinyTumor` |  |
| `number` | Number | `1, [ 1, 3 ], 4` |  |

</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Array`](./Arrays.md#array-object) | `[ CharmedFly CharmedMaggot ], CharmedAmoeba, CharmedFlea` |  |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.2, 5%, 100%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `stack_key` | [`Enum/String`](./Enums.md#enum-stack_key) | `CATHIDE` |  |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `tk_SuckStone, head_HitlersToupe, tk_JarOfRadiation` | Applies or references the 'ForceUseAbility' effect/state. |
| `PartialCleanse` | Number | `1` | Applies or references the 'PartialCleanse' effect/state. |
| `Shield` | Number | `2, 1, 3` | Applies or references the 'Shield' effect/state. |
| `ImmediateUseAbility` | [`Block`](./Items_and_Equipment.md#context-immediateuseability) | `{ ... }, head_ThrobbingCrown` | Applies or references the 'ImmediateUseAbility' effect/state. |
| `SpawnCoinAnywhere` | Number | `1` | Applies or references the 'SpawnCoinAnywhere' effect/state. |
| `AddWeaponAux` | Number | `1` | Applies or references the 'AddWeaponAux' effect/state. |
| `Burn` | Number | `3` | Applies or references the 'Burn' effect/state. |
| `Cleanse` | Number | `0` |  |
| `Conditional_HasCleansableDebuffs` | [`Block`](./Items_and_Equipment.md#context-conditional_hascleansabledebuffs) | `{ ... }` |  |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `PreEmptiveCounterNextAttacks` | Number | `1` | Applies or references the 'PreEmptiveCounterNextAttacks' effect/state. |
| `RandomStatUp` | Number | `3` |  |
| `Stealth` | [`Array`](./Arrays.md#array-stealth) | `[ 1 .1 ]` | Applies or references the 'Stealth' effect/state. |

</details>

---

### Context: `StatusOnBreak`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `3` | Applies or references the 'Bruise' effect/state. |
| `ChangeTilesUnder` | [`Enum/String`](./Enums.md#enum-changetilesunder) | `WaterTile` | Applies or references the 'ChangeTilesUnder' effect/state. |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `common` | Generates an item drop from the specified loot pool. |
| `HealthGain` | Number | `10` | Applies or references the 'HealthGain' effect/state. |
| `HealthRegenUp` | Number | `3` | Applies or references the 'HealthRegenUp' effect/state. |
| `PermanentConstitution` | Number | `2` | Applies or references the 'PermanentConstitution' effect/state. |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `DexterityUp` | Number | `1` | Applies or references the 'DexterityUp' effect/state. |
| `FindItem` | [`Enum/String`](./Enums.md#enum-finditem) | `Pearl` | Applies or references the 'FindItem' effect/state. |
| `GainDisorder` | [`Enum/String`](./Enums.md#enum-gaindisorder) | `Psychosis` | Applies or references the 'GainDisorder' effect/state. |
| `IntelligenceUp` | Number | `1` | Applies or references the 'IntelligenceUp' effect/state. |
| `ObjectOnHitCharacter` | [`Enum/String`](./Enums.md#enum-objectonhitcharacter) | `BestBud` | Spawns a specific character or entity upon impact. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Scrap, Catnip, CharmedTinySpider` |  |
| `good` | Boolean | `false` |  |
| `shield_only` | Boolean | `true` |  |
| `spawn_on_death_hit` | Boolean | `false` |  |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.25` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `number` | Number | `1` |  |

</details>

---

### Context: `Temporary`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `2, 1, 3` | Number of stacks or intensity to apply. |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Brace, FreeSpell, SpeedUp` | The status effect to apply. |
| `expires_on_end_turn` | Boolean | `true` |  |
| `turns` | Number | `1` | Duration in turns. |
| `expires_on_begin_turn` | Boolean | `true` | If true, ticks down at the start of the turn rather than the end. |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `BrittleCharismaUp` | Number | `2` | Applies or references the 'BrittleCharismaUp' effect/state. |
| `BrittleConstitutionUp` | Number | `2` | Applies or references the 'BrittleConstitutionUp' effect/state. |
| `BrittleDexterityUp` | Number | `2` | Applies or references the 'BrittleDexterityUp' effect/state. |
| `BrittleIntelligenceUp` | Number | `2` | Applies or references the 'BrittleIntelligenceUp' effect/state. |
| `BrittleLuckUp` | Number | `2` | Applies or references the 'BrittleLuckUp' effect/state. |
| `BrittleSpeedUp` | Number | `2` | Applies or references the 'BrittleSpeedUp' effect/state. |
| `BrittleStrengthUp` | Number | `2` | Applies or references the 'BrittleStrengthUp' effect/state. |
| `CharismaUp` | Number | `1` | Applies or references the 'CharismaUp' effect/state. |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `DexterityUp` | Number | `1` | Applies or references the 'DexterityUp' effect/state. |
| `EquipPermanentItem` | [`Enum/String`](./Enums.md#enum-equippermanentitem) | `BoneClub` | Applies or references the 'EquipPermanentItem' effect/state. |
| `HealthGain` | Number | `5` | Applies or references the 'HealthGain' effect/state. |
| `HealthRegenUp` | Number | `1` | Applies or references the 'HealthRegenUp' effect/state. |
| `IntelligenceUp` | Number | `1` | Applies or references the 'IntelligenceUp' effect/state. |
| `LuckUp` | Number | `1` | Applies or references the 'LuckUp' effect/state. |
| `Shield` | Number | `6` |  |
| `SpeedUp` | Number | `1` | Applies or references the 'SpeedUp' effect/state. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |

</details>

---

### Context: `AddPassivesToMinions`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `2, 5, 4` | Applies or references the 'HealthGain' effect/state. |
| `AddMaxHealth` | Number | `2, 5, 4` | Applies or references the 'AddMaxHealth' effect/state. |
| `DamageUp` | Number | `2, 1` |  |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `Buddy` | [`Enum/String`](./Enums.md#enum-buddy) | `spawner` |  |
| `ReturnBoundItemOnBattleEnd` | Number | `1` |  |
| `Shield` | Number | `2` | Applies or references the 'Shield' effect/state. |
| `tag_filter` | [`Enum/String`](./Enums.md#enum-tag_filter) | `grub_familiar` |  |

</details>

---

### Context: `DurabilityTransform`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `eq` | [`Array`](./Arrays.md#array-eq) | `[ 1 WaterBottle_Half ], [ 0 JarOfNothing ], [ 0 WaterBottle_Empty ]` |  |
| `ge` | [`Array`](./Arrays.md#array-ge) | `[ 3 EstusFlask_Full ], [ 2 WaterBottle_Full ]` |  |

</details>

---

### Context: `TransformItemOnElementInfluence`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Greater_Water, Fire` | Specific element type required or applied. |
| `full_repair` | Boolean | `true` |  |
| `item` | [`Enum/String`](./Enums.md#enum-item) | `EstusFlask_Full, WaterBottle_Full, GallonOfWater` | Item ID to reference. |

</details>

---

### Context: `GainCoinsRange`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `max` | Number | `30, 60, 25` | Maximum coins granted. |
| `min` | Number | `30, 1, 15` | Minimum coins granted. |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | `2, 1, 10` |  |
| `damage` | Number | `0` | The base damage properties of an attack. |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `2, 1` | Applies or references the 'Charge' effect/state. |
| `Thorns` | Number | `1` | Applies or references the 'Thorns' effect/state. |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `DamageUp` | Number | `2` | Applies or references the 'DamageUp' effect/state. |
| `DivineShield` | [`Array`](./Arrays.md#array-divineshield) | `[ 1, .33 ]` | Applies or references the 'DivineShield' effect/state. |
| `DodgeChance_Status` | Number | `5` | Applies or references the 'DodgeChance_Status' effect/state. |
| `RandomStatUp` | Number | `1` |  |
| `RemoveStatus` | [`Enum/String`](./Enums.md#enum-removestatus) | `AlphaCat` | Applies or references the 'RemoveStatus' effect/state. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |

</details>

---

### Context: `Craft`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `bombs, tinkerer_default` |  |
| `slot` | [`Enum/String`](./Enums.md#enum-slot) | `weapon` | Equipment slot (weapon, hat, face, chest, etc.). |
| `works_with_tech` | Boolean | `true` |  |

</details>

---

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `move, spell, attack` | Classification type. |
| `AllStatsUp` | Number | `1` |  |
| `Charge` | Number | `1` | Applies or references the 'Charge' effect/state. |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `HealthRegenUp` | Number | `1` | Applies or references the 'HealthRegenUp' effect/state. |
| `Shield` | Number | `1` | Applies or references the 'Shield' effect/state. |
| `SpellDamageUp` | Number | `1` | Applies or references the 'SpellDamageUp' effect/state. |
| `Thorns` | Number | `1` | Applies or references the 'Thorns' effect/state. |

</details>

---

### Context: `DelayedAutoRevive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `health` | Number | `50%, 30%, 15%` |  |
| `rounds` | Number | `2, 1` |  |

</details>

---

### Context: `PassiveAtHealthThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `mode` | [`Enum/String`](./Enums.md#enum-mode) | `less_or_equal, greater, equal` |  |
| `threshold` | Number | `10, 1, 5` |  |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `number` | [`Array`](./Arrays.md#array-number) | `2, [ 3 6 ], [ 0 1 ]` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `RandomPickup, Bird, Coin` |  |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `BlessingOfPeace` | Number | `1` | Applies or references the 'BlessingOfPeace' effect/state. |
| `Burn` | Number | `1` | Applies or references the 'Burn' effect/state. |
| `DestroyTrinket` | Number | `1` | Applies or references the 'DestroyTrinket' effect/state. |
| `DoubleCastSpellThisTurn` | Number | `1` | Applies or references the 'DoubleCastSpellThisTurn' effect/state. |
| `DrinkWater` | Number | `1` | Applies or references the 'DrinkWater' effect/state. |
| `Revive` | Number | `1` | Applies or references the 'Revive' effect/state. |
| `SpeedUp` | Number | `2` | Applies or references the 'SpeedUp' effect/state. |
| `Temporary` | [`Block`](./Items_and_Equipment.md#context-temporary) | `{ ... }` | A wrapper block for applying status effects that automatically expire. |
| `UseAbility` | [`Enum/String`](./Enums.md#enum-useability) | `neck_DarkFriend` | Forces the character or target to instantly use a specified ability. |
| `Wet` | Number | `1` | Applies or references the 'Wet' effect/state. |

</details>

---

### Context: `CatchProjectiles`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | `1` | Applies or references the 'Quivered' effect/state. |
| `ally_chance` | Number | `15%` |  |
| `chance` | Number | `15%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

### Context: `ItemAuxTransform`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `le` | [`Array`](./Arrays.md#array-le) | `[ 50 MoneyBag_Large ], [ 10 MoneyBag_Small ], [ 25 MoneyBag_Medium ]` |  |
| `ge` | [`Array`](./Arrays.md#array-ge) | `[ 20 BlackShard_Glowing ], [ 10 NuclearKnife_Glowing ]` |  |
| `lt` | [`Array`](./Arrays.md#array-lt) | `[ 10 NuclearKnife ]` |  |

</details>

---

### Context: `StatusAlliesOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | `2, 1` | Applies or references the 'SpeedUp' effect/state. |
| `Brace` | Number | `1` | Applies or references the 'Brace' effect/state. |
| `ConstitutionUp` | Number | `1` | Applies or references the 'ConstitutionUp' effect/state. |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `IntelligenceUp` | Number | `1` |  |
| `LuckUp` | Number | `1` |  |
| `Shield` | Number | `5` |  |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |

</details>

---

### Context: `StatusOnSetPieceBreak`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `rare` |  |
| `PermanentCharisma` | Number | `1` |  |
| `PermanentConstitution` | Number | `1` |  |
| `PermanentDexterity` | Number | `1` |  |
| `PermanentIntelligence` | Number | `1` |  |
| `PermanentLuck` | Number | `1` |  |
| `PermanentSpeed` | Number | `1` |  |
| `PermanentStrength` | Number | `1` |  |
| `set` | [`Enum/String`](./Enums.md#enum-set) | `Recycled` |  |

</details>

---

### Context: `AddDamageToElementDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `2, 1` | The base damage properties of an attack. |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Electric, Fire, Ice` | Specific element type required or applied. |

</details>

---

### Context: `AddSelfStatusToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `2, 1, 3` | Fires a randomized number of magic missiles. |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `DustDash` | Applies or references the 'ForceUseAbility' effect/state. |
| `Quivered` | [`Array`](./Arrays.md#array-quivered) | `[ 1 .10 ]` | Applies or references the 'Quivered' effect/state. |
| `Shield` | Number | `1` | Applies or references the 'Shield' effect/state. |

</details>

---

### Context: `StatusOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SafeDie` | Number | `1` | Applies or references the 'SafeDie' effect/state. |
| `Brace` | [`Enum/String`](./Enums.md#enum-brace) | `item_aux` | Applies or references the 'Brace' effect/state. |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `common` | Generates an item drop from the specified loot pool. |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `tk_DybbuksRib` | Applies or references the 'ForceUseAbility' effect/state. |
| `RandomMagicMissile` | Number | `4` | Fires a randomized number of magic missiles. |
| `SetHealth` | Number | `50%` | Applies or references the 'SetHealth' effect/state. |
| `StealthUntilBasicAttack` | Number | `1` | Applies or references the 'StealthUntilBasicAttack' effect/state. |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `2` | Applies or references the 'Charge' effect/state. |
| `SpeedUp` | Number | `1` | Applies or references the 'SpeedUp' effect/state. |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `ImmediateUseAbility` | [`Enum/String`](./Enums.md#enum-immediateuseability) | `head_MagnetoAttract` | Applies or references the 'ImmediateUseAbility' effect/state. |

</details>

---

### Context: `StatusOnKillEnemy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `Brace` | Number | `1` | Applies or references the 'Brace' effect/state. |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `head_CatChestPound` | Applies or references the 'ForceUseAbility' effect/state. |
| `LuckUp` | Number | `1` | Applies or references the 'LuckUp' effect/state. |
| `ManaGain` | Number | `2` | Applies or references the 'ManaGain' effect/state. |

</details>

---

### Context: `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `99, 1` | Quantity. |
| `Charmed` | Number | `2` | Applies or references the 'Charmed' effect/state. |
| `Confusion` | Number | `2` | Applies or references the 'Confusion' effect/state. |
| `Fear` | Number | `2` | Applies or references the 'Fear' effect/state. |
| `Freeze` | Number | `2` | Applies or references the 'Freeze' effect/state. |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `Charge` | Number | `1, 3` | Applies or references the 'Charge' effect/state. |
| `HealthGain` | Number | `3` | Applies or references the 'HealthGain' effect/state. |
| `SpeedUp` | Number | `1` | Applies or references the 'SpeedUp' effect/state. |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `reduction` | Number | `2, 1` |  |
| `class` | [`Enum/String`](./Enums.md#enum-class) | `Colorless` | Character class identifier. |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `wp_Blackjack_Auto, wp_ZodiacsSixshooter_Auto` | ID of the ability to trigger or reference. |
| `create_temp_ability` | Boolean | `true` |  |
| `enemies_only` | Boolean | `true` |  |
| `on_self_move_too` | Boolean | `true` |  |

</details>

---

### Context: `PassiveIfStrAuxEquals`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `value` | [`Enum/String`](./Enums.md#enum-value) | `dex, str, con` |  |

</details>

---

### Context: `PassiveWhenOnTile`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tile` | [`Array`](./Arrays.md#array-tile) | `[ WaterTile ], [ TallGrassTile TallFlowerTile ]` |  |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `PermanentCharisma` | Number | `1` | Applies or references the 'PermanentCharisma' effect/state. |
| `PermanentConstitution` | Number | `1` | Applies or references the 'PermanentConstitution' effect/state. |
| `PermanentDexterity` | Number | `1` | Applies or references the 'PermanentDexterity' effect/state. |
| `PermanentIntelligence` | Number | `1` | Applies or references the 'PermanentIntelligence' effect/state. |
| `PermanentLuck` | Number | `1` | Applies or references the 'PermanentLuck' effect/state. |
| `PermanentSpeed` | Number | `1` | Applies or references the 'PermanentSpeed' effect/state. |
| `PermanentStrength` | Number | `1` | Applies or references the 'PermanentStrength' effect/state. |

</details>

---

### Context: `StatusAfterXStacks`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stack_key` | [`Enum/String`](./Enums.md#enum-stack_key) | `FANNY_PACK, EMPTY_GENERATOR` |  |
| `threshold` | Number | `12, 3` |  |
| `ExtraBasicMoves_Status` | Number | `1` | Applies or references the 'ExtraBasicMoves_Status' effect/state. |
| `RefreshActPoints` | Number | `1` | Applies or references the 'RefreshActPoints' effect/state. |
| `expires_on_end_turn` | Boolean | `true` |  |

</details>

---

### Context: `Conditional_HasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Thorns, Bleed` | The specific status effect ID to remove. |
| `FlatLeechIfDamaged` | Number | `3` | Applies or references the 'FlatLeechIfDamaged' effect/state. |
| `ImmediateUseAbility_Instant` | [`Enum/String`](./Enums.md#enum-immediateuseability_instant) | `head_CrownOfHorns` | Applies or references the 'ImmediateUseAbility_Instant' effect/state. |

</details>

---

### Context: `DeathRattle`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `set_HumanFleshSetCurse, set_MummySetCurse, MiniNukeExplodey` |  |
| `pop_corpse` | Boolean | `false` |  |

</details>

---

### Context: `DoDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0` | The flat damage amount. |
| `damage_tiles` | [`Enum/String`](./Enums.md#enum-damage_tiles) | `all` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` | The classification of the damage (e.g., spell, melee). |

</details>

---

### Context: `SetItemAux`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `slot` | [`Enum/String`](./Enums.md#enum-slot) | `face, trinket, head` | Equipment slot (weapon, hat, face, chest, etc.). |
| `value` | [`Enum/String`](./Enums.md#enum-value) | `item_aux-1, item_aux+1, item_aux+2` |  |

</details>

---

### Context: `SpawnExtraThingsOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `number` | Number | `3, [ 1 2 ]` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `RandomPickup` |  |

</details>

---

### Context: `StackingFlowerTrail`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stack_key` | [`Enum/String`](./Enums.md#enum-stack_key) | `FLOWER_SET` |  |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `AbilityHealthThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `cm_HealPercent_Auto` | ID of the ability to trigger or reference. |
| `aux` | Number | `25` |  |
| `even_if_stunned` | Boolean | `true` |  |
| `immediate` | Boolean | `true` |  |
| `threshold` | [`Equation`](./Enums.md#enum-mathequation) | `"max(X*.5, 1)"` |  |

</details>

---

### Context: `AddStatusToAllDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `must_do_damage` | Boolean | `true` |  |
| `BonusKnockbackDamage` | Number | `3` | Applies or references the 'BonusKnockbackDamage' effect/state. |
| `Rot` | Number | `1` | Applies or references the 'Rot' effect/state. |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `rock, humanoid` | The specific string tag to check for. |
| `BonusCritChance` | Number | `50` |  |
| `BonusKnockbackDamage` | Number | `5` | Applies or references the 'BonusKnockbackDamage' effect/state. |
| `OverrideChainKnockback` | Number | `0` | Applies or references the 'OverrideChainKnockback' effect/state. |

</details>

---

### Context: `Conditional_OncePerBattle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ReduceManaCost` | Number | `1` | Applies or references the 'ReduceManaCost' effect/state. |
| `Shield` | Number | `3` | Applies or references the 'Shield' effect/state. |
| `ShowText` | String | `"COMBAT_POPUP_BRAINSTORM"` | Applies or references the 'ShowText' effect/state. |
| `SpellDamageUp` | Number | `1` | Applies or references the 'SpellDamageUp' effect/state. |
| `key` | [`Enum/String`](./Enums.md#enum-key) | `JewelOfDrog` |  |

</details>

---

### Context: `CounterAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `head_IronJaw, attack, neck_TentacleArmorCounter` | ID of the ability to trigger or reference. |
| `melee_only` | Boolean | `true` |  |
| `ranged_only` | Boolean | `true` |  |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0, 1` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Electric ]` |  |

</details>

---

### Context: `StatusEveryXSpellCasts`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `3, 4` | Number of stacks or intensity to apply. |
| `Charge` | Number | `3` | Applies or references the 'Charge' effect/state. |
| `IntelligenceUp` | Number | `2` | Applies or references the 'IntelligenceUp' effect/state. |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `3` | Applies or references the 'Charge' effect/state. |
| `HealthGain` | Number | `3` | Applies or references the 'HealthGain' effect/state. |
| `DivineShield` | Number | `1` |  |

</details>

---

### Context: `AddStatusToElementDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Electric, Fire` | Specific element type required or applied. |
| `Burn` | Number | `1` | Applies or references the 'Burn' effect/state. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .1 ]` | Applies or references the 'Stun' effect/state. |

</details>

---

### Context: `ArmorBreakOnHit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance_to_break` | Number | `5%, 10%` |  |
| `durability_loss` | Number | `0` |  |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `set_PlanetSetGravity, face_StevenMask2` | The ID of the ability to autocast. |
| `even_if_stunned` | Boolean | `true` | If true, bypasses stun and hard-CC restrictions to cast anyway. |

</details>

---

### Context: `BoostWeaponDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `crit_chance` | [`Enum/String`](./Enums.md#enum-crit_chance) | `.5, 1` |  |
| `damage` | Number | `0` | The base damage properties of an attack. |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `ShadowstepDodge, BlinkDodge` | ID of the ability to trigger or reference. |
| `chance` | Number | `33%, 10%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

### Context: `ChanceToRevive`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `health` | Number | `50%, 34%` |  |
| `stacks` | Number | `100, 50` | Number of stacks or intensity to apply. |

</details>

---

### Context: `ElementalManaCostReduction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Array`](./Arrays.md#array-element) | `[ Holy ], [ Fire Earth ]` | Specific element type required or applied. |
| `reduction` | Number | `1` |  |

</details>

---

### Context: `ObjectOnHitCharacter`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CharmedLeech, CharmedTinySpider` | The entity ID of the character to spawn (e.g., CharmedFlea). |
| `stacks` | Number | `1, "floor(lck/4)"` | Number of stacks or intensity to apply. |

</details>

---

### Context: `RefreshEquipmentAbilityOnElement`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Electric` | Specific element type required or applied. |
| `text` | String | `"COMBAT_POPUP_RECHARGED"` |  |

</details>

---

### Context: `SpawnCatCopyWhenDowned`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `PlayerCat_AncestralShade, PlayerCat_NecroShade` |  |
| `prevent_chain_tag` | [`Enum/String`](./Enums.md#enum-prevent_chain_tag) | `ancestorset_shade, necroset_shade` |  |

</details>

---

### Context: `SpawnItemLinkedFamiliar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean | `true` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `ZaratanaFamiliar, PyrophinaFamiliar` |  |

</details>

---

### Context: `cost`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `charge` | Number | `1` |  |
| `mana` | Number | `0` |  |

</details>

---

### Context: `global_passives`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `GlobalEnemyAutoRevive` | Number | `100%, 30%` | Applies or references the 'GlobalEnemyAutoRevive' effect/state. |
| `NoCorpses` | Number | `1` | Applies or references the 'NoCorpses' effect/state. |
| `RealTimePressure` | Number | `5` | Applies or references the 'RealTimePressure' effect/state. |

</details>

---

### Context: `meta`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `is_basic_attack` | Boolean | `false` |  |
| `is_weapon` | Boolean | `true` |  |

</details>

---

### Context: `AddAdvantageToEvent`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `add` | Number | `5` |  |
| `options` | [`Array`](./Arrays.md#array-options) | `[ smash bash open ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `treasure_box` | Classification type. |

</details>

---

### Context: `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bounty` | Number | `1` | Applies or references the 'Bounty' effect/state. |
| `Marked` | Number | `1` | Applies or references the 'Marked' effect/state. |
| `count` | Number | `1` | Quantity. |

</details>

---

### Context: `Conditional_PartyMember`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_IsSelf` | [`Block`](./Abilities_and_Spells.md#context-conditional_isself) | `{ ... }` | Conditional trigger: Executes nested logic if the target is the caster themselves. |

</details>

---

### Context: `PassiveAtStatThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `mode` | [`Enum/String`](./Enums.md#enum-mode) | `less_or_equal` |  |

</details>

---

### Context: `SpawnObjectOnPopCorpse`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `2` | Quantity. |
| `except_tiny` | Boolean | `true` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CharmedTinySpider` |  |

</details>

---

### Context: `StatusAfterCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TempMeleeRangeUp` | Number | `1` | Applies or references the 'TempMeleeRangeUp' effect/state. |
| `TempRangeUp` | Number | `1` | Applies or references the 'TempRangeUp' effect/state. |
| `UseAbility` | [`Enum/String`](./Enums.md#enum-useability) | `neck_DarkFriend` | Forces the character or target to instantly use a specified ability. |

</details>

---

### Context: `StatusOnFallAsleep`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `FillMana` | Number | `1` | Applies or references the 'FillMana' effect/state. |
| `HealRandomInjury` | Number | `1` | Applies or references the 'HealRandomInjury' effect/state. |

</details>

---

### Context: `StatusOnPopCorpse`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `5` | Applies or references the 'HealthGain' effect/state. |
| `RepairTrinket` | Number | `1` | Applies or references the 'RepairTrinket' effect/state. |
| `RepairWeapon` | Number | `1` | Applies or references the 'RepairWeapon' effect/state. |

</details>

---

### Context: `StatusOnTakeHealthOrShieldDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | [`Array`](./Arrays.md#array-divineshield) | `[ 1 .33 ], [ 1 .5 ]` | Applies or references the 'DivineShield' effect/state. |
| `Metronome` | Number | `1` | Executes a random musical or metronome ability. |

</details>

---

### Context: `TintItem`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `add` | [`Array`](./Arrays.md#array-add) | `[ 0.05 0.05 0.05 ]` |  |
| `ignore_if_str_aux_equals` | [`Enum/String`](./Enums.md#enum-ignore_if_str_aux_equals) | `ModelingClay_Default` |  |
| `mul` | [`Array`](./Arrays.md#array-mul) | `[ 0.45 0.3 0.25 ]` |  |

</details>

---

### Context: `threshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `1, 0` |  |
| `con` | Number | `0` |  |

</details>

---

### Context: `AIControlNextTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | `true` |  |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `AbilityOnRoundEndOnce`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `wp_SignalAmplifierSpawnTerminator` | ID of the ability to trigger or reference. |
| `even_of_stunned` | Boolean | `true` |  |

</details>

---

### Context: `AddStatusToFirstSpellEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Conditional_IsSelf` | [`Block`](./Abilities_and_Spells.md#context-conditional_isself) | `{ ... }` |  |
| `Else` | [`Block`](./Items_and_Equipment.md#context-else) | `{ ... }` |  |

</details>

---

### Context: `AddStatusToKnockbackDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1, .1 ]` | Applies or references the 'Stun' effect/state. |

</details>

---

### Context: `AllyDodgeChanceAura`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `25%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `range` | Number | `1` | Distance or area of effect in tiles. |

</details>

---

### Context: `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `GainDisorderFromPool` | [`Enum/String`](./Enums.md#enum-gaindisorderfrompool) | `all_disorders` | Applies or references the 'GainDisorderFromPool' effect/state. |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `BackflipDodge` | The specific dodge ability to trigger (e.g., DestroyerDodge). |
| `stacks` | Number | `2` | Number of stacks or intensity to apply. |

</details>

---

### Context: `BouncyProjectiles`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number | `1` |  |
| `max_range` | Number | `2` |  |

</details>

---

### Context: `CastAgainWithStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | Number | `1` | Applies or references the 'OverrideDamage' effect/state. |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `ChanceToBlockAndCounter`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean | `true` |  |
| `chance` | Number | `100%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

### Context: `ChanceToForceEvent`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `25%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `event` | [`Enum/String`](./Enums.md#enum-event) | `Blessing` |  |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `odds` | [`Enum/String`](./Enums.md#enum-odds) | `.3, .1` | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. |

</details>

---

### Context: `Conditional_Boss`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `-2, -1` | Applies or references the 'AllStatsUp' effect/state. |

</details>

---

### Context: `Conditional_ManaThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RepairTrinket` | Number | `1` | Applies or references the 'RepairTrinket' effect/state. |
| `threshold_flat` | Number | `0` |  |

</details>

---

### Context: `ConvertDamageToScaledStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DelayedPain` | Number | `1` | Applies or references the 'DelayedPain' effect/state. |
| `stacks` | Number | `3` | Number of stacks or intensity to apply. |

</details>

---

### Context: `CreateGlobalModifiers`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `NextPlayerCatTakesExtraTurn` | Number | `1` | Applies or references the 'NextPlayerCatTakesExtraTurn' effect/state. |
| `NoCorpses` | Number | `1` | Applies or references the 'NoCorpses' effect/state. |

</details>

---

### Context: `CyborgTurns`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TakeBonusTurnWithAIControl` | [`Block`](./Items_and_Equipment.md#context-takebonusturnwithaicontrol) | `{ ... }` |  |
| `stacks` | Number | `1` |  |

</details>

---

### Context: `DestroyEquipmentAndAttachParasite`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.75` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `pool` | [`Array`](./Arrays.md#array-pool) | `[ FaceGrub HeadGrub NeckGrub ]` | The item pool to draw the parasite from. |

</details>

---

### Context: `Eternal`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `health_percent` | Number | `100%` |  |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `FlyDamageIncrease`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | `true` |  |
| `stacks` | Number | `2` | Number of stacks or intensity to apply. |

</details>

---

### Context: `ForceUseAbilityOnTarget`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `head_MiniMoonArmorAsteroid` | ID of the ability to trigger or reference. |
| `chance` | Number | `25%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

### Context: `ImmediateUseAbility`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `wp_NuclearKnifeExplode` | ID of the ability to trigger or reference. |
| `even_if_stunned` | Boolean | `true` |  |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `distance` | Number | `3` | The distance in tiles to knock the target away. |
| `stacks` | Number | `5` | Number of stacks or intensity to apply. |

</details>

---

### Context: `KnockbackIfCrit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | `10` |  |
| `override_chain_knockback` | Number | `10` |  |

</details>

---

### Context: `ManaGainRange`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `max` | Number | `4` |  |
| `min` | Number | `0` |  |

</details>

---

### Context: `ObjectDetector`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `10%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CharmedDip` |  |

</details>

---

### Context: `PassiveAfterXKills`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `3` | Number of stacks or intensity to apply. |

</details>

---

### Context: `PassiveIfWeaponIsUsable`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `2, 1` | Applies or references the 'Brace' effect/state. |

</details>

---

### Context: `PoopWhenHit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `25%` | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Poop` |  |

</details>

---

### Context: `RemoveStatusStacks`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `1` | The number of stacks to remove. |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Thorns` | The specific status effect ID to remove. |

</details>

---

### Context: `ReviveNextRound`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | `2` | Applies or references the 'Shield' effect/state. |
| `revive_health` | Number | `100%` | The flat amount of health to revive with. |

</details>

---

### Context: `ScaldingOrbMoonBossOneShot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CompleteItemQuest` | [`Enum/String`](./Enums.md#enum-completeitemquest) | `ScaldingOrb` | Applies or references the 'CompleteItemQuest' effect/state. |
| `RemoveItem` | [`Enum/String`](./Enums.md#enum-removeitem) | `ScaldingOrb` | Applies or references the 'RemoveItem' effect/state. |

</details>

---

### Context: `SpawnCatCopyOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `PlayerCat_MiniMiniMe` |  |
| `prevent_chain_tag` | [`Enum/String`](./Enums.md#enum-prevent_chain_tag) | `minime_clone` |  |

</details>

---

### Context: `SpawnOnDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `faction` | [`Enum/String`](./Enums.md#enum-faction) | `solitary_enemies` |  |
| `obj` | [`Enum/String`](./Enums.md#enum-obj) | `BeefyCharmedLeech` |  |

</details>

---

### Context: `SpawnRandomPickupsOnTaggedUnitKilled`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | [`Array`](./Arrays.md#array-count) | `[ 2 3 ]` | Quantity. |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `poop` | Specific entity tag required. |

</details>

---

### Context: `StatusAfterXTurns`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `tk_MadGhost_Spawn` | Applies or references the 'ForceUseAbility' effect/state. |
| `stacks` | Number | `3` | Number of stacks or intensity to apply. |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `RepairTrinket` | Number | `1` | Applies or references the 'RepairTrinket' effect/state. |

</details>

---

### Context: `StatusOnBackstab`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `2` | Applies or references the 'HealthGain' effect/state. |
| `SerratedClaws` | Number | `1` | Applies or references the 'SerratedClaws' effect/state. |

</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` | Applies or references the 'Charge' effect/state. |
| `Shield` | Number | `1` | Applies or references the 'Shield' effect/state. |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `chapter_common` | Generates an item drop from the specified loot pool. |
| `RandomMagicMissile` | Number | `6` | Fires a randomized number of magic missiles. |

</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | `2` | Applies or references the 'LuckUp' effect/state. |
| `Shield` | [`Enum/String`](./Enums.md#enum-shield) | `X` | Applies or references the 'Shield' effect/state. |

</details>

---

### Context: `StatusOnTurnEndIfCastNSpells`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DoubleCastSpell` | Number | `1` |  |
| `spells` | Number | `5` |  |

</details>

---

### Context: `StatusOnUseBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `1` | Applies or references the 'DamageUp' effect/state. |
| `HealthGain` | Number | `1` | Applies or references the 'HealthGain' effect/state. |

</details>

---

### Context: `TakeBonusTurnWithAIControl`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`CyborgTurns`](./Items_and_Equipment.md#context-cyborgturns)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `end_of_round` | Boolean | `true` |  |
| `include_spells` | Boolean | `true` |  |

</details>

---

### Context: `TransformWeapon`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `from` | [`Enum/String`](./Enums.md#enum-from) | `Necro_SoulDagger_Charged` | The original weapon ID. |
| `to` | [`Enum/String`](./Enums.md#enum-to) | `Necro_SoulDagger_Uncharged` | The transformed weapon ID. |

</details>

---

### Context: `damage_instance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status` | Classification type. |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |

</details>

---

### Context: `passive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Metal` | Number | `1` | Applies or references the 'Metal' effect/state. |

</details>

---

### Context: `AddPassivesToCharmed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |

</details>

---

### Context: `AddSelfStatusToWeapons`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RepairWeapon` | [`Array`](./Arrays.md#array-repairweapon) | `[ 1 .25 ]` | Applies or references the 'RepairWeapon' effect/state. |

</details>

---

### Context: `AddStatusToBackstabs`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Leech` | Number | `1` | Applies or references the 'Leech' effect/state. |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Leech` | Number | `1` | Applies or references the 'Leech' effect/state. |

</details>

---

### Context: `AlluringDoodieEater`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `10%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

### Context: `BuffImmunity`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `exclude` | [`Enum/String`](./Enums.md#enum-exclude) | `SpellDamageUp` |  |

</details>

---

### Context: `CatPartsSizeScale`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `head` | Number | `1.3` |  |

</details>

---

### Context: `Conditional_Ally`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | `1` | Applies or references the 'ManaGain' effect/state. |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMutation` | Number | `1` | Applies or references the 'RandomMutation' effect/state. |

</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Leeches` | Number | `1` | Applies or references the 'Leeches' effect/state. |

</details>

---

### Context: `Conditional_HasCleansableDebuffs`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `VisualFX` | [`Enum/String`](./Enums.md#enum-visualfx) | `Cleanse` |  |

</details>

---

### Context: `Conditional_HealthThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `threshold_flat` | Number | `3` | A flat numerical health value threshold. |

</details>

---

### Context: `Conditional_PlayerCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` | Applies or references the 'Charge' effect/state. |

</details>

---

### Context: `Conditional_RandomChance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `odds` | Number | `20%` | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

### Context: `CritsApplyStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |

</details>

---

### Context: `Else`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddStatusToFirstSpellEachTurn`](./Items_and_Equipment.md#context-addstatustofirstspelleachturn)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Webbed` | Number | `1` |  |

</details>

---

### Context: `GlobalFlowerTrapperAura`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Tangled` | [`Array`](./Arrays.md#array-tangled) | `[ 1, .1 ]` |  |

</details>

---

### Context: `GlobalMeleeRevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | `5` |  |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `water` | Specific element type required or applied. |

</details>

---

### Context: `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `1` | Applies or references the 'Brace' effect/state. |

</details>

---

### Context: `PassiveWhileShielded`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Number | `3` | Applies or references the 'HealthRegenUp' effect/state. |

</details>

---

### Context: `RandomPermanentStatsDistinct`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusOnEatPill`](./Items_and_Equipment.md#context-statusoneatpill)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stats` | [`Array`](./Arrays.md#array-stats) | `[ 1 -1 ]` |  |

</details>

---

### Context: `Robot`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean | `true` |  |

</details>

---

### Context: `ScaledStatusOnHolyShieldBlock`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |

</details>

---

### Context: `StatDependentPassive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddDamageToBasicAttack` | [`Equation`](./Enums.md#enum-mathequation) | `"min(min(min(min(min(min(str,dex),int),con),lck),spd),cha...` | Applies or references the 'AddDamageToBasicAttack' effect/state. |

</details>

---

### Context: `StatusAdjacentOnTheirTurnEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceMoveAway` | Number | `1` | Applies or references the 'ForceMoveAway' effect/state. |

</details>

---

### Context: `StatusAllCharactersOnSpawn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |

</details>

---

### Context: `StatusAlliesOnDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `2` | Applies or references the 'DivineShield' effect/state. |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `face_FartFace` | Applies or references the 'ForceUseAbility' effect/state. |

</details>

---

### Context: `StatusIfUnusedActPoints`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `BackflipWhenTargeted` | [`Enum/String`](./Enums.md#enum-backflipwhentargeted) | `X` | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |

</details>

---

### Context: `StatusOnBreakItem`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | `3` | Applies or references the 'Shield' effect/state. |

</details>

---

### Context: `StatusOnDodge`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Number | `2` | Applies or references the 'DodgeChance_Status' effect/state. |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RepairTrinket` | Number | `1` | Applies or references the 'RepairTrinket' effect/state. |

</details>

---

### Context: `StatusOnEatPill`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomPermanentStatsDistinct` | [`Block`](./Items_and_Equipment.md#context-randompermanentstatsdistinct) | `{ ... }` |  |

</details>

---

### Context: `StatusOnEnemyDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `1` | Applies or references the 'Charge' effect/state. |

</details>

---

### Context: `StatusOnHealed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | `1` | Applies or references the 'Shield' effect/state. |

</details>

---

### Context: `StatusOnPickupCoins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `GainCoins` | Number | `1` | Applies or references the 'GainCoins' effect/state. |

</details>

---

### Context: `StatusWhenAllySpendsMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `2` | Applies or references the 'Charge' effect/state. |

</details>

---

### Context: `TempPassiveUntilSettled`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LimitHeal` | Number | `0` | Applies or references the 'LimitHeal' effect/state. |

</details>

---

### Context: `TunnelVision`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `crit_chance` | Number | `50%` |  |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ApplyPassives`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Conditional_Adjacent`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Conditional_Shielded`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ModifyAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `PassiveWhenDead`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `PassiveWhileHasDurability`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ScaledStatusAlliesOnSpendMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ScaledStatusOnSpendMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusAlliesEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusEachRoundEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusOnCollectPickup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusOnFullMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `bonus_passives`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `str_aux_is_copy_ability`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

## Map Generation & Routing

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `empty, battle, npc` | Classification type. |
| `easy` | [`Array`](./Arrays.md#array-easy) | `[ easy bigsharklevels ], [ easy ]` |  |
| `folder` | [`Enum/String`](./Enums.md#enum-folder) | `alley, bunker, boneyard` |  |
| `hard` | [`Array`](./Arrays.md#array-hard) | `[ easy bigsharklevels ], [ easy ], [ hard ]` |  |
| `miniboss` | [`Array`](./Arrays.md#array-miniboss) | `[ miniboss ]` |  |
| `normal` | [`Array`](./Arrays.md#array-normal) | `[ common boneyard_events.gon ], [ common bunker_events.gon ], [ common alley_events.gon ]` |  |
| `rare` | [`Array`](./Arrays.md#array-rare) | `[ rare ]` |  |
| `chapter_item_pool` | [`Enum/String`](./Enums.md#enum-chapter_item_pool) | `boneyarditems, alleyitems, bunkeritems` |  |
| `large` | [`Array`](./Arrays.md#array-large) | `[ KillDozer ], [ Shambler ], [ ]` |  |
| `medium` | [`Array`](./Arrays.md#array-medium) | `[ ZombieCat SkeletonCat TallSkeletonCat WolfCat Tatters S..., [ Rat Leaper Pooter Kitten TomTom Mangy CatCaller ], [ AtomicKitten RoboTom CatCultist Cultist CultistZealot C...` |  |
| `small` | [`Array`](./Arrays.md#array-small) | `[ ], [ Maggot Fly Flea Pinky ], [ Flea Wisp Fly Maggot ]` |  |
| `special` | [`Array`](./Arrays.md#array-special) | `[ special ]` |  |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `Treasure_LargeMeteor, Treasure_SmallMeteor, TreasureHard` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNode_SmallMeteor, Rare_Treasure, MapNode_LargeMetor` |  |
| `jestercat` | [`Enum/String`](./Enums.md#enum-jestercat) | `auto` |  |
| `abandonedones` | [`Enum/String`](./Enums.md#enum-abandonedones) | `auto` |  |
| `advance` | Number | `1` |  |
| `alley` | Block | `{ ... }` |  |
| `boneyard` | Block | `{ ... }` |  |
| `bumblefoot` | [`Enum/String`](./Enums.md#enum-bumblefoot) | `auto` |  |
| `bunker` | Block | `{ ... }` |  |
| `butchercat` | [`Enum/String`](./Enums.md#enum-butchercat) | `auto` |  |
| `cancreeper` | [`Enum/String`](./Enums.md#enum-cancreeper) | `auto` |  |
| `cavecatfamily` | [`Enum/String`](./Enums.md#enum-cavecatfamily) | `auto` |  |
| `caves` | Block | `{ ... }` |  |
| `cerberubs` | [`Enum/String`](./Enums.md#enum-cerberubs) | `auto` |  |
| `choose_one` | [`Array`](./Arrays.md#array-choose_one) | `[ GenFlag_Boss_Stacy, GenFlag_Boss_Spewer ]` |  |
| `clericcat` | [`Enum/String`](./Enums.md#enum-clericcat) | `auto` |  |
| `core` | Block | `{ ... }` |  |
| `crater` | Block | `{ ... }` |  |
| `desert` | Block | `{ ... }` |  |
| `dinocouple` | [`Enum/String`](./Enums.md#enum-dinocouple) | `auto` |  |
| `drmangler` | [`Enum/String`](./Enums.md#enum-drmangler) | `auto` |  |
| `druidcat` | [`Enum/String`](./Enums.md#enum-druidcat) | `auto` |  |
| `fightercat` | [`Enum/String`](./Enums.md#enum-fightercat) | `auto` |  |
| `flushmaster` | [`Enum/String`](./Enums.md#enum-flushmaster) | `auto` |  |
| `gambit` | [`Enum/String`](./Enums.md#enum-gambit) | `auto` |  |
| `head_start` | Number | `99` |  |
| `huntercat` | [`Enum/String`](./Enums.md#enum-huntercat) | `auto` |  |
| `iceelemental` | [`Enum/String`](./Enums.md#enum-iceelemental) | `auto` |  |
| `infestedduo` | [`Enum/String`](./Enums.md#enum-infestedduo) | `auto` |  |
| `junkyard` | Block | `{ ... }` |  |
| `lab` | Block | `{ ... }` |  |
| `lenny` | [`Enum/String`](./Enums.md#enum-lenny) | `auto` |  |
| `lightningelemental` | [`Enum/String`](./Enums.md#enum-lightningelemental) | `auto` |  |
| `locked` | Boolean | `true` |  |
| `magecat` | [`Enum/String`](./Enums.md#enum-magecat) | `auto` |  |
| `mamamaggot` | [`Enum/String`](./Enums.md#enum-mamamaggot) | `auto` |  |
| `meatworld` | Block | `{ ... }` |  |
| `monkcat` | [`Enum/String`](./Enums.md#enum-monkcat) | `auto` |  |
| `moon` | Block | `{ ... }` |  |
| `musiclayer` | [`Enum/String`](./Enums.md#enum-musiclayer) | `boss` |  |
| `necrocat` | [`Enum/String`](./Enums.md#enum-necrocat) | `auto` |  |
| `nemesis` | [`Array`](./Arrays.md#array-nemesis) | `[ nemesis ]` |  |
| `psychiccat` | [`Enum/String`](./Enums.md#enum-psychiccat) | `auto` |  |
| `queenhippo` | [`Enum/String`](./Enums.md#enum-queenhippo) | `auto` |  |
| `radicalrat` | [`Enum/String`](./Enums.md#enum-radicalrat) | `auto` |  |
| `ratking` | [`Enum/String`](./Enums.md#enum-ratking) | `auto` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `never` |  |
| `rockybobo` | [`Enum/String`](./Enums.md#enum-rockybobo) | `auto` |  |
| `sewers` | Block | `{ ... }` |  |
| `slime` | [`Enum/String`](./Enums.md#enum-slime) | `auto` |  |
| `spawn_node` | [`Enum/String`](./Enums.md#enum-spawn_node) | `start` |  |
| `spewer` | [`Enum/String`](./Enums.md#enum-spewer) | `auto` |  |
| `stacy` | [`Enum/String`](./Enums.md#enum-stacy) | `auto` |  |
| `tankcat` | [`Enum/String`](./Enums.md#enum-tankcat) | `auto` |  |
| `thebloat` | [`Enum/String`](./Enums.md#enum-thebloat) | `auto` |  |
| `thiefcat` | [`Enum/String`](./Enums.md#enum-thiefcat) | `auto` |  |
| `tinkerercat` | [`Enum/String`](./Enums.md#enum-tinkerercat) | `auto` |  |
| `trampy` | [`Enum/String`](./Enums.md#enum-trampy) | `auto` |  |
| `zodiac` | [`Enum/String`](./Enums.md#enum-zodiac) | `auto` |  |

</details>

---

### Context: `exit0`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean | `false, true` |  |
| `next_map` | [`Enum/String`](./Enums.md#enum-next_map) | `meatworld.gon, core.gon, sewers.gon` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNodeExit_Core, MapNodeExit_MeatWorld, MapNodeExit_Sewers` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `exit` | Classification type. |
| `hidden` | Boolean | `false, true` |  |

</details>

---

### Context: `quest_event`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNode_Veins, MapNode_VeinsDrained, MapNode_Empty` |  |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `Quest_WallOfFlesh, Quest_ThrobbingArtery2, Quest_ThrobbingArtery` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `empty, special_event` | Classification type. |

</details>

---

### Context: `boss`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `boss` | Classification type. |
| `boss_cutscene` | [`Enum/String`](./Enums.md#enum-boss_cutscene) | `spiderkitten, johnny, dybbuk` |  |
| `is_final_boss` | Boolean | `true` |  |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `spewer, stacy` |  |
| `override_music` | [`Enum/String`](./Enums.md#enum-override_music) | `chaos_boss, finalboss` |  |
| `tileset` | [`Enum/String`](./Enums.md#enum-tileset) | `finalboss` |  |
| `unlockcheck_on_complete` | [`Enum/String`](./Enums.md#enum-unlockcheck_on_complete) | `map_unlock_junkyard` |  |

</details>

---

### Context: `exit1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean | `false, true` |  |
| `next_map` | [`Enum/String`](./Enums.md#enum-next_map) | `crater.gon, future.gon, junkyard.gon` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNodeExit_Future, MapNodeExit_Junkyard, MapNodeExit_Crater` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `exit` | Classification type. |

</details>

---

### Context: `time_machine`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `Quest_TimeMachineFuture, Quest_TimeMachineJurassic, Quest_TimeMachineIceAge` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNode_TimeMachine` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `special_event` | Classification type. |

</details>

---

### Context: `hard_initial`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean | `false, true` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `hard` | Classification type. |

</details>

---

### Context: `exit_desert`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `true` |  |
| `locked` | Boolean | `true` |  |
| `next_map` | [`Enum/String`](./Enums.md#enum-next_map) | `desert.gon` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNodeExit_Desert` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `exit` | Classification type. |

</details>

---

### Context: `exit_lab`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `true` |  |
| `locked` | Boolean | `true` |  |
| `next_map` | [`Enum/String`](./Enums.md#enum-next_map) | `lab.gon` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNodeExit_Lab` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `exit` | Classification type. |

</details>

---

### Context: `mw_boss`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `boss_cutscene` | [`Enum/String`](./Enums.md#enum-boss_cutscene) | `throbbingking` |  |
| `override_music` | [`Enum/String`](./Enums.md#enum-override_music) | `throbbingking` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `boss` | Classification type. |

</details>

---

### Context: `mw_quest_event`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `Quest_DeadKing` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNode_DeadKing` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `special_event` | Classification type. |

</details>

---

### Context: `mw_hard1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `musiclayer` | [`Enum/String`](./Enums.md#enum-musiclayer) | `boss` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `hard` | Classification type. |

</details>

---

### Context: `miniboss_event`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `empty, special_event` | Classification type. |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `StacyMutant1` |  |

</details>

---

### Context: `mw_altar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `Quest_MeatWorldAltar` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNode_MeatAltar` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `special_event` | Classification type. |

</details>

---

### Context: `mw_battle1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `battle` | Classification type. |

</details>

---

### Context: `mw_event1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `event` | Classification type. |

</details>

---

### Context: `mw_home`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `home` | Classification type. |

</details>

---

### Context: `mw_treasure`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `treasure` | Classification type. |

</details>

---

### Context: `shop_cheapwater`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `WaterShopCheap` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `cheapwatershop` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `shop` | Classification type. |

</details>

---

### Context: `shop_water`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `WaterShop` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `cheapwatershop` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `shop` | Classification type. |

</details>

---

### Context: `event`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `Butch_Tutorial` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `event` | Classification type. |

</details>

---

### Context: `mw_earlyhome`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `true` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `home` | Classification type. |

</details>

---

### Context: `treasure`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `TreasureTutorial` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `treasure` | Classification type. |

</details>

---

### Context: `weather_event`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `CraterWeatherEvent` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `special_event` | Classification type. |

</details>

---

### Context: `battle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `battle` | Classification type. |

</details>

---

### Context: `dimensionx`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

</details>

---

### Context: `endoftime`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

</details>

---

### Context: `future`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

</details>

---

### Context: `home`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `home` | Classification type. |

</details>

---

### Context: `iceage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

</details>

---

### Context: `jurassic`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

</details>

---

### Context: `start`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `enter` | Classification type. |

</details>

---

### Context: `theend`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

</details>

---

### Context: `BoneyardUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `BothObelisksUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `BunkerUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `CavesUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ChaosAntennaAttached`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `CoreObeliskUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `CoreUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `CraterUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `DimensionXUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `EndOfTimeUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `FutureUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `GenFlag_Boss_Spewer`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `GenFlag_Boss_Stacy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `HardPathUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `IceAgeUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `JunkyardUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `JurassicUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `MeatWorldUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `MeatWorldUnlockedFull`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `MoonObeliskUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `MoonUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `SewersUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `TheEndUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ThrobbingArteryDone`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `VolcanoAntennaAttached`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `WallOfFleshDone`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

## Passives & Statuses

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `name` | String | `"PASSIVE_MAINCOURSE_NAME", "PASSIVE_NEVERFULL_NAME", "PASSIVE_PUTREFY_NAME"` | Localization key for the passive's display name. |
| `class` | [`Enum/String`](./Enums.md#enum-class) | `Disorder, Butcher, Colorless` | Character class identifier. |
| `desc` | String | `"PASSIVE_MAINCOURSE_DESC", "PASSIVE_NEVERFULL_DESC", "PASSIVE_PUTREFY_DESCRIPTION"` | Localization key for the passive's display description. |
| `desc_multiclass` | String | `"PASSIVE_BARBED_MULTICLASS_DESC", "PASSIVE_HOOKED_MULTICLASS_DESC", "PASSIVE_GRAPPLINGHOOK_MULTICLASS_DESC"` |  |
| `auto_plus_signs_on_name` | Boolean | `false` |  |
| `name_mod` | String | `"CAT_NAME_MOD_GIGANTISM", "CAT_NAME_MOD_VEGAN", "CAT_NAME_MOD_DWARF"` |  |
| `tags` | [`Array`](./Arrays.md#array-tags) | `[ noncopyable ]` |  |
| `override_basic_attack` | [`Enum/String`](./Enums.md#enum-override_basic_attack) | `GerdShot, BasicMelee` |  |
| `shield` | Number | `8, 4` |  |
| `bonus_items` | [`Array`](./Arrays.md#array-bonus_items) | `[ Eyeball ]` | Flat addition to a base value. |
| `grant_ability` | [`Enum/String`](./Enums.md#enum-grant_ability) | `Rest` |  |

</details>

---

### Context: `passives`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddStatusToBasicAttack` | [`Block`](./Passives_and_Statuses.md#context-addstatustobasicattack) | `{ ... }` | Injects a status effect payload that applies whenever the character performs a basic attack. |
| `MulticlassLevelUp` | [`Enum/String`](./Enums.md#enum-multiclasslevelup) | `Mage, Fighter, Hunter` | Applies the 'MulticlassLevelUp' effect. |
| `CritChanceUp` | Number | `25, 10, 5` | Applies the 'CritChanceUp' effect. |
| `SpawnOnBattleStart` | [`Block`](./Passives_and_Statuses.md#context-spawnonbattlestart) | `{ ... }, BeefyCharmedLeech, CharmedTinySpider` | Applies the 'SpawnOnBattleStart' effect. |
| `AddCritMultiplier` | Number | `25%, 50%, 100%` | Applies the 'AddCritMultiplier' effect. |
| `MissChance` | Number | `10, 5, 15` | Applies the 'MissChance' effect. |
| `StatusOnKill` | [`Block`](./Passives_and_Statuses.md#context-statusonkill) | `{ ... }` | Event Trigger: Applies nested statuses when kill. |
| `ReplaceSpawnedObjects` | [`Array`](./Arrays.md#array-replacespawnedobjects) | `[ Crow Crow3 ], [ Crow2 Crow3 ], [ Crow Crow2 ]` | Applies the 'ReplaceSpawnedObjects' effect. |
| `AddBonusRange` | Number | `2, 1, 10` | Applies the 'AddBonusRange' effect. |
| `BonusAbility` | [`Enum/String`](./Enums.md#enum-bonusability) | `Groom, FeralMelee, Bloodzerk` | Applies the 'BonusAbility' effect. |
| `Brace` | Number | `2, 1, 3` | Applies the 'Brace' effect. |
| `DodgeChance` | Number | `10%, 25%, 15%` | Applies the 'DodgeChance' effect. |
| `HealthRegenUp` | Number | `2, 1, 3` | Applies the 'HealthRegenUp' effect. |
| `CritsApplyStatus` | [`Block`](./Passives_and_Statuses.md#context-critsapplystatus) | `{ ... }` | Applies the 'CritsApplyStatus' effect. |
| `PassiveLevelUpAtCombatEnd` | Number | `1` | Applies the 'PassiveLevelUpAtCombatEnd' effect. |
| `ExtraBasicAttacks` | Number | `2, 1` | Applies the 'ExtraBasicAttacks' effect. |
| `Trample` | Number | `9, 3` | Applies the 'Trample' effect. |
| `AmplifyStatus` | [`Block`](./Passives_and_Statuses.md#context-amplifystatus) | `{ ... }, Rot, Burn` | Applies the 'AmplifyStatus' effect. |
| `EquipTemporaryItem` | [`Enum/String`](./Enums.md#enum-equiptemporaryitem) | `FoodMedium, ButcherHook_Temporary, FoodBig` | Applies the 'EquipTemporaryItem' effect. |
| `ForceSpecificInjury` | [`Enum/String`](./Enums.md#enum-forcespecificinjury) | `int, cha, lck` | Applies the 'ForceSpecificInjury' effect. |
| `InnateElement` | [`Enum/String`](./Enums.md#enum-innateelement) | `Electric, Fire, Ice` | Applies the 'InnateElement' effect. |
| `ReplaceBasicAttack` | [`Enum/String`](./Enums.md#enum-replacebasicattack) | `BasicDruidAbilityVersatile, BasicButcherMeleeWideDoubleSpin, BasicButcherMeleeWideSpin` | Applies the 'ReplaceBasicAttack' effect. |
| `SizeScale` | [`Enum/String`](./Enums.md#enum-sizescale) | `.4, 1.3, .7` | Applies the 'SizeScale' effect. |
| `StatusImmunity` | [`Array`](./Arrays.md#array-statusimmunity) | `[ Sleep SleepParalysis ], Burn, [ Fear Madness PermanentMadness ]` | Event Trigger: Applies nested statuses to immunity. |
| `AbilityOnBattleStart` | [`Enum/String`](./Enums.md#enum-abilityonbattlestart) | `Heathens, MegaFart, neck_ChefsApron` | Applies the 'AbilityOnBattleStart' effect. |
| `AddCorpseHealth` | Number | `-999999, 96, 3` | Applies the 'AddCorpseHealth' effect. |
| `BlastResistance` | Number | `2, 3, 4` | Applies the 'BlastResistance' effect. |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Electric, Fire, Ice` | Applies the 'ElementImmune' effect. |
| `Thorns` | Number | `2, 4` | Applies the 'Thorns' effect. |
| `AddElementsToBasicAttack` | [`Enum/String`](./Enums.md#enum-addelementstobasicattack) | `Electric, Fire, Ice` | Applies the 'AddElementsToBasicAttack' effect. |
| `AlphaTurns` | Number | `1, -1` | Applies the 'AlphaTurns' effect. |
| `BasicAttackDamageMultiplier` | Number | `33.333334%, 50%, 0` | Applies the 'BasicAttackDamageMultiplier' effect. |
| `BoostWeaponDamage` | Number | `2, 1, 5` | Applies the 'BoostWeaponDamage' effect. |
| `ExtraMovePoints` | Number | `1` | Applies the 'ExtraMovePoints' effect. |
| `ExtraWeaponAttacks` | Number | `2, 1` | Applies the 'ExtraWeaponAttacks' effect. |
| `ReplaceBasicAttackWhenCastable` | [`Enum/String`](./Enums.md#enum-replacebasicattackwhencastable) | `Shank, BasicSuplex, Shank2` | Applies the 'ReplaceBasicAttackWhenCastable' effect. |
| `SetSpellCosts` | Number | `0, 1, 3` | Applies the 'SetSpellCosts' effect. |
| `StatusOnStanceSwitch` | [`Block`](./Passives_and_Statuses.md#context-statusonstanceswitch) | `{ ... }` | Event Trigger: Applies nested statuses when stance switch. |
| `AddBonusMeleeRange` | Number | `2, 1, 10` | Applies the 'AddBonusMeleeRange' effect. |
| `AddManaRegen` | Number | `7, 1, 5` | Applies the 'AddManaRegen' effect. |
| `AllStatsUp` | Number | `-2, 2, -1` | Applies the 'AllStatsUp' effect. |
| `BasicAttackAOEBonus` | Number | `2, 1` | Applies the 'BasicAttackAOEBonus' effect. |
| `ReplaceBasicMove` | [`Enum/String`](./Enums.md#enum-replacebasicmove) | `BasicDashAttackMove, ToadJump_BasicMove, BellyFlop_BasicMove` | Applies the 'ReplaceBasicMove' effect. |
| `AbilityReaction` | [`Enum/String`](./Enums.md#enum-abilityreaction) | `Gassy_AssBlast2, PissYourself, Gassy_AssBlast` | Applies the 'AbilityReaction' effect. |
| `AddDamageToBasicAttack` | Number | `2, 1, 4` | Applies the 'AddDamageToBasicAttack' effect. |
| `AddLevelUpRerolls` | Number | `2, 1, 3` | Applies the 'AddLevelUpRerolls' effect. |
| `AddMovement` | Number | `2, 1, 4` | Applies the 'AddMovement' effect. |
| `AllyBonusAbilityAura` | [`Block`](./Passives_and_Statuses.md#context-allybonusabilityaura) | `{ ... }, NubbyToss` | Applies the 'AllyBonusAbilityAura' effect. |
| `BackstabCritChance` | Number | `1` | Applies the 'BackstabCritChance' effect. |
| `BoostHeals` | Number | `2, -2, 1` | Applies the 'BoostHeals' effect. |
| `FreezePiercing` | Number | `1` | Applies the 'FreezePiercing' effect. |
| `IncreaseExplosionDamage` | Number | `2, 3, 4` | Applies the 'IncreaseExplosionDamage' effect. |
| `KnockbackImmunity` | Number | `1` | Applies the 'KnockbackImmunity' effect. |
| `LevelUpClassOverride` | [`Enum/String`](./Enums.md#enum-levelupclassoverride) | `Jester, Colorless` | Applies the 'LevelUpClassOverride' effect. |
| `MakeSpellsRequireCharge` | Number | `1` | Applies the 'MakeSpellsRequireCharge' effect. |
| `MoveQuivered` | Number | `2` | Applies the 'MoveQuivered' effect. |
| `SpawnThingOnDeath` | [`Enum/String`](./Enums.md#enum-spawnthingondeath) | `ZombieCatFamiliar, CharmedDemonKitten` | Applies the 'SpawnThingOnDeath' effect. |
| `AddKnockbackDamage` | Number | `2, 1, 3` | Applies the 'AddKnockbackDamage' effect. |
| `AddTag` | [`Enum/String`](./Enums.md#enum-addtag) | `rock` | Applies the 'AddTag' effect. |
| `AllyDamageReduction` | Number | `0` | Applies the 'AllyDamageReduction' effect. |
| `AmplifyKnockback` | Number | `2, 10` | Applies the 'AmplifyKnockback' effect. |
| `AutocastEachTurnBegin` | [`Block`](./Passives_and_Statuses.md#context-autocasteachturnbegin) | `{ ... }, MindCrack_EldritchVisage2, MindCrack_EldritchVisage` | Applies the 'AutocastEachTurnBegin' effect. |
| `Bruise` | Number | `2, 1` | Applies the 'Bruise' effect. |
| `CobraReflex` | [`Enum/String`](./Enums.md#enum-cobrareflex) | `BasicMonkMelee` | Applies the 'CobraReflex' effect. |
| `ConsumablesInfiniteRange` | Number | `1` | Applies the 'ConsumablesInfiniteRange' effect. |
| `DamageUp` | Number | `4, 1, 3` | Combat Trigger: Deals damage to up. |
| `FreePathfindElement` | [`Enum/String`](./Enums.md#enum-freepathfindelement) | `Grass, Water` | Applies the 'FreePathfindElement' effect. |
| `IgnoreTiles` | Number | `1` | Applies the 'IgnoreTiles' effect. |
| `Quivered` | Number | `2, 1, 5` | Applies the 'Quivered' effect. |
| `TauntAlways` | Number | `1` | Applies the 'TauntAlways' effect. |
| `TileTrail` | [`Enum/String`](./Enums.md#enum-tiletrail) | `GrassTile, FlowerTile` | Applies the 'TileTrail' effect. |
| `TrinketActiveEffectsMultiplierBonus` | Number | `2, 1` | Applies the 'TrinketActiveEffectsMultiplierBonus' effect. |
| `TrinketPassiveMultiplierBonus` | Number | `2, 1` | Applies the 'TrinketPassiveMultiplierBonus' effect. |
| `UncappedMana` | Number | `1` | Applies the 'UncappedMana' effect. |
| `AbsorbManaAura` | Number | `1` | Applies the 'AbsorbManaAura' effect. |
| `AddHiddenTag` | [`Enum/String`](./Enums.md#enum-addhiddentag) | `bowling_ball` | Applies the 'AddHiddenTag' effect. |
| `AddInitiative` | Number | `-100, 999` | Applies the 'AddInitiative' effect. |
| `AddSpellDamage` | Number | `1` | Applies the 'AddSpellDamage' effect. |
| `AddStartingMana` | Number | `20, 5` | Applies the 'AddStartingMana' effect. |
| `AddStatusToExplosions` | [`Block`](./Passives_and_Statuses.md#context-addstatustoexplosions) | `{ ... }` | Applies the 'AddStatusToExplosions' effect. |
| `AddUnfilledMaxHealth` | Number | `50, 20` | Applies the 'AddUnfilledMaxHealth' effect. |
| `AddWeaponScaling` | Number | `1` | Applies the 'AddWeaponScaling' effect. |
| `AfterImage` | [`Enum/String`](./Enums.md#enum-afterimage) | `PlayerCat_ThiefShade2, PlayerCat_ThiefShade` | Spawns a visual decoy or shade at the caster's previous location. |
| `AllowPassTurn` | Number | `1, 0` | Applies the 'AllowPassTurn' effect. |
| `AllyDamageReaction` | [`Enum/String`](./Enums.md#enum-allydamagereaction) | `attack` | Applies the 'AllyDamageReaction' effect. |
| `AllyMoveAbilityAura` | [`Enum/String`](./Enums.md#enum-allymoveabilityaura) | `CatapultJump2, CatapultJump` | Applies the 'AllyMoveAbilityAura' effect. |
| `AllyMultiplyKnockbackDamage` | Number | `2` | Applies the 'AllyMultiplyKnockbackDamage' effect. |
| `AmplifyPositiveStatus` | Number | `2, 1` | Applies the 'AmplifyPositiveStatus' effect. |
| `AutoCritLowDamage` | Number | `2, 3` | Applies the 'AutoCritLowDamage' effect. |
| `AutoEquipConsumables` | Number | `1` | Applies the 'AutoEquipConsumables' effect. |
| `AutocastEachTurn` | [`Enum/String`](./Enums.md#enum-autocasteachturn) | `ViolentOutburst, DarkOneStrike` | Applies the 'AutocastEachTurn' effect. |
| `BasicAttackCritChance` | Number | `100%` | Applies the 'BasicAttackCritChance' effect. |
| `BasicAttackStatusCarefulness` | Number | `1` | Applies the 'BasicAttackStatusCarefulness' effect. |
| `Bleed` | Number | `1, 3` | Applies the 'Bleed' effect. |
| `BonusFoodEachBattle` | Number | `2, 20` | Applies the 'BonusFoodEachBattle' effect. |
| `BoostAllyStatsOnDeath` | Number | `2, 1` | Applies the 'BoostAllyStatsOnDeath' effect. |
| `BraceForEachNeighboringEnemy` | Number | `2, 1` | Applies the 'BraceForEachNeighboringEnemy' effect. |
| `CCImmunity` | Number | `1` | Applies the 'CCImmunity' effect. |
| `CapDamageFromAllies` | Number | `1` | Applies the 'CapDamageFromAllies' effect. |
| `ChainKnockback` | Number | `1` | Applies the 'ChainKnockback' effect. |
| `ChanceToBlockAndCounter` | Number | `33%, 15%` | Applies the 'ChanceToBlockAndCounter' effect. |
| `ChanceToRevive` | [`Block`](./Passives_and_Statuses.md#context-chancetorevive) | `{ ... }, 25` | Applies the 'ChanceToRevive' effect. |
| `ChangeTauntPriority` | Number | `-1` | Applies the 'ChangeTauntPriority' effect. |
| `CharmAllFlies` | Number | `1` | Applies the 'CharmAllFlies' effect. |
| `CoinsAddDamage` | Number | `2, 1` | Applies the 'CoinsAddDamage' effect. |
| `CollectPickupsOnBattleEnd` | [`Block`](./Passives_and_Statuses.md#context-collectpickupsonbattleend) | `{ ... }, 1` | Applies the 'CollectPickupsOnBattleEnd' effect. |
| `Conductor` | Number | `2` | Applies the 'Conductor' effect. |
| `ConjureCastSpellsForAllies` | Number | `2, 1` | Applies the 'ConjureCastSpellsForAllies' effect. |
| `ConsumableEffectsMultiplierBonus` | Number | `1` | Applies the 'ConsumableEffectsMultiplierBonus' effect. |
| `CounterAttack` | [`Enum/String`](./Enums.md#enum-counterattack) | `ReflexPunchJab2, ReflexPunchJab` | Applies the 'CounterAttack' effect. |
| `DamageEnemiesOnHeal` | Number | `2, 1` | Combat Trigger: Deals damage to enemies on heal. |
| `DamageEnemiesOnKill` | Number | `2, 1` | Combat Trigger: Deals damage to enemies on kill. |
| `DeathChill` | Number | `1` | Applies the 'DeathChill' effect. |
| `DebuffImmunity` | Number | `1` | Applies the 'DebuffImmunity' effect. |
| `DejaVu` | Number | `10%` | Applies the 'DejaVu' effect. |
| `DirtyClaws` | Number | `1` | Applies the 'DirtyClaws' effect. |
| `DoubleCastWeapons` | Number | `2, 1` | Applies the 'DoubleCastWeapons' effect. |
| `DukeOfFlies` | Number | `1` | Applies the 'DukeOfFlies' effect. |
| `Dyslexia` | [`Array`](./Arrays.md#array-dyslexia) | `[ 6 9 ], [ 3 5 ]` | Applies the 'Dyslexia' effect. |
| `EMP` | [`Block`](./Passives_and_Statuses.md#context-emp) | `{ ... }` | Applies the 'EMP' effect. |
| `Empath` | Number | `50%, 100%` | Applies the 'Empath' effect. |
| `EnemiesGetPickupsKnockedOut` | Number | `2, 1` | Applies the 'EnemiesGetPickupsKnockedOut' effect. |
| `EnergyStorm` | [`Block`](./Passives_and_Statuses.md#context-energystorm) | `{ ... }, 3` | Applies the 'EnergyStorm' effect. |
| `EquipmentPassiveMultiplierBonus` | Number | `1` | Applies the 'EquipmentPassiveMultiplierBonus' effect. |
| `EquipmentSetBonusBonus` | Number | `2, 1` | Applies the 'EquipmentSetBonusBonus' effect. |
| `ExplodeOverkilledEnemies` | Number | `2, 1` | Applies the 'ExplodeOverkilledEnemies' effect. |
| `FaceShield` | Number | `0` | Applies the 'FaceShield' effect. |
| `FamiliarSecondaryDamageImmunity` | Number | `1` | Applies the 'FamiliarSecondaryDamageImmunity' effect. |
| `FlowerPowerAuraBrace` | Number | `1` | Applies the 'FlowerPowerAuraBrace' effect. |
| `FlowerPowerAuraStrength` | Number | `1` | Applies the 'FlowerPowerAuraStrength' effect. |
| `FlowersOnEndTurn` | Number | `4, 3` | Applies the 'FlowersOnEndTurn' effect. |
| `FlyDamageIncrease` | Number | `1, 4` | Applies the 'FlyDamageIncrease' effect. |
| `Flying` | Number | `1` | Applies the 'Flying' effect. |
| `FollowUp` | [`Enum/String`](./Enums.md#enum-followup) | `FollowUpDash, FollowUpDash2` | Applies the 'FollowUp' effect. |
| `FullHealthCritChance` | Number | `100` | Applies the 'FullHealthCritChance' effect. |
| `FullPower` | Number | `3` | Applies the 'FullPower' effect. |
| `GainExtraShield` | Number | `2` | Applies the 'GainExtraShield' effect. |
| `HeadArmorPassiveMultiplierBonus` | Number | `2, 1` | Applies the 'HeadArmorPassiveMultiplierBonus' effect. |
| `HealDamagesEnemies` | Number | `1` | Applies the 'HealDamagesEnemies' effect. |
| `HealsAlsoRegenMana` | Number | `50%, 2` | Applies the 'HealsAlsoRegenMana' effect. |
| `HealsCanRevive` | Number | `1, 3` | Applies the 'HealsCanRevive' effect. |
| `HolyShieldTransferToTaggedMinions` | [`Enum/String`](./Enums.md#enum-holyshieldtransfertotaggedminions) | `any, crow` | Applies the 'HolyShieldTransferToTaggedMinions' effect. |
| `ImmortalLeeches` | Number | `1` | Applies the 'ImmortalLeeches' effect. |
| `IncreaseExplosionSize` | Number | `2` | Applies the 'IncreaseExplosionSize' effect. |
| `IncreaseHealingSpellRange` | Number | `2` | Applies the 'IncreaseHealingSpellRange' effect. |
| `IncreaseSpellRange` | Number | `10, 5` | Applies the 'IncreaseSpellRange' effect. |
| `KillsHeal` | Number | `50%, 5` | Applies the 'KillsHeal' effect. |
| `KillsToMeat` | [`Enum/String`](./Enums.md#enum-killstomeat) | `Food` | Applies the 'KillsToMeat' effect. |
| `LightningAspectCharge` | Number | `1, 0` | Applies the 'LightningAspectCharge' effect. |
| `LineOfSightTrueSightAura` | [`Enum/String`](./Enums.md#enum-lineofsighttruesightaura) | `.5, 0` | Applies the 'LineOfSightTrueSightAura' effect. |
| `LobbedHook` | Number | `2, 1` | Applies the 'LobbedHook' effect. |
| `MakeBasicAttackPassThroughThings` | Number | `1` | Applies the 'MakeBasicAttackPassThroughThings' effect. |
| `ManaRegenMultiplierIfManaEmpty` | Number | `2` | Applies the 'ManaRegenMultiplierIfManaEmpty' effect. |
| `MegaMinions` | [`Block`](./Passives_and_Statuses.md#context-megaminions) | `{ ... }, 3` | Applies the 'MegaMinions' effect. |
| `Metal` | Number | `1` | Applies the 'Metal' effect. |
| `MetalDetector` | Number | `10, 5` | Applies the 'MetalDetector' effect. |
| `MinimumTech` | Number | `1` | Applies the 'MinimumTech' effect. |
| `MoveAndUseAbilityEachTurnBeginIfPossible` | [`Enum/String`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | `Cannibalize, EatShit` | Applies the 'MoveAndUseAbilityEachTurnBeginIfPossible' effect. |
| `NoReflection` | Number | `1` | Applies the 'NoReflection' effect. |
| `NubbyTossPriority` | Number | `1` | Applies the 'NubbyTossPriority' effect. |
| `NumbingLeeches` | Number | `3` | Applies the 'NumbingLeeches' effect. |
| `OverhealGainsBothShield` | Number | `2, 1` | Applies the 'OverhealGainsBothShield' effect. |
| `OverrideBasicAttack` | [`Enum/String`](./Enums.md#enum-overridebasicattack) | `GerdShot, BasicMelee` | Applies the 'OverrideBasicAttack' effect. |
| `ParasitesArentCursed` | Number | `1` | Applies the 'ParasitesArentCursed' effect. |
| `PassiveWhenAffectedByElement` | [`Block`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement) | `{ ... }` | State Trigger: Grants nested passives when affected by element. |
| `PermanentItems` | Number | `2, 1` | Applies the 'PermanentItems' effect. |
| `PoisonThorns` | Number | `2, 1` | Applies the 'PoisonThorns' effect. |
| `ProtectTargetedAllies` | [`Enum/String`](./Enums.md#enum-protecttargetedallies) | `SwapPositions_WideLoad2, SwapPositions_WideLoad` | Applies the 'ProtectTargetedAllies' effect. |
| `Quiver` | Number | `2, 1` | Applies the 'Quiver' effect. |
| `RangedTrueShot` | Number | `1` | Applies the 'RangedTrueShot' effect. |
| `RemoveLineOfSightRestrictions` | Number | `1` | Applies the 'RemoveLineOfSightRestrictions' effect. |
| `RemoveOncePerFightRestriction` | Number | `1` | Applies the 'RemoveOncePerFightRestriction' effect. |
| `ReplaceBasicAttackWhenDead` | [`Enum/String`](./Enums.md#enum-replacebasicattackwhendead) | `Haunt` | Applies the 'ReplaceBasicAttackWhenDead' effect. |
| `ReviveOnWin` | Number | `100%` | Applies the 'ReviveOnWin' effect. |
| `RobotsInheritArmor` | Number | `2, 1` | Applies the 'RobotsInheritArmor' effect. |
| `RockDetector` | Number | `10` | Applies the 'RockDetector' effect. |
| `ShareHealthRegen` | Number | `1` | Applies the 'ShareHealthRegen' effect. |
| `SharePickups` | Number | `1` | Applies the 'SharePickups' effect. |
| `ShoulderCheck` | Number | `100%, 33%` | Applies the 'ShoulderCheck' effect. |
| `ShovingMatch` | [`Enum/String`](./Enums.md#enum-shovingmatch) | `attack` | Applies the 'ShovingMatch' effect. |
| `ShowHiddenThings` | Number | `1` | Applies the 'ShowHiddenThings' effect. |
| `SmallEnemiesIgnoreYou` | Number | `1` | Applies the 'SmallEnemiesIgnoreYou' effect. |
| `SpawnObjectOnPopCorpse` | [`Enum/String`](./Enums.md#enum-spawnobjectonpopcorpse) | `Food` | Applies the 'SpawnObjectOnPopCorpse' effect. |
| `SpeedUp` | Number | `6` | Applies the 'SpeedUp' effect. |
| `SplittableMove` | Number | `1, 3` | Applies the 'SplittableMove' effect. |
| `SpreadExtraDebuffs` | Number | `2, 1` | Applies the 'SpreadExtraDebuffs' effect. |
| `SpreadPainBonus` | Number | `2` | Applies the 'SpreadPainBonus' effect. |
| `StatMinimum` | Number | `7, 5` | Applies the 'StatMinimum' effect. |
| `StatusAlliesOnKill` | [`Block`](./Passives_and_Statuses.md#context-statusalliesonkill) | `{ ... }` | Event Trigger: Applies nested statuses to allies on kill. |
| `StatusReplacement` | [`Array`](./Arrays.md#array-statusreplacement) | `[ Petrify PetrifyCharmed ]` | Event Trigger: Applies nested statuses to replacement. |
| `Stealth` | Number | `1` | Applies the 'Stealth' effect. |
| `StrengthForEachNeighboringEnemy` | Number | `2, 3` | Applies the 'StrengthForEachNeighboringEnemy' effect. |
| `StrengthInNumbersAura` | [`Block`](./Passives_and_Statuses.md#context-strengthinnumbersaura) | `{ ... }, 1` | Applies the 'StrengthInNumbersAura' effect. |
| `StrengthUp` | Number | `2` | Applies the 'StrengthUp' effect. |
| `Study` | [`Block`](./Passives_and_Statuses.md#context-study) | `{ ... }, 1` | Applies the 'Study' effect. |
| `Tech` | Number | `1` | Applies the 'Tech' effect. |
| `TileDamageMultiplier` | [`Block`](./Passives_and_Statuses.md#context-tiledamagemultiplier) | `{ ... }, 2` | Applies the 'TileDamageMultiplier' effect. |
| `TowerDefenseReflex` | [`Enum/String`](./Enums.md#enum-towerdefensereflex) | `BasicRanged_1DMG, attack` | Applies the 'TowerDefenseReflex' effect. |
| `TrapEffectsMultiplier` | Number | `2` | Applies the 'TrapEffectsMultiplier' effect. |
| `UncappedHP` | Number | `1` | Applies the 'UncappedHP' effect. |
| `UpgradeLevelUpClassActives` | [`Enum/String`](./Enums.md#enum-upgradelevelupclassactives) | `Colorless` | Applies the 'UpgradeLevelUpClassActives' effect. |
| `UpgradeLevelUpClassPassives` | [`Enum/String`](./Enums.md#enum-upgradelevelupclasspassives) | `Colorless` | Applies the 'UpgradeLevelUpClassPassives' effect. |
| `UpgradeSpawnedPickups` | Number | `2, 1` | Applies the 'UpgradeSpawnedPickups' effect. |
| `Vengeful` | Number | `1` | Applies the 'Vengeful' effect. |
| `WaterWalk` | Number | `1` | Applies the 'WaterWalk' effect. |
| `Weakness` | Number | `1, 5` | Applies the 'Weakness' effect. |
| `WeaponCountsAsBasicAttack` | Number | `1` | Applies the 'WeaponCountsAsBasicAttack' effect. |
| `WeaponDamageMultiplierBonus` | Number | `2` | Applies the 'WeaponDamageMultiplierBonus' effect. |
| `AddAllyNeighborsToAbilityRange` | Number | `1` | Applies the 'AddAllyNeighborsToAbilityRange' effect. |
| `AddAllyNeighborsToAttackRange` | Number | `1` | Applies the 'AddAllyNeighborsToAttackRange' effect. |
| `AddChaScalingSpellDamage` | Number | `3` | Applies the 'AddChaScalingSpellDamage' effect. |
| `AddKnockbackToEverything` | Number | `1` | Applies the 'AddKnockbackToEverything' effect. |
| `AddLevelUpStatMultiplier` | Number | `1` | Applies the 'AddLevelUpStatMultiplier' effect. |
| `AddRangedCritChance` | Number | `25%` | Applies the 'AddRangedCritChance' effect. |
| `AllDamageCrits` | Number | `1` | Applies the 'AllDamageCrits' effect. |
| `AlliesAvoidTraps` | Number | `1` | Applies the 'AlliesAvoidTraps' effect. |
| `AllyChainKnockback` | Number | `1` | Applies the 'AllyChainKnockback' effect. |
| `AllyMultiplyKnockbackDistance` | Number | `2` | Applies the 'AllyMultiplyKnockbackDistance' effect. |
| `AllyUncappedHPAura` | Number | `1` | Applies the 'AllyUncappedHPAura' effect. |
| `AlphaCat` | Number | `1` | Applies the 'AlphaCat' effect. |
| `AmplifyNegativeStatus` | Number | `1` | Applies the 'AmplifyNegativeStatus' effect. |
| `ArmorDodgeChance` | Number | `10%` | Applies the 'ArmorDodgeChance' effect. |
| `BackstabImmunity` | Number | `1` | Applies the 'BackstabImmunity' effect. |
| `BackstabWeakness` | Number | `0.75` | Applies the 'BackstabWeakness' effect. |
| `BasicAttackStatusSwap` | [`Array`](./Arrays.md#array-basicattackstatusswap) | `[ TempDamageUp DamageUp ]` | Applies the 'BasicAttackStatusSwap' effect. |
| `BlacklistPickupType` | [`Enum/String`](./Enums.md#enum-blacklistpickuptype) | `food` | Applies the 'BlacklistPickupType' effect. |
| `BleedThorns` | Number | `2` | Applies the 'BleedThorns' effect. |
| `BonusHealthRegenBasedOnDex` | Number | `5` | Applies the 'BonusHealthRegenBasedOnDex' effect. |
| `BonusRangeBasedOnDex` | Number | `5` | Applies the 'BonusRangeBasedOnDex' effect. |
| `BoostDamageAura` | Number | `1` | Applies the 'BoostDamageAura' effect. |
| `BoostDamageGlobalAura` | Number | `1` | Applies the 'BoostDamageGlobalAura' effect. |
| `BoostRangeAura` | Number | `1` | Applies the 'BoostRangeAura' effect. |
| `BoostRangeGlobalAura` | Number | `1` | Applies the 'BoostRangeGlobalAura' effect. |
| `BuffImmunity` | Number | `1` | Applies the 'BuffImmunity' effect. |
| `Burn` | Number | `1` | Applies the 'Burn' effect. |
| `CanRemoveCursedItems` | Number | `1` | Applies the 'CanRemoveCursedItems' effect. |
| `CantDodge` | Number | `1` | Applies the 'CantDodge' effect. |
| `CapMovementAbilityRange` | Number | `1` | Applies the 'CapMovementAbilityRange' effect. |
| `CapTechSpent` | Number | `0` | Applies the 'CapTechSpent' effect. |
| `ConductorManaRegen` | Number | `2` | Applies the 'ConductorManaRegen' effect. |
| `ConfusionEffectOnTaggedAbilities` | [`Enum/String`](./Enums.md#enum-confusioneffectontaggedabilities) | `consumable` | Applies the 'ConfusionEffectOnTaggedAbilities' effect. |
| `ConsumablesMeleeRange` | Number | `1` | Applies the 'ConsumablesMeleeRange' effect. |
| `DepressionAura` | Number | `2` | Applies the 'DepressionAura' effect. |
| `DisableAbilities` | [`Enum/String`](./Enums.md#enum-disableabilities) | `all_items` | Applies the 'DisableAbilities' effect. |
| `DisableAbilitiesWithTag` | [`Enum/String`](./Enums.md#enum-disableabilitieswithtag) | `meat` | Applies the 'DisableAbilitiesWithTag' effect. |
| `Doomed` | Number | `3` | Applies the 'Doomed' effect. |
| `EachSpellFreeAtFullMana` | Number | `1` | Applies the 'EachSpellFreeAtFullMana' effect. |
| `EquipRandomTemporaryItemFromPool` | [`Enum/String`](./Enums.md#enum-equiprandomtemporaryitemfrompool) | `weapons` | Applies the 'EquipRandomTemporaryItemFromPool' effect. |
| `ExhaustionRoundChange` | Number | `3` | Applies the 'ExhaustionRoundChange' effect. |
| `ExplosionImmunity` | Number | `1` | Applies the 'ExplosionImmunity' effect. |
| `ExtraBasicMoves_Status` | Number | `1` | Applies the 'ExtraBasicMoves_Status' effect. |
| `ExtraInjuryOnDeath` | Number | `1` | Applies the 'ExtraInjuryOnDeath' effect. |
| `ExtraTrinketUses` | Number | `1` | Applies the 'ExtraTrinketUses' effect. |
| `FaceArmorPassiveMultiplierBonus` | Number | `2` | Applies the 'FaceArmorPassiveMultiplierBonus' effect. |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `MockingbirdForm` | Applies the 'ForceUseAbility' effect. |
| `FreeSpellsAtFullMana` | Number | `1` | Applies the 'FreeSpellsAtFullMana' effect. |
| `FrontstabBasicAttackCritChance` | Number | `100%` | Applies the 'FrontstabBasicAttackCritChance' effect. |
| `FrontstabCritChance` | Number | `100%` | Applies the 'FrontstabCritChance' effect. |
| `FullHeal` | Number | `1` | Applies the 'FullHeal' effect. |
| `FullHealthAllStatsUp` | Number | `1` | Applies the 'FullHealthAllStatsUp' effect. |
| `FullHealthManaRegen` | Number | `5` | Applies the 'FullHealthManaRegen' effect. |
| `GrassTileHealing` | Number | `1` | Applies the 'GrassTileHealing' effect. |
| `HPGainBlock` | Number | `1` | Applies the 'HPGainBlock' effect. |
| `HealAtStart` | Number | `100%` | Applies the 'HealAtStart' effect. |
| `HealingAura` | Number | `1` | Applies the 'HealingAura' effect. |
| `HolyDamageMultiplierBonus` | Number | `1` | Applies the 'HolyDamageMultiplierBonus' effect. |
| `HouseFoodRequirementMultiplier` | Number | `0` | Applies the 'HouseFoodRequirementMultiplier' effect. |
| `Hypomania` | Number | `3` | Applies the 'Hypomania' effect. |
| `IncreaseItemUsesOnEquip` | Number | `1` | Applies the 'IncreaseItemUsesOnEquip' effect. |
| `InjuryImmunity` | Number | `1` | Applies the 'InjuryImmunity' effect. |
| `InvertBrainFaction` | Number | `1` | Applies the 'InvertBrainFaction' effect. |
| `LimitDamage` | Number | `1` | Applies the 'LimitDamage' effect. |
| `LimitHeal` | Number | `1` | Applies the 'LimitHeal' effect. |
| `LimitSelfKnockbackDamage` | Number | `1` | Applies the 'LimitSelfKnockbackDamage' effect. |
| `LimitedTileTrail` | [`Enum/String`](./Enums.md#enum-limitedtiletrail) | `FlowerTile` | Applies the 'LimitedTileTrail' effect. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `ManaCostReduction` | Number | `25%` | Applies the 'ManaCostReduction' effect. |
| `MaxAccuracy` | Number | `1` | Applies the 'MaxAccuracy' effect. |
| `MaxStartingMana` | Number | `1` | Applies the 'MaxStartingMana' effect. |
| `MoveAwayFromDamageSource` | [`Enum/String`](./Enums.md#enum-moveawayfromdamagesource) | `MoveOne` | Applies the 'MoveAwayFromDamageSource' effect. |
| `MoveRandomly` | Number | `1` | Applies the 'MoveRandomly' effect. |
| `MoveSpeedMultiplier` | [`Enum/String`](./Enums.md#enum-movespeedmultiplier) | `.5` | Applies the 'MoveSpeedMultiplier' effect. |
| `NeckArmorPassiveMultiplierBonus` | Number | `2` | Applies the 'NeckArmorPassiveMultiplierBonus' effect. |
| `NoManaRegen` | Number | `1` | Applies the 'NoManaRegen' effect. |
| `OverrideMaxHealth` | Number | `1` | Applies the 'OverrideMaxHealth' effect. |
| `OverrideMaxMana` | Number | `1` | Applies the 'OverrideMaxMana' effect. |
| `OverridePalette` | Number | `87` | Applies the 'OverridePalette' effect. |
| `Paranoia` | [`Enum/String`](./Enums.md#enum-paranoia) | `ParanoiaBasicMelee` | Applies the 'Paranoia' effect. |
| `PermanentImmobile` | Number | `1` | Applies the 'PermanentImmobile' effect. |
| `PermanentKitten` | Number | `1` | Applies the 'PermanentKitten' effect. |
| `PermanentMadness` | Number | `1` | Applies the 'PermanentMadness' effect. |
| `Phasing` | Number | `1` | Applies the 'Phasing' effect. |
| `Poison` | Number | `1` | Applies the 'Poison' effect. |
| `PoisonMultiplier` | Number | `2` | Applies the 'PoisonMultiplier' effect. |
| `PoopWhenHit` | [`Enum/String`](./Enums.md#enum-poopwhenhit) | `Poop` | Applies the 'PoopWhenHit' effect. |
| `RealTimePressure_OneUnit` | Number | `5` | Applies the 'RealTimePressure_OneUnit' effect. |
| `ReceivedStatusReplacement` | [`Array`](./Arrays.md#array-receivedstatusreplacement) | `[ Sleep SleepParalysis ]` | Applies the 'ReceivedStatusReplacement' effect. |
| `RefreshMoveOnWeaponConnect` | Number | `1` | Applies the 'RefreshMoveOnWeaponConnect' effect. |
| `ReplaceSpellsWhenDead` | [`Enum/String`](./Enums.md#enum-replacespellswhendead) | `Spook` | Applies the 'ReplaceSpellsWhenDead' effect. |
| `SafeExplosions` | Number | `1` | Applies the 'SafeExplosions' effect. |
| `SchrodingerDisorder` | Number | `50%` | Applies the 'SchrodingerDisorder' effect. |
| `Scleroderma` | Number | `1` | Applies the 'Scleroderma' effect. |
| `SetDefaultFacePassive` | [`Enum/String`](./Enums.md#enum-setdefaultfacepassive) | `insane` | Applies the 'SetDefaultFacePassive' effect. |
| `Slow` | Number | `5` | Applies the 'Slow' effect. |
| `SmallRockBehavior` | Number | `5` | Applies the 'SmallRockBehavior' effect. |
| `SpawnCreepOnHit` | Number | `1` | Applies the 'SpawnCreepOnHit' effect. |
| `SpawnMeatOnMove` | [`Enum/String`](./Enums.md#enum-spawnmeatonmove) | `Food` | Applies the 'SpawnMeatOnMove' effect. |
| `SpreadPainBonusCrit` | Number | `1` | Applies the 'SpreadPainBonusCrit' effect. |
| `StatusCarefulness` | Number | `1` | Event Trigger: Applies nested statuses to carefulness. |
| `StrictLimitDamage` | Number | `1` | Applies the 'StrictLimitDamage' effect. |
| `TauntAtFullHealth` | Number | `1` | Applies the 'TauntAtFullHealth' effect. |
| `TempInitiativeChange` | Number | `-999` | Applies the 'TempInitiativeChange' effect. |
| `Triskaidekaphobia` | Number | `13` | Applies the 'Triskaidekaphobia' effect. |
| `UncappedHPBonusStr` | Number | `5` | Applies the 'UncappedHPBonusStr' effect. |
| `Vegan` | Number | `1` | Applies the 'Vegan' effect. |
| `WeaponActiveEffectsMultiplierBonus` | Number | `2` | Applies the 'WeaponActiveEffectsMultiplierBonus' effect. |
| `WeaponPassiveMultiplierBonus` | Number | `2` | Applies the 'WeaponPassiveMultiplierBonus' effect. |
| `WeaponsDontLoseDurability` | Number | `0` | Applies the 'WeaponsDontLoseDurability' effect. |
| `WobblyCat` | Number | `25%` | Applies the 'WobblyCat' effect. |

</details>

---

### Context: `2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"PASSIVE_MAINCOURSE2_DESC", "PASSIVE_PUTREFY2_DESCRIPTION", "PASSIVE_NEVERFULL2_DESC"` | Localization key for the passive's display description. |
| `desc_multiclass` | String | `"PASSIVE_HOOKED2_MULTICLASS_DESC", "PASSIVE_GRAPPLINGHOOK2_MULTICLASS_DESC", "PASSIVE_BARBED2_MULTICLASS_DESC"` |  |
| `override_basic_attack` | [`Enum/String`](./Enums.md#enum-override_basic_attack) | `BasicButcherMeleeWideDoubleSpin, BasicDruidAbilityVersatile, BasicMagicMissile` |  |
| `shield` | Number | `8, 4` |  |
| `bonus_items` | [`Array`](./Arrays.md#array-bonus_items) | `[ SpiderWebber ], [ Stick Stick Stick ], [ FoodBig FoodBig FoodBig FoodBig ]` | Flat addition to a base value. |
| `divine_shield` | Number | `1, 3` |  |
| `icon` | [`Enum/String`](./Enums.md#enum-icon) | `DejaVu2` |  |

</details>

---

### Context: `stats`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2, -2, -1` |  |
| `spd` | Number | `2, 1, 3` |  |
| `cha` | Number | `2, 3, 4` |  |
| `int` | Number | `2, -2, -1` |  |
| `str` | Number | `2, 4, -1` |  |
| `dex` | Number | `6, 3, -1` |  |
| `lck` | Number | `2, 1, 4` |  |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Poison` | Number | `1, [ 1 .5 ], 3` | Applies the 'Poison' effect. |
| `Bleed` | Number | `2, 1` | Applies the 'Bleed' effect. |
| `Knockback` | Number | `1, 3, 4` | Applies the 'Knockback' effect. |
| `Bruise` | Number | `2, 1` | Applies the 'Bruise' effect. |
| `Conditional_Ally` | [`Block`](./Passives_and_Statuses.md#context-conditional_ally) | `{ ... }` | Conditional trigger: Executes nested logic if the target is friendly to the caster. |
| `BounceObject` | [`Enum/String`](./Enums.md#enum-bounceobject) | `CharmedLeech, BeefyCharmedLeech, AllyRotFly` | Spawns a physics object that visually bounces off the target. |
| `Weakness` | Number | `1` | Applies the 'Weakness' effect. |
| `Burn` | Number | `2, 1, 5` | Applies the 'Burn' effect. |
| `Leech` | Number | `1` | Applies the 'Leech' effect. |
| `Piercing` | Number | `1` | Applies the 'Piercing' effect. |
| `Slow` | Number | `2, 1, 5` | Applies the 'Slow' effect. |
| `BurgleCoin` | Number | `1` | Applies the 'BurgleCoin' effect. |
| `ChangeTile` | [`Block`](./Passives_and_Statuses.md#context-changetile) | `{ ... }, BrambleTile` | Transforms the terrain tile under the target. |
| `Charmed` | [`Array`](./Arrays.md#array-charmed) | `[ 1 .25 ]` | Applies the 'Charmed' effect. |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1 .25 ]` | Applies the 'Fear' effect. |
| `Freeze` | [`Array`](./Arrays.md#array-freeze) | `[ 1 .20 ], [ 1 .5 ]` | Applies the 'Freeze' effect. |
| `KnockOutCoin` | Number | `1, [ 1 .5 ]` | Forces the target to drop coins. |
| `LuckUp` | Number | `-1` | Applies the 'LuckUp' effect. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `MagicWeakness` | Number | `2, 1` | Applies the 'MagicWeakness' effect. |
| `Rot` | Number | `-999999, 1` | Applies the 'Rot' effect. |
| `SoulLink` | Number | `1` | Applies the 'SoulLink' effect. |
| `SpawnBearTrapOnMiss` | Number | `1` | Applies the 'SpawnBearTrapOnMiss' effect. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .15 ], [ 1 .40 ]` | Applies the 'Stun' effect. |
| `ApplyToSource` | [`Block`](./Passives_and_Statuses.md#context-applytosource) | `{ ... }` | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| `BigSplashDamage` | Number | `2` | Applies the 'BigSplashDamage' effect. |
| `Blind` | Number | `1` | Applies the 'Blind' effect. |
| `Confusion` | Number | `1` | Applies the 'Confusion' effect. |
| `DamageOrHealConditionally` | Number | `1` | Combat Trigger: Deals damage to or heal conditionally. |
| `Else` | [`Block`](./Passives_and_Statuses.md#context-else) | `{ ... }` | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `Leeches` | Number | `1` | Applies the 'Leeches' effect. |
| `ManaLeeches` | Number | `1` | Applies the 'ManaLeeches' effect. |
| `OverrideChainKnockback` | Number | `0` | Applies the 'OverrideChainKnockback' effect. |
| `OverrideChainKnockbackDamage` | Number | `0` | Applies the 'OverrideChainKnockbackDamage' effect. |
| `SplashDamage` | Number | `2` | Applies the 'SplashDamage' effect. |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1, -1` | Applies the 'AllStatsUp' effect. |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `BleedThorns` | Number | `1` | Applies the 'BleedThorns' effect. |
| `Blind` | Number | `1` | Applies the 'Blind' effect. |
| `Brace` | Number | `1` | Applies the 'Brace' effect. |
| `Bruise` | Number | `1` | Applies the 'Bruise' effect. |
| `Burn` | Number | `1` | Applies the 'Burn' effect. |
| `Charge` | Number | `1` | Applies the 'Charge' effect. |
| `Charmed` | Number | `1` | Applies the 'Charmed' effect. |
| `Confusion` | Number | `1` | Applies the 'Confusion' effect. |
| `DiminishingHealthRegen` | Number | `1` | Applies the 'DiminishingHealthRegen' effect. |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `Fear` | Number | `1` | Applies the 'Fear' effect. |
| `Freeze` | Number | `1` | Applies the 'Freeze' effect. |
| `Immobile` | Number | `1` | Applies the 'Immobile' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `MagicWeakness` | Number | `1` | Applies the 'MagicWeakness' effect. |
| `Marked` | Number | `1` | Applies the 'Marked' effect. |
| `MoveQuivered` | Number | `1` | Applies the 'MoveQuivered' effect. |
| `ObjectOnHitCharacter` | [`Enum/String`](./Enums.md#enum-objectonhitcharacter) | `CharmedLeech, BeefyCharmedLeech` | Spawns a specific character or entity upon impact. |
| `Petrify` | Number | `1` | Applies the 'Petrify' effect. |
| `Poison` | Number | `1` | Applies the 'Poison' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `Reflect` | Number | `1` | Applies the 'Reflect' effect. |
| `Shield` | Number | `1` | Applies the 'Shield' effect. |
| `Sleep` | Number | `1` | Applies the 'Sleep' effect. |
| `Slow` | Number | `1` | Applies the 'Slow' effect. |
| `Stun` | Number | `1` | Applies the 'Stun' effect. |
| `Tarred` | Number | `1` | Applies the 'Tarred' effect. |
| `Thorns` | Number | `1` | Applies the 'Thorns' effect. |
| `Weakness` | Number | `1` | Applies the 'Weakness' effect. |
| `ConstitutionUp` | Number | `1` | Applies the 'ConstitutionUp' effect. |
| `SpawnCoinAnywhere` | Number | `1` | Applies the 'SpawnCoinAnywhere' effect. |
| `SpeedUp` | Number | `1` | Applies the 'SpeedUp' effect. |
| `StrengthUp` | Number | `1` | Applies the 'StrengthUp' effect. |

</details>

---

### Context: `Temporary`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `2, 1, 5` | The number of stacks, duration, or intensity to apply. |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Brace, Thorns, Uncontrollable` | The status effect to apply. |
| `turns` | Number | `1` | Duration in turns. |
| `expires_on_end_turn` | Boolean | `true` |  |
| `expires_on_begin_turn` | Boolean | `true` | If true, ticks down at the start of the turn rather than the end. |

</details>

---

### Context: `AddPassivesToMinions`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `2, 3` | Combat Trigger: Deals damage to up. |
| `IncreaseExplosionDamage` | Number | `2, 3, 4` | Applies the 'IncreaseExplosionDamage' effect. |
| `FreePathfindElement` | [`Enum/String`](./Enums.md#enum-freepathfindelement) | `Grass, Water` | Applies the 'FreePathfindElement' effect. |
| `AddMaxHealth` | Number | `10, 5` | Applies the 'AddMaxHealth' effect. |
| `AddSpeed` | Number | `4` | Applies the 'AddSpeed' effect. |
| `FamiliarBonusAbility` | [`Enum/String`](./Enums.md#enum-familiarbonusability) | `FamiliarSelfDestruct, FamiliarSelfDestruct2` | Applies the 'FamiliarBonusAbility' effect. |
| `ForceAttack` | Number | `1` | Forces the character to execute an immediate attack. |
| `HealthGain` | Number | `10, 5` | Applies the 'HealthGain' effect. |
| `HealthRegenUp` | Number | `3` | Applies the 'HealthRegenUp' effect. |
| `HolyShieldTransferToSpawner` | Number | `1` | Applies the 'HolyShieldTransferToSpawner' effect. |
| `IncreaseExplosionSize` | Number | `2` | Applies the 'IncreaseExplosionSize' effect. |
| `PoisonThorns` | Number | `2, 1` | Applies the 'PoisonThorns' effect. |
| `WaterWalk` | Number | `1` | Applies the 'WaterWalk' effect. |
| `tag_filter` | [`Enum/String`](./Enums.md#enum-tag_filter) | `crow` |  |
| `AddUnfilledMaxHealth` | Number | `10` | Applies the 'AddUnfilledMaxHealth' effect. |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `GrassTileHealing` | Number | `1` | Applies the 'GrassTileHealing' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `SafeExplosions` | Number | `1` | Applies the 'SafeExplosions' effect. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |
| `UncappedHP` | Number | `1` | Applies the 'UncappedHP' effect. |

</details>

---

### Context: `effects`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `VisualFXTile` | [`Enum/String`](./Enums.md#enum-visualfxtile) | `WaterConduct, IcePoof, BurnTrigger` | Applies the 'VisualFXTile' effect. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1, .05*X ], 1, [ 1, .05 ]` | Applies the 'Stun' effect. |
| `Freeze` | [`Array`](./Arrays.md#array-freeze) | `[ 1, .05 ], [ 1, .15 ]` | Applies the 'Freeze' effect. |
| `Burn` | Number | `1` | Applies the 'Burn' effect. |
| `Charmed` | [`Array`](./Arrays.md#array-charmed) | `[ 1, .40 ], [ 1, .25 ]` | Applies the 'Charmed' effect. |
| `Petrify` | [`Array`](./Arrays.md#array-petrify) | `[ 1, .1 ], [ 1, .2 ]` | Applies the 'Petrify' effect. |
| `Poison` | Number | `1` | Applies the 'Poison' effect. |
| `Slow` | Number | `2` | Applies the 'Slow' effect. |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `Bruise` | Number | `1` | Applies the 'Bruise' effect. |
| `Fear` | Number | `1` | Applies the 'Fear' effect. |
| `Immobile` | Number | `1` | Applies the 'Immobile' effect. |
| `Leeches` | Number | `1` | Applies the 'Leeches' effect. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `Marked` | Number | `1` | Applies the 'Marked' effect. |
| `Weakness` | Number | `1` | Applies the 'Weakness' effect. |

</details>

---

### Context: `SpreadDisease`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `disease` | [`Enum/String`](./Enums.md#enum-disease) | `CommonCold, Pox, Rabies` | The specific status effect ID representing the disease. |
| `chance` | Number | `25%, 50%, 100%` | Probability (0.0 to 1.0 or percentage) of transmitting. |
| `can_apply_to_anything` | Boolean | `true` |  |

</details>

---

### Context: `SpawnOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `SmallRock, [ BuffFamiliarMaggot BuffFamiliarPooter BuffFamiliarFlea ..., CharmedFlea` |  |
| `number` | Number | `1, [ 2 3 ], 3` |  |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Block`](./Passives_and_Statuses.md#context-forceuseability) | `{ ... }, MiniFart, Rest` | Applies the 'ForceUseAbility' effect. |
| `NonStackingDivineShield` | Number | `1` | Applies the 'NonStackingDivineShield' effect. |
| `SpeedUp` | Number | `-2, 1` | Applies the 'SpeedUp' effect. |
| `EmptyMana` | Number | `1` | Applies the 'EmptyMana' effect. |
| `RangeUp` | Number | `1` | Applies the 'RangeUp' effect. |
| `IntelligenceUp` | Number | `1` | Applies the 'IntelligenceUp' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |
| `PermanentMadness` | Number | `1` | Applies the 'PermanentMadness' effect. |
| `StrengthUp` | Number | `1` | Applies the 'StrengthUp' effect. |
| `UseAbility_Madness` | [`Enum/String`](./Enums.md#enum-useability_madness) | `weapon` | Applies the 'UseAbility_Madness' effect. |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | `true` | If true, triggers the effect even if the character died during the battle. |
| `FindItemFromPool` | [`Block`](./Passives_and_Statuses.md#context-finditemfrompool) | `{ ... }, chapter, consumables` | Generates an item drop from the specified loot pool. |
| `RandomPermanentStat` | Number | `1, 3, -3` | Applies the 'RandomPermanentStat' effect. |
| `PermanentSpeed` | Number | `-1` | Applies the 'PermanentSpeed' effect. |
| `RandomMutation` | Number | `1` | Applies the 'RandomMutation' effect. |
| `PermanentConstitution` | Number | `-1` | Applies the 'PermanentConstitution' effect. |
| `PermanentIntelligence` | Number | `-1` | Applies the 'PermanentIntelligence' effect. |
| `PermanentStrength` | Number | `2` | Applies the 'PermanentStrength' effect. |

</details>

---

### Context: `DamageNeighborsOnEndMove`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status` | The classification type (e.g., damage type or element). |
| `cant_miss` | Boolean | `true` |  |
| `knockback` | Number | `1` |  |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | `2, 1` | Applies the 'SpeedUp' effect. |
| `ConstitutionUp` | Number | `1, -1` | Applies the 'ConstitutionUp' effect. |
| `DamageUp` | Number | `2, 1` | Combat Trigger: Deals damage to up. |
| `IntelligenceUp` | Number | `-2, -1` | Applies the 'IntelligenceUp' effect. |
| `Shield` | Number | `2, 1` | Applies the 'Shield' effect. |
| `StrengthUp` | Number | `1, -1` | Applies the 'StrengthUp' effect. |
| `TempDamageUp` | Number | `2, 1` | Applies the 'TempDamageUp' effect. |
| `DiminishingHealthRegen` | Number | `1` | Applies the 'DiminishingHealthRegen' effect. |
| `MovementUp` | Number | `1` | Applies the 'MovementUp' effect. |
| `RandomInjury` | Number | `1` | Applies the 'RandomInjury' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |
| `TempMovement` | Number | `1` | Applies the 'TempMovement' effect. |
| `Thorns` | Number | `1` | Applies the 'Thorns' effect. |

</details>

---

### Context: `lock_item_slot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `slot` | [`Enum/String`](./Enums.md#enum-slot) | `neck, face, trinket` |  |
| `frame` | Number | `11, 16, 17` |  |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `1` | Combat Trigger: Deals damage to up. |
| `EquipPermanentItem` | [`Enum/String`](./Enums.md#enum-equippermanentitem) | `BoneClub` | Applies the 'EquipPermanentItem' effect. |
| `RefreshActPoints` | Number | `1` | Applies the 'RefreshActPoints' effect. |
| `RefreshMovePoints` | Number | `1` | Applies the 'RefreshMovePoints' effect. |
| `StrengthUp` | Number | `2` | Applies the 'StrengthUp' effect. |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `HealthGain` | Number | `5` | Applies the 'HealthGain' effect. |
| `LuckUp` | Number | `2` | Applies the 'LuckUp' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |
| `SpeedUp` | Number | `2` | Applies the 'SpeedUp' effect. |
| `Stealth` | Number | `1` | Applies the 'Stealth' effect. |

</details>

---

### Context: `StatusOnUseAbilityWithTag`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `shapeshift, musical` | The specific entity tag required or applied. |
| `RefreshActPoints` | Number | `1` | Applies the 'RefreshActPoints' effect. |
| `DamageUp` | Number | `1` | Combat Trigger: Deals damage to up. |
| `exclude_basicattack` | Boolean | `true` |  |
| `HealthGain` | Number | `1` | Applies the 'HealthGain' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |

</details>

---

### Context: `spell_graphics_override`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `area_particle` | [`Enum/String`](./Enums.md#enum-area_particle) | `WaterConduct` |  |
| `center_particle` | [`Enum/String`](./Enums.md#enum-center_particle) | `WaterConduct` |  |
| `palette` | Number | `-1` |  |
| `particle` | [`Enum/String`](./Enums.md#enum-particle) | `WaterConduct` |  |

</details>

---

### Context: `1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `bonus_items` | [`Array`](./Arrays.md#array-bonus_items) | `[ Pipe ], [ Stick Stick Stick ], [ SpiderEgg ]` | Flat addition to a base value. |
| `override_basic_attack` | [`Enum/String`](./Enums.md#enum-override_basic_attack) | `BasicDruidAbilityVersatile, BasicButcherMeleeWideSpin, BasicMagicMissile` |  |
| `divine_shield` | Number | `1` |  |
| `shield` | Number | `2, 4` |  |
| `desc` | String | `"DISORDER_DEJAVU_DESC"` | Localization key for the passive's display description. |

</details>

---

### Context: `CritsApplyStatus`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ObjectOnHitCharacter` | [`Enum/String`](./Enums.md#enum-objectonhitcharacter) | `RandomPickup, Coin` | Spawns a specific character or entity upon impact. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .25 ], [ 1 .33 ], 1` | Applies the 'Stun' effect. |
| `Weakness` | Number | `2, 1` | Applies the 'Weakness' effect. |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `Bruise` | Number | `1` | Applies the 'Bruise' effect. |
| `Confusion` | Number | `1` | Applies the 'Confusion' effect. |
| `Immobile` | Number | `1` | Applies the 'Immobile' effect. |

</details>

---

### Context: `StatusOnStanceSwitch`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `RapidFlowSpin, RapidFlowSpin2` | Applies the 'ForceUseAbility' effect. |
| `NextBasicAttackCritsThisTurn` | Number | `1` | Guarantees the next basic attack executed this turn will be a critical hit. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |
| `Shield` | Number | `2, 3` | Applies the 'Shield' effect. |
| `PartialCleanse` | Number | `1` | Applies the 'PartialCleanse' effect. |

</details>

---

### Context: `SpawnEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Array`](./Arrays.md#array-object) | `[ CharmedTumorousMaggot CharmedChargeyMaggot CharmedSwapp..., CharmedFlea, CharmedMaggot` |  |
| `chance` | Number | `50%, .5, 15%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |
| `number` | Number | `1` |  |
| `good` | Boolean | `false` |  |

</details>

---

### Context: `Conditional_Ally`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1, [ 1 .5 ]` | Applies the 'AllStatsUp' effect. |
| `Cleanse` | Number | `0` | Applies the 'Cleanse' effect. |
| `ClearNegativeEffects` | Number | `1` | Applies the 'ClearNegativeEffects' effect. |
| `DamageUp` | Number | `1` | Combat Trigger: Deals damage to up. |
| `Shield` | Number | `2, 3` | Applies the 'Shield' effect. |
| `TempSpeedUp` | Number | `4` | Applies the 'TempSpeedUp' effect. |
| `SpeedUp` | Number | `1` | Applies the 'SpeedUp' effect. |

</details>

---

### Context: `CureDisease`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `5%, 30%, 15%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |
| `disease` | [`Enum/String`](./Enums.md#enum-disease) | `Ebola, Pox, CommonCold` |  |
| `can_apply_to_anything` | Boolean | `true` |  |

</details>

---

### Context: `StatusOnTurnEndIfManaOrHealthExact`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `mana` | Number | `5, 4` |  |
| `IntelligenceUp` | Number | `1` | Applies the 'IntelligenceUp' effect. |
| `Shield` | Number | `5` | Applies the 'Shield' effect. |
| `SpellDamageUp` | Number | `1` | Applies the 'SpellDamageUp' effect. |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `HealthGain` | Number | `5` | Applies the 'HealthGain' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |

</details>

---

### Context: `AddStatusToExplosions`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddElement` | [`Enum/String`](./Enums.md#enum-addelement) | `Napalm, Fire` | Applies the 'AddElement' effect. |
| `Burn` | Number | `6, 3` | Applies the 'Burn' effect. |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | `1` | Applies the 'Charmed' effect. |
| `OverrideDamage` | Number | `0` | Applies the 'OverrideDamage' effect. |
| `Revive` | Number | `1` | Applies the 'Revive' effect. |
| `SafeDoomed` | Number | `1` | Applies the 'SafeDoomed' effect. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |
| `DamageUp` | Number | `2` | Combat Trigger: Deals damage to up. |
| `SpeedUp` | Number | `8` | Applies the 'SpeedUp' effect. |

</details>

---

### Context: `ManaCostReductionTagged`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `reduction` | Number | `50%, 1, 3` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `summon, musical` | The specific entity tag required or applied. |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CharmedLeech, Food, PoisonFood` |  |
| `good` | Boolean | `false, true` |  |
| `spawn_on_death_hit` | Boolean | `false` |  |
| `consider_all_layers` | Boolean | `true` |  |

</details>

---

### Context: `StatusAlliesOnDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `HealAndOverhealToShield` | Number | `12, 20` | Applies the 'HealAndOverhealToShield' effect. |
| `Reanimate` | Number | `100%, 33%` | Applies the 'Reanimate' effect. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |
| `triggers_limit` | Number | `1` |  |
| `Freeze` | Number | `1` | Applies the 'Freeze' effect. |
| `FullHeal` | Number | `1` | Applies the 'FullHeal' effect. |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `1, 0, 3` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Ice ], [ Fire ]` |  |
| `Poison` | Number | `3` | Applies the 'Poison' effect. |
| `SpreadDisease` | [`Block`](./Passives_and_Statuses.md#context-spreaddisease) | `{ ... }` | Provides a chance to transmit a disease status to adjacent targets. |
| `Weakness` | Number | `1` | Applies the 'Weakness' effect. |

</details>

---

### Context: `StatusOnDealtDamageThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RefreshMovePoints` | Number | `1` | Applies the 'RefreshMovePoints' effect. |
| `Shield` | Number | `2` | Applies the 'Shield' effect. |
| `count_overkill` | Boolean | `true` |  |
| `ignore_during_movement` | Boolean | `true` |  |
| `threshold` | Number | `10` |  |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |

</details>

---

### Context: `Else`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Number | `1` | Applies the 'CaptureFamiliar' effect. |
| `FactionConversion` | Number | `1` | Applies the 'FactionConversion' effect. |
| `Marked` | Number | `1` | Applies the 'Marked' effect. |
| `PermanentCharm` | Number | `1` | Applies the 'PermanentCharm' effect. |
| `Fear` | Number | `1` | Applies the 'Fear' effect. |
| `TempSpeedUp` | Number | `4` | Applies the 'TempSpeedUp' effect. |

</details>

---

### Context: `PassiveAtStatThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `mode` | [`Enum/String`](./Enums.md#enum-mode) | `less_or_equal` |  |

</details>

---

### Context: `StatusEveryXSpellCasts`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `6, 3` | The number of stacks, duration, or intensity to apply. |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `SpellDamageUp` | Number | `1` | Applies the 'SpellDamageUp' effect. |
| `ReduceManaCost` | Number | `1` | Applies the 'ReduceManaCost' effect. |
| `RepairWeapon` | Number | `1` | Applies the 'RepairWeapon' effect. |
| `RepairWeaponCondition` | Number | `1` | Applies the 'RepairWeaponCondition' effect. |

</details>

---

### Context: `StatusOnTurnEndIfManaExact`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `mana` | Number | `2, 0` |  |
| `FreeSpell` | Number | `1` | Applies the 'FreeSpell' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `MoveQuivered` | Number | `1` | Applies the 'MoveQuivered' effect. |
| `SpellDamageUp` | Number | `1` | Applies the 'SpellDamageUp' effect. |

</details>

---

### Context: `threshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `int` | Number | `-10, 0, 4` |  |
| `cha` | Number | `0` |  |
| `spd` | Number | `0` |  |

</details>

---

### Context: `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | `1` | Applies the 'Confusion' effect. |
| `Bruise` | Number | `1` | Applies the 'Bruise' effect. |
| `FaceAway` | Number | `1` | Applies the 'FaceAway' effect. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .15 ], [ 1 .2 ]` | Applies the 'Stun' effect. |

</details>

---

### Context: `AddStatusToElementAbilities`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Gravity` | The specific element type required or applied. |
| `ChangeTile` | [`Enum/String`](./Enums.md#enum-changetile) | `FloatingGlassTile` | Transforms the terrain tile under the target. |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |

</details>

---

### Context: `PassiveIfAllArmorEmpty`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddSpellDamage` | Number | `2, 1` | Applies the 'AddSpellDamage' effect. |
| `CounterAttack` | [`Enum/String`](./Enums.md#enum-counterattack) | `attack` | Applies the 'CounterAttack' effect. |
| `ExtraMovePoints` | Number | `1` | Applies the 'ExtraMovePoints' effect. |
| `ManaCostReduction` | Number | `1` | Applies the 'ManaCostReduction' effect. |
| `Flying` | Number | `1` | Applies the 'Flying' effect. |

</details>

---

### Context: `StatusOnCrit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | `1` | Applies the 'LuckUp' effect. |
| `DamageUp` | Number | `1` | Combat Trigger: Deals damage to up. |
| `Shield` | Number | `2, 3` | Applies the 'Shield' effect. |
| `CritChanceUp` | Number | `5` | Applies the 'CritChanceUp' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |

</details>

---

### Context: `StatusOnTurnEndIfCastNSpells`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spells` | Number | `2, 1` |  |
| `DoubleCastSpell` | Number | `2, 1` | Applies the 'DoubleCastSpell' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `MoveQuivered` | Number | `1` | Applies the 'MoveQuivered' effect. |

</details>

---

### Context: `schadenfreude_scaled_stats`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2` |  |
| `str` | Number | `2` |  |
| `cha` | Number | `2` |  |
| `dex` | Number | `2` |  |
| `int` | Number | `2` |  |
| `lck` | Number | `2` |  |
| `spd` | Number | `2` |  |

</details>

---

### Context: `AddDamageToElementDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `2, 1` | The base damage properties of an attack. |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Electric, Fire` | The specific element type required or applied. |

</details>

---

### Context: `AllyManaRegenAura`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `range` | [`Enum/String`](./Enums.md#enum-range) | `global` | Distance or area of effect in tiles. |
| `stacks` | Number | `2, 1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MedicObey, RaiseTheDead, MedicObey2` | The ID of the ability to autocast. |
| `even_if_stunned` | Boolean | `true` | If true, bypasses stun and hard-CC restrictions to cast anyway. |
| `force_display_name` | Boolean | `true` |  |

</details>

---

### Context: `DistanceBonusDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `min_range` | Number | `1, 3` |  |
| `stacks` | Number | `1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `GravityWell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | `true` |  |
| `damage` | Number | `0, 5` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Gravity ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `PassiveAtHealthThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `mode` | [`Enum/String`](./Enums.md#enum-mode) | `less_or_equal, equal` |  |
| `threshold` | Number | `1, 5` |  |

</details>

---

### Context: `StatusIfUnusedMovePoints`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `8` | Applies the 'HealthGain' effect. |
| `MoveQuivered` | Number | `2` | Applies the 'MoveQuivered' effect. |
| `Brace` | Number | `1` | Applies the 'Brace' effect. |
| `ConstitutionUp` | Number | `2` | Applies the 'ConstitutionUp' effect. |
| `ManaGain` | Number | `5` | Applies the 'ManaGain' effect. |
| `Shield` | Number | `2` | Applies the 'Shield' effect. |

</details>

---

### Context: `AddSelfStatusToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |

</details>

---

### Context: `CatchProjectiles`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `ally_chance` | Number | `100%` |  |
| `chance` | Number | `50%, 33%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |

</details>

---

### Context: `PassiveIfEmptyFace`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | `25%, 40%` | Applies the 'AddCritMultiplier' effect. |
| `CritChanceUp` | Number | `10` | Applies the 'CritChanceUp' effect. |
| `DodgeChance` | Number | `15%, 10%` | Applies the 'DodgeChance' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |

</details>

---

### Context: `PassiveIfEmptyHead`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | `25%, 40%` | Applies the 'AddCritMultiplier' effect. |
| `CritChanceUp` | Number | `10` | Applies the 'CritChanceUp' effect. |
| `DodgeChance` | Number | `15%, 10%` | Applies the 'DodgeChance' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |

</details>

---

### Context: `PassiveIfEmptyNeck`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddCritMultiplier` | Number | `25%, 40%` | Applies the 'AddCritMultiplier' effect. |
| `CritChanceUp` | Number | `10` | Applies the 'CritChanceUp' effect. |
| `DodgeChance` | Number | `15%, 10%` | Applies the 'DodgeChance' effect. |
| `KineticSpikes` | Number | `1` | Applies the 'KineticSpikes' effect. |

</details>

---

### Context: `StatusEachTurnBegin`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FillMana` | [`Array`](./Arrays.md#array-fillmana) | `[ 1 .10 ], [ 1 .25 ]` | Applies the 'FillMana' effect. |
| `IntelligenceUp` | Number | `1` | Applies the 'IntelligenceUp' effect. |
| `RandomStatUp` | Number | `2, 3` | Applies the 'RandomStatUp' effect. |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1 .15 ]` | Applies the 'Fear' effect. |

</details>

---

### Context: `StatusGroup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | `2` | Applies the 'LuckUp' effect. |
| `SpawnCoinAnywhere` | Number | `1` | Applies the 'SpawnCoinAnywhere' effect. |
| `SpeedUp` | Number | `2` | Applies the 'SpeedUp' effect. |
| `DexterityUp` | Number | `2` | Applies the 'DexterityUp' effect. |

</details>

---

### Context: `StatusPerInjury`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Shield` | Number | `3` | Applies the 'Shield' effect. |
| `cap` | Number | `10` |  |
| `injury` | [`Enum/String`](./Enums.md#enum-injury) | `int` |  |
| `StrengthUp` | Number | `1` | Applies the 'StrengthUp' effect. |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The ID of the ability to trigger or reference. |
| `range` | Number | `2, global` | Distance or area of effect in tiles. |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `food` | The specific entity tag required or applied. |

</details>

---

### Context: `AddPassivesToCharmed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddMaxHealth` | Number | `10, 5` | Applies the 'AddMaxHealth' effect. |
| `AddSpeed` | Number | `4` | Applies the 'AddSpeed' effect. |
| `DamageUp` | Number | `2, 3` | Combat Trigger: Deals damage to up. |

</details>

---

### Context: `AddPassivesToSummonAbilityMinions`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | `2, 4` | Combat Trigger: Deals damage to up. |
| `Doomed` | Number | `1` | Applies the 'Doomed' effect. |
| `MovementUp` | Number | `2, 4` | Applies the 'MovementUp' effect. |

</details>

---

### Context: `AddStatusToElementDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Electric, Fire` | The specific element type required or applied. |
| `Burn` | Number | `1, 3` | Applies the 'Burn' effect. |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `PullSourceToKnockbackImmuneTarget` | Number | `1` | Applies the 'PullSourceToKnockbackImmuneTarget' effect. |
| `Cleave` | Number | `1` | Causes the attack to hit adjacent enemies alongside the primary target. |
| `LeechPercent` | Number | `50` | Applies the 'LeechPercent' effect. |

</details>

---

### Context: `AmplifyStatus`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `addstacks` | Number | `2` |  |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Poison, Burn, Bleed` | The ID of the status effect to check or apply. |

</details>

---

### Context: `Conditional_Adjacent`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `2, 1` | Applies the 'Bleed' effect. |
| `BonusCritChance` | Number | `50, 25` | Applies the 'BonusCritChance' effect. |
| `BonusDamage` | Number | `2, 3` | Applies the 'BonusDamage' effect. |

</details>

---

### Context: `DamageNeighborsAfterMove`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | [`Enum/String`](./Enums.md#enum-damage) | `X` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Electric ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `DamageReductionAura`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | `true` |  |
| `range` | [`Enum/String`](./Enums.md#enum-range) | `global` | Distance or area of effect in tiles. |
| `stacks` | Number | `2, 1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `ElementalManaCostReduction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Gravity, [ Fire Ice Electric Earth Wind Water Grass Holy Gravity ]` | The specific element type required or applied. |
| `reduction` | Number | `2, 1` |  |

</details>

---

### Context: `Eternal`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `health_percent` | Number | `50%` |  |
| `stacks` | Number | `1` | The number of stacks, duration, or intensity to apply. |
| `AllStatsUp` | Number | `2` | Applies the 'AllStatsUp' effect. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |

</details>

---

### Context: `ForceUseAbility`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `TigerForm, CrohnsPoop, DysenteryPoop` | The ID of the ability to trigger or reference. |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.5, .2, 33%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

</details>

---

### Context: `HealAlliesEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean | `false` |  |
| `mana` | Number | `2, 3` |  |
| `stacks` | Number | `2, 3` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `InfiniteRebirth`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TempSpeedUp` | Number | `10` | Applies the 'TempSpeedUp' effect. |
| `health` | Number | `25%, 1` |  |
| `playercat_health` | Number | `100%` |  |

</details>

---

### Context: `MoveTowardsDamageSource`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `move, TrampleMove, TrampleMoveOne` |  |
| `move_far` | Boolean | `false` |  |

</details>

---

### Context: `ObjectOnHitCharacter`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CharmedFlea` | The entity ID of the character to spawn (e.g., CharmedFlea). |
| `stacks` | Number | `2, 1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `PassiveAtInjuryThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `injury` | [`Enum/String`](./Enums.md#enum-injury) | `spd` |  |
| `mode` | [`Enum/String`](./Enums.md#enum-mode) | `greater_or_equal` |  |
| `threshold` | Number | `4` |  |

</details>

---

### Context: `PassiveGroup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SetDefaultFace` | [`Enum/String`](./Enums.md#enum-setdefaultface) | `sad, happy` | Applies the 'SetDefaultFace' effect. |
| `AllStatsUp` | Number | `-2` | Applies the 'AllStatsUp' effect. |
| `CharismaUp` | Number | `5` | Applies the 'CharismaUp' effect. |
| `IntelligenceUp` | Number | `5` | Applies the 'IntelligenceUp' effect. |
| `SpeedUp` | Number | `5` | Applies the 'SpeedUp' effect. |

</details>

---

### Context: `PassiveWhenAtFullMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `2, 3` | Applies the 'Brace' effect. |
| `Flying` | Number | `1` | Applies the 'Flying' effect. |
| `AddMovement` | Number | `20` | Applies the 'AddMovement' effect. |
| `ReplaceBasicMove` | [`Enum/String`](./Enums.md#enum-replacebasicmove) | `Teleport` | Applies the 'ReplaceBasicMove' effect. |

</details>

---

### Context: `SmiteEnemiesWhoKill`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `10` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Holy ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `SpawnCatCopyOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `PlayerCat_MiniMiniMe, PlayerCat_MiniMe` |  |
| `prevent_chain_tag` | [`Enum/String`](./Enums.md#enum-prevent_chain_tag) | `minime_clone` |  |

</details>

---

### Context: `SpawnOnBattleStartRandomEmptyTile`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `number` | [`Array`](./Arrays.md#array-number) | `10, [ 2 3 ], [ 1 2 ]` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `RandomPickup, Coin` |  |

</details>

---

### Context: `StatusOnAllyCatDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` | Applies the 'AllStatsUp' effect. |
| `FillMana` | Number | `1` | Applies the 'FillMana' effect. |
| `HealthGain` | Number | `8` | Applies the 'HealthGain' effect. |
| `PercentHeal` | Number | `50` | Applies the 'PercentHeal' effect. |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |

</details>

---

### Context: `StatusOnOverHealed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility_NonStack` | [`Enum/String`](./Enums.md#enum-forceuseability_nonstack) | `Indigestion_Fart2, Indigestion_Fart` | Applies the 'ForceUseAbility_NonStack' effect. |
| `StrengthUp` | Number | `1` | Applies the 'StrengthUp' effect. |
| `CurrentWeaponDamageUp` | Number | `1` | Applies the 'CurrentWeaponDamageUp' effect. |
| `SpawnScaledRotFly` | Number | `0` | Applies the 'SpawnScaledRotFly' effect. |

</details>

---

### Context: `empty_armor_scaled_stats`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `1` |  |
| `int` | Number | `1` |  |
| `spd` | Number | `2, 1` |  |

</details>

---

### Context: `statuses`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `consumables, chapter` | Generates an item drop from the specified loot pool. |
| `PermanentDexterity` | Number | `1` | Applies the 'PermanentDexterity' effect. |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `HealthGain` | Number | `10` | Applies the 'HealthGain' effect. |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TakeExtraTurn` | Number | `1` | Applies the 'TakeExtraTurn' effect. |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `FillMana` | Number | `1` | Applies the 'FillMana' effect. |
| `ManaGain` | Number | `5` | Applies the 'ManaGain' effect. |

</details>

---

### Context: `PassiveWhileInMonkRangedStance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddBonusRange` | Number | `2, 1` | Applies the 'AddBonusRange' effect. |
| `AddSpellDamage` | Number | `2` | Applies the 'AddSpellDamage' effect. |
| `KineticSpikes` | Number | `2` | Applies the 'KineticSpikes' effect. |

</details>

---

### Context: `StatusAlliesOnGainCoins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `1` | Applies the 'HealthGain' effect. |
| `LuckUp` | Number | `1` | Applies the 'LuckUp' effect. |
| `scaled` | Boolean | `true` |  |

</details>

---

### Context: `StatusAlliesOnKill`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `DamageUp` | Number | `1` | Combat Trigger: Deals damage to up. |
| `HealthGain` | Number | `5` | Applies the 'HealthGain' effect. |

</details>

---

### Context: `StatusOnCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `2, 1` | Applies the 'Charge' effect. |
| `CurrentWeaponDamageUp` | Number | `1` | Applies the 'CurrentWeaponDamageUp' effect. |
| `HealthGain` | Number | `1` | Applies the 'HealthGain' effect. |

</details>

---

### Context: `StatusOnDealtDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TempDexterityUp` | Number | `2` | Applies the 'TempDexterityUp' effect. |
| `TempStrengthUp` | Number | `2, 1` | Applies the 'TempStrengthUp' effect. |
| `TempLuckUp` | Number | `2` | Applies the 'TempLuckUp' effect. |

</details>

---

### Context: `StatusOnEatFood`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `StrengthUp` | Number | `1` | Applies the 'StrengthUp' effect. |
| `Cleanse` | Number | `0` | Applies the 'Cleanse' effect. |
| `IntelligenceUp` | Number | `1` | Applies the 'IntelligenceUp' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |

</details>

---

### Context: `StatusOnKillEnemy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `HealthGain` | Number | `2` | Applies the 'HealthGain' effect. |
| `ManaGain` | Number | `3` | Applies the 'ManaGain' effect. |
| `RefreshMovePoints` | Number | `1` | Applies the 'RefreshMovePoints' effect. |

</details>

---

### Context: `StatusOnOverMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `IntelligenceUp` | Number | `1` | Applies the 'IntelligenceUp' effect. |
| `SpellDamageUp` | Number | `1` | Applies the 'SpellDamageUp' effect. |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |

</details>

---

### Context: `AddPassiveToSpawnedRocks`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddFilledMaxHealth` | Number | `7, 3` | Applies the 'AddFilledMaxHealth' effect. |
| `JoinSpawnerFaction` | Number | `1` | Applies the 'JoinSpawnerFaction' effect. |

</details>

---

### Context: `AddStatusToAllDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LeaveBehindRockOnKnockback` | Number | `1` | Applies the 'LeaveBehindRockOnKnockback' effect. |
| `Blind` | Number | `1` | Applies the 'Blind' effect. |
| `NonLethal` | Number | `1` | Applies the 'NonLethal' effect. |

</details>

---

### Context: `AllyBonusAbilityAura`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `Bowl, Bowl2` | The ID of the ability to trigger or reference. |
| `square` | Boolean | `true` |  |

</details>

---

### Context: `AllyHealthRegenAura`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `range` | [`Enum/String`](./Enums.md#enum-range) | `global` | Distance or area of effect in tiles. |
| `stacks` | Number | `2, 1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `AlternateCraftingPools`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tinkerer_0` | [`Enum/String`](./Enums.md#enum-tinkerer_0) | `tinkerer_0_bombs` |  |
| `tinkerer_1` | [`Enum/String`](./Enums.md#enum-tinkerer_1) | `tinkerer_1_bombs` |  |

</details>

---

### Context: `BoostWeaponDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `crit_chance` | [`Enum/String`](./Enums.md#enum-crit_chance) | `.5, .25` |  |
| `damage` | Number | `2, 3` | The base damage properties of an attack. |

</details>

---

### Context: `BouncyProjectiles`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `max_bounces` | Number | `2, 1` |  |
| `max_range` | Number | `4, 3` |  |

</details>

---

### Context: `CatAPultAnimation`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `CatapultJump2, CatapultJump` | The ID of the ability to trigger or reference. |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `knockupatk` |  |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `BlinkDodge` | The ID of the ability to trigger or reference. |
| `chance` | Number | `50%, 33%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

</details>

---

### Context: `ClassManaCostReduction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `class` | [`Enum/String`](./Enums.md#enum-class) | `Colorless` | Character class identifier. |
| `reduction` | Number | `2, 1` |  |

</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | `2, 3` | Applies the 'Confusion' effect. |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .5 ]` | Applies the 'Stun' effect. |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `poop, rat` | The specific string tag to check for. |
| `Charmed` | Number | `1` | Applies the 'Charmed' effect. |
| `FlatLeechIfDamaged` | Number | `5` | Applies the 'FlatLeechIfDamaged' effect. |

</details>

---

### Context: `Craft`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `tinkerer_default` |  |
| `slot` | [`Enum/String`](./Enums.md#enum-slot) | `random_empty_armor_or_weapon` |  |

</details>

---

### Context: `DeathRattle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `LastGasp, LastGasp2` | The ID of the ability to trigger or reference. |
| `pop_corpse` | Boolean | `false` |  |

</details>

---

### Context: `EMP`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status_explosion_override` | [`Enum/String`](./Enums.md#enum-status_explosion_override) | `WaterConduct` |  |

</details>

---

### Context: `EscapeSequence`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomDistanceDisplace` | Number | `20` | Displaces the target by a randomized distance. |
| `SafeExplosionIfHitSomething` | Number | `10, 5` | Applies the 'SafeExplosionIfHitSomething' effect. |

</details>

---

### Context: `HolyDamageBlessing`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | `2, 3` | Applies the 'Burn' effect. |
| `damage_multiplier` | Number | `2, 3` |  |

</details>

---

### Context: `LateBloomer`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `3` | Applies the 'AllStatsUp' effect. |
| `stacks` | Number | `5, 3` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `LowHealthAllyDodgeChanceAura`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `50%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |
| `theshold` | Number | `5` |  |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `weapon` | The ID of the ability to trigger or reference. |
| `enemies_only` | Boolean | `true` |  |

</details>

---

### Context: `NextBattleStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `3` | Applies the 'AllStatsUp' effect. |
| `FullHeal` | Number | `1` | Applies the 'FullHeal' effect. |

</details>

---

### Context: `PassiveAtFullHealth`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ManaCostReduction` | Number | `2` | Applies the 'ManaCostReduction' effect. |
| `TakeExtraDamage` | Number | `200%` | Applies the 'TakeExtraDamage' effect. |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `water` | The specific element type required or applied. |

</details>

---

### Context: `RepressedMemoriesMetronome`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `Psychic, Jester` |  |
| `stacks` | Number | `1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `SecurityBotProtect`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `attack` | The ID of the ability to trigger or reference. |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `move, MoveThree` |  |

</details>

---

### Context: `SpecialFriends`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` | Applies the 'AllStatsUp' effect. |
| `HealthGain` | Number | `8` | Applies the 'HealthGain' effect. |

</details>

---

### Context: `StatsAtLowHealth`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `threshold` | Number | `5` |  |
| `speed` | Number | `6` |  |
| `strength` | Number | `6` |  |

</details>

---

### Context: `StatusAllyWhenAllySpendsMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `threshold` | Number | `7` |  |

</details>

---

### Context: `StatusEnemiesOnDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `-2, -1` | Applies the 'AllStatsUp' effect. |
| `Freeze` | Number | `2` | Applies the 'Freeze' effect. |

</details>

---

### Context: `StatusEveryXTurnBegins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |
| `turns` | Number | `2, 3` | The duration of the effect in turns. |

</details>

---

### Context: `StatusOnPickupCoins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RefreshMovePoints` | Number | `1` | Applies the 'RefreshMovePoints' effect. |
| `DexterityUp` | Number | `1` | Applies the 'DexterityUp' effect. |
| `SpeedUp` | Number | `1` | Applies the 'SpeedUp' effect. |

</details>

---

### Context: `StatusOnUseElementAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | `2, 1` | Applies the 'SpeedUp' effect. |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Gravity` | The specific element type required or applied. |

</details>

---

### Context: `TaggedPickupEffectReplacement`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | [`Enum/String`](./Enums.md#enum-healthgain) | `3*X, 2*X` | Applies the 'HealthGain' effect. |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `scrap, money` | The specific entity tag required or applied. |

</details>

---

### Context: `TowerDefense`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `2, 1` | The base damage properties of an attack. |
| `range` | Number | `2, 1` | Distance or area of effect in tiles. |

</details>

---

### Context: `3`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"DISORDER_SEVEREDEJAVU_DESC"` | Localization key for the passive's display description. |
| `icon` | [`Enum/String`](./Enums.md#enum-icon) | `DejaVu3` |  |
| `name` | String | `"DISORDER_SEVEREDEJAVU_NAME"` | Localization key for the passive's display name. |

</details>

---

### Context: `AbilityReaction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `SpontaneouslyCombust` | The ID of the ability to trigger or reference. |
| `ability_damage_only` | Boolean | `true` |  |
| `chance` | Number | `15%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

</details>

---

### Context: `AddStatusToAllDamageAbilities`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies the 'Bleed' effect. |
| `Piercing` | Number | `1` | Applies the 'Piercing' effect. |
| `Weakness` | Number | `2` | Applies the 'Weakness' effect. |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | `2, 1` | Applies the 'CastAgain' effect. |
| `Fury` | Number | `75` | Applies the 'Fury' effect. |

</details>

---

### Context: `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bounty` | Number | `1, 3` | Applies the 'Bounty' effect. |
| `count` | Number | `2` | The numerical quantity. |

</details>

---

### Context: `AutocastEachTurnBegin`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `PoxScratch` | The ID of the ability to trigger or reference. |
| `advantage_polarity` | Number | `-1` |  |
| `chance` | Number | `10%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `odds` | [`Enum/String`](./Enums.md#enum-odds) | `.1` | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. |

</details>

---

### Context: `Conditional_HasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Fear, Marked` | The specific status ID to check for. |

</details>

---

### Context: `FurnitureStats`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Appeal` | Number | `1` | Applies the 'Appeal' effect. |
| `Comfort` | Number | `1` | Applies the 'Comfort' effect. |
| `Stimulation` | Number | `1` | Applies the 'Stimulation' effect. |

</details>

---

### Context: `PassiveLevelScaledStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Shield` | String | `"2*(X-1)"` | Applies the 'Shield' effect. |
| `SizeScalePercent` | String | `"sqrt(1.0+(.05*(X-1)))*100"` | Applies the 'SizeScalePercent' effect. |
| `Trample` | [`Array`](./Arrays.md#array-trample) | `[ 3, X-8 ]` | Applies the 'Trample' effect. |

</details>

---

### Context: `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `2, 1` | Applies the 'Brace' effect. |
| `HealthRegenUp` | Number | `2` | Applies the 'HealthRegenUp' effect. |

</details>

---

### Context: `ReplaceBrain`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `brain` | [`Enum/String`](./Enums.md#enum-brain) | `GenericBrain` |  |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `default` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance` |  |

</details>

---

### Context: `ScaledStatusOnOverMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |
| `Cleanse` | Number | `0` | Applies the 'Cleanse' effect. |

</details>

---

### Context: `StatusAfterCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TempSpellDamageUp` | Number | `1` | Applies the 'TempSpellDamageUp' effect. |
| `TempDamageUp` | Number | `1` | Applies the 'TempDamageUp' effect. |

</details>

---

### Context: `StatusDamagers`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | `-1` | Applies the 'LuckUp' effect. |
| `Fear` | [`Array`](./Arrays.md#array-fear) | `[ 1 .25 ]` | Applies the 'Fear' effect. |

</details>

---

### Context: `StatusOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FullHeal` | Number | `1` | Applies the 'FullHeal' effect. |
| `Sleep` | Number | `1` | Applies the 'Sleep' effect. |

</details>

---

### Context: `StatusOnBreakItem`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | `2, 1` | Applies the 'Thorns' effect. |
| `Shield` | Number | `3` | Applies the 'Shield' effect. |

</details>

---

### Context: `StatusOnHeal`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpeedUp` | Number | `2, 4` | Applies the 'SpeedUp' effect. |
| `RandomStatUp` | Number | `1` | Applies the 'RandomStatUp' effect. |

</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DiminishingHealthRegen` | Number | `2, 1` | Applies the 'DiminishingHealthRegen' effect. |
| `Shield` | Number | `2` | Applies the 'Shield' effect. |

</details>

---

### Context: `StatusOnTookDamageFromEnemyAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |
| `MoveQuivered` | Number | `1` | Applies the 'MoveQuivered' effect. |

</details>

---

### Context: `StatusOnTriggerTrap`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DexterityUp` | Number | `2` | Applies the 'DexterityUp' effect. |
| `Quivered` | Number | `1` | Applies the 'Quivered' effect. |

</details>

---

### Context: `StatusWhenAllySpendsMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `OneUseSpellDamageUp` | Number | `2` | Applies the 'OneUseSpellDamageUp' effect. |
| `ManaGain` | Number | `2` | Applies the 'ManaGain' effect. |

</details>

---

### Context: `fire`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `3` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Fire ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `ice`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `3` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Ice ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Weakness` | Number | `1` | Applies the 'Weakness' effect. |
| `MagicWeakness` | Number | `1` | Applies the 'MagicWeakness' effect. |

</details>

---

### Context: `lightning`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `3` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Electric ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `triattack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `6` | The base damage properties of an attack. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Fire Ice Electric ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `AbilityChargeRefundChance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `advantage_softcap` | Number | `3.5` |  |
| `chance` | Number | `50%` | The probability (0.0 to 1.0 or percentage) of this effect triggering. |

</details>

---

### Context: `AddSelfStatusToWeapons`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ChanceToBreak` | Number | `100, 50` | Applies the 'ChanceToBreak' effect. |

</details>

---

### Context: `AddStatusToBasicAttackWithCooldown`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CharmedForceAttack` | Number | `1` | Applies the 'CharmedForceAttack' effect. |

</details>

---

### Context: `AddStatusToFirstBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | `5` | Applies the 'Charmed' effect. |

</details>

---

### Context: `AddStatusToTrampleDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Cleave` | Number | `1` | Causes the attack to hit adjacent enemies alongside the primary target. |

</details>

---

### Context: `AddStatusesIfPersistentWeatherElement`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | `3` | Applies the 'Burn' effect. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Heat Fire ]` |  |

</details>

---

### Context: `AddStatusesToReceivedElementalDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | `3` | Applies the 'Burn' effect. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Heat Fire ]` |  |

</details>

---

### Context: `ApplyStatusIfCrit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Purge` | Number | `0` | Applies the 'Purge' effect. |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies the 'AllStatsUp' effect. |
| `Shield` | Number | `1` | Applies the 'Shield' effect. |

</details>

---

### Context: `Autism`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `innate` | Number | `-2` |  |
| `learned` | Number | `1` |  |

</details>

---

### Context: `ChangeTile`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `aoe` | Number | `1` | The area of effect or distance in tiles. |
| `tile` | [`Enum/String`](./Enums.md#enum-tile) | `BrambleTile` | The specific tile type to change into (e.g., GlassTile). |

</details>

---

### Context: `Conditional_Boss`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | `1` | Applies the 'Charmed' effect. |
| `Stun` | Number | `3` | Applies the 'Stun' effect. |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `UseRandomSpell_Madness` | Number | `1` | Applies the 'UseRandomSpell_Madness' effect. |
| `odds` | Number | `33%` | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |

</details>

---

### Context: `Conditional_PartyMember`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charmed` | Number | `5` | Applies the 'Charmed' effect. |

</details>

---

### Context: `Conditional_Shielded`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `BonusCritChance` | Number | `100` | Applies the 'BonusCritChance' effect. |

</details>

---

### Context: `DamageIfDidntUseSpecificAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `Groom` | The ID of the ability to trigger or reference. |
| `damage` | Number | `2` | The base damage properties of an attack. |

</details>

---

### Context: `Diabetes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `-1` | Applies the 'AllStatsUp' effect. |
| `Confusion` | Number | `1` | Applies the 'Confusion' effect. |

</details>

---

### Context: `Earth`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | [`Enum/String`](./Enums.md#enum-damage) | `X` | The base damage properties of an attack. |

</details>

---

### Context: `Electric`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Stun` | [`Array`](./Arrays.md#array-stun) | `[ 1 .1*X ]` | Applies the 'Stun' effect. |

</details>

---

### Context: `EnergyStorm`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number | `2` |  |
| `period` | Number | `3` |  |

</details>

---

### Context: `FindItemFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.5` | Probability of finding the item. |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `pills` | The item pool to draw from. |

</details>

---

### Context: `Fire`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | [`Enum/String`](./Enums.md#enum-burn) | `X` | Applies the 'Burn' effect. |

</details>

---

### Context: `Grass`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Poison` | [`Enum/String`](./Enums.md#enum-poison) | `X` | Applies the 'Poison' effect. |

</details>

---

### Context: `Gravity`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Weakness` | [`Enum/String`](./Enums.md#enum-weakness) | `X` | Applies the 'Weakness' effect. |

</details>

---

### Context: `Holy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FlatLeech` | [`Enum/String`](./Enums.md#enum-flatleech) | `X` | Applies the 'FlatLeech' effect. |

</details>

---

### Context: `Ice`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Slow` | [`Enum/String`](./Enums.md#enum-slow) | `X` | Applies the 'Slow' effect. |

</details>

---

### Context: `LightningRod`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | `1` | Applies the 'Tech' effect. |

</details>

---

### Context: `MegaMinions`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cycle_start` | Number | `3` |  |
| `stacks` | Number | `3` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `PassiveAfterXKills`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `3` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `PassiveWhenTheAlpha`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TogglableRoundEndExtraTurn` | Number | `1` | Applies the 'TogglableRoundEndExtraTurn' effect. |

</details>

---

### Context: `PassiveWhilePreviewingMonkRangedStance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddBonusRange` | Number | `2, 1` | Applies the 'AddBonusRange' effect. |

</details>

---

### Context: `PassiveWhileWearingMetal`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddElementsToWeapon` | [`Enum/String`](./Enums.md#enum-addelementstoweapon) | `Electric` | Applies the 'AddElementsToWeapon' effect. |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | `10` |  |

</details>

---

### Context: `SelfDamageWhenDealDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `1` | The base damage properties of an attack. |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `Shadow`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `crit_chance` | [`Enum/String`](./Enums.md#enum-crit_chance) | `.05*X` |  |

</details>

---

### Context: `StackingDodgeChanceOnTookDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `amount` | Number | `10%` | The numerical quantity. |
| `cap` | Number | `50%` |  |

</details>

---

### Context: `StatusAlliesEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomStatUp` | Number | `3` | Applies the 'RandomStatUp' effect. |
| `exclude_self` | Boolean | `false` |  |

</details>

---

### Context: `StatusAlliesOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `EquipTemporaryItem` | [`Enum/String`](./Enums.md#enum-equiptemporaryitem) | `SleepDart, SleepDart2` | Applies the 'EquipTemporaryItem' effect. |

</details>

---

### Context: `StatusAnyCatAllyWhoKills`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AlphaCat` | Number | `1` | Applies the 'AlphaCat' effect. |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `2, 4` | Fires a randomized number of magic missiles. |

</details>

---

### Context: `StatusKilledCharacters`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AutoReanimate` | Number | `50%, 100%` | Applies the 'AutoReanimate' effect. |

</details>

---

### Context: `StatusOnAnyDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | `1` | Applies the 'LuckUp' effect. |

</details>

---

### Context: `StatusOnBattleEndIfKillThresholdMet`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `kills` | Number | `3` |  |

</details>

---

### Context: `StatusOnCollectPickup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | `1` | Applies the 'Tech' effect. |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceAttack` | Number | `1` | Forces the character to execute an immediate attack. |

</details>

---

### Context: `StatusOnHealed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ObjectOnHitCharacter` | [`Enum/String`](./Enums.md#enum-objectonhitcharacter) | `CharmedLeech` | Spawns a specific character or entity upon impact. |
| `Thorns` | Number | `1` | Applies the 'Thorns' effect. |

</details>

---

### Context: `StatusOnPopCorpse`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | `8, 2` | Applies the 'HealthGain' effect. |

</details>

---

### Context: `StatusOnTurnEndIfDidntCastAbilityTypes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | `7` | Applies the 'ManaGain' effect. |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `attack` | The classification type (e.g., damage type or element). |

</details>

---

### Context: `StatusOnUseBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FlippedFacingForceAttack` | Number | `1` | Applies the 'FlippedFacingForceAttack' effect. |

</details>

---

### Context: `StatusThingsKnockedBack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Drag` | Number | `2, 1` | Applies the 'Drag' effect. |

</details>

---

### Context: `StrengthInNumbersAura`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count_self` | Boolean | `true` |  |
| `stacks` | Number | `1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `Study`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `marked` | Number | `2` |  |
| `stacks` | Number | `1` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `TileDamageMultiplier`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ally_multiplier` | Number | `0` |  |
| `multiplier` | Number | `2` | Multiplicative modifier to a base value. |

</details>

---

### Context: `TourettesMeows`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cooldown` | [`Array`](./Arrays.md#array-cooldown) | `[ 8 15 ]` |  |
| `pool` | [`Array`](./Arrays.md#array-pool) | `[ Hit Hiss Normal ]` |  |

</details>

---

### Context: `Water`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AOEPuddle` | [`Enum/String`](./Enums.md#enum-aoepuddle) | `X-1` | Applies the 'AOEPuddle' effect. |

</details>

---

### Context: `Wind`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | [`Enum/String`](./Enums.md#enum-knockback) | `X` |  |

</details>

---

### Context: `on_break`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SafeExplosionIfHitSomething` | Number | `10, 5` | Applies the 'SafeExplosionIfHitSomething' effect. |

</details>

---

### Context: `on_throw`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `HitExplosion` | Number | `10, 5` | Applies the 'HitExplosion' effect. |

</details>

---

### Context: `10`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `desc` | String | `"DISORDER_DISTEMPERMAX_DESC"` | Localization key for the passive's display description. |

</details>

---

### Context: `AddStatusToKnockbackDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `1` | Applies the 'Bruise' effect. |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LeechPercent` | Number | `50` | Applies the 'LeechPercent' effect. |

</details>

---

### Context: `AddTemporaryEffectsToEquipment`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | `1` | Applies the 'CastAgain' effect. |

</details>

---

### Context: `ChanceToRevive`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `33` | The number of stacks, duration, or intensity to apply. |

</details>

---

### Context: `CollectPickupsOnBattleEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pop_corpses` | Boolean | `true` |  |

</details>

---

### Context: `Conditional_DoesDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | [`Array`](./Arrays.md#array-bleed) | `[ 1 .1 ]` | Applies the 'Bleed' effect. |

</details>

---

### Context: `Conditional_SourceHasTag`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `crow` | The specific entity tag required or applied. |

</details>

---

### Context: `DelayedWind`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `distance` | Number | `2` | The area of effect or distance in tiles. |

</details>

---

### Context: `DelayedWindCone`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `distance` | Number | `10` | The area of effect or distance in tiles. |

</details>

---

### Context: `ForceMoveAway`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `free` | Boolean | `false` |  |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `weights` | [`Enum/String`](./Enums.md#enum-weights) | `stay_far_always_move` |  |

</details>

---

### Context: `Robot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean | `true` |  |

</details>

---

### Context: `ScaledStatusOnBleedDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | `2` | Applies the 'Charge' effect. |

</details>

---

### Context: `ScaledStatusOnLoseShield`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | `1` | Applies the 'Thorns' effect. |

</details>

---

### Context: `ScaledStatusOnOverHealed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpawnScaledRotFly` | Number | `1` | Applies the 'SpawnScaledRotFly' effect. |

</details>

---

### Context: `StatusAlliesOnSpendMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ManaGain` | Number | `1` | Applies the 'ManaGain' effect. |

</details>

---

### Context: `StatusAlliesScaledByCursedOnDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LuckUp` | Number | `1` | Applies the 'LuckUp' effect. |

</details>

---

### Context: `StatusIfBattleAlreadyBegan`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `PermanentMadness` | Number | `1` | Applies the 'PermanentMadness' effect. |

</details>

---

### Context: `StatusOnEatPill`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `3` | Applies the 'AllStatsUp' effect. |

</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `1` | Applies the 'DivineShield' effect. |

</details>

---

### Context: `StatusOnLoseShield`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | `1` | Applies the 'Thorns' effect. |

</details>

---

### Context: `StatusOnTakeHealthDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `PermanentConstitution` | Number | `-1` | Applies the 'PermanentConstitution' effect. |

</details>

---

### Context: `TakeBonusTurnWithStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |

</details>

---

### Context: `TheHunger`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |

</details>

---

### Context: `4`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `5`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `6`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `7`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `8`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `9`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `AddStatusToMeleeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `AddStatusToReceivedDamage_ExcludeStatuses`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `BoobyTrapItems`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Conditional_NotBoss`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `DamageNeighborTilesWhenCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ElementalAttunement`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `PassiveUntilCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `PassiveUntilGetKill`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `RandomPassivePool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ScaledStatusOnSpendMana`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusAdjacentOnTheirTurnBegin`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusEachTurnEndPerEnemyKill`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusKillers`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusOnGainShield`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

## Progression Unlocks

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `popup` | [`Block`](./Progression_Unlocks.md#context-popup) | `{ ... }` |  |
| `complete_chapter_with_class` | [`Array`](./Arrays.md#array-complete_chapter_with_class) | `[ caves Mage ], [ caves Hunter ], [ caves Fighter ]` |  |
| `unlock_item_immediate` | [`Enum/String`](./Enums.md#enum-unlock_item_immediate) | `InfinityArrow, StaffOfFlame, BattleAxe` |  |
| `trigger_npc_sequence` | [`Enum/String`](./Enums.md#enum-trigger_npc_sequence) | `class_unlock_thief, class_unlock_medic, class_unlock_necromancer` |  |
| `beat_house_boss` | [`Enum/String`](./Enums.md#enum-beat_house_boss) | `guillotina_2, pyrophina, guillotina_1` |  |
| `complete_chapter` | [`Enum/String`](./Enums.md#enum-complete_chapter) | `alley, boneyard, sewers` |  |
| `required_difficulty` | Number | `2, 1, 3` |  |
| `repeat` | Number | `6, 1, 3` |  |
| `beat_chapter_boss` | [`Enum/String`](./Enums.md#enum-beat_chapter_boss) | `alley, junkyard, sewers` |  |
| `unlock_ability` | [`Enum/String`](./Enums.md#enum-unlock_ability) | `Pawbreaker, HyperBeam, BallOfSpiders` |  |
| `unlock_passive` | [`Enum/String`](./Enums.md#enum-unlock_passive) | `ThrillOfTheHunt, DualWield, EnergyStorm` |  |
| `unlock_song` | [`Enum/String`](./Enums.md#enum-unlock_song) | `chumbucket_kitty, eatin_rats, flush` |  |
| `set_mapgen_flag` | [`Enum/String`](./Enums.md#enum-set_mapgen_flag) | `SewersUnlocked, HardPathUnlocked, JunkyardUnlocked` |  |
| `complete_checklist_with_class` | [`Enum/String`](./Enums.md#enum-complete_checklist_with_class) | `Mage, Fighter, Hunter` |  |
| `unlock_quest_item` | [`Enum/String`](./Enums.md#enum-unlock_quest_item) | `PutridLeech, GuillotinasHead, ThrobbingGristle` |  |
| `repeatable` | Boolean | `true` |  |
| `trigger_house_boss` | [`Enum/String`](./Enums.md#enum-trigger_house_boss) | `guillotina_2, guillotina_3, guillotina_1` |  |
| `complete_act_difficulty` | [`Array`](./Arrays.md#array-complete_act_difficulty) | `[ 1 2 ], [ 1 1 ], [ 1 0 ]` |  |
| `complete_item_quest` | [`Enum/String`](./Enums.md#enum-complete_item_quest) | `BlackShard, ScaldingOrb, JarOfRadiation` |  |
| `unlock_act_difficulty` | [`Array`](./Arrays.md#array-unlock_act_difficulty) | `[ 1 3 ], [ 1 1 ], [ 1 2 ]` |  |
| `queue_cutscene_immediate` | [`Enum/String`](./Enums.md#enum-queue_cutscene_immediate) | `desert_intro, dybbuk, caves_intro` |  |
| `reset_npc_sequence` | [`Enum/String`](./Enums.md#enum-reset_npc_sequence) | `beanies_bombquest_fail_jarofradiation, beanies_bombquest_2, beanies_bombquest_3` |  |
| `preempt_npc_sequence` | [`Enum/String`](./Enums.md#enum-preempt_npc_sequence) | `beanies_bombquest_2, beanies_bombquest_3, beanies_bombquest_amnesia` |  |
| `set_savefile_flag` | [`Enum/String`](./Enums.md#enum-set_savefile_flag) | `PlotFlag_Beanies_Homeless, RestlessDeadUnlocked, PlotFlag_FrankBeanies` |  |
| `unlock_boss` | [`Enum/String`](./Enums.md#enum-unlock_boss) | `gambit, jestercat, queenhippo` |  |
| `fail_item_quest` | [`Enum/String`](./Enums.md#enum-fail_item_quest) | `JarOfRadiatedBlood, JarOfRadiation, JarOfChaos` |  |
| `fully_complete_difficulty` | Number | `1, 2, 0` |  |
| `post_combat_cutscene` | [`Enum/String`](./Enums.md#enum-post_combat_cutscene) | `obelisk1_moon, obelisk1_core, obelisk2_moon` |  |
| `trigger_npc_sequence_tomorrow` | [`Enum/String`](./Enums.md#enum-trigger_npc_sequence_tomorrow) | `frank_caves_intro, organ_boneyard_intro, butch_boneyard_intro` |  |
| `unlock_npc_tomorrow` | [`Enum/String`](./Enums.md#enum-unlock_npc_tomorrow) | `tracy, beanies, jack` |  |
| `visit_chapter` | [`Enum/String`](./Enums.md#enum-visit_chapter) | `future, dimensionx, theend` |  |
| `complete_chapters` | [`Array`](./Arrays.md#array-complete_chapters) | `[ caves boneyard ], [ core moon ]` |  |
| `requires_monoclass_run` | Boolean | `true` |  |
| `requires_unlocked_npc` | [`Enum/String`](./Enums.md#enum-requires_unlocked_npc) | `tracy, frank, jack` |  |
| `complete_adventure` | [`Enum/String`](./Enums.md#enum-complete_adventure) | `anywhere` |  |
| `require_beat_house_boss` | [`Enum/String`](./Enums.md#enum-require_beat_house_boss) | `zaratana, pyrophina` |  |
| `require_mapgen_flag` | [`Enum/String`](./Enums.md#enum-require_mapgen_flag) | `CoreObeliskUnlocked, MoonObeliskUnlocked` |  |
| `surviving_kaiju` | [`Enum/String`](./Enums.md#enum-surviving_kaiju) | `zaratana, pyrophina` |  |
| `unlock_levelgroup` | [`Enum/String`](./Enums.md#enum-unlock_levelgroup) | `bigsharklevels` |  |
| `beanies_quests_intro` | [`Block`](./Progression_Unlocks.md#context-beanies_quests_intro) | `{ ... }` |  |
| `beanies_quests_repeat` | [`Block`](./Progression_Unlocks.md#context-beanies_quests_repeat) | `{ ... }` |  |
| `destinations` | [`Block`](./Progression_Unlocks.md#context-destinations) | `{ ... }` |  |
| `fail_adventure` | [`Enum/String`](./Enums.md#enum-fail_adventure) | `anywhere` |  |
| `finish_quest` | [`Enum/String`](./Enums.md#enum-finish_quest) | `JarOfChaos` |  |
| `frank_max_intro` | [`Block`](./Progression_Unlocks.md#context-frank_max_intro) | `{ ... }` |  |
| `frank_max_repeating` | [`Block`](./Progression_Unlocks.md#context-frank_max_repeating) | `{ ... }` |  |
| `house_upgrade_4throom` | [`Block`](./Progression_Unlocks.md#context-house_upgrade_4throom) | `{ ... }` |  |
| `house_upgrade_attic` | [`Block`](./Progression_Unlocks.md#context-house_upgrade_attic) | `{ ... }` |  |
| `house_upgrade_largehouse` | [`Block`](./Progression_Unlocks.md#context-house_upgrade_largehouse) | `{ ... }` |  |
| `house_upgrade_mediumhouse` | [`Block`](./Progression_Unlocks.md#context-house_upgrade_mediumhouse) | `{ ... }` |  |
| `increment_savefile_counter` | [`Enum/String`](./Enums.md#enum-increment_savefile_counter) | `GameStat_CountNukeQuestCompletions` |  |
| `intro` | [`Array`](./Arrays.md#array-intro) | `[ PersuasionDevice ]` |  |
| `jack_max_intro` | [`Block`](./Progression_Unlocks.md#context-jack_max_intro) | `{ ... }` |  |
| `jack_max_repeating` | [`Block`](./Progression_Unlocks.md#context-jack_max_repeating) | `{ ... }` |  |
| `jack_shopupgrade1` | [`Block`](./Progression_Unlocks.md#context-jack_shopupgrade1) | `{ ... }` |  |
| `jack_shopupgrade2` | [`Block`](./Progression_Unlocks.md#context-jack_shopupgrade2) | `{ ... }` |  |
| `jack_shopupgrade3` | [`Block`](./Progression_Unlocks.md#context-jack_shopupgrade3) | `{ ... }` |  |
| `jack_shopupgrade4` | [`Block`](./Progression_Unlocks.md#context-jack_shopupgrade4) | `{ ... }` |  |
| `main_pool` | [`Array`](./Arrays.md#array-main_pool) | `[ ChaosDevice MagicMirror MeStone AngryFace FartFace Spid...` |  |
| `organ_max_intro` | [`Block`](./Progression_Unlocks.md#context-organ_max_intro) | `{ ... }` |  |
| `organ_max_repeating` | [`Block`](./Progression_Unlocks.md#context-organ_max_repeating) | `{ ... }` |  |
| `organ_unlock` | [`Block`](./Progression_Unlocks.md#context-organ_unlock) | `{ ... }` |  |
| `organ_upgrade1` | [`Block`](./Progression_Unlocks.md#context-organ_upgrade1) | `{ ... }` |  |
| `organ_upgrade2` | [`Block`](./Progression_Unlocks.md#context-organ_upgrade2) | `{ ... }` |  |
| `organ_upgrade3` | [`Block`](./Progression_Unlocks.md#context-organ_upgrade3) | `{ ... }` |  |
| `organ_upgrade4` | [`Block`](./Progression_Unlocks.md#context-organ_upgrade4) | `{ ... }` |  |
| `organ_upgrade5` | [`Block`](./Progression_Unlocks.md#context-organ_upgrade5) | `{ ... }` |  |
| `organ_upgrade6` | [`Block`](./Progression_Unlocks.md#context-organ_upgrade6) | `{ ... }` |  |
| `prereqs` | [`Block`](./Progression_Unlocks.md#context-prereqs) | `{ ... }` |  |
| `requires_hard_path` | Boolean | `true` |  |
| `reset_unlock` | [`Enum/String`](./Enums.md#enum-reset_unlock) | `nuke_quest_begin` |  |
| `steven_milliontrashed` | [`Block`](./Progression_Unlocks.md#context-steven_milliontrashed) | `{ ... }` |  |
| `tink_aggression` | [`Block`](./Progression_Unlocks.md#context-tink_aggression) | `{ ... }` |  |
| `tink_basestats` | [`Block`](./Progression_Unlocks.md#context-tink_basestats) | `{ ... }` |  |
| `tink_inbreeding` | [`Block`](./Progression_Unlocks.md#context-tink_inbreeding) | `{ ... }` |  |
| `tink_max_intro` | [`Block`](./Progression_Unlocks.md#context-tink_max_intro) | `{ ... }` |  |
| `tink_max_repeating` | [`Block`](./Progression_Unlocks.md#context-tink_max_repeating) | `{ ... }` |  |
| `tink_prettybow` | [`Block`](./Progression_Unlocks.md#context-tink_prettybow) | `{ ... }` |  |
| `tink_relationships` | [`Block`](./Progression_Unlocks.md#context-tink_relationships) | `{ ... }` |  |
| `tink_sexuality` | [`Block`](./Progression_Unlocks.md#context-tink_sexuality) | `{ ... }` |  |
| `tink_tags` | [`Block`](./Progression_Unlocks.md#context-tink_tags) | `{ ... }` |  |
| `tracy_blankcollar1` | [`Block`](./Progression_Unlocks.md#context-tracy_blankcollar1) | `{ ... }` |  |
| `tracy_blankcollar2` | [`Block`](./Progression_Unlocks.md#context-tracy_blankcollar2) | `{ ... }` |  |
| `tracy_blankcollar3` | [`Block`](./Progression_Unlocks.md#context-tracy_blankcollar3) | `{ ... }` |  |
| `tracy_foodstorage1` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage1) | `{ ... }` |  |
| `tracy_foodstorage10` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage10) | `{ ... }` |  |
| `tracy_foodstorage2` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage2) | `{ ... }` |  |
| `tracy_foodstorage3` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage3) | `{ ... }` |  |
| `tracy_foodstorage4` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage4) | `{ ... }` |  |
| `tracy_foodstorage5` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage5) | `{ ... }` |  |
| `tracy_foodstorage6` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage6) | `{ ... }` |  |
| `tracy_foodstorage7` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage7) | `{ ... }` |  |
| `tracy_foodstorage8` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage8) | `{ ... }` |  |
| `tracy_foodstorage9` | [`Block`](./Progression_Unlocks.md#context-tracy_foodstorage9) | `{ ... }` |  |
| `tracy_idol1` | [`Block`](./Progression_Unlocks.md#context-tracy_idol1) | `{ ... }` |  |
| `tracy_idol2` | [`Block`](./Progression_Unlocks.md#context-tracy_idol2) | `{ ... }` |  |
| `tracy_idol3` | [`Block`](./Progression_Unlocks.md#context-tracy_idol3) | `{ ... }` |  |
| `tracy_idol4` | [`Block`](./Progression_Unlocks.md#context-tracy_idol4) | `{ ... }` |  |
| `tracy_idol5` | [`Block`](./Progression_Unlocks.md#context-tracy_idol5) | `{ ... }` |  |
| `tracy_idol6` | [`Block`](./Progression_Unlocks.md#context-tracy_idol6) | `{ ... }` |  |
| `tracy_idol7` | [`Block`](./Progression_Unlocks.md#context-tracy_idol7) | `{ ... }` |  |
| `tracy_max_intro` | [`Block`](./Progression_Unlocks.md#context-tracy_max_intro) | `{ ... }` |  |
| `tracy_max_repeating` | [`Block`](./Progression_Unlocks.md#context-tracy_max_repeating) | `{ ... }` |  |
| `unlock_item` | [`Enum/String`](./Enums.md#enum-unlock_item) | `MomsKnife` |  |
| `upgrade_storage_1` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_1) | `{ ... }` |  |
| `upgrade_storage_2` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_2) | `{ ... }` |  |
| `upgrade_storage_3` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_3) | `{ ... }` |  |
| `upgrade_storage_4` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_4) | `{ ... }` |  |
| `upgrade_storage_5` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_5) | `{ ... }` |  |
| `upgrade_storage_6` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_6) | `{ ... }` |  |
| `upgrade_storage_7` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_7) | `{ ... }` |  |
| `upgrade_storage_repeating_crazy` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_repeating_crazy) | `{ ... }` |  |
| `upgrade_storage_repeating_hard` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_repeating_hard) | `{ ... }` |  |
| `upgrade_storage_repeating_impossible` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_repeating_impossible) | `{ ... }` |  |
| `upgrade_storage_repeating_intro` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_repeating_intro) | `{ ... }` |  |
| `upgrade_storage_repeating_normal` | [`Block`](./Progression_Unlocks.md#context-upgrade_storage_repeating_normal) | `{ ... }` |  |

</details>

---

### Context: `popup`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prompt` | [`Enum/String`](./Enums.md#enum-prompt) | `AREA_UNLOCK_JUNKYARD, AREA_UNLOCK_BUNKER, AREA_UNLOCK_SEWERS` |  |
| `immediate` | Boolean | `false, true` |  |
| `frame` | [`Enum/String`](./Enums.md#enum-frame) | `UnlockArea_Junkyard, UnlockArea_Sewers, UnlockArea_Bunker` |  |

</details>

---

### Context: `tracy_special_item`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`tracy_blankcollar1`](./Progression_Unlocks.md#context-tracy_blankcollar1), [`tracy_blankcollar2`](./Progression_Unlocks.md#context-tracy_blankcollar2), [`tracy_blankcollar3`](./Progression_Unlocks.md#context-tracy_blankcollar3), [`tracy_foodstorage1`](./Progression_Unlocks.md#context-tracy_foodstorage1), [`tracy_foodstorage10`](./Progression_Unlocks.md#context-tracy_foodstorage10), [`tracy_foodstorage2`](./Progression_Unlocks.md#context-tracy_foodstorage2), [`tracy_foodstorage3`](./Progression_Unlocks.md#context-tracy_foodstorage3), [`tracy_foodstorage4`](./Progression_Unlocks.md#context-tracy_foodstorage4), [`tracy_foodstorage5`](./Progression_Unlocks.md#context-tracy_foodstorage5), [`tracy_foodstorage6`](./Progression_Unlocks.md#context-tracy_foodstorage6), [`tracy_foodstorage7`](./Progression_Unlocks.md#context-tracy_foodstorage7), [`tracy_foodstorage8`](./Progression_Unlocks.md#context-tracy_foodstorage8), [`tracy_foodstorage9`](./Progression_Unlocks.md#context-tracy_foodstorage9), [`tracy_idol1`](./Progression_Unlocks.md#context-tracy_idol1), [`tracy_idol2`](./Progression_Unlocks.md#context-tracy_idol2), [`tracy_idol3`](./Progression_Unlocks.md#context-tracy_idol3), [`tracy_idol4`](./Progression_Unlocks.md#context-tracy_idol4), [`tracy_idol5`](./Progression_Unlocks.md#context-tracy_idol5), [`tracy_idol6`](./Progression_Unlocks.md#context-tracy_idol6), [`tracy_idol7`](./Progression_Unlocks.md#context-tracy_idol7), [`tracy_max_intro`](./Progression_Unlocks.md#context-tracy_max_intro), [`tracy_max_repeating`](./Progression_Unlocks.md#context-tracy_max_repeating)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cost` | Number | `100, 150, 10` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `blankcollar, special_foodbox, random_unique_idol` |  |

</details>

---

### Context: `destinations`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `boneyard` | Number | `200` |  |
| `caves` | Number | `200` |  |
| `core` | Number | `300` |  |
| `dimensionx` | Number | `400` |  |
| `endoftime` | Number | `500` |  |
| `jurassic` | Number | `400` |  |
| `meatworld` | Number | `300` |  |
| `moon` | Number | `300` |  |
| `theend` | Number | `400` |  |

</details>

---

### Context: `upgrade_storage_repeating_crazy`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `rep_reward_count` | Number | `1` |  |
| `repeat` | Number | `25` |  |
| `required_act` | Number | `3` |  |
| `required_chapter` | Number | `4` |  |
| `required_difficulty` | Number | `2` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |

</details>

---

### Context: `upgrade_storage_repeating_hard`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `rep_reward_count` | Number | `1` |  |
| `repeat` | Number | `23` |  |
| `required_act` | Number | `3` |  |
| `required_chapter` | Number | `4` |  |
| `required_difficulty` | Number | `1` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |

</details>

---

### Context: `upgrade_storage_repeating_impossible`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `rep_reward_count` | Number | `1` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |
| `required_act` | Number | `3` |  |
| `required_chapter` | Number | `4` |  |
| `required_difficulty` | Number | `3` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |

</details>

---

### Context: `upgrade_storage_repeating_normal`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `rep_reward_count` | Number | `1` |  |
| `repeat` | Number | `20` |  |
| `required_act` | Number | `3` |  |
| `required_chapter` | Number | `4` |  |
| `required_difficulty` | Number | `0` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |

</details>

---

### Context: `upgrade_storage_repeating_intro`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `rep_reward_count` | Number | `1` |  |
| `required_act` | Number | `3` |  |
| `required_chapter` | Number | `4` |  |
| `required_difficulty` | Number | `0` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |

</details>

---

### Context: `prereqs`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `core` | [`Enum/String`](./Enums.md#enum-core) | `mapflag_IceAgeUnlocked` |  |
| `dimensionx` | [`Enum/String`](./Enums.md#enum-dimensionx) | `mapflag_IceAgeUnlocked` |  |
| `endoftime` | [`Enum/String`](./Enums.md#enum-endoftime) | `endoftime` |  |
| `jurassic` | [`Enum/String`](./Enums.md#enum-jurassic) | `endoftime` |  |
| `moon` | [`Enum/String`](./Enums.md#enum-moon) | `mapflag_IceAgeUnlocked` |  |
| `theend` | [`Enum/String`](./Enums.md#enum-theend) | `endoftime` |  |

</details>

---

### Context: `tracy_max_repeating`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_RARE"` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `beanies_quests_repeat`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `5` |  |
| `generate_beanies_quest` | [`Enum/String`](./Enums.md#enum-generate_beanies_quest) | `main_pool` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |
| `reward_text` | String | `"FAVOR_BEANIES_REPEAT"` |  |

</details>

---

### Context: `frank_max_repeating`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `gift_item_from_pool` | [`Enum/String`](./Enums.md#enum-gift_item_from_pool) | `parasites` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |
| `reward_text` | String | `"FAVOR_FRANK_PARASITE"` |  |

</details>

---

### Context: `jack_max_repeating`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `rep_reward_count` | Number | `1` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |
| `reward_text` | String | `"FAVOR_JACK_MAX"` |  |

</details>

---

### Context: `organ_max_repeating`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `gift_item` | [`Enum/String`](./Enums.md#enum-gift_item) | `disorder_needle` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |
| `reward_text` | String | `"FAVOR_GRINDER_SYRINGE"` |  |

</details>

---

### Context: `tink_max_repeating`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins` | Number | `25` |  |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |
| `reward_text` | String | `"FAVOR_TINK_MAX"` |  |

</details>

---

### Context: `tracy_blankcollar1`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_COLLAR"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_blankcollar2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_COLLAR"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_blankcollar3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_COLLAR"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage1`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage10`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage4`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage5`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage6`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage7`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage8`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_foodstorage9`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_FOOD"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_idol1`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_IDOL"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_idol2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_IDOL"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_idol3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_IDOL"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_idol4`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_IDOL"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_idol5`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_IDOL"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_idol6`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_IDOL"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_idol7`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_IDOL"` |  |
| `shop_level_up` | Number | `1` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `tracy_max_intro`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `required_age` | Number | `5` |  |
| `reward_text` | String | `"FAVOR_TRACY_RARE"` |  |
| `tracy_special_item` | [`Block`](./Progression_Unlocks.md#context-tracy_special_item) | `{ ... }` |  |

</details>

---

### Context: `upgrade_storage_1`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1` |  |
| `required_act` | Number | `0` |  |
| `required_chapter` | Number | `0` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |
| `storage_expansion` | Number | `1` |  |

</details>

---

### Context: `upgrade_storage_2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_act` | Number | `1` |  |
| `required_chapter` | Number | `2` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |
| `storage_expansion` | Number | `1` |  |

</details>

---

### Context: `upgrade_storage_3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `required_act` | Number | `1` |  |
| `required_chapter` | Number | `3` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |
| `storage_expansion` | Number | `1` |  |

</details>

---

### Context: `upgrade_storage_4`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `15` |  |
| `required_act` | Number | `2` |  |
| `required_chapter` | Number | `2` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |
| `storage_expansion` | Number | `1` |  |

</details>

---

### Context: `upgrade_storage_5`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `15` |  |
| `required_act` | Number | `2` |  |
| `required_chapter` | Number | `3` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |
| `storage_expansion` | Number | `1` |  |

</details>

---

### Context: `upgrade_storage_6`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `20` |  |
| `required_act` | Number | `3` |  |
| `required_chapter` | Number | `2` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |
| `storage_expansion` | Number | `1` |  |

</details>

---

### Context: `upgrade_storage_7`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `20` |  |
| `required_act` | Number | `3` |  |
| `required_chapter` | Number | `3` |  |
| `reward_text` | String | `"FAVOR_BUTCH_UPGRADE"` |  |
| `storage_expansion` | Number | `1` |  |

</details>

---

### Context: `frank_max_intro`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `gift_item_from_pool` | [`Enum/String`](./Enums.md#enum-gift_item_from_pool) | `parasites` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `reward_text` | String | `"FAVOR_FRANK_PARASITE"` |  |

</details>

---

### Context: `house_upgrade_largehouse`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `house_upgrade` | [`Enum/String`](./Enums.md#enum-house_upgrade) | `LargeHouse_Floor2Large, LargeHouse` |  |
| `favor` | Number | `50` |  |
| `reward_text` | String | `"FAVOR_FRANK_ROOM"` |  |

</details>

---

### Context: `house_upgrade_mediumhouse`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `house_upgrade` | [`Enum/String`](./Enums.md#enum-house_upgrade) | `MediumHouse, MediumHouse_SmallRoom` |  |
| `favor` | Number | `25` |  |
| `reward_text` | String | `"FAVOR_FRANK_ROOM"` |  |

</details>

---

### Context: `jack_max_intro`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `rep_reward_count` | Number | `1` |  |
| `reward_text` | String | `"FAVOR_JACK_MAX"` |  |

</details>

---

### Context: `organ_max_intro`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `gift_item` | [`Enum/String`](./Enums.md#enum-gift_item) | `disorder_needle` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `reward_text` | String | `"FAVOR_GRINDER_SYRINGE"` |  |

</details>

---

### Context: `tink_max_intro`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins` | Number | `25` |  |
| `favor` | Number | `10` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `reward_text` | String | `"FAVOR_TINK_MAX"` |  |

</details>

---

### Context: `beanies_quests_intro`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1` |  |
| `generate_beanies_quest` | [`Enum/String`](./Enums.md#enum-generate_beanies_quest) | `intro` |  |
| `reward_text` | String | `"FAVOR_BEANIES_INTRO"` |  |

</details>

---

### Context: `house_upgrade_4throom`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `100` |  |
| `house_upgrade` | [`Enum/String`](./Enums.md#enum-house_upgrade) | `LargeHouse_Floor2Small` |  |
| `reward_text` | String | `"FAVOR_FRANK_ROOM"` |  |

</details>

---

### Context: `house_upgrade_attic`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1` |  |
| `house_upgrade` | [`Enum/String`](./Enums.md#enum-house_upgrade) | `SmallHouse_Attic` |  |
| `reward_text` | String | `"FAVOR_FRANK_ATTIC"` |  |

</details>

---

### Context: `jack_shopupgrade1`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1` |  |
| `reward_text` | String | `"FAVOR_JACK_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `jack_shopupgrade2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_JACK_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `jack_shopupgrade3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `20` |  |
| `reward_text` | String | `"FAVOR_JACK_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `jack_shopupgrade4`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `30` |  |
| `reward_text` | String | `"FAVOR_JACK_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `organ_unlock`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1` |  |
| `reward_text` | String | `"FAVOR_GRINDER_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `organ_upgrade1`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_GRINDER_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `organ_upgrade2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `25` |  |
| `reward_text` | String | `"FAVOR_GRINDER_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `organ_upgrade3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `50` |  |
| `reward_text` | String | `"FAVOR_GRINDER_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `organ_upgrade4`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `75` |  |
| `reward_text` | String | `"FAVOR_GRINDER_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `organ_upgrade5`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `100` |  |
| `reward_text` | String | `"FAVOR_GRINDER_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `organ_upgrade6`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `150` |  |
| `reward_text` | String | `"FAVOR_GRINDER_UPGRADE"` |  |
| `shop_level_up` | Number | `1` |  |

</details>

---

### Context: `steven_milliontrashed`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1000000` |  |
| `level_display` | [`Enum/String`](./Enums.md#enum-level_display) | `max` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `infinite` |  |

</details>

---

### Context: `tink_aggression`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_TINK_AGRESSION"` |  |
| `set_savefile_flag` | [`Enum/String`](./Enums.md#enum-set_savefile_flag) | `catinfo_unlock_aggression` |  |

</details>

---

### Context: `tink_basestats`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_TINK_BASESTATS"` |  |
| `set_savefile_flag` | [`Enum/String`](./Enums.md#enum-set_savefile_flag) | `catinfo_unlock_basestats` |  |

</details>

---

### Context: `tink_inbreeding`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_TINK_INBREEDING"` |  |
| `set_savefile_flag` | [`Enum/String`](./Enums.md#enum-set_savefile_flag) | `catinfo_unlock_inbreeding` |  |

</details>

---

### Context: `tink_prettybow`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `1` |  |
| `gift_item` | [`Enum/String`](./Enums.md#enum-gift_item) | `TinksBow` |  |
| `reward_text` | String | `"FAVOR_TINK_BOW"` |  |

</details>

---

### Context: `tink_relationships`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_TINK_RELATIONSHIPS"` |  |
| `set_savefile_flag` | [`Enum/String`](./Enums.md#enum-set_savefile_flag) | `catinfo_unlock_relationships` |  |

</details>

---

### Context: `tink_sexuality`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_TINK_SEXUALITY"` |  |
| `set_savefile_flag` | [`Enum/String`](./Enums.md#enum-set_savefile_flag) | `catinfo_unlock_sexuality` |  |

</details>

---

### Context: `tink_tags`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `favor` | Number | `10` |  |
| `reward_text` | String | `"FAVOR_TINK_TAGS"` |  |
| `set_savefile_flag` | [`Enum/String`](./Enums.md#enum-set_savefile_flag) | `catinfo_unlock_tags` |  |

</details>

---

## Shops

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `meta` | [`Block`](./Shops.md#context-meta) | `{ ... }` |  |
| `breakdown` | [`Block`](./Shops.md#context-breakdown) | `{ ... }` |  |
| `item_groups` | [`Block`](./Shops.md#context-item_groups) | `{ ... }` |  |
| `item_rarity_costs` | [`Block`](./Shops.md#context-item_rarity_costs) | `{ ... }` |  |
| `stock_fill_order` | Block | `{ ... }` |  |
| `button_nav` | [`Block`](./Shops.md#context-button_nav) | `{ ... }` |  |
| `breakdown2` | [`Block`](./Shops.md#context-breakdown2) | `{ ... }` |  |
| `breakdown3` | [`Block`](./Shops.md#context-breakdown3) | `{ ... }` |  |
| `breakdown4` | [`Block`](./Shops.md#context-breakdown4) | `{ ... }` |  |

</details>

---

### Context: `Item`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`common_item`](./Shops.md#context-common_item), [`consumable`](./Shops.md#context-consumable), [`empty`](./Shops.md#context-empty), [`item`](./Shops.md#context-item), [`mandatory`](./Shops.md#context-mandatory), [`mostly_food`](./Shops.md#context-mostly_food), [`pool`](./Shops.md#context-pool), [`treasure`](./Shops.md#context-treasure)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `shop_common, treasure_easy, rare` |  |
| `cost` | Number | `10, 0, 15` |  |
| `mandatory` | Boolean | `true` |  |
| `weight` | Number | `1` |  |

</details>

---

### Context: `meta`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `movieclip` | [`Enum/String`](./Enums.md#enum-movieclip) | `Shop, JackOffice, TreasureRoom` |  |
| `treasure_room` | Boolean | `true` |  |
| `delay_enable_tooltips` | Boolean | `true` |  |
| `keeper` | Number | `0` |  |
| `npc_script` | [`Enum/String`](./Enums.md#enum-npc_script) | `tracy_adventure_shop_script.gon` |  |
| `shopkeeper_fights` | [`Array`](./Arrays.md#array-shopkeeper_fights) | `[ test.lvl ]` |  |
| `house_shop` | Boolean | `true` |  |
| `welcome_message` | [`Enum/String`](./Enums.md#enum-welcome_message) | `welcome_water_cheap, welcome_water` |  |
| `pick_n` | Number | `1` |  |

</details>

---

### Context: `item_rarity_costs`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `common` | Number | `7, 14, 5` |  |
| `consumable_common` | Number | `10, 5, 3` |  |
| `consumable_rare` | Number | `8, 10, 20` |  |
| `consumable_uncommon` | Number | `7, 14, 5` |  |
| `consumable_very_rare` | Number | `40, 12, 20` |  |
| `rare` | Number | `40, 10, 20` |  |
| `uncommon` | Number | `8, 10, 20` |  |
| `very_rare` | Number | `80, 40, 15` |  |

</details>

---

### Context: `item_groups`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `treasure` | [`Block`](./Shops.md#context-treasure) | `{ ... }` |  |
| `pool` | [`Block`](./Shops.md#context-pool) | `{ ... }` |  |
| `mandatory` | [`Block`](./Shops.md#context-mandatory) | `{ ... }` |  |
| `levelup` | [`Block`](./Shops.md#context-levelup) | `{ ... }` |  |
| `common_item` | [`Block`](./Shops.md#context-common_item) | `{ ... }` |  |
| `consumable` | [`Block`](./Shops.md#context-consumable) | `{ ... }` |  |
| `guaranteed_food` | [`Block`](./Shops.md#context-guaranteed_food) | `{ ... }` |  |
| `item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |
| `mostly_food` | [`Block`](./Shops.md#context-mostly_food) | `{ ... }` |  |
| `empty` | [`Block`](./Shops.md#context-empty) | `{ ... }` |  |

</details>

---

### Context: `breakdown`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `treasure` | Number | `1` |  |
| `pool` | Number | `2, 5, 3` |  |
| `levelup` | Number | `1` |  |
| `mandatory` | Number | `6, 1, 3` |  |
| `consumable` | Number | `2, 1` |  |
| `guaranteed_food` | Number | `1` |  |
| `mostly_food` | Number | `2, 1` |  |
| `empty` | Number | `1` |  |
| `item` | Number | `1` |  |

</details>

---

### Context: `Food`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`guaranteed_food`](./Shops.md#context-guaranteed_food), [`mostly_food`](./Shops.md#context-mostly_food)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allow_duplicates` | Boolean | `true` |  |
| `amount` | Number | `10` |  |
| `cost` | Number | `5` |  |
| `weight` | Number | `5` |  |

</details>

---

### Context: `treasure`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |

</details>

---

### Context: `pool`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |

</details>

---

### Context: `breakdown2`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `common_item` | Number | `1` |  |
| `consumable` | Number | `1` |  |
| `guaranteed_food` | Number | `1` |  |
| `mostly_food` | Number | `1` |  |
| `item` | Number | `1` |  |

</details>

---

### Context: `breakdown4`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `common_item` | Number | `2` |  |
| `consumable` | Number | `1` |  |
| `guaranteed_food` | Number | `1` |  |
| `item` | Number | `2, 1` |  |

</details>

---

### Context: `breakdown3`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `common_item` | Number | `2` |  |
| `consumable` | Number | `1` |  |
| `guaranteed_food` | Number | `1` |  |
| `item` | Number | `1` |  |

</details>

---

### Context: `button_nav`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Shops.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `default` | Block | `{ ... }` |  |

</details>

---

### Context: `mandatory`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |
| `Furniture` | Block | `{ ... }` |  |

</details>

---

### Context: `mostly_food`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Food` | [`Block`](./Shops.md#context-food) | `{ ... }` |  |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |

</details>

---

### Context: `LevelUp`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`levelup`](./Shops.md#context-levelup)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cost` | Number | `10` |  |

</details>

---

### Context: `levelup`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `LevelUp` | [`Block`](./Shops.md#context-levelup) | `{ ... }` |  |

</details>

---

### Context: `common_item`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |

</details>

---

### Context: `consumable`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |

</details>

---

### Context: `guaranteed_food`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Food` | [`Block`](./Shops.md#context-food) | `{ ... }` |  |

</details>

---

### Context: `item`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |

</details>

---

### Context: `empty`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`item_groups`](./Shops.md#context-item_groups)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Item` | [`Block`](./Shops.md#context-item) | `{ ... }` |  |

</details>

---

## Spawns & Enemy Pools

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Fly, Worm, Rat` |  |
| `value` | Number | `0, 1, .5` |  |
| `early_spawn` | Boolean | `true` |  |
| `orientation` | [`Enum/String`](./Enums.md#enum-orientation) | `east, north, south` |  |
| `tag_location` | [`Enum/String`](./Enums.md#enum-tag_location) | `FinalBossCloneSpot, ChaosValidPosition, HitlerMiniInitial` |  |
| `forced_placement` | Boolean | `true` |  |
| `trap` | [`Enum/String`](./Enums.md#enum-trap) | `WaterKittenTrap, WebTrap` |  |
| `image` | String | `"empty.png"` |  |
| `name` | String | `"Empty"` |  |
| `reserved` | [`Enum/String`](./Enums.md#enum-reserved) | `for` |  |
| `utility` | [`Enum/String`](./Enums.md#enum-utility) | `PlayerSpawn` |  |

</details>

---

### Context: `editor`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `category` | Number | `4, 1, 3` |  |
| `image` | [`Array`](./Arrays.md#array-image) | `[ "fly.png" ], [ "rat.png" ], [ "shadow.png" "cat.png" ]` |  |
| `name` | String | `"Fly", "Rat", "Player Cat Spawn"` |  |
| `paint` | Boolean | `false, true` |  |
| `image_tint` | [`Array`](./Arrays.md#array-image_tint) | `[ blue none ], [ yellow ], [ blue ]` |  |
| `subcategory` | Number | `2, 1, 3` |  |
| `layer` | Number | `2` |  |

</details>

---

### Context: `weather_element_alt`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Ice` | Specific element type required or applied. |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `IceElemental` |  |

</details>

---

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
