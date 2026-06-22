# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Abilities & Spells

> **Associated Files:** `data/abilities/, data/ability_templates/`


### Context: `ROOT` (2343 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance) | Block | Block defining the combat math and status effects applied upon successful hit. | 2343 |
| [`meta`](./Abilities_and_Spells.md#context-meta) | Block | Block defining UI display data (Name, Description, Icon). | 2333 |
| [`template`](./Enums.md#enum-template) | Enum | Inherits baseline internal logic from a hardcoded engine template. | 2174 |
| [`graphics`](./Abilities_and_Spells.md#context-graphics) | Block | Block defining visual animations and sequence timings. | 2037 |
| [`target`](./Abilities_and_Spells.md#context-target) | Block | Block defining the shape, range, and restrictions of the ability's aiming phase. | 1862 |
| [`cost`](./Abilities_and_Spells.md#context-cost) | Block | Block defining resource requirements (Mana, Act Points, Moves) needed to cast. | 1851 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum | Inherits properties from a previously defined ability (used for upgrading tiers). | 900 |
| [`tags`](./Arrays.md#array-tags) | Array | Array of string categories used by the engine for filtering (e.g. [weapon_throw, spell]). | 238 |
| [`self_damage`](./Abilities_and_Spells.md#context-self_damage) | Block | Recoil or self-inflicted damage/effects applied to the caster. | 218 |
| [`spawn`](./Abilities_and_Spells.md#context-spawn) | Block | Parameters for summoning new characters, objects, or entities. | 192 |
| [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives) | Block | Passives granted to the character while this ability is equipped. | 136 |
| [`class`](./Enums.md#enum-class) | Enum | Categorizes the ability for specific UI filters. | 90 |
| [`temporary_effects`](./Abilities_and_Spells.md#context-temporary_effects) | Block | Status applications that wear off automatically or at the end of the turn. | 88 |
| [`sounds`](./Abilities_and_Spells.md#context-sounds) | Block | Audio cues triggered by the ability. | 39 |
| [`splash_damage`](./Abilities_and_Spells.md#context-splash_damage) | Block | Secondary Area of Effect blast parameters. | 34 |
| [`ai_ability`](./Enums.md#enum-ai_ability) | Enum | Overrides the ability used when triggered by AI. | 29 |
| [`keyword_tooltips`](./Abilities_and_Spells.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear when hovering over the ability. | 23 |
| [`chain_ability`](./Enums.md#enum-chain_ability) | Enum | An ability that automatically executes sequentially after this one. | 15 |
| [`sub_ability`](./Enums.md#enum-sub_ability) | Enum | A secondary ability component referenced by complex templates. | 8 |
| [`cloned_ability`](./Enums.md#enum-cloned_ability) | Enum | Copies the properties of another ability dynamically. | 2 |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`empty_self_damage`](./Abilities_and_Spells.md#context-empty_self_damage) | Block | Recoil damage specifically applied when the attack misses all targets. | 2 |
| [`bonk_damage`](./Abilities_and_Spells.md#context-bonk_damage) | Block | Damage dealt when knocked into a wall or obstacle. | 1 |
| [`damage`](./Abilities_and_Spells.md#context-damage) | Block | The base damage properties of an attack. | 1 |

</details>

---

### Context: `damage_instance` (2344 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#context-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#context-root)

> **Engine Schema:** This block is a `[damage_instance]` container. [View all confirmed values in Engine_Damage.md](./Engine_Damage.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[damage_instance]`](./Engine_Damage.md#all-confirmed-damage-instance-values) | Block | A damage hit definition. See Engine_Damage.md for the full schema. |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1785 |
| `damage` | Number | The base damage properties of an attack. | 1446 |
| [`type`](./Enums.md#enum-type) | Enum | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). | 358 |
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 352 |
| [`knockback`](./Math_Equations.md) | Equation | The base physics pushing power (in tiles). | 254 |
| `ai_base_score` | Number | How highly the AI values using this ability. | 223 |
| `heal` | Number | Restores health instead of dealing damage. | 122 |
| `cant_miss` | Boolean | Guarantees the hit, bypassing dodge mechanics. | 110 |
| `incidentally_collects_pickups` | Boolean | Automatically grabs items in the AoE. | 103 |
| [`custom_additional_ai_weight`](./Enums.md#enum-custom_additional_ai_weight) | Enum | Granular AI preference adjustments (e.g., `prefer_dont_move`). | 82 |
| `piercing` | Boolean | Ignores a percentage of target defense/armor. | 52 |
| `makes_contact` | Boolean | If false, explicitly avoids triggering contact-based passives. | 40 |
| [`layer`](./Enums.md#enum-layer) | Enum | Z-index targeting (e.g., `characters`, `self`). | 26 |
| [`blocked_damage`](./Math_Equations.md) | Equation | Base damage dealt if the attack is blocked. | 24 |
| [`raw_damage`](./Math_Equations.md) | Equation | Unmitigated, unscaled base numbers. | 22 |
| `crit_chance` | Number | Override for base critical hit probability. | 16 |
| `override_trample_damage` | Boolean | Custom damage value for trample moves. | 15 |
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. | 14 |
| `can_revive` | Boolean | Healing instance that can bring dead allies back to life. | 8 |
| `show_damage_on_0` | Boolean | Forces the "-0" floater text to appear. | 6 |
| `force_play_hit_animation` | Boolean | Forces the flinch animation even on 0 damage. | 5 |
| `blocked_multiplier` | Number | Multiplier applied when hitting a blocking target. | 4 |
| [`accuracy`](./Enums.md#enum-accuracy) | Enum | Hit chance modifier. | 3 |
| `can_collect_pickups` | Boolean | The damage instance can grab items on the ground. | 3 |
| `can_instapop` | Boolean | Allows the attack to instantly destroy specific weak entities. | 2 |
| `disallow_modifications` | Boolean | Prevents passives from altering this damage instance. | 2 |
| `force_no_contact` | Boolean | Bypasses all contact-based retaliation (Thorns, etc). | 2 |
| `non_lethal` | Boolean | Reduces target to 1 HP but will never kill. | 2 |
| [`raw_heal`](./Math_Equations.md) | Equation | Unmitigated, unscaled base numbers. | 2 |
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

### Context: `meta` (2333 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String | The localization key for the ability's display description. | 1641 |
| [`name`](./Strings.md#string-name) | String | The localization key for the ability's display name. | 1597 |
| [`class`](./Enums.md#enum-class) | Enum | Categorizes the ability for specific UI filters. | 876 |
| [`type_icon`](./Strings.md#string-type_icon) | String |  | 283 |
| `animate_name` | Boolean | If true, adds a visual pop/animation to the name text when cast. | 177 |
| [`icon_shell_frame`](./Strings.md#string-icon_shell_frame) | String |  | 28 |
| [`is_move`](./Enums.md#enum-is_move) | Enum |  | 20 |
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

### Context: `graphics` (2037 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

> **Engine Schema:** This block is a `[graphic_block]` container. [View all confirmed values in Engine_Graphics.md](./Engine_Graphics.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[graphic_block]`](./Engine_Graphics.md#all-confirmed-graphic-block-values) | Block | A visual/animation configuration. See Engine_Graphics.md for the full schema. |
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
| [`rocket_swirl`](./Abilities_and_Spells.md#context-rocket_swirl) | Block | Visual parameters for swirling projectile paths. | 4 |
| `sync_frames` | Number |  | 4 |
| [`dash_decelerating_animation`](./Enums.md#enum-dash_decelerating_animation) | Enum |  | 3 |
| `decelerate` | Number | Visual slowdown at the end of a movement. | 3 |
| `delay_from_map_edge` | Boolean | Delays effect based on distance from the screen edge. | 3 |
| `easing` | Number | Smoothing function for movement animations. | 3 |
| [`fixed_jump_speed`](./Enums.md#enum-fixed_jump_speed) | Enum |  | 3 |
| [`grab_animation`](./Enums.md#enum-grab_animation) | Enum |  | 3 |
| [`lob_yoff`](./Enums.md#enum-lob_yoff) | Enum | Adjustments for arcing projectiles. | 3 |
| `lock_orientation_during_dash` | Boolean | Prevents the sprite from flipping mid-dash. | 3 |
| `use_projectile_spawn_offset` | Boolean |  | 3 |
| `use_rotation_once` | Boolean |  | 3 |
| `always_play_animations` | Boolean | Bypasses speed-up/skip logic. | 2 |
| `detatched_animation_cutoff` | Boolean |  | 2 |
| `do_damage_immediately` | Boolean | Applies math before the animation actually hits. | 2 |
| `jump_height_multiplier` | Number | Overrides for jump physics. | 2 |
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
| [`animate_name`](./Enums.md#enum-animate_name) | Enum | Animates the ability name text on cast. | 1 |
| `apex_distance` | Number | Calculations for the peak of a jump/lob arc. | 1 |
| [`apex_time`](./Enums.md#enum-apex_time) | Enum | Calculations for the peak of a jump/lob arc. | 1 |
| `bypass_combatspeed` | Boolean |  | 1 |
| [`damage_threshold_altanimations`](./Abilities_and_Spells.md#context-damage_threshold_altanimations) | Block | Triggers different hit animations based on the amount of damage dealt. | 1 |
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

### Context: `effects` (2012 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](./Abilities_and_Spells.md#context-dodamage), [`MeleeRevengeDamage`](./Abilities_and_Spells.md#context-meleerevengedamage), [`ROOT`](./Abilities_and_Spells.md#context-root), [`RevengeDamage`](./Abilities_and_Spells.md#context-revengedamage), [`bonk_damage`](./Abilities_and_Spells.md#context-bonk_damage), [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance), [`empty_self_damage`](./Abilities_and_Spells.md#context-empty_self_damage), [`self_damage`](./Abilities_and_Spells.md#context-self_damage), [`splash_damage`](./Abilities_and_Spells.md#context-splash_damage)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 59 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 27 |
| [`Consumed`](./Abilities_and_Spells.md#context-consumed) | Block | State block triggered when this object or entity is eaten/consumed by another character. | 15 |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 13 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill) | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 11 |
| [`ApplyPassives`](./Abilities_and_Spells.md#context-applypassives) | Block | Grants the nested passive abilities dynamically. | 9 |
| [`ApplyStatusIfCrit`](./Abilities_and_Spells.md#context-applystatusifcrit) | Block | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. | 7 |
| [`TakeBonusTurnWithStatus`](./Abilities_and_Spells.md#context-takebonusturnwithstatus) | Block | Grants the character an immediate extra turn while afflicted with specific statuses. | 4 |
| [`TakeBonusTurnWithAIControl`](./Abilities_and_Spells.md#context-takebonusturnwithaicontrol) | Block | Grants the character an immediate extra turn, but forces the AI to control them during it. | 2 |
| [`Conditional_HasCleansableDebuffs`](./Abilities_and_Spells.md#context-conditional_hascleansabledebuffs) | Block | Conditional trigger: Executes nested logic if the target currently has negative status effects that can be cleansed. | 1 |
| [`CreateGlobalModifiers`](./Abilities_and_Spells.md#context-createglobalmodifiers) | Block | Generates global map or encounter rules/modifiers. | 1 |
| [`StatusGroup`](./Abilities_and_Spells.md#context-statusgroup) | Block | Groups multiple status effects together for batch application. | 1 |

</details>

---

### Context: `target` (1862 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_range` | Number | The maximum and minimum distance required to cast. | 1088 |
| `max_aoe` | Number | The maximum and minimum radius/length of the AoE. | 795 |
| `min_range` | Number | The maximum and minimum distance required to cast. | 583 |
| [`target_mode`](./Enums.md#enum-target_mode) | Enum | How the cursor operates (`tile`, `direction`, `none`). | 503 |
| [`restrictions`](./Arrays.md#array-restrictions) | Array | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). | 463 |
| [`aoe_mode`](./Enums.md#enum-aoe_mode) | Enum | The shape of the area (`standard`, `line`, `cross`, `square`, `custom`). | 432 |
| [`knockback_mode`](./Enums.md#enum-knockback_mode) | Enum | How physics vectors apply (`character_to_tile`, `pull_to_character`, `zero`, `orientation`). | 265 |
| `min_aoe` | Number | The maximum and minimum radius/length of the AoE. | 253 |
| `aoe_excludes_self` | Boolean | Prevents the AoE from hitting the caster. | 241 |
| [`aoe_restrictions`](./Arrays.md#array-aoe_restrictions) | Array | Array of conditions the AoE tiles must meet (e.g., `must_have_line_of_sight_unpurgable`). | 197 |
| `aoe_considers_character_size` | Boolean | Scales the AoE based on the caster's tile size (e.g., 2x2). | 170 |
| [`range_mode`](./Enums.md#enum-range_mode) | Enum | How range is counted (`standard`, `ground_move`). | 114 |
| [`X_is`](./Enums.md#enum-x_is) | Enum | Applies or references the 'X_is' effect/state. | 86 |
| [`custom_aoe`](./Arrays.md#array-custom_aoe) | Array | Array of exact coordinates for a custom shape (e.g., `[[1, -1] [1, 0]]`). | 83 |
| `multihit` | Number | Hardcoded number of times the ability hits the target. | 62 |
| `max_targets` | Number | Limits on how many distinct entities can be targeted. | 56 |
| `range_excludes_blocking` | Boolean | Cannot target through walls/obstacles. | 53 |
| `prioritize_dont_change_direction` | Number | AI preference to maintain current facing angle. | 52 |
| [`target_requires_tag`](./Enums.md#enum-target_requires_tag) | Enum | Target must possess this exact character tag. | 40 |
| [`aoe_symmetry`](./Enums.md#enum-aoe_symmetry) | Enum | Determines if the AoE mirrors on axes. | 28 |
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
| [`toss_direction_restriction`](./Enums.md#enum-toss_direction_restriction) | Enum | Limits which ways an entity can be tossed. | 6 |
| `aoe_hint_teamcast` | Boolean | Visual hint for cooperative casting abilities. | 5 |
| [`aoe_tile_requires_element`](./Enums.md#enum-aoe_tile_requires_element) | Enum | Only affects tiles painted with a specific element. | 5 |
| `distance_sort_targets` | Number | Prioritizes targets based on proximity. | 5 |
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
| `low_health_character_threshold` | Number | AI targeting threshold for seeking weak targets. | 3 |
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
| `force_no_contact` | Boolean | Bypasses all contact-based retaliation (Thorns, etc). | 1 |
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

</details>

---

### Context: `cost` (1851 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `mana` | Number | MP pool and how much it restores per turn. | 1603 |
| `infcantrip` | Boolean | Can be cast infinitely as long as costs are met. | 810 |
| `cantrip` | Boolean | Does not end the turn when cast. | 560 |
| `once_per_fight` | Boolean | Exhausts for the remainder of combat after one use. | 98 |
| `act_points` | Number | Consumes primary action points (default 1). | 86 |
| `move_points` | Number | Consumes movement points. | 59 |
| `prime` | Number | Requires a "priming" turn before it fires. | 30 |
| `allow_offmap_casts` | Boolean | Can be used while the character is hidden/removed from grid. | 22 |
| `cant_cast` | Boolean | Explicitly disables casting (used for passive-triggered only abilities). | 18 |
| `must_be_consuming` | Boolean | Requires the character to be eating/holding something. | 17 |
| `charge` | Number | Cooldown timers measured in turns. | 16 |
| `must_not_be_consuming` | Boolean | Cannot be holding/eating an entity. | 14 |
| `requires_reload` | Boolean | Must spend an action to reload before casting again. | 14 |
| `can_cast_while_dead` | Boolean | Usable by corpses (e.g., DeathRattle triggers). | 12 |
| [`cantrip_group`](./Enums.md#enum-cantrip_group) | Enum | Groups cantrips so using one exhausts the others. | 12 |
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
| [`enabled_formula`](./Math_Equations.md) | Equation | Mathematical string required to be >0 to cast. | 3 |
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

### Context: `self_damage` (220 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#context-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#context-root)

> **Engine Schema:** This block is a `[damage_instance]` container. [View all confirmed values in Engine_Damage.md](./Engine_Damage.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[damage_instance]`](./Engine_Damage.md#all-confirmed-damage-instance-values) | Block | A damage hit definition. See Engine_Damage.md for the full schema. |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 200 |
| `damage` | Number | The base damage properties of an attack. | 47 |
| `piercing` | Boolean |  | 12 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 11 |
| `cant_miss` | Boolean |  | 10 |
| `knockback` | Number |  | 10 |
| `heal` | Number |  | 6 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 4 |
| `ai_base_score` | Number |  | 2 |
| `non_lethal` | Boolean |  | 1 |

</details>

---

### Context: `spawn` (192 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 184 |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 59 |
| `ai_base_score` | Number |  | 31 |
| [`additional_passives`](./Abilities_and_Spells.md#context-additional_passives) | Block | Passives granted intrinsically to a spawned entity. | 20 |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum |  | 17 |
| [`layer`](./Enums.md#enum-layer) | Enum |  | 14 |
| [`catdata`](./Enums.md#enum-catdata) | Enum | Defines genetic/clone data cloning. | 13 |
| `clone_items` | Boolean | If true, transfers inventory to the clone. | 12 |
| `lob` | Boolean |  | 4 |
| [`post_spawn_statuses`](./Abilities_and_Spells.md#context-post_spawn_statuses) | Block | Status effects applied immediately after an entity spawns. | 4 |
| `size` | Number |  | 4 |
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

### Context: `bonus_passives` (136 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`AddStatusToBasicAttack`](./Abilities_and_Spells.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 1 |
| [`RevengeDamage`](./Abilities_and_Spells.md#context-revengedamage) | Block | Reaction trigger: Deals damage to the attacker when hit. | 1 |
| [`StatusKillers`](./Abilities_and_Spells.md#context-statuskillers) | Block | Instantly kills the target if they possess the specified status effects. | 1 |

</details>

---

### Context: `temporary_effects` (88 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Trample` | Number | Applies or references the 'Trample' effect/state. | 26 |
| `CastAgain` | Number | Applies or references the 'CastAgain' effect/state. | 20 |
| `DisableTrample` | Number | Applies or references the 'DisableTrample' effect/state. | 10 |
| `Fury` | Number | Applies or references the 'Fury' effect/state. | 7 |
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum | Applies or references the 'TileTrail' effect/state. | 6 |
| `JustInCaseTrample` | Number | Applies or references the 'JustInCaseTrample' effect/state. | 5 |
| [`LeaveBehind`](./Enums.md#enum-leavebehind) | Enum | Spawns a specific object at the character's previous location when they move. | 5 |
| `DashFury` | Number | Applies or references the 'DashFury' effect/state. | 3 |
| [`AfterImage`](./Abilities_and_Spells.md#context-afterimage) | Block | Spawns a visual decoy or shade at the caster's previous location. | 2 |
| `BearTrapTrail` | Number | Applies or references the 'BearTrapTrail' effect/state. | 2 |
| `DelayedWindTrail` | Number | Applies or references the 'DelayedWindTrail' effect/state. | 1 |
| `DoubleLoot` | Number | Applies or references the 'DoubleLoot' effect/state. | 1 |
| [`JumpAttackLeaveBehind`](./Enums.md#enum-jumpattackleavebehind) | Enum | Applies or references the 'JumpAttackLeaveBehind' effect/state. | 1 |
| `KnockbackImmunity` | Number | Applies or references the 'KnockbackImmunity' effect/state. | 1 |
| [`TileTrail_Ahead`](./Enums.md#enum-tiletrail_ahead) | Enum | Applies or references the 'TileTrail_Ahead' effect/state. | 1 |

</details>

---

### Context: `Else` (71 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object), [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 |
| [`ApplyToRandomPartyMemberIfPossible`](./Abilities_and_Spells.md#context-applytorandompartymemberifpossible) | Block | Redirects the nested effects to apply to a random living member of the player's party. | 1 |
| [`Consumed`](./Abilities_and_Spells.md#context-consumed) | Block | State block triggered when this object or entity is eaten/consumed by another character. | 1 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `ApplyToSource` (51 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyStatusIfCrit`](./Abilities_and_Spells.md#context-applystatusifcrit), [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate), [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_GoodRoll`](./Abilities_and_Spells.md#context-conditional_goodroll), [`Conditional_HasStatus`](./Abilities_and_Spells.md#context-conditional_hasstatus), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#context-conditional_healththreshold), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#context-conditional_livingplayercat), [`Conditional_PlayerCat`](./Abilities_and_Spells.md#context-conditional_playercat), [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#context-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#context-else), [`Math`](./Abilities_and_Spells.md#context-math), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_HasTag` (42 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. | 41 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill) | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 2 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 2 |

</details>

---

### Context: `Temporary` (41 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate), [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_NotAlly`](./Abilities_and_Spells.md#context-conditional_notally), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
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

### Context: `sounds` (39 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ontrigger`](./Enums.md#enum-ontrigger) | Enum |  | 32 |
| [`oncast`](./Enums.md#enum-oncast) | Enum |  | 3 |
| [`oncastpoint`](./Enums.md#enum-oncastpoint) | Enum |  | 3 |
| [`ontrigger_intentional`](./Enums.md#enum-ontrigger_intentional) | Enum |  | 1 |

</details>

---

### Context: `Conditional_Enemy` (36 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Corpse`](./Abilities_and_Spells.md#context-conditional_corpse), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill) | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 1 |
| [`Conditional_FinishedSpawning`](./Abilities_and_Spells.md#context-conditional_finishedspawning) | Block | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. | 1 |

</details>

---

### Context: `splash_damage` (35 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#context-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#context-root)

> **Engine Schema:** This block is a `[damage_instance]` container. [View all confirmed values in Engine_Damage.md](./Engine_Damage.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[damage_instance]`](./Engine_Damage.md#all-confirmed-damage-instance-values) | Block | A damage hit definition. See Engine_Damage.md for the full schema. |
| `damage` | Number | The base damage properties of an attack. | 32 |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 17 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 13 |
| `knockback` | Number | Knockback force of the splash blast. | 13 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 12 |
| `makes_contact` | Boolean |  | 6 |
| `override_trample_damage` | Boolean |  | 2 |
| `ai_base_score` | Number |  | 1 |
| `crit_chance` | Number |  | 1 |
| `force_no_knockback` | Boolean |  | 1 |
| `force_play_hit_animation` | Boolean |  | 1 |
| [`layer`](./Enums.md#enum-layer) | Enum |  | 1 |

</details>

---

### Context: `Conditional_Ally` (25 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill) | Block | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 1 |

</details>

---

### Context: `keyword_tooltips` (23 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

> **Engine Schema:** This block is a `[keyword_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[keyword_id]`](./Engine_Statuses.md#all-confirmed-keyword-id-values) | String | A Status or Keyword ID whose tooltip text is defined here. See Engine_Statuses.md for all IDs. |

</details>

---

### Context: `KnockUpAndAway` (21 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Conditional_LastHit`](./Abilities_and_Spells.md#context-conditional_lasthit), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | The distance in tiles to knock the target away. | 20 |
| [`stacks`](./Math_Equations.md) | Equation | Number of stacks or intensity to apply. | 18 |
| `height` | Number |  | 2 |
| `circular_variance` | Number |  | 1 |

</details>

---

### Context: `additional_passives` (20 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#context-spawn)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |

</details>

---

### Context: `RandomStatusFromPool` (19 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyMultipleTimes`](./Abilities_and_Spells.md#context-applymultipletimes), [`Conditional_CanBeHealed`](./Abilities_and_Spells.md#context-conditional_canbehealed), [`Conditional_HasCleansableDebuffs`](./Abilities_and_Spells.md#context-conditional_hascleansabledebuffs), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `Consumed` (18 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#context-conditional_livingplayercat), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Ability triggered by the consumed entity while inside the consumer. | 13 |
| `force_contact` | Boolean | If true, enforces physical overlap. | 11 |
| `instant` | Boolean |  | 8 |
| [`mount_mode`](./Enums.md#enum-mount_mode) | Enum | If true, treats the consumption as riding/mounting instead of eating. | 8 |
| `wet` | Boolean |  | 8 |
| `do_not_pop_corpse` | Boolean |  | 7 |
| `drop_on_death` | Boolean |  | 7 |
| `drop_on_self_death` | Boolean |  | 3 |
| [`extra_statuses`](./Abilities_and_Spells.md#context-extra_statuses) | Block | Additional generic status applications. | 3 |
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum |  | 1 |
| `kill_on_consume` | Boolean |  | 1 |
| `use_placeholder` | Boolean |  | 1 |

</details>

---

### Context: `Conditional_Boss` (17 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 4 |

</details>

---

### Context: `ApplyToSourceOnKill` (15 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `CanApplyToInanimate` (15 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum | Spawns a specific character or entity upon impact. | 10 |
| [`BreakIntoRocks`](./Enums.md#enum-breakintorocks) | Enum | Applies or references the 'BreakIntoRocks' effect/state. | 4 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 3 |
| `GetAggroTarget` | Number | Applies or references the 'GetAggroTarget' effect/state. | 2 |
| `PreventDeathTransforms` | Number | Applies or references the 'PreventDeathTransforms' effect/state. | 1 |
| [`Temporary`](./Abilities_and_Spells.md#context-temporary) | Block | A wrapper block for applying status effects that automatically expire. | 1 |

</details>

---

### Context: `CatPartsTransform` (14 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
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

### Context: `Conditional_NotBoss` (14 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |

</details>

---

### Context: `FormChange` (14 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form`](./Strings.md#string-form) | String |  | 75 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Context: `Conditional_HasStatus` (13 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 13 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |

</details>

---

### Context: `EvolveAbilityFromPool` (13 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 13 |
| `upgraded` | Boolean |  | 13 |

</details>

---

### Context: `Conditional_GoodRoll` (12 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 12 |
| [`ApplyToRandomPartyMemberIfPossible`](./Abilities_and_Spells.md#context-applytorandompartymemberifpossible) | Block | Redirects the nested effects to apply to a random living member of the player's party. | 1 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |

</details>

---

### Context: `Conditional_Speculative` (12 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_AffectedByElement`](./Abilities_and_Spells.md#context-conditional_affectedbyelement), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |

</details>

---

### Context: `DoScreenShake` (12 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `intensity` | Number |  | 10 |
| `time` | Number |  | 10 |

</details>

---

### Context: `ChanceToBreakFree` (11 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ability triggered upon successfully breaking free. | 11 |
| [`fail_ability`](./Enums.md#enum-fail_ability) | Enum | The ability triggered if the break free attempt fails. | 3 |
| `stacks` | Number | Percentage base chance to break free. | 3 |

</details>

---

### Context: `ChangeTile` (11 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tile`](./Enums.md#enum-tile) | Enum | The specific tile type to change into (e.g., GlassTile). | 11 |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |
| `aoe` | Number |  | 1 |

</details>

---

### Context: `ApplyPassives` (10 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_RandomChance`](./Abilities_and_Spells.md#context-conditional_randomchance), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`StatusOnBattleEnd`](./Abilities_and_Spells.md#context-statusonbattleend) | Block | Applies the nested status effects when the encounter finishes. | 3 |

</details>

---

### Context: `Conditional_FormulaIsPositive` (10 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`formula`](./Math_Equations.md) | Equation | The math expression to evaluate. | 8 |

</details>

---

### Context: `Craft` (9 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 9 |
| [`slot`](./Enums.md#enum-slot) | Enum |  | 8 |
| `temporary` | Boolean |  | 4 |
| `works_with_tech` | Boolean |  | 1 |

</details>

---

### Context: `ApplyStatusIfCrit` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 6 |

</details>

---

### Context: `Conditional_Corpse` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |

</details>

---

### Context: `Conditional_InForm` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`form`](./Enums.md#enum-form) | Enum | The specific form ID to check for. | 7 |

</details>

---

### Context: `Conditional_HealthThreshold` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| `threshold_flat` | Number | A flat numerical health value threshold. | 4 |
| `threshold_percent` | Number | A percentage-based health threshold (e.g. 50%). | 2 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`threshold_expr`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `Conditional_Object` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 3 |

</details>

---

### Context: `Conditional_PlayerCat` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |

</details>

---

### Context: `DoDistortionRing` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `intensity` | Number |  | 6 |
| `radius` | Number | Distance or area of effect in tiles. | 6 |
| `speed` | Number |  | 6 |

</details>

---

### Context: `SwitchMusic` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | The specific audio layer to transition to (e.g., map, battle). | 6 |
| [`new_song`](./Enums.md#enum-new_song) | Enum | The ID of the new music track. | 5 |
| `crossfade_speed` | Number |  | 1 |

</details>

---

### Context: `TwisterDisplaceWithDamage` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The damage formula or inherit flag. | 6 |
| `max_dist` | Number | Maximum displacement distance. | 6 |
| `min_dist` | Number | Minimum displacement distance. | 2 |
| [`exclude_prefix`](./Enums.md#enum-exclude_prefix) | Enum |  | 1 |

</details>

---

### Context: `CollectsPickupsWithAltEffects` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | Applies or references the 'Tech' effect/state. | 2 |
| `CurrentWeaponAddPoison` | Number | Applies or references the 'CurrentWeaponAddPoison' effect/state. | 1 |
| `LuckUp` | Number | Applies or references the 'LuckUp' effect/state. | 1 |
| `Quivered` | Number | Applies or references the 'Quivered' effect/state. | 1 |
| `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. | 1 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 1 |

</details>

---

### Context: `DestroyEquipmentAndAttachParasite` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_ActiveWeather_Any`](./Abilities_and_Spells.md#context-conditional_activeweather_any), [`Conditional_DebuffRoll`](./Abilities_and_Spells.md#context-conditional_debuffroll), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | The item pool to draw the parasite from. | 5 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 3 |

</details>

---

### Context: `DoDamage` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Else`](./Abilities_and_Spells.md#context-else), [`post_spawn_statuses`](./Abilities_and_Spells.md#context-post_spawn_statuses)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The flat damage amount. | 5 |
| [`type`](./Enums.md#enum-type) | Enum | The classification of the damage (e.g., spell, melee). | 5 |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum |  | 2 |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |

</details>

---

### Context: `ApplyToConsumed` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DeleteObject` | Number | Applies or references the 'DeleteObject' effect/state. | 3 |
| `Die` | Number | Applies or references the 'Die' effect/state. | 1 |

</details>

---

### Context: `ArcLightning` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, the arc will not bounce to friendly targets. | 4 |
| `max_distance` | Number | The maximum tile range the lightning can jump between bounces. | 4 |
| `stacks` | Number | The maximum number of targets the lightning can bounce to. | 4 |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| `ignore_self` | Boolean | If true, prevents the arc from bouncing back to the caster. | 1 |

</details>

---

### Context: `BackflipWhenTargeted` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific dodge ability to trigger (e.g., DestroyerDodge). | 4 |
| `stacks` | Number | Number of stacks or intensity to apply. | 4 |

</details>

---

### Context: `Conditional_Familiar` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `GainCoinsRange` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number | Maximum coins granted. | 4 |
| `min` | Number | Minimum coins granted. | 4 |

</details>

---

### Context: `LateStatusApplication` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CurrentWeaponDamageUp` | Number | Applies or references the 'CurrentWeaponDamageUp' effect/state. | 3 |
| `AddWeaponAux` | Number | Applies or references the 'AddWeaponAux' effect/state. | 1 |

</details>

---

### Context: `LeaveBehind` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID to spawn. | 4 |

</details>

---

### Context: `ReplaceSpell` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#context-temppassivewhilehasstatus)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The new ability ID to insert. | 4 |
| `slot` | Number | The spell slot index to replace. | 4 |

</details>

---

### Context: `TakeBonusTurnWithStatus` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `TempPassiveWhileHasStatus` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_FirstApplicationThisTurn`](./Abilities_and_Spells.md#context-conditional_firstapplicationthisturn), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#context-conditional_livingplayercat)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ReplaceSpell`](./Abilities_and_Spells.md#context-replacespell) | Block | Replaces a spell in the character's hand/deck with a different one. | 4 |
| [`status`](./Enums.md#enum-status) | Enum | The required status effect. | 3 |
| [`MeleeRevengeDamage`](./Abilities_and_Spells.md#context-meleerevengedamage) | Block | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. | 2 |
| `AddManaRegen` | Number | Applies or references the 'AddManaRegen' effect/state. | 1 |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 1 |

</details>

---

### Context: `TimeDelayStatusApplication` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`delay`](./Enums.md#enum-delay) | Enum | The float time delay in seconds. | 4 |
| [`SwitchMusic`](./Abilities_and_Spells.md#context-switchmusic) | Block | Changes the background music track or layer during combat. | 2 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 1 |
| [`CreateGlobalModifiers`](./Abilities_and_Spells.md#context-createglobalmodifiers) | Block | Generates global map or encounter rules/modifiers. | 1 |
| [`DoScreenShake`](./Abilities_and_Spells.md#context-doscreenshake) | Block | Triggers a camera screen shake effect. | 1 |
| [`FormChange`](./Enums.md#enum-formchange) | Enum | Transforms the character into a different state or form (e.g., Rage, HasCat). | 1 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 1 |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | Applies or references the 'GlobalSpawnCharacter' effect/state. | 1 |
| `PlayBackground` | Number | Applies or references the 'PlayBackground' effect/state. | 1 |
| [`RemoveAmbientLightEffects`](./Enums.md#enum-removeambientlighteffects) | Enum | Applies or references the 'RemoveAmbientLightEffects' effect/state. | 1 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 1 |

</details>

---

### Context: `post_spawn_statuses` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#context-spawn)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DoDamage`](./Abilities_and_Spells.md#context-dodamage) | Block | Explicitly triggers a secondary damage instance independent of the main attack. | 2 |
| [`EnterMount`](./Enums.md#enum-entermount) | Enum | Applies or references the 'EnterMount' effect/state. | 1 |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum | Applies or references the 'VisualFXTile' effect/state. | 1 |

</details>

---

### Context: `rocket_swirl` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`radius`](./Arrays.md#array-radius) | Array | Swirl radius. | 4 |
| [`speed`](./Arrays.md#array-speed) | Array | Rotations per second. | 4 |

</details>

---

### Context: `ApplyMultipleTimes` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 3 |
| [`stacks`](./Math_Equations.md) | Equation | The number of times the nested effects block should be repeatedly executed. | 3 |

</details>

---

### Context: `BounceObject` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`obj`](./Enums.md#enum-obj) | Enum | The entity ID of the object to spawn (e.g., chapter_corpse_medium). | 3 |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0) of spawning the object. | 2 |
| `slide` | Number |  | 1 |

</details>

---

### Context: `CatPartsSizeScaleStatus` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `arm1` | Number | Scale multiplier for the front arm. | 1 |
| `arm2` | Number | Scale multiplier for the back arm. | 1 |
| `body` | Number |  | 1 |
| `mouth` | Number |  | 1 |

</details>

---

### Context: `Conditional_AffectedByElement` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type to check for. | 3 |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. | 3 |

</details>

---

### Context: `Conditional_LastHit` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `DustOnHit` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The ID of the object/particle to spawn. | 3 |

</details>

---

### Context: `IncAuxCounterClamped` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `change` | Number |  | 3 |
| `max` | Number |  | 3 |

</details>

---

### Context: `SetCrazyEyeBackgroundWeights` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Arrays.md#array-weights) | Array |  | 3 |

</details>

---

### Context: `StatusOnBattleEnd` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./Abilities_and_Spells.md#context-applypassives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 3 |

</details>

---

### Context: `extra_statuses` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Consumed`](./Abilities_and_Spells.md#context-consumed)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `AddStatusToBasicAttack` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhileNotTakingTurn`](./Abilities_and_Spells.md#context-passivewhilenottakingturn), [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `AfterImage` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#context-temporary_effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the visual decoy to spawn (e.g., PlayerCat_ThiefShade). | 2 |
| `skilltemp` | Boolean | If true, the decoy is automatically destroyed once the skill finishes executing. | 2 |

</details>

---

### Context: `ApplyToRandomPartyMemberIfPossible` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./Abilities_and_Spells.md#context-conditional_goodroll), [`Else`](./Abilities_and_Spells.md#context-else)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `ApplyToTile` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_DestructibleCorpse`](./Abilities_and_Spells.md#context-conditional_destructiblecorpse)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHit`](./Enums.md#enum-objectonhit) | Enum | Spawns a specific physics/item object upon impact. | 2 |
| `SpawnBearTrap` | Number | Applies or references the 'SpawnBearTrap' effect/state. | 2 |

</details>

---

### Context: `AutocastEachRound` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 2 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 1 |

</details>

---

### Context: `BodyGuard` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to use when intercepting (e.g., BodyGuardSwap). | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `Conditional_BadRoll` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`odds`](./Enums.md#enum-odds) | Enum | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 2 |

</details>

---

### Context: `Conditional_BossOrBig` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_Buddy` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |
| [`Consumed`](./Abilities_and_Spells.md#context-consumed) | Block | State block triggered when this object or entity is eaten/consumed by another character. | 1 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 1 |

</details>

---

### Context: `Conditional_DestructibleCorpse` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_Displaceable` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_IsSelf` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_NotAlly` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_NotBossOrBig` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_NotShielded` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_OncePerBattle` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`key`](./Enums.md#enum-key) | Enum |  | 2 |

</details>

---

### Context: `Conditional_Shielded` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `ConjureBonusAbility` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to conjure. | 2 |
| `upgraded` | Boolean | If true, conjures the upgraded version of the ability. | 2 |

</details>

---

### Context: `CreateGlobalModifiers` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[global_modifier_id]` container. [View all confirmed values in Engine_GlobalModifiers.md](./Engine_GlobalModifiers.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[global_modifier_id]`](./Engine_GlobalModifiers.md#all-confirmed-global-modifier-id-values) | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |

</details>

---

### Context: `FindItemFromPool` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability of finding the item. | 2 |
| [`pool`](./Enums.md#enum-pool) | Enum | The item pool to draw from. | 1 |

</details>

---

### Context: `ForceAttack` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `immediate` | Boolean |  | 2 |

</details>

---

### Context: `ForceMoveTowardsTaggedObject` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The movement ability to use. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | The entity tag to seek out. | 1 |

</details>

---

### Context: `LowerAmbientLight` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CreateGlobalModifiers`](./Abilities_and_Spells.md#context-createglobalmodifiers)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array | The target opacity/dimness level. | 2 |
| `speed` | Number | The transition speed. | 2 |

</details>

---

### Context: `Math` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Stun` | Number | Applies or references the 'Stun' effect/state. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |

</details>

---

### Context: `MeleeRevengeDamage` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#context-temppassivewhilehasstatus)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |

</details>

---

### Context: `NukeQuestFinalBossModifications` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`self_damage`](./Abilities_and_Spells.md#context-self_damage) | Block | Recoil or self-inflicted damage/effects applied to the caster. | 2 |
| [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance) | Block |  | 1 |
| [`splash_damage`](./Abilities_and_Spells.md#context-splash_damage) | Block | Secondary Area of Effect blast parameters. | 1 |

</details>

---

### Context: `ObjectOnHit` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the object to spawn (e.g., Poop). | 2 |

</details>

---

### Context: `ObjectOnHitCharacter` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0) of spawning. | 2 |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the character to spawn (e.g., CharmedFlea). | 2 |

</details>

---

### Context: `OverHealToStatuses` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. | 1 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 1 |
| `stack_scale` | Number |  | 1 |

</details>

---

### Context: `QuakeAreaChance` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability of triggering the quake. | 2 |
| `radius` | Number | The tile radius of the quake. | 2 |

</details>

---

### Context: `RandomKnockback` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number | Maximum knockback distance. | 2 |
| `min` | Number | Minimum knockback distance. | 2 |

</details>

---

### Context: `RandomMagicMissile` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `full_size` | Boolean | If true, fires normal sized missiles instead of mini ones. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `ScatterCoins` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#context-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stackable` | Boolean | If true, multiple instances of this trigger can stack. | 2 |
| [`stacks`](./Math_Equations.md) | Equation | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `TakeBonusTurnWithAIControl` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| `include_spells` | Boolean | If true, allows the AI to cast spells during this bonus turn. | 2 |

</details>

---

### Context: `TeamCastAbility` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The underlying logic ability executed by the team. | 2 |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum | Requires participants to share this tag. | 2 |
| `same_orientation` | Boolean |  | 1 |

</details>

---

### Context: `XIsTargetHealth` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`BonusDamage`](./Math_Equations.md) | Equation | Applies or references the 'BonusDamage' effect/state. | 2 |

</details>

---

### Context: `empty_self_damage` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 2 |

</details>

---

### Context: `AlphaStatusOnTurnBegin` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DoubleCastSpellThisTurn` | Number | Applies or references the 'DoubleCastSpellThisTurn' effect/state. | 1 |

</details>

---

### Context: `ApplyPassivesToSpawnerWhileAlive` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#context-additional_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum | Applies or references the 'HideEquipment' effect/state. | 1 |

</details>

---

### Context: `ApplyStatusesNextTurnBegin` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | Applies or references the 'Quivered' effect/state. | 1 |

</details>

---

### Context: `ApplyToOthersWithSharedTagAndFaction` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Marked` | Number | Applies or references the 'Marked' effect/state. | 1 |

</details>

---

### Context: `ApplyToRandomClosestAlly` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | Number | Applies or references the 'ForceMoveTowards' effect/state. | 1 |

</details>

---

### Context: `Cleave` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0) that the cleave effect triggers. | 1 |

</details>

---

### Context: `Conditional_ActiveWeather_Any` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. | 1 |

</details>

---

### Context: `Conditional_Backstab` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_CanBeHealed` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `Conditional_DebuffRoll` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| `odds` | Number | The probability (0.0 to 1.0) of applying the debuff. | 1 |

</details>

---

### Context: `Conditional_FinishedSpawning` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Imprison`](./Enums.md#enum-imprison) | Enum | Applies or references the 'Imprison' effect/state. | 1 |

</details>

---

### Context: `Conditional_HasCleansableDebuffs` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GenericBuff` | Number | Applies or references the 'GenericBuff' effect/state. | 1 |
| `PartialCleanse` | Number | Applies or references the 'PartialCleanse' effect/state. | 1 |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `Conditional_IsTrample` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_LivingPlayerCat` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`Consumed`](./Abilities_and_Spells.md#context-consumed) | Block | State block triggered when this object or entity is eaten/consumed by another character. | 1 |

</details>

---

### Context: `Conditional_NotBig` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_RandomChance` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`ApplyPassives`](./Abilities_and_Spells.md#context-applypassives) | Block | Grants the nested passive abilities dynamically. | 1 |
| `odds` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

### Context: `Conditional_SourceAbilityHasTag` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 1 |

</details>

---

### Context: `Conditional_SourceHasStatus` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |

</details>

---

### Context: `CopySpells` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |
| `upgraded` | Boolean |  | 1 |

</details>

---

### Context: `DelayCastAbility` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to cast later. | 1 |
| `lingering` | Boolean |  | 1 |
| `relative` | Boolean |  | 1 |

</details>

---

### Context: `DelayedWindCone` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| `distance` | Number | Distance or area of effect in tiles. | 1 |

</details>

---

### Context: `DybbukPossessed` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum |  | 1 |
| [`punch_self_ability`](./Enums.md#enum-punch_self_ability) | Enum |  | 1 |

</details>

---

### Context: `ForceImmediateMoveAndAttack` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_InForm`](./Abilities_and_Spells.md#context-conditional_inform)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ability to execute after moving. | 1 |
| `even_if_cant_reach` | Boolean | If true, executes the attack even if the move fails to reach the target. | 1 |

</details>

---

### Context: `IncAuxCounterCycle` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `change` | Number |  | 1 |
| `max` | Number |  | 1 |

</details>

---

### Context: `KnockOutCoin` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `Madness` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |
| `tickdown_this_turn` | Boolean |  | 1 |

</details>

---

### Context: `MergeDamageInstance` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `can_instapop` | Boolean | If false, prevents the damage from instantly popping the target. | 1 |
| `force_no_hit_animation` | Boolean | If true, suppresses the flinch/hit animation. | 1 |

</details>

---

### Context: `Metronome` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`banned_abilities`](./Arrays.md#array-banned_abilities) | Array |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `NextAttackSpecialCrit` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Number | Flat addition to the critical damage multiplier. | 1 |
| `extra_coins_per_stack` | Number | Grants bonus coins based on stacks. | 1 |
| `luck_increase` | Number | Increases luck stat for the attack. | 1 |

</details>

---

### Context: `NextBasicAttackCritsThisTurn` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | If true, ensures the attack cannot be dodged. | 1 |
| `piercing` | Boolean | If true, the attack ignores armor. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `NextBattleStatusStacks` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | Number | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. | 1 |
| `fights` | Number | The number of encounters this buff/debuff persists for. | 1 |

</details>

---

### Context: `PassiveWhileNotTakingTurn` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Abilities_and_Spells.md#context-addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. | 1 |

</details>

---

### Context: `PoolMetronome` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | An array of ability IDs to randomly choose from. | 1 |

</details>

---

### Context: `PopAndSpawn` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID to spawn in place. | 2 |
| `clone_items` | Boolean | If true, transfers inventory to the new entity. | 1 |
| `clone_referenced_catdata` | Boolean | If true, copies the genetic data of the popped cat. | 1 |
| `no_splatter` | Boolean |  | 1 |

</details>

---

### Context: `RandomDistanceDisplace` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `min_dist` | Number | The minimum tile distance they will be moved. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `RemoveStatusStacks` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks to remove. | 1 |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 1 |

</details>

---

### Context: `RevengeDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |

</details>

---

### Context: `ReviveNextRound` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#context-additional_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `revive_health` | Number | The flat amount of health to revive with. | 3 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 2 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 1 |

</details>

---

### Context: `ScrambleLastUsedSpell` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `permanent` | Boolean | If true, the scramble persists for the rest of the run. | 1 |

</details>

---

### Context: `SetAnimationAlts` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dead`](./Enums.md#enum-dead) | Enum |  | 1 |
| [`dying`](./Enums.md#enum-dying) | Enum |  | 1 |

</details>

---

### Context: `ShowFakeDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |
| [`style`](./Arrays.md#array-style) | Array | The visual font style for the text (e.g., [crit]). | 1 |

</details>

---

### Context: `SmartMetronome` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |
| `upgraded` | Boolean |  | 1 |

</details>

---

### Context: `SpreadDisease` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of transmitting. | 1 |
| [`disease`](./Enums.md#enum-disease) | Enum | The specific status effect ID representing the disease. | 1 |

</details>

---

### Context: `StatusGroup` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusKillers` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `SwapWeapon` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | An array of weapon item IDs to draw from. | 1 |

</details>

---

### Context: `Tangled` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_art`](./Enums.md#enum-alt_art) | Enum | The alternative sprite art to use while tangled. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `TransformEquipment` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | The original item ID. | 1 |
| [`to`](./Enums.md#enum-to) | Enum | The new item ID. | 1 |

</details>

---

### Context: `TransformWeapon` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | The original weapon ID. | 1 |
| [`to`](./Enums.md#enum-to) | Enum | The transformed weapon ID. | 1 |

</details>

---

### Context: `UseAbility` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger. | 1 |
| `respect_prime` | Boolean | If true, respects the ability's prime/cooldown state. | 1 |

</details>

---

### Context: `UseMoveAbilityWithAI` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | The AI positioning logic profile to use. | 1 |

</details>

---

### Context: `VisualCountDownThenApplyStatus` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | Applies or references the 'ForceUseAbility' effect/state. | 1 |

</details>

---

### Context: `WaggleClone` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`1x1_object`](./Enums.md#enum-1x1_object) | Enum | The 1x1 variant of the object. | 1 |
| [`2x2_object`](./Enums.md#enum-2x2_object) | Enum | The 2x2 variant of the object. | 1 |
| [`3x3_object`](./Enums.md#enum-3x3_object) | Enum | The 3x3 variant of the object. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `XIsSpellStormRampAndReset` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reset_percent` | Number | The percentage of stacks to keep after resetting. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `bonk_damage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

> **Engine Schema:** This block is a `[damage_instance]` container. [View all confirmed values in Engine_Damage.md](./Engine_Damage.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[damage_instance]`](./Engine_Damage.md#all-confirmed-damage-instance-values) | Block | A damage hit definition. See Engine_Damage.md for the full schema. |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | Non-damaging status applications and logic triggers executed on impact. | 1 |

</details>

---

### Context: `damage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 1 |

</details>

---

### Context: `damage_threshold_altanimations` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `heaviestMelee` | Number | Animation trigger for massive damage. | 1 |
| `heavyMelee` | Number | Animation trigger if damage exceeds this threshold. | 1 |

</details>

---

