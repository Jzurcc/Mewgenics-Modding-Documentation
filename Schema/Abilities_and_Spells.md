# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Abilities & Spells

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2343) |
| :--- | :--- | :--- | :--- |
| [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance) | Block | Block defining the combat math and status effects applied upon successful hit. | 2343 |
| [`meta`](./Abilities_and_Spells.md#context-meta) | Block | Block defining UI display data (Name, Description, Icon). | 2333 |
| [`template`](./Enums.md#enum-template) | Enum/String | Inherits baseline internal logic from a hardcoded engine template. | 2174 |
| [`graphics`](./Abilities_and_Spells.md#context-graphics) | Block | Block defining visual animations and sequence timings. | 2037 |
| [`target`](./Abilities_and_Spells.md#context-target) | Block | Block defining the shape, range, and restrictions of the ability's aiming phase. | 1862 |
| [`cost`](./Abilities_and_Spells.md#context-cost) | Block | Block defining resource requirements (Mana, Act Points, Moves) needed to cast. | 1851 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum/String | Inherits properties from a previously defined ability (used for upgrading tiers). | 900 |
| [`tags`](./Arrays.md#array-tags) | Array | Array of string categories used by the engine for filtering (e.g. [weapon_throw, spell]). | 238 |
| [`self_damage`](./Abilities_and_Spells.md#context-self_damage) | Block | Recoil or self-inflicted damage/effects applied to the caster. | 218 |
| [`spawn`](./Abilities_and_Spells.md#context-spawn) | Block | Parameters for summoning new characters, objects, or entities. | 192 |
| [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives) | Block | Passives granted to the character while this ability is equipped. | 136 |
| [`class`](./Enums.md#enum-class) | Enum/String | Categorizes the ability for specific UI filters. | 90 |
| [`temporary_effects`](./Abilities_and_Spells.md#context-temporary_effects) | Block | Status applications that wear off automatically or at the end of the turn. | 88 |
| [`sounds`](./Abilities_and_Spells.md#context-sounds) | Block | Audio cues triggered by the ability. | 39 |
| [`splash_damage`](./Abilities_and_Spells.md#context-splash_damage) | Block | Secondary Area of Effect blast parameters. | 34 |
| [`ai_ability`](./Enums.md#enum-ai_ability) | Enum/String | Overrides the ability used when triggered by AI. | 29 |
| [`keyword_tooltips`](./Abilities_and_Spells.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear when hovering over the ability. | 23 |
| [`chain_ability`](./Enums.md#enum-chain_ability) | Enum/String | An ability that automatically executes sequentially after this one. | 15 |
| [`sub_ability`](./Enums.md#enum-sub_ability) | Enum/String | A secondary ability component referenced by complex templates. | 8 |
| [`cloned_ability`](./Enums.md#enum-cloned_ability) | Enum/String | Copies the properties of another ability dynamically. | 2 |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`empty_self_damage`](./Abilities_and_Spells.md#context-empty_self_damage) | Block | Recoil damage specifically applied when the attack misses all targets. | 2 |
| [`bonk_damage`](./Abilities_and_Spells.md#context-bonk_damage) | Block | Damage dealt when knocked into a wall or obstacle. | 1 |
| [`damage`](./Abilities_and_Spells.md#context-damage) | Block | The base damage properties of an attack. | 1 |

</details>

---

### Context: `damage_instance`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#context-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count (X/1785) |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1785 |
| `damage` | Number | The base damage properties of an attack. | 1446 |
| [`type`](./Enums.md#enum-type) | Enum/String | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). | 358 |
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 352 |
| `knockback` | Number | The base physics pushing power (in tiles). | 254 |
| `ai_base_score` | Number | How highly the AI values using this ability. | 223 |
| `heal` | Number | Restores health instead of dealing damage. | 122 |
| `cant_miss` | Boolean | Guarantees the hit, bypassing dodge mechanics. | 110 |
| `incidentally_collects_pickups` | Boolean | Automatically grabs items in the AoE. | 103 |
| [`custom_additional_ai_weight`](./Enums.md#enum-custom_additional_ai_weight) | Enum/String | Granular AI preference adjustments (e.g., `prefer_dont_move`). | 82 |
| `piercing` | Boolean | Ignores a percentage of target defense/armor. | 52 |
| `makes_contact` | Boolean | If false, explicitly avoids triggering contact-based passives. | 40 |
| [`layer`](./Enums.md#enum-layer) | Enum/String | Z-index targeting (e.g., `characters`, `self`). | 26 |
| [`blocked_damage`](./Enums.md#enum-math_equation) | Equation | Base damage dealt if the attack is blocked. | 24 |
| [`raw_damage`](./Enums.md#enum-math_equation) | Equation | Unmitigated, unscaled base numbers. | 22 |
| [`crit_chance`](./Enums.md#enum-crit_chance) | Enum/String | Override for base critical hit probability. | 16 |
| `override_trample_damage` | Boolean | Custom damage value for trample moves. | 15 |
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. | 14 |
| `can_revive` | Boolean | Healing instance that can bring dead allies back to life. | 8 |
| `show_damage_on_0` | Boolean | Forces the "-0" floater text to appear. | 6 |
| `force_play_hit_animation` | Boolean | Forces the flinch animation even on 0 damage. | 5 |
| `blocked_multiplier` | Number | Multiplier applied when hitting a blocking target. | 4 |
| [`accuracy`](./Enums.md#enum-accuracy) | Enum/String | Hit chance modifier. | 3 |
| `can_collect_pickups` | Boolean | The damage instance can grab items on the ground. | 3 |
| `can_instapop` | Boolean | Allows the attack to instantly destroy specific weak entities. | 2 |
| `disallow_modifications` | Boolean | Prevents passives from altering this damage instance. | 2 |
| `force_no_contact` | Boolean | Bypasses all contact-based retaliation (Thorns, etc). | 2 |
| `non_lethal` | Boolean | Reduces target to 1 HP but will never kill. | 2 |
| `raw_heal` | String | Unmitigated, unscaled base numbers. | 2 |
| `two_way_contact` | Boolean | Both caster and target trigger contact effects on each other. | 2 |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 1 |
| `damage_shield_only` | Boolean | Depletes shields but cannot harm base health. | 1 |
| [`faction`](./Enums.md#enum-faction) | Enum/String | Determines alignment (`enemies`, `cats`, `neutral`). | 1 |
| [`final_hit_bonus_damage`](./Enums.md#enum-math_equation) | Equation | Extra damage applied on the last hit of a multihit. | 1 |
| `force_adjacent_and_diagonal_contact` | Boolean | Treats diagonal hits as physical contact. | 1 |
| `force_no_knockback` | Boolean | Prevents the target from being pushed. | 1 |
| `hint_dont_lowgravboost` | Boolean | AI hint to ignore wind physics. | 1 |
| [`hit_animation_alt`](./Enums.md#enum-hit_animation_alt) | Enum/String | Custom flinch animation for the target. | 1 |
| `ranged` | Boolean | Boolean flagging the damage as explicitly ranged. | 1 |

</details>

---

### Context: `meta`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count (X/1641) |
| :--- | :--- | :--- | :--- |
| `desc` | String | The localization key for the ability's display description. | 1641 |
| `name` | String | The localization key for the ability's display name. | 1597 |
| [`class`](./Enums.md#enum-class) | Enum/String | Categorizes the ability for specific UI filters. | 876 |
| `type_icon` | String |  | 283 |
| `animate_name` | Boolean | If true, adds a visual pop/animation to the name text when cast. | 177 |
| [`icon_shell_frame`](./Enums.md#enum-icon_shell_frame) | Enum/String |  | 28 |
| [`is_move`](./Enums.md#enum-is_move) | Enum/String |  | 20 |
| [`ability_icon`](./Enums.md#enum-ability_icon) | Enum/String | The UI icon to display in the action bar. | 14 |
| [`tooltip_values`](./Arrays.md#array-tooltip_values) | Array |  | 9 |
| `icon_damage_display` | String |  | 8 |
| [`icon_damage_display_eq`](./Enums.md#enum-icon_damage_display_eq) | Enum/String |  | 7 |
| `is_basic_attack` | Boolean |  | 4 |
| [`icon_damage_type`](./Enums.md#enum-icon_damage_type) | Enum/String |  | 3 |
| `is_trinket` | Boolean |  | 3 |
| `dont_visualize_ai` | Boolean |  | 2 |
| `icon_damage_display_suffix` | String |  | 2 |
| `is_weapon` | Boolean |  | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum/String |  | 1 |

</details>

---

### Context: `cost`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count (X/1603) |
| :--- | :--- | :--- | :--- |
| `mana` | Number | MP pool and how much it restores per turn. | 1603 |
| `infcantrip` | Boolean | Can be cast infinitely as long as costs are met. | 810 |
| `cantrip` | Boolean | Does not end the turn when cast. | 560 |
| `once_per_fight` | Boolean | Exhausts for the remainder of combat after one use. | 98 |
| `act_points` | Number | Consumes primary action points (default 1). | 86 |
| `move_points` | Number | Consumes movement points. | 59 |
| `prime` | Number | Requires a "priming" turn before it fires. | 30 |
| `allow_offmap_casts` | Boolean | Can be used while the character is hidden/removed from grid. | 22 |
| [`cant_cast`](./Enums.md#enum-cant_cast) | Enum/String | Explicitly disables casting (used for passive-triggered only abilities). | 18 |
| `must_be_consuming` | Boolean | Requires the character to be eating/holding something. | 17 |
| `charge` | Number | Cooldown timers measured in turns. | 16 |
| `must_not_be_consuming` | Boolean | Cannot be holding/eating an entity. | 14 |
| `requires_reload` | Boolean | Must spend an action to reload before casting again. | 14 |
| `can_cast_while_dead` | Boolean | Usable by corpses (e.g., DeathRattle triggers). | 12 |
| [`cantrip_group`](./Enums.md#enum-cantrip_group) | Enum/String | Groups cantrips so using one exhausts the others. | 12 |
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
| `enabled_formula` | Number | Mathematical string required to be >0 to cast. | 3 |
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

### Context: `graphics`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count (X/1559) |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum/String | The primary flash animation label triggered. | 1559 |
| [`particle`](./Enums.md#enum-particle) | Enum/String | References an impact or cast particle effect. | 488 |
| [`projectile`](./Enums.md#enum-projectile) | Enum/String | References a projectile entity. | 228 |
| `lob` | Boolean |  | 130 |
| `delay` | Number | Frame delay before firing projectile/effect. | 93 |
| `dont_visualize_ai` | Boolean |  | 86 |
| `dont_orient` | Boolean | Prevents the character from turning to face the target. | 83 |
| [`dash_animation`](./Enums.md#enum-dash_animation) | Enum/String | State-specific animations for trample/dash abilities. | 65 |
| [`dash_start_animation`](./Enums.md#enum-dash_start_animation) | Enum/String |  | 63 |
| `speed` | Number | Rotations per second. | 61 |
| [`affected_particle`](./Enums.md#enum-affected_particle) | Enum/String | Visuals applied to the target receiving the effect. | 51 |
| [`dash_attack_animation`](./Enums.md#enum-dash_attack_animation) | Enum/String |  | 45 |
| `lob_height` | Number | Adjustments for arcing projectiles. | 45 |
| [`animation_in`](./Enums.md#enum-animation_in) | Enum/String | Used for transition states (like burrowing). | 43 |
| [`animation_out`](./Enums.md#enum-animation_out) | Enum/String | Used for transition states (like burrowing). | 43 |
| [`jump_attack_animation`](./Enums.md#enum-jump_attack_animation) | Enum/String | Overrides for jump physics. | 39 |
| `use_projectile` | Boolean |  | 35 |
| [`full_jump_animation`](./Enums.md#enum-full_jump_animation) | Enum/String |  | 24 |
| `full_jump_sync_frames` | Number |  | 24 |
| `use_rotation` | Boolean |  | 24 |
| [`dash_end_animation`](./Enums.md#enum-dash_end_animation) | Enum/String |  | 22 |
| `palette` | Number | Swaps the color palette ID. | 21 |
| `full_jump_windup_frames` | Number |  | 20 |
| `visual_delay_but_simultaneous_damage` | Number |  | 18 |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum/String | Specific spawn points for particles. | 17 |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum/String | Specific spawn points for particles. | 16 |
| `fall_from_sky` | Boolean | Spawns the projectile from the top of the screen. | 16 |
| [`move_start_animation`](./Enums.md#enum-move_start_animation) | Enum/String |  | 14 |
| `use_placeholder` | Boolean |  | 14 |
| [`move_end_animation`](./Enums.md#enum-move_end_animation) | Enum/String |  | 13 |
| `face_toss_target` | Boolean |  | 12 |
| `ignore_slowtiles` | Boolean |  | 12 |
| [`chain_distance`](./Enums.md#enum-chain_distance) | Enum/String | Creates a tethered repeating graphic (like a hook). | 11 |
| [`chain_movieclip`](./Enums.md#enum-chain_movieclip) | Enum/String | Creates a tethered repeating graphic (like a hook). | 11 |
| `darken_screen` | Boolean | Dims the background during the ability cast. | 11 |
| [`beam_cap`](./Enums.md#enum-beam_cap) | Enum/String | Flash movieclips used to render continuous laser beams. | 10 |
| [`beam_clip`](./Enums.md#enum-beam_clip) | Enum/String | Flash movieclips used to render continuous laser beams. | 10 |
| `bounce_on_hit` | Boolean | Visual hop when striking a target. | 10 |
| `darken_screen_exclude_characters_on_tile` | Boolean |  | 10 |
| [`end`](./Enums.md#enum-end) | Enum/String | Segments for continuous channeled animations. | 10 |
| [`jump_start_animation`](./Enums.md#enum-jump_start_animation) | Enum/String |  | 10 |
| [`loop`](./Enums.md#enum-loop) | Enum/String | Segments for continuous channeled animations. | 10 |
| [`prime_animation`](./Enums.md#enum-prime_animation) | Enum/String |  | 10 |
| [`start`](./Enums.md#enum-start) | Enum/String | Segments for continuous channeled animations. | 10 |
| `max_tiles_single_loop` | Number |  | 9 |
| [`random_delay`](./Arrays.md#array-random_delay) | Array | Adds chaotic timing to multi-projectile casts. | 9 |
| `sync_speed` | Number |  | 9 |
| `fx_is_placeholder_animation` | Boolean |  | 8 |
| `aoe_spell_on_land` | Boolean | Visual trigger when a jump lands. | 7 |
| `fx_random_flip` | Boolean |  | 7 |
| [`land_animation`](./Enums.md#enum-land_animation) | Enum/String |  | 7 |
| [`miss_particle`](./Enums.md#enum-miss_particle) | Enum/String | Specific spawn points for particles. | 7 |
| `use_super_armor` | Boolean | Prevents flinch animations from interrupting this cast. | 7 |
| [`air_animation`](./Enums.md#enum-air_animation) | Enum/String | Animation played while entity is airborne. | 6 |
| [`custom_priming_animation`](./Enums.md#enum-custom_priming_animation) | Enum/String | Animation used while charging an ability. | 6 |
| `darken_screen_exclude_self` | Boolean |  | 6 |
| `darken_screen_start_early` | Boolean |  | 6 |
| [`fall_randomize_timing`](./Enums.md#enum-fall_randomize_timing) | Enum/String |  | 6 |
| `min_throw_height` | Number |  | 6 |
| [`miss_random_delay`](./Arrays.md#array-miss_random_delay) | Array |  | 6 |
| `single_projectile` | Boolean |  | 6 |
| [`detatched_animation`](./Enums.md#enum-detatched_animation) | Enum/String | Plays an animation separated from the character body. | 5 |
| `detatched_animation_reach` | Number |  | 5 |
| [`empty_animation`](./Enums.md#enum-empty_animation) | Enum/String |  | 5 |
| [`mode`](./Enums.md#enum-mode) | Enum/String |  | 5 |
| `fixed_jump_height` | Number |  | 4 |
| [`rocket_swirl`](./Abilities_and_Spells.md#context-rocket_swirl) | Block | Visual parameters for swirling projectile paths. | 4 |
| `sync_frames` | Number |  | 4 |
| [`dash_decelerating_animation`](./Enums.md#enum-dash_decelerating_animation) | Enum/String |  | 3 |
| `decelerate` | Number | Visual slowdown at the end of a movement. | 3 |
| `delay_from_map_edge` | Boolean | Delays effect based on distance from the screen edge. | 3 |
| `easing` | Number | Smoothing function for movement animations. | 3 |
| `fixed_jump_speed` | Number |  | 3 |
| [`grab_animation`](./Enums.md#enum-grab_animation) | Enum/String |  | 3 |
| [`lob_yoff`](./Enums.md#enum-lob_yoff) | Enum/String | Adjustments for arcing projectiles. | 3 |
| `lock_orientation_during_dash` | Boolean | Prevents the sprite from flipping mid-dash. | 3 |
| `use_projectile_spawn_offset` | Boolean |  | 3 |
| `use_rotation_once` | Boolean |  | 3 |
| `always_play_animations` | Boolean | Bypasses speed-up/skip logic. | 2 |
| `detatched_animation_cutoff` | Boolean |  | 2 |
| `do_damage_immediately` | Boolean | Applies math before the animation actually hits. | 2 |
| `jump_height_multiplier` | Number | Overrides for jump physics. | 2 |
| [`mask_center`](./Enums.md#enum-mask_center) | Enum/String |  | 2 |
| [`mask_extent`](./Enums.md#enum-mask_extent) | Enum/String |  | 2 |
| `max_throw_height` | Number |  | 2 |
| [`particle_mat`](./Enums.md#enum-particle_mat) | Enum/String |  | 2 |
| [`preturn_animation`](./Enums.md#enum-preturn_animation) | Enum/String |  | 2 |
| `primed_alt_animation` | String |  | 2 |
| [`pseudoprojectile`](./Enums.md#enum-pseudoprojectile) | Enum/String |  | 2 |
| `reverse_orientation` | Boolean |  | 2 |
| `self_damage_mid_port` | Boolean |  | 2 |
| `throw_speed` | Number |  | 2 |
| `use_hit_alts` | Boolean |  | 2 |
| [`affected_animation`](./Enums.md#enum-affected_animation) | Enum/String | Visuals applied to the target receiving the effect. | 1 |
| [`ally_animation`](./Enums.md#enum-ally_animation) | Enum/String | Distinct animation used when targeting a friendly unit. | 1 |
| [`animate_name`](./Enums.md#enum-animate_name) | Enum/String | Animates the ability name text on cast. | 1 |
| `apex_distance` | Number | Calculations for the peak of a jump/lob arc. | 1 |
| [`apex_time`](./Enums.md#enum-apex_time) | Enum/String | Calculations for the peak of a jump/lob arc. | 1 |
| `bypass_combatspeed` | Boolean |  | 1 |
| [`damage_threshold_altanimations`](./Abilities_and_Spells.md#context-damage_threshold_altanimations) | Block | Triggers different hit animations based on the amount of damage dealt. | 1 |
| [`dash_bonk_animation`](./Enums.md#enum-dash_bonk_animation) | Enum/String |  | 1 |
| `delay_from_map_center` | Boolean | Positional based timing delays. | 1 |
| `delay_from_reverse_map_edge` | Boolean |  | 1 |
| `do_animation_offscreen` | Boolean |  | 1 |
| `do_not_clear_placeholder` | Boolean |  | 1 |
| `face_targets` | Boolean | Forces the sprite to look at the target tile. | 1 |
| `first_castpoint_is_self_damage_only` | Boolean |  | 1 |
| [`hang_time`](./Enums.md#enum-hang_time) | Enum/String |  | 1 |
| `jump_speed_multiplier` | Number |  | 1 |
| [`lob_speed`](./Enums.md#enum-lob_speed) | Enum/String | Adjustments for arcing projectiles. | 1 |
| `max_range` | Number | The maximum and minimum distance required to cast. | 1 |
| `min_range` | Number | The maximum and minimum distance required to cast. | 1 |
| `othercat_placeholder_available` | Boolean |  | 1 |
| [`precast_delay`](./Enums.md#enum-precast_delay) | Enum/String |  | 1 |
| [`spawn_offset`](./Arrays.md#array-spawn_offset) | Array |  | 1 |
| `uncatchable` | Boolean |  | 1 |
| `use_directional_animations` | Boolean |  | 1 |
| `use_origin_offsets` | Boolean |  | 1 |

</details>

---

### Context: `target`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count (X/1088) |
| :--- | :--- | :--- | :--- |
| `max_range` | Number | The maximum and minimum distance required to cast. | 1088 |
| `max_aoe` | Number | The maximum and minimum radius/length of the AoE. | 795 |
| `min_range` | Number | The maximum and minimum distance required to cast. | 583 |
| [`target_mode`](./Enums.md#enum-target_mode) | Enum/String | How the cursor operates (`tile`, `direction`, `none`). | 503 |
| [`restrictions`](./Arrays.md#array-restrictions) | Array | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). | 463 |
| [`aoe_mode`](./Enums.md#enum-aoe_mode) | Enum/String | The shape of the area (`standard`, `line`, `cross`, `square`, `custom`). | 432 |
| [`knockback_mode`](./Enums.md#enum-knockback_mode) | Enum/String | How physics vectors apply (`character_to_tile`, `pull_to_character`, `zero`, `orientation`). | 265 |
| `min_aoe` | Number | The maximum and minimum radius/length of the AoE. | 253 |
| `aoe_excludes_self` | Boolean | Prevents the AoE from hitting the caster. | 241 |
| [`aoe_restrictions`](./Arrays.md#array-aoe_restrictions) | Array | Array of conditions the AoE tiles must meet (e.g., `must_have_line_of_sight_unpurgable`). | 197 |
| `aoe_considers_character_size` | Boolean | Scales the AoE based on the caster's tile size (e.g., 2x2). | 170 |
| [`range_mode`](./Enums.md#enum-range_mode) | Enum/String | How range is counted (`standard`, `ground_move`). | 114 |
| [`X_is`](./Enums.md#enum-x_is) | Enum/String | Applies or references the 'X_is' effect/state. | 86 |
| [`custom_aoe`](./Arrays.md#array-custom_aoe) | Array | Array of exact coordinates for a custom shape (e.g., `[[1, -1] [1, 0]]`). | 83 |
| `multihit` | Number | Hardcoded number of times the ability hits the target. | 62 |
| `max_targets` | Number | Limits on how many distinct entities can be targeted. | 56 |
| `range_excludes_blocking` | Boolean | Cannot target through walls/obstacles. | 53 |
| `prioritize_dont_change_direction` | Number | AI preference to maintain current facing angle. | 52 |
| [`target_requires_tag`](./Enums.md#enum-target_requires_tag) | Enum/String | Target must possess this exact character tag. | 40 |
| [`aoe_symmetry`](./Enums.md#enum-aoe_symmetry) | Enum/String | Determines if the AoE mirrors on axes. | 28 |
| `prioritize_face_camera` | Number | AI preference to face South. | 26 |
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
| `N` | Number | Variable modifier parameter. | 7 |
| [`custom_range`](./Arrays.md#array-custom_range) | Array | Overrides standard range scaling. | 7 |
| `always_bounce` | Boolean | Forces the attack/projectile to bounce regardless of hit. | 6 |
| [`custom_aoe_util`](./Arrays.md#array-custom_aoe_util) | Array | Utility variants of custom AoE definitions. | 6 |
| `multihit_max` | Number | Variable limits for random multihit abilities. | 6 |
| `multihit_min` | Number | Variable limits for random multihit abilities. | 6 |
| `reorient_thrown_character` | Boolean | Forces a thrown entity to face a certain way. | 6 |
| [`toss_direction_restriction`](./Enums.md#enum-toss_direction_restriction) | Enum/String | Limits which ways an entity can be tossed. | 6 |
| `aoe_hint_teamcast` | Boolean | Visual hint for cooperative casting abilities. | 5 |
| [`aoe_tile_requires_element`](./Enums.md#enum-aoe_tile_requires_element) | Enum/String | Only affects tiles painted with a specific element. | 5 |
| `distance_sort_targets` | Number | Prioritizes targets based on proximity. | 5 |
| `dont_orient_aoe` | Boolean | Prevents the AoE shape from rotating with the character. | 5 |
| `hint_can_target_pickups` | Boolean | UI hint that the player can target items on the ground. | 5 |
| `max_bounces` | Number | Hard cap on how many times a bouncing effect can trigger. | 5 |
| `splash_damage_aoe_begin` | Number | At what radius splash damage starts applying. | 5 |
| [`aoe_chance`](./Enums.md#enum-aoe_chance) | Enum/String | Percentage chance for the AoE to trigger. | 4 |
| `as_the_crow_flies` | Boolean | Calculates range ignoring all pathing terrain obstacles. | 4 |
| `force_ai_target_as_spell` | Boolean | Forces the AI to treat a physical move like a spell for targeting logic. | 4 |
| [`mouse_offset`](./Arrays.md#array-mouse_offset) | Array | Visual offset for the targeting cursor. | 4 |
| `range_display_include_aoe` | Boolean | Visual: shows the full AoE potential when previewing range. | 4 |
| `shotgun_mode` | Boolean | Deals more damage/hits if targets are closer. | 4 |
| `shuffle_tile_order` | Boolean | Randomizes the execution order of AoE tiles. | 4 |
| `upgrade_straight_shot_to_boomerang` | Boolean | Makes the projectile return to caster. | 4 |
| `dont_orient` | Boolean | Prevents the character from turning to face the target. | 3 |
| [`low_health_character_threshold`](./Enums.md#enum-low_health_character_threshold) | Enum/String | AI targeting threshold for seeking weak targets. | 3 |
| `randomize_target_within_range` | Number | Picks a random valid tile instead of the user's click. | 3 |
| [`special_tile_tag`](./Enums.md#enum-special_tile_tag) | Enum/String | Targets only tiles with this specific tag. | 3 |
| `track_target` | Boolean | Projectile/Effect follows moving targets. | 3 |
| `corpse_priority` | Number | AI preference for targeting dead bodies. | 2 |
| `hint_can_target_empty` | Boolean | UI hint that the player can click an empty tile. | 2 |
| `low_gravity_boostable` | Boolean | Can be affected by low gravity wind/effects. | 2 |
| `prioritize_change_direction` | Boolean | AI preference to attack from different angles. | 2 |
| [`range_bonuses`](./Enums.md#enum-range_bonuses) | Enum/String | How much extra range is added by stats/passives. | 2 |
| `range_display_include_direction` | Boolean | Visual: shows directional arrows. | 2 |
| `recalc_target_on_castpoint` | Boolean | Re-checks if target is valid at the exact frame of cast. | 2 |
| `redirect_location_if_blocked` | Boolean | Shifts target to adjacent tile if original is invalid. | 2 |
| [`target_requires_element`](./Arrays.md#array-target_requires_element) | Array | Target must be afflicted with this element. | 2 |
| `trample_allies_too` | Boolean | Trample movement damages allies in the path. | 2 |
| [`adjust_target`](./Enums.md#enum-adjust_target) | Enum/String | Tweaks target selection post-cast. | 1 |
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
| `force_no_contact` | Boolean | Bypasses all contact-based retaliation (Thorns, etc). | 1 |
| `hint_can_target_static` | Boolean | UI hint that the player can target inanimate objects. | 1 |
| [`knockback_modifier`](./Enums.md#enum-knockback_modifier) | Enum/String | Multiplier for the knockback physics force. | 1 |
| `lingering` | Boolean | Target zone remains active across multiple turns. | 1 |
| `mirror_custom_aoe` | Boolean | Flips the custom AoE array. | 1 |
| [`prioritize_throw_target_with_passive`](./Enums.md#enum-prioritize_throw_target_with_passive) | Enum/String | AI prefers throwing targets that have specific passives. | 1 |
| `randomize_knockback_direction_except_for_finisher` | Boolean | Chaotic knockback unless it kills the target. | 1 |
| `range_excludes_self` | Boolean | Cannot click on the caster's tile. | 1 |
| `range_max` | Number | Alternate syntax for `max_range`/`min_range`. | 1 |
| `range_min` | Number | Alternate syntax for `max_range`/`min_range`. | 1 |
| [`range_symmetry`](./Enums.md#enum-range_symmetry) | Enum/String | Mirrors the range grid. | 1 |
| `remain_off_map` | Boolean | Keeps entity removed from the grid. | 1 |
| [`restructions`](./Enums.md#enum-restructions) | Enum/String | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). | 1 |
| `reverse_target_direction` | Boolean | Inverts the targeting vector. | 1 |
| `spin_steps` | Number | Number of rotational increments for spin targeting. | 1 |
| `uncounterable` | Boolean | Bypasses counter-attack passives. | 1 |

</details>

---

### Context: `self_damage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#context-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count (X/200) |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 200 |
| `damage` | Number | The base damage properties of an attack. | 47 |
| `piercing` | Boolean |  | 12 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification/category type. | 11 |
| `cant_miss` | Boolean |  | 10 |
| `knockback` | Number |  | 10 |
| `heal` | Number |  | 6 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 4 |
| `ai_base_score` | Number |  | 2 |
| `non_lethal` | Boolean |  | 1 |

</details>

---

### Context: `spawn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count (X/184) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 184 |
| [`faction`](./Enums.md#enum-faction) | Enum/String |  | 59 |
| `ai_base_score` | Number |  | 31 |
| [`additional_passives`](./Abilities_and_Spells.md#context-additional_passives) | Block | Passives granted intrinsically to a spawned entity. | 20 |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum/String |  | 17 |
| [`layer`](./Enums.md#enum-layer) | Enum/String |  | 14 |
| [`catdata`](./Enums.md#enum-catdata) | Enum/String | Defines genetic/clone data cloning. | 13 |
| `clone_items` | Boolean | If true, transfers inventory to the clone. | 12 |
| `lob` | Boolean |  | 4 |
| [`post_spawn_statuses`](./Abilities_and_Spells.md#context-post_spawn_statuses) | Block | Status effects applied immediately after an entity spawns. | 4 |
| `size` | Number |  | 4 |
| `face_camera` | Boolean |  | 2 |
| `inherit_elite_buffs` | Boolean |  | 2 |
| `start_dead` | Boolean |  | 2 |
| [`appearance`](./Enums.md#enum-appearance) | Enum/String |  | 1 |
| [`auto_cast_on_spawn`](./Enums.md#enum-auto_cast_on_spawn) | Enum/String |  | 1 |
| [`chapter`](./Enums.md#enum-chapter) | Enum/String |  | 1 |
| [`custom_additional_ai_weight`](./Enums.md#enum-custom_additional_ai_weight) | Enum/String |  | 1 |
| `include_passives` | Boolean |  | 1 |
| `redirect_location_if_blocked` | Boolean |  | 1 |
| [`spawnin_animation`](./Enums.md#enum-spawnin_animation) | Enum/String |  | 1 |
| `trigger_battle_start` | Boolean |  | 1 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](./Abilities_and_Spells.md#context-dodamage), [`MeleeRevengeDamage`](./Abilities_and_Spells.md#context-meleerevengedamage), [`ROOT`](./Abilities_and_Spells.md#context-root), [`RevengeDamage`](./Abilities_and_Spells.md#context-revengedamage), [`bonk_damage`](./Abilities_and_Spells.md#context-bonk_damage), [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance), [`empty_self_damage`](./Abilities_and_Spells.md#context-empty_self_damage), [`self_damage`](./Abilities_and_Spells.md#context-self_damage), [`splash_damage`](./Abilities_and_Spells.md#context-splash_damage)

| Property Key | Type | Definition | Count (X/102) |
| :--- | :--- | :--- | :--- |
| [`FormChange`](./Enums.md#enum-formchange) | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 102 |
| `Stun` | Number | Applies or references the 'Stun' effect/state. | 89 |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 76 |
| `IgnoreSelf` | Number | Applies or references the 'IgnoreSelf' effect/state. | 75 |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 70 |
| `Poison` | Number | Applies or references the 'Poison' effect/state. | 65 |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum/String | Transforms the terrain tile under the target. | 62 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 59 |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. | 54 |
| [`Shield`](./Enums.md#enum-math_equation) | Equation | Applies or references the 'Shield' effect/state. | 49 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 44 |
| [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag) | Block | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 38 |
| [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy) | Block | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 35 |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 35 |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 34 |
| [`Temporary`](./Abilities_and_Spells.md#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 34 |
| [`BounceObject`](./Enums.md#enum-bounceobject) | Enum/String | Spawns a physics object that visually bounces off the target. | 31 |
| [`AllStatsUp`](./Enums.md#enum-allstatsup) | Enum/String | Applies or references the 'AllStatsUp' effect/state. | 29 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 28 |
| [`TransformAbility`](./Enums.md#enum-transformability) | Enum/String | Applies or references the 'TransformAbility' effect/state. | 28 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 27 |
| [`ManaGain`](./Enums.md#enum-math_equation) | Equation | Applies or references the 'ManaGain' effect/state. | 26 |
| [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally) | Block | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 25 |
| `Slow` | Number | Applies or references the 'Slow' effect/state. | 25 |
| `Fear` | Number | Applies or references the 'Fear' effect/state. | 23 |
| `Weakness` | Number | Applies or references the 'Weakness' effect/state. | 23 |
| `Blind` | Number | Applies or references the 'Blind' effect/state. | 22 |
| `Leech` | Number | Applies or references the 'Leech' effect/state. | 22 |
| [`StrengthUp`](./Enums.md#enum-strengthup) | Enum/String | Applies or references the 'StrengthUp' effect/state. | 22 |
| `ConstitutionUp` | Number | Applies or references the 'ConstitutionUp' effect/state. | 21 |
| [`EvolveAbilityFromPool`](./Enums.md#enum-evolveabilityfrompool) | Enum/String | Upgrades or transforms an existing ability into a new one from the specified pool. | 21 |
| `Immobile` | Number | Applies or references the 'Immobile' effect/state. | 21 |
| [`IntelligenceUp`](./Enums.md#enum-intelligenceup) | Enum/String | Applies or references the 'IntelligenceUp' effect/state. | 21 |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum/String | Applies or references the 'VisualFXTile' effect/state. | 21 |
| `Charmed` | Number | Applies or references the 'Charmed' effect/state. | 20 |
| `Sleep` | Number | Applies or references the 'Sleep' effect/state. | 20 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 20 |
| `Madness` | Number | Applies the Madness debuff/status effect. | 19 |
| `Brace` | Number | Applies or references the 'Brace' effect/state. | 17 |
| `CollectsPickups` | Number | Applies or references the 'CollectsPickups' effect/state. | 17 |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#context-knockupandaway) | Block | Displaces the target vertically and horizontally away from the source. | 17 |
| `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. | 17 |
| `Freeze` | Number | Applies or references the 'Freeze' effect/state. | 16 |
| `OverrideKnockbackDamage` | Number | Applies or references the 'OverrideKnockbackDamage' effect/state. | 16 |
| [`Consumed`](./Abilities_and_Spells.md#context-consumed) | Block | State block triggered when this object or entity is eaten/consumed by another character. | 15 |
| `VaporizeCorpse` | Number | Applies or references the 'VaporizeCorpse' effect/state. | 15 |
| [`ChangeCatClass`](./Enums.md#enum-changecatclass) | Enum/String | Applies or references the 'ChangeCatClass' effect/state. | 14 |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 14 |
| `EndTurn` | Number | Applies or references the 'EndTurn' effect/state. | 14 |
| `FaceAway` | Number | Applies or references the 'FaceAway' effect/state. | 14 |
| `RefreshMovePoints` | Number | Applies or references the 'RefreshMovePoints' effect/state. | 14 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 14 |
| [`TransformBasicAttack`](./Enums.md#enum-transformbasicattack) | Enum/String | Applies or references the 'TransformBasicAttack' effect/state. | 14 |
| [`CatPartsTransform`](./Abilities_and_Spells.md#context-catpartstransform) | Block | Transforms specific body parts into different visual variants. | 13 |
| [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss) | Block | Conditional trigger: Executes nested logic if the target is a Boss. | 13 |
| `GenericDebuff` | Number | Applies or references the 'GenericDebuff' effect/state. | 13 |
| `Leeches` | Number | Applies or references the 'Leeches' effect/state. | 13 |
| `Petrify` | Number | Applies or references the 'Petrify' effect/state. | 13 |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. | 13 |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 13 |
| `Displace` | Number | Applies or references the 'Displace' effect/state. | 12 |
| [`LuckUp`](./Enums.md#enum-luckup) | Enum/String | Applies or references the 'LuckUp' effect/state. | 12 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill) | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 11 |
| [`ChanceToBreakFree`](./Abilities_and_Spells.md#context-chancetobreakfree) | Block | Provides a probability to escape a grapple or restraining effect. | 11 |
| `Cleave` | Number | Causes the attack to hit adjacent enemies alongside the primary target. | 11 |
| [`Conditional_GoodRoll`](./Abilities_and_Spells.md#context-conditional_goodroll) | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 11 |
| [`DoScreenShake`](./Abilities_and_Spells.md#context-doscreenshake) | Block | Triggers a camera screen shake effect. | 11 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 11 |
| [`Conditional_FormulaIsPositive`](./Abilities_and_Spells.md#context-conditional_formulaispositive) | Block | Conditional trigger: Executes nested logic if the evaluated mathematical formula returns a value greater than 0. | 10 |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative) | Block | A simulation block used by the AI to test hypothetical outcomes before committing to an action. | 10 |
| [`DexterityUp`](./Enums.md#enum-dexterityup) | Enum/String | Applies or references the 'DexterityUp' effect/state. | 10 |
| `MagicWeakness` | Number | Applies or references the 'MagicWeakness' effect/state. | 10 |
| `PartialPurge` | Number | Applies or references the 'PartialPurge' effect/state. | 10 |
| `PurgeAll` | Number | Applies or references the 'PurgeAll' effect/state. | 10 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 10 |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. | 10 |
| `Ammo` | Number | Applies or references the 'Ammo' effect/state. | 9 |
| [`ApplyPassives`](./Abilities_and_Spells.md#context-applypassives) | Block | Grants the nested passive abilities dynamically. | 9 |
| `DeferVaporize` | Number | Applies or references the 'DeferVaporize' effect/state. | 9 |
| `Marked` | Number | Applies or references the 'Marked' effect/state. | 9 |
| `SpawnCreep` | Number | Applies or references the 'SpawnCreep' effect/state. | 9 |
| [`VisualFX`](./Enums.md#enum-visualfx) | Enum/String | Applies or references the 'VisualFX' effect/state. | 9 |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate) | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 8 |
| `ChanceToBreak` | Number | Applies or references the 'ChanceToBreak' effect/state. | 8 |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 8 |
| `OverrideChainKnockback` | Number | Applies or references the 'OverrideChainKnockback' effect/state. | 8 |
| `Rot` | Number | Applies or references the 'Rot' effect/state. | 8 |
| `AlphaCat` | Number | Applies or references the 'AlphaCat' effect/state. | 7 |
| [`ApplyStatusIfCrit`](./Abilities_and_Spells.md#context-applystatusifcrit) | Block | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. | 7 |
| `BramblesOnHit` | Number | Applies or references the 'BramblesOnHit' effect/state. | 7 |
| `ContextualHeal` | Number | Applies or references the 'ContextualHeal' effect/state. | 7 |
| `ForceAttack` | Number | Forces the character to execute an immediate attack. | 7 |
| `Instakill` | Number | Applies or references the 'Instakill' effect/state. | 7 |
| `KnockbackDamageImmuneUntilSettled` | Number | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. | 7 |
| `ManaSteal` | Number | Applies or references the 'ManaSteal' effect/state. | 7 |
| `Tech` | Number | Applies or references the 'Tech' effect/state. | 7 |
| `TempRangeUp` | Number | Applies or references the 'TempRangeUp' effect/state. | 7 |
| [`TriggerWerewolfTransform`](./Arrays.md#array-triggerwerewolftransform) | Array | Applies or references the 'TriggerWerewolfTransform' effect/state. | 7 |
| `BackflipWhenTargeted` | Number | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. | 6 |
| [`BounceRock`](./Enums.md#enum-bouncerock) | Enum/String | Applies or references the 'BounceRock' effect/state. | 6 |
| [`CharismaUp`](./Enums.md#enum-charismaup) | Enum/String | Applies or references the 'CharismaUp' effect/state. | 6 |
| `ClearStarving` | Number | Applies or references the 'ClearStarving' effect/state. | 6 |
| [`Conditional_Corpse`](./Abilities_and_Spells.md#context-conditional_corpse) | Block | Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 6 |
| [`ConjureBonusAbility`](./Enums.md#enum-conjurebonusability) | Enum/String | Adds a temporary bonus ability to the character's hand/deck. | 6 |
| [`Craft`](./Abilities_and_Spells.md#context-craft) | Block | Synthesizes or spawns a new item from a specific pool. | 6 |
| [`DoDistortionRing`](./Abilities_and_Spells.md#context-dodistortionring) | Block | Creates a visual distortion ring effect on the screen. | 6 |
| `Metronome` | Number | Executes a random musical or metronome ability. | 6 |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum/String | Spawns a specific character or entity upon impact. | 6 |
| `RandomInjury` | Number | Applies or references the 'RandomInjury' effect/state. | 6 |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 6 |
| `ScatterHeldCoin` | Number | Applies or references the 'ScatterHeldCoin' effect/state. | 6 |
| `SetDistanceDisplace` | Number | Applies or references the 'SetDistanceDisplace' effect/state. | 6 |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. | 6 |
| [`SpawnThingIfHitKills`](./Enums.md#enum-spawnthingifhitkills) | Enum/String | Applies or references the 'SpawnThingIfHitKills' effect/state. | 6 |
| `SpiderInfested` | Number | Applies or references the 'SpiderInfested' effect/state. | 6 |
| `Tarred` | Number | Applies or references the 'Tarred' effect/state. | 6 |
| [`TeamCastAbility`](./Enums.md#enum-teamcastability) | Enum/String | Requires or involves multiple characters to execute the ability. | 6 |
| [`TwisterDisplaceWithDamage`](./Abilities_and_Spells.md#context-twisterdisplacewithdamage) | Block | A whirlwind effect that randomly displaces targets and deals damage. | 6 |
| [`CollectsPickupsWithAltEffects`](./Abilities_and_Spells.md#context-collectspickupswithalteffects) | Block | Triggers alternative nested effects when collecting items or pickups. | 5 |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#context-conditional_hasstatus) | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 5 |
| [`Conditional_InForm`](./Abilities_and_Spells.md#context-conditional_inform) | Block | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 5 |
| [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss) | Block | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 5 |
| [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object) | Block | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 5 |
| [`Conditional_PlayerCat`](./Abilities_and_Spells.md#context-conditional_playercat) | Block | Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 5 |
| `DodgeChance_Status` | Number | Applies or references the 'DodgeChance_Status' effect/state. | 5 |
| `Drowsy` | Number | Applies or references the 'Drowsy' effect/state. | 5 |
| `FillMana` | Number | Applies or references the 'FillMana' effect/state. | 5 |
| `FlatLeech` | Number | Applies or references the 'FlatLeech' effect/state. | 5 |
| `ForceMoveAway` | Number | Applies or references the 'ForceMoveAway' effect/state. | 5 |
| `ForceMoveTowards` | Number | Applies or references the 'ForceMoveTowards' effect/state. | 5 |
| `HitExplosion` | Number | Applies or references the 'HitExplosion' effect/state. | 5 |
| [`Imprison`](./Enums.md#enum-imprison) | Enum/String | Applies or references the 'Imprison' effect/state. | 5 |
| `KnockbackDirectionIsFacingDirection` | Number | Applies or references the 'KnockbackDirectionIsFacingDirection' effect/state. | 5 |
| `MonkStanceSwitch` | Number | Applies or references the 'MonkStanceSwitch' effect/state. | 5 |
| `MovementUp` | Number | Applies or references the 'MovementUp' effect/state. | 5 |
| [`ObjectOnHit`](./Enums.md#enum-objectonhit) | Enum/String | Spawns a specific physics/item object upon impact. | 5 |
| [`ObjectOnHitEmpty`](./Enums.md#enum-objectonhitempty) | Enum/String | Applies or references the 'ObjectOnHitEmpty' effect/state. | 5 |
| [`PopAndSpawn`](./Enums.md#enum-popandspawn) | Enum/String | Destroys the target and replaces it with a new spawned entity. | 5 |
| `Purge` | Number | Applies or references the 'Purge' effect/state. | 5 |
| `RefreshMovePointsIfHit` | Number | Applies or references the 'RefreshMovePointsIfHit' effect/state. | 5 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 5 |
| `SafeDie` | Number | Applies or references the 'SafeDie' effect/state. | 5 |
| `SoulLink` | Number | Applies or references the 'SoulLink' effect/state. | 5 |
| `SpawnBearTrap` | Number | Applies or references the 'SpawnBearTrap' effect/state. | 5 |
| `SpawnRock` | Number | Applies or references the 'SpawnRock' effect/state. | 5 |
| `Stealth` | Number | Applies or references the 'Stealth' effect/state. | 5 |
| `TempDamageUp` | Number | Applies or references the 'TempDamageUp' effect/state. | 5 |
| `UpgradeRandomAbility` | Number | Applies or references the 'UpgradeRandomAbility' effect/state. | 5 |
| `Webbed` | Number | Applies or references the 'Webbed' effect/state. | 5 |
| [`ApplyToConsumed`](./Abilities_and_Spells.md#context-applytoconsumed) | Block | Redirects the nested effects to apply to the entity that just consumed this object. | 4 |
| [`ArcLightning`](./Abilities_and_Spells.md#context-arclightning) | Block | Executes a chain-lightning logic block that bounces between targets. | 4 |
| `BurgleCoin` | Number | Applies or references the 'BurgleCoin' effect/state. | 4 |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 4 |
| [`Conditional_Familiar`](./Abilities_and_Spells.md#context-conditional_familiar) | Block | Conditional trigger: Executes nested logic if the target is a familiar. | 4 |
| [`EnableWeather`](./Enums.md#enum-enableweather) | Enum/String | Applies or references the 'EnableWeather' effect/state. | 4 |
| `ExplosionIfHitSomething` | Number | Applies or references the 'ExplosionIfHitSomething' effect/state. | 4 |
| `FaceCamera` | Number | Applies or references the 'FaceCamera' effect/state. | 4 |
| `Grappled` | Number | Applies or references the 'Grappled' effect/state. | 4 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 4 |
| [`LateStatusApplication`](./Abilities_and_Spells.md#context-latestatusapplication) | Block | Applies a status effect after all primary damage and effects have fully resolved. | 4 |
| `RandomStatDown` | Number | Applies or references the 'RandomStatDown' effect/state. | 4 |
| `Reanimate` | Number | Applies or references the 'Reanimate' effect/state. | 4 |
| `RemoveActPoints` | Number | Applies or references the 'RemoveActPoints' effect/state. | 4 |
| `SendRock` | Number | Applies or references the 'SendRock' effect/state. | 4 |
| [`SpecificInjury`](./Enums.md#enum-specificinjury) | Enum/String | Applies or references the 'SpecificInjury' effect/state. | 4 |
| [`SwitchMusic`](./Abilities_and_Spells.md#context-switchmusic) | Block | Changes the background music track or layer during combat. | 4 |
| [`TakeBonusTurnWithStatus`](./Abilities_and_Spells.md#context-takebonusturnwithstatus) | Block | Grants the character an immediate extra turn while afflicted with specific statuses. | 4 |
| [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication) | Block | Delays the nested effects by a specified amount of real-time seconds. | 4 |
| [`UseAbility`](./Enums.md#enum-useability) | Enum/String | Forces the character or target to instantly use a specified ability. | 4 |
| `VaporizeInanimate` | Number | Applies or references the 'VaporizeInanimate' effect/state. | 4 |
| [`ApplyMultipleTimes`](./Abilities_and_Spells.md#context-applymultipletimes) | Block | A loop block that executes its nested logic multiple times. | 3 |
| [`CatPartsSizeScaleStatus`](./Abilities_and_Spells.md#context-catpartssizescalestatus) | Block | Visually scales specific body parts of a character. | 3 |
| [`CollideWithConsumed`](./Enums.md#enum-math_equation) | Equation | Applies or references the 'CollideWithConsumed' effect/state. | 3 |
| [`Conditional_AffectedByElement`](./Abilities_and_Spells.md#context-conditional_affectedbyelement) | Block | Conditional trigger: Executes nested logic if the target is currently afflicted by the specified element. | 3 |
| [`Conditional_FirstApplicationThisTurn`](./Abilities_and_Spells.md#context-conditional_firstapplicationthisturn) | Block | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 3 |
| [`Conditional_LastHit`](./Abilities_and_Spells.md#context-conditional_lasthit) | Block | Conditional trigger: Executes nested logic if this attack is the final hit of a multi-hit sequence. | 3 |
| `CorpseVaporizer` | Number | Applies or references the 'CorpseVaporizer' effect/state. | 3 |
| `CurrentWeaponDamageUp` | Number | Applies or references the 'CurrentWeaponDamageUp' effect/state. | 3 |
| `DamageOrHealConditionally` | Number | Applies or references the 'DamageOrHealConditionally' effect/state. | 3 |
| `DeleteObject` | Number | Applies or references the 'DeleteObject' effect/state. | 3 |
| `DestroyTrinket` | Number | Applies or references the 'DestroyTrinket' effect/state. | 3 |
| `DestroyWeapon` | Number | Applies or references the 'DestroyWeapon' effect/state. | 3 |
| `DestroyWeaponThrow` | Number | Applies or references the 'DestroyWeaponThrow' effect/state. | 3 |
| `Die` | Number | Applies or references the 'Die' effect/state. | 3 |
| `DisplaceTowardsSource` | Number | Applies or references the 'DisplaceTowardsSource' effect/state. | 3 |
| `Doomed` | Number | Applies or references the 'Doomed' effect/state. | 3 |
| [`DoubleStatus`](./Enums.md#enum-doublestatus) | Enum/String | Applies or references the 'DoubleStatus' effect/state. | 3 |
| [`DustOnHit`](./Abilities_and_Spells.md#context-dustonhit) | Block | Spawns a specific particle or cloud object upon impact. | 3 |
| `ExtraBasicAttacks_Status` | Number | Applies or references the 'ExtraBasicAttacks_Status' effect/state. | 3 |
| `ForceDisplace` | Number | Applies or references the 'ForceDisplace' effect/state. | 3 |
| `ForceMoveTowardsEnemies` | Number | Applies or references the 'ForceMoveTowardsEnemies' effect/state. | 3 |
| `InstantMaxHealthUp` | Number | Applies or references the 'InstantMaxHealthUp' effect/state. | 3 |
| `KineticSpikes` | Number | Applies or references the 'KineticSpikes' effect/state. | 3 |
| `MoveQuivered` | Number | Applies or references the 'MoveQuivered' effect/state. | 3 |
| `NextAttackBonusRange` | Number | Applies or references the 'NextAttackBonusRange' effect/state. | 3 |
| `OverrideDamage` | Number | Applies or references the 'OverrideDamage' effect/state. | 3 |
| `PermanentConstitution` | Number | Applies or references the 'PermanentConstitution' effect/state. | 3 |
| `PlayBackground` | Number | Applies or references the 'PlayBackground' effect/state. | 3 |
| `PoisonLace` | Number | Applies or references the 'PoisonLace' effect/state. | 3 |
| `PullSourceToTarget` | Number | Applies or references the 'PullSourceToTarget' effect/state. | 3 |
| `Reflect` | Number | Applies or references the 'Reflect' effect/state. | 3 |
| `RefreshWeaponAbility` | Number | Applies or references the 'RefreshWeaponAbility' effect/state. | 3 |
| `RepairAll` | Number | Applies or references the 'RepairAll' effect/state. | 3 |
| `RepairOnKill` | Number | Applies or references the 'RepairOnKill' effect/state. | 3 |
| `ReviveNextRound` | Number | Queues the character to be resurrected at the start of the next combat round. | 3 |
| [`SetCrazyEyeBackgroundWeights`](./Abilities_and_Spells.md#context-setcrazyeyebackgroundweights) | Block | Adjusts visual rendering weights for the 'Crazy Eye' background effect. | 3 |
| [`SpawnCustomTrap`](./Enums.md#enum-spawncustomtrap) | Enum/String | Applies or references the 'SpawnCustomTrap' effect/state. | 3 |
| `SpawnNeutralWebTrapOnMiss` | Number | Applies or references the 'SpawnNeutralWebTrapOnMiss' effect/state. | 3 |
| `SpellDamageUp` | Number | Applies or references the 'SpellDamageUp' effect/state. | 3 |
| `Tangled` | Number | Applies a tangled/ensnared status effect, often modifying visual sprites. | 3 |
| `TempSpeedUp` | Number | Applies or references the 'TempSpeedUp' effect/state. | 3 |
| [`TempStrengthUp`](./Enums.md#enum-tempstrengthup) | Enum/String | Applies or references the 'TempStrengthUp' effect/state. | 3 |
| `VaporizeTarget` | Number | Applies or references the 'VaporizeTarget' effect/state. | 3 |
| `AddSpiritBombCharges` | Number | Applies or references the 'AddSpiritBombCharges' effect/state. | 2 |
| [`BodyGuard`](./Abilities_and_Spells.md#context-bodyguard) | Block | Protects an ally by intercepting attacks directed at them. | 2 |
| `BonusKnockbackDamage` | Number | Applies or references the 'BonusKnockbackDamage' effect/state. | 2 |
| `Bound` | Number | Applies or references the 'Bound' effect/state. | 2 |
| `CancelPrimedAbilities` | Number | Applies or references the 'CancelPrimedAbilities' effect/state. | 2 |
| [`ChangeFaction`](./Enums.md#enum-changefaction) | Enum/String | Applies or references the 'ChangeFaction' effect/state. | 2 |
| `CharmedForceAttack` | Number | Applies or references the 'CharmedForceAttack' effect/state. | 2 |
| `CollideWithThrowTarget` | Number | Applies or references the 'CollideWithThrowTarget' effect/state. | 2 |
| [`Conditional_BadRoll`](./Abilities_and_Spells.md#context-conditional_badroll) | Block | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. | 2 |
| [`Conditional_BossOrBig`](./Abilities_and_Spells.md#context-conditional_bossorbig) | Block | Conditional trigger: Executes nested logic if the target is a Boss or has a large size classification. | 2 |
| [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy) | Block | Conditional trigger: Executes nested logic if the target is the caster's summoned buddy/familiar. | 2 |
| [`Conditional_DestructibleCorpse`](./Abilities_and_Spells.md#context-conditional_destructiblecorpse) | Block | Conditional trigger: Executes nested logic if the target is a corpse that can be destroyed or vaporized. | 2 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#context-conditional_healththreshold) | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 2 |
| [`Conditional_IsSelf`](./Abilities_and_Spells.md#context-conditional_isself) | Block | Conditional trigger: Executes nested logic if the target is the caster themselves. | 2 |
| [`Conditional_NotAlly`](./Abilities_and_Spells.md#context-conditional_notally) | Block | Conditional trigger: Executes nested logic if the target is NOT friendly to the caster. | 2 |
| [`Conditional_NotBossOrBig`](./Abilities_and_Spells.md#context-conditional_notbossorbig) | Block | Conditional trigger: Executes nested logic if the target is NEITHER a Boss nor large. | 2 |
| [`Conditional_NotShielded`](./Abilities_and_Spells.md#context-conditional_notshielded) | Block | Conditional trigger: Executes nested logic if the target does NOT currently have a Shield status. | 2 |
| [`Conditional_OncePerBattle`](./Abilities_and_Spells.md#context-conditional_onceperbattle) | Block | Conditional trigger: Executes nested logic only once per encounter/battle. | 2 |
| [`Conditional_Shielded`](./Abilities_and_Spells.md#context-conditional_shielded) | Block | Conditional trigger: Executes nested logic if the target currently has a Shield status. | 2 |
| `CopySpells` | Number | Duplicates existing spells currently in the character's hand. | 2 |
| `Counterspell` | Number | Applies or references the 'Counterspell' effect/state. | 2 |
| `CritChanceUp` | Number | Applies or references the 'CritChanceUp' effect/state. | 2 |
| `DamageBasedOnMissingHealth` | Number | Applies or references the 'DamageBasedOnMissingHealth' effect/state. | 2 |
| `DamageDistanceAOEFalloff` | Number | Applies or references the 'DamageDistanceAOEFalloff' effect/state. | 2 |
| `DamageTrinket` | Number | Applies or references the 'DamageTrinket' effect/state. | 2 |
| `DelayedFury` | Number | Applies or references the 'DelayedFury' effect/state. | 2 |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#context-destroyequipmentandattachparasite) | Block | Removes an equipped item and replaces it with a parasite from a specified pool. | 2 |
| `DieViaAbilityInternally` | Number | Applies or references the 'DieViaAbilityInternally' effect/state. | 2 |
| `DiminishingHealthRegen` | Number | Applies or references the 'DiminishingHealthRegen' effect/state. | 2 |
| `DisplaceToOriginalPosition` | Number | Applies or references the 'DisplaceToOriginalPosition' effect/state. | 2 |
| `DoubleCastSpell` | Number | Applies or references the 'DoubleCastSpell' effect/state. | 2 |
| `DoubleLoot` | Number | Applies or references the 'DoubleLoot' effect/state. | 2 |
| `FlowersOnHit` | Number | Applies or references the 'FlowersOnHit' effect/state. | 2 |
| `ForceMoveNonAlliesInRangeTowardsTile` | Number | Applies or references the 'ForceMoveNonAlliesInRangeTowardsTile' effect/state. | 2 |
| [`ForceMoveTowardsTaggedObject`](./Abilities_and_Spells.md#context-forcemovetowardstaggedobject) | Block | Forces the character to move towards the nearest object with a specific tag. | 2 |
| `FreeSpell` | Number | Applies or references the 'FreeSpell' effect/state. | 2 |
| `Hex` | Number | Applies or references the 'Hex' effect/state. | 2 |
| `IgnoreDamage` | Number | Applies or references the 'IgnoreDamage' effect/state. | 2 |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum/String | Applies or references the 'ImmediateUseAbility' effect/state. | 2 |
| [`ImmediateUseDirectionalAbility`](./Enums.md#enum-immediateusedirectionalability) | Enum/String | Applies or references the 'ImmediateUseDirectionalAbility' effect/state. | 2 |
| `JohnnyCriesForWashers` | Number | Applies or references the 'JohnnyCriesForWashers' effect/state. | 2 |
| `KnockOutCoin` | Number | Forces the target to drop coins. | 2 |
| `Knockback` | Number | Applies or references the 'Knockback' effect/state. | 2 |
| `LeaveBehindRockOnKnockback` | Number | Applies or references the 'LeaveBehindRockOnKnockback' effect/state. | 2 |
| `Lifesteal` | Number | Applies or references the 'Lifesteal' effect/state. | 2 |
| `ManaLeeches` | Number | Applies or references the 'ManaLeeches' effect/state. | 2 |
| [`Math`](./Abilities_and_Spells.md#context-math) | Block | Triggers the Tinkerer's Math ability sequence. | 2 |
| `MaxHPUp` | Number | Applies or references the 'MaxHPUp' effect/state. | 2 |
| `NextAttackSpecialCrit` | Number | Modifies the character's next attack to have special critical properties. | 2 |
| `Ostracized` | Number | Applies or references the 'Ostracized' effect/state. | 2 |
| [`OverHealToStatuses`](./Abilities_and_Spells.md#context-overhealtostatuses) | Block | Converts excessive healing beyond maximum health into specific status effects. | 2 |
| `PartialCleanse` | Number | Applies or references the 'PartialCleanse' effect/state. | 2 |
| `PermanentStrength` | Number | Applies or references the 'PermanentStrength' effect/state. | 2 |
| `PermanentUpgradeRandomActive` | Number | Applies or references the 'PermanentUpgradeRandomActive' effect/state. | 2 |
| `Possessed` | Number | Applies or references the 'Possessed' effect/state. | 2 |
| `PullSourceToKnockbackImmuneTarget` | Number | Applies or references the 'PullSourceToKnockbackImmuneTarget' effect/state. | 2 |
| [`QuakeAreaChance`](./Abilities_and_Spells.md#context-quakeareachance) | Block | Provides a probability to trigger an earthquake Area of Effect. | 2 |
| `RandomDistanceDisplace` | Number | Displaces the target by a randomized distance. | 2 |
| [`RandomKnockback`](./Abilities_and_Spells.md#context-randomknockback) | Block | Applies a randomized amount of knockback force. | 2 |
| `RangeUp` | Number | Applies or references the 'RangeUp' effect/state. | 2 |
| `RebukeDamage` | Number | Applies or references the 'RebukeDamage' effect/state. | 2 |
| `RemoveMovePoints` | Number | Applies or references the 'RemoveMovePoints' effect/state. | 2 |
| `RepairArmorCondition` | Number | Applies or references the 'RepairArmorCondition' effect/state. | 2 |
| `RepairWeapon` | Number | Applies or references the 'RepairWeapon' effect/state. | 2 |
| `RepairWeaponCondition` | Number | Applies or references the 'RepairWeaponCondition' effect/state. | 2 |
| `ResetArmorShield` | Number | Applies or references the 'ResetArmorShield' effect/state. | 2 |
| `ScrambleEverything` | Number | Applies or references the 'ScrambleEverything' effect/state. | 2 |
| `SelfStun` | Number | Applies or references the 'SelfStun' effect/state. | 2 |
| `SetShield` | Number | Applies or references the 'SetShield' effect/state. | 2 |
| `Shatter` | Number | Applies or references the 'Shatter' effect/state. | 2 |
| `SignalFinalBossShieldBroke` | Number | Applies or references the 'SignalFinalBossShieldBroke' effect/state. | 2 |
| [`SizeScale`](./Enums.md#enum-sizescale) | Enum/String | Applies or references the 'SizeScale' effect/state. | 2 |
| `SmartMetronome` | Number | Executes a 'smart' random ability that aims to be beneficial based on context. | 2 |
| `SpawnCoinAnywhere` | Number | Applies or references the 'SpawnCoinAnywhere' effect/state. | 2 |
| [`SpawnFlames`](./Arrays.md#array-spawnflames) | Array | Applies or references the 'SpawnFlames' effect/state. | 2 |
| `SpeculativeMoveSelfCorpseOffMap` | Number | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 2 |
| `StanceSwitchToMelee` | Number | Applies or references the 'StanceSwitchToMelee' effect/state. | 2 |
| `SwallowSmallCharacter` | Number | Applies or references the 'SwallowSmallCharacter' effect/state. | 2 |
| [`TakeBonusTurnWithAIControl`](./Abilities_and_Spells.md#context-takebonusturnwithaicontrol) | Block | Grants the character an immediate extra turn, but forces the AI to control them during it. | 2 |
| `TempCritChanceUp` | Number | Applies or references the 'TempCritChanceUp' effect/state. | 2 |
| [`TempDexterityUp`](./Enums.md#enum-tempdexterityup) | Enum/String | Applies or references the 'TempDexterityUp' effect/state. | 2 |
| `TempInitiativeChange` | Number | Applies or references the 'TempInitiativeChange' effect/state. | 2 |
| [`TempMovement`](./Enums.md#enum-tempmovement) | Enum/String | Applies or references the 'TempMovement' effect/state. | 2 |
| `TempSpellDamageUp` | Number | Applies or references the 'TempSpellDamageUp' effect/state. | 2 |
| `TempTrampleUntilSettled` | Number | Applies or references the 'TempTrampleUntilSettled' effect/state. | 2 |
| `TradeLife` | Number | Applies or references the 'TradeLife' effect/state. | 2 |
| [`TrailBlazer`](./Enums.md#enum-trailblazer) | Enum/String | Applies or references the 'TrailBlazer' effect/state. | 2 |
| `Trample` | Number | Applies or references the 'Trample' effect/state. | 2 |
| `TriggerDOTStatuses` | Number | Applies or references the 'TriggerDOTStatuses' effect/state. | 2 |
| `AIFavorLowHealth` | Number | Applies or references the 'AIFavorLowHealth' effect/state. | 1 |
| `AlliesTakeExtraTurn` | Number | Applies or references the 'AlliesTakeExtraTurn' effect/state. | 1 |
| [`AlternateIdleAnimation`](./Enums.md#enum-alternateidleanimation) | Enum/String | Applies or references the 'AlternateIdleAnimation' effect/state. | 1 |
| `ApplyShieldToApplierBasedOnMaxHealth` | Number | Applies or references the 'ApplyShieldToApplierBasedOnMaxHealth' effect/state. | 1 |
| [`ApplyStatusesNextTurnBegin`](./Abilities_and_Spells.md#context-applystatusesnextturnbegin) | Block | Delays the application of the nested status effects until the start of the target's next turn. | 1 |
| [`ApplyToOthersWithSharedTagAndFaction`](./Abilities_and_Spells.md#context-applytootherswithsharedtagandfaction) | Block | Redirects the nested effects to apply to all other entities on the map that share the target's faction and specified tags. | 1 |
| [`ApplyToRandomClosestAlly`](./Abilities_and_Spells.md#context-applytorandomclosestally) | Block | Redirects the nested effects to apply to the nearest friendly unit. If tied, chooses randomly among them. | 1 |
| `Attraction` | Number | Applies or references the 'Attraction' effect/state. | 1 |
| `Bloodzerked` | Number | Applies or references the 'Bloodzerked' effect/state. | 1 |
| `BombRatTurtle` | Number | Applies or references the 'BombRatTurtle' effect/state. | 1 |
| `BonusDamageBasedOnMana` | Number | Applies or references the 'BonusDamageBasedOnMana' effect/state. | 1 |
| `BypassRockKnockback` | Number | Applies or references the 'BypassRockKnockback' effect/state. | 1 |
| `CanceledQueuedInput` | Number | Applies or references the 'CanceledQueuedInput' effect/state. | 1 |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 1 |
| `ChampionUpgradeNextMinion` | Number | Applies or references the 'ChampionUpgradeNextMinion' effect/state. | 1 |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum/String | Applies or references the 'ChangeTilesUnder' effect/state. | 1 |
| `ChaosBossFlipMidTeleport` | Number | Applies or references the 'ChaosBossFlipMidTeleport' effect/state. | 1 |
| `ChaosBossFormChange` | Number | Applies or references the 'ChaosBossFormChange' effect/state. | 1 |
| `ChargeFists` | Number | Applies or references the 'ChargeFists' effect/state. | 1 |
| `CharmedFacingForceAttack` | Number | Applies or references the 'CharmedFacingForceAttack' effect/state. | 1 |
| `ClearFinalBossBattlefield` | Number | Applies or references the 'ClearFinalBossBattlefield' effect/state. | 1 |
| `CloneWeaponTemp` | Number | Applies or references the 'CloneWeaponTemp' effect/state. | 1 |
| [`CoinTossBounce`](./Enums.md#enum-cointossbounce) | Enum/String | Applies or references the 'CoinTossBounce' effect/state. | 1 |
| `Conditional_AbilityTargetIsSelf` | Block | Conditional constraint. Nested properties only trigger if this is true. | 1 |
| [`Conditional_ActiveWeather_Any`](./Abilities_and_Spells.md#context-conditional_activeweather_any) | Block | Conditional trigger: Executes nested logic if the current map weather matches any in the list. | 1 |
| [`Conditional_Backstab`](./Abilities_and_Spells.md#context-conditional_backstab) | Block | Conditional trigger: Executes nested logic if the attacker is positioned behind the target. | 1 |
| [`Conditional_CanBeHealed`](./Abilities_and_Spells.md#context-conditional_canbehealed) | Block | Conditional trigger: Executes nested logic if the target's health is below maximum and they are capable of receiving healing. | 1 |
| [`Conditional_DebuffRoll`](./Abilities_and_Spells.md#context-conditional_debuffroll) | Block | Conditional trigger: Executes nested logic based on a randomized debuff probability. | 1 |
| [`Conditional_Displaceable`](./Abilities_and_Spells.md#context-conditional_displaceable) | Block | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 1 |
| [`Conditional_HasCleansableDebuffs`](./Abilities_and_Spells.md#context-conditional_hascleansabledebuffs) | Block | Conditional trigger: Executes nested logic if the target currently has negative status effects that can be cleansed. | 1 |
| [`Conditional_IsTrample`](./Abilities_and_Spells.md#context-conditional_istrample) | Block | Conditional trigger: Executes nested logic if the current movement/attack is classified as a trample. | 1 |
| [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#context-conditional_livingplayercat) | Block | Conditional trigger: Executes nested logic if the target is an alive player-controlled cat. | 1 |
| [`Conditional_NotBig`](./Abilities_and_Spells.md#context-conditional_notbig) | Block | Conditional trigger: Executes nested logic if the target is NOT classified as large. | 1 |
| [`Conditional_RandomChance`](./Abilities_and_Spells.md#context-conditional_randomchance) | Block | Conditional trigger: Executes nested logic based on a flat percentage random roll. | 1 |
| [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#context-conditional_sourceabilityhastag) | Block | Conditional trigger: Executes nested logic if the ability that triggered this effect has the specified tag. | 1 |
| [`Conditional_SourceHasStatus`](./Abilities_and_Spells.md#context-conditional_sourcehasstatus) | Block | Conditional trigger: Executes nested logic if the caster currently has the specified status. | 1 |
| [`ConjureSingleUseBonusAbility`](./Enums.md#enum-conjuresingleusebonusability) | Enum/String | Applies or references the 'ConjureSingleUseBonusAbility' effect/state. | 1 |
| [`CreateGlobalModifiers`](./Abilities_and_Spells.md#context-createglobalmodifiers) | Block | Generates global map or encounter rules/modifiers. | 1 |
| `CurrentWeaponAddElectricElement` | Number | Applies or references the 'CurrentWeaponAddElectricElement' effect/state. | 1 |
| `DamageWeapon` | Number | Applies or references the 'DamageWeapon' effect/state. | 1 |
| [`DeathwormUnderground`](./Enums.md#enum-deathwormunderground) | Enum/String | Applies or references the 'DeathwormUnderground' effect/state. | 1 |
| `DecoySwapper` | Number | Applies or references the 'DecoySwapper' effect/state. | 1 |
| [`DelayCastAbility`](./Abilities_and_Spells.md#context-delaycastability) | Block | Queues an ability to be cast automatically after a certain delay or trigger. | 1 |
| [`DelayedWindCone`](./Abilities_and_Spells.md#context-delayedwindcone) | Block | Creates a delayed Area of Effect cone. | 1 |
| `DeleteTraps` | Number | Applies or references the 'DeleteTraps' effect/state. | 1 |
| `DestroyNeckArmor` | Number | Applies or references the 'DestroyNeckArmor' effect/state. | 1 |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. | 1 |
| [`DinoLegAnimation`](./Enums.md#enum-dinoleganimation) | Enum/String | Applies or references the 'DinoLegAnimation' effect/state. | 1 |
| `Disguised` | Number | Applies or references the 'Disguised' effect/state. | 1 |
| `DissolveRandomArmorPiece` | Number | Applies or references the 'DissolveRandomArmorPiece' effect/state. | 1 |
| `DontHealEnemies` | Number | Applies or references the 'DontHealEnemies' effect/state. | 1 |
| `DoubleCast` | Number | Applies or references the 'DoubleCast' effect/state. | 1 |
| `DoubleCastSpellsEachTurn_Status` | Number | Applies or references the 'DoubleCastSpellsEachTurn_Status' effect/state. | 1 |
| `DrainAllyCatsForFleshGolem` | Number | Applies or references the 'DrainAllyCatsForFleshGolem' effect/state. | 1 |
| `DrinkWater` | Number | Applies or references the 'DrinkWater' effect/state. | 1 |
| `DuplicateRandomEquippedItem` | Number | Applies or references the 'DuplicateRandomEquippedItem' effect/state. | 1 |
| `EliteUpgradeNextMinion` | Number | Applies or references the 'EliteUpgradeNextMinion' effect/state. | 1 |
| `EmptyMind` | Number | Applies or references the 'EmptyMind' effect/state. | 1 |
| `Enlarge` | Number | Applies or references the 'Enlarge' effect/state. | 1 |
| [`EnterMount`](./Enums.md#enum-entermount) | Enum/String | Applies or references the 'EnterMount' effect/state. | 1 |
| `ExistUntilIdleUpkeep` | Number | Applies or references the 'ExistUntilIdleUpkeep' effect/state. | 1 |
| `ExplodeCharacter` | Number | Applies or references the 'ExplodeCharacter' effect/state. | 1 |
| `ExplodeCharacter_DeathBloom` | Number | Applies or references the 'ExplodeCharacter_DeathBloom' effect/state. | 1 |
| `ExplodeCharacter_DeathBloom2` | Number | Applies or references the 'ExplodeCharacter_DeathBloom2' effect/state. | 1 |
| `ExplodeCharacter_NoDie` | Number | Applies or references the 'ExplodeCharacter_NoDie' effect/state. | 1 |
| `ExtraBasicMoves_Status` | Number | Applies or references the 'ExtraBasicMoves_Status' effect/state. | 1 |
| `FactionConversion` | Number | Applies or references the 'FactionConversion' effect/state. | 1 |
| `FactionDisguiseSource` | Number | Applies or references the 'FactionDisguiseSource' effect/state. | 1 |
| `FastKnockback` | Number | Applies or references the 'FastKnockback' effect/state. | 1 |
| `FinalBossQueueBeam` | Number | Applies or references the 'FinalBossQueueBeam' effect/state. | 1 |
| `FireArmor` | Number | Applies or references the 'FireArmor' effect/state. | 1 |
| `FireArmor2` | Number | Applies or references the 'FireArmor2' effect/state. | 1 |
| `FlatAIBonus` | Number | Applies or references the 'FlatAIBonus' effect/state. | 1 |
| `ForceCollectsPickups` | Number | Applies or references the 'ForceCollectsPickups' effect/state. | 1 |
| `ForceMoveAndAttack` | Number | Applies or references the 'ForceMoveAndAttack' effect/state. | 1 |
| `ForceTransferWeapon` | Number | Applies or references the 'ForceTransferWeapon' effect/state. | 1 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Applies or references the 'ForceUseAbility' effect/state. | 1 |
| [`GainCoinsRange`](./Abilities_and_Spells.md#context-gaincoinsrange) | Block | Grants the player a randomized amount of coins within a min/max range. | 1 |
| `GenericBuff` | Number | Applies or references the 'GenericBuff' effect/state. | 1 |
| `GiveBoundItemToTarget` | Number | Applies or references the 'GiveBoundItemToTarget' effect/state. | 1 |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum/String | Applies or references the 'GlobalSpawnCharacter' effect/state. | 1 |
| `HealPercentMaxHP` | Number | Applies or references the 'HealPercentMaxHP' effect/state. | 1 |
| `HealRandomInjury` | Number | Applies or references the 'HealRandomInjury' effect/state. | 1 |
| `HealTo` | Number | Applies or references the 'HealTo' effect/state. | 1 |
| `HeavyHits` | Number | Applies or references the 'HeavyHits' effect/state. | 1 |
| `IceArmor` | Number | Applies or references the 'IceArmor' effect/state. | 1 |
| `IgnoreDebuffs` | Number | Applies or references the 'IgnoreDebuffs' effect/state. | 1 |
| [`IncAuxCounterCycle`](./Abilities_and_Spells.md#context-incauxcountercycle) | Block | Increments a generic auxiliary counter, looping back to 0 when it exceeds the maximum. | 1 |
| `IncreaseCumulativeBlastDamage` | Number | Applies or references the 'IncreaseCumulativeBlastDamage' effect/state. | 1 |
| `IncreaseItemAuxOnKill` | Number | Applies or references the 'IncreaseItemAuxOnKill' effect/state. | 1 |
| `Infested` | Number | Applies or references the 'Infested' effect/state. | 1 |
| `InterchangeMoveActPoints` | Number | Applies or references the 'InterchangeMoveActPoints' effect/state. | 1 |
| `Invulnerable` | Number | Applies or references the 'Invulnerable' effect/state. | 1 |
| `MadnessChanceOnTurnBegin` | Number | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. | 1 |
| `MakeWeaponUnbreakable` | Number | Applies or references the 'MakeWeaponUnbreakable' effect/state. | 1 |
| `ManaStealToHealth` | Number | Applies or references the 'ManaStealToHealth' effect/state. | 1 |
| `ManglerAttack` | Number | Applies or references the 'ManglerAttack' effect/state. | 1 |
| `ManglerShuffle` | Boolean | Applies or references the 'ManglerShuffle' effect/state. | 1 |
| `MassAttackThis` | Number | Applies or references the 'MassAttackThis' effect/state. | 1 |
| `Meaty` | Number | Applies or references the 'Meaty' effect/state. | 1 |
| `MimicMetronome` | Number | Applies or references the 'MimicMetronome' effect/state. | 1 |
| `MotherTumorDebugForcePass` | Number | Applies or references the 'MotherTumorDebugForcePass' effect/state. | 1 |
| `Muted` | Number | Applies or references the 'Muted' effect/state. | 1 |
| `NextAbilityHeals` | Number | Applies or references the 'NextAbilityHeals' effect/state. | 1 |
| `NextActionLuckUp` | Number | Applies or references the 'NextActionLuckUp' effect/state. | 1 |
| [`NextBasicAttackCritsThisTurn`](./Abilities_and_Spells.md#context-nextbasicattackcritsthisturn) | Block | Guarantees the next basic attack executed this turn will be a critical hit. | 1 |
| [`NextBattleStatusStacks`](./Abilities_and_Spells.md#context-nextbattlestatusstacks) | Block | Carries over the specified status effects into the next encounter/battle. | 1 |
| `NextDamageReduceAndHealAllies` | Number | Applies or references the 'NextDamageReduceAndHealAllies' effect/state. | 1 |
| `NextTurnDoubleRangedDamage` | Number | Applies or references the 'NextTurnDoubleRangedDamage' effect/state. | 1 |
| `NonStackingDivineShield` | Number | Applies or references the 'NonStackingDivineShield' effect/state. | 1 |
| [`ObjectOnHitFullyEmpty`](./Enums.md#enum-objectonhitfullyempty) | Enum/String | Applies or references the 'ObjectOnHitFullyEmpty' effect/state. | 1 |
| `OverHealToShield` | Number | Applies or references the 'OverHealToShield' effect/state. | 1 |
| [`OverrideChainKnockbackDamage`](./Enums.md#enum-math_equation) | Equation | Applies or references the 'OverrideChainKnockbackDamage' effect/state. | 1 |
| `PermanentCharisma` | Number | Applies or references the 'PermanentCharisma' effect/state. | 1 |
| `PermanentDexterity` | Number | Applies or references the 'PermanentDexterity' effect/state. | 1 |
| `PermanentImmobile` | Number | Applies or references the 'PermanentImmobile' effect/state. | 1 |
| `PermanentIntelligence` | Number | Applies or references the 'PermanentIntelligence' effect/state. | 1 |
| `PermanentLuck` | Number | Applies or references the 'PermanentLuck' effect/state. | 1 |
| `PermanentSpeed` | Number | Applies or references the 'PermanentSpeed' effect/state. | 1 |
| `PermanentUpgradeRandomActiveOrPassive` | Number | Applies or references the 'PermanentUpgradeRandomActiveOrPassive' effect/state. | 1 |
| [`PoolMetronome`](./Abilities_and_Spells.md#context-poolmetronome) | Block | Executes a random ability drawn from a specific pool. | 1 |
| `ProbeCharmed` | Number | Applies or references the 'ProbeCharmed' effect/state. | 1 |
| [`QueueUseAbility`](./Enums.md#enum-queueuseability) | Enum/String | Applies or references the 'QueueUseAbility' effect/state. | 1 |
| `RNGCannonRandomDamage` | Number | Applies or references the 'RNGCannonRandomDamage' effect/state. | 1 |
| `RandomKnockbackDirection` | Number | Applies or references the 'RandomKnockbackDirection' effect/state. | 1 |
| `RandomPermanentStat` | Number | Applies or references the 'RandomPermanentStat' effect/state. | 1 |
| `ReduceManaCost` | Number | Applies or references the 'ReduceManaCost' effect/state. | 1 |
| `ReduceManaCostExcludeBrainstorm` | Number | Applies or references the 'ReduceManaCostExcludeBrainstorm' effect/state. | 1 |
| `ReformMoonHead` | Number | Applies or references the 'ReformMoonHead' effect/state. | 1 |
| `RefreshItemAbilities` | Number | Applies or references the 'RefreshItemAbilities' effect/state. | 1 |
| `RefreshNonManaItemAbilities` | Number | Applies or references the 'RefreshNonManaItemAbilities' effect/state. | 1 |
| `RefreshOncePerFightAbilities` | Number | Applies or references the 'RefreshOncePerFightAbilities' effect/state. | 1 |
| `Regurge` | Number | Applies or references the 'Regurge' effect/state. | 1 |
| [`RemoveStatusStacks`](./Abilities_and_Spells.md#context-removestatusstacks) | Block | Removes a specific number of stacks of a status effect. | 1 |
| `RepairAllCondition` | Number | Applies or references the 'RepairAllCondition' effect/state. | 1 |
| `RerollEnemy` | Number | Applies or references the 'RerollEnemy' effect/state. | 1 |
| `ReturnDinoLegs` | Number | Applies or references the 'ReturnDinoLegs' effect/state. | 1 |
| `ScatterRandomPickups` | Number | Applies or references the 'ScatterRandomPickups' effect/state. | 1 |
| [`ScrambleLastUsedSpell`](./Abilities_and_Spells.md#context-scramblelastusedspell) | Block | Randomizes or scrambles the properties of the last spell cast. | 1 |
| [`SetDefaultFace`](./Enums.md#enum-setdefaultface) | Enum/String | Applies or references the 'SetDefaultFace' effect/state. | 1 |
| `ShadowCrit` | Number | Applies or references the 'ShadowCrit' effect/state. | 1 |
| `ShootHereCommand` | Number | Applies or references the 'ShootHereCommand' effect/state. | 1 |
| `ShootHereReceiver` | Number | Applies or references the 'ShootHereReceiver' effect/state. | 1 |
| `ShortCircuit` | Number | Applies or references the 'ShortCircuit' effect/state. | 1 |
| `SmallHitExplosion` | Number | Applies or references the 'SmallHitExplosion' effect/state. | 1 |
| `SmellBlood` | Number | Applies or references the 'SmellBlood' effect/state. | 1 |
| [`SoundEventOnHit`](./Enums.md#enum-soundeventonhit) | Enum/String | Applies or references the 'SoundEventOnHit' effect/state. | 1 |
| [`SourceSwapsBackEndOfTurn`](./Enums.md#enum-sourceswapsbackendofturn) | Enum/String | Applies or references the 'SourceSwapsBackEndOfTurn' effect/state. | 1 |
| `SpawnWebTrap` | Number | Applies or references the 'SpawnWebTrap' effect/state. | 1 |
| [`SpecialBossMultipartInstakill`](./Enums.md#enum-specialbossmultipartinstakill) | Enum/String | Applies or references the 'SpecialBossMultipartInstakill' effect/state. | 1 |
| `SpellShield` | Number | Applies or references the 'SpellShield' effect/state. | 1 |
| `SpitConsumed` | Number | Applies or references the 'SpitConsumed' effect/state. | 1 |
| `SplashDamage` | Number | Applies or references the 'SplashDamage' effect/state. | 1 |
| [`SpreadDisease`](./Abilities_and_Spells.md#context-spreaddisease) | Block | Provides a chance to transmit a disease status to adjacent targets. | 1 |
| `StackingSandstorm` | Number | Applies or references the 'StackingSandstorm' effect/state. | 1 |
| `StatBounty` | Number | Applies or references the 'StatBounty' effect/state. | 1 |
| [`StatusGroup`](./Abilities_and_Spells.md#context-statusgroup) | Block | Groups multiple status effects together for batch application. | 1 |
| `StealDemonicGlyph` | Number | Applies or references the 'StealDemonicGlyph' effect/state. | 1 |
| [`StealEquipment`](./Enums.md#enum-stealequipment) | Enum/String | Applies or references the 'StealEquipment' effect/state. | 1 |
| `StealTurn` | Number | Applies or references the 'StealTurn' effect/state. | 1 |
| `StealthCritChance` | Number | Applies or references the 'StealthCritChance' effect/state. | 1 |
| `SwapHighestAndLowestStat` | Number | Applies or references the 'SwapHighestAndLowestStat' effect/state. | 1 |
| [`SwapWeapon`](./Abilities_and_Spells.md#context-swapweapon) | Block | Replaces the character's currently equipped weapon with one from a specified pool. | 1 |
| `Switcheroo` | Number | Applies or references the 'Switcheroo' effect/state. | 1 |
| `T3HitlerTriggerInitialSpawns` | Number | Applies or references the 'T3HitlerTriggerInitialSpawns' effect/state. | 1 |
| [`TagMetronome`](./Enums.md#enum-tagmetronome) | Enum/String | Applies or references the 'TagMetronome' effect/state. | 1 |
| `TakeExtraTurnEndOfRound` | Number | Applies or references the 'TakeExtraTurnEndOfRound' effect/state. | 1 |
| `TargetedMetronome` | Number | Applies or references the 'TargetedMetronome' effect/state. | 1 |
| `Taunting` | Number | Applies or references the 'Taunting' effect/state. | 1 |
| [`TeamBonusAbility`](./Enums.md#enum-teambonusability) | Enum/String | Applies or references the 'TeamBonusAbility' effect/state. | 1 |
| [`TeleportBackAtTurnEnd`](./Enums.md#enum-teleportbackatturnend) | Enum/String | Applies or references the 'TeleportBackAtTurnEnd' effect/state. | 1 |
| `TempBackstab` | Number | Applies or references the 'TempBackstab' effect/state. | 1 |
| `TempBackstabBleed` | Number | Applies or references the 'TempBackstabBleed' effect/state. | 1 |
| `TempBackstabPiercing` | Number | Applies or references the 'TempBackstabPiercing' effect/state. | 1 |
| `TempBackstabPoison` | Number | Applies or references the 'TempBackstabPoison' effect/state. | 1 |
| `TempBasicAttackBonusAOE` | Number | Applies or references the 'TempBasicAttackBonusAOE' effect/state. | 1 |
| `TempBonusKnockback` | Number | Applies or references the 'TempBonusKnockback' effect/state. | 1 |
| `TempBonusKnockbackDamage` | Number | Applies or references the 'TempBonusKnockbackDamage' effect/state. | 1 |
| `TempCounterAttack` | Number | Applies or references the 'TempCounterAttack' effect/state. | 1 |
| `TempInjuryImmunity` | Number | Applies or references the 'TempInjuryImmunity' effect/state. | 1 |
| `TempLuckUp` | Number | Applies or references the 'TempLuckUp' effect/state. | 1 |
| `TempManaCostReduction` | Number | Applies or references the 'TempManaCostReduction' effect/state. | 1 |
| `TempPenetrate` | Number | Applies or references the 'TempPenetrate' effect/state. | 1 |
| `TempPreEmptiveCounterAttack` | Number | Applies or references the 'TempPreEmptiveCounterAttack' effect/state. | 1 |
| `ThornsDamageImmuneUntilSettled` | Number | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. | 1 |
| [`TickDownStatus`](./Enums.md#enum-tickdownstatus) | Enum/String | Applies or references the 'TickDownStatus' effect/state. | 1 |
| `TileDamageImmuneUntilSettled` | Number | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. | 1 |
| `TilesMovedToCritChance` | Number | Applies or references the 'TilesMovedToCritChance' effect/state. | 1 |
| `TilesMovedToMana` | Number | Applies or references the 'TilesMovedToMana' effect/state. | 1 |
| [`TilesMovedToNeighborHeal`](./Enums.md#enum-tilesmovedtoneighborheal) | Enum/String | Applies or references the 'TilesMovedToNeighborHeal' effect/state. | 1 |
| `TilesMovedToStrength` | Number | Applies or references the 'TilesMovedToStrength' effect/state. | 1 |
| `TowerDefenseStatus` | Number | Applies or references the 'TowerDefenseStatus' effect/state. | 1 |
| `TowerDefenseStatus2` | Number | Applies or references the 'TowerDefenseStatus2' effect/state. | 1 |
| [`TransformBasicMove`](./Enums.md#enum-transformbasicmove) | Enum/String | Applies or references the 'TransformBasicMove' effect/state. | 1 |
| [`TransformEquipment`](./Abilities_and_Spells.md#context-transformequipment) | Block | Upgrades or transforms a specific equipped item into another. | 1 |
| [`TransformNow`](./Enums.md#enum-transformnow) | Enum/String | Applies or references the 'TransformNow' effect/state. | 1 |
| `Trapper_Status` | Number | Applies or references the 'Trapper_Status' effect/state. | 1 |
| `TriggerGameEnding` | Number | Applies or references the 'TriggerGameEnding' effect/state. | 1 |
| `TriggerMotherConsume` | Number | Applies or references the 'TriggerMotherConsume' effect/state. | 1 |
| `TriggerMotherGrow` | Number | Applies or references the 'TriggerMotherGrow' effect/state. | 1 |
| `TurnAround` | Number | Applies or references the 'TurnAround' effect/state. | 1 |
| [`TurnControlDelay`](./Enums.md#enum-turncontroldelay) | Enum/String | Applies or references the 'TurnControlDelay' effect/state. | 1 |
| `TurnRight` | Number | Applies or references the 'TurnRight' effect/state. | 1 |
| `UndoDamage` | Number | Applies or references the 'UndoDamage' effect/state. | 1 |
| [`UseMoveAbilityWithAI`](./Abilities_and_Spells.md#context-usemoveabilitywithai) | Block | Forces the character to execute a movement ability using specific AI weights. | 1 |
| [`VaporizeCorpseFlipAdvantage`](./Arrays.md#array-vaporizecorpseflipadvantage) | Array | Applies or references the 'VaporizeCorpseFlipAdvantage' effect/state. | 1 |
| `VaporizeDice` | Number | Applies or references the 'VaporizeDice' effect/state. | 1 |
| [`VisualCountDownThenApplyStatus`](./Abilities_and_Spells.md#context-visualcountdownthenapplystatus) | Block | Displays a visual countdown above the target before applying the nested effects. | 1 |
| [`WaggleClone`](./Abilities_and_Spells.md#context-waggleclone) | Block | Spawns visual clones or alternative hitbox variants of the projectile. | 1 |

</details>

---

### Context: `FormChange`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool)

| Property Key | Type | Definition | Count (X/75) |
| :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum/String |  | 75 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/41) |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum/String | The specific string tag to check for. | 41 |
| [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss) | Block | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 6 |
| `FloatingRockTrap` | Number | Applies or references the 'FloatingRockTrap' effect/state. | 6 |
| [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss) | Block | Conditional trigger: Executes nested logic if the target is a Boss. | 4 |
| `IgnoreDamage` | Number | Applies or references the 'IgnoreDamage' effect/state. | 4 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum/String | Applies or references the 'ImmediateUseAbility' effect/state. | 3 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill) | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 2 |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate) | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 2 |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum/String | Applies or references the 'ChangeTilesUnder' effect/state. | 2 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 2 |
| `Die` | Number | Applies or references the 'Die' effect/state. | 2 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 2 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 2 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 1 |
| [`Conditional_InForm`](./Abilities_and_Spells.md#context-conditional_inform) | Block | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 1 |
| `CrackMoonHead` | Number | Applies or references the 'CrackMoonHead' effect/state. | 1 |
| `DeleteObject` | Number | Applies or references the 'DeleteObject' effect/state. | 1 |
| `DisplaceTowardsSource` | Number | Applies or references the 'DisplaceTowardsSource' effect/state. | 1 |
| `EventBounty` | Number | Applies or references the 'EventBounty' effect/state. | 1 |
| `FaceAway` | Number | Applies or references the 'FaceAway' effect/state. | 1 |
| `Instakill` | Number | Applies or references the 'Instakill' effect/state. | 1 |
| [`MergeDamageInstance`](./Abilities_and_Spells.md#context-mergedamageinstance) | Block | Combines damage numbers or visual hit effects. | 1 |
| `OverrideDamage` | Number | Applies or references the 'OverrideDamage' effect/state. | 1 |
| [`PopAndSpawn`](./Abilities_and_Spells.md#context-popandspawn) | Block | Destroys the target and replaces it with a new spawned entity. | 1 |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 1 |
| `ScatterRandomPickups` | Number | Applies or references the 'ScatterRandomPickups' effect/state. | 1 |
| [`SetAnimationAlts`](./Abilities_and_Spells.md#context-setanimationalts) | Block | Overrides specific animation states with alternative animations. | 1 |
| `SetKnockback` | Number | Applies or references the 'SetKnockback' effect/state. | 1 |
| [`UseAbility`](./Enums.md#enum-useability) | Enum/String | Forces the character or target to instantly use a specified ability. | 1 |
| `VaporizeCorpse` | Number | Applies or references the 'VaporizeCorpse' effect/state. | 1 |

</details>

---

### Context: `Temporary`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate), [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_NotAlly`](./Abilities_and_Spells.md#context-conditional_notally), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/41) |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 41 |
| [`status`](./Enums.md#enum-status) | Enum/String | The status effect to apply. | 40 |
| `turns` | Number | Duration in turns. | 40 |
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 19 |
| `expires_on_end_turn` | Boolean |  | 11 |
| `data` | Number |  | 2 |
| `expires_on_appliers_turn` | Boolean |  | 2 |
| `expires_on_move` | Boolean |  | 1 |

</details>

---

### Context: `sounds`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count (X/32) |
| :--- | :--- | :--- | :--- |
| [`ontrigger`](./Enums.md#enum-ontrigger) | Enum/String |  | 32 |
| [`oncast`](./Enums.md#enum-oncast) | Enum/String |  | 3 |
| [`oncastpoint`](./Enums.md#enum-oncastpoint) | Enum/String |  | 3 |
| [`ontrigger_intentional`](./Enums.md#enum-ontrigger_intentional) | Enum/String |  | 1 |

</details>

---

### Context: `splash_damage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#context-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count (X/32) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 32 |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 17 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 13 |
| `knockback` | Number | Knockback force of the splash blast. | 13 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification/category type. | 12 |
| `makes_contact` | Boolean |  | 6 |
| `override_trample_damage` | Boolean |  | 2 |
| `ai_base_score` | Number |  | 1 |
| `crit_chance` | Number |  | 1 |
| `force_no_knockback` | Boolean |  | 1 |
| `force_play_hit_animation` | Boolean |  | 1 |
| [`layer`](./Enums.md#enum-layer) | Enum/String |  | 1 |

</details>

---

### Context: `temporary_effects`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count (X/26) |
| :--- | :--- | :--- | :--- |
| `Trample` | Number | Applies or references the 'Trample' effect/state. | 26 |
| `CastAgain` | Number | Applies or references the 'CastAgain' effect/state. | 20 |
| `DisableTrample` | Number | Applies or references the 'DisableTrample' effect/state. | 10 |
| `Fury` | Number | Applies or references the 'Fury' effect/state. | 7 |
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum/String | Applies or references the 'TileTrail' effect/state. | 6 |
| `JustInCaseTrample` | Number | Applies or references the 'JustInCaseTrample' effect/state. | 5 |
| [`LeaveBehind`](./Enums.md#enum-leavebehind) | Enum/String | Spawns a specific object at the character's previous location when they move. | 5 |
| `DashFury` | Number | Applies or references the 'DashFury' effect/state. | 3 |
| [`AfterImage`](./Abilities_and_Spells.md#context-afterimage) | Block | Spawns a visual decoy or shade at the caster's previous location. | 2 |
| `BearTrapTrail` | Number | Applies or references the 'BearTrapTrail' effect/state. | 2 |
| `DelayedWindTrail` | Number | Applies or references the 'DelayedWindTrail' effect/state. | 1 |
| `DoubleLoot` | Number | Applies or references the 'DoubleLoot' effect/state. | 1 |
| [`JumpAttackLeaveBehind`](./Enums.md#enum-jumpattackleavebehind) | Enum/String | Applies or references the 'JumpAttackLeaveBehind' effect/state. | 1 |
| `KnockbackImmunity` | Number | Applies or references the 'KnockbackImmunity' effect/state. | 1 |
| [`TileTrail_Ahead`](./Enums.md#enum-tiletrail_ahead) | Enum/String | Applies or references the 'TileTrail_Ahead' effect/state. | 1 |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Conditional_LastHit`](./Abilities_and_Spells.md#context-conditional_lasthit), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/20) |
| :--- | :--- | :--- | :--- |
| `distance` | Number | The distance in tiles to knock the target away. | 20 |
| [`stacks`](./Enums.md#enum-math_equation) | Equation | Number of stacks or intensity to apply. | 18 |
| `height` | Number |  | 2 |
| `circular_variance` | Number |  | 1 |

</details>

---

### Context: `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/13) |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum/String | The specific status ID to check for. | 13 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 6 |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 2 |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 2 |
| `Slow` | Number | Applies or references the 'Slow' effect/state. | 2 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 1 |
| `Fear` | Number | Applies or references the 'Fear' effect/state. | 1 |
| [`FormChange`](./Enums.md#enum-formchange) | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 1 |
| `Quivered` | Number | Applies or references the 'Quivered' effect/state. | 1 |

</details>

---

### Context: `Consumed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#context-conditional_livingplayercat), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/13) |
| :--- | :--- | :--- | :--- |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum/String | Ability triggered by the consumed entity while inside the consumer. | 13 |
| `force_contact` | Boolean | If true, enforces physical overlap. | 11 |
| `instant` | Boolean |  | 8 |
| [`mount_mode`](./Enums.md#enum-mount_mode) | Enum/String | If true, treats the consumption as riding/mounting instead of eating. | 8 |
| `wet` | Boolean |  | 8 |
| `do_not_pop_corpse` | Boolean |  | 7 |
| [`drop_on_death`](./Enums.md#enum-drop_on_death) | Enum/String |  | 7 |
| `drop_on_self_death` | Boolean |  | 3 |
| [`extra_statuses`](./Abilities_and_Spells.md#context-extra_statuses) | Block | Additional generic status applications. | 3 |
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum/String |  | 1 |
| `kill_on_consume` | Boolean |  | 1 |
| `use_placeholder` | Boolean |  | 1 |

</details>

---

### Context: `EvolveAbilityFromPool`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/13) |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum/String |  | 13 |
| `upgraded` | Boolean |  | 13 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 12 |
| [`GainDisorderFromPool_PostCast`](./Enums.md#enum-gaindisorderfrompool_postcast) | Enum/String | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 7 |
| [`ApplyToRandomPartyMemberIfPossible`](./Abilities_and_Spells.md#context-applytorandompartymemberifpossible) | Block | Redirects the nested effects to apply to a random living member of the player's party. | 1 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`GainDisorder`](./Enums.md#enum-gaindisorder) | Enum/String | Applies or references the 'GainDisorder' effect/state. | 1 |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum/String | Applies or references the 'ImmediateUseAbility' effect/state. | 1 |
| `RefreshWeaponAbility` | Number | Applies or references the 'RefreshWeaponAbility' effect/state. | 1 |
| `ShowText` | String | Applies or references the 'ShowText' effect/state. | 1 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyMultipleTimes`](./Abilities_and_Spells.md#context-applymultipletimes), [`Conditional_CanBeHealed`](./Abilities_and_Spells.md#context-conditional_canbehealed), [`Conditional_HasCleansableDebuffs`](./Abilities_and_Spells.md#context-conditional_hascleansabledebuffs), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`FormChange`](./Abilities_and_Spells.md#context-formchange) | Block | Transforms the character into a different state or form (e.g., Rage, HasCat). | 12 |
| `GainCoins` | Number | Applies or references the 'GainCoins' effect/state. | 7 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 7 |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 6 |
| `Poison` | Number | Applies or references the 'Poison' effect/state. | 6 |
| `Slow` | Number | Applies or references the 'Slow' effect/state. | 6 |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. | 5 |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. | 5 |
| [`BonusDamage`](./Enums.md#enum-math_equation) | Equation | Applies or references the 'BonusDamage' effect/state. | 4 |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 4 |
| `ConstitutionUp` | Number | Applies or references the 'ConstitutionUp' effect/state. | 4 |
| `KineticSpikes` | Number | Applies or references the 'KineticSpikes' effect/state. | 4 |
| `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. | 4 |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 4 |
| `Brace` | Number | Applies or references the 'Brace' effect/state. | 3 |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 3 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 3 |
| [`IncAuxCounterClamped`](./Abilities_and_Spells.md#context-incauxcounterclamped) | Block | Increments a generic auxiliary counter on the character, capped by a maximum value. | 3 |
| `MoveQuivered` | Number | Applies or references the 'MoveQuivered' effect/state. | 3 |
| `Quivered` | Number | Applies or references the 'Quivered' effect/state. | 3 |
| `Weakness` | Number | Applies or references the 'Weakness' effect/state. | 3 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 2 |
| `BackflipWhenTargeted` | Number | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. | 2 |
| `BleedThorns` | Number | Applies or references the 'BleedThorns' effect/state. | 2 |
| `CharismaUp` | Number | Applies or references the 'CharismaUp' effect/state. | 2 |
| `CritChanceUp` | Number | Applies or references the 'CritChanceUp' effect/state. | 2 |
| `DexterityUp` | Number | Applies or references the 'DexterityUp' effect/state. | 2 |
| `DiminishingHealthRegen` | Number | Applies or references the 'DiminishingHealthRegen' effect/state. | 2 |
| `DodgeChance_Status` | Number | Applies or references the 'DodgeChance_Status' effect/state. | 2 |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 2 |
| `IntelligenceUp` | Number | Applies or references the 'IntelligenceUp' effect/state. | 2 |
| `Lifesteal` | Number | Applies or references the 'Lifesteal' effect/state. | 2 |
| `LuckUp` | Number | Applies or references the 'LuckUp' effect/state. | 2 |
| `Madness` | Number | Applies the Madness debuff/status effect. | 2 |
| `MagicWeakness` | Number | Applies or references the 'MagicWeakness' effect/state. | 2 |
| [`ManaGain`](./Enums.md#enum-math_equation) | Equation | Applies or references the 'ManaGain' effect/state. | 2 |
| `Marked` | Number | Applies or references the 'Marked' effect/state. | 2 |
| `PoisonLace` | Number | Applies or references the 'PoisonLace' effect/state. | 2 |
| `Reflect` | Number | Applies or references the 'Reflect' effect/state. | 2 |
| `Rot` | Number | Applies or references the 'Rot' effect/state. | 2 |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. | 2 |
| `Stun` | Number | Applies or references the 'Stun' effect/state. | 2 |
| `Tarred` | Number | Applies or references the 'Tarred' effect/state. | 2 |
| `TempCounterAttack` | Number | Applies or references the 'TempCounterAttack' effect/state. | 2 |
| `Blind` | Number | Applies or references the 'Blind' effect/state. | 1 |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 1 |
| `Charmed` | Number | Applies or references the 'Charmed' effect/state. | 1 |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 1 |
| `DelayedPain` | Number | Applies or references the 'DelayedPain' effect/state. | 1 |
| `Fear` | Number | Applies or references the 'Fear' effect/state. | 1 |
| `Freeze` | Number | Applies or references the 'Freeze' effect/state. | 1 |
| `Hex` | Number | Applies or references the 'Hex' effect/state. | 1 |
| `Immobile` | Number | Applies or references the 'Immobile' effect/state. | 1 |
| `Infested` | Number | Applies or references the 'Infested' effect/state. | 1 |
| `Ostracized` | Number | Applies or references the 'Ostracized' effect/state. | 1 |
| `Petrify` | Number | Applies or references the 'Petrify' effect/state. | 1 |
| `RandomStatDown` | Number | Applies or references the 'RandomStatDown' effect/state. | 1 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 1 |
| `RefreshMovePoints` | Number | Applies or references the 'RefreshMovePoints' effect/state. | 1 |
| `Scrambled` | Number | Applies or references the 'Scrambled' effect/state. | 1 |
| `Sleep` | Number | Applies or references the 'Sleep' effect/state. | 1 |
| `SpellDamageUp` | Number | Applies or references the 'SpellDamageUp' effect/state. | 1 |

</details>

---

### Context: `bonus_passives`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`DeadAltAbility`](./Enums.md#enum-deadaltability) | Enum/String | Applies or references the 'DeadAltAbility' effect/state. | 12 |
| `AbilityEnabledOncePerFightAtHealthThreshold` | Number | Applies or references the 'AbilityEnabledOncePerFightAtHealthThreshold' effect/state. | 7 |
| `XIsFreeArmorSlots` | Number | Applies or references the 'XIsFreeArmorSlots' effect/state. | 7 |
| `AbilityEnabledPercentEachTurn` | Number | Applies or references the 'AbilityEnabledPercentEachTurn' effect/state. | 6 |
| `FreeFirstCast` | Number | Applies or references the 'FreeFirstCast' effect/state. | 6 |
| [`XIsLivingAlliesWithTag`](./Enums.md#enum-xislivingallieswithtag) | Enum/String | Applies or references the 'XIsLivingAlliesWithTag' effect/state. | 5 |
| `CatchBoomerang` | Number | Applies or references the 'CatchBoomerang' effect/state. | 4 |
| `CopyBasicAttackEffects` | Number | Applies or references the 'CopyBasicAttackEffects' effect/state. | 4 |
| [`DownRankAIIfWeaponUsable`](./Enums.md#enum-downrankaiifweaponusable) | Enum/String | Applies or references the 'DownRankAIIfWeaponUsable' effect/state. | 4 |
| [`AbilityEnableIfConsumedCharacterHasTag`](./Enums.md#enum-abilityenableifconsumedcharacterhastag) | Enum/String | Applies or references the 'AbilityEnableIfConsumedCharacterHasTag' effect/state. | 3 |
| `AbilityEnabledOncePerRound` | Number | Applies or references the 'AbilityEnabledOncePerRound' effect/state. | 3 |
| `AbilityInheritsWeaponEffects` | Number | Applies or references the 'AbilityInheritsWeaponEffects' effect/state. | 3 |
| `MoonHeadFinisherEnabler` | Number | Applies or references the 'MoonHeadFinisherEnabler' effect/state. | 3 |
| [`XIsMultipliedPercentHealth`](./Arrays.md#array-xismultipliedpercenthealth) | Array | Applies or references the 'XIsMultipliedPercentHealth' effect/state. | 3 |
| [`AbilityEnabledIfHasStatus`](./Enums.md#enum-abilityenabledifhasstatus) | Enum/String | Applies or references the 'AbilityEnabledIfHasStatus' effect/state. | 2 |
| [`AutocastEachRound`](./Abilities_and_Spells.md#context-autocasteachround) | Block | Forces the character to automatically cast a specific ability at the start of each combat round. | 2 |
| [`ChargeSpiritBombAura`](./Enums.md#enum-chargespiritbombaura) | Enum/String | Applies or references the 'ChargeSpiritBombAura' effect/state. | 2 |
| `CopyCatPassive_Initializer` | Number | Applies or references the 'CopyCatPassive_Initializer' effect/state. | 2 |
| [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#context-nukequestfinalbossmodifications) | Block | Special encounter trigger for the Nuke Quest ending. | 2 |
| `ReloadOnKill` | Number | Applies or references the 'ReloadOnKill' effect/state. | 2 |
| `ReloadOnKillEnemy` | Number | Applies or references the 'ReloadOnKillEnemy' effect/state. | 2 |
| `ReloadOnTotalDamageReceived` | Number | Applies or references the 'ReloadOnTotalDamageReceived' effect/state. | 2 |
| [`XIsLivingCharactersWithTag`](./Enums.md#enum-xislivingcharacterswithtag) | Enum/String | Applies or references the 'XIsLivingCharactersWithTag' effect/state. | 2 |
| `XIsOtherHealsThisTurn` | Number | Applies or references the 'XIsOtherHealsThisTurn' effect/state. | 2 |
| `XIsSpellStormRampAndReset` | Number | Math variable assignment: Evaluates X based on Spell Storm stacks, then resets them. | 2 |
| `XIsTimesDamageTaken` | Number | Applies or references the 'XIsTimesDamageTaken' effect/state. | 2 |
| `AbilityDisableIfLivingCrow` | Number | Applies or references the 'AbilityDisableIfLivingCrow' effect/state. | 1 |
| `AbilityEnabledAtHealthThreshold` | Number | Applies or references the 'AbilityEnabledAtHealthThreshold' effect/state. | 1 |
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Number | Applies or references the 'AbilityEnabledIfBasicAttackUsedThisTurn' effect/state. | 1 |
| `AbilityEnabledIfMovementTrapped` | Number | Applies or references the 'AbilityEnabledIfMovementTrapped' effect/state. | 1 |
| `AbilityEnabledIfNoAggroTarget` | Number | Applies or references the 'AbilityEnabledIfNoAggroTarget' effect/state. | 1 |
| [`AbilityEnabledIfNotHasStatus`](./Enums.md#enum-abilityenabledifnothasstatus) | Enum/String | Applies or references the 'AbilityEnabledIfNotHasStatus' effect/state. | 1 |
| [`AbilityEnabledIfSpecificItemEquipped`](./Enums.md#enum-abilityenabledifspecificitemequipped) | Enum/String | Applies or references the 'AbilityEnabledIfSpecificItemEquipped' effect/state. | 1 |
| `AbsorbManaFromOtherSpells` | Number | Applies or references the 'AbsorbManaFromOtherSpells' effect/state. | 1 |
| [`AddElementsToSpells`](./Enums.md#enum-addelementstospells) | Enum/String | Applies or references the 'AddElementsToSpells' effect/state. | 1 |
| [`AddStatusToBasicAttack`](./Abilities_and_Spells.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 1 |
| `AlphaDodgeChance` | Number | Applies or references the 'AlphaDodgeChance' effect/state. | 1 |
| [`AlphaStatusOnTurnBegin`](./Abilities_and_Spells.md#context-alphastatusonturnbegin) | Block | Grants a specific status effect to the 'Alpha' (the party leader) at the start of their turn. | 1 |
| [`BonusAbility_DelayedApplication`](./Enums.md#enum-bonusability_delayedapplication) | Enum/String | Applies or references the 'BonusAbility_DelayedApplication' effect/state. | 1 |
| `CapTechSpent` | Number | Applies or references the 'CapTechSpent' effect/state. | 1 |
| `CaveWomanBirthControl` | Number | Applies or references the 'CaveWomanBirthControl' effect/state. | 1 |
| `CritChanceUp` | Number | Applies or references the 'CritChanceUp' effect/state. | 1 |
| `FistOfFateUniqueEnemyTracker` | Number | Applies or references the 'FistOfFateUniqueEnemyTracker' effect/state. | 1 |
| `FreeFirstCastAndAfterSpendMana` | Number | Applies or references the 'FreeFirstCastAndAfterSpendMana' effect/state. | 1 |
| `FreeFirstCastEachMatch` | Number | Applies or references the 'FreeFirstCastEachMatch' effect/state. | 1 |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 1 |
| `IgnoreTiles` | Number | Applies or references the 'IgnoreTiles' effect/state. | 1 |
| `IntelligenceUp` | Number | Applies or references the 'IntelligenceUp' effect/state. | 1 |
| `InterchangeDisabler` | Number | Applies or references the 'InterchangeDisabler' effect/state. | 1 |
| `KnockbackImmunity` | Number | Applies or references the 'KnockbackImmunity' effect/state. | 1 |
| [`PassiveWhileNotTakingTurn`](./Abilities_and_Spells.md#context-passivewhilenottakingturn) | Block | Grants nested passives that are only active while it is NOT the character's turn. | 1 |
| `ReloadOnAllyCatDies` | Number | Applies or references the 'ReloadOnAllyCatDies' effect/state. | 1 |
| `ReloadOnAllyDies` | Number | Applies or references the 'ReloadOnAllyDies' effect/state. | 1 |
| `ReloadOnAnyDamage` | Number | Applies or references the 'ReloadOnAnyDamage' effect/state. | 1 |
| `ReloadOnBackstab` | Number | Applies or references the 'ReloadOnBackstab' effect/state. | 1 |
| [`ReloadOnElementalDamageReceived`](./Enums.md#enum-reloadonelementaldamagereceived) | Enum/String | Applies or references the 'ReloadOnElementalDamageReceived' effect/state. | 1 |
| `ReloadOnGainCoins` | Number | Applies or references the 'ReloadOnGainCoins' effect/state. | 1 |
| `ReloadOnGainDivineShield` | Number | Applies or references the 'ReloadOnGainDivineShield' effect/state. | 1 |
| [`ReloadOnKillTagged`](./Enums.md#enum-reloadonkilltagged) | Enum/String | Applies or references the 'ReloadOnKillTagged' effect/state. | 1 |
| `ReloadOnSpendMana` | Number | Applies or references the 'ReloadOnSpendMana' effect/state. | 1 |
| `ReloadOnUseAbilityWithManaCost` | Number | Applies or references the 'ReloadOnUseAbilityWithManaCost' effect/state. | 1 |
| [`RevengeDamage`](./Abilities_and_Spells.md#context-revengedamage) | Block | Reaction trigger: Deals damage to the attacker when hit. | 1 |
| [`StatusKillers`](./Abilities_and_Spells.md#context-statuskillers) | Block | Instantly kills the target if they possess the specified status effects. | 1 |
| `TossTargetIsAggroTarget` | Number | Applies or references the 'TossTargetIsAggroTarget' effect/state. | 1 |
| `TossTargetIsBuddy` | Number | Applies or references the 'TossTargetIsBuddy' effect/state. | 1 |
| `TossTargetIsNotInWater` | Number | Applies or references the 'TossTargetIsNotInWater' effect/state. | 1 |
| `Trample` | Number | Applies or references the 'Trample' effect/state. | 1 |
| `XIsConsumedCharacterMaxHP` | Number | Applies or references the 'XIsConsumedCharacterMaxHP' effect/state. | 1 |
| `XIsCountDeaths` | Number | Applies or references the 'XIsCountDeaths' effect/state. | 1 |
| [`XIsCountStatusStacks`](./Enums.md#enum-xiscountstatusstacks) | Enum/String | Applies or references the 'XIsCountStatusStacks' effect/state. | 1 |
| [`XIsFormulaLockedUntilComplete`](./Enums.md#enum-xisformulalockeduntilcomplete) | Enum/String | Applies or references the 'XIsFormulaLockedUntilComplete' effect/state. | 1 |
| `XIsIncreaseEachTurn` | Number | Applies or references the 'XIsIncreaseEachTurn' effect/state. | 1 |
| `XIsRampAndReset` | Number | Applies or references the 'XIsRampAndReset' effect/state. | 1 |
| `XIsRecycleCostReduction` | Number | Applies or references the 'XIsRecycleCostReduction' effect/state. | 1 |

</details>

---

### Context: `ChanceToBreakFree`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/11) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ability triggered upon successfully breaking free. | 11 |
| [`fail_ability`](./Enums.md#enum-fail_ability) | Enum/String | The ability triggered if the break free attempt fails. | 3 |
| `stacks` | Number | Percentage base chance to break free. | 3 |

</details>

---

### Context: `ChangeTile`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/11) |
| :--- | :--- | :--- | :--- |
| [`tile`](./Enums.md#enum-tile) | Enum/String | The specific tile type to change into (e.g., GlassTile). | 11 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |
| `aoe` | Number |  | 1 |

</details>

---

### Context: `additional_passives`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#context-spawn)

| Property Key | Type | Definition | Count (X/11) |
| :--- | :--- | :--- | :--- |
| `SafeDoomed` | Number | Applies or references the 'SafeDoomed' effect/state. | 11 |
| `InjuryImmunity` | Number | Applies or references the 'InjuryImmunity' effect/state. | 7 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 2 |
| `FadeInsteadOfDie` | Number | Applies or references the 'FadeInsteadOfDie' effect/state. | 2 |
| `IllusionTint` | Number | Applies or references the 'IllusionTint' effect/state. | 2 |
| `PermanentMadness` | Number | Applies or references the 'PermanentMadness' effect/state. | 2 |
| [`ApplyPassivesToSpawnerWhileAlive`](./Abilities_and_Spells.md#context-applypassivestospawnerwhilealive) | Block | Grants nested passives to the entity that spawned this object, lasting only as long as this object remains alive. | 1 |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 1 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 1 |
| `FillMana` | Number | Applies or references the 'FillMana' effect/state. | 1 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 1 |
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum/String | Applies or references the 'HideEquipment' effect/state. | 1 |
| [`ReviveNextRound`](./Abilities_and_Spells.md#context-revivenextround) | Block | Queues the character to be resurrected at the start of the next combat round. | 1 |
| `SchizoIllusionAIModifier` | Number | Applies or references the 'SchizoIllusionAIModifier' effect/state. | 1 |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 1 |

</details>

---

### Context: `CanApplyToInanimate`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/10) |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum/String | Spawns a specific character or entity upon impact. | 10 |
| [`BreakIntoRocks`](./Enums.md#enum-breakintorocks) | Enum/String | Applies or references the 'BreakIntoRocks' effect/state. | 4 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 3 |
| `GetAggroTarget` | Number | Applies or references the 'GetAggroTarget' effect/state. | 2 |
| `PreventDeathTransforms` | Number | Applies or references the 'PreventDeathTransforms' effect/state. | 1 |
| [`Temporary`](./Abilities_and_Spells.md#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 1 |

</details>

---

### Context: `CatPartsTransform`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/10) |
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

### Context: `DoScreenShake`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/10) |
| :--- | :--- | :--- | :--- |
| `intensity` | Number |  | 10 |
| [`time`](./Enums.md#enum-time) | Enum/String |  | 10 |

</details>

---

### Context: `Craft`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum/String |  | 9 |
| [`slot`](./Enums.md#enum-slot) | Enum/String |  | 8 |
| `temporary` | Boolean |  | 4 |
| `works_with_tech` | Boolean |  | 1 |

</details>

---

### Context: `Conditional_FormulaIsPositive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| [`formula`](./Enums.md#enum-formula) | Enum/String | The math expression to evaluate. | 8 |
| [`Burn`](./Enums.md#enum-burn) | Enum/String | Applies or references the 'Burn' effect/state. | 2 |
| `Immobile` | Number | Applies or references the 'Immobile' effect/state. | 2 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 2 |
| `Freeze` | Number | Applies or references the 'Freeze' effect/state. | 1 |
| [`OverrideKnockbackDamage`](./Enums.md#enum-overrideknockbackdamage) | Enum/String | Applies or references the 'OverrideKnockbackDamage' effect/state. | 1 |
| [`Slow`](./Enums.md#enum-slow) | Enum/String | Applies or references the 'Slow' effect/state. | 1 |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 1 |
| `Stun` | Number | Applies or references the 'Stun' effect/state. | 1 |

</details>

---

### Context: `Conditional_InForm`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum/String | The specific form ID to check for. | 7 |
| [`FormChange`](./Enums.md#enum-formchange) | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 5 |
| `CritChanceUp` | Number | Applies or references the 'CritChanceUp' effect/state. | 1 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 1 |
| `DodgeChance_Status` | Number | Applies or references the 'DodgeChance_Status' effect/state. | 1 |
| [`ForceImmediateMoveAndAttack`](./Abilities_and_Spells.md#context-forceimmediatemoveandattack) | Block | Forces the character to immediately move to a target and use a specified ability. | 1 |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 1 |
| [`UseAbility`](./Enums.md#enum-useability) | Enum/String | Forces the character or target to instantly use a specified ability. | 1 |

</details>

---

### Context: `Else`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object), [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| [`GainDisorderFromPool_PostCast`](./Enums.md#enum-gaindisorderfrompool_postcast) | Enum/String | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 7 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 6 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate) | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 3 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 3 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 2 |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#context-conditional_hasstatus) | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 2 |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 2 |
| [`FormChange`](./Abilities_and_Spells.md#context-formchange) | Block | Transforms the character into a different state or form (e.g., Rage, HasCat). | 2 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 2 |
| [`GainCoinsRange`](./Abilities_and_Spells.md#context-gaincoinsrange) | Block | Grants the player a randomized amount of coins within a min/max range. | 2 |
| [`RandomStatDown`](./Enums.md#enum-math_equation) | Equation | Applies or references the 'RandomStatDown' effect/state. | 2 |
| `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. | 2 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 2 |
| `SpawnBearTrapIfHitKills` | Number | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. | 2 |
| [`SpawnThingIfHitKills`](./Enums.md#enum-spawnthingifhitkills) | Enum/String | Applies or references the 'SpawnThingIfHitKills' effect/state. | 2 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 1 |
| [`ApplyToRandomPartyMemberIfPossible`](./Abilities_and_Spells.md#context-applytorandompartymemberifpossible) | Block | Redirects the nested effects to apply to a random living member of the player's party. | 1 |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 1 |
| [`CatPartsTransform`](./Abilities_and_Spells.md#context-catpartstransform) | Block | Transforms specific body parts into different visual variants. | 1 |
| `Charmed` | Number | Applies or references the 'Charmed' effect/state. | 1 |
| `Cleave` | Number | Causes the attack to hit adjacent enemies alongside the primary target. | 1 |
| [`Conditional_Displaceable`](./Abilities_and_Spells.md#context-conditional_displaceable) | Block | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 1 |
| [`Conditional_GoodRoll`](./Abilities_and_Spells.md#context-conditional_goodroll) | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 1 |
| [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag) | Block | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 1 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#context-conditional_healththreshold) | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 1 |
| [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object) | Block | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 1 |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative) | Block | A simulation block used by the AI to test hypothetical outcomes before committing to an action. | 1 |
| `ConstitutionUp` | Number | Applies or references the 'ConstitutionUp' effect/state. | 1 |
| [`Consumed`](./Abilities_and_Spells.md#context-consumed) | Block | State block triggered when this object or entity is eaten/consumed by another character. | 1 |
| `CritChanceUp` | Number | Applies or references the 'CritChanceUp' effect/state. | 1 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 1 |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#context-destroyequipmentandattachparasite) | Block | Removes an equipped item and replaces it with a parasite from a specified pool. | 1 |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. | 1 |
| [`DoDamage`](./Abilities_and_Spells.md#context-dodamage) | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 1 |
| `DodgeChance_Status` | Number | Applies or references the 'DodgeChance_Status' effect/state. | 1 |
| [`DybbukPossessed`](./Abilities_and_Spells.md#context-dybbukpossessed) | Block | Defines the abilities and behaviors available when possessing another entity. | 1 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |
| `ExplodeCharacter` | Number | Applies or references the 'ExplodeCharacter' effect/state. | 1 |
| `ExplodeCharacter_Party` | Number | Applies or references the 'ExplodeCharacter_Party' effect/state. | 1 |
| `FaceCamera` | Number | Applies or references the 'FaceCamera' effect/state. | 1 |
| `FlatAIBonus` | Number | Applies or references the 'FlatAIBonus' effect/state. | 1 |
| `ForceImmediateMove` | Number | Applies or references the 'ForceImmediateMove' effect/state. | 1 |
| `GenericDebuff` | Number | Applies or references the 'GenericDebuff' effect/state. | 1 |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum/String | Applies or references the 'ImmediateUseAbility' effect/state. | 1 |
| `Immobile` | Number | Applies or references the 'Immobile' effect/state. | 1 |
| `Instakill` | Number | Applies or references the 'Instakill' effect/state. | 1 |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#context-knockupandaway) | Block | Displaces the target vertically and horizontally away from the source. | 1 |
| `Leeches` | Number | Applies or references the 'Leeches' effect/state. | 1 |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum/String | Spawns a specific character or entity upon impact. | 1 |
| `OverrideDamage` | Number | Applies or references the 'OverrideDamage' effect/state. | 1 |
| `PartialCleanse` | Number | Applies or references the 'PartialCleanse' effect/state. | 1 |
| `PurgeAll` | Number | Applies or references the 'PurgeAll' effect/state. | 1 |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |
| `RemoveMovePoints` | Number | Applies or references the 'RemoveMovePoints' effect/state. | 1 |
| `RemoveTurnsThisRound` | Number | Applies or references the 'RemoveTurnsThisRound' effect/state. | 1 |
| [`ScatterCoins`](./Abilities_and_Spells.md#context-scattercoins) | Block | Throws coins out into the level randomly. | 1 |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. | 1 |
| `SetShield` | Number | Applies or references the 'SetShield' effect/state. | 1 |
| [`ShowFakeDamage`](./Abilities_and_Spells.md#context-showfakedamage) | Block | Displays a visual damage number without actually modifying health. | 1 |
| `Slow` | Number | Applies or references the 'Slow' effect/state. | 1 |
| `SpeculativeMoveSelfCorpseOffMap` | Number | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 1 |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 1 |
| [`Temporary`](./Abilities_and_Spells.md#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 1 |
| `VaporizeInanimate` | Number | Applies or references the 'VaporizeInanimate' effect/state. | 1 |
| [`XIsTargetHealth`](./Abilities_and_Spells.md#context-xistargethealth) | Block | Math variable assignment: Evaluates X as the target's current health. | 1 |

</details>

---

### Context: `ApplyStatusIfCrit`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 6 |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. | 3 |
| `LuckUp` | Number | Applies or references the 'LuckUp' effect/state. | 1 |

</details>

---

### Context: `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#context-conditional_hasstatus) | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 6 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 4 |
| `OverrideDamage` | Number | Applies or references the 'OverrideDamage' effect/state. | 4 |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 4 |
| [`VisualFX`](./Enums.md#enum-visualfx) | Enum/String | Applies or references the 'VisualFX' effect/state. | 3 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 2 |
| `Drowsy` | Number | Applies or references the 'Drowsy' effect/state. | 2 |
| `ExplodeCharacter_PartyBoss` | Number | Applies or references the 'ExplodeCharacter_PartyBoss' effect/state. | 2 |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Number | Applies or references the 'ExplodeCharacter_RockCrusher_PetrifyBreak' effect/state. | 2 |
| `Stun` | Number | Applies or references the 'Stun' effect/state. | 2 |
| `Charmed` | Number | Applies or references the 'Charmed' effect/state. | 1 |
| `ExplodeCharacter_NoDie` | Number | Applies or references the 'ExplodeCharacter_NoDie' effect/state. | 1 |
| `Fear` | Number | Applies or references the 'Fear' effect/state. | 1 |
| [`XIsTargetHealth`](./Abilities_and_Spells.md#context-xistargethealth) | Block | Math variable assignment: Evaluates X as the target's current health. | 1 |

</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Corpse`](./Abilities_and_Spells.md#context-conditional_corpse), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 6 |
| [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss) | Block | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 3 |
| `DisplaceToAbilityTarget` | Number | Applies or references the 'DisplaceToAbilityTarget' effect/state. | 3 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 2 |
| `Attraction` | Number | Applies or references the 'Attraction' effect/state. | 2 |
| `Fear` | Number | Applies or references the 'Fear' effect/state. | 2 |
| `Madness` | Number | Applies the Madness debuff/status effect. | 2 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 2 |
| `Weakness` | Number | Applies or references the 'Weakness' effect/state. | 2 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill) | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 1 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 1 |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 1 |
| `Charmed` | Number | Applies or references the 'Charmed' effect/state. | 1 |
| [`Conditional_FinishedSpawning`](./Abilities_and_Spells.md#context-conditional_finishedspawning) | Block | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. | 1 |
| `Doomed` | Number | Applies or references the 'Doomed' effect/state. | 1 |
| `ForceMoveTowards` | Number | Applies or references the 'ForceMoveTowards' effect/state. | 1 |
| `Hex` | Number | Applies or references the 'Hex' effect/state. | 1 |
| `Marked` | Number | Applies or references the 'Marked' effect/state. | 1 |
| `PermanentCharm` | Number | Applies or references the 'PermanentCharm' effect/state. | 1 |
| `Poison` | Number | Applies or references the 'Poison' effect/state. | 1 |
| [`Stun`](./Arrays.md#array-stun) | Array | Applies or references the 'Stun' effect/state. | 1 |
| `TempDamageUp` | Number | Applies or references the 'TempDamageUp' effect/state. | 1 |
| [`Temporary`](./Abilities_and_Spells.md#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 1 |

</details>

---

### Context: `DoDistortionRing`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| `intensity` | Number |  | 6 |
| `radius` | Number | Distance or area of effect in tiles. | 6 |
| `speed` | Number |  | 6 |

</details>

---

### Context: `SwitchMusic`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum/String | The specific audio layer to transition to (e.g., map, battle). | 6 |
| [`new_song`](./Enums.md#enum-new_song) | Enum/String | The ID of the new music track. | 5 |
| `crossfade_speed` | Number |  | 1 |

</details>

---

### Context: `TwisterDisplaceWithDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The damage formula or inherit flag. | 6 |
| `max_dist` | Number | Maximum displacement distance. | 6 |
| `min_dist` | Number | Minimum displacement distance. | 2 |
| [`exclude_prefix`](./Enums.md#enum-exclude_prefix) | Enum/String |  | 1 |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyStatusIfCrit`](./Abilities_and_Spells.md#context-applystatusifcrit), [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate), [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_GoodRoll`](./Abilities_and_Spells.md#context-conditional_goodroll), [`Conditional_HasStatus`](./Abilities_and_Spells.md#context-conditional_hasstatus), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#context-conditional_healththreshold), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#context-conditional_livingplayercat), [`Conditional_PlayerCat`](./Abilities_and_Spells.md#context-conditional_playercat), [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#context-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#context-else), [`Math`](./Abilities_and_Spells.md#context-math), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 5 |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. | 5 |
| [`EvolveAbilityFromPool`](./Enums.md#enum-evolveabilityfrompool) | Enum/String | Upgrades or transforms an existing ability into a new one from the specified pool. | 4 |
| [`FormChange`](./Enums.md#enum-formchange) | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 4 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 4 |
| `AddWeaponAux` | Number | Applies or references the 'AddWeaponAux' effect/state. | 3 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 3 |
| `ConstitutionUp` | Number | Applies or references the 'ConstitutionUp' effect/state. | 3 |
| [`Craft`](./Abilities_and_Spells.md#context-craft) | Block | Synthesizes or spawns a new item from a specific pool. | 3 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 3 |
| `AddLeechesStatus` | Number | Applies or references the 'AddLeechesStatus' effect/state. | 2 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 2 |
| [`DoDamage`](./Abilities_and_Spells.md#context-dodamage) | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 2 |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum/String | Applies or references the 'EquipPermanentItem' effect/state. | 2 |
| [`FindItemFromPool`](./Abilities_and_Spells.md#context-finditemfrompool) | Block | Generates an item drop from the specified loot pool. | 2 |
| `FreeSpell` | Number | Applies or references the 'FreeSpell' effect/state. | 2 |
| `LuckUp` | Number | Applies or references the 'LuckUp' effect/state. | 2 |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 2 |
| `Brace` | Number | Applies or references the 'Brace' effect/state. | 1 |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 1 |
| `DisableWeapon` | Number | Applies or references the 'DisableWeapon' effect/state. | 1 |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 1 |
| [`FindItem`](./Enums.md#enum-finditem) | Enum/String | Applies or references the 'FindItem' effect/state. | 1 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Applies or references the 'ForceUseAbility' effect/state. | 1 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 1 |
| [`GainCoinsRange`](./Abilities_and_Spells.md#context-gaincoinsrange) | Block | Grants the player a randomized amount of coins within a min/max range. | 1 |
| `KineticSpikes` | Number | Applies or references the 'KineticSpikes' effect/state. | 1 |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#context-knockupandaway) | Block | Displaces the target vertically and horizontally away from the source. | 1 |
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 1 |
| `MoveQuivered` | Number | Applies or references the 'MoveQuivered' effect/state. | 1 |
| `RefreshMovePoints` | Number | Applies or references the 'RefreshMovePoints' effect/state. | 1 |
| [`SpecificInjury`](./Enums.md#enum-specificinjury) | Enum/String | Applies or references the 'SpecificInjury' effect/state. | 1 |
| `StanceSwitchToMelee` | Number | Applies or references the 'StanceSwitchToMelee' effect/state. | 1 |
| `StanceSwitchToRanged` | Number | Applies or references the 'StanceSwitchToRanged' effect/state. | 1 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 1 |
| `Tech` | Number | Applies or references the 'Tech' effect/state. | 1 |
| `TempTrampleUntilSettled` | Number | Applies or references the 'TempTrampleUntilSettled' effect/state. | 1 |

</details>

---

### Context: `DestroyEquipmentAndAttachParasite`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_ActiveWeather_Any`](./Abilities_and_Spells.md#context-conditional_activeweather_any), [`Conditional_DebuffRoll`](./Abilities_and_Spells.md#context-conditional_debuffroll), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | The item pool to draw the parasite from. | 5 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 3 |

</details>

---

### Context: `DoDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Else`](./Abilities_and_Spells.md#context-else), [`post_spawn_statuses`](./Abilities_and_Spells.md#context-post_spawn_statuses)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The flat damage amount. | 5 |
| [`type`](./Enums.md#enum-type) | Enum/String | The classification of the damage (e.g., spell, melee). | 5 |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum/String |  | 2 |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum/String | Applies or references the 'BonusAbility' effect/state. | 5 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 2 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 2 |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. | 1 |
| `Brace` | Number | Applies or references the 'Brace' effect/state. | 1 |
| `Charmed` | Number | Applies or references the 'Charmed' effect/state. | 1 |
| `Madness` | Number | Applies the Madness debuff/status effect. | 1 |
| `PermanentMadness` | Number | Applies or references the 'PermanentMadness' effect/state. | 1 |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. | 1 |
| `TemporaryItem` | Number | Applies or references the 'TemporaryItem' effect/state. | 1 |
| `Webbed` | Number | Applies or references the 'Webbed' effect/state. | 1 |

</details>

---

### Context: `ArcLightning`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, the arc will not bounce to friendly targets. | 4 |
| `max_distance` | Number | The maximum tile range the lightning can jump between bounces. | 4 |
| `stacks` | Number | The maximum number of targets the lightning can bounce to. | 4 |
| [`chance`](./Enums.md#enum-chance) | Enum/String | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| `ignore_self` | Boolean | If true, prevents the arc from bouncing back to the caster. | 1 |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific dodge ability to trigger (e.g., DestroyerDodge). | 4 |
| `stacks` | Number | Number of stacks or intensity to apply. | 4 |

</details>

---

### Context: `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | Number | Applies or references the 'OverrideDamage' effect/state. | 4 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 3 |
| `KnockbackDamageImmuneUntilSettled` | Number | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. | 3 |
| [`Temporary`](./Abilities_and_Spells.md#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 3 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 2 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 2 |
| [`RandomStatUp`](./Enums.md#enum-math_equation) | Equation | Applies or references the 'RandomStatUp' effect/state. | 2 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill) | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 1 |
| `BleedThorns` | Number | Applies or references the 'BleedThorns' effect/state. | 1 |
| `ChanceToBreak` | Number | Applies or references the 'ChanceToBreak' effect/state. | 1 |
| `Charmed` | Number | Applies or references the 'Charmed' effect/state. | 1 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 1 |
| [`Conditional_Corpse`](./Abilities_and_Spells.md#context-conditional_corpse) | Block | Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 1 |
| [`Conditional_PlayerCat`](./Abilities_and_Spells.md#context-conditional_playercat) | Block | Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 1 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 1 |
| `RepairAll` | Number | Applies or references the 'RepairAll' effect/state. | 1 |
| `ShowText` | String | Applies or references the 'ShowText' effect/state. | 1 |
| `TempDamageUp` | Number | Applies or references the 'TempDamageUp' effect/state. | 1 |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. | 1 |
| `ThornsDamageImmuneUntilSettled` | Number | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. | 1 |
| `TileDamageImmuneUntilSettled` | Number | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. | 1 |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 4 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 2 |
| [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy) | Block | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 1 |
| `FlatAIBonus` | Number | Applies or references the 'FlatAIBonus' effect/state. | 1 |
| `HealRandomInjury` | Number | Applies or references the 'HealRandomInjury' effect/state. | 1 |
| `PermanentCharm` | Number | Applies or references the 'PermanentCharm' effect/state. | 1 |

</details>

---

### Context: `Conditional_HealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `threshold_flat` | Number | A flat numerical health value threshold. | 4 |
| [`SpawnThingIfHitKills`](./Enums.md#enum-spawnthingifhitkills) | Enum/String | Applies or references the 'SpawnThingIfHitKills' effect/state. | 2 |
| `threshold_percent` | Number | A percentage-based health threshold (e.g. 50%). | 2 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`BonusDamage`](./Enums.md#enum-math_equation) | Equation | Applies or references the 'BonusDamage' effect/state. | 1 |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 1 |
| `Die` | Number | Applies or references the 'Die' effect/state. | 1 |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. | 1 |
| `FactionConversion` | Number | Applies or references the 'FactionConversion' effect/state. | 1 |
| `FlatLeech` | Number | Applies or references the 'FlatLeech' effect/state. | 1 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 1 |
| `Instakill` | Number | Applies or references the 'Instakill' effect/state. | 1 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 1 |
| [`threshold_expr`](./Enums.md#enum-threshold_expr) | Enum/String |  | 1 |

</details>

---

### Context: `GainCoinsRange`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `max` | Number | Maximum coins granted. | 4 |
| `min` | Number | Minimum coins granted. | 4 |

</details>

---

### Context: `LeaveBehind`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String | The entity ID to spawn. | 4 |

</details>

---

### Context: `ReplaceSpell`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#context-temppassivewhilehasstatus)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The new ability ID to insert. | 4 |
| `slot` | Number | The spell slot index to replace. | 4 |

</details>

---

### Context: `TempPassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_FirstApplicationThisTurn`](./Abilities_and_Spells.md#context-conditional_firstapplicationthisturn), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#context-conditional_livingplayercat)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`ReplaceSpell`](./Abilities_and_Spells.md#context-replacespell) | Block | Replaces a spell in the character's hand/deck with a different one. | 4 |
| [`status`](./Enums.md#enum-status) | Enum/String | The required status effect. | 3 |
| [`MeleeRevengeDamage`](./Abilities_and_Spells.md#context-meleerevengedamage) | Block | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. | 2 |
| `AddManaRegen` | Number | Applies or references the 'AddManaRegen' effect/state. | 1 |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 1 |

</details>

---

### Context: `TimeDelayStatusApplication`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `delay` | Number | The float time delay in seconds. | 4 |
| [`SwitchMusic`](./Abilities_and_Spells.md#context-switchmusic) | Block | Changes the background music track or layer during combat. | 2 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 1 |
| [`CreateGlobalModifiers`](./Abilities_and_Spells.md#context-createglobalmodifiers) | Block | Generates global map or encounter rules/modifiers. | 1 |
| [`DoScreenShake`](./Abilities_and_Spells.md#context-doscreenshake) | Block | Triggers a camera screen shake effect. | 1 |
| [`FormChange`](./Enums.md#enum-formchange) | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 1 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 1 |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum/String | Applies or references the 'GlobalSpawnCharacter' effect/state. | 1 |
| `PlayBackground` | Number | Applies or references the 'PlayBackground' effect/state. | 1 |
| [`RemoveAmbientLightEffects`](./Enums.md#enum-removeambientlighteffects) | Enum/String | Applies or references the 'RemoveAmbientLightEffects' effect/state. | 1 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 1 |

</details>

---

### Context: `rocket_swirl`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`radius`](./Arrays.md#array-radius) | Array | Swirl radius. | 4 |
| [`speed`](./Arrays.md#array-speed) | Array | Rotations per second. | 4 |

</details>

---

### Context: `ApplyMultipleTimes`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 3 |
| [`stacks`](./Enums.md#enum-stacks) | Enum/String | The number of times the nested effects block should be repeatedly executed. | 3 |

</details>

---

### Context: `ApplyPassives`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_RandomChance`](./Abilities_and_Spells.md#context-conditional_randomchance), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`StatusOnBattleEnd`](./Abilities_and_Spells.md#context-statusonbattleend) | Block | Applies the nested status effects when the encounter finishes. | 3 |
| [`AddTag`](./Enums.md#enum-addtag) | Enum/String | Applies or references the 'AddTag' effect/state. | 2 |
| `Flying` | Number | Applies or references the 'Flying' effect/state. | 2 |
| `IgnoreTiles` | Number | Applies or references the 'IgnoreTiles' effect/state. | 2 |
| [`YOffset`](./Enums.md#enum-yoffset) | Enum/String | Applies or references the 'YOffset' effect/state. | 2 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum/String | Applies or references the 'ElementImmune' effect/state. | 1 |
| `KnockbackImmunity` | Number | Applies or references the 'KnockbackImmunity' effect/state. | 1 |
| `Plant` | Number | Applies or references the 'Plant' effect/state. | 1 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum/String | Applies or references the 'ReplaceBasicAttack' effect/state. | 1 |

</details>

---

### Context: `ApplyToConsumed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `DeleteObject` | Number | Applies or references the 'DeleteObject' effect/state. | 3 |
| `Die` | Number | Applies or references the 'Die' effect/state. | 1 |

</details>

---

### Context: `ApplyToSourceOnKill`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum/String | Applies or references the 'RemoveItem' effect/state. | 3 |
| `AlphaCat` | Number | Applies or references the 'AlphaCat' effect/state. | 2 |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum/String | Applies or references the 'CompleteItemQuest' effect/state. | 2 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 2 |
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 2 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 2 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 1 |
| [`EvolveAbilityFromPool`](./Enums.md#enum-evolveabilityfrompool) | Enum/String | Upgrades or transforms an existing ability into a new one from the specified pool. | 1 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 1 |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. | 1 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 1 |
| [`TransformWeapon`](./Abilities_and_Spells.md#context-transformweapon) | Block | Transforms the equipped weapon into another specific weapon state. | 1 |
| [`WeaponAuxMultiplier`](./Enums.md#enum-weaponauxmultiplier) | Enum/String | Applies or references the 'WeaponAuxMultiplier' effect/state. | 1 |

</details>

---

### Context: `BounceObject`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`obj`](./Enums.md#enum-obj) | Enum/String | The entity ID of the object to spawn (e.g., chapter_corpse_medium). | 3 |
| [`chance`](./Enums.md#enum-chance) | Enum/String | Probability (0.0 to 1.0) of spawning the object. | 2 |
| `slide` | Number |  | 1 |

</details>

---

### Context: `Conditional_AffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | The specific element type to check for. | 3 |
| `BonusCritChance` | Number | Applies or references the 'BonusCritChance' effect/state. | 2 |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 1 |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative) | Block | A simulation block used by the AI to test hypothetical outcomes before committing to an action. | 1 |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#context-temppassivewhilehasstatus) | Block | Grants nested passives only while the character possesses the specified status. | 3 |
| [`key`](./Enums.md#enum-key) | Enum/String | A unique string identifier to track this specific application. | 3 |

</details>

---

### Context: `Conditional_Object`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag) | Block | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 3 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 3 |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate) | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 1 |
| `RepairWeapon` | Number | Applies or references the 'RepairWeapon' effect/state. | 1 |

</details>

---

### Context: `Conditional_Speculative`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_AffectedByElement`](./Abilities_and_Spells.md#context-conditional_affectedbyelement), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `IgnoreDamage` | Number | Applies or references the 'IgnoreDamage' effect/state. | 3 |
| `BonusDamageBasedOnDistance` | Number | Applies or references the 'BonusDamageBasedOnDistance' effect/state. | 2 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#context-conditional_healththreshold) | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 2 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 1 |
| `CapDamage` | Number | Applies or references the 'CapDamage' effect/state. | 1 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |
| `Knockback` | Number | Applies or references the 'Knockback' effect/state. | 1 |
| `RandomBonusDamage` | Number | Applies or references the 'RandomBonusDamage' effect/state. | 1 |

</details>

---

### Context: `DustOnHit`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String | The ID of the object/particle to spawn. | 3 |

</details>

---

### Context: `IncAuxCounterClamped`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `change` | Number |  | 3 |
| `max` | Number |  | 3 |

</details>

---

### Context: `LateStatusApplication`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `CurrentWeaponDamageUp` | Number | Applies or references the 'CurrentWeaponDamageUp' effect/state. | 3 |
| `AddWeaponAux` | Number | Applies or references the 'AddWeaponAux' effect/state. | 1 |

</details>

---

### Context: `ReviveNextRound`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#context-additional_passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `revive_health` | Number | The flat amount of health to revive with. | 3 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 2 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 1 |

</details>

---

### Context: `SetCrazyEyeBackgroundWeights`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`weights`](./Arrays.md#array-weights) | Array |  | 3 |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./Abilities_and_Spells.md#context-applypassives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 3 |
| [`RandomTaggedMutation`](./Enums.md#enum-randomtaggedmutation) | Enum/String | Applies or references the 'RandomTaggedMutation' effect/state. | 2 |
| `RandomMutation` | Number | Applies or references the 'RandomMutation' effect/state. | 1 |

</details>

---

### Context: `AfterImage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#context-temporary_effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String | The entity ID of the visual decoy to spawn (e.g., PlayerCat_ThiefShade). | 2 |
| `skilltemp` | Boolean | If true, the decoy is automatically destroyed once the skill finishes executing. | 2 |

</details>

---

### Context: `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./Abilities_and_Spells.md#context-conditional_goodroll), [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`GainDisorderFromPool_PostCast`](./Enums.md#enum-gaindisorderfrompool_postcast) | Enum/String | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 2 |

</details>

---

### Context: `ApplyToTile`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_DestructibleCorpse`](./Abilities_and_Spells.md#context-conditional_destructiblecorpse)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHit`](./Enums.md#enum-objectonhit) | Enum/String | Spawns a specific physics/item object upon impact. | 2 |
| `SpawnBearTrap` | Number | Applies or references the 'SpawnBearTrap' effect/state. | 2 |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to autocast. | 2 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 1 |

</details>

---

### Context: `BodyGuard`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to use when intercepting (e.g., BodyGuardSwap). | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `CollectsPickupsWithAltEffects`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | Applies or references the 'Tech' effect/state. | 2 |
| `CurrentWeaponAddPoison` | Number | Applies or references the 'CurrentWeaponAddPoison' effect/state. | 1 |
| `LuckUp` | Number | Applies or references the 'LuckUp' effect/state. | 1 |
| `Quivered` | Number | Applies or references the 'Quivered' effect/state. | 1 |
| `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. | 1 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 1 |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Enum/String | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 2 |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. | 1 |
| `Instakill` | Number | Applies or references the 'Instakill' effect/state. | 1 |

</details>

---

### Context: `Conditional_BossOrBig`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Immobile`](./Arrays.md#array-immobile) | Array | Applies or references the 'Immobile' effect/state. | 2 |

</details>

---

### Context: `Conditional_DestructibleCorpse`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ApplyToTile`](./Abilities_and_Spells.md#context-applytotile) | Block | Redirects the nested effects to apply to the terrain/tile underneath the target rather than the target itself. | 2 |
| `VaporizeCorpse` | Number | Applies or references the 'VaporizeCorpse' effect/state. | 2 |

</details>

---

### Context: `Conditional_Familiar`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 2 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 1 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 1 |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 1 |

</details>

---

### Context: `Conditional_LastHit`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#context-knockupandaway) | Block | Displaces the target vertically and horizontally away from the source. | 2 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 1 |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 1 |
| [`DelayCastAbility`](./Enums.md#enum-delaycastability) | Enum/String | Queues an ability to be cast automatically after a certain delay or trigger. | 1 |

</details>

---

### Context: `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 2 |
| `Doomed` | Number | Applies or references the 'Doomed' effect/state. | 2 |
| `ExplodeCharacter_RockCrusher` | Number | Applies or references the 'ExplodeCharacter_RockCrusher' effect/state. | 2 |
| `FactionConversion` | Number | Applies or references the 'FactionConversion' effect/state. | 2 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 2 |
| `VaporizeInanimate` | Number | Applies or references the 'VaporizeInanimate' effect/state. | 2 |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate) | Block | Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 1 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#context-conditional_healththreshold) | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 1 |
| [`Fear`](./Arrays.md#array-fear) | Array | Applies or references the 'Fear' effect/state. | 1 |
| `PermanentCharm` | Number | Applies or references the 'PermanentCharm' effect/state. | 1 |

</details>

---

### Context: `Conditional_NotBossOrBig`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Immobile` | Number | Applies or references the 'Immobile' effect/state. | 2 |

</details>

---

### Context: `Conditional_NotShielded`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Knockback` | Number | Applies or references the 'Knockback' effect/state. | 2 |

</details>

---

### Context: `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum/String | Applies or references the 'CompleteItemQuest' effect/state. | 2 |
| `TriggerGameEnding` | Number | Applies or references the 'TriggerGameEnding' effect/state. | 2 |
| [`key`](./Enums.md#enum-key) | Enum/String |  | 2 |

</details>

---

### Context: `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `ConjureRandomAbilityFromCat` | Number | Applies or references the 'ConjureRandomAbilityFromCat' effect/state. | 2 |
| `Adrenaline` | Number | Applies or references the 'Adrenaline' effect/state. | 1 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 1 |
| `GenericDebuff` | Number | Applies or references the 'GenericDebuff' effect/state. | 1 |
| [`KnockOutClone`](./Enums.md#enum-knockoutclone) | Enum/String | Applies or references the 'KnockOutClone' effect/state. | 1 |
| `Scrambled` | Number | Applies or references the 'Scrambled' effect/state. | 1 |
| `T2CopyCat` | Number | Applies or references the 'T2CopyCat' effect/state. | 1 |

</details>

---

### Context: `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Cleave` | Number | Causes the attack to hit adjacent enemies alongside the primary target. | 2 |
| [`BonusDamage`](./Enums.md#enum-bonusdamage) | Enum/String | Applies or references the 'BonusDamage' effect/state. | 1 |
| `Stun` | Number | Applies or references the 'Stun' effect/state. | 1 |

</details>

---

### Context: `ConjureBonusAbility`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to conjure. | 2 |
| `upgraded` | Boolean | If true, conjures the upgraded version of the ability. | 2 |

</details>

---

### Context: `CreateGlobalModifiers`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `BloodRain` | Number | Applies or references the 'BloodRain' effect/state. | 2 |
| [`LowerAmbientLight`](./Abilities_and_Spells.md#context-lowerambientlight) | Block | A visual effect that dims the map's lighting. | 2 |

</details>

---

### Context: `FindItemFromPool`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum/String | Probability of finding the item. | 2 |
| [`pool`](./Enums.md#enum-pool) | Enum/String | The item pool to draw from. | 1 |

</details>

---

### Context: `ForceAttack`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `immediate` | Boolean |  | 2 |

</details>

---

### Context: `ForceMoveTowardsTaggedObject`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The movement ability to use. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum/String | The entity tag to seek out. | 1 |

</details>

---

### Context: `LowerAmbientLight`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CreateGlobalModifiers`](./Abilities_and_Spells.md#context-createglobalmodifiers)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array | The target opacity/dimness level. | 2 |
| `speed` | Number | The transition speed. | 2 |

</details>

---

### Context: `Math`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Stun` | Number | Applies or references the 'Stun' effect/state. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#context-temppassivewhilehasstatus)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |

</details>

---

### Context: `NukeQuestFinalBossModifications`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`self_damage`](./Abilities_and_Spells.md#context-self_damage) | Block | Recoil or self-inflicted damage/effects applied to the caster. | 2 |
| [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance) | Block |  | 1 |
| [`splash_damage`](./Abilities_and_Spells.md#context-splash_damage) | Block | Secondary Area of Effect blast parameters. | 1 |

</details>

---

### Context: `ObjectOnHit`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String | The entity ID of the object to spawn (e.g., Poop). | 2 |

</details>

---

### Context: `ObjectOnHitCharacter`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum/String | Probability (0.0 to 1.0) of spawning. | 2 |
| [`object`](./Enums.md#enum-object) | Enum/String | The entity ID of the character to spawn (e.g., CharmedFlea). | 2 |

</details>

---

### Context: `PopAndSpawn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String | The entity ID to spawn in place. | 2 |
| `clone_items` | Boolean | If true, transfers inventory to the new entity. | 1 |
| `clone_referenced_catdata` | Boolean | If true, copies the genetic data of the popped cat. | 1 |
| `no_splatter` | Boolean |  | 1 |

</details>

---

### Context: `QuakeAreaChance`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability of triggering the quake. | 2 |
| `radius` | Number | The tile radius of the quake. | 2 |

</details>

---

### Context: `RandomKnockback`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `max` | Number | Maximum knockback distance. | 2 |
| `min` | Number | Minimum knockback distance. | 2 |

</details>

---

### Context: `RandomMagicMissile`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `full_size` | Boolean | If true, fires normal sized missiles instead of mini ones. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `ScatterCoins`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#context-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `stackable` | Boolean | If true, multiple instances of this trigger can stack. | 2 |
| [`stacks`](./Enums.md#enum-stacks) | Enum/String | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `TakeBonusTurnWithAIControl`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | If true, allows the AI to cast spells during this bonus turn. | 2 |

</details>

---

### Context: `TakeBonusTurnWithStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | Applies the Madness debuff/status effect. | 2 |
| `Stun` | Number | Applies or references the 'Stun' effect/state. | 2 |
| `TempNoManaRegen` | Number | Applies or references the 'TempNoManaRegen' effect/state. | 2 |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 1 |

</details>

---

### Context: `TeamCastAbility`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The underlying logic ability executed by the team. | 2 |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum/String | Requires participants to share this tag. | 2 |
| `same_orientation` | Boolean |  | 1 |

</details>

---

### Context: `XIsTargetHealth`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`BonusDamage`](./Enums.md#enum-math_equation) | Equation | Applies or references the 'BonusDamage' effect/state. | 2 |

</details>

---

### Context: `empty_self_damage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |

</details>

---

### Context: `post_spawn_statuses`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#context-spawn)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`DoDamage`](./Abilities_and_Spells.md#context-dodamage) | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 2 |
| [`EnterMount`](./Enums.md#enum-entermount) | Enum/String | Applies or references the 'EnterMount' effect/state. | 1 |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum/String | Applies or references the 'VisualFXTile' effect/state. | 1 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhileNotTakingTurn`](./Abilities_and_Spells.md#context-passivewhilenottakingturn), [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. | 1 |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 1 |

</details>

---

### Context: `AlphaStatusOnTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `DoubleCastSpellThisTurn` | Number | Applies or references the 'DoubleCastSpellThisTurn' effect/state. | 1 |

</details>

---

### Context: `ApplyPassivesToSpawnerWhileAlive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#context-additional_passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum/String | Applies or references the 'HideEquipment' effect/state. | 1 |

</details>

---

### Context: `ApplyStatusesNextTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | Applies or references the 'Quivered' effect/state. | 1 |

</details>

---

### Context: `ApplyToOthersWithSharedTagAndFaction`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Marked` | Number | Applies or references the 'Marked' effect/state. | 1 |

</details>

---

### Context: `ApplyToRandomClosestAlly`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | Number | Applies or references the 'ForceMoveTowards' effect/state. | 1 |

</details>

---

### Context: `CatPartsSizeScaleStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `arm1` | Number | Scale multiplier for the front arm. | 1 |
| `arm2` | Number | Scale multiplier for the back arm. | 1 |
| `body` | Number |  | 1 |
| `mouth` | Number |  | 1 |

</details>

---

### Context: `Cleave`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum/String | Probability (0.0 to 1.0) that the cleave effect triggers. | 1 |

</details>

---

### Context: `Conditional_ActiveWeather_Any`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#context-destroyequipmentandattachparasite) | Block | Removes an equipped item and replaces it with a parasite from a specified pool. | 1 |
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. | 1 |

</details>

---

### Context: `Conditional_Backstab`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `BonusCritChance` | Number | Applies or references the 'BonusCritChance' effect/state. | 1 |
| `Fear` | Number | Applies or references the 'Fear' effect/state. | 1 |

</details>

---

### Context: `Conditional_Buddy`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_InForm`](./Abilities_and_Spells.md#context-conditional_inform) | Block | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 1 |
| [`Consumed`](./Abilities_and_Spells.md#context-consumed) | Block | State block triggered when this object or entity is eaten/consumed by another character. | 1 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |

</details>

---

### Context: `Conditional_CanBeHealed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `Conditional_DebuffRoll`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#context-destroyequipmentandattachparasite) | Block | Removes an equipped item and replaces it with a parasite from a specified pool. | 1 |
| `odds` | Number | The probability (0.0 to 1.0) of applying the debuff. | 1 |

</details>

---

### Context: `Conditional_Displaceable`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`LaunchOffScreen`](./Enums.md#enum-math_equation) | Equation | Applies or references the 'LaunchOffScreen' effect/state. | 1 |
| `LaunchOffScreenInstakill` | Number | Applies or references the 'LaunchOffScreenInstakill' effect/state. | 1 |
| `TempInitiativeChange` | Number | Applies or references the 'TempInitiativeChange' effect/state. | 1 |

</details>

---

### Context: `Conditional_FinishedSpawning`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Imprison`](./Enums.md#enum-imprison) | Enum/String | Applies or references the 'Imprison' effect/state. | 1 |

</details>

---

### Context: `Conditional_HasCleansableDebuffs`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `GenericBuff` | Number | Applies or references the 'GenericBuff' effect/state. | 1 |
| `PartialCleanse` | Number | Applies or references the 'PartialCleanse' effect/state. | 1 |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `Conditional_IsSelf`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | Number | Applies or references the 'OverrideDamage' effect/state. | 1 |

</details>

---

### Context: `Conditional_IsTrample`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `SetKnockback` | Number | Applies or references the 'SetKnockback' effect/state. | 1 |

</details>

---

### Context: `Conditional_LivingPlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`Consumed`](./Abilities_and_Spells.md#context-consumed) | Block | State block triggered when this object or entity is eaten/consumed by another character. | 1 |
| [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#context-temppassivewhilehasstatus) | Block | Grants nested passives only while the character possesses the specified status. | 1 |

</details>

---

### Context: `Conditional_NotAlly`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 1 |
| [`Temporary`](./Abilities_and_Spells.md#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 1 |

</details>

---

### Context: `Conditional_NotBig`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `DisplaceTowardsSource` | Number | Applies or references the 'DisplaceTowardsSource' effect/state. | 1 |

</details>

---

### Context: `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ApplyPassives`](./Abilities_and_Spells.md#context-applypassives) | Block | Grants the nested passive abilities dynamically. | 1 |
| `odds` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Context: `Conditional_SourceAbilityHasTag`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`ScatterCoins`](./Abilities_and_Spells.md#context-scattercoins) | Block | Throws coins out into the level randomly. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String | Specific entity tag required. | 1 |

</details>

---

### Context: `Conditional_SourceHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 1 |
| [`status`](./Enums.md#enum-status) | Enum/String | ID of the status effect to apply or check. | 1 |

</details>

---

### Context: `CopySpells`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |
| `upgraded` | Boolean |  | 1 |

</details>

---

### Context: `DelayCastAbility`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to cast later. | 1 |
| `lingering` | Boolean |  | 1 |
| `relative` | Boolean |  | 1 |

</details>

---

### Context: `DelayedWindCone`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| `distance` | Number | Distance or area of effect in tiles. | 1 |

</details>

---

### Context: `DybbukPossessed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum/String |  | 1 |
| [`punch_self_ability`](./Enums.md#enum-punch_self_ability) | Enum/String |  | 1 |

</details>

---

### Context: `ForceImmediateMoveAndAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_InForm`](./Abilities_and_Spells.md#context-conditional_inform)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ability to execute after moving. | 1 |
| `even_if_cant_reach` | Boolean | If true, executes the attack even if the move fails to reach the target. | 1 |

</details>

---

### Context: `IncAuxCounterCycle`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `change` | Number |  | 1 |
| `max` | Number |  | 1 |

</details>

---

### Context: `KnockOutCoin`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum/String | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `Madness`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |
| `tickdown_this_turn` | Boolean |  | 1 |

</details>

---

### Context: `MergeDamageInstance`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `can_instapop` | Boolean | If false, prevents the damage from instantly popping the target. | 1 |
| `force_no_hit_animation` | Boolean | If true, suppresses the flinch/hit animation. | 1 |

</details>

---

### Context: `Metronome`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`banned_abilities`](./Arrays.md#array-banned_abilities) | Array |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `NextAttackSpecialCrit`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Number | Flat addition to the critical damage multiplier. | 1 |
| `extra_coins_per_stack` | Number | Grants bonus coins based on stacks. | 1 |
| `luck_increase` | Number | Increases luck stat for the attack. | 1 |

</details>

---

### Context: `NextBasicAttackCritsThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | If true, ensures the attack cannot be dodged. | 1 |
| `piercing` | Boolean | If true, the attack ignores armor. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `NextBattleStatusStacks`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | Number | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. | 1 |
| `fights` | Number | The number of encounters this buff/debuff persists for. | 1 |

</details>

---

### Context: `OverHealToStatuses`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. | 1 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 1 |
| `stack_scale` | Number |  | 1 |

</details>

---

### Context: `PassiveWhileNotTakingTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Abilities_and_Spells.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 1 |

</details>

---

### Context: `PoolMetronome`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | An array of ability IDs to randomly choose from. | 1 |

</details>

---

### Context: `RandomDistanceDisplace`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `min_dist` | Number | The minimum tile distance they will be moved. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `RemoveStatusStacks`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks to remove. | 1 |
| [`status`](./Enums.md#enum-status) | Enum/String | The specific status effect ID to remove. | 1 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |

</details>

---

### Context: `ScrambleLastUsedSpell`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `permanent` | Boolean | If true, the scramble persists for the rest of the run. | 1 |

</details>

---

### Context: `SetAnimationAlts`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`dead`](./Enums.md#enum-dead) | Enum/String |  | 1 |
| [`dying`](./Enums.md#enum-dying) | Enum/String |  | 1 |

</details>

---

### Context: `ShowFakeDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |
| [`style`](./Arrays.md#array-style) | Array | The visual font style for the text (e.g., [crit]). | 1 |

</details>

---

### Context: `SmartMetronome`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |
| `upgraded` | Boolean |  | 1 |

</details>

---

### Context: `SpreadDisease`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of transmitting. | 1 |
| [`disease`](./Enums.md#enum-disease) | Enum/String | The specific status effect ID representing the disease. | 1 |

</details>

---

### Context: `StatusGroup`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `DamageOrHealConditionally` | Number | Applies or references the 'DamageOrHealConditionally' effect/state. | 1 |
| `Freeze` | Number | Applies or references the 'Freeze' effect/state. | 1 |

</details>

---

### Context: `StatusKillers`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 1 |

</details>

---

### Context: `SwapWeapon`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | An array of weapon item IDs to draw from. | 1 |

</details>

---

### Context: `Tangled`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`alt_art`](./Enums.md#enum-alt_art) | Enum/String | The alternative sprite art to use while tangled. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `TransformEquipment`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum/String | The original item ID. | 1 |
| [`to`](./Enums.md#enum-to) | Enum/String | The new item ID. | 1 |

</details>

---

### Context: `TransformWeapon`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum/String | The original weapon ID. | 1 |
| [`to`](./Enums.md#enum-to) | Enum/String | The transformed weapon ID. | 1 |

</details>

---

### Context: `UseAbility`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to trigger. | 1 |
| `respect_prime` | Boolean | If true, respects the ability's prime/cooldown state. | 1 |

</details>

---

### Context: `UseMoveAbilityWithAI`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | ID of the ability to trigger or reference. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String | The AI positioning logic profile to use. | 1 |

</details>

---

### Context: `VisualCountDownThenApplyStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Applies or references the 'ForceUseAbility' effect/state. | 1 |

</details>

---

### Context: `WaggleClone`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`1x1_object`](./Enums.md#enum-1x1_object) | Enum/String | The 1x1 variant of the object. | 1 |
| [`2x2_object`](./Enums.md#enum-2x2_object) | Enum/String | The 2x2 variant of the object. | 1 |
| [`3x3_object`](./Enums.md#enum-3x3_object) | Enum/String | The 3x3 variant of the object. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `XIsSpellStormRampAndReset`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `reset_percent` | Number | The percentage of stacks to keep after resetting. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `bonk_damage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |

</details>

---

### Context: `damage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification/category type. | 1 |

</details>

---

### Context: `damage_threshold_altanimations`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `heaviestMelee` | Number | Animation trigger for massive damage. | 1 |
| `heavyMelee` | Number | Animation trigger if damage exceeds this threshold. | 1 |

</details>

---

### Context: `extra_statuses`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Consumed`](./Abilities_and_Spells.md#context-consumed)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 1 |
| `Poison` | Number | Applies or references the 'Poison' effect/state. | 1 |
| `Tarred` | Number | Applies or references the 'Tarred' effect/state. | 1 |

</details>

---

