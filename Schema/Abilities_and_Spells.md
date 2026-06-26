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
| [`chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum | Specifies the chapter or stage condition when this spawn pool or ability takes effect, e.g. "alley" or "1". | 3 ||
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | Enum | Determines which visual or gameplay layer (e.g. "tiles", "pickups", "characters") the editor object belongs to. | 3 ||
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
| `lob` | Boolean | If true, the projectile or ability arc follows a lobbed trajectory instead of a straight line. | 130 ||
| `delay` | Number | Frame delay before firing projectile/effect. | 93 ||
| `dont_visualize_ai` | Boolean | If true, the AI's turn visualization for this ability is skipped for brevity. | 86 ||
| `dont_orient` | Boolean | Prevents the character from turning to face the target. | 83 ||
| [`dash_animation`](./Enums.md#enum-dash_animation) | Enum | State-specific animations for trample/dash abilities. | 65 ||
| [`dash_start_animation`](./Enums.md#enum-dash_start_animation) | Enum | Specifies the animation played at the start of a dash (e.g. "dashstart", "launchStart", "thrustersStart"). | 63 ||
| [`speed`](./Enums.md) | Array / Number | The movement speed of the projectile or graphic, as a single number or a range [min max]. | 61 | [1.0] |
| [`affected_particle`](./Enums.md#enum-affected_particle) | Enum | Visuals applied to the target receiving the effect. | 51 ||
| [`dash_attack_animation`](./Enums.md#enum-dash_attack_animation) | Enum | Specifies the animation played when the dash reaches the target (e.g. "dashend", "spin", "headbuttUppercut"). | 45 ||
| `lob_height` | Integer | Adjustments for arcing projectiles. | 45 ||
| [`animation_in`](./Enums.md#enum-animation_in) | Enum | Used for transition states (like burrowing). | 43 ||
| [`animation_out`](./Enums.md#enum-animation_out) | Enum | Used for transition states (like burrowing). | 43 ||
| [`jump_attack_animation`](./Enums.md#enum-jump_attack_animation) | Enum | Overrides for jump physics. | 39 ||
| `use_projectile` | Boolean | If true, the ability uses a projectile graphic instead of a direct hit. | 35 ||
| [`palette`](./Enums.md) | Integer | Index or list of palette indices used for coloring the entity or its variations. | 34 | 6 |
| [`full_jump_animation`](./Enums.md#enum-full_jump_animation) | Enum | Specifies the animation played during a full jump arc (e.g. "moonjump", "jumpsmash", "leap"). | 24 ||
| `full_jump_sync_frames` | Integer | The number of frames over which the full jump animation plays, used to synchronize timing. | 24 ||
| `use_rotation` | Boolean | If true, the character rotates during the ability's graphic sequence. | 24 ||
| [`dash_end_animation`](./Enums.md#enum-dash_end_animation) | Enum | Specifies the animation played when a dash movement ends. | 22 ||
| `full_jump_windup_frames` | Integer | The number of frames for the windup before a full jump. | 20 ||
| `visual_delay_but_simultaneous_damage` | Integer | The number of frames of visual delay applied to the graphic while damage is applied simultaneously to all targets. | 18 ||
| [`center_particle`](./Enums.md#enum-center_particle) | Enum | Specific spawn points for particles. | 17 ||
| [`area_particle`](./Enums.md#enum-area_particle) | Enum | Specific spawn points for particles. | 16 ||
| `fall_from_sky` | Boolean | Spawns the projectile from the top of the screen. | 16 ||
| [`move_start_animation`](./Enums.md#enum-move_start_animation) | Enum | Specifies the animation played when a movement ability begins. | 14 ||
| `use_placeholder` | Boolean | If true, a placeholder graphic is used instead of the intended animation. | 14 ||
| [`move_end_animation`](./Enums.md#enum-move_end_animation) | Enum | Specifies the animation played when a movement ability ends. | 13 ||
| `face_toss_target` | Boolean | If true, the character faces the target before tossing a projectile. | 12 ||
| `ignore_slowtiles` | Boolean | If true, the ability ignores movement speed penalties from slow tiles during graphic playback. | 12 ||
| [`chain_distance`](./Enums.md#enum-chain_distance) | Number | Creates a tethered repeating graphic (like a hook). | 11 ||
| [`chain_movieclip`](./Enums.md#enum-chain_movieclip) | Enum | Creates a tethered repeating graphic (like a hook). | 11 ||
| `darken_screen` | Boolean | Dims the background during the ability cast. | 11 ||
| [`beam_cap`](./Enums.md#enum-beam_cap) | Enum | Flash movieclips used to render continuous laser beams. | 10 ||
| [`beam_clip`](./Enums.md#enum-beam_clip) | Enum | Flash movieclips used to render continuous laser beams. | 10 ||
| `bounce_on_hit` | Boolean | Visual hop when striking a target. | 10 ||
| `darken_screen_exclude_characters_on_tile` | Boolean | If true, the screen darkening effect excludes characters occupying the targeted tile. | 10 ||
| [`end`](./Enums.md#enum-end) | Enum | Segments for continuous channeled animations. | 10 ||
| [`jump_start_animation`](./Enums.md#enum-jump_start_animation) | Enum | Specifies the animation played at the start of a jump. | 10 ||
| [`loop`](./Enums.md#enum-loop) | Enum | Segments for continuous channeled animations. | 10 ||
| [`prime_animation`](./Enums.md#enum-prime_animation) | Enum | Specifies the animation played while priming or charging the ability. | 10 ||
| [`start`](./Enums.md#enum-start) | Enum | Segments for continuous channeled animations. | 10 ||
| `max_tiles_single_loop` | Integer | The maximum number of tiles the character can travel in a single animation loop during movement. | 9 ||
| `sync_speed` | Integer | The number of frames per tile used to synchronize movement speed. | 9 ||
| [`random_delay`](./Arrays.md#array-random_delay) | Array | Adds chaotic timing to multi-projectile casts. | 9 ||
| `fx_is_placeholder_animation` | Boolean | If true, the FX animation is a placeholder and should be replaced. | 8 ||
| `aoe_spell_on_land` | Boolean | Visual trigger when a jump lands. | 7 ||
| `fx_random_flip` | Boolean | If true, the FX graphic is randomly flipped horizontally on each use. | 7 ||
| [`land_animation`](./Enums.md#enum-land_animation) | Enum | Specifies the animation played when the character lands after a jump. | 7 ||
| [`miss_particle`](./Enums.md#enum-miss_particle) | Enum | Specific spawn points for particles. | 7 ||
| `use_super_armor` | Boolean | Prevents flinch animations from interrupting this cast. | 7 ||
| [`air_animation`](./Enums.md#enum-air_animation) | Enum | Animation played while entity is airborne. | 6 ||
| [`custom_priming_animation`](./Enums.md#enum-custom_priming_animation) | Enum | Animation used while charging an ability. | 6 ||
| `darken_screen_exclude_self` | Boolean | If true, the screen darkening effect excludes the casting character. | 6 ||
| `darken_screen_start_early` | Boolean | If true, the screen darkening effect begins before the ability's main graphic sequence. | 6 ||
| [`fall_randomize_timing`](./Enums.md#enum-fall_randomize_timing) | Number | A random timing offset multiplier applied to falling graphics, varying the fall start frame. | 6 ||
| `min_throw_height` | Number | The minimum height of the throw arc, measured in tiles. | 6 ||
| `single_projectile` | Boolean | If true, only a single projectile is fired, ignoring any multi-projectile settings. | 6 ||
| [`miss_random_delay`](./Arrays.md#array-miss_random_delay) | Array | Specifies the random delay range in frames for a missed projectile's visual. | 6 ||
| [`detatched_animation`](./Enums.md#enum-detatched_animation) | Enum | Plays an animation separated from the character body. | 5 ||
| `detatched_animation_reach` | Integer | The maximum tile distance for detached/separated body part animations (e.g., head or limb). | 5 ||
| [`empty_animation`](./Enums.md#enum-empty_animation) | Enum | Specifies the animation to use when no other animation is active. | 5 ||
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison operator for evaluating a condition against a threshold (e.g., equal, greater). | 5 ||
| `fixed_jump_height` | Number | The height in tiles for a fixed jump animation. | 4 ||
| [`rocket_swirl`](#object-rocket_swirl) | Object | Visual parameters for swirling projectile paths. | 4 ||
| `sync_frames` | Integer | The number of frames to synchronize the animation with another event. | 4 ||
| [`dash_decelerating_animation`](./Enums.md#enum-dash_decelerating_animation) | Enum | Specifies the animation to play when the dash is decelerating. | 3 ||
| `decelerate` | Integer | Visual slowdown at the end of a movement. | 3 ||
| `delay_from_map_edge` | Boolean | Delays effect based on distance from the screen edge. | 3 ||
| `easing` | Integer | Smoothing function for movement animations. | 3 ||
| [`fixed_jump_speed`](./Enums.md#enum-fixed_jump_speed) | Number | The speed multiplier for a fixed jump animation. | 3 ||
| [`grab_animation`](./Enums.md#enum-grab_animation) | Enum | Specifies the animation used when the unit grabs an object or target. | 3 ||
| [`lob_yoff`](./Enums.md#enum-lob_yoff) | Number | Adjustments for arcing projectiles. | 3 ||
| `lock_orientation_during_dash` | Boolean | Prevents the sprite from flipping mid-dash. | 3 ||
| `use_projectile_spawn_offset` | Boolean | If true, use the projectile spawn offset defined for the graphics when firing a projectile. | 3 ||
| `use_rotation_once` | Boolean | If true, apply rotation to the graphic only once at the start instead of continuously. | 3 ||
| `always_play_animations` | Boolean | Bypasses speed-up/skip logic. | 2 ||
| `detatched_animation_cutoff` | Boolean | If true, cut off the detached animation when it completes rather than looping or fading. | 2 ||
| `do_damage_immediately` | Boolean | Applies math before the animation actually hits. | 2 ||
| `jump_height_multiplier` | Number | Overrides for jump physics. | 2 ||
| [`mask_center`](./Enums.md#enum-mask_center) | Enum | Specifies the mask center point used for rendering or clipping effects. | 2 ||
| [`mask_extent`](./Enums.md#enum-mask_extent) | Enum | Specifies the mask extent or size used for rendering or clipping. | 2 ||
| `max_throw_height` | Number | The maximum height in tiles for a thrown object's arc. | 2 ||
| [`particle_mat`](./Enums.md#enum-particle_mat) | Enum | Specifies the material/shader applied to particle effects. | 2 ||
| [`preturn_animation`](./Enums.md#enum-preturn_animation) | Enum | Specifies the animation to play before the unit's turn begins (e.g., an alert/ready pose). | 2 ||
| [`primed_alt_animation`](./Strings.md#string-primed_alt_animation) | String | Specifies the name of an alternative animation to use when the ability is primed/charged. | 2 ||
| [`pseudoprojectile`](./Enums.md#enum-pseudoprojectile) | Enum | Specifies a pseudo-projectile type that mimics a projectile without using actual projectile mechanics. | 2 ||
| `reverse_orientation` | Boolean | If true, reverse the orientation (flip) of the graphic relative to its default direction. | 2 ||
| `self_damage_mid_port` | Boolean | If true, apply self-damage mid-teleport during a port ability. | 2 ||
| `throw_speed` | Integer | The speed at which a thrown object travels. | 2 ||
| `use_hit_alts` | Boolean | If true, use alternative hit animations for different damage types or reactions. | 2 ||
| [`affected_animation`](./Enums.md#enum-affected_animation) | Enum | Visuals applied to the target receiving the effect. | 1 ||
| [`ally_animation`](./Enums.md#enum-ally_animation) | Enum | Distinct animation used when targeting a friendly unit. | 1 ||
| [`animate_name`](./Enums.md#enum-animate_name) | Boolean / Enum | Animates the ability name text on cast. | 1 ||
| `apex_distance` | Number | Calculations for the peak of a jump/lob arc. | 1 ||
| [`apex_time`](./Enums.md#enum-apex_time) | Number | Calculations for the peak of a jump/lob arc. | 1 ||
| `bypass_combatspeed` | Boolean | If true, the animation ignores the global combat speed multiplier. | 1 ||
| [`damage_threshold_altanimations`](#object-damage_threshold_altanimations) | Object | Triggers different hit animations based on the amount of damage dealt. | 1 ||
| [`dash_bonk_animation`](./Enums.md#enum-dash_bonk_animation) | Enum | Specifies the animation to play when the unit bonks (hits a wall/obstacle) during a dash. | 1 ||
| `delay_from_map_center` | Boolean | Positional based timing delays. | 1 ||
| `delay_from_reverse_map_edge` | Boolean | If true, delay the animation based on distance from the map edge when reversed. | 1 ||
| `do_animation_offscreen` | Boolean | If true, allow the animation to play even when the unit is off-screen. | 1 ||
| `do_not_clear_placeholder` | Boolean | If true, the placeholder graphics for this ability are not removed after the animation. | 1 ||
| `face_targets` | Boolean | Forces the sprite to look at the target tile. | 1 ||
| `first_castpoint_is_self_damage_only` | Boolean | If true, the first cast point of this ability only applies damage to the caster. | 1 ||
| [`hang_time`](./Enums.md#enum-hang_time) | Number | The amount of time in seconds the projectile or character hangs in the air before falling. | 1 ||
| `jump_speed_multiplier` | Number | A multiplier for the jump speed of the ability’s projectile or character. | 1 ||
| [`lob_speed`](./Enums.md#enum-lob_speed) | Number | Adjustments for arcing projectiles. | 1 ||
| `max_range` | Enum / Integer | The maximum and minimum distance required to cast. | 1 ||
| `min_range` | Integer | The maximum and minimum distance required to cast. | 1 ||
| `othercat_placeholder_available` | Boolean | If true, a placeholder for another cat is available for this ability’s graphics. | 1 ||
| [`precast_delay`](./Enums.md#enum-precast_delay) | Number | The amount of time in seconds before the ability begins its cast animation. | 1 ||
| `uncatchable` | Boolean | If true, the projectile from this ability cannot be caught or deflected. | 1 ||
| `use_directional_animations` | Boolean | If true, the ability uses directional animations based on the target’s position. | 1 ||
| `use_origin_offsets` | Boolean | If true, the ability’s graphics use origin offsets for spawning projectiles or effects. | 1 ||
| [`spawn_offset`](./Arrays.md#array-spawn_offset) | Array | A 3D vector [X, Y, Z] specifying the offset from the caster’s position where projectiles or effects spawn. | 1 ||

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
| [`desc`](./Enums.md) | Enum | Specifies the localization key or literal description text for the ability. | 1641 | ABILITY_FORMOFTHEWOLF2_DESC |
| [`name`](./Enums.md) | Enum | Specifies the localization key or literal name for the ability. | 1611 | ABILITY_HAILOFNAILS_NAME |
| [`class`](./Enums.md#enum-class) | Enum | Categorizes the ability for specific UI filters. | 876 ||
| [`type_icon`](./Strings.md#string-type_icon) | Enum | Determines which type icon (melee, ranged, magic, move, misc) is displayed for the ability. | 283 ||
| `animate_name` | Boolean / Enum | If true, adds a visual pop/animation to the name text when cast. | 177 ||
| [`icon_shell_frame`](./Strings.md#string-icon_shell_frame) | Variable | Specifies the background shell frame style for the ability’s icon (e.g., damage, nodamage, attack). | 28 ||
| [`is_move`](./Enums.md#enum-is_move) | Variable | Determines if the ability is a movement ability; ‘auto’ allows the game to decide. | 20 ||
| [`ability_icon`](./Enums.md#enum-ability_icon) | Enum | The UI icon to display in the action bar. | 14 ||
| [`tooltip_values`](./Arrays.md#array-tooltip_values) | Array | An array of mathematical expressions used to calculate values displayed in the ability’s tooltip. | 9 ||
| [`icon_damage_display`](./Strings.md#string-icon_damage_display) | String | A string representing the damage range or value displayed on the ability’s icon. | 8 ||
| [`icon_damage_display_eq`](./Math_Equations.md) | Equation | An equation used to calculate the damage value displayed on the ability’s icon. | 7 ||
| `is_basic_attack` | Boolean | If true, the ability is considered a basic attack and uses basic attack rules. | 6 ||
| `is_weapon` | Boolean | If true, the ability is treated as a ability item. | 4 ||
| [`icon_damage_type`](./Enums.md#enum-icon_damage_type) | Enum | Specifies the damage type icon (magic or physical) displayed on the ability’s icon. | 3 ||
| `is_trinket` | Boolean | If true, the item is treated as a trinket. | 3 ||
| `dont_visualize_ai` | Boolean | If true, the AI's turn visualization for this ability is skipped for brevity. | 2 ||
| [`icon_damage_display_suffix`](./Strings.md#string-icon_damage_display_suffix) | String | A string appended to the damage display on the ability’s icon, e.g., ‘x10’. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation clip to use for the ability’s meta representation. | 1 ||

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
| [`knockback`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | The base physics pushing power (in tiles). | 254 ||
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
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 1 | 2 |
| [`ranged`](./Enums.md) | Boolean | If true, the damage instance is treated as a ranged attack, allowing it to interact with range-related mechanics and modifiers. | 1 | true |

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
| [`min_aoe`](./Enums.md#enum-min_aoe) | Variable | The maximum and minimum radius/length of the AoE. | 253 ||
| `aoe_excludes_self` | Boolean | Prevents the AoE from hitting the caster. | 241 ||
| [`aoe_restrictions`](./Arrays.md#array-aoe_restrictions) | Array / Enum | Array of conditions the AoE tiles must meet (e.g., `must_have_line_of_sight_unpurgable`). | 197 ||
| `aoe_considers_character_size` | Boolean | Scales the AoE based on the caster's tile size (e.g., 2x2). | 170 ||
| [`range_mode`](./Enums.md#enum-range_mode) | Enum | How range is counted (`standard`, `ground_move`). | 114 ||
| [`X_is`](./Enums.md#enum-x_is) | Enum | Applies or references the 'X_is' effect/state. | 86 ||
| [`custom_aoe`](./Arrays.md#array-custom_aoe) | Array | Array of exact coordinates for a custom shape (e.g., `[[1, -1] [1, 0]]`). | 83 ||
| `multihit` | Enum / Integer | Hardcoded number of times the ability hits the target. | 62 ||
| `max_targets` | Integer / String | Limits on how many distinct entities can be targeted. | 56 ||
| `range_excludes_blocking` | Boolean | Cannot target through walls/obstacles. | 53 ||
| `prioritize_dont_change_direction` | Variable | AI preference to maintain current facing angle. | 52 ||
| [`target_requires_tag`](./Enums.md#enum-target_requires_tag) | Enum | Target must possess this exact character tag. | 40 ||
| [`aoe_symmetry`](./Enums.md#enum-aoe_symmetry) | Enum | Determines if the AoE mirrors on axes. | 28 ||
| `prioritize_face_camera` | Variable | AI preference to face South. | 26 ||
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
| `distance_sort_targets` | Variable | Prioritizes targets based on proximity. | 5 ||
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
| `low_health_character_threshold` | Variable | AI targeting threshold for seeking weak targets. | 3 ||
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
| [`custom_aoe_util_mirror`](./Arrays.md#array-custom_aoe_util_mirror) | Array | An array of coordinate pairs defining a mirrored Area of Effect pattern, where each inner array represents a [row, column] offset from the target tile. | 1 ||

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
| `once_per_fight` | Variable | Exhausts for the remainder of combat after one use. | 98 ||
| `act_points` | Integer | Consumes primary action points (default 1). | 86 ||
| `move_points` | Integer | Consumes movement points. | 59 ||
| `prime` | Integer | Requires a "priming" turn before it fires. | 30 ||
| `allow_offmap_casts` | Boolean | Can be used while the character is hidden/removed from grid. | 22 ||
| `cant_cast` | Variable | Explicitly disables casting (used for passive-triggered only abilities). | 18 ||
| [`charge`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Cooldown timers measured in turns. | 18 ||
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
| [`durability`](./Enums.md) | Integer | The amount of durability the item has, either as a single integer or a range [min, max] that is randomized upon acquisition. | 8 | 0 |
| `must_not_be_a_summon` | Boolean | Summons/Familiars cannot cast this. | 7 ||
| `start_reloaded` | Boolean | Spawns with the ability pre-loaded. | 7 ||
| `must_be_first_action` | Boolean | Can only be used at the very start of the turn. | 4 ||
| `enabled_formula` | Variable | Mathematical string required to be >0 to cast. | 3 ||
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
| [`damage`](./Abilities_and_Spells.md#object-damage) | Variable | The base damage properties of an attack. | 47 ||
| `piercing` | `Boolean` | If true, the damage instance ignores armor and damage reduction effects. | 12 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 11 ||
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target, bypassing accuracy and evasion checks. | 10 ||
| `knockback` | Enum / Integer | The number of tiles to push the target away from the attacker; can be negative to pull the target closer, or 'str' to scale with the attacker's strength stat. | 10 ||
| `heal` | `Number` | The amount of health restored, specified as a flat number or a formula string that evaluates to a healing value. | 6 ||
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 4 ||
| `ai_base_score` | Integer | A base priority score used by the AI to evaluate the desirability of using this ability; higher values increase the likelihood of selection. | 2 ||
| `non_lethal` | `Boolean` | If true, the damage cannot reduce a target below 1 HP, preventing fatal blows. | 1 ||

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
| [`object`](./Enums.md) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 184 | [TallSkeletonCat] |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 83 ||
| [`faction`](./Enums.md#enum-faction) | Enum | Determines which faction the spawned entity belongs to, controlling its team allegiance and targeting behavior. | 59 ||
| `ai_base_score` | Integer | A base priority score used by the AI to evaluate the desirability of using this ability; higher values increase the likelihood of selection. | 31 ||
| [`additional_passives`](#object-additional_passives) | Object | Passives granted intrinsically to a spawned entity. | 20 ||
| [`first_turn`](./Enums.md#enum-first_turn) | Enum | Determines when the spawned entity takes its first action, such as 'initiative' (immediately), 'next_turn' (after current unit), 'end_of_round', or 'next_round'. | 17 ||
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Determines which visual or gameplay layer (e.g. "tiles", "pickups", "characters") the editor object belongs to. | 14 ||
| [`catdata`](./Enums.md) | Enum | Specifies the cat data template or mutation type used for the spawned entity, such as a specific breed or clone variant. | 13 | fleshgolem |
| `clone_items` | Boolean | If true, transfers inventory to the clone. | 12 ||
| `lob` | Boolean | If true, the projectile or ability arc follows a lobbed trajectory instead of a straight line. | 4 ||
| [`post_spawn_statuses`](#object-post_spawn_statuses) | Object | Status effects applied immediately after an entity spawns. | 4 ||
| [`size`](./Enums.md) | Integer | A scale multiplier for the spawned entity's visual size, specified as a single value or a randomized range [min, max]; 'gemini' uses a special sizing mode. | 4 | 2 |
| `face_camera` | Boolean | If true, the spawned entity's sprite always rotates to face the camera, useful for billboard effects or UI elements. | 2 ||
| `inherit_elite_buffs` | Boolean | If true, the spawned entity inherits elite buffs from its source, such as increased stats or special modifiers. | 2 ||
| `start_dead` | Boolean | If true, the spawned entity begins the battle already in a dead or inactive state, often used for corpses or reanimation triggers. | 2 ||
| [`appearance`](./Enums.md#enum-appearance) | Enum | Specifies the visual appearance template for the spawned entity, overriding its default model with a named variant like 'GolemCat'. | 1 ||
| [`auto_cast_on_spawn`](./Enums.md#enum-auto_cast_on_spawn) | Enum | Specifies an ability to automatically cast upon the spawned entity's creation, such as 'Dash_Enemy' to perform an immediate dash. | 1 ||
| [`chapter`](./Enums.md#enum-chapter) | Enum | Specifies the chapter or stage condition when this spawn pool or ability takes effect, e.g. "alley" or "1". | 1 ||
| [`custom_additional_ai_weight`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | A custom AI weighting tag that modifies the decision-making score for this ability, used for special behavior rules like 'prefer_dont_move' or 'spread_grenades'. | 1 ||
| `include_passives` | Boolean | If true, the spawned entity includes its passive abilities from its template, granting innate effects on spawn. | 1 ||
| `redirect_location_if_blocked` | Boolean | If true, the spawn location is automatically redirected to the nearest valid unblocked tile if the intended position is occupied. | 1 ||
| [`spawnin_animation`](./Enums.md#enum-spawnin_animation) | Enum | Specifies the animation played when the entity spawns, such as 'digUp', 'grow', or 'summonspawnin', controlling its visual entry. | 1 ||
| `trigger_battle_start` | Boolean | If true, spawning this entity triggers the battle start sequence, such as activating introductory events or flags. | 1 ||

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
| [`DeadAltAbility`](./Enums.md) | Enum | Specifies the ability that triggers when the unit dies, granting a secondary effect based on the listed ability. | 12 | DonateBlood_Afterlife |
| [`AbilityEnabledOncePerFightAtHealthThreshold`](./Enums.md) | Integer | The health percentage at which the ability becomes enabled once per fight. | 7 | 50 |
| [`XIsFreeArmorSlots`](./Enums.md) | Integer | The number of free armor slots this passive provides, allowing equipment without a slot cost. | 7 | 1 |
| [`AbilityEnabledPercentEachTurn`](./Enums.md) | Integer | The percentage chance each turn that the ability becomes enabled. | 6 | 50 |
| [`FreeFirstCast`](./Enums.md) | Integer | The number of free casts granted for this ability, ignoring mana or resource costs. | 6 | 4 |
| [`XIsLivingAlliesWithTag`](./Enums.md) | Enum | Determines which ally tag is required for this passive to function, referring to living allies with that tag. | 5 | hitler_clone_fetus |
| [`CatchBoomerang`](./Enums.md) | Integer | If set to 1, the unit can catch a returning boomerang, negating its effect. | 4 | 1 |
| [`CopyBasicAttackEffects`](./Enums.md) | Integer | If set to 1, this ability copies the effects granted by basic attacks. | 4 | 1 |
| [`DownRankAIIfWeaponUsable`](./Enums.md) | Number | A multiplier for AI decision-making, reducing ability priority if a ability is usable. | 4 | .001 |
| [`AbilityEnableIfConsumedCharacterHasTag`](./Enums.md) | Enum | Specifies the tag the consumed character must have for this ability to be enabled. | 3 | sp_pill_normal |
| [`AbilityEnabledOncePerRound`](./Enums.md) | Integer | If set to 1, the ability can only be used once per round. | 3 | 1 |
| [`AbilityInheritsWeaponEffects`](./Enums.md) | Integer | The number indicating how deeply ability inherits ability effects, typically 1 or 2. | 3 | 2 |
| [`MoonHeadFinisherEnabler`](./Enums.md) | Integer | Controls the Moon Head finisher behavior: 1 enables it, -1 disables, 0 uses default logic. | 3 | 0 |
| [`XIsMultipliedPercentHealth`](./Enums.md) | Array | An array defining multipliers for specific health thresholds, affecting ability scaling. | 3 | [2] |
| [`AbilityEnabledIfHasStatus`](./Enums.md) | Enum | Specifies the status effect that must be present on the unit for the ability to be enabled. | 2 | DemonicGlyph_Summon |
| [`AutocastEachRound`](#object-autocasteachround) | Object | An object defining an ability that is automatically cast each round, with optional force display or ignore stun. | 2 ||
| [`ChargeSpiritBombAura`](./Enums.md) | Enum | Specifies the ability used to charge a Spirit Bomb aura, like DonateEnergy. | 2 | DonateEnergy |
| [`CopyCatPassive_Initializer`](./Enums.md) | Integer | The number indicating how many times the Copy Cat passive initializes its effect. | 2 | 2 |
| [`NukeQuestFinalBossModifications`](#object-nukequestfinalbossmodifications) | Object | An object containing modifications for the final boss in the Nuke quest, such as damage instances or win triggers. | 2 ||
| [`ReloadOnKill`](./Enums.md) | Integer | If set to 1, the ability reloads after any kill. | 2 | 1 |
| [`ReloadOnKillEnemy`](./Enums.md) | Integer | If set to 1, the ability reloads specifically after killing an enemy. | 2 | 1 |
| [`ReloadOnTotalDamageReceived`](./Enums.md) | Integer | The amount of total damage received required to trigger a reload. | 2 | 15 |
| [`XIsLivingCharactersWithTag`](./Enums.md) | Enum | Determines which character tag is required for this passive, referring to living characters with that tag. | 2 | husk |
| [`XIsOtherHealsThisTurn`](./Enums.md) | Integer | If set to 1, this ability activates when other heals occur this turn. | 2 | 1 |
| [`XIsSpellStormRampAndReset`](#object-xisspellstormrampandreset) | Integer / Object | An integer or object defining the ramp stacks and reset percentage for Spell Storm mechanics. | 2 | 0 |
| [`XIsTimesDamageTaken`](./Enums.md) | Integer | If set to 1, this ability scales based on times damage has been taken. | 2 | 1 |
| [`AbilityDisableIfLivingCrow`](./Enums.md) | Integer | If set to 1, the ability is disabled when a living crow is present. | 1 | 1 |
| [`AbilityEnabledAtHealthThreshold`](./Enums.md) | Integer | The health percentage at which the ability becomes enabled. | 1 | 50 |
| [`AbilityEnabledIfBasicAttackUsedThisTurn`](./Enums.md) | Integer | If set to 1, the ability is enabled if a basic attack was used this turn. | 1 | 1 |
| [`AbilityEnabledIfMovementTrapped`](./Enums.md) | Integer | If set to 1, the ability is enabled if the unit is movement-trapped. | 1 | 1 |
| [`AbilityEnabledIfNoAggroTarget`](./Enums.md) | Integer | If set to 1, the ability is enabled when the unit has no aggro target. | 1 | 1 |
| [`AbilityEnabledIfNotHasStatus`](./Enums.md) | Enum | Specifies the status that must not be present on the unit for the ability to be enabled. | 1 | BackflipWhenTargeted |
| [`AbilityEnabledIfSpecificItemEquipped`](./Enums.md) | Enum | Specifies the item that must be equipped for the ability to be enabled. | 1 | Neverstone |
| [`AbsorbManaFromOtherSpells`](./Enums.md) | Integer | If set to 1, the ability absorbs mana from other spells cast by the same unit. | 1 | 1 |
| [`AddElementsToSpells`](./Enums.md) | Enum | Specifies an element to add to all spells, altering their damage type. | 1 | Earth |
| [`AddStatusToBasicAttack`](#object-addstatustobasicattack) | Object | An object defining status effects to apply on basic attacks, with optional conditions. | 1 ||
| [`AlphaDodgeChance`](./Enums.md) | Integer | The percentage chance for the alpha cat to dodge attacks. | 1 | 50 |
| [`AlphaStatusOnTurnBegin`](#object-alphastatusonturnbegin) | Object | An object defining status effects applied to the alpha cat at the start of each turn. | 1 ||
| [`BonusAbility_DelayedApplication`](./Enums.md) | Enum | Specifies a bonus ability that is applied after a delay, such as Slap. | 1 | Slap |
| [`CapTechSpent`](./Enums.md) | Integer | The maximum amount of tech points that can be spent, capping resource usage. | 1 | 1 |
| [`CaveWomanBirthControl`](./Enums.md) | Integer | If set to 1, prevents the Cave Woman birth mechanic from triggering. | 1 | 1 |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance increase, in percentage points. | 1 | 2 |
| [`FistOfFateUniqueEnemyTracker`](./Enums.md) | Integer | If set to 1, tracks unique enemies for the Fist of Fate mechanic. | 1 | 1 |
| [`FreeFirstCastAndAfterSpendMana`](./Enums.md) | Integer | If set to 1, the first cast is free and after spending mana, the next cast is also free. | 1 | 1 |
| [`FreeFirstCastEachMatch`](./Enums.md) | Integer | If set to 1, the first cast of the ability each match is free. | 1 | 1 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 1 | 2 |
| [`IgnoreTiles`](./Enums.md) | Integer | If set to 1, the unit ignores tile effects while moving. | 1 | 1 |
| [`IntelligenceUp`](./Enums.md) | Enum / Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. | 1 | item_aux |
| [`InterchangeDisabler`](./Enums.md) | Integer | If set to 1, disables the Interchange ability on this unit. | 1 | 1 |
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit is immune to knockback effects. | 1 | 1 |
| [`PassiveWhileNotTakingTurn`](#object-passivewhilenottakingturn) | Object | An object defining passives that are active only when the unit is not taking its turn. | 1 ||
| [`ReloadOnAllyCatDies`](./Enums.md) | Integer | The number of times the Reload mechanic is triggered when an ally cat dies. | 1 | 1 |
| [`ReloadOnAllyDies`](./Enums.md) | Integer | The number of times the Reload mechanic is triggered when any ally dies. | 1 | 1 |
| [`ReloadOnAnyDamage`](./Enums.md) | Integer | The number of times the Reload mechanic is triggered each time the unit takes damage. | 1 | 1 |
| [`ReloadOnBackstab`](./Enums.md) | Integer | The number of times the Reload mechanic is triggered when landing a backstab. | 1 | 1 |
| [`ReloadOnElementalDamageReceived`](./Enums.md) | Enum | Specifies the element that, when received as damage, triggers a reload of this ability's magazine. | 1 | Holy |
| [`ReloadOnGainCoins`](./Enums.md) | Integer | The number of times the Reload mechanic is triggered when the unit gains coins. | 1 | 1 |
| [`ReloadOnGainDivineShield`](./Enums.md) | Integer | The number of times the Reload mechanic is triggered when the unit gains a Divine Shield. | 1 | 1 |
| [`ReloadOnKillTagged`](./Enums.md) | Enum | Specifies the tag of enemies that, when killed, trigger a reload of this ability's magazine. | 1 | rock |
| [`ReloadOnSpendMana`](./Enums.md) | Integer | The number of times the Reload mechanic is triggered when the unit spends mana. | 1 | 1 |
| [`ReloadOnUseAbilityWithManaCost`](./Enums.md) | Integer | The number of times the Reload mechanic is triggered when the unit uses an ability that costs mana. | 1 | 6 |
| [`RevengeDamage`](#object-revengedamage) | Object | An object specifying the effects (e.g., Marked, Charmed, Petrify) applied to the attacker when the unit takes damage. | 1 ||
| [`StatusKillers`](#object-statuskillers) | Object | An object defining status effects applied to enemies upon killing them, with possible conditional blocks for boss or non-boss targets. | 1 ||
| [`TossTargetIsAggroTarget`](./Enums.md) | Integer | If set to 1, the toss ability's target is the unit's current aggro target. | 1 | 1 |
| [`TossTargetIsBuddy`](./Enums.md) | Integer | If set to 1, the toss ability's target is a buddy (friendly) character. | 1 | 1 |
| [`TossTargetIsNotInWater`](./Enums.md) | Integer | If set to 1, the toss ability cannot target characters standing in water. | 1 | 1 |
| [`Trample`](./Enums.md) | Integer | The number of tiles this character can move through enemies, dealing damage or applying effects equal to the value. | 1 | 3 |
| [`XIsConsumedCharacterMaxHP`](./Enums.md) | Integer | The amount of bonus damage or effect scaling based on the consumed character's maximum HP. | 1 | 3 |
| [`XIsCountDeaths`](./Enums.md) | Integer | If set to 1, the X variable counts the number of deaths (e.g., for scaling). | 1 | 1 |
| [`XIsCountStatusStacks`](./Enums.md) | Enum | Specifies a status effect whose stacks are counted as the X variable. | 1 | DodgeChance_Status |
| [`XIsFormulaLockedUntilComplete`](./Enums.md) | Enum | Specifies a stat (e.g., dex) whose value is locked in as the X formula until the ability completes. | 1 | dex |
| [`XIsIncreaseEachTurn`](./Enums.md) | Integer | The amount by which X increases each turn. | 1 | 1 |
| [`XIsRampAndReset`](./Enums.md) | Integer | If set to 0, X ramps and does not reset; if set to 1, X ramps and resets each combat. | 1 | 0 |
| [`XIsRecycleCostReduction`](./Enums.md) | Integer | The amount of cost reduction (e.g., mana) applied when recycling an ability. | 1 | 5 |
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
| [`Trample`](./Enums.md) | Integer | The number of tiles this character can move through enemies, dealing damage or applying effects equal to the value. | 26 | 3 |
| `CastAgain` | Integer / String | Applies or references the 'CastAgain' effect/state. | 20 ||
| `DisableTrample` | Integer | Applies or references the 'DisableTrample' effect/state. | 10 ||
| `Fury` | Integer | Applies or references the 'Fury' effect/state. | 7 ||
| [`TileTrail`](./Enums.md) | Enum | Specifies the tile type (e.g., CreepTile, WaterTile) left behind as the character moves. | 6 | FloatingGlassTile |
| `JustInCaseTrample` | Integer | Applies or references the 'JustInCaseTrample' effect/state. | 5 ||
| [`LeaveBehind`](#object-leavebehind) | Enum / Object | Spawns a specific object at the character's previous location when they move. | 5 ||
| `DashFury` | Integer | Applies or references the 'DashFury' effect/state. | 3 ||
| `BearTrapTrail` | Integer | Applies or references the 'BearTrapTrail' effect/state. | 2 ||
| [`AfterImage`](#object-afterimage) | Object | An object defining an afterimage entity (e.g., PlayerCat_ThiefShade) that appears when the character moves. | 2 ||
| `DelayedWindTrail` | Integer | Applies or references the 'DelayedWindTrail' effect/state. | 1 ||
| [`JumpAttackLeaveBehind`](./Enums.md#enum-jumpattackleavebehind) | Enum | Applies or references the 'JumpAttackLeaveBehind' effect/state. | 1 ||
| [`DoubleLoot`](./Enums.md) | Integer | The number of extra loot rolls or items granted when looting. | 1 | 2 |
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit is immune to knockback effects. | 1 | 1 |
| [`TileTrail_Ahead`](./Enums.md) | Enum | Specifies the tile type placed on the tile ahead of the character's movement direction. | 1 | FlowerTile |
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
| [`Cleanse`](./Enums.md) | Integer | If set to 1, removes all status effects from the target; if 0, no cleanse. | 2 | 0 |
| [`Confusion`](./Enums.md) | Array / Integer | The number of turns of Confusion applied, or an array with duration and chance. | 2 | [.1] |
| [`GainCoinsRange`](#object-gaincoinsrange) | Object | An object with min and max values defining the range of coins gained. | 2 ||
| [`RandomStatUp`](./Enums.md) | Enum / Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 2 | ceil(X/3) |
| [`Revive`](./Enums.md) | Integer | The percentage or flat amount of HP restored when reviving a dead ally. | 2 | 50 |
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
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | 2 |
| [`Bruise`](./Enums.md) | Array / Integer | The number of Bruise stacks applied, or an array with duration and chance. | 1 | [.1] |
| [`Charmed`](./Enums.md) | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. | 1 | [.1] |
| [`Cleave`](#object-cleave) | Integer / Object | If an integer, the number of cleave hits; if an object, may contain a chance for cleave. | 1 | 1 |
| [`Conditional_HasTag`](#object-conditional_hastag) | Object | An object that executes inner effects if the target has the specified tag, else falls back. | 1 ||
| [`Conditional_Object`](#object-conditional_object) | Object | An object that provides conditional branching based on object type (e.g., inanimate). | 1 ||
| [`Conditional_Speculative`](#object-conditional_speculative) | Object | An object that checks a speculative condition (e.g., health threshold) and applies effects accordingly. | 1 ||
| [`ConstitutionUp`](./Enums.md) | Array / Enum / Integer | The amount of Constitution (HP) increase, or an array with duration and chance. | 1 | [.5] |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance increase, in percentage points. | 1 | 2 |
| [`DamageUp`](./Enums.md) | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 1 | 3 |
| [`DodgeChance_Status`](./Enums.md) | Integer | The percentage of dodge chance granted by this status effect. | 1 | 50 |
| [`DybbukPossessed`](#object-dybbukpossessed) | Object | An object configuring the Dybbuk possession effect, including exit and punch-self abilities. | 1 ||
| [`Else`](#object-else) | Object | An object containing effects that apply when the parent conditional condition is not met. | 1 ||
| [`Immobile`](./Enums.md) | Array / Integer | The number of turns of Immobile applied, or an array with duration and chance. | 1 | [.1] |
| [`Leeches`](./Enums.md) | Integer | The number of Leech stacks applied, healing the attacker. | 1 | 2 |
| [`ObjectOnHitCharacter`](#object-objectonhitcharacter) | Enum / Object | An object or entity name that spawns upon hitting a character, with optional stacks and chance. | 1 | SkeletonCatFamiliar |
| [`PartialCleanse`](./Enums.md) | Integer | The number of status effects removed from the target (partial cleanse). | 1 | 9999 |
| [`ScatterCoins`](#object-scattercoins) | Object | The number of coins scattered, or an object with stacks and stacking behavior. | 1 ||
| [`Slow`](./Enums.md) | Array / Enum / Integer | The number of turns of Slow applied, or an array with duration and chance. | 1 | [.1] |
| [`SpeedUp`](./Enums.md) | Enum / Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 1 | 4 |

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
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 6 | 2 |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 6 | 5 |
| [`StrengthUp`](./Enums.md) | Enum / Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 6 | max(int, 0) |
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 5 | 2*X |
| [`EvolveAbilityFromPool`](./Abilities_and_Spells.md#object-evolveabilityfrompool) | `String` | Upgrades or transforms an existing ability into a new one from the specified pool. | 4 ||
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | `String` | Transforms the character into a different state or form (e.g., Rage, HasCat). | 4 ||
| [`AddWeaponAux`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'AddWeaponAux' effect/state. | 3 ||
| [`Craft`](#object-craft) | Object | Synthesizes or spawns a new item from a specific pool. | 3 ||
| `RefreshActPoints` | `Number` | Applies or references the 'RefreshActPoints' effect/state. | 3 ||
| [`ConstitutionUp`](./Enums.md) | Array / Enum / Integer | The amount of Constitution (HP) increase, or an array with duration and chance. | 3 | [.5] |
| `AddLeechesStatus` | `Number` | Applies or references the 'AddLeechesStatus' effect/state. | 2 ||
| [`DoDamage`](#object-dodamage) | Object | Explicitly triggers a secondary damage instance independent of the main attack. | 2 ||
| [`Cleanse`](./Enums.md) | Integer | If set to 1, removes all status effects from the target; if 0, no cleanse. | 2 | 0 |
| [`EquipPermanentItem`](./Enums.md) | Enum | Determines which permanent item (e.g., a body part or bone club) is equipped to the source. | 2 | BoneClub |
| [`FindItemFromPool`](#object-finditemfrompool) | Object | Determines the item pool name from which a random item is granted to the source. | 2 ||
| [`FreeSpell`](./Enums.md) | Integer | The number of free spells granted, allowing the source to cast spells without consuming mana or charges. | 2 | 2 |
| [`LuckUp`](./Enums.md) | Enum / Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 2 | 2 |
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
| [`Brace`](./Enums.md) | Integer | The amount of flat damage reduction applied to the source. | 1 | 2 |
| [`Bruise`](./Enums.md) | Array / Integer | The number of Bruise stacks applied, or an array with duration and chance. | 1 | [.1] |
| [`DivineShield`](./Enums.md) | Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 2 |
| [`FindItem`](./Enums.md) | Enum | Determines which specific item (e.g., Molars, Pearl) is granted to the source. | 1 | Molars |
| [`ForceUseAbility`](./Enums.md) | Enum | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 1 | MotherTumorGrow |
| [`GainCoinsRange`](#object-gaincoinsrange) | Object | An object with min and max values defining the range of coins gained. | 1 ||
| [`KineticSpikes`](./Enums.md) | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 1 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | Specifies the number of bonus movement points granted; an array `[stacks, probability]` specifies the amount and its chance of application. | 1 | 1 |
| [`Tech`](./Enums.md) | Integer | The number of Tech stacks applied, which increase the damage of the next ability used. | 1 | 3 |

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
| [`tag`](./Enums.md) | Enum | Specifies the name of the tag to check for on the target. | 46 | megadino |
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
| [`ChangeTilesUnder`](./Enums.md) | Enum | Determines which tile type (e.g., GlassTile, DirtTile) replaces the tiles beneath the target. | 2 | LavaTile |
| [`DamageUp`](./Enums.md) | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 2 | 3 |
| [`Else`](#object-else) | Object | An object containing effects that apply when the parent conditional condition is not met. | 2 ||
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
| [`EventBounty`](./Enums.md) | Integer | The number of Event Bounty stacks applied, which increases the chance of encountering special events or loot drops. | 1 | 5 |
| [`MergeDamageInstance`](#object-mergedamageinstance) | Object | Contains properties that control whether the current damage instance merges with an existing one and whether it plays a hit animation. | 1 ||
| [`SetAnimationAlts`](#object-setanimationalts) | Object | Maps animation state names (e.g., dying, dead) to alternate animation clips to use instead. | 1 ||

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
| [`Confusion`](./Enums.md) | Array / Integer | The number of turns of Confusion applied, or an array with duration and chance. | 9 | [.1] |
| [`Conditional_NotBoss`](#object-conditional_notboss) | Object | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 3 ||
| [`DisplaceToAbilityTarget`](./Enums.md) | Integer | If set to 1, the unit is teleported to the position of the ability's primary target after the effect resolves. | 3 | 1 |
| `TakeExtraTurn` | `Number` | Applies or references the 'TakeExtraTurn' effect/state. | 2 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 2 | 2 |
| [`Attraction`](./Enums.md) | Integer | If set to 1, the target is pulled one tile toward the source of the effect. | 2 | 1 |
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | [.3] |
| [`Madness`](#object-madness) | Array / Enum / Integer / Object | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. | 2 | [.1] |
| [`Stun`](./Enums.md) | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | [0] |
| [`Weakness`](./Enums.md) | Array / Integer | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | [.1] |
| [`ApplyToSource`](#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 ||
| [`ApplyToSourceOnKill`](#object-applytosourceonkill) | Object | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 1 ||
| `BonusDamage` | `Number` | Applies or references the 'BonusDamage' effect/state. | 1 ||
| `ForceMoveTowards` | `Number` | Applies or references the 'ForceMoveTowards' effect/state. | 1 ||
| [`Temporary`](#object-temporary) | Object | A wrapper object for applying status effects that automatically expire. | 1 ||
| [`Burn`](./Enums.md) | Array / Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 1 | [.1] |
| [`Charmed`](./Enums.md) | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. | 1 | [.1] |
| [`Conditional_FinishedSpawning`](#object-conditional_finishedspawning) | Object | Contains sub-effects that trigger only after all units have finished spawning on the battlefield. | 1 ||
| [`Doomed`](./Enums.md) | Integer | The number of turns until the target is instantly killed when this counter reaches zero. | 1 | 3 |
| [`Hex`](./Enums.md) | Integer | The number of Hex stacks applied, which increases the chance of negative status effects landing on the target. | 1 | 1 |
| [`Marked`](./Enums.md) | Array / Integer | The number of Marked stacks applied, which increases damage taken from all sources; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.1] |
| [`PermanentCharm`](./Enums.md) | Integer | If set to 1, the target is permanently charmed and becomes an ally; can use an alias for the status. | 1 | 1 |
| [`Poison`](./Enums.md) | Array / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.1] |
| [`TempDamageUp`](./Enums.md) | Integer | The number of temporary damage increase stacks applied to the target for the current turn. | 1 | 2 |

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
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the owning unit's turn. | 21 ||
| `data` | Integer | An integer value used to store auxiliary data for the temporary effect, such as the number of times a triggered effect can still fire. | 2 ||
| `expires_on_appliers_turn` | Boolean | If true, the temporary effect expires at the end of the applier's next turn. | 2 ||
| `expires_on_move` | Boolean | If true, the temporary effect expires as soon as the affected unit moves from its current tile. | 1 ||

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
| [`ontrigger`](./Enums.md#enum-ontrigger) | Enum | Specifies the sound cue to play when the ability's trigger condition is met (e.g., on hit or on effect activation). | 32 ||
| [`oncast`](./Enums.md#enum-oncast) | Enum | Specifies the sound cue to play when the ability is cast. | 3 ||
| [`oncastpoint`](./Enums.md#enum-oncastpoint) | Enum | Specifies the sound cue to play at the cast point of the animation (e.g., the moment a swing connects). | 3 ||
| [`ontrigger_intentional`](./Enums.md#enum-ontrigger_intentional) | Enum | Specifies the sound cue to play when the ability is triggered intentionally (e.g., a targeted ability vs. a passive proc). | 1 ||

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
| [`DamageUp`](./Enums.md) | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 5 | 3 |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 4 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 4 | 2 |
| `KnockbackDamageImmuneUntilSettled` | `Number` | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. | 3 ||
| [`Temporary`](#object-temporary) | Object | A wrapper object for applying status effects that automatically expire. | 3 ||
| [`Cleanse`](./Enums.md) | Integer | If set to 1, removes all status effects from the target; if 0, no cleanse. | 3 | 0 |
| [`ApplyToSource`](#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 2 ||
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 2 | 5 |
| [`RandomStatUp`](./Enums.md) | Enum / Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 2 | ceil(X/3) |
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
| [`BleedThorns`](./Enums.md) | Integer | The number of Bleed Thorns stacks applied, which deals bleeding damage back to melee attackers. | 1 | 3 |
| [`Charmed`](./Enums.md) | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. | 1 | [.1] |
| [`TempDamageUp`](./Enums.md) | Integer | The number of temporary damage increase stacks applied to the target for the current turn. | 1 | 2 |
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 1 | 2 |

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
| [`BonusAbility`](./Enums.md) | Enum | Determines which additional ability is granted to the character (e.g., as a passive or keyword tooltip link). | 2 | DonateEnergy |
| [`DamageUp`](./Enums.md) | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 2 | 3 |
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 2 | 2*X |
| `TemporaryItem` | Integer | Applies or references the 'TemporaryItem' effect/state. | 1 ||
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.1] |
| [`Brace`](./Enums.md) | Integer | The amount of flat damage reduction applied to the source. | 1 | 2 |
| [`Charmed`](./Enums.md) | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. | 1 | [.1] |
| [`Madness`](#object-madness) | Array / Enum / Integer / Object | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. | 1 | [.1] |
| [`PermanentMadness`](./Enums.md) | Integer | If set to 1, the Madness status is permanent and will never expire; can use an alias for the status. | 1 | 1 |
| [`RandomMagicMissile`](#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, each dealing independent damage; can also be an object with custom tooltip data. | 1 | 5 |
| [`Webbed`](./Enums.md) | Integer | The number of Webbed stacks applied, which immobilizes the target and prevents movement; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 1 |
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
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 13 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 12 ||
| `makes_contact` | `Boolean` | If true, the damage instance is considered a contact hit, which can trigger contact-based statuses like Thorns or BleedThorns. | 6 ||
| `override_trample_damage` | `Boolean` | If true, the damage instance uses its own damage value for trample calculations instead of the default ability damage. | 2 ||
| `ai_base_score` | Integer | A base priority score used by the AI to evaluate the desirability of using this ability; higher values increase the likelihood of selection. | 1 ||
| `crit_chance` | `Number` | The chance for the damage instance to critically hit, expressed as a percentage (e.g., 50%) or a decimal fraction (e.g., .5). | 1 ||
| `force_no_knockback` | `Boolean` | If true, the damage instance does not apply any knockback to the target. | 1 ||
| `force_play_hit_animation` | `Boolean` | If true, the target plays its hit reaction animation even if the attack would normally suppress it. | 1 ||
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Determines which visual or gameplay layer (e.g. "tiles", "pickups", "characters") the editor object belongs to. | 1 ||

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
| [`Else`](#object-else) | Object | An object containing effects that apply when the parent conditional condition is not met. | 4 ||
| [`VisualFX`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'VisualFX' effect/state. | 3 ||
| [`Stun`](./Enums.md) | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 3 | [0] |
| [`BonusDamage`](./Engine_LogicKeys.md#valid-property-keys) | Enum / Integer | Applies or references the 'BonusDamage' effect/state. | 2 ||
| [`Charmed`](./Enums.md) | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. | 2 | [.1] |
| [`Drowsy`](./Enums.md) | Integer | The number of stacks of the Drowsy status effect to apply, which reduces a unit's action points or turn efficiency. | 2 | 8 |
| [`ExplodeCharacter_PartyBoss`](./Enums.md) | Integer | The value representing the number of targets affected by the Party Boss explosion effect. | 2 | 5 |
| [`ExplodeCharacter_RockCrusher_PetrifyBreak`](./Enums.md) | Integer | The value indicating the damage or effect magnitude when a Rock Crusher unit explodes after its Petrify is broken. | 2 | 5 |
| `ExplodeCharacter_NoDie` | `Number` | Applies or references the 'ExplodeCharacter_NoDie' effect/state. | 1 ||
| [`XIsTargetHealth`](#object-xistargethealth) | Object | Math variable assignment: Evaluates X as the target's current health. | 1 ||
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.3] |

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
| `upgraded` | Boolean | If true, the ability evolution uses an upgraded version or state instead of the base one. | 13 ||
| [`pool`](./Enums.md) | Array / Enum | Specifies the loot pool, ability pool, or item category from which an item or effect is selected; can be a specific pool name, table index, or inline array. | 13 | [Ping] |

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
| [`stacks`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Number of stacks or intensity to apply. | 22 ||
| `height` | Integer | The maximum height in tiles that a unit is knocked up into the air (vertical displacement for knockback arcs). | 2 ||
| `circular_variance` | Integer | The radius of circular variance in tiles applied to the final landing position of a knockback effect, adding horizontal scatter. | 1 ||

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
| [`SafeDoomed`](./Enums.md) | Enum / Integer | The number of turns until the target is instantly killed when this counter reaches zero, but unlike standard Doomed, it does not inflict injuries upon death. | 11 | 2 |
| [`InjuryImmunity`](./Enums.md) | Integer | The number of stacks of InjuryImmunity, granting immunity to receiving injuries (permanent wounds) for that many instances. | 7 | 1 |
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 2 | 2 |
| [`FadeInsteadOfDie`](./Enums.md) | Integer | The number of stacks of FadeInsteadOfDie, causing the unit to fade out and despawn instead of dying when reaching zero health. | 2 | 1 |
| [`IllusionTint`](./Enums.md) | Integer | The number of stacks of IllusionTint, applying a visual tint to the unit to mark it as an illusion or summoned copy. | 2 | 1 |
| [`PermanentMadness`](./Enums.md) | Integer | If set to 1, the Madness status is permanent and will never expire; can use an alias for the status. | 2 | 1 |
| [`ApplyPassivesToSpawnerWhileAlive`](#object-applypassivestospawnerwhilealive) | Object | An object containing passive definitions that are applied to the unit that spawned this one while this unit remains alive. | 1 ||
| [`CaptureFamiliar`](./Enums.md) | Integer | The number of stacks of CaptureFamiliar, enabling the unit to capture a target as a familiar upon defeating it. | 1 | 1 |
| [`DamageUp`](./Enums.md) | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 1 | 3 |
| [`FillMana`](./Enums.md) | Integer | The amount of mana restored to the unit; can be a fixed integer or an array `[stacks, probability]` for a chance-based application. | 1 | 1 |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 1 | 5 |
| [`HideEquipment`](./Enums.md) | Enum | Specifies which equipment slot (e.g., neck) to hide visually on the unit. | 1 | neck |
| [`ReviveNextRound`](#object-revivenextround) | Integer / Object | The number of stacks of ReviveNextRound or an object defining revival properties; causes the unit to revive with specified health, shields, or buffs at the start of the next round. | 1 | 2 |
| [`SchizoIllusionAIModifier`](./Enums.md) | Integer | The number of stacks of SchizoIllusionAIModifier, causing AI-controlled illusions to behave erratically or with reduced intelligence. | 1 | 1 |
| [`SpeedUp`](./Enums.md) | Enum / Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 1 | 4 |
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
| [`BonusDamage`](./Enums.md) | Enum / Integer | The amount of bonus damage added to an attack; can be a static integer or a formula using variables like `X` or `bonus_melee_damage`. | 6 | -4 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`ApplyToSource`](#object-applytosource) | Object | An object containing status effects or modifiers applied to the source (attacker) of the triggering condition rather than the target. | 3 ||
| [`Burn`](./Enums.md) | Array / Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 2 | [.1] |
| [`RemoveStatus`](./Enums.md) | Enum | Specifies the name of a status effect to remove from the target. | 2 | Sleep |
| [`Slow`](./Enums.md) | Array / Enum / Integer | The number of turns of Slow applied, or an array with duration and chance. | 2 | [.1] |
| [`Confusion`](./Enums.md) | Array / Integer | The number of turns of Confusion applied, or an array with duration and chance. | 1 | [.1] |
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.3] |
| [`FormChange`](#object-formchange) | Enum / Object | Specifies the target form name or an object with form parameters and optional side effects (e.g., faction change, healing). | 1 | Open |
| [`Quivered`](./Enums.md) | Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 1 | 1 |

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
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 12 | 2*X |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 12 |
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 10 | 2 |
| [`DivineShield`](./Enums.md) | Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 9 | 2 |
| [`KineticSpikes`](./Enums.md) | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 9 | 2 |
| [`Poison`](./Enums.md) | Array / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 9 | [.1] |
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 8 | [.1] |
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 8 | 2 |
| [`Weakness`](./Enums.md) | Array / Integer | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 8 | [.1] |
| [`Slow`](./Enums.md) | Array / Enum / Integer | The number of turns of Slow applied, or an array with duration and chance. | 7 | [.1] |
| [`Blind`](./Enums.md) | Array / Integer | The number of stacks of Blind to apply, reducing accuracy; can be an array `[stacks, probability]` for a chance-based application. | 6 | [2] |
| [`Brace`](./Enums.md) | Integer | The amount of flat damage reduction applied to the source. | 6 | 2 |
| [`Bruise`](./Enums.md) | Array / Integer | The number of Bruise stacks applied, or an array with duration and chance. | 6 | [.1] |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of stacks of DiminishingHealthRegen, providing health regeneration each turn that decreases with each stack. | 6 | 3 |
| [`GainCoins`](./Enums.md) | Integer | The number of coins gained or lost; can be a fixed integer, a range `[min, max]`, or a negative value to deduct coins. | 6 | 2 |
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 5 | 2 |
| [`Burn`](./Enums.md) | Array / Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 5 | [.1] |
| [`MoveQuivered`](./Enums.md) | Integer | Specifies the number of bonus movement points granted; an array `[stacks, probability]` specifies the amount and its chance of application. | 5 | 1 |
| [`Quivered`](./Enums.md) | Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 5 | 1 |
| [`RandomStatUp`](./Enums.md) | Enum / Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 5 | ceil(X/3) |
| [`BleedThorns`](./Enums.md) | Integer | The number of Bleed Thorns stacks applied, which deals bleeding damage back to melee attackers. | 4 | 3 |
| [`ConstitutionUp`](./Enums.md) | Array / Enum / Integer | The amount of Constitution (HP) increase, or an array with duration and chance. | 4 | [.5] |
| [`Madness`](#object-madness) | Array / Enum / Integer / Object | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. | 4 | [.1] |
| [`MagicWeakness`](./Enums.md) | Array / Integer | The number of stacks of MagicWeakness, increasing incoming magic damage; can be an array `[stacks, probability]`. | 4 | [.1] |
| [`Marked`](./Enums.md) | Array / Integer | The number of Marked stacks applied, which increases damage taken from all sources; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 4 | [.1] |
| [`Reflect`](./Enums.md) | Integer | The number of stacks of Reflect, causing a percentage of incoming damage to be reflected back to the attacker. | 4 | 5 |
| [`SpeedUp`](./Enums.md) | Enum / Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 4 | 4 |
| [`Stun`](./Enums.md) | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 4 | [0] |
| [`Tarred`](./Enums.md) | Array / Integer | The number of stacks of Tarred, making the unit more vulnerable to fire damage; can be an array `[stacks, probability]`. | 4 | [.1] |
| [`Charmed`](./Enums.md) | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. | 3 | [.1] |
| [`Confusion`](./Enums.md) | Array / Integer | The number of turns of Confusion applied, or an array with duration and chance. | 3 | [.1] |
| [`DamageUp`](./Enums.md) | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 3 | 3 |
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 3 | [.3] |
| [`Freeze`](./Enums.md) | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. | 3 | [.1] |
| [`Immobile`](./Enums.md) | Array / Integer | The number of turns of Immobile applied, or an array with duration and chance. | 3 | [.1] |
| [`Petrify`](./Enums.md) | Array / Integer | The number of stacks of Petrify, turning the unit to stone and immobilizing it; can be an array `[stacks, probability]`. | 3 | [.15] |
| [`Sleep`](./Enums.md) | Array / Integer | The number of stacks of Sleep, putting the unit to sleep for that many turns; can be an array `[stacks, probability]`. | 3 | [.1] |
| [`StrengthUp`](./Enums.md) | Enum / Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 3 | max(int, 0) |
| [`BackflipWhenTargeted`](#object-backflipwhentargeted) | Integer / Object | The number of stacks of BackflipWhenTargeted or an object defining the dodge ability; causes the unit to perform a backflip dodge when targeted. | 2 | 2 |
| [`BonusDamage`](./Enums.md) | Enum / Integer | The amount of bonus damage added to an attack; can be a static integer or a formula using variables like `X` or `bonus_melee_damage`. | 2 | -4 |
| [`CharismaUp`](./Enums.md) | Enum / Integer | The amount of Charisma stat increased or decreased (negative values lower the stat); can be a formula or fixed integer. | 2 | -2 |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance increase, in percentage points. | 2 | 2 |
| [`DexterityUp`](./Enums.md) | Enum / Integer | The amount of Dexterity stat increased or decreased (negative values lower the stat); can be a formula or fixed integer. | 2 | 2 |
| [`DodgeChance_Status`](./Enums.md) | Integer | The percentage of dodge chance granted by this status effect. | 2 | 50 |
| [`FormChange`](#object-formchange) | Enum / Object | Specifies the target form name or an object with form parameters and optional side effects (e.g., faction change, healing). | 2 | Open |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 2 | 2 |
| [`IntelligenceUp`](./Enums.md) | Enum / Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. | 2 | item_aux |
| [`Lifesteal`](./Enums.md) | Integer | The number of stacks of Lifesteal, converting a percentage of damage dealt into healing for the attacker. | 2 | 3 |
| [`LuckUp`](./Enums.md) | Enum / Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 2 | 2 |
| [`PoisonLace`](./Enums.md) | Enum / Integer | The amount or formula for PoisonLace damage applied per turn; can be a fixed integer or a formula like `X/3`. | 2 | X/3 |
| [`RandomStatDown`](./Enums.md) | Array / Enum / Integer | The number of stacks or chance to decrease a random stat; can be an array `[stacks, probability]` or a formula. | 2 | [.25] |
| [`Rot`](./Enums.md) | Array / Integer | The number of stacks of Rot, causing damage over time and potentially spawning a fly on death; can be an array `[stacks, probability]`. | 2 | [.1] |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp, increasing spell damage dealt by the unit. | 2 | 3 |
| [`TempCounterAttack`](./Enums.md) | Integer | The number of stacks (turns) for TempCounterAttack, causing the unit to counterattack after being hit. | 2 | 1 |
| [`DelayedPain`](./Enums.md) | Integer | The number of stacks of DelayedPain, which deals damage to the unit after a delay (e.g., at the end of its next turn). | 1 | 1 |
| [`Hex`](./Enums.md) | Integer | The number of Hex stacks applied, which increases the chance of negative status effects landing on the target. | 1 | 1 |
| [`IncAuxCounterClamped`](#object-incauxcounterclamped) | Object | An object with `change` and `max` fields that modifies an auxiliary counter, clamping it between minimum and maximum values. | 1 ||
| [`Infested`](./Enums.md) | Integer | The number of stacks of Infested, causing the unit to spawn a friendly fly or swarm upon death. | 1 | 1 |
| [`ManaGain`](./Enums.md) | Enum / Integer | The amount of mana gained; can be a fixed integer or a formula using variables like `X` (e.g., damage dealt or ability cost). | 1 | 0 |
| [`Ostracized`](./Enums.md) | Integer | The number of stacks of Ostracized, making the unit unable to be targeted by ally abilities or receive allied benefits. | 1 | 2 |
| [`RefreshActPoints`](./Enums.md) | Integer | The amount of action points restored to the unit. | 1 | 1 |
| [`RefreshMovePoints`](./Enums.md) | Integer | The amount of move points restored to the unit. | 1 | 1 |
| [`Scrambled`](./Enums.md) | Integer | The number of stacks of the Scrambled status effect applied to the target. | 1 | 2 |

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
| `instant` | `Boolean` | If true, the consumption (e.g., grabbing, eating) happens instantly without animation delay. | 12 ||
| [`mount_mode`](./Engine_LogicKeys.md#valid-property-keys) | `String` | If true, treats the consumption as riding/mounting instead of eating. | 12 ||
| `do_not_pop_corpse` | `Boolean` | If true, the consumed unit's corpse is not spawned or popped into the world. | 11 ||
| [`drop_on_death`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies whether and how the consumed unit is dropped upon death. "deferred" delays the drop, "true" forces it, "false" prevents it. | 11 ||
| `wet` | `Boolean` | If true, the consuming unit is considered wet (e.g., for interactions with electricity or drying). | 8 ||
| `drop_on_self_death` | `Boolean` | If true, the consumed unit is dropped when the consumer dies. | 3 ||
| [`extra_statuses`](#object-extra_statuses) | Object | Additional generic status applications. | 3 ||
| `use_placeholder` | Boolean | If true, a placeholder graphic is used instead of the intended animation. | 3 ||
| [`drop_body_ability`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the ability used to drop the consumed unit's body. | 1 ||
| `kill_on_consume` | `Boolean` | If true, the consumed unit is killed immediately upon being consumed. | 1 ||

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
| [`CaptureFamiliar`](./Enums.md) | Integer | The number of stacks of CaptureFamiliar, enabling the unit to capture a target as a familiar upon defeating it. | 2 | 1 |
| [`Doomed`](./Enums.md) | Integer | The number of turns until the target is instantly killed when this counter reaches zero. | 2 | 3 |
| [`ExplodeCharacter_RockCrusher`](./Enums.md) | Integer | The amount of damage dealt to the target when the RockCrusher explosion triggers. | 2 | 5 |
| [`FactionConversion`](./Enums.md) | Integer | The number of stacks of the faction conversion effect (e.g., turning an enemy to an ally) applied to the target. | 2 | 1 |
| [`Vaporize`](./Enums.md) | Integer | The number of stacks of the Vaporize status effect applied to the target, which destroys it if enough stacks are applied. | 2 | 20 |
| [`VaporizeInanimate`](./Enums.md) | Integer | The number of stacks of Vaporize applied to inanimate objects. | 2 | 1 |
| [`CanApplyToInanimate`](#object-canapplytoinanimate) | Object | A block containing effects that apply when the ability targets an inanimate object. | 1 ||
| [`Conditional_HealthThreshold`](#object-conditional_healththreshold) | Object | A block containing effects that trigger only if the target's health is below a certain threshold. | 1 ||
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.3] |
| [`PermanentCharm`](./Enums.md) | Integer | If set to 1, the target is permanently charmed and becomes an ally; can use an alias for the status. | 1 | 1 |

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
| [`form`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Specifies the form name (e.g., "Big", "Small", "Angry") the unit transforms into. | 75 ||
| [`chance`](./Enums.md) | Number | A multiplier or percentage representing the probability of the effect occurring. | 1 | .02 |

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
| [`AlphaCat`](./Enums.md) | Integer | The number of stacks of the AlphaCat status effect. | 2 | 1 |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 2 | 5 |
| [`Revive`](./Enums.md) | Integer | The percentage or flat amount of HP restored when reviving a dead ally. | 2 | 50 |
| [`EvolveAbilityFromPool`](./Abilities_and_Spells.md#object-evolveabilityfrompool) | `String` | Upgrades or transforms an existing ability into a new one from the specified pool. | 1 ||
| `RefreshActPoints` | `Number` | Applies or references the 'RefreshActPoints' effect/state. | 1 ||
| `TakeExtraTurn` | `Number` | Applies or references the 'TakeExtraTurn' effect/state. | 1 ||
| [`TransformWeapon`](#object-transformweapon) | Object | Transforms the equipped weapon into another specific weapon state. | 1 ||
| [`WeaponAuxMultiplier`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'WeaponAuxMultiplier' effect/state. | 1 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | 2 |
| [`StrengthUp`](./Enums.md) | Enum / Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 1 | max(int, 0) |

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
| [`ObjectOnHitCharacter`](#object-objectonhitcharacter) | Enum / Object | An object or entity name that spawns upon hitting a character, with optional stacks and chance. | 4 | SkeletonCatFamiliar |
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
| [`palette`](./Enums.md) | Integer | Index or list of palette indices used for coloring the entity or its variations. | 17 | 6 |
| `ear1` | Integer | Sprite variant ID for the front ear. | 13 ||
| [`tail`](./Enums.md) | Integer | The visual ID (integer) of the tail part applied to the cat. | 13 | 1042 |
| [`arm2`](./Enums.md) | Number | The visual ID (integer/number) of the second arm part applied to the cat. | 11 | 1013 |
| `ear2` | Integer | The visual ID (integer) of the second ear part applied to the cat. | 10 ||
| [`arm1`](./Enums.md) | Number | The visual ID (integer/number) of the first arm part applied to the cat. | 10 | 1013 |
| [`leg1`](./Enums.md) | Integer | The visual ID (integer) of the first leg part applied to the cat. | 8 | 338 |
| [`leg2`](./Enums.md) | Integer | The visual ID (integer) of the second leg part applied to the cat. | 8 | 338 |
| [`mouth`](./Enums.md) | Number | The visual ID (number) of the mouth part applied to the cat. | 8 | 1005 |
| [`head`](./Enums.md) | Integer | The visual ID (integer) of the head part applied to the cat. | 6 | 12 |
| [`texture`](./Enums.md) | Integer | The visual ID (integer) of the texture applied to the cat. | 6 | 1008 |
| [`body`](./Enums.md) | Number | The visual ID (number) of the body part applied to the cat. | 5 | 1029 |
| `eye1` | Integer | The visual ID (integer) of the first eye part applied to the cat. | 3 ||
| `eye2` | Integer | The visual ID (integer) of the second eye part applied to the cat. | 3 ||
| `eyebrow1` | Integer | The visual ID (integer) of the first eyebrow part applied to the cat. | 1 ||
| `eyebrow2` | Integer | The visual ID (integer) of the second eyebrow part applied to the cat. | 1 ||

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
| [`tile`](./Enums.md) | Array / Enum | Specifies the tile type(s) to change to (e.g., RoadTile, WaterTile). Can be a single tile or an array of tiles. | 12 | [BrambleTile] |
| `aoe` | Integer | The radius of the area-of-effect for the tile change. | 2 ||
| [`chance`](./Enums.md) | Number | A multiplier or percentage representing the probability of the effect occurring. | 2 | .02 |

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
| [`Else`](#object-else) | Object | An object containing effects that apply when the parent conditional condition is not met. | 1 ||
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is knocked back. | 1 | 5 |

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
| `intensity` | Integer | The intensity value of the screen shake effect. | 10 ||
| [`time`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Variable | The duration (in seconds or a float multiplier) of the screen shake effect. | 10 ||

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
| [`ability`](./Enums.md) | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 11 | MoonHandDrop |
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
| [`Revive`](./Enums.md) | Integer | The percentage or flat amount of HP restored when reviving a dead ally. | 7 | 50 |
| `TakeExtraTurn` | Integer | Applies or references the 'TakeExtraTurn' effect/state. | 2 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 2 | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Conditional_Enemy`](#object-conditional_enemy) | Object | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 1 ||
| `FlatAIBonus` | `Number` | Applies or references the 'FlatAIBonus' effect/state. | 1 ||
| [`HealRandomInjury`](./Enums.md) | Integer | The number of random injuries healed on the target. | 1 | 1 |
| [`PermanentCharm`](./Enums.md) | Integer | If set to 1, the target is permanently charmed and becomes an ally; can use an alias for the status. | 1 | 1 |

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
| [`StatusOnBattleEnd`](#object-statusonbattleend) | Object | A block containing status effects or passives that are applied to the unit when a battle ends. | 5 ||
| [`AddTag`](./Enums.md) | Enum | Specifies a unit tag (e.g., fetus, plant, bug) to add to the unit. | 2 | squirrel |
| [`Flying`](./Enums.md) | Integer | The number of stacks of the Flying status effect applied to the unit. | 2 | 1 |
| [`IgnoreTiles`](./Enums.md) | Integer | If set to 1, the unit ignores tile effects while moving. | 2 | 1 |
| [`YOffset`](./Enums.md) | Number | A vertical offset multiplier used to adjust the unit's visual position on the tile. | 2 | .25 |
| [`ElementImmune`](./Enums.md) | Enum | Specifies an element (e.g., Fire, Ice) the unit is immune to. | 1 | Creep |
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit is immune to knockback effects. | 1 | 1 |
| [`Plant`](./Enums.md) | Integer | The number of stacks of the Plant status effect applied to the unit. | 1 | 1 |
| [`ReplaceBasicAttack`](./Enums.md) | Enum | Specifies the name of the ability that replaces the unit's basic attack. | 1 | BasicPuke |

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
| [`Burn`](./Enums.md) | Array / Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 2 | [.1] |
| [`Immobile`](./Enums.md) | Array / Integer | The number of turns of Immobile applied, or an array with duration and chance. | 2 | [.1] |
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 2 | 2*X |
| [`OverrideKnockbackDamage`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'OverrideKnockbackDamage' effect/state. | 1 ||
| [`Freeze`](./Enums.md) | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. | 1 | [.1] |
| [`Slow`](./Enums.md) | Array / Enum / Integer | The number of turns of Slow applied, or an array with duration and chance. | 1 | [.1] |
| [`SpeedUp`](./Enums.md) | Enum / Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 1 | 4 |
| [`Stun`](./Enums.md) | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [0] |

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
| [`pool`](./Enums.md) | Array / Enum | Specifies the loot pool, ability pool, or item category from which an item or effect is selected; can be a specific pool name, table index, or inline array. | 15 | [Ping] |
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Specifies the equipment slot(s) to craft into (e.g., weapon, neck, face). Can be an integer index or an array of slot names. | 14 ||
| `temporary` | Boolean | If true, the crafted item is temporary and will be removed after use or at end of battle. | 4 ||
| `works_with_tech` | Boolean | If true, the craft ability can be used in technological (non-organic) crafting contexts. | 4 ||

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
| [`ApplyToSource`](#object-applytosource) | Object | An object containing status effects or modifiers applied to the source (attacker) of the triggering condition rather than the target. | 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 3 | [.1] |
| [`LuckUp`](./Enums.md) | Enum / Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 1 | 2 |

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
| [`threshold_expr`](./Math_Equations.md) | Equation | An equation that determines the health threshold condition, evaluated with auxiliary values. | 1 ||
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
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance increase, in percentage points. | 1 | 2 |
| [`DamageUp`](./Enums.md) | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 1 | 3 |
| [`DodgeChance_Status`](./Enums.md) | Integer | The percentage of dodge chance granted by this status effect. | 1 | 50 |
| [`SpeedUp`](./Enums.md) | Enum / Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 1 | 4 |

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
| [`Adrenaline`](./Enums.md) | Integer | The amount of adrenaline the player cat has, used as a condition threshold. | 1 | 10 |
| [`Cleanse`](./Enums.md) | Integer | If set to 1, removes all status effects from the target; if 0, no cleanse. | 1 | 0 |
| [`Scrambled`](./Enums.md) | Integer | The number of stacks of the Scrambled status effect applied to the target. | 1 | 2 |

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
| `immediate` | Boolean | If true, the forced attack executes immediately without waiting. | 2 ||

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
| [`ability`](./Enums.md) | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 7 | MoonHandDrop |

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
| [`Else`](#object-else) | Object | An object containing effects that apply when the parent conditional condition is not met. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`CanApplyToInanimate`](#object-canapplytoinanimate) | Object | Modifier object that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 1 ||
| [`RepairWeapon`](./Enums.md) | Integer | The number of stacks of RepairWeapon applied (or an array [stacks, probability] for random application). | 1 | 99 |

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
| `intensity` | Integer | The intensity value of the screen shake effect. | 6 ||
| `radius` | Array / Integer | Distance or area of effect in tiles. | 6 ||
| [`speed`](./Enums.md) | Array / Number | The movement speed of the projectile or graphic, as a single number or a range [min max]. | 6 | [1.0] |

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
| [`banned_abilities`](./Arrays.md#array-banned_abilities) | Array | An array of ability names that are banned from being randomly selected by Metronome. | 1 ||

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
| `crossfade_speed` | Integer | The speed of the crossfade transition when switching music. | 1 ||

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
| [`damage`](./Abilities_and_Spells.md#object-damage) | Variable | The damage formula or inherit flag. | 6 ||
| `max_dist` | Integer | Maximum displacement distance. | 6 ||
| `min_dist` | Integer | Minimum displacement distance. | 2 ||
| [`exclude_prefix`](./Enums.md#enum-exclude_prefix) | Enum | Specifies the prefix of abilities to exclude from displacement targeting. | 1 ||

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
| [`Tech`](./Enums.md) | Integer | The number of Tech stacks applied, which increase the damage of the next ability used. | 2 | 3 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `CurrentWeaponAddPoison` | Integer | Applies or references the 'CurrentWeaponAddPoison' effect/state. | 1 ||
| [`LuckUp`](./Enums.md) | Enum / Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 1 | 2 |
| [`Quivered`](./Enums.md) | Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 1 | 1 |
| [`RandomStatUp`](./Enums.md) | Enum / Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 1 | ceil(X/3) |
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 1 | 2*X |

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
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum | Determines which tiles are damaged by the effect (e.g., 'all'). | 4 ||
| [`effects`](#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 4 ||
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 2 ||

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
| [`chance`](./Enums.md) | Number | A multiplier or percentage representing the probability of the effect occurring. | 1 | .02 |

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
| [`DamageUp`](./Enums.md) | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 2 | 3 |
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | 2 |
| [`BonusDamage`](./Enums.md) | Enum / Integer | The amount of bonus damage added to an attack; can be a static integer or a formula using variables like `X` or `bonus_melee_damage`. | 1 | -4 |
| [`DivineShield`](./Enums.md) | Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 2 |
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
| [`key`](./Enums.md#enum-key) | Enum | A unique identifier string that marks this condition as one-time per battle. | 3 ||
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
| [`Burn`](./Enums.md) | Array / Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 1 | [.1] |
| [`Poison`](./Enums.md) | Array / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.1] |
| [`Tarred`](./Enums.md) | Array / Integer | The number of stacks of Tarred, making the unit more vulnerable to fire damage; can be an array `[stacks, probability]`. | 1 | [.1] |

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
| [`ability`](./Enums.md) | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 4 | MoonHandDrop |

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
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 3 | 2*X |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 2 ||
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 2 | 2 |
| [`DivineShield`](./Enums.md) | Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 2 |
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
| [`speed`](./Enums.md) | Array / Number | The movement speed of the projectile or graphic, as a single number or a range [min max]. | 4 | [1.0] |

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
| [`Madness`](#object-madness) | Array / Enum / Integer / Object | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. | 3 | [.1] |
| [`Stun`](./Enums.md) | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | [0] |
| [`TempNoManaRegen`](./Enums.md) | Integer | The number of turns for which mana regeneration is suppressed. | 2 | 1 |
| [`Confusion`](./Enums.md) | Array / Integer | The number of turns of Confusion applied, or an array with duration and chance. | 1 | [.1] |
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
| [`MeleeRevengeDamage`](#object-meleerevengedamage) | Object | A damage instance object that triggers when the unit is hit by melee attacks while this passive is active. | 2 ||
| [`AddManaRegen`](./Enums.md) | Integer | The amount of additional mana regeneration per turn granted while this passive is active. | 1 | 5 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 1 | 2 |
| [`ReplaceSpell`](#object-replacespell) | Object | An object that specifies a spell slot and an ability to replace it with while the passive is active. | 1 ||

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
| [`delay`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Variable | The float time delay in seconds. | 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`SwitchMusic`](#object-switchmusic) | Object | Changes the background music track or layer during combat. | 2 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`DoScreenShake`](#object-doscreenshake) | Integer / Object | Triggers a camera screen shake effect. | 1 ||
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | `String` | Transforms the character into a different state or form (e.g., Rage, HasCat). | 1 ||
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 1 ||
| [`GlobalSpawnCharacter`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'GlobalSpawnCharacter' effect/state. | 1 ||
| `PlayBackground` | `Number` | Applies or references the 'PlayBackground' effect/state. | 1 ||
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 1 ||
| [`Cleanse`](./Enums.md) | Integer | If set to 1, removes all status effects from the target; if 0, no cleanse. | 1 | 0 |
| [`CreateGlobalModifiers`](#object-createglobalmodifiers) | Object | An object containing global modifier effects to apply after the time delay. | 1 ||
| [`RemoveAmbientLightEffects`](./Enums.md) | Number | The duration or amount of ambient light effect removal applied over time. | 1 | .5 |

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
| [`stacks`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | The number of times the nested effects block should be repeatedly executed. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`RandomStatusFromPool`](#object-randomstatusfrompool) | Object | An object listing possible status effects to randomly pick from and apply. | 3 ||
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
| [`chance`](./Enums.md) | Number | A multiplier or percentage representing the probability of the effect occurring. | 2 | .02 |
| `slide` | Integer | The distance in tiles the bounced object slides after contact. | 1 ||

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
| [`BonusCritChance`](./Enums.md) | Integer | The percentage increase in critical hit chance when the target is affected by the specified element. | 2 | 100 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Burn`](./Enums.md) | Array / Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 1 | [.1] |
| [`Conditional_Speculative`](#object-conditional_speculative) | Object | An object that checks a speculative condition (e.g., health threshold) and applies effects accordingly. | 1 ||

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
| [`Bruise`](./Enums.md) | Array / Integer | The number of Bruise stacks applied, or an array with duration and chance. | 1 | [.1] |

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
| `change` | Integer | The amount to change an auxiliary counter by, clamped within min/max bounds. | 3 ||
| `max` | Integer | The maximum value that the auxiliary counter can reach. | 3 ||

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
| [`weights`](./Arrays.md#array-weights) | Array / Enum | An array of three weighting values or a named preset for Crazy Eye background behavior weights. | 3 ||

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
| [`RandomMutation`](./Enums.md) | Integer | The number of random mutations to apply. | 9 | 3 |
| [`RandomTaggedMutation`](./Enums.md) | Enum | Specifies a tag filter to restrict random mutations to those with that tag. | 2 | bird |

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
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 30 | [.1] |
| [`Bruise`](./Enums.md) | Array / Integer | The number of Bruise stacks applied, or an array with duration and chance. | 12 | [.1] |

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
| [`object`](./Enums.md) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 2 | [TallSkeletonCat] |

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
| [`ability`](./Enums.md) | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 9 | MoonHandDrop |
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
| [`ability`](./Enums.md) | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | MoonHandDrop |

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
| [`Conditional_InForm`](#object-conditional_inform) | Object | A conditional block that applies effects only when the buddy is in a specific form. | 1 ||
| [`Consumed`](#object-consumed) | Object | An object defining behavior when a buddy is consumed, including instant kill or status application. | 1 ||
| [`Else`](#object-else) | Object | An object containing effects that apply when the parent conditional condition is not met. | 1 ||

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
| [`LaunchOffScreen`](./Enums.md) | String | An expression that calculates the distance (in tiles) to launch the target off-screen, based on damage formula. | 1 | 10+bonus_melee_ability_damage |
| [`LaunchOffScreenInstakill`](./Enums.md) | Integer | If set to 1, instantly kills the target when launched off-screen. | 1 | 1 |
| [`TempInitiativeChange`](./Enums.md) | Integer | The amount of temporary initiative change applied to the displaced unit. | 1 | -100 |
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
| [`PartialCleanse`](./Enums.md) | Integer | The number of status effects removed from the target (partial cleanse). | 1 | 9999 |

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
| [`Confusion`](./Enums.md) | Array / Integer | The number of turns of Confusion applied, or an array with duration and chance. | 1 | [.1] |
| [`Temporary`](#object-temporary) | Object | An object that defines a temporary status effect with duration and expiration conditions. | 1 ||
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
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is knocked back. | 2 | 5 |
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
| [`ability`](./Enums.md) | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | MoonHandDrop |

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
| `upgraded` | Boolean | If true, the ability evolution uses an upgraded version or state instead of the base one. | 1 ||

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
| [`BloodRain`](./Enums.md) | Integer | If set to 1, enables a blood rain visual effect globally. | 3 | 1 |
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
| [`chance`](./Enums.md) | Number | A multiplier or percentage representing the probability of the effect occurring. | 1 | .02 |

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
| [`speed`](./Enums.md) | Array / Number | The movement speed of the projectile or graphic, as a single number or a range [min max]. | 3 | [1.0] |

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
| [`Stun`](./Enums.md) | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 2 | [0] |
| [`ApplyToSource`](#object-applytosource) | Object | An object containing status effects or modifiers applied to the source (attacker) of the triggering condition rather than the target. | 1 ||
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
| [`self_damage`](#object-self_damage) | Object | A damage instance object that applies damage and effects to the source unit itself. | 2 ||
| [`damage_instance`](#object-damage_instance) | Object | A damage instance object that defines the damage, type, effects, and AI scoring for an ability. | 1 ||
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
| `stack_scale` | Integer | If non-zero, scales the conversion of overheal to status stacks by this factor. | 1 ||
| [`RandomStatUp`](./Enums.md) | Enum / Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 1 | ceil(X/3) |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the unit. | 1 | 1 |

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
| [`chance`](./Enums.md) | Number | A multiplier or percentage representing the probability of the effect occurring. | 2 | .02 |

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
| `upgraded` | Boolean | If true, the ability evolution uses an upgraded version or state instead of the base one. | 1 ||

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
| [`ability`](./Enums.md) | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | MoonHandDrop |
| `same_orientation` | Boolean | If true, the team-cast ability is executed with the same facing orientation as the caster. | 1 ||

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
| [`DoubleCastSpellThisTurn`](./Enums.md) | Integer | If set to 1, allows the unit to cast spells twice this turn. | 1 | 1 |

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
| [`HideEquipment`](./Enums.md) | Enum | Specifies which equipment slot (e.g., neck) to hide visually on the unit. | 1 | neck |

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
| [`Quivered`](./Enums.md) | Integer | The number of stacks of Quivered, which grants bonus attacks; can be an array [stacks, probability]. | 1 | 1 |

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
| [`DestroyEquipmentAndAttachParasite`](#object-destroyequipmentandattachparasite) | Object | An object that destroys a piece of equipment and attaches a parasite from a specified pool, with optional chance. | 1 ||
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
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | [.3] |
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
| [`DestroyEquipmentAndAttachParasite`](#object-destroyequipmentandattachparasite) | Object | An object that destroys a piece of equipment and attaches a parasite from a specified pool, with optional chance. | 1 ||
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
| [`ApplyToSource`](#object-applytosource) | Object | An object containing status effects or modifiers applied to the source (attacker) of the triggering condition rather than the target. | 1 ||
| [`Consumed`](#object-consumed) | Object | An object defining behavior when a buddy is consumed, including instant kill or status application. | 1 ||

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
| [`ApplyToSource`](#object-applytosource) | Object | An object containing status effects or modifiers applied to the source (attacker) of the triggering condition rather than the target. | 1 ||
| [`ScatterCoins`](#object-scattercoins) | Object | The number of coins scattered, or an object with stacks and stacking behavior. | 1 ||
| [`tag`](./Enums.md) | Enum | Specifies the name of the tag to check for on the target. | 1 | megadino |
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
| [`Bruise`](./Enums.md) | Array / Integer | The number of Bruise stacks applied, or an array with duration and chance. | 1 | [.1] |
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
| `lingering` | Boolean | If true, the delayed ability persists on the target and can trigger multiple times. | 1 ||
| `relative` | Boolean | If true, the delay time is relative to current turn order; if false, absolute turns. | 1 ||
| [`ability`](./Enums.md) | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 1 | MoonHandDrop |

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
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum | Specifies the ability used to exit the possession state. | 1 ||
| [`punch_self_ability`](./Enums.md#enum-punch_self_ability) | Enum | Specifies the ability that makes the possessed unit attack itself. | 1 ||

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
| [`ability`](./Enums.md) | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 1 | MoonHandDrop |

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
| `change` | Integer | The amount to change an auxiliary counter by, clamped within min/max bounds. | 1 ||
| `max` | Integer | The maximum value that the auxiliary counter can reach. | 1 ||

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
| `tickdown_this_turn` | Boolean | If true, the madness stacks tick down at the end of the current turn instead of next turn. | 1 ||

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
| [`fights`](./Enums.md) | Integer | The number of future battles that the status stacks persist for. | 1 | 9999 |
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
| [`object`](./Enums.md) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 2 | [TallSkeletonCat] |
| `clone_items` | Boolean | If true, transfers inventory to the new entity. | 1 ||
| `clone_referenced_catdata` | Boolean | If true, copies the genetic data of the popped cat. | 1 ||
| `no_splatter` | Boolean | If true, prevents blood splatter visual effect when the object pops and spawns. | 1 ||

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
| [`dying`](./Enums.md#enum-dying) | Enum | Specifies the dying animation alternative to use. | 1 ||
| [`dead`](./Enums.md) | Enum | Specifies the dead animation alternative or a facial expression override. | 1 | deadShot |

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
| [`chance`](./Enums.md) | Number | A multiplier or percentage representing the probability of the effect occurring. | 12 | .02 |

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
| [`DamageOrHealConditionally`](./Enums.md) | Integer | If set to 1, the status group effect conditionally deals damage or heals based on target. | 1 | 1 |
| [`Freeze`](./Enums.md) | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. | 1 | [.1] |

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
| [`ability`](./Enums.md) | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 2 | MoonHandDrop |

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
| [`ability`](./Enums.md) | Enum | Specifies which ability is granted or triggered (e.g., from a death rattle or autocast). | 1 | MoonHandDrop |

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
| [`ForceUseAbility`](./Enums.md) | Enum | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 1 | MotherTumorGrow |

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
| [`cWaggle`](#object-cwaggle) | Object | A clone of the Waggle enemy type with custom graphics settings. | 1 ||
| [`cWaggle2x2`](#object-cwaggle2x2) | Object | A larger clone of cWaggle that occupies 2x2 tiles. | 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||
| [`cWaggle3x3`](#object-cwaggle3x3) | Object | An even larger clone of cWaggle2x2 that occupies 3x3 tiles. | 1 ||

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
| [`Stun`](./Enums.md) | Array / Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 98 | [0] |
| [`Burn`](./Enums.md) | Array / Enum / Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 85 | [.1] |
| [`Bruise`](./Enums.md) | Array / Integer | The number of Bruise stacks applied, or an array with duration and chance. | 79 | [.1] |
| `IgnoreSelf` | `Number` | Applies or references the 'IgnoreSelf' effect/state. | 75 ||
| [`Poison`](./Enums.md) | Array / Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 67 | [.1] |
| [`ChangeTile`](./Abilities_and_Spells.md#object-changetile) | `String` | Transforms the terrain tile under the target. | 62 ||
| [`Else`](#object-else) | Object | An object containing effects that apply when the parent conditional condition is not met. | 59 ||
| [`Bleed`](./Enums.md) | Array / Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 54 | [.1] |
| [`Shield`](./Enums.md) | Enum / Integer | Specifies the number of Shield stacks applied, where each stack reduces incoming damage by a flat amount. | 49 | 2*X |
| [`Cleanse`](./Enums.md) | Integer | If set to 1, removes all status effects from the target; if 0, no cleanse. | 44 | 0 |
| [`Confusion`](./Enums.md) | Array / Integer | The number of turns of Confusion applied, or an array with duration and chance. | 37 | [.1] |
| [`Conditional_HasTag`](#object-conditional_hastag) | Object | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 36 ||
| [`Conditional_Enemy`](#object-conditional_enemy) | Object | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 35 ||
| [`VisualFXTile`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'VisualFXTile' effect/state. | 34 ||
| [`SpeedUp`](./Enums.md) | Enum / Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 34 | 4 |
| [`Fear`](./Enums.md) | Array / Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 31 | [.3] |
| [`AllStatsUp`](./Enums.md) | Enum / Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 29 | 2 |
| [`Slow`](./Enums.md) | Array / Enum / Integer | The number of turns of Slow applied, or an array with duration and chance. | 29 | [.1] |
| [`TransformAbility`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'TransformAbility' effect/state. | 28 ||
| [`DamageUp`](./Enums.md) | Integer / String | The amount of damage increase, or a string formula for dynamic calculation. | 28 | 3 |
| [`ApplyToSource`](#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 27 ||
| [`BounceObject`](./Abilities_and_Spells.md#object-bounceobject) | `String` | Spawns a physics object that visually bounces off the target. | 26 ||
| [`Temporary`](#object-temporary) | Object | A wrapper object for applying status effects that automatically expire. | 26 ||
| [`ManaGain`](./Engine_LogicKeys.md#valid-property-keys) | Enum / Integer | Applies or references the 'ManaGain' effect/state. | 26 ||
| [`Conditional_Ally`](#object-conditional_ally) | Object | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 25 ||
| [`Blind`](./Enums.md) | Array / Integer | The number of stacks of Blind to apply, reducing accuracy; can be an array `[stacks, probability]` for a chance-based application. | 24 | [2] |
| [`Immobile`](./Enums.md) | Array / Integer | The number of turns of Immobile applied, or an array with duration and chance. | 24 | [.1] |
| [`Weakness`](./Enums.md) | Array / Integer | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 23 | [.1] |
| [`Charmed`](./Enums.md) | Array / Enum / Integer | The number of turns of Charmed applied, or an array with duration and chance. | 22 | [.1] |
| [`ConstitutionUp`](./Enums.md) | Array / Enum / Integer | The amount of Constitution (HP) increase, or an array with duration and chance. | 22 | [.5] |
| [`Leech`](./Enums.md) | Integer | The amount of health stolen per hit as a percentage of damage dealt. | 22 | 1 |
| [`StrengthUp`](./Enums.md) | Enum / Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 22 | max(int, 0) |
| [`EvolveAbilityFromPool`](./Abilities_and_Spells.md#object-evolveabilityfrompool) | `String` | Upgrades or transforms an existing ability into a new one from the specified pool. | 21 ||
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 21 ||
| [`IntelligenceUp`](./Enums.md) | Enum / Integer | The amount of intelligence increase, which can be a fixed integer or a mathematical expression. | 21 | item_aux |
| [`Freeze`](./Enums.md) | Array / Integer | The number of stacks of Freeze, immobilizing the unit for that many turns; can be an array `[stacks, probability]`. | 19 | [.1] |
| [`Madness`](#object-madness) | Array / Enum / Integer / Object | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. | 19 | [.1] |
| [`Sleep`](./Enums.md) | Array / Integer | The number of stacks of Sleep, putting the unit to sleep for that many turns; can be an array `[stacks, probability]`. | 19 | [.1] |
| `CollectsPickups` | `Number` | Applies or references the 'CollectsPickups' effect/state. | 17 ||
| [`KnockUpAndAway`](#object-knockupandaway) | Object | Displaces the target vertically and horizontally away from the source. | 17 ||
| [`Brace`](./Enums.md) | Integer | The amount of flat damage reduction applied to the source. | 17 | 2 |
| `OverrideKnockbackDamage` | `Number` | Applies or references the 'OverrideKnockbackDamage' effect/state. | 16 ||
| [`Consumed`](#object-consumed) | Object | State object triggered when this object or entity is eaten/consumed by another character. | 15 ||
| `VaporizeCorpse` | `Number` | Applies or references the 'VaporizeCorpse' effect/state. | 15 ||
| [`Petrify`](./Enums.md) | Array / Integer | The number of stacks of Petrify, turning the unit to stone and immobilizing it; can be an array `[stacks, probability]`. | 15 | [.15] |
| [`RandomStatUp`](./Enums.md) | Enum / Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 15 | ceil(X/3) |
| [`ChangeCatClass`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ChangeCatClass' effect/state. | 14 ||
| [`Conditional_GoodRoll`](#object-conditional_goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 14 ||
| `EndTurn` | `Number` | Applies or references the 'EndTurn' effect/state. | 14 ||
| `FaceAway` | `Number` | Applies or references the 'FaceAway' effect/state. | 14 ||
| [`RandomStatusFromPool`](#object-randomstatusfrompool) | Object | Selects and applies a random status effect from the provided nested block. | 14 ||
| `RefreshMovePoints` | `Number` | Applies or references the 'RefreshMovePoints' effect/state. | 14 ||
| `TakeExtraTurn` | `Number` | Applies or references the 'TakeExtraTurn' effect/state. | 14 ||
| [`TransformBasicAttack`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'TransformBasicAttack' effect/state. | 14 ||
| [`DivineShield`](./Enums.md) | Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 14 | 2 |
| [`Leeches`](./Enums.md) | Integer | The number of Leech stacks applied, healing the attacker. | 14 | 2 |
| [`CatPartsTransform`](#object-catpartstransform) | Object | Transforms specific body parts into different visual variants. | 13 ||
| [`Conditional_Boss`](#object-conditional_boss) | Object | Conditional trigger: Executes nested logic if the target is a Boss. | 13 ||
| `GenericDebuff` | `Number` | Applies or references the 'GenericDebuff' effect/state. | 13 ||
| `Displace` | `Number` | Applies or references the 'Displace' effect/state. | 12 ||
| [`Cleave`](#object-cleave) | Integer / Object | If an integer, the number of cleave hits; if an object, may contain a chance for cleave. | 12 | 1 |
| [`LuckUp`](./Enums.md) | Enum / Integer | Specifies the number of Luck stacks applied, where positive values increase critical hit chance and loot quality and negative values decrease them. | 12 | 2 |
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 12 | 2 |
| [`ApplyToSourceOnKill`](#object-applytosourceonkill) | Object | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 11 ||
| [`ChanceToBreakFree`](#object-chancetobreakfree) | Object | Provides a probability to escape a grapple or restraining effect. | 11 ||
| [`DoScreenShake`](#object-doscreenshake) | Integer / Object | Triggers a camera screen shake effect. | 11 ||
| `FullHeal` | Integer | Applies or references the 'FullHeal' effect/state. | 11 ||
| [`Conditional_Speculative`](#object-conditional_speculative) | Object | A simulation object used by the AI to test hypothetical outcomes before committing to an action. | 10 ||
| `RefreshActPoints` | `Number` | Applies or references the 'RefreshActPoints' effect/state. | 10 ||
| [`VisualFX`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'VisualFX' effect/state. | 10 ||
| [`DexterityUp`](./Enums.md) | Enum / Integer | The amount of Dexterity stat increased or decreased (negative values lower the stat); can be a formula or fixed integer. | 10 | 2 |
| `PurgeAll` | `Number` | Applies or references the 'PurgeAll' effect/state. | 9 ||
| [`ApplyPassives`](#object-applypassives) | Object | Grants the nested passive abilities dynamically. | 9 ||
| `DeferVaporize` | `Number` | Applies or references the 'DeferVaporize' effect/state. | 9 ||
| `SpawnCreep` | `Number` | Applies or references the 'SpawnCreep' effect/state. | 9 ||
| [`MagicWeakness`](./Enums.md) | Array / Integer | The number of stacks of MagicWeakness, increasing incoming magic damage; can be an array `[stacks, probability]`. | 9 | [.1] |
| [`Marked`](./Enums.md) | Array / Integer | The number of Marked stacks applied, which increases damage taken from all sources; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 9 | [.1] |
| [`RandomMagicMissile`](#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, each dealing independent damage; can also be an object with custom tooltip data. | 9 | 5 |
| [`Conditional_FormulaIsPositive`](#object-conditional_formulaispositive) | Object | Conditional trigger: Executes nested logic if the evaluated mathematical formula returns a value greater than 0. | 8 ||
| [`CanApplyToInanimate`](#object-canapplytoinanimate) | Object | Modifier object that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 8 ||
| `ChanceToBreak` | Integer | Applies or references the 'ChanceToBreak' effect/state. | 8 ||
| `OverrideChainKnockback` | `Number` | Applies or references the 'OverrideChainKnockback' effect/state. | 8 ||
| [`SpreadDisease`](#object-spreaddisease) | Object | Provides a chance to transmit a disease status to adjacent targets. | 8 ||
| [`Ammo`](./Enums.md) | Integer | The change in ammunition count; positive values add ammo, negative values consume ammo. | 8 | -1 |
| [`Grappled`](./Enums.md) | Integer | The number of turns the target is grappled, preventing movement and actions. | 8 | 1 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 8 | 2 |
| [`ApplyStatusIfCrit`](#object-applystatusifcrit) | Object | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. | 7 ||
| `BramblesOnHit` | `Number` | Applies or references the 'BramblesOnHit' effect/state. | 7 ||
| `ContextualHeal` | `Number` | Applies or references the 'ContextualHeal' effect/state. | 7 ||
| `ForceAttack` | `Number` | Forces the character to execute an immediate attack. | 7 ||
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 7 ||
| `KnockbackDamageImmuneUntilSettled` | `Number` | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. | 7 ||
| `ManaSteal` | `Number` | Applies or references the 'ManaSteal' effect/state. | 7 ||
| [`TriggerWerewolfTransform`](./Engine_LogicKeys.md#valid-property-keys) | `Array` | Applies or references the 'TriggerWerewolfTransform' effect/state. | 7 ||
| [`AlphaCat`](./Enums.md) | Integer | The number of stacks of the AlphaCat status effect. | 7 | 1 |
| [`Rot`](./Enums.md) | Array / Integer | The number of stacks of Rot, causing damage over time and potentially spawning a fly on death; can be an array `[stacks, probability]`. | 7 | [.1] |
| [`Tarred`](./Enums.md) | Array / Integer | The number of stacks of Tarred, making the unit more vulnerable to fire damage; can be an array `[stacks, probability]`. | 7 | [.1] |
| [`Tech`](./Enums.md) | Integer | The number of Tech stacks applied, which increase the damage of the next ability used. | 7 | 3 |
| [`TempRangeUp`](./Enums.md) | Integer | The number of turns this unit gains increased attack range. | 7 | 2 |
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
| [`BackflipWhenTargeted`](#object-backflipwhentargeted) | Integer / Object | The number of stacks of BackflipWhenTargeted or an object defining the dodge ability; causes the unit to perform a backflip dodge when targeted. | 6 | 2 |
| [`CharismaUp`](./Enums.md) | Enum / Integer | The amount of Charisma stat increased or decreased (negative values lower the stat); can be a formula or fixed integer. | 6 | -2 |
| [`ObjectOnHitCharacter`](#object-objectonhitcharacter) | Enum / Object | An object or entity name that spawns upon hitting a character, with optional stacks and chance. | 6 | SkeletonCatFamiliar |
| [`RandomInjury`](./Enums.md) | Integer | The number of random injuries applied to the target. | 6 | 1 |
| [`SpiderInfested`](./Enums.md) | Integer | The number of turns the target is infested with spiders, taking damage over time. | 6 | 2 |
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
| [`DodgeChance_Status`](./Enums.md) | Integer | The percentage of dodge chance granted by this status effect. | 5 | 50 |
| [`Drowsy`](./Enums.md) | Integer | The number of stacks of the Drowsy status effect to apply, which reduces a unit's action points or turn efficiency. | 5 | 8 |
| [`MovementUp`](./Enums.md) | Integer | The number of points of additional movement gained for a number of turns. | 5 | -2 |
| [`Revive`](./Enums.md) | Integer | The percentage or flat amount of HP restored when reviving a dead ally. | 5 | 50 |
| [`SoulLink`](./Enums.md) | Integer | The number of turns the linked status lasts, sharing damage between linked units. | 5 | 1 |
| [`Stealth`](./Enums.md) | Integer | The number of turns the unit is invisible, or [stacks, probability] of gaining stealth. | 5 | 2 |
| [`TempDamageUp`](./Enums.md) | Integer | The number of temporary damage increase stacks applied to the target for the current turn. | 5 | 2 |
| [`Webbed`](./Enums.md) | Integer | The number of Webbed stacks applied, which immobilizes the target and prevents movement; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 5 | 1 |
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
| [`Charge`](./Enums.md) | Integer | The number of stacks of Charge, which makes the caster gain 1 Mana per stack at the start of its next turn. | 4 | 2 |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 4 | 5 |
| [`Reanimate`](./Enums.md) | Integer | The percentage chance (e.g., 50%) to revive upon death. | 4 | 50 |
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
| [`DamageOrHealConditionally`](./Enums.md) | Integer | If set to 1, the status group effect conditionally deals damage or heals based on target. | 3 | 1 |
| [`Doomed`](./Enums.md) | Integer | The number of turns until the target is instantly killed when this counter reaches zero. | 3 | 3 |
| [`ExtraBasicAttacks_Status`](./Enums.md) | Integer | The number of extra basic attacks the unit can perform each turn. Stacks for additional attacks. | 3 | 1 |
| [`KineticSpikes`](./Enums.md) | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 3 | 2 |
| [`MoveQuivered`](./Enums.md) | Integer | Specifies the number of bonus movement points granted; an array `[stacks, probability]` specifies the amount and its chance of application. | 3 | 1 |
| [`NextAttackBonusRange`](./Enums.md) | Integer | The bonus range added to the next attack. | 3 | 3 |
| [`PermanentConstitution`](./Enums.md) | Integer | The amount of permanent Constitution (max HP) added. | 3 | 2 |
| [`PoisonLace`](./Enums.md) | Enum / Integer | The amount or formula for PoisonLace damage applied per turn; can be a fixed integer or a formula like `X/3`. | 3 | X/3 |
| [`Reflect`](./Enums.md) | Integer | The number of stacks of Reflect, causing a percentage of incoming damage to be reflected back to the attacker. | 3 | 5 |
| [`ReviveNextRound`](#object-revivenextround) | Integer / Object | The number of stacks of ReviveNextRound or an object defining revival properties; causes the unit to revive with specified health, shields, or buffs at the start of the next round. | 3 | 2 |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp, increasing spell damage dealt by the unit. | 3 | 3 |
| [`Tangled`](#object-tangled) | Integer / Object | The number of turns the target is unable to move, with optional [stacks, probability] format. | 3 | 1 |
| [`TempSpeedUp`](./Enums.md) | Enum / Integer | Alias for TempSpeedUp; temporarily increases the unit's speed stat. | 3 | 4 |
| [`TempStrengthUp`](./Enums.md) | Enum | Alias for TempStrengthUp; temporarily increases the unit's strength stat. | 3 | X |
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
| [`BodyGuard`](#object-bodyguard) | Object | An object containing `stacks` and `ability` to define a bodyguard protector effect. | 2 ||
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance increase, in percentage points. | 2 | 2 |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of stacks of DiminishingHealthRegen, providing health regeneration each turn that decreases with each stack. | 2 | 3 |
| [`DoubleCastSpell`](./Enums.md) | Integer | The number of times spells are cast twice in a single action. | 2 | 1 |
| [`DoubleLoot`](./Enums.md) | Integer | The number of extra loot rolls or items granted when looting. | 2 | 2 |
| [`FreeSpell`](./Enums.md) | Integer | The number of free spells granted, allowing the source to cast spells without consuming mana or charges. | 2 | 2 |
| [`Hex`](./Enums.md) | Integer | The number of Hex stacks applied, which increases the chance of negative status effects landing on the target. | 2 | 1 |
| [`KnockOutCoin`](#object-knockoutcoin) | Integer / Object | Either an integer for guaranteed stacks or an object with `stacks` and `chance` for a probability-based knock-out effect. | 2 | 1 |
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is knocked back. | 2 | 5 |
| [`Lifesteal`](./Enums.md) | Integer | The number of stacks of Lifesteal, converting a percentage of damage dealt into healing for the attacker. | 2 | 3 |
| [`ManaLeeches`](./Enums.md) | Integer | The number of mana leech stacks that drain mana on hit. | 2 | 2 |
| [`Ostracized`](./Enums.md) | Integer | The number of stacks of Ostracized, making the unit unable to be targeted by ally abilities or receive allied benefits. | 2 | 2 |
| [`PartialCleanse`](./Enums.md) | Integer | The number of status effects removed from the target (partial cleanse). | 2 | 9999 |
| [`Possessed`](./Enums.md) | Integer | The number of stacks of the Possessed status effect applied, which causes the unit to be controlled by an external force. | 2 | 1 |
| [`RangeUp`](./Enums.md) | Integer | The amount of bonus range added to the unit's attacks. Each stack adds one tile of range. | 2 | 1 |
| [`RepairWeapon`](./Enums.md) | Integer | The number of stacks of RepairWeapon applied (or an array [stacks, probability] for random application). | 2 | 99 |
| [`SizeScale`](./Enums.md) | Number | A multiplier for the unit's visual size. Values above 1 increase size, values below 1 decrease size. | 2 | .6 |
| [`SpawnFlames`](./Enums.md) | Array | An array defining [stacks, probability] for spawning flames on the target. The first number is the amount of flames spawned, and the second is the probability of occurrence. | 2 | [.20+.1*level] |
| [`TempCritChanceUp`](./Enums.md) | Integer | A temporary increase to critical hit chance for a number of turns or attacks. | 2 | 30 |
| [`TempDexterityUp`](./Enums.md) | Enum | A temporary increase to the dexterity stat, specified as an alias or integer. | 2 | X |
| [`TempInitiativeChange`](./Enums.md) | Integer | The amount of temporary initiative change applied to the displaced unit. | 2 | -100 |
| [`TempMovement`](./Enums.md) | Enum / Integer | Specifies the temporary movement range granted to the unit, either as an integer or via an alias. Stacks determine duration in turns. | 2 | 20 |
| [`TempSpellDamageUp`](./Enums.md) | Integer | A temporary increase to spell damage output. | 2 | 1 |
| [`TrailBlazer`](./Enums.md) | Enum / Integer | Either a movement speed boost or the number of affected units. | 2 | mov |
| [`Trample`](./Enums.md) | Integer | The number of tiles this character can move through enemies, dealing damage or applying effects equal to the value. | 2 | 3 |
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
| [`Attraction`](./Enums.md) | Integer | If set to 1, the target is pulled one tile toward the source of the effect. | 1 | 1 |
| [`Bloodzerked`](./Enums.md) | Integer | The number of stacks of the Bloodzerk status, which grants attack power at the cost of health. | 1 | 1 |
| [`ChampionUpgradeNextMinion`](./Enums.md) | Integer | The number of times the next summoned minion is upgraded to champion rank. | 1 | 1 |
| [`ChangeTilesUnder`](./Enums.md) | Enum | Determines which tile type (e.g., GlassTile, DirtTile) replaces the tiles beneath the target. | 1 | LavaTile |
| [`ChargeFists`](./Enums.md) | Integer | The number of charges for the Charge Fists ability. | 1 | 1 |
| [`CreateGlobalModifiers`](#object-createglobalmodifiers) | Object | An object containing global modifier effects to apply after the time delay. | 1 ||
| [`DoubleCast`](./Enums.md) | Integer | The number of times the next ability is automatically cast again. | 1 | 1 |
| [`DrinkWater`](./Enums.md) | Integer | The number of stacks of the Drink Water status effect applied, which may trigger water-related behaviors or effects. | 1 | 1 |
| [`EliteUpgradeNextMinion`](./Enums.md) | Integer | The number of times the next summoned minion is upgraded to elite rank. | 1 | 1 |
| [`EmptyMind`](./Enums.md) | Integer | The number of stacks of the Empty Mind status effect applied, which prevents the unit from gaining or using mental effects. | 1 | 1 |
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer | The number of extra basic moves the unit can perform each turn. Stacks for additional moves. | 1 | 1 |
| [`FireArmor`](./Enums.md) | Integer | The number of stacks of fire armor, dealing fire damage to attackers. | 1 | 1 |
| [`FireArmor2`](./Enums.md) | Integer | An alternate version of FireArmor with modified damage or duration values. | 1 | 1 |
| [`ForceUseAbility`](./Enums.md) | Enum | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 1 | MotherTumorGrow |
| [`GainCoinsRange`](#object-gaincoinsrange) | Object | An object with min and max values defining the range of coins gained. | 1 ||
| [`HealRandomInjury`](./Enums.md) | Integer | The number of random injuries healed on the target. | 1 | 1 |
| [`HeavyHits`](./Enums.md) | Integer | The number of stacks that cause attacks to deal extra knockback or damage. | 1 | 1 |
| [`IceArmor`](./Enums.md) | Integer | The number of stacks of ice armor, reducing incoming damage or freezing attackers. | 1 | 1 |
| [`Infested`](./Enums.md) | Integer | The number of stacks of Infested, causing the unit to spawn a friendly fly or swarm upon death. | 1 | 1 |
| [`Invulnerable`](./Enums.md) | Integer | The number of turns or stacks of temporary invulnerability. | 1 | 1 |
| [`Meaty`](./Enums.md) | Integer | The number of stacks that increase max HP or provide damage reduction. | 1 | 1 |
| [`Muted`](./Enums.md) | Integer | The number of turns the unit is silenced, unable to cast spells. | 1 | 1 |
| [`NextAbilityHeals`](./Enums.md) | Integer | The number of times the next ability will heal instead of damage. | 1 | 1 |
| [`NextActionLuckUp`](./Enums.md) | Integer | The amount of bonus luck applied to the unit's next action. Stacks increase the luck bonus. | 1 | 99 |
| [`NextDamageReduceAndHealAllies`](./Enums.md) | Integer | The number of stacks that reduce next damage taken and heal adjacent allies. | 1 | 1 |
| [`NextTurnDoubleRangedDamage`](./Enums.md) | Integer | The number of turns the next ranged attack deals double damage. | 1 | 1 |
| [`NonStackingDivineShield`](./Enums.md) | Integer | A non-stacking shield that blocks the next instance of damage; applied as an integer for the number of shields. | 1 | 1 |
| [`PermanentDexterity`](./Enums.md) | Integer | The amount of permanent dexterity added to the unit. | 1 | 2 |
| [`PermanentImmobile`](./Enums.md) | Integer | The number of stacks of permanent immobility applied, preventing the unit from moving indefinitely. | 1 | 1 |
| [`PermanentIntelligence`](./Enums.md) | Integer | The number of permanent intelligence stat points added or subtracted. | 1 | 2 |
| [`PermanentSpeed`](./Enums.md) | Integer | The number of permanent speed stat points added or subtracted. | 1 | 2 |
| [`ProbeCharmed`](./Enums.md) | Integer | The number of stacks of ProbeCharmed status, which charms the target when probed. | 1 | 1 |
| [`RandomPermanentStat`](./Enums.md) | Integer | The amount of random permanent stat change applied, positive or negative. | 1 | 1 |
| [`ReduceManaCost`](./Enums.md) | Integer | The number by which mana cost of abilities is reduced, up to a minimum of zero. | 1 | 1 |
| [`ReduceManaCostExcludeBrainstorm`](./Enums.md) | Integer | The number by which mana cost is reduced, excluding the Brainstorm ability from the reduction. | 1 | 1 |
| [`Regurge`](./Enums.md) | Integer | Number of stacks of Regurge status, causing the unit to regurgitate items or statuses. | 1 | 1 |
| [`SetDefaultFace`](./Enums.md) | Enum | Specifies the default face expression for the unit (e.g., sad, happy, insane). | 1 | insane |
| [`ShortCircuit`](./Enums.md) | Integer | Number of stacks causing the unit to lose its turn or be interrupted. | 1 | 1 |
| [`SpawnCoinAnywhere`](./Enums.md) | Array / Integer | If integer, the number of coins spawned; if array, [stacks, probability] of spawning a coin anywhere on the map. | 1 | [.5] |
| [`SpellShield`](./Enums.md) | Integer | Number of shields that block incoming spells or magical damage. | 1 | 1 |
| [`StatBounty`](./Enums.md) | Integer | Number of stacks that grant a bounty of permanent stat increases upon performing certain actions. | 1 | 1 |
| [`StatusGroup`](#object-statusgroup) | Object | A collection of status effects applied together as a group, each with its own stack count. | 1 ||
| [`Switcheroo`](./Enums.md) | Integer | Number of stacks that allow swapping positions with another unit. | 1 | 1 |
| [`Taunting`](./Enums.md) | Integer | Number of stacks that force enemies to target this unit preferentially. | 1 | 1 |
| [`TempBackstab`](./Enums.md) | Integer | Temporary increase in backstab damage, with stacks representing the bonus percentage. | 1 | 75 |
| [`TempBonusKnockback`](./Enums.md) | Integer | Temporary increase in knockback distance, with stacks representing the bonus. | 1 | 1 |
| [`TempBonusKnockbackDamage`](./Enums.md) | Integer | Temporary increase in damage dealt when knocking back an enemy. | 1 | 1 |
| [`TempCounterAttack`](./Enums.md) | Integer | The number of stacks (turns) for TempCounterAttack, causing the unit to counterattack after being hit. | 1 | 1 |
| [`TempInjuryImmunity`](./Enums.md) | Integer | Number of turns the unit is immune to receiving injuries. | 1 | 1 |
| [`TempManaCostReduction`](./Enums.md) | Integer | Temporary reduction in mana cost of abilities, with stacks representing the amount reduced. | 1 | 1 |
| [`TempPreEmptiveCounterAttack`](./Enums.md) | Integer | Number of turns during which the unit will preemptively counterattack when targeted. | 1 | 1 |
| [`TilesMovedToCritChance`](./Enums.md) | Integer | Number of stacks that convert tiles moved into bonus critical hit chance. | 1 | 1 |
| [`TilesMovedToMana`](./Enums.md) | Integer | Number of stacks that convert tiles moved into mana regeneration. | 1 | 1 |
| [`TilesMovedToNeighborHeal`](./Enums.md) | Enum | Specifies the type of neighbor heal triggered by moving tiles, e.g., 'level'. | 1 | level |
| [`TilesMovedToStrength`](./Enums.md) | Integer | Number of stacks that convert tiles moved into temporary strength increase. | 1 | 1 |
| [`TowerDefenseStatus`](./Enums.md) | Integer | Stacks of sentry mode status, allowing the unit to attack enemies that enter range. | 1 | 1 |
| [`TowerDefenseStatus2`](./Enums.md) | Integer | Enhanced sentry mode stacks, providing additional benefits over TowerDefenseStatus. | 1 | 1 |
| [`VaporizeCorpseFlipAdvantage`](./Enums.md) | Array | Array [stacks, probability] granting advantage when flipping vaporized corpses. | 1 | [.33] |

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
