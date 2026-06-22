# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Abilities & Spells

> **Associated Files:** `data/abilities/, data/ability_templates/`


### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2343

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance) | Block | {'type': '`Block`', 'df': 'Block defining the combat math and status effects applied upon successful hit. | 2343 |
| [`meta`](./Abilities_and_Spells.md#context-meta) | Block | {'type': '`Block`', 'df': 'Block defining UI display data (Name, Description, Icon). | 2333 |
| [`template`](./Enums.md#enum-template) | Enum | {'type': '`Enum/String`', 'df': 'Inherits baseline internal logic from a hardcoded engine template.'} | 2174 |
| [`graphics`](./Abilities_and_Spells.md#context-graphics) | Block | {'type': '`Block`', 'df': 'Block defining visual animations and sequence timings. | 2037 |
| [`target`](./Abilities_and_Spells.md#context-target) | Block | {'type': '`Block`', 'df': "Block defining the shape, range, and restrictions of the ability's aiming phase. | 1862 |
| [`cost`](./Abilities_and_Spells.md#context-cost) | Block | {'type': '`Block`', 'df': 'Block defining resource requirements (Mana, Act Points, Moves) needed to cast. | 1851 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum | {'type': '`Enum/String`', 'df': 'Inherits properties from a previously defined ability (used for upgrading tiers).'} | 900 |
| [`tags`](./Arrays.md#array-tags) | Array | {'type': '`Array`', 'df': 'Array of string categories used by the engine for filtering (e.g. [weapon_throw, spell]).'} | 238 |
| [`self_damage`](./Abilities_and_Spells.md#context-self_damage) | Block | {'type': '`Block`', 'df': 'Recoil or self-inflicted damage/effects applied to the caster. | 218 |
| [`spawn`](./Abilities_and_Spells.md#context-spawn) | Block | {'type': '`Block`', 'df': 'Parameters for summoning new characters, objects, or entities. | 192 |
| [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives) | Block | {'type': '`Block`', 'df': "Passives granted to the character while this ability is equipped. | 136 |
| [`class`](./Enums.md#enum-class) | Enum | {'type': 'Enum/String', 'df': 'Categorizes the ability for specific UI filters.'} | 90 |
| [`temporary_effects`](./Abilities_and_Spells.md#context-temporary_effects) | Block | {'type': '`Block`', 'df': "Status applications that wear off automatically or at the end of the turn. | 88 |
| [`sounds`](./Abilities_and_Spells.md#context-sounds) | Block | {'type': '`Block`', 'df': 'Audio cues triggered by the ability. | 39 |
| [`splash_damage`](./Abilities_and_Spells.md#context-splash_damage) | Block | {'type': '`Block`', 'df': 'Secondary Area of Effect blast parameters. | 34 |
| [`ai_ability`](./Enums.md#enum-ai_ability) | Enum | {'type': '`Enum/String`', 'df': 'Overrides the ability used when triggered by AI.'} | 29 |
| [`keyword_tooltips`](./Abilities_and_Spells.md#context-keyword_tooltips) | Block | {'type': '`Block`', 'df': "Forces specific UI tooltips to appear when hovering over the ability. | 23 |
| [`chain_ability`](./Enums.md#enum-chain_ability) | Enum | {'type': '`Enum/String`', 'df': 'An ability that automatically executes sequentially after this one.'} | 15 |
| [`sub_ability`](./Enums.md#enum-sub_ability) | Enum | {'type': '`Enum/String`', 'df': 'A secondary ability component referenced by complex templates.'} | 8 |
| [`cloned_ability`](./Enums.md#enum-cloned_ability) | Enum | {'type': '`Enum/String`', 'df': 'Copies the properties of another ability dynamically.'} | 2 |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | {'type': 'Block', 'df': 'Non-damaging status applications and logic triggers executed on impact.'} | 2 |
| [`empty_self_damage`](./Abilities_and_Spells.md#context-empty_self_damage) | Block | {'type': '`Block`', 'df': 'Recoil damage specifically applied when the attack misses all targets. | 2 |
| [`bonk_damage`](./Abilities_and_Spells.md#context-bonk_damage) | Block | {'type': '`Block`', 'df': 'Damage dealt when knocked into a wall or obstacle. | 1 |
| [`damage`](./Abilities_and_Spells.md#context-damage) | Block | {'type': 'Number', 'df': 'The base damage properties of an attack.'} | 1 |

</details>

---

### Context: `damage_instance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2344

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#context-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | {'type': '`Block`', 'df': 'Non-damaging status applications and logic triggers executed on impact. | 1785 |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1446 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`).'} | 358 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': 'Array of elemental tags to apply (e.g., `[Fire Holy]`).'} | 352 |
| `knockback` | Mixed | {'type': '`Number`', 'df': 'The base physics pushing power (in tiles).'} | 254 |
| `ai_base_score` | Number | {'type': '`Number`', 'df': 'How highly the AI values using this ability.'} | 223 |
| `heal` | Number | {'type': '`Number`', 'df': 'Restores health instead of dealing damage.'} | 122 |
| `cant_miss` | Boolean | {'type': '`Boolean`', 'df': 'Guarantees the hit, bypassing dodge mechanics.'} | 110 |
| `incidentally_collects_pickups` | Boolean | {'type': '`Boolean`', 'df': 'Automatically grabs items in the AoE.'} | 103 |
| [`custom_additional_ai_weight`](./Enums.md#enum-custom_additional_ai_weight) | Enum | {'type': '`Enum/String`', 'df': 'Granular AI preference adjustments (e.g., `prefer_dont_move`).'} | 82 |
| `piercing` | Boolean | {'type': '`Boolean`', 'df': 'Ignores a percentage of target defense/armor.'} | 52 |
| `makes_contact` | Boolean | {'type': '`Boolean`', 'df': 'If false, explicitly avoids triggering contact-based passives.'} | 40 |
| [`layer`](./Enums.md#enum-layer) | Enum | {'type': '`Enum/String`', 'df': 'Z-index targeting (e.g., `characters`, `self`).'} | 26 |
| [`blocked_damage`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': 'Base damage dealt if the attack is blocked.'} | 24 |
| [`raw_damage`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': 'Unmitigated, unscaled base numbers.'} | 22 |
| `crit_chance` | Mixed | {'type': '`Number`', 'df': 'Override for base critical hit probability.'} | 16 |
| `override_trample_damage` | Boolean | {'type': '`Boolean`', 'df': 'Custom damage value for trample moves.'} | 15 |
| `contact_requires_adjacency` | Boolean | {'type': '`Boolean`', 'df': 'Contact effects only trigger if standing next to the target.'} | 14 |
| `can_revive` | Boolean | {'type': '`Boolean`', 'df': 'Healing instance that can bring dead allies back to life.'} | 8 |
| `show_damage_on_0` | Boolean | {'type': '`Boolean`', 'df': 'Forces the "-0" floater text to appear.'} | 6 |
| `force_play_hit_animation` | Boolean | {'type': '`Boolean`', 'df': 'Forces the flinch animation even on 0 damage.'} | 5 |
| `blocked_multiplier` | Number | {'type': '`Number`', 'df': 'Multiplier applied when hitting a blocking target.'} | 4 |
| [`accuracy`](./Enums.md#enum-accuracy) | Enum | {'type': '`Enum/String`', 'df': 'Hit chance modifier.'} | 3 |
| `can_collect_pickups` | Boolean | {'type': '`Boolean`', 'df': 'The damage instance can grab items on the ground.'} | 3 |
| `can_instapop` | Boolean | {'type': '`Boolean`', 'df': 'Allows the attack to instantly destroy specific weak entities.'} | 2 |
| `disallow_modifications` | Boolean | {'type': '`Boolean`', 'df': 'Prevents passives from altering this damage instance.'} | 2 |
| `force_no_contact` | Boolean | {'type': '`Boolean`', 'df': 'Bypasses all contact-based retaliation (Thorns, etc).'} | 2 |
| `non_lethal` | Boolean | {'type': '`Boolean`', 'df': 'Reduces target to 1 HP but will never kill.'} | 2 |
| [`raw_heal`](./Math_Equations.md) | Equation | {'type': '`String`', 'df': 'Unmitigated, unscaled base numbers.'} | 2 |
| `two_way_contact` | Boolean | {'type': '`Boolean`', 'df': 'Both caster and target trigger contact effects on each other.'} | 2 |
| `HealthRegenUp` | Number | {'type': 'Number', 'df': "Applies or references the 'HealthRegenUp' effect/state."} | 1 |
| `damage_shield_only` | Boolean | {'type': '`Boolean`', 'df': 'Depletes shields but cannot harm base health.'} | 1 |
| [`faction`](./Enums.md#enum-faction) | Enum | {'type': '`Enum/String`', 'df': 'Determines alignment (`enemies`, `cats`, `neutral`).'} | 1 |
| [`final_hit_bonus_damage`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': 'Extra damage applied on the last hit of a multihit.'} | 1 |
| `force_adjacent_and_diagonal_contact` | Boolean | {'type': '`Boolean`', 'df': 'Treats diagonal hits as physical contact.'} | 1 |
| `force_no_knockback` | Boolean | {'type': '`Boolean`', 'df': 'Prevents the target from being pushed.'} | 1 |
| `hint_dont_lowgravboost` | Boolean | {'type': '`Boolean`', 'df': 'AI hint to ignore wind physics.'} | 1 |
| [`hit_animation_alt`](./Enums.md#enum-hit_animation_alt) | Enum | {'type': '`Enum/String`', 'df': 'Custom flinch animation for the target.'} | 1 |
| `ranged` | Boolean | {'type': '`Boolean`', 'df': 'Boolean flagging the damage as explicitly ranged.'} | 1 |

</details>

---

### Context: `meta`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2333

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String | {'type': '`String`', 'df': "The localization key for the ability's display description."} | 1641 |
| [`name`](./Strings.md#string-name) | String | {'type': '`String`', 'df': "The localization key for the ability's display name."} | 1597 |
| [`class`](./Enums.md#enum-class) | Enum | {'type': '`Enum/String`', 'df': 'Categorizes the ability for specific UI filters.'} | 876 |
| [`type_icon`](./Strings.md#string-type_icon) | String | {'type': '`String`', 'df': ''} | 283 |
| `animate_name` | Boolean | {'type': '`Boolean`', 'df': 'If true, adds a visual pop/animation to the name text when cast.'} | 177 |
| `icon_shell_frame` | Mixed | {'type': '`Enum/String`', 'df': ''} | 28 |
| `is_move` | Mixed | {'type': '`Enum/String`', 'df': ''} | 20 |
| [`ability_icon`](./Enums.md#enum-ability_icon) | Enum | {'type': '`Enum/String`', 'df': 'The UI icon to display in the action bar.'} | 14 |
| [`tooltip_values`](./Arrays.md#array-tooltip_values) | Array | {'type': '`Array`', 'df': ''} | 9 |
| [`icon_damage_display`](./Strings.md#string-icon_damage_display) | String | {'type': '`String`', 'df': ''} | 8 |
| [`icon_damage_display_eq`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': ''} | 7 |
| `is_basic_attack` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| [`icon_damage_type`](./Enums.md#enum-icon_damage_type) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| `is_trinket` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| `dont_visualize_ai` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| [`icon_damage_display_suffix`](./Strings.md#string-icon_damage_display_suffix) | String | {'type': '`String`', 'df': ''} | 2 |
| `is_weapon` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `graphics`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2037

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | {'type': '`Enum/String`', 'df': 'The primary flash animation label triggered.'} | 1559 |
| [`particle`](./Enums.md#enum-particle) | Enum | {'type': '`Enum/String`', 'df': 'References an impact or cast particle effect.'} | 488 |
| [`projectile`](./Enums.md#enum-projectile) | Enum | {'type': '`Enum/String`', 'df': 'References a projectile entity.'} | 228 |
| `lob` | Boolean | {'type': '`Boolean`', 'df': ''} | 130 |
| `delay` | Number | {'type': '`Number`', 'df': 'Frame delay before firing projectile/effect.'} | 93 |
| `dont_visualize_ai` | Boolean | {'type': '`Boolean`', 'df': ''} | 86 |
| `dont_orient` | Boolean | {'type': '`Boolean`', 'df': 'Prevents the character from turning to face the target.'} | 83 |
| [`dash_animation`](./Enums.md#enum-dash_animation) | Enum | {'type': '`Enum/String`', 'df': 'State-specific animations for trample/dash abilities.'} | 65 |
| [`dash_start_animation`](./Enums.md#enum-dash_start_animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 63 |
| `speed` | Mixed | {'type': '`Number`', 'df': 'Rotations per second.'} | 61 |
| [`affected_particle`](./Enums.md#enum-affected_particle) | Enum | {'type': '`Enum/String`', 'df': 'Visuals applied to the target receiving the effect.'} | 51 |
| [`dash_attack_animation`](./Enums.md#enum-dash_attack_animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 45 |
| `lob_height` | Number | {'type': '`Number`', 'df': 'Adjustments for arcing projectiles.'} | 45 |
| [`animation_in`](./Enums.md#enum-animation_in) | Enum | {'type': '`Enum/String`', 'df': 'Used for transition states (like burrowing).'} | 43 |
| [`animation_out`](./Enums.md#enum-animation_out) | Enum | {'type': '`Enum/String`', 'df': 'Used for transition states (like burrowing).'} | 43 |
| [`jump_attack_animation`](./Enums.md#enum-jump_attack_animation) | Enum | {'type': '`Enum/String`', 'df': 'Overrides for jump physics.'} | 39 |
| `use_projectile` | Boolean | {'type': '`Boolean`', 'df': ''} | 35 |
| [`full_jump_animation`](./Enums.md#enum-full_jump_animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 24 |
| `full_jump_sync_frames` | Number | {'type': '`Number`', 'df': ''} | 24 |
| `use_rotation` | Boolean | {'type': '`Boolean`', 'df': ''} | 24 |
| [`dash_end_animation`](./Enums.md#enum-dash_end_animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 22 |
| `palette` | Number | {'type': '`Number`', 'df': 'Swaps the color palette ID.'} | 21 |
| `full_jump_windup_frames` | Number | {'type': '`Number`', 'df': ''} | 20 |
| `visual_delay_but_simultaneous_damage` | Number | {'type': '`Number`', 'df': ''} | 18 |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum | {'type': '`Enum/String`', 'df': 'Specific spawn points for particles.'} | 17 |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum | {'type': '`Enum/String`', 'df': 'Specific spawn points for particles.'} | 16 |
| `fall_from_sky` | Boolean | {'type': '`Boolean`', 'df': 'Spawns the projectile from the top of the screen.'} | 16 |
| [`move_start_animation`](./Enums.md#enum-move_start_animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 14 |
| `use_placeholder` | Boolean | {'type': '`Boolean`', 'df': ''} | 14 |
| [`move_end_animation`](./Enums.md#enum-move_end_animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 13 |
| `face_toss_target` | Boolean | {'type': '`Boolean`', 'df': ''} | 12 |
| `ignore_slowtiles` | Boolean | {'type': '`Boolean`', 'df': ''} | 12 |
| [`chain_distance`](./Enums.md#enum-chain_distance) | Enum | {'type': '`Enum/String`', 'df': 'Creates a tethered repeating graphic (like a hook).'} | 11 |
| [`chain_movieclip`](./Enums.md#enum-chain_movieclip) | Enum | {'type': '`Enum/String`', 'df': 'Creates a tethered repeating graphic (like a hook).'} | 11 |
| `darken_screen` | Boolean | {'type': '`Boolean`', 'df': 'Dims the background during the ability cast.'} | 11 |
| [`beam_cap`](./Enums.md#enum-beam_cap) | Enum | {'type': '`Enum/String`', 'df': 'Flash movieclips used to render continuous laser beams.'} | 10 |
| [`beam_clip`](./Enums.md#enum-beam_clip) | Enum | {'type': '`Enum/String`', 'df': 'Flash movieclips used to render continuous laser beams.'} | 10 |
| `bounce_on_hit` | Boolean | {'type': '`Boolean`', 'df': 'Visual hop when striking a target.'} | 10 |
| `darken_screen_exclude_characters_on_tile` | Boolean | {'type': '`Boolean`', 'df': ''} | 10 |
| [`end`](./Enums.md#enum-end) | Enum | {'type': '`Enum/String`', 'df': 'Segments for continuous channeled animations.'} | 10 |
| [`jump_start_animation`](./Enums.md#enum-jump_start_animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 10 |
| [`loop`](./Enums.md#enum-loop) | Enum | {'type': '`Enum/String`', 'df': 'Segments for continuous channeled animations.'} | 10 |
| [`prime_animation`](./Enums.md#enum-prime_animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 10 |
| [`start`](./Enums.md#enum-start) | Enum | {'type': '`Enum/String`', 'df': 'Segments for continuous channeled animations.'} | 10 |
| `max_tiles_single_loop` | Number | {'type': '`Number`', 'df': ''} | 9 |
| [`random_delay`](./Arrays.md#array-random_delay) | Array | {'type': '`Array`', 'df': 'Adds chaotic timing to multi-projectile casts.'} | 9 |
| `sync_speed` | Number | {'type': '`Number`', 'df': ''} | 9 |
| `fx_is_placeholder_animation` | Boolean | {'type': '`Boolean`', 'df': ''} | 8 |
| `aoe_spell_on_land` | Boolean | {'type': '`Boolean`', 'df': 'Visual trigger when a jump lands.'} | 7 |
| `fx_random_flip` | Boolean | {'type': '`Boolean`', 'df': ''} | 7 |
| [`land_animation`](./Enums.md#enum-land_animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 7 |
| [`miss_particle`](./Enums.md#enum-miss_particle) | Enum | {'type': '`Enum/String`', 'df': 'Specific spawn points for particles.'} | 7 |
| `use_super_armor` | Boolean | {'type': '`Boolean`', 'df': 'Prevents flinch animations from interrupting this cast.'} | 7 |
| [`air_animation`](./Enums.md#enum-air_animation) | Enum | {'type': '`Enum/String`', 'df': 'Animation played while entity is airborne.'} | 6 |
| [`custom_priming_animation`](./Enums.md#enum-custom_priming_animation) | Enum | {'type': '`Enum/String`', 'df': 'Animation used while charging an ability.'} | 6 |
| `darken_screen_exclude_self` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| `darken_screen_start_early` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| [`fall_randomize_timing`](./Enums.md#enum-fall_randomize_timing) | Enum | {'type': '`Enum/String`', 'df': ''} | 6 |
| `min_throw_height` | Number | {'type': '`Number`', 'df': ''} | 6 |
| [`miss_random_delay`](./Arrays.md#array-miss_random_delay) | Array | {'type': '`Array`', 'df': ''} | 6 |
| `single_projectile` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| [`detatched_animation`](./Enums.md#enum-detatched_animation) | Enum | {'type': '`Enum/String`', 'df': 'Plays an animation separated from the character body.'} | 5 |
| `detatched_animation_reach` | Number | {'type': '`Number`', 'df': ''} | 5 |
| [`empty_animation`](./Enums.md#enum-empty_animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 5 |
| [`mode`](./Enums.md#enum-mode) | Enum | {'type': '`Enum/String`', 'df': ''} | 5 |
| `fixed_jump_height` | Number | {'type': '`Number`', 'df': ''} | 4 |
| [`rocket_swirl`](./Abilities_and_Spells.md#context-rocket_swirl) | Block | {'type': '`Block`', 'df': 'Visual parameters for swirling projectile paths. | 4 |
| `sync_frames` | Number | {'type': '`Number`', 'df': ''} | 4 |
| [`dash_decelerating_animation`](./Enums.md#enum-dash_decelerating_animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| `decelerate` | Number | {'type': '`Number`', 'df': 'Visual slowdown at the end of a movement.'} | 3 |
| `delay_from_map_edge` | Boolean | {'type': '`Boolean`', 'df': 'Delays effect based on distance from the screen edge.'} | 3 |
| `easing` | Number | {'type': '`Number`', 'df': 'Smoothing function for movement animations.'} | 3 |
| `fixed_jump_speed` | Mixed | {'type': '`Number`', 'df': ''} | 3 |
| [`grab_animation`](./Enums.md#enum-grab_animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`lob_yoff`](./Enums.md#enum-lob_yoff) | Enum | {'type': '`Enum/String`', 'df': 'Adjustments for arcing projectiles.'} | 3 |
| `lock_orientation_during_dash` | Boolean | {'type': '`Boolean`', 'df': 'Prevents the sprite from flipping mid-dash.'} | 3 |
| `use_projectile_spawn_offset` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| `use_rotation_once` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| `always_play_animations` | Boolean | {'type': '`Boolean`', 'df': 'Bypasses speed-up/skip logic.'} | 2 |
| `detatched_animation_cutoff` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `do_damage_immediately` | Boolean | {'type': '`Boolean`', 'df': 'Applies math before the animation actually hits.'} | 2 |
| `jump_height_multiplier` | Mixed | {'type': '`Number`', 'df': 'Overrides for jump physics.'} | 2 |
| [`mask_center`](./Enums.md#enum-mask_center) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`mask_extent`](./Enums.md#enum-mask_extent) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| `max_throw_height` | Number | {'type': '`Number`', 'df': ''} | 2 |
| [`particle_mat`](./Enums.md#enum-particle_mat) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`preturn_animation`](./Enums.md#enum-preturn_animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`primed_alt_animation`](./Strings.md#string-primed_alt_animation) | String | {'type': '`String`', 'df': ''} | 2 |
| [`pseudoprojectile`](./Enums.md#enum-pseudoprojectile) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| `reverse_orientation` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `self_damage_mid_port` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `throw_speed` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `use_hit_alts` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| [`affected_animation`](./Enums.md#enum-affected_animation) | Enum | {'type': '`Enum/String`', 'df': 'Visuals applied to the target receiving the effect.'} | 1 |
| [`ally_animation`](./Enums.md#enum-ally_animation) | Enum | {'type': '`Enum/String`', 'df': 'Distinct animation used when targeting a friendly unit.'} | 1 |
| [`animate_name`](./Enums.md#enum-animate_name) | Enum | {'type': '`Enum/String`', 'df': 'Animates the ability name text on cast.'} | 1 |
| `apex_distance` | Number | {'type': '`Number`', 'df': 'Calculations for the peak of a jump/lob arc.'} | 1 |
| [`apex_time`](./Enums.md#enum-apex_time) | Enum | {'type': '`Enum/String`', 'df': 'Calculations for the peak of a jump/lob arc.'} | 1 |
| `bypass_combatspeed` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`damage_threshold_altanimations`](./Abilities_and_Spells.md#context-damage_threshold_altanimations) | Block | {'type': '`Block`', 'df': 'Triggers different hit animations based on the amount of damage dealt. | 1 |
| [`dash_bonk_animation`](./Enums.md#enum-dash_bonk_animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `delay_from_map_center` | Boolean | {'type': '`Boolean`', 'df': 'Positional based timing delays.'} | 1 |
| `delay_from_reverse_map_edge` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `do_animation_offscreen` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `do_not_clear_placeholder` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `face_targets` | Boolean | {'type': '`Boolean`', 'df': 'Forces the sprite to look at the target tile.'} | 1 |
| `first_castpoint_is_self_damage_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`hang_time`](./Enums.md#enum-hang_time) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `jump_speed_multiplier` | Number | {'type': '`Number`', 'df': ''} | 1 |
| [`lob_speed`](./Enums.md#enum-lob_speed) | Enum | {'type': '`Enum/String`', 'df': 'Adjustments for arcing projectiles.'} | 1 |
| `max_range` | Number | {'type': '`Number`', 'df': 'The maximum and minimum distance required to cast.'} | 1 |
| `min_range` | Number | {'type': '`Number`', 'df': 'The maximum and minimum distance required to cast.'} | 1 |
| `othercat_placeholder_available` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`precast_delay`](./Enums.md#enum-precast_delay) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`spawn_offset`](./Arrays.md#array-spawn_offset) | Array | {'type': '`Array`', 'df': ''} | 1 |
| `uncatchable` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `use_directional_animations` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `use_origin_offsets` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2012

> **Referenced by:** [`DoDamage`](./Abilities_and_Spells.md#context-dodamage), [`MeleeRevengeDamage`](./Abilities_and_Spells.md#context-meleerevengedamage), [`ROOT`](./Abilities_and_Spells.md#context-root), [`RevengeDamage`](./Abilities_and_Spells.md#context-revengedamage), [`bonk_damage`](./Abilities_and_Spells.md#context-bonk_damage), [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance), [`empty_self_damage`](./Abilities_and_Spells.md#context-empty_self_damage), [`self_damage`](./Abilities_and_Spells.md#context-self_damage), [`splash_damage`](./Abilities_and_Spells.md#context-splash_damage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`FormChange`](./Enums.md#enum-formchange) | Enum | {'type': 'Enum/String', 'df': 'Transforms the character into a different state or form (e.g., Rage, HasCat).'} | 102 |
| [`Stun`](./Arrays.md#array-stun) | Array | {'type': 'Number', 'df': "Applies or references the 'Stun' effect/state."} | 89 |
| `Burn` | Number | {'type': 'Number', 'df': "Applies or references the 'Burn' effect/state."} | 76 |
| `IgnoreSelf` | Mixed | {'type': '`Number`', 'df': "Applies or references the 'IgnoreSelf' effect/state."} | 75 |
| `Bruise` | Number | {'type': 'Number', 'df': "Applies or references the 'Bruise' effect/state."} | 70 |
| `Poison` | Number | {'type': 'Number', 'df': "Applies or references the 'Poison' effect/state."} | 65 |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum | {'type': '`Enum/String`', 'df': 'Transforms the terrain tile under the target.'} | 62 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | {'type': 'Block', 'df': 'Fallback block that executes if the preceding `Conditional_` block evaluated to false.'} | 59 |
| `Bleed` | Number | {'type': 'Number', 'df': "Applies or references the 'Bleed' effect/state."} | 54 |
| `Shield` | Mixed | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 49 |
| `Cleanse` | Number | {'type': 'Number', 'df': "Applies or references the 'Cleanse' effect/state."} | 44 |
| [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag) | Block | {'type': 'Block', 'df': 'Conditional trigger: Executes nested logic if the target possesses the specified entity tag.'} | 38 |
| [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic if the target is hostile to the caster.'} | 35 |
| `Confusion` | Number | {'type': 'Number', 'df': "Applies or references the 'Confusion' effect/state."} | 35 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpeedUp' effect/state."} | 34 |
| [`Temporary`](./Abilities_and_Spells.md#context-temporary) | Block | {'type': '`Block`', 'df': 'A wrapper block for applying status effects that automatically expire.'} | 34 |
| [`BounceObject`](./Enums.md#enum-bounceobject) | Enum | {'type': '`Enum/String`', 'df': 'Spawns a physics object that visually bounces off the target.'} | 31 |
| `AllStatsUp` | Mixed | {'type': 'Number', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 29 |
| `DamageUp` | Number | {'type': 'Number', 'df': "Applies or references the 'DamageUp' effect/state."} | 28 |
| [`TransformAbility`](./Enums.md#enum-transformability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'TransformAbility' effect/state."} | 28 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': 'Block', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target.'} | 27 |
| `ManaGain` | Mixed | {'type': 'String', 'df': "Applies or references the 'ManaGain' effect/state."} | 26 |
| [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic if the target is friendly to the caster. | 25 |
| [`Slow`](./Arrays.md#array-slow) | Array | {'type': '`Number`', 'df': "Applies or references the 'Slow' effect/state."} | 25 |
| [`Fear`](./Arrays.md#array-fear) | Array | {'type': 'Number', 'df': "Applies or references the 'Fear' effect/state."} | 23 |
| [`Weakness`](./Arrays.md#array-weakness) | Array | {'type': '`Number`', 'df': "Applies or references the 'Weakness' effect/state."} | 23 |
| [`Blind`](./Arrays.md#array-blind) | Array | {'type': 'Number', 'df': "Applies or references the 'Blind' effect/state."} | 22 |
| `Leech` | Number | {'type': '`Number`', 'df': "Applies or references the 'Leech' effect/state."} | 22 |
| `StrengthUp` | Mixed | {'type': '`Number`', 'df': "Applies or references the 'StrengthUp' effect/state."} | 22 |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array | {'type': 'Number', 'df': "Applies or references the 'ConstitutionUp' effect/state."} | 21 |
| [`EvolveAbilityFromPool`](./Abilities_and_Spells.md#context-evolveabilityfrompool) | Block | {'type': '`Enum/String`', 'df': 'Upgrades or transforms an existing ability into a new one from the specified pool.'} | 21 |
| `Immobile` | Number | {'type': 'Number', 'df': "Applies or references the 'Immobile' effect/state."} | 21 |
| `IntelligenceUp` | Mixed | {'type': 'Number', 'df': "Applies or references the 'IntelligenceUp' effect/state."} | 21 |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'VisualFXTile' effect/state."} | 21 |
| [`Charmed`](./Arrays.md#array-charmed) | Array | {'type': 'Number', 'df': "Applies or references the 'Charmed' effect/state."} | 20 |
| [`Sleep`](./Arrays.md#array-sleep) | Array | {'type': '`Number`', 'df': "Applies or references the 'Sleep' effect/state."} | 20 |
| `Vaporize` | Number | {'type': '`Number`', 'df': "Applies or references the 'Vaporize' effect/state."} | 20 |
| `Madness` | Number | {'type': 'Number', 'df': 'Applies the Madness debuff/status effect.'} | 19 |
| `Brace` | Number | {'type': 'Number', 'df': "Applies or references the 'Brace' effect/state."} | 17 |
| `CollectsPickups` | Number | {'type': '`Number`', 'df': "Applies or references the 'CollectsPickups' effect/state."} | 17 |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#context-knockupandaway) | Block | {'type': '`Block`', 'df': 'Displaces the target vertically and horizontally away from the source.'} | 17 |
| `RandomStatUp` | Number | {'type': 'Number', 'df': "Applies or references the 'RandomStatUp' effect/state."} | 17 |
| [`Freeze`](./Arrays.md#array-freeze) | Array | {'type': 'Number', 'df': "Applies or references the 'Freeze' effect/state."} | 16 |
| `OverrideKnockbackDamage` | Mixed | {'type': '`Number`', 'df': "Applies or references the 'OverrideKnockbackDamage' effect/state."} | 16 |
| [`Consumed`](./Abilities_and_Spells.md#context-consumed) | Block | {'type': 'Block', 'df': 'State block triggered when this object or entity is eaten/consumed by another character.'} | 15 |
| `VaporizeCorpse` | Number | {'type': '`Number`', 'df': "Applies or references the 'VaporizeCorpse' effect/state."} | 15 |
| [`ChangeCatClass`](./Enums.md#enum-changecatclass) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ChangeCatClass' effect/state."} | 14 |
| `DivineShield` | Number | {'type': 'Number', 'df': "Applies or references the 'DivineShield' effect/state."} | 14 |
| `EndTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'EndTurn' effect/state."} | 14 |
| `FaceAway` | Number | {'type': '`Number`', 'df': "Applies or references the 'FaceAway' effect/state."} | 14 |
| `RefreshMovePoints` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshMovePoints' effect/state."} | 14 |
| `TakeExtraTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'TakeExtraTurn' effect/state."} | 14 |
| [`TransformBasicAttack`](./Enums.md#enum-transformbasicattack) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'TransformBasicAttack' effect/state."} | 14 |
| [`CatPartsTransform`](./Abilities_and_Spells.md#context-catpartstransform) | Block | {'type': 'Block', 'df': 'Transforms specific body parts into different visual variants.'} | 13 |
| [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss) | Block | {'type': 'Block', 'df': 'Conditional trigger: Executes nested logic if the target is a Boss.'} | 13 |
| `GenericDebuff` | Number | {'type': '`Number`', 'df': "Applies or references the 'GenericDebuff' effect/state."} | 13 |
| `Leeches` | Number | {'type': '`Number`', 'df': "Applies or references the 'Leeches' effect/state."} | 13 |
| [`Petrify`](./Arrays.md#array-petrify) | Array | {'type': 'Number', 'df': "Applies or references the 'Petrify' effect/state."} | 13 |
| [`RandomMagicMissile`](./Abilities_and_Spells.md#context-randommagicmissile) | Block | {'type': '`Number`', 'df': 'Fires a randomized number of magic missiles.'} | 13 |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | {'type': '`Block`', 'df': 'Selects and applies a random status effect from the provided nested block.'} | 13 |
| `Displace` | Number | {'type': '`Number`', 'df': "Applies or references the 'Displace' effect/state."} | 12 |
| `LuckUp` | Mixed | {'type': 'Number', 'df': "Applies or references the 'LuckUp' effect/state."} | 12 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill) | Block | {'type': 'Block', 'df': 'Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action.'} | 11 |
| [`ChanceToBreakFree`](./Abilities_and_Spells.md#context-chancetobreakfree) | Block | {'type': '`Block`', 'df': 'Provides a probability to escape a grapple or restraining effect. | 11 |
| [`Cleave`](./Abilities_and_Spells.md#context-cleave) | Block | {'type': 'Number', 'df': 'Causes the attack to hit adjacent enemies alongside the primary target.'} | 11 |
| [`Conditional_GoodRoll`](./Abilities_and_Spells.md#context-conditional_goodroll) | Block | {'type': 'Block', 'df': 'Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.'} | 11 |
| [`DoScreenShake`](./Abilities_and_Spells.md#context-doscreenshake) | Block | {'type': 'Block', 'df': 'Triggers a camera screen shake effect.'} | 11 |
| `FullHeal` | Number | {'type': 'Number', 'df': "Applies or references the 'FullHeal' effect/state."} | 11 |
| [`Conditional_FormulaIsPositive`](./Abilities_and_Spells.md#context-conditional_formulaispositive) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the evaluated mathematical formula returns a value greater than 0. | 10 |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative) | Block | {'type': 'Block', 'df': 'A simulation block used by the AI to test hypothetical outcomes before committing to an action.'} | 10 |
| `DexterityUp` | Mixed | {'type': 'Number', 'df': "Applies or references the 'DexterityUp' effect/state."} | 10 |
| [`MagicWeakness`](./Arrays.md#array-magicweakness) | Array | {'type': 'Number', 'df': "Applies or references the 'MagicWeakness' effect/state."} | 10 |
| `PartialPurge` | Number | {'type': '`Number`', 'df': "Applies or references the 'PartialPurge' effect/state."} | 10 |
| `PurgeAll` | Number | {'type': '`Number`', 'df': "Applies or references the 'PurgeAll' effect/state."} | 10 |
| `RefreshActPoints` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshActPoints' effect/state."} | 10 |
| `Thorns` | Number | {'type': '`Number`', 'df': "Applies or references the 'Thorns' effect/state."} | 10 |
| `Ammo` | Number | {'type': '`Number`', 'df': "Applies or references the 'Ammo' effect/state."} | 9 |
| [`ApplyPassives`](./Abilities_and_Spells.md#context-applypassives) | Block | {'type': 'Block', 'df': 'Grants the nested passive abilities dynamically.'} | 9 |
| `DeferVaporize` | Number | {'type': '`Number`', 'df': "Applies or references the 'DeferVaporize' effect/state."} | 9 |
| [`Marked`](./Arrays.md#array-marked) | Array | {'type': 'Number', 'df': "Applies or references the 'Marked' effect/state."} | 9 |
| `SpawnCreep` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpawnCreep' effect/state."} | 9 |
| [`VisualFX`](./Enums.md#enum-visualfx) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'VisualFX' effect/state."} | 9 |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate) | Block | {'type': 'Block', 'df': 'Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters.'} | 8 |
| `ChanceToBreak` | Number | {'type': 'Number', 'df': "Applies or references the 'ChanceToBreak' effect/state."} | 8 |
| `HealthRegenUp` | Number | {'type': 'Number', 'df': "Applies or references the 'HealthRegenUp' effect/state."} | 8 |
| `OverrideChainKnockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'OverrideChainKnockback' effect/state."} | 8 |
| [`Rot`](./Arrays.md#array-rot) | Array | {'type': '`Number`', 'df': "Applies or references the 'Rot' effect/state."} | 8 |
| `AlphaCat` | Number | {'type': 'Number', 'df': "Applies or references the 'AlphaCat' effect/state."} | 7 |
| [`ApplyStatusIfCrit`](./Abilities_and_Spells.md#context-applystatusifcrit) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. | 7 |
| `BramblesOnHit` | Number | {'type': '`Number`', 'df': "Applies or references the 'BramblesOnHit' effect/state."} | 7 |
| `ContextualHeal` | Number | {'type': '`Number`', 'df': "Applies or references the 'ContextualHeal' effect/state."} | 7 |
| [`ForceAttack`](./Abilities_and_Spells.md#context-forceattack) | Block | {'type': '`Number`', 'df': 'Forces the character to execute an immediate attack.'} | 7 |
| `Instakill` | Number | {'type': '`Number`', 'df': "Applies or references the 'Instakill' effect/state."} | 7 |
| `KnockbackDamageImmuneUntilSettled` | Number | {'type': '`Number`', 'df': "Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state."} | 7 |
| `ManaSteal` | Number | {'type': '`Number`', 'df': "Applies or references the 'ManaSteal' effect/state."} | 7 |
| `Tech` | Number | {'type': '`Number`', 'df': "Applies or references the 'Tech' effect/state."} | 7 |
| `TempRangeUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempRangeUp' effect/state."} | 7 |
| [`TriggerWerewolfTransform`](./Arrays.md#array-triggerwerewolftransform) | Array | {'type': '`Array`', 'df': "Applies or references the 'TriggerWerewolfTransform' effect/state."} | 7 |
| [`BackflipWhenTargeted`](./Abilities_and_Spells.md#context-backflipwhentargeted) | Block | {'type': 'Number', 'df': 'Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack.'} | 6 |
| [`BounceRock`](./Arrays.md#array-bouncerock) | Array | {'type': '`Enum/String`', 'df': "Applies or references the 'BounceRock' effect/state."} | 6 |
| `CharismaUp` | Mixed | {'type': 'Number', 'df': "Applies or references the 'CharismaUp' effect/state."} | 6 |
| `ClearStarving` | Number | {'type': '`Number`', 'df': "Applies or references the 'ClearStarving' effect/state."} | 6 |
| [`Conditional_Corpse`](./Abilities_and_Spells.md#context-conditional_corpse) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic if the target is a dead body/corpse.'} | 6 |
| [`ConjureBonusAbility`](./Abilities_and_Spells.md#context-conjurebonusability) | Block | {'type': '`Enum/String`', 'df': "Adds a temporary bonus ability to the character's hand/deck."} | 6 |
| [`Craft`](./Abilities_and_Spells.md#context-craft) | Block | {'type': '`Block`', 'df': 'Synthesizes or spawns a new item from a specific pool.'} | 6 |
| [`DoDistortionRing`](./Abilities_and_Spells.md#context-dodistortionring) | Block | {'type': '`Block`', 'df': 'Creates a visual distortion ring effect on the screen. | 6 |
| [`Metronome`](./Abilities_and_Spells.md#context-metronome) | Block | {'type': '`Number`', 'df': 'Executes a random musical or metronome ability.'} | 6 |
| [`ObjectOnHitCharacter`](./Abilities_and_Spells.md#context-objectonhitcharacter) | Block | {'type': '`Enum/String`', 'df': 'Spawns a specific character or entity upon impact.'} | 6 |
| `RandomInjury` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomInjury' effect/state."} | 6 |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'RemoveStatus' effect/state."} | 6 |
| [`ScatterHeldCoin`](./Arrays.md#array-scatterheldcoin) | Array | {'type': '`Number`', 'df': "Applies or references the 'ScatterHeldCoin' effect/state."} | 6 |
| `SetDistanceDisplace` | Number | {'type': '`Number`', 'df': "Applies or references the 'SetDistanceDisplace' effect/state."} | 6 |
| `SetHealth` | Number | {'type': '`Number`', 'df': "Applies or references the 'SetHealth' effect/state."} | 6 |
| [`SpawnThingIfHitKills`](./Enums.md#enum-spawnthingifhitkills) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'SpawnThingIfHitKills' effect/state."} | 6 |
| `SpiderInfested` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpiderInfested' effect/state."} | 6 |
| [`Tarred`](./Arrays.md#array-tarred) | Array | {'type': '`Number`', 'df': "Applies or references the 'Tarred' effect/state."} | 6 |
| [`TeamCastAbility`](./Enums.md#enum-teamcastability) | Enum | {'type': '`Enum/String`', 'df': 'Requires or involves multiple characters to execute the ability.'} | 6 |
| [`TwisterDisplaceWithDamage`](./Abilities_and_Spells.md#context-twisterdisplacewithdamage) | Block | {'type': '`Block`', 'df': 'A whirlwind effect that randomly displaces targets and deals damage. | 6 |
| [`CollectsPickupsWithAltEffects`](./Abilities_and_Spells.md#context-collectspickupswithalteffects) | Block | {'type': '`Block`', 'df': "Triggers alternative nested effects when collecting items or pickups. | 5 |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#context-conditional_hasstatus) | Block | {'type': 'Block', 'df': 'Conditional trigger: Executes nested logic if the target currently has the specified status effect.'} | 5 |
| [`Conditional_InForm`](./Abilities_and_Spells.md#context-conditional_inform) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic if the target is currently in the specified transformation form.'} | 5 |
| [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic if the target is NOT a Boss.'} | 5 |
| [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object) | Block | {'type': 'Block', 'df': 'Conditional trigger: Executes nested logic if the target is an inanimate object or furniture.'} | 5 |
| [`Conditional_PlayerCat`](./Abilities_and_Spells.md#context-conditional_playercat) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic if the target is a player-controlled cat.'} | 5 |
| `DodgeChance_Status` | Number | {'type': 'Number', 'df': "Applies or references the 'DodgeChance_Status' effect/state."} | 5 |
| `Drowsy` | Number | {'type': '`Number`', 'df': "Applies or references the 'Drowsy' effect/state."} | 5 |
| `FillMana` | Number | {'type': '`Number`', 'df': "Applies or references the 'FillMana' effect/state."} | 5 |
| `FlatLeech` | Number | {'type': '`Number`', 'df': "Applies or references the 'FlatLeech' effect/state."} | 5 |
| `ForceMoveAway` | Number | {'type': '`Number`', 'df': "Applies or references the 'ForceMoveAway' effect/state."} | 5 |
| `ForceMoveTowards` | Number | {'type': '`Number`', 'df': "Applies or references the 'ForceMoveTowards' effect/state."} | 5 |
| `HitExplosion` | Number | {'type': '`Number`', 'df': "Applies or references the 'HitExplosion' effect/state."} | 5 |
| [`Imprison`](./Enums.md#enum-imprison) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'Imprison' effect/state."} | 5 |
| `KnockbackDirectionIsFacingDirection` | Mixed | {'type': '`Enum/String`', 'df': "Applies or references the 'KnockbackDirectionIsFacingDirection' effect/state."} | 5 |
| `MonkStanceSwitch` | Number | {'type': '`Number`', 'df': "Applies or references the 'MonkStanceSwitch' effect/state."} | 5 |
| `MovementUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'MovementUp' effect/state."} | 5 |
| [`ObjectOnHit`](./Abilities_and_Spells.md#context-objectonhit) | Block | {'type': '`Enum/String`', 'df': 'Spawns a specific physics/item object upon impact.'} | 5 |
| [`ObjectOnHitEmpty`](./Enums.md#enum-objectonhitempty) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ObjectOnHitEmpty' effect/state."} | 5 |
| [`PopAndSpawn`](./Enums.md#enum-popandspawn) | Enum | {'type': '`Enum/String`', 'df': 'Destroys the target and replaces it with a new spawned entity.'} | 5 |
| `Purge` | Number | {'type': '`Number`', 'df': "Applies or references the 'Purge' effect/state."} | 5 |
| `RefreshMovePointsIfHit` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshMovePointsIfHit' effect/state."} | 5 |
| `Revive` | Number | {'type': '`Number`', 'df': "Applies or references the 'Revive' effect/state."} | 5 |
| `SafeDie` | Number | {'type': '`Number`', 'df': "Applies or references the 'SafeDie' effect/state."} | 5 |
| `SoulLink` | Number | {'type': '`Number`', 'df': "Applies or references the 'SoulLink' effect/state."} | 5 |
| `SpawnBearTrap` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpawnBearTrap' effect/state."} | 5 |
| [`SpawnRock`](./Arrays.md#array-spawnrock) | Array | {'type': '`Number`', 'df': "Applies or references the 'SpawnRock' effect/state."} | 5 |
| `Stealth` | Number | {'type': '`Number`', 'df': "Applies or references the 'Stealth' effect/state."} | 5 |
| `TempDamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempDamageUp' effect/state."} | 5 |
| `UpgradeRandomAbility` | Number | {'type': '`Number`', 'df': "Applies or references the 'UpgradeRandomAbility' effect/state."} | 5 |
| `Webbed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Webbed' effect/state."} | 5 |
| [`ApplyToConsumed`](./Abilities_and_Spells.md#context-applytoconsumed) | Block | {'type': '`Block`', 'df': "Redirects the nested effects to apply to the entity that just consumed this object. | 4 |
| [`ArcLightning`](./Abilities_and_Spells.md#context-arclightning) | Block | {'type': '`Block`', 'df': 'Executes a chain-lightning logic block that bounces between targets. | 4 |
| [`BurgleCoin`](./Arrays.md#array-burglecoin) | Array | {'type': '`Number`', 'df': "Applies or references the 'BurgleCoin' effect/state."} | 4 |
| `Charge` | Number | {'type': 'Number', 'df': "Applies or references the 'Charge' effect/state."} | 4 |
| [`Conditional_Familiar`](./Abilities_and_Spells.md#context-conditional_familiar) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is a familiar. | 4 |
| [`EnableWeather`](./Enums.md#enum-enableweather) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'EnableWeather' effect/state."} | 4 |
| `ExplosionIfHitSomething` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExplosionIfHitSomething' effect/state."} | 4 |
| `FaceCamera` | Number | {'type': '`Number`', 'df': "Applies or references the 'FaceCamera' effect/state."} | 4 |
| `Grappled` | Number | {'type': '`Number`', 'df': "Applies or references the 'Grappled' effect/state."} | 4 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 4 |
| [`LateStatusApplication`](./Abilities_and_Spells.md#context-latestatusapplication) | Block | {'type': '`Block`', 'df': "Applies a status effect after all primary damage and effects have fully resolved. | 4 |
| [`RandomStatDown`](./Arrays.md#array-randomstatdown) | Array | {'type': 'Number', 'df': "Applies or references the 'RandomStatDown' effect/state."} | 4 |
| `Reanimate` | Number | {'type': '`Number`', 'df': "Applies or references the 'Reanimate' effect/state."} | 4 |
| `RemoveActPoints` | Number | {'type': '`Number`', 'df': "Applies or references the 'RemoveActPoints' effect/state."} | 4 |
| `SendRock` | Number | {'type': '`Number`', 'df': "Applies or references the 'SendRock' effect/state."} | 4 |
| [`SpecificInjury`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'SpecificInjury' effect/state."} | 4 |
| [`SwitchMusic`](./Abilities_and_Spells.md#context-switchmusic) | Block | {'type': 'Block', 'df': 'Changes the background music track or layer during combat.'} | 4 |
| [`TakeBonusTurnWithStatus`](./Abilities_and_Spells.md#context-takebonusturnwithstatus) | Block | {'type': '`Block`', 'df': "Grants the character an immediate extra turn while afflicted with specific statuses. | 4 |
| [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication) | Block | {'type': '`Block`', 'df': "Delays the nested effects by a specified amount of real-time seconds. | 4 |
| [`UseAbility`](./Enums.md#enum-useability) | Enum | {'type': '`Enum/String`', 'df': 'Forces the character or target to instantly use a specified ability.'} | 4 |
| `VaporizeInanimate` | Number | {'type': '`Number`', 'df': "Applies or references the 'VaporizeInanimate' effect/state."} | 4 |
| [`ApplyMultipleTimes`](./Abilities_and_Spells.md#context-applymultipletimes) | Block | {'type': '`Block`', 'df': 'A loop block that executes its nested logic multiple times. | 3 |
| [`CatPartsSizeScaleStatus`](./Abilities_and_Spells.md#context-catpartssizescalestatus) | Block | {'type': '`Block`', 'df': 'Visually scales specific body parts of a character. | 3 |
| [`CollideWithConsumed`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'CollideWithConsumed' effect/state."} | 3 |
| [`Conditional_AffectedByElement`](./Abilities_and_Spells.md#context-conditional_affectedbyelement) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is currently afflicted by the specified element. | 3 |
| [`Conditional_FirstApplicationThisTurn`](./Abilities_and_Spells.md#context-conditional_firstapplicationthisturn) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 3 |
| [`Conditional_LastHit`](./Abilities_and_Spells.md#context-conditional_lasthit) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if this attack is the final hit of a multi-hit sequence. | 3 |
| `CorpseVaporizer` | Number | {'type': '`Number`', 'df': "Applies or references the 'CorpseVaporizer' effect/state."} | 3 |
| `CurrentWeaponDamageUp` | Number | {'type': 'Number', 'df': "Applies or references the 'CurrentWeaponDamageUp' effect/state."} | 3 |
| `DamageOrHealConditionally` | Number | {'type': 'Number', 'df': "Applies or references the 'DamageOrHealConditionally' effect/state."} | 3 |
| `DeleteObject` | Number | {'type': '`Number`', 'df': "Applies or references the 'DeleteObject' effect/state."} | 3 |
| `DestroyTrinket` | Number | {'type': '`Number`', 'df': "Applies or references the 'DestroyTrinket' effect/state."} | 3 |
| `DestroyWeapon` | Number | {'type': '`Number`', 'df': "Applies or references the 'DestroyWeapon' effect/state."} | 3 |
| `DestroyWeaponThrow` | Number | {'type': '`Number`', 'df': "Applies or references the 'DestroyWeaponThrow' effect/state."} | 3 |
| `Die` | Number | {'type': '`Number`', 'df': "Applies or references the 'Die' effect/state."} | 3 |
| `DisplaceTowardsSource` | Number | {'type': '`Number`', 'df': "Applies or references the 'DisplaceTowardsSource' effect/state."} | 3 |
| `Doomed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Doomed' effect/state."} | 3 |
| [`DoubleStatus`](./Enums.md#enum-doublestatus) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'DoubleStatus' effect/state."} | 3 |
| [`DustOnHit`](./Abilities_and_Spells.md#context-dustonhit) | Block | {'type': '`Block`', 'df': 'Spawns a specific particle or cloud object upon impact. | 3 |
| `ExtraBasicAttacks_Status` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExtraBasicAttacks_Status' effect/state."} | 3 |
| `ForceDisplace` | Number | {'type': '`Number`', 'df': "Applies or references the 'ForceDisplace' effect/state."} | 3 |
| `ForceMoveTowardsEnemies` | Mixed | {'type': '`Number`', 'df': "Applies or references the 'ForceMoveTowardsEnemies' effect/state."} | 3 |
| `InstantMaxHealthUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'InstantMaxHealthUp' effect/state."} | 3 |
| `KineticSpikes` | Number | {'type': 'Number', 'df': "Applies or references the 'KineticSpikes' effect/state."} | 3 |
| `MoveQuivered` | Number | {'type': 'Number', 'df': "Applies or references the 'MoveQuivered' effect/state."} | 3 |
| `NextAttackBonusRange` | Number | {'type': '`Number`', 'df': "Applies or references the 'NextAttackBonusRange' effect/state."} | 3 |
| `OverrideDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'OverrideDamage' effect/state."} | 3 |
| `PermanentConstitution` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentConstitution' effect/state."} | 3 |
| `PlayBackground` | Number | {'type': 'Number', 'df': "Applies or references the 'PlayBackground' effect/state."} | 3 |
| `PoisonLace` | Mixed | {'type': 'Number', 'df': "Applies or references the 'PoisonLace' effect/state."} | 3 |
| `PullSourceToTarget` | Number | {'type': '`Number`', 'df': "Applies or references the 'PullSourceToTarget' effect/state."} | 3 |
| `Reflect` | Number | {'type': '`Number`', 'df': "Applies or references the 'Reflect' effect/state."} | 3 |
| `RefreshWeaponAbility` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshWeaponAbility' effect/state."} | 3 |
| `RepairAll` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairAll' effect/state."} | 3 |
| `RepairOnKill` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairOnKill' effect/state."} | 3 |
| [`ReviveNextRound`](./Abilities_and_Spells.md#context-revivenextround) | Block | {'type': '`Number`', 'df': 'Queues the character to be resurrected at the start of the next combat round.'} | 3 |
| [`SetCrazyEyeBackgroundWeights`](./Abilities_and_Spells.md#context-setcrazyeyebackgroundweights) | Block | {'type': '`Block`', 'df': "Adjusts visual rendering weights for the 'Crazy Eye' background effect. | 3 |
| [`SpawnCustomTrap`](./Enums.md#enum-spawncustomtrap) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'SpawnCustomTrap' effect/state."} | 3 |
| `SpawnNeutralWebTrapOnMiss` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpawnNeutralWebTrapOnMiss' effect/state."} | 3 |
| `SpellDamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpellDamageUp' effect/state."} | 3 |
| [`Tangled`](./Abilities_and_Spells.md#context-tangled) | Block | {'type': '`Number`', 'df': 'Applies a tangled/ensnared status effect, often modifying visual sprites.'} | 3 |
| `TempSpeedUp` | Mixed | {'type': '`Number`', 'df': "Applies or references the 'TempSpeedUp' effect/state."} | 3 |
| [`TempStrengthUp`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'TempStrengthUp' effect/state."} | 3 |
| `VaporizeTarget` | Number | {'type': '`Number`', 'df': "Applies or references the 'VaporizeTarget' effect/state."} | 3 |
| `AddSpiritBombCharges` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddSpiritBombCharges' effect/state."} | 2 |
| [`BodyGuard`](./Abilities_and_Spells.md#context-bodyguard) | Block | {'type': '`Block`', 'df': 'Protects an ally by intercepting attacks directed at them. | 2 |
| `BonusKnockbackDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'BonusKnockbackDamage' effect/state."} | 2 |
| `Bound` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bound' effect/state."} | 2 |
| `CancelPrimedAbilities` | Number | {'type': '`Number`', 'df': "Applies or references the 'CancelPrimedAbilities' effect/state."} | 2 |
| [`ChangeFaction`](./Enums.md#enum-changefaction) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ChangeFaction' effect/state."} | 2 |
| `CharmedForceAttack` | Number | {'type': '`Number`', 'df': "Applies or references the 'CharmedForceAttack' effect/state."} | 2 |
| `CollideWithThrowTarget` | Number | {'type': '`Number`', 'df': "Applies or references the 'CollideWithThrowTarget' effect/state."} | 2 |
| [`Conditional_BadRoll`](./Abilities_and_Spells.md#context-conditional_badroll) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic based on a randomized bad outcome probability. | 2 |
| [`Conditional_BossOrBig`](./Abilities_and_Spells.md#context-conditional_bossorbig) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is a Boss or has a large size classification. | 2 |
| [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is the caster's summoned buddy/familiar. | 2 |
| [`Conditional_DestructibleCorpse`](./Abilities_and_Spells.md#context-conditional_destructiblecorpse) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is a corpse that can be destroyed or vaporized. | 2 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#context-conditional_healththreshold) | Block | {'type': 'Block', 'df': "Conditional trigger: Executes nested logic if the target's health falls below the specified threshold."} | 2 |
| [`Conditional_IsSelf`](./Abilities_and_Spells.md#context-conditional_isself) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is the caster themselves. | 2 |
| [`Conditional_NotAlly`](./Abilities_and_Spells.md#context-conditional_notally) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is NOT friendly to the caster. | 2 |
| [`Conditional_NotBossOrBig`](./Abilities_and_Spells.md#context-conditional_notbossorbig) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is NEITHER a Boss nor large. | 2 |
| [`Conditional_NotShielded`](./Abilities_and_Spells.md#context-conditional_notshielded) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target does NOT currently have a Shield status. | 2 |
| [`Conditional_OncePerBattle`](./Abilities_and_Spells.md#context-conditional_onceperbattle) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic only once per encounter/battle. | 2 |
| [`Conditional_Shielded`](./Abilities_and_Spells.md#context-conditional_shielded) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target currently has a Shield status. | 2 |
| [`CopySpells`](./Abilities_and_Spells.md#context-copyspells) | Block | {'type': '`Number`', 'df': "Duplicates existing spells currently in the character's hand."} | 2 |
| `Counterspell` | Number | {'type': '`Number`', 'df': "Applies or references the 'Counterspell' effect/state."} | 2 |
| `CritChanceUp` | Number | {'type': 'Number', 'df': "Applies or references the 'CritChanceUp' effect/state."} | 2 |
| `DamageBasedOnMissingHealth` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageBasedOnMissingHealth' effect/state."} | 2 |
| `DamageDistanceAOEFalloff` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageDistanceAOEFalloff' effect/state."} | 2 |
| `DamageTrinket` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageTrinket' effect/state."} | 2 |
| `DelayedFury` | Number | {'type': '`Number`', 'df': "Applies or references the 'DelayedFury' effect/state."} | 2 |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#context-destroyequipmentandattachparasite) | Block | {'type': 'Block', 'df': 'Removes an equipped item and replaces it with a parasite from a specified pool.'} | 2 |
| `DieViaAbilityInternally` | Number | {'type': '`Number`', 'df': "Applies or references the 'DieViaAbilityInternally' effect/state."} | 2 |
| `DiminishingHealthRegen` | Number | {'type': 'Number', 'df': "Applies or references the 'DiminishingHealthRegen' effect/state."} | 2 |
| `DisplaceToOriginalPosition` | Number | {'type': '`Number`', 'df': "Applies or references the 'DisplaceToOriginalPosition' effect/state."} | 2 |
| `DoubleCastSpell` | Number | {'type': '`Number`', 'df': "Applies or references the 'DoubleCastSpell' effect/state."} | 2 |
| `DoubleLoot` | Number | {'type': '`Number`', 'df': "Applies or references the 'DoubleLoot' effect/state."} | 2 |
| `FlowersOnHit` | Number | {'type': '`Number`', 'df': "Applies or references the 'FlowersOnHit' effect/state."} | 2 |
| `ForceMoveNonAlliesInRangeTowardsTile` | Number | {'type': '`Number`', 'df': "Applies or references the 'ForceMoveNonAlliesInRangeTowardsTile' effect/state."} | 2 |
| [`ForceMoveTowardsTaggedObject`](./Abilities_and_Spells.md#context-forcemovetowardstaggedobject) | Block | {'type': '`Block`', 'df': 'Forces the character to move towards the nearest object with a specific tag. | 2 |
| `FreeSpell` | Number | {'type': '`Number`', 'df': "Applies or references the 'FreeSpell' effect/state."} | 2 |
| `Hex` | Number | {'type': 'Number', 'df': "Applies or references the 'Hex' effect/state."} | 2 |
| `IgnoreDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'IgnoreDamage' effect/state."} | 2 |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ImmediateUseAbility' effect/state."} | 2 |
| [`ImmediateUseDirectionalAbility`](./Enums.md#enum-immediateusedirectionalability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ImmediateUseDirectionalAbility' effect/state."} | 2 |
| `JohnnyCriesForWashers` | Number | {'type': '`Number`', 'df': "Applies or references the 'JohnnyCriesForWashers' effect/state."} | 2 |
| [`KnockOutCoin`](./Abilities_and_Spells.md#context-knockoutcoin) | Block | {'type': '`Number`', 'df': 'Forces the target to drop coins.'} | 2 |
| `Knockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'Knockback' effect/state."} | 2 |
| `LeaveBehindRockOnKnockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'LeaveBehindRockOnKnockback' effect/state."} | 2 |
| `Lifesteal` | Number | {'type': 'Number', 'df': "Applies or references the 'Lifesteal' effect/state."} | 2 |
| `ManaLeeches` | Number | {'type': '`Number`', 'df': "Applies or references the 'ManaLeeches' effect/state."} | 2 |
| [`Math`](./Abilities_and_Spells.md#context-math) | Block | {'type': '`Block`', 'df': "Triggers the Tinkerer's Math ability sequence. | 2 |
| `MaxHPUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'MaxHPUp' effect/state."} | 2 |
| [`NextAttackSpecialCrit`](./Abilities_and_Spells.md#context-nextattackspecialcrit) | Block | {'type': '`Number`', 'df': "Modifies the character's next attack to have special critical properties."} | 2 |
| `Ostracized` | Number | {'type': 'Number', 'df': "Applies or references the 'Ostracized' effect/state."} | 2 |
| [`OverHealToStatuses`](./Abilities_and_Spells.md#context-overhealtostatuses) | Block | {'type': '`Block`', 'df': "Converts excessive healing beyond maximum health into specific status effects. | 2 |
| `PartialCleanse` | Number | {'type': '`Number`', 'df': "Applies or references the 'PartialCleanse' effect/state."} | 2 |
| `PermanentStrength` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentStrength' effect/state."} | 2 |
| `PermanentUpgradeRandomActive` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentUpgradeRandomActive' effect/state."} | 2 |
| `Possessed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Possessed' effect/state."} | 2 |
| `PullSourceToKnockbackImmuneTarget` | Number | {'type': '`Number`', 'df': "Applies or references the 'PullSourceToKnockbackImmuneTarget' effect/state."} | 2 |
| [`QuakeAreaChance`](./Abilities_and_Spells.md#context-quakeareachance) | Block | {'type': '`Block`', 'df': 'Provides a probability to trigger an earthquake Area of Effect. | 2 |
| [`RandomDistanceDisplace`](./Abilities_and_Spells.md#context-randomdistancedisplace) | Block | {'type': '`Number`', 'df': 'Displaces the target by a randomized distance.'} | 2 |
| [`RandomKnockback`](./Abilities_and_Spells.md#context-randomknockback) | Block | {'type': '`Block`', 'df': 'Applies a randomized amount of knockback force. | 2 |
| `RangeUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'RangeUp' effect/state."} | 2 |
| `RebukeDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'RebukeDamage' effect/state."} | 2 |
| `RemoveMovePoints` | Number | {'type': '`Number`', 'df': "Applies or references the 'RemoveMovePoints' effect/state."} | 2 |
| `RepairArmorCondition` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairArmorCondition' effect/state."} | 2 |
| `RepairWeapon` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairWeapon' effect/state."} | 2 |
| `RepairWeaponCondition` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairWeaponCondition' effect/state."} | 2 |
| `ResetArmorShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'ResetArmorShield' effect/state."} | 2 |
| `ScrambleEverything` | Number | {'type': '`Number`', 'df': "Applies or references the 'ScrambleEverything' effect/state."} | 2 |
| [`SelfStun`](./Arrays.md#array-selfstun) | Array | {'type': '`Number`', 'df': "Applies or references the 'SelfStun' effect/state."} | 2 |
| `SetShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'SetShield' effect/state."} | 2 |
| `Shatter` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shatter' effect/state."} | 2 |
| `SignalFinalBossShieldBroke` | Number | {'type': '`Number`', 'df': "Applies or references the 'SignalFinalBossShieldBroke' effect/state."} | 2 |
| [`SizeScale`](./Enums.md#enum-sizescale) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'SizeScale' effect/state."} | 2 |
| [`SmartMetronome`](./Abilities_and_Spells.md#context-smartmetronome) | Block | {'type': '`Number`', 'df': "Executes a 'smart' random ability that aims to be beneficial based on context."} | 2 |
| [`SpawnCoinAnywhere`](./Arrays.md#array-spawncoinanywhere) | Array | {'type': '`Number`', 'df': "Applies or references the 'SpawnCoinAnywhere' effect/state."} | 2 |
| [`SpawnFlames`](./Arrays.md#array-spawnflames) | Array | {'type': '`Array`', 'df': "Applies or references the 'SpawnFlames' effect/state."} | 2 |
| `SpeculativeMoveSelfCorpseOffMap` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state."} | 2 |
| `StanceSwitchToMelee` | Number | {'type': '`Number`', 'df': "Applies or references the 'StanceSwitchToMelee' effect/state."} | 2 |
| `SwallowSmallCharacter` | Number | {'type': '`Number`', 'df': "Applies or references the 'SwallowSmallCharacter' effect/state."} | 2 |
| [`TakeBonusTurnWithAIControl`](./Abilities_and_Spells.md#context-takebonusturnwithaicontrol) | Block | {'type': '`Block`', 'df': 'Grants the character an immediate extra turn, but forces the AI to control them during it. | 2 |
| `TempCritChanceUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempCritChanceUp' effect/state."} | 2 |
| [`TempDexterityUp`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'TempDexterityUp' effect/state."} | 2 |
| `TempInitiativeChange` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempInitiativeChange' effect/state."} | 2 |
| `TempMovement` | Mixed | {'type': '`Number`', 'df': "Applies or references the 'TempMovement' effect/state."} | 2 |
| `TempSpellDamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempSpellDamageUp' effect/state."} | 2 |
| `TempTrampleUntilSettled` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempTrampleUntilSettled' effect/state."} | 2 |
| `TradeLife` | Number | {'type': '`Number`', 'df': "Applies or references the 'TradeLife' effect/state."} | 2 |
| `TrailBlazer` | Mixed | {'type': '`Number`', 'df': "Applies or references the 'TrailBlazer' effect/state."} | 2 |
| `Trample` | Number | {'type': '`Number`', 'df': "Applies or references the 'Trample' effect/state."} | 2 |
| `TriggerDOTStatuses` | Number | {'type': '`Number`', 'df': "Applies or references the 'TriggerDOTStatuses' effect/state."} | 2 |
| `AIFavorLowHealth` | Number | {'type': '`Number`', 'df': "Applies or references the 'AIFavorLowHealth' effect/state."} | 1 |
| `AlliesTakeExtraTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'AlliesTakeExtraTurn' effect/state."} | 1 |
| [`AlternateIdleAnimation`](./Enums.md#enum-alternateidleanimation) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'AlternateIdleAnimation' effect/state."} | 1 |
| `ApplyShieldToApplierBasedOnMaxHealth` | Number | {'type': '`Number`', 'df': "Applies or references the 'ApplyShieldToApplierBasedOnMaxHealth' effect/state."} | 1 |
| [`ApplyStatusesNextTurnBegin`](./Abilities_and_Spells.md#context-applystatusesnextturnbegin) | Block | {'type': '`Block`', 'df': "Delays the application of the nested status effects until the start of the target's next turn. | 1 |
| [`ApplyToOthersWithSharedTagAndFaction`](./Abilities_and_Spells.md#context-applytootherswithsharedtagandfaction) | Block | {'type': '`Block`', 'df': "Redirects the nested effects to apply to all other entities on the map that share the target's faction and specified tags. | 1 |
| [`ApplyToRandomClosestAlly`](./Abilities_and_Spells.md#context-applytorandomclosestally) | Block | {'type': '`Block`', 'df': "Redirects the nested effects to apply to the nearest friendly unit. If tied, chooses randomly among them. | 1 |
| `Attraction` | Number | {'type': 'Number', 'df': "Applies or references the 'Attraction' effect/state."} | 1 |
| `Bloodzerked` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bloodzerked' effect/state."} | 1 |
| `BombRatTurtle` | Number | {'type': '`Number`', 'df': "Applies or references the 'BombRatTurtle' effect/state."} | 1 |
| `BonusDamageBasedOnMana` | Number | {'type': '`Number`', 'df': "Applies or references the 'BonusDamageBasedOnMana' effect/state."} | 1 |
| `BypassRockKnockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'BypassRockKnockback' effect/state."} | 1 |
| `CanceledQueuedInput` | Number | {'type': '`Number`', 'df': "Applies or references the 'CanceledQueuedInput' effect/state."} | 1 |
| `CaptureFamiliar` | Number | {'type': 'Number', 'df': "Applies or references the 'CaptureFamiliar' effect/state."} | 1 |
| `ChampionUpgradeNextMinion` | Number | {'type': '`Number`', 'df': "Applies or references the 'ChampionUpgradeNextMinion' effect/state."} | 1 |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | {'type': 'Enum/String', 'df': "Applies or references the 'ChangeTilesUnder' effect/state."} | 1 |
| `ChaosBossFlipMidTeleport` | Number | {'type': '`Number`', 'df': "Applies or references the 'ChaosBossFlipMidTeleport' effect/state."} | 1 |
| `ChaosBossFormChange` | Number | {'type': '`Number`', 'df': "Applies or references the 'ChaosBossFormChange' effect/state."} | 1 |
| `ChargeFists` | Number | {'type': '`Number`', 'df': "Applies or references the 'ChargeFists' effect/state."} | 1 |
| `CharmedFacingForceAttack` | Number | {'type': '`Number`', 'df': "Applies or references the 'CharmedFacingForceAttack' effect/state."} | 1 |
| `ClearFinalBossBattlefield` | Number | {'type': '`Number`', 'df': "Applies or references the 'ClearFinalBossBattlefield' effect/state."} | 1 |
| `CloneWeaponTemp` | Number | {'type': '`Number`', 'df': "Applies or references the 'CloneWeaponTemp' effect/state."} | 1 |
| [`CoinTossBounce`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'CoinTossBounce' effect/state."} | 1 |
| `Conditional_AbilityTargetIsSelf` | Block | {'type': '`Block`', 'df': 'Conditional constraint. Nested properties only trigger if this is true.'} | 1 |
| [`Conditional_ActiveWeather_Any`](./Abilities_and_Spells.md#context-conditional_activeweather_any) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic if the current map weather matches any in the list. | 1 |
| [`Conditional_Backstab`](./Abilities_and_Spells.md#context-conditional_backstab) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the attacker is positioned behind the target. | 1 |
| [`Conditional_CanBeHealed`](./Abilities_and_Spells.md#context-conditional_canbehealed) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target's health is below maximum and they are capable of receiving healing. | 1 |
| [`Conditional_DebuffRoll`](./Abilities_and_Spells.md#context-conditional_debuffroll) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic based on a randomized debuff probability. | 1 |
| [`Conditional_Displaceable`](./Abilities_and_Spells.md#context-conditional_displaceable) | Block | {'type': 'Block', 'df': 'Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement.'} | 1 |
| [`Conditional_HasCleansableDebuffs`](./Abilities_and_Spells.md#context-conditional_hascleansabledebuffs) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target currently has negative status effects that can be cleansed. | 1 |
| [`Conditional_IsTrample`](./Abilities_and_Spells.md#context-conditional_istrample) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the current movement/attack is classified as a trample. | 1 |
| [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#context-conditional_livingplayercat) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic if the target is an alive player-controlled cat. | 1 |
| [`Conditional_NotBig`](./Abilities_and_Spells.md#context-conditional_notbig) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is NOT classified as large. | 1 |
| [`Conditional_RandomChance`](./Abilities_and_Spells.md#context-conditional_randomchance) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic based on a flat percentage random roll. | 1 |
| [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#context-conditional_sourceabilityhastag) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic if the ability that triggered this effect has the specified tag. | 1 |
| [`Conditional_SourceHasStatus`](./Abilities_and_Spells.md#context-conditional_sourcehasstatus) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the caster currently has the specified status. | 1 |
| [`ConjureSingleUseBonusAbility`](./Enums.md#enum-conjuresingleusebonusability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ConjureSingleUseBonusAbility' effect/state."} | 1 |
| [`CreateGlobalModifiers`](./Abilities_and_Spells.md#context-createglobalmodifiers) | Block | {'type': 'Block', 'df': 'Generates global map or encounter rules/modifiers.'} | 1 |
| `CurrentWeaponAddElectricElement` | Number | {'type': '`Number`', 'df': "Applies or references the 'CurrentWeaponAddElectricElement' effect/state."} | 1 |
| `DamageWeapon` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageWeapon' effect/state."} | 1 |
| [`DeathwormUnderground`](./Enums.md#enum-deathwormunderground) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'DeathwormUnderground' effect/state."} | 1 |
| `DecoySwapper` | Number | {'type': '`Number`', 'df': "Applies or references the 'DecoySwapper' effect/state."} | 1 |
| [`DelayCastAbility`](./Abilities_and_Spells.md#context-delaycastability) | Block | {'type': '`Block`', 'df': 'Queues an ability to be cast automatically after a certain delay or trigger.'} | 1 |
| [`DelayedWindCone`](./Abilities_and_Spells.md#context-delayedwindcone) | Block | {'type': '`Block`', 'df': 'Creates a delayed Area of Effect cone. | 1 |
| `DeleteTraps` | Number | {'type': '`Number`', 'df': "Applies or references the 'DeleteTraps' effect/state."} | 1 |
| `DestroyNeckArmor` | Number | {'type': '`Number`', 'df': "Applies or references the 'DestroyNeckArmor' effect/state."} | 1 |
| `DieViolently` | Number | {'type': 'Number', 'df': "Applies or references the 'DieViolently' effect/state."} | 1 |
| [`DinoLegAnimation`](./Enums.md#enum-dinoleganimation) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'DinoLegAnimation' effect/state."} | 1 |
| `Disguised` | Number | {'type': '`Number`', 'df': "Applies or references the 'Disguised' effect/state."} | 1 |
| `DissolveRandomArmorPiece` | Number | {'type': '`Number`', 'df': "Applies or references the 'DissolveRandomArmorPiece' effect/state."} | 1 |
| `DontHealEnemies` | Number | {'type': '`Number`', 'df': "Applies or references the 'DontHealEnemies' effect/state."} | 1 |
| `DoubleCast` | Number | {'type': '`Number`', 'df': "Applies or references the 'DoubleCast' effect/state."} | 1 |
| `DoubleCastSpellsEachTurn_Status` | Number | {'type': '`Number`', 'df': "Applies or references the 'DoubleCastSpellsEachTurn_Status' effect/state."} | 1 |
| `DrainAllyCatsForFleshGolem` | Number | {'type': '`Number`', 'df': "Applies or references the 'DrainAllyCatsForFleshGolem' effect/state."} | 1 |
| `DrinkWater` | Number | {'type': '`Number`', 'df': "Applies or references the 'DrinkWater' effect/state."} | 1 |
| `DuplicateRandomEquippedItem` | Number | {'type': '`Number`', 'df': "Applies or references the 'DuplicateRandomEquippedItem' effect/state."} | 1 |
| `EliteUpgradeNextMinion` | Number | {'type': '`Number`', 'df': "Applies or references the 'EliteUpgradeNextMinion' effect/state."} | 1 |
| `EmptyMind` | Number | {'type': '`Number`', 'df': "Applies or references the 'EmptyMind' effect/state."} | 1 |
| `Enlarge` | Number | {'type': '`Number`', 'df': "Applies or references the 'Enlarge' effect/state."} | 1 |
| [`EnterMount`](./Enums.md#enum-entermount) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'EnterMount' effect/state."} | 1 |
| `ExistUntilIdleUpkeep` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExistUntilIdleUpkeep' effect/state."} | 1 |
| `ExplodeCharacter` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExplodeCharacter' effect/state."} | 1 |
| `ExplodeCharacter_DeathBloom` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExplodeCharacter_DeathBloom' effect/state."} | 1 |
| `ExplodeCharacter_DeathBloom2` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExplodeCharacter_DeathBloom2' effect/state."} | 1 |
| `ExplodeCharacter_NoDie` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExplodeCharacter_NoDie' effect/state."} | 1 |
| `ExtraBasicMoves_Status` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExtraBasicMoves_Status' effect/state."} | 1 |
| `FactionConversion` | Number | {'type': '`Number`', 'df': "Applies or references the 'FactionConversion' effect/state."} | 1 |
| `FactionDisguiseSource` | Number | {'type': '`Number`', 'df': "Applies or references the 'FactionDisguiseSource' effect/state."} | 1 |
| `FastKnockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'FastKnockback' effect/state."} | 1 |
| `FinalBossQueueBeam` | Number | {'type': '`Number`', 'df': "Applies or references the 'FinalBossQueueBeam' effect/state."} | 1 |
| `FireArmor` | Number | {'type': '`Number`', 'df': "Applies or references the 'FireArmor' effect/state."} | 1 |
| `FireArmor2` | Number | {'type': '`Number`', 'df': "Applies or references the 'FireArmor2' effect/state."} | 1 |
| `FlatAIBonus` | Number | {'type': '`Number`', 'df': "Applies or references the 'FlatAIBonus' effect/state."} | 1 |
| `ForceCollectsPickups` | Number | {'type': '`Number`', 'df': "Applies or references the 'ForceCollectsPickups' effect/state."} | 1 |
| `ForceMoveAndAttack` | Number | {'type': '`Number`', 'df': "Applies or references the 'ForceMoveAndAttack' effect/state."} | 1 |
| `ForceTransferWeapon` | Number | {'type': '`Number`', 'df': "Applies or references the 'ForceTransferWeapon' effect/state."} | 1 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | {'type': 'Enum/String', 'df': "Applies or references the 'ForceUseAbility' effect/state."} | 1 |
| [`GainCoinsRange`](./Abilities_and_Spells.md#context-gaincoinsrange) | Block | {'type': '`Block`', 'df': 'Grants the player a randomized amount of coins within a min/max range.'} | 1 |
| `GenericBuff` | Number | {'type': '`Number`', 'df': "Applies or references the 'GenericBuff' effect/state."} | 1 |
| `GiveBoundItemToTarget` | Number | {'type': '`Number`', 'df': "Applies or references the 'GiveBoundItemToTarget' effect/state."} | 1 |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | {'type': 'Enum/String', 'df': "Applies or references the 'GlobalSpawnCharacter' effect/state."} | 1 |
| `HealPercentMaxHP` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealPercentMaxHP' effect/state."} | 1 |
| `HealRandomInjury` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealRandomInjury' effect/state."} | 1 |
| `HealTo` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealTo' effect/state."} | 1 |
| `HeavyHits` | Number | {'type': '`Number`', 'df': "Applies or references the 'HeavyHits' effect/state."} | 1 |
| `IceArmor` | Number | {'type': '`Number`', 'df': "Applies or references the 'IceArmor' effect/state."} | 1 |
| `IgnoreDebuffs` | Number | {'type': '`Number`', 'df': "Applies or references the 'IgnoreDebuffs' effect/state."} | 1 |
| [`IncAuxCounterCycle`](./Abilities_and_Spells.md#context-incauxcountercycle) | Block | {'type': '`Block`', 'df': 'Increments a generic auxiliary counter, looping back to 0 when it exceeds the maximum. | 1 |
| `IncreaseCumulativeBlastDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'IncreaseCumulativeBlastDamage' effect/state."} | 1 |
| `IncreaseItemAuxOnKill` | Number | {'type': '`Number`', 'df': "Applies or references the 'IncreaseItemAuxOnKill' effect/state."} | 1 |
| `Infested` | Number | {'type': 'Number', 'df': "Applies or references the 'Infested' effect/state."} | 1 |
| `InterchangeMoveActPoints` | Number | {'type': '`Number`', 'df': "Applies or references the 'InterchangeMoveActPoints' effect/state."} | 1 |
| `Invulnerable` | Number | {'type': '`Number`', 'df': "Applies or references the 'Invulnerable' effect/state."} | 1 |
| `MadnessChanceOnTurnBegin` | Number | {'type': 'Number', 'df': "Applies or references the 'MadnessChanceOnTurnBegin' effect/state."} | 1 |
| `MakeWeaponUnbreakable` | Number | {'type': '`Number`', 'df': "Applies or references the 'MakeWeaponUnbreakable' effect/state."} | 1 |
| `ManaStealToHealth` | Number | {'type': '`Number`', 'df': "Applies or references the 'ManaStealToHealth' effect/state."} | 1 |
| `ManglerAttack` | Number | {'type': '`Number`', 'df': "Applies or references the 'ManglerAttack' effect/state."} | 1 |
| `ManglerShuffle` | Boolean | {'type': '`Boolean`', 'df': "Applies or references the 'ManglerShuffle' effect/state."} | 1 |
| `MassAttackThis` | Number | {'type': '`Number`', 'df': "Applies or references the 'MassAttackThis' effect/state."} | 1 |
| `Meaty` | Number | {'type': '`Number`', 'df': "Applies or references the 'Meaty' effect/state."} | 1 |
| `MimicMetronome` | Number | {'type': '`Number`', 'df': "Applies or references the 'MimicMetronome' effect/state."} | 1 |
| `MotherTumorDebugForcePass` | Number | {'type': '`Number`', 'df': "Applies or references the 'MotherTumorDebugForcePass' effect/state."} | 1 |
| `Muted` | Number | {'type': '`Number`', 'df': "Applies or references the 'Muted' effect/state."} | 1 |
| `NextAbilityHeals` | Number | {'type': '`Number`', 'df': "Applies or references the 'NextAbilityHeals' effect/state."} | 1 |
| `NextActionLuckUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'NextActionLuckUp' effect/state."} | 1 |
| [`NextBasicAttackCritsThisTurn`](./Abilities_and_Spells.md#context-nextbasicattackcritsthisturn) | Block | {'type': '`Block`', 'df': 'Guarantees the next basic attack executed this turn will be a critical hit. | 1 |
| [`NextBattleStatusStacks`](./Abilities_and_Spells.md#context-nextbattlestatusstacks) | Block | {'type': '`Block`', 'df': "Carries over the specified status effects into the next encounter/battle. | 1 |
| `NextDamageReduceAndHealAllies` | Number | {'type': '`Number`', 'df': "Applies or references the 'NextDamageReduceAndHealAllies' effect/state."} | 1 |
| `NextTurnDoubleRangedDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'NextTurnDoubleRangedDamage' effect/state."} | 1 |
| `NonStackingDivineShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'NonStackingDivineShield' effect/state."} | 1 |
| [`ObjectOnHitFullyEmpty`](./Enums.md#enum-objectonhitfullyempty) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ObjectOnHitFullyEmpty' effect/state."} | 1 |
| `OverHealToShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'OverHealToShield' effect/state."} | 1 |
| [`OverrideChainKnockbackDamage`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'OverrideChainKnockbackDamage' effect/state."} | 1 |
| `PermanentCharisma` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentCharisma' effect/state."} | 1 |
| `PermanentDexterity` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentDexterity' effect/state."} | 1 |
| `PermanentImmobile` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentImmobile' effect/state."} | 1 |
| `PermanentIntelligence` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentIntelligence' effect/state."} | 1 |
| `PermanentLuck` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentLuck' effect/state."} | 1 |
| `PermanentSpeed` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentSpeed' effect/state."} | 1 |
| `PermanentUpgradeRandomActiveOrPassive` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentUpgradeRandomActiveOrPassive' effect/state."} | 1 |
| [`PoolMetronome`](./Abilities_and_Spells.md#context-poolmetronome) | Block | {'type': '`Block`', 'df': 'Executes a random ability drawn from a specific pool. | 1 |
| `ProbeCharmed` | Number | {'type': '`Number`', 'df': "Applies or references the 'ProbeCharmed' effect/state."} | 1 |
| [`QueueUseAbility`](./Enums.md#enum-queueuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'QueueUseAbility' effect/state."} | 1 |
| `RNGCannonRandomDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'RNGCannonRandomDamage' effect/state."} | 1 |
| `RandomKnockbackDirection` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomKnockbackDirection' effect/state."} | 1 |
| `RandomPermanentStat` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomPermanentStat' effect/state."} | 1 |
| `ReduceManaCost` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReduceManaCost' effect/state."} | 1 |
| `ReduceManaCostExcludeBrainstorm` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReduceManaCostExcludeBrainstorm' effect/state."} | 1 |
| `ReformMoonHead` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReformMoonHead' effect/state."} | 1 |
| `RefreshItemAbilities` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshItemAbilities' effect/state."} | 1 |
| `RefreshNonManaItemAbilities` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshNonManaItemAbilities' effect/state."} | 1 |
| `RefreshOncePerFightAbilities` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshOncePerFightAbilities' effect/state."} | 1 |
| `Regurge` | Number | {'type': '`Number`', 'df': "Applies or references the 'Regurge' effect/state."} | 1 |
| [`RemoveStatusStacks`](./Abilities_and_Spells.md#context-removestatusstacks) | Block | {'type': '`Block`', 'df': 'Removes a specific number of stacks of a status effect. | 1 |
| `RepairAllCondition` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairAllCondition' effect/state."} | 1 |
| `RerollEnemy` | Number | {'type': '`Number`', 'df': "Applies or references the 'RerollEnemy' effect/state."} | 1 |
| `ReturnDinoLegs` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReturnDinoLegs' effect/state."} | 1 |
| `ScatterRandomPickups` | Number | {'type': '`Number`', 'df': "Applies or references the 'ScatterRandomPickups' effect/state."} | 1 |
| [`ScrambleLastUsedSpell`](./Abilities_and_Spells.md#context-scramblelastusedspell) | Block | {'type': '`Block`', 'df': 'Randomizes or scrambles the properties of the last spell cast. | 1 |
| [`SetDefaultFace`](./Enums.md#enum-setdefaultface) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'SetDefaultFace' effect/state."} | 1 |
| `ShadowCrit` | Number | {'type': '`Number`', 'df': "Applies or references the 'ShadowCrit' effect/state."} | 1 |
| `ShootHereCommand` | Number | {'type': '`Number`', 'df': "Applies or references the 'ShootHereCommand' effect/state."} | 1 |
| `ShootHereReceiver` | Number | {'type': '`Number`', 'df': "Applies or references the 'ShootHereReceiver' effect/state."} | 1 |
| `ShortCircuit` | Number | {'type': '`Number`', 'df': "Applies or references the 'ShortCircuit' effect/state."} | 1 |
| `SmallHitExplosion` | Number | {'type': '`Number`', 'df': "Applies or references the 'SmallHitExplosion' effect/state."} | 1 |
| `SmellBlood` | Number | {'type': '`Number`', 'df': "Applies or references the 'SmellBlood' effect/state."} | 1 |
| [`SoundEventOnHit`](./Enums.md#enum-soundeventonhit) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'SoundEventOnHit' effect/state."} | 1 |
| [`SourceSwapsBackEndOfTurn`](./Enums.md#enum-sourceswapsbackendofturn) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'SourceSwapsBackEndOfTurn' effect/state."} | 1 |
| `SpawnWebTrap` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpawnWebTrap' effect/state."} | 1 |
| [`SpecialBossMultipartInstakill`](./Enums.md#enum-specialbossmultipartinstakill) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'SpecialBossMultipartInstakill' effect/state."} | 1 |
| `SpellShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpellShield' effect/state."} | 1 |
| `SpitConsumed` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpitConsumed' effect/state."} | 1 |
| `SplashDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'SplashDamage' effect/state."} | 1 |
| [`SpreadDisease`](./Abilities_and_Spells.md#context-spreaddisease) | Block | {'type': '`Block`', 'df': 'Provides a chance to transmit a disease status to adjacent targets. | 1 |
| `StackingSandstorm` | Number | {'type': '`Number`', 'df': "Applies or references the 'StackingSandstorm' effect/state."} | 1 |
| `StatBounty` | Number | {'type': '`Number`', 'df': "Applies or references the 'StatBounty' effect/state."} | 1 |
| [`StatusGroup`](./Abilities_and_Spells.md#context-statusgroup) | Block | {'type': '`Block`', 'df': "Groups multiple status effects together for batch application. | 1 |
| `StealDemonicGlyph` | Number | {'type': '`Number`', 'df': "Applies or references the 'StealDemonicGlyph' effect/state."} | 1 |
| [`StealEquipment`](./Enums.md#enum-stealequipment) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'StealEquipment' effect/state."} | 1 |
| `StealTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'StealTurn' effect/state."} | 1 |
| `StealthCritChance` | Number | {'type': '`Number`', 'df': "Applies or references the 'StealthCritChance' effect/state."} | 1 |
| `SwapHighestAndLowestStat` | Number | {'type': '`Number`', 'df': "Applies or references the 'SwapHighestAndLowestStat' effect/state."} | 1 |
| [`SwapWeapon`](./Abilities_and_Spells.md#context-swapweapon) | Block | {'type': '`Block`', 'df': "Replaces the character's currently equipped weapon with one from a specified pool. | 1 |
| `Switcheroo` | Number | {'type': '`Number`', 'df': "Applies or references the 'Switcheroo' effect/state."} | 1 |
| `T3HitlerTriggerInitialSpawns` | Number | {'type': '`Number`', 'df': "Applies or references the 'T3HitlerTriggerInitialSpawns' effect/state."} | 1 |
| [`TagMetronome`](./Enums.md#enum-tagmetronome) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'TagMetronome' effect/state."} | 1 |
| `TakeExtraTurnEndOfRound` | Number | {'type': '`Number`', 'df': "Applies or references the 'TakeExtraTurnEndOfRound' effect/state."} | 1 |
| `TargetedMetronome` | Number | {'type': '`Number`', 'df': "Applies or references the 'TargetedMetronome' effect/state."} | 1 |
| `Taunting` | Number | {'type': '`Number`', 'df': "Applies or references the 'Taunting' effect/state."} | 1 |
| [`TeamBonusAbility`](./Enums.md#enum-teambonusability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'TeamBonusAbility' effect/state."} | 1 |
| [`TeleportBackAtTurnEnd`](./Enums.md#enum-teleportbackatturnend) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'TeleportBackAtTurnEnd' effect/state."} | 1 |
| `TempBackstab` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempBackstab' effect/state."} | 1 |
| `TempBackstabBleed` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempBackstabBleed' effect/state."} | 1 |
| `TempBackstabPiercing` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempBackstabPiercing' effect/state."} | 1 |
| `TempBackstabPoison` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempBackstabPoison' effect/state."} | 1 |
| `TempBasicAttackBonusAOE` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempBasicAttackBonusAOE' effect/state."} | 1 |
| `TempBonusKnockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempBonusKnockback' effect/state."} | 1 |
| `TempBonusKnockbackDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempBonusKnockbackDamage' effect/state."} | 1 |
| `TempCounterAttack` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempCounterAttack' effect/state."} | 1 |
| `TempInjuryImmunity` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempInjuryImmunity' effect/state."} | 1 |
| `TempLuckUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempLuckUp' effect/state."} | 1 |
| `TempManaCostReduction` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempManaCostReduction' effect/state."} | 1 |
| `TempPenetrate` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempPenetrate' effect/state."} | 1 |
| `TempPreEmptiveCounterAttack` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempPreEmptiveCounterAttack' effect/state."} | 1 |
| `ThornsDamageImmuneUntilSettled` | Number | {'type': '`Number`', 'df': "Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state."} | 1 |
| [`TickDownStatus`](./Enums.md#enum-tickdownstatus) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'TickDownStatus' effect/state."} | 1 |
| `TileDamageImmuneUntilSettled` | Number | {'type': '`Number`', 'df': "Applies or references the 'TileDamageImmuneUntilSettled' effect/state."} | 1 |
| `TilesMovedToCritChance` | Number | {'type': '`Number`', 'df': "Applies or references the 'TilesMovedToCritChance' effect/state."} | 1 |
| `TilesMovedToMana` | Number | {'type': '`Number`', 'df': "Applies or references the 'TilesMovedToMana' effect/state."} | 1 |
| [`TilesMovedToNeighborHeal`](./Enums.md#enum-tilesmovedtoneighborheal) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'TilesMovedToNeighborHeal' effect/state."} | 1 |
| `TilesMovedToStrength` | Number | {'type': '`Number`', 'df': "Applies or references the 'TilesMovedToStrength' effect/state."} | 1 |
| `TowerDefenseStatus` | Number | {'type': '`Number`', 'df': "Applies or references the 'TowerDefenseStatus' effect/state."} | 1 |
| `TowerDefenseStatus2` | Number | {'type': '`Number`', 'df': "Applies or references the 'TowerDefenseStatus2' effect/state."} | 1 |
| [`TransformBasicMove`](./Enums.md#enum-transformbasicmove) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'TransformBasicMove' effect/state."} | 1 |
| [`TransformEquipment`](./Abilities_and_Spells.md#context-transformequipment) | Block | {'type': '`Block`', 'df': 'Upgrades or transforms a specific equipped item into another. | 1 |
| [`TransformNow`](./Enums.md#enum-transformnow) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'TransformNow' effect/state."} | 1 |
| `Trapper_Status` | Number | {'type': '`Number`', 'df': "Applies or references the 'Trapper_Status' effect/state."} | 1 |
| `TriggerGameEnding` | Number | {'type': '`Number`', 'df': "Applies or references the 'TriggerGameEnding' effect/state."} | 1 |
| `TriggerMotherConsume` | Number | {'type': '`Number`', 'df': "Applies or references the 'TriggerMotherConsume' effect/state."} | 1 |
| `TriggerMotherGrow` | Number | {'type': '`Number`', 'df': "Applies or references the 'TriggerMotherGrow' effect/state."} | 1 |
| `TurnAround` | Number | {'type': '`Number`', 'df': "Applies or references the 'TurnAround' effect/state."} | 1 |
| [`TurnControlDelay`](./Enums.md#enum-turncontroldelay) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'TurnControlDelay' effect/state."} | 1 |
| `TurnRight` | Number | {'type': '`Number`', 'df': "Applies or references the 'TurnRight' effect/state."} | 1 |
| `UndoDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'UndoDamage' effect/state."} | 1 |
| [`UseMoveAbilityWithAI`](./Abilities_and_Spells.md#context-usemoveabilitywithai) | Block | {'type': '`Block`', 'df': 'Forces the character to execute a movement ability using specific AI weights. | 1 |
| [`VaporizeCorpseFlipAdvantage`](./Arrays.md#array-vaporizecorpseflipadvantage) | Array | {'type': '`Array`', 'df': "Applies or references the 'VaporizeCorpseFlipAdvantage' effect/state."} | 1 |
| `VaporizeDice` | Number | {'type': '`Number`', 'df': "Applies or references the 'VaporizeDice' effect/state."} | 1 |
| [`VisualCountDownThenApplyStatus`](./Abilities_and_Spells.md#context-visualcountdownthenapplystatus) | Block | {'type': '`Block`', 'df': "Displays a visual countdown above the target before applying the nested effects. | 1 |
| [`WaggleClone`](./Abilities_and_Spells.md#context-waggleclone) | Block | {'type': '`Block`', 'df': 'Spawns visual clones or alternative hitbox variants of the projectile. | 1 |

</details>

---

### Context: `target`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1862

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_range` | Number | {'type': '`Number`', 'df': 'The maximum and minimum distance required to cast.'} | 1088 |
| `max_aoe` | Number | {'type': '`Number`', 'df': 'The maximum and minimum radius/length of the AoE.'} | 795 |
| `min_range` | Number | {'type': '`Number`', 'df': 'The maximum and minimum distance required to cast.'} | 583 |
| [`target_mode`](./Enums.md#enum-target_mode) | Enum | {'type': '`Enum/String`', 'df': 'How the cursor operates (`tile`, `direction`, `none`).'} | 503 |
| [`restrictions`](./Arrays.md#array-restrictions) | Array | {'type': '`Enum/String`', 'df': 'Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`).'} | 463 |
| [`aoe_mode`](./Enums.md#enum-aoe_mode) | Enum | {'type': '`Enum/String`', 'df': 'The shape of the area (`standard`, `line`, `cross`, `square`, `custom`).'} | 432 |
| [`knockback_mode`](./Enums.md#enum-knockback_mode) | Enum | {'type': '`Enum/String`', 'df': 'How physics vectors apply (`character_to_tile`, `pull_to_character`, `zero`, `orientation`).'} | 265 |
| `min_aoe` | Mixed | {'type': '`Number`', 'df': 'The maximum and minimum radius/length of the AoE.'} | 253 |
| `aoe_excludes_self` | Boolean | {'type': '`Boolean`', 'df': 'Prevents the AoE from hitting the caster.'} | 241 |
| [`aoe_restrictions`](./Arrays.md#array-aoe_restrictions) | Array | {'type': '`Array`', 'df': 'Array of conditions the AoE tiles must meet (e.g., `must_have_line_of_sight_unpurgable`).'} | 197 |
| `aoe_considers_character_size` | Boolean | {'type': '`Boolean`', 'df': "Scales the AoE based on the caster's tile size (e.g., 2x2)."} | 170 |
| [`range_mode`](./Enums.md#enum-range_mode) | Enum | {'type': '`Enum/String`', 'df': 'How range is counted (`standard`, `ground_move`).'} | 114 |
| [`X_is`](./Enums.md#enum-x_is) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'X_is' effect/state."} | 86 |
| [`custom_aoe`](./Arrays.md#array-custom_aoe) | Array | {'type': '`Array`', 'df': 'Array of exact coordinates for a custom shape (e.g., `[[1, -1] [1, 0]]`).'} | 83 |
| `multihit` | Number | {'type': '`Number`', 'df': 'Hardcoded number of times the ability hits the target.'} | 62 |
| `max_targets` | Number | {'type': '`Number`', 'df': 'Limits on how many distinct entities can be targeted.'} | 56 |
| `range_excludes_blocking` | Boolean | {'type': '`Boolean`', 'df': 'Cannot target through walls/obstacles.'} | 53 |
| `prioritize_dont_change_direction` | Mixed | {'type': '`Number`', 'df': 'AI preference to maintain current facing angle.'} | 52 |
| [`target_requires_tag`](./Enums.md#enum-target_requires_tag) | Enum | {'type': '`Enum/String`', 'df': 'Target must possess this exact character tag.'} | 40 |
| [`aoe_symmetry`](./Enums.md#enum-aoe_symmetry) | Enum | {'type': '`Enum/String`', 'df': 'Determines if the AoE mirrors on axes.'} | 28 |
| `prioritize_face_camera` | Mixed | {'type': '`Number`', 'df': 'AI preference to face South.'} | 26 |
| `straight_shot` | Boolean | {'type': '`Boolean`', 'df': 'Ensures projectiles do not arc.'} | 24 |
| `can_multihit` | Boolean | {'type': '`Boolean`', 'df': 'If true, overlapping AoEs can hit the same target multiple times.'} | 17 |
| `allow_any_orientation` | Boolean | {'type': '`Boolean`', 'df': "Allows casting regardless of the character's facing direction."} | 16 |
| `range_considers_character_size` | Boolean | {'type': '`Boolean`', 'df': 'Range calculation accounts for large entities.'} | 16 |
| `throw_consumed_character` | Boolean | {'type': '`Boolean`', 'df': 'Throws the entity currently held/eaten.'} | 15 |
| `min_targets` | Number | {'type': '`Number`', 'df': 'Limits on how many distinct entities can be targeted.'} | 14 |
| `aoe_leading_edge_only` | Boolean | {'type': '`Boolean`', 'df': 'Only the outermost edge of the AoE shape applies effects.'} | 13 |
| `allow_diagonals` | Boolean | {'type': '`Boolean`', 'df': 'Allows targeting on diagonal grid axes.'} | 12 |
| `range_display_include_character_size` | Boolean | {'type': '`Boolean`', 'df': 'Visual: offsets the range indicator for 2x2 units.'} | 12 |
| `stagger_multihit_targets` | Boolean | {'type': '`Boolean`', 'df': 'Delays hits slightly between multiple targets.'} | 12 |
| `upgrade_straight_shot_to_piercing` | Boolean | {'type': '`Boolean`', 'df': 'Allows the projectile to pass through multiple targets.'} | 11 |
| `delayed_trigger` | Boolean | {'type': '`Boolean`', 'df': 'Delays the actual execution of the target effect.'} | 10 |
| `consider_trample` | Boolean | {'type': '`Boolean`', 'df': 'AI consideration for moving through units.'} | 9 |
| `N` | Number | {'type': '`Number`', 'df': 'Variable modifier parameter.'} | 7 |
| [`custom_range`](./Arrays.md#array-custom_range) | Array | {'type': '`Array`', 'df': 'Overrides standard range scaling.'} | 7 |
| `always_bounce` | Boolean | {'type': '`Boolean`', 'df': 'Forces the attack/projectile to bounce regardless of hit.'} | 6 |
| [`custom_aoe_util`](./Arrays.md#array-custom_aoe_util) | Array | {'type': '`Array`', 'df': 'Utility variants of custom AoE definitions.'} | 6 |
| `multihit_max` | Number | {'type': '`Number`', 'df': 'Variable limits for random multihit abilities.'} | 6 |
| `multihit_min` | Number | {'type': '`Number`', 'df': 'Variable limits for random multihit abilities.'} | 6 |
| `reorient_thrown_character` | Boolean | {'type': '`Boolean`', 'df': 'Forces a thrown entity to face a certain way.'} | 6 |
| [`toss_direction_restriction`](./Enums.md#enum-toss_direction_restriction) | Enum | {'type': '`Enum/String`', 'df': 'Limits which ways an entity can be tossed.'} | 6 |
| `aoe_hint_teamcast` | Boolean | {'type': '`Boolean`', 'df': 'Visual hint for cooperative casting abilities.'} | 5 |
| [`aoe_tile_requires_element`](./Enums.md#enum-aoe_tile_requires_element) | Enum | {'type': '`Enum/String`', 'df': 'Only affects tiles painted with a specific element.'} | 5 |
| `distance_sort_targets` | Mixed | {'type': '`Number`', 'df': 'Prioritizes targets based on proximity.'} | 5 |
| `dont_orient_aoe` | Boolean | {'type': '`Boolean`', 'df': 'Prevents the AoE shape from rotating with the character.'} | 5 |
| `hint_can_target_pickups` | Boolean | {'type': '`Boolean`', 'df': 'UI hint that the player can target items on the ground.'} | 5 |
| `max_bounces` | Number | {'type': '`Number`', 'df': 'Hard cap on how many times a bouncing effect can trigger.'} | 5 |
| `splash_damage_aoe_begin` | Number | {'type': '`Number`', 'df': 'At what radius splash damage starts applying.'} | 5 |
| [`aoe_chance`](./Enums.md#enum-aoe_chance) | Enum | {'type': '`Enum/String`', 'df': 'Percentage chance for the AoE to trigger.'} | 4 |
| `as_the_crow_flies` | Boolean | {'type': '`Boolean`', 'df': 'Calculates range ignoring all pathing terrain obstacles.'} | 4 |
| `force_ai_target_as_spell` | Boolean | {'type': '`Boolean`', 'df': 'Forces the AI to treat a physical move like a spell for targeting logic.'} | 4 |
| [`mouse_offset`](./Arrays.md#array-mouse_offset) | Array | {'type': '`Array`', 'df': 'Visual offset for the targeting cursor.'} | 4 |
| `range_display_include_aoe` | Boolean | {'type': '`Boolean`', 'df': 'Visual: shows the full AoE potential when previewing range.'} | 4 |
| `shotgun_mode` | Boolean | {'type': '`Boolean`', 'df': 'Deals more damage/hits if targets are closer.'} | 4 |
| `shuffle_tile_order` | Boolean | {'type': '`Boolean`', 'df': 'Randomizes the execution order of AoE tiles.'} | 4 |
| `upgrade_straight_shot_to_boomerang` | Boolean | {'type': '`Boolean`', 'df': 'Makes the projectile return to caster.'} | 4 |
| `dont_orient` | Boolean | {'type': '`Boolean`', 'df': 'Prevents the character from turning to face the target.'} | 3 |
| `low_health_character_threshold` | Mixed | {'type': '`Enum/String`', 'df': 'AI targeting threshold for seeking weak targets.'} | 3 |
| `randomize_target_within_range` | Number | {'type': '`Number`', 'df': "Picks a random valid tile instead of the user's click."} | 3 |
| [`special_tile_tag`](./Enums.md#enum-special_tile_tag) | Enum | {'type': '`Enum/String`', 'df': 'Targets only tiles with this specific tag.'} | 3 |
| `track_target` | Boolean | {'type': '`Boolean`', 'df': 'Projectile/Effect follows moving targets.'} | 3 |
| `corpse_priority` | Number | {'type': '`Number`', 'df': 'AI preference for targeting dead bodies.'} | 2 |
| `hint_can_target_empty` | Boolean | {'type': '`Boolean`', 'df': 'UI hint that the player can click an empty tile.'} | 2 |
| `low_gravity_boostable` | Boolean | {'type': '`Boolean`', 'df': 'Can be affected by low gravity wind/effects.'} | 2 |
| `prioritize_change_direction` | Boolean | {'type': '`Boolean`', 'df': 'AI preference to attack from different angles.'} | 2 |
| [`range_bonuses`](./Enums.md#enum-range_bonuses) | Enum | {'type': '`Enum/String`', 'df': 'How much extra range is added by stats/passives.'} | 2 |
| `range_display_include_direction` | Boolean | {'type': '`Boolean`', 'df': 'Visual: shows directional arrows.'} | 2 |
| `recalc_target_on_castpoint` | Boolean | {'type': '`Boolean`', 'df': 'Re-checks if target is valid at the exact frame of cast.'} | 2 |
| `redirect_location_if_blocked` | Boolean | {'type': '`Boolean`', 'df': 'Shifts target to adjacent tile if original is invalid.'} | 2 |
| [`target_requires_element`](./Arrays.md#array-target_requires_element) | Array | {'type': '`Array`', 'df': 'Target must be afflicted with this element.'} | 2 |
| `trample_allies_too` | Boolean | {'type': '`Boolean`', 'df': 'Trample movement damages allies in the path.'} | 2 |
| [`adjust_target`](./Enums.md#enum-adjust_target) | Enum | {'type': '`Enum/String`', 'df': 'Tweaks target selection post-cast.'} | 1 |
| `allow_diagonal_passthrough` | Boolean | {'type': '`Boolean`', 'df': 'Permits diagonal targeting through tight corners.'} | 1 |
| `ally_priority` | Number | {'type': '`Number`', 'df': 'AI preference for targeting allies.'} | 1 |
| `aoe_display_exclude_restrictions` | Boolean | {'type': '`Boolean`', 'df': 'Visual only: Hides invalid tiles from the AoE preview.'} | 1 |
| `aoe_rotate_around_character_center` | Boolean | {'type': '`Boolean`', 'df': 'Anchors the AoE rotation to the character rather than the tile.'} | 1 |
| `aoe_spell_on_land` | Boolean | {'type': '`Boolean`', 'df': 'Visual trigger when a jump lands.'} | 1 |
| `bonus_pathing_leniency` | Number | {'type': '`Number`', 'df': 'Gives the AI leeway when calculating complex paths.'} | 1 |
| [`custom_aoe_mirror`](./Arrays.md#array-custom_aoe_mirror) | Array | {'type': '`Array`', 'df': 'How the custom shape mirrors when facing left vs right.'} | 1 |
| [`custom_aoe_util_mirror`](./Arrays.md#array-custom_aoe_util_mirror) | Array | {'type': '`Array`', 'df': ''} | 1 |
| `damage_collided_only` | Boolean | {'type': '`Boolean`', 'df': 'Only damages the first entity the projectile/dash hits.'} | 1 |
| `enemy_priority` | Number | {'type': '`Number`', 'df': 'AI preference for targeting enemies.'} | 1 |
| `force_no_contact` | Boolean | {'type': '`Boolean`', 'df': 'Bypasses all contact-based retaliation (Thorns, etc).'} | 1 |
| `hint_can_target_static` | Boolean | {'type': '`Boolean`', 'df': 'UI hint that the player can target inanimate objects.'} | 1 |
| [`knockback_modifier`](./Enums.md#enum-knockback_modifier) | Enum | {'type': '`Enum/String`', 'df': 'Multiplier for the knockback physics force.'} | 1 |
| `lingering` | Boolean | {'type': '`Boolean`', 'df': 'Target zone remains active across multiple turns.'} | 1 |
| `mirror_custom_aoe` | Boolean | {'type': '`Boolean`', 'df': 'Flips the custom AoE array.'} | 1 |
| [`prioritize_throw_target_with_passive`](./Enums.md#enum-prioritize_throw_target_with_passive) | Enum | {'type': '`Enum/String`', 'df': 'AI prefers throwing targets that have specific passives.'} | 1 |
| `randomize_knockback_direction_except_for_finisher` | Boolean | {'type': '`Boolean`', 'df': 'Chaotic knockback unless it kills the target.'} | 1 |
| `range_excludes_self` | Boolean | {'type': '`Boolean`', 'df': "Cannot click on the caster's tile."} | 1 |
| `range_max` | Number | {'type': '`Number`', 'df': 'Alternate syntax for `max_range`/`min_range`.'} | 1 |
| `range_min` | Number | {'type': '`Number`', 'df': 'Alternate syntax for `max_range`/`min_range`.'} | 1 |
| [`range_symmetry`](./Enums.md#enum-range_symmetry) | Enum | {'type': '`Enum/String`', 'df': 'Mirrors the range grid.'} | 1 |
| `remain_off_map` | Boolean | {'type': '`Boolean`', 'df': 'Keeps entity removed from the grid.'} | 1 |
| [`restructions`](./Enums.md#enum-restructions) | Enum | {'type': '`Enum/String`', 'df': 'Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`).'} | 1 |
| `reverse_target_direction` | Boolean | {'type': '`Boolean`', 'df': 'Inverts the targeting vector.'} | 1 |
| `spin_steps` | Number | {'type': '`Number`', 'df': 'Number of rotational increments for spin targeting.'} | 1 |
| `uncounterable` | Boolean | {'type': '`Boolean`', 'df': 'Bypasses counter-attack passives.'} | 1 |

</details>

---

### Context: `cost`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1851

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `mana` | Number | {'type': '`Number`', 'df': 'MP pool and how much it restores per turn.'} | 1603 |
| `infcantrip` | Boolean | {'type': '`Boolean`', 'df': 'Can be cast infinitely as long as costs are met.'} | 810 |
| `cantrip` | Boolean | {'type': '`Boolean`', 'df': 'Does not end the turn when cast.'} | 560 |
| `once_per_fight` | Mixed | {'type': '`Enum/String`', 'df': 'Exhausts for the remainder of combat after one use.'} | 98 |
| `act_points` | Number | {'type': '`Number`', 'df': 'Consumes primary action points (default 1).'} | 86 |
| `move_points` | Number | {'type': '`Number`', 'df': 'Consumes movement points.'} | 59 |
| `prime` | Number | {'type': '`Number`', 'df': 'Requires a "priming" turn before it fires.'} | 30 |
| `allow_offmap_casts` | Boolean | {'type': '`Boolean`', 'df': 'Can be used while the character is hidden/removed from grid.'} | 22 |
| `cant_cast` | Mixed | {'type': '`Enum/String`', 'df': 'Explicitly disables casting (used for passive-triggered only abilities).'} | 18 |
| `must_be_consuming` | Boolean | {'type': '`Boolean`', 'df': 'Requires the character to be eating/holding something.'} | 17 |
| `charge` | Mixed | {'type': '`Number`', 'df': 'Cooldown timers measured in turns.'} | 16 |
| `must_not_be_consuming` | Boolean | {'type': '`Boolean`', 'df': 'Cannot be holding/eating an entity.'} | 14 |
| `requires_reload` | Boolean | {'type': '`Boolean`', 'df': 'Must spend an action to reload before casting again.'} | 14 |
| `can_cast_while_dead` | Boolean | {'type': '`Boolean`', 'df': 'Usable by corpses (e.g., DeathRattle triggers).'} | 12 |
| [`cantrip_group`](./Enums.md#enum-cantrip_group) | Enum | {'type': '`Enum/String`', 'df': 'Groups cantrips so using one exhausts the others.'} | 12 |
| `must_be_offmap` | Boolean | {'type': '`Boolean`', 'df': 'Requires the character to be hidden/dug underground.'} | 12 |
| `X_cant_be_zero` | Boolean | {'type': '`Boolean`', 'df': "Applies or references the 'X_cant_be_zero' effect/state."} | 11 |
| `disallow_cost_modification` | Boolean | {'type': '`Boolean`', 'df': 'Prevents passives from making this cheaper.'} | 9 |
| `coins` | Number | {'type': '`Number`', 'df': 'Consumes currency to cast.'} | 8 |
| `durability` | Number | {'type': '`Number`', 'df': 'Consumes item durability.'} | 8 |
| `main_turn_only` | Boolean | {'type': '`Boolean`', 'df': 'Cannot be cast during bonus or dispersed turns.'} | 8 |
| `requires_destructible_weapon` | Boolean | {'type': '`Boolean`', 'df': 'The equipped weapon must be breakable.'} | 8 |
| `requires_exact_character_aux` | Number | {'type': '`Number`', 'df': 'Hardcoded character specific lock.'} | 8 |
| `must_not_be_a_summon` | Boolean | {'type': '`Boolean`', 'df': 'Summons/Familiars cannot cast this.'} | 7 |
| `start_reloaded` | Boolean | {'type': '`Boolean`', 'df': 'Spawns with the ability pre-loaded.'} | 7 |
| `must_be_first_action` | Boolean | {'type': '`Boolean`', 'df': 'Can only be used at the very start of the turn.'} | 4 |
| `enabled_formula` | Mixed | {'type': '`Number`', 'df': 'Mathematical string required to be >0 to cast.'} | 3 |
| `must_be_first_nonmove_action` | Boolean | {'type': '`Boolean`', 'df': 'Can move first, but cannot use other abilities first.'} | 3 |
| `must_have_weapon` | Boolean | {'type': '`Boolean`', 'df': 'Requires a weapon equipped in the item slot.'} | 2 |
| `can_be_refreshed` | Boolean | {'type': '`Boolean`', 'df': "Passives/Effects can reset this ability's cooldown."} | 1 |
| `can_pay_over_multiple_turns` | Boolean | {'type': '`Boolean`', 'df': 'Allows channeling costs over time.'} | 1 |
| `can_self_refresh` | Boolean | {'type': '`Boolean`', 'df': 'The ability has mechanics to reset its own cooldown.'} | 1 |
| `damage_cant_be_zero` | Boolean | {'type': '`Boolean`', 'df': 'Requires the ability to have >0 calculated damage to cast.'} | 1 |
| `initial_charge` | Number | {'type': '`Number`', 'df': 'How many turns it starts on cooldown at battle start.'} | 1 |
| `manacost_cant_be_zero` | Boolean | {'type': '`Boolean`', 'df': 'Fails to cast if mana cost is reduced to 0.'} | 1 |
| `minimum_con` | Number | {'type': '`Number`', 'df': 'Stat thresholds required to cast.'} | 1 |
| `minimum_spd` | Number | {'type': '`Number`', 'df': 'Stat thresholds required to cast.'} | 1 |
| `require_default_size` | Boolean | {'type': '`Boolean`', 'df': '2x2 or altered characters cannot cast this.'} | 1 |
| `requires_attack_damage_threshold` | Number | {'type': '`Number`', 'df': 'Needs a certain amount of innate damage.'} | 1 |
| `requires_consumed_trinket` | Boolean | {'type': '`Boolean`', 'df': 'Must have eaten a specific item type.'} | 1 |
| `requires_empty_trinket` | Boolean | {'type': '`Boolean`', 'df': 'Must not have an accessory equipped.'} | 1 |
| `requires_hp_threshold` | Number | {'type': '`Number`', 'df': 'Must be below/above a certain health percentage.'} | 1 |
| `requires_weapon` | Boolean | {'type': '`Boolean`', 'df': 'Prerequisite: Must meet this condition.'} | 1 |

</details>

---

### Context: `self_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 220

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#context-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | {'type': '`Block`', 'df': 'Non-damaging status applications and logic triggers executed on impact. | 200 |
| `damage` | Mixed | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 47 |
| `piercing` | Boolean | {'type': '`Boolean`', 'df': ''} | 12 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'Classification/category type.'} | 11 |
| `cant_miss` | Boolean | {'type': '`Boolean`', 'df': ''} | 10 |
| `knockback` | Number | {'type': '`Number`', 'df': ''} | 10 |
| `heal` | Number | {'type': '`Number`', 'df': ''} | 6 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 4 |
| `ai_base_score` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `non_lethal` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `spawn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 192

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 184 |
| [`faction`](./Enums.md#enum-faction) | Enum | {'type': '`Enum/String`', 'df': ''} | 59 |
| `ai_base_score` | Number | {'type': '`Number`', 'df': ''} | 31 |
| [`additional_passives`](./Abilities_and_Spells.md#context-additional_passives) | Block | {'type': '`Block`', 'df': "Passives granted intrinsically to a spawned entity. | 20 |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum | {'type': '`Enum/String`', 'df': ''} | 17 |
| [`layer`](./Enums.md#enum-layer) | Enum | {'type': '`Enum/String`', 'df': ''} | 14 |
| [`catdata`](./Enums.md#enum-catdata) | Enum | {'type': '`Enum/String`', 'df': 'Defines genetic/clone data cloning.'} | 13 |
| `clone_items` | Boolean | {'type': '`Boolean`', 'df': 'If true, transfers inventory to the clone.'} | 12 |
| `lob` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| [`post_spawn_statuses`](./Abilities_and_Spells.md#context-post_spawn_statuses) | Block | {'type': '`Block`', 'df': "Status effects applied immediately after an entity spawns. | 4 |
| `size` | Number | {'type': '`Number`', 'df': ''} | 4 |
| `face_camera` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `inherit_elite_buffs` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `start_dead` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| [`appearance`](./Enums.md#enum-appearance) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`auto_cast_on_spawn`](./Enums.md#enum-auto_cast_on_spawn) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`chapter`](./Enums.md#enum-chapter) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`custom_additional_ai_weight`](./Enums.md#enum-custom_additional_ai_weight) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `include_passives` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `redirect_location_if_blocked` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`spawnin_animation`](./Enums.md#enum-spawnin_animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `trigger_battle_start` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `bonus_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 136

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DeadAltAbility`](./Enums.md#enum-deadaltability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'DeadAltAbility' effect/state."} | 12 |
| `AbilityEnabledOncePerFightAtHealthThreshold` | Number | {'type': '`Number`', 'df': "Applies or references the 'AbilityEnabledOncePerFightAtHealthThreshold' effect/state."} | 7 |
| `XIsFreeArmorSlots` | Number | {'type': '`Number`', 'df': "Applies or references the 'XIsFreeArmorSlots' effect/state."} | 7 |
| `AbilityEnabledPercentEachTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'AbilityEnabledPercentEachTurn' effect/state."} | 6 |
| `FreeFirstCast` | Number | {'type': '`Number`', 'df': "Applies or references the 'FreeFirstCast' effect/state."} | 6 |
| [`XIsLivingAlliesWithTag`](./Enums.md#enum-xislivingallieswithtag) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'XIsLivingAlliesWithTag' effect/state."} | 5 |
| `CatchBoomerang` | Number | {'type': '`Number`', 'df': "Applies or references the 'CatchBoomerang' effect/state."} | 4 |
| `CopyBasicAttackEffects` | Number | {'type': '`Number`', 'df': "Applies or references the 'CopyBasicAttackEffects' effect/state."} | 4 |
| [`DownRankAIIfWeaponUsable`](./Enums.md#enum-downrankaiifweaponusable) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'DownRankAIIfWeaponUsable' effect/state."} | 4 |
| [`AbilityEnableIfConsumedCharacterHasTag`](./Enums.md#enum-abilityenableifconsumedcharacterhastag) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'AbilityEnableIfConsumedCharacterHasTag' effect/state."} | 3 |
| `AbilityEnabledOncePerRound` | Number | {'type': '`Number`', 'df': "Applies or references the 'AbilityEnabledOncePerRound' effect/state."} | 3 |
| `AbilityInheritsWeaponEffects` | Number | {'type': '`Number`', 'df': "Applies or references the 'AbilityInheritsWeaponEffects' effect/state."} | 3 |
| `MoonHeadFinisherEnabler` | Number | {'type': '`Number`', 'df': "Applies or references the 'MoonHeadFinisherEnabler' effect/state."} | 3 |
| [`XIsMultipliedPercentHealth`](./Arrays.md#array-xismultipliedpercenthealth) | Array | {'type': '`Array`', 'df': "Applies or references the 'XIsMultipliedPercentHealth' effect/state."} | 3 |
| [`AbilityEnabledIfHasStatus`](./Enums.md#enum-abilityenabledifhasstatus) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'AbilityEnabledIfHasStatus' effect/state."} | 2 |
| [`AutocastEachRound`](./Abilities_and_Spells.md#context-autocasteachround) | Block | {'type': '`Block`', 'df': 'Forces the character to automatically cast a specific ability at the start of each combat round. | 2 |
| [`ChargeSpiritBombAura`](./Enums.md#enum-chargespiritbombaura) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ChargeSpiritBombAura' effect/state."} | 2 |
| `CopyCatPassive_Initializer` | Number | {'type': '`Number`', 'df': "Applies or references the 'CopyCatPassive_Initializer' effect/state."} | 2 |
| [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#context-nukequestfinalbossmodifications) | Block | {'type': '`Block`', 'df': 'Special encounter trigger for the Nuke Quest ending. | 2 |
| `ReloadOnKill` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReloadOnKill' effect/state."} | 2 |
| `ReloadOnKillEnemy` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReloadOnKillEnemy' effect/state."} | 2 |
| `ReloadOnTotalDamageReceived` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReloadOnTotalDamageReceived' effect/state."} | 2 |
| [`XIsLivingCharactersWithTag`](./Enums.md#enum-xislivingcharacterswithtag) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'XIsLivingCharactersWithTag' effect/state."} | 2 |
| `XIsOtherHealsThisTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'XIsOtherHealsThisTurn' effect/state."} | 2 |
| [`XIsSpellStormRampAndReset`](./Abilities_and_Spells.md#context-xisspellstormrampandreset) | Block | {'type': '`Number`', 'df': 'Math variable assignment: Evaluates X based on Spell Storm stacks, then resets them.'} | 2 |
| `XIsTimesDamageTaken` | Number | {'type': '`Number`', 'df': "Applies or references the 'XIsTimesDamageTaken' effect/state."} | 2 |
| `AbilityDisableIfLivingCrow` | Number | {'type': '`Number`', 'df': "Applies or references the 'AbilityDisableIfLivingCrow' effect/state."} | 1 |
| `AbilityEnabledAtHealthThreshold` | Number | {'type': '`Number`', 'df': "Applies or references the 'AbilityEnabledAtHealthThreshold' effect/state."} | 1 |
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'AbilityEnabledIfBasicAttackUsedThisTurn' effect/state."} | 1 |
| `AbilityEnabledIfMovementTrapped` | Number | {'type': '`Number`', 'df': "Applies or references the 'AbilityEnabledIfMovementTrapped' effect/state."} | 1 |
| `AbilityEnabledIfNoAggroTarget` | Number | {'type': '`Number`', 'df': "Applies or references the 'AbilityEnabledIfNoAggroTarget' effect/state."} | 1 |
| [`AbilityEnabledIfNotHasStatus`](./Enums.md#enum-abilityenabledifnothasstatus) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'AbilityEnabledIfNotHasStatus' effect/state."} | 1 |
| [`AbilityEnabledIfSpecificItemEquipped`](./Enums.md#enum-abilityenabledifspecificitemequipped) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'AbilityEnabledIfSpecificItemEquipped' effect/state."} | 1 |
| `AbsorbManaFromOtherSpells` | Number | {'type': '`Number`', 'df': "Applies or references the 'AbsorbManaFromOtherSpells' effect/state."} | 1 |
| [`AddElementsToSpells`](./Enums.md#enum-addelementstospells) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'AddElementsToSpells' effect/state."} | 1 |
| [`AddStatusToBasicAttack`](./Abilities_and_Spells.md#context-addstatustobasicattack) | Block | {'type': 'Block', 'df': 'Injects a status effect payload that applies whenever the character performs a basic attack.'} | 1 |
| `AlphaDodgeChance` | Number | {'type': '`Number`', 'df': "Applies or references the 'AlphaDodgeChance' effect/state."} | 1 |
| [`AlphaStatusOnTurnBegin`](./Abilities_and_Spells.md#context-alphastatusonturnbegin) | Block | {'type': '`Block`', 'df': "Grants a specific status effect to the 'Alpha' (the party leader) at the start of their turn. | 1 |
| [`BonusAbility_DelayedApplication`](./Enums.md#enum-bonusability_delayedapplication) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'BonusAbility_DelayedApplication' effect/state."} | 1 |
| `CapTechSpent` | Number | {'type': '`Number`', 'df': "Applies or references the 'CapTechSpent' effect/state."} | 1 |
| `CaveWomanBirthControl` | Number | {'type': '`Number`', 'df': "Applies or references the 'CaveWomanBirthControl' effect/state."} | 1 |
| `CritChanceUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'CritChanceUp' effect/state."} | 1 |
| `FistOfFateUniqueEnemyTracker` | Number | {'type': '`Number`', 'df': "Applies or references the 'FistOfFateUniqueEnemyTracker' effect/state."} | 1 |
| `FreeFirstCastAndAfterSpendMana` | Number | {'type': '`Number`', 'df': "Applies or references the 'FreeFirstCastAndAfterSpendMana' effect/state."} | 1 |
| `FreeFirstCastEachMatch` | Number | {'type': '`Number`', 'df': "Applies or references the 'FreeFirstCastEachMatch' effect/state."} | 1 |
| `HealthRegenUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthRegenUp' effect/state."} | 1 |
| `IgnoreTiles` | Number | {'type': '`Number`', 'df': "Applies or references the 'IgnoreTiles' effect/state."} | 1 |
| `IntelligenceUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'IntelligenceUp' effect/state."} | 1 |
| `InterchangeDisabler` | Number | {'type': '`Number`', 'df': "Applies or references the 'InterchangeDisabler' effect/state."} | 1 |
| `KnockbackImmunity` | Number | {'type': '`Number`', 'df': "Applies or references the 'KnockbackImmunity' effect/state."} | 1 |
| [`PassiveWhileNotTakingTurn`](./Abilities_and_Spells.md#context-passivewhilenottakingturn) | Block | {'type': '`Block`', 'df': "Grants nested passives that are only active while it is NOT the character's turn. | 1 |
| `ReloadOnAllyCatDies` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReloadOnAllyCatDies' effect/state."} | 1 |
| `ReloadOnAllyDies` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReloadOnAllyDies' effect/state."} | 1 |
| `ReloadOnAnyDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReloadOnAnyDamage' effect/state."} | 1 |
| `ReloadOnBackstab` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReloadOnBackstab' effect/state."} | 1 |
| [`ReloadOnElementalDamageReceived`](./Enums.md#enum-reloadonelementaldamagereceived) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ReloadOnElementalDamageReceived' effect/state."} | 1 |
| `ReloadOnGainCoins` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReloadOnGainCoins' effect/state."} | 1 |
| `ReloadOnGainDivineShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReloadOnGainDivineShield' effect/state."} | 1 |
| [`ReloadOnKillTagged`](./Enums.md#enum-reloadonkilltagged) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ReloadOnKillTagged' effect/state."} | 1 |
| `ReloadOnSpendMana` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReloadOnSpendMana' effect/state."} | 1 |
| `ReloadOnUseAbilityWithManaCost` | Number | {'type': '`Number`', 'df': "Applies or references the 'ReloadOnUseAbilityWithManaCost' effect/state."} | 1 |
| [`RevengeDamage`](./Abilities_and_Spells.md#context-revengedamage) | Block | {'type': '`Block`', 'df': 'Reaction trigger: Deals damage to the attacker when hit. | 1 |
| [`StatusKillers`](./Abilities_and_Spells.md#context-statuskillers) | Block | {'type': '`Block`', 'df': "Instantly kills the target if they possess the specified status effects. | 1 |
| `TossTargetIsAggroTarget` | Number | {'type': '`Number`', 'df': "Applies or references the 'TossTargetIsAggroTarget' effect/state."} | 1 |
| `TossTargetIsBuddy` | Number | {'type': '`Number`', 'df': "Applies or references the 'TossTargetIsBuddy' effect/state."} | 1 |
| `TossTargetIsNotInWater` | Number | {'type': '`Number`', 'df': "Applies or references the 'TossTargetIsNotInWater' effect/state."} | 1 |
| `Trample` | Number | {'type': '`Number`', 'df': "Applies or references the 'Trample' effect/state."} | 1 |
| `XIsConsumedCharacterMaxHP` | Number | {'type': '`Number`', 'df': "Applies or references the 'XIsConsumedCharacterMaxHP' effect/state."} | 1 |
| `XIsCountDeaths` | Number | {'type': '`Number`', 'df': "Applies or references the 'XIsCountDeaths' effect/state."} | 1 |
| [`XIsCountStatusStacks`](./Enums.md#enum-xiscountstatusstacks) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'XIsCountStatusStacks' effect/state."} | 1 |
| [`XIsFormulaLockedUntilComplete`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'XIsFormulaLockedUntilComplete' effect/state."} | 1 |
| `XIsIncreaseEachTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'XIsIncreaseEachTurn' effect/state."} | 1 |
| `XIsRampAndReset` | Number | {'type': '`Number`', 'df': "Applies or references the 'XIsRampAndReset' effect/state."} | 1 |
| `XIsRecycleCostReduction` | Number | {'type': '`Number`', 'df': "Applies or references the 'XIsRecycleCostReduction' effect/state."} | 1 |

</details>

---

### Context: `temporary_effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 88

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Trample` | Number | {'type': '`Number`', 'df': "Applies or references the 'Trample' effect/state."} | 26 |
| `CastAgain` | Number | {'type': '`Number`', 'df': "Applies or references the 'CastAgain' effect/state."} | 20 |
| `DisableTrample` | Number | {'type': '`Number`', 'df': "Applies or references the 'DisableTrample' effect/state."} | 10 |
| `Fury` | Number | {'type': '`Number`', 'df': "Applies or references the 'Fury' effect/state."} | 7 |
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'TileTrail' effect/state."} | 6 |
| `JustInCaseTrample` | Number | {'type': '`Number`', 'df': "Applies or references the 'JustInCaseTrample' effect/state."} | 5 |
| [`LeaveBehind`](./Abilities_and_Spells.md#context-leavebehind) | Block | {'type': '`Enum/String`', 'df': "Spawns a specific object at the character's previous location when they move."} | 5 |
| `DashFury` | Number | {'type': '`Number`', 'df': "Applies or references the 'DashFury' effect/state."} | 3 |
| [`AfterImage`](./Abilities_and_Spells.md#context-afterimage) | Block | {'type': '`Block`', 'df': "Spawns a visual decoy or shade at the caster's previous location. | 2 |
| `BearTrapTrail` | Number | {'type': '`Number`', 'df': "Applies or references the 'BearTrapTrail' effect/state."} | 2 |
| `DelayedWindTrail` | Number | {'type': '`Number`', 'df': "Applies or references the 'DelayedWindTrail' effect/state."} | 1 |
| `DoubleLoot` | Number | {'type': '`Number`', 'df': "Applies or references the 'DoubleLoot' effect/state."} | 1 |
| [`JumpAttackLeaveBehind`](./Enums.md#enum-jumpattackleavebehind) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'JumpAttackLeaveBehind' effect/state."} | 1 |
| `KnockbackImmunity` | Number | {'type': '`Number`', 'df': "Applies or references the 'KnockbackImmunity' effect/state."} | 1 |
| [`TileTrail_Ahead`](./Enums.md#enum-tiletrail_ahead) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'TileTrail_Ahead' effect/state."} | 1 |

</details>

---

### Context: `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 71

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object), [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`GainDisorderFromPool_PostCast`](./Enums.md#enum-gaindisorderfrompool_postcast) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'GainDisorderFromPool_PostCast' effect/state."} | 7 |
| `BonusDamage` | Mixed | {'type': 'String', 'df': "Applies or references the 'BonusDamage' effect/state."} | 6 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': 'Block', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target.'} | 3 |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate) | Block | {'type': 'Block', 'df': 'Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters.'} | 3 |
| `Vaporize` | Number | {'type': '`Number`', 'df': "Applies or references the 'Vaporize' effect/state."} | 3 |
| `Cleanse` | Number | {'type': 'Number', 'df': "Applies or references the 'Cleanse' effect/state."} | 2 |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#context-conditional_hasstatus) | Block | {'type': 'Block', 'df': 'Conditional trigger: Executes nested logic if the target currently has the specified status effect.'} | 2 |
| `Confusion` | Number | {'type': 'Number', 'df': "Applies or references the 'Confusion' effect/state."} | 2 |
| [`FormChange`](./Enums.md#enum-formchange) | Enum | {'type': 'Block', 'df': 'Transforms the character into a different state or form (e.g., Rage, HasCat).'} | 2 |
| `FullHeal` | Number | {'type': '`Number`', 'df': "Applies or references the 'FullHeal' effect/state."} | 2 |
| [`GainCoinsRange`](./Abilities_and_Spells.md#context-gaincoinsrange) | Block | {'type': '`Block`', 'df': 'Grants the player a randomized amount of coins within a min/max range.'} | 2 |
| [`RandomStatDown`](./Math_Equations.md) | Equation | {'type': 'Number', 'df': "Applies or references the 'RandomStatDown' effect/state."} | 2 |
| `RandomStatUp` | Number | {'type': 'Number', 'df': "Applies or references the 'RandomStatUp' effect/state."} | 2 |
| `Revive` | Number | {'type': '`Number`', 'df': "Applies or references the 'Revive' effect/state."} | 2 |
| `SpawnBearTrapIfHitKills` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpawnBearTrapIfHitKills' effect/state."} | 2 |
| [`SpawnThingIfHitKills`](./Enums.md#enum-spawnthingifhitkills) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'SpawnThingIfHitKills' effect/state."} | 2 |
| `AllStatsUp` | Number | {'type': 'Number', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 1 |
| [`ApplyToRandomPartyMemberIfPossible`](./Abilities_and_Spells.md#context-applytorandompartymemberifpossible) | Block | {'type': 'Block', 'df': "Redirects the nested effects to apply to a random living member of the player's party."} | 1 |
| `Bruise` | Number | {'type': 'Number', 'df': "Applies or references the 'Bruise' effect/state."} | 1 |
| [`CatPartsTransform`](./Abilities_and_Spells.md#context-catpartstransform) | Block | {'type': 'Block', 'df': 'Transforms specific body parts into different visual variants.'} | 1 |
| `Charmed` | Number | {'type': 'Number', 'df': "Applies or references the 'Charmed' effect/state."} | 1 |
| `Cleave` | Number | {'type': 'Number', 'df': 'Causes the attack to hit adjacent enemies alongside the primary target.'} | 1 |
| [`Conditional_Displaceable`](./Abilities_and_Spells.md#context-conditional_displaceable) | Block | {'type': 'Block', 'df': 'Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement.'} | 1 |
| [`Conditional_GoodRoll`](./Abilities_and_Spells.md#context-conditional_goodroll) | Block | {'type': 'Block', 'df': 'Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.'} | 1 |
| [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag) | Block | {'type': 'Block', 'df': 'Conditional trigger: Executes nested logic if the target possesses the specified entity tag.'} | 1 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#context-conditional_healththreshold) | Block | {'type': 'Block', 'df': "Conditional trigger: Executes nested logic if the target's health falls below the specified threshold."} | 1 |
| [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object) | Block | {'type': 'Block', 'df': 'Conditional trigger: Executes nested logic if the target is an inanimate object or furniture.'} | 1 |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative) | Block | {'type': 'Block', 'df': 'A simulation block used by the AI to test hypothetical outcomes before committing to an action.'} | 1 |
| `ConstitutionUp` | Number | {'type': 'Number', 'df': "Applies or references the 'ConstitutionUp' effect/state."} | 1 |
| [`Consumed`](./Abilities_and_Spells.md#context-consumed) | Block | {'type': 'Block', 'df': 'State block triggered when this object or entity is eaten/consumed by another character.'} | 1 |
| `CritChanceUp` | Number | {'type': 'Number', 'df': "Applies or references the 'CritChanceUp' effect/state."} | 1 |
| `DamageUp` | Number | {'type': 'Number', 'df': "Applies or references the 'DamageUp' effect/state."} | 1 |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#context-destroyequipmentandattachparasite) | Block | {'type': 'Block', 'df': 'Removes an equipped item and replaces it with a parasite from a specified pool.'} | 1 |
| `DieViolently` | Number | {'type': 'Number', 'df': "Applies or references the 'DieViolently' effect/state."} | 1 |
| [`DoDamage`](./Abilities_and_Spells.md#context-dodamage) | Block | {'type': 'Block', 'df': 'Explicitly triggers a secondary damage instance independent of the main attack.'} | 1 |
| `DodgeChance_Status` | Number | {'type': 'Number', 'df': "Applies or references the 'DodgeChance_Status' effect/state."} | 1 |
| [`DybbukPossessed`](./Abilities_and_Spells.md#context-dybbukpossessed) | Block | {'type': 'Block', 'df': 'Defines the abilities and behaviors available when possessing another entity.'} | 1 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | {'type': 'Block', 'df': 'Fallback block that executes if the preceding `Conditional_` block evaluated to false.'} | 1 |
| `ExplodeCharacter` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExplodeCharacter' effect/state."} | 1 |
| `ExplodeCharacter_Party` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExplodeCharacter_Party' effect/state."} | 1 |
| `FaceCamera` | Number | {'type': '`Number`', 'df': "Applies or references the 'FaceCamera' effect/state."} | 1 |
| `FlatAIBonus` | Number | {'type': '`Number`', 'df': "Applies or references the 'FlatAIBonus' effect/state."} | 1 |
| `ForceImmediateMove` | Number | {'type': '`Number`', 'df': "Applies or references the 'ForceImmediateMove' effect/state."} | 1 |
| `GenericDebuff` | Number | {'type': '`Number`', 'df': "Applies or references the 'GenericDebuff' effect/state."} | 1 |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ImmediateUseAbility' effect/state."} | 1 |
| `Immobile` | Number | {'type': 'Number', 'df': "Applies or references the 'Immobile' effect/state."} | 1 |
| `Instakill` | Number | {'type': '`Number`', 'df': "Applies or references the 'Instakill' effect/state."} | 1 |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#context-knockupandaway) | Block | {'type': '`Block`', 'df': 'Displaces the target vertically and horizontally away from the source.'} | 1 |
| `Leeches` | Number | {'type': '`Number`', 'df': "Applies or references the 'Leeches' effect/state."} | 1 |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum | {'type': '`Enum/String`', 'df': 'Spawns a specific character or entity upon impact.'} | 1 |
| `OverrideDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'OverrideDamage' effect/state."} | 1 |
| `PartialCleanse` | Number | {'type': '`Number`', 'df': "Applies or references the 'PartialCleanse' effect/state."} | 1 |
| `PurgeAll` | Number | {'type': '`Number`', 'df': "Applies or references the 'PurgeAll' effect/state."} | 1 |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | {'type': '`Block`', 'df': 'Selects and applies a random status effect from the provided nested block.'} | 1 |
| `RemoveMovePoints` | Number | {'type': '`Number`', 'df': "Applies or references the 'RemoveMovePoints' effect/state."} | 1 |
| `RemoveTurnsThisRound` | Number | {'type': '`Number`', 'df': "Applies or references the 'RemoveTurnsThisRound' effect/state."} | 1 |
| [`ScatterCoins`](./Abilities_and_Spells.md#context-scattercoins) | Block | {'type': '`Block`', 'df': 'Throws coins out into the level randomly.'} | 1 |
| `SetHealth` | Number | {'type': '`Number`', 'df': "Applies or references the 'SetHealth' effect/state."} | 1 |
| `SetShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'SetShield' effect/state."} | 1 |
| [`ShowFakeDamage`](./Abilities_and_Spells.md#context-showfakedamage) | Block | {'type': '`Block`', 'df': 'Displays a visual damage number without actually modifying health.'} | 1 |
| `Slow` | Number | {'type': '`Number`', 'df': "Applies or references the 'Slow' effect/state."} | 1 |
| `SpeculativeMoveSelfCorpseOffMap` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state."} | 1 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpeedUp' effect/state."} | 1 |
| [`Temporary`](./Abilities_and_Spells.md#context-temporary) | Block | {'type': '`Block`', 'df': 'A wrapper block for applying status effects that automatically expire.'} | 1 |
| `VaporizeInanimate` | Number | {'type': '`Number`', 'df': "Applies or references the 'VaporizeInanimate' effect/state."} | 1 |
| [`XIsTargetHealth`](./Abilities_and_Spells.md#context-xistargethealth) | Block | {'type': '`Block`', 'df': "Math variable assignment: Evaluates X as the target's current health."} | 1 |

</details>

---

### Context: `ApplyToSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 51

> **Referenced by:** [`ApplyStatusIfCrit`](./Abilities_and_Spells.md#context-applystatusifcrit), [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate), [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_GoodRoll`](./Abilities_and_Spells.md#context-conditional_goodroll), [`Conditional_HasStatus`](./Abilities_and_Spells.md#context-conditional_hasstatus), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#context-conditional_healththreshold), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#context-conditional_livingplayercat), [`Conditional_PlayerCat`](./Abilities_and_Spells.md#context-conditional_playercat), [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#context-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#context-else), [`Math`](./Abilities_and_Spells.md#context-math), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 5 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'StrengthUp' effect/state."} | 5 |
| [`EvolveAbilityFromPool`](./Enums.md#enum-evolveabilityfrompool) | Enum | {'type': '`Enum/String`', 'df': 'Upgrades or transforms an existing ability into a new one from the specified pool.'} | 4 |
| [`FormChange`](./Abilities_and_Spells.md#context-formchange) | Block | {'type': '`Enum/String`', 'df': 'Transforms the character into a different state or form (e.g., Rage, HasCat).'} | 4 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 4 |
| `AddWeaponAux` | Mixed | {'type': '`String`', 'df': "Applies or references the 'AddWeaponAux' effect/state."} | 3 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 3 |
| `ConstitutionUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'ConstitutionUp' effect/state."} | 3 |
| [`Craft`](./Abilities_and_Spells.md#context-craft) | Block | {'type': '`Block`', 'df': 'Synthesizes or spawns a new item from a specific pool. | 3 |
| `RefreshActPoints` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshActPoints' effect/state."} | 3 |
| `AddLeechesStatus` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddLeechesStatus' effect/state."} | 2 |
| `Cleanse` | Number | {'type': '`Number`', 'df': "Applies or references the 'Cleanse' effect/state."} | 2 |
| [`DoDamage`](./Abilities_and_Spells.md#context-dodamage) | Block | {'type': '`Block`', 'df': 'Explicitly triggers a secondary damage instance independent of the main attack. | 2 |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'EquipPermanentItem' effect/state."} | 2 |
| [`FindItemFromPool`](./Abilities_and_Spells.md#context-finditemfrompool) | Block | {'type': '`Block`', 'df': 'Generates an item drop from the specified loot pool. | 2 |
| `FreeSpell` | Number | {'type': '`Number`', 'df': "Applies or references the 'FreeSpell' effect/state."} | 2 |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'LuckUp' effect/state."} | 2 |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'RemoveStatus' effect/state."} | 2 |
| `Brace` | Number | {'type': '`Number`', 'df': "Applies or references the 'Brace' effect/state."} | 1 |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bruise' effect/state."} | 1 |
| `DisableWeapon` | Number | {'type': '`Number`', 'df': "Applies or references the 'DisableWeapon' effect/state."} | 1 |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'DivineShield' effect/state."} | 1 |
| [`FindItem`](./Enums.md#enum-finditem) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'FindItem' effect/state."} | 1 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ForceUseAbility' effect/state."} | 1 |
| `FullHeal` | Number | {'type': '`Number`', 'df': "Applies or references the 'FullHeal' effect/state."} | 1 |
| [`GainCoinsRange`](./Abilities_and_Spells.md#context-gaincoinsrange) | Block | {'type': '`Block`', 'df': 'Grants the player a randomized amount of coins within a min/max range. | 1 |
| `KineticSpikes` | Number | {'type': '`Number`', 'df': "Applies or references the 'KineticSpikes' effect/state."} | 1 |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#context-knockupandaway) | Block | {'type': '`Block`', 'df': 'Displaces the target vertically and horizontally away from the source. | 1 |
| `ManaGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'ManaGain' effect/state."} | 1 |
| `MoveQuivered` | Number | {'type': '`Number`', 'df': "Applies or references the 'MoveQuivered' effect/state."} | 1 |
| `RefreshMovePoints` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshMovePoints' effect/state."} | 1 |
| [`SpecificInjury`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'SpecificInjury' effect/state."} | 1 |
| `StanceSwitchToMelee` | Number | {'type': '`Number`', 'df': "Applies or references the 'StanceSwitchToMelee' effect/state."} | 1 |
| `StanceSwitchToRanged` | Number | {'type': '`Number`', 'df': "Applies or references the 'StanceSwitchToRanged' effect/state."} | 1 |
| `TakeExtraTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'TakeExtraTurn' effect/state."} | 1 |
| `Tech` | Number | {'type': '`Number`', 'df': "Applies or references the 'Tech' effect/state."} | 1 |
| `TempTrampleUntilSettled` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempTrampleUntilSettled' effect/state."} | 1 |

</details>

---

### Context: `Conditional_HasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 42

> **Referenced by:** [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The specific string tag to check for.'} | 41 |
| [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is NOT a Boss. | 6 |
| `FloatingRockTrap` | Number | {'type': '`Number`', 'df': "Applies or references the 'FloatingRockTrap' effect/state."} | 6 |
| [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is a Boss. | 4 |
| `IgnoreDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'IgnoreDamage' effect/state."} | 4 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': 'Block', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target.'} | 3 |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ImmediateUseAbility' effect/state."} | 3 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill) | Block | {'type': '`Block`', 'df': "Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 2 |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate) | Block | {'type': 'Block', 'df': 'Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters.'} | 2 |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ChangeTilesUnder' effect/state."} | 2 |
| `DamageUp` | Number | {'type': 'Number', 'df': "Applies or references the 'DamageUp' effect/state."} | 2 |
| `Die` | Number | {'type': '`Number`', 'df': "Applies or references the 'Die' effect/state."} | 2 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | {'type': 'Block', 'df': 'Fallback block that executes if the preceding `Conditional_` block evaluated to false.'} | 2 |
| `Vaporize` | Number | {'type': '`Number`', 'df': "Applies or references the 'Vaporize' effect/state."} | 2 |
| `BonusDamage` | Number | {'type': 'Number', 'df': "Applies or references the 'BonusDamage' effect/state."} | 1 |
| [`Conditional_InForm`](./Abilities_and_Spells.md#context-conditional_inform) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 1 |
| `CrackMoonHead` | Number | {'type': '`Number`', 'df': "Applies or references the 'CrackMoonHead' effect/state."} | 1 |
| `DeleteObject` | Number | {'type': '`Number`', 'df': "Applies or references the 'DeleteObject' effect/state."} | 1 |
| `DisplaceTowardsSource` | Number | {'type': '`Number`', 'df': "Applies or references the 'DisplaceTowardsSource' effect/state."} | 1 |
| `EventBounty` | Number | {'type': '`Number`', 'df': "Applies or references the 'EventBounty' effect/state."} | 1 |
| `FaceAway` | Number | {'type': '`Number`', 'df': "Applies or references the 'FaceAway' effect/state."} | 1 |
| `Instakill` | Number | {'type': '`Number`', 'df': "Applies or references the 'Instakill' effect/state."} | 1 |
| [`MergeDamageInstance`](./Abilities_and_Spells.md#context-mergedamageinstance) | Block | {'type': '`Block`', 'df': 'Combines damage numbers or visual hit effects. | 1 |
| `OverrideDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'OverrideDamage' effect/state."} | 1 |
| [`PopAndSpawn`](./Abilities_and_Spells.md#context-popandspawn) | Block | {'type': '`Block`', 'df': 'Destroys the target and replaces it with a new spawned entity. | 1 |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'RemoveStatus' effect/state."} | 1 |
| `ScatterRandomPickups` | Number | {'type': '`Number`', 'df': "Applies or references the 'ScatterRandomPickups' effect/state."} | 1 |
| [`SetAnimationAlts`](./Abilities_and_Spells.md#context-setanimationalts) | Block | {'type': '`Block`', 'df': 'Overrides specific animation states with alternative animations. | 1 |
| `SetKnockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'SetKnockback' effect/state."} | 1 |
| [`UseAbility`](./Enums.md#enum-useability) | Enum | {'type': '`Enum/String`', 'df': 'Forces the character or target to instantly use a specified ability.'} | 1 |
| `VaporizeCorpse` | Number | {'type': '`Number`', 'df': "Applies or references the 'VaporizeCorpse' effect/state."} | 1 |

</details>

---

### Context: `Temporary`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 41

> **Referenced by:** [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate), [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_NotAlly`](./Abilities_and_Spells.md#context-conditional_notally), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 41 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The status effect to apply.'} | 40 |
| `turns` | Number | {'type': '`Number`', 'df': 'Duration in turns.'} | 40 |
| `expires_on_begin_turn` | Boolean | {'type': '`Boolean`', 'df': 'If true, ticks down at the start of the turn rather than the end.'} | 19 |
| `expires_on_end_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 11 |
| `data` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `expires_on_appliers_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `expires_on_move` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `sounds`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 39

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ontrigger`](./Enums.md#enum-ontrigger) | Enum | {'type': '`Enum/String`', 'df': ''} | 32 |
| [`oncast`](./Enums.md#enum-oncast) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`oncastpoint`](./Enums.md#enum-oncastpoint) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`ontrigger_intentional`](./Enums.md#enum-ontrigger_intentional) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Conditional_Enemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 36

> **Referenced by:** [`Conditional_Corpse`](./Abilities_and_Spells.md#context-conditional_corpse), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Confusion`](./Arrays.md#array-confusion) | Array | {'type': '`Number`', 'df': "Applies or references the 'Confusion' effect/state."} | 6 |
| [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is NOT a Boss. | 3 |
| `DisplaceToAbilityTarget` | Number | {'type': '`Number`', 'df': "Applies or references the 'DisplaceToAbilityTarget' effect/state."} | 3 |
| `AllStatsUp` | Number | {'type': 'Number', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 2 |
| `Attraction` | Number | {'type': '`Number`', 'df': "Applies or references the 'Attraction' effect/state."} | 2 |
| `Fear` | Number | {'type': '`Number`', 'df': "Applies or references the 'Fear' effect/state."} | 2 |
| `Madness` | Number | {'type': '`Number`', 'df': 'Applies the Madness debuff/status effect.'} | 2 |
| `TakeExtraTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'TakeExtraTurn' effect/state."} | 2 |
| `Weakness` | Number | {'type': '`Number`', 'df': "Applies or references the 'Weakness' effect/state."} | 2 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill) | Block | {'type': '`Block`', 'df': "Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 1 |
| `BonusDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'BonusDamage' effect/state."} | 1 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies or references the 'Burn' effect/state."} | 1 |
| `Charmed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charmed' effect/state."} | 1 |
| [`Conditional_FinishedSpawning`](./Abilities_and_Spells.md#context-conditional_finishedspawning) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. | 1 |
| `Doomed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Doomed' effect/state."} | 1 |
| `ForceMoveTowards` | Number | {'type': '`Number`', 'df': "Applies or references the 'ForceMoveTowards' effect/state."} | 1 |
| `Hex` | Number | {'type': '`Number`', 'df': "Applies or references the 'Hex' effect/state."} | 1 |
| `Marked` | Number | {'type': '`Number`', 'df': "Applies or references the 'Marked' effect/state."} | 1 |
| `PermanentCharm` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentCharm' effect/state."} | 1 |
| `Poison` | Number | {'type': '`Number`', 'df': "Applies or references the 'Poison' effect/state."} | 1 |
| [`Stun`](./Arrays.md#array-stun) | Array | {'type': '`Array`', 'df': "Applies or references the 'Stun' effect/state."} | 1 |
| `TempDamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempDamageUp' effect/state."} | 1 |
| [`Temporary`](./Abilities_and_Spells.md#context-temporary) | Block | {'type': '`Block`', 'df': 'A wrapper block for applying status effects that automatically expire. | 1 |

</details>

---

### Context: `splash_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#context-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 32 |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | {'type': '`Block`', 'df': 'Non-damaging status applications and logic triggers executed on impact. | 17 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 13 |
| `knockback` | Number | {'type': '`Number`', 'df': 'Knockback force of the splash blast.'} | 13 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'Classification/category type.'} | 12 |
| `makes_contact` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| `override_trample_damage` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `ai_base_score` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `crit_chance` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `force_no_knockback` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `force_play_hit_animation` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`layer`](./Enums.md#enum-layer) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Conditional_Ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 25

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'OverrideDamage' effect/state."} | 4 |
| `DamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageUp' effect/state."} | 3 |
| `KnockbackDamageImmuneUntilSettled` | Number | {'type': '`Number`', 'df': "Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state."} | 3 |
| [`Temporary`](./Abilities_and_Spells.md#context-temporary) | Block | {'type': '`Block`', 'df': 'A wrapper block for applying status effects that automatically expire. | 3 |
| `AllStatsUp` | Number | {'type': 'Number', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 2 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 2 |
| [`RandomStatUp`](./Math_Equations.md) | Equation | {'type': '`String`', 'df': "Applies or references the 'RandomStatUp' effect/state."} | 2 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': 'Block', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target.'} | 1 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill) | Block | {'type': '`Block`', 'df': "Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 1 |
| `BleedThorns` | Number | {'type': '`Number`', 'df': "Applies or references the 'BleedThorns' effect/state."} | 1 |
| `ChanceToBreak` | Number | {'type': '`Number`', 'df': "Applies or references the 'ChanceToBreak' effect/state."} | 1 |
| `Charmed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charmed' effect/state."} | 1 |
| `Cleanse` | Number | {'type': 'Number', 'df': "Applies or references the 'Cleanse' effect/state."} | 1 |
| [`Conditional_Corpse`](./Abilities_and_Spells.md#context-conditional_corpse) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 1 |
| [`Conditional_PlayerCat`](./Abilities_and_Spells.md#context-conditional_playercat) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 1 |
| `FullHeal` | Number | {'type': '`Number`', 'df': "Applies or references the 'FullHeal' effect/state."} | 1 |
| `RepairAll` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairAll' effect/state."} | 1 |
| [`ShowText`](./Strings.md#string-showtext) | String | {'type': '`String`', 'df': "Applies or references the 'ShowText' effect/state."} | 1 |
| `TempDamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempDamageUp' effect/state."} | 1 |
| `Thorns` | Number | {'type': '`Number`', 'df': "Applies or references the 'Thorns' effect/state."} | 1 |
| `ThornsDamageImmuneUntilSettled` | Number | {'type': '`Number`', 'df': "Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state."} | 1 |
| `TileDamageImmuneUntilSettled` | Number | {'type': '`Number`', 'df': "Applies or references the 'TileDamageImmuneUntilSettled' effect/state."} | 1 |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'BonusAbility' effect/state."} | 4 |
| `DamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageUp' effect/state."} | 2 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 2 |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bleed' effect/state."} | 1 |
| `Brace` | Number | {'type': '`Number`', 'df': "Applies or references the 'Brace' effect/state."} | 1 |
| `Charmed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charmed' effect/state."} | 1 |
| `Madness` | Number | {'type': '`Number`', 'df': 'Applies the Madness debuff/status effect.'} | 1 |
| `PermanentMadness` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentMadness' effect/state."} | 1 |
| `RandomMagicMissile` | Number | {'type': '`Number`', 'df': 'Fires a randomized number of magic missiles.'} | 1 |
| `TemporaryItem` | Number | {'type': '`Number`', 'df': "Applies or references the 'TemporaryItem' effect/state."} | 1 |
| `Webbed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Webbed' effect/state."} | 1 |

</details>

---

### Context: `EvolveAbilityFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum | {'type': '`Enum/String`', 'df': ''} | 13 |
| `upgraded` | Boolean | {'type': '`Boolean`', 'df': ''} | 13 |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Conditional_LastHit`](./Abilities_and_Spells.md#context-conditional_lasthit), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | {'type': '`Number`', 'df': 'The distance in tiles to knock the target away.'} | 20 |
| `stacks` | Mixed | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 18 |
| `height` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `circular_variance` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `additional_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#context-spawn)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SafeDoomed` | Mixed | {'type': '`Number`', 'df': "Applies or references the 'SafeDoomed' effect/state."} | 11 |
| `InjuryImmunity` | Number | {'type': '`Number`', 'df': "Applies or references the 'InjuryImmunity' effect/state."} | 7 |
| `AllStatsUp` | Number | {'type': 'Number', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 2 |
| `FadeInsteadOfDie` | Number | {'type': '`Number`', 'df': "Applies or references the 'FadeInsteadOfDie' effect/state."} | 2 |
| `IllusionTint` | Number | {'type': '`Number`', 'df': "Applies or references the 'IllusionTint' effect/state."} | 2 |
| `PermanentMadness` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentMadness' effect/state."} | 2 |
| [`ApplyPassivesToSpawnerWhileAlive`](./Abilities_and_Spells.md#context-applypassivestospawnerwhilealive) | Block | {'type': '`Block`', 'df': "Grants nested passives to the entity that spawned this object, lasting only as long as this object remains alive. | 1 |
| `CaptureFamiliar` | Number | {'type': '`Number`', 'df': "Applies or references the 'CaptureFamiliar' effect/state."} | 1 |
| `DamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageUp' effect/state."} | 1 |
| `FillMana` | Number | {'type': '`Number`', 'df': "Applies or references the 'FillMana' effect/state."} | 1 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 1 |
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'HideEquipment' effect/state."} | 1 |
| [`ReviveNextRound`](./Abilities_and_Spells.md#context-revivenextround) | Block | {'type': '`Block`', 'df': "Queues the character to be resurrected at the start of the next combat round. | 1 |
| `SchizoIllusionAIModifier` | Number | {'type': '`Number`', 'df': "Applies or references the 'SchizoIllusionAIModifier' effect/state."} | 1 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpeedUp' effect/state."} | 1 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 19

> **Referenced by:** [`ApplyMultipleTimes`](./Abilities_and_Spells.md#context-applymultipletimes), [`Conditional_CanBeHealed`](./Abilities_and_Spells.md#context-conditional_canbehealed), [`Conditional_HasCleansableDebuffs`](./Abilities_and_Spells.md#context-conditional_hascleansabledebuffs), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`FormChange`](./Abilities_and_Spells.md#context-formchange) | Block | {'type': '`Block`', 'df': 'Transforms the character into a different state or form (e.g., Rage, HasCat). | 12 |
| `GainCoins` | Number | {'type': '`Number`', 'df': "Applies or references the 'GainCoins' effect/state."} | 7 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 7 |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'DivineShield' effect/state."} | 6 |
| `Poison` | Number | {'type': '`Number`', 'df': "Applies or references the 'Poison' effect/state."} | 6 |
| `Slow` | Number | {'type': '`Number`', 'df': "Applies or references the 'Slow' effect/state."} | 6 |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bleed' effect/state."} | 5 |
| `Thorns` | Number | {'type': '`Number`', 'df': "Applies or references the 'Thorns' effect/state."} | 5 |
| `BonusDamage` | Mixed | {'type': '`String`', 'df': "Applies or references the 'BonusDamage' effect/state."} | 4 |
| `Charge` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charge' effect/state."} | 4 |
| `ConstitutionUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'ConstitutionUp' effect/state."} | 4 |
| `KineticSpikes` | Number | {'type': '`Number`', 'df': "Applies or references the 'KineticSpikes' effect/state."} | 4 |
| `RandomStatUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomStatUp' effect/state."} | 4 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpeedUp' effect/state."} | 4 |
| `Brace` | Number | {'type': '`Number`', 'df': "Applies or references the 'Brace' effect/state."} | 3 |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bruise' effect/state."} | 3 |
| `DamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageUp' effect/state."} | 3 |
| [`IncAuxCounterClamped`](./Abilities_and_Spells.md#context-incauxcounterclamped) | Block | {'type': '`Block`', 'df': 'Increments a generic auxiliary counter on the character, capped by a maximum value. | 3 |
| `MoveQuivered` | Number | {'type': '`Number`', 'df': "Applies or references the 'MoveQuivered' effect/state."} | 3 |
| `Quivered` | Number | {'type': '`Number`', 'df': "Applies or references the 'Quivered' effect/state."} | 3 |
| `Weakness` | Number | {'type': '`Number`', 'df': "Applies or references the 'Weakness' effect/state."} | 3 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 2 |
| `BackflipWhenTargeted` | Number | {'type': '`Number`', 'df': 'Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack.'} | 2 |
| `BleedThorns` | Number | {'type': '`Number`', 'df': "Applies or references the 'BleedThorns' effect/state."} | 2 |
| `CharismaUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'CharismaUp' effect/state."} | 2 |
| `CritChanceUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'CritChanceUp' effect/state."} | 2 |
| `DexterityUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DexterityUp' effect/state."} | 2 |
| `DiminishingHealthRegen` | Number | {'type': '`Number`', 'df': "Applies or references the 'DiminishingHealthRegen' effect/state."} | 2 |
| `DodgeChance_Status` | Number | {'type': '`Number`', 'df': "Applies or references the 'DodgeChance_Status' effect/state."} | 2 |
| `HealthRegenUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthRegenUp' effect/state."} | 2 |
| `IntelligenceUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'IntelligenceUp' effect/state."} | 2 |
| `Lifesteal` | Number | {'type': '`Number`', 'df': "Applies or references the 'Lifesteal' effect/state."} | 2 |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'LuckUp' effect/state."} | 2 |
| `Madness` | Number | {'type': '`Number`', 'df': 'Applies the Madness debuff/status effect.'} | 2 |
| `MagicWeakness` | Number | {'type': '`Number`', 'df': "Applies or references the 'MagicWeakness' effect/state."} | 2 |
| [`ManaGain`](./Math_Equations.md) | Equation | {'type': '`String`', 'df': "Applies or references the 'ManaGain' effect/state."} | 2 |
| `Marked` | Number | {'type': '`Number`', 'df': "Applies or references the 'Marked' effect/state."} | 2 |
| `PoisonLace` | Number | {'type': '`Number`', 'df': "Applies or references the 'PoisonLace' effect/state."} | 2 |
| `Reflect` | Number | {'type': '`Number`', 'df': "Applies or references the 'Reflect' effect/state."} | 2 |
| `Rot` | Number | {'type': '`Number`', 'df': "Applies or references the 'Rot' effect/state."} | 2 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'StrengthUp' effect/state."} | 2 |
| `Stun` | Number | {'type': '`Number`', 'df': "Applies or references the 'Stun' effect/state."} | 2 |
| `Tarred` | Number | {'type': '`Number`', 'df': "Applies or references the 'Tarred' effect/state."} | 2 |
| `TempCounterAttack` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempCounterAttack' effect/state."} | 2 |
| `Blind` | Number | {'type': '`Number`', 'df': "Applies or references the 'Blind' effect/state."} | 1 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies or references the 'Burn' effect/state."} | 1 |
| `Charmed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charmed' effect/state."} | 1 |
| `Confusion` | Number | {'type': '`Number`', 'df': "Applies or references the 'Confusion' effect/state."} | 1 |
| `DelayedPain` | Number | {'type': '`Number`', 'df': "Applies or references the 'DelayedPain' effect/state."} | 1 |
| `Fear` | Number | {'type': '`Number`', 'df': "Applies or references the 'Fear' effect/state."} | 1 |
| `Freeze` | Number | {'type': '`Number`', 'df': "Applies or references the 'Freeze' effect/state."} | 1 |
| `Hex` | Number | {'type': '`Number`', 'df': "Applies or references the 'Hex' effect/state."} | 1 |
| `Immobile` | Number | {'type': '`Number`', 'df': "Applies or references the 'Immobile' effect/state."} | 1 |
| `Infested` | Number | {'type': '`Number`', 'df': "Applies or references the 'Infested' effect/state."} | 1 |
| `Ostracized` | Number | {'type': '`Number`', 'df': "Applies or references the 'Ostracized' effect/state."} | 1 |
| `Petrify` | Number | {'type': '`Number`', 'df': "Applies or references the 'Petrify' effect/state."} | 1 |
| `RandomStatDown` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomStatDown' effect/state."} | 1 |
| `RefreshActPoints` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshActPoints' effect/state."} | 1 |
| `RefreshMovePoints` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshMovePoints' effect/state."} | 1 |
| `Scrambled` | Number | {'type': '`Number`', 'df': "Applies or references the 'Scrambled' effect/state."} | 1 |
| `Sleep` | Number | {'type': '`Number`', 'df': "Applies or references the 'Sleep' effect/state."} | 1 |
| `SpellDamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpellDamageUp' effect/state."} | 1 |

</details>

---

### Context: `Consumed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#context-conditional_livingplayercat), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | {'type': '`Enum/String`', 'df': 'Ability triggered by the consumed entity while inside the consumer.'} | 13 |
| `force_contact` | Boolean | {'type': '`Boolean`', 'df': 'If true, enforces physical overlap.'} | 11 |
| `instant` | Boolean | {'type': '`Boolean`', 'df': ''} | 8 |
| `mount_mode` | Mixed | {'type': '`Enum/String`', 'df': 'If true, treats the consumption as riding/mounting instead of eating.'} | 8 |
| `wet` | Boolean | {'type': '`Boolean`', 'df': ''} | 8 |
| `do_not_pop_corpse` | Boolean | {'type': '`Boolean`', 'df': ''} | 7 |
| `drop_on_death` | Mixed | {'type': '`Enum/String`', 'df': ''} | 7 |
| `drop_on_self_death` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| [`extra_statuses`](./Abilities_and_Spells.md#context-extra_statuses) | Block | {'type': '`Block`', 'df': "Additional generic status applications. | 3 |
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `kill_on_consume` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `use_placeholder` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `Conditional_Boss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 17

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#context-conditional_hasstatus) | Block | {'type': 'Block', 'df': 'Conditional trigger: Executes nested logic if the target currently has the specified status effect.'} | 6 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | {'type': 'Block', 'df': 'Fallback block that executes if the preceding `Conditional_` block evaluated to false.'} | 4 |
| `OverrideDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'OverrideDamage' effect/state."} | 4 |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'RemoveStatus' effect/state."} | 4 |
| [`VisualFX`](./Enums.md#enum-visualfx) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'VisualFX' effect/state."} | 3 |
| `BonusDamage` | Number | {'type': 'String', 'df': "Applies or references the 'BonusDamage' effect/state."} | 2 |
| `Drowsy` | Number | {'type': '`Number`', 'df': "Applies or references the 'Drowsy' effect/state."} | 2 |
| `ExplodeCharacter_PartyBoss` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExplodeCharacter_PartyBoss' effect/state."} | 2 |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExplodeCharacter_RockCrusher_PetrifyBreak' effect/state."} | 2 |
| `Stun` | Number | {'type': '`Number`', 'df': "Applies or references the 'Stun' effect/state."} | 2 |
| `Charmed` | Number | {'type': 'Number', 'df': "Applies or references the 'Charmed' effect/state."} | 1 |
| `ExplodeCharacter_NoDie` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExplodeCharacter_NoDie' effect/state."} | 1 |
| `Fear` | Number | {'type': '`Number`', 'df': "Applies or references the 'Fear' effect/state."} | 1 |
| [`XIsTargetHealth`](./Abilities_and_Spells.md#context-xistargethealth) | Block | {'type': '`Block`', 'df': "Math variable assignment: Evaluates X as the target's current health."} | 1 |

</details>

---

### Context: `FormChange`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `form` | Mixed | {'type': '`String`', 'df': ''} | 75 |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |

</details>

---

### Context: `ApplyToSourceOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'RemoveItem' effect/state."} | 3 |
| `AlphaCat` | Number | {'type': '`Number`', 'df': "Applies or references the 'AlphaCat' effect/state."} | 2 |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'CompleteItemQuest' effect/state."} | 2 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 2 |
| `ManaGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'ManaGain' effect/state."} | 2 |
| `Revive` | Number | {'type': '`Number`', 'df': "Applies or references the 'Revive' effect/state."} | 2 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 1 |
| [`EvolveAbilityFromPool`](./Enums.md#enum-evolveabilityfrompool) | Enum | {'type': '`Enum/String`', 'df': 'Upgrades or transforms an existing ability into a new one from the specified pool.'} | 1 |
| `RefreshActPoints` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshActPoints' effect/state."} | 1 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'StrengthUp' effect/state."} | 1 |
| `TakeExtraTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'TakeExtraTurn' effect/state."} | 1 |
| [`TransformWeapon`](./Abilities_and_Spells.md#context-transformweapon) | Block | {'type': '`Block`', 'df': 'Transforms the equipped weapon into another specific weapon state. | 1 |
| [`WeaponAuxMultiplier`](./Enums.md#enum-weaponauxmultiplier) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'WeaponAuxMultiplier' effect/state."} | 1 |

</details>

---

### Context: `CanApplyToInanimate`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum | {'type': '`Enum/String`', 'df': 'Spawns a specific character or entity upon impact.'} | 10 |
| [`BreakIntoRocks`](./Enums.md#enum-breakintorocks) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'BreakIntoRocks' effect/state."} | 4 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 |
| `Vaporize` | Number | {'type': '`Number`', 'df': "Applies or references the 'Vaporize' effect/state."} | 3 |
| `GetAggroTarget` | Number | {'type': '`Number`', 'df': "Applies or references the 'GetAggroTarget' effect/state."} | 2 |
| `PreventDeathTransforms` | Number | {'type': '`Number`', 'df': "Applies or references the 'PreventDeathTransforms' effect/state."} | 1 |
| [`Temporary`](./Abilities_and_Spells.md#context-temporary) | Block | {'type': '`Block`', 'df': 'A wrapper block for applying status effects that automatically expire. | 1 |

</details>

---

### Context: `CatPartsTransform`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ear1` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the front ear.'} | 10 |
| `tail` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the tail.'} | 10 |
| `ear2` | Number | {'type': '`Number`', 'df': ''} | 9 |
| `arm2` | Number | {'type': '`Number`', 'df': ''} | 8 |
| `mouth` | Number | {'type': '`Number`', 'df': ''} | 8 |
| `arm1` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the front arm.'} | 7 |
| `leg1` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the front leg.'} | 5 |
| `leg2` | Number | {'type': '`Number`', 'df': ''} | 5 |
| `head` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the head.'} | 3 |
| `texture` | Number | {'type': '`Number`', 'df': ''} | 3 |
| `body` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the body.'} | 2 |
| `eye1` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `eye2` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `eyebrow1` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `eyebrow2` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `palette` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `Conditional_NotBoss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Number | {'type': 'Number', 'df': "Applies or references the 'CaptureFamiliar' effect/state."} | 2 |
| `Doomed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Doomed' effect/state."} | 2 |
| `ExplodeCharacter_RockCrusher` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExplodeCharacter_RockCrusher' effect/state."} | 2 |
| `FactionConversion` | Number | {'type': '`Number`', 'df': "Applies or references the 'FactionConversion' effect/state."} | 2 |
| `Vaporize` | Number | {'type': '`Number`', 'df': "Applies or references the 'Vaporize' effect/state."} | 2 |
| `VaporizeInanimate` | Number | {'type': '`Number`', 'df': "Applies or references the 'VaporizeInanimate' effect/state."} | 2 |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate) | Block | {'type': '`Block`', 'df': "Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 1 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#context-conditional_healththreshold) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 1 |
| [`Fear`](./Arrays.md#array-fear) | Array | {'type': '`Array`', 'df': "Applies or references the 'Fear' effect/state."} | 1 |
| `PermanentCharm` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentCharm' effect/state."} | 1 |

</details>

---

### Context: `Conditional_HasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The specific status ID to check for.'} | 13 |
| `BonusDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'BonusDamage' effect/state."} | 6 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies or references the 'Burn' effect/state."} | 2 |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'RemoveStatus' effect/state."} | 2 |
| `Slow` | Number | {'type': '`Number`', 'df': "Applies or references the 'Slow' effect/state."} | 2 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| `Confusion` | Number | {'type': '`Number`', 'df': "Applies or references the 'Confusion' effect/state."} | 1 |
| `Fear` | Number | {'type': '`Number`', 'df': "Applies or references the 'Fear' effect/state."} | 1 |
| [`FormChange`](./Enums.md#enum-formchange) | Enum | {'type': '`Enum/String`', 'df': 'Transforms the character into a different state or form (e.g., Rage, HasCat).'} | 1 |
| `Quivered` | Number | {'type': '`Number`', 'df': "Applies or references the 'Quivered' effect/state."} | 1 |

</details>

---

### Context: `RandomMagicMissile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `full_size` | Boolean | {'type': '`Boolean`', 'df': 'If true, fires normal sized missiles instead of mini ones.'} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 2 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `odds` | Number | {'type': '`Number`', 'df': "The probability (0.0 to 1.0) of triggering the 'good roll' success state."} | 12 |
| [`GainDisorderFromPool_PostCast`](./Enums.md#enum-gaindisorderfrompool_postcast) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'GainDisorderFromPool_PostCast' effect/state."} | 7 |
| [`ApplyToRandomPartyMemberIfPossible`](./Abilities_and_Spells.md#context-applytorandompartymemberifpossible) | Block | {'type': '`Block`', 'df': "Redirects the nested effects to apply to a random living member of the player's party. | 1 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`GainDisorder`](./Enums.md#enum-gaindisorder) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'GainDisorder' effect/state."} | 1 |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ImmediateUseAbility' effect/state."} | 1 |
| `RefreshWeaponAbility` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshWeaponAbility' effect/state."} | 1 |
| [`ShowText`](./Strings.md#string-showtext) | String | {'type': '`String`', 'df': "Applies or references the 'ShowText' effect/state."} | 1 |

</details>

---

### Context: `Conditional_Speculative`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`Conditional_AffectedByElement`](./Abilities_and_Spells.md#context-conditional_affectedbyelement), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `IgnoreDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'IgnoreDamage' effect/state."} | 3 |
| `BonusDamageBasedOnDistance` | Number | {'type': '`Number`', 'df': "Applies or references the 'BonusDamageBasedOnDistance' effect/state."} | 2 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#context-conditional_healththreshold) | Block | {'type': 'Block', 'df': "Conditional trigger: Executes nested logic if the target's health falls below the specified threshold."} | 2 |
| `BonusDamage` | Number | {'type': 'Number', 'df': "Applies or references the 'BonusDamage' effect/state."} | 1 |
| `CapDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'CapDamage' effect/state."} | 1 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | {'type': 'Block', 'df': 'Fallback block that executes if the preceding `Conditional_` block evaluated to false.'} | 1 |
| `Knockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'Knockback' effect/state."} | 1 |
| `RandomBonusDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomBonusDamage' effect/state."} | 1 |

</details>

---

### Context: `DoScreenShake`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `intensity` | Number | {'type': '`Number`', 'df': ''} | 10 |
| `time` | Mixed | {'type': '`Number`', 'df': ''} | 10 |

</details>

---

### Context: `ChanceToBreakFree`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ability triggered upon successfully breaking free.'} | 11 |
| [`fail_ability`](./Enums.md#enum-fail_ability) | Enum | {'type': '`Enum/String`', 'df': 'The ability triggered if the break free attempt fails.'} | 3 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Percentage base chance to break free.'} | 3 |

</details>

---

### Context: `ChangeTile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tile`](./Arrays.md#array-tile) | Array | {'type': '`Enum/String`', 'df': 'The specific tile type to change into (e.g., GlassTile).'} | 11 |
| `chance` | Mixed | {'type': '`Enum/String`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 2 |
| `aoe` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `Cleave`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | {'type': '`Enum/String`', 'df': 'Probability (0.0 to 1.0) that the cleave effect triggers.'} | 1 |

</details>

---

### Context: `ApplyPassives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`Conditional_RandomChance`](./Abilities_and_Spells.md#context-conditional_randomchance), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`StatusOnBattleEnd`](./Abilities_and_Spells.md#context-statusonbattleend) | Block | {'type': '`Block`', 'df': "Applies the nested status effects when the encounter finishes. | 3 |
| [`AddTag`](./Enums.md#enum-addtag) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'AddTag' effect/state."} | 2 |
| `Flying` | Number | {'type': '`Number`', 'df': "Applies or references the 'Flying' effect/state."} | 2 |
| `IgnoreTiles` | Number | {'type': '`Number`', 'df': "Applies or references the 'IgnoreTiles' effect/state."} | 2 |
| [`YOffset`](./Enums.md#enum-yoffset) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'YOffset' effect/state."} | 2 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ElementImmune' effect/state."} | 1 |
| `KnockbackImmunity` | Number | {'type': '`Number`', 'df': "Applies or references the 'KnockbackImmunity' effect/state."} | 1 |
| `Plant` | Number | {'type': '`Number`', 'df': "Applies or references the 'Plant' effect/state."} | 1 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ReplaceBasicAttack' effect/state."} | 1 |

</details>

---

### Context: `Conditional_FormulaIsPositive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`formula`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': 'The math expression to evaluate.'} | 8 |
| [`Burn`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'Burn' effect/state."} | 2 |
| `Immobile` | Number | {'type': '`Number`', 'df': "Applies or references the 'Immobile' effect/state."} | 2 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 2 |
| `Freeze` | Number | {'type': '`Number`', 'df': "Applies or references the 'Freeze' effect/state."} | 1 |
| [`OverrideKnockbackDamage`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'OverrideKnockbackDamage' effect/state."} | 1 |
| [`Slow`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'Slow' effect/state."} | 1 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpeedUp' effect/state."} | 1 |
| `Stun` | Number | {'type': '`Number`', 'df': "Applies or references the 'Stun' effect/state."} | 1 |

</details>

---

### Context: `Craft`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum | {'type': '`Enum/String`', 'df': ''} | 9 |
| [`slot`](./Enums.md#enum-slot) | Enum | {'type': '`Enum/String`', 'df': ''} | 8 |
| `temporary` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| `works_with_tech` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `ApplyStatusIfCrit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 6 |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bleed' effect/state."} | 3 |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'LuckUp' effect/state."} | 1 |

</details>

---

### Context: `Conditional_Corpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Revive` | Number | {'type': '`Number`', 'df': "Applies or references the 'Revive' effect/state."} | 4 |
| `AllStatsUp` | Number | {'type': 'Number', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 2 |
| [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is hostile to the caster. | 1 |
| `FlatAIBonus` | Number | {'type': '`Number`', 'df': "Applies or references the 'FlatAIBonus' effect/state."} | 1 |
| `HealRandomInjury` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealRandomInjury' effect/state."} | 1 |
| `PermanentCharm` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentCharm' effect/state."} | 1 |

</details>

---

### Context: `Conditional_InForm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum | {'type': '`Enum/String`', 'df': 'The specific form ID to check for.'} | 7 |
| [`FormChange`](./Enums.md#enum-formchange) | Enum | {'type': '`Enum/String`', 'df': 'Transforms the character into a different state or form (e.g., Rage, HasCat).'} | 5 |
| `CritChanceUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'CritChanceUp' effect/state."} | 1 |
| `DamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageUp' effect/state."} | 1 |
| `DodgeChance_Status` | Number | {'type': '`Number`', 'df': "Applies or references the 'DodgeChance_Status' effect/state."} | 1 |
| [`ForceImmediateMoveAndAttack`](./Abilities_and_Spells.md#context-forceimmediatemoveandattack) | Block | {'type': '`Block`', 'df': 'Forces the character to immediately move to a target and use a specified ability. | 1 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpeedUp' effect/state."} | 1 |
| [`UseAbility`](./Enums.md#enum-useability) | Enum | {'type': '`Enum/String`', 'df': 'Forces the character or target to instantly use a specified ability.'} | 1 |

</details>

---

### Context: `ForceAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `immediate` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific dodge ability to trigger (e.g., DestroyerDodge).'} | 4 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 4 |

</details>

---

### Context: `Conditional_HealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `threshold_flat` | Number | {'type': '`Number`', 'df': 'A flat numerical health value threshold.'} | 4 |
| [`SpawnThingIfHitKills`](./Enums.md#enum-spawnthingifhitkills) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'SpawnThingIfHitKills' effect/state."} | 2 |
| `threshold_percent` | Number | {'type': '`Number`', 'df': 'A percentage-based health threshold (e.g. 50%).'} | 2 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`BonusDamage`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'BonusDamage' effect/state."} | 1 |
| `CaptureFamiliar` | Number | {'type': '`Number`', 'df': "Applies or references the 'CaptureFamiliar' effect/state."} | 1 |
| `Die` | Number | {'type': '`Number`', 'df': "Applies or references the 'Die' effect/state."} | 1 |
| `DieViolently` | Number | {'type': '`Number`', 'df': "Applies or references the 'DieViolently' effect/state."} | 1 |
| `FactionConversion` | Number | {'type': '`Number`', 'df': "Applies or references the 'FactionConversion' effect/state."} | 1 |
| `FlatLeech` | Number | {'type': '`Number`', 'df': "Applies or references the 'FlatLeech' effect/state."} | 1 |
| `FullHeal` | Number | {'type': '`Number`', 'df': "Applies or references the 'FullHeal' effect/state."} | 1 |
| `Instakill` | Number | {'type': '`Number`', 'df': "Applies or references the 'Instakill' effect/state."} | 1 |
| `Vaporize` | Number | {'type': '`Number`', 'df': "Applies or references the 'Vaporize' effect/state."} | 1 |
| [`threshold_expr`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Conditional_Object`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag) | Block | {'type': 'Block', 'df': 'Conditional trigger: Executes nested logic if the target possesses the specified entity tag.'} | 3 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | {'type': 'Block', 'df': 'Fallback block that executes if the preceding `Conditional_` block evaluated to false.'} | 3 |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate) | Block | {'type': 'Block', 'df': 'Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters.'} | 1 |
| `RepairWeapon` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairWeapon' effect/state."} | 1 |

</details>

---

### Context: `Conditional_PlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ConjureRandomAbilityFromCat` | Number | {'type': '`Number`', 'df': "Applies or references the 'ConjureRandomAbilityFromCat' effect/state."} | 2 |
| `Adrenaline` | Number | {'type': '`Number`', 'df': "Applies or references the 'Adrenaline' effect/state."} | 1 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| `Cleanse` | Number | {'type': '`Number`', 'df': "Applies or references the 'Cleanse' effect/state."} | 1 |
| `GenericDebuff` | Number | {'type': '`Number`', 'df': "Applies or references the 'GenericDebuff' effect/state."} | 1 |
| [`KnockOutClone`](./Enums.md#enum-knockoutclone) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'KnockOutClone' effect/state."} | 1 |
| `Scrambled` | Number | {'type': '`Number`', 'df': "Applies or references the 'Scrambled' effect/state."} | 1 |
| `T2CopyCat` | Number | {'type': '`Number`', 'df': "Applies or references the 'T2CopyCat' effect/state."} | 1 |

</details>

---

### Context: `ConjureBonusAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to conjure.'} | 2 |
| `upgraded` | Boolean | {'type': '`Boolean`', 'df': 'If true, conjures the upgraded version of the ability.'} | 2 |

</details>

---

### Context: `DoDistortionRing`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `intensity` | Number | {'type': '`Number`', 'df': ''} | 6 |
| `radius` | Number | {'type': '`Number`', 'df': 'Distance or area of effect in tiles.'} | 6 |
| `speed` | Number | {'type': '`Number`', 'df': ''} | 6 |

</details>

---

### Context: `Metronome`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`banned_abilities`](./Arrays.md#array-banned_abilities) | Array | {'type': '`Array`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `ObjectOnHitCharacter`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Mixed | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0) of spawning.'} | 2 |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': 'The entity ID of the character to spawn (e.g., CharmedFlea).'} | 2 |

</details>

---

### Context: `SwitchMusic`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | {'type': '`Enum/String`', 'df': 'The specific audio layer to transition to (e.g., map, battle).'} | 6 |
| [`new_song`](./Enums.md#enum-new_song) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the new music track.'} | 5 |
| `crossfade_speed` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `TwisterDisplaceWithDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Mixed | {'type': '`Number`', 'df': 'The damage formula or inherit flag.'} | 6 |
| `max_dist` | Number | {'type': '`Number`', 'df': 'Maximum displacement distance.'} | 6 |
| `min_dist` | Number | {'type': '`Number`', 'df': 'Minimum displacement distance.'} | 2 |
| [`exclude_prefix`](./Enums.md#enum-exclude_prefix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `CollectsPickupsWithAltEffects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | {'type': '`Number`', 'df': "Applies or references the 'Tech' effect/state."} | 2 |
| `CurrentWeaponAddPoison` | Number | {'type': '`Number`', 'df': "Applies or references the 'CurrentWeaponAddPoison' effect/state."} | 1 |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'LuckUp' effect/state."} | 1 |
| `Quivered` | Number | {'type': '`Number`', 'df': "Applies or references the 'Quivered' effect/state."} | 1 |
| `RandomStatUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomStatUp' effect/state."} | 1 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 1 |

</details>

---

### Context: `DestroyEquipmentAndAttachParasite`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`Conditional_ActiveWeather_Any`](./Abilities_and_Spells.md#context-conditional_activeweather_any), [`Conditional_DebuffRoll`](./Abilities_and_Spells.md#context-conditional_debuffroll), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | {'type': '`Enum/String`', 'df': 'The item pool to draw the parasite from.'} | 5 |
| `chance` | Mixed | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 3 |

</details>

---

### Context: `DoDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Else`](./Abilities_and_Spells.md#context-else), [`post_spawn_statuses`](./Abilities_and_Spells.md#context-post_spawn_statuses)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The flat damage amount.'} | 5 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification of the damage (e.g., spell, melee).'} | 5 |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | {'type': '`Block`', 'df': 'Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 2 |

</details>

---

### Context: `LeaveBehind`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#context-temporary_effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': 'The entity ID to spawn.'} | 4 |

</details>

---

### Context: `ObjectOnHit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': 'The entity ID of the object to spawn (e.g., Poop).'} | 2 |

</details>

---

### Context: `ApplyToConsumed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DeleteObject` | Number | {'type': '`Number`', 'df': "Applies or references the 'DeleteObject' effect/state."} | 3 |
| `Die` | Number | {'type': '`Number`', 'df': "Applies or references the 'Die' effect/state."} | 1 |

</details>

---

### Context: `ArcLightning`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | {'type': '`Boolean`', 'df': 'If true, the arc will not bounce to friendly targets.'} | 4 |
| `max_distance` | Number | {'type': '`Number`', 'df': 'The maximum tile range the lightning can jump between bounces.'} | 4 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The maximum number of targets the lightning can bounce to.'} | 4 |
| [`chance`](./Enums.md#enum-chance) | Enum | {'type': '`Enum/String`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |
| `ignore_self` | Boolean | {'type': '`Boolean`', 'df': 'If true, prevents the arc from bouncing back to the caster.'} | 1 |

</details>

---

### Context: `Conditional_Familiar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageUp' effect/state."} | 2 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 1 |
| `BonusDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'BonusDamage' effect/state."} | 1 |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'DivineShield' effect/state."} | 1 |

</details>

---

### Context: `GainCoinsRange`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number | {'type': '`Number`', 'df': 'Maximum coins granted.'} | 4 |
| `min` | Number | {'type': '`Number`', 'df': 'Minimum coins granted.'} | 4 |

</details>

---

### Context: `LateStatusApplication`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CurrentWeaponDamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'CurrentWeaponDamageUp' effect/state."} | 3 |
| `AddWeaponAux` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddWeaponAux' effect/state."} | 1 |

</details>

---

### Context: `ReplaceSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#context-temppassivewhilehasstatus)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The new ability ID to insert.'} | 4 |
| `slot` | Number | {'type': '`Number`', 'df': 'The spell slot index to replace.'} | 4 |

</details>

---

### Context: `ReviveNextRound`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#context-additional_passives), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `revive_health` | Number | {'type': '`Number`', 'df': 'The flat amount of health to revive with.'} | 3 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 2 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 2 |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'DivineShield' effect/state."} | 1 |

</details>

---

### Context: `TakeBonusTurnWithStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | {'type': '`Number`', 'df': 'Applies the Madness debuff/status effect.'} | 2 |
| [`Stun`](./Arrays.md#array-stun) | Array | {'type': '`Number`', 'df': "Applies or references the 'Stun' effect/state."} | 2 |
| `TempNoManaRegen` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempNoManaRegen' effect/state."} | 2 |
| `Confusion` | Number | {'type': '`Number`', 'df': "Applies or references the 'Confusion' effect/state."} | 1 |

</details>

---

### Context: `TempPassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`Conditional_FirstApplicationThisTurn`](./Abilities_and_Spells.md#context-conditional_firstapplicationthisturn), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#context-conditional_livingplayercat)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ReplaceSpell`](./Abilities_and_Spells.md#context-replacespell) | Block | {'type': '`Block`', 'df': "Replaces a spell in the character's hand/deck with a different one. | 4 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The required status effect.'} | 3 |
| [`MeleeRevengeDamage`](./Abilities_and_Spells.md#context-meleerevengedamage) | Block | {'type': '`Block`', 'df': 'Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. | 2 |
| `AddManaRegen` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddManaRegen' effect/state."} | 1 |
| `HealthRegenUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthRegenUp' effect/state."} | 1 |

</details>

---

### Context: `TimeDelayStatusApplication`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `delay` | Mixed | {'type': '`Number`', 'df': 'The float time delay in seconds.'} | 4 |
| [`SwitchMusic`](./Abilities_and_Spells.md#context-switchmusic) | Block | {'type': '`Block`', 'df': 'Changes the background music track or layer during combat. | 2 |
| `Cleanse` | Number | {'type': '`Number`', 'df': "Applies or references the 'Cleanse' effect/state."} | 1 |
| [`CreateGlobalModifiers`](./Abilities_and_Spells.md#context-createglobalmodifiers) | Block | {'type': '`Block`', 'df': "Generates global map or encounter rules/modifiers. | 1 |
| [`DoScreenShake`](./Abilities_and_Spells.md#context-doscreenshake) | Block | {'type': '`Block`', 'df': 'Triggers a camera screen shake effect. | 1 |
| [`FormChange`](./Enums.md#enum-formchange) | Enum | {'type': '`Enum/String`', 'df': 'Transforms the character into a different state or form (e.g., Rage, HasCat).'} | 1 |
| `FullHeal` | Number | {'type': '`Number`', 'df': "Applies or references the 'FullHeal' effect/state."} | 1 |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'GlobalSpawnCharacter' effect/state."} | 1 |
| `PlayBackground` | Number | {'type': '`Number`', 'df': "Applies or references the 'PlayBackground' effect/state."} | 1 |
| [`RemoveAmbientLightEffects`](./Enums.md#enum-removeambientlighteffects) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'RemoveAmbientLightEffects' effect/state."} | 1 |
| `Vaporize` | Number | {'type': '`Number`', 'df': "Applies or references the 'Vaporize' effect/state."} | 1 |

</details>

---

### Context: `post_spawn_statuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#context-spawn)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DoDamage`](./Abilities_and_Spells.md#context-dodamage) | Block | {'type': '`Block`', 'df': 'Explicitly triggers a secondary damage instance independent of the main attack. | 2 |
| [`EnterMount`](./Enums.md#enum-entermount) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'EnterMount' effect/state."} | 1 |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'VisualFXTile' effect/state."} | 1 |

</details>

---

### Context: `rocket_swirl`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`radius`](./Arrays.md#array-radius) | Array | {'type': '`Array`', 'df': 'Swirl radius.'} | 4 |
| [`speed`](./Arrays.md#array-speed) | Array | {'type': '`Array`', 'df': 'Rotations per second.'} | 4 |

</details>

---

### Context: `ApplyMultipleTimes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | {'type': '`Block`', 'df': 'Selects and applies a random status effect from the provided nested block. | 3 |
| `stacks` | Mixed | {'type': '`Number`', 'df': 'The number of times the nested effects block should be repeatedly executed.'} | 3 |

</details>

---

### Context: `BounceObject`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`obj`](./Enums.md#enum-obj) | Enum | {'type': '`Enum/String`', 'df': 'The entity ID of the object to spawn (e.g., chapter_corpse_medium).'} | 3 |
| [`chance`](./Enums.md#enum-chance) | Enum | {'type': '`Enum/String`', 'df': 'Probability (0.0 to 1.0) of spawning the object.'} | 2 |
| `slide` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `CatPartsSizeScaleStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `arm1` | Number | {'type': '`Number`', 'df': 'Scale multiplier for the front arm.'} | 1 |
| `arm2` | Number | {'type': '`Number`', 'df': 'Scale multiplier for the back arm.'} | 1 |
| `body` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `mouth` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `Conditional_AffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'The specific element type to check for.'} | 3 |
| `BonusCritChance` | Number | {'type': '`Number`', 'df': "Applies or references the 'BonusCritChance' effect/state."} | 2 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies or references the 'Burn' effect/state."} | 1 |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative) | Block | {'type': '`Block`', 'df': "A simulation block used by the AI to test hypothetical outcomes before committing to an action. | 1 |

</details>

---

### Context: `Conditional_FirstApplicationThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#context-temppassivewhilehasstatus) | Block | {'type': '`Block`', 'df': "Grants nested passives only while the character possesses the specified status. | 3 |
| [`key`](./Enums.md#enum-key) | Enum | {'type': '`Enum/String`', 'df': 'A unique string identifier to track this specific application.'} | 3 |

</details>

---

### Context: `Conditional_LastHit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#context-knockupandaway) | Block | {'type': '`Block`', 'df': 'Displaces the target vertically and horizontally away from the source. | 2 |
| `BonusDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'BonusDamage' effect/state."} | 1 |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bruise' effect/state."} | 1 |
| [`DelayCastAbility`](./Enums.md#enum-delaycastability) | Enum | {'type': '`Enum/String`', 'df': 'Queues an ability to be cast automatically after a certain delay or trigger.'} | 1 |

</details>

---

### Context: `DustOnHit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the object/particle to spawn.'} | 3 |

</details>

---

### Context: `IncAuxCounterClamped`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `change` | Number | {'type': '`Number`', 'df': ''} | 3 |
| `max` | Number | {'type': '`Number`', 'df': ''} | 3 |

</details>

---

### Context: `SetCrazyEyeBackgroundWeights`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Arrays.md#array-weights) | Array | {'type': '`Array`', 'df': ''} | 3 |

</details>

---

### Context: `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ApplyPassives`](./Abilities_and_Spells.md#context-applypassives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | {'type': '`Boolean`', 'df': 'If true, triggers the effect even if the character died during the battle.'} | 3 |
| [`RandomTaggedMutation`](./Enums.md#enum-randomtaggedmutation) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'RandomTaggedMutation' effect/state."} | 2 |
| `RandomMutation` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomMutation' effect/state."} | 1 |

</details>

---

### Context: `Tangled`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_art`](./Enums.md#enum-alt_art) | Enum | {'type': '`Enum/String`', 'df': 'The alternative sprite art to use while tangled.'} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `extra_statuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`Consumed`](./Abilities_and_Spells.md#context-consumed)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies or references the 'Burn' effect/state."} | 1 |
| `Poison` | Number | {'type': '`Number`', 'df': "Applies or references the 'Poison' effect/state."} | 1 |
| `Tarred` | Number | {'type': '`Number`', 'df': "Applies or references the 'Tarred' effect/state."} | 1 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`PassiveWhileNotTakingTurn`](./Abilities_and_Spells.md#context-passivewhilenottakingturn), [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bleed' effect/state."} | 1 |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bruise' effect/state."} | 1 |

</details>

---

### Context: `AfterImage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#context-temporary_effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': 'The entity ID of the visual decoy to spawn (e.g., PlayerCat_ThiefShade).'} | 2 |
| `skilltemp` | Boolean | {'type': '`Boolean`', 'df': 'If true, the decoy is automatically destroyed once the skill finishes executing.'} | 2 |

</details>

---

### Context: `ApplyToRandomPartyMemberIfPossible`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_GoodRoll`](./Abilities_and_Spells.md#context-conditional_goodroll), [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`GainDisorderFromPool_PostCast`](./Enums.md#enum-gaindisorderfrompool_postcast) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'GainDisorderFromPool_PostCast' effect/state."} | 2 |

</details>

---

### Context: `ApplyToTile`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_DestructibleCorpse`](./Abilities_and_Spells.md#context-conditional_destructiblecorpse)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHit`](./Enums.md#enum-objectonhit) | Enum | {'type': '`Enum/String`', 'df': 'Spawns a specific physics/item object upon impact.'} | 2 |
| `SpawnBearTrap` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpawnBearTrap' effect/state."} | 2 |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to autocast.'} | 2 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': 'If true, bypasses stun and hard-CC restrictions to cast anyway.'} | 1 |

</details>

---

### Context: `BodyGuard`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to use when intercepting (e.g., BodyGuardSwap).'} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 2 |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Enum | {'type': '`Enum/String`', 'df': "The probability (0.0 to 1.0) of triggering the 'bad roll' failure state."} | 2 |
| `DieViolently` | Number | {'type': '`Number`', 'df': "Applies or references the 'DieViolently' effect/state."} | 1 |
| `Instakill` | Number | {'type': '`Number`', 'df': "Applies or references the 'Instakill' effect/state."} | 1 |

</details>

---

### Context: `Conditional_BossOrBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Immobile`](./Arrays.md#array-immobile) | Array | {'type': '`Array`', 'df': "Applies or references the 'Immobile' effect/state."} | 2 |

</details>

---

### Context: `Conditional_Buddy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_InForm`](./Abilities_and_Spells.md#context-conditional_inform) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 1 |
| [`Consumed`](./Abilities_and_Spells.md#context-consumed) | Block | {'type': 'Block', 'df': 'State block triggered when this object or entity is eaten/consumed by another character.'} | 1 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | {'type': 'Block', 'df': 'Fallback block that executes if the preceding `Conditional_` block evaluated to false.'} | 1 |

</details>

---

### Context: `Conditional_DestructibleCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ApplyToTile`](./Abilities_and_Spells.md#context-applytotile) | Block | {'type': '`Block`', 'df': "Redirects the nested effects to apply to the terrain/tile underneath the target rather than the target itself. | 2 |
| `VaporizeCorpse` | Number | {'type': '`Number`', 'df': "Applies or references the 'VaporizeCorpse' effect/state."} | 2 |

</details>

---

### Context: `Conditional_Displaceable`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`LaunchOffScreen`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'LaunchOffScreen' effect/state."} | 1 |
| `LaunchOffScreenInstakill` | Number | {'type': '`Number`', 'df': "Applies or references the 'LaunchOffScreenInstakill' effect/state."} | 1 |
| `TempInitiativeChange` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempInitiativeChange' effect/state."} | 1 |

</details>

---

### Context: `Conditional_IsSelf`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'OverrideDamage' effect/state."} | 1 |

</details>

---

### Context: `Conditional_NotAlly`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | {'type': '`Number`', 'df': "Applies or references the 'Confusion' effect/state."} | 1 |
| [`Temporary`](./Abilities_and_Spells.md#context-temporary) | Block | {'type': '`Block`', 'df': 'A wrapper block for applying status effects that automatically expire. | 1 |

</details>

---

### Context: `Conditional_NotBossOrBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Immobile` | Number | {'type': '`Number`', 'df': "Applies or references the 'Immobile' effect/state."} | 2 |

</details>

---

### Context: `Conditional_NotShielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Knockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'Knockback' effect/state."} | 2 |

</details>

---

### Context: `Conditional_OncePerBattle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'CompleteItemQuest' effect/state."} | 2 |
| `TriggerGameEnding` | Number | {'type': '`Number`', 'df': "Applies or references the 'TriggerGameEnding' effect/state."} | 2 |
| [`key`](./Enums.md#enum-key) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `Conditional_Shielded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Cleave` | Number | {'type': '`Number`', 'df': 'Causes the attack to hit adjacent enemies alongside the primary target.'} | 2 |
| [`BonusDamage`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'BonusDamage' effect/state."} | 1 |
| `Stun` | Number | {'type': '`Number`', 'df': "Applies or references the 'Stun' effect/state."} | 1 |

</details>

---

### Context: `CopySpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |
| `upgraded` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `CreateGlobalModifiers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BloodRain` | Number | {'type': '`Number`', 'df': "Applies or references the 'BloodRain' effect/state."} | 2 |
| [`LowerAmbientLight`](./Abilities_and_Spells.md#context-lowerambientlight) | Block | {'type': '`Block`', 'df': "A visual effect that dims the map's lighting. | 2 |

</details>

---

### Context: `FindItemFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | {'type': '`Enum/String`', 'df': 'Probability of finding the item.'} | 2 |
| [`pool`](./Enums.md#enum-pool) | Enum | {'type': '`Enum/String`', 'df': 'The item pool to draw from.'} | 1 |

</details>

---

### Context: `ForceMoveTowardsTaggedObject`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The movement ability to use.'} | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The entity tag to seek out.'} | 1 |

</details>

---

### Context: `KnockOutCoin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | {'type': '`Enum/String`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `LowerAmbientLight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`CreateGlobalModifiers`](./Abilities_and_Spells.md#context-createglobalmodifiers)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array | {'type': '`Array`', 'df': 'The target opacity/dimness level.'} | 2 |
| `speed` | Number | {'type': '`Number`', 'df': 'The transition speed.'} | 2 |

</details>

---

### Context: `Math`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Stun` | Number | {'type': '`Number`', 'df': "Applies or references the 'Stun' effect/state."} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 2 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#context-temppassivewhilehasstatus)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | {'type': '`Block`', 'df': 'Non-damaging status applications and logic triggers executed on impact. | 2 |

</details>

---

### Context: `NextAttackSpecialCrit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Number | {'type': '`Number`', 'df': 'Flat addition to the critical damage multiplier.'} | 1 |
| `extra_coins_per_stack` | Number | {'type': '`Number`', 'df': 'Grants bonus coins based on stacks.'} | 1 |
| `luck_increase` | Number | {'type': '`Number`', 'df': 'Increases luck stat for the attack.'} | 1 |

</details>

---

### Context: `NukeQuestFinalBossModifications`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`self_damage`](./Abilities_and_Spells.md#context-self_damage) | Block | {'type': '`Block`', 'df': 'Recoil or self-inflicted damage/effects applied to the caster. | 2 |
| [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance) | Block | {'type': '`Block`', 'df': ' | 1 |
| [`splash_damage`](./Abilities_and_Spells.md#context-splash_damage) | Block | {'type': '`Block`', 'df': 'Secondary Area of Effect blast parameters. | 1 |

</details>

---

### Context: `OverHealToStatuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomStatUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomStatUp' effect/state."} | 1 |
| `TakeExtraTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'TakeExtraTurn' effect/state."} | 1 |
| `stack_scale` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `QuakeAreaChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability of triggering the quake.'} | 2 |
| `radius` | Number | {'type': '`Number`', 'df': 'The tile radius of the quake.'} | 2 |

</details>

---

### Context: `RandomDistanceDisplace`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `min_dist` | Number | {'type': '`Number`', 'df': 'The minimum tile distance they will be moved.'} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `RandomKnockback`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number | {'type': '`Number`', 'df': 'Maximum knockback distance.'} | 2 |
| `min` | Number | {'type': '`Number`', 'df': 'Minimum knockback distance.'} | 2 |

</details>

---

### Context: `ScatterCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#context-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stackable` | Boolean | {'type': '`Boolean`', 'df': 'If true, multiple instances of this trigger can stack.'} | 2 |
| [`stacks`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': 'Number of stacks or intensity to apply.'} | 2 |

</details>

---

### Context: `SmartMetronome`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |
| `upgraded` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `TakeBonusTurnWithAIControl`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | {'type': '`Boolean`', 'df': 'If true, allows the AI to cast spells during this bonus turn.'} | 2 |

</details>

---

### Context: `TeamCastAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The underlying logic ability executed by the team.'} | 2 |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum | {'type': '`Enum/String`', 'df': 'Requires participants to share this tag.'} | 2 |
| `same_orientation` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `XIsSpellStormRampAndReset`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reset_percent` | Number | {'type': '`Number`', 'df': 'The percentage of stacks to keep after resetting.'} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `XIsTargetHealth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`BonusDamage`](./Math_Equations.md) | Equation | {'type': '`String`', 'df': "Applies or references the 'BonusDamage' effect/state."} | 2 |

</details>

---

### Context: `empty_self_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | {'type': '`Block`', 'df': 'Non-damaging status applications and logic triggers executed on impact. | 2 |

</details>

---

### Context: `AlphaStatusOnTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DoubleCastSpellThisTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'DoubleCastSpellThisTurn' effect/state."} | 1 |

</details>

---

### Context: `ApplyPassivesToSpawnerWhileAlive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#context-additional_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'HideEquipment' effect/state."} | 1 |

</details>

---

### Context: `ApplyStatusesNextTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | {'type': '`Number`', 'df': "Applies or references the 'Quivered' effect/state."} | 1 |

</details>

---

### Context: `ApplyToOthersWithSharedTagAndFaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Marked` | Number | {'type': '`Number`', 'df': "Applies or references the 'Marked' effect/state."} | 1 |

</details>

---

### Context: `ApplyToRandomClosestAlly`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | Number | {'type': '`Number`', 'df': "Applies or references the 'ForceMoveTowards' effect/state."} | 1 |

</details>

---

### Context: `Conditional_ActiveWeather_Any`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#context-destroyequipmentandattachparasite) | Block | {'type': '`Block`', 'df': 'Removes an equipped item and replaces it with a parasite from a specified pool. | 1 |
| [`weather`](./Arrays.md#array-weather) | Array | {'type': '`Array`', 'df': 'An array of weather states to check against.'} | 1 |

</details>

---

### Context: `Conditional_Backstab`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BonusCritChance` | Number | {'type': '`Number`', 'df': "Applies or references the 'BonusCritChance' effect/state."} | 1 |
| `Fear` | Number | {'type': '`Number`', 'df': "Applies or references the 'Fear' effect/state."} | 1 |

</details>

---

### Context: `Conditional_CanBeHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | {'type': '`Block`', 'df': 'Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `Conditional_DebuffRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#context-destroyequipmentandattachparasite) | Block | {'type': '`Block`', 'df': 'Removes an equipped item and replaces it with a parasite from a specified pool. | 1 |
| `odds` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0) of applying the debuff.'} | 1 |

</details>

---

### Context: `Conditional_FinishedSpawning`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Imprison`](./Enums.md#enum-imprison) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'Imprison' effect/state."} | 1 |

</details>

---

### Context: `Conditional_HasCleansableDebuffs`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GenericBuff` | Number | {'type': '`Number`', 'df': "Applies or references the 'GenericBuff' effect/state."} | 1 |
| `PartialCleanse` | Number | {'type': '`Number`', 'df': "Applies or references the 'PartialCleanse' effect/state."} | 1 |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | {'type': '`Block`', 'df': 'Selects and applies a random status effect from the provided nested block. | 1 |

</details>

---

### Context: `Conditional_IsTrample`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SetKnockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'SetKnockback' effect/state."} | 1 |

</details>

---

### Context: `Conditional_LivingPlayerCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`Consumed`](./Abilities_and_Spells.md#context-consumed) | Block | {'type': '`Block`', 'df': 'State block triggered when this object or entity is eaten/consumed by another character. | 1 |
| [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#context-temppassivewhilehasstatus) | Block | {'type': '`Block`', 'df': "Grants nested passives only while the character possesses the specified status. | 1 |

</details>

---

### Context: `Conditional_NotBig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DisplaceTowardsSource` | Number | {'type': '`Number`', 'df': "Applies or references the 'DisplaceTowardsSource' effect/state."} | 1 |

</details>

---

### Context: `Conditional_RandomChance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ApplyPassives`](./Abilities_and_Spells.md#context-applypassives) | Block | {'type': '`Block`', 'df': "Grants the nested passive abilities dynamically. | 1 |
| `odds` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |

</details>

---

### Context: `Conditional_SourceAbilityHasTag`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`ScatterCoins`](./Abilities_and_Spells.md#context-scattercoins) | Block | {'type': '`Block`', 'df': 'Throws coins out into the level randomly. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'Specific entity tag required.'} | 1 |

</details>

---

### Context: `Conditional_SourceHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bruise' effect/state."} | 1 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 1 |

</details>

---

### Context: `DelayCastAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to cast later.'} | 1 |
| `lingering` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `relative` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `DelayedWindCone`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| `distance` | Number | {'type': '`Number`', 'df': 'Distance or area of effect in tiles.'} | 1 |

</details>

---

### Context: `DybbukPossessed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`punch_self_ability`](./Enums.md#enum-punch_self_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `ForceImmediateMoveAndAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_InForm`](./Abilities_and_Spells.md#context-conditional_inform)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ability to execute after moving.'} | 1 |
| `even_if_cant_reach` | Boolean | {'type': '`Boolean`', 'df': 'If true, executes the attack even if the move fails to reach the target.'} | 1 |

</details>

---

### Context: `IncAuxCounterCycle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `change` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `max` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `Madness`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |
| `tickdown_this_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `MergeDamageInstance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `can_instapop` | Boolean | {'type': '`Boolean`', 'df': 'If false, prevents the damage from instantly popping the target.'} | 1 |
| `force_no_hit_animation` | Boolean | {'type': '`Boolean`', 'df': 'If true, suppresses the flinch/hit animation.'} | 1 |

</details>

---

### Context: `NextBasicAttackCritsThisTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | {'type': '`Boolean`', 'df': 'If true, ensures the attack cannot be dodged.'} | 1 |
| `piercing` | Boolean | {'type': '`Boolean`', 'df': 'If true, the attack ignores armor.'} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `NextBattleStatusStacks`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | Number | {'type': '`Number`', 'df': "Applies or references the 'MadnessChanceOnTurnBegin' effect/state."} | 1 |
| `fights` | Number | {'type': '`Number`', 'df': 'The number of encounters this buff/debuff persists for.'} | 1 |

</details>

---

### Context: `PassiveWhileNotTakingTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Abilities_and_Spells.md#context-addstatustobasicattack) | Block | {'type': '`Block`', 'df': "Injects a status effect payload that applies whenever the character performs a basic attack. | 1 |

</details>

---

### Context: `PoolMetronome`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | {'type': '`Array`', 'df': 'An array of ability IDs to randomly choose from.'} | 1 |

</details>

---

### Context: `PopAndSpawn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': 'The entity ID to spawn in place.'} | 2 |
| `clone_items` | Boolean | {'type': '`Boolean`', 'df': 'If true, transfers inventory to the new entity.'} | 1 |
| `clone_referenced_catdata` | Boolean | {'type': '`Boolean`', 'df': 'If true, copies the genetic data of the popped cat.'} | 1 |
| `no_splatter` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `RemoveStatusStacks`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks to remove.'} | 1 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The specific status effect ID to remove.'} | 1 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | {'type': '`Block`', 'df': 'Non-damaging status applications and logic triggers executed on impact. | 1 |

</details>

---

### Context: `ScrambleLastUsedSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `permanent` | Boolean | {'type': '`Boolean`', 'df': 'If true, the scramble persists for the rest of the run.'} | 1 |

</details>

---

### Context: `SetAnimationAlts`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dead`](./Enums.md#enum-dead) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`dying`](./Enums.md#enum-dying) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `ShowFakeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |
| [`style`](./Arrays.md#array-style) | Array | {'type': '`Array`', 'df': 'The visual font style for the text (e.g., [crit]).'} | 1 |

</details>

---

### Context: `SpreadDisease`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of transmitting.'} | 1 |
| [`disease`](./Enums.md#enum-disease) | Enum | {'type': '`Enum/String`', 'df': 'The specific status effect ID representing the disease.'} | 1 |

</details>

---

### Context: `StatusGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DamageOrHealConditionally` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageOrHealConditionally' effect/state."} | 1 |
| `Freeze` | Number | {'type': '`Number`', 'df': "Applies or references the 'Freeze' effect/state."} | 1 |

</details>

---

### Context: `StatusKillers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | {'type': '`Number`', 'df': "Applies or references the 'Confusion' effect/state."} | 1 |

</details>

---

### Context: `SwapWeapon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | {'type': '`Array`', 'df': 'An array of weapon item IDs to draw from.'} | 1 |

</details>

---

### Context: `TransformEquipment`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | {'type': '`Enum/String`', 'df': 'The original item ID.'} | 1 |
| [`to`](./Enums.md#enum-to) | Enum | {'type': '`Enum/String`', 'df': 'The new item ID.'} | 1 |

</details>

---

### Context: `TransformWeapon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | {'type': '`Enum/String`', 'df': 'The original weapon ID.'} | 1 |
| [`to`](./Enums.md#enum-to) | Enum | {'type': '`Enum/String`', 'df': 'The transformed weapon ID.'} | 1 |

</details>

---

### Context: `UseAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger.'} | 1 |
| `respect_prime` | Boolean | {'type': '`Boolean`', 'df': "If true, respects the ability's prime/cooldown state."} | 1 |

</details>

---

### Context: `UseMoveAbilityWithAI`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'ID of the ability to trigger or reference.'} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': 'The AI positioning logic profile to use.'} | 1 |

</details>

---

### Context: `VisualCountDownThenApplyStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ForceUseAbility' effect/state."} | 1 |

</details>

---

### Context: `WaggleClone`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cWaggle` | Flag |  | 1 |
| `cWaggle2x2` | Flag |  | 1 |
| `cWaggle3x3` | Flag |  | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `bonk_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | {'type': '`Block`', 'df': 'Non-damaging status applications and logic triggers executed on impact. | 1 |

</details>

---

### Context: `damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'Classification/category type.'} | 1 |

</details>

---

### Context: `damage_threshold_altanimations`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `heaviestMelee` | Number | {'type': '`Number`', 'df': 'Animation trigger for massive damage.'} | 1 |
| `heavyMelee` | Number | {'type': '`Number`', 'df': 'Animation trigger if damage exceeds this threshold.'} | 1 |

</details>

---

