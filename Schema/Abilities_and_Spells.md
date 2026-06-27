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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 2731 ||
| [`graphics`](#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 2609 ||
| [`meta`](#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 2372 ||
| [`damage_instance`](#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 2344 ||
| [`template`](./Enums.md#enum-template) | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 2174 ||
| [`target`](#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1861 ||
| [`cost`](#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1851 ||
| [`variant_of`](./Enums.md#enum-variant_of) | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. | 1195 ||
| [`class`](./Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 600 ||
| [`tags`](./Arrays.md#array-tags) | Array / Enum | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 241 ||
| [`self_damage`](#object-self_damage) | Boolean / Integer / Object | Defines damage or effects applied to the caster when using the ability. | 218 ||
| [`spawn`](#object-spawn) | Object | Defines what object or unit is spawned when the ability is used. | 192 ||
| [`bonus_passives`](#object-bonus_passives) | Object | Grants temporary passive abilities to the caster for the duration of the ability. | 136 ||
| [`temporary_effects`](#object-temporary_effects) | Object | Applies temporary status effects on the caster upon using the ability. | 88 ||
| [`effects`](#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 60 ||
| [`sounds`](#object-sounds) | Object | Defines sound effects played at various points of the ability (e.g., ontrigger, oncastpoint). | 39 ||
| [`splash_damage`](#object-splash_damage) | Object | Defines additional damage or effects applied to nearby targets around the primary target. | 34 ||
| [`ai_ability`](./Enums.md#enum-ai_ability) | Enum | Specifies the ability to use as the AI's behavior for this ability. | 29 ||
| [`keyword_tooltips`](#object-keyword_tooltips) | Object | Associates keyword tooltips with the ability, often used for status effects. | 28 ||
| [`chain_ability`](./Enums.md#enum-chain_ability) | Enum | Specifies the ability to chain into after this ability is used. | 15 ||
| [`sub_ability`](./Enums.md#enum-sub_ability) | Enum | Specifies a sub-ability that is part of this ability, often used for multi-part abilities. | 8 ||
| [`chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum | Specifies which chapter or scenario this ability is available in. | 3 ||
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | Enum | Specifies the layer on which the ability's effect operates (e.g., characters, tiles, gas). | 3 ||
| [`cloned_ability`](./Enums.md#enum-cloned_ability) | Enum | Specifies an ability that is cloned from another. | 2 ||
| [`empty_self_damage`](#object-empty_self_damage) | Object | Defines self-damage or effects when the ability is used with no target (empty). | 2 ||
| [`bonk_damage`](#object-bonk_damage) | Object | Defines damage and effects applied when a dash or move hits a wall or obstacle. | 1 ||
| [`damage`](#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1557 ||
| [`particle`](./Enums.md#enum-particle) | Enum | Specifies the particle effect displayed. | 486 ||
| [`projectile`](./Enums.md#enum-projectile) | Enum | Specifies the projectile spawned for the ability. | 227 ||
| `lob` | Boolean | If true, the projectile follows a lobbed trajectory. | 130 ||
| `delay` | Number | The delay in seconds before the ability's effect triggers. | 93 ||
| `dont_visualize_ai` | Boolean | If true, the AI's visualization of this ability is suppressed. | 86 ||
| `dont_orient` | Boolean | If true, the caster does not rotate to face the target. | 83 ||
| [`dash_animation`](./Enums.md#enum-dash_animation) | Enum | Specifies the animation played during the dash movement. | 65 ||
| [`dash_start_animation`](./Enums.md#enum-dash_start_animation) | Enum | Specifies the animation played at the start of the dash. | 63 ||
| [`speed`](./Enums.md) | Array / Number | The speed of the projectile or move, can be a value or a range. | 61 | [1.0] |
| [`affected_particle`](./Enums.md#enum-affected_particle) | Enum | Specifies the particle effect on affected targets. | 51 ||
| [`dash_attack_animation`](./Enums.md#enum-dash_attack_animation) | Enum | Specifies the animation played at the end of the dash when attacking. | 45 ||
| `lob_height` | Integer | Controls the height of the lobbed projectile trajectory. | 45 ||
| [`animation_in`](./Enums.md#enum-animation_in) | Enum | Specifies the animation played when entering the target tile (e.g., teleport in). | 43 ||
| [`animation_out`](./Enums.md#enum-animation_out) | Enum | Specifies the animation played when leaving the origin tile. | 43 ||
| [`jump_attack_animation`](./Enums.md#enum-jump_attack_animation) | Enum | Specifies the animation played at the end of a jump attack. | 39 ||
| `use_projectile` | Boolean | If true, the ability uses a projectile. | 35 ||
| [`palette`](./Enums.md) | Integer | Specifies the color palette index for the ability's visuals. | 34 | 6 |
| [`full_jump_animation`](./Enums.md#enum-full_jump_animation) | Enum | Specifies the animation for a full jump (encompassing entire jump). | 24 ||
| `full_jump_sync_frames` | Integer | The frame count to sync the jump animation with the movement. | 24 ||
| `use_rotation` | Boolean | If false, the ability effect does not rotate with the caster. | 24 ||
| [`dash_end_animation`](./Enums.md#enum-dash_end_animation) | Enum | Specifies the animation played at the end of a dash. | 22 ||
| `full_jump_windup_frames` | Integer | The number of frames of windup before the jump. | 20 ||
| `visual_delay_but_simultaneous_damage` | Integer | The visual delay in frames for the ability while damage is applied simultaneously. | 18 ||
| [`center_particle`](./Enums.md#enum-center_particle) | Enum | Specifies the FX particle effect emitted at the center of the ability's origin tile. | 17 ||
| [`area_particle`](./Enums.md#enum-area_particle) | Enum | Specifies the FX particle effect emitted across the affected area tiles. | 16 ||
| `fall_from_sky` | Boolean | If true, the projectile or visual element originates from above the map and falls downward. | 16 ||
| [`move_start_animation`](./Enums.md#enum-move_start_animation) | Enum | Determines which character animation plays at the beginning of a movement ability. | 14 ||
| `use_placeholder` | Boolean | If true, renders the ability using a temporary placeholder animation instead of the final art. | 14 ||
| [`move_end_animation`](./Enums.md#enum-move_end_animation) | Enum | Determines which character animation plays at the end of a movement ability. | 13 ||
| `face_toss_target` | Boolean | If true, the unit rotates to face the target before performing a toss or throw. | 12 ||
| `ignore_slowtiles` | Boolean | If true, the unit's movement during this ability ignores tile-based speed penalties. | 12 ||
| [`chain_distance`](./Enums.md#enum-chain_distance) | Number | The distance between chain links, as a fraction of a tile. | 11 ||
| [`chain_movieclip`](./Enums.md#enum-chain_movieclip) | Enum | Specifies the visual MovieClip asset used for the chain's links. | 11 ||
| `darken_screen` | Boolean | If true, darkens the entire screen during the ability's execution. | 11 ||
| [`beam_cap`](./Enums.md#enum-beam_cap) | Enum | Specifies the MovieClip used for the visual cap (end) of a beam effect. | 10 ||
| [`beam_clip`](./Enums.md#enum-beam_clip) | Enum | Specifies the MovieClip used for the main body of a beam effect. | 10 ||
| `bounce_on_hit` | Boolean | If true, the projectile bounces off the first target it hits instead of being destroyed. | 10 ||
| `darken_screen_exclude_characters_on_tile` | Boolean | If true, characters standing on a tile are not darkened when the screen darkens. | 10 ||
| [`end`](./Enums.md#enum-end) | Enum | Defines the final animation state or offset vector for a particle's lifespan. | 10 ||
| [`jump_start_animation`](./Enums.md#enum-jump_start_animation) | Enum | Determines which character animation plays at the start of a jump ability. | 10 ||
| [`loop`](./Enums.md#enum-loop) | Enum | Specifies the character animation that plays repeatedly during an ability's execution. | 10 ||
| [`prime_animation`](./Enums.md#enum-prime_animation) | Enum | Specifies the character animation that plays during the ability's priming or charge phase. | 10 ||
| [`start`](./Enums.md#enum-start) | Enum | Specifies the initial animation state played at the beginning of an ability. | 10 ||
| `max_tiles_single_loop` | Integer | The maximum number of tiles the unit can traverse during a single animation loop. | 9 ||
| `sync_speed` | Integer | The movement speed (in frames per tile) used to synchronize the animation with traversal. | 9 ||
| [`random_delay`](./Arrays.md#array-random_delay) | Array | A random range [min, max] in frames added to delay the start of an FX or animation. | 9 ||
| `fx_is_placeholder_animation` | Boolean | If true, marks the associated FX animation as a temporary placeholder. | 8 ||
| `aoe_spell_on_land` | Boolean | If true, triggers an area-of-effect spell upon the unit landing after a jump or movement. | 7 ||
| `fx_random_flip` | Boolean | If true, the FX graphic randomly flips horizontally at spawn time. | 7 ||
| [`land_animation`](./Enums.md#enum-land_animation) | Enum | Specifies the character animation that plays when the unit lands after a jump. | 7 ||
| [`miss_particle`](./Enums.md#enum-miss_particle) | Enum | Specifies the FX particle effect emitted when the ability misses its target. | 7 ||
| `use_super_armor` | Boolean | If true, the unit cannot be interrupted or knocked back during this ability. | 7 ||
| [`air_animation`](./Enums.md#enum-air_animation) | Enum | Specifies the character animation that plays while the unit is airborne during a jump. | 6 ||
| [`custom_priming_animation`](./Enums.md#enum-custom_priming_animation) | Enum | Specifies a custom idle animation for the unit while it is priming an ability. | 6 ||
| `darken_screen_exclude_self` | Boolean | If true, the casting unit is not darkened when the screen darkens. | 6 ||
| `darken_screen_start_early` | Boolean | If true, the screen darkening effect begins before the main ability animation. | 6 ||
| [`fall_randomize_timing`](./Enums.md#enum-fall_randomize_timing) | Number | The maximum random fraction of the fall duration added to stagger when objects fall from the sky. | 6 ||
| `min_throw_height` | Number | The minimum height (in tiles) the projectile reaches during an arc or toss. | 6 ||
| `single_projectile` | Boolean | If true, only a single projectile is spawned instead of a volley or spread. | 6 ||
| [`miss_random_delay`](./Arrays.md#array-miss_random_delay) | Array | A random range [min, max] in frames added to delay the miss particle effect. | 6 ||
| [`detatched_animation`](./Enums.md#enum-detatched_animation) | Enum | Specifies a visual MovieClip that plays independently from the unit's main body. | 5 ||
| `detatched_animation_reach` | Integer | The tile range at which the detached animation is displayed. | 5 ||
| [`empty_animation`](./Enums.md#enum-empty_animation) | Enum | Specifies the character animation that plays when the unit's ability has no charges remaining. | 5 ||
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 5 ||
| `fixed_jump_height` | Number | The fixed height (in tiles) the unit reaches during a jump, overriding default arc calculations. | 4 ||
| [`rocket_swirl`](#object-rocket_swirl) | Object | An object defining the spiral rotation parameters for a rocket-style projectile. | 4 ||
| `sync_frames` | Integer | The total number of animation frames used to synchronize a looping ability sequence. | 4 ||
| [`dash_decelerating_animation`](./Enums.md#enum-dash_decelerating_animation) | Enum | Specifies the character animation that plays when the unit begins slowing down during a dash. | 3 ||
| `decelerate` | Integer | The number of frames over which the unit's dash movement decelerates to a stop. | 3 ||
| `delay_from_map_edge` | Boolean | If true, the projectile's initial delay is calculated based on its distance from the map edge. | 3 ||
| `easing` | Integer | The easing function index applied to the projectile's movement or rotation for smoothing. | 3 ||
| [`fixed_jump_speed`](./Enums.md#enum-fixed_jump_speed) | Number | The fixed horizontal speed (in tiles per second) the unit moves at while jumping. | 3 ||
| [`grab_animation`](./Enums.md#enum-grab_animation) | Enum | Specifies the character animation that plays when the unit grabs a target for a throw or carry. | 3 ||
| [`lob_yoff`](./Enums.md#enum-lob_yoff) | Number | The vertical offset applied to the lob arc of a projectile or thrown object. | 3 ||
| `lock_orientation_during_dash` | Boolean | If true, the unit's facing direction is locked for the duration of the dash animation. | 3 ||
| `use_projectile_spawn_offset` | Boolean | If true, the projectile spawns at the offset defined by the ability's spawn offset rather than the unit's origin. | 3 ||
| `use_rotation_once` | Boolean | If true, the rotation is applied only once at the start of the animation rather than continuously. | 3 ||
| `always_play_animations` | Boolean | If true, the animation plays even when the game is paused or the unit is off-screen. | 2 ||
| `detatched_animation_cutoff` | Boolean | If true, the animation is cut off when the detachment state ends. | 2 ||
| `do_damage_immediately` | Boolean | If true, damage is applied at the start of the animation rather than at the impact frame. | 2 ||
| `jump_height_multiplier` | Number | A multiplier for the jump height during the ability's movement. | 2 ||
| [`mask_center`](./Enums.md#enum-mask_center) | Enum | Specifies the mask center point used for area-of-effect targeting. | 2 ||
| [`mask_extent`](./Enums.md#enum-mask_extent) | Enum | Specifies the mask extent (radius or shape) for area-of-effect targeting. | 2 ||
| `max_throw_height` | Number | The maximum height of the arc when throwing an object. | 2 ||
| [`particle_mat`](./Enums.md#enum-particle_mat) | Enum | Determines the material shader used for particles during the ability. | 2 ||
| [`preturn_animation`](./Enums.md#enum-preturn_animation) | Enum | Specifies the animation played when the unit is selected to act. | 2 ||
| [`primed_alt_animation`](./Strings.md#string-primed_alt_animation) | String | The name of the animation to play when the ability is primed (ready to fire). | 2 ||
| [`pseudoprojectile`](./Enums.md#enum-pseudoprojectile) | Enum | Specifies a visual effect that simulates a projectile without actually firing one. | 2 ||
| `reverse_orientation` | Boolean | If true, the unit faces the opposite direction during the animation. | 2 ||
| `self_damage_mid_port` | Boolean | If true, the unit takes damage during the middle of a teleport effect. | 2 ||
| `throw_speed` | Integer | The speed multiplier for thrown objects. | 2 ||
| `use_hit_alts` | Boolean | If true, the ability uses alternative hit animations based on hit type. | 2 ||
| [`affected_animation`](./Enums.md#enum-affected_animation) | Enum | Specifies the animation played on the target unit when it is affected by the ability. | 1 ||
| [`ally_animation`](./Enums.md#enum-ally_animation) | Enum | Specifies the animation played on an ally when targeted by a beneficial ability. | 1 ||
| [`animate_name`](./Enums.md#enum-animate_name) | Boolean / Enum | If true, the ability name is animated; if set to an enum, it specifies a specific animation type like 'pointout'. | 1 ||
| `apex_distance` | Number | The distance from the start point to the apex of a jump or lob arc. | 1 ||
| [`apex_time`](./Enums.md#enum-apex_time) | Number | The time (in seconds) to reach the apex of a jump or lob arc. | 1 ||
| `bypass_combatspeed` | Boolean | If true, the ability animation ignores the combat speed setting. | 1 ||
| [`damage_threshold_altanimations`](#object-damage_threshold_altanimations) | Object | A mapping of damage threshold values to alternate animation names, triggering different animations based on damage dealt. | 1 ||
| [`dash_bonk_animation`](./Enums.md#enum-dash_bonk_animation) | Enum | Specifies the animation played when the unit collides with an obstacle during a dash. | 1 ||
| `delay_from_map_center` | Boolean | If true, the animation delay is calculated based on distance from the center of the map. | 1 ||
| `delay_from_reverse_map_edge` | Boolean | If true, the animation delay is calculated based on distance from the opposite edge of the map. | 1 ||
| `do_animation_offscreen` | Boolean | If true, the animation plays even if the unit is off-screen. | 1 ||
| `do_not_clear_placeholder` | Boolean | If true, the placeholder object (e.g., a held item) is not cleared after the ability resolves. | 1 ||
| `face_targets` | Boolean | If true, the unit rotates to face its target during the animation. | 1 ||
| `first_castpoint_is_self_damage_only` | Boolean | If true, the first cast point of a multi-hit ability only applies self-damage. | 1 ||
| [`hang_time`](./Enums.md#enum-hang_time) | Number | The duration of the hang time at the apex of a jump or lob arc. | 1 ||
| `jump_speed_multiplier` | Number | A multiplier for the horizontal speed during a jump. | 1 ||
| [`lob_speed`](./Enums.md#enum-lob_speed) | Number | The speed of a lobbed projectile's arc. | 1 ||
| `max_range` | Enum / Integer | The maximum range of the ability, can be a static number or an expression. | 1 ||
| `min_range` | Integer | The minimum range of the ability. | 1 ||
| `othercat_placeholder_available` | Boolean | If true, a placeholder for another cat (ally) is available for multi-cat abilities. | 1 ||
| [`precast_delay`](./Enums.md#enum-precast_delay) | Number | A delay (in seconds) before the casting animation begins. | 1 ||
| `uncatchable` | Boolean | If true, the projectile or effect cannot be caught or intercepted. | 1 ||
| `use_directional_animations` | Boolean | If true, the ability uses directional animations based on the unit's facing or movement direction. | 1 ||
| `use_origin_offsets` | Boolean | If true, the animation uses offset values relative to the unit's origin point. | 1 ||
| [`spawn_offset`](./Arrays.md#array-spawn_offset) | Array | A 3D vector offset [x, y, z] for where the spawn effect appears relative to the unit. | 1 ||

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
| [`desc`](./Enums.md) | Enum | Specifies the localized description string for the item or ability. | 1641 | ABILITY_FORMOFTHEWOLF2_DESC |
| [`name`](./Enums.md) | Enum | Specifies the localized name string for the entity, item, or ability. | 1611 | ABILITY_HAILOFNAILS_NAME |
| [`class`](./Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 876 ||
| [`type_icon`](./Strings.md#string-type_icon) | Enum | Determines the icon type (e.g., 'defense', 'heal', 'ranged') displayed on the ability or item. | 283 ||
| `animate_name` | Boolean / Enum | If true, the ability name is animated; if set to an enum, it specifies a specific animation type like 'pointout'. | 177 ||
| [`icon_shell_frame`](./Strings.md#string-icon_shell_frame) | Variable | Specifies the shell frame type (e.g., 'attack', 'damage') for the ability's icon border. | 28 ||
| [`is_move`](./Enums.md#enum-is_move) | Variable | If set to true or 'auto', marks the ability as a movement action. | 20 ||
| [`ability_icon`](./Enums.md#enum-ability_icon) | Enum | Specifies the specific icon graphic for the ability. | 14 ||
| [`tooltip_values`](./Arrays.md#array-tooltip_values) | Array | An array of equation strings used to dynamically generate numeric display values in the ability's tooltip, such as damage or healing ranges. | 9 ||
| [`icon_damage_display`](./Strings.md#string-icon_damage_display) | String | Specifies the static text or range shown on the ability icon to represent its damage output (e.g., "1-5" or "?"). | 8 ||
| [`icon_damage_display_eq`](./Math_Equations.md) | Equation | An equation string that dynamically calculates the numeric value displayed on the ability icon for damage or healing. | 7 ||
| `is_basic_attack` | Boolean | If true, this ability is treated as a basic attack, typically used for default melee or ranged strikes without special properties. | 6 ||
| `is_weapon` | Boolean | If true, this ability is classified as a weapon, allowing it to benefit from weapon-specific modifiers and UI grouping. | 4 ||
| [`icon_damage_type`](./Enums.md#enum-icon_damage_type) | Enum | Determines which damage type icon (magic or physical) is displayed on the ability icon. | 3 ||
| `is_trinket` | Boolean | If true, this ability is classified as a trinket, typically a one-use or passive item effect with its own UI category. | 3 ||
| `dont_visualize_ai` | Boolean | If true, the AI's visualization of this ability is suppressed. | 2 ||
| [`icon_damage_display_suffix`](./Strings.md#string-icon_damage_display_suffix) | String | A string appended to the damage display on the ability icon, such as "x10" to indicate multiplier attacks. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||

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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 2344 ||
| [`effects`](#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 1787 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1554 ||
| [`damage`](#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 1447 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 359 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 352 ||
| [`knockback`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 254 ||
| `ai_base_score` | Integer | The base priority score the AI assigns to using this damage instance, with higher values indicating greater preference. | 222 ||
| `heal` | `Number` | An equation string that determines the amount of health restored by this damage instance. | 122 ||
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target regardless of accuracy or evasion. | 110 ||
| `incidentally_collects_pickups` | `Boolean` | If true, the damage instance collects nearby pickups (e.g., coins, items) as part of its effect. | 103 ||
| [`custom_additional_ai_weight`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | A string identifier for a custom AI weighting condition that modifies the AI's scoring for this damage instance. | 82 ||
| `piercing` | `Boolean` | If true, the damage instance ignores armor or damage reduction effects on the target. | 52 ||
| `makes_contact` | `Boolean` | If true, the damage instance is considered a contact hit, triggering contact-based passives on both the attacker and target. | 40 ||
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Specifies the layer on which the ability's effect operates (e.g., characters, tiles, gas). | 26 ||
| [`blocked_damage`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | An equation string that calculates the amount of damage that can be blocked or reduced by the target's defenses. | 24 ||
| [`raw_damage`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | An equation string that calculates the base damage before any modifiers or bonuses are applied. | 22 ||
| `crit_chance` | `Number` | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 16 ||
| `override_trample_damage` | `Boolean` | If true, this damage instance replaces any default trample damage when the unit passes through an occupied tile. | 15 ||
| `contact_requires_adjacency` | Boolean | If false, contact effects are not restricted to adjacent tiles, allowing contact to trigger at range. | 14 ||
| `can_revive` | `Boolean` | If true, the damage instance can revive a downed unit instead of dealing damage. | 8 ||
| `show_damage_on_0` | `Boolean` | If true, the damage number is still displayed even when the resulting damage is zero. | 6 ||
| `force_play_hit_animation` | `Boolean` | If true, the hit animation is forced to play regardless of other conditions (e.g., miss or block). | 5 ||
| `blocked_multiplier` | `Number` | A multiplier applied to blocked damage, increasing the effectiveness of the defensive reduction. | 4 ||
| [`accuracy`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | A decimal value (e.g., .5) representing the base hit chance of the damage instance, where 1.0 is guaranteed. | 3 ||
| `can_collect_pickups` | `Boolean` | If true, the damage instance can collect pickups from the target's tile as part of its effect. | 3 ||
| `can_instapop` | `Boolean` | If false, the ability cannot instantly kill or remove the target, often used for non-lethal effects. | 2 ||
| `disallow_modifications` | `Boolean` | If true, the damage instance cannot be modified by external effects (e.g., passives, statuses). | 2 ||
| `force_no_contact` | `Boolean` | If true, the damage instance does not trigger contact-based passives even if it would normally be a contact hit. | 2 ||
| `non_lethal` | `Boolean` | If true, the damage instance cannot reduce a unit below 1 HP, preventing kills. | 2 ||
| [`raw_heal`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | An equation string that calculates the base healing amount before any modifiers are applied. | 2 ||
| `two_way_contact` | `Boolean` | If true, contact effects apply to both the attacker and the target when the damage instance hits. | 2 ||
| `damage_shield_only` | `Boolean` | If true, the damage instance only affects damage shields (e.g., barrier effects) and not health directly. | 1 ||
| [`faction`](./Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 1 ||
| [`final_hit_bonus_damage`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | An equation string that adds bonus damage to the final hit of a multi-hit damage instance. | 1 ||
| `force_adjacent_and_diagonal_contact` | `Boolean` | If true, contact effects are forced for both adjacent and diagonal tiles even if not normally triggered. | 1 ||
| `force_no_knockback` | `Boolean` | If true, the damage instance applies no knockback regardless of any knockback values set. | 1 ||
| `hint_dont_lowgravboost` | `Boolean` | If true, the damage instance does not receive a damage boost from low gravity tiles. | 1 ||
| [`hit_animation_alt`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Specifies an alternative hit animation name (e.g., "catch") to play instead of the default on successful hit. | 1 ||
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | 2 |
| [`ranged`](./Enums.md) | Boolean | If true, the damage instance is considered a ranged attack, interacting with ranged-specific modifiers and passives. | 1 | true |

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
| `max_range` | Enum / Integer | The maximum range of the ability, can be a static number or an expression. | 1088 ||
| `max_aoe` | Enum / Integer | An equation or integer defining the maximum radius or number of tiles for the area of effect target selection. | 792 ||
| `min_range` | Integer | The minimum range of the ability. | 583 ||
| [`target_mode`](./Enums.md#enum-target_mode) | Enum | Determines how the targeting input is handled (e.g., direction8, tile, random_direction) for selecting a target location. | 503 ||
| [`restrictions`](./Arrays.md#array-restrictions) | Array / Enum | An array of constraint tags (e.g., [aoe_must_exist must_have_enemy]) that filter valid targets for the ability. | 462 ||
| [`aoe_mode`](./Enums.md#enum-aoe_mode) | Enum | Specifies the shape or pattern of the area of effect (e.g., standard, cross, circle) for targeting multiple tiles. | 429 ||
| [`knockback_mode`](./Enums.md#enum-knockback_mode) | Enum / Integer | Determines the directional behavior of knockback (e.g., pull_to_character_plus1, zero, character_to_tile). | 264 ||
| [`min_aoe`](./Enums.md#enum-min_aoe) | Variable | An equation or integer defining the minimum radius or number of tiles for the area of effect target selection. | 253 ||
| `aoe_excludes_self` | Boolean | If true, the casting unit is excluded from being a target of its own area of effect. | 241 ||
| [`aoe_restrictions`](./Arrays.md#array-aoe_restrictions) | Array / Enum | Specifies the list of restrictions for area-of-effect targets, such as allies only, enemies only, or requiring line of sight. | 197 ||
| `aoe_considers_character_size` | Boolean | If true, the area of effect accounts for the size of characters when determining which tiles are affected. | 170 ||
| [`range_mode`](./Enums.md#enum-range_mode) | Enum | Determines the shape or logic used to calculate ability range, such as standard, ground_move, cross, custom, or special_tagged_tiles. | 114 ||
| [`X_is`](./Enums.md#enum-x_is) | Enum | Defines what the ability's variable 'X' represents, such as custom, storm_count, random_0_to_N, alpha_exists, or current_shield. | 86 ||
| [`custom_aoe`](./Arrays.md#array-custom_aoe) | Array | A list of tile offsets relative to the target that defines the shape of a custom area of effect. | 83 ||
| `multihit` | Enum / Integer | The number of times the ability hits each target, or an expression involving X. | 62 ||
| `max_targets` | Integer / String | The maximum number of targets the ability can affect. | 56 ||
| `range_excludes_blocking` | Boolean | If true, the range calculation ignores obstacles that block line of sight. | 53 ||
| `prioritize_dont_change_direction` | Variable | If true, the unit's facing direction is not changed when selecting a target. | 52 ||
| [`target_requires_tag`](./Enums.md#enum-target_requires_tag) | Enum | Restricts targeting to characters that possess a specific tag. | 40 ||
| [`aoe_symmetry`](./Enums.md#enum-aoe_symmetry) | Enum | Determines the symmetry applied to the custom area of effect shape, such as four_way, eight_way, or none. | 28 ||
| `prioritize_face_camera` | Variable | If set, the unit's sprite faces the camera during targeting. | 26 ||
| `straight_shot` | Boolean | If true, the ability fires in a straight line, hitting all units in its path. | 24 ||
| `can_multihit` | Boolean | If true, the ability can hit the same target multiple times per cast. | 17 ||
| `allow_any_orientation` | Boolean | If true, the ability can be used in any facing direction, not just cardinal. | 16 ||
| `range_considers_character_size` | Boolean | If true, the range calculation includes the size of the character occupying the tile. | 16 ||
| `throw_consumed_character` | Boolean | If true, the consumed character is thrown as a projectile toward the target. | 15 ||
| `min_targets` | Integer | The minimum number of targets the ability must hit; if insufficient valid targets exist, the ability may fail. | 14 ||
| `aoe_leading_edge_only` | Boolean | If true, only the outermost tiles of the area of effect are considered for targeting. | 13 ||
| `allow_diagonals` | Boolean | If true, diagonal tiles are considered valid targets. | 12 ||
| `range_display_include_character_size` | Boolean | If true, the displayed range indicator accounts for the character's size. | 12 ||
| `stagger_multihit_targets` | Boolean | If true, multihit instances are distributed across different targets rather than hitting the same one repeatedly. | 12 ||
| `upgrade_straight_shot_to_piercing` | Boolean | If true, the straight shot pierces through all enemies instead of stopping at the first. | 11 ||
| `delayed_trigger` | Boolean | If true, the ability's effect is applied after a short delay rather than instantly. | 10 ||
| `consider_trample` | Boolean | If true, the ability accounts for trample mechanics when moving through enemies. | 9 ||
| `N` | Integer | A generic numeric parameter used in custom targeting logic. | 7 ||
| [`custom_range`](./Arrays.md#array-custom_range) | Array | A list of tile offsets relative to the caster that defines the shape of a custom range indicator. | 7 ||
| `always_bounce` | Boolean | If true, the projectile always bounces off the target and can hit additional targets. | 6 ||
| `multihit_max` | Integer | The maximum number of hits per cast when multihit is variable. | 6 ||
| `multihit_min` | Integer | The minimum number of hits per cast when multihit is variable. | 6 ||
| `reorient_thrown_character` | Boolean | If true, the thrown character is reoriented to face the direction it is thrown. | 6 ||
| [`toss_direction_restriction`](./Enums.md#enum-toss_direction_restriction) | Enum | Limits the direction a thrown character can be tossed to forwards or backwards. | 6 ||
| [`custom_aoe_util`](./Arrays.md#array-custom_aoe_util) | Array | An additional list of tile offsets for utility targeting within the area of effect. | 6 ||
| `aoe_hint_teamcast` | Boolean | If true, the area of effect is displayed as a team-wide ability. | 5 ||
| [`aoe_tile_requires_element`](./Enums.md#enum-aoe_tile_requires_element) | Enum | Restricts the area of effect to tiles with a specific terrain element type. | 5 ||
| `distance_sort_targets` | Variable | If set, targets are sorted by distance from the caster for hit order. | 5 ||
| `dont_orient_aoe` | Boolean | If true, the area of effect shape is not rotated to match the caster's facing. | 5 ||
| `hint_can_target_pickups` | Boolean | If true, the ability can target pickups as valid targets. | 5 ||
| `max_bounces` | Integer | The maximum number of bounces for a projectile; -1 means infinite. | 5 ||
| `splash_damage_aoe_begin` | Integer | The hit number at which splash damage area of effect begins for multihit abilities. | 5 ||
| [`aoe_chance`](./Enums.md#enum-aoe_chance) | Number / String | The probability (0 to 1) that the area of effect is applied per hit, or an expression using level. | 4 ||
| `as_the_crow_flies` | Boolean | If true, movement ignores obstacles and uses straight-line distance. | 4 ||
| `force_ai_target_as_spell` | Boolean | If true, the AI treats this ability as a spell for targeting decisions. | 4 ||
| `range_display_include_aoe` | Boolean | If true, the range display also shows the area of effect. | 4 ||
| `shotgun_mode` | Boolean | If true, the ability fires multiple projectiles in a spread pattern. | 4 ||
| `shuffle_tile_order` | Boolean | If true, the order in which tiles are hit is randomized. | 4 ||
| `upgrade_straight_shot_to_boomerang` | Boolean | If true, the straight shot becomes a boomerang that returns to the caster. | 4 ||
| [`mouse_offset`](./Arrays.md#array-mouse_offset) | Array | A 2D offset [x, y] applied to the mouse cursor position for targeting. | 4 ||
| `dont_orient` | Boolean | If true, the caster does not rotate to face the target. | 3 ||
| `low_health_character_threshold` | Variable | The health threshold below which a character is considered low health for targeting. | 3 ||
| `randomize_target_within_range` | Integer | The number of times to randomize the target's position within the ability's range. | 3 ||
| [`special_tile_tag`](./Enums.md#enum-special_tile_tag) | Enum | Specifies a special tile tag that the ability can target. | 3 ||
| `track_target` | Boolean | If true, the ability will track the target's movement. | 3 ||
| `corpse_priority` | Integer | The priority value for targeting corpses. | 2 ||
| `hint_can_target_empty` | Boolean | If true, the ability can target empty tiles. | 2 ||
| `low_gravity_boostable` | Boolean | If true, the ability is affected by low gravity boosts. | 2 ||
| `prioritize_change_direction` | Boolean | If true, the ability prioritizes changing the caster's direction to face the target. | 2 ||
| [`range_bonuses`](./Enums.md#enum-range_bonuses) | Enum | Specifies the range bonus modifier to apply. | 2 ||
| `range_display_include_direction` | Boolean | If true, the range display includes direction indicators. | 2 ||
| `recalc_target_on_castpoint` | Boolean | If true, the target is recalculated at the cast point instead of at the start. | 2 ||
| `redirect_location_if_blocked` | Boolean | If true, the target location is redirected if the original is blocked. | 2 ||
| `trample_allies_too` | Boolean | If true, the ability can trample or pass through allies. | 2 ||
| [`target_requires_element`](./Arrays.md#array-target_requires_element) | Array | Specifies the list of tile elements that the target must have. | 2 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1 ||
| [`adjust_target`](./Enums.md#enum-adjust_target) | Enum | Specifies the type of target adjustment. | 1 ||
| `allow_diagonal_passthrough` | Boolean | If true, the target can be diagonal and pass through diagonally. | 1 ||
| `ally_priority` | Integer | The priority value for targeting allies. | 1 ||
| `aoe_display_exclude_restrictions` | Boolean | If true, the AoE display ignores targeting restrictions. | 1 ||
| `aoe_rotate_around_character_center` | Boolean | If true, the AoE area rotates around the character's center. | 1 ||
| `aoe_spell_on_land` | Boolean | If true, triggers an area-of-effect spell upon the unit landing after a jump or movement. | 1 ||
| `bonus_pathing_leniency` | Integer | The amount of extra pathing leniency allowed. | 1 ||
| `damage_collided_only` | Boolean | If true, damage is only applied to targets that the projectile collided with. | 1 ||
| `enemy_priority` | Integer | The priority value for targeting enemies. | 1 ||
| `force_no_contact` | `Boolean` | If true, the damage instance does not trigger contact-based passives even if it would normally be a contact hit. | 1 ||
| `hint_can_target_static` | Boolean | If true, the ability can target static objects. | 1 ||
| [`knockback_modifier`](./Enums.md#enum-knockback_modifier) | Enum | Specifies the knockback direction modifier. | 1 ||
| `lingering` | Boolean | If true, the ability effect lingers after the initial cast. | 1 ||
| `mirror_custom_aoe` | Boolean | If true, the custom AoE shape is mirrored. | 1 ||
| [`prioritize_throw_target_with_passive`](./Enums.md#enum-prioritize_throw_target_with_passive) | Enum | Specifies the passive that the target must have to be prioritized. | 1 ||
| `randomize_knockback_direction_except_for_finisher` | Boolean | If true, knockback direction is randomized except for the finisher hit. | 1 ||
| `range_excludes_self` | Boolean | If true, the ability cannot target the caster. | 1 ||
| `range_max` | Integer | The maximum range of the ability. | 1 ||
| `range_min` | Integer | The minimum range of the ability. | 1 ||
| [`range_symmetry`](./Enums.md#enum-range_symmetry) | Enum | Specifies the range symmetry type. | 1 ||
| `remain_off_map` | Boolean | If true, the target can be off the map. | 1 ||
| [`restructions`](./Enums.md#enum-restructions) | Enum | Specifies additional targeting restrictions. | 1 ||
| `reverse_target_direction` | Boolean | If true, the target's facing direction is reversed. | 1 ||
| `spin_steps` | Integer | The number of steps to spin the target. | 1 ||
| `uncounterable` | Boolean | If true, the ability cannot be countered. | 1 ||
| [`custom_aoe_mirror`](./Arrays.md#array-custom_aoe_mirror) | Array | Lists the mirror transformations for the custom AoE shape. | 1 ||
| [`custom_aoe_util_mirror`](./Arrays.md#array-custom_aoe_util_mirror) | Array | Lists the utility mirror transformations for the custom AoE shape. | 1 ||

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
| `mana` | Enum / Integer | The amount of mana required to cast, as a formula or stat. | 1605 ||
| `infcantrip` | Boolean | If true, the ability is an infinite cantrip (costs no mana and can be cast repeatedly). | 810 ||
| `cantrip` | Boolean | If true, the ability is a cantrip (costs no mana). | 560 ||
| `once_per_fight` | Variable | The number of times the ability can be used per fight, or true/false for single use. | 98 ||
| `act_points` | Integer | The number of action points required to use the ability. | 86 ||
| `move_points` | Integer | The number of move points required to use the ability. | 59 ||
| `prime` | Integer | The number of prime points required to use the ability. | 30 ||
| `allow_offmap_casts` | Boolean | If true, the ability can be cast from off-map locations. | 22 ||
| `cant_cast` | Variable | The condition or counter that prevents the ability from being cast. | 18 ||
| [`charge`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | The amount of charge required or the formula to calculate charge cost. | 18 ||
| `must_be_consuming` | Boolean | If true, the ability can only be used while the unit is consuming. | 17 ||
| `must_not_be_consuming` | Boolean | If true, the ability can only be used while the unit is not consuming. | 14 ||
| `requires_reload` | Boolean | If true, the ability must be reloaded before it can be used again. | 14 ||
| `can_cast_while_dead` | Boolean | If true, the ability can be cast while the unit is dead. | 12 ||
| [`cantrip_group`](./Enums.md#enum-cantrip_group) | Enum | Specifies the cantrip group this ability belongs to, used for grouping related cantrip abilities. | 12 ||
| `must_be_offmap` | Boolean | If true, the unit must be off the map (not on the battlefield) to use this ability. | 12 ||
| `X_cant_be_zero` | Boolean | If true, the variable X used in cost calculation cannot be zero. | 11 ||
| `disallow_cost_modification` | Boolean | If true, prevents any modifications to the cost of this ability. | 9 ||
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 8 ||
| `main_turn_only` | Boolean | If true, the ability can only be used during the unit's main turn. | 8 ||
| `requires_destructible_weapon` | Boolean | If true, the ability requires a weapon that has durability and can be destroyed. | 8 ||
| `requires_exact_character_aux` | Integer | The exact character auxiliary value required for the unit to use this ability. | 8 ||
| [`durability`](./Enums.md) | Integer | The amount of durability consumed by this ability or required for its use. | 8 | 0 |
| `must_not_be_a_summon` | Boolean | If true, the unit must not be a summon to use this ability. | 7 ||
| `start_reloaded` | Boolean | If true, the ability begins the battle already reloaded and ready to use. | 7 ||
| `must_be_first_action` | Boolean | If true, this ability must be the first action taken by the unit in its turn. | 4 ||
| `enabled_formula` | Variable | A formula using variables (e.g., X) that evaluates to a boolean indicating if the ability is enabled. | 3 ||
| `must_be_first_nonmove_action` | Boolean | If true, this ability must be the first non-move action taken by the unit in its turn. | 3 ||
| `must_have_weapon` | Boolean | If true, the unit must be wielding a weapon to use this ability. | 2 ||
| `can_be_refreshed` | Boolean | If true, the ability's charges can be refreshed by other effects. | 1 ||
| `can_pay_over_multiple_turns` | Boolean | If true, the cost of this ability can be paid over multiple turns. | 1 ||
| `can_self_refresh` | Boolean | If true, this ability can refresh its own charges. | 1 ||
| `damage_cant_be_zero` | Boolean | If true, the damage dealt by this ability cannot be zero. | 1 ||
| `initial_charge` | Integer | The starting number of charges for this ability at the beginning of battle. | 1 ||
| `manacost_cant_be_zero` | Boolean | If true, the mana cost of this ability cannot be zero. | 1 ||
| `minimum_con` | Integer | The minimum Constitution (CON) stat required to use this ability. | 1 ||
| `minimum_spd` | Integer | The minimum Speed (SPD) stat required to use this ability. | 1 ||
| `require_default_size` | Boolean | If true, the unit must be of default size to use this ability. | 1 ||
| `requires_attack_damage_threshold` | Integer | The minimum attack damage threshold the unit must have to use this ability. | 1 ||
| `requires_consumed_trinket` | Boolean | If true, the unit must have a trinket that has been consumed to use this ability. | 1 ||
| `requires_empty_trinket` | Boolean | If true, the unit must have an empty trinket slot to use this ability. | 1 ||
| `requires_hp_threshold` | Integer | The minimum HP threshold (current HP) required to use this ability. | 1 ||
| `requires_weapon` | Boolean | If true, the unit must have a weapon equipped to use this ability. | 1 ||

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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 220 ||
| [`effects`](#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 200 ||
| [`damage`](./Abilities_and_Spells.md#object-damage) | Variable | Specifies the amount of damage dealt, can be a number or expression. | 47 ||
| `piercing` | `Boolean` | If true, the damage instance ignores armor or damage reduction effects on the target. | 12 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 11 ||
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target regardless of accuracy or evasion. | 10 ||
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 10 ||
| `heal` | `Number` | An equation string that determines the amount of health restored by this damage instance. | 6 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 4 ||
| `ai_base_score` | Integer | The base priority score the AI assigns to using this damage instance, with higher values indicating greater preference. | 2 ||
| `non_lethal` | `Boolean` | If true, the damage instance cannot reduce a unit below 1 HP, preventing kills. | 1 ||

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
| [`object`](./Enums.md) | Array / Enum | Specifies the object or unit to be spawned. | 184 | [TallSkeletonCat] |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 83 ||
| [`faction`](./Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 59 ||
| `ai_base_score` | Integer | The base priority score the AI assigns to using this damage instance, with higher values indicating greater preference. | 31 ||
| [`additional_passives`](#object-additional_passives) | Object | Additional passive abilities applied to the spawned unit. | 20 ||
| [`first_turn`](./Enums.md#enum-first_turn) | Enum | Determines when the spawned unit takes its first turn relative to the spawn event. | 17 ||
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Specifies the layer on which the ability's effect operates (e.g., characters, tiles, gas). | 14 ||
| [`catdata`](./Enums.md) | Enum | Specifies the cat data identifier for the spawned unit, linking to a character template. | 13 | fleshgolem |
| `clone_items` | Boolean | If true, the spawned unit clones the items of the original unit. | 12 ||
| `lob` | Boolean | If true, the projectile follows a lobbed trajectory. | 4 ||
| [`post_spawn_statuses`](#object-post_spawn_statuses) | Object | Status effects applied to the spawned unit immediately after it appears. | 4 ||
| [`size`](./Enums.md) | Integer | The scale factor (size multiplier) of the spawned unit. | 4 | 2 |
| `face_camera` | Boolean | If true, the spawned unit always faces the camera. | 2 ||
| `inherit_elite_buffs` | Boolean | If true, the spawned unit inherits elite buffs from the original unit. | 2 ||
| `start_dead` | Boolean | If true, the spawned unit starts the battle dead (e.g., for revival effects). | 2 ||
| [`appearance`](./Enums.md#enum-appearance) | Enum | Specifies the visual appearance or model override for the spawned unit. | 1 ||
| [`auto_cast_on_spawn`](./Enums.md#enum-auto_cast_on_spawn) | Enum | Specifies an ability to automatically cast on the spawned unit when it spawns. | 1 ||
| [`chapter`](./Enums.md#enum-chapter) | Enum | Specifies which chapter or scenario this ability is available in. | 1 ||
| [`custom_additional_ai_weight`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | A string identifier for a custom AI weighting condition that modifies the AI's scoring for this damage instance. | 1 ||
| `include_passives` | Boolean | If true, includes passives from the source unit when spawning. | 1 ||
| `redirect_location_if_blocked` | Boolean | If true, the target location is redirected if the original is blocked. | 1 ||
| [`spawnin_animation`](./Enums.md#enum-spawnin_animation) | Enum | Specifies the animation played when the unit spawns in. | 1 ||
| `trigger_battle_start` | Boolean | If true, triggers the battle start event after spawning. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 137 ||
| [`DeadAltAbility`](./Enums.md) | Enum | Specifies an alternative ability used when the unit is dead. | 12 | DonateBlood_Afterlife |
| [`AbilityEnabledOncePerFightAtHealthThreshold`](./Enums.md) | Integer | The health threshold (absolute or percentage) at which this ability becomes enabled once per fight. | 7 | 50 |
| [`XIsFreeArmorSlots`](./Enums.md) | Integer | The number of armor slots that are free (no cost) for the unit. | 7 | 1 |
| [`AbilityEnabledPercentEachTurn`](./Enums.md) | Integer | The percentage chance each turn that this ability is enabled. | 6 | 50 |
| [`FreeFirstCast`](./Enums.md) | Integer | The number of free casts of this ability per battle. | 6 | 4 |
| [`XIsLivingAlliesWithTag`](./Enums.md) | Enum | Specifies the tag that living allies must have for this passive to affect them. | 5 | hitler_clone_fetus |
| [`CatchBoomerang`](./Enums.md) | Integer | If set, allows the ability to catch a boomerang, with the integer representing the number of catches. | 4 | 1 |
| [`CopyBasicAttackEffects`](./Enums.md) | Integer | If set, the ability copies the effects from the unit's basic attack. | 4 | 1 |
| [`DownRankAIIfWeaponUsable`](./Enums.md) | Number | A multiplier that reduces the AI's priority to use this ability if the unit has a usable weapon. | 4 | .001 |
| [`AbilityEnableIfConsumedCharacterHasTag`](./Enums.md) | Enum | Specifies the tag that a consumed character must have for the ability to be enabled. | 3 | sp_pill_normal |
| [`AbilityEnabledOncePerRound`](./Enums.md) | Integer | If set, the ability can only be used once per round. | 3 | 1 |
| [`AbilityInheritsWeaponEffects`](./Enums.md) | Integer | If set, the ability inherits properties from the unit's weapon, with higher values indicating different inheritance modes. | 3 | 2 |
| [`MoonHeadFinisherEnabler`](./Enums.md) | Integer | Determines the finisher state for MoonHead abilities; negative values may disable. | 3 | 0 |
| [`XIsMultipliedPercentHealth`](./Enums.md) | Array | The [stacks, probability] for multiplying health by a percentage. | 3 | [2] |
| [`AbilityEnabledIfHasStatus`](./Enums.md) | Enum | Specifies the status effect that must be present on the unit for the ability to be enabled. | 2 | DemonicGlyph_Summon |
| [`AutocastEachRound`](#object-autocasteachround) | Object | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 2 ||
| [`ChargeSpiritBombAura`](./Enums.md) | Enum | Specifies the ability to charge for spirit bomb aura. | 2 | DonateEnergy |
| [`CopyCatPassive_Initializer`](./Enums.md) | Integer | The number of copies of this passive to initialize. | 2 | 2 |
| [`NukeQuestFinalBossModifications`](#object-nukequestfinalbossmodifications) | Object | Contains modifications for the nuke quest final boss, such as damage_instance effects. | 2 ||
| [`ReloadOnKill`](./Enums.md) | Integer | If set, this ability's reload charge is restored on kill (any kill). | 2 | 1 |
| [`ReloadOnKillEnemy`](./Enums.md) | Integer | If set, this ability's reload charge is restored only when killing an enemy. | 2 | 1 |
| [`ReloadOnTotalDamageReceived`](./Enums.md) | Integer | The threshold of total damage received to restore a reload charge. | 2 | 15 |
| [`XIsLivingCharactersWithTag`](./Enums.md) | Enum | Specifies the tag that living characters must have for this passive to affect them. | 2 | husk |
| [`XIsOtherHealsThisTurn`](./Enums.md) | Integer | If set, tracks other heals this turn for some effect. | 2 | 1 |
| [`XIsSpellStormRampAndReset`](#object-xisspellstormrampandreset) | Integer / Object | If integer 0, resets stacks; if object, contains 'stacks' and 'reset_percent' for spell storm ramp. | 2 | 0 |
| [`XIsTimesDamageTaken`](./Enums.md) | Integer | If set, multiplier for damage taken to apply some effect. | 2 | 1 |
| [`AbilityDisableIfLivingCrow`](./Enums.md) | Integer | If set, disables the ability if there is a living crow on the field. | 1 | 1 |
| [`AbilityEnabledAtHealthThreshold`](./Enums.md) | Integer | The health percentage threshold at which the ability becomes enabled. | 1 | 50 |
| [`AbilityEnabledIfBasicAttackUsedThisTurn`](./Enums.md) | Integer | If set, ability is enabled only if the unit used a basic attack this turn. | 1 | 1 |
| [`AbilityEnabledIfMovementTrapped`](./Enums.md) | Integer | If set, ability is enabled only when the unit's movement is trapped. | 1 | 1 |
| [`AbilityEnabledIfNoAggroTarget`](./Enums.md) | Integer | If set, ability is enabled only when the unit has no aggro target. | 1 | 1 |
| [`AbilityEnabledIfNotHasStatus`](./Enums.md) | Enum | Specifies the status that must be absent for ability to be enabled. | 1 | BackflipWhenTargeted |
| [`AbilityEnabledIfSpecificItemEquipped`](./Enums.md) | Enum | Specifies the item that must be equipped for ability to be enabled. | 1 | Neverstone |
| [`AbsorbManaFromOtherSpells`](./Enums.md) | Integer | If set, this ability absorbs mana from other spells when cast. | 1 | 1 |
| [`AddElementsToSpells`](./Enums.md) | Enum | Specifies which element to add to spells. | 1 | Earth |
| [`AddStatusToBasicAttack`](#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 1 ||
| [`AlphaDodgeChance`](./Enums.md) | Integer | The dodge chance granted to the alpha (leader) unit. | 1 | 50 |
| [`AlphaStatusOnTurnBegin`](#object-alphastatusonturnbegin) | Object | Specifies status effects applied to the alpha at the start of each turn. | 1 ||
| [`BonusAbility_DelayedApplication`](./Enums.md) | Enum | Specifies the name of a bonus ability to apply with a delay. | 1 | Slap |
| [`CapTechSpent`](./Enums.md) | Integer | The maximum amount of tech that can be spent on this ability per turn. | 1 | 1 |
| [`CaveWomanBirthControl`](./Enums.md) | Integer | If true, restricts or controls the spawning of additional units via birth mechanics. | 1 | 1 |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 1 | 2 |
| [`FistOfFateUniqueEnemyTracker`](./Enums.md) | Integer | Increases the damage tracking counter for unique enemies hit by Fist of Fate. | 1 | 1 |
| [`FreeFirstCastAndAfterSpendMana`](./Enums.md) | Integer | If set to 1, the first cast of the ability and each cast after spending mana costs no resources. | 1 | 1 |
| [`FreeFirstCastEachMatch`](./Enums.md) | Integer | If set to 1, the first cast of the ability each match costs no resources. | 1 | 1 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | 2 |
| [`IgnoreTiles`](./Enums.md) | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 1 | 1 |
| [`IntelligenceUp`](./Enums.md) | Enum / Integer | The amount of Intelligence added as a flat bonus. | 1 | item_aux |
| [`InterchangeDisabler`](./Enums.md) | Integer | If set to 1, prevents the unit from being interchanged with another unit. | 1 | 1 |
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit cannot be knocked back. | 1 | 1 |
| [`PassiveWhileNotTakingTurn`](#object-passivewhilenottakingturn) | Object | A nested passive object that is active only while the unit is not currently taking its turn. | 1 ||
| [`ReloadOnAllyCatDies`](./Enums.md) | Integer | If set to 1, restores a charge when an allied cat dies. | 1 | 1 |
| [`ReloadOnAllyDies`](./Enums.md) | Integer | If set to 1, restores a charge when any ally dies. | 1 | 1 |
| [`ReloadOnAnyDamage`](./Enums.md) | Integer | If set to 1, restores a charge when any damage is taken. | 1 | 1 |
| [`ReloadOnBackstab`](./Enums.md) | Integer | If set to 1, restores a charge when performing a backstab. | 1 | 1 |
| [`ReloadOnElementalDamageReceived`](./Enums.md) | Enum | Specifies the elemental type of damage that, when received, restores a charge. | 1 | Holy |
| [`ReloadOnGainCoins`](./Enums.md) | Integer | If set to 1, restores a charge when coins are gained. | 1 | 1 |
| [`ReloadOnGainDivineShield`](./Enums.md) | Integer | If set to 1, restores a charge when a Divine Shield is gained. | 1 | 1 |
| [`ReloadOnKillTagged`](./Enums.md) | Enum | Specifies the tag of enemies that, when killed, restore a charge. | 1 | rock |
| [`ReloadOnSpendMana`](./Enums.md) | Integer | If set to 1, restores a charge when mana is spent. | 1 | 1 |
| [`ReloadOnUseAbilityWithManaCost`](./Enums.md) | Integer | Specifies the amount of mana cost that, when used, restores a charge. | 1 | 6 |
| [`RevengeDamage`](#object-revengedamage) | Object | An object defining the damage and effects that trigger when the unit is attacked. | 1 ||
| [`StatusKillers`](#object-statuskillers) | Object | An object containing nested conditionals that apply status effects when the unit kills an enemy. | 1 ||
| [`TossTargetIsAggroTarget`](./Enums.md) | Integer | If set to 1, the toss target is the unit's current aggro target. | 1 | 1 |
| [`TossTargetIsBuddy`](./Enums.md) | Integer | If set to 1, the toss target is the unit's buddy. | 1 | 1 |
| [`TossTargetIsNotInWater`](./Enums.md) | Integer | If set to 1, the toss target must not be in water terrain. | 1 | 1 |
| [`Trample`](./Enums.md) | Integer | The amount of bonus damage dealt when moving through an enemy. | 1 | 3 |
| [`XIsConsumedCharacterMaxHP`](./Enums.md) | Integer | Specifies the multiplier used to set X to the maximum HP of the consumed character. | 1 | 3 |
| [`XIsCountDeaths`](./Enums.md) | Integer | If set to 1, X is equal to the number of deaths in the match. | 1 | 1 |
| [`XIsCountStatusStacks`](./Enums.md) | Enum | Specifies the status field whose stacks are counted to set X. | 1 | DodgeChance_Status |
| [`XIsFormulaLockedUntilComplete`](./Enums.md) | Enum | Specifies a stat (e.g., dex) whose value is locked in and used for X until the ability completes. | 1 | dex |
| [`XIsIncreaseEachTurn`](./Enums.md) | Integer | Specifies the amount by which X increases each turn. | 1 | 1 |
| [`XIsRampAndReset`](./Enums.md) | Integer | If set to 1, X ramps up over time and resets after use; 0 disables this behavior. | 1 | 0 |
| [`XIsRecycleCostReduction`](./Enums.md) | Integer | Specifies the amount of recycle cost reduction applied to X. | 1 | 5 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 37 ||
| [`Trample`](./Enums.md) | Integer | The amount of bonus damage dealt when moving through an enemy. | 26 | 3 |
| `CastAgain` | Integer / String | The number of additional times the ability can be cast this turn. | 20 ||
| `DisableTrample` | Integer | If set to 1, trample damage is disabled for the duration of the effect. | 10 ||
| `Fury` | Integer | The amount of Fury (bonus damage or charges) gained. | 7 ||
| [`TileTrail`](./Enums.md) | Enum | Specifies the type of tile left behind as the unit moves. | 6 | FloatingGlassTile |
| `JustInCaseTrample` | Integer | If set to a non-zero value, applies a trample effect as a fallback. | 5 ||
| [`LeaveBehind`](#object-leavebehind) | Enum / Object | Specifies the object or entity to spawn after the unit leaves a tile. | 5 ||
| `DashFury` | Integer | The amount of Fury gained after dashing. | 3 ||
| `BearTrapTrail` | Integer | If set to 1, leaves bear traps behind as the unit moves. | 2 ||
| [`AfterImage`](#object-afterimage) | Object | Specifies the object or skill used to create an afterimage of the unit. | 2 ||
| `DelayedWindTrail` | Integer | If set to 1, creates a delayed wind trail behind the unit. | 1 ||
| [`JumpAttackLeaveBehind`](./Enums.md#enum-jumpattackleavebehind) | Enum | Specifies the entity to leave behind at the jump attack's landing point. | 1 ||
| [`DoubleLoot`](./Enums.md) | Integer | The multiplier for loot drops, where 1 or 2 doubles the loot. | 1 | 2 |
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit cannot be knocked back. | 1 | 1 |
| [`TileTrail_Ahead`](./Enums.md) | Enum | Specifies the type of tile to place one tile ahead of the unit's movement. | 1 | FlowerTile |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 66 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 23 ||
| [`GainDisorderFromPool_PostCast`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the pool of disorders the unit can gain after the spell is cast. | 7 ||
| [`ApplyToSource`](#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 6 ||
| [`BonusDamage`](./Engine_LogicKeys.md#valid-property-keys) | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 6 ||
| [`CanApplyToInanimate`](#object-canapplytoinanimate) | Object | An object containing effects that can be applied to inanimate objects. | 3 ||
| `Vaporize` | `Number` | Removes the target from play, preventing its corpse from being interacted with. | 3 ||
| `CaptureFamiliar` | Integer | The number of times to attempt to capture the target as a familiar. | 2 ||
| [`Conditional_HasStatus`](#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 2 ||
| `FactionConversion` | Integer | Converts the target to the caster's faction. | 2 ||
| [`FormChange`](#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 2 ||
| `FullHeal` | `Number` | If non-zero, fully restores the target's health. | 2 ||
| `RandomStatDown` | Array / Integer / String | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 2 ||
| `SpawnBearTrapIfHitKills` | `Number` | If non-zero, spawns a bear trap at the target's location upon a killing blow. | 2 ||
| [`SpawnThingIfHitKills`](./Engine_LogicKeys.md#valid-property-keys) | `String` | The name of the thing (e.g., a food type) to spawn at the target's location upon a killing blow. | 2 ||
| [`RandomStatusFromPool`](#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 2 ||
| [`Cleanse`](./Enums.md) | Integer | The number of stacks of negative status effects removed from the target. | 2 | 0 |
| [`Confusion`](./Enums.md) | Array / Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 2 | [.1] |
| [`GainCoinsRange`](#object-gaincoinsrange) | Object | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 2 ||
| [`RandomStatUp`](./Enums.md) | Enum / Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | ceil(X/3) |
| [`Revive`](./Enums.md) | Integer | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | 50 |
| [`ApplyToRandomPartyMemberIfPossible`](#object-applytorandompartymemberifpossible) | Object | Contains an inner effect block that is applied to a random living party member if one exists. | 1 ||
| [`CatPartsTransform`](#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 ||
| [`Conditional_Displaceable`](#object-conditional_displaceable) | Object | Contains an inner effect block that only executes if the target can be displaced (knocked back). | 1 ||
| [`Conditional_GoodRoll`](#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 ||
| [`Conditional_HealthThreshold`](#object-conditional_healththreshold) | Object | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 1 ||
| [`Consumed`](#object-consumed) | Object | An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`. | 1 ||
| [`DestroyEquipmentAndAttachParasite`](#object-destroyequipmentandattachparasite) | Object | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 1 ||
| `DieViolently` | Integer | If true, causes the target to die with a violent, explosive visual effect. | 1 ||
| [`DoDamage`](#object-dodamage) | Object | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 1 ||
| `ExplodeCharacter` | `Number` | The radius (in tiles) of an explosion centered on the character. | 1 ||
| `ExplodeCharacter_Party` | `Number` | The radius (in tiles) of an explosion centered on the character that also damages party members. | 1 ||
| `FaceCamera` | `Number` | If non-zero, forces the character to rotate and face the camera. | 1 ||
| `FlatAIBonus` | `Number` | A flat adjustment to the AI's evaluation score for this action; positive values encourage the AI to use it, negative values discourage it. | 1 ||
| `ForceImmediateMove` | `Number` | If non-zero, forces the character to move instantly without waiting for normal action order. | 1 ||
| `GenericDebuff` | `Number` | The number of stacks of a generic, untooltipped debuff applied to the target. | 1 ||
| [`ImmediateUseAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of an ability to be triggered instantly from this effect. | 1 ||
| `Instakill` | `Number` | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 1 ||
| [`KnockUpAndAway`](#object-knockupandaway) | Object | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 ||
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 1 ||
| `PurgeAll` | `Number` | If non-zero, removes all temporary status effects (buffs, debuffs) from the target. | 1 ||
| `RemoveMovePoints` | `Number` | The number of move points to remove from the target, preventing them from moving. | 1 ||
| `RemoveTurnsThisRound` | `Number` | The number of turns to remove from the target's turn order this round. | 1 ||
| `SetHealth` | `Number` | Sets the target's health to a specific flat value or percentage. | 1 ||
| `SetShield` | `Number` | Sets the target's shield value to a specific flat amount. | 1 ||
| [`ShowFakeDamage`](#object-showfakedamage) | Object | Displays a fake damage number (with optional style) for visual effect without actually changing health. | 1 ||
| `SpeculativeMoveSelfCorpseOffMap` | `Number` | If true, attempts to remove the character's corpse from the map, used for speculative AI targeting. | 1 ||
| [`Temporary`](#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 1 ||
| `VaporizeInanimate` | `Number` | If non-zero, instantly destroys inanimate objects (corpses, rocks) as if they were vaporized. | 1 ||
| [`XIsTargetHealth`](#object-xistargethealth) | Object | Evaluates a bonus damage formula where X is the target's current health. | 1 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | 2 |
| [`Bruise`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 1 | [.1] |
| [`Charmed`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | [.1] |
| [`Cleave`](#object-cleave) | Integer / Object | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 1 | 1 |
| [`Conditional_HasTag`](#object-conditional_hastag) | Object | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 1 ||
| [`Conditional_Object`](#object-conditional_object) | Object | Evaluates whether the target is an object (vs a character); if true, applies the effects within; otherwise, runs the Else block. | 1 ||
| [`Conditional_Speculative`](#object-conditional_speculative) | Object | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 1 ||
| [`ConstitutionUp`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | [.5] |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 1 | 2 |
| [`DamageUp`](./Enums.md) | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | 3 |
| [`DodgeChance_Status`](./Enums.md) | Integer | The flat percentage increase to dodge chance applied as a status effect. | 1 | 50 |
| [`DybbukPossessed`](#object-dybbukpossessed) | Object | Contains parameters for the Dybbuk possession status, specifying exit ability and self-punch ability. | 1 ||
| [`Else`](#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 ||
| [`Immobile`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | [.1] |
| [`Leeches`](./Enums.md) | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 1 | 2 |
| [`ObjectOnHitCharacter`](#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | SkeletonCatFamiliar |
| [`PartialCleanse`](./Enums.md) | Integer | The number of stacks of temporary status effects to remove from the target. | 1 | 9999 |
| [`ScatterCoins`](#object-scattercoins) | Object | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 1 ||
| [`Slow`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 1 | [.1] |
| [`SpeedUp`](./Enums.md) | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | 4 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 43 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 20 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 6 | 2 |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 6 | 5 |
| [`StrengthUp`](./Enums.md) | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 6 | max(int, 0) |
| [`Shield`](./Enums.md) | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 5 | 2*X |
| [`EvolveAbilityFromPool`](./Abilities_and_Spells.md#object-evolveabilityfrompool) | `String` | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 4 ||
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | `String` | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 4 ||
| [`AddWeaponAux`](./Engine_LogicKeys.md#valid-property-keys) | `String` | The amount or expression to add to the source's weapon auxiliary stat. | 3 ||
| [`Craft`](#object-craft) | Object | Specifies the loot pool and slot to craft an item for the source. | 3 ||
| `RefreshActPoints` | `Number` | The amount of action points restored to the source. | 3 ||
| [`ConstitutionUp`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 3 | [.5] |
| `AddLeechesStatus` | `Number` | The number of stacks of Leech status applied to the source, healing when dealing damage. | 2 ||
| [`DoDamage`](#object-dodamage) | Object | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 2 ||
| [`Cleanse`](./Enums.md) | Integer | The number of stacks of negative status effects removed from the target. | 2 | 0 |
| [`EquipPermanentItem`](./Enums.md) | Enum | The name of the item to permanently equip to the source. | 2 | BoneClub |
| [`FindItemFromPool`](#object-finditemfrompool) | Object | Specifies the loot pool from which to find an item, with an optional chance. | 2 ||
| [`FreeSpell`](./Enums.md) | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. | 2 | 2 |
| [`LuckUp`](./Enums.md) | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | 2 |
| [`RemoveStatus`](./Engine_LogicKeys.md#valid-property-keys) | `String` | The name of the status effect to remove from the source. | 1 ||
| `DisableWeapon` | `Number` | If set, disables the source's weapon, preventing its use. | 1 ||
| `FullHeal` | `Number` | If non-zero, fully restores the target's health. | 1 ||
| [`KnockUpAndAway`](#object-knockupandaway) | Object | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 ||
| `ManaGain` | `Number` | The amount of mana restored to the source, which can be an expression. | 1 ||
| `RefreshMovePoints` | `Number` | The amount of movement points restored to the source. | 1 ||
| [`SpecificInjury`](./Engine_LogicKeys.md#valid-property-keys) | `String` | The stat (str, spd, int) to which a specific injury is applied, reducing that stat. | 1 ||
| `StanceSwitchToMelee` | `Number` | If set, switches the source to melee stance. | 1 ||
| `StanceSwitchToRanged` | `Number` | If set, switches the source to ranged stance. | 1 ||
| `TakeExtraTurn` | `Number` | The number of extra turns granted to the source. | 1 ||
| `TempTrampleUntilSettled` | `Number` | The number of stacks of temporary Trample applied to the source, allowing movement through enemies until the source ends its turn. | 1 ||
| [`Brace`](./Enums.md) | Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | 2 |
| [`Bruise`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 1 | [.1] |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | 2 |
| [`FindItem`](./Enums.md) | Enum | The name of the specific item to find and add to the source's inventory. | 1 | Molars |
| [`ForceUseAbility`](./Enums.md) | Enum | The name of the ability the source is forced to use, optionally with a chance. | 1 | MotherTumorGrow |
| [`GainCoinsRange`](#object-gaincoinsrange) | Object | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 1 ||
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 1 | 1 |
| [`Tech`](./Enums.md) | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 1 | 3 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 46 ||
| [`tag`](./Enums.md) | Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 46 | megadino |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 11 ||
| [`Conditional_NotBoss`](#object-conditional_notboss) | Object | Contains effects that apply only if the target is not a boss enemy. | 6 ||
| `FloatingRockTrap` | `Number` | The number of stacks of Floating Rock Trap applied to the target, dealing damage when stepped on. | 6 ||
| [`Conditional_Boss`](#object-conditional_boss) | Object | Contains effects that apply only if the target is a boss enemy. | 4 ||
| `IgnoreDamage` | `Number` | If set, the target ignores all damage for the duration. | 4 ||
| [`ApplyToSource`](#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 3 ||
| [`ImmediateUseAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of an ability to be triggered instantly from this effect. | 3 ||
| [`ApplyToSourceOnKill`](#object-applytosourceonkill) | Object | Contains effects that are applied to the source when it kills the target. | 2 ||
| [`CanApplyToInanimate`](#object-canapplytoinanimate) | Object | An object containing effects that can be applied to inanimate objects. | 2 ||
| `Die` | `Number` | If set, kills the target immediately. | 2 ||
| `Vaporize` | `Number` | Removes the target from play, preventing its corpse from being interacted with. | 2 ||
| [`ChangeTilesUnder`](./Enums.md) | Enum | The tile type to change the ground tiles under the target to. | 2 | LavaTile |
| [`DamageUp`](./Enums.md) | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | 3 |
| [`Else`](#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 2 ||
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 1 ||
| [`Conditional_InForm`](#object-conditional_inform) | Object | Contains effects that apply only if the target is in the specified form. | 1 ||
| `CrackMoonHead` | `Number` | If set, cracks the MoonHead's head, triggering its death sequence. | 1 ||
| `DeleteObject` | `Number` | If set, deletes the target object from the map. | 1 ||
| `DisplaceTowardsSource` | `Number` | If set, displaces the target towards the source of the effect. | 1 ||
| `FaceAway` | `Number` | If set, forces the target to face away from the source. | 1 ||
| `Instakill` | `Number` | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 1 ||
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 1 ||
| [`PopAndSpawn`](#object-popandspawn) | Enum / Object | The object (enemy or entity) to spawn on the target's tile, optionally with visual effects. | 1 ||
| [`RemoveStatus`](./Engine_LogicKeys.md#valid-property-keys) | `String` | The name of the status effect to remove from the source. | 1 ||
| `ScatterRandomPickups` | `Number` | The number of random pickups scattered around the target's location. | 1 ||
| `SetKnockback` | `Number` | The knockback distance to set for the damage instance, overriding default. | 1 ||
| [`UseAbility`](./Abilities_and_Spells.md#object-useability) | `String` | The name of the ability the target is forced to use. | 1 ||
| `VaporizeCorpse` | `Number` | If set, vaporizes the target's corpse, preventing revival. | 1 ||
| [`EventBounty`](./Enums.md) | Integer | The number of stacks of Event Bounty applied, increasing event rewards. | 1 | 5 |
| [`MergeDamageInstance`](#object-mergedamageinstance) | Object | Specifies parameters to merge multiple damage instances into one, controlling hit animation and instant pop behavior. | 1 ||
| [`SetAnimationAlts`](#object-setanimationalts) | Object | Specifies alternative animation names for the target's dying and dead states. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 34 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 12 ||
| [`Confusion`](./Enums.md) | Array / Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 9 | [.1] |
| [`Conditional_NotBoss`](#object-conditional_notboss) | Object | Contains effects that apply only if the target is not a boss enemy. | 3 ||
| [`DisplaceToAbilityTarget`](./Enums.md) | Integer | If set, displaces the source to the ability's target location. | 3 | 1 |
| `TakeExtraTurn` | `Number` | The number of extra turns granted to the source. | 2 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | 2 |
| [`Attraction`](./Enums.md) | Integer | The number of stacks of Attraction applied, drawing enemy units toward the target. | 2 | 1 |
| [`Fear`](./Enums.md) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | [.3] |
| [`Madness`](#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 2 | [.1] |
| [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | [0] |
| [`Weakness`](./Enums.md) | Array / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 2 | [.1] |
| [`ApplyToSource`](#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 1 ||
| [`ApplyToSourceOnKill`](#object-applytosourceonkill) | Object | Contains effects that are applied to the source when it kills the target. | 1 ||
| `BonusDamage` | `Number` | The amount of flat bonus damage added (negative values reduce damage). | 1 ||
| `ForceMoveTowards` | `Number` | The number of tiles to force the target to move toward the caster. | 1 ||
| [`Temporary`](#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 1 ||
| [`Burn`](./Enums.md) | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | [.1] |
| [`Charmed`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | [.1] |
| [`Conditional_FinishedSpawning`](#object-conditional_finishedspawning) | Object | Contains an inner effect block that only executes if the target has finished its spawning animation. | 1 ||
| [`Doomed`](./Enums.md) | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 1 | 3 |
| [`Hex`](./Enums.md) | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. | 1 | 1 |
| [`Marked`](./Enums.md) | Array / Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 1 | [.1] |
| [`PermanentCharm`](./Enums.md) | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 1 | 1 |
| [`Poison`](./Enums.md) | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | [.1] |
| [`TempDamageUp`](./Enums.md) | Integer | The amount of temporary damage increase applied. | 1 | 2 |

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 57 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 56 ||
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 52 ||
| `expires_on_begin_turn` | Boolean | If true, the temporary effect expires at the start of the target's turn. | 25 ||
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 21 ||
| `data` | Integer | An integer value used for custom data associated with the temporary effect. | 2 ||
| `expires_on_appliers_turn` | Boolean | If true, the temporary effect expires at the start of the applier's next turn. | 2 ||
| `expires_on_move` | Boolean | If true, the temporary effect expires when the target moves. | 1 ||

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
| [`ontrigger`](./Enums.md#enum-ontrigger) | Enum | Specifies the sound effect to play when the ability triggers (e.g., hits a target). | 32 ||
| [`oncast`](./Enums.md#enum-oncast) | Enum | Specifies the sound effect to play when the ability is cast. | 3 ||
| [`oncastpoint`](./Enums.md#enum-oncastpoint) | Enum | Specifies the sound effect to play at a specific cast point during the ability animation. | 3 ||
| [`ontrigger_intentional`](./Enums.md#enum-ontrigger_intentional) | Enum | Specifies the sound effect to play when the ability is triggered intentionally (as opposed to automatically). | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 28 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 ||
| [`DamageUp`](./Enums.md) | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 5 | 3 |
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 4 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | 2 |
| `KnockbackDamageImmuneUntilSettled` | `Number` | If non-zero, makes the target immune to damage from knockback until they stop moving. | 3 ||
| [`Temporary`](#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 3 ||
| [`Cleanse`](./Enums.md) | Integer | The number of stacks of negative status effects removed from the target. | 3 | 0 |
| [`ApplyToSource`](#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 2 ||
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 2 | 5 |
| [`RandomStatUp`](./Enums.md) | Enum / Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | ceil(X/3) |
| [`ApplyToSourceOnKill`](#object-applytosourceonkill) | Object | Contains effects that are applied to the source when it kills the target. | 1 ||
| `ChanceToBreak` | `Number` | Specifies the percentage chance that the item breaks on use. | 1 ||
| [`Conditional_Corpse`](#object-conditional_corpse) | Object | Contains an inner effect block that only executes if the target is a corpse. | 1 ||
| [`Conditional_PlayerCat`](#object-conditional_playercat) | Object | Defines effects that only apply if the target is a player-controlled cat. | 1 ||
| `FullHeal` | `Number` | If non-zero, fully restores the target's health. | 1 ||
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. | 1 ||
| `RepairAll` | `Number` | The amount of durability restored to all equipped items. | 1 ||
| [`ShowText`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the localization key for a popup text displayed on the target. | 1 ||
| `ThornsDamageImmuneUntilSettled` | `Number` | The number of turns the target is immune to thorns damage until it settles. | 1 ||
| `TileDamageImmuneUntilSettled` | `Number` | The number of turns the target is immune to tile damage until it settles. | 1 ||
| [`BleedThorns`](./Enums.md) | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 1 | 3 |
| [`Charmed`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | [.1] |
| [`TempDamageUp`](./Enums.md) | Integer | The amount of temporary damage increase applied. | 1 | 2 |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | 2 |

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
| `odds` | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 37 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 37 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 28 ||
| [`GainDisorderFromPool_PostCast`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the pool of disorders the unit can gain after the spell is cast. | 7 ||
| [`ApplyToRandomPartyMemberIfPossible`](#object-applytorandompartymemberifpossible) | Object | Contains an inner effect block that is applied to a random living party member if one exists. | 1 ||
| [`ApplyToSource`](#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 1 ||
| [`GainDisorder`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the disorder gained. | 1 ||
| [`ImmediateUseAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of an ability to be triggered instantly from this effect. | 1 ||
| `RefreshWeaponAbility` | `Number` | The number of times the weapon's ability is refreshed. | 1 ||
| [`ShowText`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the localization key for a popup text displayed on the target. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 16 ||
| [`BonusAbility`](./Enums.md) | Enum | Specifies the name of a bonus ability granted. | 2 | DonateEnergy |
| [`DamageUp`](./Enums.md) | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | 3 |
| [`Shield`](./Enums.md) | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 2 | 2*X |
| `TemporaryItem` | Integer | The number of times a temporary item can be used before disappearing. | 1 ||
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | [.1] |
| [`Brace`](./Enums.md) | Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | 2 |
| [`Charmed`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | [.1] |
| [`Madness`](#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | [.1] |
| [`PermanentMadness`](./Enums.md) | Integer | The number of permanent madness stacks applied. | 1 | 1 |
| [`RandomMagicMissile`](#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, or an object defining its properties. | 1 | 5 |
| [`Webbed`](./Enums.md) | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 35 ||
| [`damage`](#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 32 ||
| [`effects`](#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 17 ||
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 13 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 13 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 12 ||
| `makes_contact` | `Boolean` | If true, the damage instance is considered a contact hit, triggering contact-based passives on both the attacker and target. | 6 ||
| `override_trample_damage` | `Boolean` | If true, this damage instance replaces any default trample damage when the unit passes through an occupied tile. | 2 ||
| `ai_base_score` | Integer | The base priority score the AI assigns to using this damage instance, with higher values indicating greater preference. | 1 ||
| `crit_chance` | `Number` | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 1 ||
| `force_no_knockback` | `Boolean` | If true, the damage instance applies no knockback regardless of any knockback values set. | 1 ||
| `force_play_hit_animation` | `Boolean` | If true, the hit animation is forced to play regardless of other conditions (e.g., miss or block). | 1 ||
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Specifies the layer on which the ability's effect operates (e.g., characters, tiles, gas). | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 19 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 ||
| [`Conditional_HasStatus`](#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 6 ||
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 4 ||
| [`RemoveStatus`](./Engine_LogicKeys.md#valid-property-keys) | `String` | The name of the status effect to remove from the source. | 4 ||
| [`Else`](#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 4 ||
| [`VisualFX`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the visual effect to play. | 3 ||
| [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 3 | [0] |
| [`BonusDamage`](./Engine_LogicKeys.md#valid-property-keys) | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 2 ||
| [`Charmed`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | [.1] |
| [`Drowsy`](./Enums.md) | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. | 2 | 8 |
| [`ExplodeCharacter_PartyBoss`](./Enums.md) | Integer | The damage dealt to the party boss when it explodes. | 2 | 5 |
| [`ExplodeCharacter_RockCrusher_PetrifyBreak`](./Enums.md) | Integer | The damage dealt when a petrified RockCrusher explodes. | 2 | 5 |
| `ExplodeCharacter_NoDie` | `Number` | The damage dealt when a character explodes without dying. | 1 ||
| [`XIsTargetHealth`](#object-xistargethealth) | Object | Evaluates a bonus damage formula where X is the target's current health. | 1 ||
| [`Fear`](./Enums.md) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | [.3] |

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
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 13 ||
| [`pool`](./Enums.md) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 13 | [Ping] |

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
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 24 ||
| [`stacks`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 22 ||
| `height` | Integer | The height in tiles the target is launched into the air. | 2 ||
| `circular_variance` | Integer | The random variance in the knockback direction, in tiles. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 19 ||
| [`SafeDoomed`](./Enums.md) | Enum / Integer | The number of SafeDoomed stacks applied, or 'level' to scale with character level. | 11 | 2 |
| [`InjuryImmunity`](./Enums.md) | Integer | The number of turns the unit is immune to injuries. | 7 | 1 |
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | 2 |
| [`FadeInsteadOfDie`](./Enums.md) | Integer | If non-zero, the unit fades out instead of dying. | 2 | 1 |
| [`IllusionTint`](./Enums.md) | Integer | If non-zero, applies an illusionary tint to the unit's sprite. | 2 | 1 |
| [`PermanentMadness`](./Enums.md) | Integer | The number of permanent madness stacks applied. | 2 | 1 |
| [`ApplyPassivesToSpawnerWhileAlive`](#object-applypassivestospawnerwhilealive) | Object | An object defining passives that are applied to the spawner while this unit is alive. | 1 ||
| [`CaptureFamiliar`](./Enums.md) | Integer | The number of times to attempt to capture the target as a familiar. | 1 | 1 |
| [`DamageUp`](./Enums.md) | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | 3 |
| [`FillMana`](./Enums.md) | Integer | The amount of mana restored, or an [amount, probability] array. | 1 | 1 |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 1 | 5 |
| [`HideEquipment`](./Enums.md) | Enum | Specifies which equipment slot is visually hidden. | 1 | neck |
| [`ReviveNextRound`](#object-revivenextround) | Integer / Object | The number of revives granted, or an object defining revive properties. | 1 | 2 |
| [`SchizoIllusionAIModifier`](./Enums.md) | Integer | If non-zero, modifies the AI behavior for schizo illusions. | 1 | 1 |
| [`SpeedUp`](./Enums.md) | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | 4 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 20 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 20 ||
| [`BonusDamage`](./Enums.md) | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 6 | -4 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 |
| [`ApplyToSource`](#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 3 ||
| [`Burn`](./Enums.md) | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 2 | [.1] |
| [`RemoveStatus`](./Enums.md) | Enum | The name of the status effect to remove from the source. | 2 | Sleep |
| [`Slow`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 2 | [.1] |
| [`Confusion`](./Enums.md) | Array / Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | [.1] |
| [`Fear`](./Enums.md) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | [.3] |
| [`FormChange`](#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 1 | Open |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 33 ||
| [`Shield`](./Enums.md) | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 12 | 2*X |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 12 |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 10 | 2 |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 9 | 2 |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 9 | 2 |
| [`Poison`](./Enums.md) | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 9 | [.1] |
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 8 | [.1] |
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 8 | 2 |
| [`Weakness`](./Enums.md) | Array / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 8 | [.1] |
| [`Slow`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 7 | [.1] |
| [`Blind`](./Enums.md) | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | [2] |
| [`Brace`](./Enums.md) | Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 6 | 2 |
| [`Bruise`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 6 | [.1] |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of diminishing health regen stacks applied. | 6 | 3 |
| [`GainCoins`](./Enums.md) | Integer | The amount of coins gained, or a [min, max] range. | 6 | 2 |
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 5 | 2 |
| [`Burn`](./Enums.md) | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 5 | [.1] |
| [`MoveQuivered`](./Enums.md) | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 5 | 1 |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 5 | 1 |
| [`RandomStatUp`](./Enums.md) | Enum / Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 5 | ceil(X/3) |
| [`BleedThorns`](./Enums.md) | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 4 | 3 |
| [`ConstitutionUp`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 4 | [.5] |
| [`Madness`](#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 4 | [.1] |
| [`MagicWeakness`](./Enums.md) | Array / Integer | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 4 | [.1] |
| [`Marked`](./Enums.md) | Array / Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 4 | [.1] |
| [`Reflect`](./Enums.md) | Integer | The amount of reflect stacks applied. | 4 | 5 |
| [`SpeedUp`](./Enums.md) | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 4 | 4 |
| [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 4 | [0] |
| [`Tarred`](./Enums.md) | Array / Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 4 | [.1] |
| [`Charmed`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 3 | [.1] |
| [`Confusion`](./Enums.md) | Array / Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 3 | [.1] |
| [`DamageUp`](./Enums.md) | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 3 | 3 |
| [`Fear`](./Enums.md) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 3 | [.3] |
| [`Freeze`](./Enums.md) | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. | 3 | [.1] |
| [`Immobile`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 3 | [.1] |
| [`Petrify`](./Enums.md) | Array / Integer | The amount of petrify stacks applied, or an [stacks, probability] array. | 3 | [.15] |
| [`Sleep`](./Enums.md) | Array / Integer | The amount of sleep stacks applied, or an [stacks, probability] array. | 3 | [.1] |
| [`StrengthUp`](./Enums.md) | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 3 | max(int, 0) |
| [`BackflipWhenTargeted`](#object-backflipwhentargeted) | Integer / Object | The number of backflip charges, or an object defining its ability. | 2 | 2 |
| [`BonusDamage`](./Enums.md) | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 2 | -4 |
| [`CharismaUp`](./Enums.md) | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. | 2 | -2 |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 2 | 2 |
| [`DexterityUp`](./Enums.md) | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. | 2 | 2 |
| [`DodgeChance_Status`](./Enums.md) | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 | 50 |
| [`FormChange`](#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 2 | Open |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 2 | 2 |
| [`IntelligenceUp`](./Enums.md) | Enum / Integer | The amount of Intelligence added as a flat bonus. | 2 | item_aux |
| [`Lifesteal`](./Enums.md) | Integer | The amount of lifesteal stacks applied. | 2 | 3 |
| [`LuckUp`](./Enums.md) | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | 2 |
| [`PoisonLace`](./Enums.md) | Enum / Integer | Integer or fractional string (e.g., 'X/3') specifying the duration or intensity of the PoisonLace effect. | 2 | X/3 |
| [`RandomStatDown`](./Enums.md) | Array / Enum / Integer | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 2 | [.25] |
| [`Rot`](./Enums.md) | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 2 | [.1] |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 2 | 3 |
| [`TempCounterAttack`](./Enums.md) | Integer | The number of turns TempCounterAttack lasts, ticking down at the start of the unit's turn. | 2 | 1 |
| [`DelayedPain`](./Enums.md) | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. | 1 | 1 |
| [`Hex`](./Enums.md) | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. | 1 | 1 |
| [`IncAuxCounterClamped`](#object-incauxcounterclamped) | Object | An object with `change` and `max` properties modifying the auxiliary counter by `change`, clamped to `max`. | 1 ||
| [`Infested`](./Enums.md) | Integer | The number of stacks of Infested applied. | 1 | 1 |
| [`ManaGain`](./Enums.md) | Enum / Integer | The amount of mana restored to the source, which can be an expression. | 1 | 0 |
| [`Ostracized`](./Enums.md) | Integer | The number of stacks of Ostracized applied. | 1 | 2 |
| [`RefreshActPoints`](./Enums.md) | Integer | The amount of action points restored to the source. | 1 | 1 |
| [`RefreshMovePoints`](./Enums.md) | Integer | The amount of movement points restored to the source. | 1 | 1 |
| [`Scrambled`](./Enums.md) | Integer | The number of stacks of Scrambled applied. | 1 | 2 |

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 22 ||
| [`struggle_ability`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the ability the consumed unit uses to attempt escape. | 17 ||
| `force_contact` | `Boolean` | If true, the consumed unit is forced into contact with the consumer. | 15 ||
| `instant` | `Boolean` | If true, the consumption happens immediately without a timer. | 12 ||
| [`mount_mode`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the mounting mode; values include 'auto' or 'true'. | 12 ||
| `do_not_pop_corpse` | `Boolean` | If true, the consumed unit's corpse is not popped upon consumption. | 11 ||
| [`drop_on_death`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Determines if and how the consumed unit is dropped on death; values include 'true', 'false', or 'deferred'. | 11 ||
| `wet` | `Boolean` | If true, the consumed unit is considered wet (e.g., for elemental interactions). | 8 ||
| `drop_on_self_death` | `Boolean` | If true, the consumed unit is dropped when the consumer dies. | 3 ||
| [`extra_statuses`](#object-extra_statuses) | Object | An object containing additional status effects (with stack counts) applied to the consumed unit. | 3 ||
| `use_placeholder` | Boolean | If true, renders the ability using a temporary placeholder animation instead of the final art. | 3 ||
| [`drop_body_ability`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the ability used to drop the consumed body. | 1 ||
| `kill_on_consume` | `Boolean` | If true, the consumed unit is killed immediately upon consumption. | 1 ||

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
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 13 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 ||
| [`CaptureFamiliar`](./Enums.md) | Integer | The number of times to attempt to capture the target as a familiar. | 2 | 1 |
| [`Doomed`](./Enums.md) | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 2 | 3 |
| [`ExplodeCharacter_RockCrusher`](./Enums.md) | Integer | The number of RockCrusher explosion triggers applied to non-boss characters. | 2 | 5 |
| [`FactionConversion`](./Enums.md) | Integer | Converts the target to the caster's faction. | 2 | 1 |
| [`Vaporize`](./Enums.md) | Integer | Removes the target from play, preventing its corpse from being interacted with. | 2 | 20 |
| [`VaporizeInanimate`](./Enums.md) | Integer | If non-zero, instantly destroys inanimate objects (corpses, rocks) as if they were vaporized. | 2 | 1 |
| [`CanApplyToInanimate`](#object-canapplytoinanimate) | Object | An object containing effects that can be applied to inanimate objects. | 1 ||
| [`Conditional_HealthThreshold`](#object-conditional_healththreshold) | Object | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 1 ||
| [`Fear`](./Enums.md) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | [.3] |
| [`PermanentCharm`](./Enums.md) | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 1 | 1 |

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
| [`form`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Specifies the name of the form the unit changes into. | 75 ||
| [`chance`](./Enums.md) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | .02 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 13 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 ||
| [`RemoveItem`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the item ID to remove from the source on kill. | 2 ||
| [`CompleteItemQuest`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the item quest ID to mark as complete on kill. | 2 ||
| `ManaGain` | `Number` | The amount of mana restored to the source, which can be an expression. | 2 ||
| [`AlphaCat`](./Enums.md) | Integer | The number of AlphaCat stacks applied to the source on kill. | 2 | 1 |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 2 | 5 |
| [`Revive`](./Enums.md) | Integer | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | 50 |
| [`EvolveAbilityFromPool`](./Abilities_and_Spells.md#object-evolveabilityfrompool) | `String` | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 1 ||
| `RefreshActPoints` | `Number` | The amount of action points restored to the source. | 1 ||
| `TakeExtraTurn` | `Number` | The number of extra turns granted to the source. | 1 ||
| [`TransformWeapon`](#object-transformweapon) | Object | An object with `from` and `to` fields specifying the weapon transformation. | 1 ||
| [`WeaponAuxMultiplier`](./Engine_LogicKeys.md#valid-property-keys) | `String` | A multiplier string (e.g., '.5') for the weapon's auxiliary counter on kill. | 1 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | 2 |
| [`StrengthUp`](./Enums.md) | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | max(int, 0) |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 ||
| [`BreakIntoRocks`](./Enums.md#enum-breakintorocks) | Enum | Specifies the type of rock (e.g., 'Coin', 'SmallRock') to spawn when breaking an inanimate object. | 4 ||
| [`ObjectOnHitCharacter`](#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 4 | SkeletonCatFamiliar |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 ||
| [`ApplyToSource`](#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 3 ||
| `Vaporize` | `Number` | Removes the target from play, preventing its corpse from being interacted with. | 3 ||
| `GetAggroTarget` | Integer | The number of aggro targets to acquire. | 2 ||
| `PreventDeathTransforms` | Integer | Number of death transforms prevented for non-boss characters. | 1 ||
| [`Temporary`](#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 1 ||

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
| [`palette`](./Enums.md) | Integer | Specifies the color palette index for the ability's visuals. | 17 | 6 |
| `ear1` | Integer | The catalog ID for the cat's first ear part. | 13 ||
| [`tail`](./Enums.md) | Integer | The catalog ID for the cat's tail part. | 13 | 1042 |
| [`arm2`](./Enums.md) | Number | The catalog ID for the cat's second arm part. | 11 | 1013 |
| `ear2` | Integer | The catalog ID for the cat's second ear part. | 10 ||
| [`arm1`](./Enums.md) | Number | The catalog ID for the cat's first arm part. | 10 | 1013 |
| [`leg1`](./Enums.md) | Integer | The catalog ID for the cat's first leg part. | 8 | 338 |
| [`leg2`](./Enums.md) | Integer | The catalog ID for the cat's second leg part. | 8 | 338 |
| [`mouth`](./Enums.md) | Number | The catalog ID for the cat's mouth part. | 8 | 1005 |
| [`head`](./Enums.md) | Integer | The catalog ID for the cat's head part. | 6 | 12 |
| [`texture`](./Enums.md) | Integer | The catalog ID for the cat's texture. | 6 | 1008 |
| [`body`](./Enums.md) | Number | The catalog ID for the cat's body part. | 5 | 1029 |
| `eye1` | Integer | The catalog ID for the cat's first eye part. | 3 ||
| `eye2` | Integer | The catalog ID for the cat's second eye part. | 3 ||
| `eyebrow1` | Integer | The catalog ID for the cat's first eyebrow part. | 1 ||
| `eyebrow2` | Integer | The catalog ID for the cat's second eyebrow part. | 1 ||

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
| `full_size` | Boolean | If true, the magic missile uses its full size instead of a reduced size. | 2 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||

</details>

---

### Object: `ChangeTile`


**Definition:** Transforms the terrain tile under the target.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tile`](./Enums.md) | Array / Enum | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 12 | [BrambleTile] |
| `aoe` | Integer | The radius (in tiles) of the area affected by the tile change. | 2 ||
| [`chance`](./Enums.md) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | .02 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 ||
| `IgnoreDamage` | `Number` | If set, the target ignores all damage for the duration. | 3 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 ||
| `BonusDamageBasedOnDistance` | `Number` | The flat bonus damage added per tile of distance between the source and target. | 2 ||
| [`Conditional_HealthThreshold`](#object-conditional_healththreshold) | Object | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 2 ||
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 1 ||
| `CapDamage` | `Number` | The maximum amount of damage dealt, capping the total after all modifiers are applied. | 1 ||
| `RandomBonusDamage` | `Number` | The maximum random bonus damage added to the base damage; the actual bonus is a random value between 0 and this number. | 1 ||
| [`Else`](#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 ||
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is pushed away from the source on hit. | 1 | 5 |

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
| `intensity` | Integer | The strength of the screen shake effect; positive values shake more, negative values may invert direction. | 10 ||
| [`time`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Variable | The duration in seconds of the screen shake effect. | 10 ||

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
| [`ability`](./Enums.md) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 11 | MoonHandDrop |
| [`fail_ability`](./Enums.md#enum-fail_ability) | Enum | Specifies the ability to be used when the parent condition (e.g., breaking free) fails. | 3 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 10 ||
| [`Revive`](./Enums.md) | Integer | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 7 | 50 |
| `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 2 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 ||
| [`Conditional_Enemy`](#object-conditional_enemy) | Object | An object containing status effects or actions applied only if the target is an enemy. | 1 ||
| `FlatAIBonus` | `Number` | A flat adjustment to the AI's evaluation score for this action; positive values encourage the AI to use it, negative values discourage it. | 1 ||
| [`HealRandomInjury`](./Enums.md) | Integer | The number of random injuries healed on the target. | 1 | 1 |
| [`PermanentCharm`](./Enums.md) | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 13 ||
| [`StatusOnBattleEnd`](#object-statusonbattleend) | Object | An object containing status effects or passives applied to the unit when the battle ends. | 5 ||
| [`AddTag`](./Enums.md) | Enum | Specifies a gameplay tag (e.g., 'rock', 'plant') to add to the unit, used for interaction checks. | 2 | squirrel |
| [`Flying`](./Enums.md) | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 2 | 1 |
| [`IgnoreTiles`](./Enums.md) | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 2 | 1 |
| [`YOffset`](./Enums.md) | Number | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 2 | .25 |
| [`ElementImmune`](./Enums.md) | Enum | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 1 | Creep |
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit cannot be knocked back. | 1 | 1 |
| [`Plant`](./Enums.md) | Integer | If set to 1, marks the unit as a Plant type, granting associated immunities and interactions. | 1 | 1 |
| [`ReplaceBasicAttack`](./Enums.md) | Enum | Specifies the ability ID that replaces the unit's basic attack. | 1 | BasicPuke |

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
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 |
| [`formula`](./Math_Equations.md) | Equation | A mathematical expression evaluated to determine if its result is positive, enabling the parent conditional. | 8 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 ||
| [`Burn`](./Enums.md) | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 2 | [.1] |
| [`Immobile`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 2 | [.1] |
| [`Shield`](./Enums.md) | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 2 | 2*X |
| [`OverrideKnockbackDamage`](./Engine_LogicKeys.md#valid-property-keys) | `String` | A formula or flat value that sets the damage dealt when knockback occurs, overriding default calculations. | 1 ||
| [`Freeze`](./Enums.md) | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | [.1] |
| [`Slow`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 1 | [.1] |
| [`SpeedUp`](./Enums.md) | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | 4 |
| [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 1 | [0] |

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
| [`pool`](./Enums.md) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 15 | [Ping] |
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 14 ||
| `temporary` | Boolean | If true, the crafted item is temporary and will be removed after the battle or a set duration. | 4 ||
| `works_with_tech` | Boolean | If true, the craft effect is compatible with tech-based interactions or abilities. | 4 ||

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
| [`odds`](./Enums.md#enum-odds) | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 8 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| `DieViolently` | `Number` | If true, causes the target to die with a violent, explosive visual effect. | 1 ||
| `Instakill` | `Number` | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 ||
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 3 ||
| [`TempPassiveWhileHasStatus`](#object-temppassivewhilehasstatus) | Object | An object defining passives temporarily granted to the unit while it has a specific status effect. | 3 ||

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
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 |
| [`ApplyToSource`](#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 3 | [.1] |
| [`LuckUp`](./Enums.md) | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | 2 |

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 7 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 ||
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 5 ||
| [`SpawnThingIfHitKills`](./Engine_LogicKeys.md#valid-property-keys) | `String` | The name of the thing (e.g., a food type) to spawn at the target's location upon a killing blow. | 2 ||
| `threshold_percent` | Integer | The percentage of max health below which the target must be for the conditional to trigger. | 2 ||
| [`ApplyToSource`](#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 1 ||
| [`BonusDamage`](./Engine_LogicKeys.md#valid-property-keys) | `String` | The amount of flat bonus damage added (negative values reduce damage). | 1 ||
| `CaptureFamiliar` | `Number` | The number of times to attempt to capture the target as a familiar. | 1 ||
| `Die` | `Number` | If set, kills the target immediately. | 1 ||
| `DieViolently` | `Number` | If true, causes the target to die with a violent, explosive visual effect. | 1 ||
| `FactionConversion` | `Number` | Converts the target to the caster's faction. | 1 ||
| `FlatLeech` | `Number` | The flat amount of health restored to the source when dealing damage, applied after the hit. | 1 ||
| `FullHeal` | `Number` | If non-zero, fully restores the target's health. | 1 ||
| `Instakill` | `Number` | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 1 ||
| [`threshold_expr`](./Math_Equations.md) | Equation | A mathematical expression whose result is used as the dynamic health threshold for the conditional. | 1 ||
| `Vaporize` | `Number` | Removes the target from play, preventing its corpse from being interacted with. | 1 ||

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
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 7 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 7 ||
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | `String` | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 5 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`ForceImmediateMoveAndAttack`](#object-forceimmediatemoveandattack) | Object | An object that forces the unit to instantly move toward the target and perform a specified ability attack. | 1 ||
| [`UseAbility`](./Abilities_and_Spells.md#object-useability) | `String` | The name of the ability the target is forced to use. | 1 ||
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 1 | 2 |
| [`DamageUp`](./Enums.md) | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | 3 |
| [`DodgeChance_Status`](./Enums.md) | Integer | The flat percentage increase to dodge chance applied as a status effect. | 1 | 50 |
| [`SpeedUp`](./Enums.md) | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | 4 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 ||
| `ConjureRandomAbilityFromCat` | `Number` | The number of random abilities created or given to the cat unit from a pool of cat-themed abilities. | 2 ||
| [`ApplyToSource`](#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 1 ||
| `GenericDebuff` | `Number` | The number of stacks of a generic, untooltipped debuff applied to the target. | 1 ||
| [`KnockOutClone`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the ability ID used to knock out or remove the player's clone unit from battle. | 1 ||
| `T2CopyCat` | `Number` | The number of T2 Clone copies created or applied to the target cat. | 1 ||
| [`Adrenaline`](./Enums.md) | Integer | The flat amount of Adrenaline (a resource or stat) granted to the unit. | 1 | 10 |
| [`Cleanse`](./Enums.md) | Integer | The number of stacks of negative status effects removed from the target. | 1 | 0 |
| [`Scrambled`](./Enums.md) | Integer | The number of stacks of Scrambled applied. | 1 | 2 |

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
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 2 ||

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 7 ||
| [`ability`](./Enums.md) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 7 | MoonHandDrop |

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
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [`Conditional_HasTag`](#object-conditional_hastag) | Object | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 3 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 ||
| [`Else`](#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`CanApplyToInanimate`](#object-canapplytoinanimate) | Object | An object containing effects that can be applied to inanimate objects. | 1 ||
| [`RepairWeapon`](./Enums.md) | Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 1 | 99 |

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
| `intensity` | Integer | The strength of the screen shake effect; positive values shake more, negative values may invert direction. | 6 ||
| `radius` | Array / Integer | The range in tiles of the distortion ring effect; an array [min, max] specifies a random radius within that range. | 6 ||
| [`speed`](./Enums.md) | Array / Number | The speed of the projectile or move, can be a value or a range. | 6 | [1.0] |

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| [`banned_abilities`](./Arrays.md#array-banned_abilities) | Array | A list of ability IDs that are excluded from random selection or usage in the Metronome effect. | 1 ||

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
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | Specifies the music layer to switch to (e.g., 'event', 'battle', 'map'). | 7 ||
| [`new_song`](./Enums.md#enum-new_song) | Enum | Specifies the song to switch to; 'same' keeps the current song playing on the new layer. | 6 ||
| `crossfade_speed` | Integer | The duration in seconds for the crossfade transition between music tracks. | 1 ||

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
| [`damage`](./Abilities_and_Spells.md#object-damage) | Variable | Specifies the amount of damage dealt, can be a number or expression. | 6 ||
| `max_dist` | Integer | The maximum distance in tiles the target can be displaced by the knockback effect. | 6 ||
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 2 ||
| [`exclude_prefix`](./Enums.md#enum-exclude_prefix) | Enum | Specifies a prefix string; units with a matching prefix in their ID are excluded from the displacement effect. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`Tech`](./Enums.md) | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | 3 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |
| `CurrentWeaponAddPoison` | Integer | The number of poison stacks added to the target's current weapon; an integer value applies that many stacks. | 1 ||
| [`LuckUp`](./Enums.md) | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | 2 |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | 1 |
| [`RandomStatUp`](./Enums.md) | Enum / Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | ceil(X/3) |
| [`Shield`](./Enums.md) | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 1 | 2*X |

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | |

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
| [`damage`](#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 ||

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
| [`damage`](#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 7 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 7 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 7 ||
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum | Specifies whether the damage effect applies to tiles; 'all' damages every tile in the area. | 4 ||
| [`effects`](#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 4 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 2 ||

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
| `DeleteObject` | `Number` | If set, deletes the target object from the map. | 3 ||
| `Die` | `Number` | If set, kills the target immediately. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 4 ||
| `max_distance` | Integer | The maximum range in tiles for the arc lightning to chain to subsequent targets. | 4 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 ||
| `ignore_self` | Boolean | If true, the arc lightning effect does not chain to or affect the source unit itself. | 1 ||
| [`chance`](./Enums.md) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | .02 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`DamageUp`](./Enums.md) | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | 3 |
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | 2 |
| [`BonusDamage`](./Enums.md) | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 1 | -4 |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 3 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 ||
| [`CompleteItemQuest`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the item quest ID to mark as complete on kill. | 2 ||
| `TriggerGameEnding` | `Number` | If set to 1, triggers the game's ending sequence; 0 disables it. | 2 ||

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
| `odds` | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 4 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 ||
| [`ApplyPassives`](#object-applypassives) | Object | Specifies the passives or status effects to apply to the unit. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |
| [`Burn`](./Enums.md) | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | [.1] |
| [`Poison`](./Enums.md) | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | [.1] |
| [`Tarred`](./Enums.md) | Array / Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 1 | [.1] |

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
| `max` | Integer | The maximum amount of coins that can be gained. | 11 ||
| `min` | Integer | The minimum amount of coins that will be gained. | 11 ||

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 ||
| [`DoDamage`](#object-dodamage) | Object | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 2 ||
| [`EnterMount`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the mount status to apply to the unit. | 1 ||
| [`VisualFXTile`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the visual effect to play on the target tile. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||

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
| `slot` | Enum / Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 4 ||
| [`ability`](./Enums.md) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 | MoonHandDrop |

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
| `revive_health` | Integer | The amount of health (as a flat integer or percentage) the unit revives with. | 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`Shield`](./Enums.md) | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 3 | 2*X |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | 2 |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`radius`](./Arrays.md#array-radius) | Array / Integer | The range in tiles of the distortion ring effect; an array [min, max] specifies a random radius within that range. | 4 ||
| [`speed`](./Enums.md) | Array / Number | The speed of the projectile or move, can be a value or a range. | 4 | [1.0] |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
| [`Madness`](#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 3 | [.1] |
| [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | [0] |
| [`TempNoManaRegen`](./Enums.md) | Integer | The number of turns the unit cannot regenerate mana. | 2 | 1 |
| [`Confusion`](./Enums.md) | Array / Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | [.1] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 3 ||
| [`MeleeRevengeDamage`](#object-meleerevengedamage) | Object | Defines the damage and effects applied back to a melee attacker upon being hit. | 2 ||
| [`AddManaRegen`](./Enums.md) | Integer | The flat amount of mana regenerated per turn. | 1 | 5 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | 2 |
| [`ReplaceSpell`](#object-replacespell) | Object | Defines which spell slot to replace and with which ability. | 1 ||

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
| [`delay`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Variable | The delay in seconds before the ability's effect triggers. | 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`SwitchMusic`](#object-switchmusic) | Object | Defines a new song or layer for the background music. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 ||
| [`DoScreenShake`](#object-doscreenshake) | Integer / Object | If an integer, the number of screen shakes; if an object, defines the duration and intensity of the screen shake. | 1 ||
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | `String` | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 1 ||
| `FullHeal` | `Number` | If non-zero, fully restores the target's health. | 1 ||
| [`GlobalSpawnCharacter`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of a character to spawn globally. | 1 ||
| `PlayBackground` | `Number` | Specifies the background index to play. | 1 ||
| `Vaporize` | `Number` | Removes the target from play, preventing its corpse from being interacted with. | 1 ||
| [`Cleanse`](./Enums.md) | Integer | The number of stacks of negative status effects removed from the target. | 1 | 0 |
| [`CreateGlobalModifiers`](#object-createglobalmodifiers) | Object | Defines global gameplay modifiers to activate. | 1 ||
| [`RemoveAmbientLightEffects`](./Enums.md) | Number | The fade-out duration in seconds for ambient light effects. | 1 | .5 |

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
| [`stacks`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`RandomStatusFromPool`](#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 3 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

</details>

---

### Object: `BounceObject`


**Definition:** Spawns a physics object that visually bounces off the target.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`obj`](./Enums.md#enum-obj) | Array / Enum | Specifies one or more object names to bounce towards the target. | 3 ||
| [`chance`](./Enums.md) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | .02 |
| `slide` | Integer | The number of tiles the bounced object slides toward the target. | 1 ||

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
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`BonusCritChance`](./Enums.md) | Integer | The flat percentage increase to critical hit chance. | 2 | 100 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 ||
| [`Burn`](./Enums.md) | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | [.1] |
| [`Conditional_Speculative`](#object-conditional_speculative) | Object | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 1 ||

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
| [`KnockUpAndAway`](#object-knockupandaway) | Object | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 ||
| `BonusDamage` | `Number` | The amount of flat bonus damage added (negative values reduce damage). | 1 ||
| [`DelayCastAbility`](./Abilities_and_Spells.md#object-delaycastability) | `String` | Specifies the name of an ability to cast after a delay. | 1 ||
| [`Bruise`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 1 | [.1] |

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
| `change` | Integer | The amount to adjust the auxiliary counter by. | 3 ||
| `max` | Integer | The maximum amount of coins that can be gained. | 3 ||

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
| [`weights`](./Arrays.md#array-weights) | Array / Enum | Specifies the weight array or named preset for the crazy eye background AI. | 3 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 52 ||
| `even_if_dead` | Boolean | If true, the effect triggers even if the unit is dead. | 25 ||
| [`RandomMutation`](./Enums.md) | Integer | The number of random mutations to apply. | 9 | 3 |
| [`RandomTaggedMutation`](./Enums.md) | Enum | Specifies the tag to filter random mutations by. | 2 | bird |

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
| [`alt_art`](./Enums.md#enum-alt_art) | Enum | Specifies an alternative art asset name to use for the status. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 205 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 56 |
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 30 | [.1] |
| [`Bruise`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 12 | [.1] |

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
| `skilltemp` | Boolean | If true, the afterimage is treated as a skill temporary effect. | 2 ||
| [`object`](./Enums.md) | Array / Enum | Specifies the object or unit to be spawned. | 2 | [TallSkeletonCat] |

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
| [`GainDisorderFromPool_PostCast`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the pool of disorders the unit can gain after the spell is cast. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 ||

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
| [`ObjectOnHit`](./Abilities_and_Spells.md#object-objectonhit) | `String` | Specifies the object to spawn on the hit tile. | 2 ||
| `SpawnBearTrap` | `Number` | If non-zero, spawns a bear trap on the tile. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [`ability`](./Enums.md) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 9 | MoonHandDrop |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 6 ||

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||
| [`ability`](./Enums.md) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | MoonHandDrop |

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | |

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`Conditional_InForm`](#object-conditional_inform) | Object | Contains effects that apply only if the target is in the specified form. | 1 ||
| [`Consumed`](#object-consumed) | Object | An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`. | 1 ||
| [`Else`](#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 ||

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
| [`ApplyToTile`](#object-applytotile) | Object | Defines effects to apply to the target tile. | 2 ||
| `VaporizeCorpse` | `Number` | If set, vaporizes the target's corpse, preventing revival. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 |
| [`LaunchOffScreen`](./Enums.md) | String | A formula string that determines the knockback force to launch the unit off-screen. | 1 | 10+bonus_melee_ability_damage |
| [`LaunchOffScreenInstakill`](./Enums.md) | Integer | If non-zero, the unit is instantly killed and launched off-screen. | 1 | 1 |
| [`TempInitiativeChange`](./Enums.md) | Integer | The flat change to the unit's initiative value. | 1 | -100 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 ||
| `GenericBuff` | `Number` | A generic buff value applied to the unit. | 1 ||
| [`RandomStatusFromPool`](#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 1 ||
| [`PartialCleanse`](./Enums.md) | Integer | The number of stacks of temporary status effects to remove from the target. | 1 | 9999 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`Confusion`](./Enums.md) | Array / Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | [.1] |
| [`Temporary`](#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is pushed away from the source on hit. | 2 | 5 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | |

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
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 2 ||
| [`ability`](./Enums.md) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | MoonHandDrop |

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 1 ||

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
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | Inherits game-wide rule modifiers. You can utilize any key from the Engine Global Modifier Keys list here to alter overarching game mechanics (e.g., changing gravity or stamina costs). | 5 ||
| [`LowerAmbientLight`](#object-lowerambientlight) | Object | If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly. | 3 ||
| [`BloodRain`](./Enums.md) | Integer | If non-zero, enables the blood rain visual effect. | 3 | 1 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 |

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
| [`effects`](#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 2 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 2 ||

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| [`chance`](./Enums.md) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | .02 |

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
| [`amount`](./Arrays.md#array-amount) | Array | For ambient light, the target brightness value (as a float or percentage array for RGB). | 3 ||
| [`speed`](./Enums.md) | Array / Number | The speed of the projectile or move, can be a value or a range. | 3 | [1.0] |

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | [0] |
| [`ApplyToSource`](#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 70 ||
| [`effects`](#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 47 ||

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
| `crit_multiplier_bonus` | Integer | The additional critical hit damage multiplier. | 1 ||
| `extra_coins_per_stack` | Integer | The number of extra coins gained per stack of the associated status. | 1 ||
| `luck_increase` | Integer | The flat increase to the unit's luck stat. | 1 ||

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
| [`self_damage`](#object-self_damage) | Object | Defines damage or effects applied to the caster when using the ability. | 2 ||
| [`damage_instance`](#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`splash_damage`](#object-splash_damage) | Object | Defines additional damage or effects applied to nearby targets around the primary target. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| `stack_scale` | Integer | The scaling factor for how many stacks of the over-heal status are applied. | 1 ||
| [`RandomStatUp`](./Enums.md) | Enum / Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | ceil(X/3) |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the source. | 1 | 1 |

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
| `radius` | Array / Integer | The range in tiles of the distortion ring effect; an array [min, max] specifies a random radius within that range. | 2 ||
| [`chance`](./Enums.md) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | .02 |

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
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

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
| `max` | Integer | The maximum amount of coins that can be gained. | 2 ||
| `min` | Integer | The minimum amount of coins that will be gained. | 2 ||

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
| `stackable` | Boolean | If true, the scatter coins effect can stack with multiple applications. | 2 ||
| [`stacks`](./Math_Equations.md) | Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 1 ||

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
| `include_spells` | Boolean | If true, the AI-controlled bonus turn includes spells as available actions. | 3 ||

</details>

---

### Object: `TeamCastAbility`


**Definition:** Requires or involves multiple characters to execute the ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum | Specifies a tag that the target unit must have for the team cast to trigger. | 2 ||
| [`ability`](./Enums.md) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | MoonHandDrop |
| `same_orientation` | Boolean | If true, the team cast ability only triggers if the caster and target face the same direction. | 1 ||

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
| `reset_percent` | Integer | The percentage of the ramp-up value to reset to upon casting. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`DoubleCastSpellThisTurn`](./Enums.md) | Integer | If non-zero, grants the unit a double cast effect for spells this turn. | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`HideEquipment`](./Enums.md) | Enum | Specifies which equipment slot is visually hidden. | 1 | neck |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | 1 |

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
| `ForceMoveTowards` | `Number` | The number of tiles to force the target to move toward the caster. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [`damage`](#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 ||
| [`effects`](#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1 ||

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
| [`weather`](./Arrays.md#array-weather) | Array | Specifies one or more weather types to check for. | 1 ||
| [`DestroyEquipmentAndAttachParasite`](#object-destroyequipmentandattachparasite) | Object | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

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
| `BonusCritChance` | `Number` | The flat percentage increase to critical hit chance. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`Fear`](./Enums.md) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | [.3] |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | |

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
| `odds` | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 1 ||
| [`DestroyEquipmentAndAttachParasite`](#object-destroyequipmentandattachparasite) | Object | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`Imprison`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the type of unit or object to summon as a prison. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| `SetKnockback` | `Number` | The knockback distance to set for the damage instance, overriding default. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 ||
| [`TempPassiveWhileHasStatus`](#object-temppassivewhilehasstatus) | Object | An object defining passives temporarily granted to the unit while it has a specific status effect. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`ApplyToSource`](#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 1 ||
| [`Consumed`](#object-consumed) | Object | An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`. | 1 ||

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
| `DisplaceTowardsSource` | `Number` | If set, displaces the target towards the source of the effect. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`ApplyToSource`](#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 1 ||
| [`ScatterCoins`](#object-scattercoins) | Object | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 1 ||
| [`tag`](./Enums.md) | Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | megadino |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`Bruise`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 1 | [.1] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| `heaviestMelee` | Integer | The minimum damage value to trigger the heaviest melee hit animation. | 1 ||
| `heavyMelee` | Integer | The minimum damage value to trigger a heavy melee hit animation. | 1 ||

</details>

---


<details>
<summary><b>ApplyToOthersWithSharedTagAndFaction</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>ApplyToRandomPartyMemberIfPossible</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>Conditional_BossOrBig</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>Conditional_CanBeHealed</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>Conditional_DebuffRoll</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>Conditional_DestructibleCorpse</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>Conditional_Displaceable</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>Conditional_FinishedSpawning</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>Conditional_FormulaIsPositive</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>Conditional_IsSelf</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>Conditional_IsTrample</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>Conditional_NotBig</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>Conditional_NotBoss</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>Conditional_NotBossOrBig</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>Conditional_OncePerBattle</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>Conditional_Shielded</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>LateStatusApplication</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>PassiveWhileNotTakingTurn</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>StatusKillers</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>XIsTargetHealth</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

### Object: `DelayCastAbility`


**Definition:** Queues an ability to be cast automatically after a certain delay or trigger.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `lingering` | Boolean | If true, the ability effect lingers after the initial cast. | 1 ||
| `relative` | Boolean | If true, the delay is calculated relative to the current turn count rather than as an absolute time. | 1 ||
| [`ability`](./Enums.md) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | MoonHandDrop |

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
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 2 ||
| [`damage`](#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 ||

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
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum | Determines the ability used when the Dybbuk possession ends. | 1 ||
| [`punch_self_ability`](./Enums.md#enum-punch_self_ability) | Enum | Determines the ability used for the possessed unit to attack itself. | 1 ||

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
| `even_if_cant_reach` | Boolean | If true, forces the unit to attempt to move and attack even if the target is not reachable. | 1 ||
| [`ability`](./Enums.md) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | MoonHandDrop |

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
| `change` | Integer | The amount to adjust the auxiliary counter by. | 1 ||
| `max` | Integer | The maximum amount of coins that can be gained. | 1 ||

</details>

---

### Object: `Madness`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| `tickdown_this_turn` | Boolean | If true, madness stacks decrease at the start of this turn instead of the next. | 1 ||

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
| `can_instapop` | `Boolean` | If false, the ability cannot instantly kill or remove the target, often used for non-lethal effects. | 1 ||
| `force_no_hit_animation` | Boolean | If true, suppresses the hit animation when merging damage instances. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1 ||

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
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target regardless of accuracy or evasion. | 1 ||
| `piercing` | `Boolean` | If true, the damage instance ignores armor or damage reduction effects on the target. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1 ||

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
| `MadnessChanceOnTurnBegin` | `Number` | The chance (as a multiplier) to inflict Madness status at the start of each turn in the next battle. | 1 ||
| [`fights`](./Enums.md) | Integer | The number of future battles the status effect will be applied at the start of. | 1 | 9999 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [`object`](./Enums.md) | Array / Enum | Specifies the object or unit to be spawned. | 2 | [TallSkeletonCat] |
| `clone_items` | Boolean | If true, the spawned unit clones the items of the original unit. | 1 ||
| `clone_referenced_catdata` | Boolean | If true, the spawned unit is a clone of the referenced cat data, including its stats and equipment. | 1 ||
| `no_splatter` | Boolean | If true, prevents the blood splatter visual effect from appearing when the object spawns or is popped. | 1 ||

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 4 ||

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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 31 ||
| [`effects`](#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 29 ||

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
| `permanent` | Boolean | If true, the scrambled spell selection persists permanently rather than resetting after use. | 1 ||

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
| [`dying`](./Enums.md#enum-dying) | Enum | Determines the animation set used when the unit is in a dying state. | 1 ||
| [`dead`](./Enums.md) | Enum | Determines the animation set used when the unit is dead. | 1 | deadShot |

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| [`style`](./Arrays.md#array-style) | Array | Specifies the visual styles (e.g., crit) used for the fake damage display. | 1 ||

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
| [`disease`](./Enums.md#enum-disease) | Enum | Determines which disease is applied when spreading disease. | 13 ||
| [`chance`](./Enums.md) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 12 | .02 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |
| [`DamageOrHealConditionally`](./Enums.md) | Integer | The amount of conditional damage or healing applied, based on certain conditions (e.g., ally or enemy). | 1 | 1 |
| [`Freeze`](./Enums.md) | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | [.1] |

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
| [`from`](./Enums.md#enum-from) | Enum | Specifies the source equipment item to be transformed. | 1 ||
| [`to`](./Enums.md#enum-to) | Enum | Specifies the target equipment item after transformation. | 1 ||

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
| [`from`](./Enums.md#enum-from) | Enum | Specifies the source equipment item to be transformed. | 2 ||
| [`to`](./Enums.md#enum-to) | Enum | Specifies the target equipment item after transformation. | 2 ||

</details>

---

### Object: `UseAbility`


**Definition:** Forces the character or target to instantly use a specified ability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `respect_prime` | Boolean | If true, the ability will only be used if the unit is primed for it. | 2 ||
| [`ability`](./Enums.md) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | MoonHandDrop |

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
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||
| [`ability`](./Enums.md) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | MoonHandDrop |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`ForceUseAbility`](./Enums.md) | Enum | The name of the ability the source is forced to use, optionally with a chance. | 1 | MotherTumorGrow |

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
| [`cWaggle`](#object-cwaggle) | Object | Defines a clone variant of the Waggle unit with its own graphics and properties. | 1 ||
| [`cWaggle2x2`](#object-cwaggle2x2) | Object | Defines a larger 2x2 tile clone variant of the Waggle unit. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| [`cWaggle3x3`](#object-cwaggle3x3) | Object | Defines an even larger 3x3 tile clone variant of the Waggle unit. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1695 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 750 ||
| [`FormChange`](#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 102 ||
| [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 98 | [0] |
| [`Burn`](./Enums.md) | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 85 | [.1] |
| [`Bruise`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 79 | [.1] |
| `IgnoreSelf` | `Number` | If set to 1 or true, the damage instance ignores the source unit (does not affect itself). | 75 ||
| [`Poison`](./Enums.md) | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 67 | [.1] |
| [`ChangeTile`](./Abilities_and_Spells.md#object-changetile) | `String` | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 62 ||
| [`Else`](#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 59 ||
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 54 | [.1] |
| [`Shield`](./Enums.md) | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 49 | 2*X |
| [`Cleanse`](./Enums.md) | Integer | The number of stacks of negative status effects removed from the target. | 44 | 0 |
| [`Confusion`](./Enums.md) | Array / Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 37 | [.1] |
| [`Conditional_HasTag`](#object-conditional_hastag) | Object | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 36 ||
| [`Conditional_Enemy`](#object-conditional_enemy) | Object | An object containing status effects or actions applied only if the target is an enemy. | 35 ||
| [`VisualFXTile`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the visual effect to play on the target tile. | 34 ||
| [`SpeedUp`](./Enums.md) | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 34 | 4 |
| [`Fear`](./Enums.md) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 31 | [.3] |
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 29 | 2 |
| [`Slow`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 29 | [.1] |
| [`TransformAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the ability that replaces the current ability. | 28 ||
| [`DamageUp`](./Enums.md) | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 28 | 3 |
| [`ApplyToSource`](#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 27 ||
| [`BounceObject`](./Abilities_and_Spells.md#object-bounceobject) | `String` | Specifies the object or projectile to spawn and bounce from the target. | 26 ||
| [`Temporary`](#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 26 ||
| [`ManaGain`](./Engine_LogicKeys.md#valid-property-keys) | Enum / Integer | The amount of mana restored to the source, which can be an expression. | 26 ||
| [`Conditional_Ally`](#object-conditional_ally) | Object | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 25 ||
| [`Blind`](./Enums.md) | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 24 | [2] |
| [`Immobile`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 24 | [.1] |
| [`Weakness`](./Enums.md) | Array / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 23 | [.1] |
| [`Charmed`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 22 | [.1] |
| [`ConstitutionUp`](./Enums.md) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 22 | [.5] |
| [`Leech`](./Enums.md) | Integer | The amount of health leeched from the target (heals the attacker). | 22 | 1 |
| [`StrengthUp`](./Enums.md) | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 22 | max(int, 0) |
| [`EvolveAbilityFromPool`](./Abilities_and_Spells.md#object-evolveabilityfrompool) | `String` | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 21 ||
| `Vaporize` | `Number` | Removes the target from play, preventing its corpse from being interacted with. | 21 ||
| [`IntelligenceUp`](./Enums.md) | Enum / Integer | The amount of Intelligence added as a flat bonus. | 21 | item_aux |
| [`Freeze`](./Enums.md) | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. | 19 | [.1] |
| [`Madness`](#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 19 | [.1] |
| [`Sleep`](./Enums.md) | Array / Integer | The amount of sleep stacks applied, or an [stacks, probability] array. | 19 | [.1] |
| `CollectsPickups` | `Number` | If set to 1 or greater, the unit collects pickups (e.g., items) on contact. | 17 ||
| [`KnockUpAndAway`](#object-knockupandaway) | Object | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 17 ||
| [`Brace`](./Enums.md) | Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 17 | 2 |
| `OverrideKnockbackDamage` | `Number` | A formula or flat value that sets the damage dealt when knockback occurs, overriding default calculations. | 16 ||
| [`Consumed`](#object-consumed) | Object | An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`. | 15 ||
| `VaporizeCorpse` | `Number` | If set, vaporizes the target's corpse, preventing revival. | 15 ||
| [`Petrify`](./Enums.md) | Array / Integer | The amount of petrify stacks applied, or an [stacks, probability] array. | 15 | [.15] |
| [`RandomStatUp`](./Enums.md) | Enum / Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 15 | ceil(X/3) |
| [`ChangeCatClass`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the new class to assign to the unit. | 14 ||
| [`Conditional_GoodRoll`](#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 14 ||
| `EndTurn` | `Number` | If set to 1, ends the current unit's turn immediately after this effect. | 14 ||
| `FaceAway` | `Number` | If set, forces the target to face away from the source. | 14 ||
| [`RandomStatusFromPool`](#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 14 ||
| `RefreshMovePoints` | `Number` | The amount of movement points restored to the source. | 14 ||
| `TakeExtraTurn` | `Number` | The number of extra turns granted to the source. | 14 ||
| [`TransformBasicAttack`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the ability that replaces the unit's basic attack. | 14 ||
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 14 | 2 |
| [`Leeches`](./Enums.md) | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 14 | 2 |
| [`CatPartsTransform`](#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 13 ||
| [`Conditional_Boss`](#object-conditional_boss) | Object | Contains effects that apply only if the target is a boss enemy. | 13 ||
| `GenericDebuff` | `Number` | The number of stacks of a generic, untooltipped debuff applied to the target. | 13 ||
| `Displace` | `Number` | If set to 1, the unit is displaced to another location (e.g., teleport). | 12 ||
| [`Cleave`](#object-cleave) | Integer / Object | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 12 | 1 |
| [`LuckUp`](./Enums.md) | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 12 | 2 |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 12 | 2 |
| [`ApplyToSourceOnKill`](#object-applytosourceonkill) | Object | Contains effects that are applied to the source when it kills the target. | 11 ||
| [`ChanceToBreakFree`](#object-chancetobreakfree) | Object | Defines the chance and ability used for a grappled or restrained unit to break free. | 11 ||
| [`DoScreenShake`](#object-doscreenshake) | Integer / Object | If an integer, the number of screen shakes; if an object, defines the duration and intensity of the screen shake. | 11 ||
| `FullHeal` | Integer | If non-zero, fully restores the target's health. | 11 ||
| [`Conditional_Speculative`](#object-conditional_speculative) | Object | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 10 ||
| `RefreshActPoints` | `Number` | The amount of action points restored to the source. | 10 ||
| [`VisualFX`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the visual effect to play. | 10 ||
| [`DexterityUp`](./Enums.md) | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. | 10 | 2 |
| `PurgeAll` | `Number` | If non-zero, removes all temporary status effects (buffs, debuffs) from the target. | 9 ||
| [`ApplyPassives`](#object-applypassives) | Object | Specifies the passives or status effects to apply to the unit. | 9 ||
| `DeferVaporize` | `Number` | If set to 1, the unit's vaporize (instant death) is delayed until the end of the current action. | 9 ||
| `SpawnCreep` | `Number` | If set to 1, spawns a creep tile under the target. | 9 ||
| [`MagicWeakness`](./Enums.md) | Array / Integer | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 9 | [.1] |
| [`Marked`](./Enums.md) | Array / Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 9 | [.1] |
| [`RandomMagicMissile`](#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, or an object defining its properties. | 9 | 5 |
| [`Conditional_FormulaIsPositive`](#object-conditional_formulaispositive) | Object | Defines effects that apply only if a given formula evaluates to a positive value. | 8 ||
| [`CanApplyToInanimate`](#object-canapplytoinanimate) | Object | An object containing effects that can be applied to inanimate objects. | 8 ||
| `ChanceToBreak` | Integer | Specifies the percentage chance that the item breaks on use. | 8 ||
| `OverrideChainKnockback` | `Number` | The custom number of tiles for chain knockback, overriding the default. | 8 ||
| [`SpreadDisease`](#object-spreaddisease) | Object | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 8 ||
| [`Ammo`](./Enums.md) | Integer | The amount of ammo to add or remove (negative values subtract). | 8 | -1 |
| [`Grappled`](./Enums.md) | Integer | The number of stacks and probability of applying the Grappled status, in format [stacks, probability] or just stacks. | 8 | 1 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 8 | 2 |
| [`ApplyStatusIfCrit`](#object-applystatusifcrit) | Object | Defines effects that are applied only when the attack scores a critical hit. | 7 ||
| `BramblesOnHit` | `Number` | If set to 1, spawns bramble tiles on the target's location on hit. | 7 ||
| `ContextualHeal` | `Number` | The amount of healing applied contextually (e.g., to allies). | 7 ||
| `ForceAttack` | `Number` | If set to 1, forces the target to perform an attack against a random or specified target. | 7 ||
| `Instakill` | `Number` | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 7 ||
| `KnockbackDamageImmuneUntilSettled` | `Number` | If non-zero, makes the target immune to damage from knockback until they stop moving. | 7 ||
| `ManaSteal` | `Number` | The amount of mana stolen (negative values may drain instead). | 7 ||
| [`TriggerWerewolfTransform`](./Engine_LogicKeys.md#valid-property-keys) | `Array` | The number of stacks and probability of triggering the werewolf transformation. | 7 ||
| [`AlphaCat`](./Enums.md) | Integer | The number of AlphaCat stacks applied to the source on kill. | 7 | 1 |
| [`Rot`](./Enums.md) | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 7 | [.1] |
| [`Tarred`](./Enums.md) | Array / Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 7 | [.1] |
| [`Tech`](./Enums.md) | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 7 | 3 |
| [`TempRangeUp`](./Enums.md) | Integer | The amount of temporary range increase applied. | 7 | 2 |
| `ClearStarving` | `Number` | The number of stacks of Starving cleared. | 6 ||
| [`Conditional_Corpse`](#object-conditional_corpse) | Object | Contains an inner effect block that only executes if the target is a corpse. | 6 ||
| [`ConjureBonusAbility`](./Abilities_and_Spells.md#object-conjurebonusability) | `String` | Specifies the name of the bonus ability to conjure. | 6 ||
| [`Craft`](#object-craft) | Object | Specifies the loot pool and slot to craft an item for the source. | 6 ||
| [`DoDistortionRing`](#object-dodistortionring) | Object | Configuration for a distortion ring visual effect, with speed, intensity, and radius. | 6 ||
| `Metronome` | `Number` | The number of times Metronome triggers, or an object with stacks and banned abilities. | 6 ||
| `SetDistanceDisplace` | `Number` | The fixed distance to displace the target. | 6 ||
| `SetHealth` | `Number` | Sets the target's health to a specific flat value or percentage. | 6 ||
| [`TeamCastAbility`](./Abilities_and_Spells.md#object-teamcastability) | `String` | Specifies the ability name for the team to cast, with optional tag restriction and same orientation. | 6 ||
| [`TwisterDisplaceWithDamage`](#object-twisterdisplacewithdamage) | Object | Configuration for a twister displacement that deals damage, with min/max distance and damage value. | 6 ||
| [`BounceRock`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the rock object to bounce. | 6 ||
| [`BackflipWhenTargeted`](#object-backflipwhentargeted) | Integer / Object | The number of backflip charges, or an object defining its ability. | 6 | 2 |
| [`CharismaUp`](./Enums.md) | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. | 6 | -2 |
| [`ObjectOnHitCharacter`](#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 6 | SkeletonCatFamiliar |
| [`RandomInjury`](./Enums.md) | Integer | The number of random injuries applied. | 6 | 1 |
| [`SpiderInfested`](./Enums.md) | Integer | The number of spider infestation stacks applied. | 6 | 2 |
| [`CollectsPickupsWithAltEffects`](#object-collectspickupswithalteffects) | Object | Contains alternative effects that are applied when collecting pickups. | 5 ||
| [`Conditional_HasStatus`](#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 5 ||
| [`Conditional_NotBoss`](#object-conditional_notboss) | Object | Contains effects that apply only if the target is not a boss enemy. | 5 ||
| [`Conditional_Object`](#object-conditional_object) | Object | Evaluates whether the target is an object (vs a character); if true, applies the effects within; otherwise, runs the Else block. | 5 ||
| [`Conditional_PlayerCat`](#object-conditional_playercat) | Object | Defines effects that only apply if the target is a player-controlled cat. | 5 ||
| `FillMana` | `Number` | The amount of mana restored, or an [amount, probability] array. | 5 ||
| `FlatLeech` | `Number` | The flat amount of health restored to the source when dealing damage, applied after the hit. | 5 ||
| `ForceMoveAway` | `Number` | The distance to force the target away from the source. | 5 ||
| `ForceMoveTowards` | `Number` | The number of tiles to force the target to move toward the caster. | 5 ||
| `HitExplosion` | `Number` | The radius of the explosion triggered on hit. | 5 ||
| [`Imprison`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the type of unit or object to summon as a prison. | 5 ||
| [`KnockbackDirectionIsFacingDirection`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies how to alter knockback direction relative to the unit's facing: 1 (same), flip (opposite), rotate_right. | 5 ||
| `MonkStanceSwitch` | `Number` | The number of times to switch monk stance. | 5 ||
| [`ObjectOnHit`](./Abilities_and_Spells.md#object-objectonhit) | `String` | Specifies the object to spawn on the hit tile. | 5 ||
| [`ObjectOnHitEmpty`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the object to spawn on hitting an empty cell. | 5 ||
| [`PopAndSpawn`](./Abilities_and_Spells.md#object-popandspawn) | `String` | The object (enemy or entity) to spawn on the target's tile, optionally with visual effects. | 5 ||
| `Purge` | `Number` | The number of status effects to purge from the target. | 5 ||
| `RefreshMovePointsIfHit` | `Number` | The amount of movement points restored on hit. | 5 ||
| `SafeDie` | `Number` | The number of times the unit can survive a fatal hit. | 5 ||
| `SpawnBearTrap` | `Number` | If non-zero, spawns a bear trap on the tile. | 5 ||
| `SpawnRock` | `Number` | The number of rocks to spawn, or an array with stacks and probability. | 5 ||
| [`DodgeChance_Status`](./Enums.md) | Integer | The flat percentage increase to dodge chance applied as a status effect. | 5 | 50 |
| [`Drowsy`](./Enums.md) | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. | 5 | 8 |
| [`MovementUp`](./Enums.md) | Integer | The amount of movement increase or decrease applied. | 5 | -2 |
| [`Revive`](./Enums.md) | Integer | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 5 | 50 |
| [`SoulLink`](./Enums.md) | Integer | The number of soul link stacks applied. | 5 | 1 |
| [`Stealth`](./Enums.md) | Integer | The number of stealth stacks applied. | 5 | 2 |
| [`TempDamageUp`](./Enums.md) | Integer | The amount of temporary damage increase applied. | 5 | 2 |
| [`Webbed`](./Enums.md) | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 5 | 1 |
| [`RemoveStatus`](./Engine_LogicKeys.md#valid-property-keys) | `String` | The name of the status effect to remove from the source. | 4 ||
| [`SpawnThingIfHitKills`](./Engine_LogicKeys.md#valid-property-keys) | `String` | The name of the thing (e.g., a food type) to spawn at the target's location upon a killing blow. | 4 ||
| [`ApplyToConsumed`](#object-applytoconsumed) | Object | Container for effects that are applied to the consumed object. | 4 ||
| [`ArcLightning`](#object-arclightning) | Object | Configuration for arc lightning chain, with stacks, chance, max distance, and enemy-only flag. | 4 ||
| [`Conditional_Familiar`](#object-conditional_familiar) | Object | Container for effects applied if the unit has a familiar, with an optional Else block. | 4 ||
| [`EnableWeather`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the weather effect to enable. | 4 ||
| `ExplosionIfHitSomething` | `Number` | The radius of explosion triggered if the attack hits an entity. | 4 ||
| `FaceCamera` | `Number` | If non-zero, forces the character to rotate and face the camera. | 4 ||
| [`LateStatusApplication`](#object-latestatusapplication) | Object | Container for status effects that are applied late after the main effect. | 4 ||
| `RemoveActPoints` | `Number` | The number of action points removed from the target. | 4 ||
| `SendRock` | `Number` | The number of rocks to send as projectiles. | 4 ||
| [`SpecificInjury`](./Engine_LogicKeys.md#valid-property-keys) | `String` | The stat (str, spd, int) to which a specific injury is applied, reducing that stat. | 4 ||
| [`SwitchMusic`](#object-switchmusic) | Object | Defines a new song or layer for the background music. | 4 ||
| [`TakeBonusTurnWithStatus`](#object-takebonusturnwithstatus) | Object | Container for status effects applied when taking a bonus turn. | 4 ||
| [`TimeDelayStatusApplication`](#object-timedelaystatusapplication) | Object | Container for status effects applied after a specified delay. | 4 ||
| [`UseAbility`](./Abilities_and_Spells.md#object-useability) | `String` | The name of the ability the target is forced to use. | 4 ||
| `VaporizeInanimate` | `Number` | If non-zero, instantly destroys inanimate objects (corpses, rocks) as if they were vaporized. | 4 ||
| [`LowerAmbientLight`](#object-lowerambientlight) | Object | If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly. | 4 ||
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 4 | 2 |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 4 | 5 |
| [`Reanimate`](./Enums.md) | Integer | The percentage chance to reanimate the target. | 4 | 50 |
| [`Conditional_InForm`](#object-conditional_inform) | Object | Contains effects that apply only if the target is in the specified form. | 3 ||
| [`CatPartsSizeScaleStatus`](#object-catpartssizescalestatus) | Object | Configures scale multipliers for individual cat body parts (body, arms, mouth). | 3 ||
| [`CollideWithConsumed`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Damage formula for collision with consumed objects, e.g., '4+bonus_melee_damage'. | 3 ||
| [`Conditional_AffectedByElement`](#object-conditional_affectedbyelement) | Object | Container for effects applied if the target is affected by a specified element, with optional Else block. | 3 ||
| [`Conditional_FirstApplicationThisTurn`](#object-conditional_firstapplicationthisturn) | Object | Container for effects applied only on the first application of this ability during the turn. | 3 ||
| [`Conditional_LastHit`](#object-conditional_lasthit) | Object | Container for effects applied only on the final hit of a multi-hit attack, with optional Else block. | 3 ||
| `CorpseVaporizer` | `Number` | The number of corpses vaporized on hit. | 3 ||
| `CurrentWeaponDamageUp` | Integer | The amount of temporary damage increase to the current weapon. | 3 ||
| `DeleteObject` | `Number` | If set, deletes the target object from the map. | 3 ||
| `DestroyTrinket` | `Number` | The number of trinkets destroyed. | 3 ||
| `DestroyWeapon` | `Number` | The number of weapons destroyed. | 3 ||
| `DestroyWeaponThrow` | `Number` | The number of weapons destroyed after being thrown. | 3 ||
| `Die` | `Number` | If set, kills the target immediately. | 3 ||
| `DisplaceTowardsSource` | `Number` | If set, displaces the target towards the source of the effect. | 3 ||
| [`DustOnHit`](#object-dustonhit) | Object | Configuration for a dust object spawned on hit. | 3 ||
| `ForceDisplace` | `Number` | The distance the target is forced to displace. | 3 ||
| `ForceMoveTowardsEnemies` | `Number` | Specifies the ability or distance to force the target to move towards enemies. | 3 ||
| `InstantMaxHealthUp` | `Number` | The amount of permanent maximum health increase. | 3 ||
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 3 ||
| `PlayBackground` | Integer | Specifies the background index to play. | 3 ||
| `PullSourceToTarget` | `Number` | The amount of tiles the source is pulled towards the target after the attack. | 3 ||
| `RefreshWeaponAbility` | `Number` | The number of times the weapon's ability is refreshed. | 3 ||
| `RepairAll` | `Number` | The amount of durability restored to all equipped items. | 3 ||
| `RepairOnKill` | `Number` | The number of charges restored to the ability upon killing a target. | 3 ||
| [`SetCrazyEyeBackgroundWeights`](#object-setcrazyeyebackgroundweights) | Object | An object containing a `weights` array that sets the weighting for which Crazy Eye background variant is displayed. | 3 ||
| [`SpawnCustomTrap`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of a custom trap blueprint to spawn at the target location. | 3 ||
| `SpawnNeutralWebTrapOnMiss` | `Number` | The number of neutral web traps spawned on the tile if the attack misses. | 3 ||
| `VaporizeTarget` | `Number` | If non-zero, instantly destroys the target, leaving no corpse. | 3 ||
| [`DamageOrHealConditionally`](./Enums.md) | Integer | The amount of conditional damage or healing applied, based on certain conditions (e.g., ally or enemy). | 3 | 1 |
| [`Doomed`](./Enums.md) | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 3 | 3 |
| [`ExtraBasicAttacks_Status`](./Enums.md) | Integer | The number of additional basic attacks the unit can perform each turn. | 3 | 1 |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 3 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 3 | 1 |
| [`NextAttackBonusRange`](./Enums.md) | Integer | The added range for the unit's next basic attack. | 3 | 3 |
| [`PermanentConstitution`](./Enums.md) | Integer | The amount of permanent Constitution stat added or removed. | 3 | 2 |
| [`PoisonLace`](./Enums.md) | Enum / Integer | Integer or fractional string (e.g., 'X/3') specifying the duration or intensity of the PoisonLace effect. | 3 | X/3 |
| [`Reflect`](./Enums.md) | Integer | The amount of reflect stacks applied. | 3 | 5 |
| [`ReviveNextRound`](#object-revivenextround) | Integer / Object | The number of revives granted, or an object defining revive properties. | 3 | 2 |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 3 | 3 |
| [`Tangled`](#object-tangled) | Integer / Object | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 3 | 1 |
| [`TempSpeedUp`](./Enums.md) | Enum / Integer | The number of stacks of temporary Speed Up applied to the unit. | 3 | 4 |
| [`TempStrengthUp`](./Enums.md) | Enum | The number of stacks of temporary Strength Up applied to the unit. | 3 | X |
| `PartialPurge` | `Number` | The amount of beneficial status effects removed from the target. | 2 ||
| `UpgradeRandomAbility` | `Number` | The number of random abilities upgraded upon effect. | 2 ||
| [`ApplyMultipleTimes`](#object-applymultipletimes) | Object | An object containing a `stacks` value that specifies how many times the nested effects are applied. | 2 ||
| `AddSpiritBombCharges` | `Number` | The number of charges added to the Spirit Bomb ability. | 2 ||
| `BonusKnockbackDamage` | `Number` | The extra damage dealt per tile of knockback. | 2 ||
| `Bound` | `Number` | The number of stacks of the Bound status effect applied to the target. | 2 ||
| `BurgleCoin` | `Number` | The number of coins stolen from the target, or an array of `[number, probability]`. | 2 ||
| `CancelPrimedAbilities` | `Number` | If non-zero, cancels any primed abilities on the target. | 2 ||
| [`ChangeFaction`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the faction to switch the target to. | 2 ||
| `CharmedForceAttack` | `Number` | If non-zero, forces the charmed target to use its basic attack on a random nearby unit. | 2 ||
| `CollideWithThrowTarget` | `Number` | Determines whether the thrown object collides with the primary target (0 disables collision). | 2 ||
| [`Conditional_BadRoll`](#object-conditional_badroll) | Object | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 2 ||
| [`Conditional_BossOrBig`](#object-conditional_bossorbig) | Object | An object containing effects that are only applied if the target is a boss or large unit. | 2 ||
| [`Conditional_Buddy`](#object-conditional_buddy) | Object | An object containing effects that are only applied if the caster has a buddy (follower) unit. | 2 ||
| [`Conditional_DestructibleCorpse`](#object-conditional_destructiblecorpse) | Object | An object containing effects that are only applied if the corpse is destructible. | 2 ||
| [`Conditional_HealthThreshold`](#object-conditional_healththreshold) | Object | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 2 ||
| [`Conditional_IsSelf`](#object-conditional_isself) | Object | An object containing effects that are only applied if the target is the source unit itself. | 2 ||
| [`Conditional_NotAlly`](#object-conditional_notally) | Object | An object containing effects that are only applied if the target is not an ally of the source. | 2 ||
| [`Conditional_NotBossOrBig`](#object-conditional_notbossorbig) | Object | An object containing effects that are only applied if the target is not a boss or large unit. | 2 ||
| [`Conditional_NotShielded`](#object-conditional_notshielded) | Object | An object containing effects that are only applied if the target does not have a shield active. | 2 ||
| [`Conditional_OncePerBattle`](#object-conditional_onceperbattle) | Object | An object containing effects that can only trigger once per battle, preventing double-activation. | 2 ||
| [`Conditional_Shielded`](#object-conditional_shielded) | Object | An object containing effects that are only applied if the target has a shield active. | 2 ||
| `CopySpells` | `Number` | The number of spells copied from the target, or an object specifying `stacks` and whether the copy is `upgraded`. | 2 ||
| `Counterspell` | `Number` | If non-zero, negates the next incoming enemy spell and triggers the configured counterspell effects. | 2 ||
| `DamageBasedOnMissingHealth` | `Number` | The percentage of the target's missing health dealt as additional damage. | 2 ||
| `DamageDistanceAOEFalloff` | `Number` | The falloff multiplier applied to AoE damage based on distance from the center of the effect. | 2 ||
| `DamageTrinket` | `Number` | The amount of durability damage dealt to the target's equipped trinket. | 2 ||
| `DelayedFury` | `Number` | The percentage of Fury damage that is stored and applied after a delay. | 2 ||
| [`DestroyEquipmentAndAttachParasite`](#object-destroyequipmentandattachparasite) | Object | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 2 ||
| `DieViaAbilityInternally` | `Number` | If non-zero, causes the target to die via an internal ability trigger. | 2 ||
| `DisplaceToOriginalPosition` | `Number` | If non-zero, returns the unit to its original position after the effect resolves. | 2 ||
| `FlowersOnHit` | `Number` | The number of flowers spawned on the tile upon hitting the target. | 2 ||
| `ForceMoveNonAlliesInRangeTowardsTile` | `Number` | The tile range within which non-allied units are forcibly moved towards a specified tile. | 2 ||
| [`ForceMoveTowardsTaggedObject`](#object-forcemovetowardstaggedobject) | Object | An object specifying the `ability` and optional `tag` used to forcibly move the unit towards a tagged object. | 2 ||
| `IgnoreDamage` | `Number` | If set, the target ignores all damage for the duration. | 2 ||
| [`ImmediateUseAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of an ability to be triggered instantly from this effect. | 2 ||
| [`ImmediateUseDirectionalAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of a directional ability to be used immediately by the unit. | 2 ||
| `JohnnyCriesForWashers` | `Number` | The number of washers (currency) requested by the Johnny NPC. | 2 ||
| `LeaveBehindRockOnKnockback` | `Number` | If non-zero, leaves behind a rock on each tile the target is knocked through. | 2 ||
| [`Math`](#object-math) | Object | An object containing a `stacks` value that determines how many times the nested effects are applied. | 2 ||
| `MaxHPUp` | `Number` | The amount of maximum health permanently increased. | 2 ||
| `NextAttackSpecialCrit` | `Number` | The number of charges for a special crit on the next attack, or an object defining its bonus properties. | 2 ||
| [`OverHealToStatuses`](#object-overhealtostatuses) | Object | Specifies a set of statuses applied to the target based on the amount of over-healing dealt. | 2 ||
| `PermanentStrength` | `Number` | The amount of permanent bonus strength (physical damage modifier) granted. | 2 ||
| `PermanentUpgradeRandomActive` | `Number` | The number of random active abilities permanently upgraded. | 2 ||
| `PullSourceToKnockbackImmuneTarget` | `Number` | The amount of pull force applied to the source toward a knockback-immune target. | 2 ||
| [`QuakeAreaChance`](#object-quakeareachance) | Object | An object containing a radius and a chance to trigger a quake area effect. | 2 ||
| `RandomDistanceDisplace` | `Number` | The number of stacks of a random distance displacement effect, or an object with stacks, min_dist, and chance. | 2 ||
| [`RandomKnockback`](#object-randomknockback) | Object | An object defining the minimum and maximum distance in tiles for a random knockback. | 2 ||
| `RebukeDamage` | `Number` | The amount of damage dealt by a rebuke backlash effect. | 2 ||
| `RemoveMovePoints` | `Number` | The number of move points to remove from the target, preventing them from moving. | 2 ||
| `RepairArmorCondition` | `Number` | The amount of armor condition restored. | 2 ||
| `RepairWeaponCondition` | `Number` | The amount of weapon condition restored. | 2 ||
| `ResetArmorShield` | `Number` | The amount of armor shield restored. | 2 ||
| `ScatterHeldCoin` | `Number` | The number of coins scattered, with an optional probability as a second element. | 2 ||
| `ScrambleEverything` | `Number` | The percentage chance to scramble all abilities and passives on the target. | 2 ||
| `SetShield` | `Number` | Sets the target's shield value to a specific flat amount. | 2 ||
| `Shatter` | `Number` | The amount of damage dealt when a frozen or petrified status is shattered, or a template definition for a Shatter ability. | 2 ||
| `SignalFinalBossShieldBroke` | `Number` | If set to a non-zero number, signals that the final boss's shield has been broken. | 2 ||
| `SmartMetronome` | `Number` | The number of stacks of a buff that increases damage by a percentage, with an optional upgrade flag. | 2 ||
| `SpeculativeMoveSelfCorpseOffMap` | `Number` | If true, attempts to remove the character's corpse from the map, used for speculative AI targeting. | 2 ||
| `StanceSwitchToMelee` | `Number` | If set, switches the source to melee stance. | 2 ||
| `SwallowSmallCharacter` | `Number` | The percentage chance to swallow a smaller character on hit. | 2 ||
| [`TakeBonusTurnWithAIControl`](#object-takebonusturnwithaicontrol) | Object | An object configuring whether the bonus turn happens at the end of the round and whether spells are included. | 2 ||
| `TempTrampleUntilSettled` | `Number` | The number of stacks of temporary Trample applied to the source, allowing movement through enemies until the source ends its turn. | 2 ||
| `TradeLife` | `Number` | The amount of health life traded, or a template for a TradeLife ability. | 2 ||
| `TriggerDOTStatuses` | `Number` | If set to 1, triggers damage over time statuses on the target immediately. | 2 ||
| `RandomStatDown` | Array / Integer / String | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 2 ||
| `SelfStun` | `Number` | The number of stacks of self-stun applied, with an optional probability as a second element. | 2 ||
| [`BodyGuard`](#object-bodyguard) | Object | An object that applies a bodyguard status, optionally linking to a swap ability. | 2 ||
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 2 | 2 |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of diminishing health regen stacks applied. | 2 | 3 |
| [`DoubleCastSpell`](./Enums.md) | Integer | The number of times the next spell cast is doubled, or a template with name and tooltip. | 2 | 1 |
| [`DoubleLoot`](./Enums.md) | Integer | The multiplier for loot drops, where 1 or 2 doubles the loot. | 2 | 2 |
| [`FreeSpell`](./Enums.md) | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. | 2 | 2 |
| [`Hex`](./Enums.md) | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. | 2 | 1 |
| [`KnockOutCoin`](#object-knockoutcoin) | Integer / Object | The number of coins knocked out, with an optional probability or an object with stacks and chance. | 2 | 1 |
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is pushed away from the source on hit. | 2 | 5 |
| [`Lifesteal`](./Enums.md) | Integer | The amount of lifesteal stacks applied. | 2 | 3 |
| [`ManaLeeches`](./Enums.md) | Integer | The number of mana leech stacks applied. | 2 | 2 |
| [`Ostracized`](./Enums.md) | Integer | The number of stacks of Ostracized applied. | 2 | 2 |
| [`PartialCleanse`](./Enums.md) | Integer | The number of stacks of temporary status effects to remove from the target. | 2 | 9999 |
| [`Possessed`](./Enums.md) | Integer | The number of possession stacks applied, or a template with name and tooltips. | 2 | 1 |
| [`RangeUp`](./Enums.md) | Integer | The number of stacks of bonus attack range applied. | 2 | 1 |
| [`RepairWeapon`](./Enums.md) | Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 2 | 99 |
| [`SizeScale`](./Enums.md) | Number | The multiplier applied to the unit's visual and hitbox size. | 2 | .6 |
| [`SpawnFlames`](./Enums.md) | Array | An array containing the number of flame tiles to spawn and the chance per tile. | 2 | [.20+.1*level] |
| [`TempCritChanceUp`](./Enums.md) | Integer | The amount of temporary critical hit chance (in percentage points) added. | 2 | 30 |
| [`TempDexterityUp`](./Enums.md) | Enum | The number of temporary dexterity stacks applied, or a string alias like 'X'. | 2 | X |
| [`TempInitiativeChange`](./Enums.md) | Integer | The flat change to the unit's initiative value. | 2 | -100 |
| [`TempMovement`](./Enums.md) | Enum / Integer | The amount of temporary movement range added, or a string alias like 'mov'. | 2 | 20 |
| [`TempSpellDamageUp`](./Enums.md) | Integer | The amount of temporary spell damage increase applied. | 2 | 1 |
| [`TrailBlazer`](./Enums.md) | Enum / Integer | The number of trail blazer stacks applied, or a string alias like 'mov'. | 2 | mov |
| [`Trample`](./Enums.md) | Integer | The amount of bonus damage dealt when moving through an enemy. | 2 | 3 |
| [`DoubleStatus`](./Engine_LogicKeys.md#valid-property-keys) | `String` | The name of a status effect whose stacks are doubled when applied. | 1 ||
| `AIFavorLowHealth` | `Number` | The AI's favorability weight for targeting low-health units. | 1 ||
| `AlliesTakeExtraTurn` | `Number` | The number of extra turns granted to allies. | 1 ||
| [`AlternateIdleAnimation`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of an alternative idle animation to play. | 1 ||
| `ApplyShieldToApplierBasedOnMaxHealth` | `Number` | The amount of shield applied to the applier based on a fraction of their max health. | 1 ||
| [`ApplyStatusesNextTurnBegin`](#object-applystatusesnextturnbegin) | Object | Specifies a set of statuses to apply to the target at the beginning of their next turn. | 1 ||
| [`ApplyToOthersWithSharedTagAndFaction`](#object-applytootherswithsharedtagandfaction) | Object | Specifies statuses to apply to other units that share a tag and faction with the target. | 1 ||
| [`ApplyToRandomClosestAlly`](#object-applytorandomclosestally) | Object | Specifies statuses to apply to a random ally closest to the target. | 1 ||
| `BombRatTurtle` | `Number` | The number of bomb rat turtle spawns triggered. | 1 ||
| `BonusDamageBasedOnMana` | `Number` | The amount of bonus damage dealt, scaled by the target's current mana. | 1 ||
| `BypassRockKnockback` | `Number` | If set to a non-zero number, bypasses normal rock knockback behavior. | 1 ||
| `CanceledQueuedInput` | `Number` | If set to a non-zero number, cancels any queued input from the target. | 1 ||
| `CaptureFamiliar` | Integer | The number of times to attempt to capture the target as a familiar. | 1 ||
| `ChaosBossFlipMidTeleport` | `Number` | If set to a non-zero number, causes the chaos boss to flip direction mid-teleport. | 1 ||
| `ChaosBossFormChange` | `Number` | If set to a non-zero number, triggers a chaos boss form change. | 1 ||
| `CharmedFacingForceAttack` | `Number` | If set to a non-zero number, the charmed target is forced to attack the direction they are facing. | 1 ||
| `ClearFinalBossBattlefield` | `Number` | If set to a non-zero number, clears the battlefield during the final boss fight. | 1 ||
| `CloneWeaponTemp` | `Number` | The number of turns the cloned weapon persists before being removed. | 1 ||
| [`CoinTossBounce`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the ability triggered when the coin lands on its edge after a bounce. | 1 ||
| [`Conditional_AbilityTargetIsSelf`](Engine_Uncategorized_Resources.md#conditional_abilitytargetisself) | Object | An object containing effects that execute only if the ability's target is the source unit. | 1 ||
| [`Conditional_ActiveWeather_Any`](#object-conditional_activeweather_any) | Object | An object containing effects that execute only if any of the specified weather types are active. | 1 ||
| [`Conditional_Backstab`](#object-conditional_backstab) | Object | An object containing effects that execute only if the attack lands on the target's back. | 1 ||
| [`Conditional_CanBeHealed`](#object-conditional_canbehealed) | Object | An object containing effects that execute only if the target can be healed. | 1 ||
| [`Conditional_DebuffRoll`](#object-conditional_debuffroll) | Object | An object containing effects that execute if a debuff roll succeeds, with an odds value defined inside. | 1 ||
| [`Conditional_Displaceable`](#object-conditional_displaceable) | Object | Contains an inner effect block that only executes if the target can be displaced (knocked back). | 1 ||
| [`Conditional_HasCleansableDebuffs`](#object-conditional_hascleansabledebuffs) | Object | An object containing effects that execute only if the unit has cleansable debuffs. | 1 ||
| [`Conditional_IsTrample`](#object-conditional_istrample) | Object | An object containing effects that execute only if the ability is a trample attack. | 1 ||
| [`Conditional_LivingPlayerCat`](#object-conditional_livingplayercat) | Object | An object containing effects that execute only if the source is a living player-owned cat. | 1 ||
| [`Conditional_NotBig`](#object-conditional_notbig) | Object | An object containing effects that execute only if the target is not a 'big' unit. | 1 ||
| [`Conditional_RandomChance`](#object-conditional_randomchance) | Object | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 1 ||
| [`Conditional_SourceAbilityHasTag`](#object-conditional_sourceabilityhastag) | Object | An object containing effects that execute only if the source ability has the specified tag. | 1 ||
| [`Conditional_SourceHasStatus`](#object-conditional_sourcehasstatus) | Object | An object containing effects that execute only if the source unit has the specified status. | 1 ||
| [`ConjureSingleUseBonusAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the bonus ability to conjure for single use (e.g., 'random' for a random one). | 1 ||
| `CurrentWeaponAddElectricElement` | `Number` | The number of turns the current weapon gains the electric element. | 1 ||
| `DamageWeapon` | `Number` | The amount of durability damage dealt to the equipped weapon. | 1 ||
| [`DeathwormUnderground`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the ability triggered when the Deathworm emerges from underground. | 1 ||
| `DecoySwapper` | `Number` | If true, the decoy swaps places with the source when spawned. | 1 ||
| [`DelayCastAbility`](#object-delaycastability) | Enum / Object | Specifies the name of an ability to cast after a delay. | 1 ||
| [`DelayedWindCone`](#object-delayedwindcone) | Object | An object containing parameters for a delayed wind cone, such as damage and distance. | 1 ||
| `DeleteTraps` | `Number` | If true, removes all traps from the map. | 1 ||
| `DestroyNeckArmor` | `Number` | If true, destroys the target's neck armor slot. | 1 ||
| `DieViolently` | Integer | If true, causes the target to die with a violent, explosive visual effect. | 1 ||
| [`DinoLegAnimation`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the animation trigger for the dinosaur leg (e.g., 'poop' for the poop animation). | 1 ||
| `Disguised` | `Number` | If true, the unit is disguised, appearing as a different faction or model. | 1 ||
| `DissolveRandomArmorPiece` | `Number` | If true, destroys a random armor piece (head, body, neck) on the target. | 1 ||
| `DontHealEnemies` | `Number` | If true, the healing effect does not affect enemy units. | 1 ||
| `DoubleCastSpellsEachTurn_Status` | `Number` | The number of turns the unit gains Double Cast for spells each turn. | 1 ||
| `DrainAllyCatsForFleshGolem` | `Number` | The amount of health drained from ally cats to heal the Flesh Golem. | 1 ||
| `DuplicateRandomEquippedItem` | `Number` | If true, creates a copy of a random equipped item. | 1 ||
| `Enlarge` | `Number` | The number of turns the unit is enlarged, increasing its size and stats. | 1 ||
| [`EnterMount`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the mount status to apply to the unit. | 1 ||
| `ExistUntilIdleUpkeep` | `Number` | If true, the entity persists until the source unit enters idle upkeep. | 1 ||
| `ExplodeCharacter` | `Number` | The radius (in tiles) of an explosion centered on the character. | 1 ||
| `ExplodeCharacter_DeathBloom` | `Number` | The amount of damage dealt by the DeathBloom explosion. | 1 ||
| `ExplodeCharacter_DeathBloom2` | `Number` | The amount of damage dealt by the DeathBloom2 explosion. | 1 ||
| `ExplodeCharacter_NoDie` | `Number` | The damage dealt when a character explodes without dying. | 1 ||
| `FactionConversion` | `Number` | Converts the target to the caster's faction. | 1 ||
| `FactionDisguiseSource` | `Number` | If true, the unit adopts the faction of the source unit for disguise. | 1 ||
| `FastKnockback` | `Number` | The number of tiles the target is knocked back with fast animation. | 1 ||
| `FinalBossQueueBeam` | `Number` | If true, queues the final boss beam attack. | 1 ||
| `FlatAIBonus` | `Number` | A flat adjustment to the AI's evaluation score for this action; positive values encourage the AI to use it, negative values discourage it. | 1 ||
| `ForceCollectsPickups` | `Number` | If true, the unit automatically collects nearby pickups. | 1 ||
| `ForceMoveAndAttack` | `Number` | If true, forces the target to move and attack its nearest enemy. | 1 ||
| `ForceTransferWeapon` | `Number` | If true, forces the weapon to be transferred to the target. | 1 ||
| `GenericBuff` | `Number` | A generic buff value applied to the unit. | 1 ||
| `GiveBoundItemToTarget` | `Number` | If true, gives the source's bound item to the target. | 1 ||
| [`GlobalSpawnCharacter`](./Engine_LogicKeys.md#valid-property-keys) | Enum | Specifies the name of a character to spawn globally. | 1 ||
| `HealPercentMaxHP` | `Number` | The percentage of max HP healed (e.g., 100 for full heal). | 1 ||
| `HealTo` | `Number` | The target HP percentage to heal the unit to (e.g., '50%' for half max HP). | 1 ||
| `IgnoreDebuffs` | `Number` | If true, the effect ignores debuffs on the target. | 1 ||
| [`IncAuxCounterCycle`](#object-incauxcountercycle) | Object | An object containing parameters for incrementing an auxiliary counter with a change and maximum value. | 1 ||
| `IncreaseCumulativeBlastDamage` | `Number` | If true, increases the cumulative blast damage counter. | 1 ||
| `IncreaseItemAuxOnKill` | `Number` | If true, increases the item's aux counter on kill. | 1 ||
| `InterchangeMoveActPoints` | `Number` | If true, swaps the unit's remaining move points and action points. | 1 ||
| `MadnessChanceOnTurnBegin` | Integer | The chance (as a multiplier) to inflict Madness status at the start of each turn in the next battle. | 1 ||
| `MakeWeaponUnbreakable` | `Number` | If true, makes the equipped weapon unbreakable. | 1 ||
| `ManaStealToHealth` | `Number` | The amount of mana stolen and converted to health (negative values may drain health). | 1 ||
| `ManglerAttack` | `Number` | If true, the attack triggers the Mangler's attack pattern. | 1 ||
| `ManglerShuffle` | `Boolean` | If true, the order of effects in this damage instance is randomized before application. | 1 ||
| `MassAttackThis` | `Number` | The number of additional targets this attack hits via the Mass Attack mechanic. | 1 ||
| `MimicMetronome` | `Number` | The number of random abilities the Metronome effect selects from this unit's ability pool. | 1 ||
| `MotherTumorDebugForcePass` | `Number` | If non-zero, forces the Mother Tumor boss to pass its turn, skipping its normal action. | 1 ||
| [`NextBasicAttackCritsThisTurn`](#object-nextbasicattackcritsthisturn) | Object | An object or number configuring the next basic attack to be a critical hit this turn. An object may contain stack, cant_miss, or piercing sub-keys. | 1 ||
| [`NextBattleStatusStacks`](#object-nextbattlestatusstacks) | Object | An object specifying status effects and their stacks to be applied at the start of the next battle. Contains a "fights" counter and nested status keys. | 1 ||
| [`ObjectOnHitFullyEmpty`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the object (e.g., RandomArmorPickup) to spawn on the target when the attacker's inventory is completely empty. | 1 ||
| `OverHealToShield` | `Number` | The amount of excess healing converted into temporary shield points. | 1 ||
| [`OverrideChainKnockbackDamage`](./Engine_LogicKeys.md#valid-property-keys) | `String` | A formula string that overrides the damage dealt by chain knockback (e.g., "3+bonus_melee_ability_damage"). | 1 ||
| `PermanentCharisma` | `Number` | The amount of permanent Charisma added to the unit's base stats. | 1 ||
| `PermanentLuck` | `Number` | The amount of permanent Luck added to the unit's base stats. | 1 ||
| `PermanentUpgradeRandomActiveOrPassive` | `Number` | The number of random active or passive abilities permanently upgraded. | 1 ||
| [`PoolMetronome`](#object-poolmetronome) | Object | An object containing a "pool" array of ability names that the Metronome effect can randomly select from. | 1 ||
| [`QueueUseAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the ability ID to be used immediately after the current action resolves. | 1 ||
| `RandomKnockbackDirection` | `Number` | The number of random directions the target can be knocked back (e.g., 4 selects from 4 cardinal directions). | 1 ||
| `ReformMoonHead` | `Number` | If non-zero, triggers the Moon Head's reformation mechanic (e.g., after it eats a cat). | 1 ||
| `RefreshItemAbilities` | `Number` | The number of times all item abilities are recharged (cooldowns reset). | 1 ||
| `RefreshNonManaItemAbilities` | `Number` | The number of times non-mana item abilities are recharged. | 1 ||
| `RefreshOncePerFightAbilities` | `Number` | The number of times abilities limited to once per fight are refreshed. | 1 ||
| [`RemoveStatusStacks`](#object-removestatusstacks) | Object | An object specifying a status name and the number of stacks to remove from the target. | 1 ||
| `RepairAllCondition` | `Number` | If non-zero, fully repairs the condition of all equipped items. | 1 ||
| `RerollEnemy` | `Number` | The number of times the target enemy is re-rolled (transformed into a new random enemy). | 1 ||
| `ReturnDinoLegs` | `Number` | If non-zero, returns the Dino Legs ability to the unit after it is consumed. | 1 ||
| `RNGCannonRandomDamage` | `Number` | The maximum random damage value for the RNG Cannon attack. | 1 ||
| `ScatterRandomPickups` | `Number` | The number of random pickups scattered around the target's location. | 1 ||
| [`ScrambleLastUsedSpell`](#object-scramblelastusedspell) | Object | An object containing a "permanent" boolean. If true, permanently scrambles (randomizes) the last used spell. | 1 ||
| `ShadowCrit` | `Number` | If non-zero, enables the Shadow Crit mechanic, granting bonus critical hit chance or damage from stealth. | 1 ||
| `ShootHereCommand` | `Number` | If non-zero, commands an allied unit to shoot at this unit's target. | 1 ||
| `ShootHereReceiver` | `Number` | If non-zero, marks this unit as the receiver of a Shoot Here command. | 1 ||
| `SmallHitExplosion` | `Number` | The number of small explosion VFX to spawn on hit. | 1 ||
| `SmellBlood` | `Number` | If non-zero, activates the Smell Blood ability which reveals nearby injured units. | 1 ||
| [`SoundEventOnHit`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the sound event ID to play on hit (e.g., "Batterup_Connect"). | 1 ||
| [`SourceSwapsBackEndOfTurn`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the ability ID to use to swap the source unit back at the end of the turn. | 1 ||
| `SpawnWebTrap` | `Number` | The number of web traps to spawn on the target tile. | 1 ||
| [`SpecialBossMultipartInstakill`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the boss ID (e.g., "moonboss") whose multipart instakill mechanic is triggered. | 1 ||
| `SpitConsumed` | `Number` | If non-zero, marks the object consumed by the Spit ability as having been used. | 1 ||
| `SplashDamage` | `Number` | The radius (in tiles) for splash damage applied to adjacent targets. | 1 ||
| `StackingSandstorm` | `Number` | If non-zero, enables the stacking sandstorm mechanic which increases damage per stack. | 1 ||
| `StealDemonicGlyph` | `Number` | The number of Demonic Glyphs stolen from the target. | 1 ||
| [`StealEquipment`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the type of equipment to steal (e.g., "any") from the target. | 1 ||
| `StealthCritChance` | `Number` | The percentage chance to critically hit while stealthed. | 1 ||
| `StealTurn` | `Number` | The number of turns stolen from the target to grant to the attacker. | 1 ||
| `SwapHighestAndLowestStat` | `Number` | If non-zero, swaps the unit's highest base stat value with its lowest. | 1 ||
| [`SwapWeapon`](#object-swapweapon) | Object | An object containing a "pool" array of weapon names to randomly swap to. | 1 ||
| `T3HitlerTriggerInitialSpawns` | `Number` | If non-zero, triggers the initial spawn sequence for the T3 Hitler boss. | 1 ||
| [`TagMetronome`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies a tag (e.g., "musical") used to filter which abilities the Metronome effect can pick. | 1 ||
| `TakeExtraTurnEndOfRound` | `Number` | The number of extra turns taken at the end of the round. | 1 ||
| `TargetedMetronome` | `Number` | The number of random targets hit by the Targeted Metronome effect. | 1 ||
| [`TeamBonusAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the ability ID granted to allies as a team bonus. | 1 ||
| [`TeleportBackAtTurnEnd`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the ability ID used to teleport the unit back to its starting position at turn end. | 1 ||
| `TempBackstabBleed` | `Number` | The number of temporary Bleed status stacks applied on a backstab attack. | 1 ||
| `TempBackstabPiercing` | `Number` | The amount of temporary piercing added to backstab attacks. | 1 ||
| `TempBackstabPoison` | `Number` | The amount of temporary poison stacks applied with backstab attacks. | 1 ||
| `TempBasicAttackBonusAOE` | `Number` | The amount of temporary area-of-effect bonus on basic attacks. | 1 ||
| `TempLuckUp` | `Number` | The amount of temporary luck increase. | 1 ||
| `TempPenetrate` | `Number` | The amount of temporary penetration applied to attacks. | 1 ||
| `ThornsDamageImmuneUntilSettled` | `Number` | The number of turns the target is immune to thorns damage until it settles. | 1 ||
| [`TickDownStatus`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the status effect whose duration is reduced by one tick. | 1 ||
| `TileDamageImmuneUntilSettled` | `Number` | The number of turns the target is immune to tile damage until it settles. | 1 ||
| [`TransformBasicMove`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the basic move to transform into. | 1 ||
| [`TransformEquipment`](#object-transformequipment) | Object | Defines an equipment transformation from one item to another, with 'from' and 'to' sub-keys. | 1 ||
| [`TransformNow`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the form to immediately transform into. | 1 ||
| `Trapper_Status` | `Number` | The number of trap-related status stacks applied. | 1 ||
| `TriggerGameEnding` | `Number` | If set to 1, triggers the game's ending sequence; 0 disables it. | 1 ||
| `TriggerMotherConsume` | `Number` | The number of times the Mother consume effect is triggered. | 1 ||
| `TriggerMotherGrow` | `Number` | The number of times the Mother grow effect is triggered. | 1 ||
| `TurnAround` | `Number` | The number of times the unit turns around. | 1 ||
| [`TurnControlDelay`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the delay in seconds before the unit regains turn control. | 1 ||
| `TurnRight` | `Number` | The number of times the unit turns to the right. | 1 ||
| `UndoDamage` | `Number` | The amount of damage reversed. | 1 ||
| [`UseMoveAbilityWithAI`](#object-usemoveabilitywithai) | Object | Defines a move ability to execute with AI-controlled movement weights. | 1 ||
| `VaporizeDice` | `Number` | The number of dice vaporized. | 1 ||
| [`VisualCountDownThenApplyStatus`](#object-visualcountdownthenapplystatus) | Object | Contains a visual countdown sequence that culminates in applying a status effect, optionally forcing an ability use. | 1 ||
| [`WaggleClone`](#object-waggleclone) | Object | Defines a waggle clone ability with health thresholds and object sizes. | 1 ||
| [`Attraction`](./Enums.md) | Integer | The number of stacks of Attraction applied, drawing enemy units toward the target. | 1 | 1 |
| [`Bloodzerked`](./Enums.md) | Integer | The number of Bloodzerk stacks applied. | 1 | 1 |
| [`ChampionUpgradeNextMinion`](./Enums.md) | Integer | The number of champion upgrades applied to the next spawned minion. | 1 | 1 |
| [`ChangeTilesUnder`](./Enums.md) | Enum | The tile type to change the ground tiles under the target to. | 1 | LavaTile |
| [`ChargeFists`](./Enums.md) | Integer | The number of charge stacks applied to unarmed attacks. | 1 | 1 |
| [`CreateGlobalModifiers`](#object-createglobalmodifiers) | Object | Defines global gameplay modifiers to activate. | 1 ||
| [`DoubleCast`](./Enums.md) | Integer | The number of double-cast stacks, allowing a spell to be cast twice. | 1 | 1 |
| [`DrinkWater`](./Enums.md) | Integer | The number of water-drink actions performed. | 1 | 1 |
| [`EliteUpgradeNextMinion`](./Enums.md) | Integer | The number of elite upgrades applied to the next spawned minion. | 1 | 1 |
| [`EmptyMind`](./Enums.md) | Integer | The number of Empty Mind stacks, likely disabling special abilities. | 1 | 1 |
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer | The number of extra basic moves per turn granted. | 1 | 1 |
| [`FireArmor`](./Enums.md) | Integer | The number of Fire Armor stacks providing damage reflection. | 1 | 1 |
| [`FireArmor2`](./Enums.md) | Integer | The number of Fire Armor2 stacks (likely a variant). | 1 | 1 |
| [`ForceUseAbility`](./Enums.md) | Enum | The name of the ability the source is forced to use, optionally with a chance. | 1 | MotherTumorGrow |
| [`GainCoinsRange`](#object-gaincoinsrange) | Object | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 1 ||
| [`HealRandomInjury`](./Enums.md) | Integer | The number of random injuries healed on the target. | 1 | 1 |
| [`HeavyHits`](./Enums.md) | Integer | The number of Heavy Hits stacks increasing attack impact. | 1 | 1 |
| [`IceArmor`](./Enums.md) | Integer | The number of Ice Armor stacks granting defensive properties. | 1 | 1 |
| [`Infested`](./Enums.md) | Integer | The number of stacks of Infested applied. | 1 | 1 |
| [`Invulnerable`](./Enums.md) | Integer | The number of Invulnerable stacks, making the unit immune to damage. | 1 | 1 |
| [`Meaty`](./Enums.md) | Integer | The number of Meaty stacks increasing health or size. | 1 | 1 |
| [`Muted`](./Enums.md) | Integer | The number of Muted stacks, disabling certain abilities. | 1 | 1 |
| [`NextAbilityHeals`](./Enums.md) | Integer | The number of stacks causing the next ability to heal instead of damage. | 1 | 1 |
| [`NextActionLuckUp`](./Enums.md) | Integer | The number of stacks increasing luck for the next action. | 1 | 99 |
| [`NextDamageReduceAndHealAllies`](./Enums.md) | Integer | The number of stacks reducing next damage and healing nearby allies. | 1 | 1 |
| [`NextTurnDoubleRangedDamage`](./Enums.md) | Integer | The number of stacks doubling ranged damage on the next turn. | 1 | 1 |
| [`NonStackingDivineShield`](./Enums.md) | Integer | The number of Divine Shield stacks that do not stack with duplicates. | 1 | 1 |
| [`PermanentDexterity`](./Enums.md) | Integer | The permanent amount of dexterity added or removed. | 1 | 2 |
| [`PermanentImmobile`](./Enums.md) | Integer | The permanent amount of immobility stacks applied. | 1 | 1 |
| [`PermanentIntelligence`](./Enums.md) | Integer | The permanent amount of intelligence added or removed. | 1 | 2 |
| [`PermanentSpeed`](./Enums.md) | Integer | The permanent amount of speed added or removed. | 1 | 2 |
| [`ProbeCharmed`](./Enums.md) | Integer | The number of charm stacks applied by a probe. | 1 | 1 |
| [`RandomPermanentStat`](./Enums.md) | Integer | The amount of a random permanent stat change (positive or negative). | 1 | 1 |
| [`ReduceManaCost`](./Enums.md) | Integer | The number of stacks reducing mana cost of abilities. | 1 | 1 |
| [`ReduceManaCostExcludeBrainstorm`](./Enums.md) | Integer | The number of stacks reducing mana cost, excluding Brainstorm. | 1 | 1 |
| [`Regurge`](./Enums.md) | Integer | The number of regurgitation triggers. | 1 | 1 |
| [`SetDefaultFace`](./Enums.md) | Enum | Specifies the default facial expression, such as 'happy', 'sad', or 'insane'. | 1 | insane |
| [`ShortCircuit`](./Enums.md) | Integer | The number of stacks of the ShortCircuit status effect. | 1 | 1 |
| [`SpawnCoinAnywhere`](./Enums.md) | Array / Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 1 | [.5] |
| [`SpellShield`](./Enums.md) | Integer | The number of stacks of SpellShield, which blocks incoming spells. | 1 | 1 |
| [`StatBounty`](./Enums.md) | Integer | The number of stacks of the StatBounty status effect. | 1 | 1 |
| [`StatusGroup`](#object-statusgroup) | Object | A container grouping multiple status effects to be applied simultaneously. | 1 ||
| [`Switcheroo`](./Enums.md) | Integer | The number of stacks of the Switcheroo status effect. | 1 | 1 |
| [`Taunting`](./Enums.md) | Integer | The number of stacks of Taunting, which forces enemies to target the unit. | 1 | 1 |
| [`TempBackstab`](./Enums.md) | Integer | The amount of temporary backstab bonus, typically as a percentage. | 1 | 75 |
| [`TempBonusKnockback`](./Enums.md) | Integer | The number of stacks of temporary bonus knockback distance. | 1 | 1 |
| [`TempBonusKnockbackDamage`](./Enums.md) | Integer | The number of stacks of temporary bonus knockback damage. | 1 | 1 |
| [`TempCounterAttack`](./Enums.md) | Integer | The number of turns TempCounterAttack lasts, ticking down at the start of the unit's turn. | 1 | 1 |
| [`TempInjuryImmunity`](./Enums.md) | Integer | The number of stacks of temporary immunity to Injuries. | 1 | 1 |
| [`TempManaCostReduction`](./Enums.md) | Integer | The number of stacks of temporary mana cost reduction. | 1 | 1 |
| [`TempPreEmptiveCounterAttack`](./Enums.md) | Integer | The number of turns of temporary pre-emptive counterattack status. | 1 | 1 |
| [`TilesMovedToCritChance`](./Enums.md) | Integer | The number of stacks of a status that grants critical hit chance based on tiles moved. | 1 | 1 |
| [`TilesMovedToMana`](./Enums.md) | Integer | The number of stacks of a status that grants mana based on tiles moved. | 1 | 1 |
| [`TilesMovedToNeighborHeal`](./Enums.md) | Enum | Specifies the scaling type for healing neighbors based on tiles moved (e.g., 'level'). | 1 | level |
| [`TilesMovedToStrength`](./Enums.md) | Integer | The number of stacks of a status that grants strength based on tiles moved. | 1 | 1 |
| [`TowerDefenseStatus`](./Enums.md) | Integer | The number of stacks of the sentry/tower defense status, granting stationary attack capabilities. | 1 | 1 |
| [`TowerDefenseStatus2`](./Enums.md) | Integer | The number of stacks of the enhanced sentry/tower defense status. | 1 | 1 |
| [`VaporizeCorpseFlipAdvantage`](./Enums.md) | Array | The number of stacks and probability of vaporizing a corpse to gain loot flip advantage. | 1 | [.33] |

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
