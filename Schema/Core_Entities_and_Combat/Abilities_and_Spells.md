---
title: "Abilities & Spells Schema"
description: "Defines the properties and engine hooks for combat abilities."
---

# Abilities & Spells Schema


<details open>
<summary><strong>Quick Navigation</strong></summary>

<table>
  <tr>
    <td width="22%"><strong>Core Entities & Combat</strong></td>
    <td><a href="../Core_Entities_and_Combat/Abilities_and_Spells.md">Abilities & Spells</a> • <a href="../Core_Entities_and_Combat/Characters_and_Bosses.md">Characters & Bosses</a> • <a href="../Core_Entities_and_Combat/Items_and_Equipment.md">Items & Equipment</a> • <a href="../Core_Entities_and_Combat/Passives_and_Statuses.md">Passives & Statuses</a> • <a href="../Core_Entities_and_Combat/Elite_Buffs.md">Elite Buffs</a> • <a href="../Core_Entities_and_Combat/Enemy_AI.md">Enemy AI</a> • <a href="../Core_Entities_and_Combat/Status_Effect_Keywords.md">Status Keywords</a></td>
  </tr>
  <tr>
    <td><strong>Engine Scripts & Logic</strong></td>
    <td><a href="../Engine_Scripts_and_Logic/Engine_LogicKeys.md">Logic Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_EventKeys.md">Event Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_DamagingKeys.md">Damaging Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md">Status & Passive Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md">Global Modifiers</a> • <a href="../Engine_Scripts_and_Logic/Math_Equations.md">Math Equations</a></td>
  </tr>
  <tr>
    <td><strong>Player Progression & Cats</strong></td>
    <td><a href="../Player_Progression_and_Cats/Cat_Classes.md">Cat Classes</a> • <a href="../Player_Progression_and_Cats/Cat_Mutations.md">Cat Mutations</a> • <a href="../Player_Progression_and_Cats/Custom_Cats.md">Custom Cats</a> • <a href="../Player_Progression_and_Cats/Injuries.md">Injuries</a> • <a href="../Player_Progression_and_Cats/Progression_Unlocks.md">Progression Unlocks</a> • <a href="../Player_Progression_and_Cats/Combat_Rewards.md">Combat Rewards</a></td>
  </tr>
  <tr>
    <td><strong>World, Maps & Events</strong></td>
    <td><a href="../World_Maps_and_Events/Events_and_Encounters.md">Events & Encounters</a> • <a href="../World_Maps_and_Events/House_and_Environment.md">House & Environment</a> • <a href="../World_Maps_and_Events/Map_Generation_and_Routing.md">Map Gen & Routing</a> • <a href="../World_Maps_and_Events/Furniture_and_Metaprogression.md">Furniture & Meta</a> • <a href="../World_Maps_and_Events/Shops.md">Shops</a> • <a href="../World_Maps_and_Events/Spawns_and_Enemy_Pools.md">Spawns & Enemy Pools</a> • <a href="../World_Maps_and_Events/Boss_Cutscene_Info.md">Boss Cutscenes</a> • <a href="../World_Maps_and_Events/NPC_Scripts.md">NPC Scripts</a></td>
  </tr>
  <tr>
    <td><strong>Assets & Localization</strong></td>
    <td><a href="../Assets_and_Localization/Audio_SFX_Dictionary.md">Audio SFX</a> • <a href="../Assets_and_Localization/Particles_and_VFX_Dictionary.md">Particles & VFX</a> • <a href="../Assets_and_Localization/Damage_Text_Styles.md">Damage Text</a> • <a href="../Assets_and_Localization/Localization_Guide.md">Localization Guide</a> • <a href="../Assets_and_Localization/Text_Formatting_and_Effects.md">Text Formatting</a> • <a href="../Assets_and_Localization/Strings.md">Strings</a></td>
  </tr>
  <tr>
    <td><strong>Reference & Meta</strong></td>
    <td><a href="../Reference_and_Meta/Enums.md">Enums</a> • <a href="../Reference_and_Meta/Arrays.md">Arrays</a> • <a href="../Reference_and_Meta/Item_Pools.md">Item Pools</a> • <a href="../Reference_and_Meta/Difficulties.md">Difficulties</a> • <a href="../Reference_and_Meta/Engine_Hidden_Passives_and_Statuses.md">Hidden Passives</a> • <a href="../Reference_and_Meta/Passive_Identifiers_Audit.md">Passive Audit</a> • <a href="../Reference_and_Meta/Engine_Uncategorized_Resources.md">Uncategorized Keys</a> • <a href="../Reference_and_Meta/Miscellaneous.md">Miscellaneous</a></td>
  </tr>
</table>

</details>

