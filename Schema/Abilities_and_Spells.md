# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

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