## Overview
> [!NOTE]
> This schema defines the behavior, targeting, cost, and visual effects of attacks and spells used by characters, enemies, and items.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
HogRush {
    template move
    
    meta {
        name "ABILITY_HOGRUSH_NAME"
        desc "ABILITY_HOGRUSH_DESC"
        animate_name true
        class Butcher
    }

    graphics {
        speed 2
        animation dash
    }

    cost {
        infcantrip true
        mana 7
    }

    temporary_effects {
        Trample 3
    }

    target {
        max_range 100
        restrictions [must_be_moveable must_have_tag must_move]
        target_requires_tag food
        trample_allies_too true
    }
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Ability_Pools.md`](../../Directory/Abilities/Ability_Pools.md)
- [`Cat_Abilities.md`](../../Directory/Abilities/Cat_Abilities.md)
- [`Enemy_and_Boss_Abilities.md`](../../Directory/Abilities/Enemy_and_Boss_Abilities.md)
- [`System_and_Item_Abilities.md`](../../Directory/Abilities/System_and_Item_Abilities.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Abilities & Spells

> **Associated Files:** `data/abilities/, data/ability_templates/`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3099

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related keys. | 2418 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`damage_instance`](./Abilities_and_Spells.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 2337 | `{ . . . }` |
| [`meta`](./Abilities_and_Spells.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 2328 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 2168 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`graphics`](./Abilities_and_Spells.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 2032 | `{ . . . }` |
| [`target`](./Abilities_and_Spells.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1859 | `{ . . . }` |
| [`cost`](./Abilities_and_Spells.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1845 | `{ . . . }` |
| [`variant_of`](../Reference_and_Meta/Enums.md#enum-variant_of) | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. | 900 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 414 | `{ . . . }` |
| [`spawn`](./Abilities_and_Spells.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. | 346 | `{ . . . }` |
| [`tags`](../Reference_and_Meta/Arrays.md#array-tags) | Array / Enum | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 236 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| [`self_damage`](./Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 218 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives) | Object  | Grants temporary passive abilities to the caster for the duration of the ability. | 136 | `{ . . . }` |
| [`class`](../Reference_and_Meta/Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 90 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`temporary_effects`](./Abilities_and_Spells.md#object-temporary_effects) | Object  | Applies temporary status effects on the caster upon using the ability. | 88 | `{ . . . }` |
| [`sounds`](./Abilities_and_Spells.md#object-sounds) | Object  | Defines sound effects played at various points of the ability (e.g., ontrigger, oncastpoint). | 39 | `{ . . . }` |
| [`splash_damage`](./Abilities_and_Spells.md#object-splash_damage) | Object  | Defines additional damage or effects applied to nearby targets around the primary target. | 34 | `{ . . . }` |
| [`ai_ability`](../Reference_and_Meta/Enums.md#enum-ai_ability) | Enum | Specifies the ability to use as the AI's behavior for this ability. | 29 | `AZ_Jump_AI`<br>`BasicBigMelee`<br>`BasicMelee` |
| [`keyword_tooltips`](./Abilities_and_Spells.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 23 | `{ . . . }` |
| [`chain_ability`](../Reference_and_Meta/Enums.md#enum-chain_ability) | Enum | Specifies the ability to chain into after this ability is used. | 15 | `BoyDinoDash`<br>`ChaosStacyAttackChain`<br>`ControlPlantsPartTwo` |
| [`sub_ability`](../Reference_and_Meta/Enums.md#enum-sub_ability) | Enum | Specifies a sub-ability that is part of this ability, often used for multi-part abilities. | 8 | `CollectiveCounterImpl`<br>`CollectiveSpinImpl`<br>`HomingBlasts2_sub` |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2 | `{ . . . }` |
| [`cloned_ability`](../Reference_and_Meta/Enums.md#enum-cloned_ability) | Enum | Specifies an ability that is cloned from another. | 2 | `attack` |
| [`empty_self_damage`](./Abilities_and_Spells.md#object-empty_self_damage) | Object  | Defines self-damage or effects when the ability is used with no target (empty). | 2 | `{ . . . }` |
| [`damage`](./Abilities_and_Spells.md#object-damage) | Equation / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`bonk_damage`](./Abilities_and_Spells.md#object-bonk_damage) | Object  | Defines damage and effects applied when a dash or move hits a wall or obstacle. | 1 | `{ . . . }` |
| [`layer`](../Reference_and_Meta/Enums.md#enum-layer) | Enum  | Specifies the layer on which the ability's effect operates (e.g., characters, tiles, gas). | 0 | `2`<br>`all`<br>`characters` |
| [`chapter`](../Reference_and_Meta/Enums.md#enum-chapter) | Enum  | Specifies which chapter or scenario this ability is available in. | 0 | `1`<br>`alley` |

</details>


---


### Object: `graphics`


**Definition:** An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects.  
**Total Count:** 2629

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1559 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`particle`](../Reference_and_Meta/Enums.md#enum-particle) | Enum | Specifies the particle effect displayed. | 488 | `ArrowFromAbove`<br>`BigMagicMissileBlast`<br>`Bolt` |
| [`projectile`](../Reference_and_Meta/Enums.md#enum-projectile) | Enum | Specifies the projectile spawned for the ability. | 228 | `AcidshotProjectile`<br>`AnimalEgg`<br>`ArmorPickup` |
| `lob` | Boolean | If true, the projectile follows a lobbed trajectory. | 130 | `false`<br>`true` |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 93 | `.05`<br>`.1`<br>`.25` |
| `dont_visualize_ai` | Boolean | If true, the AI's visualization of this ability is suppressed. | 86 | `true` |
| `dont_orient` | Boolean | If true, the caster does not rotate to face the target. | 83 | `true` |
| [`dash_animation`](../Reference_and_Meta/Enums.md#enum-dash_animation) | Enum | Specifies the animation played during the dash movement. | 65 | `dash`<br>`dash2`<br>`dashing` |
| [`dash_start_animation`](../Reference_and_Meta/Enums.md#enum-dash_start_animation) | Enum | Specifies the animation played at the start of the dash. | 63 | `dashbegin`<br>`dashstart`<br>`dashstart2` |
| `speed` | Array / Float  | The speed of the projectile or move, can be a value or a range. | 61 | `-30`<br>`-4`<br>`.5` |
| [`affected_particle`](../Reference_and_Meta/Enums.md#enum-affected_particle) | Enum | Specifies the particle effect on affected targets. | 51 | `Cleanse`<br>`ExclamationPointEnemy`<br>`HealBig` |
| [`dash_attack_animation`](../Reference_and_Meta/Enums.md#enum-dash_attack_animation) | Enum | Specifies the animation played at the end of the dash when attacking. | 45 | `block`<br>`dashEnd`<br>`dashEnd2` |
| `lob_height` | Integer | Controls the height of the lobbed projectile trajectory. | 45 | `-1`<br>`0`<br>`1` |
| [`animation_in`](../Reference_and_Meta/Enums.md#enum-animation_in) | Enum | Specifies the animation played when entering the target tile (e.g., teleport in). | 43 | `digUp`<br>`digin`<br>`exitWater` |
| [`animation_out`](../Reference_and_Meta/Enums.md#enum-animation_out) | Enum | Specifies the animation played when leaving the origin tile. | 43 | `digDown`<br>`digout`<br>`enterWater` |
| [`jump_attack_animation`](../Reference_and_Meta/Enums.md#enum-jump_attack_animation) | Enum | Specifies the animation played at the end of a jump attack. | 39 | `bellyflopEnd`<br>`block`<br>`entrance_land` |
| `use_projectile` | Boolean | If true, the ability uses a projectile. | 35 | `true` |
| [`full_jump_animation`](../Reference_and_Meta/Enums.md#enum-full_jump_animation) | Enum | Specifies the animation for a full jump (encompassing entire jump). | 24 | `attack`<br>`attack1`<br>`backflip` |
| `full_jump_sync_frames` | Integer | The frame count to sync the jump animation with the movement. | 24 | `24`<br>`25`<br>`27` |
| `use_rotation` | Boolean | If false, the ability effect does not rotate with the caster. | 24 | `false` |
| [`dash_end_animation`](../Reference_and_Meta/Enums.md#enum-dash_end_animation) | Enum | Specifies the animation played at the end of a dash. | 22 | `dashend`<br>`launchStop`<br>`none` |
| `palette` | Integer | Specifies the color palette index for the ability's visuals. | 21 | `-1`<br>`0`<br>`1` |
| `full_jump_windup_frames` | Integer | The number of frames of windup before the jump. | 20 | `10`<br>`13`<br>`14` |
| `visual_delay_but_simultaneous_damage` | Integer | The visual delay in frames for the ability while damage is applied simultaneously. | 18 | `0`<br>`10`<br>`2` |
| [`center_particle`](../Reference_and_Meta/Enums.md#enum-center_particle) | Enum | Specifies the FX particle effect emitted at the center of the ability's origin tile. | 17 | `BigMagicMissileBlast`<br>`Explosion`<br>`FireBlastMushroom` |
| [`area_particle`](../Reference_and_Meta/Enums.md#enum-area_particle) | Enum | Specifies the FX particle effect emitted across the affected area tiles. | 16 | `Bolt`<br>`BurnTrigger`<br>`Earthquake` |
| `fall_from_sky` | Boolean | If true, the projectile or visual element originates from above the map and falls downward. | 16 | `true` |
| `use_placeholder` | Boolean | If true, renders the ability using a temporary placeholder animation instead of the final art. | 14 | `true` |
| [`move_start_animation`](../Reference_and_Meta/Enums.md#enum-move_start_animation) | Enum | Determines which character animation plays at the beginning of a movement ability. | 14 | `backflipStart`<br>`buttScootStart`<br>`cartwheelStart` |
| [`move_end_animation`](../Reference_and_Meta/Enums.md#enum-move_end_animation) | Enum | Determines which character animation plays at the end of a movement ability. | 13 | `backflipEnd`<br>`buttScootEnd`<br>`cartwheelEnd` |
| `face_toss_target` | Boolean | If true, the unit rotates to face the target before performing a toss or throw. | 12 | `true` |
| `ignore_slowtiles` | Boolean | If true, the unit's movement during this ability ignores tile-based speed penalties. | 12 | `true` |
| `chain_distance` | Float | The distance between chain links, as a fraction of a tile. | 11 | `.25`<br>`.38` |
| [`chain_movieclip`](../Reference_and_Meta/Enums.md#enum-chain_movieclip) | Enum | Specifies the visual MovieClip asset used for the chain's links. | 11 | `Bramblechain`<br>`ChainLink`<br>`Frogchain` |
| `darken_screen` | Boolean | If true, darkens the entire screen during the ability's execution. | 11 | `false`<br>`true` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 11 | `{ . . . }` |
| [`end`](../Reference_and_Meta/Enums.md#enum-end) | Enum | Defines the final animation state or offset vector for a particle's lifespan. | 10 | `[-20, 0, 20]`<br>`[0, -450, 0]`<br>`[0, [200, 900], 0]` |
| [`start`](../Reference_and_Meta/Enums.md#enum-start) | Enum | Specifies the initial animation state played at the beginning of an ability. | 10 | `attack`<br>`lickAttack`<br>`monkAttack` |
| [`beam_cap`](../Reference_and_Meta/Enums.md#enum-beam_cap) | Enum | Specifies the MovieClip used for the visual cap (end) of a beam effect. | 10 | `Gambitmouthbeamcap`<br>`fx_bloatlasercap`<br>`fx_kingbloodlasercap` |
| [`beam_clip`](../Reference_and_Meta/Enums.md#enum-beam_clip) | Enum | Specifies the MovieClip used for the main body of a beam effect. | 10 | `Gambitmouthbeam`<br>`fx_bloatlaser`<br>`fx_kingbloodlaser` |
| `bounce_on_hit` | Boolean | If true, the projectile bounces off the first target it hits instead of being destroyed. | 10 | `false`<br>`true` |
| `darken_screen_exclude_characters_on_tile` | Boolean | If true, characters standing on a tile are not darkened when the screen darkens. | 10 | `false`<br>`true` |
| [`jump_start_animation`](../Reference_and_Meta/Enums.md#enum-jump_start_animation) | Enum | Determines which character animation plays at the start of a jump ability. | 10 | `bellyflopStart`<br>`enterbattle`<br>`gravitySlamStart` |
| [`loop`](../Reference_and_Meta/Enums.md#enum-loop) | Enum | Specifies the character animation that plays repeatedly during an ability's execution. | 10 | `attack`<br>`lickAttack`<br>`monkAttack` |
| [`prime_animation`](../Reference_and_Meta/Enums.md#enum-prime_animation) | Enum | Specifies the character animation that plays during the ability's priming or charge phase. | 10 | `angry`<br>`chargeholy`<br>`command1` |
| `max_tiles_single_loop` | Integer | The maximum number of tiles the unit can traverse during a single animation loop. | 9 | `1`<br>`5`<br>`6` |
| `sync_speed` | Integer | The movement speed (in frames per tile) used to synchronize the animation with traversal. | 9 | `17`<br>`22`<br>`28` |
| [`random_delay`](../Reference_and_Meta/Arrays.md#array-random_delay) | Array | A random range [min, max] in frames added to delay the start of an FX or animation. | 9 | `[0, 120]`<br>`[30 50]`<br>`[70 100]` |
| `fx_is_placeholder_animation` | Boolean | If true, marks the associated FX animation as a temporary placeholder. | 8 | `true` |
| `aoe_spell_on_land` | Boolean | If true, triggers an area-of-effect spell upon the unit landing after a jump or movement. | 7 | `true` |
| `fx_random_flip` | Boolean | If true, the FX graphic randomly flips horizontally at spawn time. | 7 | `true` |
| [`land_animation`](../Reference_and_Meta/Enums.md#enum-land_animation) | Enum | Specifies the character animation that plays when the unit lands after a jump. | 7 | `none` |
| [`miss_particle`](../Reference_and_Meta/Enums.md#enum-miss_particle) | Enum | Specifies the FX particle effect emitted when the ability misses its target. | 7 | `fx_tentaclestrangleMiss` |
| `use_super_armor` | Boolean | If true, the unit cannot be interrupted or knocked back during this ability. | 7 | `false`<br>`true` |
| [`air_animation`](../Reference_and_Meta/Enums.md#enum-air_animation) | Enum | Specifies the character animation that plays while the unit is airborne during a jump. | 6 | `bellyflop_air`<br>`entrance`<br>`gravitySlam_air` |
| [`custom_priming_animation`](../Reference_and_Meta/Enums.md#enum-custom_priming_animation) | Enum | Specifies a custom idle animation for the unit while it is priming an ability. | 6 | `idleCommand1`<br>`idleCommand2`<br>`idleCommand3` |
| `darken_screen_exclude_self` | Boolean | If true, the casting unit is not darkened when the screen darkens. | 6 | `true` |
| `darken_screen_start_early` | Boolean | If true, the screen darkening effect begins before the main ability animation. | 6 | `true` |
| `fall_randomize_timing` | Float | The maximum random fraction of the fall duration added to stagger when objects fall from the sky. | 6 | `.3` |
| `min_throw_height` | Float | The minimum height (in tiles) the projectile reaches during an arc or toss. | 6 | `.25`<br>`0`<br>`1.75` |
| `single_projectile` | Boolean | If true, only a single projectile is spawned instead of a volley or spread. | 6 | `true` |
| [`miss_random_delay`](../Reference_and_Meta/Arrays.md#array-miss_random_delay) | Array | A random range [min, max] in frames added to delay the miss particle effect. | 6 | `[0, 20]`<br>`[0, 60]` |
| [`mode`](../Reference_and_Meta/Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 5 | `equal`<br>`greater`<br>`greater_or_equal` |
| [`detatched_animation`](../Reference_and_Meta/Enums.md#enum-detatched_animation) | Enum | Specifies a visual MovieClip that plays independently from the unit's main body. | 5 | `LiquidMetalSpear`<br>`SpearGuyAttack`<br>`TinaSpear` |
| `detatched_animation_reach` | Integer | The tile range at which the detached animation is displayed. | 5 | `20`<br>`3`<br>`4` |
| [`empty_animation`](../Reference_and_Meta/Enums.md#enum-empty_animation) | Enum | Specifies the character animation that plays when the unit's ability has no charges remaining. | 5 | `empty` |
| `fixed_jump_height` | Float | The fixed height (in tiles) the unit reaches during a jump, overriding default arc calculations. | 4 | `1`<br>`3.5` |
| [`rocket_swirl`](./Abilities_and_Spells.md#object-rocket_swirl) | Object  | An object defining the spiral rotation parameters for a rocket-style projectile. | 4 | `{ . . . }` |
| `sync_frames` | Integer | The total number of animation frames used to synchronize a looping ability sequence. | 4 | `26`<br>`34` |
| [`dash_decelerating_animation`](../Reference_and_Meta/Enums.md#enum-dash_decelerating_animation) | Enum | Specifies the character animation that plays when the unit begins slowing down during a dash. | 3 | `dashslow` |
| `decelerate` | Integer | The number of frames over which the unit's dash movement decelerates to a stop. | 3 | `5` |
| `delay_from_map_edge` | Boolean | If true, the projectile's initial delay is calculated based on its distance from the map edge. | 3 | `false`<br>`true` |
| `easing` | Integer | The easing function index applied to the projectile's movement or rotation for smoothing. | 3 | `1` |
| `fixed_jump_speed` | Float | The fixed horizontal speed (in tiles per second) the unit moves at while jumping. | 3 | `.8`<br>`1`<br>`2` |
| [`grab_animation`](../Reference_and_Meta/Enums.md#enum-grab_animation) | Enum | Specifies the character animation that plays when the unit grabs a target for a throw or carry. | 3 | `grab` |
| `lob_yoff` | Float | The vertical offset applied to the lob arc of a projectile or thrown object. | 3 | `-.5` |
| `lock_orientation_during_dash` | Boolean | If true, the unit's facing direction is locked for the duration of the dash animation. | 3 | `true` |
| `use_projectile_spawn_offset` | Boolean | If true, the projectile spawns at the offset defined by the ability's spawn offset rather than the unit's origin. | 3 | `true` |
| `use_rotation_once` | Boolean | If true, the rotation is applied only once at the start of the animation rather than continuously. | 3 | `true` |
| `always_play_animations` | Boolean | If true, the animation plays even when the game is paused or the unit is off-screen. | 2 | `true` |
| `detatched_animation_cutoff` | Boolean | If true, the animation is cut off when the detachment state ends. | 2 | `true` |
| `do_damage_immediately` | Boolean | If true, damage is applied at the start of the animation rather than at the impact frame. | 2 | `true` |
| `jump_height_multiplier` | Float | A multiplier for the jump height during the ability's movement. | 2 | `.25`<br>`2` |
| [`mask_center`](../Reference_and_Meta/Enums.md#enum-mask_center) | Enum | Specifies the mask center point used for area-of-effect targeting. | 2 | `SpearMaskCenter` |
| [`mask_extent`](../Reference_and_Meta/Enums.md#enum-mask_extent) | Enum | Specifies the mask extent (radius or shape) for area-of-effect targeting. | 2 | `SpearMaskExtent` |
| `max_throw_height` | Float | The maximum height of the arc when throwing an object. | 2 | `1.75` |
| [`particle_mat`](../Reference_and_Meta/Enums.md#enum-particle_mat) | Enum | Determines the material shader used for particles during the ability. | 2 | `shadow_occluded_spelldissolve` |
| [`preturn_animation`](../Reference_and_Meta/Enums.md#enum-preturn_animation) | Enum | Specifies the animation played when the unit is selected to act. | 2 | `alertstart` |
| [`primed_alt_animation`](../Assets_and_Localization/Strings.md#string-primed_alt_animation) | String | The name of the animation to play when the ability is primed (ready to fire). | 2 | `"shootPrimed"` |
| [`pseudoprojectile`](../Reference_and_Meta/Enums.md#enum-pseudoprojectile) | Enum | Specifies a visual effect that simulates a projectile without actually firing one. | 2 | `RocketFromAbove` |
| `reverse_orientation` | Boolean | If true, the unit faces the opposite direction during the animation. | 2 | `true` |
| `self_damage_mid_port` | Boolean | If true, the unit takes damage during the middle of a teleport effect. | 2 | `true` |
| `throw_speed` | Integer | The speed multiplier for thrown objects. | 2 | `3` |
| `use_hit_alts` | Boolean | If true, the ability uses alternative hit animations based on hit type. | 2 | `false` |
| [`max_range`](../Reference_and_Meta/Enums.md#enum-max_range) | Equation   | The maximum range of the ability, can be a static number or an expression. | 1 | `"4+(1-clamp(spd,0,1))*2"`<br>`"max(5-int, 1)"`<br>`-1` |
| `min_range` | Integer | The minimum range of the ability. | 1 | `0`<br>`1`<br>`2` |
| [`animate_name`](../Reference_and_Meta/Enums.md#enum-animate_name) | Boolean / Enum | If true, the ability name is animated; if set to an enum, it specifies a specific animation type like 'pointout'. | 1 | `false`<br>`pointout`<br>`true` |
| [`affected_animation`](../Reference_and_Meta/Enums.md#enum-affected_animation) | Enum | Specifies the animation played on the target unit when it is affected by the ability. | 1 | `statDown` |
| [`ally_animation`](../Reference_and_Meta/Enums.md#enum-ally_animation) | Enum | Specifies the animation played on an ally when targeted by a beneficial ability. | 1 | `lickAttack` |
| `apex_distance` | Float | The distance from the start point to the apex of a jump or lob arc. | 1 | `0.875` |
| `apex_time` | Float | The time (in seconds) to reach the apex of a jump or lob arc. | 1 | `.35` |
| `bypass_combatspeed` | Boolean | If true, the ability animation ignores the combat speed setting. | 1 | `true` |
| [`damage_threshold_altanimations`](./Abilities_and_Spells.md#object-damage_threshold_altanimations) | Object  | A mapping of damage threshold values to alternate animation names, triggering different animations based on damage dealt. | 1 | `{ . . . }` |
| [`dash_bonk_animation`](../Reference_and_Meta/Enums.md#enum-dash_bonk_animation) | Enum | Specifies the animation played when the unit collides with an obstacle during a dash. | 1 | `bonk` |
| `delay_from_map_center` | Boolean | If true, the animation delay is calculated based on distance from the center of the map. | 1 | `true` |
| `delay_from_reverse_map_edge` | Boolean | If true, the animation delay is calculated based on distance from the opposite edge of the map. | 1 | `true` |
| `do_animation_offscreen` | Boolean | If true, the animation plays even if the unit is off-screen. | 1 | `true` |
| `do_not_clear_placeholder` | Boolean | If true, the placeholder object (e.g., a held item) is not cleared after the ability resolves. | 1 | `true` |
| `face_targets` | Boolean | If true, the unit rotates to face its target during the animation. | 1 | `true` |
| `first_castpoint_is_self_damage_only` | Boolean | If true, the first cast point of a multi-hit ability only applies self-damage. | 1 | `true` |
| `hang_time` | Float | The duration of the hang time at the apex of a jump or lob arc. | 1 | `.6` |
| `jump_speed_multiplier` | Float | A multiplier for the horizontal speed during a jump. | 1 | `1.5` |
| `lob_speed` | Float | The speed of a lobbed projectile's arc. | 1 | `.5` |
| `othercat_placeholder_available` | Boolean | If true, a placeholder for another cat (ally) is available for multi-cat abilities. | 1 | `true` |
| `precast_delay` | Float | A delay (in seconds) before the casting animation begins. | 1 | `.25` |
| `uncatchable` | Boolean | If true, the projectile or effect cannot be caught or intercepted. | 1 | `true` |
| `use_directional_animations` | Boolean | If true, the ability uses directional animations based on the unit's facing or movement direction. | 1 | `true` |
| `use_origin_offsets` | Boolean | If true, the animation uses offset values relative to the unit's origin point. | 1 | `false` |
| [`spawn_offset`](../Reference_and_Meta/Arrays.md#array-spawn_offset) | Array | A 3D vector offset [x, y, z] for where the spawn effect appears relative to the unit. | 1 | `[0, .5, 0]` |

</details>


---  


### Object: `meta`


**Definition:** Contains metadata for the ability including name, description, class, and type icon.  
**Total Count:** 2374

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1641 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1597 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`class`](../Reference_and_Meta/Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 876 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`type_icon`](../Reference_and_Meta/Enums.md#enum-type_icon) | Enum  | Determines the icon type (e.g., 'defense', 'heal', 'ranged') displayed on the ability or item. | 283 | `"attack"`<br>`"buff"`<br>`"debuff"` |
| [`animate_name`](../Reference_and_Meta/Enums.md#enum-animate_name) | Boolean / Enum   | If true, the ability name is animated; if set to an enum, it specifies a specific animation type like 'pointout'. | 177 | `false`<br>`pointout`<br>`true` |
| [`icon_shell_frame`](../Reference_and_Meta/Enums.md#enum-icon_shell_frame) | Enum | Specifies the shell frame type (e.g., 'attack', 'damage') for the ability's icon border. | 28 | `"attack"`<br>`attack`<br>`big_damage` |
| [`is_move`](../Reference_and_Meta/Enums.md#enum-is_move) | Boolean / Enum | If set to true or 'auto', marks the ability as a movement action. | 20 | `auto`<br>`true` |
| [`ability_icon`](../Reference_and_Meta/Enums.md#enum-ability_icon) | Enum | Specifies the specific icon graphic for the ability. | 14 | `"BreakShortCircuit"`<br>`"Escape"`<br>`"Flail"` |
| [`tooltip_values`](../Reference_and_Meta/Arrays.md#array-tooltip_values) | Array | An array of equation strings used to dynamically generate numeric display values in the ability's tooltip, such as damage or healing ranges. | 9 | `["X"]`<br>`["max((X-1)*2, 0)"]`<br>`["max(X*3, 0)"]` |
| [`icon_damage_display`](../Assets_and_Localization/Strings.md#string-icon_damage_display) | String | Specifies the static text or range shown on the ability icon to represent its damage output (e.g., "1-5" or "?"). | 8 | `"0-25"`<br>`"0-50"`<br>`"1-5"` |
| `icon_damage_display_eq` | Equation | An equation string that dynamically calculates the numeric value displayed on the ability icon for damage or healing. | 7 | `"10+bonus_melee_ability_damage"`<br>`"3+bonus_melee_ability_damage"`<br>`1+bonus_spell_damage_display` |
| `is_basic_attack` | Boolean | If true, this ability is treated as a basic attack, typically used for default melee or ranged strikes without special properties. | 4 | `false`<br>`true` |
| [`icon_damage_type`](../Reference_and_Meta/Enums.md#enum-icon_damage_type) | Enum | Determines which damage type icon (magic or physical) is displayed on the ability icon. | 3 | `magic`<br>`physical` |
| `is_trinket` | Boolean | If true, this ability is classified as a trinket, typically a one-use or passive item effect with its own UI category. | 3 | `true` |
| `dont_visualize_ai` | Boolean | If true, the AI's visualization of this ability is suppressed. | 2 | `true` |
| `is_weapon` | Boolean | If true, this ability is classified as a weapon, allowing it to benefit from weapon-specific modifiers and UI grouping. | 2 | `true` |
| [`icon_damage_display_suffix`](../Assets_and_Localization/Strings.md#string-icon_damage_display_suffix) | String | A string appended to the damage display on the ability icon, such as "x10" to indicate multiplier attacks. | 2 | `"x10"`<br>`"x2"` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `damage_instance`


**Definition:** Defines damage properties, effects, and healing for the ability's direct damage.  
**Total Count:** 2346

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#object-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 2342 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1785 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1554 | passives<br>class<br>tag |
| [`damage`](./Abilities_and_Spells.md#object-damage) | Equation / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1446 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 358 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 352 | `[`<br>`[Heat Fire]` |
| `knockback` | Equation | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 254 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| `ai_base_score` | Integer | The base priority score the AI assigns to using this damage instance, with higher values indicating greater preference. | 223 | `-99999`<br>`-999999`<br>`1` |
| `heal` | `Equation` | An equation string that determines the amount of health restored by this damage instance. | 122 | `"ceil(X*item_aux/100)"`<br>`0`<br>`1` |
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target regardless of accuracy or evasion. | 110 | `true` |
| `incidentally_collects_pickups` | `Boolean` | If true, the damage instance collects nearby pickups (e.g., coins, items) as part of its effect. | 103 | `false`<br>`true` |
| `custom_additional_ai_weight` | `String` | A string identifier for a custom AI weighting condition that modifies the AI's scoring for this damage instance. | 82 | `avoid_redundant_debuffs`<br>`avoid_redundant_debuffs_strict`<br>`avoid_target_map_top` |
| `piercing` | `Boolean` | If true, the damage instance ignores armor or damage reduction effects on the target. | 52 | `true` |
| `makes_contact` | `Boolean` | If true, the damage instance is considered a contact hit, triggering contact-based passives on both the attacker and target. | 40 | `false`<br>`true` |
| `layer` | `String` | Specifies the layer on which the ability's effect operates (e.g., characters, tiles, gas). | 26 | `2`<br>`all`<br>`characters` |
| `blocked_damage` | Equation | An equation string that calculates the amount of damage that can be blocked or reduced by the target's defenses. | 24 | `"(3+bonus_melee_ability_damage)*2"`<br>`3+bonus_melee_ability_damage`<br>`5` |
| `raw_damage` | `String` | An equation string that calculates the base damage before any modifiers or bonuses are applied. | 22 | `"(con+1)/2"`<br>`"8-X"`<br>`"max((X-1)*2, 0)"` |
| `ranged` | Boolean | If true, the damage instance is considered a ranged attack, interacting with ranged-specific modifiers and passives. | 17 | `Ranged`<br>`true` |
| `crit_chance` | Float | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 16 | `-999999`<br>`.05*X`<br>`.25` |
| `override_trample_damage` | `Boolean` | If true, this damage instance replaces any default trample damage when the unit passes through an occupied tile. | 15 | `true` |
| `contact_requires_adjacency` | Boolean | If false, contact effects are not restricted to adjacent tiles, allowing contact to trigger at range. | 14 | `false` |
| `can_revive` | `Boolean` | If true, the damage instance can revive a downed unit instead of dealing damage. | 8 | `true` |
| `show_damage_on_0` | `Boolean` | If true, the damage number is still displayed even when the resulting damage is zero. | 6 | `true` |
| `force_play_hit_animation` | `Boolean` | If true, the hit animation is forced to play regardless of other conditions (e.g., miss or block). | 5 | `true` |
| `blocked_multiplier` | `Number` | A multiplier applied to blocked damage, increasing the effectiveness of the defensive reduction. | 4 | `2` |
| `accuracy` | Float | A decimal value (e.g., .5) representing the base hit chance of the damage instance, where 1.0 is guaranteed. | 3 | `.5` |
| `can_collect_pickups` | `Boolean` | If true, the damage instance can collect pickups from the target's tile as part of its effect. | 3 | `true` |
| `can_instapop` | `Boolean` | If false, the ability cannot instantly kill or remove the target, often used for non-lethal effects. | 2 | `false` |
| `force_no_contact` | `Boolean` | If true, the damage instance does not trigger contact-based passives even if it would normally be a contact hit. | 2 | `true` |
| `non_lethal` | `Boolean` | If true, the damage instance cannot reduce a unit below 1 HP, preventing kills. | 2 | `true` |
| `disallow_modifications` | `Boolean` | If true, the damage instance cannot be modified by external effects (e.g., passives, statuses). | 2 | `true` |
| `raw_heal` | `String` | An equation string that calculates the base healing amount before any modifiers are applied. | 2 | `"(str+1)/2"`<br>`"100-X"` |
| `two_way_contact` | `Boolean` | If true, contact effects apply to both the attacker and the target when the damage instance hits. | 2 | `true` |
| [`faction`](../Reference_and_Meta/Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 1 | `allies`<br>`auto`<br>`birds` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |
| `force_no_knockback` | `Boolean` | If true, the damage instance applies no knockback regardless of any knockback values set. | 1 | `true` |
| `damage_shield_only` | `Boolean` | If true, the damage instance only affects damage shields (e.g., barrier effects) and not health directly. | 1 | `true` |
| `final_hit_bonus_damage` | `String` | An equation string that adds bonus damage to the final hit of a multi-hit damage instance. | 1 | `5+bonus_melee_ability_damage` |
| `force_adjacent_and_diagonal_contact` | `Boolean` | If true, contact effects are forced for both adjacent and diagonal tiles even if not normally triggered. | 1 | `true` |
| `hint_dont_lowgravboost` | `Boolean` | If true, the damage instance does not receive a damage boost from low gravity tiles. | 1 | `true` |
| `hit_animation_alt` | `String` | Specifies an alternative hit animation name (e.g., "catch") to play instead of the default on successful hit. | 1 | `catch` |

</details>


---


### Object: `effects`


**Definition:** Applies a list of status effects or visual effects to targets.  
**Total Count:** 2166

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](./Abilities_and_Spells.md#object-dodamage), [`MeleeRevengeDamage`](./Abilities_and_Spells.md#object-meleerevengedamage), [`ROOT`](./Abilities_and_Spells.md#object-root), [`RevengeDamage`](./Abilities_and_Spells.md#object-revengedamage), [`bonk_damage`](./Abilities_and_Spells.md#object-bonk_damage), [`damage_instance`](./Abilities_and_Spells.md#object-damage_instance), [`empty_self_damage`](./Abilities_and_Spells.md#object-empty_self_damage), [`self_damage`](./Abilities_and_Spells.md#object-self_damage), [`splash_damage`](./Abilities_and_Spells.md#object-splash_damage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 976 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 510 | Default<br>FormChange<br>Druid |
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 102 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 89 | `1`<br>`2`<br>`3` |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 77 | `1`<br>`10`<br>`2` |
| `IgnoreSelf` | `Number` | If set to 1 or true, the damage instance ignores the source unit (does not affect itself). | 75 | `1`<br>`true` |
| [`Bruise`](../Reference_and_Meta/Arrays.md#array-bruise) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 70 | `1`<br>`2`<br>`3` |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 66 | `1`<br>`10`<br>`2` |
| `ChangeTile` | `String` | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 62 | `BlankTile`<br>`BrambleTile`<br>`CreepTile` |
| [`Else`](./Abilities_and_Spells.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 59 | `{ . . . }` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 55 | `1`<br>`10`<br>`2` |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 49 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `Cleanse` | Integer | The number of stacks of negative status effects removed from the target. | 44 | `0`<br>`1` |
| [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 38 | `{ . . . }` |
| [`Confusion`](../Reference_and_Meta/Arrays.md#array-confusion) | Array / Integer  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 35 | `1`<br>`10`<br>`2` |
| [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy) | Object  | An object containing status effects or actions applied only if the target is an enemy. | 35 | `{ . . . }` |
| `SpeedUp` | Array / Equation | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 34 | `-1`<br>`-2`<br>`-4` |
| [`Temporary`](./Abilities_and_Spells.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 34 | `{ . . . }` |
| `BounceObject` | `String` | Specifies the object or projectile to spawn and bounce from the target. | 31 | `AllyRotFly`<br>`Amoeba`<br>`BeefyCharmedLeech` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 29 | `-1`<br>`-2`<br>`1` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 28 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `TransformAbility` | `String` | Specifies the ability that replaces the current ability. | 28 | `BerserkDash`<br>`BerserkDash2`<br>`BirthSquirrel` |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 27 | `{ . . . }` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 26 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Slow`](../Reference_and_Meta/Arrays.md#array-slow) | Array / Equation  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 25 | `-1`<br>`1`<br>`2` |
| [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally) | Object  | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 25 | `{ . . . }` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 23 | `1`<br>`10`<br>`2` |
| [`Weakness`](../Reference_and_Meta/Arrays.md#array-weakness) | Array / Integer  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 23 | `1`<br>`2`<br>`3` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 22 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`Blind`](../Reference_and_Meta/Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 22 | `-1`<br>`1`<br>`2` |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 22 | `1`<br>`2` |
| [`Immobile`](../Reference_and_Meta/Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 21 | `0`<br>`1`<br>`10%` |
| [`ConstitutionUp`](../Reference_and_Meta/Arrays.md#array-constitutionup) | Array / Equation  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 21 | `-1`<br>`-2`<br>`1` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 21 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `VisualFXTile` | `String` | Specifies the name of the visual effect to play on the target tile. | 21 | `Bolt`<br>`BurnTrigger`<br>`Explosion` |
| [`Sleep`](../Reference_and_Meta/Arrays.md#array-sleep) | Array / Integer  | The amount of sleep stacks applied, or an [stacks, probability] array. | 21 | `1`<br>`2`<br>`3` |
| `EvolveAbilityFromPool` | `String` | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 21 | `Butcher`<br>`Druid`<br>`Fighter` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Equation  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 20 | `1`<br>`2`<br>`3` |
| `Vaporize` | `Number` | Removes the target from play, preventing its corpse from being interacted with. | 20 | `1`<br>`20` |
| [`Madness`](./Abilities_and_Spells.md#object-madness) | Array / Equation / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 19 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 18 | `1`<br>`10`<br>`2` |
| `RandomStatUp` | Array / Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 17 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 17 | `{ . . . }` |
| `CollectsPickups` | `Number` | If set to 1 or greater, the unit collects pickups (e.g., items) on contact. | 17 | `1`<br>`2` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 16 | `1`<br>`2`<br>`[1 .01]` |
| `OverrideKnockbackDamage` | `Equation` | A formula or flat value that sets the damage dealt when knockback occurs, overriding default calculations. | 16 | `"max(5+bonus_melee_ability_damage, 1)"`<br>`0`<br>`2` |
| [`Consumed`](./Abilities_and_Spells.md#object-consumed) | Object  | An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`. | 15 | `{ . . . }` |
| `VaporizeCorpse` | `Number` | If set, vaporizes the target's corpse, preventing revival. | 15 | `1` |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 14 | `1`<br>`2`<br>`4` |
| `TakeExtraTurn` | `Number` | The number of extra turns granted to the source. | 14 | `1` |
| `RefreshMovePoints` | `Number` | The amount of movement points restored to the source. | 14 | `1` |
| `FaceAway` | `Number` | If set, forces the target to face away from the source. | 14 | `1` |
| `ChangeCatClass` | `String` | Specifies the new class to assign to the unit. | 14 | `Butcher`<br>`Colorless`<br>`Druid` |
| `EndTurn` | `Number` | If set to 1, ends the current unit's turn immediately after this effect. | 14 | `1` |
| `TransformBasicAttack` | `String` | Specifies the ability that replaces the unit's basic attack. | 14 | `AntlerSwipe`<br>`AntlerSwipe2`<br>`Chitter` |
| [`CatPartsTransform`](./Abilities_and_Spells.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 13 | `{ . . . }` |
| [`RandomMagicMissile`](./Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. | 13 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Petrify`](../Reference_and_Meta/Arrays.md#array-petrify) | Array / Integer  | The amount of petrify stacks applied, or an [stacks, probability] array. | 13 | `1`<br>`[1 .15]`<br>`[1 .1]` |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 13 | `{ . . . }` |
| `Leeches` | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 13 | `1`<br>`2`<br>`3` |
| [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional_boss) | Object  | Contains effects that apply only if the target is a boss enemy. | 13 | `{ . . . }` |
| `GenericDebuff` | `Number` | The number of stacks of a generic, untooltipped debuff applied to the target. | 13 | `1`<br>`10`<br>`100` |
| `LuckUp` | Equation | The amount of Luck stat changed on the source, affecting random chance outcomes. | 12 | `-1`<br>`-2`<br>`-4` |
| `Displace` | `Number` | If set to 1, the unit is displaced to another location (e.g., teleport). | 12 | `1` |
| [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 11 | `{ . . . }` |
| `FullHeal` | Integer | If non-zero, fully restores the target's health. | 11 | `0`<br>`1` |
| [`Cleave`](./Abilities_and_Spells.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 11 | `{ . . . }`<br>`1` |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#object-applytosourceonkill) | Object  | Contains effects that are applied to the source when it kills the target. | 11 | `{ . . . }` |
| [`DoScreenShake`](./Abilities_and_Spells.md#object-doscreenshake) | Integer / Object  | If an integer, the number of screen shakes; if an object, defines the duration and intensity of the screen shake. | 11 | `{ . . . }`<br>`1` |
| [`ChanceToBreakFree`](./Abilities_and_Spells.md#object-chancetobreakfree) | Object  | Defines the chance and ability used for a grappled or restrained unit to break free. | 11 | `{ . . . }` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 10 | `1`<br>`2`<br>`3` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 10 | `-1`<br>`1`<br>`2` |
| `RefreshActPoints` | `Number` | The amount of action points restored to the source. | 10 | `1` |
| [`MagicWeakness`](../Reference_and_Meta/Arrays.md#array-magicweakness) | Array / Integer  | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 10 | `1`<br>`2`<br>`3` |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional_speculative) | Object  | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 10 | `{ . . . }` |
| `PurgeAll` | `Number` | If non-zero, removes all temporary status effects (buffs, debuffs) from the target. | 10 | `1` |
| [`Conditional_FormulaIsPositive`](./Abilities_and_Spells.md#object-conditional_formulaispositive) | Object  | Defines effects that apply only if a given formula evaluates to a positive value. | 10 | `{ . . . }` |
| `PartialPurge` | `Number` | The amount of beneficial status effects removed from the target. | 10 | `1` |
| [`Marked`](../Reference_and_Meta/Arrays.md#array-marked) | Array / Integer  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 9 | `1`<br>`3`<br>`5` |
| `Ammo` | Integer | The amount of ammo to add or remove (negative values subtract). | 9 | `-1`<br>`-99999`<br>`1` |
| `VisualFX` | `String` | Specifies the name of the visual effect to play. | 9 | `BigMagicMissileBlast`<br>`Bolt`<br>`Cleanse` |
| [`ApplyPassives`](./Abilities_and_Spells.md#object-applypassives) | Object  | Specifies the passives or status effects to apply to the unit. | 9 | `{ . . . }` |
| `DeferVaporize` | `Number` | If set to 1, the unit's vaporize (instant death) is delayed until the end of the current action. | 9 | `1` |
| `SpawnCreep` | `Number` | If set to 1, spawns a creep tile under the target. | 9 | `1` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 8 | `1`<br>`2`<br>`3` |
| [`Rot`](../Reference_and_Meta/Arrays.md#array-rot) | Array / Integer  | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 8 | `-999999`<br>`1`<br>`2` |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate) | Object  | An object containing effects that can be applied to inanimate objects. | 8 | `{ . . . }` |
| `ChanceToBreak` | Integer | Specifies the percentage chance that the item breaks on use. | 8 | `100`<br>`15`<br>`20` |
| `OverrideChainKnockback` | `Number` | The custom number of tiles for chain knockback, overriding the default. | 8 | `0`<br>`1`<br>`10` |
| `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 7 | `1` |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 7 | `1`<br>`3` |
| `Instakill` | `Number` | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 7 | `25`<br>`50`<br>`999` |
| `ForceAttack` | `Number` | If set to 1, forces the target to perform an attack against a random or specified target. | 7 | `1` |
| `KnockbackDamageImmuneUntilSettled` | `Number` | If non-zero, makes the target immune to damage from knockback until they stop moving. | 7 | `1` |
| [`ApplyStatusIfCrit`](./Abilities_and_Spells.md#object-applystatusifcrit) | Object  | Defines effects that are applied only when the attack scores a critical hit. | 7 | `{ . . . }` |
| `TempRangeUp` | Integer | The amount of temporary range increase applied. | 7 | `1`<br>`2`<br>`20` |
| `BramblesOnHit` | `Number` | If set to 1, spawns bramble tiles on the target's location on hit. | 7 | `1` |
| `ContextualHeal` | `Number` | The amount of healing applied contextually (e.g., to allies). | 7 | `1` |
| `ManaSteal` | `Number` | The amount of mana stolen (negative values may drain instead). | 7 | `-1`<br>`5` |
| `TriggerWerewolfTransform` | Array / Float | The number of stacks and probability of triggering the werewolf transformation. | 7 | `.5`<br>`[1 .15]`<br>`[1 .20]` |
| [`ObjectOnHitCharacter`](./Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 6 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`Craft`](./Abilities_and_Spells.md#object-craft) | Object  | Specifies the loot pool and slot to craft an item for the source. | 6 | `{ . . . }` |
| [`Tarred`](../Reference_and_Meta/Arrays.md#array-tarred) | Array / Integer  | The amount of tarred stacks applied, or an [stacks, probability] array. | 6 | `1`<br>`2`<br>`[1 .1]` |
| `Metronome` | `Number` | The number of times Metronome triggers, or an object with stacks and banned abilities. | 6 | `1`<br>`2` |
| `CharismaUp` | Array / Equation | The amount of charisma change, or a keyword like 'item_aux'. | 6 | `-1`<br>`-2`<br>`1` |
| `RemoveStatus` | `String` | The name of the status effect to remove from the source. | 6 | `AlphaCat`<br>`Brace`<br>`DodgeChance_Status` |
| [`BackflipWhenTargeted`](./Abilities_and_Spells.md#object-backflipwhentargeted) | Integer / Object  | The number of backflip charges, or an object defining its ability. | 6 | `{ . . . }`<br>`1`<br>`2`<br>`X` |
| `Drowsy` | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. | 6 | `1`<br>`8` |
| [`Conditional_Corpse`](./Abilities_and_Spells.md#object-conditional_corpse) | Object  | Contains an inner effect block that only executes if the target is a corpse. | 6 | `{ . . . }` |
| `SpiderInfested` | Integer | The number of spider infestation stacks applied. | 6 | `1`<br>`2`<br>`4` |
| `SpawnThingIfHitKills` | `String` | The name of the thing (e.g., a food type) to spawn at the target's location upon a killing blow. | 6 | `Bait`<br>`BigFood`<br>`BiggestFood` |
| `SetHealth` | `Number` | Sets the target's health to a specific flat value or percentage. | 6 | `1`<br>`100%`<br>`50%` |
| `ConjureBonusAbility` | `String` | Specifies the name of the bonus ability to conjure. | 6 | `Class`<br>`Colorless`<br>`Mage` |
| `RandomInjury` | Integer | The number of random injuries applied. | 6 | `1` |
| `ClearStarving` | `Number` | The number of stacks of Starving cleared. | 6 | `1` |
| [`DoDistortionRing`](./Abilities_and_Spells.md#object-dodistortionring) | Object  | Configuration for a distortion ring visual effect, with speed, intensity, and radius. | 6 | `{ . . . }` |
| `SetDistanceDisplace` | `Number` | The fixed distance to displace the target. | 6 | `5` |
| `TeamCastAbility` | `String` | Specifies the ability name for the team to cast, with optional tag restriction and same orientation. | 6 | `Huddle_Impl`<br>`Spin`<br>`TeamFlex_Impl` |
| [`TwisterDisplaceWithDamage`](./Abilities_and_Spells.md#object-twisterdisplacewithdamage) | Object  | Configuration for a twister displacement that deals damage, with min/max distance and damage value. | 6 | `{ . . . }` |
| `BounceRock` | `String` | Specifies the rock object to bounce. | 6 | `LavaBoulder`<br>`SmallLavaRock`<br>`SmallRock` |
| `ScatterHeldCoin` | `Number` | The number of coins scattered, with an optional probability as a second element. | 6 | `1`<br>`[1 .3]`<br>`[1 .5]` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 5 | `1`<br>`10`<br>`100` |
| `Revive` | Integer | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 5 | `1`<br>`100%`<br>`50%` |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#object-conditional_hasstatus) | Object  | Contains an inner effect block that only executes if the target has the specified status effect. | 5 | `{ . . . }` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 5 | `1`<br>`2`<br>`[1 .1]` |
| [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional_notboss) | Object  | Contains effects that apply only if the target is not a boss enemy. | 5 | `{ . . . }` |
| `SoulLink` | Integer | The number of soul link stacks applied. | 5 | `1` |
| `MovementUp` | Integer | The amount of movement increase or decrease applied. | 5 | `-2`<br>`1`<br>`2` |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. | 5 | `-1`<br>`1`<br>`2` |
| `FillMana` | `Number` | The amount of mana restored, or an [amount, probability] array. | 5 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| `Stealth` | Integer | The number of stealth stacks applied. | 5 | `1`<br>`2`<br>`[1 .1]` |
| `Purge` | `Number` | The number of status effects to purge from the target. | 5 | `0`<br>`3` |
| `FlatLeech` | `Number` | The flat amount of health restored to the source when dealing damage, applied after the hit. | 5 | `1`<br>`10`<br>`2` |
| [`Conditional_PlayerCat`](./Abilities_and_Spells.md#object-conditional_playercat) | Object  | Defines effects that only apply if the target is a player-controlled cat. | 5 | `{ . . . }` |
| `ForceMoveAway` | `Number` | The distance to force the target away from the source. | 5 | `1` |
| `ForceMoveTowards` | `Number` | The number of tiles to force the target to move toward the caster. | 5 | `1` |
| `HitExplosion` | `Number` | The radius of the explosion triggered on hit. | 5 | `10`<br>`5`<br>`X` |
| `ObjectOnHit` | `String` | Specifies the object to spawn on the hit tile. | 5 | `Bait`<br>`BiggestFood`<br>`Carcus` |
| `SafeDie` | `Number` | The number of times the unit can survive a fatal hit. | 5 | `1` |
| `SpawnBearTrap` | `Number` | If non-zero, spawns a bear trap on the tile. | 5 | `1` |
| [`Conditional_InForm`](./Abilities_and_Spells.md#object-conditional_inform) | Object  | Contains effects that apply only if the target is in the specified form. | 5 | `{ . . . }` |
| [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional_object) | Object  | Evaluates whether the target is an object (vs a character); if true, applies the effects within; otherwise, runs the Else block. | 5 | `{ . . . }` |
| `Imprison` | `String` | Specifies the type of unit or object to summon as a prison. | 5 | `BeefyCharmedLeech`<br>`CharmedLeech`<br>`Fly` |
| `PopAndSpawn` | `String` | The object (enemy or entity) to spawn on the target's tile, optionally with visual effects. | 5 | `Sprout`<br>`StemCat_HalfHealth`<br>`TheDestroyer` |
| [`CollectsPickupsWithAltEffects`](./Abilities_and_Spells.md#object-collectspickupswithalteffects) | Object  | Contains alternative effects that are applied when collecting pickups. | 5 | `{ . . . }` |
| `KnockbackDirectionIsFacingDirection` | `String` | Specifies how to alter knockback direction relative to the unit's facing: 1 (same), flip (opposite), rotate_right. | 5 | `1`<br>`flip`<br>`rotate_right` |
| `MonkStanceSwitch` | `Number` | The number of times to switch monk stance. | 5 | `1` |
| `ObjectOnHitEmpty` | `String` | Specifies the object to spawn on hitting an empty cell. | 5 | `AnimalEgg`<br>`AnimalEgg2`<br>`HeadTumor` |
| `RefreshMovePointsIfHit` | `Number` | The amount of movement points restored on hit. | 5 | `1` |
| `SpawnRock` | `Number` | The number of rocks to spawn, or an array with stacks and probability. | 5 | `1`<br>`[1, .20]` |
| `UpgradeRandomAbility` | `Number` | The number of random abilities upgraded upon effect. | 5 | `1` |
| `HealthGain` | Integer | The amount of health restored to the source. | 4 | `1`<br>`10`<br>`2` |
| `Charge` | Equation | The number of charge stacks applied. | 4 | `1`<br>`2`<br>`3` |
| `UseAbility` | `String` | The name of the ability the target is forced to use. | 4 | `GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| `Reanimate` | Integer | The percentage chance to reanimate the target. | 4 | `100%`<br>`33%`<br>`50%` |
| [`RandomStatDown`](../Reference_and_Meta/Arrays.md#array-randomstatdown) | Array / Integer / String  | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 4 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`1` |
| `Die` | `Number` | If set, kills the target immediately. | 4 | `1`<br>`6` |
| `Grappled` | Integer | The number of stacks and probability of applying the Grappled status, in format [stacks, probability] or just stacks. | 4 | `1`<br>`[1, .50]`<br>`[1, .75]` |
| `VaporizeInanimate` | `Number` | If non-zero, instantly destroys inanimate objects (corpses, rocks) as if they were vaporized. | 4 | `1` |
| [`SwitchMusic`](./Abilities_and_Spells.md#object-switchmusic) | Object  | Defines a new song or layer for the background music. | 4 | `{ . . . }` |
| `BurgleCoin` | `Number` | The number of coins stolen from the target, or an array of `[number, probability]`. | 4 | `1`<br>`3`<br>`[1 .5]` |
| `FaceCamera` | `Number` | If non-zero, forces the character to rotate and face the camera. | 4 | `1` |
| `SpecificInjury` | `String` | The stat (str, spd, int) to which a specific injury is applied, reducing that stat. | 4 | `int`<br>`spd`<br>`str` |
| [`TakeBonusTurnWithStatus`](./Abilities_and_Spells.md#object-takebonusturnwithstatus) | Object  | Container for status effects applied when taking a bonus turn. | 4 | `{ . . . }` |
| [`ApplyToConsumed`](./Abilities_and_Spells.md#object-applytoconsumed) | Object  | Container for effects that are applied to the consumed object. | 4 | `{ . . . }` |
| [`ArcLightning`](./Abilities_and_Spells.md#object-arclightning) | Object  | Configuration for arc lightning chain, with stacks, chance, max distance, and enemy-only flag. | 4 | `{ . . . }` |
| [`Conditional_Familiar`](./Abilities_and_Spells.md#object-conditional_familiar) | Object  | Container for effects applied if the unit has a familiar, with an optional Else block. | 4 | `{ . . . }` |
| `EnableWeather` | `String` | Specifies the weather effect to enable. | 4 | `KaijuFirestorm`<br>`KaijuMeteornado`<br>`KaijuMeteornadoSolo` |
| `ExplosionIfHitSomething` | `Number` | The radius of explosion triggered if the attack hits an entity. | 4 | `5` |
| [`LateStatusApplication`](./Abilities_and_Spells.md#object-latestatusapplication) | Object  | Container for status effects that are applied late after the main effect. | 4 | `{ . . . }` |
| `RemoveActPoints` | `Number` | The number of action points removed from the target. | 4 | `1` |
| `SendRock` | `Number` | The number of rocks to send as projectiles. | 4 | `1` |
| [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#object-timedelaystatusapplication) | Object  | Container for status effects applied after a specified delay. | 4 | `{ . . . }` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 3 | `1`<br>`2`<br>`3` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 3 | `1`<br>`3` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 3 | `1`<br>`2`<br>`[1, 0.1]` |
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 3 | `-10`<br>`0`<br>`1` |
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. | 3 | `-1`<br>`-2`<br>`1` |
| `Reflect` | Integer | The amount of reflect stacks applied. | 3 | `1`<br>`5` |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 3 | `1`<br>`2`<br>`3` |
| `PoisonLace` | Enum / Equation | Integer or fractional string (e.g., 'X/3') specifying the duration or intensity of the PoisonLace effect. | 3 | `"X/3"`<br>`"X/5"`<br>`1` |
| [`Tangled`](./Abilities_and_Spells.md#object-tangled) | Integer / Object  | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 3 | `{ . . . }`<br>`1`<br>`2`<br>`[1, .05]` |
| `CurrentWeaponDamageUp` | Integer | The amount of temporary damage increase to the current weapon. | 3 | `1`<br>`3`<br>`5` |
| `TempSpeedUp` | Equation | The number of stacks of temporary Speed Up applied to the unit. | 3 | `10`<br>`4`<br>`X` |
| [`Conditional_FirstApplicationThisTurn`](./Abilities_and_Spells.md#object-conditional_firstapplicationthisturn) | Object  | Container for effects applied only on the first application of this ability during the turn. | 3 | `{ . . . }` |
| `DamageOrHealConditionally` | Integer | The amount of conditional damage or healing applied, based on certain conditions (e.g., ally or enemy). | 3 | `1` |
| `DeleteObject` | `Number` | If set, deletes the target object from the map. | 3 | `1` |
| `ExtraBasicAttacks_Status` | Integer | The number of additional basic attacks the unit can perform each turn. | 3 | `1` |
| `TempStrengthUp` | Enum | The number of stacks of temporary Strength Up applied to the unit. | 3 | `1`<br>`2`<br>`X` |
| [`ReviveNextRound`](./Abilities_and_Spells.md#object-revivenextround) | Integer / Object  | The number of revives granted, or an object defining revive properties. | 3 | `{ . . . }`<br>`2` |
| `DestroyTrinket` | `Number` | The number of trinkets destroyed. | 3 | `1` |
| `DisplaceTowardsSource` | `Number` | If set, displaces the target towards the source of the effect. | 3 | `1` |
| `PlayBackground` | Integer | Specifies the background index to play. | 3 | `0`<br>`1` |
| `RepairAll` | `Number` | The amount of durability restored to all equipped items. | 3 | `1`<br>`10` |
| `PullSourceToTarget` | `Number` | The amount of tiles the source is pulled towards the target after the attack. | 3 | `1` |
| `RefreshWeaponAbility` | `Number` | The number of times the weapon's ability is refreshed. | 3 | `1` |
| `NextAttackBonusRange` | Integer | The added range for the unit's next basic attack. | 3 | `1`<br>`3`<br>`5` |
| [`CatPartsSizeScaleStatus`](./Abilities_and_Spells.md#object-catpartssizescalestatus) | Object  | Configures scale multipliers for individual cat body parts (body, arms, mouth). | 3 | `{ . . . }` |
| `CollideWithConsumed` | `String` | Damage formula for collision with consumed objects, e.g., '4+bonus_melee_damage'. | 3 | `1+bonus_melee_damage`<br>`4+bonus_melee_damage`<br>`5+bonus_melee_damage` |
| [`Conditional_AffectedByElement`](./Abilities_and_Spells.md#object-conditional_affectedbyelement) | Object  | Container for effects applied if the target is affected by a specified element, with optional Else block. | 3 | `{ . . . }` |
| [`Conditional_LastHit`](./Abilities_and_Spells.md#object-conditional_lasthit) | Object  | Container for effects applied only on the final hit of a multi-hit attack, with optional Else block. | 3 | `{ . . . }` |
| `CorpseVaporizer` | `Number` | The number of corpses vaporized on hit. | 3 | `1` |
| `DestroyWeapon` | `Number` | The number of weapons destroyed. | 3 | `1` |
| `DestroyWeaponThrow` | `Number` | The number of weapons destroyed after being thrown. | 3 | `1` |
| [`DustOnHit`](./Abilities_and_Spells.md#object-dustonhit) | Object  | Configuration for a dust object spawned on hit. | 3 | `{ . . . }` |
| `ForceDisplace` | `Number` | The distance the target is forced to displace. | 3 | `1` |
| `ForceMoveTowardsEnemies` | `Number` | Specifies the ability or distance to force the target to move towards enemies. | 3 | `1`<br>`DumbMove_Impl`<br>`MoveOne` |
| `InstantMaxHealthUp` | `Number` | The amount of permanent maximum health increase. | 3 | `20`<br>`4` |
| `RepairOnKill` | `Number` | The number of charges restored to the ability upon killing a target. | 3 | `1`<br>`2` |
| [`SetCrazyEyeBackgroundWeights`](./Abilities_and_Spells.md#object-setcrazyeyebackgroundweights) | Object  | An object containing a `weights` array that sets the weighting for which Crazy Eye background variant is displayed. | 3 | `{ . . . }` |
| `SpawnCustomTrap` | `String` | Specifies the name of a custom trap blueprint to spawn at the target location. | 3 | `CharmTrap`<br>`EggSackTrap`<br>`SpikeTrap` |
| `SpawnNeutralWebTrapOnMiss` | `Number` | The number of neutral web traps spawned on the tile if the attack misses. | 3 | `1` |
| `VaporizeTarget` | `Number` | If non-zero, instantly destroys the target, leaving no corpse. | 3 | `1` |
| [`ApplyMultipleTimes`](./Abilities_and_Spells.md#object-applymultipletimes) | Object  | An object containing a `stacks` value that specifies how many times the nested effects are applied. | 3 | `{ . . . }` |
| `DoubleStatus` | `String` | The name of a status effect whose stacks are doubled when applied. | 3 | `Bleed`<br>`Burn`<br>`Poison` |
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 2 | `1`<br>`3`<br>`4` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 2 | `1`<br>`10`<br>`100` |
| `Knockback` | Equation | The number of tiles the target is pushed away from the source on hit. | 2 | `1`<br>`10`<br>`2` |
| `SizeScale` | Float | The multiplier applied to the unit's visual and hitbox size. | 2 | `.4`<br>`.6`<br>`.7` |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. | 2 | `1`<br>`2`<br>`3` |
| `ImmediateUseAbility` | `String` | Specifies the name of an ability to be triggered instantly from this effect. | 2 | `FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `IgnoreDamage` | `Number` | If set, the target ignores all damage for the duration. | 2 | `1` |
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. | 2 | `1`<br>`9999` |
| [`Conditional_BadRoll`](./Abilities_and_Spells.md#object-conditional_badroll) | Object  | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 2 | `{ . . . }` |
| `SmartMetronome` | `Number` | The number of stacks of a buff that increases damage by a percentage, with an optional upgrade flag. | 2 | `20` |
| [`BodyGuard`](./Abilities_and_Spells.md#object-bodyguard) | Object  | An object that applies a bodyguard status, optionally linking to a swap ability. | 2 | `{ . . . }` |
| `FreeSpell` | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. | 2 | `1`<br>`2` |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 2 | `{ . . . }` |
| `RepairWeapon` | Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 2 | `1`<br>`6`<br>`99` |
| `ShortCircuit` | Integer | The number of stacks of the ShortCircuit status effect. | 2 | `1` |
| [`SpawnCoinAnywhere`](../Reference_and_Meta/Arrays.md#array-spawncoinanywhere) | Array / Integer  | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 2 | `1`<br>`[1 .5]` |
| [`Conditional_IsSelf`](./Abilities_and_Spells.md#object-conditional_isself) | Object  | An object containing effects that are only applied if the target is the source unit itself. | 2 | `{ . . . }` |
| `Counterspell` | `Number` | If non-zero, negates the next incoming enemy spell and triggers the configured counterspell effects. | 2 | `1` |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#object-destroyequipmentandattachparasite) | Object  | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 2 | `{ . . . }` |
| [`Math`](./Abilities_and_Spells.md#object-math) | Object  | An object containing a `stacks` value that determines how many times the nested effects are applied. | 2 | `{ . . . }` |
| `TradeLife` | `Number` | The amount of health life traded, or a template for a TradeLife ability. | 2 | `1` |
| `DoubleCastSpell` | Integer | The number of times the next spell cast is doubled, or a template with name and tooltip. | 2 | `1`<br>`2` |
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. | 2 | `1` |
| `Lifesteal` | Integer | The amount of lifesteal stacks applied. | 2 | `1`<br>`3` |
| `RangeUp` | Integer | The number of stacks of bonus attack range applied. | 2 | `1` |
| [`Conditional_Shielded`](./Abilities_and_Spells.md#object-conditional_shielded) | Object  | An object containing effects that are only applied if the target has a shield active. | 2 | `{ . . . }` |
| `PermanentStrength` | `Number` | The amount of permanent bonus strength (physical damage modifier) granted. | 2 | `1`<br>`2` |
| `Shatter` | `Number` | The amount of damage dealt when a frozen or petrified status is shattered, or a template definition for a Shatter ability. | 2 | `15` |
| `DoubleLoot` | Integer | The multiplier for loot drops, where 1 or 2 doubles the loot. | 2 | `1`<br>`2` |
| [`KnockOutCoin`](./Abilities_and_Spells.md#object-knockoutcoin) | Integer / Object  | The number of coins knocked out, with an optional probability or an object with stacks and chance. | 2 | `{ . . . }`<br>`1`<br>`[1 .5]` |
| `ManaLeeches` | Integer | The number of mana leech stacks applied. | 2 | `1`<br>`2` |
| `TempDexterityUp` | Enum | The number of temporary dexterity stacks applied, or a string alias like 'X'. | 2 | `2`<br>`X` |
| `TempInitiativeChange` | Integer | The flat change to the unit's initiative value. | 2 | `-100`<br>`-999`<br>`100` |
| `TempSpellDamageUp` | Integer | The amount of temporary spell damage increase applied. | 2 | `1` |
| `TrailBlazer` | Array / Equation | The number of trail blazer stacks applied, or a string alias like 'mov'. | 2 | `1`<br>`mov` |
| `BonusKnockbackDamage` | `Number` | The extra damage dealt per tile of knockback. | 2 | `2`<br>`3`<br>`5` |
| `CharmedForceAttack` | `Number` | If non-zero, forces the charmed target to use its basic attack on a random nearby unit. | 2 | `1` |
| [`Conditional_OncePerBattle`](./Abilities_and_Spells.md#object-conditional_onceperbattle) | Object  | An object containing effects that can only trigger once per battle, preventing double-activation. | 2 | `{ . . . }` |
| `LeaveBehindRockOnKnockback` | `Number` | If non-zero, leaves behind a rock on each tile the target is knocked through. | 2 | `1` |
| `PullSourceToKnockbackImmuneTarget` | `Number` | The amount of pull force applied to the source toward a knockback-immune target. | 2 | `1` |
| `RandomDistanceDisplace` | `Number` | The number of stacks of a random distance displacement effect, or an object with stacks, min_dist, and chance. | 2 | `20` |
| `Ostracized` | Integer | The number of stacks of Ostracized applied. | 2 | `1`<br>`2`<br>`4` |
| `Possessed` | Integer | The number of possession stacks applied, or a template with name and tooltips. | 2 | `1` |
| `TempMovement` | Array / Equation | The amount of temporary movement range added, or a string alias like 'mov'. | 2 | `1`<br>`20`<br>`mov` |
| `RemoveMovePoints` | `Number` | The number of move points to remove from the target, preventing them from moving. | 2 | `1` |
| `RepairWeaponCondition` | `Number` | The amount of weapon condition restored. | 2 | `1` |
| `SetShield` | `Number` | Sets the target's shield value to a specific flat amount. | 2 | `0`<br>`88` |
| `SpeculativeMoveSelfCorpseOffMap` | `Number` | If true, attempts to remove the character's corpse from the map, used for speculative AI targeting. | 2 | `1` |
| `StanceSwitchToMelee` | `Number` | If set, switches the source to melee stance. | 2 | `1` |
| [`TakeBonusTurnWithAIControl`](./Abilities_and_Spells.md#object-takebonusturnwithaicontrol) | Object  | An object configuring whether the bonus turn happens at the end of the round and whether spells are included. | 2 | `{ . . . }` |
| `TempTrampleUntilSettled` | `Number` | The number of stacks of temporary Trample applied to the source, allowing movement through enemies until the source ends its turn. | 2 | `3` |
| `TempCritChanceUp` | Integer | The amount of temporary critical hit chance (in percentage points) added. | 2 | `100`<br>`30` |
| `AddSpiritBombCharges` | `Number` | The number of charges added to the Spirit Bomb ability. | 2 | `1`<br>`2` |
| `Bound` | `Number` | The number of stacks of the Bound status effect applied to the target. | 2 | `3` |
| `CancelPrimedAbilities` | `Number` | If non-zero, cancels any primed abilities on the target. | 2 | `1` |
| `ChangeFaction` | `String` | Specifies the name of the faction to switch the target to. | 2 | `sabertooths` |
| `CollideWithThrowTarget` | `Number` | Determines whether the thrown object collides with the primary target (0 disables collision). | 2 | `0` |
| [`Conditional_BossOrBig`](./Abilities_and_Spells.md#object-conditional_bossorbig) | Object  | An object containing effects that are only applied if the target is a boss or large unit. | 2 | `{ . . . }` |
| [`Conditional_Buddy`](./Abilities_and_Spells.md#object-conditional_buddy) | Object  | An object containing effects that are only applied if the caster has a buddy (follower) unit. | 2 | `{ . . . }` |
| [`Conditional_DestructibleCorpse`](./Abilities_and_Spells.md#object-conditional_destructiblecorpse) | Object  | An object containing effects that are only applied if the corpse is destructible. | 2 | `{ . . . }` |
| [`Conditional_NotAlly`](./Abilities_and_Spells.md#object-conditional_notally) | Object  | An object containing effects that are only applied if the target is not an ally of the source. | 2 | `{ . . . }` |
| [`Conditional_NotBossOrBig`](./Abilities_and_Spells.md#object-conditional_notbossorbig) | Object  | An object containing effects that are only applied if the target is not a boss or large unit. | 2 | `{ . . . }` |
| [`Conditional_NotShielded`](./Abilities_and_Spells.md#object-conditional_notshielded) | Object  | An object containing effects that are only applied if the target does not have a shield active. | 2 | `{ . . . }` |
| `CopySpells` | `Number` | The number of spells copied from the target, or an object specifying `stacks` and whether the copy is `upgraded`. | 2 | `1` |
| `DamageBasedOnMissingHealth` | `Number` | The percentage of the target's missing health dealt as additional damage. | 2 | `25`<br>`50` |
| `DamageDistanceAOEFalloff` | `Number` | The falloff multiplier applied to AoE damage based on distance from the center of the effect. | 2 | `1`<br>`2` |
| `DamageTrinket` | `Number` | The amount of durability damage dealt to the target's equipped trinket. | 2 | `1` |
| `DelayedFury` | `Number` | The percentage of Fury damage that is stored and applied after a delay. | 2 | `0`<br>`75` |
| `DieViaAbilityInternally` | `Number` | If non-zero, causes the target to die via an internal ability trigger. | 2 | `1` |
| `DisplaceToOriginalPosition` | `Number` | If non-zero, returns the unit to its original position after the effect resolves. | 2 | `1` |
| `FlowersOnHit` | `Number` | The number of flowers spawned on the tile upon hitting the target. | 2 | `1` |
| `ForceMoveNonAlliesInRangeTowardsTile` | `Number` | The tile range within which non-allied units are forcibly moved towards a specified tile. | 2 | `3`<br>`4` |
| [`ForceMoveTowardsTaggedObject`](./Abilities_and_Spells.md#object-forcemovetowardstaggedobject) | Object  | An object specifying the `ability` and optional `tag` used to forcibly move the unit towards a tagged object. | 2 | `{ . . . }` |
| `ImmediateUseDirectionalAbility` | `String` | Specifies the name of a directional ability to be used immediately by the unit. | 2 | `BowlDash`<br>`BowlDash2` |
| `JohnnyCriesForWashers` | `Number` | The number of washers (currency) requested by the Johnny NPC. | 2 | `1`<br>`2` |
| `MaxHPUp` | `Number` | The amount of maximum health permanently increased. | 2 | `100` |
| `NextAttackSpecialCrit` | `Number` | The number of charges for a special crit on the next attack, or an object defining its bonus properties. | 2 | `1` |
| [`OverHealToStatuses`](./Abilities_and_Spells.md#object-overhealtostatuses) | Object  | Specifies a set of statuses applied to the target based on the amount of over-healing dealt. | 2 | `{ . . . }` |
| `PermanentUpgradeRandomActive` | `Number` | The number of random active abilities permanently upgraded. | 2 | `1`<br>`4` |
| [`QuakeAreaChance`](./Abilities_and_Spells.md#object-quakeareachance) | Object  | An object containing a radius and a chance to trigger a quake area effect. | 2 | `{ . . . }` |
| [`RandomKnockback`](./Abilities_and_Spells.md#object-randomknockback) | Object  | An object defining the minimum and maximum distance in tiles for a random knockback. | 2 | `{ . . . }` |
| `RebukeDamage` | `Number` | The amount of damage dealt by a rebuke backlash effect. | 2 | `1`<br>`2` |
| `RepairArmorCondition` | `Number` | The amount of armor condition restored. | 2 | `1` |
| `ResetArmorShield` | `Number` | The amount of armor shield restored. | 2 | `1` |
| `ScrambleEverything` | `Number` | The percentage chance to scramble all abilities and passives on the target. | 2 | `0`<br>`10%` |
| `SignalFinalBossShieldBroke` | `Number` | If set to a non-zero number, signals that the final boss's shield has been broken. | 2 | `1` |
| `SwallowSmallCharacter` | `Number` | The percentage chance to swallow a smaller character on hit. | 2 | `100%`<br>`50%` |
| `TriggerDOTStatuses` | `Number` | If set to 1, triggers damage over time statuses on the target immediately. | 2 | `0`<br>`1` |
| `SelfStun` | `Number` | The number of stacks of self-stun applied, with an optional probability as a second element. | 2 | `1`<br>`[1 .5]` |
| [`SpawnFlames`](../Reference_and_Meta/Arrays.md#array-spawnflames) | Array  | An array containing the number of flame tiles to spawn and the chance per tile. | 2 | `[1, .20+.1*level]`<br>`[1, .20]` |
| [`ForceUseAbility`](../Reference_and_Meta/Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `Infested` | Integer | The number of stacks of Infested applied. | 1 | `1` |
| [`SpreadDisease`](./Abilities_and_Spells.md#object-spreaddisease) | Object  | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 1 | `{ . . . }` |
| [`GainCoinsRange`](./Abilities_and_Spells.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 1 | `{ . . . }` |
| `RandomPermanentStat` | Integer | The amount of a random permanent stat change (positive or negative). | 1 | `-1`<br>`-2`<br>`-3` |
| `NonStackingDivineShield` | Integer | The number of Divine Shield stacks that do not stack with duplicates. | 1 | `1` |
| [`ChangeTilesUnder`](../Reference_and_Meta/Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. | 1 | `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| `CaptureFamiliar` | Integer | The number of times to attempt to capture the target as a familiar. | 1 | `1` |
| `IceArmor` | Integer | The number of Ice Armor stacks granting defensive properties. | 1 | `1` |
| `FactionConversion` | `Number` | Converts the target to the caster's faction. | 1 | `1` |
| `ChargeFists` | Integer | The number of charge stacks applied to unarmed attacks. | 1 | `1` |
| `EmptyMind` | Integer | The number of Empty Mind stacks, likely disabling special abilities. | 1 | `1` |
| `ExtraBasicMoves_Status` | Integer | The number of extra basic moves per turn granted. | 1 | `1` |
| `FireArmor` | Integer | The number of Fire Armor stacks providing damage reflection. | 1 | `1` |
| `PermanentIntelligence` | Integer | The permanent amount of intelligence added or removed. | 1 | `-1`<br>`1`<br>`2` |
| [`StatusGroup`](./Abilities_and_Spells.md#object-statusgroup) | Object  | A container grouping multiple status effects to be applied simultaneously. | 1 | `{ . . . }` |
| `SmellBlood` | `Number` | If non-zero, activates the Smell Blood ability which reveals nearby injured units. | 1 | `1` |
| [`CreateGlobalModifiers`](./Abilities_and_Spells.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. | 1 | `{ . . . }` |
| `PermanentDexterity` | Integer | The permanent amount of dexterity added or removed. | 1 | `1`<br>`2` |
| `PermanentSpeed` | Integer | The permanent amount of speed added or removed. | 1 | `-1`<br>`1`<br>`2` |
| `ReduceManaCost` | Integer | The number of stacks reducing mana cost of abilities. | 1 | `1`<br>`2` |
| `Regurge` | Integer | The number of regurgitation triggers. | 1 | `1` |
| `Switcheroo` | Integer | The number of stacks of the Switcheroo status effect. | 1 | `1` |
| `BombRatTurtle` | `Number` | The number of bomb rat turtle spawns triggered. | 1 | `1` |
| [`Conditional_RandomChance`](./Abilities_and_Spells.md#object-conditional_randomchance) | Object  | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 1 | `{ . . . }` |
| `DieViolently` | Integer | If true, causes the target to die with a violent, explosive visual effect. | 1 | `1` |
| [`RemoveStatusStacks`](./Abilities_and_Spells.md#object-removestatusstacks) | Object  | An object specifying a status name and the number of stacks to remove from the target. | 1 | `{ . . . }` |
| [`WaggleClone`](./Abilities_and_Spells.md#object-waggleclone) | Object  | Defines a waggle clone ability with health thresholds and object sizes. | 1 | `{ . . . }` |
| `Attraction` | Integer | The number of stacks of Attraction applied, drawing enemy units toward the target. | 1 | `1` |
| `FireArmor2` | Integer | The number of Fire Armor2 stacks (likely a variant). | 1 | `1` |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. | 1 | `1` |
| `TempCounterAttack` | Integer | The number of turns TempCounterAttack lasts, ticking down at the start of the unit's turn. | 1 | `1` |
| `Enlarge` | `Number` | The number of turns the unit is enlarged, increasing its size and stats. | 1 | `3` |
| `FlatAIBonus` | `Number` | A flat adjustment to the AI's evaluation score for this action; positive values encourage the AI to use it, negative values discourage it. | 1 | `-999999`<br>`100`<br>`999999` |
| [`GlobalSpawnCharacter`](../Reference_and_Meta/Enums.md#enum-globalspawncharacter) | Enum  | Specifies the name of a character to spawn globally. | 1 | `MegaGuppy` |
| [`NextBasicAttackCritsThisTurn`](./Abilities_and_Spells.md#object-nextbasicattackcritsthisturn) | Object  | An object or number configuring the next basic attack to be a critical hit this turn. An object may contain stack, cant_miss, or piercing sub-keys. | 1 | `{ . . . }` |
| `PermanentCharisma` | `Number` | The amount of permanent Charisma added to the unit's base stats. | 1 | `1`<br>`2` |
| `PermanentLuck` | `Number` | The amount of permanent Luck added to the unit's base stats. | 1 | `1`<br>`2` |
| `TriggerGameEnding` | `Number` | If set to 1, triggers the game's ending sequence; 0 disables it. | 1 | `0`<br>`1` |
| `DoubleCast` | Integer | The number of double-cast stacks, allowing a spell to be cast twice. | 1 | `1` |
| `DrinkWater` | Integer | The number of water-drink actions performed. | 1 | `1` |
| `Meaty` | Integer | The number of Meaty stacks increasing health or size. | 1 | `1` |
| `NextAbilityHeals` | Integer | The number of stacks causing the next ability to heal instead of damage. | 1 | `1` |
| `NextDamageReduceAndHealAllies` | Integer | The number of stacks reducing next damage and healing nearby allies. | 1 | `1` |
| `PermanentImmobile` | Integer | The permanent amount of immobility stacks applied. | 1 | `1` |
| `ProbeCharmed` | Integer | The number of charm stacks applied by a probe. | 1 | `1` |
| [`SetDefaultFace`](../Reference_and_Meta/Enums.md#enum-setdefaultface) | Enum  | Specifies the default facial expression, such as 'happy', 'sad', or 'insane'. | 1 | `happy`<br>`insane`<br>`sad` |
| `SpellShield` | Integer | The number of stacks of SpellShield, which blocks incoming spells. | 1 | `1` |
| `Taunting` | Integer | The number of stacks of Taunting, which forces enemies to target the unit. | 1 | `1` |
| `TilesMovedToCritChance` | Integer | The number of stacks of a status that grants critical hit chance based on tiles moved. | 1 | `1` |
| `TilesMovedToMana` | Integer | The number of stacks of a status that grants mana based on tiles moved. | 1 | `1` |
| [`TilesMovedToNeighborHeal`](../Reference_and_Meta/Enums.md#enum-tilesmovedtoneighborheal) | Enum  | Specifies the scaling type for healing neighbors based on tiles moved (e.g., 'level'). | 1 | `level` |
| `TilesMovedToStrength` | Integer | The number of stacks of a status that grants strength based on tiles moved. | 1 | `1` |
| [`Conditional_Displaceable`](./Abilities_and_Spells.md#object-conditional_displaceable) | Object  | Contains an inner effect block that only executes if the target can be displaced (knocked back). | 1 | `{ . . . }` |
| [`Conditional_HasCleansableDebuffs`](./Abilities_and_Spells.md#object-conditional_hascleansabledebuffs) | Object  | An object containing effects that execute only if the unit has cleansable debuffs. | 1 | `{ . . . }` |
| [`DelayCastAbility`](./Abilities_and_Spells.md#object-delaycastability) | Enum / Object  | Specifies the name of an ability to cast after a delay. | 1 | `{ . . . }`<br>`HitlerNuke` |
| [`DelayedWindCone`](./Abilities_and_Spells.md#object-delayedwindcone) | Object  | An object containing parameters for a delayed wind cone, such as damage and distance. | 1 | `{ . . . }` |
| `Disguised` | `Number` | If true, the unit is disguised, appearing as a different faction or model. | 1 | `1` |
| `DoubleCastSpellsEachTurn_Status` | `Number` | The number of turns the unit gains Double Cast for spells each turn. | 1 | `1` |
| `EnterMount` | `String` | Specifies the name of the mount status to apply to the unit. | 1 | `enter` |
| `ExistUntilIdleUpkeep` | `Number` | If true, the entity persists until the source unit enters idle upkeep. | 1 | `1` |
| `ExplodeCharacter` | `Number` | The radius (in tiles) of an explosion centered on the character. | 1 | `5` |
| `ExplodeCharacter_NoDie` | `Number` | The damage dealt when a character explodes without dying. | 1 | `1`<br>`5` |
| `GenericBuff` | `Number` | A generic buff value applied to the unit. | 1 | `100`<br>`5` |
| `MadnessChanceOnTurnBegin` | Integer | The chance (as a multiplier) to inflict Madness status at the start of each turn in the next battle. | 1 | `2` |
| `OverrideChainKnockbackDamage` | `String` | A formula string that overrides the damage dealt by chain knockback (e.g., "3+bonus_melee_ability_damage"). | 1 | `0`<br>`3+bonus_melee_ability_damage` |
| `ScatterRandomPickups` | `Number` | The number of random pickups scattered around the target's location. | 1 | `2`<br>`5` |
| `SplashDamage` | `Number` | The radius (in tiles) for splash damage applied to adjacent targets. | 1 | `1`<br>`2` |
| `StackingSandstorm` | `Number` | If non-zero, enables the stacking sandstorm mechanic which increases damage per stack. | 1 | `1` |
| `SwapHighestAndLowestStat` | `Number` | If non-zero, swaps the unit's highest base stat value with its lowest. | 1 | `1` |
| `TempLuckUp` | `Number` | The amount of temporary luck increase. | 1 | `2`<br>`99` |
| `ThornsDamageImmuneUntilSettled` | `Number` | The number of turns the target is immune to thorns damage until it settles. | 1 | `1` |
| `TileDamageImmuneUntilSettled` | `Number` | The number of turns the target is immune to tile damage until it settles. | 1 | `1` |
| [`TransformEquipment`](./Abilities_and_Spells.md#object-transformequipment) | Object  | Defines an equipment transformation from one item to another, with 'from' and 'to' sub-keys. | 1 | `{ . . . }` |
| `Bloodzerked` | Integer | The number of Bloodzerk stacks applied. | 1 | `1` |
| `ChampionUpgradeNextMinion` | Integer | The number of champion upgrades applied to the next spawned minion. | 1 | `1` |
| `EliteUpgradeNextMinion` | Integer | The number of elite upgrades applied to the next spawned minion. | 1 | `1` |
| `HeavyHits` | Integer | The number of Heavy Hits stacks increasing attack impact. | 1 | `1` |
| `Invulnerable` | Integer | The number of Invulnerable stacks, making the unit immune to damage. | 1 | `1` |
| `Muted` | Integer | The number of Muted stacks, disabling certain abilities. | 1 | `1` |
| `NextActionLuckUp` | Integer | The number of stacks increasing luck for the next action. | 1 | `99` |
| `NextTurnDoubleRangedDamage` | Integer | The number of stacks doubling ranged damage on the next turn. | 1 | `1` |
| `ReduceManaCostExcludeBrainstorm` | Integer | The number of stacks reducing mana cost, excluding Brainstorm. | 1 | `1` |
| `StatBounty` | Integer | The number of stacks of the StatBounty status effect. | 1 | `1` |
| `TempBackstab` | Integer | The amount of temporary backstab bonus, typically as a percentage. | 1 | `75` |
| `TempBonusKnockback` | Integer | The number of stacks of temporary bonus knockback distance. | 1 | `1` |
| `TempBonusKnockbackDamage` | Integer | The number of stacks of temporary bonus knockback damage. | 1 | `1` |
| `TempInjuryImmunity` | Integer | The number of stacks of temporary immunity to Injuries. | 1 | `1` |
| `TempManaCostReduction` | Integer | The number of stacks of temporary mana cost reduction. | 1 | `1` |
| `TempPreEmptiveCounterAttack` | Integer | The number of turns of temporary pre-emptive counterattack status. | 1 | `1` |
| `TowerDefenseStatus` | Integer | The number of stacks of the sentry/tower defense status, granting stationary attack capabilities. | 1 | `1` |
| `TowerDefenseStatus2` | Integer | The number of stacks of the enhanced sentry/tower defense status. | 1 | `1` |
| `AIFavorLowHealth` | `Number` | The AI's favorability weight for targeting low-health units. | 1 | `100` |
| `AlliesTakeExtraTurn` | `Number` | The number of extra turns granted to allies. | 1 | `1` |
| `AlternateIdleAnimation` | `String` | Specifies the name of an alternative idle animation to play. | 1 | `berserkIdle` |
| `ApplyShieldToApplierBasedOnMaxHealth` | `Number` | The amount of shield applied to the applier based on a fraction of their max health. | 1 | `1` |
| [`ApplyStatusesNextTurnBegin`](./Abilities_and_Spells.md#object-applystatusesnextturnbegin) | Object  | Specifies a set of statuses to apply to the target at the beginning of their next turn. | 1 | `{ . . . }` |
| [`ApplyToOthersWithSharedTagAndFaction`](./Abilities_and_Spells.md#object-applytootherswithsharedtagandfaction) | Object  | Specifies statuses to apply to other units that share a tag and faction with the target. | 1 | `{ . . . }` |
| [`ApplyToRandomClosestAlly`](./Abilities_and_Spells.md#object-applytorandomclosestally) | Object  | Specifies statuses to apply to a random ally closest to the target. | 1 | `{ . . . }` |
| `BonusDamageBasedOnMana` | `Number` | The amount of bonus damage dealt, scaled by the target's current mana. | 1 | `1` |
| `BypassRockKnockback` | `Number` | If set to a non-zero number, bypasses normal rock knockback behavior. | 1 | `1` |
| `CanceledQueuedInput` | `Number` | If set to a non-zero number, cancels any queued input from the target. | 1 | `1` |
| `ChaosBossFlipMidTeleport` | `Number` | If set to a non-zero number, causes the chaos boss to flip direction mid-teleport. | 1 | `1` |
| `ChaosBossFormChange` | `Number` | If set to a non-zero number, triggers a chaos boss form change. | 1 | `1` |
| `CharmedFacingForceAttack` | `Number` | If set to a non-zero number, the charmed target is forced to attack the direction they are facing. | 1 | `1` |
| `ClearFinalBossBattlefield` | `Number` | If set to a non-zero number, clears the battlefield during the final boss fight. | 1 | `1` |
| `CloneWeaponTemp` | `Number` | The number of turns the cloned weapon persists before being removed. | 1 | `1` |
| `CoinTossBounce` | `String` | Specifies the ability triggered when the coin lands on its edge after a bounce. | 1 | `X` |
| `Conditional_AbilityTargetIsSelf` | Object | An object containing effects that execute only if the ability's target is the source unit. | 1 | `{ . . . }` |
| [`Conditional_ActiveWeather_Any`](./Abilities_and_Spells.md#object-conditional_activeweather_any) | Object  | An object containing effects that execute only if any of the specified weather types are active. | 1 | `{ . . . }` |
| [`Conditional_Backstab`](./Abilities_and_Spells.md#object-conditional_backstab) | Object  | An object containing effects that execute only if the attack lands on the target's back. | 1 | `{ . . . }` |
| [`Conditional_CanBeHealed`](./Abilities_and_Spells.md#object-conditional_canbehealed) | Object  | An object containing effects that execute only if the target can be healed. | 1 | `{ . . . }` |
| [`Conditional_DebuffRoll`](./Abilities_and_Spells.md#object-conditional_debuffroll) | Object  | An object containing effects that execute if a debuff roll succeeds, with an odds value defined inside. | 1 | `{ . . . }` |
| [`Conditional_IsTrample`](./Abilities_and_Spells.md#object-conditional_istrample) | Object  | An object containing effects that execute only if the ability is a trample attack. | 1 | `{ . . . }` |
| [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#object-conditional_livingplayercat) | Object  | An object containing effects that execute only if the source is a living player-owned cat. | 1 | `{ . . . }` |
| [`Conditional_NotBig`](./Abilities_and_Spells.md#object-conditional_notbig) | Object  | An object containing effects that execute only if the target is not a 'big' unit. | 1 | `{ . . . }` |
| [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#object-conditional_sourceabilityhastag) | Object  | An object containing effects that execute only if the source ability has the specified tag. | 1 | `{ . . . }` |
| [`Conditional_SourceHasStatus`](./Abilities_and_Spells.md#object-conditional_sourcehasstatus) | Object  | An object containing effects that execute only if the source unit has the specified status. | 1 | `{ . . . }` |
| `ConjureSingleUseBonusAbility` | `String` | Specifies the bonus ability to conjure for single use (e.g., 'random' for a random one). | 1 | `random` |
| `CurrentWeaponAddElectricElement` | `Number` | The number of turns the current weapon gains the electric element. | 1 | `1` |
| `DamageWeapon` | `Number` | The amount of durability damage dealt to the equipped weapon. | 1 | `1` |
| `DeathwormUnderground` | `String` | Specifies the ability triggered when the Deathworm emerges from underground. | 1 | `DeathWormEat` |
| `DecoySwapper` | `Number` | If true, the decoy swaps places with the source when spawned. | 1 | `1` |
| `DeleteTraps` | `Number` | If true, removes all traps from the map. | 1 | `1` |
| `DestroyNeckArmor` | `Number` | If true, destroys the target's neck armor slot. | 1 | `1` |
| `DinoLegAnimation` | `String` | Specifies the animation trigger for the dinosaur leg (e.g., 'poop' for the poop animation). | 1 | `poop` |
| `DissolveRandomArmorPiece` | `Number` | If true, destroys a random armor piece (head, body, neck) on the target. | 1 | `1` |
| `DontHealEnemies` | `Number` | If true, the healing effect does not affect enemy units. | 1 | `1` |
| `DrainAllyCatsForFleshGolem` | `Number` | The amount of health drained from ally cats to heal the Flesh Golem. | 1 | `7` |
| `DuplicateRandomEquippedItem` | `Number` | If true, creates a copy of a random equipped item. | 1 | `1` |
| `ExplodeCharacter_DeathBloom` | `Number` | The amount of damage dealt by the DeathBloom explosion. | 1 | `5` |
| `ExplodeCharacter_DeathBloom2` | `Number` | The amount of damage dealt by the DeathBloom2 explosion. | 1 | `5` |
| `FactionDisguiseSource` | `Number` | If true, the unit adopts the faction of the source unit for disguise. | 1 | `1` |
| `FastKnockback` | `Number` | The number of tiles the target is knocked back with fast animation. | 1 | `4` |
| `FinalBossQueueBeam` | `Number` | If true, queues the final boss beam attack. | 1 | `1` |
| `ForceCollectsPickups` | `Number` | If true, the unit automatically collects nearby pickups. | 1 | `1` |
| `ForceMoveAndAttack` | `Number` | If true, forces the target to move and attack its nearest enemy. | 1 | `1` |
| `ForceTransferWeapon` | `Number` | If true, forces the weapon to be transferred to the target. | 1 | `1` |
| `GiveBoundItemToTarget` | `Number` | If true, gives the source's bound item to the target. | 1 | `1` |
| `HealPercentMaxHP` | `Number` | The percentage of max HP healed (e.g., 100 for full heal). | 1 | `100` |
| `HealTo` | `Number` | The target HP percentage to heal the unit to (e.g., '50%' for half max HP). | 1 | `50%` |
| `IgnoreDebuffs` | `Number` | If true, the effect ignores debuffs on the target. | 1 | `1` |
| [`IncAuxCounterCycle`](./Abilities_and_Spells.md#object-incauxcountercycle) | Object  | An object containing parameters for incrementing an auxiliary counter with a change and maximum value. | 1 | `{ . . . }` |
| `IncreaseCumulativeBlastDamage` | `Number` | If true, increases the cumulative blast damage counter. | 1 | `1` |
| `IncreaseItemAuxOnKill` | `Number` | If true, increases the item's aux counter on kill. | 1 | `1` |
| `InterchangeMoveActPoints` | `Number` | If true, swaps the unit's remaining move points and action points. | 1 | `1` |
| `MakeWeaponUnbreakable` | `Number` | If true, makes the equipped weapon unbreakable. | 1 | `1` |
| `ManaStealToHealth` | `Number` | The amount of mana stolen and converted to health (negative values may drain health). | 1 | `-1` |
| `ManglerAttack` | `Number` | If true, the attack triggers the Mangler's attack pattern. | 1 | `1` |
| `ManglerShuffle` | `Boolean` | If true, the order of effects in this damage instance is randomized before application. | 1 | `false` |
| `MassAttackThis` | `Number` | The number of additional targets this attack hits via the Mass Attack mechanic. | 1 | `1` |
| `MimicMetronome` | `Number` | The number of random abilities the Metronome effect selects from this unit's ability pool. | 1 | `1` |
| `MotherTumorDebugForcePass` | `Number` | If non-zero, forces the Mother Tumor boss to pass its turn, skipping its normal action. | 1 | `1` |
| [`NextBattleStatusStacks`](./Abilities_and_Spells.md#object-nextbattlestatusstacks) | Object  | An object specifying status effects and their stacks to be applied at the start of the next battle. Contains a "fights" counter and nested status keys. | 1 | `{ . . . }` |
| `ObjectOnHitFullyEmpty` | `String` | Specifies the object (e.g., RandomArmorPickup) to spawn on the target when the attacker's inventory is completely empty. | 1 | `RandomArmorPickup` |
| `OverHealToShield` | `Number` | The amount of excess healing converted into temporary shield points. | 1 | `1` |
| `PermanentUpgradeRandomActiveOrPassive` | `Number` | The number of random active or passive abilities permanently upgraded. | 1 | `1` |
| [`PoolMetronome`](./Abilities_and_Spells.md#object-poolmetronome) | Object  | An object containing a "pool" array of ability names that the Metronome effect can randomly select from. | 1 | `{ . . . }` |
| `QueueUseAbility` | `String` | Specifies the ability ID to be used immediately after the current action resolves. | 1 | `Spider_GoInsane` |
| `RandomKnockbackDirection` | `Number` | The number of random directions the target can be knocked back (e.g., 4 selects from 4 cardinal directions). | 1 | `4` |
| `ReformMoonHead` | `Number` | If non-zero, triggers the Moon Head's reformation mechanic (e.g., after it eats a cat). | 1 | `1` |
| `RefreshItemAbilities` | `Number` | The number of times all item abilities are recharged (cooldowns reset). | 1 | `1` |
| `RefreshNonManaItemAbilities` | `Number` | The number of times non-mana item abilities are recharged. | 1 | `1` |
| `RefreshOncePerFightAbilities` | `Number` | The number of times abilities limited to once per fight are refreshed. | 1 | `1` |
| `RepairAllCondition` | `Number` | If non-zero, fully repairs the condition of all equipped items. | 1 | `1` |
| `RerollEnemy` | `Number` | The number of times the target enemy is re-rolled (transformed into a new random enemy). | 1 | `1` |
| `ReturnDinoLegs` | `Number` | If non-zero, returns the Dino Legs ability to the unit after it is consumed. | 1 | `1` |
| `RNGCannonRandomDamage` | `Number` | The maximum random damage value for the RNG Cannon attack. | 1 | `100` |
| [`ScrambleLastUsedSpell`](./Abilities_and_Spells.md#object-scramblelastusedspell) | Object  | An object containing a "permanent" boolean. If true, permanently scrambles (randomizes) the last used spell. | 1 | `{ . . . }` |
| `ShadowCrit` | `Number` | If non-zero, enables the Shadow Crit mechanic, granting bonus critical hit chance or damage from stealth. | 1 | `1` |
| `ShootHereCommand` | `Number` | If non-zero, commands an allied unit to shoot at this unit's target. | 1 | `1` |
| `ShootHereReceiver` | `Number` | If non-zero, marks this unit as the receiver of a Shoot Here command. | 1 | `1` |
| `SmallHitExplosion` | `Number` | The number of small explosion VFX to spawn on hit. | 1 | `1` |
| `SoundEventOnHit` | `String` | Specifies the sound event ID to play on hit (e.g., "Batterup_Connect"). | 1 | `Batterup_Connect` |
| `SourceSwapsBackEndOfTurn` | `String` | Specifies the ability ID to use to swap the source unit back at the end of the turn. | 1 | `ThiefSwapBack` |
| `SpawnWebTrap` | `Number` | The number of web traps to spawn on the target tile. | 1 | `1` |
| `SpecialBossMultipartInstakill` | `String` | Specifies the boss ID (e.g., "moonboss") whose multipart instakill mechanic is triggered. | 1 | `moonboss` |
| `SpitConsumed` | `Number` | If non-zero, marks the object consumed by the Spit ability as having been used. | 1 | `1` |
| `StealDemonicGlyph` | `Number` | The number of Demonic Glyphs stolen from the target. | 1 | `1` |
| `StealEquipment` | `String` | Specifies the type of equipment to steal (e.g., "any") from the target. | 1 | `any` |
| `StealthCritChance` | `Number` | The percentage chance to critically hit while stealthed. | 1 | `100` |
| `StealTurn` | `Number` | The number of turns stolen from the target to grant to the attacker. | 1 | `1` |
| [`SwapWeapon`](./Abilities_and_Spells.md#object-swapweapon) | Object  | An object containing a "pool" array of weapon names to randomly swap to. | 1 | `{ . . . }` |
| `T3HitlerTriggerInitialSpawns` | `Number` | If non-zero, triggers the initial spawn sequence for the T3 Hitler boss. | 1 | `1` |
| `TagMetronome` | `String` | Specifies a tag (e.g., "musical") used to filter which abilities the Metronome effect can pick. | 1 | `musical` |
| `TakeExtraTurnEndOfRound` | `Number` | The number of extra turns taken at the end of the round. | 1 | `1` |
| `TargetedMetronome` | `Number` | The number of random targets hit by the Targeted Metronome effect. | 1 | `20` |
| `TeamBonusAbility` | `String` | Specifies the ability ID granted to allies as a team bonus. | 1 | `ShootHere` |
| `TeleportBackAtTurnEnd` | `String` | Specifies the ability ID used to teleport the unit back to its starting position at turn end. | 1 | `FlashBack` |
| `TempBackstabBleed` | `Number` | The number of temporary Bleed status stacks applied on a backstab attack. | 1 | `1` |
| `TempBackstabPiercing` | `Number` | The amount of temporary piercing added to backstab attacks. | 1 | `1` |
| `TempBackstabPoison` | `Number` | The amount of temporary poison stacks applied with backstab attacks. | 1 | `1` |
| `TempBasicAttackBonusAOE` | `Number` | The amount of temporary area-of-effect bonus on basic attacks. | 1 | `1` |
| `TempPenetrate` | `Number` | The amount of temporary penetration applied to attacks. | 1 | `1` |
| `TickDownStatus` | `String` | Specifies the name of the status effect whose duration is reduced by one tick. | 1 | `ShortCircuit` |
| `TransformBasicMove` | `String` | Specifies the name of the basic move to transform into. | 1 | `BasicDashAttackMove_NoKnockback` |
| `TransformNow` | `String` | Specifies the name of the form to immediately transform into. | 1 | `Hitler` |
| `Trapper_Status` | `Number` | The number of trap-related status stacks applied. | 1 | `1` |
| `TriggerMotherConsume` | `Number` | The number of times the Mother consume effect is triggered. | 1 | `1` |
| `TriggerMotherGrow` | `Number` | The number of times the Mother grow effect is triggered. | 1 | `4` |
| `TurnAround` | `Number` | The number of times the unit turns around. | 1 | `1` |
| `TurnControlDelay` | Float | Specifies the delay in seconds before the unit regains turn control. | 1 | `.25` |
| `TurnRight` | `Number` | The number of times the unit turns to the right. | 1 | `1` |
| `UndoDamage` | `Number` | The amount of damage reversed. | 1 | `1` |
| [`UseMoveAbilityWithAI`](./Abilities_and_Spells.md#object-usemoveabilitywithai) | Object  | Defines a move ability to execute with AI-controlled movement weights. | 1 | `{ . . . }` |
| `VaporizeDice` | `Number` | The number of dice vaporized. | 1 | `1` |
| [`VisualCountDownThenApplyStatus`](./Abilities_and_Spells.md#object-visualcountdownthenapplystatus) | Object  | Contains a visual countdown sequence that culminates in applying a status effect, optionally forcing an ability use. | 1 | `{ . . . }` |
| [`VaporizeCorpseFlipAdvantage`](../Reference_and_Meta/Arrays.md#array-vaporizecorpseflipadvantage) | Array  | The number of stacks and probability of vaporizing a corpse to gain loot flip advantage. | 1 | `[1 .33]` |
| [`LowerAmbientLight`](./Abilities_and_Spells.md#object-lowerambientlight) | Object  | If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly. | 0 | `{ . . . }` |

</details>


---


---


## Auto-Discovered Objects


### Object: `cost`


**Definition:** Defines the resource cost (e.g., mana) and other casting requirements.  
**Total Count:** 1903

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Equation | The amount of mana required to cast, as a formula or stat. | 1603 | `"4-clamp(floor(X/7), 0, 1)"`<br>`"max(4-X, 0)"`<br>`"max(7-2*X,0)"` |
| `infcantrip` | Boolean | If true, the ability is an infinite cantrip (costs no mana and can be cast repeatedly). | 810 | `false`<br>`true` |
| `cantrip` | Boolean | If true, the ability is a cantrip (costs no mana). | 560 | `false`<br>`true` |
| `once_per_fight` | Boolean / Equation | The number of times the ability can be used per fight, or true/false for single use. | 98 | `3-X`<br>`false`<br>`true` |
| `act_points` | Integer | The number of action points required to use the ability. | 86 | `0`<br>`1`<br>`2` |
| `move_points` | Integer | The number of move points required to use the ability. | 59 | `0`<br>`1`<br>`2` |
| `prime` | Integer | The number of prime points required to use the ability. | 30 | `1` |
| `allow_offmap_casts` | Boolean | If true, the ability can be cast from off-map locations. | 22 | `true` |
| `cant_cast` | Equation | The condition or counter that prevents the ability from being cast. | 18 | `1-X`<br>`2-X`<br>`3-X` |
| `must_be_consuming` | Boolean | If true, the ability can only be used while the unit is consuming. | 17 | `true` |
| `charge` | Equation | The amount of charge required or the formula to calculate charge cost. | 16 | `"1-clamp(spd,0,1)"`<br>`0`<br>`1` |
| `must_not_be_consuming` | Boolean | If true, the ability can only be used while the unit is not consuming. | 14 | `true` |
| `requires_reload` | Boolean | If true, the ability must be reloaded before it can be used again. | 14 | `true` |
| `can_cast_while_dead` | Boolean | If true, the ability can be cast while the unit is dead. | 12 | `true` |
| [`cantrip_group`](../Reference_and_Meta/Enums.md#enum-cantrip_group) | Enum | Specifies the cantrip group this ability belongs to, used for grouping related cantrip abilities. | 12 | `THC_CoinRoll`<br>`cavemomtoss`<br>`kaiju_roar` |
| `must_be_offmap` | Boolean | If true, the unit must be off the map (not on the battlefield) to use this ability. | 12 | `true` |
| `X_cant_be_zero` | Boolean | If true, the variable X used in cost calculation cannot be zero. | 11 | `true` |
| `disallow_cost_modification` | Boolean | If true, prevents any modifications to the cost of this ability. | 9 | `true` |
| `durability` | Integer | The amount of durability consumed by this ability or required for its use. | 8 | `0`<br>`1`<br>`10` |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 8 | `1`<br>`2`<br>`25` |
| `main_turn_only` | Boolean | If true, the ability can only be used during the unit's main turn. | 8 | `true` |
| `requires_destructible_weapon` | Boolean | If true, the ability requires a weapon that has durability and can be destroyed. | 8 | `true` |
| `requires_exact_character_aux` | Integer | The exact character auxiliary value required for the unit to use this ability. | 8 | `0`<br>`1`<br>`2` |
| `must_not_be_a_summon` | Boolean | If true, the unit must not be a summon to use this ability. | 7 | `true` |
| `start_reloaded` | Boolean | If true, the ability begins the battle already reloaded and ready to use. | 7 | `true` |
| `must_be_first_action` | Boolean | If true, this ability must be the first action taken by the unit in its turn. | 4 | `false`<br>`true` |
| `enabled_formula` | Equation | A formula using variables (e.g., X) that evaluates to a boolean indicating if the ability is enabled. | 3 | `1`<br>`1-X`<br>`X` |
| `must_be_first_nonmove_action` | Boolean | If true, this ability must be the first non-move action taken by the unit in its turn. | 3 | `true` |
| `must_have_weapon` | Boolean | If true, the unit must be wielding a weapon to use this ability. | 2 | `true` |
| `can_be_refreshed` | Boolean | If true, the ability's charges can be refreshed by other effects. | 1 | `false` |
| `can_pay_over_multiple_turns` | Boolean | If true, the cost of this ability can be paid over multiple turns. | 1 | `true` |
| `can_self_refresh` | Boolean | If true, this ability can refresh its own charges. | 1 | `false` |
| `damage_cant_be_zero` | Boolean | If true, the damage dealt by this ability cannot be zero. | 1 | `true` |
| `initial_charge` | Integer | The starting number of charges for this ability at the beginning of battle. | 1 | `1` |
| `manacost_cant_be_zero` | Boolean | If true, the mana cost of this ability cannot be zero. | 1 | `true` |
| `minimum_con` | Integer | The minimum Constitution (CON) stat required to use this ability. | 1 | `1` |
| `minimum_spd` | Integer | The minimum Speed (SPD) stat required to use this ability. | 1 | `1` |
| `require_default_size` | Boolean | If true, the unit must be of default size to use this ability. | 1 | `true` |
| `requires_attack_damage_threshold` | Integer | The minimum attack damage threshold the unit must have to use this ability. | 1 | `2` |
| `requires_consumed_trinket` | Boolean | If true, the unit must have a trinket that has been consumed to use this ability. | 1 | `true` |
| `requires_empty_trinket` | Boolean | If true, the unit must have an empty trinket slot to use this ability. | 1 | `true` |
| `requires_hp_threshold` | Integer | The minimum HP threshold (current HP) required to use this ability. | 1 | `200` |
| `requires_weapon` | Boolean | If true, the unit must have a weapon equipped to use this ability. | 1 | `true` |

</details>


---


### Object: `target`


**Definition:** Defines targeting parameters like range, AoE, restrictions, and multihit behavior.  
**Total Count:** 1862

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`max_range`](../Reference_and_Meta/Enums.md#enum-max_range) | Equation   | The maximum range of the ability, can be a static number or an expression. | 1088 | `"4+(1-clamp(spd,0,1))*2"`<br>`"max(5-int, 1)"`<br>`-1` |
| [`max_aoe`](../Reference_and_Meta/Enums.md#enum-max_aoe) | Equation   | An equation or integer defining the maximum radius or number of tiles for the area of effect target selection. | 795 | `"(X+1)/2"`<br>`"X/2"`<br>`-1` |
| `min_range` | Integer | The minimum range of the ability. | 583 | `0`<br>`1`<br>`2` |
| [`target_mode`](../Reference_and_Meta/Enums.md#enum-target_mode) | Enum | Determines how the targeting input is handled (e.g., direction8, tile, random_direction) for selecting a target location. | 503 | `direction`<br>`direction8`<br>`none` |
| [`restrictions`](../Reference_and_Meta/Arrays.md#array-restrictions) | Array / Enum | An array of constraint tags (e.g., [aoe_must_exist must_have_enemy]) that filter valid targets for the ability. | 463 | `[]`<br>`[aoe_must_be_displaceable aoe_must_exist]`<br>`[aoe_must_be_displaceable must_have_character]` |
| [`aoe_mode`](../Reference_and_Meta/Enums.md#enum-aoe_mode) | Enum | Specifies the shape or pattern of the area of effect (e.g., standard, cross, circle) for targeting multiple tiles. | 432 | `8cross`<br>`all`<br>`all_except_edges` |
| [`knockback_mode`](../Reference_and_Meta/Enums.md#enum-knockback_mode) | Enum / Integer | Determines the directional behavior of knockback (e.g., pull_to_character_plus1, zero, character_to_tile). | 265 | `0`<br>`back_orientation`<br>`character_to_target` |
| `min_aoe` | Integer | An equation or integer defining the minimum radius or number of tiles for the area of effect target selection. | 253 | `-1`<br>`-10`<br>`0` |
| `aoe_excludes_self` | Boolean | If true, the casting unit is excluded from being a target of its own area of effect. | 241 | `false`<br>`true` |
| [`aoe_restrictions`](../Reference_and_Meta/Arrays.md#array-aoe_restrictions) | Array / Enum | Specifies the list of restrictions for area-of-effect targets, such as allies only, enemies only, or requiring line of sight. | 197 | `[allies_only character_has_turns_left]`<br>`[allies_only]`<br>`[enemies_only must_have_living_character]` |
| `aoe_considers_character_size` | Boolean | If true, the area of effect accounts for the size of characters when determining which tiles are affected. | 170 | `false`<br>`true` |
| [`range_mode`](../Reference_and_Meta/Enums.md#enum-range_mode) | Enum | Determines the shape or logic used to calculate ability range, such as standard, ground_move, cross, custom, or special_tagged_tiles. | 114 | `8cross`<br>`cross`<br>`custom` |
| [`X_is`](../Reference_and_Meta/Enums.md#enum-x_is) | Enum | Defines what the ability's variable 'X' represents, such as custom, storm_count, random_0_to_N, alpha_exists, or current_shield. | 86 | `alpha_exists`<br>`basic_attack_damage`<br>`cast_count` |
| [`custom_aoe`](../Reference_and_Meta/Arrays.md#array-custom_aoe) | Array | A list of tile offsets relative to the target that defines the shape of a custom area of effect. | 83 | `[`<br>`[ [-1, -1] ]`<br>`[ [-1, 0] ]` |
| `multihit` | Integer | The number of times the ability hits each target, or an expression involving X. | 62 | `10`<br>`14`<br>`2` |
| `max_targets` | Equation | The maximum number of targets the ability can affect. | 56 | `-1`<br>`-X`<br>`1` |
| `range_excludes_blocking` | Boolean | If true, the range calculation ignores obstacles that block line of sight. | 53 | `false`<br>`true` |
| `prioritize_dont_change_direction` | Boolean / Integer | If true, the unit's facing direction is not changed when selecting a target. | 52 | `1`<br>`true` |
| [`target_requires_tag`](../Reference_and_Meta/Enums.md#enum-target_requires_tag) | Enum | Restricts targeting to characters that possess a specific tag. | 40 | `bishop_hat`<br>`bowling_ball`<br>`food` |
| [`aoe_symmetry`](../Reference_and_Meta/Enums.md#enum-aoe_symmetry) | Enum | Determines the symmetry applied to the custom area of effect shape, such as four_way, eight_way, or none. | 28 | `eight_way`<br>`four_way`<br>`none` |
| `prioritize_face_camera` | Boolean / Integer | If set, the unit's sprite faces the camera during targeting. | 26 | `1`<br>`true` |
| `straight_shot` | Boolean | If true, the ability fires in a straight line, hitting all units in its path. | 24 | `false`<br>`true` |
| `can_multihit` | Boolean | If true, the ability can hit the same target multiple times per cast. | 17 | `false`<br>`true` |
| `allow_any_orientation` | Boolean | If true, the ability can be used in any facing direction, not just cardinal. | 16 | `true` |
| `range_considers_character_size` | Boolean | If true, the range calculation includes the size of the character occupying the tile. | 16 | `false` |
| `throw_consumed_character` | Boolean | If true, the consumed character is thrown as a projectile toward the target. | 15 | `true` |
| `min_targets` | Integer | The minimum number of targets the ability must hit; if insufficient valid targets exist, the ability may fail. | 14 | `1`<br>`2`<br>`3` |
| `aoe_leading_edge_only` | Boolean | If true, only the outermost tiles of the area of effect are considered for targeting. | 13 | `true` |
| `allow_diagonals` | Boolean | If true, diagonal tiles are considered valid targets. | 12 | `true` |
| `range_display_include_character_size` | Boolean | If true, the displayed range indicator accounts for the character's size. | 12 | `true` |
| `stagger_multihit_targets` | Boolean | If true, multihit instances are distributed across different targets rather than hitting the same one repeatedly. | 12 | `true` |
| `upgrade_straight_shot_to_piercing` | Boolean | If true, the straight shot pierces through all enemies instead of stopping at the first. | 11 | `true` |
| `delayed_trigger` | Boolean | If true, the ability's effect is applied after a short delay rather than instantly. | 10 | `false`<br>`true` |
| `consider_trample` | Boolean | If true, the ability accounts for trample mechanics when moving through enemies. | 9 | `false`<br>`true` |
| `N` | Integer | A generic numeric parameter used in custom targeting logic. | 7 | `2`<br>`3`<br>`4` |
| [`custom_range`](../Reference_and_Meta/Arrays.md#array-custom_range) | Array | A list of tile offsets relative to the caster that defines the shape of a custom range indicator. | 7 | `[ [0 0] [-1 0] [-2 0] [-3 0] [-4 0] ]`<br>`[ [1, 1] [1, -1] [-1, 1] [-1, -1] ]`<br>`[[1 2]]` |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 7 | `damage_instance`<br>`spell`<br>`self_damage` |
| `always_bounce` | Boolean | If true, the projectile always bounces off the target and can hit additional targets. | 6 | `true` |
| `multihit_max` | Integer | The maximum number of hits per cast when multihit is variable. | 6 | `10`<br>`3`<br>`5` |
| `multihit_min` | Integer | The minimum number of hits per cast when multihit is variable. | 6 | `1`<br>`2`<br>`3` |
| `reorient_thrown_character` | Boolean | If true, the thrown character is reoriented to face the direction it is thrown. | 6 | `true` |
| [`toss_direction_restriction`](../Reference_and_Meta/Enums.md#enum-toss_direction_restriction) | Enum | Limits the direction a thrown character can be tossed to forwards or backwards. | 6 | `backwards`<br>`forwards` |
| [`custom_aoe_util`](../Reference_and_Meta/Arrays.md#array-custom_aoe_util) | Array | An additional list of tile offsets for utility targeting within the area of effect. | 6 | `[[0, 1] [1, 1]   [0,  0] [1,  0]]`<br>`[[1, 0] [1, 1]  [1, 0] [1, 1]  [1, 0] [1, 1]]`<br>`[[1, 1] [1,  0]]` |
| `max_bounces` | Integer | The maximum number of bounces for a projectile; -1 means infinite. | 5 | `-1`<br>`1`<br>`10` |
| `aoe_hint_teamcast` | Boolean | If true, the area of effect is displayed as a team-wide ability. | 5 | `true` |
| [`aoe_tile_requires_element`](../Reference_and_Meta/Enums.md#enum-aoe_tile_requires_element) | Enum | Restricts the area of effect to tiles with a specific terrain element type. | 5 | `Earth`<br>`Grass`<br>`Water` |
| `distance_sort_targets` | Boolean / Integer | If set, targets are sorted by distance from the caster for hit order. | 5 | `1`<br>`true` |
| `dont_orient_aoe` | Boolean | If true, the area of effect shape is not rotated to match the caster's facing. | 5 | `true` |
| `hint_can_target_pickups` | Boolean | If true, the ability can target pickups as valid targets. | 5 | `true` |
| `splash_damage_aoe_begin` | Integer | The hit number at which splash damage area of effect begins for multihit abilities. | 5 | `1`<br>`999` |
| `aoe_chance` | Equation | The probability (0 to 1) that the area of effect is applied per hit, or an expression using level. | 4 | `.33`<br>`.4+.2*level`<br>`.5` |
| `as_the_crow_flies` | Boolean | If true, movement ignores obstacles and uses straight-line distance. | 4 | `true` |
| `force_ai_target_as_spell` | Boolean | If true, the AI treats this ability as a spell for targeting decisions. | 4 | `true` |
| `range_display_include_aoe` | Boolean | If true, the range display also shows the area of effect. | 4 | `true` |
| `shotgun_mode` | Boolean | If true, the ability fires multiple projectiles in a spread pattern. | 4 | `true` |
| `shuffle_tile_order` | Boolean | If true, the order in which tiles are hit is randomized. | 4 | `true` |
| `upgrade_straight_shot_to_boomerang` | Boolean | If true, the straight shot becomes a boomerang that returns to the caster. | 4 | `true` |
| [`mouse_offset`](../Reference_and_Meta/Arrays.md#array-mouse_offset) | Array | A 2D offset [x, y] applied to the mouse cursor position for targeting. | 4 | `[.5 .5]` |
| `dont_orient` | Boolean | If true, the caster does not rotate to face the target. | 3 | `true` |
| `low_health_character_threshold` | Equation | The health threshold below which a character is considered low health for targeting. | 3 | `10`<br>`5`<br>`item_aux` |
| `randomize_target_within_range` | Integer | The number of times to randomize the target's position within the ability's range. | 3 | `0`<br>`2`<br>`3` |
| [`special_tile_tag`](../Reference_and_Meta/Enums.md#enum-special_tile_tag) | Enum | Specifies a special tile tag that the ability can target. | 3 | `ChaosValidPosition`<br>`FinalBossCloneSpot`<br>`FinalBossTheChildLocation` |
| `track_target` | Boolean | If true, the ability will track the target's movement. | 3 | `true` |
| `redirect_location_if_blocked` | Boolean | If true, the target location is redirected if the original is blocked. | 2 | `true` |
| `corpse_priority` | Integer | The priority value for targeting corpses. | 2 | `10`<br>`5` |
| `hint_can_target_empty` | Boolean | If true, the ability can target empty tiles. | 2 | `false`<br>`true` |
| `low_gravity_boostable` | Boolean | If true, the ability is affected by low gravity boosts. | 2 | `false`<br>`true` |
| `prioritize_change_direction` | Boolean | If true, the ability prioritizes changing the caster's direction to face the target. | 2 | `true` |
| [`range_bonuses`](../Reference_and_Meta/Enums.md#enum-range_bonuses) | Enum | Specifies the range bonus modifier to apply. | 2 | `include_alpha` |
| `range_display_include_direction` | Boolean | If true, the range display includes direction indicators. | 2 | `true` |
| `recalc_target_on_castpoint` | Boolean | If true, the target is recalculated at the cast point instead of at the start. | 2 | `true` |
| `trample_allies_too` | Boolean | If true, the ability can trample or pass through allies. | 2 | `true` |
| [`target_requires_element`](../Reference_and_Meta/Arrays.md#array-target_requires_element) | Array | Specifies the list of tile elements that the target must have. | 2 | `[grass water]`<br>`[grass]` |
| `aoe_spell_on_land` | Boolean | If true, triggers an area-of-effect spell upon the unit landing after a jump or movement. | 1 | `true` |
| `force_no_contact` | `Boolean` | If true, the damage instance does not trigger contact-based passives even if it would normally be a contact hit. | 1 | `true` |
| `lingering` | Boolean | If true, the ability effect lingers after the initial cast. | 1 | `true` |
| [`adjust_target`](../Reference_and_Meta/Enums.md#enum-adjust_target) | Enum | Specifies the type of target adjustment. | 1 | `stalk` |
| `allow_diagonal_passthrough` | Boolean | If true, the target can be diagonal and pass through diagonally. | 1 | `true` |
| `ally_priority` | Integer | The priority value for targeting allies. | 1 | `1` |
| `aoe_display_exclude_restrictions` | Boolean | If true, the AoE display ignores targeting restrictions. | 1 | `true` |
| `aoe_rotate_around_character_center` | Boolean | If true, the AoE area rotates around the character's center. | 1 | `true` |
| `bonus_pathing_leniency` | Integer | The amount of extra pathing leniency allowed. | 1 | `4` |
| `damage_collided_only` | Boolean | If true, damage is only applied to targets that the projectile collided with. | 1 | `true` |
| `enemy_priority` | Integer | The priority value for targeting enemies. | 1 | `10` |
| `hint_can_target_static` | Boolean | If true, the ability can target static objects. | 1 | `true` |
| [`knockback_modifier`](../Reference_and_Meta/Enums.md#enum-knockback_modifier) | Enum | Specifies the knockback direction modifier. | 1 | `rotate_cw` |
| `mirror_custom_aoe` | Boolean | If true, the custom AoE shape is mirrored. | 1 | `true` |
| [`prioritize_throw_target_with_passive`](../Reference_and_Meta/Enums.md#enum-prioritize_throw_target_with_passive) | Enum | Specifies the passive that the target must have to be prioritized. | 1 | `NubbyTossPriority` |
| `randomize_knockback_direction_except_for_finisher` | Boolean | If true, knockback direction is randomized except for the finisher hit. | 1 | `true` |
| `range_excludes_self` | Boolean | If true, the ability cannot target the caster. | 1 | `false` |
| `range_max` | Integer | The maximum range of the ability. | 1 | `4` |
| `range_min` | Integer | The minimum range of the ability. | 1 | `1` |
| [`range_symmetry`](../Reference_and_Meta/Enums.md#enum-range_symmetry) | Enum | Specifies the range symmetry type. | 1 | `eight_way` |
| `remain_off_map` | Boolean | If true, the target can be off the map. | 1 | `true` |
| [`restructions`](../Reference_and_Meta/Enums.md#enum-restructions) | Enum | Specifies additional targeting restrictions. | 1 | `aoe_must_exist` |
| `reverse_target_direction` | Boolean | If true, the target's facing direction is reversed. | 1 | `true` |
| `spin_steps` | Integer | The number of steps to spin the target. | 1 | `-16` |
| `uncounterable` | Boolean | If true, the ability cannot be countered. | 1 | `true` |
| [`custom_aoe_mirror`](../Reference_and_Meta/Arrays.md#array-custom_aoe_mirror) | Array | Lists the mirror transformations for the custom AoE shape. | 1 | `[[1  0] [1  0]  [1, 0] [1, 0]  [1, 0] [1, 0]]` |
| [`custom_aoe_util_mirror`](../Reference_and_Meta/Arrays.md#array-custom_aoe_util_mirror) | Array | Lists the utility mirror transformations for the custom AoE shape. | 1 | `[[1, 1] [1, 0]  [1, 1] [1, 0]  [1, 1] [1, 0]]` |

</details>


---


### Object: `damage`


**Definition:** Specifies the amount of damage dealt, can be a number or expression.  
**Total Count:** 1684

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Abilities_and_Spells.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `spawn`


**Definition:** Defines what object or unit is spawned when the ability is used.  
**Total Count:** 377

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 184 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 83 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`faction`](../Reference_and_Meta/Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 59 | `allies`<br>`auto`<br>`birds` |
| `ai_base_score` | Integer | The base priority score the AI assigns to using this damage instance, with higher values indicating greater preference. | 31 | `-99999`<br>`-999999`<br>`1` |
| [`additional_passives`](./Abilities_and_Spells.md#object-additional_passives) | Object  | Additional passive abilities applied to the spawned unit. | 20 | `{ . . . }` |
| [`first_turn`](../Reference_and_Meta/Enums.md#enum-first_turn) | Enum | Determines when the spawned unit takes its first turn relative to the spawn event. | 17 | `end_of_round`<br>`initiative`<br>`keep_turns` |
| `layer` | `String` | Specifies the layer on which the ability's effect operates (e.g., characters, tiles, gas). | 14 | `2`<br>`all`<br>`characters` |
| [`catdata`](../Reference_and_Meta/Enums.md#enum-catdata) | Enum  | Specifies the cat data identifier for the spawned unit, linking to a character template. | 13 | `Beaver`<br>`Bigfoot`<br>`Bunny` |
| `clone_items` | Boolean | If true, the spawned unit clones the items of the original unit. | 12 | `false`<br>`true` |
| `size` | Integer | The scale factor (size multiplier) of the spawned unit. | 4 | `.2`<br>`.5`<br>`1` |
| `lob` | Boolean | If true, the projectile follows a lobbed trajectory. | 4 | `false`<br>`true` |
| [`post_spawn_statuses`](./Abilities_and_Spells.md#object-post_spawn_statuses) | Object  | Status effects applied to the spawned unit immediately after it appears. | 4 | `{ . . . }` |
| `face_camera` | Boolean | If true, the spawned unit always faces the camera. | 2 | `1000`<br>`true` |
| `inherit_elite_buffs` | Boolean | If true, the spawned unit inherits elite buffs from the original unit. | 2 | `false` |
| `start_dead` | Boolean | If true, the spawned unit starts the battle dead (e.g., for revival effects). | 2 | `true` |
| `custom_additional_ai_weight` | `String` | A string identifier for a custom AI weighting condition that modifies the AI's scoring for this damage instance. | 1 | `avoid_redundant_debuffs`<br>`avoid_redundant_debuffs_strict`<br>`avoid_target_map_top` |
| [`chapter`](../Reference_and_Meta/Enums.md#enum-chapter) | Enum | Specifies which chapter or scenario this ability is available in. | 1 | `1`<br>`alley` |
| [`spawnin_animation`](../Reference_and_Meta/Enums.md#enum-spawnin_animation) | Enum | Specifies the animation played when the unit spawns in. | 1 | `"digUp"`<br>`"howl"`<br>`beamin` |
| `redirect_location_if_blocked` | Boolean | If true, the target location is redirected if the original is blocked. | 1 | `true` |
| [`appearance`](../Reference_and_Meta/Enums.md#enum-appearance) | Enum | Specifies the visual appearance or model override for the spawned unit. | 1 | `GolemCat` |
| [`auto_cast_on_spawn`](../Reference_and_Meta/Enums.md#enum-auto_cast_on_spawn) | Enum | Specifies an ability to automatically cast on the spawned unit when it spawns. | 1 | `Dash_Enemy` |
| `include_passives` | Boolean | If true, includes passives from the source unit when spawning. | 1 | `true` |
| `trigger_battle_start` | Boolean | If true, triggers the battle start event after spawning. | 1 | `true` |

</details>


---


### Object: `self_damage`


**Definition:** Defines damage or effects applied to the caster when using the ability.  
**Total Count:** 271

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#object-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 220 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 200 | `{ . . . }` |
| [`damage`](./Abilities_and_Spells.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 47 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `piercing` | `Boolean` | If true, the damage instance ignores armor or damage reduction effects on the target. | 12 | `true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 11 | `[attack move spell]`<br>`attack`<br>`battle` |
| `knockback` | Equation | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 10 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target regardless of accuracy or evasion. | 10 | `true` |
| `heal` | `Equation` | An equation string that determines the amount of health restored by this damage instance. | 6 | `"ceil(X*item_aux/100)"`<br>`0`<br>`1` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 4 | `[`<br>`[Heat Fire]` |
| `ai_base_score` | Integer | The base priority score the AI assigns to using this damage instance, with higher values indicating greater preference. | 2 | `-99999`<br>`-999999`<br>`1` |
| `non_lethal` | `Boolean` | If true, the damage instance cannot reduce a unit below 1 HP, preventing kills. | 1 | `true` |

</details>


---


### Object: `AddStatusToBasicAttack`


**Definition:** Contains status effects to add to the basic attack.  
**Total Count:** 248

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhileNotTakingTurn`](./Abilities_and_Spells.md#object-passivewhilenottakingturn), [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`Bruise`](../Reference_and_Meta/Arrays.md#array-bruise) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 1 | `1`<br>`2`<br>`3` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 45 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `FormChange`


**Definition:** Specifies the form the target transforms into, either as a string or an object with a `form` field.  
**Total Count:** 140

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form`](../Assets_and_Localization/Strings.md#string-form) | String | Specifies the name of the form the unit changes into. | 75 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `bonus_passives`


**Definition:** Grants temporary passive abilities to the caster for the duration of the ability.  
**Total Count:** 138

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 135 | passives<br>class<br>tag |
| [`DeadAltAbility`](../Reference_and_Meta/Enums.md#enum-deadaltability) | Enum  | Specifies an alternative ability used when the unit is dead. | 12 | `CarrionShot_Afterlife`<br>`CarrionShot_Afterlife2`<br>`CoffinFlop_Afterlife` |
| `AbilityEnabledOncePerFightAtHealthThreshold` | Integer | The health threshold (absolute or percentage) at which this ability becomes enabled once per fight. | 7 | `16`<br>`25%`<br>`50%` |
| `XIsFreeArmorSlots` | Integer | The number of armor slots that are free (no cost) for the unit. | 7 | `1` |
| `AbilityEnabledPercentEachTurn` | Integer | The percentage chance each turn that this ability is enabled. | 6 | `25%`<br>`33%`<br>`35%` |
| `FreeFirstCast` | Integer | The number of free casts of this ability per battle. | 6 | `1`<br>`4` |
| [`XIsLivingAlliesWithTag`](../Reference_and_Meta/Enums.md#enum-xislivingallieswithtag) | Enum  | Specifies the tag that living allies must have for this passive to affect them. | 5 | `dc_crow`<br>`hitler_clone_fetus`<br>`terminator_mini` |
| `CatchBoomerang` | Integer | If set, allows the ability to catch a boomerang, with the integer representing the number of catches. | 4 | `1` |
| `CopyBasicAttackEffects` | Integer | If set, the ability copies the effects from the unit's basic attack. | 4 | `1` |
| `DownRankAIIfWeaponUsable` | Float | A multiplier that reduces the AI's priority to use this ability if the unit has a usable weapon. | 4 | `.001` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid`
| [`AbilityEnableIfConsumedCharacterHasTag`](../Reference_and_Meta/Enums.md#enum-abilityenableifconsumedcharacterhastag) | Enum  | Specifies the tag that a consumed character must have for the ability to be enabled. | 3 | `sp_pill_fire`<br>`sp_pill_normal`<br>`sp_pill_tar` |
| `AbilityEnabledOncePerRound` | Integer | If set, the ability can only be used once per round. | 3 | `1` |
| `AbilityInheritsWeaponEffects` | Integer | If set, the ability inherits properties from the unit's weapon, with higher values indicating different inheritance modes. | 3 | `1`<br>`2` |
| `MoonHeadFinisherEnabler` | Integer | Determines the finisher state for MoonHead abilities; negative values may disable. | 3 | `-1`<br>`0`<br>`1` |
| [`XIsMultipliedPercentHealth`](../Reference_and_Meta/Arrays.md#array-xismultipliedpercenthealth) | Array  | The [stacks, probability] for multiplying health by a percentage. | 3 | `[1 12]`<br>`[14 1]`<br>`[6 2]` |
| [`AutocastEachRound`](./Abilities_and_Spells.md#object-autocasteachround) | Object  | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 2 | `{ . . . }` |
| [`AbilityEnabledIfHasStatus`](../Reference_and_Meta/Enums.md#enum-abilityenabledifhasstatus) | Enum  | Specifies the status effect that must be present on the unit for the ability to be enabled. | 2 | `DemonicGlyph_Bite`<br>`DemonicGlyph_Summon` |
| [`ChargeSpiritBombAura`](../Reference_and_Meta/Enums.md#enum-chargespiritbombaura) | Enum  | Specifies the ability to charge for spirit bomb aura. | 2 | `DonateEnergy`<br>`DonateEnergy2` |
| `CopyCatPassive_Initializer` | Integer | The number of copies of this passive to initialize. | 2 | `1`<br>`2` |
| [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#object-nukequestfinalbossmodifications) | Object  | Contains modifications for the nuke quest final boss, such as damage_instance effects. | 2 | `{ . . . }` |
| `ReloadOnKill` | Integer | If set, this ability's reload charge is restored on kill (any kill). | 2 | `1` |
| `ReloadOnKillEnemy` | Integer | If set, this ability's reload charge is restored only when killing an enemy. | 2 | `1` |
| `ReloadOnTotalDamageReceived` | Integer | The threshold of total damage received to restore a reload charge. | 2 | `15`<br>`25` |
| [`XIsLivingCharactersWithTag`](../Reference_and_Meta/Enums.md#enum-xislivingcharacterswithtag) | Enum  | Specifies the tag that living characters must have for this passive to affect them. | 2 | `husk`<br>`rock` |
| `XIsOtherHealsThisTurn` | Integer | If set, tracks other heals this turn for some effect. | 2 | `1` |
| [`XIsSpellStormRampAndReset`](./Abilities_and_Spells.md#object-xisspellstormrampandreset) | Integer / Object  | If integer 0, resets stacks; if object, contains 'stacks' and 'reset_percent' for spell storm ramp. | 2 | `{ . . . }`<br>`0` |
| `XIsTimesDamageTaken` | Integer | If set, multiplier for damage taken to apply some effect. | 2 | `1` |
| [`AddStatusToBasicAttack`](./Abilities_and_Spells.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 1 | `{ . . . }` |
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 1 | `1`<br>`3`<br>`4` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 1 | `1`<br>`10`<br>`100` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`RevengeDamage`](./Abilities_and_Spells.md#object-revengedamage) | Object  | An object defining the damage and effects that trigger when the unit is attacked. | 1 | `{ . . . }` |
| `IgnoreTiles` | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 1 | `1` |
| `KnockbackImmunity` | Integer | If set to 1, the unit cannot be knocked back. | 1 | `1` |
| [`StatusKillers`](./Abilities_and_Spells.md#object-statuskillers) | Object  | An object containing nested conditionals that apply status effects when the unit kills an enemy. | 1 | `{ . . . }` |
| `AlphaDodgeChance` | Integer | The dodge chance granted to the alpha (leader) unit. | 1 | `50%` |
| `CapTechSpent` | Integer | The maximum amount of tech that can be spent on this ability per turn. | 1 | `0`<br>`1` |
| `AbilityDisableIfLivingCrow` | Integer | If set, disables the ability if there is a living crow on the field. | 1 | `1` |
| `AbilityEnabledAtHealthThreshold` | Integer | The health percentage threshold at which the ability becomes enabled. | 1 | `50%` |
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Integer | If set, ability is enabled only if the unit used a basic attack this turn. | 1 | `1` |
| `AbilityEnabledIfMovementTrapped` | Integer | If set, ability is enabled only when the unit's movement is trapped. | 1 | `1` |
| `AbilityEnabledIfNoAggroTarget` | Integer | If set, ability is enabled only when the unit has no aggro target. | 1 | `1` |
| [`AbilityEnabledIfNotHasStatus`](../Reference_and_Meta/Enums.md#enum-abilityenabledifnothasstatus) | Enum  | Specifies the status that must be absent for ability to be enabled. | 1 | `BackflipWhenTargeted` |
| [`AbilityEnabledIfSpecificItemEquipped`](../Reference_and_Meta/Enums.md#enum-abilityenabledifspecificitemequipped) | Enum  | Specifies the item that must be equipped for ability to be enabled. | 1 | `Neverstone` |
| `AbsorbManaFromOtherSpells` | Integer | If set, this ability absorbs mana from other spells when cast. | 1 | `1` |
| [`AddElementsToSpells`](../Reference_and_Meta/Enums.md#enum-addelementstospells) | Enum  | Specifies which element to add to spells. | 1 | `Earth` |
| [`AlphaStatusOnTurnBegin`](./Abilities_and_Spells.md#object-alphastatusonturnbegin) | Object  | Specifies status effects applied to the alpha at the start of each turn. | 1 | `{ . . . }` |
| [`BonusAbility_DelayedApplication`](../Reference_and_Meta/Enums.md#enum-bonusability_delayedapplication) | Enum  | Specifies the name of a bonus ability to apply with a delay. | 1 | `Slap` |
| `CaveWomanBirthControl` | Integer | If true, restricts or controls the spawning of additional units via birth mechanics. | 1 | `1` |
| `FistOfFateUniqueEnemyTracker` | Integer | Increases the damage tracking counter for unique enemies hit by Fist of Fate. | 1 | `1` |
| `FreeFirstCastAndAfterSpendMana` | Integer | If set to 1, the first cast of the ability and each cast after spending mana costs no resources. | 1 | `1` |
| `FreeFirstCastEachMatch` | Integer | If set to 1, the first cast of the ability each match costs no resources. | 1 | `1` |
| `InterchangeDisabler` | Integer | If set to 1, prevents the unit from being interchanged with another unit. | 1 | `1` |
| [`PassiveWhileNotTakingTurn`](./Abilities_and_Spells.md#object-passivewhilenottakingturn) | Object  | A nested passive object that is active only while the unit is not currently taking its turn. | 1 | `{ . . . }` |
| `ReloadOnAllyCatDies` | Integer | If set to 1, restores a charge when an allied cat dies. | 1 | `1` |
| `ReloadOnAllyDies` | Integer | If set to 1, restores a charge when any ally dies. | 1 | `1` |
| `ReloadOnAnyDamage` | Integer | If set to 1, restores a charge when any damage is taken. | 1 | `1` |
| `ReloadOnBackstab` | Integer | If set to 1, restores a charge when performing a backstab. | 1 | `1` |
| [`ReloadOnElementalDamageReceived`](../Reference_and_Meta/Enums.md#enum-reloadonelementaldamagereceived) | Enum  | Specifies the elemental type of damage that, when received, restores a charge. | 1 | `Holy` |
| `ReloadOnGainCoins` | Integer | If set to 1, restores a charge when coins are gained. | 1 | `1` |
| `ReloadOnGainDivineShield` | Integer | If set to 1, restores a charge when a Divine Shield is gained. | 1 | `1` |
| [`ReloadOnKillTagged`](../Reference_and_Meta/Enums.md#enum-reloadonkilltagged) | Enum  | Specifies the tag of enemies that, when killed, restore a charge. | 1 | `rock` |
| `ReloadOnSpendMana` | Integer | If set to 1, restores a charge when mana is spent. | 1 | `1` |
| `ReloadOnUseAbilityWithManaCost` | Integer | Specifies the amount of mana cost that, when used, restores a charge. | 1 | `6` |
| `TossTargetIsAggroTarget` | Integer | If set to 1, the toss target is the unit's current aggro target. | 1 | `1` |
| `TossTargetIsBuddy` | Integer | If set to 1, the toss target is the unit's buddy. | 1 | `1` |
| `TossTargetIsNotInWater` | Integer | If set to 1, the toss target must not be in water terrain. | 1 | `1` |
| `XIsConsumedCharacterMaxHP` | Integer | Specifies the multiplier used to set X to the maximum HP of the consumed character. | 1 | `3` |
| `XIsCountDeaths` | Integer | If set to 1, X is equal to the number of deaths in the match. | 1 | `1` |
| [`XIsCountStatusStacks`](../Reference_and_Meta/Enums.md#enum-xiscountstatusstacks) | Enum  | Specifies the status field whose stacks are counted to set X. | 1 | `DodgeChance_Status` |
| `XIsFormulaLockedUntilComplete` | Enum | Specifies a stat (e.g., dex) whose value is locked in and used for X until the ability completes. | 1 | `dex` |
| `XIsIncreaseEachTurn` | Integer | Specifies the amount by which X increases each turn. | 1 | `1` |
| `XIsRampAndReset` | Integer | If set to 1, X ramps up over time and resets after use; 0 disables this behavior. | 1 | `0` |
| `XIsRecycleCostReduction` | Integer | Specifies the amount of recycle cost reduction applied to X. | 1 | `5` |

</details>


---


### Object: `temporary_effects`


**Definition:** Applies temporary status effects on the caster upon using the ability.  
**Total Count:** 88

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 37 | passives<br>class<br>tag |
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 26 | `1`<br>`3`<br>`4` |
| `CastAgain` | Integer | The number of additional times the ability can be cast this turn. | 20 | `1`<br>`2`<br>`3` |
| `DisableTrample` | Integer | If set to 1, trample damage is disabled for the duration of the effect. | 10 | `1` |
| `Fury` | Integer | The amount of Fury (bonus damage or charges) gained. | 7 | `10`<br>`55`<br>`75` |
| [`TileTrail`](../Reference_and_Meta/Enums.md#enum-tiletrail) | Enum  | Specifies the type of tile left behind as the unit moves. | 6 | `BrambleTile`<br>`CreepTile`<br>`FireTile` |
| `JustInCaseTrample` | Integer | If set to a non-zero value, applies a trample effect as a fallback. | 5 | `0` |
| [`LeaveBehind`](./Abilities_and_Spells.md#object-leavebehind) | Enum / Object  | Specifies the object or entity to spawn after the unit leaves a tile. | 5 | `{ . . . }`<br>`Bait` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 4 | Default<br>FormChange<br>Druid |
| `DashFury` | Integer | The amount of Fury gained after dashing. | 3 | `4` |
| [`AfterImage`](./Abilities_and_Spells.md#object-afterimage) | Object  | Specifies the object or skill used to create an afterimage of the unit. | 2 | `{ . . . }` |
| `BearTrapTrail` | Integer | If set to 1, leaves bear traps behind as the unit moves. | 2 | `1` |
| `KnockbackImmunity` | Integer | If set to 1, the unit cannot be knocked back. | 1 | `1` |
| `DoubleLoot` | Integer | The multiplier for loot drops, where 1 or 2 doubles the loot. | 1 | `1`<br>`2` |
| [`TileTrail_Ahead`](../Reference_and_Meta/Enums.md#enum-tiletrail_ahead) | Enum  | Specifies the type of tile to place one tile ahead of the unit's movement. | 1 | `FireTile`<br>`FlowerTile`<br>`OilTile` |
| `DelayedWindTrail` | Integer | If set to 1, creates a delayed wind trail behind the unit. | 1 | `1` |
| [`JumpAttackLeaveBehind`](../Reference_and_Meta/Enums.md#enum-jumpattackleavebehind) | Enum | Specifies the entity to leave behind at the jump attack's landing point. | 1 | `BungaThrone` |

</details>


---


### Object: `Else`


**Definition:** Contains the fallback effects to apply when a preceding conditional check fails.  
**Total Count:** 86

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional_boss), [`Conditional_Buddy`](./Abilities_and_Spells.md#object-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional_object), [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional_speculative), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 14 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 13 | passives<br>class<br>tag |
| `GainDisorderFromPool_PostCast` | `String` | Specifies the pool of disorders the unit can gain after the spell is cast. | 7 | `forbidden_spell_consequences`<br>`forbidden_spell_consequences_crippling` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 6 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 3 | `{ . . . }` |
| `Vaporize` | `Number` | Removes the target from play, preventing its corpse from being interacted with. | 3 | `1`<br>`20` |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate) | Object  | An object containing effects that can be applied to inanimate objects. | 3 | `{ . . . }` |
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 2 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`Confusion`](../Reference_and_Meta/Arrays.md#array-confusion) | Array / Integer  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| `Cleanse` | Integer | The number of stacks of negative status effects removed from the target. | 2 | `0`<br>`1` |
| `RandomStatUp` | Enum / Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `FullHeal` | `Number` | If non-zero, fully restores the target's health. | 2 | `0`<br>`1` |
| `Revive` | Integer | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `1`<br>`100%`<br>`50%` |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#object-conditional_hasstatus) | Object  | Contains an inner effect block that only executes if the target has the specified status effect. | 2 | `{ . . . }` |
| [`RandomStatDown`](../Reference_and_Meta/Arrays.md#array-randomstatdown) | Array / Integer / String  | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`1` |
| [`GainCoinsRange`](./Abilities_and_Spells.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 2 | `{ . . . }` |
| `SpawnThingIfHitKills` | `String` | The name of the thing (e.g., a food type) to spawn at the target's location upon a killing blow. | 2 | `Bait`<br>`BigFood`<br>`BiggestFood` |
| `SpawnBearTrapIfHitKills` | `Number` | If non-zero, spawns a bear trap at the target's location upon a killing blow. | 2 | `1` |
| [`Bruise`](../Reference_and_Meta/Arrays.md#array-bruise) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 1 | `1`<br>`2`<br>`3` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| [`Else`](./Abilities_and_Spells.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| `Slow` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 1 | `-1`<br>`1`<br>`2` |
| [`Temporary`](./Abilities_and_Spells.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 1 | `{ . . . }` |
| [`CatPartsTransform`](./Abilities_and_Spells.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 1 | `1`<br>`10`<br>`100` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 1 | `{ . . . }` |
| [`Immobile`](../Reference_and_Meta/Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | `0`<br>`1`<br>`10%` |
| [`ConstitutionUp`](../Reference_and_Meta/Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ . . . }` |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 1 | `{ . . . }` |
| [`ObjectOnHitCharacter`](./Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 1 | `1`<br>`10`<br>`100` |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 | `{ . . . }` |
| `Leeches` | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 1 | `1`<br>`2`<br>`3` |
| [`Consumed`](./Abilities_and_Spells.md#object-consumed) | Object  | An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`. | 1 | `{ . . . }` |
| [`Cleave`](./Abilities_and_Spells.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 1 | `{ . . . }`<br>`1` |
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 1 | `-10`<br>`0`<br>`1` |
| `GenericDebuff` | `Number` | The number of stacks of a generic, untooltipped debuff applied to the target. | 1 | `1`<br>`10`<br>`100` |
| `Instakill` | `Number` | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 1 | `25`<br>`50`<br>`999` |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional_speculative) | Object  | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 1 | `{ . . . }` |
| `ImmediateUseAbility` | `String` | Specifies the name of an ability to be triggered instantly from this effect. | 1 | `FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `PurgeAll` | `Number` | If non-zero, removes all temporary status effects (buffs, debuffs) from the target. | 1 | `1` |
| `SetHealth` | `Number` | Sets the target's health to a specific flat value or percentage. | 1 | `1`<br>`100%`<br>`50%` |
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. | 1 | `1`<br>`9999` |
| `VaporizeInanimate` | `Number` | If non-zero, instantly destroys inanimate objects (corpses, rocks) as if they were vaporized. | 1 | `1` |
| [`ScatterCoins`](./Abilities_and_Spells.md#object-scattercoins) | Object  | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 1 | `{ . . . }` |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 1 | `{ . . . }` |
| [`DoDamage`](./Abilities_and_Spells.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 1 | `{ . . . }` |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#object-destroyequipmentandattachparasite) | Object  | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 1 | `{ . . . }` |
| [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional_object) | Object  | Evaluates whether the target is an object (vs a character); if true, applies the effects within; otherwise, runs the Else block. | 1 | `{ . . . }` |
| `FaceCamera` | `Number` | If non-zero, forces the character to rotate and face the camera. | 1 | `1` |
| `DieViolently` | Integer | If true, causes the target to die with a violent, explosive visual effect. | 1 | `1` |
| [`ApplyToRandomPartyMemberIfPossible`](./Abilities_and_Spells.md#object-applytorandompartymemberifpossible) | Object  | Contains an inner effect block that is applied to a random living party member if one exists. | 1 | `{ . . . }` |
| `FlatAIBonus` | `Number` | A flat adjustment to the AI's evaluation score for this action; positive values encourage the AI to use it, negative values discourage it. | 1 | `-999999`<br>`100`<br>`999999` |
| `RemoveMovePoints` | `Number` | The number of move points to remove from the target, preventing them from moving. | 1 | `1` |
| `SetShield` | `Number` | Sets the target's shield value to a specific flat amount. | 1 | `0`<br>`88` |
| `SpeculativeMoveSelfCorpseOffMap` | `Number` | If true, attempts to remove the character's corpse from the map, used for speculative AI targeting. | 1 | `1` |
| [`DybbukPossessed`](./Abilities_and_Spells.md#object-dybbukpossessed) | Object  | Contains parameters for the Dybbuk possession status, specifying exit ability and self-punch ability. | 1 | `{ . . . }` |
| [`Conditional_Displaceable`](./Abilities_and_Spells.md#object-conditional_displaceable) | Object  | Contains an inner effect block that only executes if the target can be displaced (knocked back). | 1 | `{ . . . }` |
| `ExplodeCharacter` | `Number` | The radius (in tiles) of an explosion centered on the character. | 1 | `5` |
| [`XIsTargetHealth`](./Abilities_and_Spells.md#object-xistargethealth) | Object  | Evaluates a bonus damage formula where X is the target's current health. | 1 | `{ . . . }` |
| `ExplodeCharacter_Party` | `Number` | The radius (in tiles) of an explosion centered on the character that also damages party members. | 1 | `5` |
| `ForceImmediateMove` | `Number` | If non-zero, forces the character to move instantly without waiting for normal action order. | 1 | `1` |
| `RemoveTurnsThisRound` | `Number` | The number of turns to remove from the target's turn order this round. | 1 | `1` |
| [`ShowFakeDamage`](./Abilities_and_Spells.md#object-showfakedamage) | Object  | Displays a fake damage number (with optional style) for visual effect without actually changing health. | 1 | `{ . . . }` |
| `CaptureFamiliar` | Integer | The number of times to attempt to capture the target as a familiar. | 0 | `1` |
| `FactionConversion` | Integer | Converts the target to the caster's faction. | 0 | `1` |

</details>


---


### Object: `ChangeTile`


**Definition:** Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect).  
**Total Count:** 74

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tile`](../Reference_and_Meta/Arrays.md#array-tile) | Array / Enum  | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 11 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |
| `aoe` | Integer | The radius (in tiles) of the area affected by the tile change. | 1 | `1` |

</details>


---


### Object: `MeleeRevengeDamage`


**Definition:** Defines the damage and effects applied back to a melee attacker upon being hit.  
**Total Count:** 73

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#object-temppassivewhilehasstatus)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 2 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `ApplyToSource`


**Definition:** An object of effects that are applied to the source of the ability (the caster).  
**Total Count:** 59

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyStatusIfCrit`](./Abilities_and_Spells.md#object-applystatusifcrit), [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate), [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional_goodroll), [`Conditional_HasStatus`](./Abilities_and_Spells.md#object-conditional_hasstatus), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional_healththreshold), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#object-conditional_livingplayercat), [`Conditional_PlayerCat`](./Abilities_and_Spells.md#object-conditional_playercat), [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#object-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#object-else), [`Math`](./Abilities_and_Spells.md#object-math), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 18 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 14 | Default<br>FormChange<br>Druid |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 5 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `HealthGain` | Integer | The amount of health restored to the source. | 5 | `1`<br>`10`<br>`2` |
| `FormChange` | `String` | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 4 | `Big`<br>`BigHolding`<br>`BigHoldingCat` |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 4 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `EvolveAbilityFromPool` | `String` | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 4 | `Butcher`<br>`Druid`<br>`Fighter` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 3 | `-1`<br>`-2`<br>`1` |
| [`ConstitutionUp`](../Reference_and_Meta/Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 3 | `-1`<br>`-2`<br>`1` |
| `RefreshActPoints` | `Number` | The amount of action points restored to the source. | 3 | `1` |
| [`Craft`](./Abilities_and_Spells.md#object-craft) | Object  | Specifies the loot pool and slot to craft an item for the source. | 3 | `{ . . . }` |
| `AddWeaponAux` | Equation | The amount or expression to add to the source's weapon auxiliary stat. | 3 | `"-max(min(X+1, item_aux), 0)"`<br>`-item_aux`<br>`1` |
| `Cleanse` | Integer | The number of stacks of negative status effects removed from the target. | 2 | `0`<br>`1` |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| [`FindItemFromPool`](./Abilities_and_Spells.md#object-finditemfrompool) | Object  | Specifies the loot pool from which to find an item, with an optional chance. | 2 | `{ . . . }` |
| `RemoveStatus` | `String` | The name of the status effect to remove from the source. | 2 | `AlphaCat`<br>`Brace`<br>`DodgeChance_Status` |
| `FreeSpell` | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. | 2 | `1`<br>`2` |
| [`DoDamage`](./Abilities_and_Spells.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 2 | `{ . . . }` |
| [`EquipPermanentItem`](../Reference_and_Meta/Enums.md#enum-equippermanentitem) | Enum  | The name of the item to permanently equip to the source. | 2 | `BoneClub`<br>`Kidney` |
| `AddLeechesStatus` | `Number` | The number of stacks of Leech status applied to the source, healing when dealing damage. | 2 | `1` |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | `1`<br>`10`<br>`2` |
| [`Bruise`](../Reference_and_Meta/Arrays.md#array-bruise) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 1 | `1`<br>`2`<br>`3` |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | `1`<br>`2`<br>`3` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 1 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`ForceUseAbility`](../Reference_and_Meta/Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `TakeExtraTurn` | `Number` | The number of extra turns granted to the source. | 1 | `1` |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 | `{ . . . }` |
| `FullHeal` | `Number` | If non-zero, fully restores the target's health. | 1 | `0`<br>`1` |
| `RefreshMovePoints` | `Number` | The amount of movement points restored to the source. | 1 | `1` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`[1, 0.1]` |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 1 | `1`<br>`3` |
| [`GainCoinsRange`](./Abilities_and_Spells.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 1 | `{ . . . }` |
| `SpecificInjury` | `String` | The stat (str, spd, int) to which a specific injury is applied, reducing that stat. | 1 | `int`<br>`spd`<br>`str` |
| `StanceSwitchToMelee` | `Number` | If set, switches the source to melee stance. | 1 | `1` |
| `TempTrampleUntilSettled` | `Number` | The number of stacks of temporary Trample applied to the source, allowing movement through enemies until the source ends its turn. | 1 | `3` |
| [`FindItem`](../Reference_and_Meta/Enums.md#enum-finditem) | Enum  | The name of the specific item to find and add to the source's inventory. | 1 | `BoneClub`<br>`Molars`<br>`Pearl` |
| `DisableWeapon` | `Number` | If set, disables the source's weapon, preventing its use. | 1 | `1` |
| `StanceSwitchToRanged` | `Number` | If set, switches the source to ranged stance. | 1 | `1` |

</details>


---


### Object: `Temporary`


**Definition:** Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions.  
**Total Count:** 57

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate), [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_NotAlly`](./Abilities_and_Spells.md#object-conditional_notally), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 41 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 41 | `{ . . . }` |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 40 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 40 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `expires_on_begin_turn` | Boolean | If true, the temporary effect expires at the start of the target's turn. | 19 | `true` |
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 11 | `true` |
| `data` | Integer | An integer value used for custom data associated with the temporary effect. | 2 | `2` |
| `expires_on_appliers_turn` | Boolean | If true, the temporary effect expires at the start of the applier's next turn. | 2 | `true` |
| `expires_on_move` | Boolean | If true, the temporary effect expires when the target moves. | 1 | `true` |

</details>


---


### Object: `CatPartsTransform`


**Definition:** Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs.  
**Total Count:** 55

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `tail` | Integer | The catalog ID for the cat's tail part. | 10 | `-1`<br>`1000`<br>`1001` |
| `ear1` | Integer | The catalog ID for the cat's first ear part. | 10 | `-2`<br>`1005`<br>`1013` |
| `ear2` | Integer | The catalog ID for the cat's second ear part. | 9 | `1005`<br>`1013`<br>`1036` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 8 | `-1`<br>`-2`<br>`1` |
| `arm2` | Number | The catalog ID for the cat's second arm part. | 8 | `-1`<br>`-2`<br>`1` |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 7 | `-1`<br>`-2`<br>`1` |
| `leg1` | Integer | The catalog ID for the cat's first leg part. | 5 | `-1`<br>`-2`<br>`1` |
| `leg2` | Integer | The catalog ID for the cat's second leg part. | 5 | `-1`<br>`1`<br>`10` |
| `head` | Float | The catalog ID for the cat's head part. | 3 | `-1`<br>`1`<br>`1.3` |
| `texture` | Integer | The catalog ID for the cat's texture. | 3 | `-1`<br>`1`<br>`1000` |
| `body` | Float | The catalog ID for the cat's body part. | 2 | `-1`<br>`1`<br>`1.1` |
| `palette` | Integer | Specifies the color palette index for the ability's visuals. | 1 | `-1`<br>`0`<br>`1` |
| `eye1` | Integer | The catalog ID for the cat's first eye part. | 1 | `-1`<br>`-2`<br>`1013` |
| `eye2` | Integer | The catalog ID for the cat's second eye part. | 1 | `-1`<br>`1013`<br>`1057` |
| `eyebrow1` | Integer | The catalog ID for the cat's first eyebrow part. | 1 | `-2`<br>`1069` |
| `eyebrow2` | Integer | The catalog ID for the cat's second eyebrow part. | 1 | `1070` |

</details>


---


### Object: `StatusOnBattleEnd`


**Definition:** An object containing status effects or passives applied to the unit when the battle ends.  
**Total Count:** 53

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./Abilities_and_Spells.md#object-applypassives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `even_if_dead` | Boolean | If true, the effect triggers even if the unit is dead. | 3 | `true` |
| [`RandomTaggedMutation`](../Reference_and_Meta/Enums.md#enum-randomtaggedmutation) | Enum  | Specifies the tag to filter random mutations by. | 2 | `bird`<br>`melted` |
| `RandomMutation` | Integer | The number of random mutations to apply. | 1 | `1`<br>`3` |

</details>


---


### Object: `Conditional_HasTag`


**Definition:** Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block.  
**Total Count:** 47

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional_object), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 41 | passives<br>class<br>tag |
| [`tag`](../Reference_and_Meta/Enums.md#enum-tag) | Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 41 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 37 | Default<br>FormChange<br>Druid |
| [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional_notboss) | Object  | Contains effects that apply only if the target is not a boss enemy. | 6 | `{ . . . }` |
| `FloatingRockTrap` | `Number` | The number of stacks of Floating Rock Trap applied to the target, dealing damage when stepped on. | 6 | `1` |
| [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional_boss) | Object  | Contains effects that apply only if the target is a boss enemy. | 4 | `{ . . . }` |
| `IgnoreDamage` | `Number` | If set, the target ignores all damage for the duration. | 4 | `1` |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 3 | `{ . . . }` |
| `ImmediateUseAbility` | `String` | Specifies the name of an ability to be triggered instantly from this effect. | 3 | `FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Else`](./Abilities_and_Spells.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 2 | `{ . . . }` |
| `Vaporize` | `Number` | Removes the target from play, preventing its corpse from being interacted with. | 2 | `1`<br>`20` |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#object-applytosourceonkill) | Object  | Contains effects that are applied to the source when it kills the target. | 2 | `{ . . . }` |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate) | Object  | An object containing effects that can be applied to inanimate objects. | 2 | `{ . . . }` |
| `Die` | `Number` | If set, kills the target immediately. | 2 | `1`<br>`6` |
| [`ChangeTilesUnder`](../Reference_and_Meta/Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. | 2 | `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 1 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| `FaceAway` | `Number` | If set, forces the target to face away from the source. | 1 | `1` |
| `VaporizeCorpse` | `Number` | If set, vaporizes the target's corpse, preventing revival. | 1 | `1` |
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 1 | `-10`<br>`0`<br>`1` |
| `RemoveStatus` | `String` | The name of the status effect to remove from the source. | 1 | `AlphaCat`<br>`Brace`<br>`DodgeChance_Status` |
| `UseAbility` | `String` | The name of the ability the target is forced to use. | 1 | `GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| `Instakill` | `Number` | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 1 | `25`<br>`50`<br>`999` |
| [`Conditional_InForm`](./Abilities_and_Spells.md#object-conditional_inform) | Object  | Contains effects that apply only if the target is in the specified form. | 1 | `{ . . . }` |
| `DeleteObject` | `Number` | If set, deletes the target object from the map. | 1 | `1` |
| [`PopAndSpawn`](./Abilities_and_Spells.md#object-popandspawn) | Enum / Object  | The object (enemy or entity) to spawn on the target's tile, optionally with visual effects. | 1 | `{ . . . }`<br>`Sprout`<br>`StemCat_HalfHealth`<br>`TheDestroyer` |
| `DisplaceTowardsSource` | `Number` | If set, displaces the target towards the source of the effect. | 1 | `1` |
| `ScatterRandomPickups` | `Number` | The number of random pickups scattered around the target's location. | 1 | `2`<br>`5` |
| `SetKnockback` | `Number` | The knockback distance to set for the damage instance, overriding default. | 1 | `0` |
| `EventBounty` | Integer | The number of stacks of Event Bounty applied, increasing event rewards. | 1 | `5` |
| `CrackMoonHead` | `Number` | If set, cracks the MoonHead's head, triggering its death sequence. | 1 | `1` |
| [`MergeDamageInstance`](./Abilities_and_Spells.md#object-mergedamageinstance) | Object  | Specifies parameters to merge multiple damage instances into one, controlling hit animation and instant pop behavior. | 1 | `{ . . . }` |
| [`SetAnimationAlts`](./Abilities_and_Spells.md#object-setanimationalts) | Object  | Specifies alternative animation names for the target's dying and dead states. | 1 | `{ . . . }` |

</details>


---


### Object: `Madness`


**Definition:** The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability].  
**Total Count:** 45

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `tickdown_this_turn` | Boolean | If true, madness stacks decrease at the start of this turn instead of the next. | 1 | `true` |

</details>


---


### Object: `Conditional_Enemy`


**Definition:** An object containing status effects or actions applied only if the target is an enemy.  
**Total Count:** 44

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Corpse`](./Abilities_and_Spells.md#object-conditional_corpse), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](../Reference_and_Meta/Arrays.md#array-confusion) | Array / Integer  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `1`<br>`10`<br>`2` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 5 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional_notboss) | Object  | Contains effects that apply only if the target is not a boss enemy. | 3 | `{ . . . }` |
| `DisplaceToAbilityTarget` | Integer | If set, displaces the source to the ability's target location. | 3 | `1` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| [`Weakness`](../Reference_and_Meta/Arrays.md#array-weakness) | Array / Integer  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| [`Madness`](./Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `TakeExtraTurn` | `Number` | The number of extra turns granted to the source. | 2 | `1` |
| `Attraction` | Integer | The number of stacks of Attraction applied, drawing enemy units toward the target. | 2 | `1` |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 1 | `{ . . . }` |
| [`Temporary`](./Abilities_and_Spells.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 1 | `{ . . . }` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 1 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`Marked`](../Reference_and_Meta/Arrays.md#array-marked) | Array / Integer  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`3`<br>`5` |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#object-applytosourceonkill) | Object  | Contains effects that are applied to the source when it kills the target. | 1 | `{ . . . }` |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. | 1 | `-1`<br>`1`<br>`2` |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 1 | `1`<br>`2`<br>`3` |
| `ForceMoveTowards` | `Number` | The number of tiles to force the target to move toward the caster. | 1 | `1` |
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. | 1 | `1` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 1 | `1` |
| [`Conditional_FinishedSpawning`](./Abilities_and_Spells.md#object-conditional_finishedspawning) | Object  | Contains an inner effect block that only executes if the target has finished its spawning animation. | 1 | `{ . . . }` |

</details>


---


### Object: `FindItemFromPool`


**Definition:** Specifies the loot pool from which to find an item, with an optional chance.  
**Total Count:** 43

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `RandomMagicMissile`


**Definition:** The number of random magic missiles fired, or an object defining its properties.  
**Total Count:** 41

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `full_size` | Boolean | If true, the magic missile uses its full size instead of a reduced size. | 2 | `true` |

</details>


---


### Object: `sounds`


**Definition:** Defines sound effects played at various points of the ability (e.g., ontrigger, oncastpoint).  
**Total Count:** 39

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ontrigger`](../Reference_and_Meta/Enums.md#enum-ontrigger) | Enum | Specifies the sound effect to play when the ability triggers (e.g., hits a target). | 32 | `OldHose_Start_Trigger`<br>`SE_AnkylosaurusAttack`<br>`SE_AstroTaserPoke` |
| [`oncast`](../Reference_and_Meta/Enums.md#enum-oncast) | Enum | Specifies the sound effect to play when the ability is cast. | 3 | `AbilitySnd_Assassinate`<br>`AbilitySnd_BoulderDrop` |
| [`oncastpoint`](../Reference_and_Meta/Enums.md#enum-oncastpoint) | Enum | Specifies the sound effect to play at a specific cast point during the ability animation. | 3 | `AirHorn`<br>`Batterup_Swing_Castpoint` |
| [`ontrigger_intentional`](../Reference_and_Meta/Enums.md#enum-ontrigger_intentional) | Enum | Specifies the sound effect to play when the ability is triggered intentionally (as opposed to automatically). | 1 | `Lenny_HereKitty` |

</details>


---


### Object: `BounceObject`


**Definition:** Specifies the object or projectile to spawn and bounce from the target.  
**Total Count:** 39

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`obj`](../Reference_and_Meta/Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 3 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |
| `slide` | Integer | The number of tiles the bounced object slides toward the target. | 1 | `10` |

</details>


---


### Object: `Conditional_GoodRoll`


**Definition:** Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 12 | Default<br>FormChange<br>Druid |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 12 | `.1`<br>`.16666666`<br>`.3` |
| `GainDisorderFromPool_PostCast` | `String` | Specifies the pool of disorders the unit can gain after the spell is cast. | 7 | `forbidden_spell_consequences`<br>`forbidden_spell_consequences_crippling` |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 1 | `{ . . . }` |
| `ImmediateUseAbility` | `String` | Specifies the name of an ability to be triggered instantly from this effect. | 1 | `FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `RefreshWeaponAbility` | `Number` | The number of times the weapon's ability is refreshed. | 1 | `1` |
| [`ApplyToRandomPartyMemberIfPossible`](./Abilities_and_Spells.md#object-applytorandompartymemberifpossible) | Object  | Contains an inner effect block that is applied to a random living party member if one exists. | 1 | `{ . . . }` |
| `ShowText` | `String` | Specifies the localization key for a popup text displayed on the target. | 1 | `"COMBAT_POPUP_BRAINSTORM"`<br>`"COMBAT_POPUP_RELOAD"`<br>`"COMBAT_POPUP_REPAIRED"` |
| `GainDisorder` | `String` | Specifies the name of the disorder gained. | 1 | `Chungus`<br>`Psychosis` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `Conditional_Ally`


**Definition:** Defines effects that apply only if the target is an ally, with an optional else block for non-allies.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 13 | passives<br>class<br>tag |
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 4 | `-10`<br>`0`<br>`1` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 3 | Default<br>FormChange<br>Druid |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 3 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Temporary`](./Abilities_and_Spells.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 3 | `{ . . . }` |
| `KnockbackDamageImmuneUntilSettled` | `Number` | If non-zero, makes the target immune to damage from knockback until they stop moving. | 3 | `1` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| `HealthGain` | Integer | The amount of health restored to the source. | 2 | `1`<br>`10`<br>`2` |
| `RandomStatUp` | Enum / Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| `Cleanse` | Integer | The number of stacks of negative status effects removed from the target. | 1 | `0`<br>`1` |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 1 | `{ . . . }` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| `FullHeal` | `Number` | If non-zero, fully restores the target's health. | 1 | `0`<br>`1` |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#object-applytosourceonkill) | Object  | Contains effects that are applied to the source when it kills the target. | 1 | `{ . . . }` |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. | 1 | `-1`<br>`1`<br>`2` |
| `ChanceToBreak` | `Number` | Specifies the percentage chance that the item breaks on use. | 1 | `100`<br>`15`<br>`20` |
| [`Conditional_Corpse`](./Abilities_and_Spells.md#object-conditional_corpse) | Object  | Contains an inner effect block that only executes if the target is a corpse. | 1 | `{ . . . }` |
| [`Conditional_PlayerCat`](./Abilities_and_Spells.md#object-conditional_playercat) | Object  | Defines effects that only apply if the target is a player-controlled cat. | 1 | `{ . . . }` |
| `RepairAll` | `Number` | The amount of durability restored to all equipped items. | 1 | `1`<br>`10` |
| `ShowText` | `String` | Specifies the localization key for a popup text displayed on the target. | 1 | `"COMBAT_POPUP_BRAINSTORM"`<br>`"COMBAT_POPUP_RELOAD"`<br>`"COMBAT_POPUP_REPAIRED"` |
| `ThornsDamageImmuneUntilSettled` | `Number` | The number of turns the target is immune to thorns damage until it settles. | 1 | `1` |
| `TileDamageImmuneUntilSettled` | `Number` | The number of turns the target is immune to tile damage until it settles. | 1 | `1` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 0 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |

</details>


---


### Object: `splash_damage`


**Definition:** Defines additional damage or effects applied to nearby targets around the primary target.  
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#object-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 35 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`damage`](./Abilities_and_Spells.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 32 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 17 | `{ . . . }` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 13 | `[`<br>`[Heat Fire]` |
| `knockback` | Equation | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 13 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 12 | `[attack move spell]`<br>`attack`<br>`battle` |
| `makes_contact` | `Boolean` | If true, the damage instance is considered a contact hit, triggering contact-based passives on both the attacker and target. | 6 | `false`<br>`true` |
| `override_trample_damage` | `Boolean` | If true, this damage instance replaces any default trample damage when the unit passes through an occupied tile. | 2 | `true` |
| `ai_base_score` | Integer | The base priority score the AI assigns to using this damage instance, with higher values indicating greater preference. | 1 | `-99999`<br>`-999999`<br>`1` |
| `layer` | `String` | Specifies the layer on which the ability's effect operates (e.g., characters, tiles, gas). | 1 | `2`<br>`all`<br>`characters` |
| `crit_chance` | Float | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 1 | `-999999`<br>`.05*X`<br>`.25` |
| `force_play_hit_animation` | `Boolean` | If true, the hit animation is forced to play regardless of other conditions (e.g., miss or block). | 1 | `true` |
| `force_no_knockback` | `Boolean` | If true, the damage instance applies no knockback regardless of any knockback values set. | 1 | `true` |

</details>


---


### Object: `RandomStatusFromPool`


**Definition:** A collection of status effects; one is randomly chosen and applied to the target.  
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyMultipleTimes`](./Abilities_and_Spells.md#object-applymultipletimes), [`Conditional_CanBeHealed`](./Abilities_and_Spells.md#object-conditional_canbehealed), [`Conditional_HasCleansableDebuffs`](./Abilities_and_Spells.md#object-conditional_hascleansabledebuffs), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 14 | passives<br>class<br>tag |
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 12 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 7 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `GainCoins` | Integer | The amount of coins gained, or a [min, max] range. | 7 | `-5`<br>`1`<br>`2` |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 6 | `1`<br>`10`<br>`2` |
| `Slow` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 6 | `-1`<br>`1`<br>`2` |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 6 | `1`<br>`2`<br>`4` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 5 | `1`<br>`10`<br>`2` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 4 | `-1`<br>`-2`<br>`-4` |
| `RandomStatUp` | Enum / Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 4 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`ConstitutionUp`](../Reference_and_Meta/Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 4 | `-1`<br>`-2`<br>`1` |
| `Charge` | Equation | The number of charge stacks applied. | 4 | `1`<br>`2`<br>`3` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 4 | `1`<br>`2`<br>`3` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 4 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 24 | Default<br>FormChange<br>Druid |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 3 | `1`<br>`10`<br>`2` |
| [`Bruise`](../Reference_and_Meta/Arrays.md#array-bruise) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 3 | `1`<br>`2`<br>`3` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 3 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Weakness`](../Reference_and_Meta/Arrays.md#array-weakness) | Array / Integer  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`2`<br>`3` |
| `Quivered` | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 3 | `1`<br>`2`<br>`5` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 3 | `1`<br>`2`<br>`[1, 0.1]` |
| [`IncAuxCounterClamped`](./Abilities_and_Spells.md#object-incauxcounterclamped) | Object  | An object with `change` and `max` properties modifying the auxiliary counter by `change`, clamped to `max`. | 3 | `{ . . . }` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 2 | `1`<br>`2`<br>`3` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 2 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 2 | `1`<br>`10`<br>`100` |
| [`Madness`](./Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 2 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 2 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Marked`](../Reference_and_Meta/Arrays.md#array-marked) | Array / Integer  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`3`<br>`5` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 | `1`<br>`10`<br>`100` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 2 | `-1`<br>`1`<br>`2` |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 2 | `1`<br>`2`<br>`3` |
| [`MagicWeakness`](../Reference_and_Meta/Arrays.md#array-magicweakness) | Array / Integer  | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`3` |
| [`Rot`](../Reference_and_Meta/Arrays.md#array-rot) | Array / Integer  | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 2 | `-999999`<br>`1`<br>`2` |
| [`Tarred`](../Reference_and_Meta/Arrays.md#array-tarred) | Array / Integer  | The amount of tarred stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`[1 .1]` |
| `CharismaUp` | Integer | The amount of charisma change, or a keyword like 'item_aux'. | 2 | `-1`<br>`-2`<br>`1` |
| [`BackflipWhenTargeted`](./Abilities_and_Spells.md#object-backflipwhentargeted) | Integer / Object  | The number of backflip charges, or an object defining its ability. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`X` |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. | 2 | `1`<br>`2`<br>`3` |
| `Reflect` | Integer | The amount of reflect stacks applied. | 2 | `1`<br>`5` |
| `PoisonLace` | Enum / Equation | Integer or fractional string (e.g., 'X/3') specifying the duration or intensity of the PoisonLace effect. | 2 | `"X/3"`<br>`"X/5"`<br>`1` |
| `Lifesteal` | Integer | The amount of lifesteal stacks applied. | 2 | `1`<br>`3` |
| `TempCounterAttack` | Integer | The number of turns TempCounterAttack lasts, ticking down at the start of the unit's turn. | 2 | `1` |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`Confusion`](../Reference_and_Meta/Arrays.md#array-confusion) | Array / Integer  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .01]` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| [`Immobile`](../Reference_and_Meta/Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | `0`<br>`1`<br>`10%` |
| [`Blind`](../Reference_and_Meta/Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 1 | `-1`<br>`1`<br>`2` |
| [`Petrify`](../Reference_and_Meta/Arrays.md#array-petrify) | Array / Integer  | The amount of petrify stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`[1 .15]`<br>`[1 .1]` |
| [`Sleep`](../Reference_and_Meta/Arrays.md#array-sleep) | Array / Integer  | The amount of sleep stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`3` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 1 | `1`<br>`3` |
| `RefreshMovePoints` | Integer | The amount of movement points restored to the source. | 1 | `1` |
| `RefreshActPoints` | Integer | The amount of action points restored to the source. | 1 | `1` |
| `Infested` | Integer | The number of stacks of Infested applied. | 1 | `1` |
| [`RandomStatDown`](../Reference_and_Meta/Arrays.md#array-randomstatdown) | Array / Enum / Integer  | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`1` |
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. | 1 | `1` |
| `Ostracized` | Integer | The number of stacks of Ostracized applied. | 1 | `1`<br>`2`<br>`4` |
| `DelayedPain` | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. | 1 | `1` |
| `Scrambled` | Integer | The number of stacks of Scrambled applied. | 1 | `1`<br>`2` |

</details>


---


### Object: `keyword_tooltips`


**Definition:** Associates keyword tooltips with the ability, often used for status effects.  
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 10 | passives<br>class<br>tag |
| [`BonusAbility`](../Reference_and_Meta/Enums.md#enum-bonusability) | Enum  | Specifies the name of a bonus ability granted. | 5 | `Bloodzerk`<br>`BonusToss`<br>`BonusToss2` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | `1`<br>`10`<br>`2` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| [`Madness`](./Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`RandomMagicMissile`](./Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. | 1 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .1]` |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. | 1 | `1` |
| `TemporaryItem` | Integer | The number of times a temporary item can be used before disappearing. | 1 ||
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `RevengeDamage`


**Definition:** An object defining the damage and effects that trigger when the unit is attacked.  
**Total Count:** 31

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |

</details>


---


### Object: `ObjectOnHitCharacter`


**Definition:** Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit.  
**Total Count:** 31

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>tag |

</details>


---


### Object: `EvolveAbilityFromPool`


**Definition:** Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it.  
**Total Count:** 26

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 13 | `2`<br>`3`<br>`4` |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 13 | `true` |

</details>


---


### Object: `KnockUpAndAway`


**Definition:** Contains parameters for launching the target upward and away from the source, including stacks and distance.  
**Total Count:** 25

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`Conditional_LastHit`](./Abilities_and_Spells.md#object-conditional_lasthit), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 20 | `-3`<br>`10`<br>`2` |
| `stacks` | Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 18 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `height` | Integer | The height in tiles the target is launched into the air. | 2 | `0`<br>`1`<br>`2` |
| `circular_variance` | Integer | The random variance in the knockback direction, in tiles. | 1 | `2` |

</details>


---


### Object: `Consumed`


**Definition:** An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`.  
**Total Count:** 23

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#object-conditional_buddy), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#object-conditional_livingplayercat), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 18 | Default<br>FormChange<br>Druid |
| `struggle_ability` | `String` | Specifies the name of the ability the consumed unit uses to attempt escape. | 13 | `CHuskStruggle`<br>`CaveWomanEscape`<br>`LennyStruggle` |
| `force_contact` | `Boolean` | If true, the consumed unit is forced into contact with the consumer. | 11 | `true` |
| `instant` | `Boolean` | If true, the consumption happens immediately without a timer. | 8 | `true` |
| `mount_mode` | `String` | Specifies the mounting mode; values include 'auto' or 'true'. | 8 | `auto`<br>`true` |
| `wet` | `Boolean` | If true, the consumed unit is considered wet (e.g., for elemental interactions). | 8 | `false`<br>`true` |
| `do_not_pop_corpse` | `Boolean` | If true, the consumed unit's corpse is not popped upon consumption. | 7 | `true` |
| `drop_on_death` | `String` | Determines if and how the consumed unit is dropped on death; values include 'true', 'false', or 'deferred'. | 7 | `deferred`<br>`false`<br>`true` |
| [`extra_statuses`](./Abilities_and_Spells.md#object-extra_statuses) | Object  | An object containing additional status effects (with stack counts) applied to the consumed unit. | 3 | `{ . . . }` |
| `drop_on_self_death` | `Boolean` | If true, the consumed unit is dropped when the consumer dies. | 3 | `true` |
| `use_placeholder` | Boolean | If true, renders the ability using a temporary placeholder animation instead of the final art. | 1 | `true` |
| `drop_body_ability` | `String` | Specifies the ability used to drop the consumed body. | 1 | `MoonHandDrop` |
| `kill_on_consume` | `Boolean` | If true, the consumed unit is killed immediately upon consumption. | 1 | `true` |

</details>


---


### Object: `Conditional_Boss`


**Definition:** Contains effects that apply only if the target is a boss enemy.  
**Total Count:** 21

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 6 | Default<br>FormChange<br>Druid |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#object-conditional_hasstatus) | Object  | Contains an inner effect block that only executes if the target has the specified status effect. | 6 | `{ . . . }` |
| [`Else`](./Abilities_and_Spells.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 4 | `{ . . . }` |
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 4 | `-10`<br>`0`<br>`1` |
| `RemoveStatus` | `String` | The name of the status effect to remove from the source. | 4 | `AlphaCat`<br>`Brace`<br>`DodgeChance_Status` |
| `VisualFX` | `String` | Specifies the name of the visual effect to play. | 3 | `BigMagicMissileBlast`<br>`Bolt`<br>`Cleanse` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 2 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| `Drowsy` | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`8` |
| `ExplodeCharacter_PartyBoss` | Integer | The damage dealt to the party boss when it explodes. | 2 | `5` |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Integer | The damage dealt when a petrified RockCrusher explodes. | 2 | `5`<br>`9` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| `ExplodeCharacter_NoDie` | `Number` | The damage dealt when a character explodes without dying. | 1 | `1`<br>`5` |
| [`XIsTargetHealth`](./Abilities_and_Spells.md#object-xistargethealth) | Object  | Evaluates a bonus damage formula where X is the target's current health. | 1 | `{ . . . }` |

</details>


---


### Object: `Craft`


**Definition:** Specifies the loot pool and slot to craft an item for the source.  
**Total Count:** 20

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 9 | `2`<br>`3`<br>`4` |
| `slot` | Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 8 | `0`<br>`1`<br>`2` |
| `temporary` | Boolean | If true, the crafted item is temporary and will be removed after the battle or a set duration. | 4 | `false` |
| `works_with_tech` | Boolean | If true, the craft effect is compatible with tech-based interactions or abilities. | 1 | `true` |

</details>


---


### Object: `Conditional_HasStatus`


**Definition:** Contains an inner effect block that only executes if the target has the specified status effect.  
**Total Count:** 20

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional_boss), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 13 | passives<br>class<br>tag |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 13 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 6 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 10 | Default<br>FormChange<br>Druid |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 2 | `1`<br>`10`<br>`2` |
| [`Confusion`](../Reference_and_Meta/Arrays.md#array-confusion) | Array / Integer  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| `Slow` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 2 | `-1`<br>`1`<br>`2` |
| [`RemoveStatus`](../Reference_and_Meta/Enums.md#enum-removestatus) | Enum  | The name of the status effect to remove from the source. | 2 | `AlphaCat`<br>`Brace`<br>`DodgeChance_Status` |
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 1 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| `Quivered` | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`5` |

</details>


---


### Object: `additional_passives`


**Definition:** Additional passive abilities applied to the spawned unit.  
**Total Count:** 20

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#object-spawn)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 16 | passives<br>class<br>tag |
| `SafeDoomed` | Equation | The number of SafeDoomed stacks applied, or 'level' to scale with character level. | 11 | `1`<br>`2`<br>`level` |
| `InjuryImmunity` | Integer | The number of turns the unit is immune to injuries. | 7 | `1` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. | 2 | `1` |
| `FadeInsteadOfDie` | Integer | If non-zero, the unit fades out instead of dying. | 2 | `1` |
| `IllusionTint` | Integer | If non-zero, applies an illusionary tint to the unit's sprite. | 2 | `1` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. | 1 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| `CaptureFamiliar` | Integer | The number of times to attempt to capture the target as a familiar. | 1 | `1` |
| [`ReviveNextRound`](./Abilities_and_Spells.md#object-revivenextround) | Integer / Object  | The number of revives granted, or an object defining revive properties. | 1 | `{ . . . }`<br>`2` |
| [`HideEquipment`](../Reference_and_Meta/Enums.md#enum-hideequipment) | Enum  | Specifies which equipment slot is visually hidden. | 1 | `neck` |
| [`ApplyPassivesToSpawnerWhileAlive`](./Abilities_and_Spells.md#object-applypassivestospawnerwhilealive) | Object  | An object defining passives that are applied to the spawner while this unit is alive. | 1 | `{ . . . }` |
| `SchizoIllusionAIModifier` | Integer | If non-zero, modifies the AI behavior for schizo illusions. | 1 | `1` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `Cleave`


**Definition:** The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt.  
**Total Count:** 19

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `Metronome`


**Definition:** The number of times Metronome triggers, or an object with stacks and banned abilities.  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`banned_abilities`](../Reference_and_Meta/Arrays.md#array-banned_abilities) | Array | A list of ability IDs that are excluded from random selection or usage in the Metronome effect. | 1 ||
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |

</details>


---


### Object: `Conditional_NotBoss`


**Definition:** Contains effects that apply only if the target is not a boss enemy.  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` | [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | Default<br>FormChange<br>Druid |
| `Vaporize` | Integer | Removes the target from play, preventing its corpse from being interacted with. | 2 | `1`<br>`20` |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 2 | `1`<br>`2`<br>`3` |
| `CaptureFamiliar` | Integer | The number of times to attempt to capture the target as a familiar. | 2 | `1` |
| `VaporizeInanimate` | Integer | If non-zero, instantly destroys inanimate objects (corpses, rocks) as if they were vaporized. | 2 | `1` |
| `FactionConversion` | Integer | Converts the target to the caster's faction. | 2 | `1` |
| `ExplodeCharacter_RockCrusher` | Integer | The number of RockCrusher explosion triggers applied to non-boss characters. | 2 | `5`<br>`9` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate) | Object  | An object containing effects that can be applied to inanimate objects. | 1 | `{ . . . }` |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 1 | `{ . . . }` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 1 | `1` |

</details>


---


### Object: `CanApplyToInanimate`


**Definition:** An object containing effects that can be applied to inanimate objects.  
**Total Count:** 15

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional_notboss), [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional_object), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 10 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>tag |
| [`BreakIntoRocks`](../Reference_and_Meta/Enums.md#enum-breakintorocks) | Enum | Specifies the type of rock (e.g., 'Coin', 'SmallRock') to spawn when breaking an inanimate object. | 4 | `Coin`<br>`SmallRock` |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 3 | `{ . . . }` |
| `Vaporize` | `Number` | Removes the target from play, preventing its corpse from being interacted with. | 3 | `1`<br>`20` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 3 | Default<br>FormChange<br>Druid |
| `GetAggroTarget` | Integer | The number of aggro targets to acquire. | 2 | `1` |
| [`Temporary`](./Abilities_and_Spells.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 1 | `{ . . . }` |
| `PreventDeathTransforms` | Integer | Number of death transforms prevented for non-boss characters. | 1 | `1` |

</details>


---


### Object: `BackflipWhenTargeted`


**Definition:** The number of backflip charges, or an object defining its ability.  
**Total Count:** 15

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `ApplyToSourceOnKill`


**Definition:** Contains effects that are applied to the source when it kills the target.  
**Total Count:** 15

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 4 | Default<br>FormChange<br>Druid |
| `RemoveItem` | `String` | Specifies the item ID to remove from the source on kill. | 3 | `BlackShard`<br>`BlackShard_Glowing`<br>`ScaldingOrb` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `HealthGain` | Integer | The amount of health restored to the source. | 2 | `1`<br>`10`<br>`2` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 2 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `Revive` | Integer | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `1`<br>`100%`<br>`50%` |
| `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 2 | `1` |
| `CompleteItemQuest` | `String` | Specifies the item quest ID to mark as complete on kill. | 2 | `BlackShard`<br>`Nuke`<br>`ScaldingOrb` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `TakeExtraTurn` | `Number` | The number of extra turns granted to the source. | 1 | `1` |
| `EvolveAbilityFromPool` | `String` | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 1 | `Butcher`<br>`Druid`<br>`Fighter` |
| `RefreshActPoints` | `Number` | The amount of action points restored to the source. | 1 | `1` |
| [`TransformWeapon`](./Abilities_and_Spells.md#object-transformweapon) | Object  | An object with `from` and `to` fields specifying the weapon transformation. | 1 | `{ . . . }` |
| `WeaponAuxMultiplier` | Float | A multiplier string (e.g., '.5') for the weapon's auxiliary counter on kill. | 1 | `.5` |

</details>


---


### Object: `UseAbility`


**Definition:** The name of the ability the target is forced to use.  
**Total Count:** 14

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `respect_prime` | Boolean | If true, the ability will only be used if the unit is primed for it. | 1 | `true` |

</details>


---


### Object: `Conditional_NotBoss`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>
### Object: `SpreadDisease`


**Definition:** Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target.  
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`disease`](../Reference_and_Meta/Enums.md#enum-disease) | Enum | Determines which disease is applied when spreading disease. | 1 | `BirdFlu`<br>`Cancer`<br>`CommonCold` |

</details>


---


### Object: `ApplyPassives`


**Definition:** Specifies the passives or status effects to apply to the unit.  
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_RandomChance`](./Abilities_and_Spells.md#object-conditional_randomchance), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 10 | passives<br>class<br>tag |
| [`StatusOnBattleEnd`](./Abilities_and_Spells.md#object-statusonbattleend) | Object  | An object containing status effects or passives applied to the unit when the battle ends. | 3 | `{ . . . }` |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 2 | `1` |
| `IgnoreTiles` | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 2 | `1` |
| [`AddTag`](../Reference_and_Meta/Enums.md#enum-addtag) | Enum  | Specifies a gameplay tag (e.g., 'rock', 'plant') to add to the unit, used for interaction checks. | 2 | `bug`<br>`cat`<br>`fetus` |
| `YOffset` | Float | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 2 | `-.18`<br>`.25`<br>`.35` |
| [`ElementImmune`](../Reference_and_Meta/Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 1 | `Creep`<br>`Electric`<br>`Fire` |
| [`ReplaceBasicAttack`](../Reference_and_Meta/Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 1 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| `KnockbackImmunity` | Integer | If set to 1, the unit cannot be knocked back. | 1 | `1` |
| `Plant` | Integer | If set to 1, marks the unit as a Plant type, granting associated immunities and interactions. | 1 | `1` |

</details>


---


### Object: `DoScreenShake`


**Definition:** If an integer, the number of screen shakes; if an object, defines the duration and intensity of the screen shake.  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#object-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intensity` | Integer | The strength of the screen shake effect; positive values shake more, negative values may invert direction. | 10 | `-1`<br>`-2`<br>`1` |
| `time` | Float | The duration in seconds of the screen shake effect. | 10 | `.5`<br>`.75`<br>`1` |

</details>


---


### Object: `Conditional_Speculative`


**Definition:** Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts.  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_AffectedByElement`](./Abilities_and_Spells.md#object-conditional_affectedbyelement), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `IgnoreDamage` | `Number` | If set, the target ignores all damage for the duration. | 3 | `1` |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 2 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 2 | Default<br>FormChange<br>Druid |
| `BonusDamageBasedOnDistance` | `Number` | The flat bonus damage added per tile of distance between the source and target. | 2 | `1` |
| [`Else`](./Abilities_and_Spells.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| `Knockback` | Equation | The number of tiles the target is pushed away from the source on hit. | 1 | `1`<br>`10`<br>`2` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 1 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `CapDamage` | `Number` | The maximum amount of damage dealt, capping the total after all modifiers are applied. | 1 | `1` |
| `RandomBonusDamage` | `Number` | The maximum random bonus damage added to the base damage; the actual bonus is a random value between 0 and this number. | 1 | `25` |

</details>


---


### Object: `GainCoinsRange`


**Definition:** An object with `min` and `max` fields specifying a range for the amount of coins gained.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 4 | `10`<br>`2`<br>`25` |
| `min` | Integer | The minimum amount of coins that will be gained. | 4 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `ForceAttack`


**Definition:** If set to 1, forces the target to perform an attack against a random or specified target.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 2 | `false`<br>`true` |

</details>


---


### Object: `Conditional_Corpse`


**Definition:** Contains an inner effect block that only executes if the target is a corpse.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Revive` | Integer | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 4 | `1`<br>`100%`<br>`50%` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy) | Object  | An object containing status effects or actions applied only if the target is an enemy. | 1 | `{ . . . }` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 1 | `1` |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. | 1 | `1` |
| `FlatAIBonus` | `Number` | A flat adjustment to the AI's evaluation score for this action; positive values encourage the AI to use it, negative values discourage it. | 1 | `-999999`<br>`100`<br>`999999` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |
| `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 0 | `1` |

</details>


---


### Object: `ChanceToBreakFree`


**Definition:** Defines the chance and ability used for a grappled or restrained unit to break free.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 11 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`fail_ability`](../Reference_and_Meta/Enums.md#enum-fail_ability) | Enum | Specifies the ability to be used when the parent condition (e.g., breaking free) fails. | 3 | `CHuskDropFail`<br>`LennyStruggleFail`<br>`XXX` |

</details>


---


### Object: `Tangled`


**Definition:** The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`alt_art`](../Reference_and_Meta/Enums.md#enum-alt_art) | Enum | Specifies an alternative art asset name to use for the status. | 1 | `TangledMeat` |

</details>


---


### Object: `Conditional_FormulaIsPositive`


**Definition:** Defines effects that apply only if a given formula evaluates to a positive value.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 8 | Default<br>FormChange<br>Druid |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 2 | `1`<br>`10`<br>`2` |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Immobile`](../Reference_and_Meta/Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 2 | `0`<br>`1`<br>`10%` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` | [`formula`](../Engine_Scripts_and_Logic/Math_Equations.md) | Equation | A mathematical expression evaluated to determine if its result is positive, enabling the parent conditional. | 1 | passives<br>class<br>tag |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| `Slow` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 1 | `-1`<br>`1`<br>`2` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .01]` |
| `OverrideKnockbackDamage` | `String` | A formula or flat value that sets the damage dealt when knockback occurs, overriding default calculations. | 1 | `"max(5+bonus_melee_ability_damage, 1)"`<br>`0`<br>`2` |

</details>


---


### Object: `Conditional_FormulaIsPositive`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>
### Object: `AutocastEachRound`


**Definition:** Contains an ability name and optional 'even_if_stunned' flag to autocast each round.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 1 | `true` |

</details>


---


### Object: `ApplyStatusIfCrit`


**Definition:** Defines effects that are applied only when the attack scores a critical hit.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 | `Default`<br>`FormChange`<br>`Druid` | [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 3 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 3 | `1`<br>`10`<br>`2` |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |

</details>


---


### Object: `SmartMetronome`


**Definition:** The number of stacks of a buff that increases damage by a percentage, with an optional upgrade flag.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 1 | `true` |

</details>


---


### Object: `ScatterCoins`


**Definition:** The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#object-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `stackable` | Boolean | If true, the scatter coins effect can stack with multiple applications. | 2 | `true` |

</details>


---


### Object: `ConjureBonusAbility`


**Definition:** Specifies the name of the bonus ability to conjure.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 2 | `true` |

</details>


---


### Object: `Conditional_FirstApplicationThisTurn`


**Definition:** Container for effects applied only on the first application of this ability during the turn.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 3 | Default<br>FormChange<br>Druid |
| [`key`](../Reference_and_Meta/Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 3 | `EtherSoakedRag`<br>`JewelOfDrog`<br>`TaintedOffering` |
| [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#object-temppassivewhilehasstatus) | Object  | An object defining passives temporarily granted to the unit while it has a specific status effect. | 3 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |

</details>


---


### Object: `Conditional_BadRoll`


**Definition:** An object containing an `odds` value and effects that are applied when a random roll succeeds.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 2 | Default<br>FormChange<br>Druid |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 2 | `.1`<br>`.16666666`<br>`.3` |
| `Instakill` | `Number` | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 1 | `25`<br>`50`<br>`999` |
| `DieViolently` | `Number` | If true, causes the target to die with a violent, explosive visual effect. | 1 | `1` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `BodyGuard`


**Definition:** An object that applies a bodyguard status, optionally linking to a swap ability.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `SwitchMusic`


**Definition:** Defines a new song or layer for the background music.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#object-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`new_layer`](../Reference_and_Meta/Enums.md#enum-new_layer) | Enum | Specifies the music layer to switch to (e.g., 'event', 'battle', 'map'). | 6 | `battle`<br>`event`<br>`map` |
| [`new_song`](../Reference_and_Meta/Enums.md#enum-new_song) | Enum | Specifies the song to switch to; 'same' keeps the current song playing on the new layer. | 5 | `same` |
| `crossfade_speed` | Integer | The duration in seconds for the crossfade transition between music tracks. | 1 | `1` |

</details>


---


### Object: `ObjectOnHit`


**Definition:** Specifies the object to spawn on the hit tile.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `LowerAmbientLight`


**Definition:** If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CreateGlobalModifiers`](./Abilities_and_Spells.md#object-createglobalmodifiers)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `speed` | Array / Float  | The speed of the projectile or move, can be a value or a range. | 2 | `-30`<br>`-4`<br>`.5` |
| `amount` | Array / Float | For ambient light, the target brightness value (as a float or percentage array for RGB). | 2 | `.1`<br>`.25`<br>`.35` |

</details>


---


### Object: `DoDamage`


**Definition:** Contains damage parameters (amount, type, tile targets) to deal damage to the target.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`Else`](./Abilities_and_Spells.md#object-else), [`post_spawn_statuses`](./Abilities_and_Spells.md#object-post_spawn_statuses)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | passives<br>class<br>tag |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 5 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`damage`](./Abilities_and_Spells.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 5 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 5 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2 | `{ . . . }` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 2 | `[`<br>`[Heat Fire]` |
| [`damage_tiles`](../Reference_and_Meta/Enums.md#enum-damage_tiles) | Enum | Specifies whether the damage effect applies to tiles; 'all' damages every tile in the area. | 2 | `all` |

</details>


---


### Object: `Conditional_PlayerCat`


**Definition:** Defines effects that only apply if the target is a player-controlled cat.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ConjureRandomAbilityFromCat` | `Number` | The number of random abilities created or given to the cat unit from a pool of cat-themed abilities. | 2 | `1` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `Cleanse` | Integer | The number of stacks of negative status effects removed from the target. | 1 | `0`<br>`1` |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 1 | `{ . . . }` |
| `GenericDebuff` | `Number` | The number of stacks of a generic, untooltipped debuff applied to the target. | 1 | `1`<br>`10`<br>`100` |
| `Scrambled` | Integer | The number of stacks of Scrambled applied. | 1 | `1`<br>`2` |
| `Adrenaline` | Integer | The flat amount of Adrenaline (a resource or stat) granted to the unit. | 1 | `10` |
| `KnockOutClone` | `String` | Specifies the ability ID used to knock out or remove the player's clone unit from battle. | 1 | `PlayerCat_MiniMiniMe` |
| `T2CopyCat` | `Number` | The number of T2 Clone copies created or applied to the target cat. | 1 | `1` |

</details>


---


### Object: `Conditional_InForm`


**Definition:** Contains effects that apply only if the target is in the specified form.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#object-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form`](../Reference_and_Meta/Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 7 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 7 | Default<br>FormChange<br>Druid |
| `FormChange` | `String` | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 5 | `Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 1 | `1`<br>`10`<br>`100` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 1 | `1`<br>`10`<br>`100` |
| `UseAbility` | `String` | The name of the ability the target is forced to use. | 1 | `GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| [`ForceImmediateMoveAndAttack`](./Abilities_and_Spells.md#object-forceimmediatemoveandattack) | Object  | An object that forces the unit to instantly move toward the target and perform a specified ability attack. | 1 | `{ . . . }` |

</details>


---


### Object: `Conditional_HealthThreshold`


**Definition:** Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional_notboss), [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional_speculative), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 6 | Default<br>FormChange<br>Druid |
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 4 | `0`<br>`10`<br>`3` |
| `SpawnThingIfHitKills` | `String` | The name of the thing (e.g., a food type) to spawn at the target's location upon a killing blow. | 2 | `Bait`<br>`BigFood`<br>`BiggestFood` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `threshold_percent` | Integer | The percentage of max health below which the target must be for the conditional to trigger. | 2 | `25%`<br>`50%` |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 1 | `{ . . . }` |
| `Vaporize` | `Number` | Removes the target from play, preventing its corpse from being interacted with. | 1 | `1`<br>`20` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 1 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| `FullHeal` | `Number` | If non-zero, fully restores the target's health. | 1 | `0`<br>`1` |
| `Instakill` | `Number` | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 1 | `25`<br>`50`<br>`999` |
| `Die` | `Number` | If set, kills the target immediately. | 1 | `1`<br>`6` |
| `FlatLeech` | `Number` | The flat amount of health restored to the source when dealing damage, applied after the hit. | 1 | `1`<br>`10`<br>`2` |
| `CaptureFamiliar` | `Number` | The number of times to attempt to capture the target as a familiar. | 1 | `1` |
| `FactionConversion` | `Number` | Converts the target to the caster's faction. | 1 | `1` |
| `DieViolently` | `Number` | If true, causes the target to die with a violent, explosive visual effect. | 1 | `1` |
| `threshold_expr` | Equation | A mathematical expression whose result is used as the dynamic health threshold for the conditional. | 1 | `item_aux` |

</details>


---


### Object: `AfterImage`


**Definition:** Specifies the object or skill used to create an afterimage of the unit.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#object-temporary_effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `skilltemp` | Boolean | If true, the afterimage is treated as a skill temporary effect. | 2 | `true` |

</details>


---


### Object: `TwisterDisplaceWithDamage`


**Definition:** Configuration for a twister displacement that deals damage, with min/max distance and damage value.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Abilities_and_Spells.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 6 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `max_dist` | Integer | The maximum distance in tiles the target can be displaced by the knockback effect. | 6 | `2`<br>`20`<br>`3` |
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 2 | `2`<br>`3`<br>`4` |
| [`exclude_prefix`](../Reference_and_Meta/Enums.md#enum-exclude_prefix) | Enum | Specifies a prefix string; units with a matching prefix in their ID are excluded from the displacement effect. | 1 | `Twister` |

</details>


---


### Object: `TeamCastAbility`


**Definition:** Specifies the ability name for the team to cast, with optional tag restriction and same orientation.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`tag_restriction`](../Reference_and_Meta/Enums.md#enum-tag_restriction) | Enum | Specifies a tag that the target unit must have for the team cast to trigger. | 2 | `collective`<br>`dc_cat`<br>`dinofamily` |
| `same_orientation` | Boolean | If true, the team cast ability only triggers if the caster and target face the same direction. | 1 | `true` |

</details>


---


### Object: `StatusGroup`


**Definition:** A container grouping multiple status effects to be applied simultaneously.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .01]` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `DamageOrHealConditionally` | Integer | The amount of conditional damage or healing applied, based on certain conditions (e.g., ally or enemy). | 2 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `ReviveNextRound`


**Definition:** The number of revives granted, or an object defining revive properties.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#object-additional_passives), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `revive_health` | Integer | The amount of health (as a flat integer or percentage) the unit revives with. | 3 | `1`<br>`100%`<br>`50%` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `PopAndSpawn`


**Definition:** The object (enemy or entity) to spawn on the target's tile, optionally with visual effects.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `no_splatter` | Boolean | If true, prevents the blood splatter visual effect from appearing when the object spawns or is popped. | 1 | `false`<br>`true` |
| `clone_items` | Boolean | If true, the spawned unit clones the items of the original unit. | 1 | `false`<br>`true` |
| `clone_referenced_catdata` | Boolean | If true, the spawned unit is a clone of the referenced cat data, including its stats and equipment. | 1 | `true` |

</details>


---


### Object: `Math`


**Definition:** An object containing a `stacks` value that determines how many times the nested effects are applied.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 1 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `DoDistortionRing`


**Definition:** Configuration for a distortion ring visual effect, with speed, intensity, and radius.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `speed` | Array / Float  | The speed of the projectile or move, can be a value or a range. | 6 | `-30`<br>`-4`<br>`.5` |
| `intensity` | Integer | The strength of the screen shake effect; positive values shake more, negative values may invert direction. | 6 | `-1`<br>`-2`<br>`1` |
| [`radius`](../Reference_and_Meta/Arrays.md#array-radius) | Array / Integer  | The range in tiles of the distortion ring effect; an array [min, max] specifies a random radius within that range. | 6 | `0`<br>`1`<br>`13` |

</details>


---


### Object: `DestroyEquipmentAndAttachParasite`


**Definition:** Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_ActiveWeather_Any`](./Abilities_and_Spells.md#object-conditional_activeweather_any), [`Conditional_DebuffRoll`](./Abilities_and_Spells.md#object-conditional_debuffroll), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `Conditional_Object`


**Definition:** Evaluates whether the target is an object (vs a character); if true, applies the effects within; otherwise, runs the Else block.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Else`](./Abilities_and_Spells.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 3 | `{ . . . }` |
| [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 3 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 3 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate) | Object  | An object containing effects that can be applied to inanimate objects. | 1 | `{ . . . }` |
| `RepairWeapon` | Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 1 | `1`<br>`6`<br>`99` |

</details>


---


### Object: `Conditional_IsSelf`


**Definition:** An object containing effects that are only applied if the target is the source unit itself.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 1 | `-10`<br>`0`<br>`1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `TakeBonusTurnWithStatus`


**Definition:** Container for status effects applied when taking a bonus turn.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| [`Madness`](./Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `TempNoManaRegen` | Integer | The number of turns the unit cannot regenerate mana. | 2 | `1` |
| [`Confusion`](../Reference_and_Meta/Arrays.md#array-confusion) | Array / Integer  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `LeaveBehind`


**Definition:** Specifies the object or entity to spawn after the unit leaves a tile.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#object-temporary_effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `KnockOutCoin`


**Definition:** The number of coins knocked out, with an optional probability or an object with stacks and chance.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `CreateGlobalModifiers`


**Definition:** Defines global gameplay modifiers to activate.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#object-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Global Modifier Keys}`](../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md#valid-property-keys) | Variable | If true, activates a global modifier effect on the house environment. | 2 | `CreateGlobalModifiers`<br>`BloodRain`<br>`NextPlayerCatTakesExtraTurn` |
| `BloodRain` | Integer | If non-zero, enables the blood rain visual effect. | 2 | `1` |
| [`LowerAmbientLight`](./Abilities_and_Spells.md#object-lowerambientlight) | Object  | If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly. | 2 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag`

</details>


---


### Object: `Conditional_Shielded`


**Definition:** An object containing effects that are only applied if the target has a shield active.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `CollectsPickupsWithAltEffects`


**Definition:** Contains alternative effects that are applied when collecting pickups.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | `1`<br>`3` |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `RandomStatUp` | Enum / Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |
| `Quivered` | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`5` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `CurrentWeaponAddPoison` | Integer | The number of poison stacks added to the target's current weapon; an integer value applies that many stacks. | 2 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `WaggleClone`


**Definition:** Defines a waggle clone ability with health thresholds and object sizes.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`cWaggle`](./Abilities_and_Spells.md#object-cwaggle) | Object  | Defines a clone variant of the Waggle unit with its own graphics and properties. | 1 | `{ . . . }` |
| [`cWaggle2x2`](./Abilities_and_Spells.md#object-cwaggle2x2) | Object  | Defines a larger 2x2 tile clone variant of the Waggle unit. | 1 | `{ . . . }` |
| [`cWaggle3x3`](./Abilities_and_Spells.md#object-cwaggle3x3) | Object  | Defines an even larger 3x3 tile clone variant of the Waggle unit. | 1 | `{ . . . }` |

</details>


---


### Object: `TimeDelayStatusApplication`


**Definition:** Container for status effects applied after a specified delay.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 4 | `.05`<br>`.1`<br>`.25` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`SwitchMusic`](./Abilities_and_Spells.md#object-switchmusic) | Object  | Defines a new song or layer for the background music. | 2 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 2 | Default<br>FormChange<br>Druid |
| `FormChange` | `String` | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 1 | `Big`<br>`BigHolding`<br>`BigHoldingCat` |
| `Cleanse` | Integer | The number of stacks of negative status effects removed from the target. | 1 | `0`<br>`1` |
| `Vaporize` | `Number` | Removes the target from play, preventing its corpse from being interacted with. | 1 | `1`<br>`20` |
| `FullHeal` | `Number` | If non-zero, fully restores the target's health. | 1 | `0`<br>`1` |
| [`DoScreenShake`](./Abilities_and_Spells.md#object-doscreenshake) | Integer / Object  | If an integer, the number of screen shakes; if an object, defines the duration and intensity of the screen shake. | 1 | `{ . . . }`<br>`1` |
| `PlayBackground` | `Number` | Specifies the background index to play. | 1 | `0`<br>`1` |
| [`CreateGlobalModifiers`](./Abilities_and_Spells.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. | 1 | `{ . . . }` |
| `GlobalSpawnCharacter` | `String` | Specifies the name of a character to spawn globally. | 1 | `MegaGuppy` |
| `RemoveAmbientLightEffects` | Float | The fade-out duration in seconds for ambient light effects. | 1 | `.5`<br>`4` |

</details>


---


### Object: `TempPassiveWhileHasStatus`


**Definition:** An object defining passives temporarily granted to the unit while it has a specific status effect.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_FirstApplicationThisTurn`](./Abilities_and_Spells.md#object-conditional_firstapplicationthisturn), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#object-conditional_livingplayercat)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ReplaceSpell`](./Abilities_and_Spells.md#object-replacespell) | Object  | Defines which spell slot to replace and with which ability. | 4 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 3 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`MeleeRevengeDamage`](./Abilities_and_Spells.md#object-meleerevengedamage) | Object  | Defines the damage and effects applied back to a melee attacker upon being hit. | 2 | `{ . . . }` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |
| `AddManaRegen` | Integer | The flat amount of mana regenerated per turn. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `rocket_swirl`


**Definition:** An object defining the spiral rotation parameters for a rocket-style projectile.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#object-graphics)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `speed` | Array / Float  | The speed of the projectile or move, can be a value or a range. | 4 | `-30`<br>`-4`<br>`.5` |
| [`radius`](../Reference_and_Meta/Arrays.md#array-radius) | Array / Integer | The range in tiles of the distortion ring effect; an array [min, max] specifies a random radius within that range. | 4 | `0`<br>`1`<br>`13` |

</details>


---


### Object: `ReplaceSpell`


**Definition:** Defines which spell slot to replace and with which ability.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#object-temppassivewhilehasstatus)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `slot` | Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 4 | `0`<br>`1`<br>`2` |

</details>


---


### Object: `RemoveStatusStacks`


**Definition:** An object specifying a status name and the number of stacks to remove from the target.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |

</details>


---


### Object: `RandomDistanceDisplace`


**Definition:** The number of stacks of a random distance displacement effect, or an object with stacks, min_dist, and chance.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 1 | `2`<br>`3`<br>`4` |

</details>


---


### Object: `post_spawn_statuses`


**Definition:** Status effects applied to the spawned unit immediately after it appears.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#object-spawn)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 3 | Default<br>FormChange<br>Druid |
| [`DoDamage`](./Abilities_and_Spells.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 2 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `VisualFXTile` | `String` | Specifies the name of the visual effect to play on the target tile. | 1 | `Bolt`<br>`BurnTrigger`<br>`Explosion` |
| `EnterMount` | `String` | Specifies the name of the mount status to apply to the unit. | 1 | `enter` |

</details>


---


### Object: `LateStatusApplication`


**Definition:** Container for status effects that are applied late after the main effect.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `LateStatusApplication`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `extra_statuses`


**Definition:** An object containing additional status effects (with stack counts) applied to the consumed unit.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Consumed`](./Abilities_and_Spells.md#object-consumed)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`Tarred`](../Reference_and_Meta/Arrays.md#array-tarred) | Array / Integer  | The amount of tarred stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .1]` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 2 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_RandomChance`


**Definition:** An object containing effects that execute only if a random roll succeeds, with an odds value defined inside.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 1 | `.1`<br>`.16666666`<br>`.3` |
| [`ApplyPassives`](./Abilities_and_Spells.md#object-applypassives) | Object  | Specifies the passives or status effects to apply to the unit. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `Conditional_OncePerBattle`


**Definition:** An object containing effects that can only trigger once per battle, preventing double-activation.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 2 | Default<br>FormChange<br>Druid |
| [`key`](../Reference_and_Meta/Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 2 | `EtherSoakedRag`<br>`JewelOfDrog`<br>`TaintedOffering` |
| `CompleteItemQuest` | `String` | Specifies the item quest ID to mark as complete on kill. | 2 | `BlackShard`<br>`Nuke`<br>`ScaldingOrb` |
| `TriggerGameEnding` | `Number` | If set to 1, triggers the game's ending sequence; 0 disables it. | 2 | `0`<br>`1` |

</details>


---


### Object: `Conditional_Familiar`


**Definition:** Container for effects applied if the unit has a familiar, with an optional Else block.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 1 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `ArcLightning`


**Definition:** Configuration for arc lightning chain, with stacks, chance, max distance, and enemy-only flag.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 4 | `false`<br>`true` |
| `max_distance` | Integer | The maximum range in tiles for the arc lightning to chain to subsequent targets. | 4 | `1`<br>`2`<br>`3` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| `ignore_self` | Boolean | If true, the arc lightning effect does not chain to or affect the source unit itself. | 1 | `true` |

</details>


---


### Object: `ApplyToConsumed`


**Definition:** Container for effects that are applied to the consumed object.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DeleteObject` | `Number` | If set, deletes the target object from the map. | 3 | `1` |
| `Die` | `Number` | If set, kills the target immediately. | 1 | `1`<br>`6` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `TakeBonusTurnWithAIControl`


**Definition:** An object configuring whether the bonus turn happens at the end of the round and whether spells are included.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | If true, the AI-controlled bonus turn includes spells as available actions. | 2 | `true` |

</details>


---


### Object: `StatusKillers`


**Definition:** An object containing nested conditionals that apply status effects when the unit kills an enemy.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `SetCrazyEyeBackgroundWeights`


**Definition:** An object containing a `weights` array that sets the weighting for which Crazy Eye background variant is displayed.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](../Reference_and_Meta/Arrays.md#array-weights) | Array / Enum | Specifies the weight array or named preset for the crazy eye background AI. | 3 | `[0 0 1]`<br>`[0 1 0]`<br>`[1 0 0]` |

</details>


---


### Object: `NextBasicAttackCritsThisTurn`


**Definition:** An object or number configuring the next basic attack to be a critical hit this turn. An object may contain stack, cant_miss, or piercing sub-keys.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target regardless of accuracy or evasion. | 1 | `true` |
| `piercing` | `Boolean` | If true, the damage instance ignores armor or damage reduction effects on the target. | 1 | `true` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1 | `damage_instance`<br>`spell`<br>`self_damage` |

</details>


---


### Object: `IncAuxCounterClamped`


**Definition:** An object with `change` and `max` properties modifying the auxiliary counter by `change`, clamped to `max`.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 3 | `10`<br>`2`<br>`25` |
| `change` | Integer | The amount to adjust the auxiliary counter by. | 3 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `DybbukPossessed`


**Definition:** Contains parameters for the Dybbuk possession status, specifying exit ability and self-punch ability.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit_ability`](../Reference_and_Meta/Enums.md#enum-exit_ability) | Enum | Determines the ability used when the Dybbuk possession ends. | 1 | `DybbukReturn` |
| [`punch_self_ability`](../Reference_and_Meta/Enums.md#enum-punch_self_ability) | Enum | Determines the ability used for the possessed unit to attack itself. | 1 | `Dybbuk_StopHittingYourself` |

</details>


---


### Object: `DustOnHit`


**Definition:** Configuration for a dust object spawned on hit.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `cWaggle2x2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `cWaggle`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `Conditional_LastHit`


**Definition:** Container for effects applied only on the final hit of a multi-hit attack, with optional Else block.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 2 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 2 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`Bruise`](../Reference_and_Meta/Arrays.md#array-bruise) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 1 | `1`<br>`2`<br>`3` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 1 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| `DelayCastAbility` | `String` | Specifies the name of an ability to cast after a delay. | 1 | `HitlerNuke` |

</details>


---


### Object: `Conditional_AffectedByElement`


**Definition:** Container for effects applied if the target is affected by a specified element, with optional Else block.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 3 | `Electric`<br>`Fire`<br>`Gravity` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `BonusCritChance` | Integer | The flat percentage increase to critical hit chance. | 2 | `100`<br>`25`<br>`50` |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional_speculative) | Object  | Evaluates AI-only speculative conditions (like health thresholds) without affecting the main action in PvP or direct casts. | 1 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `CatPartsSizeScaleStatus`


**Definition:** Configures scale multipliers for individual cat body parts (body, arms, mouth).  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `ApplyToRandomPartyMemberIfPossible`


**Definition:** Contains an inner effect block that is applied to a random living party member if one exists.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional_goodroll), [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GainDisorderFromPool_PostCast` | `String` | Specifies the pool of disorders the unit can gain after the spell is cast. | 2 | `forbidden_spell_consequences`<br>`forbidden_spell_consequences_crippling` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `ApplyMultipleTimes`


**Definition:** An object containing a `stacks` value that specifies how many times the nested effects are applied.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `stacks` | Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 3 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `XIsTargetHealth`


**Definition:** Evaluates a bonus damage formula where X is the target's current health.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional_boss), [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `XIsTargetHealth`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


### Object: `XIsSpellStormRampAndReset`


**Definition:** If integer 0, resets stacks; if object, contains 'stacks' and 'reset_percent' for spell storm ramp.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `reset_percent` | Integer | The percentage of the ramp-up value to reset to upon casting. | 1 | `50%` |

</details>


---


### Object: `TransformWeapon`


**Definition:** An object with `from` and `to` fields specifying the weapon transformation.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#object-applytosourceonkill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`to`](../Reference_and_Meta/Enums.md#enum-to) | Enum | Specifies the target equipment item after transformation. | 1 | `JarOfNothing`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |
| [`from`](../Reference_and_Meta/Enums.md#enum-from) | Enum | Specifies the source equipment item to be transformed. | 1 | `JarOfChaos`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |

</details>


---


### Object: `TransformEquipment`


**Definition:** Defines an equipment transformation from one item to another, with 'from' and 'to' sub-keys.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`to`](../Reference_and_Meta/Enums.md#enum-to) | Enum | Specifies the target equipment item after transformation. | 1 | `JarOfNothing`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |
| [`from`](../Reference_and_Meta/Enums.md#enum-from) | Enum | Specifies the source equipment item to be transformed. | 1 | `JarOfChaos`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |

</details>


---


### Object: `RandomKnockback`


**Definition:** An object defining the minimum and maximum distance in tiles for a random knockback.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 2 | `10`<br>`2`<br>`25` |
| `min` | Integer | The minimum amount of coins that will be gained. | 2 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `QuakeAreaChance`


**Definition:** An object containing a radius and a chance to trigger a quake area effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |
| [`radius`](../Reference_and_Meta/Arrays.md#array-radius) | Array / Integer  | The range in tiles of the distortion ring effect; an array [min, max] specifies a random radius within that range. | 2 | `0`<br>`1`<br>`13` |

</details>


---


### Object: `OverHealToStatuses`


**Definition:** Specifies a set of statuses applied to the target based on the amount of over-healing dealt.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomStatUp` | Enum / Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 1 | `1` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `stack_scale` | Integer | The scaling factor for how many stacks of the over-heal status are applied. | 1 | `0` |

</details>


---


### Object: `NukeQuestFinalBossModifications`


**Definition:** Contains modifications for the nuke quest final boss, such as damage_instance effects.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](./Abilities_and_Spells.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 2 | `{ . . . }` |
| [`damage_instance`](./Abilities_and_Spells.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`splash_damage`](./Abilities_and_Spells.md#object-splash_damage) | Object  | Defines additional damage or effects applied to nearby targets around the primary target. | 1 | `{ . . . }` |

</details>


---


### Object: `NextAttackSpecialCrit`


**Definition:** The number of charges for a special crit on the next attack, or an object defining its bonus properties.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Integer | The additional critical hit damage multiplier. | 1 | `2` |
| `extra_coins_per_stack` | Integer | The number of extra coins gained per stack of the associated status. | 1 | `2` |
| `luck_increase` | Integer | The flat increase to the unit's luck stat. | 1 | `1` |

</details>


---


### Object: `ForceMoveTowardsTaggedObject`


**Definition:** An object specifying the `ability` and optional `tag` used to forcibly move the unit towards a tagged object.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `empty_self_damage`


**Definition:** Defines self-damage or effects when the ability is used with no target (empty).  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2 | `{ . . . }` |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 2 | `damage_instance`<br>`spell`<br>`self_damage` |

</details>


---


### Object: `DelayedWindCone`


**Definition:** An object containing parameters for a delayed wind cone, such as damage and distance.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Abilities_and_Spells.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 1 | `-3`<br>`10`<br>`2` |

</details>


---


### Object: `DelayCastAbility`


**Definition:** Specifies the name of an ability to cast after a delay.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `lingering` | Boolean | If true, the ability effect lingers after the initial cast. | 1 | `true` |
| `relative` | Boolean | If true, the delay is calculated relative to the current turn count rather than as an absolute time. | 1 | `false` |

</details>


---


### Object: `cWaggle3x3`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>
### Object: `CopySpells`


**Definition:** The number of spells copied from the target, or an object specifying `stacks` and whether the copy is `upgraded`.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 1 | `true` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `Conditional_Shielded`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `Conditional_OncePerBattle`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>
### Object: `Conditional_NotShielded`


**Definition:** An object containing effects that are only applied if the target does not have a shield active.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Knockback` | Equation | The number of tiles the target is pushed away from the source on hit. | 2 | `1`<br>`10`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_NotBossOrBig`


**Definition:** An object containing effects that are only applied if the target is not a boss or large unit.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_NotBossOrBig`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `Conditional_NotAlly`


**Definition:** An object containing effects that are only applied if the target is not an ally of the source.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](../Reference_and_Meta/Arrays.md#array-confusion) | Array / Integer  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`Temporary`](./Abilities_and_Spells.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `Conditional_IsSelf`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `Conditional_HasCleansableDebuffs`


**Definition:** An object containing effects that execute only if the unit has cleansable debuffs.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 1 | `{ . . . }` |
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. | 1 | `1`<br>`9999` |
| `GenericBuff` | `Number` | A generic buff value applied to the unit. | 1 | `100`<br>`5` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_Displaceable`


**Definition:** Contains an inner effect block that only executes if the target can be displaced (knocked back).  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` | `LaunchOffScreen` | String | A formula string that determines the knockback force to launch the unit off-screen. | 1 | passives<br>class<br>tag |
| `TempInitiativeChange` | Integer | The flat change to the unit's initiative value. | 1 | `-100`<br>`-999`<br>`100` |
| `LaunchOffScreenInstakill` | Integer | If non-zero, the unit is instantly killed and launched off-screen. | 1 | `1` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_Displaceable`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>
### Object: `Conditional_DestructibleCorpse`


**Definition:** An object containing effects that are only applied if the corpse is destructible.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `VaporizeCorpse` | `Number` | If set, vaporizes the target's corpse, preventing revival. | 2 | `1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>tag |
| [`ApplyToTile`](./Abilities_and_Spells.md#object-applytotile) | Object  | Defines effects to apply to the target tile. | 2 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_DestructibleCorpse`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>
### Object: `Conditional_Buddy`


**Definition:** An object containing effects that are only applied if the caster has a buddy (follower) unit.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| [`Else`](./Abilities_and_Spells.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| [`Consumed`](./Abilities_and_Spells.md#object-consumed) | Object  | An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`. | 1 | `{ . . . }` |
| [`Conditional_InForm`](./Abilities_and_Spells.md#object-conditional_inform) | Object  | Contains effects that apply only if the target is in the specified form. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `Conditional_BossOrBig`


**Definition:** An object containing effects that are only applied if the target is a boss or large unit.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_BossOrBig`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `ApplyToTile`


**Definition:** Defines effects to apply to the target tile.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_DestructibleCorpse`](./Abilities_and_Spells.md#object-conditional_destructiblecorpse)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ObjectOnHit` | `String` | Specifies the object to spawn on the hit tile. | 2 | `Bait`<br>`BiggestFood`<br>`Carcus` |
| `SpawnBearTrap` | `Number` | If non-zero, spawns a bear trap on the tile. | 2 | `1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 2 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `ApplyToRandomPartyMemberIfPossible`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `VisualCountDownThenApplyStatus`


**Definition:** Contains a visual countdown sequence that culminates in applying a status effect, optionally forcing an ability use.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](../Reference_and_Meta/Enums.md#enum-forceuseability) | Enum  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `UseMoveAbilityWithAI`


**Definition:** Defines a move ability to execute with AI-controlled movement weights.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `SwapWeapon`


**Definition:** An object containing a "pool" array of weapon names to randomly swap to.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusKillers`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `ShowFakeDamage`


**Definition:** Displays a fake damage number (with optional style) for visual effect without actually changing health.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`style`](../Reference_and_Meta/Arrays.md#array-style) | Array | Specifies the visual styles (e.g., crit) used for the fake damage display. | 1 | `[crit]` |

</details>


---


### Object: `SetAnimationAlts`


**Definition:** Specifies alternative animation names for the target's dying and dead states.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dying`](../Reference_and_Meta/Enums.md#enum-dying) | Enum | Determines the animation set used when the unit is in a dying state. | 1 | `shot` |
| [`dead`](../Reference_and_Meta/Enums.md#enum-dead) | Enum  | Determines the animation set used when the unit is dead. | 1 | `deadShot` |

</details>


---


### Object: `ScrambleLastUsedSpell`


**Definition:** An object containing a "permanent" boolean. If true, permanently scrambles (randomizes) the last used spell.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `permanent` | Boolean | If true, the scrambled spell selection persists permanently rather than resetting after use. | 1 | `true` |

</details>


---


### Object: `PoolMetronome`


**Definition:** An object containing a "pool" array of ability names that the Metronome effect can randomly select from.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `PassiveWhileNotTakingTurn`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>
### Object: `PassiveWhileNotTakingTurn`


**Definition:** A nested passive object that is active only while the unit is not currently taking its turn.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `NextBattleStatusStacks`


**Definition:** An object specifying status effects and their stacks to be applied at the start of the next battle. Contains a "fights" counter and nested status keys.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | `Number` | The chance (as a multiplier) to inflict Madness status at the start of each turn in the next battle. | 1 | `2` |
| `fights` | Integer | The number of future battles the status effect will be applied at the start of. | 1 | `1`<br>`9999` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `MergeDamageInstance`


**Definition:** Specifies parameters to merge multiple damage instances into one, controlling hit animation and instant pop behavior.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `can_instapop` | `Boolean` | If false, the ability cannot instantly kill or remove the target, often used for non-lethal effects. | 1 | `false` |
| `force_no_hit_animation` | Boolean | If true, suppresses the hit animation when merging damage instances. | 1 | `true` |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1 | `damage_instance`<br>`spell`<br>`self_damage` |

</details>


---


### Object: `IncAuxCounterCycle`


**Definition:** An object containing parameters for incrementing an auxiliary counter with a change and maximum value.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 1 | `10`<br>`2`<br>`25` |
| `change` | Integer | The amount to adjust the auxiliary counter by. | 1 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `ForceImmediateMoveAndAttack`


**Definition:** An object that forces the unit to instantly move toward the target and perform a specified ability attack.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_InForm`](./Abilities_and_Spells.md#object-conditional_inform)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_cant_reach` | Boolean | If true, forces the unit to attempt to move and attack even if the target is not reachable. | 1 | `true` |

</details>


---


### Object: `damage_threshold_altanimations`


**Definition:** A mapping of damage threshold values to alternate animation names, triggering different animations based on damage dealt.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#object-graphics)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `heaviestMelee` | Integer | The minimum damage value to trigger the heaviest melee hit animation. | 1 | `20` |
| `heavyMelee` | Integer | The minimum damage value to trigger a heavy melee hit animation. | 1 | `10` |

</details>


---


### Object: `Conditional_SourceHasStatus`


**Definition:** An object containing effects that execute only if the source unit has the specified status.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`Bruise`](../Reference_and_Meta/Arrays.md#array-bruise) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 1 | `1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `Conditional_SourceAbilityHasTag`


**Definition:** An object containing effects that execute only if the source ability has the specified tag.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`tag`](../Reference_and_Meta/Enums.md#enum-tag) | Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 1 | `{ . . . }` |
| [`ScatterCoins`](./Abilities_and_Spells.md#object-scattercoins) | Object  | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 1 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `Conditional_NotBig`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `Conditional_NotBig`


**Definition:** An object containing effects that execute only if the target is not a 'big' unit.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DisplaceTowardsSource` | `Number` | If set, displaces the target towards the source of the effect. | 1 | `1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_LivingPlayerCat`


**Definition:** An object containing effects that execute only if the source is a living player-owned cat.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 1 | `{ . . . }` |
| [`Consumed`](./Abilities_and_Spells.md#object-consumed) | Object  | An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`. | 1 | `{ . . . }` |
| [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#object-temppassivewhilehasstatus) | Object  | An object defining passives temporarily granted to the unit while it has a specific status effect. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `Conditional_IsTrample`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `Conditional_IsTrample`


**Definition:** An object containing effects that execute only if the ability is a trample attack.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SetKnockback` | `Number` | The knockback distance to set for the damage instance, overriding default. | 1 | `0` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_FinishedSpawning`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `Conditional_FinishedSpawning`


**Definition:** Contains an inner effect block that only executes if the target has finished its spawning animation.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Imprison` | `String` | Specifies the type of unit or object to summon as a prison. | 1 | `BeefyCharmedLeech`<br>`CharmedLeech`<br>`Fly` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_DebuffRoll`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `Conditional_DebuffRoll`


**Definition:** An object containing effects that execute if a debuff roll succeeds, with an odds value defined inside.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 1 | `.1`<br>`.16666666`<br>`.3` |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#object-destroyequipmentandattachparasite) | Object  | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 1 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `Conditional_CanBeHealed`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>
### Object: `Conditional_CanBeHealed`


**Definition:** An object containing effects that execute only if the target can be healed.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_Backstab`


**Definition:** An object containing effects that execute only if the attack lands on the target's back.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| `BonusCritChance` | `Number` | The flat percentage increase to critical hit chance. | 1 | `100`<br>`25`<br>`50` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_ActiveWeather_Any`


**Definition:** An object containing effects that execute only if any of the specified weather types are active.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#object-destroyequipmentandattachparasite) | Object  | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 1 | `{ . . . }` |
| [`weather`](../Reference_and_Meta/Arrays.md#array-weather) | Array | Specifies one or more weather types to check for. | 1 | `[FlySwarm FireflySwarm ButterflySwarm]` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid` | [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `bonk_damage`


**Definition:** Defines damage and effects applied when a dash or move hits a wall or obstacle.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`damage`](./Abilities_and_Spells.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1 | `damage_instance`<br>`spell`<br>`self_damage` |

</details>


---


### Object: `ApplyToRandomClosestAlly`


**Definition:** Specifies statuses to apply to a random ally closest to the target.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | `Number` | The number of tiles to force the target to move toward the caster. | 1 | `1` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `ApplyToOthersWithSharedTagAndFaction`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `ApplyToOthersWithSharedTagAndFaction`


**Definition:** Specifies statuses to apply to other units that share a tag and faction with the target.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `ApplyStatusesNextTurnBegin`


**Definition:** Specifies a set of statuses to apply to the target at the beginning of their next turn.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Quivered` | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`5` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `ApplyPassivesToSpawnerWhileAlive`


**Definition:** An object defining passives that are applied to the spawner while this unit is alive.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#object-additional_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`HideEquipment`](../Reference_and_Meta/Enums.md#enum-hideequipment) | Enum  | Specifies which equipment slot is visually hidden. | 1 | `neck` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `AlphaStatusOnTurnBegin`


**Definition:** Specifies status effects applied to the alpha at the start of each turn.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DoubleCastSpellThisTurn` | Integer | If non-zero, grants the unit a double cast effect for spells this turn. | 1 | `1` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---

